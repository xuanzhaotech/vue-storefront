<template>
  <div class="button-outline uppercase px40 py15" :class="{ 
    light : color === 'light', 'brdr-white' : color === 'light', 'c-white' : color === 'light',
    dark : color === 'dark', 'brdr-black' : color === 'dark', 'c-black' : color === 'dark'
  }">
    {{ text }}
  </div>
</template>

<script>
export default {
  name: 'button-outline',
  props: {
    text: {
      type: String,
      required: true
    },
    color: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
.button-outline {
    font-size: 16px;
    border: 2px solid;
    display: inline-flex;
    cursor: pointer;
    font-weight: 400;
}
.light:hover {
    color: #000;
    background: white;
    border-color: white;
}
.dark:hover {
    color: white;
    background: #000;
    border-color: black;
}
</style>