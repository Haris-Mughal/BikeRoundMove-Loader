# BikeRoundMove-Loader
This is a Loader for websites. 

# Code :

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Bike Round Rolling</title>
    <style>
      body {
  background: #000;
  overflow: hidden;
}
.centerBike {
  position: absolute;
  top: 50%;
  left: 50%;
  margin-top: 26px;
  margin-left: -12px;
}
.center {
  position: absolute;
  top: 50%;
  left: 50%;
  margin-top: -50px;
  margin-left: -50px;
}
#loop {
  height: 100px;
  width: 100px;
  border: #bb5f27 solid 4px;
  border-radius: 200px;
}
#loop:before {
  background: linear-gradient(
    to left,
    #bb5f2700 0%,
    #bb5f27 30%,
    #bb5f27 70%,
    #bb5f27 100%
  );
  content: "";
  display: block;
  height: 4px;
  left: -100px;
  position: relative;
  top: 100px;
  width: 300px;
}
#bike-wrapper {
  height: 108px;
  width: 108px;
  animation: drive 3s linear infinite;
}
#bike {
  height: 24px;
  width: 25px;
  background-image: url("https://s3-us-west-2.amazonaws.com/s.cdpn.io/133687/motorbike.png");
}
@keyframes drive {
  0% {
    margin-left: -364px;
    opacity: 0;
  }
  33.33% {
    transform: rotate(0deg);
    margin-left: -50px;
    opacity: 1;
  }
  66.66% {
    transform: rotate(-360deg);
    margin-left: -50px;
    opacity: 1;
  }
  100% {
    margin-left: 264px;
    transform: rotate(-360deg);
    opacity: 0;
  }
}
    </style>
  </head>
  <body>
    <div id="loop" class="center"></div>
    <div id="bike-wrapper" class="center">
      <div id="bike" class="centerBike"></div>
    </div>
  </body>
</html>


