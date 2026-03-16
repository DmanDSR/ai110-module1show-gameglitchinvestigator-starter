# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?


- What did the game look like the first time you ran it?

it looked normal, a simple game that displayed the number of guesses and the range to guess from. 
then on the left it would show the option to change difficultly, the range and the max number of guesses.
looked normal, without playing the game.

- List at least two concrete bugs you noticed at the start  
  (for example: "the secret number kept changing" or "the hints were backwards").

<!-- 
1. Typed numbers don't work
2. the hint is wrong (says go lower, but should have been higher
3. shows the wrong number of attempts left, stops 1 short
4. new game button doesn't work
5. debug info says -10, the display says a score of -15
6. difficulty does not work properly  -->

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).

I used Claude code to help me, it helped me bugs like the score inconsistency, and the difficulty being wrong. where it may be wrong is the wrong hints section, I fixed this part already but it still doesn't see if as fixed for some reason  

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

to decide if a bug was really fixed I would start the game up again with the fixed and observe if the past problem was still persistent. so when I fixed the new game button I started a new game and once i played through once I checked if the button worked, and it did.  

AI did not help with the testing part.

---

## 4. What did you learn about Streamlit and state?

- In your own words, explain why the secret number kept changing in the original app.
- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
- What change did you make that finally gave the game a stable secret number?

so to my understanding the secret number kept changing because the variable being called wasn't the right one, every time the wrong variable was called it constantly was changing the number it wasn't the saved secret number from the beginning.

Every single time you click a button or type something, it reruns your entire Python file from top to bottom, like hitting refresh on the page.
Session state is basically a little storage box that survives each rerun.

I changed the variable that was being called and the secret number stayed consistent. 

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.


I liked using the hashtags when giving context to the AI. I would probably have the AI help me create tests more. This project helped my to see how I can add more context for the AI in different ways like with the hashtags, it also helped me to use AI as a teammate more then just a tool to do everything. 