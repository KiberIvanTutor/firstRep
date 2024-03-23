 Я поделился с вами своим репозиторием!
Поздравляю с началом!
Вариантов много. Например, при нажатии на кнопку оператора, соответствующе устанавливаем переменную текущего оператора. Затем, при нажатии на кнопку равняется считаем результат в зависимости от текущего оператора.

<input id="num1" />

<div id="operator_btns">
  <button id="plus" class="operator" onclick="op='+'">+</button>
  <button id="minus" class="operator" onclick="op='-'">-</button>
  <button id="times" class="operator" onclick="op='*'">x</button>
  <button id="divide" class="operator" onclick="op='/'">:</button>
</div>

<input id="num2" />

<button onclick="func()">равняется...</button>

<p id="result"></p>


<script>
  var op; //выбранный оператор
  function func() {
    var result;
    var num1 = Number(document.getElementById("num1").value);
    var num2 = Number(document.getElementById("num2").value);
    switch (op) {
      case '+':
        result = num1 + num2;
        break;
      case '-':
        result = num1 - num2;
        break;
      case '*':
        result = num1 * num2;
        break;
      case '/':
        if (num2) {
          result = num1 / num2;
        } else {
          result = 'бесконечность';
        }
        break;
      default:
        result = 'выберите операцию';
    }

    document.getElementById("result").innerHTML = result;
  }
</script>
