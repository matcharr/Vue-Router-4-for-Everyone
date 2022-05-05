<template>
  <div class="card">
    <img :alt="experience.name" :src="`/images/${experience.image}`"/>
    <span class="card__text">
    {{ experience.name }}
  </span>
  </div>

</template>

<script>
export default {
  name: "ExperienceCard",
  props: {
    experience: {type: Object, required: true}
  }
}
</script>

<style scoped>

</style>