Modified Course Order

**Weekly activities**

| **Week  | Topics | Readings | Assigned| Due |
|---------|--------|----------|---------|-----|
| 1 | Course Introduction, Software Installation, Intro to Git |Configuration| E0 Configuration |
| 2 | Python Introduction, Test Driven Development, Koans |Scientific Python, Ch 2| E1 Basic Python Types | E0 Configuration |
| 3 | Python Interpreters, Editors, Local Testing, Strings, None | Ch 1, Ch 8, Ap. A | E2 Strings & None| E1 Basic Python Types | 
| 4 | Continious Integration Environments, Operators/operands | TBA |E3 Point Statistics | E2 Strings & None
| 5 | Sequences, Dictionaries |Ch7, Ch9, Ch11, Ch20 | Exam 1 | E3 Point Statistics |
| 6 | Conditional Execution, Files | Ch5, Ch13| E4 Iterables & Conditions | Exam 1|
| 7 | Functions, Methods, Modules | Ch4, Ch6, Ch12, Ch15 | E5 Point Pattern Module I | E4 Iterables & Conditions|
| 8 | OOP, Inheritance | Ch16, Ch21, Ch23 | E6 | E5 Point Pattern Module II |
| 9 | Composition | Ch22 | E6 Functional Point Patterns | E5 Point Pattern Module II | 
| 10| Functional Programming, List Comprehensions| TBA |Exam 2 | E5 Point Pattern Module II |
| 11| Geospatial & Numerical Libraries | TBA | E7 Numerical Programming | Exam 2| 
| 12| Event Driven Programming, Basic GUI Development | Ch10, | E8 PyQt | E7 Numerical Programming | 
| 13| Plugins & APIs| TBA| E9 QGIS Plugin I | E8 PyQt |
| 14| Event Handling & Widgets|TBA| E10 QGIS Plugin II | E9 QGIS Plugin I|
| 15| MVC |TBA| E11 Integration | E10 QGIS Plugin II |
| 16| Final Exam | | E11 Integration |

Week breakdown - my thinking is that from week 4 onwards a concept will be introduced and that concept used in some spatial way (data structure, algorithm, both, etc.).  What if we build a point pattern analysis module?

-------------

Week 1 focuses on intro readings, getting anaconda python installed (use Serge's awesome install instructions, especially for windows), and an intro to how assignments will be managed in git.  

Week 2, still no interpreter (intentionally).  Students will fix a number of assertion, and type errors in a unittest using the git web editor and validating using a pull request (Travis-CI).  Red-Green-Refactor.  This is basically a review of the basic data types covered in CSE110 (a java class).  Assignment is submitted as a PR and undergoes travis-ci testing.

Week 3, introduces the interpreter (iPython via a shell, Jupyter notebook (?)), editors, strings, and None.  

Week 4, operators / operands.  This is still pretty basic, but some spatial concepts must be coverable:
	
  * Distance between 2 points
  * Projection from Lat/Lon to Equirectangular
  * Basic descriptive statistics (can easily extend to point pattern, no simulation, algorithms

Week 5, focuses on iterable types (sets, lists), dictionaries, and an introduction to continious integration (tests have been running via Travis-CI, but here the what and why questions are explored.  Spatial data structures / algorithms that might be good for iterables:

 * Simple point metrics might be best - points within a given distances, nearest point, farthest point.
 * Topology (from polyline, to adjacency structures, to a network)
 * Using topology, line intersection would be simple enough to be achievable, point in polygon as well.
 * Gift wrapping algorithm for convex hulls is another good choice (Good if building a point module)
 * Something not in the computation geometry realm?

Week 6, conditional execution - this is where is might be good to use the convex hull (gift wrapping algorithm) because conditional execution is required.  It would also be easy to generate a marked point dataset in a generic file and look at the `with` statement for discussing context.  Reading those points in, it would then be possible to apply previously developed code to look at things like mean neighbor distance given some labeling, etc.

Week 7, 

Week 11, for the numpy items a Shimbel matrix might be a good way to explore concepts of vectorization.  Could also use a spatial interaction model (gravity model is easy).

| **Week  | Topics | Readings | Assigned| Due |
|---------|--------|----------|---------|-----|
| 1 | Course Introduction, Software Installation, Intro to Git | E0 Configuration |
| 2 | Python Introduction, Interpreters | Ch 1 | E1 Basic Python | E0 Configuration | 
| 3 | Editors , Repositories | TBA | E2 Git | E1 Basic Python |
| 4 | Operators/Operands, Sequences | Ch 2, Ch 8, 9, 11 | E3 Sequences | E2 Git |
| 5 | Dictionaries, **Exam 1** | Ch 10 | |
| 6 | Conditional Execution, Files |Ch 5, Ch 14 | E4 Random access | E3 Sequences| 
| 7 | Functions, Modules | Ch 3, 6 | E5 Functions | E4 Random access|
| 8 | Object Orientation, Inheritance | Ch 15,16, 17 | E6 Dispatching | E5 Functions |
| 9 | Composition, Functional Programming | Ch 18 | E7 Object Orientation | E6 Dispatching|
| 10 | List Comprehension, **Exam 2** ||||
| 11 | Numerical Programming, Numpy | TBA | E8 Numerical Programming | E7 Object Orientation |
| 12 | Event Driven Programming, Tkinter Introduction | Ch 19 | E9 GUI Design | E8 Numerical Programming |
| 13 | Widgets, Event Handling | Ch 19 | E10 Interaction | E9 Gui Design | 
| 14 | Test Driven Development, Doc Tests | TBA | E11 |  Doc Tests | E10 Interaction| 
| 15 | Debugging, *Review* |App A | E11 Doc Tests| 
| 16 | *Final Exam*|