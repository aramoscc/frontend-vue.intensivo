<script setup >
    defineProps(["id","r","g","b"])
    const emit = defineEmits(["borrar"])
</script>

<template>
    <li :style="{backgroundColor : `rgb(${[r,g,b].join(',')})`}"
    @click="emit('borrar', id)"
    >{{ r }},{{ g }},{{ b }}</li>
</template>