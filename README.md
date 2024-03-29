# Tourism hotspots hit hard by Covid-19 jobs crisis

![](https://ichef.bbci.co.uk/news/976/cpsprodpb/12192/production/_117303147_london_bridge.jpg)

In March 2021, the BBC Shared Data Unit [reported](https://www.bbc.co.uk/news/uk-56127385) parts of the UK reliant on tourism had been most affected by the Covid-19 jobs crisis, according to analysis.

In some areas, around three out of five people who began claiming universal credit at the outset of the pandemic were still doing so six months later.

Experts said areas with seasonal employment were more likely to see furloughed workers, those in low-wage jobs or on zero-hours contracts.

The government said it was boosting welfare support by "billions" to help.


## Method

The BBC Shared Data Unit analysed official statistics detailing the number of people who were on Universal Credit up to 12 November.

It was sourced from the DWP’s [Stat-Xplore](https://stat-xplore.dwp.gov.uk/webapi/jsf/login.xhtml) datasets:
* Starts on Universal Credit 
* People on Universal Credit

The programming language R was used to combine and reshape the data for analysis. [The process is documented in this R notebook](https://github.com/BBC-Data-Unit/Universal-credit/blob/main/welfarecap.Rmd)

In order to establish the minimum numbers of people still on Universal Credit 6 months after their claims began we analysed increases in the numbers of claimants in the 6-12 month category between September and October (6 months after April and May).

Any increases in those categories could only be due to claimants moving into the 6-12 month category from the 3-6 month category, i.e. those hitting 6 months in that month. (We would have excluded any areas where there was a fall, but this did not apply to any areas).

We also factored in extra increases needed to compensate for claimants moving *out* of the 6-12 month category, into the 1-2 years category. Where the 1-2 year category *also* increased that month, we added that number to the calculation of those hitting 6 months (where there was no increase, or a fall, in the 1-2 years category, no additional increase was made).

For example: in Torquay there were 4176 claimants in September in the 6-12 months category (those who had had claims open for that length of time). In October that category swelled to 8745. This means that at least 4569 claimants joined the category that month, as they hit the 6 month point and moved up from the previous category (3-6 months), even before factoring in how many more claimants would be needed to compensate for any moving *out* of that category.

On that matter, the 1-2 year category increased by 100 claimants that month, who must have moved *out* of the 6-12 months category. That means that the numbers moving *in* to the 6-12 months category creating an increase overall, are 100 higher - 4669.

Of course this is only a **minimum** number moving up into that category, as there are likely to be further claimants moving out of the 6-12 month category due to closing their claim (because, for example, they found work or their wages increased above the threshold for claiming Universal Credit).



## Data and sources

The data and background methodology released to partners are available here:
* [Background](https://docs.google.com/document/d/1g0ZJSjDSlnkrn9dHumCA-F0vV0qeui2S2DEO4Oq-Vz8/edit)
* [Data](https://docs.google.com/spreadsheets/d/1S2jbHPm0f14BsdlE1REI1s1tJ7KyagDvrrrbkRvSDbs/edit#gid=644190398)

## Interviews and quotes

* Richard Burge, Chief Executive of London Chamber of Commerce and Industry
* Labour’s London Assembly Economy Spokesperson, Leonie Cooper AM
* Powys County Council
* Richmondshire District Council
* Minesh Patel, principal policy manager at Citizens Advice UK
* Emma Congreve, Knowledge Exchange Fellow at the Fraser of Allander Institute at the University of Strathclyde
* Peter Matejic, deputy director for evidence and impact at the Joseph Rowntree Foundation
* Nye Cominetti, senior economist at the Resolution Foundation think-tank
* The Department for Work and Pensions

## Partner usage

The Shared Data Unit makes data journalism available to the wider news industry as part of the BBC Local News Partnership.
Stories written by partners based on this research included:

* Teesside Live: [Teesside worst hit by covid-19 jobs crisis as huge numbers turn to Universal Credit](https://www.gazettelive.co.uk/news/teesside-news/teesside-worst-hit-covid-19-19942670) *2 March 2021*
* Cambridgeshire Live: [Cambridgeshire revealed as one of areas worst hit by coronavirus jobs crisis](https://www.cambridge-news.co.uk/news/cambridge-news/cambridgeshire-covid-coronavirus-jobs-crisis-19943043) *2 March 2021*
* In Your Area (Reach): [Revealed: The areas most affected by the Covid-19 jobs crisis](https://www.inyourarea.co.uk/news/areas-most-affected-by-covid-jobs-crisis/) *2 March 2021*
* Shetland News: [New study sheds light on rise in benefits claims during pandemic](https://www.shetnews.co.uk/2021/03/02/new-study-sheds-light-on-rise-in-benefits-claims-during-pandemic/) *2 March 2021*
* Lancashire Telegraph: [Universal Credit claims by people in work rise as Ribble Valley tourism hit](https://www.lancashiretelegraph.co.uk/news/19126798.in-work-uc-claims-tourism-industry-hit/) *2 March 2021*
* Southampton Daily Echo: [Benefit claims soared across Southampton as virus hit the region](https://www.dailyecho.co.uk/news/19127655.benefit-claims-soared-across-southampton-virus-hit-region/) *2 March 2021*
* Aberdeen Evening Express: [Number of north-east Universal Credit claimants still receiving benefits after six months drops](https://www.eveningexpress.co.uk/fp/news/local/number-of-north-east-universal-credit-claimants-still-receiving-benefits-after-six-months-drops/) *2 March 2021*
* Bournemouth Daily Echo: [Universal Credit claims soared in BH postcodes as pandemic hit](https://www.bournemouthecho.co.uk/news/19127632.universal-credit-claims-soared-bh-postcodes-pandemic-hit/) *2 March 2021*
* Wigan Today: [Thousands of Wiganers needing benefits in lockdown still claiming six months later](https://www.wigantoday.net/news/politics/thousands-of-wiganers-needing-benefits-in-lockdown-still-claiming-six-months-later-3152153) *3 March 2021*
* East Anglian Daily Times: [New benefit claims in Ipswich shot up over 500% during pandemic](https://www.eadt.co.uk/news/ipswich-universal-credit-claims-rise-over-500-percent-7801020) *3 March 2021*

The story featured on BBC front, home and England pages. It was also used by BBC Somerset, BBC Radio Shropshire and BBC Radio Tees.

## Related repos

You can [find all coronavirus-related stories by the BBC data units tagged 'coronavirus' here](https://github.com/search?q=topic%3Acoronavirus+org%3ABBC-Data-Unit&type=Repositories)
