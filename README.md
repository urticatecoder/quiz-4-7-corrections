# Quizzes 4-7 Corrections
## Quiz 4
### Question 7
For this question, I selected the wrong data types because I was confusing Javascript with other languages. In javascript, the data types are object, symbol, null, undefined, number, string and boolean. Javascript does not include separate data types for integers and floating point numbers, nor does it include a character data type like Java does. Those three (integers, floating point, and character) are the incorrect answers that I put on question number 7.

### Question 8
I got this question wrong because I failed to remember proper naming conventions for variables declared with the const keyword. In javascript, convention dictates that variables declared with the let or var keyword are named in lowerCamelCase, where the first letter of the name is lowercase, and the first letter of every subsequent word is capitalized. However, const variables are declared with a different convention, in which the whole name is in caps, with underscores separating the words, such as "NUM_ONE." Since the question specifically asks for the MOST correct answer, `const PI = 3.14;` is more correct than `const pi = 3.14;`.

### Queston 11
```
function offToCollege(){
  let favCollege = prompt("What is your favorite college?");
  let totalCost = prompt("Please enter the approximate cost of staying at " + favCollege + " for all 4 years.");
  document.getElementById("off-to-college").innerHTML = favCollege + " is a pretty expensive school! It'll cost you $" + (totalCost/4) + " per year!"
}

function carpool(){
  let numOfFriends = Number(prompt("How many friends do you want to bring to the movies?"));
  let numOfSuvs = Number(prompt("How many SUVS are available for driving?"));
  let suvsNeeded = Math.floor(numOfFriends/7);
  let suvs;
  let sedans;
  if(suvsNeeded>numOfSuvs){
    suvs = numOfSuvs;
    sedans = Math.ceil((numOfFriends-(7*numOfSuvs))/4);
    console.log(suvs + " parents who drive SUVs and " + sedans + " parents who drive sedans are required to transport the " + numOfFriends + " friends to the movies." );
  }else if(suvsNeeded<numOfSuvs){
    suvs = suvsNeeded;
    sedans = Math.ceil((numOfFriends-(7*suvsNeeded))/4);
    console.log(suvs + " parents who drive SUVs and " + sedans + " parents who drive sedans are required to transport the " + numOfFriends + " friends to the movies." );
  }
}
```
## Quiz 5
### Question 14
For this question, the correct answers were 
`do {
   x--;
} while (x > 100);`
and
`do {
   x++;
} while (x < 100);`
however I only selected the former. The reason why the second one works in addition to the first one is because it will start by adding 1 to the value of x, to make it 124. Then, it will check the condition provided and see that x is not less than 100, and the loop will terminate. In this way, both the former and the latter options are valid do...while loops that will terminate.

## Quiz 6
### Question 1
The part I got wrong about this question was saying Math.random() accepts a parameter. In reality, built-in Math.random() function simply chooses a pseudorandom number between 0 and 1. It does not provide an opportunity to pass a value through it and do something with that value. Therefore, it accepts no parameters.

### Question 4
Here, I selected, "I need to do chores, homework, and... So busy!" As one of the correct answers, when in reality, the correct answer in place of that should have been, "I need to do chores, homework, and undefined... So busy!" This is because the second time doSomeStuff is called, it is given fewer values to pass through it than it has parameters. Therefore, the final parameter would become undefined, and when javascript tried to concatenate it to, "I need to do chores, homework, and" the word undefined would have been added after homework.

### Question 9
For this question, I said that Math.random does return a value, which Canvas marked incorrect. However, I am fairly sure that Math.random does indeed return a value, as you are able do declare a variable by calling Math.random, and having its value returned to the variable. This is confirmed by the official documentation of Javascript on developer.mozilla.org, which says, "The Math.random() function returns a floating-point, pseudo-random number in the range 0–1 (inclusive of 0, but not 1) with approximately uniform distribution over that range — which you can then scale to your desired range."

## Quiz 7
### Question 14
This question asks which example array shows why a given algorithm would not work as intended to find the maximum value in the array. I selected the array, `[-9, 1, -8, 2, -7, 3, -6, 4, -5]`. However, the correct answer should have been, `[-9, -1, -8, -2, -7, -3, -6, -4, -5]`. This is because in the given algorithm, maximum is declared as 0. If the function was run for the second array, it would never encounter a value greater than zero, and it would say that 0 was the maximum value in the array, even though 0 was not in the array.
