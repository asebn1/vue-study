<template>
    <header>
        <h1> {{ propsdata }}</h1>
        <!-- 하위 -> 상위 이벤트 날리기 -->
        <button v-on:click="sendEvent">send</button>
    </header>
</template>

<script>
export default {
    props: ['propsdata'],
    methods: {
        sendEvent: function(){
            this.$emit('renew')
        }
    }
}
</script>

<style>

</style> 