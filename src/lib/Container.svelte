<!--
	The typical Meower container, used literally everywhere.
-->

<div><slot /></div>

<style>
	div {
		background-color: var(--background);
		border: solid 1px var(--orange);
		border-radius: 10px;
		padding: 0.4em;
		margin-bottom: 0.2em;
		overflow-wrap: break-word;
		position: relative;
	}
</style>
