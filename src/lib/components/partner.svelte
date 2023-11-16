<script>
    export let website

    import arrowRight from '$lib/assets/arrow_right.svg';

    const faviconAPI =
		'https://t1.gstatic.com/faviconV2?client=SOCIAL&type=FAVICON&fallback_opts=TYPE,SIZE,URL&url=';
</script>

<article class="website">
    <a href={website.slug}>
        <section class="logo-partner-section">
            <div>
                <img
                    height="60"
                    src="{faviconAPI}{website.homepage}/&size=128"
                    alt=""
                />
                <h2 class="name">{website.titel}</h2>
            </div>
            <img src={arrowRight} alt="arrow right" />
        </section>

        <section class="more-info-section">
            <span>Laatst bewerkt: 12 min. geleden</span>

            <div class="progress-container">
                <progress
                    id="progress-partner"
                    max="100"
                    value="0"
                />
                <label
                    class="progress-percentage"
                    for="progress-partner">0%</label
                >
            </div>
        </section>
    </a>
</article>

<style>
    article {
        display: flex;
    }
    
    article a {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        gap: 2.25em;
        color: var(--c-text);
        text-decoration: none;
        background-color: var(--c-container);
        padding: 1em;
        border-radius: 0.5em;
        border: solid 1px var(--c-container-stroke);
        width: 100%;
        transition: 0.25s ease;
    }

    article a:hover {
        border: solid 1px var(--c-pink);
    }
</style>
