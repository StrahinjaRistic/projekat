<template>
  <div class="container">
  <div class="row">
    <div class="col-xs-12">
      <button class="plava" @click="selectedComponent = 'appBlue'">Blue Template</button>
      <button class="crvena" @click="selectedComponent = 'appRed'">Red Template</button>
      <button class="zelena" @click="selectedComponent = 'appGreen'">Green Template</button>
      <hr>
      <keep-alive>
          <component :is="selectedComponent">
              <p>Default Component</p>
          </component>
        </keep-alive>

    </div>
  </div>
</div>
</template>
</template>

<script>
import Blue from './components/Blue.vue';
import Red from './components/Red.vue';
import Green from './components/Green.vue';

export default {
  data: function()  {
    return {
      selectedComponent: 'appBlue'
    }
  },
  components: {
    appBlue: Blue,
    appRed: Red,
    appGreen: Green
  }

}
</script>

<style>
.plava {
  background-color: blue;
  font-size: 20px;
  color: white;
  border-radius: 12px;

}
.crvena {
  background-color: red;
  font-size: 20px;
  color: white;
  border-radius: 12px;
}
.zelena {
  background-color: green;
  font-size: 20px;
  color: white;
  border-radius: 12px;
}

</style>
