<template>
  <div id="footer">
    <v-footer
        padless
    >
      <v-card
          class="text-center"
          tile
          width="100%"
      >
        <v-card-text>
          <v-fab-transition>
            <v-btn
                absolute
                color="pink"
                dark
                fab
                right
                top
                @click="switchTheme"
            >
              <v-icon v-if="!this.$vuetify.theme.dark">mdi-weather-night</v-icon>
              <v-icon v-else>mdi-weather-sunny</v-icon>
            </v-btn>
          </v-fab-transition>
          本服务由 <a href="https://blog.iamsjy.com/">Tony</a> 运营。感谢 BlackBE 云黑团队的源码。
          <br>
          <v-btn
              class="mx-4"
              href="https://github.com/blackbedevelopment"
              icon
              target="_blank"
          >
            <v-icon size="24px">
              mdi-github
            </v-icon>
          </v-btn>
          <p>
            Copyright &copy {{ new Date().getFullYear() }} <strong>BlackBEDevelopment</strong> all reight
            reserved. Made by <a href="//github.com/lixworth">lixworth</a> with 🐱 .
          </p>
        </v-card-text>

      </v-card>
    </v-footer>
  </div>
</template>

<script>
export default {
  name: "Footer",
  methods: {
    switchTheme() {
      this.$store.commit('mutationDark', !this.$vuetify.theme.dark);
      this.$vuetify.theme.dark = !this.$vuetify.theme.dark;
    }
  }
}
</script>

<style scoped>

</style>
