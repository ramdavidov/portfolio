<script setup lang="ts" >

import { ref } from 'vue'

const count = ref<number>(0)

const onIncrementClick = (): void => {
    count.value++
}

const onDecrementClick = (): void => {
    if (count.value > 0) {
        count.value--;
    }
}

</script>

<template>
    <div class="test">
        <h1>COUNT {{ count }}</h1>
        <div class="buttons">
            <button class="increment" @click="onIncrementClick">+</button>
            <button class="decrement" @click="onDecrementClick">_</button>
        </div>
    </div>
</template>F