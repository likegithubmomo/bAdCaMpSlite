<script>
    export let camp;
    import {campmarket} from "../stores/currentcamp.js"
    function handleClicky(){
        campmarket.set(camp)
        localStorage.setItem
        window.location.href = `http://localhost:5173/#/camp/${camp.id}`
    }
</script>

<div class="camp-widget" on:click={handleClicky} on:keydown={handleClicky}>
    <h3>{camp.name}</h3>
    <p>-------------------------------------------------</p>
    <p>{camp.description}</p>
</div>

<style>
    .camp-widget {
        width: 1000px;
        height: 300px;
        background-color: white;
        border-radius: 5px;
        cursor: pointer;
        color: black;
        padding-right: 10px;
        padding-left: 10px;
    }

    h3 {
        color: black;
        font-weight: 100;
    }

    .camp-widget:hover {
        box-shadow: rgba(50, 50, 93, 0.25) 0px 6px 12px -2px, rgba(0, 0, 0, 0.3) 0px 3px 7px -3px;
    }
</style>

