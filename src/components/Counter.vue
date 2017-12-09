<template>
  <div id="app">
    <p class="md-display-1">Clicked: {{ $store.state.count }} times, count is {{ evenOrOdd }}.</p>
    <md-button class="md-raised md-primary" @click="increment">+</md-button>
    <md-button class="md-raised md-accent" @click="decrement">-</md-button>
    <md-button class="md-raised" @click="incrementIfOdd">Increment if odd</md-button>
    <md-button class="md-raised" @click="incrementAsync">Increment async</md-button>
  </div>
</template>

<script>
import { mapGetters, mapActions } from 'vuex'
export default {
  computed: {
    ...mapGetters([
      'evenOrOdd'
    ])
  },
  methods: {
    ...mapActions([
      'increment',
      'decrement',
      'incrementIfOdd',
      'incrementAsync'
    ])
  }
}
</script>
