<template>
  <v-app id="inspire">
    <Drawer />

    <Toolbar />

    <v-main
      class="base"
    >
      <v-container
        fluid
      >
        <router-view></router-view>
      </v-container>
    </v-main>

    <BackToTop :visibilityHeight="100" />
  </v-app>
</template>

<script>
  import Drawer from './Drawer'
  import BackToTop from '@/components/BackToTop'
  import Toolbar from './Toolbar'

  export default {
    name: 'Layout',
    components: { Drawer, BackToTop, Toolbar },
    data: () => ({
      drawer: true,
    }),
  }
</script>

<style scoped>
  .base {
    background-color: var(--v-background-base);
  }
</style>