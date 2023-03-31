>230301 Wed

1. In null-hypothesis significant testing, the p-value is the probability of obtaining test results of at least as extream as the result acually observed, under the assumbtion that the null-hypothesis is correct.
2. A very small P-value wold be very unlikely under the null-hypothesis.
3. If we state one hypothesis only and the aim of the statiscal test is to see whether this hypothesis is tenable, but not to investigate other sepecific hypotheses, than such a test is called a null-hypothesis.
4. Statistical Significant: A result can reject it.
5. The more independent observations from the same probability distribution one has, the more accurate the test wil be able to determine the mean value and show that it is not equal to 0, but this will also increase the importance of evaluation the real-world or scientific relevence of this deviation.
6. F-Value Equition.
7. 총확율의 법칙; The law of Total Probability : $P(A)=\displaystyle\sum_{n}P(An)=1$
8. A,B 사건이 연관이 되어 있느 경우 - B가 일어나 상태에서, A가 발생할 확률: $P(A|B)$
9. 연관이 없는 경우 - B가 일어난 상태, A가 발생할 확률:  $P(A) * P(B)$

>230313 Mon
1. Probability: a branch of mathematics that allows us quantify uncertainty.
2. Set Theory: a branch of mathematics based around the concept of sets. In simple terms, a set is a collection of things.
   Two key rules: 1) Each element in set is distinct. 2) The elements in a set are in no partivular order.
   Define a set, using capital letter. A = {1,2,3,4,5}
   Sets can also contain subsets.
   ex) A={1,2,3}    B={1,2,3,4,5}
   Set A is a subset of set B if all the elements in A exist within B.
3. Experiments and Sample Spaces. In probability, an experiment is somethin that produces observation(s) with some level of uncertainty.
4. A Sameple Point: a simgle possible outcome of an experiment.
5. A Sample Space: the set of all possible sample points for an experiment.
6. An Event: a specific outcome(or set of outcomes) and is a subset of the sample space. 
7. The frequentist definition of probability: If we run an experiment an infinite amount of times, the probability of each event is the proportion of times it occurs; $P(\text{EVENT})=\frac{\text{Number of Times Event Occurred}}{\text{Total Number of Trials}}$
8. Law of large numbers: The more the event occurs, the more the tru probability is calculated precisly.
>Rules of probability
1. Union $(A \ or \ B)$ of two sets encompasses any element that exists in either one or both of them.
2. Inersection $(A \ and \ B)$ of tows encompasses any element that exists in both of the sets.
3. Complement $A^{\mathrm{C}}$ of a set consists of all possible outcomes outside of the set.
>Independence and Dependence
1. Independence: The fact that a event doesn't affect the others.
2. Dependence: The fact that a event depends on the effect of the others.
3. Mutually Exclusive Events: Two events are considered mutually exclusive of they cannot occur at the same time.

>230314 Tue
- Any events that have a non-empty intersection are not mutually exclusive.
>Addtion Rule: 
1. $P(A\ or\ B) = P(A) + P(B) - P(A\ and\ B)$ because It is included twice in the addition of P(A) and P(B)
2. When it's mutual exclusive $P(A\ or\ B) = P(A) + P(B)$ becuase inersection is empty.
>Conditional Probability: 
1. measures the probability of one event occurring, given that another one has already occurred.
2. Word 'given' with a vertical line
3. Indpendent events $P(A|B) = P(A) and P(B|A) = P(B)$
>Multiplication Rule
1. A and B: $P(A\ and\ B)$ or the probability of the intersection of A and B.
2. General formula: $P(A\ and\ B)=P(A) * P(B|A)$
3. Dependent Events: $P(A\ and\ B)=P(A) * P(B|A)$
>Tree diagram
1. One way to visualize all possible outcomes of a pair of events in a tree diagram.
2. Tree Diagrams have following properties:
   - Each branch represents a specific set of events.
   - The probabilities the terminal branches( all possible sets of outcomes) sum to one.
   - We multiply across braches (using the mutiplication rule) to calculate the probabilit that each branch(set of outcomes) will occur.
3. Independent events: $P(A\ and\ B) = P(A) * P(B)$ because $P(B|A) = P(B)$
>Conditional Probability Continued
1. In case of one event, the other event is affected. we can layout all of outcomes with this situation. However, If we need a result of the opposite outcomes, which event B happend after event A, instead.
2. Bayes' Theorem $$P(B|A) = \frac{P(A|B) * P(A)}{P(B)}$$ $$P(B) = P(A\ and\ B) + P(\text{Not}A\ and\ B)$$
3. Alternative Method $$1= P(A|B)+P(\text{Not}A|B)$$ $$P(\text{Not}A|B) = 1-P(A|B)$$ $$P(\text{Not}A|B) = \ Answer$$

>230325Wed
1. Random Variables: A function to represent random events.(must be numeric) Code:

```
from numpy
random.choice(am suze=size, replace= True/False)
```
- a: A list or other object that has values we are sampling from.
- size: A number that represents how many values to choose.
- replace can be equal to True or False, and determines whether we keep a value in a after drawing it. (replace= True) or Remove it from the pool (replace= False)
2. Discrete and Continuous Random Variables
   - Discrete Random Variables: Randome variables with a countable number of possible values. (When observing counting events)
   - Continuous Random Variables: When the possible values of a random variable are uncountable, because measurements can always be more precise. etc: meters, degree
3. Probability Mass Functions
   - PMF is a type of probabnility distribution that defines the probability of observing a particular value of a discrete random variable.
   - These are certain kinds of random variables (and associated probability distributions) that are relevent for many different kind of problems. These commonly ised probability distributions have names and parameters that make them adaptable for different situations.
   - Binominal Distribution: The sum of the heights of all the bars will always equal 1.
   - When $x$ is larger, the event that we observe increases, and the probability need to be divided between more values.
4. Calculating Probabilities using Python
   ```
   import scipy
   binom.pmf()
   x: The value of interest (event)
   n: The number of trials
   p: The probability of success
   #ex
   import scupy.stats as stats
   print(stats.bionom.pmf(6, 10, 0.5)
   ```
   Notice that tow of the three values that fo into the `stats.pmf()` method are the parameters that define the binominal distribution: $n$ represents the number of trials and $p$ represents the probability of success.
5. Using the Probability Mass Function over Range $$1-(the\ sum\ of\ the\ opposite\ values)
   - Summation is always 1
   - It is used in a reverse way  
6. Cumulative Distiribution Function
   - The cumulative distribution function for a discrete random variable can be derived from the probablility mass function. However, instead of the probability of observing a specific value, the cumulative distribution function gives the probability of obseving a specific value **OR LESS**
   - The value of a cultivative distribution function at a given value is equal to the sum of the probabilities lower than it, with a value of 1 for the largest popssible number.
   - cumulative distribution functions are constantly increasing, so for two different numbers that the random variable could take on, the value of the function will always be greater for the larger number.
   - Mathematically, this is represented as: $${\sf If}\ x_{1} < x_{2} {\to} {\sf CDF(x_{1})}<{\sf CDF(x_{2})}$$
7. Cumulative Distribution Function Continued
   - To calculate the probability of a specific range by taking the difference between two values from the cumulative distribution function. Mathematically, $$P(3<=x<=6)=\ P(x<=6)-P(x<3)$$<p style="text-align: center;">OR</p>$$P(3<=x<=6)=\ P(x<=6)-P(x<=2)$$
