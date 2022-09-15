<template>
  <div id="app">
    <table>
      <tr>
        <th>Picture</th>
        <th>Name</th>
        <th>Popularity</th>
      </tr>
      <Contact
        v-for="contactFor in firstFive"
        :key="contactFor"
        :contactFor="contactFor"
      />
    </table>
  </div>
</template>

<script>
import contacts from "./contacts.json";
import Contact from "./components/Contact.vue";
export default {
  name: "App",
  data() {
    return {
      contacts: contacts,
      firstFive: [...contacts.slice(0, 5)],
    };
  },

  components: { Contact },
};
</script>
