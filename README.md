<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tarjeta<ESTAS GUAPO>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f0f0f0;
        }
        #card {
            display: none;
            padding: 20px;
            background-color: white;
            border: 1px solid #ddd;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        #codePrompt {
            text-align: center;
        }
    </style>
</head>
<body>
    <div id="codePrompt">
        <h2>Ingrese el código para ver la tarjeta</h2>
        <input type="text" id="codeInput" placeholder="Código">
        <button onclick="checkCode()">Enviar</button>
    </div>
    <div id="card">
        <h1>¡GUAPITO!</h1>
        <p>Este es un mensaje especial solo para ti.</p>
        <p>Que tengas un día maravilloso.</p>
    </div>

    <script>
        const correctCode = "12345"; // Cambia este código por el que desees

        function checkCode() {
            const userCode = document.getElementById("codeInput").value;
            if (userCode === correctCode) {
                document.getElementById("codePrompt").style.display = "none";
                document.getElementById("card").style.display = "block";
            } else {
                alert("Código incorrecto. Por favor, inténtelo de nuevo.");
            }
        }
    </script>
</body>
</html>
