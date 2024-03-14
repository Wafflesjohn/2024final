<script setup lang="ts">
import { RouterLink } from 'vue-router';
import { ref } from 'vue';

let isActive = ref(false);

function toggleMenu() {
  isActive.value = !isActive.value;
}

</script>

<template>
<nav class="navbar" role="navigation" aria-label="main navigation">
  <div class="navbar-brand">
    <a class="navbar-item" href="https://bulma.io">
      <img src="https://bulma.io/images/bulma-logo.png" width="112" height="28">
    </a>

    <a role="button" @click="toggleMenu" :class="{ 'is-active': isActive } " class="navbar-burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
    </a>
  </div>

  <div :class="{ 'is-active': isActive } " id="navbarBasicExample" class="navbar-menu"  >
    <div class="navbar-start">
      <RouterLink to="/" class="navbar-item">
        <img src="/assets/logo.da9b9095.svg" width="28">
      </RouterLink>

      <RouterLink to="/activity" class="navbar-item">
        <span class="icon">
            <i class="fas fa-running">
                ::before
            </i>
        </span>
        <span>My Activity</span>
      </RouterLink>

      <RouterLink to="/statistics" class="navbar-item">
        <span class="icon">
            <i class="fas fa-chart-line">
                ::before
            </i>
        </span>
        <span>Statistics</span>
      </RouterLink>

      <RouterLink to="/friends-activity" class="navbar-item">
        <span class="icon">
            <i class="fas fa-people-group">
                ::before
            </i>
        </span>
        <span>Friends Activity</span>
      </RouterLink>

      <RouterLink to="/people-search" class="navbar-item">
        <span class="icon">
            <i class="fas fa-search">
                ::before
            </i>
        </span>
            <span>People Search</span>
      </RouterLink>

      <div class="navbar-item has-dropdown is-hoverable">
        <a class="navbar-link">
          More
        </a>
    
        <div class="navbar-item has-dropdown is-hoverable">
            <a class="navbar-link">
                 Admin 
            </a>
            <div class="navbar-dropdown">
                <a href="/users" class="navbar-item">
                     Users 
                </a>
            </div>
        </div>

        <div class="navbar-dropdown">
          <RouterLink to="/about" class="navbar-item">
            About
          </RouterLink>
          <a class="navbar-item">
            Jobs
          </a>
          <a class="navbar-item">
            Contact
          </a>
          <hr class="navbar-divider">
          <a class="navbar-item">
            Report an issue
          </a>
        </div>
      </div>
    </div>

    <div class="navbar-end">
        <div class="navbar-item">
            <div class="buttons" data-v-1f0da592="">
                <a href="/signup" class="button is-primary" data-v-1f0da592="">
                    <strong data-v-1f0da592="">
                        Sign up
                    </strong>
                </a>
                <div class="dropdown" data-v-1f0da592="">
                    <div class="dropdown-trigger">
                        <button class="button" aria-haspopup="true" aria-controls="dropdown-menu">
                            <span data-v-1f0da592="">
                                Log in
                            </span>
                            <span class="icon is-small" data-v-1f0da592="">
                                <i class="fas fa-angle-down" aria-hidden="true" data-v-1f0da592="">
                                    ::before
                                </i>
                            </span>
                        </button>
                    </div>
                    <div class="dropdown-menu" id="dropdown-menu" role="menu">
                        <div class="dropdown-content">
                            <a class="dropdown-item" data-v-1f0da592="">
                                Moshe 
                            </a>
                            <a class="dropdown-item" data-v-1f0da592="">
                                 Kamala Harris 
                                </a>
                                <a class="dropdown-item" data-v-1f0da592="">
                                     John Smith 
                                </a>
                                <hr class="dropdown-divider" data-v-1f0da592="">
                                <a href="/login" class="router-link-active router-link-exact-active dropdown-item is-disabled" data-v-1f0da592="" aria-current="page">
                                     Other Account 
                                    </a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <messages></messages>
                <div class="navbar-item">
                    <a class="bd-tw-button button" data-social-network="Twitter" data-social-action="tweet" data-social-target="https://bulma.io" target="_blank" href="https://twitter.com/intent/tweet?text=Bulma: a modern CSS framework based on Flexbox&amp;hashtags=bulmaio&amp;url=https://bulma.io&amp;via=jgthms"><span class="icon">
                        <i class="fab fa-twitter">
                            ::before
                        </i>
                    </span>
                    <span>
                         Tweet 
                        </span>
                    </a>
                </div>
            </div>

    <div class="navbar-end">
      <div class="navbar-item">
        <div class="buttons">
          <a class="button is-primary">
            <strong>Sign up</strong>
          </a>
          <a class="button is-light">
            Log in
          </a>
        </div>
      </div>
    </div>
  </div>
</nav>
</template>

<style scoped>

    .router-link-active {
        border-bottom: 2px solid #00d1b2;
    }


</style>