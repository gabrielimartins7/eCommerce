<template>
  <v-carousel height="100vh" hide-delimiter-background>
    <template #prev="{attrs, on}">
      <v-btn fab color="transparent" depressed v-bind="attrs" v-on="on">
        <v-icon size="20">mdi-arrow-left</v-icon>
      </v-btn>
    </template>
    <template #next="{attrs, on}">
      <v-btn fab color="transparent" depressed v-bind="attrs" v-on="on">
        <v-icon size="20">mdi-arrow-right</v-icon>
      </v-btn>
    </template>
  </v-carousel>
</template>

<script>
export default {

}
</script>

<style>

</style>
