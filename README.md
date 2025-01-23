# Sentiment-Analysis-and-Text-Generator-Using-Twitter-data
This project involves constructing an auto-complete system, a tool commonly encountered in daily
activities. For instance, when conducting a Google search, suggestions often appear to assist in completing
your query. Similarly, while composing an email, you receive prompts suggesting potential endings to your
sentences. Upon completing this project, you'll create a prototype of such a system.
A foundational element for an auto-complete system is a language model, that assigns probabilities to
sequences of words based on their likelihood in real-world usage. For instance, "I have a pen" is expected
to have a higher probability than "I am a pen" due to its naturalness.
Utilizing this probability framework, you can develop an auto-complete system. For example, if the user
types "I eat scrambled," the system can suggest a word "x" such that "I eat scrambled x" yields the highest
probability. If "x" is "eggs," the completed sentence would be "I eat scrambled eggs."

Here's an overview of the project steps:
1. Load and preprocess data:<br>
*a. Load and tokenize the data.<br>
b. Divide sentences into training and testing sets.<br>
c. Replace infrequent words with an unknown marker* ("<*unk*>").<br>
2. Develop N-gram-based language models:<br>
*a. Compute the count of n-grams from the dataset.<br>
b. Estimate the conditional probability of the next word using k-smoothing.<br>
c. Evaluate the N-gram models by calculating the perplexity score.<br>*
3. Utilize your model to suggest the next word given a sentence.<br>

N-gram based language model
In this task, you'll develop an n-grams language model where the probability of the next word depends
only on the previous n-gram. The previous n-gram refers to the series of the preceding 'n' words in the
sentence. To estimate the conditional probability for the word at position 't' in the sentence, given the
preceding words, you'll use the following equation:<br>
![Screenshot 2025-01-23 202141](https://github.com/user-attachments/assets/77c51282-2893-446f-ad82-19a1c9793c2d)<br>


This equation calculates the probability of word 't' given the previous n-gram.<br>

Probabilities for all words
To estimate the probability of a word given the prior 'n' words using the n-gram counts and k-smoothing,
you can define a function that implements the formula:

![image](https://github.com/user-attachments/assets/116c66f3-b3e1-44cb-96de-0cc144ceb236)<br>

where V the size of the vocabulary, and k is a positive constant (smoothing parameter). Consider k = 1

For n-grams with zero counts, the probability estimate becomes:

![image](https://github.com/user-attachments/assets/18584529-bf59-4874-96c9-30ab4973b561)<br>


