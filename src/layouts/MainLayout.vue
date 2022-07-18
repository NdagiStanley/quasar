<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="bg-white text-grey-10" bordered>
      <q-toolbar class="constraint">
        <q-btn class="large-screen-only q-mr-sm" icon="apps" flat round dense />
        <q-separator class="large-screen-only" vertical spaced />
        <q-toolbar-title class="text-tangerine">App</q-toolbar-title>
        <q-btn
          @click="goHome"
          class="large-screen-only"
          icon="home"
          dense
          flat
          round
        />
        <q-btn
          @click="goNext"
          class="large-screen-only"
          icon="add"
          dense
          flat
          round
        />
      </q-toolbar>
    </q-header>

    <q-footer class="bg-white small-screen-only" bordered>
      <q-tabs
        class="text-grey-10"
        active-color="primary"
        indicator-color="transparent"
      >
        <q-route-tab icon="home" label="Index" to="/" />
        <q-route-tab icon="add" label="Another" to="/another" />
      </q-tabs>
    </q-footer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
function goHome() {
  window.location.assign('/#/')
}
function goNext() {
  window.location.assign('/#another')
}
</script>

<style lang="sass">
.q-toolbar
  @media (min-width: $breakpoint-xs-max)
    height: 60px
.q-toolbar__title
  @media (max-width: $breakpoint-xs-max)
    text-align: center
</style>
