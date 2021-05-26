# restaurante
<div id="app">
  <div ui-view></div>
</div>
...
<!DOCTYPE html>
<html lang="en">

<head>

  <meta charset="UTF-8">
  <title>Restaurante</title>

  <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">

  <script>
    angular.module("appRestaurante",[]);

        angular.module("appRestaurante").controller("cozinhaCtrl",function($scope) {

        });

        angular.module("appRestaurante").controller("recepcaoCtrl",function($scope) {


            $scope.clientes = [{nome: "Jorge"},
                               {nome: "Mateus"}];
            //Main functions__________________________________________
            $scope.adicionarCliente = function(cliente) {
                $scope.clientes.push(cliente.nome);
                console.log("action",$scope.clientes);
//                delete $scope.$4;
            }
        });



            //Functions________________________________________________


  </script>
</head>

<body ng-app="appRestaurante">
  <img class="img-responsive" src="https://png.pngtree.com/png-clipart/20200709/original/pngtree-restaurant-border-png-image_2331901.jpg">
  <div class="jumbotron">
    <h2>Restaurante TI</h2>
  </div>

  <div class="container">
    <h2>Clientes</h2>

    <table class="table" ng-controller="recepcaoCtrl">
      <thead>
        <tr>
          <th>CPF</th>
        </tr>
        <input type="passwordnome" ng-required ng-model="passwordnome" class="form-control" name="nome" placeholder="PasswordNome">
        <!-- SUBMIT BUTTON -->
        <button type="submit" class="btn btn-primary">Cadastrar</button>
        <form ng-controller="recepcaoCtrl">
      </thead>
      <tbody>
        <tr ng-repeat="cliente in clientes">
          <td>
            <input type="cpf" ng-required ng-model="passwordcpf" class="form-control" name="nome" placeholder="PasswordCPF">
            <!-- SUBMIT BUTTON -->
            <button type="submit" class="btn btn-primary">Cadastrar</button>
            <form ng-controller="recepcaoCtrl">
          </td>

        </tr>
      </tbody>
    </table>

  </div>


  <div
    ng-include="'/home/MatheusDeperon/Documentos/AngularJS/MatheusDeperon/Meu/angularJS/html/https://github.com/analistadeperon'">
  </div>



  <div class="container jumbotron">

    <h2>Adicionar</h2>

    <form ng-controller="cozinhaCtrl">
      <h3>Comida</h3>
      <div class="form-group">
        <input class="form-control"  placeholder="Nome"  ng-model="nomeComida">
      </div>
      <button type="submit" class="btn btn-primary">Adicionar</button>
      <!-- SUBMIT BUTTON -->
      <button type="submit" class="btn btn-primary">Cadastrar</button>
      <form ng-controller="recepcaoCtrl">
      </form>
      <h3>Cardapio</h3>
      <div class="form-group">
        <input class="form-control"  placeholder="Cardapio"  ng-model="Cardapio">
      </div>
      <button type="submit" class="btn btn-primary">Adicionar</button>
      <!-- SUBMIT BUTTON -->
      <button type="submit" class="btn btn-primary">Cadastrar</button>
      <form ng-controller="recepcaoCtrl">
        <h3>Couvert</h3>
        <div class="form-group">
          <input class="form-control"  placeholder="couvert" ng-model="couvert.nome">
        </div>
        <button type="submit" class="btn btn-primary" ng-click="adicionarTempero(tempero)">Adicionar</button>
        <!-- SUBMIT BUTTON -->
        <button type="submit" class="btn btn-primary">Cadastrar</button>
        <h3>Bebidas</h3>
        <input type="bebidas" ng-required ng-model="passwordbebidas" class="form-control" name="bebida" placeholder="bebida">
        <button type="submit" class="btn btn-primary" ng-click="adicionarbebida(bebida)">Adicionar</button>
        <!-- SUBMIT BUTTON -->
        <button type="submit" class="btn btn-primary">Cadastrar</button>
      </form>



  </div>



</body>

</html>
<html>

<head>
  <!-- load bootstrap css -->
  <link rel="stylesheet" href="http://netdna.bootstrapcdn.com/bootstrap/3.0.3/css/bootstrap.min.css">
  <style>
    body {
      padding-top: 30px;
    }
  </style>

  <!-- load angularJS -->
  <script src="http://code.angularjs.org/1.2.6/angular.js"></script>
  <script src="app.js"></script>
</head>

<!-- aplicar app angular e controlador para o nosso body -->

