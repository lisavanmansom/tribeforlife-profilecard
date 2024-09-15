<script>
    export let data
</script>

<main>
    <header>
        <h1>{data.person.name}
            {data.person.surname}</h1>

        <picture>
            <source srcset="../Onderwerp-5?format=avif 500w" type="images/avif" sizes="(max-width: 1439px) 56vw, 40vw">
            <source srcset="../Onderwerp-5?format=webp 500w" type="images/webp" sizes="(max-width: 1439px) 56vw, 40vw">
            <img src="../Onderwerp-5.png" 
            width="250" height="250"  alt="" loading="auto">
        </picture>

        <div class="i-g-1">
            <div class="item-1"></div><div class="item-1"></div><div class="item-1"></div><div class="item-1"></div><div class="item-1"></div><div class="item-1"></div>
        </div>
        <div class="i-g-2">
            <div class="item-2"></div><div class="item-2"></div><div class="item-2"></div><div class="item-2"></div><div class="item-2"></div><div class="item-2"></div>
        </div>
        <div class="i-g-3">
            <div class="item-3"></div><div class="item-3"></div><div class="item-3"></div><div class="item-3"></div><div class="item-3"></div><div class="item-3"></div>
        </div>
        <div class="i-g-4">
            <div class="item-4"></div><div class="item-4"></div><div class="item-4"></div><div class="item-4"></div><div class="item-4"></div><div class="item-4"></div>
        </div>
            
    </header>

    <section>
        <h2>About me</h2>
        <p class="p-1">I am Lisa, a netherland based frontend designer. I am keen on funky websites, animations, eclastic designs, literature and art.</p>
        <p class="p-2"><span>Likes /</span> a clockwork orange / earth, wind and fire / bibimbap / Zoolander / concerts / gin tonics</p>
        <p class="p-3"><span>Dislikes /</span> insects / george orwell's 1984 / anise lattes / cold weather</p>

        <div class="item-5"></div>
        <div class="item-6"></div>
        <div class="item-7"></div>
    </section>
</main>

<style>

    main {
        width: 100%;
        min-height: 100dvh;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        overflow-y: hidden;

        background-image: url("/Mojave.jpg");
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
    }

    /* header styling */
    header {
        background-image: url("/tranquil-desert.png");
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;

        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: end;
        position: relative;
        overflow: hidden;
    }

    h1 {
        order: 0;
        font: italic 700 6em "ApexNewTrial", sans-serif;
        inline-size: 4.1em;
        text-align: center;
        color: var(--bat);
        -webkit-text-stroke-width: 1.5px;
        -webkit-text-stroke-color: var(--b);
        z-index: 110;
    }

    picture {
        order: -1;
        z-index: 10;
        margin: 0 -3em -20em 0;
        transform: scale(2.1);
    }

    img {
        height: 26em;
        width: 100%;
        object-fit: contain;
    }

    
    .i-g-1, .i-g-2,
    .i-g-3, .i-g-4 {
        width: 8em;
        height: 40em;
        display: flex;
        position: absolute;
    }

    .i-g-1 {
        animation: move1 infinite 2s;
        transform: matrix3d(            
            1,      0,     -0.87,   0,
            0,      -1,    0,       0.1,
            1,      0,     0.5,     0,
            4.98,   -50,     0,       11   );
    }

    .i-g-2 {
        animation: move2 infinite 2s;
        transform: matrix3d(                                
            1,      0,     -0.87,   0,
            0,      -1,    0,       1,
            1,      0,     0,     0,
            4.98,   -70,     0,       11   );
    }


    .i-g-3 {
        animation: move3 infinite 2s;
        transform: matrix3d(                                
            1,      10,     -0.87,   0,
            6,      5,    0,       0.1,
            1,      0,     0.5,     0,
            0,   0,     0,       8    );
    }

    .i-g-4 {
        animation: move4 infinite 2s;
        transform: matrix3d(                                
            1,      10,     -0.87,   0,
            -6,      5,    0,       0.1,
            1,      0,     0.5,     0,
            0,   0,     0,       8    );
    }


    .item-1, .item-2,
    .item-3, .item-4 {
        height: 100%;
        width: 10em;
        border: .15em solid var(--b);
    }



    @keyframes move1 {
        50% {
            transform: matrix3d(                                
            1,      0,     -0.87,   0,
            0,      -1,    0,       1,
            1,      0,     0,     0,
            4.98,   -70,     0,       11   );
        }
    }
    @keyframes move2 {
        50% {
            transform: matrix3d(                                
            1,      0,     -0.87,   0,
            0,      -1,    0,       0.1,
            1,      0,     0.5,     0,
            4.98,   -50,     0,       11    );
                }
    }
    @keyframes move3 {
        50% {
            transform: matrix3d(                                
                1,      10,     -0.87,   0,
            -6,      5,    0,       0.1,
            1,      0,     0.5,     0,
            0,   0,     0,       8    );
                }
    }
    @keyframes move4 {
        50% {
            transform: matrix3d(                                
                1,      10,     -0.87,   0,
            6,      5,    0,       0.1,
            1,      0,     0.5,     0,
            0,   0,     0,       8     );
                }
    }


    section {
        background-color: rgba(255, 255, 255, 0.14);
        color: var(--b);

        display: grid;
        grid-template-columns: repeat(20, 5%);
        grid-template-rows: repeat(20, 5%);
    }

    header, section {
        height: 40em;
        width: 75%;
        border: .21em solid var(--w);
    }

    /* secion styling */
    h2 {
        background: rgba(112, 164, 255, 0.75);
        font: italic 700 1.7em "ApexNewTrial", sans-serif;
        grid-column: 6 / 19;
        grid-row: 1 / 3;
        z-index: 15;
    }

    h2, p, section, header,
    .item-5, .item-6,
    .item-7 {
        border-radius: 16px;
        border: .1em solid var(--b);
        box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
        backdrop-filter: blur(13.6px);
        -webkit-backdrop-filter: blur(13.6px);
    }

    p {
        font: italic 300 1.5em "ApexNewTrial", sans-serif;
        color: var(--b);
    }

    p, h2 {
        padding: .15em 0 0 .15em;
    }

    span {
        font-weight: 400;
    }

    .p-1 {
        background: rgba(255, 161, 29, 0.75);
        grid-column: 10 / -1;
        grid-row: 4 / 15;
        z-index: 15;
    }

    .p-2 {
        background: rgba(150, 240, 254, 0.75);
        grid-column: 1 / 9;
        grid-row: 7 / 18;
        z-index: 20;
    }

    .p-3 {
        background: rgba(255, 83, 218, 0.75);
        grid-column: 7 / -1;
        grid-row: 16 / -1;
        z-index: 15;
    }

    .item-5 {
        background: rgba(56, 23, 221, 0.75);
        grid-column: 4 / 18;
        grid-row: 12 / 18;
    }

    .item-6 {
        background: rgba(255, 17, 0, 0.75);
        grid-column: 16 / 21;
        grid-row: 2 / 20;
    }

    .item-7 {
        background: rgba(255, 230, 0, 0.75);
        grid-column: 1 / 11;
        grid-row: 2 / 10;
    }

    @media (min-width:700px) {
        main {flex-direction: row;}
        header {width: 40%;}
        section {width: 40%;}
        h2 {font: italic 700 2.2em "ApexNewTrial", sans-serif;}
        p {font: italic 500 1.8em "ApexNewTrial", sans-serif;}
    }

</style>
