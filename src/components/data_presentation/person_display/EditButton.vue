<template>
  <div class="edit-button">
    <router-link v-if="id !== undefined" :to="{ name: 'Edit', params: { id: id } }">
      <button type="button"
              v-text="'Edit'"/>
    </router-link>
  </div>
</template>

<script>
  export default {
    name: 'EditButton',
    props: { id: String },
  };
</script>

<style scoped>

.edit-button {
  display: grid;
  place-items: center;
}

button {
  cursor: pointer;
  width: clamp(3rem, 12vw, 15rem);
  margin-right: clamp(0rem, 2vw, 1rem);
  height: 3.5vh;
  background-color: #3d3a3a;
  color: white;
  border: none;
  font-size: clamp(1rem, 2vh, 1.5rem);
  border-radius: 5vw;
}

</style>
