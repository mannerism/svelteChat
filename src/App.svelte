<script>
  import { FirebaseApp, User } from "sveltefire";
  import firebase from "firebase/app";
  import "firebase/firestore";
  import "firebase/auth";
  import AuthForm from "./components/AuthForm.svelte";

  const firebaseConfig = {
    apiKey: "AIzaSyDcEJKKwOBAgq8Rd2KgL-UJWkD6pxfcjq4",
    authDomain: "svelte-chat-25a1f.firebaseapp.com",
    projectId: "svelte-chat-25a1f",
    storageBucket: "svelte-chat-25a1f.appspot.com",
    messagingSenderId: "365895790533",
    appId: "1:365895790533:web:c9220dae23c30f687d65ac",
    measurementId: "G-GBRPRH31CQ",
  };
  firebase.initializeApp(firebaseConfig);
</script>

<main class="container section">
  <FirebaseApp {firebase}>
    <User let:user let:auth>
      <div slot="signed-out">
        <AuthForm {auth} />
      </div>
    </User>
  </FirebaseApp>
</main>

<style>

</style>
