Download Link: https://assignmentchef.com/product/solved-csci-1133-assignment-10-complex-class
<br>
In this problem you need to create a class named Complex that models a <u><a href="https://en.wikipedia.org/wiki/Complex_number">complex number</a></u><a href="https://en.wikipedia.org/wiki/Complex_number">,</a> numbers of the form x+yi, where x and y are real numbers, and i is the imaginary unit equal to the square root of -1.  In the x+yi representation, we say that x is the real component of the complex number, and y is the imaginary component.  Note that Python already has a built-in Complex class, but this makes for a good, simple example, so we’re going to make our own.  Obviously, you’re not allowed to use the built-in Complex class to implement your Complex class.




Complex objects have two instance variables:

<ul>

 <li>real (a numeric value representing the real component of the complex number)</li>

 <li>imag (a numeric value representing the imaginary component of the complex number)</li>

</ul>




(Note: <strong>Please do not write all of these methods at once.</strong>  Copy the test cases in the section below this into your hw10.py file, and uncomment a few of them at a time as you implement things: make sure that each method works before moving on to the next one.  This is something you should be doing anyway but is especially important when writing long pieces of code like class definitions)




The Complex class must include the following:

<ul>

 <li>__init__(self, real, imag): A constructor with two numeric arguments (not counting self), that initialize the real and imag instance variables, respectively.</li>

</ul>




<ul>

 <li>You must have getter and setter methods for both real and imag. They should have the following signatures:

  <ul>

   <li>get_real(self)</li>

  </ul></li>

</ul>

○ get_imag(self)

○ set_real(self, new_real)

○ set_imag(self, new_imag)




<ul>

 <li>Overload the __str__(self) method so that it returns a string of the format:</li>

</ul>

“<em>&lt;real&gt;</em> + <em>&lt;imag&gt;</em>i”

where <em>&lt;real&gt;</em> and <em>&lt;imag&gt;</em> represent the real and imaginary components of the complex number, respectively.




<ul>

 <li>Overload the + and * operators, so that they take in a Complex object other, and return a new Complex object representing the sum or product (respectively) of the complex numbers represented by self and other. See the Hints section if you’re not familiar with how to add or multiply two complex numbers.  You’ll need to have the following method signatures to overload the operators:

  <ul>

   <li>__add__(self, other)</li>

  </ul></li>

</ul>

○ __mul__(self, other)




<ul>

 <li>Overload the == operator, so that it takes in a Complex object other, and returns True if the two objects are equal (their real components are equal, and their imaginary components are equal), or False You’ll need to have the following method signature to overload the operator:

  <ul>

   <li>__eq__(self, other)</li>

  </ul></li>

</ul>




<strong>Hints: </strong>

<ul>

 <li>Review on how to add/multiply complex numbers: ○ (a + bi) + (c + di) = (a + c) + (b + d)i

  <ul>

   <li>(a + bi)(c + di) = (ac – bd) + (ad + bc)i</li>

  </ul></li>

</ul>




<strong>Constraints: </strong>

<ul>

 <li>Do not import/use any library modules.</li>

 <li>Your submission should have no code outside of class/function definitions (comments are fine).</li>

 <li>You are not permitted to use Python’s built-in Complex class</li>

 <li>Your methods must have exactly the same names and arguments as described above.</li>

</ul>







<strong>Example: </strong>Copy the following code into your hw10.py file, and uncomment lines as you write the relevant methods.  What each line should print is noted in the comment on the right.  You should write some additional tests of your own: this is not a very good set of tests for the number of methods this problem requires.  Make sure to comment out all tests before submitting to github.




##x = Complex(2.7,3)

##y = Complex(-4,0)

##z = Complex(0,-1.5)




