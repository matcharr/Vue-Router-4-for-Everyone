<template>
  <a v-if="isExternal"
     :href="to"
     class="external-link"
     rel="noopener"
     target="_blank"
  >
    <slot/>
  </a>
  <router-link v-else class="internal-link" v-bind="$props">
    <slot/>
  </router-link>
</template>

<script>
import {RouterLink} from 'vue-router';

export default {
  name: "AppLink",
  props: {
    ...RouterLink.props
  },
  computed: {
    isExternal() {
      return typeof this.to === 'string' && this.to.startsWith('http');
    }
  }
}
</script>

<style scoped>

</style>