<template>
<h1>{{ title }}</h1>
<p>Have a look at our promotion</p>
<div v-if="showModal">
 <Modal theme="promomtion" @close="toggleModal">
 <template v-slot:links>
   <a href="#">Register</a>
   <a href="#">Find Out More</a>
 </template>
 <h1>Sindile Makhathini</h1>
 <p>Cone get your 50% discount now whilst stock last!</p>
 </Modal>
</div>
<button @click="toggleModel">Open Modal</button>
</template>

<script>
import Modal from "./components/Modal.vue";
export default {
  name: 'App',
  components: {
     Modal 
    },
  data() {
    return {
      title: 'Sindile Makhathini',
      header: 'Sign up to win a prize!',
      text: 'Come get your 50% discount now whilst stock last!',
      showModal: false
    }
  },
  methods: {
    toggelModal(){
      this.showModal = !this.showModal;
    }
    }
}
</script>

