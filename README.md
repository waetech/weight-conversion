# weight-conversion
This is a simple weight conversion app.
<!DOCTYPE HTML>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <meta http-equiv="X-UA-Compatible" content="ie=edge">
        <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-alpha.6/css/bootstrap.min.css" integrity="sha384-rwoIResjU2yc3z8GV/NPeZWAv56rSmLldC3R/AZzGRnGxQQKnKkoFVhFQhNUwEyJ" crossorigin="anonymous">
        <title>Weight Converter</title>
   <style>
       body{
           margin-top:70px;
           background: #333;
           color: #fff;
           
       }
        </style>
    </head>
    
  <body>
      <div class="container">
      <div class="row">
          <div class="col-md-6 offset-md-3">
              <h1 class="display-4 text-centermb-3">Weight Converter</h1>
              <form>
              <div class="form-group">
                  <input id="lbsInput"
                         type="number" 
                         class="form-control form-control-lg" 
                         placeholder="Enter pounds">
                  </div>
              </form>
              <div id="output">
              <div class="card card-primary mb-2">
                  <div class="card-block">
                  <h4>Grams:</h4>
                      <div id="gramsOutput"></div>
                  </div>
                  </div>
                  
                  <div class="card card-success mb-2">
                  <div class="card-block">
                      <h4>Kilograms:</h4>
                      <div id="KgOutput"></div>
                  </div>
                  </div>
                  
                  <div class="card card-danger mb-2">
                  <div class="card-block">
                      <h4>Ounces:</h4>
                      <div id="ozOutput"><div>
                  </div>
                  </div>
                  
              </div>
          </div>
          </div>
      </div>
          <script>
              
             
         document.getElementById('lbsInput').addEventListener('input', function(e){
             document.getElementById('output').style.visibility = 'visible';
            
             let lbs= e.target.value;
              document.getElementById('gramsOutput').innerHTML = lbs/0.0022046;
              document.getElementById('kgOutput').innerHTML = (lbs/2.2046).toFixed(2);
              document.getElementById('ozOutput').innerHTML = lbs*16;
          });
          </script>
    
    </body>    
</html>
