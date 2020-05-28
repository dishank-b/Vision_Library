# Variational Inference

### Summary 

Variational Inference allow us to re-write statistical inference problems \(i.e. infer the value of a random variable given the value of another random variable\) as optimization problems \(i.e. find the parameter values that minimize some objective function\)

When you have intractable probability distribution $$p$$. Variational techniques will try to solve an optimization problem over a class of tractable distributions Q in order to find a q ∈ Q that is most similar to p.

For example, we can use **KL divergence** between $$p$$ and $$q$$, so that $$q$$ will be approximate to $$p$$ which intractable, hence we can use $$q$$ in place of $$p$$. 

$$
KL(q||p) = \sum_x q(x)\log \frac{q(x)}{p(x)}
$$

### Probabilistic Model

Let's say you have some  data denoted by a random variable $$X$$. $$X$$is basically your observed \(I will explain what's meant by observed\) variable. Now we believe that there is some random variable $$Z$$which is responsible for generating $$X$$, but  $$Z$$is hidden/latent i.e. we don't have any information about $$Z$$directly. The idea of **latent variable** is basically _our belief_ of having a _hidden factor_ $$Z$$ behind generation of our data $$X$$.

Let's take an example of a factory that manufacture boxes. Now we have  dataset of number of boxes generated by the factory each day over the year. This is our observed variable $$X$$. Why is this called observed variable? Because we have observed this i.e it's given. Now if $$X$$is observed, then something must be not observed in contrast, else why would be specifically call it observed. 

Now think of factors that can affect $$X$$ i.e number of boxes produced in a day. There can be multiple factors which influence $$X$$such as number of workers on that day, number of machines operating that day, morale of workers that day, etc. Let's take random variable $$Z$$which is number of machines working on a day. Now one things to understand is that $$Z$$influence $$X$$, more number of machines working then more number of boxes produced. But the things is that we don't have any data regarding $$Z$$, that's the reason that $$Z$$is called **hidden/latent variable.**  

![](../.gitbook/assets/image%20%28152%29.png)

### What we want to achieve?

We want to infer about latent/hidden variable $$Z$$given the variable $$X$$. We want to find how many machine would have been working on some day if I know number of boxes produced that day. 





### Resources

* [https://dasayan05.github.io/blog-tut/2019/11/20/inference-in-pgm.html](https://dasayan05.github.io/blog-tut/2019/11/20/inference-in-pgm.html)
* [https://www.cs.princeton.edu/courses/archive/fall11/cos597C/lectures/variational-inference-i.pdf](https://www.cs.princeton.edu/courses/archive/fall11/cos597C/lectures/variational-inference-i.pdf)
* [https://blog.evjang.com/2016/08/variational-bayes.html](https://blog.evjang.com/2016/08/variational-bayes.html)
