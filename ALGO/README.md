The following pseudocode represents an algorithm designed to analyze a given sentence character by character, calculating its length, word count, and the total number of vowels. Initialize three separate counters: one for the sentence length (starting at 0), one for the word count (starting at 1, assuming a minimum of one word), and one for the vowel count (starting at 0). Input the sentence as a string. Proceed to iterate through each character in the string, executing the subsequent actions: a. Increment the length counter. b. If the character is a space, increment the word counter. c. If the character is a vowel (a, e, i, o, or u), increment the vowel counter. d. If the character is a period, terminate the loop. Finally, display the calculated sentence length, word count, and vowel count.
Here is the refined JavaScript code:
const readline = require('readline').createInterface({ input: process.stdin, output: process.stdout });

readline.question('Please enter a sentence: ', sentence => {
let lengthCounter = 0;
let wordCounter = 1;
let vowelCounter = 0;

for (let i = 0; i < sentence.length; i++) {
const character = sentence.charAt(i);
lengthCounter++;
if (character === ' ') {
wordCounter++;
} else if (/[aeiou]/i.test(character)) {
vowelCounter++;
} else if (character === '.') {
break;
}
}

console.log(`Sentence Length: ${lengthCounter}`);
console.log(`Word Count: ${wordCounter}`);
console.log(`Vowel Count: ${vowelCounter}`);

readline.close();
});
