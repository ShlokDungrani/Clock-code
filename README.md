      <!DOCTYPE html>
      <html lang="en">

       <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=, initial-scale=">
       <title>Clock</title>
      <style>
      body {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: "Lato", sans-serif;
      }
      #clock {
      height: 100vh;
      width: 100%;
      background-color: #14080e;
      color: #e9eb9e;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 50px;
      }
      </style>
      </head>

      <body>
       <div id="clock">
       </div>
      <script>
      function clock() {
      let date = new Date();
      let hrs = date.getHours();
      let mins = date.getMinutes();
      let secs = date.getSeconds();
      let period = "AM";
    
      if (hrs == 0) hrs = 12;
      if (hrs > 12) {
        hrs = hrs - 12;
        period = "PM";
      }
    
      hrs = hrs < 10 ? `0${hrs}` : hrs;
      mins = mins < 10 ? `0${mins}` : mins;
      secs = secs < 10 ? `0${secs}` : secs;
    
      let time = `${hrs}:${mins}:${secs} ${period}`;
      setInterval(clock, 1000);
      document.getElementById("clock").innerText = time;
      }
    
      clock();

      </script>
     </body>

     </html>
