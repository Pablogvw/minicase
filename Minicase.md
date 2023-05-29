![](Aspose.Words.bce40b48-2d3c-4af1-81a5-af85247f565c.001.png)

`                                                                   `Decision Support Analysis	 



![](Aspose.Words.bce40b48-2d3c-4af1-81a5-af85247f565c.002.png)

**Collaborative activity: Mini case 1 - Linear programming**


Pablo García Von Westarp - **A01737407**

Alejandro Domínguez Cañongo - **A01737708**

Jose Angel Maldonado Navarrete - 

Luis Efrén Victorio Nava - **A01736847**

26 May 2023


Decision Support Analysis

Hesus Garcia Cobos 



Consider the WhiskasModel1.py

1. What are the two parameters that the LpProblem function implements?

**The first is “The whiskas problem” and the second is “LpMinimize”**


1. Is it mandatory to name the prob variable as prob?

**No, the name is not important. Variable names can be chosen freely In this case “prob” is the abbreviation for “probability” and it was used because it was an adequate option for the probability variable.**


1. What are LpContinous and LpInteger used for?

**They are the options of the four parameters of the class “LpVariable”; the predetermined value is LpContinuous. If we were modeling the number of cans to be produced, we would need to input LpInteger since it is discrete data.**

**The choice between LpContinuous and LpInteger depends on the problem, if it involves continuous or discrete decision-making.**


1. Explain and copy the section of code that defines the objective function.

**# The objective function is added to 'prob' first**

**prob += 0.013 \* x1 + 0.008 \* x2, "Total Cost of Ingredients per can"**

`	`Explanation:

The objective function is being defined and added to a variable called prob. The objective function represents the quantity that needs to be minimized or maximized in an optimization problem.

The objective function consists of two terms: **0.013 \* x1** and **0.008 \* x2**. 

The terms involve two variables, **x1** and **x2**, which are likely decision variables in the optimization problem. The objective function is evaluating the total cost of ingredients per can based on the values assigned to **x1** and **x2**. The coefficients **0.013** and **0.008** determine the impact of each variable on the cost.

By adding this expression to prob, it is being included as the objective function in the optimization model. The objective function's purpose is to be either minimized or maximized, depending on the nature of the optimization problem being solved.

The comment "Total Cost of Ingredients per can" provides a descriptive label or explanation for the objective function, which may be useful for documentation or interpretation purposes but does not affect the functionality of the code itself.


1. Explain and copy the section of code that defines the constraints.

**# The five constraints are entered**

**prob += x1 + x2 == 100, "PercentagesSum"**

**prob += 0.100 \* x1 + 0.200 \* x2 >= 8.0, "ProteinRequirement"**

**prob += 0.080 \* x1 + 0.100 \* x2 >= 6.0, "FatRequirement"**

**prob += 0.001 \* x1 + 0.005 \* x2 <= 2.0, "FibreRequirement"**

**prob += 0.002 \* x1 + 0.005 \* x2 <= 0.4, "SaltRequirement"**

`	`Explanation:

In the code, the constraints are added to a variable called prob, which represents the optimization problem itself.

Let's go through each constraint one by one:

**prob += x1 + x2 == 100, "PercentagesSum":**

This constraint represents a requirement that the sum of x1 and x2 should equal 100. It ensures that the percentages of x1 and x2 together add up to 100%. The label or comment "PercentagesSum" provides a descriptive name for this constraint.

**prob += 0.100 \* x1 + 0.200 \* x2 >= 8.0, "ProteinRequirement":**

This constraint represents a protein requirement. It specifies that the product of 0.100 and x1 plus the product of 0.200 and x2 should be greater than or equal to 8.0. The values 0.100 and 0.200 are coefficients that determine the impact of x1 and x2 on meeting the protein requirement. The label "ProteinRequirement" provides a description of this constraint.

**prob += 0.080 \* x1 + 0.100 \* x2 >= 6.0, "FatRequirement":**

This constraint represents a fat requirement. It specifies that the product of 0.080 and x1 plus the product of 0.100 and x2 should be greater than or equal to 6.0. The values 0.080 and 0.100 are coefficients that determine the impact of x1 and x2 on meeting the fat requirement. The label "FatRequirement" provides a description of this constraint.

**prob += 0.001 \* x1 + 0.005 \* x2 <= 2.0, "FibreRequirement":**

This constraint represents a fiber requirement. It specifies that the product of 0.001 and x1 plus the product of 0.005 and x2 should be less than or equal to 2.0. The values 0.001 and 0.005 are coefficients that determine the impact of x1 and x2 on meeting the fiber requirement. The label "FibreRequirement" provides a description of this constraint.

**prob += 0.002 \* x1 + 0.005 \* x2 <= 0.4, "SaltRequirement":**

This constraint represents a salt requirement. It specifies that th

e product of 0.002 and x1 plus the product of 0.005 and x2 should be less than or equal to 0.4. The values 0.002 and 0.005 are coefficients that determine the impact of x1 and x2 on meeting the salt requirement. The label "SaltRequirement" provides a description of this constraint.

By adding these constraints to prob, they are included as part of the optimization model. 

The purpose of constraints is to impose restrictions on the values that **x1** and **x2** can take during the optimization process. 

The objective is to find values for x1 and x2 that simultaneously satisfy all the constraints while optimizing the objective function.

1. Is this a minimization or maximization problem?

`	`**Minimization problem**

**Uncle Ben's wants to produce its cat food products as economically as possible, varying the amounts of each ingredient used while still meeting their nutritional standards.**

1. Run the WhiskasModel1.py code. (no need to make changes, just runt it as is) What is the value of the following variables. 

**Status:**

` `**Beef Percent = 66.0**

**Chicken Percent = 34.0**

**Total Cost of Ingredients per can = 0 .97**





