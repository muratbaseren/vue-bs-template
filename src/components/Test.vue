<template>
  <div>
    <b-button v-b-modal.modal-1>Launch demo modal</b-button>

    <b-modal id="modal-1" :title="title">
      <p class="my-4">Hello from modal!</p>
    </b-modal>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "Test",
  props: { title: String },
  created() {
    axios
      .get("https://api.coindesk.com/v1/bpi/currentprice.json")
      .then(x => console.log(x.data));
  }
};
</script>

<style scoped></style>
