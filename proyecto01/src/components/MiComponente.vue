  <template>
  <div id="mi-componente">
    <h3>{{ titulo }}</h3>
    <button v-on:click="counter += 1">Contador</button>
    <button id="destroyButton" class="btn btn-danger" v-on:click="onDestroyClick">Destroy</button>
    <p>Se ha hecho clic en el botón de arriba {{ counter }} veces.</p>
  </div>
</template>
  
  <script>
export default {
  name: "MiComponente",

  data() {
    return {
      titulo: "Este es mi nuevo componente",
      counter: 0,
    };
  },

  beforeCreate() {
    console.log("1 - beforeCreate");
  },
  created() {
    // Al crear los métodos, observadores y eventos
    console.log("2 - created");
  },
  beforeMount() {
    // Se ejecuta antes de insertar el DOM
    console.log("3 - beforeMount");
  },
  mounted() {
    // Se ejecuta al insertar el DOM
    console.log("4 - mounted");
  },
  beforeUpdate() {
    // Se ejecuta al detectar un cambio
    console.log("5 - beforeUpdate");
  },
  updated() {
    // Se ejecuta al realizar los cambios
    console.log("6 - updated");
  },
  beforeDestroy() {
    // Se ejecuta antes de destruir la instancia
    console.log("7 - beforeDestroy");
  },
  destroyed() {
    // Se ejecuta al destruir toda la instancia
    console.log("8 - destroyed");
  },
  
  methods: {
    onDestroyClick: function () {
      this.$destroy();
    },
  },

};
</script>