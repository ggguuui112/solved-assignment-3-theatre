Download Link: https://assignmentchef.com/product/solved-assignment-3-theatre
<br>
This is the most complex application that you have seen so far. It is comprised of six user defined types: four classes and two enums. This assignment attempts to simulate a simple version of a Theater application. In this application the user is able to search for a movie based on genre, name of actor, the time of the day and the day of the week.

You should define your types in the following order: the two enums, Time, Movie, Show and then Theater You will perform some simple queries on this collection.




<h2>The MovieDay Enum</h2>

This type represents the days of the week and is comprised of seven constants. The constants are the first three letters of the day of the week.




<h2>The MovieGenre Enum</h2>

This type represents the various categories of movie. Because a movie may fall under multiple categories, you will have to use the [Flags] to decorate this enum.

The bit-wise operator is used to combine more than one genre. E.g.<strong> MovieGenre</strong> genre = <strong>MovieGenre</strong>.Action | <strong>MovieGenre</strong>.Romance | <strong>MovieGenre</strong>.Comedy;

For this to work correctly, you will have to assign appropriate values for each name. Appropriate values are 0, 1, 2, 4, 8, 16, 32 etc.




<h2>The Time Class</h2>

This type represents the days of the week.




<table>

 <tbody>

  <tr>

   <td width="397"><strong>Time</strong>Class</td>

  </tr>

  <tr>

   <td width="397"><strong>Properties</strong></td>

  </tr>

  <tr>

   <td width="397">+  Hours {get; set;} : int+  Minutes {get; set;}: int+  Seconds {get; set;}: int</td>

  </tr>

  <tr>

   <td width="397"><strong>Methods</strong></td>

  </tr>

  <tr>

   <td width="397">+  Time(hours : int, minutes : int, seconds : int)+  ToString() : string</td>

  </tr>

 </tbody>

</table>




<h3>Properties:</h3>

All of the properties have public getters and private setters and are self-explanatory.

<ol>

 <li><strong>Hours</strong> – this property is an int representing the hour. The getter is public and the setter is private.</li>

 <li><strong>Minutes</strong> – this property is an int representing the minute. The getter is public and the setter is private.</li>

 <li><strong>Seconds</strong> – this property is an int representing the second. The getter is public and the setter is private.</li>

</ol>

<h3>Methods:</h3>

<ol>

 <li><strong>Time(</strong><strong>int</strong><strong> hours, </strong><strong>int</strong><strong> minutes, </strong><strong>int</strong><strong> seconds)</strong> – This public constructor takes three int parameters and assigns them to the appropriate properties</li>

 <li><strong>ToString()</strong> – This method overrides the same method of the Object class. It does not take any parameter but return a string representation of itself. You decide on the format for the output.</li>

</ol>

<h2>The Movie Class</h2>

This class will model a movie.




<table>

 <tbody>

  <tr>

   <td width="397"><strong>Movie</strong>Class</td>

  </tr>

  <tr>

   <td width="397"><strong>Properties</strong></td>

  </tr>

  <tr>

   <td width="397">+  Length {get; set;} : int+  Title {get; set;}: string+  Genre {get; set;}: MovieGenre+  Cast {get; set;}: List&lt;string&gt;</td>

  </tr>

  <tr>

   <td width="397"><strong>Methods</strong></td>

  </tr>

  <tr>

   <td width="397">+  Movie(title : string, length : int)+  AddActor(actor : string) : void+  SetGenre(genre : MovieGenre) : void+  ToString() : string</td>

  </tr>

 </tbody>

</table>




<h3>Properties:</h3>

All of the properties have public getters and private setters and are self-explanatory.

<ol>

 <li><strong>Length</strong> – this property is an int representing the length of the movie in minutes. The getter is public and the setter is private.</li>

 <li><strong>Title</strong> – this property is a string representing the title of the movie. The getter is public and the setter is private.</li>

 <li><strong>Genre</strong> – this property is an enum representing the genre of this movie. The getter is public and the setter is private.</li>

 <li><strong>Cast</strong> – this property is a list of string representing the names of the actors in this movie. The getter is public and the setter is private.</li>

</ol>

<h3>Methods:</h3>

