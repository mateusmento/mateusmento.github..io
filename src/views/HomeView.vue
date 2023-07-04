<script setup lang="ts">
import ArrowRight from '@/assets/ArrowRight.vue';

function url(path: string) {
  return new URL(path, import.meta.url).href;
}
</script>

<template>
  <main class="flx">
    <div class="left flx-vert w-100">
      <h2 class="logo-headline">
        Mateus<br/>Sarmento
      </h2>
      <div class="personal-description flx-vert">
        <div>A pragmatic software engineer with 4 years of experience in full stack development using agile practices and a wide range of technologies.</div>
        <button class="learn-more">
          Learn More <ArrowRight/>
        </button>
      </div>
    </div>
    <div class="right flx-vert w-100">
      <h1 class="main-headline">
        Agile,<br />
        Pragmatic,<br />
        Ready to<br />
        Contribute<br />
      </h1>
      <div class="glass-section flx-vert">
        <img class="me-photo" :src="url('../assets/me.png')"/>
        <button class="lets-talk">
          Let's Talk <ArrowRight/>
        </button>
      </div>
    </div>
  </main>
</template>

<style scoped>
main {
  width: 1365px;
  height: calc(100vh - 25px);
  margin: auto;
  background-image: url("../assets/home-bg.png");
  background-size: cover;
  /* background-position: center; */
  border-radius: 20px 20px 0 0;
}

.main-headline {
  color: white;
  font-weight: 600;
  --font-size: 64px;
  font-size: var(--font-size);
  line-height: calc(var(--font-size) + .2em);
  font-family: Plus Jakarta Sans;
  padding-top: 40px;
}

.glass-section {
  justify-content: space-between;
  height: 250px;
  padding: 40px;
  padding-top: 27px;
  border-top-left-radius: 13px;
  background-color: rgba(182, 201, 252, .3);
}

.me-photo {
  width: fit-content;
  height: 112px;
}

.logo-headline {
  color: white;
  font-weight: 600;
  --font-size: 24px;
  font-size: var(--font-size);
  line-height: calc(var(--font-size) + .2em);
  font-family: Plus Jakarta Sans;
  padding: 40px;
  padding-bottom: 0;
}

.personal-description {
  justify-content: space-between;
  color: white;
  /* font-weight: 600; */
  --font-size: 24px;
  font-size: var(--font-size);
  line-height: calc(var(--font-size) + .4em);
  font-family: Plus Jakarta Sans;
  padding: 40px;
  height: 250px;
  box-sizing: border-box;
  font-family: Manrope;
}

.learn-more {
  width: 250px;
  padding: 13px 27px;
  border-radius: 40px;
  color: black;
  font-size: 16px;
  font-weight: 600;
  font-family: Plus Jakarta Sans;
}

.lets-talk {
  width: 120px;
  padding-bottom: 13px;
  border-bottom: 2px solid white;
  background-color: transparent;
  color: white;
  font-size: 16px;
  font-weight: 600;
  font-family: Plus Jakarta Sans;
}

.left {
  justify-content: space-between;
}

.right {
  justify-content: space-between;
}
</style>
