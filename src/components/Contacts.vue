<template>
  <div class="hello">
    <template v-for="contact in contacts">
      <slot :contact="contact"></slot>
    </template>
  </div>
</template>

<script>
export default {
  name: "Contacts",
  data() {
    return {
      contacts: [{ name: "Saksham" }, { name: "Priyam" }, { name: "Isham" }]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
