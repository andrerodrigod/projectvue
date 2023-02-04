<script setup>
import list from "../../views/list"
</script>

<template>
    <div class="content">
        <div class="item" v-for="product in list">
            <img :src="product.picture"
                :style="{ maxWidth: '80px', maxHeight: '80px', margin: '0 auto', display: 'block' }" />
            <h1>{{ product.name }}</h1>
            <p>{{ product.description }}</p>
            <span>{{ product.price.toLocaleString('pt-br',{style: 'currency', currency: 'BRL'}) }}</span>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.content {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    .item {
        background: white;
        max-width: 300px;
        color: red;
        padding: 10px;
        border-radius: 8px;
        overflow: hidden;
    }

}
</style>