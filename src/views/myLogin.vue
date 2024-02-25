<template>
    <div>
      <h2>ログイン</h2>
      <label for="email">Email：</label>
      <input v-model="email" type="email" id="email">
      <br>
      <br>
      <label for="password">Password：</label>
      <input v-model="password" type="password" id="password">
      <br><br>
      <button @click="login">送信</button>
    </div>
</template>
  
<script>
export default{
    data(){
        return {
            email:"",
            password:"",
            };
    },
    methods:{
        login(){
            this.$store.dispatch('login', {
                email: this.email,
                password: this.password
            });      
            this.email = "";
            this.password = "";
        }
    }
};
</script>