<template>
  <v-container>
    <v-container id="cards-container">
      <CardEmpresa
        color="white"
        class="mx-3"
        width="300"
        v-for="empresa in teste"
        :key="empresa"
        :empresa="empresa"
      >
      </CardEmpresa>
    </v-container>
    <v-text-field v-model="texto" label="Regular"></v-text-field>
    <v-btn @click="logarTexto">TESTE</v-btn>
  </v-container>
</template>

<script>
import CardEmpresa from "./CardEmpresa.vue";
export default {
  name: "HelloWorld",

  components: {
    CardEmpresa,
  },

  data: () => ({
    teste: ["Facebook", "Amazon", "Google", "Nubank"],
    mostrarAvatar: false,
    texto: "BATATA",
  }),

  methods: {
    logarTexto() {
      console.log(this.texto);
    },
  },
};
</script>

<style scoped>
#cards-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}
</style>
