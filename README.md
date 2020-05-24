Table of contents
-----------
1. [ Preface ](#desc)
2. [ Descriptive Analysis ](#usage)
3. [ Association Rules ](#usag)
4. [ Self-Organising Maps ](#usa)

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

**FIGURA 1**
<p align="justify">
Taking into account the first two levels of the variable, there is a slight difference in terms of relative frequencies: in particular in this sample, the frequency of women who renew is around 70% while it is of 69% for men. The third column shows the units for which there is no answer linked to the gender variable and it allows us to reject the hypothesis of a link between NA and the renewal by sex variable, since the distribution seems to be similar to the other columns.
</p>
**FIGURA 2**
<p align="justify">
On the other hand, the differences in terms of age between those who renew the subscription and those who do not, are more marked; indeed the average age of the former seems to be greater, suggesting therefore that the renewal tends to be more frequent in older subscribers.
Therefore, unlike gender, it can be concluded that the age variable differs significantly between the two groups.
</p>
**FIGURA 3 E TABELLA**
<p align="justify">
The bar chart above shows how the distribution of renewals varies by geographic area: thus, the more one gets away from the City of Turin, the more the relative churn frequencies tend to increase. To enrich this study the adjacent table is reported in absolute terms and it shows that the largest number of members who renew the card comes from the capital of Piedmont and that the two “belts” together have the largest number of renewals of the rest of Northern Italy.
These two analyses, taken together, highlight the relevance of this variable for the purpose of this report.
</p>
**FIGURA 4**
<p align="justify">
The density curves show how the relative distribution of the number of visits differs between people who renew their subscription compared to those who churn. It can be predictably assumed that the number of visits influences positively the probability of renewal (re-subscription card).
 </p>
 **FIGURA5**
 <p align="justify">
 A similar interpretation is applicable to the amortization of the subscription cost, since the number of entries is highly correlated with the total cost of visits.
The variable highlights the costs that would have been incurred if the visitors had not subscribed the museum card.
</p>
**FIGURA 6**
<p align="justify">
The above bar chart shows the discount variable, at first defined by 24 levels and, for clarity, here coded as a dummy; in detail it is clear that the proportion of withdrawals among those who have not received any discount or reduction on the subscription price is significantly higher if compared to the respective proportion of subscribers with discount rights.
</p>
**FIGURA 7**
<p align="justify">
The distribution of visits does not seem to differ on weekdays between those who renew and do not: however there is a slight variation on weekends and in particular those who renew the subscription tend to visit more museum sites on weekends with significant distribution on Fridays and Saturdays (in addition to differing even on less common days such as Wednesdays and Thursdays in favour of those who renew the card). 
</p>
**FIGURA 8**
<p align="justify">
A quick inspection of the distribution by Cap of the subscribers allows us to conclude that this effect can be analyzed especially in the Turin hinterland and, for this reason, we focus on the Turin Cap because of the highest number of members. The most numerous members are concentrated in the Mirafiori area (North), Borgo San Paolo and Pozzo Strada. It is curious to note that the most central areas such as San Donato and Quadrilatero, despite their great proximity to the museum sites, in absolute terms show the lowest number of members.
</p
  
**FIGURA 9**

<p align="justify">
The map of the province of Turin shows the number of cumulated entries per Cap and it seems to fit perfectly with the previous results. It can therefore be concluded that the areas with the highest number of members are also those with the highest number of cumulative visits. The reading that I want to deepen now is how to distribute the relative frequencies of churn and in particular if the areas with fewer visits and members are also those with higher probability of churn.
</p>

**Figura 10** e tabella
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
**FIGURE 11**
<p align="justify">
It is noteworthy that the greater is the number of distinct people with whom all visits have been shared, the greater is the frequency of renewals compared to those who churn. The most interesting aspect that emerges is that those who churn are accompanied by a number of different people on average lower, suggesting that the variable in question, may have a negative effect on the probability of abandoning. It can probably be interpreted with the fact that the greater is the number of people with whom one shares a passion for art or cultural visits, the greater is the stimulus received to renew the subscription.
Moreover, according to the average age of those who go to the museum with a smaller number of people, on average it appears that they are older than those who share visits with a larger number of distinct people.
This second analysis, carried out through the Market Basket Analysis, first focuses on considering which are the most visited museums (in particular for three of them, it will be investigated
where went people who visited a particular site).
</p>
**FIGURE 12**
Most of the reported "rules” highlights visits to close-located museums, especially in the Centre of Turin. Unfortunately, it cannot be understood whether this is an effect linked to individual thematic preferences or simply a proximity effect.

<a name="usa"></a>
Self-Organising Maps
-----------
<p align="justify">
The last methodology that will be used for our descriptive purposes is a non-parametric model with unsupervised learning: the Self-Organising Maps. The iterative algorithm has the ability to capture, through a two-dimensional neuronal structure, the non-linear relations between variables keeping however the topological order.
1 The aim of implementing Self Organising Maps in this context is to be able to segment consumers ,
verifying whether the first relationships, detected at the descriptive level, can be confirmed. To obtain a sufficient degree of convergence 1000 interactions were chosen and a number of clusters equal to 4 was assumed. Being an unsupervised learning model, this preference was made on the basis of graphic considerations (codes), together with the outcome of the Ward method.
</p>
**FIGURE 13**
<p align="justify">
The graph shows the number of observations "captured" by each neuron and the areas with higher density. In this case the map is a 20x20 grid and, as can be inferred from the adjacent coloured scale; thicker areas are more frequent in the left area and, in particular, the empty neurons (in grey tones) graphically tend to delimit the distinct areas.
Linked to this graph, the "U-matrix" is analysed with the intent of showing the distance between the identified neurons. In particular, it is evident that there are two well-defined and clearer areas; so that you can at least consider two groups, whose deep colour is inversely proportional to the distance.
</p>

:!toc:

AsciidocFX shows links in PDFs as footnotes http://stackoverflow.com[SO].

.Asciidoc in PDF does not work in Asciidoctor, but works in AsciidocFX.
[cols="2,5a"]
|===
|Line with Asciidoc code
|here comes a list:

* item 1
* item 2
* item 3

http://stackoverflow.com[Get Answers]!

|Line
|with a footnotefootnote:[footnotes do work in AsciidocFX's PDF output (but not in the preview).]

|===
