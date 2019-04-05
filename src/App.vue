<template>
  <v-app>
    <v-navigation-drawer app
      v-model="drawer"
      ></v-navigation-drawer>
    <v-toolbar app>
    <v-btn
          color="pink"
          dark
          @click.stop="drawer = !drawer"
        >
          Toggle
        </v-btn>
    </v-toolbar>
    <v-content>
      <v-container fluid>
        <router-view></router-view>
      </v-container>
    </v-content>
    <v-footer app></v-footer>
  </v-app>
</template>

<script>
  export default {
    data () {
      return {
        drawer: null,
        items: [
          { title: 'Home', icon: 'dashboard' },
          { title: 'About', icon: 'question_answer' }
        ]
      }
    }
  }
</script>
