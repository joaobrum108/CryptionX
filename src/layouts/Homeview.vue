<template>
  <v-layout class="body">
    <Header />
    <v-main class="hero-section">
      <v-img class="imagem-estatica" :src="background" cover />

      <video
        ref="videoFundo"
        class="video-fundo"
        :class="{ 'video-visivel': videoCarregado }"
        autoplay
        muted
        loop
        playsinline
        preload="auto"
        :src="video"
      />

      <v-container class="conteudo ">
        <v-col cols="12" md="8" align="center">
          <h1>
            Own Your Digital Wealth With Confidence
          </h1>
          <p class="subtitulo">
            A premium all-in-one platform to manage, monitor, and optimize your digital assets with real-time analytics, secure transactions, and intelligent portfolio insights.
          </p>

          <v-btn class="cta-btn" size="x-large" elevation="0">
            Get Started Free
          </v-btn>
        </v-col>
      </v-container>
    </v-main>

  </v-layout>
</template>

<script setup>
import { ref, onMounted } from 'vue'

import background from '../assets/background.png'
import video from '../assets/Futuristic_space_background_anim…_202606222056.mp4'
import Header from '../components/Header.vue'

const videoFundo = ref(null)
const videoCarregado = ref(false)

onMounted(() => {
  if (videoFundo.value) {
    videoFundo.value.addEventListener('loadeddata', () => {
      videoCarregado.value = true
    })
  }
})
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300..800;1,300..800&display=swap');

h1 {
  color: #fff;
  font-family: "Open Sans", sans-serif;
  font-size: 3.5rem !important;
  font-weight: 700;
  line-height: 1.15;
  letter-spacing: -0.02em;
}

.subtitulo {
  color: rgba(255, 255, 255, 0.7);
  font-family: "Open Sans", sans-serif;
  font-size: 1.1rem;
  font-weight: 400;
  line-height: 1.6;
  margin-top: 1.25rem;
  margin-bottom: 2rem;
}

.cta-btn {
  font-family: "Open Sans", sans-serif;
  font-weight: 600;
  text-transform: none;
  letter-spacing: 0;
  padding: 0 2.5rem;
  border-radius: 8px;
  border: none;
  background: linear-gradient(135deg, #00d4b8 0%, #0099d4 100%);
  color: #fff;
  box-shadow: 0 4px 20px rgba(0, 180, 200, 0.35);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.cta-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 28px rgba(0, 180, 200, 0.5);
}

.body {
  width: 100%;
  display: flex;
  flex-direction: column;
}

.hero-section {
  position: relative;
  width: 100%;
  height: 100vh;
  height: 100svh;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: flex-start;
  padding: 14vh 5vw;
}

.imagem-estatica {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  z-index: -2;
}

.video-fundo {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
  opacity: 0;
  transition: opacity 0.6s ease;
  z-index: -1;
}

.video-visivel {
  opacity: 1;
}

.conteudo {
  position: relative;
  z-index: 1;
  justify-content: center;
  align-items: center;
}

@media (max-width: 960px) {
  .hero-section {
    padding: 10vh 4vw;
  }

  h1 {
    font-size: 2.5rem !important;
  }
}

@media (max-width: 600px) {
  .hero-section {
    padding: 6vh 4vw;
  }

  h1 {
    font-size: 1.9rem !important;
  }

  .subtitulo {
    font-size: 1rem;
  }
}
</style>