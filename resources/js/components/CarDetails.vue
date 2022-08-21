<template>
    <div class="d-flex">
        <h1>{{ licenc }}</h1><button @click="buttonClick" class="btn btn-info">Részletek</button>
    </div>
        <table v-show="isOpen" class="table">
            <thead>
            <tr>
                <th></th>
                <th></th>
            </tr>
            </thead>
            <tbody>
            <tr>
                <th>Serial</th>
                <td>{{ serial }}</td>
            </tr>
            <tr>
                <th>Color</th>
                <td>{{ color }}</td>
            </tr>
            <tr>
                <th>Doors</th>
                <td>{{ doors }}</td>
            </tr>
            </tbody>
        </table>
</template>

<script>
export default {
    name: "CarDetails",
    props: ['licenc','serial','color','doors'],
    data(){
        return{
            isOpen:false,
        }
    },
    methods: {
        buttonClick() {
            if (this.isOpen === true)
                return this.isOpen = false;
                else return this.isOpen = true;
        }
    }
}
</script>

<style scoped>

</style>
