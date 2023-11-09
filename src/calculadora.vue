<template>
    <div>
      <input v-model="numero1" type="number" @input="calcularResultado" />
      <select v-model="operacao" @change="calcularResultado">
        <option value="soma">+</option>
        <option value="subtracao">-</option>
        <option value="multiplicacao">*</option>
        <option value="divisao">/</option>
      </select>
      <input v-model="numero2" type="number" @input="calcularResultado" />
      <p>Resultado: {{ resultado }}</p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        numero1: 0,
        numero2: 0,
        operacao: "soma",
        resultado: 0,
      };
    },
    methods: {
      calcularResultado() {
        if (this.operacao === "soma") {
          this.resultado = this.numero1 + this.numero2;
        } else if (this.operacao === "subtracao") {
          this.resultado = this.numero1 - this.numero2;
        } else if (this.operacao === "multiplicacao") {
          this.resultado = this.numero1 * this.numero2;
        } else if (this.operacao === "divisao") {
          this.resultado = this.numero1 / this.numero2;
        }
      },
    },
  };
  </script>
  