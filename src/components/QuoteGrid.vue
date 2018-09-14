<template>
  <div class="row">
    <app-quote v-for="(quote, index) in quotes"
               @click.native="deleteQuote(index)">
      <p>{{ quote }}</p>
    </app-quote>
  </div>
</template>

<script>
import Quote from './Quote.vue'

export default {
  props: {
    quotes: Array
  },
  methods: {
    deleteQuote(index) {
      this.$emit('deleteQuote', index)
    }
  },
  components: {
    'app-quote': Quote
  }
}
</script>

<style>
</style>
