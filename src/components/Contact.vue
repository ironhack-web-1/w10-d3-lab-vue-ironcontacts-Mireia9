<template>
  <tr>
    <td><img :src="contactFor.pictureUrl" /></td>
    <td>{{ contactFor.name }}</td>
    <td>{{ contactFor.popularity.toFixed(2) }}</td>
  </tr>
</template>

<script>
export default {
  name: "Contact",
  props: {
    contactFor: {
      type: Object,
      required: true,
    },
  },
};
</script>
<style scoped>
td {
  height: 150px;
  padding: 10px 50px;
}

img {
  width: 5rem;
}
</style>
