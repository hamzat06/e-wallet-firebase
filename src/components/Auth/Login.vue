<template lang="html">
  <div class="login py-5">
    <router-link to="/">
      <i class="bi bi-chevron-left"></i>
      Back to Home
    </router-link>
    <h1 class="text-center mb-4">Login</h1>
    <form class="mx-auto" @submit.prevent="loginUser">
      <div class="mb-3">
        <label class="form-label">Email</label>
        <input type="email" class="form-control" placeholder="Email" v-model="email">
      </div>
      <div class="mb-3">
        <label class="form-label">Password</label>
        <input type="password" class="form-control" placeholder="Password" v-model="password">
      </div>
      <div class="text-center">
        <button type="submit" class="btn btn-outline-dark btn-general mt-2 mb-3">Log in</button>
        <p>Don't have an account? <router-link to="/auth/register">Register</router-link></p>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: 'Login',
  data: () => ({
    email: '',
    password: ''
  }),
  methods: {
    loginUser () {
      const data = {
        email: this.email,
        password: this.password
      }

      console.log(data)
      // axios.post( , data)
      //   .then((res) => {
      //     user = res.data
      //     console.log(user)
      //   })
      //   .then(() -> {
      //     this.$router.push('/dashboard/' + user.type)
      //   })
    }
  }
}
</script>

<style lang="css" scoped>
form {
  max-width: 400px;
}
</style>
