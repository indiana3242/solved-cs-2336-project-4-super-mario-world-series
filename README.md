Download Link: https://assignmentchef.com/product/solved-cs-2336-project-4-super-mario-world-series
<br>
<strong>Pseudocode</strong>

<strong>KEY ITEMS:</strong> Key items are marked in red. Failure to include or complete key items will incur additional deductions as noted beside the item.

<strong>Submission and Grading:</strong>

<ul>

 <li>All project source code will be submitted in zyLabs.

  <ul>

   <li>Projects submitted after the due date are subject to the late penalties described in the syllabus.</li>

  </ul></li>

 <li>Each submitted program will be graded with the rubric provided in eLearning as well as a set of test cases. These test cases will be posted in eLearning after the due date. – zyLabs will provide you with an opportunity to see how well your project works against the test cases. Although you cannot see the actual test cases, a description will be provided for each test case that should help you understand where your program fails.</li>

 <li><strong>Type your name and netID in the comments at the top of all files submitted. (-5 points)</strong></li>

</ul>

<strong>Objective:</strong> Utilize common features of a hash table in the design of an object-oriented program

<strong>Problem:</strong> Now that the Mushroom Kingdom League has ended and crowned a new champion, it is time to determine the league leaders in several different baseball categories. Being the only person in the Mushroom Kingdom that knows how to write a computer program, you have been asked by Princess Peach herself to write a program that will determine the league leaders.

<strong>Pseudocode:</strong> Your pseudocode should describe the following items

<ul>

 <li>Identify the functions you plan to create for each class

  <ul>

   <li>You do not have to include pseudocode for basic items like constructors, accessors, mutators</li>

  </ul></li>

 <li>For each function, identify the following

  <ul>

   <li>Determine the parameters</li>

   <li>Determine the return type</li>

   <li>Detail the step-by-step logic that the function will perform</li>

  </ul></li>

</ul>

<strong>Classes</strong>

<ul>

 <li>Design a class suitable for holding player information

  <ul>

   <li>Be careful of including members that may become stale</li>

   <li>Name the file <strong>Player.java</strong></li>

  </ul></li>

 <li>Use good programming practice for classes – proper variable access, mutators and accessors, proper constructors, etc.</li>

 <li>Remember that classes exist to be used by other people. Just because you don’t use it in the program doesn’t mean it shouldn’t be coded and available for others to use in theirs.</li>

 <li>As with previous projects, you are open to design the classes as you see fit</li>

</ul>

<strong>Details:</strong>

<ul>

 <li>Start the program by prompting the user for the input filename.

  <ul>

   <li>This would normally be hardcoded in an application, but zyLabs requires a filename for multiple test files</li>

  </ul></li>

 <li>This program will calculate stats based on the game play-by-play

  <ul>

   <li>Each possible plate appearance is provided in a file named <strong>keyfile.txt</strong> &#x25aa; This will be used for every test case &#x25aa; <strong>Do not prompt for this file</strong></li>

   <li>Each player’s plate appearance will be given in a file</li>

   <li>Analyze each plate appearance to determine the result (hit, out, strikeout, etc.)</li>

   <li>Record the information for each player and determine leaders</li>

  </ul></li>

 <li>Hash tables will be used for quick lookup of results and players (-15 points if not)

  <ul>

   <li>After reading the play, a hash table will be used to determine the result (i.e. H, O, K, etc.)</li>

   <li>For example, a play of 1B (single) is a hit (H) (which as you know is also an at-bat and a plate appearance)</li>

   <li>The result is then recorded for the player &#x25aa; Use a hash table to find the player and update the stats</li>

   <li>You may utilize the built-in Java hashmap</li>

   <li><strong>EXTRA CREDIT</strong>

    <ul>

     <li>Instead of using the built-in Java hashmap, create your own hashmap class</li>

     <li>Make the hashmap class generic (5 points)</li>

     <li>Implement double hashing for collision handling ( 7 points)</li>

     <li>Implement a rehashing function ( 8 points)

      <ul>

       <li>The size of the new hashmap will be the next highest prime number after doubling the old size</li>

      </ul></li>

     <li>The filename for the HashMap class will be <strong>HashMap.java</strong></li>

    </ul></li>

  </ul></li>

 <li>If you use the built-in Java hashmap you must submit an empty file named</li>

