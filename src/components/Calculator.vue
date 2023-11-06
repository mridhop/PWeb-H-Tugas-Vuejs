<script setup>
    import { ref } from 'vue';
    
    const num1 = ref(0);
    const num2 = ref(0);
    const result = ref(0);

    function add() {
        result.value = num1.value + num2.value;
    }

    function subtract() {
        result.value = num1.value - num2.value;
    }

    function multiply() {
        result.value = num1.value * num2.value;
    }

    function divide() {
        result.value = num1.value / num2.value;
    }
</script>

<template>
    <div>
        <h1>Calculator</h1>
    </div>
    <div>
        <input v-model="num1"/>
        <input v-model="num2"/>
    </div>
    <div>
        <button v-on:click="result=parseFloat(num1)+parseFloat(num2)">+</button>
        <button v-on:click="subtract">-</button>
        <button @click="multiply">*</button>
        <button @click="divide">/</button>
    </div>
    <div>
        <h2>Result: {{ result }}</h2>
    </div>
</template>