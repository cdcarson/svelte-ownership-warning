<script lang="ts">
	let data = $state({
		firstName: '',
		lastName: ''
	});
	let touched = $state({
		firstName: false,
		lastName: false
	});
</script>

<form>
	<div>
		<label for="firstName">First Name</label>
		<input
			type="text"
			name="firstName"
			id="firstName"
			bind:value={data.firstName}
			on:blur={() => (touched.firstName = true)}
		/>
	</div>
  <div>
		<label for="lastName">Last Name</label>
		<input
			type="text"
			name="lastName"
			id="lastName"
			bind:value={data.lastName}
			on:blur={() => (touched.lastName = true)}
		/>
	</div>
</form>
