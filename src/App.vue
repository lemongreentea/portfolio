<script setup>
import AboutMe from './components/AboutMe.vue'
import Skills from './components/Skills.vue'
import Projects from './components/Projects.vue'
import Career from './components/Career.vue'
import NavBar from './components/NavBar.vue'
</script>

<template>
  <div id="app">
    <header class="header">
      <NavBar />
      <div class="header-content">
        <h1>SEOHUI's Portfolio</h1>
        <h3>박서희 개발자의 포트폴리오</h3>
        <p>항상 최선을 다하는 개발자가 되겠습니다.</p>
        <p>반응형 웹으로써 모바일과 웹 ui가 다를 수 있습니다.</p>
      </div>
    </header>
    <main>
      <section id="about-me">
        <AboutMe />
      </section>
      <section id="skills">
        <Skills />
      </section>
      <section id="projects">
        <Projects />
      </section>
      <section id="career">
        <Career />
      </section>
    </main>
    <footer class="footer">
      <p>&copy; 2024 SEOHUI. All rights reserved.</p>
      <p>Follow me on <a href="https://github.com/lemongreentea" target="_blank">GitHub</a></p>
    </footer>
  </div>
</template>

<!--<script>

export default {
  name: 'App',
  components: {
    AboutMe,
    Skills,
    Archiving,
    Projects
  }
}
</script>-->

<style scoped>
#app {
  text-align: center;
  font-family: 'Arial', sans-serif;
}

.header {
  background-image: url('@/assets/back.png');
  background-size: cover;
  background-position: center;
  color: white;
  height: 50vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  position: relative;
}

.header-content {
  position: relative;
  z-index: 1;
}

.header::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.5);
  z-index: 0;
}

.footer {
  background-color: #333;
  color: white;
  padding: 20px;
  text-align: center;
}
.footer a {
  color: #ff5722;
  text-decoration: none;
}
.footer a:hover {
  text-decoration: underline;
}
</style>
