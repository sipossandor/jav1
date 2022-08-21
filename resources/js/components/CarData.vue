<template>
<h1>Autók</h1>
    <car-details v-for="car in cars" :licenc="car.licenc" :serial="car.serial" :color="car.color" :doors="car.doors"></car-details>
</template>

<script>
import CarDetails from "./CarDetails";
export default {
    name: "CarData",
    components: {CarDetails},
    props:['cars']
}
</script>

<style scoped>

</style>
