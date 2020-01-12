<template>
    <div id="app">
        <div class="mx-12 text-gray-900">
            <div class="flex flex-wrap mx-1">
                <Card v-for="character in characters" :key="character.id" :data='character'></Card>
            </div>
        </div>
    </div>
</template>

<script>
    import Card from './components/Card.vue'

    export default {
        name: 'app',
        components: {
            Card
        },
        data() {
            return {
                characters: null,
            }
        },
        mounted() {
            this.data = this.$http.get('https://rickandmortyapi.com/api/character')
                .then(response => {
                    this.characters = response.data.results
                })
        }
    }
</script>

<style>
#app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
