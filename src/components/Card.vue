<template>
    <div class="card">
        <h1>{{ title }}</h1>
        <h3>{{ user }}</h3>
        <div v-for="item in list" :key='item'>
            <h3>{{item}}</h3>
        </div>
    </div>
</template>

<script>

export default {
  name: 'DefaultCard',
  props: {
    title: String,
    user: String,
    list: Array
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
