# Machine_Learning-for-Economics
# probability

<b>Sample space</b>
* describe the sample space
* describe the likehood of the outcomes

setes are denoted by $\omega$ 

<b>sets</b>
* infinite
* descrete/finite
* continious


<b> De Morgon's Law</b>

$(S\cap T)^{c} = S^c \cup T^c$

or,

$ S^c \cap T^c = (S \cup T)^c $


### sequences and their limits

$a_i \to a $ if $a_i$ converges to a
$b_i \to b $ if $b_i$ converges to b 


then

$a_i + b_i \to a+b$


$\sum \limits_{i=0} ^\infty \alpha^{i}$ = $1 + \alpha + \alpha^2+ ........$ where 

$\mid\alpha \mid< 1$

its sum equal to =

   $\frac{1}{1-\alpha}$ 

### conditioning probability
$P(A \mid B)$ = Probability of events A, where the events B has occured.

$P(A \mid B) = \frac{P(A \cap B)}{P(B)}$


#### multiplication Rule
$P(A \mid B) = \frac{P(A \cap B)}{P(B)}$

therefore,

$P(A \cap B) = P(B) * P(A \mid B)$


#### total probability theorem
suppose there is an event B which occurs in the three scenerio A1,A2,A3 or consider a universal set is divided among A1,A2,A3 
and there is a circle inside it which lies in the areas of all the A's .

$P(B)$ = $P(B \cap A_1) + P(B \cap A_2) + P( B \cap A_3)$
 $= P(A_1)P(B\mid A_1)+........$
 
 
 $P(B) = \sum \limits_{i}^{} P(A_i)P(B \mid A_i)$
#### Baye's Rule
check on internet..formula can be derive from the conditioning probability
#### independent events
if A and B are independent events then
$P (A \mid B) = P (B)$

and 

$P ( A \cap B) = P(A)*P(B)$
### Descrete Random variable

* takes value in finite and countable
* PMF
* Random variable examples
    * bernoulli
    * uniform
    * binomial
    * geometric
* expectation and its properties
    * expected value rule 
    * linearity
Random variable:
    it takes the finite random values.
    eg: taking the random students and recording their weights

        f(takes student) = produce weight
        
   eg: now suppose you have taken the data of height and the weight then the body mass index $B = \frac{w}{h^2}$ we can find our sample space of the bodymass index of the students
        
#### Probability Mass Function
consider a scenerio where and evens denoted by some numbers let's say 5,4,3
where, each events has two elements
5 --> a,b
4 --> c
3 --> d
Now probability of an event 5 would be:
$x =5$

${w:X(w) = 5} ={a,b}$

$P(X=5) = \frac{2}{4}$


$_{pX}(x)=P(X=x) = P({\omega\in\Omega s.t. X(\omega)=x })$ 

#### Bernoulli Random Variable
A random varibale which takes the values either 1 or 0.dentoed as

$X =
\left\{
        \begin{array}{lr}
            1, \text{w.p  }  p\\
            0, \text{w.p  }  1-p\\
        \end{array}
\right\}$

means, suppose there is a sample space containing two portions denoted by $A$ and $A^C$ then whatever comes in $A$ will be denoted by 1 and similarly whatever comes in $A^c$ will be denoted by zero.

$P_{x_{A}}(1) = P(I_A =1) = P(A)$

#### uniform Random Variable

##### descrete  uniform Random variable
* it takes values in the certain range
* each value in that range have the same value.

eg: 
* Parameters: integeres a,b : $a \leq b $
* experiment: pick on of a, a+1, ----------,b at random all are equally likely.
* Sapmle space: {a, a+1,-----,b}    
* random variable:
    $X\colon X(\omega)=\omega$
* so toatal number of values would be b-a+1.
* hence, the probability of occurance of each value would be 
$\frac{1}{b-a+1}$

##### uniform Random Variable
* <b>Experiment</b>: n independent tosses of a coin with P(heads) =p
* sample sapce : set of sequences of H and T, of length n
* Random Variable X : number of heads observed.
now,
after tossing three times a coin the outcomes would be:
* HHH  
* HHT
* HTH
* HTT
* THH
* THT
* TTH
* TTT
* so 3 heads occur one time, 2 heads occur 3 times, 1 head occur 3 times, 0 head occur 1 time.
*$P_x(2) = P(X=2) = P(HHT) + P(HTH) + P(THH) $
* since for 0(no heads) prob is 1-p and for 1 it is p.
* hence,
    $P_x(2) = p*p*(1-p) + p*(1-p)*p + (1-p)*(p)*(p)$
    $=3p^2(1-p)$

