<template>
    <button class="customized-button " @click="emitClick">
        <slot name="text"></slot>
    </button>
</template>
<script setup>
const emit = defineEmits(['click'])
const emitClick = () => {
    emit('click')
}
</script>
<style scoped>
.customized-button {
    padding: 0.5rem 1rem;
    border-radius: 5px;
    border: none;
    background-color: #dc3545;
    color: white;
    cursor: pointer;
    width: 100%;
    
}
@media (max-width:  568px) {
    .customized-button {
        padding: 0.8rem 1rem;
    }
}
.customized-button:hover {
    background-color: #c82333;
}
</style>