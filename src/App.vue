<template>
  <div class="m-5">
    <div class="border box p-2 mb-3">
      <h1 class="fs-3 m-4">Футы в метры</h1>
      <div class="row ms-4">
        <div class="col">
          <div class="d-flex">
            <p class="fs-4 me-2">Футы:</p>
            <!--Поле для ввода и вывода ед. Футов -->
            <input v-model="feet" @input="convertToMeter" class="input-site border fs-4 p-2 w-100" type="text">
          </div>

        </div>
        <div class="col">
          <div class="d-flex">
            <p class="fs-4 me-2">Метр:</p>
            <!--Поле для ввода и вывода ед. Метров -->
            <input v-model="meter" @input="convertToFeet" class="input-site border fs-4 p-2 w-100" type="text">
          </div>

        </div>
      </div>
    </div>



    <div class="border box p-2 mb-3">
      <h1 class="fs-3 m-4">Мили в километры</h1>
      <div class="row ms-4">
        <div class="col">
          <div class="d-flex">
            <p class="fs-4 me-2">Мили:</p>
            <!--Поле для ввода и вывода ед. Миль -->
            <input v-model="mile" @input="convertToKilometer" class="input-site border fs-4 p-2 w-100" type="text">
          </div>

        </div>
        <div class="col">
          <div class="d-flex">
            <p class="fs-4 me-2">Километр:</p>
            <!--Поле для ввода и вывода ед. Километров -->
            <input v-model="kilometer" @input="convertToMile" class="input-site border fs-4 p-2 w-100" type="text">
          </div>

        </div>
      </div>
    </div>


    <div class="border box p-2 mb-3">
      <h1 class="fs-3 m-4">Градусы в радианы</h1>
      <div class="row ms-4">
        <div class="col">
          <div class="d-flex">
            <p class="fs-4 me-2">Градусы:</p>
            <!--Поле для ввода и вывода ед. Градусов -->
            <input v-model="degree" @input="convertToRadian" class="input-site border fs-4 p-2 w-100" type="text">
          </div>

        </div>
        <div class="col">
          <div class="d-flex">
            <p class="fs-4 me-2">Радианы:</p>
            <!--Поле для ввода и вывода ед. Радиан -->
            <input v-model="radian" @input="convertToDegree" class="input-site border fs-4 p-2 w-100" type="text">
          </div>

        </div>
      </div>
    </div>

    <div class="border box p-2 mb-3">
      <h1 class="fs-3 m-4">C в F</h1>
      <div class="row ms-4">
        <div class="col">
          <div class="d-flex">
            <p class="fs-4 me-2">C:</p>
            <!--Поле для ввода и вывода ед. Цельсий -->
            <input v-model="celsius" @input="convertToFahrenheit" class="input-site border fs-4 p-2 w-100" type="text">
          </div>

        </div>
        <div class="col">
          <div class="d-flex">
            <p class="fs-4 me-2">F:</p>
            <!--Поле для ввода и вывода ед. Фаренгейта -->
            <input v-model="fahrenheit" @input="convertToCelsius" class="input-site border fs-4 p-2 w-100" type="text">
          </div>

        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  // Исходные данные + константы для перевода единиц
  data() {
    return {
      feet: 0,
      meter: 0,
      fToM: 3.28,
      mile: 0,
      kilometer: 0,
      mToK: 1.85,
      degree: 0,
      radian: 0,
      rToD: 57.3,
      celsius: 0,
      fahrenheit: 0,
      fToC: 33.8,
    }
  },
  // Методы перевода из одних ед. в другие
  methods: {
    convertToMeter() {
      this.meter = this.feet / this.fToM;
    },
    convertToFeet() {
      this.feet = this.meter * this.fToM;
    },
    convertToMile() {
      this.mile = this.kilometer / this.mToK;
    },
    convertToKilometer() {
      this.kilometer = this.mile * this.mToK;
    },
    convertToDegree() {
      this.degree = this.radian * this.rToD;
    },
    convertToRadian() {
      this.radian = this.degree / this.rToD;
    },
    convertToCelsius() {
      this.celsius = this.fahrenheit / this.fToC;
    },
    convertToFahrenheit() {
      this.fahrenheit = this.celsius * this.fToC;
    },
  }
}
</script>

<style scoped>
.box {
  width: 900px;
}

.input-site {
  height: 35px;
  border-radius: 3px;
}
</style>