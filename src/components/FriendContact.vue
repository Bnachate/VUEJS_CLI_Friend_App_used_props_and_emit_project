<template>
  <section>
    <li>
      <h2>{{ friend.name }}</h2>
      <button v-on:click="toggleDetails">{{detailsAreVisible ? 'Hide' :  'Show' }} Details</button>
      <ul v-if="detailsAreVisible">
        <li><strong>Phone:</strong> {{ friend.phone }}</li>
        <li><strong>Email:</strong> {{ friend.mail }}</li>
      </ul>
    </li>
  </section>
</template>
<script>
export default {
  data() {
    return {
      detailsAreVisible: false,
      friend: {
          id: "manuel",
          name: "Manuel Lorenz",
          phone: "1234 5678 991",
          mail: "manuel@localhost.com",
        },
    };
  },
  methods: {
    toggleDetails() {
      this.detailsAreVisible = !this.detailsAreVisible;
    },
  },
};
</script>
