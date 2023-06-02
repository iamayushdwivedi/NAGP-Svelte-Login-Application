<script>
  // Hardcoded login
  let isLoggedIn = false;
  let username = 'admin';
  let password = 'password';

  function handleLogin() {
    if (username === 'admin' && password === 'password') {
      isLoggedIn = true;
    } else {
      alert('Invalid credentials');
    }
  }
</script>



{#if isLoggedIn}
  <h1>File/Folder Management</h1>
  <iframe src="https://tiny-gumdrop-762825.netlify.app/"></iframe>
{:else}
  <h1>Login</h1>
  <div>
    <label for="username">Username:</label>
    <input type="text" id="username" bind:value={username} />
  </div>
  <div>
    <label for="password">Password:</label>
    <input type="password" id="password" bind:value={password} />
  </div>
  <button on:click={handleLogin}>Login</button>
{/if}
<style>
iframe {
  width: 80vw;
  height: 80vh;
  border: none;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>