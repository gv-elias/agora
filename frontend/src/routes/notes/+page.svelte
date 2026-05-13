<script>
	let numbers = $state([1, 2, 3, 4]);

	function addNumber() {
		numbers.push(numbers.length + 1);
	}

	let total = $derived(numbers.reduce((t, n) => t + n, 0));
</script>

<p>{numbers.join(' + ')} = {total}</p>

