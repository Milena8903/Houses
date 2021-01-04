<template>
<div>

<div class="navigation-bar">
    <div class="logo-container"></div>
    <div class="whatsapp-logo">
        <a :href="`https://wa.me/${phone}?text=hola%20como%20estas`">
        <img class="whatsapp-image" src="~/assets/whatsapp.png" alt="">
        </a>
    </div>



</div>
<br>
<br>
<br>
<input type="text" class="telefono-input" placeholder="cambia el telefono"  v-model="phone">
<button @click="dispararEvento">Click me</button>
<p>el numero cambiado<b>{{phone}}</b></p>
</div>
</template>

<script>
export default {
    data(){
        return {
            phone: "3165311874"
        }
    },
    methods:{
        dispararEvento: function(e){
            alert("hola mundo");
        }
    }
}
</script>

<style>

.telefono-input{
    border: none;
    outline: none;
    font-size: 1.5rem;
    display: block;
    margin: 0 auto;
    border-radius: 10px;
    padding: 10px;
    box-shadow: 1px 2px 10px #2222;
}
.navigation-bar{
    padding: 0 15px;
    display: flex;
    justify-content: space-between;
    box-shadow: 0px 2px 6px #2222;

}

.logo-container {
    width: 11rem;
    background: purple;
}



.navigation-bar .whatsapp-logo{
   
}
.whatsapp-image{
    width: 2rem;    
}

</style>


