<template>
  <div class="container">
    <h1>App banco</h1>
    <div class="row">
      <div class="col-6">
        <formulario></formulario>
        <button type="submit" @click="crearCuenta()" class="btn btn-primary">
          Crear Cuenta
        </button>
      </div>
      <div class="col-6">
        <h1>Listado de cuentas</h1>
        <br />
        <div class="row">
          <div class="col-6">
            <p>{{ nombreCompleto }}</p>
          </div>
          <div class="col-5">
            <button type="submit" class="btn btn-primary">Transferir</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import formulario from "../components/formulario.vue";

export default {
  components: { formulario },
  name: "appBanco",
  data() {
    return {
      formulario: [
        {
          cc: 123,
          nombreCompleto: "Juan Esteban Cano Marin",
          saldoInicial: 1000,
        },
      ],
      cc: 0,
      nombreCompleto: null,
      poder: null,
      saldoInicial: null,
    };
  },
  computed: {},
  methods: {
    CrearCuenta() {
      const nuevaCuenta = {
        cc: this.cc,
        nombreCompleto: this.nombreCompleto,
        saldoInicial: this.poder,
      };
      this.formulario.push(nuevaCuenta);
    },
  },
};
</script>