<table width="0">

 <tbody>

  <tr>

   <td width="226">##print(x.real)</td>

   <td width="88"># 2.7</td>

   <td width="44"> </td>

  </tr>

  <tr>

   <td width="226">##print(x.get_real())</td>

   <td width="88"># 2.7</td>

   <td width="44"> </td>

  </tr>

  <tr>

   <td width="226">##print(y.get_imag()) ##x.set_real(6)##z.set_imag(-2.5) </td>

   <td width="88"># 0</td>

   <td width="44"> </td>

  </tr>

  <tr>

   <td width="226">##print(x.real)</td>

   <td width="88"># 6</td>

   <td width="44"> </td>

  </tr>

  <tr>

   <td width="226">##print(x)</td>

   <td width="88"># 6 + 3i</td>

   <td width="44"> </td>

  </tr>

  <tr>

   <td width="226">##print(y)</td>

   <td width="88"># -4 + 0i</td>

   <td width="44"> </td>

  </tr>

  <tr>

   <td width="226">##print(z)</td>

   <td width="88"># 0 + -2.5i</td>

   <td width="44"> </td>

  </tr>

  <tr>

   <td width="226">##print(x+y)</td>

   <td width="88"># 2 + 3i</td>

   <td width="44"> </td>

  </tr>

  <tr>

   <td width="226">##print(z+y+x)</td>

   <td colspan="2" width="120"># 2 + 0.5i</td>

  </tr>

  <tr>

   <td width="226">##print(y*z)</td>

   <td colspan="2" width="120"># 0.0 + 10.0i</td>

  </tr>

  <tr>

   <td width="226">##print(x*z)</td>

   <td colspan="2" width="120"># 7.5 + -15.0i</td>

  </tr>

  <tr>

   <td width="226">##print(x*y+x*z)</td>

   <td colspan="2" width="120"># -16.5 + -27.0i</td>

  </tr>

  <tr>

   <td width="226">##print(x*(y+z))</td>

   <td colspan="2" width="120"># -16.5 + -27.0i</td>

  </tr>

  <tr>

   <td width="226">##print(x == y)</td>

   <td colspan="2" width="120"># False</td>

  </tr>

 </tbody>

</table>

##print(x*y+x*z == x*(y+z))   # True










<h1>Problem B. (30<em> points</em>)  <strong>Employee Database</strong></h1>

You work for the HR department, in the corporate headquarters of Holistic Synergies, Ltd.  Your supervisor, Dr. Boss Manager III, has instructed you to “leverage our operational efficiency to create unique opportunities for strategic alliances, so that the full human resources portfolio, from data to incentives to programs and beyond, can be the most innovative across the industry, but in ways that also reflect our leading stewardship of resources and cost-effective sensibility.”




You have no idea what this means, so instead you’ve decided to make a program that processes information about the various branches of your company.  Your company cuts employees with alarming frequency, so you’ve also decided to automate the decision-making process for those tasks with your program (note: this is sort of automation is ethically dubious at best, please don’t do this for any real company).




Download the CSV files contained in hw10.zip on Canvas, and place them in the same folder as your hw10.py file.  Each CSV file represents one branch of the company.  Note the layout of the files: the first two rows contain information about the location of the branch and the annual upkeep cost for the building (in USD) respectively.  The third row is a set of column titles for the employees, and the remaining rows contain information about each employee.




You may notice that every employee is mentioned only by first name; it is against company policy to have a last name, as this “disincentivizes exceptional distillation of latent mnemonic energies into innovative crystallization”, according to your CEO.  For similar reasons, it is against company policy to hire more than one person with the same first name, even across different branches.




You will need three interconnected classes for this system: one for a single employee, one for a branch, and one for the entire company.  Since the information for each branch is in a file, and each line of that file (past the 3rd) is an employee, you’ll be using that information directly in your initialization of the employee and branch classes.




<h2>Employee class</h2>

The Employee class must have five instance variables:

<ul>

 <li>name is a string representing the employee’s first name (corresponding to the first column in the CSV, from row 5 onwards)</li>

 <li>position is a string representing the employee’s job title (the second column)</li>

 <li>salary is a floating point number representing the employee’s annual salary in USD (the third column). This must be stored as a float value, not a string (use the float function), and the same applies to the next two as well.</li>

 <li>seniority is a floating point number representing the number of years the employee has worked at that branch of the company (the fourth column).</li>

 <li>value is a floating point number representing an estimate of the average annual earnings that the employee generates for the company (not taking into account his salary); that is, how much the employee is worth to the company (the fifth column)</li>

</ul>

The Employee class should also have a constructor and three methods:

<ul>

 <li>The constructor must take only one parameter (other than self), a single string representing the line in the CSV file that contains the employee’s data. The constructor should parse that line using the .split string method to initialize all five instance variables mentioned above. ● Overload the __str__ method so that it returns a string in the format</li>

</ul>

“&lt;Name&gt;, &lt;Position&gt;”

(see example below)

<ul>

 <li>net_value(self) takes in no arguments (other than self), and returns the employee’s value, minus their salary.</li>

 <li>Overload the &lt; operator (__lt__) so that it takes in another Employee object, and returns True if the left operand (self) has a lower net_value than the right operand (other), or False</li>

</ul>

<strong> </strong>

<strong>Examples: </strong>Copy the following code into your hw10.py file, and uncomment lines as you write the relevant methods.  What each line should print is noted in the comment on the right.  Make sure to comment out all tests before submitting to github.  You may run into minor floating point rounding errors – ignore them.

