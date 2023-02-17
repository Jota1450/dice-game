<script setup>
import Dices from './components/Dices.vue';
</script>

<template>
  <div class="container is-max-desktop">
    <section class="section">
      <div class="card">
        <div class="card-header">
          <div class="card-header-title">
            Dice Game
          </div>
        </div>
        <div class="card-content">
          <div class="content">
            <Dices />
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
@import "https://cdn.jsdelivr.net/npm/bulma@0.9.4/css/bulma.min.css";
</style>
