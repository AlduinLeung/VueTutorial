<template>
  <div id="app">
    {{ user.username }} - {{ fullName }} <strong>followers</strong
    >{{ followers }}
    <button v-on="">follow</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      followers: 0,
      user: {
        id: 1,
        username: '@_mitchelRomney',
        firstName: 'mitch',
        lastName: 'Ronney',
        email: '111@gmail.com',
        isAdmin: true,
      },
    };
  },
  computed: {
    fullName() {
      return `${this.user.firstName} ${this.user.lastName}`;
    },
  },
  method: {
    followers() {
      this.followers++;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  display: flex;
  flex-direction: column;
  /* justify-content: center; */
  text-align: center;
}
</style>
