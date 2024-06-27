<template>
  <v-container>
    <v-card 
    v-for="(word, idx) in $props.wordsArr" 
    :key="idx" 
    elevation="0" 
    >
      <p 
      :style="`font-size: ${$props.size}px;`"
      :class="`text-${$props.leveling}`">
      
      <v-icon>{{ icon[word.icon] }}</v-icon>
        {{ word.text }}
      </p>
    </v-card>
  </v-container>
</template>

<script>
import { mdiCircleSmall } from '@mdi/js'
export default {
  name: 'WordsComponent',
  props: {
    wordsArr: Array,
    leveling: String,
    size: String,
  },
  data: () => ({
    icon: {
      mdiCircleSmall,
    }
  }),
}
</script>
<style>
</style>
