<script>
// @ts-nocheck

 import Card from "../components/card.svelte";
 import Widget from "../components/widget.svelte";
</script>

<Card let:hovering>
	<span slot="name" >
			홍길동
	</span>

	<span slot="address">
			서울특별시 여의도동
	</span>
	<span slot="email">
			{#if hovering}
					<b>myemail@google.com</b> 
			{:else}
					myemail@google.com
			{/if}
	</span>
</Card>

<Widget>
	<h1 slot="header">Hello</h1>
	<svelte:fragment slot="footer">
			<p>All rights reserved.</p>
			<p>Copyright (c) 2019 Svelte Industries</p>
	</svelte:fragment>
</Widget>