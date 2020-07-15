<template>
    <div id="home">
        <nav-bar class="home-nav"><div slot="center">购物车</div></nav-bar>
    </div>
</template>

<script>
import NavBar from 'components/common/navbar/NavBar'
import {getHomeMultidata} from 'network/home'
export default {
    name: 'Home',
    components: {
        NavBar
    },
    created() {
        getHomeMultidata().then(res => {
            console.log(res)
        })
    }
}
</script>

<style scoped>
.home-nav {
    background-color: var(--color-tint);
    color: #fff;
}
</style>