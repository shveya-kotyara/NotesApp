<template>
  <div class="message">
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  props: {
    message: {
      type: String,
      required: true,
    },
  },
};
</script>

<style lang="scss" scoped>
    p {
        color: rgb(187, 87, 87)
    }
    .message {
        text-align: center;
        padding: 20px;
    }
</style>