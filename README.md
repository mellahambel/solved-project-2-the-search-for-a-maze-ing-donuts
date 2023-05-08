Download Link: https://assignmentchef.com/product/solved-project-2-the-search-for-a-maze-ing-donuts
<br>
<p class="centered">Important Deadlines

<table border="0" cellpadding="0">

 <tbody>

  <tr>

   <td width="300">Project released</td>

   <td width="120">Fri. April 10</td>

   <td></td>

  </tr>

  <tr>

   <td>Partner selection</td>

   <td>Mon. April 13</td>

   <td><a href="https://norfolk.cs.washington.edu/htbin-php/gtng/gtng.php">Pair up by 11:59pm</a></td>

  </tr>

  <tr>

   <td>Phase A Due</td>

   <td>Wed. April 22</td>

   <td>Electronic turnin by 11:59 pm using <a href="https://catalysttools.washington.edu/collectit/dropbox/jaf1978/5335">this online dropbox</a></td>

  </tr>

  <tr>

   <td>Phase B Due</td>

   <td>Wed. May 06</td>

   <td>Electronic turnin by 11:59 pm</td>

  </tr>

 </tbody>

</table>

<hr class="centered" size="2" width="100%">

5/5 - (2 votes)

<h2>Outline</h2>

<ul type="disc">

 <li><a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/#Introduction">I. Introduction</a></li>

 <li><a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/#Objectives">II. Learning Objectives</a></li>

 <li><a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/#Assignment">III. Assignment and Algorithm Overview</a></li>

 <li>

  <ul type="circle">

   <li><a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/#PhaseA">IIIa. Phase A: DFS and BFS</a></li>

   <li><a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/#PhaseB">IIIb. Phase B: Priority Queues and Best-First Search</a></li>

  </ul></li>

 <li><a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/#Requirements">IV. Detailed Requirements</a></li>

 <li>

  <ul type="circle">

   <li><a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/#Clarifications">IVa. Clarifications</a></li>

   <li><a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/#IO">IVb. Input and Output</a> <span class="red strong"><strong>(important)</strong></span></li>

   <li><a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/#README">IVc. README.txt Questions</a></li>

   <li><a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/#Grading">IVd. Grading Breakdown</a></li>

  </ul></li>

 <li><a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/#Code">V. Provided Code</a></li>

 <li><a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/#Logistics">VI. Logistics and Extra Information</a>

  <ul>

   <li><a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/#Teams">Teams</a></li>

   <li><a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/#Subversion">Subversion and Group Spaces</a></li>

   <li><a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/#Testing">Testing (JUnit)</a></li>

  </ul></li>

 <li><a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/#Starting">VII. Getting Started</a></li>

 <li><a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/#Above">VIII. Going Above and Beyond</a></li>

 <li><a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/#Files">IX. What to Turn In</a>

  <ul type="square">

   <li><a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/#TurninA">Phase A</a></li>

   <li><a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/#TurninB">Phase B</a></li>

  </ul></li>

</ul>

<h2>I. Introduction</h2>

It is an incredibly serendipitous day for you at the Paul Allen Center. A mysterious bearded benefactor has appeared during the night and has left behind donuts for the entire CSE 326 class! You’ve managed to get out of bed at a yawningly-early <b><i>10 AM</i></b>, meaning you have first dibs on all the yummy goodness of fresh-baked donuts <b><i>if</i></b> you can get to them in time (and the always hungry grad students from the night before haven’t beat you there). Unfortunately, the Allen Center space czars just happened to have decided to rearrange all the furniture during the night (as part of their experimentation with different settings in the new building), turning the entire building into one complex and mystifying maze. You haven’t had your morning coffee yet, and you just don’t feel like running around looking for donuts—but you’re so hungry! Why not let your computer solve the maze and find the donuts FOR you?

<h2>II. Learning Objectives</h2>

In this assignment, you will:

<ul type="disc">

 <li>Work on the <tt>PriorityQueue</tt> ADT, and implement your own data structures.</li>

 <li>Gain experience with systematic testing.</li>

 <li>Explore the similarities and differences between recursive and iterative algorithms.</li>

 <li>See an application of the <tt>Stack</tt>, <tt>Queue</tt>, and <tt>PriorityQueue</tt> ADT’s in maze search.</li>

 <li>Gain experience analyzing and modifying an existing code base.</li>

 <li>Train your computer to do your most important tasks for you—like finding donuts!</li>

