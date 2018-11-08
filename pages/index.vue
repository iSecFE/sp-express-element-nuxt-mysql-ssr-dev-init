<template>
  <section class="container">
    <logo :user-list="userList" />
  </section>
</template>

<script>
import axios from 'axios'
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },
  async asyncData(c) {
    let { data } = await axios.get(`http://localhost:3000/api/users`)
    return { userList: data.data}
  },
  mounted() {
  },
  methods: {
  }
}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
