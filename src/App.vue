<template>
  <v-app>
    <v-main>
      <AuthForm/>
    </v-main>
  </v-app>
</template>

<script>
import AuthForm from './components/AuthForm.vue';

export default {
  name: 'App',

  components: {
    AuthForm,
  },

  data: () => ({
    //
  }),
};
</script>

<style>
.v-main__wrap {
  //background: #020203;
  color: #F5F5F6;

  margin: 0;
  padding: 0;
  background-color: #020203;
  background-image: radial-gradient(circle at -50px -50px, rgba(250, 250, 250, 0.3) 0%, rgba(250, 250, 250, 0.15) 50px, rgba(250, 250, 250, 0) 800px),
  radial-gradient(circle at calc(100% + 50px) calc(100% + 50px), rgba(250, 250, 250, 0.3) 0%, rgba(250, 250, 250, 0.15) 50px, rgba(250, 250, 250, 0) 800px);
  background-size: 100% 100%;
  background-repeat: no-repeat;
  width: 100vw;
  height: 100vh;
}

</style>