<body ng-app="validationApp" ng-controller="mainController">
  <div class="container">
    <div class="col-sm-8 col-sm-offset-2">

      <!-- PAGE HEADER -->
      <div class="page-header">
        <h1> Formulário do Cliente VIP</h1>
      </div>

      <!-- FORM -->
      <!-- passa a variável se nosso formulário é válida ou inválida -->
      <!-- novalidate isso vai evitar a validação padrão do HTML5, já que vamos fazer isso usando o Angular -->
      <form name="userForm" ng-submit="submitForm(userForm.$valid)" novalidate>

        <!-- NAME -->
        <div class="form-group">
          <label>Name</label>
          <input type="text" name="name" class="form-control" ng-model="name" required>
        </div>

        <!-- USERNAME -->
        <div class="form-group">
          <label>Username</label>
          <input type="text" name="username" class="form-control" ng-model="user.username" ng-minlength="3" ng-maxlength="8">
        </div>

        <!-- EMAIL -->
        <div class="form-group">
          <label>Email</label>
          <input type="email" name="email" class="form-control" ng-model="email">
        </div>
        <!-- TELEFONE -->
        <div class="form-group">
          <label>Telefone</label>
          <input type="teleofne" name="telefone" class="form-control" ng-model="telefone">
        </div>
        <!-- FAST FFOD -->
        <div class="form-group">
          <label>Fast Food</label>
          <input type="fast food" name="fast food" class="form-control" ng-model="fast food">
        </div>
        <!-- EMAIL -->
        <div class="form-group">
          <label>Email</label>
          <input type="email" name="email" class="form-control" ng-model="email">
          <!-- FORMA PAGAMENTO -->
          <div class="form-group">
            <label>Forma de pagamento</label>
            <input type="forma pagamento" name="forma pagamento" class="form-control" ng-model="forma pagamento">
            <label>Debito</label>
            <div class="form-group" ng-class="{ 'has-error': form.senha.$invalid && !form.senha.$pristine }">
              <label for="exampleInputPassword1">Senha</label>
              <input type="digite senha" ng-required ng-model="password" class="form-control" name="senha" placeholder="digite a senha">
            </div>
            <label>Credito</label>
            <div class="form-group" ng-class="{ 'has-error': form.senha.$invalid && !form.senha.$pristine }">
              <label for="exampleInputPassword1">Senha</label>
              <input type="digite senha" ng-required ng-model="password" class="form-control" name="senha" placeholder="digite a senha">
            </div>
            <label>Dinheiro</label>
            <div class="form-group" ng-class="{ 'has-error': form.senha.$invalid && !form.senha.$pristine }">
              <label for="exampleInputPassword1">A vista</label>
              <input type="vista" ng-required ng-model="password" class="form-control" name="a vista" placeholder="valor pago">
            </div>
          </div>
          <!-- SUBMIT BUTTON -->
          <button type="submit" class="btn btn-primary">Cadastrar</button>
          <!-- SUBMIT BUTTON -->
          <button type="submit" class="btn btn-primary">Enviar</button>

      </form>
    </div><!-- col-sm-8 -->
  </div><!-- /container -->
</body>

</html>
<html ng-app="app">

<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css" />
  <script src="//code.jquery.com/jquery-1.12.0.min.js"></script>
  <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/js/bootstrap.min.js"></script>
  <script src="https://code.angularjs.org/1.4.9/angular.min.js"></script>

</head>

<body ng-controller="ClientController">
  <div class="navbar navbar-inverse navbar-fixed-top">
    <div class="container">
      <div class="navbar-header">
        <button type="button" class="navbar-toggle" data-toggle="collapse" data-target=".navbar-collapse">
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                </button>
      </div>
    </div>
  </div>

  <div class="container body-content" style="margin-top:100px;">

    <form name="form" ng-submit="createClient();" novalidate>
      analistadeperon@hotmail.com.AntiForgeryToken( 2021);
      <div class="form-group" ng-class="{ 'has-error': form.nome.$invalid && !form.nome.$pristine }">
        <label for="exampleInputEmail1">Nome Completo</label>
        <input type="text" required ng-model="name" class="form-control" name="nome" placeholder="Nome Completo">
      </div>
      <div class="form-group" ng-class="{ 'has-error': form.cpf.$invalid && !form.cpf.$pristine }">
        <label for="exampleInputEmail1">CPF</label>
        <input type="number" ng-required ng-model="cpf" class="form-control" name="cpf" placeholder="CPF">
      </div>
      <div class="form-group" ng-class="{ 'has-error': form.email.$invalid && !form.email.$pristine }">
        <label for="exampleInputPassword1">Email</label>
        <input type="email" ng-required ng-model="email" class="form-control" name="email" placeholder="Email">
      </div>
      <div class="form-group" ng-class="{ 'has-error': form.senha.$invalid && !form.senha.$pristine }">
        <label for="exampleInputPassword1">Senha</label>
        <input type="password" ng-required ng-model="password" class="form-control" name="senha" placeholder="Password">
      </div>
      <button class="btn btn-default btn-primary" ng-disabled="form.$invalid">Submit</button>
      <!-- SUBMIT BUTTON -->
      <button type="submit" class="btn btn-primary">Cadastrar</button>
    </form>
    <hr />
  </div>
  <script>
    angular.module("app", [])
            .controller("ClientController",["$scope", "$http", function ($scope, $http) {
                $scope.createClient = function () {
                   
                    if ($scope.form.$invalid)
                        return;
                    var data = {
                        name: $scope.name,
                        cpf: $scope.cpf,
                        email: $scope.email,
                        senha: $scope.password
                    }
                    $http.post('/home/createuser', data).then(function (response) {
                    });
                };
        }]);
  </script>
</body>

</html>
