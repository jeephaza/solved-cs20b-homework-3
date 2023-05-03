Download Link: https://assignmentchef.com/product/solved-cs20b-homework-3
<br>



<ol>

 <li> Given the following method:</li>

</ol>

<table width="0">

 <tbody>

  <tr>

   <td width="39">int</td>

   <td width="395">exer(int num)</td>

  </tr>

  <tr>

   <td width="39">{}</td>

   <td width="395">if (num == 0) return 0;elsereturn num + exer(num + 1);</td>

  </tr>

 </tbody>

</table>




<ul>

 <li>Is there a constraint on the value that can be passed as an argument for this method to pass the smaller-caller test?</li>

 <li>Is exer(7) a valid call? If so, what is returned from the method? (c) Is exer(0) a valid call? If so, what is returned from the method?</li>

</ul>

(d) Is exer(-5) a valid call? If so, what is returned from the method?

<ol start="2">

 <li> You must assign the grades for a programming class. Right now the class is studying recursion, and students have been given this assignment: Write a recursive method <em>sumValues </em>that is passed an index into an array values of int (this array is accessible from within the <em>sumValues </em>method) and returns the sum of the values in the array between the location indicated by index and the end of the array. The argument will be between 0 and values.length inclusive. For example, given this configuration:</li>

</ol>

then <em>sumValues(4) </em>returns 12 and <em>sumValues(0) </em>returns 34 (the sum of all the values in the array). You have received quite a variety of solutions. Grade the methods below. If the solution is incorrect, explain what the code actually does in lieu of returning the correct result. You can assume the array is “full.” You can assume a “friendly” user-the method is invoked with an argument between 0 and values.length.

Figure 1: Example

(a)

<table width="0">

 <tbody>

  <tr>

   <td width="39">int</td>

   <td width="366">sumValues(int index)</td>

  </tr>

  <tr>

   <td width="39">{}</td>

   <td width="366">if (index == values.length) return 0;else return index + sumValues(index + 1);</td>

  </tr>

 </tbody>

</table>




8 (b)

<table width="0">

 <tbody>

  <tr>

   <td width="39">int</td>

   <td width="366">sumValues(int index)</td>

  </tr>

  <tr>

   <td width="39">{}</td>

   <td width="366">int sum = 0; for (int i = index; i &lt; values.length; i++) sum = sum + values[i];return sum;</td>

  </tr>

 </tbody>

</table>




7 (c)

<table width="0">

 <tbody>

  <tr>

   <td width="39">int</td>

   <td width="366">sumValues(int index)</td>

  </tr>

  <tr>

   <td width="39">{}</td>

   <td width="366">if (index == values.length) return 0;else return (1 + sumValues(index + 1);</td>

  </tr>

 </tbody>

</table>




7 (d)

<table width="0">

 <tbody>

  <tr>

   <td width="39">int</td>

   <td width="366">sumValues(int index)</td>

  </tr>

  <tr>

   <td width="39">{}</td>

   <td width="366">return values[index] + sumValues(index + 1);</td>

  </tr>

 </tbody>

</table>




4 (e)

<table width="0">

 <tbody>

  <tr>

   <td width="404">int sumValues(int index){if (index &gt; values.length) return 0;else return values[index] + sumValues(index + 1);}</td>

  </tr>

 </tbody>

</table>




Figure 2: Comparison of Collection Implementations.

(f)

<table width="0">

 <tbody>

  <tr>

   <td width="39">int</td>

   <td width="366">sumValues(int index)</td>

  </tr>

  <tr>

   <td width="39">{}</td>

   <td width="366">if (index &gt;= values.length) return 0;else return values[index]+sumValues(index + 1);</td>

  </tr>

 </tbody>

</table>




7 (g)

<table width="0">

 <tbody>

  <tr>

   <td width="39">int</td>

   <td width="366">sumValues(int index)</td>

  </tr>

  <tr>

   <td width="39">{}</td>

   <td width="366">if (index &lt; 0) return 0;else return values[index] + sumValues(index – 1);</td>

  </tr>

 </tbody>

</table>




<ol start="3">

 <li>Read Chapter 5, view all the code examples there: even those we didn’t see in the class (the complete code for classes from this Chapter is provided for you, you can also find partial code in the book). Look at the table provided in Chapter 5 (see Figure 2 in this file). Explain the following:

  <ul>

   <li>(2 points) Why does <em>SortedArrayCollection </em>exhibit logarithmic time for <em>contains </em>and <em>get </em>methods?</li>

   <li>(2 points) Why do <em>ArrayCollection </em>and <em>LinkedCollection </em>exhibit <em>O</em>(1) time for <em>add </em>(adding an element method), while <em>SortedArrayCollection </em>exhibits a worse <em>O</em>(<em>N</em>) time for the same method?</li>

   <li>(2 points) How is <em>O</em>(1) accomplished for <em>size </em>method for all of these collections in the table?</li>

  </ul></li>

 <li> a) Which method do we need to implement to check if the contents of our objects are the same? b) Write its signature. c) Is it inherited from some class? d) If yes, which one?</li>

 <li>Based on the equals method for Circle objects defined in Section 5.4, “Comparing Objects Revisited,” what is the output of the following code sequence and <strong>why</strong>! (you need to provide 8 answers for each printout, and a very short explanation of why it is so)?</li>

</ol>

1 Circle c1 = new Circle(5);

2

3 Circle c2 = new Circle(5);

4

