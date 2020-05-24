 <p align="center">
<img src="Pictures%20and%20Graphs/First_page.png" > 
 </p>

Table of contents
-----------
1. [ Preface ](#desc)
2. [ Descriptive Analysis ](#usage)
3. [ Association Rules ](#usag)
4. [ Self-Organising Maps ](#usa)
5. [ Casual Model(Logit) ](#us)
6. [ Classification Models and Profit Lines](#u)


<a name="desc"></a>
Preface
-----------
<p align="justify">
The primary aim of this text is to analyze the behavior of holders of the museum card in 2013, focusing on the underlined dynamics and quantitative relationships.
The single subscription, as internet domain reported, has its origin in 1995 with a beginning valid ticket in 4 Civic museums. Since the first year of experimentation, the affiliated museum sites have been implemented, offering increasing opportunities and focusing on the "cherz-soi" tourist experience, through a continuous updating of the cultural landscape. The real growth in numerical terms, not without stationary periods, is attested starting from 2003 (going from 30,000 units up to over 100,000 in 2014), until representing up to 12% of the total number of visits. This market did not experience relevant slowdowns- due to the economic crisis- and it has been constantly modernized thanks to frequent qualitative and quantitative surveys.
Descriptive analysis, random and predictive modeling are the means by which this report will focus on card renewal.
</p>

<a name="usage"></a>
Descriptive Analysis
------------------
<p align="justify">
The research has been carried out using 3 main datasets broadly showing personal data, information about the visits for each ID, the amounts paid and related discounts and furthermore the ID renewal.
In addition to these socio-demographic variables (already included in the reference datasets) to highlight further relationships, the following variables have been generated:

* _count_: number of total visits for each subscriber;
* _numero_ingressi_unici_: indicator of entrances to different museums for each visitor;
* _costi_entrate_: sum of the total cost that each visitor would have had to pay if he had not been a card holder; 
* _some geographical dummies_ to break down the territorial effect to live in the Center of Turin, in the first belt, in the second one and in the rest of the Northern Italy.

Moreover, thanks to the study of the consumers’ joint visit through the association rules, it has been possible to consider in the descriptive analysis, **the number of visits that each individual has made at least with another person (binding no less than two shared entries), the average number of people with whom each member has shared an exhibition visit and finally the number of different people with whom each subscriber has logged in**. One of the first studies carried out, in terms of descriptive analysis, is related to the renewal by gender and age.
</p>

 <p align="center">
<img src="Pictures%20and%20Graphs/Distribution%20of%20the%20renewal%20variable%20(si2014)%20by%20gender.png" > 
 </p>

<p align="justify">
Taking into account the first two levels of the variable, there is a slight difference in terms of relative frequencies: in particular in this sample, the frequency of women who renew is around 70% while it is of 69% for men. The third column shows the units for which there is no answer linked to the gender variable and it allows us to reject the hypothesis of a link between NA and the renewal by sex variable, since the distribution seems to be similar to the other columns.
</p>

 <p align="center">
<img src="Pictures%20and%20Graphs/Distribution%20of%20the%20renewal%20variable%20(si2014)%20by%20age.png" > 
 </p>

<p align="justify">
On the other hand, the differences in terms of age between those who renew the subscription and those who do not, are more marked; indeed the average age of the former seems to be greater, suggesting therefore that the renewal tends to be more frequent in older subscribers.
Therefore, unlike gender, it can be concluded that the age variable differs significantly between the two groups.
</p>

 <p align="center">
<img src="Pictures%20and%20Graphs/Distribution%20of%20the%20renewal%20variable%20by%20residence%20variable%20levels.png" > 
 </p>
 
<p align="center"><table style="border-collapse:collapse;border-spacing:0" class="tg"><thead><tr><th style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;font-weight:bold;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Areas</th><th style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;font-weight:bold;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">N° people who churn</th><th style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;font-weight:bold;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">N° people who renew</th></tr></thead><tbody><tr><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;font-weight:bold;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Torino</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal">11291</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal">29893</td></tr><tr><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;font-weight:bold;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Cintura1</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal">5415</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal">11489</td></tr><tr><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;font-weight:bold;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Cintura2</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal">2075</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal">4040</td></tr><tr><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;font-weight:bold;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Altrove</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal">4914</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal">8596</td></tr></tbody></table></p>
 
<p align="justify">
The bar chart above shows how the distribution of renewals varies by geographic area: thus, the more one gets away from the City of Turin, the more the relative churn frequencies tend to increase. To enrich this study the adjacent table is reported in absolute terms and it shows that the largest number of members who renew the card comes from the capital of Piedmont and that the two “belts” together have the largest number of renewals of the rest of Northern Italy.
These two analyses, taken together, highlight the relevance of this variable for the purpose of this report.
</p>

 <p align="center">
<img src="Pictures%20and%20Graphs/Distribution%20of%20the%20number%20of%20visits%20for%20each%20ID%20comparing%20those%20who renew%20and%20churn.png" > 
 </p>

<p align="justify">
The density curves show how the relative distribution of the number of visits differs between people who renew their subscription compared to those who churn. It can be predictably assumed that the number of visits influences positively the probability of renewal (re-subscription card).
 </p>
 
 <p align="center">
<img src="Pictures%20and%20Graphs/Distribution%20of%20the%20cumulative%20entry%20cost%20for%20each%20id%20by%20comparing%20those%20who%20renew%20and%20churn.png" > 
 </p>

 <p align="justify">
 A similar interpretation is applicable to the amortization of the subscription cost, since the number of entries is highly correlated with the total cost of visits.
The variable highlights the costs that would have been incurred if the visitors had not subscribed the museum card.
</p>

 <p align="center">
<img src="Pictures%20and%20Graphs/Distribution%20of%20discount%20variable%20by%20renewal%20(2014).png" > 
 </p>
<p align="justify">
The above bar chart shows the discount variable, at first defined by 24 levels and, for clarity, here coded as a dummy; in detail it is clear that the proportion of withdrawals among those who have not received any discount or reduction on the subscription price is significantly higher if compared to the respective proportion of subscribers with discount rights.
</p>


 <p align="center">
<img src="Pictures%20and%20Graphs/Weekly%20frequency%20of%20entries%20for%20renewal%20and%20churn.png" > 
 </p>
 
<p align="justify">
The distribution of visits does not seem to differ on weekdays between those who renew and do not: however there is a slight variation on weekends and in particular those who renew the subscription tend to visit more museum sites on weekends with significant distribution on Fridays and Saturdays (in addition to differing even on less common days such as Wednesdays and Thursdays in favour of those who renew the card). 
</p>

<img src="Pictures%20and%20Graphs/Representation%20of%20the%20territorial%20distribution%20of%20museum%20card%20holders%20in%20Northern%20Italy.png" width="520" height="400"/> <img src="Pictures%20and%20Graphs/Representation%20of%20the%20territorial%20distribution%20of%20museum%20card%20holders%20in%20the%20city%20of%20Turin.png" width="350" height="300"/> 

<p align="justify">
A quick inspection of the distribution by Cap of the subscribers allows us to conclude that this effect can be analyzed especially in the Turin hinterland and, for this reason, we focus on the Turin Cap because of the highest number of members. The most numerous members are concentrated in the Mirafiori area (North), Borgo San Paolo and Pozzo Strada. It is curious to note that the most central areas such as San Donato and Quadrilatero, despite their great proximity to the museum sites, in absolute terms show the lowest number of members.
</p

<p align="center">
 <img src="Pictures%20and%20Graphs/Territorial%20distribution%20of%20cumulative%20entries%20for%20Turin%20cap.png"> 
</p>


<p align="justify">
The map of the province of Turin shows the number of cumulated entries per Cap and it seems to fit perfectly with the previous results. It can therefore be concluded that the areas with the highest number of members are also those with the highest number of cumulative visits. The reading that I want to deepen now is how to distribute the relative frequencies of churn and in particular if the areas with fewer visits and members are also those with higher probability of churn.
</p>

 <p align="center">
<img src="Pictures%20and%20Graphs/Distribution%20of%20churn%20relative%20frequencies%20in%20Turin.png" height="300"> 
 </p> 
 

 
| Cap   	| Number of card owners 	| Number of renewal 	| Prob. of churn 	|
|-------	|-----------------------	|-------------------	|----------------	|
| 10151 	| 703                   	| 482               	| 0.3143670      	|
| 10148 	| 435                   	| 294               	| 0.324138       	|
| 10131 	| 886                   	| 692               	| 0.218961       	|
| 10145 	| 615                   	| 468               	| 0.239024       	|



<p align="justify">
This assumption is even confirmed if we consider the centre-north areas, such as Barriera di Milano, Borgo Vittoria, San Salvario and Quadrilatero; the highest rate of dropp off is seen here. Borgo Po and Campidoglio are, on the contrary, the areas with the lowest probability; this result, unlike what could be suggested, does not only depend on the absolute number of members (as can be seen from the adjacent comparative table). The four areas listed above are the most likely to churn and renew with the respective number of members. It is noteworthy that the areas closest to the museum sites show the highest number of abandonments too, despite the fact that these are the zones with the highest real estate evaluation per square meter (although weak, this is the only proxy for income, given that the profession variable is not usable).
</p>

<a name="usag"></a>
Association Rules
-----------
<p align="justify">
The second part of this descriptive analysis focuses on the study of the association rules in order to understand if there may be a relationship between subscribers visiting together the museum and then highlight if there are any potential relationships between museum sites visited. The graph depicting the members shows the first 100 rules, sorted according to "confidence", and mainly including relationships undertaken between two or three units.
For explanatory and interpretative clarity, the attention may be focused on the adjacent graph (figure 11.a) and in particular, considering the rhomboid association with the ID "33666" and "144932", it can be seen that the remaining vertices indicate the rules "to have entered in more museums together with a few minutes away".
Unlike other rules, this connection is bidirectional and can be interpreted with the fact that ID "33666" has always entered the museum with ID "144932" and vice versa. Similarly, if we consider the two nearby nodes with ID "265598" and "135859", we can quickly conclude that the first individual went to the museum at least one time without the second person.
In line with this study, computing the list of all accesses per museum-date-every 5 minutes, the following indicators were evaluated: the number of shared entrances, the average number of people with whom card holders entered and finally the different number of accompanying people.
</p>

<img src="Pictures%20and%20Graphs/Representation%20of%20the%20card%20holders%20network.png" width="520" height="400"/> <img src="Pictures%20and%20Graphs/Zoomed%20figure.png" width="350" height="300"/> 

 <p align="center">
<img src="Pictures%20and%20Graphs/Distribution%20of%20the%20number%20of%20different%20people%20who%20shared%20visits%20by%20renewal (si2014).png" > 
 </p> 
 
<p align="justify">
It is noteworthy that the greater is the number of distinct people with whom all visits have been shared, the greater is the frequency of renewals compared to those who churn. The most interesting aspect that emerges is that those who churn are accompanied by a number of different people on average lower, suggesting that the variable in question, may have a negative effect on the probability of abandoning. It can probably be interpreted with the fact that the greater is the number of people with whom one shares a passion for art or cultural visits, the greater is the stimulus received to renew the subscription.
Moreover, according to the average age of those who go to the museum with a smaller number of people, on average it appears that they are older than those who share visits with a larger number of distinct people.
This second analysis, carried out through the Market Basket Analysis, first focuses on considering which are the most visited museums (in particular for three of them, it will be investigated
where went people who visited a particular site).
</p>

 <p align="center">
<img src="Pictures%20and%20Graphs/%20Infographic%20representing%20the%20twenty-five%20most%20visited%20museums%20in%202013%20by%20subscribers.png" > 
 </p> 
 
 <p align="center">
<img src="Pictures%20and%20Graphs/Representation%20of%20Museo%20Egizio,%20Reggia%20di%20Venaria%20Reale%20and%20Royal%20Palace%20network.png" > 
 </p>  
 
Most of the reported "rules” highlights visits to close-located museums, especially in the Centre of Turin. Unfortunately, it cannot be understood whether this is an effect linked to individual thematic preferences or simply a proximity effect.

<a name="usa"></a>
Self-Organising Maps
-----------
<p align="justify">
The last methodology that will be used for our descriptive purposes is a non-parametric model with unsupervised learning: the Self-Organising Maps. The iterative algorithm has the ability to capture, through a two-dimensional neuronal structure, the non-linear relations between variables keeping however the topological order.
The aim of implementing Self Organising Maps in this context is to be able to segment consumers <a href="#note1" id="note1ref"><sup>1</sup></a>, verifying whether the first relationships, detected at the descriptive level, can be confirmed. To obtain a sufficient degree of convergence 1000 interactions were chosen and a number of clusters equal to 4 was assumed. Being an unsupervised learning model, this preference was made on the basis of graphic considerations (codes), together with the outcome of the Ward method.
</p>

 <p align="center">
<img src="Pictures%20and%20Graphs/Counts%20and%20Neighbor%20distance%20plot-first%20graphical%20analysis.png" > 
 </p>  
 
<p align="justify">
 
The graph shows the number of observations "captured" by each neuron and the areas with higher density. In this case the map is a 20x20 grid and, as can be inferred from the adjacent coloured scale; thicker areas are more frequent in the left area and, in particular, the empty neurons (in grey tones) graphically tend to delimit the distinct areas.
Linked to this graph, the "U-matrix" is analysed with the intent of showing the distance between the identified neurons. In particular, it is evident that there are two well-defined and clearer areas; so that you can at least consider two groups, whose deep colour is inversely proportional to the distance.
</p>

 <p align="center">
<img src="Pictures%20and%20Graphs/Codes%20plot%20and%20Clusters-second%20graphical%20inspection.png" > 
 </p>  
 
<p align="justify">
Furthermore the observation of the codes also let us identify some other areas (in addition to the two main ones highlighted by the "U-matrix") in line with what examined in the count plot. Moreover, it is possible to catalogue 4 clusters whose relevant characteristics have to be examined, for a hermeneutical interpretation, both with regard to the variables considered in and out the algorithm.
</p>

 <p align="center">
<img src="Pictures%20and%20Graphs/Comparison%20between%20clusters%20by%20discount%20and%20number%20of%20visits.png" > 
 </p>  
 ...
 
 <p align="center">
<img src="Pictures%20and%20Graphs/Comparison%20between%20clusters%20by%20gender%20and%20churn.png" > 
 </p>  


<p align="justify">
From this first comparative analysis is evident that the fourth cluster effectively manages to capture those who do not renew the subscription. Now the interest is to understand if this identified group shows different characteristics for the other variables. Sex seems to be more or less uniform as tendency among the clusters; in all groups women prevail and thus, at first glance, it is not possible to identify a clear relationship.
</p>

 <p align="center">
<img src="Pictures%20and%20Graphs/Comparison%20between%20clusters%20by%20living%20in%20Turin%20and%20Age.png" > 
 </p>  

<p align="justify">
Taking into account these graphical representations, we may formulate a definition of the obtained clusters:
 
* __First cluster__: mainly contains residents of Turin with higher average age, average number of visits and average number of discount receivers. The index variable (average number of people with whom they entered) is also higher than all the other groups analyzed.

* __Second cluster__: has a majority of non-residents in Turin. It does not differ from the first one in proportion to people who received discounts and to the average age. The variable “average number of people” does not seem to differ from the remaining groups.

* __Third cluster__: it tends to be composed by a large proportion of Turin City inhabitants, mainly women, although this is the group with the highest proportion of men. The average age and number of visits are lower than those of the previous clusters.
* __Fourth cluster__: Mainly non-resident subjects in Turin, with number of visits and average age lower than all the other clusters. The majority of these individuals did not receive any discount.
</p>



<a name="us"></a>

Casual Model (Logit)
-----------

<p align="justify">
The aim of this section is not only descriptive but causal; the purpose is to identify the variables that can explain the renewal. The model used is “logit model” and employs, as outcome, the two-level qualitative explanatory "si2014". Among the estimated coefficients, "second belt" and “index” (average number of people who entered together for each ID) are not significant. Looking at the first picture, it can be inferred that the probability of renewal increases monotonically with the number of entries. The graph shows the differences between levels of the variable residence and gender too. Both for men and women, the probability of renewal is numerically decreasing by moving away from Turin - the levels "second belt" and "elsewhere", confirming what was previously presented, do not seem to be significantly different. The probability curves between the two sexes are parallel because the study of the interaction effects did not reveal any significant coefficient between residence and gender.
At the same level of residence women are more likely to renew than men - in line with what has been analyzed at the descriptive level - and in particular it is surprising that for all numbers of visits, women living in the rest of Northern Italy ("Elsewhere") are more likely to re-subscribe than men living in the different belts of Piedmont capital.
</p>


<p align="justify">
These further charts, supporting the causal study, show the effect of both the amount paid for the subscription and the age of the members. For the first variable, the change in the price of the card has almost a linear effect on the probability, with the greatest decrease of around 4%, ceteris paribus. Differently, the age determines a visibly non-linear effect, the increase in probability is significant between 20 and 50 years, while it is much more limited in the following years.
As already pointed out above, for these two variables there are no significant effects of interaction between gender and amount or gender and age (this consideration applies to the cap too).
</p>

<p align="justify">
To allow such an interpretation in terms of odds ratio, the coefficients are presented as arguments of an exponential function; this choice determines the fact that they are represented on a zero plus infinite scale and the effect is increasing or not depending on whether they are higher or lower than the unit. The coefficient higher than the unit means that the variable under examination has a positive effect on the probability of renewal. In particular, the explanatory with the greatest impact is "discount"; those who benefit from the discount more than double the odds. In addition to the considerations on the variable "number of entries", it results that the "number of shared entries" and the "number of different people" have a positive effect. Therefore It can be assumed that subjects who share a passion for art and exhibitions with a large number of people and do not go alone to the museums are more likely to renew; however, only one hypothesis is not fully supported by these data because, taking into account this sample, the number of people with whom one actually goes to the museum is not significant.
</p>

 <p align="center">
<img src="Pictures%20and%20Graphs/Graph%20showing%20the%20main%20odds%20ratio%20variables.png" > 
 </p>  


<a name="u"></a>
Classification Models and Profit Lines
------------------------


<p align="justify">
The intent of this last section of the report is to identify supervised learning forecasting models that can well foresee renewals. The dataset under study has been divided into training and test sets, with proportions 70-30.
Six models with the same variables and trained on the same “training set” are used; their performance is analyzed on the test set. To this end, are used two distinct approaches: the former of statistical nature, compares the models with classification measurements (including accuracy) while the latter is of a more economic nature. This last evaluation passes through the maximisation of profits, in the light of the costs of contacting consumers and the budget constraint set up for the direct marketing campaign.
A first statistical comparison will be based on the realization of confusion matrix taking into account the initial threshold of 0.5.
</p>
<p align="justify">
The two input tables compared show the above classes with actual values and then, given a threshold of 0.5, they will be used to estimate the accuracy of the models.
</p>
<p align="justify">
All values are above the "base-rate" of the dataset of 0.70: if all visitors had been placed in the renewal group it would have obtained a measure of accuracy of 0.70. Although these models pass a first inspection, the remaining fact is that this assessment is strictly bound to a threshold.
In order to overcome the problem, a representation in terms of Roc Curve is proposed, but it does not produce a model which totally dominates the others, and consequently let us identify the best model. These difficulties are added to the fact that, being an unbalanced distribution in the target population of si2014 variable (0.70-0.30), the measures may not be entirely reliable.
 
  <p align="center">
<img src="Pictures%20and%20Graphs/Roc%20Curves%20of%20the%20six%20models%20studied.png" > 
 </p>  

</p>
<p align="justify">
Taking into account these problems, there is a need for a study that can reconcile the necessity of defining the best model with contemporary considerating costs and profits. After the "training" has been carried out and the coefficients estimated, the same coefficients are applied to obtain a probability or score of renewal for each consumer. Each model will associate to the same person (with certain individual characteristics), a differing probability.
</p>

Figure 24 shows the cumulative profits, calculated using the following formula:
<p align="justify">
𝜋 =(𝑅 −𝐶𝑖/2)∗𝛾 −Χ
</p>
<p align="justify">
where 𝑅𝑖 indicates the revenue for the company Museums Subscriptions for each individual, 𝐶𝑖 are the costs for each individual, 𝛾𝑖 is the variable ditocomic "si2014" and finally Χ is the cost to contact members (the same for all subscribers).
The profits for each member will be ordered, and then accumulated, on the value of the expected profit. The only difference between expected and real profit-at a formulation level- is that the latter is calculated by replacing the variable si2014 (variable label) with the score previously obtained by each model.
The budget constraint placed at 5000 euros is represented with a vertical dotted line, and it is near this curve that it can be identified the model with the highest cumulative profit. Considering together the graph and the table, it can be inferred that the model with the best results is the Random Forest, generates a cumulative profit of 125834.2 compared to an expense of only 5000 euros.
 </p>

 <p align="center">
<img src="Pictures%20and%20Graphs/Profit%20Lines%20with%20cumulative%20profits%20sorted%20by%20expected%20profit.png" > 
 </p>  

In conclusion, a further robustness analysis has been proposed to validate the data obtained.
In particular, a problem related to the annuality of subscriptions is highlighted: the duration does not
coincide with the calendar year but it is valid for 365 days from the day of the activation. In quantitative
terms, this problem can be reflected by the observation of units only for short periods because of the
fact that they have renewed the subscription in the last months of the year. A few visits are attributed
to them, since the first months of 2014 do not appear.
In order to bypass the problem and hypothesizing a uniform distribution of visits over the year, the data
have been annualized <a href="#note2" id="note2ref"><sup>2</sup></a>. Finally the result confirms what has been argued so far, that is to say that the
most performing and profitable model is the Random Forest.



<a id="note1" href="#note1ref"><sup>1</sup></a>In a similar way to the application shown by Rawan Ghnemat and Edward Jaser in the paper "Classification of Mobile Customers Behavior and Usage Patterns using Self-Organizing Neural Networks", International Journal of Interactive Mobile Technologies, Volume 9, Issue 4, 2015.

<a id="note2" href="#note1ref"><sup>2</sup></a> If panel data had been available, the visits could have been annualised on the basis of previous years.
