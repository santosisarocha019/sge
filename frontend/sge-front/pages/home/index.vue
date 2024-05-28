<script setup lang="ts">
const{ signOut }= useAuth();
definePageMeta({
    middleware: 'auth'
})
const submitLogout = () =>{
        signOut ( {redirect:false}).then(()=>{
            console.log("successfully logged")
            navigateTo('/');
        })
        .catch((error)=>{
            console.log("error when trying to login", error);
        });

}

</script>

<template>
    <div>
        <h1>Minha Tela Home!!!</h1>    
        <button @click="submitLogout" class="customButton">SAIR</button>
    </div>
</template>

<style lang="scss">

</style>