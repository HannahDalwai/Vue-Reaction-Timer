<template >
<p>Reaction time  = {{ score }}ms</p>
<p class="rank"> {{ rank }}</p>
</template>

<script>
export default {
    props:[`score`],
    data(){
        return{
            rank: null
        }
    },
    mounted(){
        if(this.score < 250 ){
            this.rank='Lightning Fast'
        } else if(this.score < 400 ){
            this.rank = 'Average'
        } else {
            this.rank = 'Snail pace...'
        }
    }
}
</script>
<style>
    .rank{
        font-size:1.5 rem;
        color:#706B3D;
        font-weight:bold;
    }
</style>