<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
import Firebase from 'firebase'
let config = {
	apiKey: "AIzaSyCgf8SSRbd_4yzsPtUPj67AkOBdpCgRFPA",
    authDomain: "vuejs-fb288.firebaseapp.com",
    databaseURL: "https://vuejs-fb288.firebaseio.com",
    projectId: "vuejs-fb288",
    storageBucket: "vuejs-fb288.appspot.com",
    messagingSenderId: "19889610700"
  };
  
let app = Firebase.initializeApp(config)
let db = app.database()
let booksRef = db.ref('books')
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
