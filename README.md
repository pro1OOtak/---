<!DOCTYPE html>
<html>

<body>

  <h3>Введите элементы массива через пробел</h3>
  <input id="mass1" placeholder="Первый массив">
  <input id="mass2" placeholder="Второй массив">
  <p>
    <button onclick="myFunction()">Выполнить</button>
  </p>

  <p id="exit1"></p>

  <script>

    function myFunction() {
      const mass1 = document.getElementById('mass1').value.split(' ');
      const mass2 = document.getElementById('mass2').value.split(' ');

      let result = [];
      mass1.forEach((el) => {
        result.push(+(mass2.indexOf(el) > -1))
      })
      document.getElementById('exit1').innerHTML = result.join(' ');
    }

  </script>

</body>

</html>
