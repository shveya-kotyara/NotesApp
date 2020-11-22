<template>
  <!-- new note -->
  <div class="new-note">
    <label>Title</label>
    <input v-model="note.title" type="text" />
    <label>Importance</label>
    <div class="importance">
      <p><input v-model="note.impor" type="radio" v-bind:value="false">Normal</p>
      <p><input v-model="note.impor" type="radio" v-bind:value="true">Danger</p>
    </div>
    <label>Description</label>
    <textarea v-model="note.descr"></textarea>
    <button class="btn btnPrimary" @click="addNote">New note</button>
  </div>
</template>

<script>
export default {
  props: {
    note: {
      type: Object,
      required: true,
    },
  },
  methods: {
    addNote() {
      this.$emit("addNote", this.note);
    },
  },
};
</script>

<style lang="scss">
.importance {
  display: flex;
  justify-content: center;
  input {
    width: 50px;
  }
}
.new-note {
  text-align: center;
}
</style>
