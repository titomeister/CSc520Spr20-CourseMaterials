# Coding Rubric

See https://www.cs.tufts.edu/comp/105-2019s/coding-rubric.html for
the same coding rubric in a different format.

## Documentation

### Exemplary

* The contract of each function is clear from the function's name, the names of 
  its parameters, and the documentation.

* Each function is documented with a contract that explains what the function 
  returns, in terms of the parameters, which are mentioned by name.

* From the name of a function, the names of its parameters, and the accompanying 
  documentation, it is easy to determine how each parameter affects the result.

* When not clear from just parameter names, the contract includes constraints on 
  what inputs are permissible, e.g. that n must be nonnegative.

* The contract of each function is written without case analysis, or case 
  analysis was unavoidable.

* Documentation appears consistent with the code being described.

### Satisfactory

* A function's contract omits some parameters.

* A function's documentation mentions every parameter, but does not specify a 
  contract.

* A function's documentation includes information that is redundant with the 
  code, e.g., "this function has two parameters."

* A function's contract omits some constraints on parameters, e.g., forgetting 
  to say that the contract requires nonnegative parameters.

* A function's contract includes a case analysis that could have been avoided, 
  perhaps by letting some behavior go unspecified.

### Must Improve

* A function is not named after the thing it returns, and the function's 
  documentation does not say what it returns.

* A function's documentation includes a narrative description of what happens in 
  the body of the function, instead of a contract that mentions only the 
  parameters and result.

* A function's documentation neither specifies a contract nor mentions every 
  parameter.

* There are multiple functions that are not part of the specification of the 
  problem, and from looking just at the names of the functions and the names of 
  their parameters, it's hard for us to figure out what the functions do.

* A function's contract includes a redundant case analysis.

* Documentation appears inconsistent with the code being described.

## Form

### Exemplary

* All code fits in 80 columns.

* The submitted code contains no tab characters.

* All code respects the offside rule

* Indentation is consistent everywhere.

* Indentation leaves most code in the left half or middle part of the line.

* In bridge languages, if a construct spans multiple lines, its closing 
  parenthesis appears at the end of a line, possibly grouped with one or more 
  other closing parentheses.

* No code is commented out.

* Code is tested using unit-test forms, not print calls. Submitted solutions do 
  not print.

### Satisfactory

* One or two lines are substantially wider than 80 columns.

* The code contains one or two violations of the offside rule

* In one or two places, code is not indented in the same way as structurally 
  similar code elsewhere.

* Indentation pushes significant amounts of code to the right margin.

* Solution file may contain clearly marked test functions, but they are never 
  executed. It's easy to read the code without having to look at the test 
  functions.

### Must Improve

* Three or more lines are substantially wider than 80 columns.

* An ASCII tab character lurks somewhere in the submission.

* The code contains three or more violations of the offside rule

* The code is not indented consistently.

* Indentation pushes significant amounts of code so far to the right margin that 
  lots of extra line breaks are needed to stick within the 80-column limit.

* The closing parenthesis of a multi-line construct is followed by more code (or 
  by an open parenthesis) on the same line.

* A closing parenthesis appears on a line by itself.

* Solution file contains code that has been commented out.

* Solution file contains test expressions that are outside any `check-expect` or 
  `check-error`.

* When loaded, solution file prints test results.

## Naming	

### Exemplary

* Each function is named either with a noun describing the result it returns, or 
  with a verb describing the action it does to its argument. (Or the function is 
  a predicate and is named as suggested below.)

* A function that is used as a predicate (for if or while) has a name that is 
  formed by writing a property followed by a question mark. Examples might 
  include even? or prime?. (Applies only if the language permits question marks 
  in names.)

* In a function definition, the name of each parameter is a noun saying what, in 
  the world of ideas, the parameter represents.

* Or the name of a parameter is the name of an entity in the problem statement, 
  or a name from the underlying mathematics.

* Or the name of a parameter is short and conventional. For example, a magnitude 
  or count might be `n` or `m`. An index might be `i`, `j`, or `k`. A pointer 
  might be `p`; a string might be `s`. A variable might be `x`; an expression 
  might be `e`.

