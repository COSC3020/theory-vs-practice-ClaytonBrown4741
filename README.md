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
  2: Asymptotic analysis does not take into account the hardware that the user
  is running their algorithm on. If the user is running an algorithm on a sub-optimal
  piece of machinery, then it's possible that their code will run significantly longer
  than the asymptotic analysis says that it should.
  3: Some asymptotic relationships are faster than others, but only when they pass
  a certain sample size (usually represented as C in many asymptotic proofs). For an
  simply example of this, compare the two equations of 10000n and $n^2$. Although the
  first is much faster for larger cases, it is still a lot slower when dealing with
  smaller sample sizes. Asymptotic analysis does not usually display these sorts of
  relations.

  Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.
  **Answer:** The average time it takes to search a binary tree is O(log(n)). Using this
  information, along with the knowledge that the number of elements will be going up
  by one magnitude of 10, we can conclude that it will probably take around 6.66 seconds
  to find the element when there are 10,000 elements. I calculated this by the ratio at
  which log increases when increasing it's size by a factor of 10. The calculation
  for 1000 ended up being 9.9657, while for 10,000 it was 13.2877. By dividing these
  two values, I found that it increased at a rate of 1.333. I then mulitiplied this
  by 5 to get the final answer of 6.66 seconds.

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
  In addition to this, we assumed that finding the element was an average case, but
  it's very possible that the search in the first exampe was the best case scenario (the root).
  If this is the case, it would change our calculations and ultimately cause us
  seriously underestimate how long it would actually take to traverse this tree.
  2: Another thing to keep in mind is that we don't know anything about what the user
  is running this program on. It is very possible that background processes caused
  the computer to slow down a lot, or it may even be a completely different machine
  than the first time they ran it. This could cause a lot of time delay that didn't
  exist before.
  3: Asymptotic analysis usually does not account for different element types. For
  instance, if the elements you're comparing are long strings, then it will take
  signficantly longer to compare them than if you simply used integers instead.
  As a result, adding more values into the tree can ultimately cause the
  waiting time to increase by an extremely large degree that doesn't match at all
  with what the asymptotic analysis implies. This is can be an even bigger issue if
  the elements in the original tree were all number values (which are fairly easy to sort through)
  while most of the elements in the larger tree are much more complicated (like strings or even
  whole files). This could result in the waiting time being even longer than we believed it
  to be at first.
