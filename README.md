# MIST4610 Group 9 Project 2

# Team Members

1. [Lee Hopkins](https://github.com/LeePHop)
2. [James Troutt](https://github.com/trouttjames6)
3. [Sean Fisher](https://github.com/SeanFishe5)
4. [Akhila Kothapalli](https://github.com/akhilakoth04)

# About Our Data Set

The dataset utilized for the analysis was taken from the NHTSA Recall Database, which offers free access to safety recalls information for vehicles and equipment in the USA. This dataset consists of 29,940 rows and 15 columns, thus giving the possibility for an extensive analysis.

Our Data Set: https://catalog.data.gov/dataset/recalls-data?from_hint=eyJxIjoicmVjYWxscyBkYXRhIiwic29ydCI6InJlbGV2YW5jZSJ9

Every row presents one recall case, whereas the columns represent various features related to the case. Some of the most informative columns are Report Received Date (recalls' dates), NHTSA ID (unique code), Manufacturer (the manufacturer of the product), Subject (title of the problem), and Component (defects category, e.g., seats, structure, and equipment). In addition to those descriptive columns, there are several quantitative columns, such as Recall Type, Potentially Affected (total number of potentially affected vehicles), and Completion Rate %. At last, the dataset also includes the textual columns, such as Recall Description, Consequence Summary, and Corrective Action.

When considering the type of data included in the dataset, there are both categorical data types (such as Manufacturer, Component, and Recall Type), numeric data types (such as Potentially Affected and Completion Rate %), and string data types (such as Recall Description and Consequence Summary). There is a temporal variable in the form of Report Received Date, which could be considered for time-series analysis. Additionally, there are some missing values in the dataset, especially in variables like Completion Rate, due to realistic data limitations.

Considering all the information above, one may conclude that the provided dataset is sufficient and complex enough, as it contains many observations and different types of variables, varying greatly in the aspects of manufacturer, defect, and recall size.

When formulating our research questions, it was deliberate that they would be useful to ask from the viewpoint of an insurance company. This is important because apart from being data-based, the research questions should be practical, with a focus on risk assessment, financial implications, and liability in the future. Insurance companies are heavily dependent on finding patterns in safety issues like recalls when deciding how much premiums to charge for their customers, which policy to underwrite, and the risk involved.

# Question 1

    What vehicle manufacturers have the highest number of potentially affected parts from recalls between 2000 and 2026?

<img width="3167" height="1848" alt="Screenshot 2026-04-23 093049" src="https://github.com/user-attachments/assets/8b0eaf3a-6a1f-44c6-8f74-cad0a62b748f" />

## Why the question is important

The question is posed from the point of view of an insurance company to determine which manufacturers pose the biggest risk exposure on the basis of the number of recalls. From the chart, one can see that manufactures such as Ford, General Motors, and Chrysler have a large number of vehicles that could be affected, with figures running in excess of 100 million units. This is relevant due to the fact that the number of cars affected reflects the magnitude of claim risks faced by the insurer.

From an insurance point of view, the bigger the number of recalls, the greater the probability of mechanical breakdowns and accidents resulting in claims that include collisions and liabilities. The probability of claims even from a few percents of the vehicles involved in the recalls would translate into considerable aggregate risk for the insurer.

Moreover, through asking this particular question, we get an opportunity to differentiate between high frequency-low impact recalls and low frequency-high impact recalls. In essence, manufacturers who have less recall activities but whose recall volumes are enormous may be more risky for insurers compared to those with numerous smaller volume recalls. This is highly important for segmentation purposes as insurers need to make proper premium decisions on different makes and models.

In economic terms, the outcomes of our study allow for premium, reinsurance, and capital management. We know that insurers are aware of the possibility of a sharp rise in recall-related claims and need to be adequately prepared. From social point of view, identification of manufacturers with enormous recall activity raises questions about safety standards.

The connection between the question and the dataset is apparent from the variable "Manufacturer" and the numerical variable "Potentially Affected." Through the process of aggregation, the question becomes sophisticated and highly relevant, enabling the comparison of risks among different firms based on data.

## Manipulations

The first manipulation we made was filtering the data by recall type. Because we are taking the stance as an auto insurance agency, the only recall type that we are interested in is vehicles that are recalled. This means that the data will not display any data involving child seats, eqipment, or tires.

The next manipulation we made was to set what years we were looking at. In order to keep the data more focused, we determined we were only interested in recalls made in the 21st century. We filtered the reports receieved date field by year, and selected all years starting from 2000 and ending at 2026.  

The last manipulation we made was the range of how many potentially affected vehicles there were. We decided we wanted to focus on the top 15 manufactuers with the most recalls, as we felt this would help us focus our data and analysis better. Because of this, we set the lower range to be 5,000,000 recalls, which gave us the top 15 manufacturers we were looking for. We made no changes to the upper range.

No calculations were made in this question.

## Analysis
In the graph above there are three companies that have over 100 million potentially affect parts: Ford, General Motors, and Chrysler. All three of these companies are based in the United States, potentially indicating that American-made vehicles are less reliable than vehicles from other countries. Furthermore, there is a significant drop off between the third most affected company, Chrysler, and the fourth most affected company, Toyota. This adds more credibility to the theoryu that American-made vehicles are more likely to be recalled. Because of this issue of reliability, the safety of American-made vehicles may be called into question. As a result, insurance companies may charge higher premiums for American vehicles to ensure they are covered.

# Question 2

    Has Ford improved their recalls over the last 26 years?
<img width="3153" height="1851" alt="Screenshot 2026-04-28 184418" src="https://github.com/user-attachments/assets/c93ba41a-d4e8-4593-91f3-227d9d3dd24e" />


## Why the question is important

It is vital to consider this question from the standpoint of an insurance company since its analysis will be able to reveal whether the risk profile of the company is getting better or, conversely, stays constant. The thing is, insurance companies always analyze trends in order to evaluate whether certain manufacturers become more reliable. Thus, this information affects premiums and the company's future estimates of claims.

From what we see in the graph, it becomes obvious that Ford has not made considerable improvements over the past 26 years. In particular, we can observe periods when the number of vehicles involved in the process was lower, but then, there was a rise in the number of recalls; at that, some recalls have even exceeded 12 million vehicles.

From the perspective of insurance, this suggests that there is no improvement in terms of risk. Higher increases in recalls will mean that insurers will face a greater likelihood of claims, which will be detrimental to their bottom line. From an economic perspective, this will mean that insurers cannot afford to lower their risks when it comes to insurance coverage from Ford.

This question is relevant to the database because of the two variable fields, “Report Received Date (Year)” and “Potentially Affected”. This question will help with a time series analysis of recalls over a period of years. This is an important question because of its predictability for the future.

## Manipulations

For question 2, all of the same filter manipulations are applied from question 1. This is because the question 2 takes that information from question 1, and uses it to look specifically at one manufactuerer. Additionally though, question 2 inlvolves us specifically analyzing Ford's recall trend. This is because they, by far, had the largest number of vehicle recalls, which made their product riskier than others. In order to look at Ford specifically, we filtered manufacturer by company, and only selected Ford. Combined with the other filters, we created a time series graph illustrating how Ford's recalls have changed over time. 

For the rows, we changed Reports Received Date into a continous variable rather than a discrete variable. Since we are analyzing a trend over time, it makes more sense to identify the years we are looking at over time. 

No calculations were made for this question. 

## Analysis
In 2001, Ford had a huge spike in recalls reported. However, every year thenon saw either sharp decreases or sharp increases in recalls within the year to indicate a relatively stable trend. This was until 2014, when though the pattern continued, the amount of vehicles being recalled were overall increasing. Ford had its largest spike in recalls in 2025 with almost 13 million units potentially affected vehicles. The large spike in 2025 might cause a higher frequency of losses of vehicles. This implies that insurance companies might be more cautious with 2025 Ford vehicles, leading to a higher premium or making sure the liability is heavily on the manufacturer. Currently in 2026, there are already roughly 9 million affected parts, indicating that this year may be another high recall year.
