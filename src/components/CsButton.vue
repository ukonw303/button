<template>
  <div>
    <button v-on:click="upFunction" class="btn btn-primary">LIKE {{lable}}</button>
    <button v-on:click="LoveFunction" class="btn btn-info ml-3">LOVE {{lable}}</button>
    <button v-on:click="downFunction" class="btn  btn-danger ml-3">DIS LINE {{lable}}</button>
    <button v-on:click="ResetFunction" class="btn btn-danger ml-3">RESET {{lable}}</button>
  </div>
</template>
<script>
export default {
  data: function () {
    return {
      counter: 0,
    };
  },
  props: {
    lable: String,
  },
  methods: {
    upFunction: function () {
      this.counter += 10;
      this.$emit("cc", this.counter);
    },

     LoveFunction: function () {
      this.counter += 15;
      this.$emit("cc", this.counter);
    },

    downFunction: function () {
      this.counter += -10;
      this.$emit("cc", this.counter);
    },

    ResetFunction: function () {
      this.counter = 0;
      this.$emit("cc", this.counter);
    },
  },
};
</script>
<style>
</style>