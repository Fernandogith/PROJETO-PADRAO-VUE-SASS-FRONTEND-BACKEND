<template>
    <div class="container">
        <h1>Home</h1>

        <div class="componentes-scss">
            <h1>Componentes criados com SCSS</h1>

            <div class="divider" style="padding: 20px"></div>

            <div class="">
                <button class="btn-primary" @click="buscarNoBack()">btn-primary</button>
            </div>

            <div class="divider" style="padding: 20px"></div>
            
            <div class="">
                <button class="btn-secondary">.btn-secondary</button>
            </div>
        </div>

    </div>


</template>


<script>
import api from '@/services/api'


export default {
    name: "PessoasCadastro",
    

    data() {
        return {
    
        }
    },
    
    methods: {

        buscarNoBack: function () {

            api.get('/').then(response => {

                console.log(response.data); 
            });
        }
        
    },
}

</script>

<style src="./home.scss" lang="scss" scoped>