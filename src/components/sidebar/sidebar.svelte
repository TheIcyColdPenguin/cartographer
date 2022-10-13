<script lang="ts">
    let collapsed = false;
</script>

<div class="container" class:collapsed>
    <div>side</div>
    <button on:click={() => (collapsed = !collapsed)}>☰</button>
</div>

<style>
    div.container {
        height: 100vh;

        display: grid;
        align-items: center;
        grid-template-columns: 20vw 5vw;

        color: black;

        z-index: 100;
        transition: all 0.15s ease;
    }

    div.container > div:first-child {
        height: 100vh;
        background-color: blanchedalmond;
    }

    div.container.collapsed {
        transform: translateX(-20vw);
    }

    button {
        align-self: start;
        background-color: transparent;
        color: white;
        border: none;
        font-size: large;
        font-weight: lighter;
        transition: all 0.1s ease-in;
    }

    button:hover,
    button:focus {
        outline: none;
        font-size: x-large;
        font-weight: bolder;
    }
</style>
