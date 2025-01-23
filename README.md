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
