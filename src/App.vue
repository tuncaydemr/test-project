<template>
  <div class="container">
    <div class="mb-3">
      <label for="name" class="form-label">Name</label>
      <input type="text" class="form-control" ref="name" id="name">
    </div>
    <div class="mb-3">
      <label for="password" class="form-label">Password</label>
      <input type="password" class="form-control" ref="password" id="password">
    </div>
    <button @click="login" class="btn btn-primary">Submit</button>
    <br class="mb-5">
    <p v-if="isLogin">Giriş Başarılı</p>
    <p v-else>Giriş Başarısız</p>
  </div>
</template>

<script>
import Index from './components/Index.vue'

export default {
  name: 'App',
  components: { Index },
  data() {
    return {
      title: 'Login',
      name: 'Tuncay',
      password: '1234',
      isLogin: false,
    }
  },

  methods: {
    login() {
      return this.$refs.name.value === 'Tuncay' && this.$refs.password.value === '1234' ? this.isLogin = true : this.isLogin = false
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
