# Задание 1

Напиши скрипт, который, для объекта `user`, последовательно:

- добавляет поле `mood` со значением `'happy'`
- заменяет значение `hobby` на `'javascript'`
- заменяет значение `premium` на `false`
- выводит содержимое объекта `user` в формате `ключ:значение` используя
  `Object.keys()` и `for...of`

```js
const user = {
  name: 'Mango',
  age: 20,
  hobby: 'html',
  premium: true,
};
```

# Задание 2

Напиши скрипт который определит и выведет в консоль имя сотрудника который
выполнил больше всех задач. Сотрудники и кол-во выполненых задач содержатся как
свойства объекта `employees` в формате `"имя":"кол-во задач"`.

```js
const employees = {
  ann: 29,
  david: 35,
  helen: 1,
  lorence: 99,
};
```

# Задание 3

Напиши функцию `countProps(obj)`, считающую кол-во свойств в объекте. Функция
возвращает количество свойств.

```js
// Вызовы функции для проверки
console.log(countProps({})); // 0

console.log(countProps({ name: 'Mango', age: 2 })); // 2

console.log(countProps({ mail: 'poly@m.com', isOnline: true, score: 500 })); // 3
```

# Задание 4

Напиши функцию `countTotalSalary(employees)` принимающую объект зарплат. Функция
считает общую сумму запрплаты работников и возращает ее. Каждое поле объекта,
передаваемого в функцию, имеет вид `"имя":"зарплата"`.

```js
// Вызовы функции для проверки
console.log(countTotalSalary({})); // 0

console.log(
  countTotalSalary({
    mango: 100,
    poly: 150,
    alfred: 80,
  }),
); // 330
```

# Задание 5

Напиши функцию `getAllPropValues(arr, prop)`, которая получает массив объектов и
имя ключа. Возвращает массив значений определенного поля `prop` из каждого
объекта в массиве.

```js
const users = [
  { name: 'Poly', age: 7, mood: 'happy' },
  { name: 'Mango', age: 4, mood: 'blissful' },
  { name: 'Ajax', age: 3, mood: 'tired' },
];

// Вызовы функции для проверки
console.log(getAllPropValues(users, 'name')); // ['Poly', 'Mango', 'Ajax']

console.log(getAllPropValues(users, 'mood')); // ['happy', 'blissful', 'tired']

console.log(getAllPropValues(users, 'active')); // []
```

# Задание 6

Есть два массива `names` и `prices` с именами и ценами товаров. Напиши функцию
`combine(names, prices)`, которая получает эти два массива и возвращает массив
объектов со свойствами `name` и `price`.

```js
const names = [
  'Радар',
  'Сканер',
  'Дроид',
  'Захват',
  'Двигатель',
  'Топливный бак',
];
const prices = [1000, 2000, 1500, 2700, 1600, 8000];

const products = combine(names, prices);
console.log(products); // массив объектов {Радар: 1000} {Сканер: 2000} итд
```

# Задание 7

Напиши скрипт управления личным кабинетом интернет банка. Есть объект `account`
в котором необходимо реализовать методы для работы с балансом и историей
транзакций.

```js
/*
 * Транзацкий всего две.
 * Можно положить либо снять деньги со счета.
 */
const Transaction = {
  DEPOSIT: 'deposit',
  WITHDRAW: 'withdraw',
};

/*
 * Каждая транзакция это объект со свойствами: id, type и amount
 */

const account = {
  // Текущий баланс счета
  balance: 0,
  // История транзакций
  transactions: [],
  /*
   * Метод отвечающий за добавление суммы к балансу
   * Создает объект транзакции и вызывает addTransaction
   */
  deposit(amount) {},
  /*
   * Метод отвечающий за снятие суммы с баланса.
   * Создает объект транзакции и вызывает addTransaction
   *
   * Если amount больше чем текущий баланс, выводи сообщение
   * о том что снятие такой суммы не возможно, недостаточно средств.
   */
  withdraw(amount) {},
  /*
   * Метод добавляющий транзацию в свойство transactions
   * Принимает объект трназкции
   */
  addTransaction(transaction) {},
  /*
   * Метод возвращает текущий баланс
   */
  getBalance() {},
  /*
   * Метод возвращает историю транзакций
   */
  getTransactionHistory() {},
  /*
   * Метод ищет и возвращает объект транзации по id
   */
  getTransactionDetails(id) {},

  /*
   * Метод возвращает количество средств
   * определенного типа транзакции из всей истории транзакций
   */
  getTransactionAmountByType(type) {},
};
```