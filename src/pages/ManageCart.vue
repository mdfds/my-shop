<template>
    <div>
        <p v-if="cartItems.length === 0">Cart is empty</p>
    </div>

    <ul class="cart_list">
        <li 
            class="Item_cart" 
            v-for="(item, index) in cartItems" 
            :key="index"
        >
            <img 
                :src="item.image" 
                :alt="item.name" 
                class="cart_img"
            >
            <p>{{ item.name }} - {{ item.price }} grn</p>
        </li>
    </ul>
</template>

<script>
    export default{
        name: "ManageCart",

        data() {
            return({
                cartItems: []
            })
        }
    }
</script>