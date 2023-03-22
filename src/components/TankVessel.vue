<template>
  <div class="tank-container">
    <div class="space-front"></div>
    <div class="tank water">
      <div class="fill"></div>
      <div class="level"></div>
    </div>
    <div class="tank sand">
      <div class="fill"></div>
      <div class="level"></div>
    </div>
    <div class="tank oil">
      <div class="fill"></div>
      <div class="level"></div>
    </div>
    <div class="space-back"></div>
  </div>
</template>

<script lang="ts">
export default {
  name: 'TankVessel',
  // Props are passed in from the parent component.
  // They are immutable and can be used to trigger updates.
  props: {
    water: {
      type: Number,
      required: true,
    },
    oil: {
      type: Number,
      required: true,
    },
    sand: {
      type: Number,
      required: true,
    },
  },
  // Properties returned from data() become reactive state
  // and will be exposed on `this`.
  data() {
    return {
      water: 0,
      oil: 0,
      sand: 0,
    };
  },

  // Methods are functions that mutate state and trigger updates.
  // They can be bound as event listeners in templates.
  methods: {
    increment() {
      console.log('increment');
    },
  },

  // Lifecycle hooks are called at different stages
  // of a component's lifecycle.
  // This function will be called when the component is mounted.
  mounted() {},
};
</script>

<style scoped>
.tank-container {
  display: flex;
  background-image: url('../assets/tank.svg');
  background-repeat: no-repeat;
  background-size: cover;
}

.space-front {
  width: 78%;
  position: relative;
  text-align: center;
}
.space-back {
  width: 50%;

  position: relative;
  text-align: center;
}
.tank {
  width: 75%;
  margin: 4em 0.5em 0em 0.5em;

  position: relative;
  text-align: center;
}

/* .tank {
  height: 100%;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-image: url('../assets/tank.svg');
  background-repeat: no-repeat;
  background-size: cover;
} */
.level {
  position: absolute;
  bottom: 50%;
  width: 100%;
  border-top: 2px solid rgb(127, 151, 48);
}

.fill {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 20%;
  background-color: blue;
}

.water .fill {
  background-color: blue;
}

.sand .fill {
  background-color: yellow;
}

.oil .fill {
  background-color: brown;
}
</style>
