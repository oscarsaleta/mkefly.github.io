---
layout: home
title: Home
landing-title: 'COVID-19 Statistics and Research'
description: 'This website aims to help increase the public’s understanding of the evolving COVID-19.'
image: null
author: 'Miquel Oliver & Xisco Jimenez Forteza'
show_tile: true
---  
<!-- Main -->
<div id="main">
    <div class="image">
        <img src="{% link assets/images/Sigmoid-simulation-linear.png %}" alt="" data-position="center center" width="100%"/>
    </div>
        <div class="row top-buffer1"></div>
<p>In this figure we compare the current number of COVID-19 fatalities to date shown with color dots, with the multiple projections drawn from the posterior predictive distribution; these projections are shown as faint solid lines (note that the more lines we have the more likely that path will be). We have defined the zeroth time for each country to the day they announced their first fatality record. The vertical grid lines represent important events that may have affected the growth rate such as the separate lockdowns (LD) applied by China, Italy and Spain. Note that all curves have been drawn from a <a data-scroll href="#logistic">logistic model</a> and predict the <code># fatalities (N)</code> for each country analysed here.</p>
    <div class="image">
        <img src="{% link assets/images/Sigmoid-simulation-log.png %}" alt="" data-position="center center" width="100%"/>
    </div>
    <div class="row top-buffer1"></div>
            <p>This figure shows the same results as the previous one but now we have changed the <code>Total # of deaths</code> axis to a logaritmic scale. This generates a visual straight line at the begining of the outbreak and it "bends down" as it surpasses the inflexion point; this point corresponds to the moment for which the evolution or the growth starts to slow down. Note that our estimates are consistent with a total number of deaths within [2000, 6000] for all countries. These estimates could vary with any relaxation of the measures each country takes.</p>
</div>

<!-- Two -->
<h4>Estimated end & the number of fatalities:</h4>
<div class="row">
  <div class="column">
            <img src="{% link assets/images/daystoend.png %}" alt="" data-position="center center" width="100%"/>
            <p>Marginalised probability distribution on the number of estimated number of deaths by the end of the outbreak's date, when a country arrives to the flat zone i.e. when the number of deaths per day tends to zero. As we can see in the figure China has already surpassed that point. Remember that the zero in this case corresponds to the latest update and the highest point in the bulb of the distributions is the most likely date for the outbreak to finish.</p>
  </div>
  <div class="column">
        <img src="{% link assets/images/fatalities.png %}" alt="" data-position="center center" width="100%"/>
        <p>Marginalised probability distribution on the estimated number of deaths. The prediction for China agrees with the 3226 cases reported at 17/09/2020. These cases must be taken as a lower limit to the death estimate number. Any non-expected reburst of the curve make increase the number of cases. An strict confinement of the population is therefore essential.</p>
  </div>
</div>


