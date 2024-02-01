<script setup>
import HeroImage from '../components/HeroImage.vue'
import SpaOffers from '../components/SpaOffers.vue'
</script>

<template>
  <main>
<HeroImage/>
<h1 class="title">{{ message }}</h1>
<div id="offers">
    <div class="container text-center">
        <div class="row align-items-center">
            <spa-offer v-for="spa in spas" :key="spa.id" :offer="spa"/>
        </div>

    </div>
</div>
</main>
</template>

<script>
    export default {
        data() {
            return{
                spas: [],
                message: 'Vilket paket önskas?'
            }
        },
        name: 'HomeView',
        components: {'spa-offer': SpaOffers},
        created(){
            this.fetchData()
        },
        methods:{
            async fetchData(){
                const res = await fetch('spa.json')
                const val = await res.json()
                this.spas = val
            }
        }

    }
</script>
<style scoped>
#offers{
    display: flex;
    justify-content: center;
    margin-top: 10vh;
    margin-bottom: 10vh;
}

#contact{
    display:flex;
    justify-content: center;
    flex-direction: column;
    width: 300px;
    margin: 0 auto;
    margin-bottom:20vh;
}
</style>
