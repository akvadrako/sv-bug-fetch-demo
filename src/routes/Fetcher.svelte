<script>
    import { onMount } from 'svelte';

    let body = '...loading...';
    
    onMount(async () => {
        let resp = await fetch(`https://api.iconify.design/carbon.json?icons=sun`);
        body = JSON.stringify(await resp.json(), null, 4);
    })
</script>

<pre>{body}</pre>