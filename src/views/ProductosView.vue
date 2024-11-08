<template>
  <section class="container" id="productos">
    <h1 class="text-center">Producto</h1>
    <RouterLink class="d-flex justify-content-center" to="/">Volver al Inicio</RouterLink>
    <div class="row g-3 my-4">
      <div
      v-for="producto in productos"
        :key="producto"
        class="col-12 col-md-3">
        <Producto
          :nombre="producto.nombre"
          :precio="producto.precio"
          :descripcion="producto.descripcion"
          :cantidad="producto.cantidad"
        />
      </div>
    </div>
  </section>
</template>
<script>
import Producto from "../components/Producto.vue";
export default {
  components: {
    Producto,
  },
  data() {
    return {
      productos: [
        {
          nombre: "Desayuno",
          precio: 3000,
          descripcion: "El mejor desayuno de la ciudad",
          cantidad: "Para una persona",
        },
        {
          nombre: "Almuerzo",
          precio: 6000,
          descripcion: "El mejor almuerzo de la ciudad",
          cantidad: "Para una persona",
        },
        {
          nombre: "Cena",
          precio: 5000,
          descripcion: "La mejor cena de la ciudad",
          cantidad: "Para una persona",
        },
        {
          nombre: "Once",
          precio: 2000,
          descripcion: "La mejor once de la ciudad",
          cantidad: "Para una persona",
        },
      ],
    };
  },
};
</script>