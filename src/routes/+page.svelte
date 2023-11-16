<script>
    import "../global.css";
    import Partner from "$lib/components/partner.svelte";

    export let data;
</script>

<section>
    {#each data.websites as website}
        <Partner {website} />
    {/each}
</section>

<style>
    section {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(20em, 1fr));
        gap: 1em;
        margin: 1em;
    }
</style>
