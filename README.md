# Verificador_de_Idade

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> Verificador de idade</title>
    <link rel="stylesheet" href="./style.css">
</head>
<body>
    <div class="Container">
        <h1> Verificador de Idade</h1>
        <input type="number" id="idadeInput">
        <button onclick="VerificarIdade()"> Verificar </button>
        <p id="resultado"></p>
    </div>

    <script>
        function VerificarIdade(){
            const idade = parseInt(document.getElementById('idadeInput'). value);

            let mensagem="";

            if(isNaN(idade) || idade < 0){
            mensagem="Por favor insira uma idade válida ";
            }else if(idade < 18){
            mensagem="Você é menor de idade ";
            }else if(idade <60){
            mensagem="Você é Adulto";
            }else{
            mensagem="Você é idoso";
            }

            document.getElementById('resultado').innerText = mensagem
        }
    </script>
</body>
</html>

# Verificador_de_Idade

body{
    font-family: Arial, Helvetica, sans-serif;
    text-align: center;
    margin: 50px;
}

.Container{
    max-width: 400px;
    margin: auto;
    padding: 20px;
    border: 2px solid #333;
    border-radius: 10px;
}

input, button{
    margin: 10px;
    padding: 10px;
    font-size: 16px;
}
