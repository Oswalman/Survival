<template>
  <v-app>
    <v-app-bar color="white" max-height="60px" height="60px" dense>
      <v-btn to="/" text>
        INICIO
      </v-btn>
      <v-spacer></v-spacer>

      <v-btn to="/services" text>
        SERVICIOS
      </v-btn>
      <v-spacer></v-spacer>
      <v-btn to="/services" text>
        Tienda
      </v-btn>
      <v-btn icon>
        <v-icon>mdi-account</v-icon>
      </v-btn>
  
    </v-app-bar>

    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>

    <v-footer :absolute="!fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: "mdi-apps",
          title: "Welcome",
          to: "/"
        },
        {
          icon: "mdi-chart-bubble",
          title: "Inspire",
          to: "/inspire"
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "Vuetify.js"
    };
  }
};
</script>
