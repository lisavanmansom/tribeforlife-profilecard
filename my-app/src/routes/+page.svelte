<script>
    export let data
</script>

<main>
    <header>
        <h1>{data.person.name}
            {data.person.surname}</h1>

        <picture>
            <source srcset="../Onderwerp-4?format=avif 500w" type="images/avif" sizes="(max-width: 1439px) 56vw, 40vw">
            <source srcset="../Onderwerp-4?format=webp 500w" type="images/webp" sizes="(max-width: 1439px) 56vw, 40vw">
            <img src="../Onderwerp-4.png" 
            width="250" height="250"  alt="" loading="auto">
        </picture>

        <div class="item-1"></div>
        <div class="item-2"></div>
        <div class="item-3"></div>
        <div class="item-4"></div>
    </header>

    <section>
        <h2>About me</h2>
        <p>I am Lisa, a netherland based frontend designer. I am keen on funky websites, animations, eclastic designs, literature and art.</p>
        <p>Likes / a clockwork orange / earth, wind and fire / bibimbap / Zoolander / concerts / gin tonics </p>
        <p>Dislikes / insects / george orwell's 1984 / anise lattes / cold weather </p>
    </section>
</main>

<style>

    main {
        background-color: var(--bkdkdkd);
        width: 100%;
        min-height: 100vh;
    }

</style>
