<template>
    <footer>
        <p>Copyright &copy; 2023</p>
        <router-link to="/about" v-show="aboutButton">About</router-link>
    </footer>
</template>

<script>
    export default {
        name: 'Footer',
        computed : {
            aboutButton() {
                if(this.$route.path === '/'){
                    return true
                }
                return false
            }
        }
    }
</script>

<style scoped>
    a {
        color: #333;
    }

    footer {
        margin-top: 30px;
        text-align: center;
    }
</style>