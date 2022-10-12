<template>
  <div class="container">
    <div class="row">
      <div class="col-12">
        <form>
          <div class="mb-3">
            <h1>Creacion de cuenta</h1>
            <input
              v-model.number="cc"
              placeholder="Cedula"
              type="number"
              class="form-control"
            />
          </div>
          <div class="mb-3">
            <input
              v-model="nombreCompleto"
              placeholder="Nombre Completo"
              type="text"
              class="form-control"
            />
          </div>
          <div class="mb-3">
            <input
              v-model="saldoInicial"
              placeholder="Saldo inicial"
              type="number"
              class="form-control"
            />
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "formulario",

  props: {
    type: Object,
    default: () => {},
  },
};
</script>
