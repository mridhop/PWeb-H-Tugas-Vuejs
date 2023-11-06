<script setup>
    import { ref } from 'vue';

    const items = ref([
        { id: 1, text: 'Pemrograman Web - Ridho Rahman', done: true },
        { id: 2, text: 'Sistem Deteksi Intrusi - Hatma Surotrisongko', done: true },
        { id: 3, text: 'Smart City - M Husni', done: true },
        { id: 4, text: 'Internet of Things - M Husni', done: true }
    ]);
</script>

<template>
    <div>
        <h1>Hello</h1>
    </div>
    <div>
        <ul>
            <li v-for="item in items" :key="item.id" @click="item.done = !item.done" :style="{ backgroundColor: item.done ? 'aqua' : 'white' }">
                {{ item.text }}
            </li>
        </ul>
    </div>
</template>

<style scoped>
    li {
        margin-bottom: 5px;
    }
</style>