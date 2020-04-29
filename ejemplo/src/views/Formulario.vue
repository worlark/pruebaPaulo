<template>
    <div class="mt-5"> 
        <h1 class="text-left">Formulario</h1>
        <form>
            <b-row>
                <b-col md="3">
                    <b-form-input type="text" v-model="texto" :state="comprobar"></b-form-input>
                    <h6 class="text-left">minimo 3 caracteres</h6>
                </b-col>
                <b-col md="3">
                    <b-form-select v-model="select" :options="animales">
                        
                        
                    </b-form-select>
                    <p class="text-left"> seleccionado : {{select}}</p>
                </b-col>
                <b-col md="3">
                    <b-form-radio-group v-model="radio" :options="animalesRadio">

                    </b-form-radio-group>
                </b-col>
                <b-col md="3">
                    <b-form-checkbox-group v-model="check" :options="animalesRadio">
                        
                    </b-form-checkbox-group>
                </b-col>
            </b-row>
            
            
        </form>
        <p class="text-left mt-3"> texto: {{texto}}</p>
    </div>
</template>

<script>
export default {
    name: 'Formulario',

    data(){
        return{
            texto: '',
            select: '',
            animales:[
                {value:null,text:'seleccione un animal'},
                {value:'perro',text:'guau'},
                {value:'gato',text:'miau'},
                {value:'pato',text:'cuak'},
            ],
            animalesRadio:[
                {value:'perro',text:'guau'},
                {value:'gato',text:'miau'},
                {value:'pato',text:'cuak'},
            ],
            check:[],

        }
    },

    computed:{
        comprobar(){
            return this.texto.length >2 ? true:false;
        }

    }

    
}
</script>