<strong> </strong>

##emp1 = Employee(‘Milton,Underling,310423.01,5.0,22.99
’)

##emp2 = Employee(‘Bill,Boss,403567.34,5.0,519.35
’)




##print(emp1.name)            # Milton

##print(emp1.position)        # Underling

##print(emp1.salary)          # 310423.01

##print(emp1.seniority)       # 5.0

##print(emp1.value)           # 22.99

##print(emp1)                 # Milton, Underling

##print(emp1.net_value())     # -310400.02

##print(emp2.net_value())     # -403047.99

##print(emp1 &lt; emp2)          # False

##print(emp2 &lt; emp1)          # True










<h2>Branch class</h2>

The Branch class must have three instance variables:

<ul>

 <li>location is a string, representing the city in which the branch is located</li>

 <li>upkeep is a float, representing the annual upkeep cost of the building</li>

 <li>team is a list of Employee objects, representing every employee working at the branch.</li>

</ul>

The Branch class should also have a constructor and four methods:

<ul>

 <li>The constructor must take only one parameter (other than self), a string representing the filename for the CSV where the branch information is stored. The constructor should then open that file, read in each line, and use that information to initialize all of the instance variables for the Branch.</li>

 <li>Overload the __str__ method so that it returns a string containing the location of the branch, followed by the string representation of each employee (order does not matter), separated by newlines (see example below).  You must call the str() function on each Employee object to do this.</li>

 <li>profit(self) takes in no arguments (other than self), and returns the sum of the net values of all of the employees in the branch, minus the upkeep of the branch.</li>

 <li>Overload the &lt; operator (__lt__) so that it takes in another Branch object, and returns True if the left operand (self) has a lower profit than the right operand (other), or False</li>

 <li>cut(self, num) takes in one argument: num is an integer representing the number of employees that must be cut from the branch. cut sorts the employees by their net value, and removes the lowest num Employees from the team list  (see Hint below for how to do this quickly).</li>

</ul>




<strong>Hint: </strong>

<ul>

 <li>There are two built-in ways of quickly sorting lists: the sorted() function, and the .sort() list method; see <u><a href="https://docs.python.org/3/howto/sorting.html">https://docs.python.org/3/howto/sorting.html</a></u><a href="https://docs.python.org/3/howto/sorting.html">.</a> The difference is that .sort() is in-place: it doesn’t return anything but will change the list to be in sorted order, while sorted() does not change the original list: sorted() creates a copy, sorts the copy, and returns it.  By default, .sort() and sorted() sort objects based on their overloaded &lt; operator (__lt__), so because we changed the behavior of &lt; to order Employees based on their net value, you should be able to use .sort() or sorted() on a list of Employees without specifying a key function.</li>

</ul>




