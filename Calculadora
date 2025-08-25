const readline = require('readline');

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout
});

/**
 * Função para realizar a operação matemática.
 * @param {number} num1 - O primeiro número.
 * @param {string} operador - O operador matemático (+, -, *, /).
 * @param {number} num2 - O segundo número.
 * @returns {number|string} O resultado da operação ou uma mensagem de erro.
 */
function calcular(num1, operador, num2) {
  let resultado;
  const numero1 = parseFloat(num1);
  const numero2 = parseFloat(num2);


  if (isNaN(numero1) || isNaN(numero2)) {
    return 'Erro: Por favor, insira apenas números.';
  }


  switch (operador) {
    case '+':
      resultado = numero1 + numero2;
      break;
    case '-':
      resultado = numero1 - numero2;
      break;
    case '*':
      resultado = numero1 * numero2;
      break;
    case '/':
          if (numero2 === 0) {
        return 'Erro: Divisão por zero não é permitida.';
      }
      resultado = numero1 / numero2;
      break;
    default:
      return `Erro: O operador '${operador}' não é válido. Use +, -, * ou /.`;
  }

  return +resultado.toFixed(2);
}

console.log('Calculadora em Node.js');

rl.question('Digite o primeiro número: ', (num1) => {
  rl.question('Digite o operador (+, -, *, /): ', (operador) => {
    rl.question('Digite o segundo número: ', (num2) => {
      const resultado = calcular(num1, operador, num2);
      console.log(`Resultado: ${resultado}`);


      rl.close();
    });
  });
});