</ul>

<h2><a id="Assignment" name="Assignment"></a>III. Assignment and Algorithm Overview</h2>

For the <i>complete</i> assignment, you are required to write several new maze-solving <tt>MazeRunner</tt> classes, each with one or more associated data structures. There should be one <tt>MazeRunner</tt> class for each of the following algorithms:

<ol start="1" type="1">

 <li>Depth-First Search (DFS) — please implement this search with a <tt>Stack</tt><i>More information on DFS can be found <a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/t2.html#dfs">here</a>.</i></li>

 <li>Breadth-First Search (BFS) — please implement this search with a <tt>Queue</tt><i>More information on BFS can be found <a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/t2.html#bfs">here</a>.</i></li>

 <li>Best-First Search (not abbreviated for obvious reasons) — please implement this using your priority queue implementations, with your MazeRunnerLauncher choosing among implementations as specified in Section IVb<i>More information on Best-First Search can be found <a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/t2.html#bestfirst">here</a>.</i></li>

</ol>

<h2>IIIa. Phase A: DFS and BFS</h2>

Your task for Phase A is to implement a stack, a queue, a depth-first search maze runner and a breadth-first search maze runner, according to the interfaces provided. Your data structure implementations should automatically grow (if interested you may also make them shrink—this is optional) as necessary. You should test these implementations to be sure they are correct before proceeding to Phase B. We’ll also ask you to design and implement a collection of unit tests to verify that your code works properly.

<blockquote>

 <em>Note:</em> Growing an array implementation one element at a time is not likely to be the most time efficient solution; if you use arrays, try to come up with a more time-efficient solution. You may reuse any code you wrote for Project #1 for this purpose but be sure that you implement the interfaces provided for this project.

</blockquote>

You are free to implement the stacks and queues as you wish, although arrays are as simple as anything. Our usual rule prohibiting use of the Java class libraries to do the actual work remains. You should also take this opportunity to get an understanding of how the three graph search algorithms described <a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/t2.html">here</a> work for a <em>general graph</em>.

You should also implement unit tests for your data structures and verify that your code passes the tests. You should turn in a TESTING.txt file with an informal description of your test plan. Summarize the tests you implemented and explain how they provide comprehensive test coverage for your classes. This should not just be a dump of the test names and comments from the code file—we can read that. What we want is to get an idea of the thinking behind what you did. We recommend use of JUnit, but this is not a requirement. The testing strategy you discuss in TESTING.txt will be evaluated as a part of the project, but the code of your actual unit tests will not.

<h2>IIIb. Phase B: Priority Queues and Best-First Search</h2>

For Phase B you will write several implementations of the Priority Queue ADT and a best-first search maze runner to use them. Specifically, you will write a binary heap, a three heap, a d-heap, and a pointer-based heap (one of: skew heap, leftist heap, or binomial queue). You will also need to modify <tt>MazeRunnerLauncher.java</tt> to accept command line arguments appropriate for each type of maze runner or priority queue. Finally, you’ll need to answer the questions from the write-up and turn them in in README.txt.

<span class="red">All of this is more work than it sounds, so do not leave it to the last minute.</span>

<h2>IV. Detailed Requirements</h2>

<h3>IVa. Clarifications</h3>

