<template>
  <div class="container">
    <header class="header">
      <img
        src="https://www.goodfreephotos.com/albums/vector-images/pig-vector-art.png"
        class="header__icon"
        alt="Pig Icon"
      />
      <h1 class="header__title">Pig Latin Translator</h1>
    </header>
    <div class="text-input">
      <textarea v-model="inputText" class="text-input__input" id="textInput" cols="30" rows="10"></textarea>
    </div>
    <div class="text-output" id="textOutput">{{ outputLatin }}</div>
  </div>
</template>

<script>
const vowels = ['e', 'i', 'a', 'o', 'u']
const ending = 'ay'
export default {
  data() {
    return {
      inputText: ''
    }
  },
  computed: {
    outputLatin() {
      const output = this.inputText
        .split(' ')
        .map(word => {
          if (vowels.includes(word[0])) {
            return word + ending
          } else {
            return word
          }
          let consonantsPrefix = ''
          for (let i = 0; i < word.length; i++) {
            const char = word[i]
            if (vowels.includes(char)) {
              break
            }
            consonantsPrefix += char
          }
          return (
            word.substring(consonantsPrefix.length) + consonantsPrefix + ending
          )
        }).join(' ')
      return output
    }
  }
}
</script>

<style scoped>
</style>