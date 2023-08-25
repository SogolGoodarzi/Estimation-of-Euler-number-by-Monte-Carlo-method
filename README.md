# Estimation-of-Euler-number-by-Monte-Carlo-method
<p align="justify"> You are probably familiar with Euler's constant(e). This number is sometimes known as Napier's number, although each naming is done as a tribute to these mathematicians and the discoverer of this number is someone else. The first appearance of Napier's number in papers was in 1618 by John Napier, the inventor of the logarithm. Although he did not discover the constant itself, he did publish a list of logarithms that were obtained with the help of this constant. However, the list mentioned was probably prepared by William Oughtred. This constant was established 65 years later by Jacob Bernoulli in 1683 during the investigation of the limit of the following expression. </p>

![image](https://github.com/SogolGoodarzi/Estimation-of-Euler-number-by-Monte-Carlo-method/assets/125180530/41202a01-c81c-4e18-81d0-24c139ceddd6)

<p align="justify"> In this project, we are going to estimate the value of this constant using the Monte Carlo method. Monte Carlo methods are a wide category of computational algorithms based on random sampling from the environment. In fact, in these methods, we try to use the randomness of samples to calculate a value that is inherently non-random. The first researches on this method started with the solution of Buffon's needle problem, and after that (almost since 1930), this method was used in simulations in the fields of biology, physics, engineering, etc. During the description of the problem, you will get to know this concept better. </p>

<p align="justify"> We are going to estimate the Euler constant. Consider the curve $f(x)=e^{−x}$. We turn our attention to the range of (0, 1): (the part inside the marked rectangle). </p>

![image](https://github.com/SogolGoodarzi/Estimation-of-Euler-number-by-Monte-Carlo-method/assets/125180530/8e05ce19-ef82-4de3-9fa5-e799976913af)

### Part a.
<p align="justify"> Assuming Euler's constant, calculate the area of ​​the part of the rectangle cut off from the above figure that is under the exponential curve. (parametrically and according to e). According to the given diagram, first we calculate the area under the diagram by integration, and then we subtract the area of ​​the lower rectangle that does not include the specified rectangle from the total area. </p>

![image](https://github.com/SogolGoodarzi/Estimation-of-Euler-number-by-Monte-Carlo-method/assets/125180530/df98471e-146d-4a44-8cea-8f6b05b6ab7a)

![image](https://github.com/SogolGoodarzi/Estimation-of-Euler-number-by-Monte-Carlo-method/assets/125180530/af5976db-28bd-48ff-abaa-85caa4e325ec)

### Part b.
<p align="justify"> Now suppose we know the area of ​​the part specified in part(a) in advance (S). According to the relation obtained from the previous part, get the value of e in terms of S. According to the results, we have:

![image](https://github.com/SogolGoodarzi/Estimation-of-Euler-number-by-Monte-Carlo-method/assets/125180530/e6485d48-03d1-4277-b226-08e950635eb5)

### Part c.
<p align="justify"> Now, from the two-dimensional space enclosed by the rectangle, we extract n samples from a univariate distribution defined on this space. According to the rule of the law of large numbers, if the number of samples converges to infinity, the ratio of the number of samples that are below the curve to the total number of samples is equal to the ratio of the surface area under the chart to the total area of ​​the rectangle. That is, if you pay attention to the image in the following figure, we have: </p>

![image](https://github.com/SogolGoodarzi/Estimation-of-Euler-number-by-Monte-Carlo-method/assets/125180530/4a6be7e8-4ee8-452c-88e5-20510399f3ce)

![image](https://github.com/SogolGoodarzi/Estimation-of-Euler-number-by-Monte-Carlo-method/assets/125180530/35d7cbc8-db66-4026-871c-0492f1705bf7)

<p align="justify"> It is possible to estimate Euler's constant using Monte-Carlo's method. Assuming n = 100, provide an estimate of e. First, using the program we write, we form a two-dimensional uniform distribution for each 100 points. According to the desired ratio ($the number of lower points of the curve/the total number of points$) with the written program, this numerical ratio is approximately between 0.3 and 0.4, which is equal to the ratio of the area under the curve inside the rectangle to the total area of ​​the rectangle. So, according to the relationships we obtained in the previous sections, we will have: </p>

![image](https://github.com/SogolGoodarzi/Estimation-of-Euler-number-by-Monte-Carlo-method/assets/125180530/bb41de27-c9e7-44d6-9da6-85a9d9281073)

On the other hand, we have according to the given relationship in the question:

![image](https://github.com/SogolGoodarzi/Estimation-of-Euler-number-by-Monte-Carlo-method/assets/125180530/dc78c539-9ce6-43bc-85c6-4b6228cdc60e)

<p align="justify"> That is, the result of the upper limit, which is equal to the ratio of the mentioned areas, must be the same as the value we obtained in the simulation. As a result, we will have: </p>

![image](https://github.com/SogolGoodarzi/Estimation-of-Euler-number-by-Monte-Carlo-method/assets/125180530/bee4d120-f198-439d-aac0-c9c9dac14618)

<p align="justify"> It can be seen that the estimated value for the Napier number is very little different from its actual value. So it can be said that with this simulation we were able to find a suitable estimate for this number. </p>

### Part d.
<p align="justify"> The estimate provided in part(c) is a function of samples taken from the environment. As a result of this estimate, it is a random variable itself, in other words, if you run the script of the previous part several times, you will get different values. Suppose this random variable has a Gaussian distribution. For estimation of the values ​​of the mathematical expectation and its variance, several samples should be taken and then using maximum likelihood estimation, the mean and variance values ​​for a fixed and large n should be calculated. The estimated distribution of the estimation variable presented in part(c) is obtained. </p>

![image](https://github.com/SogolGoodarzi/Estimation-of-Euler-number-by-Monte-Carlo-method/assets/125180530/ef466614-2222-4d55-a86b-508a9eb1b7bb)

![image](https://github.com/SogolGoodarzi/Estimation-of-Euler-number-by-Monte-Carlo-method/assets/125180530/132eb864-ddbc-4436-9570-8a4c2cf07409)

Now, according to the desired program, the values ​​of expectation and estimated variance are as follows:

![image](https://github.com/SogolGoodarzi/Estimation-of-Euler-number-by-Monte-Carlo-method/assets/125180530/e2120c7d-3a21-40d4-a1f7-a69202501a50)

These values ​​are actually obtained by sampling for different $X_{i}$s. 

<p align="justify"> The estimated distribution that can be obtained from the previous section is Gaussian normal distribution. According to the central limit law, when the number of samples increases, the distribution of samples converges to a normal distribution. </p>

### Part e.
<p align="justify"> Finally, the mathematical expectation of the estimated distribution can be presented as a better estimate, and the variance of the above Gaussian estimate is a measure of our uncertainty compared to the estimate we have provided. Obviously, our uncertainty will never be zero, for example, one of the first factors that creates uncertainty is the approximation that we applied to the number of samples. According to relation 4, the number of samples should approach infinity, but in part (c) and (d) we assumed the number of samples to be equal to 100. So we can expect that the larger n we make, the uncertainty of the estimate will decrease and converges to zero. To evaluate this hypothesis, change the number of samples between 1 and 1000 and for each value, calculate the mathematical expectation n and the variance of the random distribution of the estimate. Then, in a graph, draw the mathematical expectation values ​​according to the number of samples, then for each data on the graph, specify the 95% confidence interval of the data with a vertical line. Was the hypothesis we proposed confirmed? If the answer is negative, check why this is the case. </p>

<p align="justify"> As it is known, by plotting the graphs, it can be seen that the uncertainty of the estimate will decrease as the value of n increases. This is because the more samples we take, the more chances we have to get the true value of the desired parameter. </p>

![image](https://github.com/SogolGoodarzi/Estimation-of-Euler-number-by-Monte-Carlo-method/assets/125180530/9bdecdd3-5dd1-4e2b-b984-a21279998e44)

![image](https://github.com/SogolGoodarzi/Estimation-of-Euler-number-by-Monte-Carlo-method/assets/125180530/bd7dddcc-fbb3-43ad-a5ac-344f4f8d8171)
