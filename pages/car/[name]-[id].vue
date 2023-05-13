<script setup lang="ts">
const route = useRoute()
const { toTitleCase } = useUtilities()
useHead({
    title: toTitleCase(route.params.name.toString())
})

definePageMeta({ layout: 'container' })
</script>
<template>
    <CarDetailHero />
    <CarDetailAttributes />
    <CarDetailDescription />
    <CarDetailContact />
</template>