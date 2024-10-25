<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Soma de Dois Números</title>
</head>
<body>
    <h2>Calculadora de Soma</h2>
    <p>Digite dois números para somar:</p>

    <input type="number" id="numero1" placeholder="Digite o primeiro número">
    <input type="number" id="numero2" placeholder="Digite o segundo número">
    <button onclick="somar()">Somar</button>

    <p id="resultado"></p>

    <script>
        function somar() {
            // Pega os valores dos inputs
            var num1 = parseFloat(document.getElementById("numero1").value);
            var num2 = parseFloat(document.getElementById("numero2").value);

            // Verifica se os números são válidos
            if (isNaN(num1) || isNaN(num2)) {
                document.getElementById("resultado").innerText = "Por favor, insira dois números válidos.";
                return;
            }

            // Calcula a soma
            var soma = num1 + num2;

            // Exibe o resultado na página
            document.getElementById("resultado").innerText = "A soma é: " + soma;
        }
    </script>
</body>
</html>
