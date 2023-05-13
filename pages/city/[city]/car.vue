<script setup lang="ts">
const route = useRoute()
const { toTitleCase } = useUtilities()
useHead({
    title: `${route.params.make ? toTitleCase(route.params.make.toString()) : 'Voiture'} à ${toTitleCase(route.params.city.toString())}`
})
definePageMeta({ layout: 'container' })
</script>

<template>
    <div>
        <div class="mt-32 flex">
            <CarSidebar />
            <CarCard />
        </div>
    </div>
</template>