<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <div class="wrapper">
    <h1>
      My Work
    </h1>
    <div class="imageWrap">
      <div v-for="n in 6" :key="n">
        <img src="~/assets/laptop.jpg" alt="laptop">
      </div>
      <p>DUDE Project</p>
    </div>
  </div>
    </v-col>
  </v-row>
</template>

<script>
// eslint-disable-next-line import/no-named-as-default
import gsap from 'gsap'
export default {
  name: 'WorkPage',
  mounted () {
    gsap.to('.wrapper', {
      opacity: 1,
      duration: 1.5,
      ease: 'power2.in'
    })
    gsap.to('h1', {
      opacity: 1,
      duration: 1.5,
      delay: 0.3,
      y: 0,
      ease: 'power2.in'
    })
    gsap.to('.imageWrap', {
      opacity: 1,
      duration: 1.5,
      delay: 0.6,
      y: 0,
      ease: 'power2.in'
    })
  }
}
</script>

<style scoped>
  .wrapper {
    height: 100vh;
    width: 100vw;
    background-color: black;
    opacity: 0;
  }

  h1 {
    font-size: 5em;
    padding: 20px;
    color: white;
    font-family: 'Montserrat';
    text-transform: uppercase;
    opacity: 0;
    transform: translateY(30px);
  }

  .imageWrap {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    opacity: 0;
    transform: translateY(30px);
  }

  img {
    object-fit: cover;
    height: 70vh;
  }
</style>
