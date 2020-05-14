<template>
  <input type="text" v-model="value" @input="log" />
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {
    const value = ref('')
    return {
      value,
      log: (event) => console.log('domValue', event.target.value, 'isComposing', event.isComposing)
    }
  }
}
</script>
