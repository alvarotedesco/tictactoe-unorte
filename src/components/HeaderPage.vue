<template>
  <section class="root-header-page">
    <nav class="w-full flex items-center">
      <div class="w-2/5 flex flex-wrap justify-around">
        <img class="w-[180px] min-h-[82px]" src="../assets/images/UNORTE_BRANCO.svg" alt="Logo UNORTE">
        <img class="w-[150px] min-h-[82px]" src="../assets/images/LAMPI_BRANCO.svg" alt="Logo LAMPI">
        <img class="w-[80px] min-h-[82px]" src="../assets/images/LER_BRANCO.svg" alt="Logo LER">
        <img class="w-[70px] min-h-[82px]" src="../assets/images/NIC_BRANCO.svg" alt="Logo NIC">
      </div>

      <div class="w-3/5 px-16 flex flex-wrap justify-between">
        <div class=" flex justify-center">
          <label class="text-white font-bold text-xl">Jogo da Velha</label>
        </div>

        <div class=" flex flex-wrap justify-center gap-8">
          <router-link :to="{name: 'home',}">
            <span>Página inicial</span>
          </router-link>

          <router-link :to="{name: 'matches',}">
            <span>Partidas</span>
          </router-link>
        </div>
      </div>
    </nav>
  </section>
</template>

<script>
import VButton from "../components/VButton.vue";

export default {
  name: "HeaderPage",

  components: {
    VButton,
  },

  props: {
    backButton: {type: Function, default: null,},
  },
};
</script>

<style lang="scss" scoped>
.root-header-page {
  width: 100%;
  color: transparent;
  border-bottom: 1px solid rgba(255, 255, 255, 0.3);

    a {
      color: #FFFFFF;
      text-decoration: none;

      &.router-link-exact-active, &.router-link-active {
      color: darkslateblue;
      text-decoration: underline;
    }
  }
}
</style>
