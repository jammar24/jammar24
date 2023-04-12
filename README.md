### Hi there 👋
<!DOCTYPE html>
<html>
<head>
	<title>Adivina el número</title>
</head>
<body>
	<h1>Adivina el número</h1>
	<p>Estoy pensando en un número entre 1 y 10. ¿Puedes adivinar cuál es?</p>
	<input type="number" id="guess">
	<button onclick="checkGuess()">Adivinar</button>
	<p id="message"></p>
	<script>
		let number = Math.floor(Math.random() * 10) + 1;
		let attempts = 0;

		function checkGuess() {
			let guess = parseInt(document.getElementById("guess").value);
			if (isNaN(guess) || guess < 1 || guess > 10) {
				document.getElementById("message").textContent = "Por favor ingresa un número válido entre 1 y 10.";
			} else if (guess === number) {
				attempts++;
				document.getElementById("message").textContent = `¡Felicidades! Adivinaste el número en ${attempts} intentos.`;
				document.getElementById("guess").disabled = true;
			} else {
				attempts++;
				let message = guess < number ? "El número que estoy pensando es mayor." : "El número que estoy pensando es menor.";
				document.getElementById("message").textContent = `${message} Intenta de nuevo.`;
			}
		}
	</script>
</body>
</html>
<!--
**jammar24/jammar24** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
