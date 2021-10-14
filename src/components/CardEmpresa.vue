<template>
  <v-card>
    <v-card-title class="primary white--text"
      ><h2>{{ empresa }}</h2></v-card-title
    >
    <v-card-content>
      <v-container class="pa-3">
        <v-avatar
          v-show="mostrarAvatar"
          color="primary"
          size="56"
          class="mb-3"
        ></v-avatar>
        <p>Ótimo lugar para trabalhar. Gostei muito da experiência</p>
      </v-container>
    </v-card-content>
  </v-card>
</template>

<script>
export default {
  name: "CardEmpresa",
  props: {
    empresa: String,
  },
};
</script>
