# barre-de-rechercher-google-avec-php-html5-sql
la balise dataliste

<!DOCTYPE HTML>
<html>

        <body>
              <input type="text" list="ki"/>
              <datalist id="ki">
              
                      <?php
                      
                      $db = New PDO('mysql:host=localhost;dbname=bassedonne','root','password',array(PDO::ATTR_ERRMODE => PDO:: ERRMODE_EXCEPTION));
                      
                      $sql="SELECT nom FROM employeur";
                      $resulta=$db->query($sql);
                      $data=$resulta->fetchAll(PDO::FETCH_ASSOC);
                      Foreach($data as $donne){?>
                      
                      <option> <?php echo $donne['nom'] ?> </option>
                      
                    <?php }  ?>
              </datalist>
        </body>


</html>