so the general formula for obtaining the probability is 

$ p_{X} (k) = \binom{n}{k} * p^k * (1-p)^{n-k} $

so the above problem can be solved as 
$ p_{X} (2) = \binom{3}{2} * p^2 * (1-p)^{3-2} $
##### Geometric Random variable

* Experiment : infinitely many independent tosses of a coin p(heads)=p
* sample space : set of infinite sequence of H and T
* random variable X: number of tosses unitll the first heads 
* Model of: waiting times; number of trails unitll a success

* $ p_X (k) = P(X=k)$ means, first head appeard in k trails
so,
P(T,T,T,......k-1 times,<b>H</b>)

probability would be 
$=(1-p)^{k-1}* p$ where k = 1,2,3,4,5,....
##### Expectation/ mean of a random variable
 * suppose you are playing a game of chance 1000 times, where your earning shows as a random varibale as
 
 
 $ X =
 \left\{
     \begin{array}{lr}
         1, \text(with prob.) 2/10\\
         2, \text(with prob.) 5/10 \\
         4, \text(with prob.) 3/10 \\
     \end{array}
  \right\}
 $
 
 * avg gain would be 
 $\frac{1*200 + 2*500 + 4*300 }{1000}$
 * it can also be equal to 
 $1 * \frac{2}{10} + 2*\frac{5}{10}+3*\frac{3}{10}$
 
 or
 
 * general term
 
 $E[X] = \sum \limits_{x}^{} x*p_X(x)$
 
 * interpretation: avg in large number of independent repetitions of the experiment
example: calculate the expectation of a Bernoulli r.v

$X=
\left\{
        \begin{array}{lr}
        1, \texttt{with p  }  p\\
        0, \texttt{with p  }  1-p\\
        \end{array}
 \right\}
$

therefore,
$E[X]= 1*p + 0*(1-p) =p$


example: calculate the expectation of a uniform r.v
* uniform on 0,1,2,3,...........,n

so,

total number of values are n+1
hence, each prob of occurance is p = $\frac{1}{n+1}$

$E[X]= 0*\frac{1}{n+1}+1*\frac{1}{n+1}+2*\frac{1}{n+1}+.......$
$E[X]= \frac{1}{n+1}(0+1+2+............+n)$
$= \frac{1}{n+1} * \frac{n(n+1)}{2}$
$=\frac{n}{2}$
Example: suppose there are n students each have weight $x_i$. and exeperiment is performed where a student is randomly picked what can be the expected weight of the randomly selected student.

$p_X(x_i) = \frac{1}{n}$ denotes probability of a selection of i student at random.

$E[x] = \sum \limits_{i}^{} x_i \frac{1}{n}= \frac{1}{n} \sum \limits_{i}^{} x_i$



##### Elementary properties of expectation
* if E[constant] = constant
#### E[g(X)]
* let X be a random variable, and let Y = g(X), we have to calculate the expected value of the new random variable Y means, E[g(X)]

* averaging over y:
$E[Y]= \sum\limits_{y}^{}yP_Y(y)$

* averaging over x:
$E[Y] = E[g(X)]= \sum \limits_{x}^{}g(x)*p_X(x)$
##### Linearity of expectation

* $E[aX+b] = aE[X]+b$


x = salary, E[X] =avg.salary,  
y= new salary = 2x+100,

E[y] = E[2x +100] = 2E[x] +100

##### variance : measure of the spread of PMF
consider a random variable $X$ with mean $\mu$ = $E[X]$
* Then the distance from the mean would be $X- \mu$
* average distance from the mean would be?

$E[X-\mu] = E[X] - \mu = \mu -\mu = 0 $

so, the avg value of distance from the mean is always zero, so we want avg absolute value.so we came across variance.

<b>Variance</b>

$var(X) = E[(X - \mu)^2]$


* calculation using expected value rule

$E[g(X)]= \sum \limits_{x}^{}g(x)p_X(x)$


