<template>
<v-content>
  <v-app id="inspire">
    <v-navigation-drawer v-model="drawer" app>
      <v-list rounded>
        <v-subheader>REPORTS</v-subheader>
        <v-list-item-group v-model="selectedItem" color="primary">
          <v-list-item v-for="(item, i) in items" :key="i">
            <v-list-item-icon>
              <v-icon v-text="item.icon"></v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title v-text="item.text"></v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Coffee-log-app</v-toolbar-title>
    </v-app-bar>

    <v-main class="hoge">
      <v-container class="pa-0">
        <router-view></router-view>
      </v-container>
    </v-main>
  </v-app>
</v-content>
</template>

<script>
export default {
  data: () => ({
    drawer: null,
    selectedItem: 1,
    items: [
      { text: "Your log list", icon: "mdi-clipboard-list-outline" },
      { text: "Create a new log", icon: "mdi-pencil-plus-outline" },
      { text: "Coffee shop list", icon: "mdi-store" },
    ],
  }),
};
</script>

<style scoped>
  .hoge{
    background-color: blanchedalmond;
  }
</style>
