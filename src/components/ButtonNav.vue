<template>
  <button class="nav--button solid">
    {{ label }}
  </button>
</template>

<script>
export default {
  name: "ButtonNav",
  props: {
    label: String,
  },
}
</script>

<style lang="scss" scoped>
button.nav--button {
  margin: 0 10px;
  font-size: 20px;
  text-decoration: none;
  text-align: center;
  padding: 10px;
  color: white;
  background: rgba(0, 0, 0, 0.5);
  -webkit-box-shadow: -1px 1px 2px rgba(0, 0, 0, 0.4);
  box-shadow: -1px 1px 2px rgba(0, 0, 0, 0.4);
  border-radius: 2px;
  border: none;
  -webkit-transition: all 0.3s;
  -moz-transition: all 0.3s;
  transition: all 0.3s;
  &:hover {
    background: white;
    -webkit-box-shadow: none;
    box-shadow: none;
    cursor: pointer;
  }
  &:after {
    width: 100%;
    height: 0;
    top: 0;
    left: 0;
    background: #fff;
  }
  &:hover,
  :active {
    color: #0e83cd;
  }
  &:focus {
    outline-color: none;
  }
  &:hover:after,
  :active:after {
    height: 100%;
  }
}
</style>