</ul>

HashMap.java

<ul>

 <li>This is a restriction of the system in which a list of all files to be compiled must be provided in advance.</li>

 <li>Stats will be calculated for the following categories:</li>

 <li>Batting Average (BA)

  <ul>

   <li>Batting average = hits / at-bats</li>

  </ul></li>

 <li>On-base percentage (OB%)

  <ul>

   <li>On-base percentage = (hits + walks + hit by pitch) / plate appearances</li>

   <li>Strikeouts (K)</li>

   <li>Walks (BB)</li>

   <li>Hit by Pitch (HBP)</li>

   <li>Hits (H)</li>

  </ul></li>

 <li>Calculate all stats per person and record the highest values for each category

  <ul>

   <li>There may be ties for the leaders</li>

   <li>If there is a tie, output all names for tied value</li>

  </ul></li>

 <li>Any global variables used must be constant</li>

 <li>Use as few variables as possible</li>

</ul>

<strong>Input:</strong> All input will be read from a file. Each line in the file will represent a plate appearance and will follow the same format.

<ul>

 <li>Line format: _H/A_space_player name_space_plate appearance

  <ul>

   <li>H Mario 6-3</li>

  </ul></li>

 <li>The name will be a single word.</li>

 <li>The plate appearance will be a sequence of characters (a code) describing what happened

  <ul>

   <li>All plate appearance “codes” will be valid and will be present in the results file provided</li>

  </ul></li>

 <li>Errors are considered an at-bat</li>

 <li>Walks, sacrifices and hit by pitches are not considered an at-bat</li>

 <li>Each line in the file will end in a newline (except the last line which may or may not have a newline)</li>

 <li>The total number of plate appearances may be different for each player</li>

 <li>The input file will have multiple entries for the same person

  <ul>

   <li>Combine data for each player</li>

  </ul></li>

</ul>

<strong>Output:</strong>

<ul>

 <li>All output will be written to a file – <strong>leaders.txt</strong></li>

 <li>Divide the player information into home and away teams.</li>

 <li>For each team, the player names will be in alphabetical order with his/her data on the same line</li>

 <li>Output format for the away team

  <ul>

   <li>AWAY</li>

   <li>Player data – display each player’s data in the following order with a tab between each field</li>

   <li>Player name</li>

   <li>At-bats</li>

   <li>Hits</li>

   <li>Walks</li>

   <li>Strikeouts</li>

   <li>Hits by pitch</li>

   <li>Sacrifices</li>

   <li>Batting average</li>

   <li>On-base percentage</li>

   <li>Write a newline after the on-base percentage (there is no tab before the newline)</li>

  </ul></li>

 <li>After all away data has been displayed, display another newline

  <ul>

   <li>This will put a blank line between the Home and Away sections</li>

  </ul></li>

 <li>Display the Home team data with the same format as the Away team

  <ul>

   <li>Display HOME instead of AWAY</li>

  </ul></li>

 <li>After the player data table, display an additional newline and the LEAGUE LEADERS header</li>

 <li>Display the top 3 leaders for each category</li>

 <li>Because of ties all places may not be awarded.

  <ul>

   <li>For example, if there is a 3 way tie for first, there would not be a second or third place.</li>

  </ul></li>

</ul>

<strong>League Leader Order</strong>

<ul>

 <li>Batting Average</li>

 <li>On-Base Percentage</li>

 <li>Hits</li>

 <li>Walks</li>

 <li>Strikeouts</li>

 <li>Hit By Pitch</li>

</ul>

<strong>League Leader Output Format</strong>

<ul>

 <li>CATEGORY_newline

  <ul>

   <li>All caps</li>

  </ul></li>

 <li>value_tab_first leader list_newline</li>

 <li>value_tab_second leader list_newline

  <ul>

   <li>Second leader list is optional</li>

   <li>No second place if first place has 3 or more ties</li>

  </ul></li>

 <li>value_tab_third leader list_newline

  <ul>

   <li>Third leader list is optional</li>

   <li>No third place if first or second place has a tie</li>

  </ul></li>

 <li>newline</li>

</ul>