# ljaramilloh.github.io
<!doctype html>
<html lang="en">
<head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
    <!-- Bootstrap CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css"
          integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    <title>Covid</title>

  <style>

        body {
          font-family: Arial, Helvetica, sans-serif;
          padding-left: 10px;
        }

        header {
            font-size: 20px;
        }

        nav1 {
          float: left;
          width: 20%;
          height: 150px;
          background-color: White;
          padding: 20px;
        }

        .seltext {
            font-weight: bold;
        }

        .auxtext {
            font-size: 14px;
            color: #807F7F;
        }

    </style>


</head>
<body>
<h1><strong><FONT COLOR="Black">Covid 19 Colombia</FONT></strong></h1>
<div class="container">
    <div class="row">
        <div class="col-sm">
            <div class="card">
                <div class="card-body">
                    Infectados: <strong><span id="connected_users">0</span></strong>
                </div>
            </div>
        </div>
        <div class="col-sm">
            <div class="card">
                <div class="card-body">
                    Recuperados: <strong><span id="daily_revenue">0</span></strong>
                </div>
            </div>
        </div>
        <div class="col-sm">
            <div class="card">
                <div class="card-body">
                    Muertos: <strong><span id="daily_revenue2">0</span></strong>
                </div>
            </div>
        </div>
    </div>
</div>

</header>
  <hr>
    <nav1 style="border:1px solid Gainsboro; border-width:2px;">
      <p class="seltext">Ciudad:</p>
      <select id="region" name="region"  onchange="selectPlot()">
        <option value="casos_Colombia">Colombia</option>
        <option value="casos_Medellin">Medellín</option>
        <option value="casos_Bogota D.C.">Bogotá</option>
        <option value="casos_Cali">Cali</option>
        <option value="casos_Cartagena de Indias">Cartagena</option>
        <option value="casos_Barranquilla">Barranquilla</option>
      </select>
      
    </nav1>

    <div>
      <div class="myImage" id="casos_Colombia"   style="display:block"> <img src="figs/casos_Colombia.png"   alt="casos_Colombia">   </div>
      <div class="myImage" id="casos_Medellin"   style="display:none">  <img src="figs/casos_Medellin.png"   alt="casos_Medellin">   </div>
      <div class="myImage" id="casos_Bogota D.C."     style="display:none">  <img src="figs/casos_Bogota D.C..png"     alt="casos_Bogota D.C.">     </div>
      <div class="myImage" id="casos_Cali"   style="display:none">  <img src="figs/casos_Cali.png"   alt="casos_Cali">   </div>
      <div class="myImage" id="casos_Cartagena de Indias"  style="display:none">  <img src="figs/casos_Cartagena de Indias.png"  alt="casos_Cartagena de Indias">  </div>
      <div class="myImage" id="casos_Barranquilla"   style="display:none">  <img src="figs/casos_Barranquilla.png"   alt="casos_Barranquilla">   </div>
    </div>

    <script>
      function selectPlot() {
        var region = document.getElementById("region").value;
        var images = document.getElementsByClassName("myImage");
        for (var i = 0; i < images.length; i++) {
          if (images[i].id == region) {
            images[i].style.display = "block"
          }else{
            images[i].style.display = "none"
          }
        }
      }
    </script>

</body>
</html>