<ul>

 <li>In your implementations of Queue and PriorityQueue, you should throw a NoSuchElementException (java.util.NoSuchElementException) if dequeue, peek, findMin, or deleteMin are called on an empty queue. Obviously, this means it’s OK to import <tt>java.util.NoSuchElementException</tt> in your code.</li>

 <li>Your d-heap class should implement the PriorityQueue interface.</li>

 <li>When writing your additional <b>pointer-based implementation</b> (either a LeftistHeap or a SkewHeap or a BinomialQueue) of a PriorityQueue, <b>do not use implementations of these that you may find on any web site – including the web site for our text book! Such use will be considered a violation of our collaboration policy.</b> You are free to refer to skeleton code provided in our text book or in other course materials; however, the code you turn in should be your own.</li>

 <li>Your priority queue implementations must accept <tt>Comparable</tt> objects.Many classes such as <tt>String</tt> and <tt>Integer</tt> implement the <tt>Comparable</tt> interface. In Phase B you will need to modify/create some more classes that implement the<tt>Comparable</tt> interface (in other words, writing your own <tt>compareTo</tt> method). Then you will be able to have priority queues containing those objects. Unlike your stacks implementations for Project1 that were hardcoded to use doubles, your implementations of the <tt>Stack</tt>, <tt>Queue</tt>, and <tt>PriorityQueue</tt> interface need to use generics. Your implementations need to use <tt>compareTo</tt> when comparing elements so the code will work on any <tt>Comparable</tt> object. More information about Java’s <tt>Comparable</tt> interface may be found at <a href="http://java.sun.com/j2se/1.5.0/docs/api/java/lang/Comparable.html">Sun’s website</a>. In addition, you might find <a href="https://www.cs.washington.edu/education/courses/cse143/06au/notes/notes21.html%0d%0a">this</a> description from CSE 143 of Fall 2006 to be useful. Both generics and the <tt>Comparable</tt> interface are discussed in section 1.5 of the Weiss text, and there is a good <a href="http://java.sun.com/docs/books/tutorial/extra/generics/index.html">tutorial</a> on Sun’s web site. The tutorial is based on <a href="http://java.sun.com/j2se/1.5/pdf/generics-tutorial.pdf">this paper</a> by Gilad Bracha, one of the Java language designers.</li>

</ul>

<h3>IVb. Input and Output</h3>

<h4>INPUT:</h4>

<ul type="disc">

 <li>You are required towrite MazeRunner classes for BFS, DFS, and BestFS. Please modify MazeRunnerLauncher to use <b>EXACTLY</b> the following parameters to determine which search algorithm to use:

  <table>

   <tbody>

    <tr>

     <td width="50"></td>

     <td width="100">-BFS</td>

     <td>use BFS</td>

    </tr>

    <tr>

     <td></td>

     <td>-DFS</td>

     <td>use DFS</td>

    </tr>

    <tr>

     <td></td>

     <td>-BestFS</td>

     <td>use BestFS</td>

    </tr>

   </tbody>

  </table></li>

 <li>You should assure that <b><i>all</i></b> of your PriorityQueue implementations work with MazeRunner.  Please modify MazeRunnerLauncher to use <b>EXACTLY</b> the following parameters to determine which priority queue implementation to use when needed:

  <table>

   <tbody>

    <tr>

     <td width="50"></td>

     <td width="100">-bin</td>

     <td>use Binary Heap</td>

    </tr>

    <tr>

     <td></td>

     <td>-three</td>

     <td>use Three Heap</td>

    </tr>

    <tr>

     <td></td>

     <td>-dheap #</td>

     <td>use a d-heap, where d = #</td>

    </tr>

    <tr>

     <td></td>

     <td>-ptr</td>

     <td>use your pointer-based heap (Leftist, Skew or Binomial)</td>

    </tr>

   </tbody>

  </table></li>

 <li>The <tt>MazeFactory</tt> class reads a maze from a text file specified on the command prompt. The file format is a picture of the maze. There is also some header information at the front that gives the dimensions of the maze (width, then height). In the maze, ‘<code>-</code>‘ and ‘<code>|</code>‘ are used for walls, ‘ ‘ for rooms and unblocked passages, ‘<code>+</code>‘ for the corners of the rooms, ‘<code>*</code>‘ for the start, and ‘<code>O</code>‘ for the donut. (Note: start and donut can be in any cells in the maze, not just the corners.) Once you find the donut, you get to chow down and then exit out of the maze. For example, the following is a legal maze :<pre>                7 5                +-+-+-+-+-+-+-+                |*|   | | |   |                + +-+ + + +-+ +                |   |   |     |                + + + +-+ +-+ +                | |   |     | |                + +-+-+ +-+-+ +                |       |     |                +-+ + +-+-+ +-+                |   |        O|                +-+-+-+-+-+-+-+            </pre></li>