$ var(X) = E[g(x)] = \sum \limits_{x}{}(x-\mu)^2 p_X(x)$

<b>Standard Deviation</b>
captures the width of the distribution

$\sigma_x = \sqrt{var(X)}$

* $\mu = E[X] $

* $ var(aX+b) = a^2*var(X) $

* $ var(X) = E[X^2] - (E[X])^2$
##### Variance of the Bernoulli
problem:

$
X =
\left\{
    \begin{array}{lr}
    1, \texttt{w.p}, p\\
    0, \texttt{w.p}, 1-p\\
    \end{array}
\right\}
$

as we know,
$E[X]= 1*p + 0*(1-p) =p$

and 

* From the first formula to find variance :

$ var(X) = E[g(x)] = \sum \limits_{x}{}(x-E[X])^2 p_X(x)$

$= (1-p)^2 * p + (0-p)^2 * (1-p)$

$=p(1-p)$

* From the second formula
* $ var(X) = E[X^2] - (E[X])^2$

$p-p^2 = p(1-p)$


##### Variance of uniform random variable
$X = {0,1,2,3,......,n}$
* Each will have the prob $\frac{1}{n+1}$

as we know

$var(x) = E[X^2] - (E[X])^2 =\frac{1}{n+1}(0^2 + 1^2+...+n^2)- (\frac{n}{2})^2 $

$= \frac{1}{12} n(n+2)$

now lwt say a is the first term and b is the last so, n =b-a

$= \frac{1}{12} (b-a)(b-a+2)$
##### Conditional PMFs and Expectations given an Event
* condition on a event A
* $p_{X \mid A}(x) = P(X= x \mid A)$
* $ \sum\limits_{x}^{}p_{X \mid A}(x) = 1$
* $E[X \mid A] = \sum\limits_{x}^{} xp_{X \mid A}(x)$
* conditional model are similar like the ordinary pmf except that prob will be replaced by the conditional probability.


* <b>Problem</b>

:consider a uniform random variable where $x \in {1,2,3,4}$
* so, each will have the probability of $1/4$


* $E[X] = 2.5$
*$var = \frac{1}{12} n(n+2) = \frac{5}{4}$
 
 now let's say that $A= {X \geq 2}$
 
* $E[X \mid A] = \frac{2+4}{2}=3$


* $var(X \mid A) = \frac{1}{3}(4-3)^2 +\frac{1}{3}(3-3)^2 +\frac{1}{3}(2-3)^2 = \frac{2}{3}$
 
###### total expectation theroem
$p_X(x) = P(A_1)p_{X \mid A_1}(x) + ......+P(A_n)p_{X \mid A_n}(x)$

$E[X] = P(A_1)E[X\mid A_1] +........+P(A_n)E[X\mid A_n]$
###### Geometrc random variable(conditioning)
* X : number of independent coin tosses untill first head.
$\Pr(H) =p$
* $p_X(k) = (1-p)^{k-1}p$ where,$ 
\texttt{k = 1,2,3,....}$
* Memorylessness: number of remaining coin tosses, conditioned on Tails in the first toss,is Geometric, with parameter p


<b>Problem</b> what is the probability of getting first head given that the first toss is tail.

$\Pr(X-1 = 3 \mid X>1$ = $ \Pr(T_2 T_3 H_4 \mid T_1)$ = $\Pr(T_2,T_3,H_4)$ = $(1-p)^2 * p = P_x (3)$

so, in general

$P_{x-1 \mid x>1}(k) = P_x(k)$

##### Joint PMF( Multiple Random Variable)
Joint PMF : $p_{XY}(x,y)= \Pr(X =x \texttt{  and  } Y=y)$
* $E[X+Y] = E[X] + E[Y]$
*$E[X+Y] = E[g(x,y)]$ where. $g(x,y) = x+y$

$=\sum\limits_{x}^{}\sum\limits_{y}^{}(x+y)P_{X,Y}(x,y)$
##### The Mean of Binomial
* X: binomial with parameter n, p
* number of successes in n independent trails.
* $X_i = 1$ if the ith trial is a success. and its probability is  p
* $X_i = 0$ otherwise and its probability is 1-p

now,

let's say number of success is n

so,

$X= X_1 + X_2 + .........+X_n$
therefore,

$E[X]= E[X_1] + .............+E[X_n]$
$= n*p$