<ol>

 <li><strong>Movie(</strong><strong>string</strong><strong> name, </strong><strong>int</strong><strong> length)</strong> – This public constructor takes one string and one int It does the following:

  <ol>

   <li>Assigns the arguments to the appropriate properties.</li>

   <li>Initialize the Cast property to</li>

  </ol></li>

 <li><strong>AddActor(string actor)</strong> – This public method takes a single a string argument and adds it to the collection of actors (<strong>Cast</strong>).</li>

 <li><strong>SetGenre(</strong><strong>MovieGenre</strong><strong> genre)</strong> – This public method takes a single enum argument and assigns it to the property of the same name.</li>

 <li><strong>ToString()</strong> – This method overrides the same method of the Object class. It does not take any parameter but return a string representation of itself. You will need to build a single string comprising all of the actors in this movie. You decide on the format for the output.</li>

</ol>

<h2>The Show Class</h2>

This class models a movie show. You will also implement this in Visual Studio. A short description of the class members is given below:

<table>

 <tbody>

  <tr>

   <td width="397"><strong>Show</strong>Class</td>

  </tr>

  <tr>

   <td width="397"><strong>Properties</strong></td>

  </tr>

  <tr>

   <td width="397">+  Price {get; set;} : double+  Day {get; set;} : MovieDay+  Movie {get; set;} : Movie+  Time {get; set;} : Time</td>

  </tr>

  <tr>

   <td width="397"><strong>Methods</strong></td>

  </tr>

  <tr>

   <td width="397">+  Show(movie : Movie, day : MovieDay, price  : double, time : Time )+  ToString() : string</td>

  </tr>

 </tbody>

</table>

























<h3>Properties:</h3>

<ol>

 <li><strong>Price</strong> – this property is a double representing the price of admission to this show. The getter is public and the setter is private.</li>

 <li><strong>Day</strong> – this property is an enum representing the day of the week of this show. The getter is public and the setter is private.</li>

 <li><strong>Movie</strong> – this property is an object reference of the movie class. The getter is public and the setter is private.</li>

 <li><strong>Time</strong> – this property is an object of the Time class representing the time of this show. The getter is public and the setter is private.</li>

</ol>

<h3>Methods:</h3>

<ol>

 <li><strong>Show(</strong><strong>Movie</strong><strong> movie, </strong><strong>MovieDay</strong><strong> day, </strong><strong>double</strong><strong> price, </strong><strong>Time</strong><strong> time)</strong> – This is the public constructor that takes four arguments and assigns them to the appropriate properties.</li>

 <li><strong>ToString()</strong> – This is the public method overrides the method of the same name in the object class to return a meaningful description of this object.</li>

</ol>




<h2>The Theater Class</h2>

This class models a theater. You will also implement this in Visual Studio. A short description of the class members is given below:




<table>

 <tbody>

  <tr>

   <td width="397"><strong>Theatre</strong>Class</td>

  </tr>

  <tr>

   <td width="397"><strong>Properties</strong></td>

  </tr>

  <tr>

   <td width="397">+  Shows {get; set;} : List&lt;Show&gt;+  Name {get; set;} : string</td>

  </tr>

  <tr>

   <td width="397"><strong>Methods</strong></td>

  </tr>

  <tr>

   <td width="397">+  Theater(name : string)+  AddShow(show : Show) : void+  PrintShows() : void+  PrintShows(genre : MovieGenre) : void+  PrintShows(day : MovieDay) : void+  PrintShows(time : Time) : void+  PrintShows(actor : string) : void</td>

  </tr>

 </tbody>

</table>




<h3>Properties:</h3>

<ol>

 <li><strong>Shows</strong> – this private field is a list of Show objects. The getter is public and the setter is private.</li>

 <li><strong>Name</strong> – this private field is a string representing the name of the theater.</li>

</ol>

<h3>Methods:</h3>

<ol>

 <li><strong>Theater(</strong><strong>string</strong><strong> name)</strong> – This is the public constructor that takes the name of the theater. This constructor does the following:

  <ol>

   <li>Assigns the argument to the property.</li>

   <li>Initialize the <strong>Shows</strong> property to a new list of show</li>

  </ol></li>

 <li></li>

</ol>

<table width="100%">

 <tbody>

  <tr>

   <td>Again, this is a good example of method overloading</td>

  </tr>

 </tbody>

</table>

<ul>

 <li><strong>AddShow(</strong><strong>Show</strong><strong> show)</strong> – This public method takes a show object and adds it to the collection of shows.</li>

</ul>

