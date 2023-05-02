Download Link: https://assignmentchef.com/product/solved-comp1210-project-7-icosahedron-list2-menu-app
<br>
<u>The objective is to modify your Project 6 to use arrays instead of ArrayList objects</u>.  You will write a program this week that is composed of three classes: the first class defines Icosahedron objects, the second class defines IcosahedronList2 objects, and the third, IcosahedronList2MenuApp, presents a menu to the user with eight options and implements these: (1) read input file (which creates an IcosahedronList2 object), (2) print report, (3) print summary, (4) add an Icosahedron object to the IcosahedronList2 object, (5) delete an Icosahedron object from the IcosahedronList2 object, (6) find an Icosahedron object in the IcosahedronList2 object, (7) Edit an Icosahedron in the IcosahedronList2 object, and (8) quit the program.<strong> [You should create a new “Project 7” folder and copy your Project 6 files </strong>(Icosahedron.java, IcosahedronList.java, IcosahedronListMenuApp.java,

icosahedron_data_1.txt, and icosahedron_data_0.txt)<strong> to it, rather than work in the same folder as Project 6 files.]  </strong>

<strong> </strong>

<strong><u>To rename an existing .java file, </u>open the file in jGRASP, change the name of the class <u>and</u> the name of the constructor (if it has one) in the source file, and then click the Save button.  In the dialog that pops up, click the “Rename and Save” button.  This will rename save the .java file and delete the old associated .class file. </strong>




<ul>

 <li><strong>Icosahedron.java (<u>assuming that you successfully created this class in Project 4, 5, or 6 just</u> <u>copy the file to your new Project 7 folder and go on to IcosahedronList2.java on page 4.</u> <u>Otherwise, you will need to create Icosahedron.java as part of this project</u>.) </strong></li>

</ul>

<strong> </strong>

<strong>Requirements</strong>: Create an Icosahedron class that stores the label, color, and edge (i.e., length of an edge, <u>which must be greater than zero</u>).  The Icosahedron class also includes methods to set and get each of these fields, as well as methods to calculate the surface area, volume, and surface

to volume ratio of an Icosahedron object, and a method to provide a String value of an Icosahedron object (i.e., a class instance).




<table width="586">

 <tbody>

  <tr>

   <td colspan="3" width="586">An <strong>Icosahedron</strong> has 20 equilateral triangle faces, 12 vertices, and 30 edges as depicted below. The formulas are provided to assist you in computing return values for the respective methods in the Icosahedron class described in this project.</td>

  </tr>

  <tr>

   <td width="191"> </td>

   <td width="191"> Surface Area (A) Volume (V) Edge length (a) Surface/Volume ratio (A/V)</td>

   <td width="204">  </td>

  </tr>

  <tr>

   <td colspan="3" width="586"> </td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong>Design</strong>:  The Icosahedron class has fields, a constructor, and methods as outlined below.




<ul>

 <li><strong>Fields</strong> (instance variables): label of type String, color of type String, and edge of type double. Initialize the Strings to “” and the double to 0 in their respective declarations. These instance variables should be private so that they are not directly accessible from outside of the Icosahedron class, and <u>these should be the only instance variables in the class</u>.</li>

</ul>




<ul>

 <li><strong>Constructor</strong>: Your Icosahedron class must contain a public constructor that accepts three parameters (see types of above) representing the label, color, and edge. Instead of assigning the parameters directly to the fields, the respective set method for each field (described below) should be called. For example, instead of the statement label = labelIn; use the statement setLabel(labelIn); Below are examples of how the constructor could be used to create Icosahedron objects.  Note that although String and numeric literals are used for the actual parameters (or arguments) in these examples, variables of the required type could have been used instead of the literals.</li>

</ul>




Icosahedron example1 = new Icosahedron(“Small”, “blue”, 0.01);




Icosahedron example2 = new Icosahedron(”    Medium    “, “orange”, 12.3);




Icosahedron example3 = new Icosahedron(“Large”, ”  white  “, 123.4);




