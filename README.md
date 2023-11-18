# Sistema-de-Notas
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> Sistema de Notas 1</title>
</head>
<body>
    <script>
        let notasTurma = [];
        let contAluno = 1;
        let soma = 0;
        let media = 0

        while(true){
            var nota = Number(prompt("Digite a nota do "+contAluno+"º  aluno: " ));
            if(nota < 0){
                break;
            }
            else{
                contAluno++;
                notasTurma.push(nota)
            }
       }

    for (let i of notasTurma) {
        soma = soma+i;
    }

    media = soma/notasTurma.length;
    document.write("A média da turma foi: "+media+"<br>");

    contAluno =0;
    for (let x of notasTurma) {
        if(x >= 6){
            var situacao = "Aprovação"
        }
        else if(x>=2 && x < 6){
            var situacao = "Prova final"
        }
        else{
            var situacao =" Reprovação"
        }
        contAluno++;
        document.write("a nota do "+(contAluno)+"º aluno é: "+x+" | Situação: "+situacao+"<br>");
    }


    </script>
</body>
</html>