### Satisfactory

* Functions' names contain appropriate nouns and verbs, but the names are more 
  complex than needed to convey the function's meaning.

* Functions' names contain some suitable nouns and verbs, but they don't convey enough information about what the function returns or does.

* A function that is used as a predicate (for if or while) does not have a name 
  that ends in a question mark. (Applies only if the language permits question 
  marks in names.)

* The name of a parameter is a noun phrase formed from multiple words.

* Although the name of a parameter is not short and conventional, not an English 
  noun, and not a name from the math or the problem, it is still 
  recognizable—perhaps as an abbreviation or a compound of abbreviations.

### Must Improve

* Function's names include verbs that are too generic, like "calculate", 
  "process", "get", "find", or "check"

* Auxiliary functions are given names that don't state their contracts, but that 
  instead indicate a vague relationship with another function. Often such names 
  are formed by combining the name of the other function with a suffix such as 
  aux, helper, 1, or even _.

* Course staff cannot identify the connection between a function's name and what 
  it returns or what it does.

* The name of a parameter is a compound phrase phrase which could be reduced to 
  a single noun.

* The name of some parameter is not recognizable—or at least, course staff 
  cannot figure it out.


## Structure	

### Exemplary

* In every case analysis, all cases are necessary.

* The code of each function is so clear that, with the help of the function's 
  contract, course staff can easily tell whether the code is correct or 
  incorrect.

* There's only as much code as is needed to do the job.

* In the body of a recursive function, the code that handles the base case(s) 
  appears before any recursive calls.

* Solutions to Impcore and uScheme problems are recursive, as requested in the 
  assignment.

* Expressions cannot be made any simpler by application of algebraic laws.


### Satisfactory

* In some case analyses, there are cases which are redundant (i.e., the 
  situation is covered by other cases which are also present in the code).

* Course staff have to work to tell whether the code is correct or incorrect.

* There's somewhat more code than is needed to do the job.

* Code for one or more base cases appears after a recursive call.


### Must Improve

* From reading the code, course staff cannot tell whether it is correct or incorrect.

* From reading the code, course staff cannot easily tell what it is doing.

* There's about twice as much code as is needed to do the job.

* Impcore or uScheme code uses while or set (serious fault)

* A significant fraction of the case analyses in the code, maybe a third,
  are redundant.

* Code can be simplified by applying algebraic laws. For example, the code says 
  `(+ x 0)`, but it could say just `x`.

## Testing	

### Exemplary

* Tests are written using check-expect, check-assert, check-error, or other 
  unit-testing forms.

* Expected outputs are tested using check-assert for Boolean functions and 
  check-expect for other functions.

* Every test checks behavior that is required by the function's contract.

* There is one unit test for each permissible form of input.

* Additional tests are documented with a note about their purpose.

* To the degree possible, every Boolean function is tested with every form of 
  input for both "true" and "false" results. (Not every result is always 
  possible with every form of input.)


### Satisfactory

* An expected Boolean output is tested by using check-expect to expect truth or 
  falsehood.

* There is a test for each permissible form of input, plus additional, 
  undocumented tests.

* Boolean functions are tested with only one result per form of input.

### Must Improve

* Tests are written as top-level expressions.

* An expected output is tested by using check-assert with = or other equality 
  test.

* Some test uses inputs that violate the function's contract or provoke other 
  undefined behavior.

* There are so many tests that course staff can't easily identify the basic 
  tests for each form of input.


## Correctness

### Exemplary

* Staff functional correctness tests pass with no faults.

* Or, under test, staff functional correctness tests identify tiny faults 
  arising from problems with arithmetic overflow or from some confusion about 
  exactly what numbers are prime.

### Satisfactory

* Staff functional correctness tests identify a few faults.

* Or, staff functional correctness tests identify a single fault that shows a 
  lack of understanding.

### Must Improve

* Staff functional correctness tests identify a preponderance of faults.

* Staff functional correctness tests fail because the names of helper functions  
  are spelled differently in different places (serious fault).

* When we attempt to load solution code, there are errors (No Credit).

* The solution does not complete the test suite in 250ms of CPU time (No 
  Credit).
