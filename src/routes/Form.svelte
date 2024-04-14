<script lang="ts">
  let data = $state({
    name: '',
  });
  let touched = $state({
    name: false,
  });
</script>

<form>
  <div>
    <label for="name">Name</label>
    <input
      type="text"
      name="name"
      id="name"
      bind:value={data.name}
      onblur={() => (touched.name = true)}
    />
  </div>
</form>
