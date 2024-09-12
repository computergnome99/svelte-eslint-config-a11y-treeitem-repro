<script>
	import { page } from '$app/stores';
	let groupExpanded = false;
</script>

<nav aria-label="Example">
	<ul role="tree" aria-label="Example">
		<li role="none">
			<button
				role="treeitem"
				aria-expanded={groupExpanded}
				aria-owns="example-group"
				on:click={() => {
					groupExpanded = !groupExpanded;
				}}
			>
				Example 1
			</button>

			{#if groupExpanded}
				<ul role="group">
					<li role="none">
						<a href="item-1" role="treeitem" aria-selected={$page.route.id === 'item-1'}>
							Item 1
						</a>
					</li>
				</ul>
			{/if}
		</li>
	</ul>
</nav>
