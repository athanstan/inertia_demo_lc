<template>

    <nav class='flex space-x-8 items-center justify-between'>
        <h1 class="text-2xl font-bold">My App</h1>
        <p>Welcome Back, {{ username }} </p>
        <ul class="flex space-x-4">
            <li>
                <Link href="/" class='text-blue-700 hover:underline' :class="{'font-bold underline': $page.component === 'Home'}">Home</Link>
            </li>
            <li>
                <Link href="/users" class='text-blue-700 hover:underline' :class="{'font-bold underline': $page.component === 'Users'}">Users</Link>
            </li>
            <li>
                <Link href="/settings" class='text-blue-700 hover:underline' :class="{'font-bold underline': $page.component === 'Settings'}">Settings</Link>
            </li>
            <li>
                <Link method='post' href="/logout" as="button" class='text-blue-700 hover:underline'>Log Out</Link>
            </li>
        </ul>
    </nav>

</template>

<script>

    import { Link } from '@inertiajs/inertia-vue3';

    export default {
        components: { Link },

        computed: {
            username() {
                return this.$page.props.auth.user.username;
            }
        }
    };
</script>
