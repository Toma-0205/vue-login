<template>
    <div>
      <h2>登録</h2>
      <label for="email">Email：</label>
      <input v-model="email" type="email" id="email">
      <br>
      <br>
      <label for="password">Password：</label>
      <input v-model="password" type="password" id="password">
      <br><br>
      <button @click="register">送信</button>
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
        register(){
            this.$store.dispatch('resister', {
                email: this.email,
                password: this.password
            });
        this.email = "";
        this.password = "";
        }
    }
};
</script>