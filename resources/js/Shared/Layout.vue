<template>
    <section class="py-3 px-2 bg-indigo-100">
        <header class="">
            <Nav />
            <input type="text" value="My App">
        </header>
    </section>

    <section class="p-8">
        <div class="max-w-3xl mx-auto">
            <slot />
        </div>
    </section>
</template>

<script>
    import Nav from '../Shared/Nav'

    export default{
        components:{ Nav }
    };
</script>
