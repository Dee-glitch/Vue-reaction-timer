<template>
  <p>Reaction Time - {{ score }} ms</p>
  <p class="rank">{{ rank }}</p>
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
            this.rank = 'Lightning fingers!'
        } else if (this.score < 400) {
            this.rank = 'Rapid reflexes!'
        } else {
            this.rank = 'Snail pace...!'
        }
    }
}
</script>

<style>
    .rank {
        font-size: 1.4em;
        color:  #df4e4e;
        font-weight: bold;
    }
</style>