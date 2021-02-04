<script>
  export let auth;
  let mode = "signIn";
  let email = "";
  let password = "";
</script>

<h1 class="title has-text-info has-text-centered">Svelte Chat</h1>
<h2 class="title">{mode == "signIn" ? "Sign In" : "Sign Up"}</h2>
<form>
  <div class="field">
    <label for="" class="label">Email</label>
    <input type="email" class="input" required bind:value={email} />
  </div>
  <div class="field">
    <label for="" class="label">Password</label>
    <input type="password" class="input" required bind:value={password} />
  </div>
</form>
