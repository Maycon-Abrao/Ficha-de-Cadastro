<?php 
$nome = "João ";
$idade = 30;
$sexo = 'F';
$salarioMensal = 2210.30;
$estaEmpregado = false;
$habilidades = ['PHP, JavaScript, HTML, CSS'];

$situcaoEmprego = null;
if($estaEmpregado){
    $situcaoEmprego = 'Empregado';
} else {
    $situcaoEmprego = 'Desempregado';
}

 $anosNecessarioParaAposentar = null;
if($sexo == 'M'){
   $anosNecessarioParaAposentar = 65;
} else{
   $anosNecessarioParaAposentar = 62;
}

?>



<!DOCTYPE html>
<html lang="pt-br">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ficha de Cadastro</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .container {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100%;
        }

        .card {
            background: #fff;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            padding: 20px;
            max-width: 400px;
            text-align: center;
        }

        h1 {
            color: #333;
        }

        p {
            color: #666;
            font-size: 1.1em;
        }

        strong {
            color: #111;
        }
    </style>
</head>

<body>
    <div class="container">
        <div class="card">
            <h1>Ficha Cadastral</h1>
            <p>Nome: <strong><?= $nome; ?></strong></p>
            <p>Idade: <strong><?= $idade; ?></strong></p>
            <p>Sexo: <strong><?= $sexo; ?></strong></p>
            <p>Salário Mensal: <strong><?= $salarioMensal; ?></strong></p>
            <p>Salário Anual: <strong><?= $salarioMensal * 12; ?></strong></p>
            <p>Status de Emprego: <strong><?= $situcaoEmprego; ?></strong></p>
            <p>Anos para Aposentadoria: <strong><?= $anosNecessarioParaAposentar -$idade;?></strong></p>
            <p>Habilidades: <strong><?= implode( ', ', $habilidades)?></strong></p>
        </div>
    </div>
</body>

</html>