<strong>Examples</strong> (assumes that you are running hw10.py from the same folder as all of the CSV files in hw10.zip, which can be found on Canvas)<strong>: </strong>Copy the following code into your hw10.py file, and uncomment lines as you write the relevant methods.  What each line should print is noted in the comment on the right, or to the right and below when printing entire branches (don’t uncomment the lines starting with #### since those are supposed to remain comments).  Make sure to comment out all tests before submitting to github.  You may run into minor floating point rounding errors – ignore them.  Remember, the order in which the employees are listed does not matter when printing out a Branch object.




##branch2 = Branch(‘branch2.csv’)

##print(branch2.location)         #Pawnee

##print(branch2.upkeep)           #98229.98

##print()

##

##print(branch2)

####                Pawnee

####                Ron, Efficiency Logistics Strategist

####                Leslie, Creative Evolution Strategist

####                Ann, Data Evolution Engineer

####                Mark, Operational Services Specialist ####                Tom, Creative Logistics Coordinator

####                April, Enterprise Services Consultant ####                Andy, Creative Logistics Specialist

####                Jerry, Enterprise Services Technician

####                Donna, Operational Innovation Engineer

##

##print()

##branch2.cut(7)

##print(branch2)

####                Pawnee

####                Leslie, Creative Evolution Strategist

####                Ann, Data Evolution Engineer

##

##print()

##print(branch2.profit())         #12577.81

##branch1 = Branch(‘branch1.csv’)

##print(branch1.upkeep)           #57867.07

##

##print()

##print(branch1)

####                Scranton

####                Dwight, Efficiency Evolution Specialist

####                Jim, Data Innovation Specialist

####                Pam, Operational Analytics Technician

####                Ryan, Data Evolution Consultant

####                Stanley, Efficiency Logistics Technician

####                Michael, Enterprise Communications Technician

####                Kevin, Operational Services Technician

####                Meredith, Data Evolution Technician

####                Angela, Enterprise Communications Consultant

####                Oscar, Creative Innovation Coordinator

####                Phyllis, Enterprise Analytics Technician

##branch1.cut(8)

##

##print()

##print(branch1)

####                Scranton

####                Pam, Operational Analytics Technician

####                Michael, Enterprise Communications Technician

####                Stanley, Efficiency Logistics Technician



















<h2>Company class</h2>

The Company class must have two instance variables:

<ul>

 <li>name is a string, representing the name of the company</li>

 <li>branches is a list of Branch objects, representing all of the branches associated with the company</li>

</ul>

The Company class should also have a constructor and two methods:

<ul>

 <li>The constructor must take two parameters (other than self): a string representing the name of the company, and a list of Branch objects, representing the branches of the company: it should use this information to initialize the two instance variables.</li>

 <li>Overload the __str__ method so that it returns the company name, followed by the string representation of each branch (in no particular order), separated by two newlines (so one empty line between each branch). See the example below for details.</li>

 <li>synergize(self) takes in no arguments (other than self), and implements the company’s ultimate HR strategy: find the branch with the lowest profit margin and cut half (rounded down) of the employees from that branch.</li>

</ul>




<strong>Constraints</strong>:

<ul>

 <li>Do not import/use any Python modules.</li>

 <li>Don’t use the input() function, as this will break our grading scripts.</li>

 <li>You may use any string or list method that is appropriate to solving this problem.</li>

 <li>Your submission should have no code outside of the function definitions (comments are fine).</li>

</ul>




<strong>Examples: </strong>Copy the following code into your hw10.py file, and uncomment lines as you write the relevant methods.  What each line should print is noted in the comment on the right, or to the right and below when printing entire branches (don’t uncomment the lines starting with #### since those are supposed to remain comments).  Make sure to comment out all tests before submitting to github.  You may run into minor floating point rounding errors – ignore them.  Remember, the order in which the branches are listed does not matter when printing out a Company object.




##b1 = Branch(‘branch1.csv’)

##b2 = Branch(‘branch2.csv’)

##b3 = Branch(‘branch3.csv’)

##b4 = Branch(‘branch4.csv’)

##hs = Company(‘Synergistic Management Solutions’,[b1,b2,b3,b4])

##print(hs.name)           #Synergistic Management Solutions




##print()

##print(hs)

####                    Synergistic Management Solutions

####

####                    Scranton

####                    Dwight, Efficiency Evolution Specialist

####                    Jim, Data Innovation Specialist

####                    Pam, Operational Analytics Technician

####                    Ryan, Data Evolution Consultant

####                    Stanley, Efficiency Logistics Technician

####                    Michael, Enterprise Communications Technician ####                    Kevin, Operational Services Technician

####                    Meredith, Data Evolution Technician

####                    Angela, Enterprise Communications Consultant

####                    Oscar, Creative Innovation Coordinator

####                    Phyllis, Enterprise Analytics Technician

####

####                    Pawnee

####                    Ron, Efficiency Logistics Strategist

####                    Leslie, Creative Evolution Strategist

####                    Ann, Data Evolution Engineer

####                    Mark, Operational Services Specialist

####                    Tom, Creative Logistics Coordinator

####                    April, Enterprise Services Consultant ####                    Andy, Creative Logistics Specialist

####                    Jerry, Enterprise Services Technician

####                    Donna, Operational Innovation Engineer

####

####                    Greendale

####                    Britta, Enterprise Services Coordinator ####                    Abed, Operational Services Strategist

####                    Troy, Efficiency Innovation Coordinator

####                    Annie, Efficiency Innovation Consultant

####                    Shirley, Enterprise Innovation Engineer

####                    Pierce, Enterprise Evolution Specialist

####                    Ben, Enterprise Communications Consultant ####                    Jeff, Brand Logistics Specialist

####                    Craig, Enterprise Communications Engineer

####

####                    Ambiguous

####                    J.D., Efficiency Analytics Coordinator

####                    Turk, Efficiency Innovation Technician ####                    Elliot, Data Innovation Specialist

####                    Perry, Efficiency Evolution Technician

####                    Bob, Enterprise Logistics Engineer

####                    Carla, Brand Services Technician

####                    Janitor, Efficiency Evolution Coordinator




##print()

##hs.synergize()

##print()




##print(hs)

####                    Synergistic Management Solutions

####

####                    Greendale

####                    Ben, Enterprise Communications Consultant

####                    Craig, Enterprise Communications Engineer

####                    Britta, Enterprise Services Coordinator

####                    Pierce, Enterprise Evolution Specialist

####                    Jeff, Brand Logistics Specialist

####

####                    Pawnee

####                    Ron, Efficiency Logistics Strategist

####                    Leslie, Creative Evolution Strategist

####                    Ann, Data Evolution Engineer

####                    Mark, Operational Services Specialist

####                    Tom, Creative Logistics Coordinator

####                    April, Enterprise Services Consultant ####                    Andy, Creative Logistics Specialist

####                    Jerry, Enterprise Services Technician

####                    Donna, Operational Innovation Engineer

####

####                    Scranton

####                    Dwight, Efficiency Evolution Specialist

####                    Jim, Data Innovation Specialist

####                    Pam, Operational Analytics Technician

####                    Ryan, Data Evolution Consultant

####                    Stanley, Efficiency Logistics Technician

####                    Michael, Enterprise Communications Technician

####                    Kevin, Operational Services Technician

####                    Meredith, Data Evolution Technician

####                    Angela, Enterprise Communications Consultant

####                    Oscar, Creative Innovation Coordinator

####                    Phyllis, Enterprise Analytics Technician

####

####                    Ambiguous

####                    J.D., Efficiency Analytics Coordinator

####                    Turk, Efficiency Innovation Technician

####                    Elliot, Data Innovation Specialist

####                    Perry, Efficiency Evolution Technician

####                    Bob, Enterprise Logistics Engineer

####                    Carla, Brand Services Technician

####                    Janitor, Efficiency Evolution Coordinator




##print()

##hs.synergize()

##print()




##print(hs)

####                    Synergistic Management Solutions

####

####                    Pawnee

####                    Jerry, Enterprise Services Technician

####                    Ron, Efficiency Logistics Strategist

####                    Andy, Creative Logistics Specialist

####                    Leslie, Creative Evolution Strategist

####                    Ann, Data Evolution Engineer

####

####                    Scranton

####                    Dwight, Efficiency Evolution Specialist

####                    Jim, Data Innovation Specialist

####                    Pam, Operational Analytics Technician

####                    Ryan, Data Evolution Consultant

####                    Stanley, Efficiency Logistics Technician

####                    Michael, Enterprise Communications Technician

####                    Kevin, Operational Services Technician

####                    Meredith, Data Evolution Technician

####                    Angela, Enterprise Communications Consultant

####                    Oscar, Creative Innovation Coordinator

####                    Phyllis, Enterprise Analytics Technician

####

####                    Ambiguous

####                    J.D., Efficiency Analytics Coordinator

####                    Turk, Efficiency Innovation Technician ####                    Elliot, Data Innovation Specialist

####                    Perry, Efficiency Evolution Technician

####                    Bob, Enterprise Logistics Engineer

####                    Carla, Brand Services Technician

####                    Janitor, Efficiency Evolution Coordinator

####

####                    Greendale

####                    Ben, Enterprise Communications Consultant

####                    Craig, Enterprise Communications Engineer

####                    Britta, Enterprise Services Coordinator

####                    Pierce, Enterprise Evolution Specialist

####                    Jeff, Brand Logistics Specialist




##print()

##hs.synergize()

##print()




##print(hs)

####                    Scranton

####                    Meredith, Data Evolution Technician

####                    Kevin, Operational Services Technician

####                    Phyllis, Enterprise Analytics Technician

####                    Pam, Operational Analytics Technician

####                    Michael, Enterprise Communications Technician

####                    Stanley, Efficiency Logistics Technician

####

####                    Ambiguous

####                    J.D., Efficiency Analytics Coordinator

####                    Turk, Efficiency Innovation Technician ####                    Elliot, Data Innovation Specialist

####                    Perry, Efficiency Evolution Technician

####                    Bob, Enterprise Logistics Engineer

####                    Carla, Brand Services Technician

####                    Janitor, Efficiency Evolution Coordinator

####

####                    Greendale

####                    Ben, Enterprise Communications Consultant

####                    Craig, Enterprise Communications Engineer

####                    Britta, Enterprise Services Coordinator

####                    Pierce, Enterprise Evolution Specialist

####                    Jeff, Brand Logistics Specialist

####

####                    Pawnee

####                    Jerry, Enterprise Services Technician

####                    Ron, Efficiency Logistics Strategist

####                    Andy, Creative Logistics Specialist

####                    Leslie, Creative Evolution Strategist

####                    Ann, Data Evolution Engineer











