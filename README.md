# Programming-Problem

Solutions to some programming problems found online


#### May 06, 2018
[Longest Palindromic Subsequence](https://leetcode.com/problems/longest-palindromic-subsequence/description/)
This is a review of a question I've done before so not a big deal. 
Tag: DP, String, Subsequence.


[3Sum](https://fizzbuzzed.com/top-interview-questions-1/#twopointerm)
Classic 3Sum problem. Use 2 pointers (actually 3) to solve. The solution is pretty straightforward. However need to check for 2 places where duplicates are not allowed


#### May 08, 2018

[Delete And Earn](https://leetcode.com/problems/delete-and-earn/description/)
One of the easy DP problem although it seems deceptive at first. 

#### May 23, 2018

[Best time to buy and sell stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/description/)
Given a list of ints of value of stock. You can only buy/sell once through the whole thing. Return the maximum profit.
The optimal solution of this problem is O(n). A bit tricky.

[Containter with most water](https://leetcode.com/problems/container-with-most-water/description/)
An easier version of Trapping Rain Water. Can be solved with 2 pointers in linear time with constant space. Have been asked in interview before.
Just use two pointers from left and right and move the smaller one in while updating the max water store.

[CombinationSum IV](https://leetcode.com/problems/combination-sum-iv/description/)
A variation of DP. Pretty simple and straightforward DP.

#### May 25, 2018

[Number of Islands](https://leetcode.com/problems/number-of-islands/description/)
Redid this problem. One pass.

[Maximum Subarray](https://leetcode.com/problems/maximum-subarray/description/)
Easy problem but very tricky with indexes

#### May 30, 2018

[Surrounded Region](https://leetcode.com/problems/surrounded-regions/description/)
Graph search problem. There is a trick. Do mutiple bfs/dfs from the side.

[Binary Tree Maximum Path Sum](https://leetcode.com/problems/binary-tree-maximum-path-sum/description/)
Seen this before. Have to do a Post Order Traversal. There are 4 cases I need to keep track of: max(root, root + left,root. right, root + left + right). 

[House Robber III](https://leetcode.com/problems/house-robber-iii/description/)
Pretty straight forward solution but a little bit tricky to implement traversal


#### May 31, 2018

Reviewed implementing QuickSort and MergeSort.

#### June 7, 2018
Review LinkedList, Palindrome in C in both recursive and iterative method

#### June 27, 2018
[Split array into consecutive subquence](https://leetcode.com/problems/split-array-into-consecutive-subsequences/description/)
Pretty interesting problem. Could be done in O(n^2) or O(n)

[Binary Tree Vertical Order Traversal](https://leetcode.com/problems/binary-tree-vertical-order-traversal/description/)
Traverse and append to a list in vertical order. Can be solved with in order BFS, or something better!

#### June 28, 2018
[Number of subarray with bounded maximum](https://leetcode.com/problems/number-of-subarrays-with-bounded-maximum/description/)
Interesting problem. Brute force is DP O(n^2  * logn) but there can be O(n) O(n) solution.
Snippet Code to calculate the index(start, end) of adjacent similar values.
```
A = [False, False, True, False, True, True, True, False, True]
ans = []
idx = 0
while idx < len(A):
    count = 0
    while idx < len(A) and A[idx] :
        count += 1
        idx += 1
    if count > 0:
        ans.append([idx - count, idx])
    else:
        idx += 1
print(ans)
#[[2, 3], [4, 7], [8, 9]]
```

[Find Eventual Safe Place](https://leetcode.com/problems/find-eventual-safe-states/description/)
Pretty straight forward graph problem. Can be done in O(n) by implementing a simple finding circle in graph algorithm

[Find all duplicates in array](https://leetcode.com/problems/find-all-duplicates-in-an-array/description/)
Very tricky problem. Solution is not bitshifting but playing around with array from 1 to n

[Partition Label](https://leetcode.com/problems/partition-labels/description/)
Can be solved by DP O(n^2) brute force way but can also be done in  O(n), O(n). Think differently.

#### June 29, 2018

How to check if a singly linkedList is palindromic using recursion with 1 traversal and constant space:

```
bool recursiveCheck(ListNode* right, ListNode** left){
	if (right != NULL){
		if (recursiveCheck(right->next, left)){
			if (right->val == (*left)->val){
				(*left) = (*left)->next;
				return true; 	
			}else{
				return false;
			}	
		}else{
			return false;
		}
	}
	return true;
}
bool isRecursive(ListNode* head){
	ListNode* node = head;
	return recursiveCheck(head, &node);
}
``` 

#### July 2, 2018

[Verify Preorder Serialization of a Binary Tree](https://leetcode.com/problems/verify-preorder-serialization-of-a-binary-tree/description/)
Can do stack or can do with regex. Good medium problem

#### July 3, 2018
[Distinct Subsequence](https://leetcode.com/problems/distinct-subsequences/description/)
Classic DP problem with lots of optimization. I came up with a non-DP solution with a little bit better space.

[Palindromic Substring](https://leetcode.com/problems/palindromic-substrings/description/)
Could be done in O(n^3),O(n^2), O(n)[Review Manacher's algorithm](https://www.youtube.com/watch?time_continue=894&v=nbTSfrEfo6M)

#### July 4, 2018
[Combination Sum](https://leetcode.com/problems/combination-sum/description/)
More like a review but there's a catch when implementing.

#### July 5, 2018
[Score after flipping matrix](https://leetcode.com/problems/score-after-flipping-matrix/description/)
Adhoc problem. Pretty good problem to solve.

[Longest mountain in array](https://leetcode.com/problems/longest-mountain-in-array/description/)
Tricky to implement right. A lot of edge cases

### Synchronized sorting two lists	 
[Most profit in assigning work](https://leetcode.com/problems/most-profit-assigning-work/description/) and
[Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/description/)
These 2 problems are related to the technic of sorting 2 synchronized lists. Really good technic to know.
The point of is to sort one list and try to sort the other list in ascending order by following the nature of the problem

#### July 6, 2018
[Binary Tree with factors](https://leetcode.com/problems/binary-trees-with-factors/description/)
Tricky to write the code right. Interesting to think about the approach. Good question for interview. Make sure to % the answer.

[Count of smaller number after i](https://leetcode.com/problems/count-of-smaller-numbers-after-self/description/)
Problem isn't hard. Can be done in O(nlogn). Review Binary Search Tree, Binary Indexed Tree and Segment Tree.

[Super Washing Machine](https://leetcode.com/problems/super-washing-machines/description/)
I still dont understand how I solved it...

#### July 8, 2018
[Subarray Product Less Than K](https://leetcode.com/problems/subarray-product-less-than-k/solution/)

[Bus Routes](https://leetcode.com/problems/bus-routes/description/)
Interesting problem. Should probably solve it again. Use graph but do it in a smart way to reduce runtime

#### July 9, 2018
[Friend Circles](https://leetcode.com/problems/friend-circles/description/)
Review Union Find

#### July 10, 2018
[Similar String Group](https://leetcode.com/problems/similar-string-groups/description/)
Review Trie

[Making a Large Island](https://leetcode.com/problems/making-a-large-island/description/)
An extension problem from [Number of islands](https://leetcode.com/problems/number-of-islands/description/)

[Valid Parenthesis String](https://leetcode.com/problems/valid-parenthesis-string/description/)
Greedy. Review.

[Maximum Swap](https://leetcode.com/problems/maximum-swap/description/)
Ad hoc question. Number question

## Scheduling Problem Review:
[My Calendar I](https://leetcode.com/problems/my-calendar-i/)

#### July 11, 2018
[Longest Consecutive Sequence](https://leetcode.com/problems/longest-consecutive-sequence/description/)
A bit of review on set.

#### July 12, 2018
[SubTree of another tree](https://leetcode.com/problems/subtree-of-another-tree/description/)
[Find duplicate subtree](https://leetcode.com/problems/find-duplicate-subtrees/description/)
Interesting problem. Use Merkle Hashing algorithm to hash unique paths in binary tree.


#### July 13,2018
[Count Complete Tree Node](https://leetcode.com/problems/count-complete-tree-nodes/description/)
Interesting binary tree problem. log(n)*log(n)

#### July 30, 2018
[Max Point On a Line](https://leetcode.com/problems/max-points-on-a-line/description/)
Ad hoc problem. Not too hard but interesting.
