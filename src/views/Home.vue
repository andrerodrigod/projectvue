<script setup>
import { ref } from "vue"
import Header from "../components/home/Header.vue"
import Content from "../components/home/Content.vue"
import Footer from "../components/home/Footer.vue"
const headerView = ref(true)

const changeView = () => { headerView.value = !headerView.value }
</script>

<template>
  <div class="container">
    <Header v-if="headerView" />
    <Content />
    <Footer />
  </div>
</template>

<style scoped>
.container {
  width: 100% !important;
  display: flex;
  flex-direction: column;
  gap: 30px;
}
</style>
