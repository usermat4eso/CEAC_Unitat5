<script setup type="text/javascript">
import vueLogo from './assets/logo.svg';
import githubLogo from './assets/github-mark.svg';
import githubLogoWhite from './assets/github-mark-white.svg';
</script>

<template>
  <router-view :quizzes="quizzes"></router-view>
  <hr />
  <p  style="display:none"  class="footer">
    
    Made by
    <a href="https://github.com/FluxCapacitor2/" target="_blank" rel="noopener noreferrer">
      <img src="https://avatars.githubusercontent.com/u/31071265" class="inline" />
      FluxCapacitor2
    </a>
    with
    <img :src="vueLogo" class="inline-sm" />
    <a href="https://vuejs.org" target="_blank" rel="noopener noreferrer">VueJS</a>
    &middot;
    <img :src="githubLogo" class="inline light-theme-only" />
    <img :src="githubLogoWhite" class="inline dark-theme-only" />
    <a href="https://github.com/FluxCapacitor2/WebQuiz" target="_blank" rel="noopener noreferrer">
      View Source Code
    </a>
  </p>
</template>

<script>
export default {
  data() {
    return {
      quizzes: [
      { subject: "APES", name: "Circulació de la correspondència", id: "circulació_correspondencia", resource: () => import("./assets/quiz/APES_Circulacio_Correspondencia.json"), },
        { subject: "APES", name: "Correspondència Entrada", id: "correspondencia_entrada", resource: () => import("./assets/quiz/APES_Correspondencia_Entrada.json"), },
        { subject: "APES", name: "Correspondència Eixida", id: "correspondencia_eixida", resource: () => import("./assets/quiz/APES_Correspondencia_Eixida.json"), },
        { subject: "APES", name: "Procediments Administració", id: "procediments_adminstracio_publica", resource: () => import("./assets/quiz/APES_Procediments_Administracio.json"), },
        { subject: "APES", name: "Serveis Correus", id: "serveis_correus", resource: () => import("./assets/quiz/APES_Serveis_Correus.json"), },
        { subject: "APES", name: "Administració Pública Electrònica", id: "administracio_publica_electronica", resource: () => import("./assets/quiz/APES_Administracio_Electronica.json"), },
        { subject: "APES", name: "Normes de confidencialitat", id: "normes", resource: () => import("./assets/quiz/APES_Normes.json"), }
       
      ],
    };
  }
};
</script>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

img.inline {
  height: 24px;
  vertical-align: text-bottom;
}

img.inline-sm {
  height: 20px;
  vertical-align: text-bottom;
}

hr {
  border: 2px solid var(--item-bg-color);
  margin: 10px 0;
}

.light-theme-only,
.dark-theme-only {
  display: none;
}

@media (prefers-color-scheme: dark) {
  .dark-theme-only {
    display: initial;
  }
}

@media (prefers-color-scheme: light),
(prefers-color-scheme: no-preference) {
  .light-theme-only {
    display: initial;
  }
}
</style>
