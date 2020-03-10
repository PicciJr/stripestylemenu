<template>
    <div>
        <ul>
            <li v-for="prod in products" :key="prod">{{prod.title}}</li>
        </ul>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                products: [
                    {
                        title: 'Payments',
                        description: 'A complete payments solution'
                    },
                    {
                        title: 'Building',
                        description: 'A complete building solution'
                    },
                    {
                        title: 'Connect',
                        description: 'A complete connect solution'
                    },
                ]
            }
        }
    }
</script>

<style scoped>

li {
  display: block;
  padding: 10px;
  position: relative;
  top: 0px;
  left: -80px;
}

</style>