</ul>

There are some sample input files in the starter files mentioned above that you can use to test your program. <strong>You are highly encouraged to write (and share with your classmates!) other test mazes to run your</strong> <tt>MazeRunner</tt> <strong>on</strong>. Send them to us or post them on the message board (preferred).

<h4>OUTPUT:</h4>

After solving a maze, your <tt>MazeRunner</tt> should output the name of the search algorithm used followed by the solution path calculated by the search. The path should be given on a single line and should consist of the printed cells from the start to the exit, separated by single spaces. On the next line should be the length of the solution path, and on the following line should be the number of cells visited in the search, including cells that were not completely explored (i.e., marked “Visit in progress” when the search completes).  For example, the output for the above maze might be:

<pre>                Random search:                (0,0) (0,1) (0,2) (0,3) (1,3) (2,3) (2,4) (3,4) (4,4) (5,4) (6,4)                Length of path: 10                Number of cells visited: 15            </pre>

Please note that the start and end cells are both included, but the length of the path is the number of edges traversed ( <strong>one less</strong> than the number of cells visited). Please do not include extraneous output. For the other search algorithms, use text “<tt>Breadth-first search:</tt>“, “<tt>Depth-first search:</tt>” and “<tt>Best-first search:</tt>“.

The solution displayed above corresponds to the solution path shown below with dots:

<pre>                +-+-+-+-+-+-+-+                |*|   | | |   |                + +-+ + + +-+ +                |.  |   |     |                + + + +-+ +-+ +                |.|   |     | |                + +-+-+ +-+-+ +                |. . .  |     |                +-+ + +-+-+ +-+                |   |. . . . O|                +-+-+-+-+-+-+-+            </pre>

Note that your <tt>MazeRunner</tt> does <i>not</i> need to output a text-graphical solution such as the one displayed above.

Note also that a search very likely involves visiting many nodes that are not on the final solution path. You will have to explore ways of keeping track of the solution path from the collection of nodes you visited. <tt>RandomMazeRunner</tt> gives an example of how this might be done. You will need to modify this technique to work for your algorithms.

<h3>IVc. README.txt Questions</h3>

Your README.txt should contain the following information and answer the following questions:

<ol start="1" type="1">

 <li>The names of your team members and your team’s name</li>

 <li>A breakdown of the work – a brief who-did-what description.</li>

 <li>How much time did you spend on this project?</li>

 <li>Acknowledgement of any assistance you received from anyone but your partner, the course staff, or the Weiss book.</li>

 <li>Did you do any extra credit?  If so, describe what you did and give instructions on how to run your code.</li>

 <li>Why is it more important for DFS than BFS to check whether a cell has been visited yet?</li>

 <li>If you gave your MazeRunners a maze that was too large to fit in main memory, which would likely run faster, BFS or DFS? (Any reasonable answer—as long as it is justified—will be accepted.)</li>

 <li>In what ways are DFS and Best-first search similar? How are BFS and Best-first similar?</li>

 <li>Why is it important that a heuristic be easy to compute? Why is it important that a heuristic yield unique (or almost unique) values?</li>

 <li>Why is BFS guaranteed to find the <i>shortest</i> path? Are the other two algorithms guaranteed to find the shortest path? If yes say why, if not, give a counter example.</li>

 <li>What are the tradeoffs between a pointer vs. array-based heap? In particular, what are the tradeoffs between a binary heap, a threeheap, and a pointer-based heap? Some possible topics to cover include runtime, coding complexity, and memory usage. Did you observe any differences (for example in runtimes or memory use) between using these three for the larger maze inputs?  (Just note if you noticed anything, it is fine if you did not.  You are welcome to explore this question in more detail (timings, measurements, calculations) for extra credit.)</li>

 <li>In general (not necessarily in the context of this project), why could it be better to use a sorted array implementation of a priority queue versus a binary heap? Why could it be worse?</li>

 <li>What did you enjoy about this assignment? What did you hate? Could we have done anything better?</li>

</ol>

<h2>IVd. Grading Breakdown</h2>

The amount of code required for this project is actually very small. A significant part of your grade will be based on your program design and your README.txt.

