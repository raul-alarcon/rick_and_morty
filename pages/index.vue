<template>
  <v-app>
    <v-app-bar app color=''>
      <div class='d-flex align-center'>
        <v-toolbar-title>Mi App</v-toolbar-title>
      </div>
      <v-spacer></v-spacer>
      <v-btn flat elevation='0'>Inicio</v-btn>
      <v-btn flat elevation='0'>Buscar</v-btn>
      <v-btn flat elevation='0'>Acerca de</v-btn>
    </v-app-bar>
    <v-main>
      <v-row>
        <v-col md='4' v-for='(personaje, index) in personajes' :key='index'>
          <v-card class='mx-auto' max-width='400'>
            <v-img class='white--text align-end' :src='personaje.imagen'>
            </v-img>
            <v-card-text>{{ personaje.nombre }}</v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'App',

  components: {},

  data: () => ({
    personajes: [
      {
        id: 1,
        nombre: 'Morty',
        imagen: 'https://rickandmortyapi.com/api/character/avatar/2.jpeg'
      },
      {
        id: 2,
        nombre: 'Rick',
        imagen: 'https://rickandmortyapi.com/api/character/avatar/1.jpeg'
      },
      {
        id: 3,
        nombre: 'Summer',
        imagen: 'https://rickandmortyapi.com/api/character/avatar/3.jpeg'
      },
      {
        id: 4,
        nombre: 'Beth',
        imagen: 'https://rickandmortyapi.com/api/character/avatar/4.jpeg'
      },
      {
        id: 5,
        nombre: 'Jerry',
        imagen: 'https://rickandmortyapi.com/api/character/avatar/5.jpeg'
      }
    ]
  })
}
</script>
