# numeros-primos-
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="_css/estilo.css"/>
  <meta charset="UTF-8"/>
  
</head>
<body>
<div>
    <form method="get" action="parte02.php">
     Numero: <input type="number" name="num">
        <input type="submit" value="é primo?" />
        
    </form>    
</div>
</body>
</html>

##parte 2

<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="_css/estilo.css"/>
  <meta charset="UTF-8"/>
  <title></title>
</head>
<body>
<div>
    <?php

        $c= 1;
        $mult= 0;
        $num = isset($_GET["num"])?$_GET["num"]:0;
        echo "Analisando o numero $num <br/>";
        echo "Valores Multiplos";
        for ($c=1; $c<=$num; $c++) {
          $mod= $num%$c;

          if ($mod ==0 && $c >=1) {
            $mult++;
            echo "<span class='foco'>$c</span>";
          }
        }

            echo "<br/> Total de Multiplos: <span class='foco'>$mult</span>";
            if ($mult==2) {
              # code...
              echo "<br/>". "resultado:$num "."<span class ='foco'>"."Não é primo"."</span>";
            }

    ?>
    <br/> <a href="javascript:history.go(-1)"> Voltar <a/>
</div>
</body>
</html>
