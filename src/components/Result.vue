<template>
  <h5 class="score">Reaction time: {{ score }}ms</h5>
  <p class="rank score">{{ rank }}</p>
</template>
<script>
export default {
  props: ['score'],
  data() {
    return {
      rank: null
    }
  },
  mounted() {
    if (this.score < 250) {
      this.rank = `Alla, Bossu!🙌🏽`
    } else if (this.score < 400) {
      this.rank = 'Uhuh, okay!👏🏾'
    } else {
      this.rank = 'Masa, why? Were you sleeping?😂'
    }
  }
}
</script>
<style>
.score {
  text-align: center;
}

.rank {
  font-size: 1.4em;
  color: #0faf87;
  font-weight: bold;
}
</style>