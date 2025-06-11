# cmsc430-project-2-solved
**TO GET THIS SOLUTION VISIT:** [CMSC430 Project 2 Solved](https://mantutor.com/product/cmsc-430-project-2-solved-2/)


---

**For Custom/Order Solutions:** **Email:** mantutorcodes@gmail.com  

*We deliver quick, professional, and affordable assignment help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;113943&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CMSC430 Project 2 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
The second project involves modifying the syntactic analyzer for the attached compiler by adding to the existing grammar. The full grammar of the language is shown below. The highlighted portions of the grammar show what you must either modify or add to the existing grammar.

function:

function_header {variable} body

function_header:

FUNCTION IDENTIFIER [parameters] RETURNS type ;

variable:

IDENTIFIER : type IS statement

parameters:

parameter {, parameter}

parameter: IDENTIFIER : type

type:

INTEGER | REAL | BOOLEAN

body:

BEGIN statement END ;

statement:

expression ; |

REDUCE operator {statement} ENDREDUCE ; |

IF expression THEN statement ELSE statement ENDIF ; |

CASE expression IS {case} OTHERS ARROW statement ENDCASE ;

operator: ADDOP | MULOP

case:

WHEN INT_LITERAL ARROW statement

expression: ( expression ) |

expression binary_operator expression |

NOTOP expression |

INT_LITERAL | REAL_LITERAL | BOOL_LITERAL |

IDENTIFIER binary_operator: ADDOP | MULOP | REMOP | EXPOP | RELOP | ANDOP | OROP

In the above grammar, the red symbols are nonterminals, the blue symbols are terminals and the black punctuation are EBNF metasymbols. The braces denote repetition 0 or more times and the brackets denote optional.

Your parser should be able to correctly parse any syntactically correct program without any problem.

You must modify the syntactic analyzer to detect and recover from additional syntax errors using the semicolon as the synchronization token. To accomplish detecting additional errors an error production must be added to the function header, another to the variable declaration and a final one to the when clause of the case statement.

Your bison input file should not produce any shift/reduce or reduce/reduce errors. Eliminating them can be difficult so the best strategy is not introduce any. That is best achieved by making small incremental additions to the grammar and ensuring that no addition introduces any such errors.

An example of compilation listing output containing syntax errors is shown below:

1 — Multiple errors

2

3 function main a integer returns real;

Syntax Error, Unexpected INTEGER, expecting ‘:’

4 b: integer is * 2;

Syntax Error, Unexpected MULOP 5 c: real is 6.0;

6 begin

7 if a &gt; c then

8 b 3.0;

Syntax Error, Unexpected REAL_LITERAL, expecting ‘;’

9 else

10 b = 4.;

11 endif;

12 ;

Syntax Error, Unexpected ‘;’, expecting END

Lexical Errors 0

Syntax Errors 4

Semantic Errors 0

You are to submit two files.

• The first is a .zip file that contains all the source code for the project. The .zip file should contain the flex input file, which should be a .l file, the bison file, which should be a .y file, all .cc and .h files and a makefile that builds the project.

• The second is a Word document (PDF or RTF is also acceptable) that contains the documentation for the project, which should include the following:

a. A discussion of how you approached the project

b. A test plan that includes test cases that you have created indicating what aspects of the program each one is testing and a screen shot of your compiler run on that test case

c. A discussion of lessons learned from the project and any improvements that could be made

Grading Rubric

Criteria Meets Does Not Meet

Functionality 70 points 0 points

Parses all syntactically correct programs (25) Does not parse all syntactically correct programs (0)

Productions correctly implement precedence and associativity (10) Productions do not correctly

implement precedence and associativity (0)

Grammar contains no shift/reduce or reduce/reduce errors (5) Grammar contains shift/reduce or reduce/reduce errors (0)

Detects and recovers from all programs with single syntax errors (20) Does not detect and recover from errors in the function header (0)

Detects and recovers from a program with multiple syntax errors (10) Does not detect and recover from multiple errors (0)

Test Cases 15 points 0 points

Includes test cases that test all grammar productions (6) Does not include test cases that test all grammar productions (0)

Includes test cases that test errors in all productions (6) Does not include test cases that test errors in all productions (0)

Includes test case with multiple errors

(3) Does not include test case with multiple errors (0)

Documentation 15 points 0 points

Discussion of approach included (5) Discussion of approach not included (0)

Lessons learned included (5) Lessons learned not included (0)
