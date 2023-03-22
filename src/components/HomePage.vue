<template>
  <v-container>
    <v-row>
      <v-col cols="12" class="blue-grey--text mt-4" align="center">
        <tank-vessel class="tank-view" :water="10" :oil="20" :sand="30" />
      </v-col>
    </v-row>
    <v-row>
      <v-col class="blue-grey--text mt-4" align="center">
        <h3 class="ma-4">Tank Tester - Version 0.0.1</h3>
      </v-col>
    </v-row>
  </v-container>
</template>

<script lang="ts">
import TankVessel from './TankVessel.vue';

export default {
  name: 'App',
  components: {
    TankVessel,
  },
};
</script>

<style scoped>
.tank-view {
  width: 80vw;
  height: 35vw;
  padding: 1em;
}
</style>
