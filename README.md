# UnitTesting
Learn about Unit testing

what is the unit testing :
-----
the process where you test the smallest functional unit of code

why unit test:
-----------
-->Detects Bugs early
-->Improves code Quality (Trusted Code,Safe)
-->Faciliates Refactoring(can check, if code is modified will it affect other functionality)
-->Enhances Development Speed(Not much to debug)
-->Supports CI/CD(Automated Test)

ways to achieve Unit Test:
-------------------
MS Test
NUnit ---> Trending in the market
XUnit

------------------
MS Test:
------
This was introduced by microsoft And it is the first
Built in Visual Studio integration
Good for enterprise and legacy.NET Framework projects
Simple to understand
only suitable for .NET framework

Drawbacks:
--------
Fewer advanced features compared to NUnit/xUnit
Less flexible attribute system
slower innovation historically
Not the default in modern ASP.NET Core templates
Weaker dependency injextion 

============================================================
Nunit:
-----
Best suitablr projects requring for the parameterized
Very mature and stable
Rich attribute support
Excellent parameterized testing
Large community support
Flexible test

Drawbacks:
-----------
Not suitable for .NET Core
Less support for DI

==============
xUnit:
-----
modern design
Default for ASP.NET Core project
used for the .NET core

Drawbacks:
--------
not for beginners
Less features compare to NUnit

=======================

for all the attribute:
---------------
Setup --> use this attribute if you want to run any logic before running the test.
TearDown --> use this attribute if you want to run any logic after running the test.
OnetimeSetup --> use this attribute if you want to run the test before running all the test.
OnetimeTeardown --> use this attribute if you want too run the test after running all the test.
category
Ignore


=======================================================
comparsion of NUnit, MStest and xUnit:
-------------------------------

NUnit                                           MSTest                                                                    XUnit
----------
Test                                            TestMethod                                                               Fact
TestCase                                        DateRow                                                                  theory & InlineData
TestCaseSource                                  DynamicData                                                              memeberdata
oneTimeSetup                                    ClassInitialize                                                          IClassFixture<> (override before)
SetUp                                           TestInitialize                                                           Constructor
TearDown                                        TestCleanUp                                                              IDisposable.Dispose()
OneTimeTearDown                                 ClassCleanup                                                             IClassFixture<>(override after)
Ignore                                          Ignore                                                                   [Fact(Skip ="reason")]
Category                                        Category                                                                 [Trait("Key","Value")]


============================================================================================================================================================================================


TDD:
---
Test Driven Development
 -->in TDD approach the user will write testcase first and then we create necessary classes and methods
--> to fix the error:
                    you have to right click on class or method and use this potential fix.
 
MOQ Framework:
-------------
--> is all about testing a fake method
--> the data are getting from the arrays,strings and collection
--> when the real method is not there then go for the fake method

MOQ means--> Not real / Not genuine
creating fake objects(mocks)
so that we can focus on its functionality

===================================================
We can able to achieve MOQ by 3 Method:
-----------
Stub    -->   these two are custom
Fake 


MOQ Framework --> built in package

====================================================
Stub:
-----
It  gives the hard coded output
this test deosn't care about the interaction
it only rnsures the Add method returns a value so the client can function


-------------------------------------------------------------------
Fake:
----
Fakes are simplified implementations of classes or interface
basic logic is written in fake 
the database is connected in real so that we can able to write a test

-------------------------------------------------------------------
MOQ Framework:
--> it is used to create stub and fake in ready made way.
--> built in way to mock stub and fake.
objectname.object ---> is will act as a stub  object

Adv:
---
No need to create manually fake or stub class using Moq

