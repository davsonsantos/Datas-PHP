# Classe workData 
Classe para manipulr datas em PHP

### Developers
* [Davson Santos] - Developer of this class!

** Plus One Blog Davson Santos, Make Good Use! **

[//]: #
[Davson Santos]: <mailto: contato@davsonsantos.com.br>
[Blog Davson Santos]: <https://www.davsonsantoscom.br>

<?php

include 'Datas.class.php';
$Datas = new workData;

echo "<h2>Trabalhando com datas</h2>";



$Datas->dataAtual();

echo "<hr>";

$DT = $Datas->DataExtenso('21-07-2018'); // dd/mm/YYYY; dd-mm-YYYY; YYYY-mm-dd
echo "{$DT['Week']}, {$DT['Day']} de {$DT['Month']} de {$DT['Year']}";

echo "<hr>";

$Data = ['dtStart' => '25/02/2015', 'dtEnd' => '2018-03-01'];
$Diff =  $Datas->deferencaDatas($Data);
var_dump($Diff);

echo "<hr>";

echo $Datas->add_dias_uteis('11/10/2018', 1);
 
echo "<hr>";
$Dados = ['Periodo' => 'Y', 'Data' => '01/06/2018', 'Valor' => '2'];
$R = $Datas->add_sub_dias($Dados);
echo $R;

echo "<hr>";

$S = $Datas->validateDate('21/05/2018');
echo $S;
?>
