# The Cashier
[![Status overview badge](../../blob/badges/.github/badges/main/badge.svg)](#-results)


Write a function named `cashCounter` that helps a cashier give adequate change to customers. The function should return the amount of notes and coins for the customer's change.

Example1: If the price is €3.75 and the paid amount is €50, then the client should receive €46.25 back in change.

```javascript
console.log(cashCounter(3.75, 20));
// [
// { '20 Euro': 2 },
// { '5 Euro': 1 },
// { '1 Euro': 1 },
// { '0.2 Cent': 1 },
// { '0.05 Cent': 1 }
// ]
```

Example2: Price: €4.50, Paid amount: €20, Change: 15.50

```javascript
console.log(cashCounter(4.5, 20));
// [ { '10 Euro': 1 }, { '5 Euro': 1 }, { '0.5 Cent': 1 } ]
```

- Include outputs for exceptions:

1. price: €4, paid amount: €3. // 'Customer should pay 1 more Euro'
2. cash box is empty or not enough coins // 'No change available'

## Guidelines

1. Write a higher order function named `createCashCounter`.
2. This function should return an anonymous function with a cash box in its closure.

Example Cash Box:

```javascript
let cashBox = [
  { 50: 10 },
  { 20: 10 },
  { 10: 10 },
  { 5: 25 },
  { 2: 25 },
  { 1: 25 },
  { 0.5: 25 },
  { 0.2: 25 },
  { 0.1: 25 },
  { 0.05: 25 },
  { 0.02: 25 },
  { 0.01: 25 },
];
```

3. Call the `createCashCounter` function and assign the returned function to a variable called `cashCounter` like this:

```javascript
cashCounter = createCashCounter();
```

4. Call the `cashCounter` function and pass the price and paid cash as shown in the examples above.
5. Add the paid cash to cash box and deduct the change from the cashbox.
6. Call the `cashCounter` function with a few different price/paid cash combo and check if the cash box is updating properly.

[//]: # (autograding info start)
# <img src="https://github.com/DCI-EdTech/autograding-setup/raw/main/assets/bot-large.svg" alt="" data-canonical-src="https://github.com/DCI-EdTech/autograding-setup/raw/main/assets/bot-large.svg" height="31" /> Results
> ⌛ Give it a minute. As long as you see the orange dot ![processing](https://raw.githubusercontent.com/DCI-EdTech/autograding-setup/main/assets/processing.svg) on top, CodeBuddy is still processing. Refresh this page to see it's current status.
>
> This is what CodeBuddy found when running your code. It is to show you what you have achieved and to give you hints on how to complete the exercise.


### cashCounter

|                 Status                  | Check                                                                                    |
| :-------------------------------------: | :--------------------------------------------------------------------------------------- |
| ![Status](../../blob/badges/.github/badges/main/status0.svg) | Should be defined |
| ![Status](../../blob/badges/.github/badges/main/status1.svg) | Should tender exact change with available denominations |



[🔬 Results Details](../../actions)
[🐞 Tips on Debugging](https://github.com/DCI-EdTech/autograding-setup/wiki/How-to-work-with-CodeBuddy)
[📢 Report Problem](https://docs.google.com/forms/d/e/1FAIpQLSfS8wPh6bCMTLF2wmjiE5_UhPiOEnubEwwPLN_M8zTCjx5qbg/viewform?usp=pp_url&entry.652569746=PB-the-cashier-problem)


[//]: # (autograding info end)