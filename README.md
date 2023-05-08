Download Link: https://assignmentchef.com/product/solved-si507-homework-4-classes-and-inheritance
<br>
<h2><strong>Homework Objective:</strong></h2>

Demonstrate the ability to:

<ul>

 <li>Understand how Python classes contain

  <ul>

   <li>data representations (attributes, or instance variables)</li>

   <li>ways to interact with class instances (methods)</li>

  </ul></li>

 <li>Become familiar with defining classes with and without inheritance</li>

 <li>Implement and use classes and inheritance</li>

 <li>Understand how and why to implement special class methods __init__ and __str__</li>

</ul>

<h2><strong>Supporting Material:</strong></h2>

File: <a href="https://www.dropbox.com/s/wi6qestw1wzooyf/hw4.py?dl=0">hw4.py</a>

Reading: <a href="https://www.programsinformationpeople.org/runestone/static/publicPIP/index.html">chapters on classes and inheritance</a>

<h3><strong>Part 1: Classes (10pts)</strong></h3>

<h4><strong>Task A: Exploration of a class (2pts)</strong></h4>

For Task A, we are going to explore a class, called <em>Explore_pet</em>, which is already implemented. Please look through the class in the python file.




The class represents a generic pet that can get hungry and/or bored. Depending on the pet’s state, it will print different statements about itself. The pet becomes “bored” when its boredom value exceeds its boredom_threshold, and it becomes “hungry” when its hunger value exceeds its hunger_threshold.




You will see that an instance, <em>coco</em>, has been created. Alter the instance’s hunger and/or boredom value so that if we call print(<em>coco</em>), it would say “I’m Coco. I feel bored. You can teach me new words.” Now create another Pet called <em>brian </em>(with the name “Brian”) and set the values so that print(brian) will output “I’m Brian. I feel hungry. Feed me.”

<h4><strong>Task B: Implementation of Pet class (4pts)</strong></h4>

For the task B, we are going to implement <em>Pet</em> class so that we could use it for any kind of pet: dog, cat, and others. In the python file, you will find <em>Pet</em> class, which you will need to expand. After you finish that, we will use the class and interact with it on the task C. The <em>Pet</em> class should contain:

<ol>

 <li>An additional instance variable

  <ol>

   <li>words: a list of words that the pet knows

    <ol>

     <li>Initially, this should be [“hello”].</li>

    </ol></li>

  </ol></li>

 <li>Additional methods [remember to include the self parameter]

  <ol>

   <li>clock_tick( ): a method called when time passes

    <ol>

     <li>An additional unit of 2 is added to the current hunger</li>

     <li>An additional unit of 2 is added to the current boredom</li>

    </ol></li>

   <li>say( )

    <ol>

     <li>It should print “I know how to say: ” first.</li>

     <li>Then, it should print all the words the instance could say – one word per line</li>

    </ol></li>

   <li>teach(word)

    <ol>

     <li>learns a new word</li>

     <li>boredom_decrement is added to the current boredom; this becomes new boredom. If it goes to negative (boredom_decrement is larger than the current boredom), then the current boredom becomes simply zero.</li>

    </ol></li>

   <li>feed( )

    <ol>

     <li>hunger_decrement is added to the current hunger; this becomes new hunger. If it goes to negative (hunger_decrement is larger than the current hunger), then the current hunger becomes simply zero.</li>

    </ol></li>

  </ol></li>

</ol>

<h4><strong>Task C: Utilization of Pet class (4pts)</strong></h4>

For the task C, we are going to utilize the <em>Pet</em> class that we created in task B.




First, add the method hi( ) to <em>Pet</em>. When hi( ) is called, the <em>Pet </em>should say() (i.e., print) a random word from the list of words that it knows.




Second, complete the implementation of the teaching_session( ) function. teaching_session( ) takes two parameters: a Pet (in the parameter my_pet) and a list of words (in the parameter new_words). Within the function following things happen:

<ul>

 <li>my_pet learns the new_words</li>

 <li>For <strong>each time</strong> my_pet learns a word from the new_words,

  <ul>

   <li>my_pet says a random word he/she knows (hint: use hi( ))</li>

   <li>my_pet prints out her current status (e.g., “I’m Fido and I feel happy” or “I’m Furball and I feel hungry. Feed me”)</li>

   <li>if my_pet is hungry, he/she is fed</li>

   <li>The clock ticks once for my_pet</li>

  </ul></li>

</ul>




Third, create a Pet (you choose the name!) and teach it [‘I am sleepy’, ‘You are the best’,’I love you, too’] through the teaching_session( ).

<h3><strong>Part 2: Inheritance – subclasses (10pts)</strong></h3>

