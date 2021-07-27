<template>
  <div id="app">
    <h1 class="text-center">Tabla de Usuario</h1>
    <div class="container">
      <table class="table table-striped">
        <thead>
          <tr>
            <th scope="col">Nombre</th>
            <th scope="col">Apellido</th>
            <th scope="col">Run</th>
            <th scope="col">Fecha de Nacimiento</th>
            <th scope="col">Edad</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="dato in datos" v-bind:key="dato">
            <th scope="row">{{ dato.nombre }}</th>
            <td>{{ dato.apellido }}</td>
            <td>{{ dato.run }}</td>
            <td>{{ dato.nacimiento }}</td>
            <td>{{ dato.edad }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",

  data() {
    return {
      datos: [
        {
          nombre: "Jose",
          apellido: "Pérez",
          run: "123456-2",
          nacimiento: "12-04-1967",
          edad: 52,
        },

        {
          nombre: "María",
          apellido: "rodriguez",
          run: "654321-1",
          nacimiento: "30-11-1990",
          edad: 29,
        },

        {
          nombre: "Manuel",
          apellido: "Patiño",
          run: "14223456-6",
          nacimiento: "02-03-1959",
          edad: 60,
        },
      ],
    };
  },
};
</script>
