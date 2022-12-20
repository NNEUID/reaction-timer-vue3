<template>
    <h5 class="score">Reaction time: {{ score }}ms</h5>
</template>

<script>
export default {
    props: ['score']
}
</script>
<style>
.score {
    text-align: center;
}
</style>