<ol start="3">

 <li><strong>PrintShows()</strong> – This public method does not take any argument neither does it return a value. It displays all the shows that is available.</li>

 <li><strong>PrintShows(</strong><strong>MovieGenre</strong><strong> genre)</strong> – This public method takes a genre as an argument and display all the shows that contains the flag of this genre.</li>

 <li><strong>PrintShows(</strong><strong>MovieDay</strong><strong> day)</strong> – This public method takes a day object as an argument and display all the shows matching this day object.</li>

 <li><strong>PrintShows(</strong><strong>Time</strong><strong> time)</strong> – This public method takes a time object as an argument and display all the shows matching the hour value of this time object.</li>

 <li><strong>PrintShows(</strong><strong>string</strong><strong> actor)</strong> – This public method takes a string representing the name of an actor as an argument and display all the shows that this actor appears in.</li>

</ol>

<h2>Testing</h2>

In your test harness (the Main() method in the Program Class), copy and paste the following code:

Movie terminator = new Movie(“Judgement Day”, 105);

terminator.AddActor(“Arnold Schwarzenegger”);

terminator.SetGenre(MovieGenre.Horror | MovieGenre.Action);

terminator.AddActor(“Linda Hamilton”);

Show s1 = new Show(terminator, MovieDay.Mon, 5.95, new Time(11, 35, 0));




Console.WriteLine(s1);

Theater eglinton = new Theater(“Cineplex”);

eglinton.AddShow(s1);

eglinton.PrintShows();                                   //displays one object




Movie godzilla = new Movie(“Godzilla 2014”, 123);

godzilla.AddActor(“Aaron Johnson”);

godzilla.AddActor(“Ken Watanabe”);

godzilla.AddActor(“Elizabeth Olsen”);

godzilla.SetGenre(MovieGenre.Action);




Movie trancendence = new Movie(“Transendence”, 120);

trancendence.AddActor(“Johnny Depp”);

trancendence.AddActor(“Morgan Freeman”);

trancendence.SetGenre(MovieGenre.Comedy);

eglinton.AddShow(new Show(trancendence, MovieDay.Sun, 7.87, new Time(18, 5, 0)));




Movie m1 = new Movie(“The Shawshank Redemption”, 120);

m1.AddActor(“Tim Robbins”);

m1.AddActor(“Morgan Freeman”);

m1.SetGenre(MovieGenre.Action);

eglinton.AddShow(new Show(m1, MovieDay.Sun, 8.87, new Time(14, 5, 0)));







m1 = new Movie(“Olympus Has Fallen”, 120);

m1.AddActor(“Gerard Butler”);

m1.AddActor(“Morgan Freeman”);

m1.SetGenre(MovieGenre.Action);

eglinton.AddShow(new Show(m1, MovieDay.Sun, 8.87, new Time(16, 5, 0)));




m1 = new Movie(“The Mask of Zorro”, 136);

m1.AddActor(“Antonio Banderas”);

m1.AddActor(“Anthony Hopkins”);

m1.AddActor(” Catherine Zeta-Jones”);

m1.SetGenre(MovieGenre.Action | MovieGenre.Romance);

eglinton.AddShow(new Show(m1, MovieDay.Sun, 8.87, new Time(16, 5, 0)));




m1 = new Movie(“Four Weddings and a Funeral”, 117);

m1.AddActor(“Hugh Grant”);

m1.AddActor(“Andie MacDowell”);

m1.AddActor(“Kristin Scott Thomas”);

m1.SetGenre(MovieGenre.Comedy | MovieGenre.Romance);

eglinton.AddShow(new Show(m1, MovieDay.Sat, 8.87, new Time(15, 5, 0)));




m1 = new Movie(“You’ve Got Mail”, 119);

m1.AddActor(“Tom Hanks”);

m1.AddActor(“Meg Ryan”);

m1.SetGenre(MovieGenre.Comedy | MovieGenre.Romance);

eglinton.AddShow(new Show(m1, MovieDay.Sat, 8.87, new Time(15, 5, 0)));




Show s2 = new Show(godzilla, MovieDay.Mon, 6.89, new Time(13, 15, 0));

eglinton.AddShow(s2);




s2 = new Show(godzilla, MovieDay.Sun, 6.89, new Time(14, 15, 0));

eglinton.AddShow(s2);




s2 = new Show(godzilla, MovieDay.Sun, 6.89, new Time(16, 55, 0));

eglinton.AddShow(s2);




eglinton.PrintShows();                                       //displays ten objects




eglinton.PrintShows(MovieDay.Sun);                           //displays six objects




eglinton.PrintShows(MovieGenre.Action);                      //displays seven objects




eglinton.PrintShows(MovieGenre.Romance);                     //displays three objects




eglinton.PrintShows(MovieGenre.Action | MovieGenre.Romance); //displays one object




eglinton.PrintShows(“Morgan Freeman”);                       //displays three objects




eglinton.PrintShows(new Time(14, 30, 0));                    //displays two objects