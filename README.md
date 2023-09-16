<!DOCTYPE html>
<html lang="en" style="background-color: white">
<head>
    <meta charset="UTF-8">
    <title>Пример HTML страницы</title>
    <!-- Load the Telegram Library -->
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
    <!--Load the AngularJS Library-->
    <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.8.2/angular.min.js"></script>

    <script>
      //initialize the AngularJS stuff...
      angular.module("custom-webapp-ui", []).controller('CustomUIController', function CustomUIController($scope) {
        //init our slider values that we will display
        $scope.foods = [
                { name: "fruits", value: 5 },
                { name: "vegetables", value: 5 },
                { name: "meat", value: 5 },
                { name: "dairy", value: 5 }
            ];
        //initialize the button
        const mainButton = window.Telegram.WebApp.MainButton;
        mainButton.text = "Save Preferences";
        mainButton.enable();
        mainButton.show();
        // and make it send the "foods" object (as JSON string) back to the bot
        mainButton.onClick(function(){
          window.Telegram.WebApp.sendData(JSON.stringify($scope.foods));
        })
      });
    </script>
    
</head>
<body>    
  <div ng-repeat="food in foods">
    <div style="width: 100px; display: inline-block">{{food.name}} : {{food.value}}</div>
      <input style="display: inline-block" type="range" min="1" max="10" ng-model="food.value" value="{{food.value}}">
  </div>
  <div is="main">
    <h1>Заголовок страницы</h1>
    <img src="https://raw.githubusercontent.com/DmPanf/DokuWiki/main/images/00.jpg" alt="Пример картинки">
    <button id="start">START</button>
  </div>
</body>
</html>
