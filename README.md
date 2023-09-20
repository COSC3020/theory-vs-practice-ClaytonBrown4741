[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=11856773&assignment_repo_type=AssignmentRepo)
# Theory vs. Practice

   **THE FOLLOWING HAVE ALL MY ANSWERS. PLEASE LET ME KNOW IF ANY OF THEM ARE
  WRONG OR REQUIRE REVISION**
- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  **ANSWER:**
  1: Asymptotic analysis mainly deals with values as they reach infinity.
  Because of this, constant values are often ignored, but this can lead to
  issues when dealing with smaller lists. For instance, 1000n and n are
  asymptotically the same, but one is much, much longer than the other.
  This can result in a misleading measurement of the algorithms true speed
  on normal lists.
  2: Although usually displayed elsewhere, asymptotic analysis does not take
  into account memory usage. There are some sorting algorithms like mergesort
  that can be quite quick, but they need a large amount of space in order to
  operate. Those who are unaware of this may use the algorithm and encounter
  freezing,errors, or slower-than-promised runtime due to not accounting for
  amount of required memory.
  3: Asymptotic relationships are often misleading in the sense of what the
  average, best, and worst cases can be for the same algorithm. For instance,
  consider insertion sort.
  Asymptotically speaking, the average and worst cases for it are both the same.
  However, average cases will always run faster than the worst case. In fact, many
  of the of the cases will run *significantly* faster than the worst case.
  This can lead to users making the assumption that insertion sort is only good
  to use on already sorted lists, while this is not the case.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.
  **Answer:** The average time it takes to search a binary tree is O(log(n)). Using this
  information, along with the knowledge that the number of elements will be going up
  by one magnitude of 10, we can conclude that it will probably take around 6.66 seconds
  to find the element when there are 10,000 elements.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.
  **Answer:**
  1: It's possible that inserting the extra elements caused a close-to worst
  case scenario for a binary tree (that being when all the values are on one
  side, which essentially creates a list). If this is the case, then although
  it *technically* would still be considered an average case, the runtime would
  actually be much closer to the worst case for binary search. The same thing would
  apply if the element simply got pushed down the tree a lot by the new elements.
  2: Another thing to keep in mind is that we claim the asymptotic complexity of
  searching a binary tree is O(log(n)). However, all logs, regardless of their
  base, are technically equal asymptotically speaking. Because of that, the *actual*
  runtime for searching through a binary tree is closer to log2(n), which is much
  slower. This may be leading to the extremely large waiting time.
  3: Asymptotic analysis usually does not account for different element types. For
  instance, if the elements you're comparing are long strings, then it will take
  signficantly longer to compare them than if you simply used integers instead.
  As a result, adding more values into the tree can ultimately cause the
  waiting time to increase by an extremely large degree that doesn't match at all
  with what the asymptotic analysis implies. 

Add your answers to this markdown file.
