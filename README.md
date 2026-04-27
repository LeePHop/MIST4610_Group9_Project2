# MIST4610_Group9_Project2

# About Our Data Set

The dataset utilized for the analysis was taken from the NHTSA Recall Database, which offers free access to safety recalls information for vehicles and equipment in the USA. This dataset consists of 29,940 rows and 15 columns, thus giving the possibility for an extensive analysis.

Every row presents one recall case, whereas the columns represent various features related to the case. Some of the most informative columns are Report Received Date (recalls' dates), NHTSA ID (unique code), Manufacturer (the manufacturer of the product), Subject (title of the problem), and Component (defects category, e.g., seats, structure, and equipment). In addition to those descriptive columns, there are several quantitative columns, such as Recall Type, Potentially Affected (total number of potentially affected vehicles), and Completion Rate %. At last, the dataset also includes the textual columns, such as Recall Description, Consequence Summary, and Corrective Action.

When considering the type of data included in the dataset, there are both categorical data types (such as Manufacturer, Component, and Recall Type), numeric data types (such as Potentially Affected and Completion Rate %), and string data types (such as Recall Description and Consequence Summary). There is a temporal variable in the form of Report Received Date, which could be considered for time-series analysis. Additionally, there are some missing values in the dataset, especially in variables like Completion Rate, due to realistic data limitations.

Considering all the information above, one may conclude that the provided dataset is sufficient and complex enough, as it contains many observations and different types of variables, varying greatly in the aspects of manufacturer, defect, and recall size.

When formulating our research questions, it was deliberate that they would be useful to ask from the viewpoint of an insurance company. This is important because apart from being data-based, the research questions should be practical, with a focus on risk assessment, financial implications, and liability in the future. Insurance companies are heavily dependent on finding patterns in safety issues like recalls when deciding how much premiums to charge for their customers, which policy to underwrite, and the risk involved.

    Question 1: What vehicle manufacturers have the highest number of potentially affected parts from recalls between 2000 and 2026?

<img width="3167" height="1848" alt="Screenshot 2026-04-23 093049" src="https://github.com/user-attachments/assets/8b0eaf3a-6a1f-44c6-8f74-cad0a62b748f" />

The question is very significant in relation to the insurer, as it is concerned with how much they may be exposed to risks and how they should cover for the risks. Companies that manufacture more cars with the possibility of defect, accident, or malfunction are more likely to attract more insurance claims. There will be many cases where large numbers of their products will have to be recalled, resulting in insurance claims for property damage and bodily injuries.

On an economic basis, the question can enable the insurer to make considerations on the premium rates, risks involved in the underwriting process, and the coverage limits for particular brands. On social grounds, there may also be safety concerns involving the use of particular vehicles that should affect the consumers. This question is highly correlated with the dataset because it involves the analysis of “Manufacturer” and “Potentially Affected” variables.”



    #Question 2: How have recall volumes (in terms of potentially affected vehicles) changed over time for Ford Motor Company?

<img width="3162" height="1848" alt="Screenshot 2026-04-23 092857" src="https://github.com/user-attachments/assets/dc4803de-465d-4279-b3d4-b49da291f753" />

It was formulated from the standpoint of the insurer, specifically, how risk changes through time for one significant automobile manufacturing firm. It is critical since insurers not only assess overall risk but also monitor its trends to foresee future claims and possible expenses.

According to the graph, there are several noticeable peaks in the number of cars recalled by Ford. For instance, there were more than 10 million recalls during the beginning of the 2000s and almost 12.8 million recalls recently. Such peaks suggest that some specific periods are associated with high risks, when there are many vehicles that are prone to malfunction and, thus, can cause various accidents.

From an insurance perspective, this particular question is significant since it aids in determining whether there is an increase, decrease, or variability in risk exposure by manufacturers over time. If there are consistent peaks, then it indicates inconsistency in the manufacturing process which in turn might result in the insurer hiking its premiums or even denying the policyholder cover. Economically, it affects the bottom line since the company has to pay out the claim. This issue is social since it has safety implications.

The question has strong ties with the database used since “Report Received Date (Year)” represents time, while “Potentially Affected” represents the size of recalls. The combination of the two creates a more complex, analytical, and forward-looking perspective, thus making the question both sophisticated and relevant.
