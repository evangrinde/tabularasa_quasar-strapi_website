<template>
  <q-layout view="hHh Lpr lFf">
    <q-header>
      <q-toolbar>
        <!-- <q-btn
          flat
          dense
          round
          icon="fas fa-bars"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        /> -->

        <q-toolbar-title class="text-center">Your Website</q-toolbar-title>

        <div>
          <!-- <a @click="logOut()">Logout</a> -->
        </div>
      </q-toolbar>
    </q-header>

    <!-- <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-grey-1"
    >
      <q-img
        class="absolute-top"
        src="https://cdn.quasar.dev/img/material.png"
        style="height: 150px"
      >
        <div class="absolute-bottom bg-transparent">
          <div>hello world</div>
        </div>
      </q-img>

      <q-scroll-area
        style="
          height: calc(100% - 150px);
          margin-top: 150px;
          border-right: 1px solid #ddd;
        "
      >
        <q-list>
          <EssentialLink
            v-for="link in essentialLinks"
            :key="link.title"
            v-bind="link"
          />
        </q-list>
      </q-scroll-area>
    </q-drawer> -->

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: "MainLayout",
  components: {
    EssentialLink: () => import("components/EssentialLink"),
  },
  data() {
    return {
      leftDrawerOpen: false,
      essentialLinks: [
        {
          title: "Dashboard",
          // caption: "Dashboard",
          // icon: "plus",
          link: "/",
        },
      ],
    };
  },
};
</script>