<section id="one">
    <div class="inner">
        <h3>The Data:</h3>
    </div>
    <p>On the table below we show the COVID-19 data collected for the set of countries with at least one fatality. We show the number of deaths in each country (<code># of deaths</code>), the number of days since the first official report of death (<code># days</code>), the growth rate that reflects the percentual increase of the deaths in that day i.e. <em>(Today-Yesterday)/Yesterday x 100</em> and the growth factor we will discuss more about it in a future section. Finally the growth factor (<code>GF</code>) is represented as <em>(Today-Yesterday)/(Yesterday-Day before)</em> i.e. the quotient of todays and yesterdays derivatives.</p>
    <div class="row top-buffer"></div>
    <div w3-include-html="./assets/tables/tabledata.html"></div>
    <script>
    includeHTML();
    </script>
</section>


<!-- Two -->
<section id="two" class="spotlights">
    <section>
        <div class="content">
            <img width="350" src="{% link assets/images/pic08.jpg %}" alt="" data-position="center center" />
        </div>
        <div class="content">
            <div class="inner">
                <header class="major">
                    <h3>JHU CSSE repository</h3>
                </header>
            </div>
            <p>The data used in this repository comes from the Johns Hopkins University Center for Systems Science and Engineering (JHU CSSE) repository devoted to the 2019 Novel Coronavirus Visual Dashboard operated.</p>
            <div class="row">
                <div class="col-md-6">
                    <ul class="actions">
                        <li><a href="https://github.com/CSSEGISandData/COVID-19" class="button">Repository</a></li>
                    </ul>
                </div>
                <div class="col-md-6">
                    <ul class="actions">
                        <li><a href="https://www.arcgis.com/apps/opsdashboard/index.html#/bda7594740fd40299423467b48e9ecf6" class="button">Dashboard</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
</section>


<div class="row top-buffer"></div>

<section id="three">
    <section>
        <div class="inner">
            <header class="major">
                <h3>The death evalution simulations:</h3>
            </header>
        </div>
        <div id="logistic"></div>
        <h3>Exponential & logistic growth</h3>
        <p>A population will grow its size according to a growth rate. In the case of exponential growth this rate stays the same regardless of the population size, inducing the population to grow faster and faster as it gets larger, without an end.</p>
        <ul>
            <li>In nature, populations can only grow exponentially during some period, but inevitably the growth rate will ultimately be limited for example by the resource availability.</li>
            <li>In logistic growth, the population growth rate gets smaller and smaller as population size approaches a maximum. This maximum is in esence a product of over population limiting population's resources.</li>
            <li>Exponential growth produces a J-shaped curve, while logistic growth produces an S-shaped curve.</li>
            <li>When we read about bending the curve we are talking about using a logaritmic scale to plot the data, in that case that J-shaped curve becomes a straight line. The moment when this straight line bends downwards we start seeing the limiting factors and we are close to the center of the S-shaped curve, that in this case looks like an inverse J-shape. (Remember this is only a matter of how the data is plotted or shown, it does not affect the data itself).</li>
        </ul>        
        <h5>*Text from: <a href="https://www.khanacademy.org/science/biology/ecology/population-growth-and-regulation/a/exponential-logistic-growth">khanacademy</a>*</h5> 
        <p>In theory, any kind of organism could take over the Earth just by reproducing. For instance, imagine that we started with a single pair of male and female rabbits. If these rabbits and their descendants reproduced at top speed ("like bunnies") for 777 years, without any deaths, we would have enough rabbits to cover the entire state of Rhode Island. And that's not even so impressive – if we used E. coli bacteria instead, we could start with just one bacterium and have enough bacteria to cover the Earth with a 111-foot layer in just 36 hours!</p>

        <p>As you've probably noticed, there isn't a 111-foot layer of bacteria covering the entire Earth (at least, not at my house), nor have bunnies taken possession of Rhode Island. Why, then, don't we see these populations getting as big as they theoretically could? E. coli, rabbits, and all living organisms need specific resources, such as nutrients and suitable environments, in order to survive and reproduce. These resources aren’t unlimited, and a population can only reach a size that match the availability of resources in its local environment.</p>

        <p>Population ecologists use a variety of mathematical methods to model population dynamics (how populations change in size and composition over time). Some of these models represent growth without environmental constraints, while others include "ceilings" determined by limited resources. Mathematical models of populations can be used to accurately describe changes occurring in a population and, importantly, to predict future changes.</p>    
<div class="text-align">
    <img src="{% link assets/images/cartoon_exp_log.png %}" alt="" width="950"/>
    <p>*end of the <a href="https://www.khanacademy.org/science/biology/ecology/population-growth-and-regulation/a/exponential-logistic-growth">khanacademy</a> citation*</p>
</div>
        <p>The figure above shows how the logistic and exponential models are constructed; to underestand them better you can watch the video  <a data-scroll href="#bazinga">"Exponential growth and epidemics"</a> bellow.</p> 
        <p>After reading this text it should be obvious to us that the growth of the virus cannot be exponential indefinitely but it has to flatten at some point. One of these functions is the logistic model, used here to predict the number of deaths. </p>
        <h3>The logistic function:</h3>
        <p>If we solve the equation on the right of the previous figure, we obtain the logistic function. A logistic function or logistic curve is S-shaped. This type of curve is known as a sigmoid and its equation is as follows:</p>
        $$N(t) = \frac{K}{1 + e^{-r(t-t_0)}}.$$
        <ul> 
            <li> $e$ = the natural logarithm base (also known as Euler's number),</li>
            <li> $t_0$ = the $t$-value of the sigmoid where the rate starts to decrease, the midpoint of its evolution and the 'inflexion point' of the sigmoid's curve.</li>
            <li> $K$ =the curve's maximum value; in this case the maximum number of deaths.</li>
            <li> $r$ = the logistic growth rate or steepness of the curve</li>
        </ul>   
        <h3>Simulating possible future scenarios:</h3>
        <p>The logistic model defined above and a non negative binomial distribution as likelihood, to obtain the posterior predictive distribution of our model; from which we will sample to generate new data based on our estimated posteriors. (Please do not get disturbed by this, if you want to have a rough idea of the concep behind all this go lower to the video title "The Bayesian Trap" by Veritasium).</p>
        <p>The figures shows, considering these dataset and our model, the predicted evolution of the curves that is expected to be observe. Note that the predictions have the uncertainty into account. Meaning that in the cases where few data points are availeble the uncertainty grows i.e. the spam of the predictions.</p>   
        In short, the figures we shows that given the data and our model, what evolutions are expect to be observe. Note that the predictions have the uncertainty into account. This implies that for the cases where few data points are available this uncertainty grows.     
    </section>
</section>

<!-- Two -->
<div class="row">
  <div class="column" style="background-color:#2d3450;">
    <header class="major">
        <h3>Exponential growth and epidemics:</h3>
    </header>
                    <p>While this video uses COVID-19 as a motivating example, 
                    the main goal is simply a math lesson on exponentials 
                    and logistic curves.</p>
                    <div id="bazinga"></div>
                    <p>by 3Blue1Brown</p>
                    <ul class="actions">
                        <li><a href="https://www.youtube.com/channel/UCYO_jab_esuFRV4b17AJtAw" class="button">Go to their channel</a></li>
                    </ul>

  </div>
  <div class="column" style="background-color:#2d3450;">
                    <iframe width="100%" height="100%" src="https://www.youtube.com/embed/Kas0tIxDvrg" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>
</div>

<div class="row top-buffer"></div>
<div class="inner">
    <header class="major">
        <h3>Posterior parameters:</h3>
    </header>
</div>
<div class="text-fixed-left">
    <p>Here we show the results of the Bayesian inference parameter estimation. Our goal is to show the inferred probability distributions over the model parameters of interest, the probabilities of models and the probability distributions over predicted data.</p>
    <p>This is a universal approach for fitting models to data. We have defined the generative model for the data, the likelihood function, and a prior distribution over the parameters.</p> 
    <p>The following figures show the results:</p>
    <img src="{% link assets/images/parameters-c1-c2.png %}" alt="" data-position="center center" width="95%"/>
    <p>In this figure we show the results obtained from the posterior i.e. the most likely scenarios given our current model. We show the results for the growth rate value in terms of the total number or deaths predicted by the logistic curves for all the countries.</p>
</div>
<div class="text-fixed-left">
    <img src="{% link assets/images/parameters-c3-c1.png %}" alt="" data-position="center center" width="95%"/>
    <p>In this figure we show the results obtained for the 'Inflexion day' in terms of the total growth rate; note that the end of the outbreak is simply the double of the 'Inflexion day'.</p>
</div>
<div class="text-fixed-left">
    <img src="{% link assets/images/parameters-c3-c2.png %}" alt="" data-position="center center" width="95%"/>
    <p>Figure for the 'Total number of deaths' and the 'Inflexion day'.</p>
</div>
<div style="overflow: auto; width:100%;">
    <div w3-include-html="./assets/tables/bay_summary.html"></div>
</div>
<div class="row top-buffer"></div>

<div class="row">
  <div class="column" style="background-color:#2d3450;">
    <header class="major">
        <h3>The Bayesian Trap:</h3>
    </header>
                <p>Bayes' theorem explained with examples and implications for life.</p>
                <p>by Veritasium</p>
                    <ul class="actions">
                    <li><a href="https://www.youtube.com/channel/UCHnyfMqiRRG1u-2MsSQLbXA" class="button">Go to their channel</a></li>
                    </ul>

  </div>
  <div class="column" style="background-color:#2d3450;">
            <iframe width="100%" height="100%" src="https://www.youtube.com/embed/R13BD8qKeTg" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>
</div>

<!-- 
<div class="row top-buffer"></div>
<div class="inner">
    <header class="major">
        <h3>Posterior parameters:</h3>
    </header>
</div>
<div class="text-fixed-left">
    <p>....</p> 
    <p>The following figures show the results:</p>
    <img src="{% link assets/images/Growth-China.png %}" alt="" data-position="center center" width="95%"/>
    <p>.............................................................................</p>
</div>
<div class="text-fixed-left">
    <img src="{% link assets/images/Growth-Iran.png %}" alt="" data-position="center center" width="95%"/>
    <p>.............................................................................</p>
</div>
<div class="text-fixed-left">
    <img src="{% link assets/images/Growth-Italy.png %}" alt="" data-position="center center" width="95%"/>
    <p>.............................................................................</p>
</div>
<div class="text-fixed-left">
    <img src="{% link assets/images/Growth-Spain.png %}" alt="" data-position="center center" width="95%"/>
    <p>.............................................................................</p>
</div>
<div class="row top-buffer"></div> -->
