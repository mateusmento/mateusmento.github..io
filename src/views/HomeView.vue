<script setup lang="ts">
import ArrowRight from '@/assets/ArrowRight.vue';

const experiences = [
  {
    occupation: "Software Engineer",
    stack: "Java/Vue",
    company: "Blumar",
    period: "AGO 2019 to AGO 2022",
  },
  {
    occupation: "Software Engineer",
    stack: ".NET/Angular",
    company: "Minds at Work",
    period: "AGO 2018 to AGO 2019",
  },
  {
    occupation: "Software Engineer",
    stack: "Node.js/React",
    company: "Doctor SAC",
    period: "MAR 2018 to AGO 2018",
  },
]

function url(path: string) {
  return new URL(path, import.meta.url).href;
}
</script>

<template>
  <header class="jumbotron">
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
    <footer>
      <section class="experiences-section">
        <h3 class="experience-title">EXPERIENCES</h3>
        <div class="experiences">
          <div v-for="experience of experiences" :key="experience.period" class="experience">
            <div class="activity">
              <b>{{ experience.occupation }}</b>
              {{ experience.stack }}
            </div>
            <div class="work">
              <b>{{ experience.company }}</b>
              {{ experience.period }}
            </div>
          </div>
        </div>
      </section>
      <section class="skills-section">
        <div class="skills-presentation">
          <h3 class="skills-title">SKILLS</h3>
          <div class="skills-message">
            By leveraging open-source projects,
            <br/>I am able to efficiently deliver
            <br/> high quality software products.
          </div>
          <button class="see-skills-demos">
            See Skills & Demos <ArrowRight/>
          </button>
        </div>
        <div class="drop-gradient">
          <div class="skills">
            <div class="skill">Websites</div>
            <div class="skill">Microservices</div>
            <div class="skill">Mobile Apps</div>
            <div class="skill">Infrastructure</div>
            <div class="skill">Design Systems</div>
            <div class="skill">Real-time Data</div>
          </div>
        </div>
      </section>
    </footer>
  </header>
</template>

<style scoped>
/* 688 * 25 / 1012  */
header {
  display: flex;
  flex-direction: column;
  align-items: stretch;
  gap: 6px;
}

main {
  min-height: calc(100vh - 25px);
  background-image: url("../assets/home-bg.png");
  background-size: cover;
  border-radius: 20px 20px 0 0;
  gap: 6px;
}

footer {
  display: flex;
  min-height: 252px;
  gap: 6px;
}

.experiences-section, .skills-section {
  min-height: 252px;
  max-height: 252px;
}

.experiences-section {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  background: white;
  border-radius: 0 0 0 16px;
  padding: 27px 40px;
  font-size: 13px;
  width: 100%;
  background-image: url('../assets/experience-bg.webp');
  background-size: cover;
  background-position: center;
}

.experience-title {
  font-size: 21px;
  font-weight: 600;
  background-color: white;
  width: fit-content;
}

.experiences {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.experience {
  display: flex;
  justify-content: space-between;
}

.activity {
  background: var(--black);
  font-size: 16px;
  color: white;
}

.work {
  background: white;
}

b {
  font-weight: 600;
  font-size: 16px;
}

.skills-section {
  display: flex;
  justify-content: space-between;
  width: 100%;
  padding: 0 40px;
  min-height: 252px;
  background: var(--black);
  color: white;
  border-radius: 0 0 16px 0;
}

.skills-presentation {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding: 27px 0;
}

.skills-title {
  font-size: 32px;
  width: fit-content;
}

.skills {
  overflow: hidden;
  height: 100%;
}

.drop-gradient {
  position: relative;
}

.drop-gradient::before {
  content: '';
  pointer-events: none;
  position: absolute;
  display: block;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  width: 100%;
  background: linear-gradient(0deg, rgba(22, 22, 22, 0.00) 39.70%, rgba(22, 22, 22, 0.76) 70.96%, rgba(22, 22, 22, 0.78) 70.97%, #161616 100%);
}

.skill {
  font-size: 32px;
  font-weight: 600;
}

.see-skills-demos {
  background-color: transparent;
  color: white;
  padding-bottom: 16px;
  border-bottom: 2px solid white;
  font-family: Manrope;
  font-weight: 500;
  font-size: 16px;
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
  color: var(--black);
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
