<script setup>

const pokemon = defineProps(["name", "xp", "height", "img", "loading"])


</script>



<template>
    <div 
    class="card CardPokemonSelected"
    :class="loading ? '' : 'animate__animated animate__flipInY'"
    >
        <img 
        :src="pokemon.img" 
        height="250"
        class="card-img-top pt-2" 
        :alt="pokemon.name"
        >
        <div class="card-body">
            <h5 class="card-title text-center">{{ pokemon.name }}</h5>
            <hr>
            <div class="row">
                <section class="col">
                    <strong>XP:</strong>
                    <span>{{ pokemon.xp }}</span>
                </section>

                <section class="col">
                    <strong>Altura:</strong>
                    <span>{{ pokemon.height }}</span>
                </section>

            </div>
        </div>
    </div>



</template>



<style scoped>

.CardPokemonSelected{
    height: 450px;
    background: rgb(251, 0, 0);
    background: radial-gradient(circle, rgba(243, 112, 25, 0.6) 0%, rgba(253, 39, 39, 0.452) 100%);
}


</style>