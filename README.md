# Text-Em-All Back End Coding Challenge


1. [Requirements](#requirements)
2. [Setup](#setup)
3. [Challenge 1](#challenge-1)
4. [Challenge 2](#challenge-2)
5. [Submission](#submission)

<a name="requirements"></a>
## Requirements

You will need the following to complete this coding challenge:

1. Visual Studio 2017 or later
2. SQL Server 2016 or later

<a name="setup"></a>
## Setup

1. Using Visual Studio, create a Web API project.  You may choose to use either
   .NET Framework 4.7 or above, .NET Core 3.1, or .NET 5.
2. Optionally, add your project to a Git repo.  Although this is not required,
   it is our preferred method to review your code.  *Note:  Please do not attempt to add your code to this repo (through a fork or PR) as this would make your solution visible to others.*
3. Using SQL Server, run the `db_scripts\create_tea_test_db.sql` script.  This script will create the `School` database, set up the schema shown below, and populate it with test data.

![school-db-schema](readme_assets/db_schema.png)

<a name="challenge-1"></a>
## Challenge 1

Add an endpoint to return a list of students and their GPAs.  

```
GET /students
```

1. The endpoint should return JSON similar to that shown below.
2. The GPA is not stored in the database, so it must be calculated.
3. Ignore `null` grades when calculating the GPA.

```
[
   {
      "studentId":2,
      "firstName":"Gytis",
      "lastName":"Barzdukas",
      "gpa":3.8
   },
   {
      "studentId":3,
      "firstName":"Peggy",
      "lastName":"Justice",
      "gpa":3.4
   },
   ...
   {
      "studentId":30,
      "firstName":"Alicia",
      "lastName":"Shan",
      "gpa":3.75
   }
]
```

<a name="challenge-2"></a>
## Challenge 2

This challenge is unrelated to the School database or API, but should be
included in the same solution.

Create a class named `Challenge2` with the following method named
`MaxDistance`:  

```
public class Challenge2
{
   public int MaxDistance(string input)
   {
       throw new NotImplementedException();
   }
}
```

Implement `MaxDistance` to return the maximum distance for a pair of letters in the string `input`.  The maximum distance is defined as the largest difference between any `input[i]` and `input[j]` where `i < j` and `input[i]` comes before `input[j]` in the alphabet. 

* Sample Input = `"gbcjbdha"`
* Sample Output = 7
* Explanation: There are 7 letters between `'b'` and `'j'` AND `'b'` comes before `'j'` alphabetically AND index of `'j'` > index of `'b'`

<a name="submission"></a>
## Submission

1. Make your solution available to us, ideally in a public Git repository.  You
   may also try to email a zipped copy of your solution, but there is a
   chance this will be blocked.  In that case, be prepared to use another
   method, such as Dropbox or Google Drive.
2. Include any special instructions to run your code.
