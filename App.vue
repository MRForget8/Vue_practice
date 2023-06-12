<template>
  <div class="app">
    <div v-if="loggedIn">
      <button @click="logout">Logout</button>
    </div>
    <div v-else>
      <!-- 登录组件 -->
      <Login @login-success="handleLoginSuccess" />
    </div>
  </div>
</template>

<script>
import Login from './components/LoginForm.vue';

export default {
  components: {
    Login
  },
  data() {
    return {
      loggedIn: false
    };
  },
  methods: {
    handleLoginSuccess() {
      this.loggedIn = true;
    },
    logout() {
      this.loggedIn = false;
    }
  }
};
</script>

<style>
.app {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

button {
  padding: 10px 20px;
  background-color: #007bff;
  color: #fff;
  border: none;
  cursor: pointer;
  margin-top: 10px;
}
</style>
