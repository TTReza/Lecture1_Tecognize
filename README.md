# Lecture1_Tecognize

#Time complexity is the amount of time taken by an algorithm to run, as a function of the length of the input. It measures the time taken to execute each statement of code in an algorithm. To say elaborately, Time complexity measures the time taken to execute each statement of code in an algorithm. If a statement is set to execute repeatedly then the number of times that statement gets executed is equal to N multiplied by the time required to run that function each time.

#“Big Oh notation is a mathematical notation that describes the limiting behavior of a function when the argument tends towards a particular value or infinity.In computer science, big O notation is used to classify algorithms according to how their run time or space requirements grow as the input size grows. In analytic number theory, big O notation is often used to express a bound on the difference between an arithmetical function and a better understood approximation. ” -Wikipedia’s definition
To understand the basics of time complexity, let us consider a scenario of two friends and their file-sharing with each other.
Alex and John are two friends. They live in the same town but there is a distance of five kilometres among them. After their final exam, they planned to play computer games. But the problem is, Alex has a game whose size is around 20Gb. So John can’t receive the huge file through the internet. What could be the solution to share the file?
I hope you got the answer! Physically they can exchange their pen drives containing the file. Let us consider that the game size is in Kb. Hence they can easily share the file through the internet. But you see, whenever the file size increases the run time or sharing time increases, it is like a proportional relation between file size and runtime. Right? However, if you see on the first case you can notice that whatever huge the file size is they should share it physically. So we can say, the first scenario of run time remains constant, which can be written as a big Oh of 1 (O(1)). The second scenario of the run time increases linearly, written as Big Oh of n ( O(n)). Let us plot our two cases and visualise them with Big-Oh notation.

If we try to understand the big oh notation for our story let us take two algorithms for each scenario.
Algorithm 1: As there is a physical file sharing process we can assume that the friend who has gone to share the file may spend time travelling, giving the file to his friend, again coming back home. So we may write it like,
algo 1 = k1 + k2 + k3 
or, algo 1 = k1 * (n⁰) + k1 + k2
So the big O notation will be for the input time (n) which has taken as to the power of zero which equals 1. Hence, it is O(1) a constant term.
Algorithm 2: The second case can be considered as whenever the file size increases the input time increases. So we can assume the algorithm as an equation of a straight line.
algo 2 = k1 * (n) + C 
To calculate big Oh, the non-dominant terms and constant can be deleted as the higher the term, the higher it is relevant to our algorithm. So,
algo 2 = k1 * n
Hence, the big Oh notation is O(n) which is linear.
Now let us take an algorithm where there is an array containing some elements. The objective of this array is to find a number from the array.
int arr[] = {4,9,15,21,34,56,68,91}
We want to search for 68 from the above array. If you are intelligent enough you can go for searching the element by dividing the array elements into half and so on. Yes ! You were right! If we do the division thing we can ultimately go for 68. Such as,
iteration 1 = n/2 #divides the array in half
iteration 2 = (n/2)/2 #divides the second half again into half
iteration 3 = (n/2²)/2 #divides the previous half again into half and we get 68.
Therefore, iteration, K = n/2^k 
or, 1 = n / 2^k
or, n = 2^k
or, log n = k ; which is Big Oh of log n. 
So, here the searching algorithm is lengthy enough. That's why it is the Worst Case of Big-Oh. On the other hand, if we had got the expected number at the first attempt, the Big-Oh notation would be O(1) which is the Best Case scenario.

In lecture 1 we learned about arrays,lists, finding numbrs in array, reversing array. 

let, a = [1,8,13,5,4] 
Our target is to find 8

#CODE: 
a = [1, 8,13,5,4]
start = 0
end = len(a) 
while start<=end:
   if a[start] == target:
      print()
      start +=1 


Reversing an array: 
#CODE:
a = [1.2.3.4]
s = 0
e = len(a) -1
while s<e:
   a[s],a[e] = a[e],a[s]
   print(a)
   
Time complexity : O(n)
Space Complexity: O(n)
