<template>
  <div class="container">
    <header>LOGIN FORM</header>
    <form>
      <div class="input-field">
        <input type="text" placeholder="Email" required />
      </div>
      <div class="input-field">
        <input
          class="pass"
          :type='inputPassword'
          placeholder="Password"
          minlength="6"
          required
        />
        <span class="show" v-on:click= "show" >{{textShow}}</span>
      </div>
      <div class="button">
        <div class="inner"></div>
        <button type="submit">Login</button>
      </div>
    </form>
    <div class="signup">
      <a href="#">Sign Up</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "LoginForm",
  data(){
    return{
      textShow: 'Show',
      inputPassword:'password'
    }
  },
  created() {
    console.log(`ini terbuat`);
  },
  mounted() {
    console.log(`ini sudah di mounting`);
  },
  updated() {
    console.log(`element ini ke update`);
  },
  methods: {
    show() {
      if(this.inputPassword == 'password'){
        this.inputPassword = 'text'
        this.textShow = 'Hide'
      }else{
        this.inputPassword = 'password'
        this.textShow = 'Show'
      }
    },
    methodBaru(){
      console.log("method baru")
    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url("https://fonts.googleapis.com/css2?family=M+PLUS+Rounded+1c:wght@400;700&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap");

* {
  margin: 0;
  padding: 0;
  border-radius: 5px;
  box-sizing: border-box;
}

body {
  height: 100vh;
  display: flex;
  align-items: center;
  text-align: center;
  font-family: sans-serif;
  justify-content: center;
}

.container {
  position: relative;
  width: 400px;
  background: white;
  padding: 60px 40px;
}

header {
  font-size: 40px;
  font-weight: bold;
  margin-bottom: 50px;
  color: #0e6655;
  font-family: "M PLUS Rounded 1c", sans-serif;
}

.input-field,
form .button {
  margin: 15px 0;
  position: relative;
  height: 50px;
  width: 100%;
}

.input-field input {
  height: 100%;
  width: 100%;
  color: #0e6655;
  border: 2px solid #0e6655;
  padding-left: 20px;
  padding-right: 70px;
  outline: none;
  font-size: 18px;
  transition: all 0.3s ease;
}

input:focus {
  border: 2px solid #138d75;
  transition: all 0.3s ease;
}

span.show {
  position: absolute;
  top: 30%;
  right: 15px;
  color: #0e6655;
  font-size: 15px;
  font-weight: bold;
  cursor: pointer;
  user-select: none;
  visibility: hidden;
  font-family: "Roboto", sans-serif;
}

input:valid ~ span.show {
  visibility: visible;
}

form .button {
  margin-top: 50px;
  z-index: 11;
}

.button .inner {
  position: absolute;
  height: 100%;
  width: 100%;
  z-index: -1;
  transition: all 0.4s;
  background: #0e6655;
}

.button:hover .inner {
  left: 0;
  background: #138d75;
}

.button button {
  width: 100%;
  height: 100%;
  border: none;
  background: none;
  outline: none;
  color: white;
  font-size: 20px;
  cursor: pointer;
  font-family: "Roboto", sans-serif;
}

.signup {
  margin-top: 25px;
  font-family: "Roboto", sans-serif;
}

.signup a {
  color: #0e6655;
  text-decoration: none;
}

.signup a:hover {
  text-decoration: underline;
}
</style>
