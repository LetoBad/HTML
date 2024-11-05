<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contagem de Dias para o Aniversário</title>
</head>

<body>
    <em>Indique o seu proximo aniversario</em>
    <br>
    <input type="date" id="pesquisa">
    <button id="enviar">Enviar</button>
    <p id="paragrafo"></p>
    <br>
    <em>---------------------------------------------------</em>
    <br>
    <em>Ingrese o numero</em>
    <input type="number" id="number1">
    <br>
    <em>Ingrese quantas veces vai elevar o numero</em>
    <input type="number" id="number2">
    <br>
    <button id="enviar2">Enviar</button>
    <script>
        document.querySelector("#enviar").onclick = function () {
            var dataSelecionada = document.querySelector("#pesquisa").value;

            if (dataSelecionada) {
                var hoje = new Date();
                var aniversario = new Date(dataSelecionada);


                aniversario.setFullYear(hoje.getFullYear());


                if (hoje > aniversario) {
                    aniversario.setFullYear(hoje.getFullYear() + 1);
                }


                var msPorDia = 24 * 60 * 60 * 1000;
                var diasRestantes = Math.round((aniversario.getTime() - hoje.getTime()) / msPorDia);


                document.querySelector("#paragrafo").innerHTML = "Faltam " + diasRestantes + " dias para o seu aniversário!";
            } else {
                document.querySelector("#paragrafo").innerHTML = "Por favor, selecione a data do seu aniversário!";
            }
        }

    </script>
     <script>
        document.querySelector("#enviar2").onclick = function () {

            for(int i=0 ; number2 < i++ ){

            }
        }

    </script>
</body>

</html>
