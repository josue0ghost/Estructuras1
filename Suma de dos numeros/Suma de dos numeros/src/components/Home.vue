<template>
    <div class="home">
        <h1>Suma de dos numeros:</h1>
        <input v-model.number="A" placeholder="Inserta un numero" />
        <hr />
        <input v-model.number="B" placeholder="Inserta un numero" />
        <hr />        
        <button @click="suma">Operar</button>
        <hr />
        <span>La suma de los dos numeros es: {{ SUM }}</span>    
    </div>
</template>

<script lang="ts">
    import { Component, Prop, Vue } from 'vue-property-decorator';

    @Component
    export default class Home extends Vue {
        @Prop() private msg!: string;

        A: number = 0
        B: number = 0
        SUM: number = 0

        suma() {
            this.SUM = this.A + this.B 
        }
    }
    
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
