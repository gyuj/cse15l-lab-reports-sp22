# Week 8 Lab Report 4
## Debuggers and Snippets


In this lab, we will show how to run tests for our markdown snippets
using our JUnit tests and compare our MarkdownParseTest with other tests.

___

`Links to personal and other mdp`

[This is the link to my implementatin of mdp](https://github.com/gyuj/markdown-parse.git)

[This is the link to the other group's implementation of mdp from Week 7: clingunis ](https://github.com/clingunis/markdown-parse.git)

---

`Preview of snippets on what they should look like`

> Snippet #1
![Snippet 1](snip-1_prev.png)

> Snippet #2
![Snippet_2](snip-2_prev.png)

> Snippet #3
![Snippet_3](snip-3_prev.png)

> How to test the snippets in our MardownParseTest.java
![Code for tests of snippets](mdp-sniptest.png)

___

`Below are the corresponding outputs when running the two tests on the three snippets.`

> For my implementation, 
![Personalimp output](my_imp_ouput.png)

> the three tests failed for all three snippets
> It seems to have been caused by an extra url.com being printed in addition to the normal link arguments passed in.


> For the other implementation, 
![Other imp out](other_output_1.png)
![Other_imp_out_fin](other_output_2.png)

> The three tests failed for all three snippets again. 
> The cause for this time seems to have been the snippet #1 not being named correctly the previous time, snippet #2 not printing the last "example.com" link, and snippet #3 printing the links in awkward spacings. The other group also added a note for identifying errors, where they printed the link not including a closing parentheses. That was helpful.

> Renamed the first snippet to correctly run the test, saw that the error in snippet #1 was caused by the first link having an extra "url.com" as identified in my own implementation, and missing the last link, "ucsd.edu" at the end.
![Fixed other imp](fixed_snippet1.png)

___

`Questions answered from lab instructions`

// 1. Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change.

Yes, I believe that there is a small code change possible than will make my program work for snippet 1 and any other cases that uses backticks. We can check the passed argument for our links whether they have two backticks, if there are more or less than two, we can disregard the changes it bring to our argument of input and render the necessary characters for our links.

// 2. Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be a more involved change. 

No, there isn't a small code change that can make my program work for snippet 2. There could be a way to recognize the double / nested parentheses within our passed arguments by using a counter or any other sorts of identifying brackets and parentheses that are escaped or doubled in quantity, but it wouldn't be possible with just a few amount of code change. 

// 3. Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would be a more involved change.

Yes, it is possible to make small code changes to make my program work for snippet 3 that has random spaces and lines within the brackets and parentheses. We can use existing String methods to trim the spaces and blank lines within our passed argument to return a normal link. 