<ul type="disc">

 <li>Correctness – 40%</li>

 <li>Architecture/design – 30%</li>

 <li>README.txt – 30%</li>

</ul>

Look at the <a href="https://www.cs.washington.edu/education/courses/326/CurrentQtr/grading-policies.shtml">course grading policy</a> for a more detailed explanation on grading guidelines.

<h2>V. Provided Code</h2>

The skeleton code can be downloaded as <a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/p2code.zip">p2code.zip</a>. Some of the important files are:

<ul type="disc">

 <li><tt>PriorityQueue.java</tt> — interface for a PriorityQueue ADT. All of your heaps should implement this..</li>

 <li><tt>Stack.java</tt> — interface for a Stack ADT.</li>

 <li><tt>Queue.java</tt> — interface for a Queue ADT.</li>

 <li><tt>MazeRunnerLauncher.java</tt> — the launcher that you’ll need to modify to accept the specified command line arguments and construct the appropriate MazeRunner</li>

 <li><tt>MazeRunner.java</tt> — interface that each MazeRunner should extend. You may be able to prevent a significant amount of code duplication by handling your MazeRunner inheritance appropriately.</li>

</ul>

For Phase A we provide interfaces for a <tt>Stack</tt> and a <tt>Queue</tt>, as we as an example <tt>MazeRunner</tt> (<tt>RandomMazeRunner</tt>, which picks the direction to explore in a random fashion.). You must write the implementations of the provided <tt>Stack</tt> and <tt>Queue</tt> interfaces as described <a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/#PhaseA">above</a>. Your own <tt>MazeRunner</tt> classes should inherit from the abstract <tt>MazeRunner</tt> class.

For Phase B we provide code to read the input maze given as a text file, parse it, and build a <tt>Maze</tt> class object from it, which your algorithm will operate on. We also provide the interface for the Priority Queue ADT, <tt>PriorityQueue.java</tt>. <a name="hint"></a>You must write several implementations of the <tt>PriorityQueue</tt> interface–a BinaryHeap, a ThreeHeap, a DHeap, and a pointer-based priority queue of some kind. For the array-based heaps (BinaryHeap, ThreeHeap, etc.) you can start with a copy of your code from one and make changes as necessary, although making the original code easy to generalize making appropriate use of inheritance may save a lot of time (<strong>hint, hint</strong>).

You are not required to modify any of the provided files besides <tt>MazeRunnerLauncher.java</tt>.

<a name="hint"></a><em>Further documentation on the Maze code architecture and how to get started can be found </em><em><a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/architecture.html">here</a></em>. If you find the large codebase a bit overwhelming, this is good place to start.

<h2>VI. Logistics and Extra Information</h2>

<h3>Teams</h3>

You are encouraged (although not required) to work with a partner of your own choosing for this project. You may choose how to divide the work between the two of you under three conditions:

<ul>

 <li>You must document each team member’s effort in the README file (record this now so you have the info for the Phase B readme file);</li>

 <li>Work together so that you <i>both</i> understand your answers to the questions answered in the README (for Phase B);</li>

 <li>Understand (at least) at a high level how your team member’s code is structured and how it works (code for both Phases A &amp; B).</li>

</ul>

Remember to test your team’s code as a whole to make sure that your portions work together properly! Also, be aware that except in extreme cases and provided you notify us <i>in advance</i> of the deadline, all team members will receive the same grade for the project.

<h3>Subversion and Group Spaces</h3>

If you would like to use a shared group directory, please contact one of the TA’s for instructions. This is NOT necessary, just optional if it is your preference.

We can create shared space on <tt>attu</tt> for each group if you wish to set up a subversion repository; we’ll have more details once the project groups are finalized.

