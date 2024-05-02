<script>
    export let activePage = '';

    const pages = [
        { name: 'Home', path: '/' },
        { name: 'About Me', path: '/about' },
        { name: 'Projects', path: '/projects' }
    ];
</script>

<nav>
    <div class="logo">
        <img src="../src/assets/inits.svg" alt="Logo" style="width: 30px; height: 30px;" />
    </div>
    <ul class="nav-links">
        {#each pages as page}
            <li class={activePage === page.path ? 'active' : ''}>
                <a href={page.path}>{page.name}</a>
            </li>
        {/each}
    </ul>
</nav>

<style>
    /* Add your custom styles here */
</style>