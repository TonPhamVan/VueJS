<template>
  <base-modal 
  v-if="isShowModal"
  title="đây là modal" 
  content="đây là content"
  theme="wrong"
  @cancel="onToggleModal"
  />
  <button @click="onToggleModal">Toggle Modal</button>
</template>

<script>
import Modal from "./components/Modal.vue";
export default {
  name: "App",
  components: {
    BaseModal: Modal
  },
  data() {
    return {
      isShowModal: false,
    };
  },
  methods: {
    onToggleModal() {
      this.isShowModal = !this.isShowModal;
    }
  },
};
</script>

<style>

</style>