<h4><strong>Task A: Dog and Cat: subclasses of Pet (6pts)</strong></h4>

For the task A, we are going to implement the <em>Dog</em> and <em>Cat</em> subclasses.

<ul>

 <li>In the <em>Dog</em> class, dogs express their moods a bit differently. They always say “arrrf!” at the end. For example, instead of saying “I’m Coco. I feel happy.”, dogs express “I’m Coco, arrrf! I feel happy, arrrf!”; you would delete the period but add “, arrrf!” at the end of each sentence.</li>

 <li>In the <em>Cat</em> class, cats will have an additional instance variable, <em>meow_count</em>. That is, Cat will take two parameters: <em>name</em> and <em>meow_count</em>. We are also going to redefine the hi() method for cats. As opposed to superclass’s hi() method, cats will print the randomly chosen word for the number of <em>meow_count </em> For example, if <em>meow_count</em> was 3 and one random word was “hello”, it should print “hellohellohello”.</li>

</ul>

<h4><strong>Task B: Poodle – a subclass of Dog (4pts)</strong></h4>

First, we will implement a subclass of <em>Dog</em> class: <em>Poodle</em>.

<ul>

 <li><em>Poodle</em>

  <ul>

   <li>Has an additional method called <em>dance</em>, which returns “Dancing in circles like poodles do!”</li>

   <li>When the say method is executed, it will print the dance method first and then the say method from the superclass.</li>

  </ul></li>

</ul>




Second, we are going to create two instances and see if we get what is expected

<ol>

 <li>Create a poodle (you choose the name!) and call the say( )method</li>

 <li>Create a cat (you choose the name and meow_count below 10) and call hi( )method</li>

</ol>




<h3><strong>Extra credit 1 (2pts)</strong></h3>

For the first extra credit, you are going to implement a pet game. You need to create a new python file and save it as pet_game.py. Running the file — python3 pet_game.py — should automatically start the game. The pet game is a modified version of the textbook exercise and we encourage you to take a look at <a href="https://www.programsinformationpeople.org/runestone/static/publicPIP/Inheritance/TamagotchiRevisited.html">the exercise code</a> and understand it. You should simply copy and paste the code from line 107 (def whichone…) to the end. You can ignore any class that you did not implement for the homework. Your pet game should follow additional rules along with the logic from the exercise code.




Additional rules

<ol>

 <li>A new instance variable: self.age

  <ol>

   <li>A pet will initially become an age of 0 and live up to 18 integer units (or years)</li>

   <li><em>Dog</em> – increment of 2 for every clock_tick</li>

   <li><em>Cat</em> – increment of 3 for every clock_tick</li>

   <li>Once either a cat or a dog gets older than 18 years, they will leave the world.</li>

   <li>Any method that needs to be overridden should preserve everything from the superclass.</li>

  </ol></li>

 <li>A game ends when there is no pet except the beginning of the game where a player does not have any pets yet.</li>

 <li>When the game ends, it should provide a player two options to make: play it again or quit.</li>

</ol>

<h3><strong>Extra credit 2 (2pts)</strong></h3>

For the second extra credit, you are going to build <em>Library</em> class and subclasses and create Library simulation. Your library could have different types of media: reserve books, regular books, CDs, Movies, etc. Each media type should have different checkout policies; reserve books can be checked out for 1 integer unit (or day), regular books for 15 days, CDs for 7 days, Movies for 2 days.




First, you need to create a new python file and save it as sim_library.py and running the file — python3 sim_library.py — should automatically start the simulation.




you should do the followings:

<ol>

 <li>Create a class and at least three subclasses representing different media types

  <ol>

   <li>Possible attributes and methods to consider

    <ol>

     <li>self.max_days</li>

     <li>self.days_passed or self.days_remaining</li>

     <li>clock_tick( ): the clock ticks, i.e. advances one day</li>

     <li>checkout( ): check an item out</li>

     <li>item_return( ): return an item</li>

     <li>advance( ):move ahead the number of days</li>

     <li>overdue( ):check if it is overdue</li>

    </ol></li>

  </ol></li>

 <li>When the library simulation begins,

  <ol>

   <li>Catalog should contain at least 6 items – two instances from each subclass</li>

  </ol></li>

</ol>




<strong>Sample run</strong>

What would you like to do?

catalog: show the catalog

checkout &lt;item_number&gt;

return &lt;item_number&gt;

advance &lt;num_days&gt;

account: see account status, including checked out items and overdue items










<strong>What to turn in</strong>:




All codes must be executable. Any code that does not run in Python3 will be given a score of 0.  You can receive partial credit for working programs.

Submit following python module(s):

<ul>

 <li>py</li>

 <li>py (optional)</li>

 <li>py (optional)</li>

</ul>