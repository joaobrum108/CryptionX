<template>
  <header class="header">
    <v-container class="header-conteudo">
      <div class="logo">
        CryptionX
      </div>

      <nav class="nav-links">
        <a href="#" class="nav-link">Product</a>
        <a href="#" class="nav-link">Pricing</a>
        <a href="#" class="nav-link">Docs</a>
      </nav>

      <v-btn class="header-cta" variant="outlined" size="default">
        Sign In
      </v-btn>
    </v-container>
  </header>
</template>

<script setup>
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300..800;1,300..800&display=swap');

.header {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 10;
  font-family: "Open Sans", sans-serif;
}

.header-conteudo {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1.75rem 2rem;
  max-width: 1400px;
}

.logo {
  color: #fff;
  font-size: 1.15rem;
  font-weight: 700;
  letter-spacing: -0.01em;
}

.nav-links {
  display: flex;
  gap: 2.25rem;
}

.nav-link {
  color: rgba(255, 255, 255, 0.65);
  font-size: 0.9rem;
  font-weight: 500;
  text-decoration: none;
  transition: color 0.2s ease;
}

.nav-link:hover {
  color: #fff;
}

.header-cta {
  font-family: "Open Sans", sans-serif;
  font-weight: 600;
  text-transform: none;
  letter-spacing: 0;
  border-radius: 8px;
  border-color: rgba(255, 255, 255, 0.3);
  color: #fff;
}

@media (max-width: 960px) {
  .nav-links {
    display: none;
  }
}
</style>