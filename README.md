# data-311-assignment-3-bonus-written-part-solved
**TO GET THIS SOLUTION VISIT:** [DATA 311 Assignment 3 (Bonus Written Part) Solved](https://www.ankitcodinghub.com/product/data-311-assignment-3-bonus-written-part-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;115874&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;DATA 311 Assignment 3 (Bonus Written Part) Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
Yunfan Yang 30067857

Searching on a linked list (10 points)

What is the biggest drawback in a linked list (SLL or DLL) that makes O(logn) search impossible on it?

For a search algorithm with O(logn) such as binary search, it usually divides the given array in half to subarrays and repeat this process until the value is found; by achieving this, the algorithm has to have the ability to find the middle point of the array repeatedly. Since linked lists always only track the head or both head and tail, and there is no direct way to access the middle point of the list. Therefore, the O(logn) search algorithms are impossible on a linked list.

A candidate modification to linked lists (10 points)

Consider a doubly linked list. We know that every node in a DLL contains a pointer to the next and previous nodes respectively. Now suppose every node has a next pointer to every other node that appears on the list after it, and a previous pointer to every other node that appears on the list prior to it. Suppose this list has n such nodes.

1. WHAT IS THE OVERALL OVERHEAD IN TERMS OF POINTER STORAGE PER NODE AND ON THE LIST AS A WHOLE?

For each node on the list will now have 𝑛−1 pointers. For the whole list, the number of pointers will be 𝑛(𝑛−1)=𝑛2−𝑛, the memory will have an increment for each new Node add to the linked list at a rate of 0.5 compared to the original linked list.

2. WHAT IS THE AVERAGE ASYMPTOTIC COST FOR INSERTING A NODE AT AN ARBITRARY LOCATION IN THIS LIST?

The average asymptotic cost for inserting now will be O(1) since each node has the pointers of any other nodes, which the node can be directly inserted into an arbitrary location instead of tracing every node O(n).

3. DESCRIBE HOW YOU MIGHT PERFORM BINARY SEARCH ON THIS MODIFIED LIST. My implementation in the code file provided tries to be the same as possible with the original binary search (although there are other easier ways, I believe, to implement). The index in the algorithm will be the same as the original list; there will be a importFromArray function to import an original list to a linked list for testing, and the order of all the elements keeps the same. The search will be started from the middle point of the linked list (the middle point can be found by the element number of the successor list of the linked list head, and minus one since it needs to exclude itself when dealing with the index, and floor divided by 2, and minus one because of the same reason), and it will pass the middle point Node instance to start the searching.

The followings are the steps:

a. The base case of the modified binary search is still “when the middle point value is the goal value”

b. Also if the Node’s value is None, or the current Node index is invalid (which is less than 0), or the searching range is invalid (which is less than 0), it means the goal value is not in the list.

c. If the goal value is less than the middle value, then divide the array into half by limiting the search range and calculate the new middle point in the search range from the current Node’s predecessor. Then it will pass the middle point Node instance to keep finding.

d. If the goal value is greater than the middle value, then divide the array and set the middle point as on the above step, but the middle point is from the current Node’s successor.

e. After dividing, it will recursively invoke _binarysearch function until the base case is satisfied.

The index variable has no direct effect on the algorithm itself but just to keep track of the current Node’s index in the list, we need this variable since Node instance does not have an index attribute.
