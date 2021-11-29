<template>
  <div id="app" class="container-fluid">
    <div class="row">
      <div class="col">

      </div>
      <div class="col">
        <h1>LOGOSCAN</h1>
      </div>
      <div class="col">

      </div>
    </div>
    <div class="row">
      <div>
      <b-navbar type="light" variant="light">
        <b-navbar-nav>
          <b-nav-item :to="{name:'Home'}">Home</b-nav-item>
          <b-nav-item :to="{name:'Inicio'}">Inicio</b-nav-item>
          <b-nav-item :to="{name:'Descarga'}">Descarga</b-nav-item>
          <b-nav-item :to="{name:'Doc'}">Documentación</b-nav-item>
          <b-nav-item :to="{name:'About'}">Acerca de:</b-nav-item>
        </b-navbar-nav>
      </b-navbar>
      </div>
    </div>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
