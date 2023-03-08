<!-- Composition API -->

<script setup>
import { ref } from 'vue';
const count = ref(0);

console.log(count);

const addToCount = () => {
    //console.log('inside count');
    count.value = count.value + 1;
};

const subtractFromCount = () => {
    //console.log('inside sub count');
    count.value = count.value - 1;
};
</script>

<!-- OPTIONS API Example below-->
<!--
<script>
export default {
    data() {
        return {
            count: 0,
        };
    },
    methods: {
        addToCount() {
            console.log('Inside Add Count');
            this.count = this.count + 1;
        },
        subtractFromCount() {
            console.log('Inside Subtract COunt');
            this.count = this.count - 1;
        },
    },
};
</script>
-->
<template>
    <main>
        <div>
            <h4>The current count is..</h4>
            <h1>{{ count }}</h1>
            <button @click="addToCount()">+</button>
            <button @click="subtractFromCount">-</button>
        </div>
    </main>
</template>

<style scoped>
main {
    background-color: aliceblue;
    width: 100vw;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
}
div {
    text-align: center;
}
</style>
