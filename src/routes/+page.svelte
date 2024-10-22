<script lang="ts">
	class Temparature {
		#celcius = $state(0);
		#fahrenheit = $state(0);

		get celcius() {
			return this.#celcius;
		}

		set celcius(newValue) {
			this.#celcius = newValue;
			this.#fahrenheit = newValue * (9 / 5) + 32;
		}

		get fahrenheit() {
			return this.#fahrenheit;
		}

		set fahrenheit(newValue) {
			this.#fahrenheit = newValue;
			this.#fahrenheit = (newValue - 32) * (5 / 9);
		}
	}

	const temparature = new Temparature();
</script>

<h1>Bi-directional temparature converter</h1>

<label for="celcius">Celcius</label>
<input id="celcius" type="number" bind:value={temparature.celcius} />

<div class="">=</div>

<label for="fahrenheit">Fahrenheit</label>
<input id="fahrenheit" type="number" bind:value={temparature.fahrenheit} />

<style>
</style>
