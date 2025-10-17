<script>
    const { pokemon } = $props()
</script>

<article>
    <img src={pokemon.sprites.other['official-artwork'].front_default || pokemon.sprites.front_default} alt={pokemon.name}>
    <div class="info">
        <span class="pokemon-id">#{String(pokemon.id).padStart(3,'0')}</span>
        <h3 class="pokemon-name">{pokemon.name}</h3>
    </div>
</article>


<style>
    article{
        width: 180px;
        height: 240px;
        border: 2px solid grey;
        border-radius: 16px;
        padding: 16px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }

    .info{
        width: 100%;
        display: flex;
        flex-direction: column;
        gap: 12px;
    }

    h3{
        margin: 0;
        text-transform: capitalize;
    }

    img{
        max-height: 150px;
    }

</style>