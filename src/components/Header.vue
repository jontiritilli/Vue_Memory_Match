<template>
  <header id="header">
    <img class="logo logo--medium" alt="Vue logo" src="@/assets/logo.png" />
    <div class="btn--container">
      <ButtonNav v-for="label of buttonLabels" :key="label" :label="label" />
    </div>
  </header>
</template>

<script>
import ButtonNav from "./ButtonNav";

export default {
  name: "Header",
  components: {
    ButtonNav
  },
  data() {
    return {
      buttonLabels: [ "Home", "Play" ]
    }
  },
};
</script>

<style lang="scss">
  #header {
    display: flex;
  }
  .btn--container {
    width: 100%;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    justify-content: flex-end;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    margin-right: 20px;
  }
</style>
