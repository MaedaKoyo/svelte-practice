<script lang="ts">
    // import {onMount} from 'svelte'

    // type User = {
    //     name: string
    // };

    // let users: User[] = [];

    // onMount(async () => {
    //     const responce = await
    //     fetch('https://jsonplaceholder.typicode.com/users');
    //     users =  await responce.json();
    // });
    import type { PageData } from './$types';
    export let data: PageData;
</script>

<h1>ユーザ一覧</h1>
<ul>
	{#each data.users as user}
		<li><a href={`/user/${user.id}`}>{user.id}</a></li>
	{/each}
</ul>