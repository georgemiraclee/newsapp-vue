<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>News App</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon color="grey">mdi-magnify</v-icon>
      </v-btn>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" app color="primary" dark>
      <v-list dense>
        <v-list-item v-for="(item, idx) in items" :key="idx" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <v-container>
        <v-card class="my-8" elevation="2" v-for="n in 5" :key="n">
          <v-img
            height="400"
            src="https://imageio.forbes.com/specials-images/imageserve/60521e8eb22ac9277f31d40d/0x0.jpg?format=jpg&width=1200"
          ></v-img>

          <v-card-title>Why You Need A Cybersecurity Strategy Now</v-card-title>

          <v-card-subtitle class="my-4">
            If you’re one of the many still doubting whether you need a
            cybersecurity strategy, here are some of the top-line reasons why
            investing in one is critical for your business’ short-term survival
            and long-term success.
          </v-card-subtitle>

          <v-card-actions>
            <v-flex class="d-flex flex-row justify-space-between my-4">
              <v-chip color="black" dark>
                <strong>TechCrunch</strong>
              </v-chip>

              <div>
                <v-icon
                  class="mx-2"
                  v-for="(icon, idx) in icons"
                  :key="idx"
                  :color="icon.color"
                >
                  {{ icon.name }}
                </v-icon>
              </div>

              <v-btn color="primary"> Read More </v-btn>
            </v-flex>
          </v-card-actions>
        </v-card>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      drawer: true,
      items: [
        { title: "Home", icon: "mdi-home-city" },
        { title: "My Account", icon: "mdi-account" },
        { title: "Users", icon: "mdi-account-group-outline" },
        { title: "Home", icon: "mdi-home-city" },
        { title: "My Account", icon: "mdi-account" },
        { title: "Users", icon: "mdi-account-group-outline" },
        { title: "Home", icon: "mdi-home-city" },
        { title: "My Account", icon: "mdi-account" },
        { title: "Users", icon: "mdi-account-group-outline" },
        { title: "Home", icon: "mdi-home-city" },
        { title: "My Account", icon: "mdi-account" },
        { title: "Users", icon: "mdi-account-group-outline" },
        { title: "Home", icon: "mdi-home-city" },
        { title: "My Account", icon: "mdi-account" },
        { title: "Users", icon: "mdi-account-group-outline" },
        { title: "Home", icon: "mdi-home-city" },
        { title: "My Account", icon: "mdi-account" },
        { title: "Users", icon: "mdi-account-group-outline" },
        { title: "Home", icon: "mdi-home-city" },
        { title: "My Account", icon: "mdi-account" },
        { title: "Users", icon: "mdi-account-group-outline" },
        { title: "Home", icon: "mdi-home-city" },
        { title: "My Account", icon: "mdi-account" },
        { title: "Users", icon: "mdi-account-group-outline" },
      ],
      icons: [
        { name: "mdi-reddit", color: "orange" },
        { name: "mdi-twitter", color: "blue" },
        { name: "mdi-facebook", color: "blue" },
        { name: "mdi-google", color: "orange" },
        { name: "mdi-linkedin", color: "blue" },
        { name: "mdi-netflix", color: "red" },
      ],
    };
  },
};
</script>
