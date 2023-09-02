<script>
  import Navbar from "./lib/Navbar.svelte";
  import { initializeApp } from "firebase/app";
  import { firebaseConfig } from "./utils/firebaseConfig";
  import Home from "./pages/Home.svelte";
  import Login from "./pages/login.svelte";
  import SearchResults from "./lib/searchResults.svelte";

  import Router from "svelte-spa-router";
  import DynamicPage from "./pages/DynamicPage.svelte";
  const app = initializeApp(firebaseConfig);
</script>

<main>
  <Navbar />
  <Router routes={{
    "/": Home,
    "/search/:query":SearchResults,
    "/login":Login,
    "/camp/:id": DynamicPage
  }}/>
</main>

<style>
  main {
		position: relative;
		min-height: 98.5vh;
		background-size: cover;
    width: 100vw;
    height: 100vh;
	}
</style>
