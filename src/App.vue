<template>
  <div id="app" class="container">
    <div id="nav">
      <ul class="nav justify-content-center">
        <li class="nav-item">
          <router-link class="nav-link active"  to="/">Home</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/blog/1">Blog</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/servicios">Servicios</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" :to="{name: 'Contacto'}">Contacto</router-link>
        </li>
      </ul>
    </div>
    <router-view/>
  </div>
</template>

<style>

</style>
