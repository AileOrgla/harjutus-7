harjutus-7
==========
<!DOCTYPE HTML>
<html>
   <head>
    <title>Harjutus7</title>
    <meta http-equiv="Content-Type" content="text/html;
    charset=utf-8">
    <title>PHP põhitõed</title>
    <style type="text/css">
      .contact-table, td{
        border-collapse: collapse;
      }
      .contact-table, td{
        border: 1px solid red;
      }
      td{
        padding:10px;
      }
      .first-column{
        background-color: #ccc;
        font-weight: bold;
      }
    </style>
   </head>
   <body>
    <h2>While loop</h2>
      <?php
        $count = 10;

          while ($count <= 100) {
              echo $count . ", ";
              $count += 1;
          }
      ?>
      <br>
      <?php
         $count = 100;

          while ($count <= 1000) {
              echo $count . ", ";
             $count += 100;
          }
      ?>
    <h3>Infinitive while loop</h3>
      <?php
        $count = 1;

          //while ($count <= 10) {
             //echo $count; 
          //}
      ?>
    <h3>If statement in while loop</h3>
      <?php
        $count = 1;

          while ($count <= 10) {
             if ($count == 3) {
                echo "<script>alert('kolm');</script>";
              } 
              elseif ($count == 7) {
                echo "<script>alert('seitse');</script>";
              }
              else {
              echo $count;
            } 

          $count += 1;
         }
      ?>
    <h2>For loop</h2>
      <?php
          for ($count = 1; $count <= 20; $count += 1) {
            if ($count % 2 == 0) {
                echo "Number $count on paarisarv. <br>";
              } 
              elseif ($count % 2 == 1) {
                echo "Number $count on paaritu arv. <br>";
              } 
              $count % 2;
            }
      ?> 
    <h2>Foreach loop</h2>
      <?php
        $firms = array("DHL", "IBM", "INTEL", "HTC", "LEGO");
          echo "<ul>";
          foreach ($firms as $firm) {

                      echo "<li>".$firm."</li>"
                  ;
          }
          echo "</ul>";
        $subjects = array("Serveripoolsete veebirakenduste programmeerimine", "Arvutigraafika", "3D alused", "Veebiarendus", "Veebidisain");
                  $number = 1;
                  echo "<tr>";
                   foreach ($subjects as $subject) { 
                  echo "<td>".$number.". ".$subject."</td><br>";
                  $number += 1;
          }
         echo "</tr>";
      ?>
      <br>
            <?php
              $contact = array(
                  "first_name" => "Aile", 
                  "last_name" => "Orgla", 
                  "e-mail" => "aile.orgla@khk.ee",
                  "age" => 20
        );
            echo "<table class='contact-table'><tbody>";
                  foreach ($contact as $attribute => $value) {
                  $attribute_formatted = ucfirst(str_replace("_", " ", $attribute));
              echo "<tr><td class='first-column'>".$attribute_formatted."</td> "."<td>".$value."</td></tr>"; 
          };
            echo "</tbody></table>";
      ?>

   </body>
