<script>
    import Main from '../components/main/main.svelte';
    import Sidebar from '../components/sidebar/sidebar.svelte';
</script>

<main>
    <div>
        <Sidebar />
    </div>
    <Main />
</main>

<style>
    main {
        display: flex;
        justify-content: space-between;
        align-items: center;

        transition: all 0.15s ease;
    }
    main > div:first-child {
        flex: 0;
    }
    main > div:last-child {
        flex: 0.75;
    }
</style>
