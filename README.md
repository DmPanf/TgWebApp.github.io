## Tg Web APP Example


<!--
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

-->
