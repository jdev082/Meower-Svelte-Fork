<script>
	import Modal from "../Modal.svelte";

	import {modalShown} from "../stores.js";

	if ("cr" in localStorage) {
	} else {
		$modalShown = true;
		localStorage.setItem("cr", "value");
	}
</script>

<Modal
	on:close={() => {
		$modalShown = false;
	}}
>
	<h2 slot="header">Client Reminder</h2>
	<div slot="default">
		<p>
			This is a reminder that this is an unofficial client developed by
			jdev082. Please do not contact Meower Media, or Meower developers
			about issues related to this client. If you are unaware if an issue
			is client or server, please try using the official meower client.
		</p>
		<br />
		<div class="modal-buttons">
			<a href="https://app.meower.org" target="_blank">Official Client</a>
			<button
				on:click={() => {
					$modalShown = false;
				}}>Close</button
			>
		</div>
	</div>
</Modal>
