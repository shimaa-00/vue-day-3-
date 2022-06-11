<template>
  <div class="container">
    <div class="row">
      <div class="col-12 m-4">
        <ul class="navbar-nav mr-auto w-100 text-center d-inline-block">
          <li class="nav-item d-inline-block mx-3">
            <router-link to="/">Home</router-link>
          </li>
          <li class="nav-item d-inline-block mx-3">
            <router-link to="/about">About</router-link>
          </li>
          <li class="nav-item d-inline-block mx-3">
            <router-link to="/contact">Contact</router-link>
          </li>
        </ul>
      </div>
    </div>
    <div class="row">
      <router-view></router-view>
    </div>
  </div>
</template>
