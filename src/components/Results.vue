<template>
  <div class="result">
    <h1>here is your score</h1>
    <p>{{score}} ms</p>
    <p class="rank"> {{rank}} </p>
  </div>
</template>

<script>
export default {
    props: ['score'],
    data () {
        return {
            rank: null,
        }
    },
    mounted() {
        if (this.score < 250) {
            this.rank = 'Ninjia fingers'

        } else if(this.score < 400) {
            this.rank = 'rapid reflexes'
        } else {
            this.rank = 'snail pace hehe'
        }
    }
}
</script>

<style>
    .rank {
        color: red;
    }

</style>