Each group can have a Subversion repository available if you wish to use a repository to coordinate modifications to your code base. Subversion is useful for both teams and individuals, as it allows you to store backups of your code in a central server. For teams, each team member may be working on the code concurrently, and Subversion checks for conflicts when the changes are committed. For more information about Subversion, try the <a href="http://svnbook.red-bean.com/en/1.4/svn.tour.initial.html">Subversion book</a>. That link describes how to use Subversion on the command-line; you can also use TortoiseSVN on Windows (<a href="http://tortoisesvn.net/docs/release/TortoiseSVN_en/tsvn-dug.html">documentation</a>) or the Subclipse plugin for Eclipse (not yet installed on the lab machines, but go <a href="http://subclipse.tigris.org/servlets/ProjectProcess?pageID=p4wYuA">here</a> for install instructions for your own machine and <a href="http://open.ncsu.edu/se/tutorials/subclipse/index.html#section4_0">here</a> for usage instructions). The repository address is:

<blockquote>

 <tt>svn+ssh://<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="95e0e6f0e7fbf4f8f0d5f4e1e1e0bbf6e6bbe2f4e6fdfcfbf2e1fafbbbf0f1e0">[email protected]</a>/projects/instr/09sp/cse326/project2/groupname</tt>

</blockquote>

where <tt>username</tt> is your username and <tt>groupname</tt> is <tt>username1-username2</tt> for pairs and <tt>username</tt> for loners.

<h3>Testing Strategy</h3>

To facilitate understanding of this rather complex project, and to encourage good modular decomposition and “unit testing” (testing small pieces of code instead of testing the entire program all at once), we suggest improving and testing your “helper” data structures (i.e. <tt>Stack</tt>, <tt>Queue</tt>, <tt>BsinaryHeap,</tt> <tt>ThreeHeap</tt>, etc.) without worrying about the Maze-related code.

Your tests should be:

<ul>

 <li><strong>Comprehensive</strong> – you should cover all types of behavior your code might exhibit. For example, if a method’s specifiication says it might throw an exception in certain cases, you should test those cases in addition to normal behavior. Also be sure to check edge cases – maybe your stack works fine when there are five elements, but what if there is just one? Or zero?</li>

 <li><strong>Modular</strong> – as much as possible, test each method separately, and keep the tests small and self-contained.</li>

 <li><strong>Concise</strong> – good test coverage is not synonymous with having lots of tests that are fundamentally the same. (Hint: You may be able to reuse a single suite of tests for both implementations of the priority queue if you think about how to take advantage of interface types and maybe inheritance in the test code. Massive cut-‘n-paste is not a good an alternative.)</li>

</ul>

Using JUnit is straightforward. Your section should cover the basics of writing test cases; to run a test case from the command line, do:

<blockquote>

 <tt>java junit.textui.TestRunner MyTestCase</tt>

</blockquote>

where MyTestCase if the name of one of your TestCase classes. Eclipse has a JUnit GUI built in; see <a href="https://www.eclipse.org/resources/resource.php?id=408">here</a> for a howto.

<h2>VII. Getting Started</h2>

After downloading the provided code, compile everything and try to run the provided random mazeRunner from the launcher class as follows:

<pre>       % java MazeRunnerLauncher -r sample-inputs/maze2.txt</pre>

(Or try one of the other mazes in sample-inputs) The “-r” option invokes the random maze runner. Take a look at <tt>RandomMazeRunner.java</tt> to get a general idea of how things work. After understanding this file, make a copy (say <tt>BFSMazeRunner.java</tt>) and try implementing a better algorithm.

To add these files to your SVN repository, you should do an <tt>svn add &lt;filename&gt;</tt> for each file. To import into Eclipse, you can drag-and-drop the files into your project or go to File-&gt;Import…

<h2>VIII. Going Above and Beyond</h2>

The following suggestions are meant for you to try if you finish the requirements early. Be sure to clearly describe what you did and how to run it in your README.txt. Recall that any extra-credit points you earn for these are kept separate from your assignment score and will be used to adjust your grade at the end of the quarter, as detailed in the <a href="https://www.cs.washington.edu/education/courses/326/CurrentQtr/grading-policies.shtml">course grading policy</a>.  Please don’t put extra credit code in your main turnin—instead, put modified versions of your files in an archive <tt>extracredit.zip</tt>.

