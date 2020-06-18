<template>
  <b-container>
    <b-row
      ><b-col
        ><h1 class="text-center my-5">{{ titulo }}</h1></b-col
      ></b-row
    >
    <b-row>
      <b-col v-for="(personaje, index) in personajes" :key="index">
        <b-card
          :title="personaje.nombre"
          :img-src="personaje.imagen"
          :img-alt="personaje.nombre"
          img-top
          tag="article"
          class="mb-2"
        >
        </b-card>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import { mapState } from 'vuex'

export default {
  name: 'Inicio',
  components: {},
  computed: {
    ...mapState(['titulo', 'personajes'])
  }
}
</script>
