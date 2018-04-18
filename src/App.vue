<template>
<div id="app">
    <div class="panel-body">
	<table class="table table-striped">
      <thead>
        <tr>
          <th>Title</th>
          <th>Author</th>
        </tr>
      </thead>
	<tbody> 
	<tr v-for="book in books">
              <td><a v-bind:href="book.url">{{book.title}}</a></td>
              <td>{{book.author}}</td>
            </tr>
      </tbody>
    </table>
</div>
</div>
</template>
<script>
import Firebase from 'firebase'
let config = {
  apiKey: 'AIzaSyCgf8SSRbd_4yzsPtUPj67AkOBdpCgRFPA',
  authDomain: 'vuejs-fb288.firebaseapp.com',
  databaseURL: 'https://vuejs-fb288.firebaseio.com',
  projectId: 'vuejs-fb288',
  storageBucket: 'vuejs-fb288.appspot.com',
  messagingSenderId: '19889610700'}
let app = Firebase.initializeApp(config)
let db = app.database()
let booksRef = db.ref('books')
export default {
  name: 'App',
  firebase: {
    books: booksRef
  }
}
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
