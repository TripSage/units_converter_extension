### Methods
During the testing sessions, two experimenters were scheduled to analyse the testee (lab rat). Experimenter 1 tracked time taken for each activity and any other notes about the experiment. Experimenter 2 guided the testee through each activity.

We compared our Smart Units Converter chrome extension with the highest rated units converter in the Chrome marketplace. And we used a couple different activities to find the better extension.

We had 6 total activities. 
* Installing Smart Units Converter Chrome Extension.
* Using a product on Amazon.com and find 3 different units to convert. (Ex: currency, length, volume)
* Using Skyscanner.com to find 2 units to convert
* Uninstalling Smart Units Converter
* Installing Units Converter Chrome Extension. (highest rated on Chrome extensions)
* Using a product on Amazon.com and find 3 different units to convert. (Ex:  length, volume, temperature)
* Using Skyscanner.com to find 2 units to convert
* Uninstalling Units Converter Chrome Extension

We asked the testers to use amazon and skyscanner to test the extension like they would when looking to buy something. This allowed us to get an insight on how the  extension behaves with different texts and formats. 

For each activity, Experimenter 1 noted down the time taken. We also utilised google forms to gain more information about the testee’s thoughts on the extension when compared to the best unit converter in the market.


### Materials : 
#### Technologies Used:
* Google forms [https://docs.google.com/forms/d/e/1FAIpQLSdAw6q0F9eH7-4E4a28tgTYkoPKRqPbNzxFlldrEcT6OJCxng/viewform] to collect the data: At the end of Testing Each participant was required to fill the google form in an anonymous manner.
* Zoom video for observation and interactions: The lab trials were conducted on Zoom and each participant was allotted 50 minutes to perform the experiments. And 10 minutes to fill out google form.
* Comparative Analysis: We asked participants to use another competitive chrome extension [https://chrome.google.com/webstore/detail/unit-converter/igjeajmonjofckmiheidpmebpmdbbiam?utm_campaign=en&utm_source=en-ha-na-us-bk-ext&utm_medium=ha] and asked them to rate our extension by using the other extension as baseline.
* Excel Sheet was used to note down the observations w.r.t time taken by a participant and manual notes were taken for subjective analysis like Bugs discovered or feedback presented.
* While freedom to use any website to play with the extension was given to lab-testers, We suggested use of websites such as Amazon.com, Skyscanner, Tesla and Google maps to ensure comprehensive testing of most capabilities of extension.

#### Data Collected/Analyzed: 
* Ease of Installing Extension
* Ease of Uninstalling extension
* Universality: Ability to use on Multiple [Major] websites
* Subjective: How did Product help you? Sentiment evaluated manually
* Number of Bugs discovered, if any?
* Willingness to use the product in Future.
* Is the extension Production Ready?
* How would you rate the product?


### Observations :  
* This is our observation for the installation and uninstallation of the product onto the user’s browser of Google Chrome. Below graph shows the result which has ratings out of 5, 5 claimed easiest to install/uninstall.
![picture](https://github.com/TripSage/units_converter_extension/blob/master/assets/one.png)


* From the testers’ records of ease of use of the tool on different sites is shown in the following chart -
![picture](https://github.com/TripSage/units_converter_extension/blob/master/assets/two.png)


* Question of “Do you think the product helped you? If so, in what way?’” - The observation of the textual evidence was about describing 
    * The use to convert units that are used frequently, 
    * The way the tool saves the time,
    * The convenience offered by the tool 
    
* Question of “Did you experience any difficulty/bug in the product? If so what?” -
The observation of the textual evidence was about describing
    * Minor bugs when units are written in full form/words,
    * Converting standards and precisions.

Following is the analytical chart for the other questions from the survey - 

![picture](https://github.com/TripSage/units_converter_extension/blob/master/assets/three.png)


We can see the results, in the charts above.  



### Analysis :  
From our observations, it is evident that in general, the testers found the product both easy to install and uninstall. Users were able to work with the extension easily and quickly. The test subjects were satisfied with the speed and accuracy of the conversion and mentioned that they would prefer to use this extension in comparison to a traditional conversion system like google unit converter.

As mentioned before, the test subjects were asked to test another similar extension. Below is a comparative analysis of the two extensions:

#### Units Converter
* Average time to install: 3 mins
* Average time to uninstall: 1 min 30 secs
* Average time to begin use: 45 secs

#### Alternative Chrome Extension
* Average time to install: 30 secs
* Average time to install: 30 secs
* Average time to begin use: 2 min 30 secs

The Alternative chrome extension was faster to install as our unit converter source code had to be downloaded from github. However, it can be observed that the time to begin using the extension is much higher. Overall, testers preferred our Unit converter due to its easy of use and more features like currency conversion which was missing from the alternative extension.



#### Statistical nonparametric significance tests and effect size tests :
* Cliff’s Delta - 
This is used for effect size tests. 
It is a statistical nonparametric effect size measure. It helps to quantify the difference between two observations and hence can be used as a complimentary analysis tool for hypothesis testing.
Null hypothesis - “Testers feel the extension is a smart/interesting tool.” 
Alternate hypothesis - “Testers feel the unit converter extension is a useful tool”

* For this, if Cliff’s delta between most of the pairs of the observations is minimum or false, then the analysis says that those pairs have similar opinions. When all the opinions are similar and all of them say one, we can prove our null hypothesis, otherwise, an alternate hypothesis would be regarded as a universal truth.

* Following table shows the questions we put in our analysis along with the maximum and lowest values for each of them:


| Questions | Max score | Lowest Score  |
|---------------------|-----------|---------------|
| How easy is it to install the extension?  |  5 - being easiest | 4 |
| How easy is it to uninstall the extension? | 5 - being easiest  | 2  |
| Are you able to use it in multiple website  | 5 - All websites under test   | 3 |
| Do you think the product helped you? If so, in what way? | NaN | NaN  |
| Did you experience any difficulty/bug in the product? If so what? | NaN  | NaN  |
| How likely are you going to use this product in the future? |  5-sure | 4  |
| Do you think it’s a production ready product? | 5 - sure  | 4  |
| How likely are you to rate this product from your experience? | 5 - excellent  | 4  |


* We can calculate Cliff’s delta between all pairs of the observations we have.
Threshold for overall analysis -> 1/36 -> 0.027778
Algorithm for the same for evaluating cliff’s delta is as follows ->


    def cliffsDelta(lst1, lst2, small=0.147): # assumes all samples are nums
        "Cliff's delta between two lists of numbers i,j."
        lt = gt = 0
        for x in lst1:
          for y in lst2 :
            if x > y: gt += 1
            if x < y: lt += 1
        z = abs(lt - gt) / (len(lst1) * len(lst2))
        return z < small # true is small effect in difference


* There are a total 6 numerically answered questions. Let’s perform the Cliff’s delta analysis on each pair.

| Observations  | 1 | 2  | 3 | 4  | 5  | 6 | 7 | 8  | 9  | 10  |
|---|---|---|---|---|---|---|---|---|---|---|
| 1  | False  | True  | False  | True  | True  | False  | True  | False  | False  | False  |
| 2  |   |  False | False  | False  |False   | False  | True  | False  | False  |  True |
| 3  |   |   |  False | False  | False  | False  | True  | False  | False  |  True |
| 4  |   |   |   |  False | False  |True   | False  | False  | True  | False  |
| 5  |   |   |   |   |  False | False  | False  | False  | False  |  True |
| 6  |   |   |   |   |   |  False | True  | False  | True  | False  |
| 7  |   |   |   |   |   |   |  False | False  | False  | False  |
| 8  |   |   |   |   |   |   |   |  False | True  |False   |
| 9  |   |   |   |   |   |   |   |   | False |  False |
| 10  |   |   |   |   |   |   |   |   |   | False  |

(Lower part of the table is not filled as the table is symmetric)
From most of the answers, we can see, Cliff’s Delta is false. So a similar opinion is present across this cluster can be inferred from this and hence our null hypothesis is proved. 


### Conclusions : 
* Our unit converter when compared with the top-rated unit converter extension provided on Google Chrome, performed better and proved to be more handy, easy to install/uninstall,and use. The top-rated one proved to be user unfriendly.
* Testers, themselves, after getting hold on how to use our extension of the unit converter, started using it on different websites to check the conversions. 
* There were 2-3 websites testers encountered during the session where they could not use the extension and they have mentioned about them in the survey. 
* There were some of the units that were not supported by our unit converter. Testers have mentioned that as well in the survey.
* Ease of using our tool, like just selecting the portion of the unit to be converted, installing and keeping it pinned on our browser, made testers more comfortable during testing and were able to explore more by themselves.
* Based on the comments on how interesting testers are to use our tool, we can say our tool converter is extremely likeable.

### Threats to validity :
There are two types of threats to validity: technical and subjective. 

* Technical threats occur due to the technical aspect of the experiment. In our case, our program is too small to affect any serious technical threats to the experiment. Another technical threat that could have occured is if Chrome malfunctioned during the test. Fortunately, this didn’t happen since Chrome is generally reliable. 

* Subjective threats to validity occur due to mistakes by the experimenter or the testee bias affecting the experiment. In our experimentations, one person was usually the note taker and one would guide the testee. Notes about the experiment would differ slightly from each experimenter. The smaller nuances of the experiment also varied. Some testees spent more time looking up the products they wanted to buy than measure units. Some testees already worked on the smart units converter and already had it installed. They also knew how it works so they breezed through half the activities faster than other testees. Other testees didn’t initially have Google Chrome and took more time to install and figure out how to install it. In our experiment, we asked our testees to visit the websites most frequently visited like amazon or skyscanner as well any other website they wanted to explore. Since most websites the testees chose to experiment with were the more popular ones, we haven’t tested the product with “edge case” websites that use different fonts and formats of text. 


