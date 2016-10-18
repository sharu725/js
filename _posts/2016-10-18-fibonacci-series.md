---
layout: post
title: Fibonacci on first try!
permalink: /fibonacci-series-js/
---

I'm very impressed by the ways suggested by Josh Kaufman to learn anything in 20 hours. He says we can become good at anything in just 20 hours. Well, this actually is a far fetched statement in case of JavaScript. 

He explains that you should try simple things right away. I thought I will give it a try! Watch the video at the end to know more.

So I know a little of JavaScript already. By little I mean variables, functions, loops etc., These are very basic things you should know in any programming language.

## So what is Fibonacci series?
It is a series of numbers generated by adding a number and its previois number. That's it. It needs two numbers to start off with. 

```0, 1, 1, 2, 3, 5, 8, ...```

This can start from any two numbers

```2, 4, 6, 10, 16, 26, ...```

I chose 3 and 4. Now, I will be generate first 100 Fibonacci numbers.

## Brainstorm

The data is pretty straight forward. I have two numbers, I have to add them to get the 3rd number. Then add the 3rd and 2nd number to get the 4th number and so on.

```3, 4, 7, 11, 18, 29, ...```

How may variables should I use? I must use 2. May be one more to hold the sum of these two.

So initially we have,

**x = 3**

**y = 4**

the sum of these 

**z = x+y**

We got the third number in the series. Now for fourth number, we should add **y** and **z**. We can actually loop this process.

Once we get **z** in the last process, assign 

**x = y**

**y = z**

This way the next addition 

**x+y** is actually **y+z**.


So the complete code with for loop looks like

{% highlight html %}
<!DOCTYPE html>
<html lang="en">
<body>
   <script>
   
   // Initial values
    var x = 3;
    var y = 4;

       // Calculating for 100 terms
       for(i=0;i<100;i++){
           
           z = x + y;
           
           // Output with a break to get the numbers in a table
           document.write(z + "<br />");
           
           // Assigning x to y and y to z for next fibonacci number in the next loop
           x = y;
           y = z;
       }
    </script> 
</body>
</html>
{% endhighlight %}

I came up with this code because this is how I used to do it in C in college. There can be a better way to do this but I wanted to come up with my own code. Not to copy from anywhere. Let me know if there's an easier way.

Output

{% highlight html %}
7

11

18

29

47

76

123

199

322

521

843

1364

.

.

.

3.3552659205930536e+21
{% endhighlight %}


<br />



<iframe class="video" src="https://www.youtube.com/embed/5MgBikgcWnY?rel=0" frameborder="0" allowfullscreen></iframe>

Thanks for reading!