<ul>

 <li><strong>Methods</strong>: Usually a class provides methods to access and modify each of its instance variables (known as get and set methods) along with any other required methods. The methods for Icosahedron, which should each be public, are described below.  See formulas in Code and Test below. o getLabel:  Accepts no parameters and returns a String representing the label field.</li>

 <li>setLabel: Takes a String parameter and returns a boolean. If the string parameter is not null, then the “trimmed” String is set to the label field and the method returns true. Otherwise, the method returns false and the label is not set.</li>

 <li>getColor: Accepts no parameters and returns a String representing the color field.</li>

 <li>setColor: Takes a String parameter and returns a boolean. If the string parameter is not null, then the “trimmed” String is set to the color field and the method returns true. Otherwise, the method returns false and the label is not set.</li>

 <li>getEdge: Accepts no parameters and returns a double representing the edge field.</li>

 <li>setEdge: Accepts a double parameter and returns a boolean as follows. If the edge is greater than zero, sets the edge field to the double passed in and returns true.  Otherwise, the method returns false and the edge is not set.</li>

 <li>surfaceArea: Accepts no parameters and returns the double value for the total surface area calculated using the value for edge.</li>

 <li>volume: Accepts no parameters and returns the double value for the volume calculated using the value for edge.</li>

 <li>surfaceToVolumeRatio: Accepts no parameters and returns the double value calculated by dividing the total surface area by the volume.</li>

 <li>toString: Returns a String containing the information about the Icosahedron object formatted as shown below, including decimal formatting (“#,##0.0#####”) for the double values.  Newline and tab escape sequences should be used to achieve the proper layout.  In addition to the field values (or corresponding “get” methods), the following methods should be used to compute appropriate values in the toString method:</li>

</ul>

surfaceArea(), volume(), and surfaceToVolumeRatio().  Each line should have no trailing spaces (e.g., there should be no spaces before a newline (
) character).  The toString value for example1, example2, and example3 respectively are shown below (the blank lines are not part of the toString values).

Icosahedron “Small” is “blue” with 30 edges of length 0.01 units.    surface area = 0.000866 square units    volume = 0.000002 cubic units    surface/volume ratio = 396.950723




Icosahedron “Medium” is “orange” with 30 edges of length 12.3 units.

surface area = 1,310.209833 square units    volume = 4,059.844212 cubic units    surface/volume ratio = 0.322724




Icosahedron “Large” is “white” with 30 edges of length 123.4 units.    surface area = 131,874.537977 square units    volume = 4,099,581.395236 cubic units    surface/volume ratio = 0.032168

<strong>Code and Test</strong>: As you implement your Icosahedron class, you should compile it and then test it using interactions.  For example, as soon you have implemented and successfully compiled the constructor, you should create instances of Icosahedron in interactions (e.g., copy/paste the examples above).  Remember that when you have an instance on the workbench, you can unfold it to see its values.  You can also open a viewer canvas window and drag the instance from the Workbench tab to the canvas window.  After you have implemented and compiled one or more methods, create an Icosahedron object in interactions and invoke each of your methods on the object to make sure the methods are working as intended.  You may find it useful to create a separate class with a main method that creates an instance of Icosahedron then prints it out.




<ul>

 <li><strong>java – You must use arrays instead of ArrayList objects. (<u>Assuming that</u> <u>you successfully created this class in Project 6, just copy IcosahedronList.java to your new</u> <u>Project 7 folder and then open in jGRASP and rename as IcosahedronList2.  To rename an</u> <u>existing .java file, open the file in jGRASP, change the name of the class and the name of the</u> <u>constructor in the source code, and then click the Save button.  In the dialog that pops up,</u> <u>click the “Rename and Save” button.  This will rename and save the .java file and then</u> <u>delete old associated .class file.  Otherwise, you will need to create all of</u> </strong></li>

</ul>

<strong><u>IcosahedronList2.java as part of this project</u>.)  In the requirements below, <u>IcosahedronList</u> <u>has been changed to IcosahedronList2. Be sure to make these changes in your methods as</u> <u>necessary.</u></strong>




<strong>Requirements</strong>: Create an IcosahedronList2 class that stores the name of the list and an array of Icosahedron objects, and the number of Icosahedron objects in the array.  It also includes methods that return the name of the list, number of Icosahedron objects in the IcosahedronList2, total surface area, total volume, average surface area, average volume, and average surface to volume ratio for all Icosahedron objects in the IcosahedronList2.  The toString method returns a String containing the name of the list followed by each Icosahedron in the array, and a summaryInfo method returns summary information about the list (see below).




<strong>Design</strong>:  The IcosahedronList2 class has <u>three fields</u>, a constructor, and methods as outlined below.




<ul>

 <li><strong>Fields</strong> (or instance variables): (1) a String representing the name of the list, (2) an array of Icosahedron objects, and (3) an int representing the number of Icosahedron objects in the Icosahedron array. These are the only fields (or instance variables) that this class should have.</li>

 <li><strong>Constructor</strong>: Your IcosahedronList2 class must contain a constructor that accepts a parameter of type String representing the name of the list, a parameter of type</li>

</ul>

Icosahedron[], representing the list of Icosahedron objects, and a parameter of type int representing the number of Icosahedron objects in the Icosahedron array.  These parameters should be used to assign the fields described above (i.e., the instance variables).

<strong> </strong>

<ul>

 <li><strong>Methods</strong>: The methods for IcosahedronList2 are described below.</li>

 <li>getName: Returns a String representing the name of the list.</li>

 <li>numberOfIcosahedrons: Returns an int representing the number of Icosahedron objects in the IcosahedronList2.  If there are zero Icosahedron objects in the list, zero should be returned. <strong> </strong></li>

 <li>totalSurfaceArea: Returns a double representing the total surface areas for all Icosahedron objects in the list.  If there are zero Icosahedron objects in the list, zero should be returned. <strong> </strong></li>

 <li>totalVolume: Returns a double representing the total volumes for all Icosahedron objects in the list.  If there are zero Icosahedron objects in the list, zero should be returned. <strong> </strong></li>

 <li>averageSurfaceArea: Returns a double representing the average surface area for all Icosahedron objects in the list.  If there are zero Icosahedron objects in the list, zero should be returned. <strong> </strong></li>

 <li>averageVolume: Returns a double representing the average volume for all Icosahedron objects in the list.  If there are zero Icosahedron objects in the list, zero should be returned. <strong> </strong></li>

 <li>averageSurfaceToVolumeRatio: Returns a double representing the average surface to volume ratio for all Icosahedron objects in the list.  If there are zero Icosahedron objects in the list, zero should be returned. <strong> </strong></li>

 <li>toString: Returns a String (does <u>not</u> begin with 
) containing the name of the list followed by each Icosahedron in the list.  In the process of creating the return result, this toString() method should include a while loop that calls the toString() method for each Icosahedron object in the list (adding a 
 before and after each).  Be sure to include appropriate newline escape sequences.  For an example, see <u>lines 2 through 19</u> in the output below from IcosahedronList2App for the <em>txt</em> input file. [<u>Note</u> <u>that the toString result should <strong>not</strong> include the return value of summaryInfo()</u>.]</li>

 <li>summaryInfo: Returns a String (does<u> not </u>begin with 
) containing the name of the list (which can change depending of the value read from the file) followed by various summary items:  number of Icosahedrons, total surface area, total volume, average surface area, average volume, and average surface to volume ratio.  Use “#,##0.0##” as the pattern to format the double values.</li>

 <li>getList: Returns the array of Icosahedron objects (the second field above).</li>

 <li>readFile: Takes a String parameter representing the file name, reads in the file, storing the list name and creating an array of Icosahedron objects, uses the list name, the array, and number of Icosahedron objects in the array to create an IcosahedronList2 object, and then returns the IcosahedronList2 object.  See note #1 under <u>Important</u> <u>Considerations</u> for the IcosahedronList2MenuApp class (last page) to see how this method should be called. <strong> </strong></li>

 <li>addIcosahedron: Returns nothing but takes three parameters (label, color, and edge), creates a new Icosahedron object, and adds it to the IcosahedronList2 object.</li>

 <li>findIcosahedron: Takes a label of an Icosahedron as the String parameter and returns the corresponding Icosahedron object if found in the IcosahedronList2 object; otherwise returns null.  <u>Case should be ignored when attempting to match the label</u>.</li>

 <li>deleteIcosahedron: Takes a String as a parameter that represents the label of the Icosahedron and returns the Icosahedron if it is found in the IcosahedronList2 object and deleted; otherwise returns null.  <u>Case should be ignored when attempting to match the</u> <u>label; consider calling/using </u><u>findIcosahedron in this method</u>.  When an element is deleted from an array, elements to the right of the deleted element must be shifted to the left. After shifting the items to the left, the last Icosahedron element in the array should be set to null.  Finally, the number of elements field must be decremented.</li>

 <li>editIcosahedron: Takes three parameters (label, color, and edge), uses the label to find the corresponding the Icosahedron object in the list.  If found, sets the color and edge to the values passed in as parameters, and returns true.  If not found, returns false.</li>

</ul>

<strong> </strong>

<strong>Code and Test</strong>: Remember to import java.util.Scanner, java.io.File,

java.io.FileNotFoundException.  These classes will be needed in the readFile method which will require a throws clause for FileNotFoundException.  Some of the methods above require that you use a loop to go through the objects in the array.  You may want to implement the class below in parallel with this one to facilitate testing.  That is, after implementing one to the methods above, you can implement the corresponding “case” in the switch for menu described below in the IcosahedronList2MenuApp class.




<ul>

 <li><strong>java </strong>(replaces IcosahedronListMenuApp class from Project 6; <u>the</u> <u>file and class name in the file must be renamed to reflect IcosahedronList2MenuApp</u>).  <strong>To rename an existing .java file, open the file in jGRASP, change the name of the class in the source code, and then click the Save button.  In the dialog that pops up, click the “Rename and Save” button.  This will rename the .java file and delete the old associated .class file.  <u>Be</u> <u>sure to make these changes in your main method as necessary.</u></strong></li>

</ul>




<strong>Requirements</strong>: Create an IcosahedronList2MenuApp class with a main method that presents the user with a menu with eight options, each of which is implemented to do the following: (1) read the input file and create an IcosahedronList2 object, (2) print the IcosahedronList2 object, (3) print the summary for the IcosahedronList2 object, (4) add an Icosahedron object to the IcosahedronList2 object, (5) delete an Icosahedron object from the IcosahedronList2 object, (6) find an Icosahedron object in the IcosahedronList2 object, (7) Edit an Icosahedron object in the IcosahedronList2 object, and (8) quit the program.




<strong>Design</strong>:  The main method should print a list of options with the action code and a short description followed by a line with just the action codes prompting the user to select an action.  After the user enters an action code, the action is performed, including output if any.  Then the line with just the action codes prompting the user to select an action is printed again to accept the next code.  The first action a user would normally perform is ‘R’ to read in the file and create an IcosahedronList2 object.  However, the other action codes should work even if an input file has not been processed. The user may continue to perform actions until ‘Q’ is entered to quit (or end) the program.  Note that your program should accept both uppercase and lowercase action codes.       Below is output produced after printing the action codes with short descriptions followed by the prompt with the action codes waiting for the user to make a selection.




<table width="566">

 <tbody>

  <tr>

   <td width="55">Line #</td>

   <td width="511">Program output</td>

  </tr>

  <tr>

   <td width="55">12345678910</td>

   <td width="511">Icosahedron List System MenuR – Read File and Create Icosahedron ListP – Print Icosahedron ListS – Print SummaryA – Add IcosahedronD – Delete IcosahedronF – Find IcosahedronE – Edit IcosahedronQ – QuitEnter Code [R, P, S, A, D, F, E, or Q]:</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

Below shows the screen after the user entered ‘r’ and then (when prompted) the file name.  Notice the output from this action was “File read in and Icosahedron List created”.  This is followed by the prompt with the action codes waiting for the user to make the next selection.  You should use the <em>icosahedron_data_1.txt </em>file from Project 5 to test your program.




<table width="566">

 <tbody>

  <tr>

   <td width="55">Line #</td>

   <td width="511">Program output</td>

  </tr>

  <tr>

   <td width="55">12345</td>

   <td width="511">Enter Code [R, P, S, A, D, F, E, or Q]: rFile name: icosahedron_data_1.txtFile read in and Icosahedron List created Enter Code [R, P, S, A, D, F, E, or Q]:</td>

  </tr>

 </tbody>

</table>




The result of the user selecting ‘p’ to Print Icosahedron List is shown below and next page.




<table width="625">

 <tbody>

  <tr>

   <td width="54">Line #</td>

   <td width="571">Program output</td>

  </tr>

  <tr>

   <td width="54">12345678910111213141516171819 </td>

   <td width="571">Enter Code [R, P, S, A, D, F, E, or Q]: pIcosahedron Test List Icosahedron “Small” is “blue” with 30 edges of length 0.01 units.    surface area = 0.000866 square units    volume = 0.000002 cubic units    surface/volume ratio = 396.950723 Icosahedron “Medium” is “orange” with 30 edges of length 12.3 units.surface area = 1,310.209833 square units    volume = 4,059.844212 cubic units    surface/volume ratio = 0.322724 Icosahedron “Large” is “white” with 30 edges of length 123.4 units.    surface area = 131,874.537977 square units    volume = 4,099,581.395236 cubic units    surface/volume ratio = 0.032168 Enter Code [R, P, S, A, D, F, E, or Q]: <em> </em></td>

  </tr>

 </tbody>

</table>




The result of the user selecting ‘s’ to print the summary for the list is shown below.




<table width="566">

 <tbody>

  <tr>

   <td width="55">Line #</td>

   <td width="511">Program output</td>

  </tr>

  <tr>

   <td width="55">1234567891011 </td>

   <td width="511">Enter Code [R, P, S, A, D, F, E, or Q]: s —– Summary for Icosahedron Test List —–Number of Icosahedrons: 3Total Surface Area: 133,184.749 Total Volume: 4,103,641.239Average Surface Area: 44,394.916Average Volume: 1,367,880.413Average Surface/Volume Ratio: 132.435 Enter Code [R, P, S, A, D, F, E, or Q]: <em> </em></td>

  </tr>

 </tbody>

</table>







The result of the user selecting ‘a’ to add an icosahedron object is shown below.  Note that after ‘a’ was entered, the user was prompted for label, color, and edge.  Then after the Icosahedron object is added to the Icosahedron List, the message “*** Icosahedron added ***” was printed.  This is followed by the prompt for the next action. After you do an “add”, you should do a “print” or a “find” to confirm that the “add” was successful.




<table width="566">

 <tbody>

  <tr>

   <td width="55">Line #</td>

   <td width="511">Program output</td>

  </tr>

  <tr>

   <td width="55">1234567 </td>

   <td width="511">Enter Code [R, P, S, A, D, F, E, or Q]: aLabel: NewIcosahedronColor: navy blueEdge: 12.5*** Icosahedron added *** Enter Code [R, P, S, A, D, F, E, or Q]: <em> </em></td>

  </tr>

 </tbody>

</table>




Here is an example of the successful “delete” for an icosahedron object, followed by an attempt that was not successful (i.e., the Icosahedron object was not found).  Do “p” to confirm the “d”.




<table width="566">

 <tbody>

  <tr>

   <td width="55">Line #</td>

   <td width="511">Program output</td>

  </tr>

  <tr>

   <td width="55">123456789 </td>

   <td width="511">Enter Code [R, P, S, A, D, F, E, or Q]: dLabel: small“Small” deleted Enter Code [R, P, S, A, D, F, E, or Q]: dLabel: giant“giant” not found Enter Code [R, P, S, A, D, F, E, or Q]:</td>

  </tr>

 </tbody>

</table>




Here is an example of the successful “find” for an icosahedron object, followed by an attempt that was <u>not</u> successful (i.e., the Icosahedron object was not found).




<table width="625">

 <tbody>

  <tr>

   <td width="54">Line #</td>

   <td width="571">Program output</td>

  </tr>

  <tr>

   <td width="54">123456789101112 </td>

   <td width="571">Enter Code [R, P, S, A, D, F, E, or Q]: fLabel: mediumIcosahedron “Medium” is “orange” with 30 edges of length 12.3 units.    surface area = 1,310.209833 square units    volume = 4,059.844212 cubic units    surface/volume ratio = 0.322724Enter Code [R, P, S, A, D, F, E, or Q]: fLabel: really big“really big” not found Enter Code [R, P, S, A, D, F, E, or Q]:</td>

  </tr>

 </tbody>

</table>

<strong> </strong>







Here is an example of the successful “edit” for an icosahedron object, followed by an attempt that was <u>not</u> successful (i.e., the Icosahedron object was not found).  In order to verify the edit, you should do a “find” for “medium” or you could do a “print” to print the whole list.




<table width="625">

 <tbody>

  <tr>

   <td width="54">Line #</td>

   <td width="571">Program output</td>

  </tr>

  <tr>

   <td width="54">12345678910111213 </td>

   <td width="571">Enter Code [R, P, S, A, D, F, E, or Q]: eLabel: mediumColor: bright orangeEdge: 25“medium” successfully edited Enter Code [R, P, S, A, D, F, E, or Q]: eLabel: fake oneColor: redEdge: 0.1“fake one” not found Enter Code [R, P, S, A, D, F, E, or Q]: <em> </em></td>

  </tr>

 </tbody>

</table>




Finally, below is an example of entering an invalid code, followed by an example of entering a ‘q’ to quit the application with no message.




<table width="625">

 <tbody>

  <tr>

   <td width="54">Line #</td>

   <td width="571">Program output</td>

  </tr>

  <tr>

   <td width="54">12345</td>

   <td width="571">Enter Code [R, P, S, A, D, F, E, or Q]: g*** invalid code *** Enter Code [R, P, S, A, D, F, E, or Q]: q —-jGRASP: operation complete. </td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong>Code and Test</strong>:

<u>Important considerations</u>:  This class should import java.util.Scanner and java.io.FileNotFoundException.  Carefully consider the following information as you develop this class.




<ol>

 <li>At the beginning of your main method, you should declare and create an array of Icosahedron objects and then declare and create an IcosahedronList2 object using the list name, the array, and 0 as the parameters in the constructor. This will be an IcosahedronList2 object that contains no Icosahedron objects. For example:</li>

</ol>

String _______ = <strong>“</strong>*** no list name assigned ***”;

Icosahedron[] _________ = new Icosahedron[100];

IcosahedronList2 _________ = new IcosahedronList2(_________,_________,_________);




The ‘R’ option in the menu should invoke the readFile method on your IcosahedronList2 object.  This will return a new IcosahedronList2 object based on the data read from the file, and this new IcosahedronList2 object should replace (be assigned to) your original

IcosahedronList2 object variable in main.  Since the readFile method throws




<h1>         Page</h1>

FileNotFoundException, your main method needs to do this as well.




<ol start="2">

 <li><strong><u>Very Important</u></strong>: <strong><u>You should declare only one Scanner on System.in for your entire</u> <u>program, and this should be done in the main method</u>. </strong>That is, all input from the keyboard (System.in) must be done in your <em>main</em>   Declaring more than one Scanner on System.in in your program will likely result in a very low score from Web-CAT.</li>

</ol>




<ol start="3">

 <li>For the menu, your switch statement expression should evaluate to a char and each case should be a char; alternatively, your switch statement expression should evaluate to a String with a length of 1 and each case should be a String with a length of 1.</li>

</ol>




After printing the menu of actions with descriptions, you should have a <em>do-while</em> loop that prints the prompt with just the action codes followed by a switch statement that performs the indicated action.  The <em>do-while</em> loop ends when the user enters ‘q’ to quit.  You should strongly consider using a <em>for-each</em> loop as appropriate in the new methods that require you to search the list.  You should be able to test your program by exercising each of the action codes.  After you implement the “Print Icosahedron List” option, you should be able to print the IcosahedronList2 object after operations such as ‘A’ and ‘D’ to see if they worked.  You may also want to run in debug mode with a breakpoint set at the switch statement so that you can step-into your methods if something is not working.  In conjunction with running the debugger, you should also create a canvas drag the items of interest (e.g., the Scanner on the file, your IcosahedronList2 object, etc.) onto the canvas and save it.  As you play or step through your program, you’ll be able to see the state of these objects change when the ‘R’, ‘A’, and ‘D’ options are selected.




<ol>

 <li>For option P, when you print the IcosahedronList2 object (e.g., myList) be sure to append a leading “
” in println:</li>

</ol>




System.out.println(<strong>“
”</strong> + myList);




<ol>

 <li>For option S, when you print the summary for IcosahedronList2 object (e.g., cList) be sure to append a leading and trailing “
” in the .println:</li>

</ol>




System.out.println(<strong>“
”</strong> + myList.summaryInfo() + <strong>“
”</strong>);




Although your program may not use all of the methods in your Icosahedron and IcosahedronList2 classes, you should ensure that all of your methods work according to the specification.  You can run your program in the canvas and then after the file has been read in, you can call methods on the IcosahedronList2 object in interactions or you can write another class and main method to exercise the methods