5 Circle c3 = new Circle(15);

6

7 Circle c4 = null;

8

9 System.out.println(c1 == c1);

10

11 System.out.println(c1 == c2);

12

13 System.out.println(c1 == c3);

14

15 System.out.println(c1 == c4);

16

17 System.out.println(c1.equals(c1));

18

19 System.out.println(c1.equals(c2));

20

21 System.out.println(c1.equals(c3));

22

23 System.out.println(c1.equals(c4));

<ol start="6">

 <li>(6 points) Consider the following interfaces:</li>

</ol>

<ul>

 <li>public interface Event{</li>

 <li>public void RSVP();</li>

 <li>}</li>

</ul>

4

<ul>

 <li>public interface PublicEvent extends Event{</li>

 <li>public void doSecurityCheck();</li>

 <li>}</li>

</ul>

8

<ul>

 <li>public interface PrivateEvent extends Event{</li>

 <li>public void checkIdentification();</li>

 <li>}</li>

</ul>

12

13               public interface PartneredEvent extends Event{ 14           public void findPartner(); 15                       }

Which method(s) should implement a class

<ul>

 <li>(3 point) called <em>Hockey </em>that implements <em>PublicEvent</em>?</li>

 <li>(3 point) called <em>Prom </em>that implements <em>PrivateEvent </em>and <em>PartneredEvent</em>.</li>

</ul>

<h1>2           Programming exercises</h1>

For the programming exercises, please follow the provided instructions in the instructions.pdf. Each of the exercises below should be a separate zip of a Java project.

<ol>

 <li>Project 1:  Attached to this homework is a .java file called <em>java</em>. Part of it is implemented for you and there is a main method already written that will test your code. A recursive printing of a linked list is also provided for you in method called <em>recRevPrintList</em>. You need to implement <em>iterRevPrintList </em>(method signature is given to you) which <strong>iteratively</strong>, not recursively, does the same – prints a linked list in reverse. Make sure you include and import all necessary support classes for this code to work.</li>

 <li> Add the following methods to the <em>LinkedQueue </em>class (from ch04.zip), and create a test driver for each to show that they work correctly. In order to practice your linked list coding skills, code each of these methods by accessing the internal variables of the LinkedQueue, not by calling the previously defined public methods of the class.

  <ul>

   <li><em>String toString() </em>creates and returns a string that correctly represents the current queue. Such a method could prove useful for testing and debugging the class and for testing and debugging applications that use the class. Assume each queued element already provides its own reasonable toString method.</li>

   <li>(10 points) <em>void remove(int N) </em>removes the front <em>N </em>elements from the queue; throws <em>QueueUnderflowException </em>if less than <em>N </em>elements are in the queue.</li>

  </ul></li>

 <li> Add the following methods to the <em>ArrayCollection </em>class, and create a test driver for each to show that they work correctly. <strong>Note </strong>that you can find the implementation of the classes mentioned here in <em>zip </em>or check the book for the implementation details. Some classes require imports from other packages. All the packages you need and classes can be found in the code I shared with you. In order to practice your array coding skills, code each of these methods by accessing the internal variables of the ArrayCollection, not by calling the previously defined public methods of the class. Make sure you have a driver class that will put your methods to use (and also serve to check whether your methods are correct).

  <ul>

   <li><em>String toString() </em>creates and returns a string that correctly represents the current collection. Such a method could prove useful for testing and debugging the class and for testing and debugging applications that use the class. Assume each stored element already provides its own reasonable <em>toString() </em></li>

   <li><em>int count(T target) </em>returns a count of the number of elements <strong>e </strong>in the collection such that <strong>equals(target) </strong>is true.</li>

   <li><em>void removeAll(T target) </em>removes all elements <strong>e </strong>from the collection such that <strong>equals(target) </strong>is true.</li>

   <li> ArrayCollection<em>&lt;</em>T<em>&gt; </em>combine(ArrayCollection<em>&lt;</em>T<em>&gt; </em>other) creates and returns a new ArrayCollection object that is a combination of this object and the argument object. Choose any way to combine these collections and make sure you include comments to explain what the combination is. <strong>(Note: add the signature of this method to </strong><em>CollectionInterface</em></li>

  </ul></li>

 <li> Create a <em>FacebookUser </em>class that includes <em>numFriends </em>and <em>username </em>attributes of type int and String, respectively, both set by a constructor. The attribute <em>numFriends </em>represents the number of friends a user with <em>username </em> Implement an <em>equals </em>method that such that two FacebookUsers are equal if they have the same username.</li>

 <li>(Bonus Exercise) <em>This one is not as hard as the next Bonus Exercise.</em></li>

</ol>

An <em>Advanced Set </em>includes all the operations of a <em>Basic Set </em>plus operations for the union, intersection, and difference of sets.

<ol>

 <li>Define an Advanced Set interface.</li>

 <li>Implement the Advanced Set using an unsorted array; include a testdriver that demonstrates your implementation works correctly.</li>

</ol>

Hint: you can find the implementation of Basic Set in ch05.zip code, and also you can check the book for more details.

<ol start="6">

 <li>(Bonus exercise) <em>This is a rather challenging but very interesting exercise from Chapter 4.</em></li>

</ol>

Design and code the Queue ADT operations using a circular linked implementation. With the circular linked list we don’t need to maintain two pointers for front and rear. We can maintain a pointer to the last inserted node and front can always be obtained as next of last. The book gives you some hints on how to do this in the end of Section 4.5.