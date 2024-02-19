<template>
    <header class="sticky top-0 bg-weather-primary shadow-lg">
        <nav class="container flex items-center text-white py-3">
            <RouterLink :to="{name:'home'}">
                <div class="flex items-center gap-3 flex-1">
                    <i class="fa-solid fa-sun text-white text-1xl" ></i>
                    <p class="text-1xl">The Local Weather</p>
                </div>
            </RouterLink>

            <div class="flex flex-1 gap-3 justify-end">
                <i @click="toggleModal" class="fa-solid fa-circle-info hover:text-weather-secondary duration-150 cursor-pointer"></i>
            </div>
            <BaseModal :modalActive="modalActive" @Close="toggleModal">
                <h1 class="text-black"> Hello from Modal</h1>
                <p class="text-black">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ullam quae tempora, ab rem vel at hic dolore obcaecati repellendus ducimus tenetur, architecto saepe, aut expedita minima eligendi error. Quo, voluptate.</p>
            </BaseModal>
        </nav>
        
    </header>
    
</template>

<script setup>
import { ref } from 'vue';
import { RouterLink } from 'vue-router';
import BaseModal from './BaseModal.vue';

const modalActive = ref(null)
const toggleModal = () => {
    modalActive.value = !modalActive.value
}
</script>
