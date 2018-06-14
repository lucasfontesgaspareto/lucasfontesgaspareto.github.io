<template>
  <v-layout row wrap fill-height>
    <v-flex xs2>
      <div class="text-xs-center mt-4">
        <v-avatar size="125px">
          <img
            class="img-circle elevation-7 mb-1"
            src="perfil.jpeg"
          >
        </v-avatar>
        <div class="headline">Lucas <span style="font-weight:bold">Gaspareto</span></div>
        <div class="subheading text-xs-center grey--text pt-1 pb-3">Javscript expert</div>
        <v-layout column>
          <nuxt-link to="/" class="body-2">Home</nuxt-link>
          <a href="https://github.com/lucasfontesgaspareto" target="_blank" class="body-2">Github</a>
          <h3 class="mt-4">Projetos</h3>
          <nuxt-link to="/to-do-list" class="body-2">To-Do List</nuxt-link>
        </v-layout>
      </div>
    </v-flex>
    <v-flex xs10>
      <nuxt-child></nuxt-child>
    </v-flex>
  </v-layout>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    Logo,
    VuetifyLogo
  }
}
</script>
