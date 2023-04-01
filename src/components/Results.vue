<template>
  <h2>Reaction Time: {{ score }} ms</h2>
  <p> {{ ranking }}</p>
</template>

<script>
export default {
props: ['score'],
 data() {
    return {
        ranking: null,
    }
 },
 mounted() {
    this.setRank()
 },
 methods: {
    setRank() {
        if (this.score < 300){
            this.ranking = 'Speedy boi!'
        } else if (this.score >= 300 && this.score < 1000) {
            this.ranking = 'Medicore bruh!'
        } else {
            this.ranking = 'Were you AFK?'
        }
    }
 }
}
</script>

<style>
    p{
        font-size: 1.4em;
        color: #0faf87;
        font-weight: bold;
    }
</style>