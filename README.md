[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/FgMJElkj)
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

    1. Asymptotic analysis focuses on growth rates as the input size reaches infinity.
       This method typically ignores constants and lower order terms. While they are
       far less impactful with a massive amount of input, with smaller inputs or large
       constants the performance can be dramatically changed

    2. Asymptotic analysis will typically provide best, worse, or average time complexity
       based on the size of the input. In practice, however, the actual data can play a large
       role on performance. For example, with quicksort the best case occurs when the array
       is divided perfectly in half, while the worst case occurs when the chosen pivot is the first
       or last element. 

    3. Asymptotic analysis says nothing about your hardware. A PC with a better processor will
       outperfom a PC with a worse one, regardless of the algorithm used.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.
      Complexity of BST: O(log^2(n))

      5 = k * log^2(1000)
      5 = k * 9.966
      k = 0.501

      t = 0.501 * log^2(10000)
      t = 0.501 * 13.288
      t = 6.644 seconds

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

    1. The tree could be heavily imbalanced, causing a worst case scenario.

    2. While our asymptotic anlysis assumes a decent algorithm, this may not be the case.
       It is possible that the algorithm is extremely inefficient, and as a result our
       average runtime calculation would probably not reflect that.
    
    3. You could be attempting to run a binary search on the first Macintosh.
       Or just poor hardware in general.

Add your answers to this markdown file.
