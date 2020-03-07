---
layout: post
title:  "Flan Deep Dive"
date:   2020-02-13 13:20:00 -0800
categories:
---
Flan Deep Dive



Notes:
    Flan ingredient decomposotion and assesment of importance / influence / bounds
        - Milk
        - Milk solids (evaporated milk)
        - Cream
        - Eggs (white vs yolk)
        - Sugar
        - Acid (??)
    Evaluation of flan recipes in this context (Bayless, etc.)
        - Light (milk rather than evaportaed milk, less cream)
        - Medium creamy (replace milk with evaporated milk)
        - Rich and creamy (evaporated milk and more cream)
        - I can think of no good reason to have both sweetened condensed milk and evaporated milk in a recipe -- very redundant.
    Flan recipe calculator (sliders for creamy, rich, sweet, quantity, etc.)
        - Slider from light -> medium -> rich and creamy as above.  Is there any other obvious direction to go as far as sliders are concered?
        - Definitely could have slider for sweetness (lower/upper bound being limit of acceptable sweetness).
        - Slider for yield.
        - Cream content should really be correlated with milk solid content.  Only reason they would be separate is if you didn't want to bother
          with obtaining evaporated milk.
        - We should be able to determine whether egg yolks are better than whites or not, or best together.  Maybe egg whites are more
          appropriate for light textured flan, while egg yolks are better for rich flans.  Lightest flan might be milk, egg white, sugar;
          richest evaporated milk, cream, egg yolk.
        - Perhaps recipe general template may look something like:
            - x g Milk (evaporation %)
            - x g Cream (0 -> Milk amount)
            - x g Egg                       egg: below richness threshold, only add egg for egg portion
            - x g Egg yolk                  egg yolk: above richness threshold, only add egg yolk for egg portion
            - x g Sugar                     sugar = sweetness * yield
    Flan cooking methods
        - Oven: baked in water bath (classic)
        - Stove: steamed
        - Stove: water bath
        - Immersion circulator
        - Smoker / grill
        - Stove top: stirred to completion
    Flan flavor variation (how to modify to create interesting flavors)
        - Alternative milks (e.g. coconut)

    Need to try still:
        - try with all evaporated milk vs evaported milk + cream (test cream influece compared to evap milk)
        - try with whole egg vs only egg yolk (or egg white vs egg yolk)
        - try with small amound of acid (lemon juice) vs without
        - try simplest / lightest possible flan and heaviest / richest possible flan (max/min bounds on scale)


Lemon Pot de Creme recipe:
1 C cream
2 T honey
1 T sugar
1/2 T lemon zest
dash salt
4 egg yolks (could have done about 3 maybe)
2 T lemon juice

Lemon juice was whisked in at the end, and this was baked.  Texture was really nice in the end,
and quite firm, not curdled at all.

The Takout flan:
50 g sugar
150 g caramelized evaporated milk
150 g cream
75 g egg yolk
0.5 # vanilla bean
(non egg mass = 350 g)
(egg ratio: 0.197)

My flan recipe (as of 2/13/20):
14 g egg white
55 g egg yolk
98 g cream
121 g milk
43 g cajeta
23 g sugar
(non egg mass = 285)
(egg ratio: 

Steam lightly at around 180F steam temp for ~ 1 hour.

I'm inclined to return to sugar rather than cajeta -- simplify. Could play with condensation ratio, milk vs cream ratio, egg yolk vs white ratio, and total egg ratio, and inclusion of acid / culturing (via lemon juice or cultured cream / cream cheese, etc).  Let's try:











You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

Jekyll requires blog post files to be named according to the following format:

`YEAR-MONTH-DAY-title.MARKUP`

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `MARKUP` is the file extension representing the format used in the file. After that, include the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
