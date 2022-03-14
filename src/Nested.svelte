<script>
    export let count;

    let boomed = false;

    let imageSrc = "https://c.tenor.com/4MOc_udzsRQAAAAd/explosion.gif";

    $: if (count <= 0) {
        alert('The Boom is Exploded!');
        count = 0;
        boomed = true;
    }

    function handleClick() {
        count -= 1;
    }

</script>

<button on:click={handleClick}>
    Left {count} {count === 1 ? 'click' : 'clicks'}
</button>

{#if boomed}
    <div>
        <img src={imageSrc} alt="The boom exploded."/>
    </div>
{/if}