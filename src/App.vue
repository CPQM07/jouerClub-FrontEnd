<template>
  <v-app>
    <component v-bind:is="layout"></component>
  </v-app>
</template>

<script>
import AppLayout from './layouts/AppLayout'
import LoginLayout from './layouts/LoginLayout'

export default {
  computed: {
    layout () {
      return this.$store.getters.layout
    }
  },
  components: {
    'app-layout': AppLayout,
    'login-layout': LoginLayout
    // define as many layouts you want for the application
  }
}
</script>
