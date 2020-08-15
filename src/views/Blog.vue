<template>
  <div>
    <h1 v-text="title"></h1>
    <router-link :to="paginate(false)">Anterior </router-link>
    <router-link :to="paginate(true)">Siguiente</router-link>
    <br>
    <router-link :to="{name:'Comments'}">Comentarios</router-link>
    <router-view></router-view>
  </div>
</template>
<script>
export default {
  computed: {
    title () {
      return `Este es el blog N°${this.$route.params.post}`
    }
  },
  methods: {
    paginate (dir) {
    // currentPost post actual
      const currentPost = parseInt(this.$route.params.post)
      if (dir) {
        return `/blog/${currentPost + 1}` // actual avance
      } else {
        return currentPost > 1 ? `/blog/${currentPost - 1}` : `/blog/${currentPost}`/* si post actual es mayor a 1 mostrar la ruta menos 1,
                                                                                      si no mostrar la ruta actual */
      }
    }
  }
}
</script>