<ul type="disc">

 <li>Using the Manhattan distance has several problems, including the fact that the <tt>MazeRunner</tt> is sometimes fooled into going down “dead ends” in the maze. What <b>other heuristics</b> might be used in your <tt>MazeRunner</tt>? When might your heuristics perform better than the Manhattan distance, and when might they perform worse (you may want to consider factors such as space usage and time to calculate the heuristic)? Implement and run your Best-First <tt>MazeRunner</tt> with its new heuristic on several mazes and report which heuristic performed better, and in what type of maze it did better in. (2 points)</li>

 <li>There is a variation of the Best-First Search heuristic called A* (pronounced “A-Star”). A* has some theoretically and practically interesting qualities. Take a look <a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/Astar.html">here</a> for a description of the algorithm. Implement A* and give a description of why the algorithm works and how it compares to your other search algorithms (e.g. When does it work better? When does it work worse? Which one would you generally choose to use? etc.) (2 points)</li>

 <li>Add a <b>maze generator</b> to your program or applet. (4 points)</li>

 <li>Create a <b>visualization routine</b> that runs as the maze is being solved. Pop up a window that shows the graph, with different colors used to indicate the state of each room. Drawing routines will need to be invoked when the maze is create and from setState. Include instructions in your README.txt file on how to run the visualization as a Java program and/or as an applet. Please have it so we can run the visualizer in your program using the “-v” oprion to <tt>MazeRunnerLauncher</tt>. <i>Hint: have your visualizer class extend JFrame and implement MazeChangeListener.</i>(4-6 points, depending on how nice it looks.)</li>

 <li><b>Choose your own extension!</b>: Exercise your creativity and think how you can extend this project. Can your <tt>MazeRunner</tt> handle mazes with multiple exits? What about rendering your maze in 3-D? If you do anything that alters the basic design specifications, check with the staff, and document what you did. Of course, your code should still meet the basic requirements.</li>

</ul>

<h2>IX. What to Turn In</h2>

Phases A and B will be graded together when your entire assignment is turned in with Phase B. However, 15% of your grade will be based upon the “in-progress” checkin for Phase A. Although 15% is a relatively small fraction, you are highly encouraged to successfully complete all of Phase A by this deadline, as there is much more work to do in Phase B.

<b>Only one person from each team should submit. The same person should submit both Phases A and B.</b> You should submit all of the Java code you wrote.

<h3>Phase A Turn-in</h3>

For Phase A please include the following files plus any others you find necessary:

<ul>

 <li><tt>MazeRunnerLauncher.java</tt> – Main launcher file, with added options to invoke your mazerunners, etc.</li>

 <li><tt>MazeStack.java</tt> – Your stack implementation</li>

 <li><tt>MazeQueue.java</tt> – Your queue implementation</li>

 <li><tt>DFSMazeRunner.java</tt> – Your DFS maze runner implementation</li>

 <li><tt>BFSMazeRUnner.java</tt> – Your BFS maze runner implementation</li>

 <li><tt>TESTING.txt</tt> – Your testing strategy description</li>

</ul>

<h3>Phase B Turn-in</h3>

For Phase B, turn in all your code for this assignment (from both Phase A and Phase B). So you’ll turn in the following files plus any others you find necessary:

<ul>

 <li><a href="http://courses.cs.washington.edu/courses/cse326/09sp/projects/proj2/#TurninA">Files turned in in Phase A</a></li>

 <li><tt>BinaryHeap.java</tt> – Your binary heap implementation</li>

 <li><tt>ThreeHeap.java</tt> – Your three heap implementation</li>

 <li><tt>DHeap.java</tt> – Your d-heap implementation</li>

 <li>Your pointer-based priority queue implementation, <strong>one</strong> of

  <ul>

   <li><tt>LeftistHeap.java</tt></li>

   <li><tt>SkewHeap.java</tt></li>

   <li><tt>BinomialQueue.java</tt></li>

  </ul></li>

 <li><tt>BestFSMazeRunner.java</tt> – Your best-first maze runner implementation</li>

 <li><tt>README.txt</tt> – Your answers to the assignment write-up</li>

 <li><tt>extracredit.zip</tt> – Any extra credit work you’ve done above and beyond the assignment ought to be placed in a separate zip file</li>

 <li>Any supporting classes required to make anything else you’ve turned in work (wrapper classes, additional abstractions, etc.)</li>