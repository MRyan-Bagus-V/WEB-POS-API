<template>
  <header class="header_section fixed-top">
    <div class="container">
      <nav class="navbar navbar-expand-lg custom_nav-container">
        <router-link to="/" class="navbar-brand">
          <img src="/images/about-image.png" alt="" style="height: 70px;">
          <span class="ms-3 ml-4 navbar-title">StyleHub</span>
        </router-link>

        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span></span>
        </button>

        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav mx-auto">
            <li class="nav-item" :class="{ active: route.path === '/' }">
              <router-link class="nav-link" to="/">Home</router-link>
            </li>
            <li class="nav-item" :class="{ active: route.path === '/menu' }">
              <router-link class="nav-link" to="/menu">Product</router-link>
            </li>
            <li class="nav-item" :class="{ active: route.path === '/about' }">
              <router-link class="nav-link" to="/about">About</router-link>
            </li>
          </ul>

          <div class="user_option">
            <a href="#" class="user_link">
              <i class="fa fa-user" aria-hidden="true"></i>
            </a>
            <a class="cart_link" href="#">
              <svg version="1.1" id="Capa_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 456.029 456.029" xml:space="preserve">
                <g>
                  <g>
                    <path d="M345.6,338.862c-29.184,0-53.248,23.552-53.248,53.248c0,29.184,23.552,53.248,53.248,53.248
                    c29.184,0,53.248-23.552,53.248-53.248C398.336,362.926,374.784,338.862,345.6,338.862z" />
                  </g>
                </g>
                <g>
                  <g>
                    <path d="M439.296,84.91c-1.024,0-2.56-0.512-4.096-0.512H112.64l-5.12-34.304C104.448,27.566,84.992,10.67,61.952,10.67H20.48
                    C9.216,10.67,0,19.886,0,31.15c0,11.264,9.216,20.48,20.48,20.48h41.472c2.56,0,4.608,2.048,5.12,4.608l31.744,216.064
                    c4.096,27.136,27.648,47.616,55.296,47.616h212.992c26.624,0,49.664-18.944,55.296-45.056l33.28-166.4
                    C457.728,97.71,450.56,86.958,439.296,84.91z" />
                  </g>
                </g>
                <g>
                  <g>
                    <path d="M215.04,389.55c-1.024-28.16-24.576-50.688-52.736-50.688c-29.696,1.536-52.224,26.112-51.2,55.296
                    c1.024,28.16,24.064,50.688,52.224,50.688h1.024C193.536,443.31,216.576,418.734,215.04,389.55z" />
                  </g>
                </g>
              </svg>
            </a>
            <form class="form-inline">
              <button class="btn my-2 my-sm-0 nav_search-btn" type="submit">
                <i class="fa fa-search" aria-hidden="true"></i>
              </button>
            </form>
            <a href="#" class="order_online">
              Order Online
            </a>
          </div>
        </div>
      </nav>
    </div>
  </header>
</template>

<script>
import { useRoute } from "vue-router";

export default {
  setup() {
    const route = useRoute();
    return { route };
  }
};
</script>

<style scoped>
/* Background header */
header.header_section {
  background-color: rgb(27, 27, 27);
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1000;
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
}

/* Tambahkan padding atas untuk konten agar tidak tertutup navbar */
body {
  padding-top: 70px;
}

/* Styling menu */
.navbar-nav .nav-item {
  margin-right: 15px;
}

/* Warna default menu */
.navbar-nav .nav-item .nav-link {
  color: white;
  transition: 0.3s;
}

/* Menu aktif */
.navbar-nav .nav-item.active .nav-link {
  color: #ff9800; /* Warna oranye untuk menu aktif */
  font-weight: bold;
  border-bottom: 2px solid #ff9800;
}
</style>
