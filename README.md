# Introduction
What factors play a role in credit card eligibility? Using a dataset obtained from [Kaggle](https://www.kaggle.com/datasets/rohit265/credit-card-eligibility-data-determining-factors), We will be taking a deep dive into the data using Excel. This project aims to analyze a comprehensive dataset of credit card eligibility, focusing on key determinants such as gender, income, account length, age, asset ownership, and more. 

## We will be using this data to answer the following questions:
1) Is there a significant difference in credit card eligibility between different genders?
2) How does income affect the likelihood of being eligible for a credit card?
3) What is the relationship between the length of an individual's account and their eligibility for a credit card?
4) What role does age play in determining an individual's eligibility for a credit card?

5) How does asset ownership, such as owning a car or property, influence credit card eligibility


.
# Data Cleaning 
[Before and After](/Dataset%20Img/)

### Steps to my data cleaning process are as follows:
* Gender Transformation: Changed 0 to Male and 1 to Female for readability.
* Binary Columns (Own Car, Own Property): Changed 0 to No and 1 to Yes for better clarity and consistency across all binary columns.
* Number of Children (Num_children): Grouped into categories: No Children, Few Children (1-2), Several Children (3-4), Many Children (5+).

   **Formula: =IF(I4=0, "No Children", IF(AND(I4>=1, I4<=2), "Few Children", IF(AND(I4>=3, I4<=4), "Several Children", "Many Children")))** 

* Account Length (Account_length): Grouped into categories: Short Term (≤10), Medium Term (11-30), Long Term (31+).

  **Formula: =IF(L5<=10, "Short Term", IF(AND(L5>=11, L5<=30), "Medium Term", IF(L5>30, "Long Term", "N/A")))**
.
* Total Income (Total_income): Grouped into income levels: Low Income (<50,000), Medium Income (50,000-99,999), High Income (100,000-499,999), Very High Income (500,000+).

  **Formula: =IF(N4<50000, "Low Income", IF(N4<100000, "Medium Income", IF(N4<500000, "High Income", "Very High Income")))**

* Years Employed (Years_employed): Grouped into categories: Not Employed (0), New Employee (1-2), Mid-Level Employee (3-10), * Experienced Employee (11-20), Senior Employee (21+).

  **Formula: =IF(R2=0, "Not Employed", IF(R2<=2, "New Employee", IF(AND(R2>=3, R2<=10), "Mid-Level Employee", IF(AND(R2>=11, R2<=20), "Experienced Employee", "Senior Employee"))))**

* Age: Grouped into age categories: Young Adult (21-30), Adult (31-45), Middle-Aged (46-60), Senior (61-69).

  **Formula: =IF(P2<=30, "Young Adult", IF(P2<=45, "Adult", IF(P2<=60, "Middle-Aged", "Senior")))**

 .

# Analysis
With the use of a pivot table and visualization tools, I will demonstrate relevant insights that answer the question at hand
1) ### Is there a significant difference in credit card eligibility between different genders?

   ![Male vs Female](https://github.com/AbdoulMohd/CreditCard_Eligibility_Project-Excel-/blob/main/%231%20Visualization/Eligibility%20By%20Gender.png?raw=true) ![](https://github.com/AbdoulMohd/CreditCard_Eligibility_Project-Excel-/blob/main/%231%20Visualization/Eligibility%20By%20Gender%20Visual.png?raw=true)
  
 The data above shows that there appears to be a slightly higher percentage of eligible individuals among Females (13.91%) compared to Males (12.84%). While there is a slight difference in credit card eligibility rates between genders, the difference is not substantial.

 Among individuals eligible for a credit card, 48% are male while 52% are female. This indicates a marginal but notable difference, suggesting that females have a higher likelihood of being eligible for a credit card compared to males.

![Male](https://github.com/AbdoulMohd/CreditCard_Eligibility_Project-Excel-/blob/main/%231%20Visualization/Male%20vs%20Female%20Visual.png?raw=true)

.

2) ### How does income affect the likelihood of being eligible for a credit card?

![Eligibity By Income](https://github.com/AbdoulMohd/CreditCard_Eligibility_Project-Excel-/blob/main/%232%20Visualization/Eligibity%20By%20Income%20Visual.png?raw=true)  
![](https://github.com/AbdoulMohd/CreditCard_Eligibility_Project-Excel-/blob/main/%232%20Visualization/Eligibility%20By%20Income.png?raw=true) ![](https://github.com/AbdoulMohd/CreditCard_Eligibility_Project-Excel-/blob/main/%232%20Visualization/%25%20Eligibible.png?raw=true) 

Higher income levels generally correlate with a higher likelihood of being eligible for a credit card. The "Very High Income" group has the highest eligibility rate at 21.30%, indicating that income is a significant factor in credit card eligibility.

![M v F income Distribution](https://github.com/AbdoulMohd/CreditCard_Eligibility_Project-Excel-/blob/main/%232%20Visualization/M%20vs%20F%20income%20distrubution.png?raw=true) 

More over when comparing Male and Female based on income, there are notable differences in income ranges. In some income categories, such as high and medium incomes, females tend to have higher eligibility percentages, while in others, such as low income, males have higher percentages. This shows why women have a slight edge in credit card eligibility. 

.

3) ### What is the relationship between the length of an individual's account and their eligibility for a credit card?

![Account Length](https://github.com/AbdoulMohd/CreditCard_Eligibility_Project-Excel-/blob/main/%233%20Visualization/Account%20Length.png?raw=true) ![Account Length Visual](https://github.com/AbdoulMohd/CreditCard_Eligibility_Project-Excel-/blob/main/%233%20Visualization/Account%20Length%20Visual.png?raw=true)

The data suggests a positive correlation between the length of an individual's account and their likelihood of being eligible for a credit card. Individuals with longer account histories are more likely to qualify for a credit card compared to those with shorter histories. This underscores the importance of a strong banking relationship and established credit history in the credit card eligibility determination process.

.

4) ### What role does age play in determining an individual's eligibility for a credit card?
![Eligibility By Age](https://github.com/AbdoulMohd/CreditCard_Eligibility_Project-Excel-/blob/main/%234%20Visualization/Eligibility%20By%20Age.png?raw=true) ![Eligibility By Age Visual](https://github.com/AbdoulMohd/CreditCard_Eligibility_Project-Excel-/blob/main/%234%20Visualization/Eligibility%20By%20Age%20Visual.png?raw=true)

Overall, age plays a significant role in determining an individual's eligibility for a credit card. Younger individuals, especially those in the young adult age range (21-30), have the highest likelihood of being eligible, while eligibility rates tend to decrease with age. This trend underscores the importance of considering age as a factor in credit card eligibility assessments and tailoring credit offerings to different age demographics.

.

5) ### How does asset ownership, such as owning a car or property, influence credit card eligibility
![Car_Ownership](https://github.com/AbdoulMohd/CreditCard_Eligibility_Project-Excel-/blob/main/%235%20Visualization/Car%20Ownership%20El.png?raw=true) ![Car_Ownership Visual](https://github.com/AbdoulMohd/CreditCard_Eligibility_Project-Excel-/blob/main/%235%20Visualization/Car%20Ownership%20El.%20Visual.png?raw=true)


![Property_Ownership](https://github.com/AbdoulMohd/CreditCard_Eligibility_Project-Excel-/blob/main/%235%20Visualization/Property%20Ownership%20El.png?raw=true) ![Car_Ownership Visual](https://github.com/AbdoulMohd/CreditCard_Eligibility_Project-Excel-/blob/main/%235%20Visualization/Property%20Ownership%20El%20Visual.png?raw=true)

Ownership of assets such as a car or property has a minimal impact on credit card eligibility. The differences in eligibility rates between individuals who own these assets and those who do not are relatively small. This indicates that while asset ownership may be considered, it is not a primary determinant of credit card eligibility.

.

# Conclusion
The analysis of credit card eligibility determinants reveals that **income, account length, and age** play significant roles in the approval process. While gender and asset ownership show some influence, their impact is less pronounced. These insights can help financial institutions refine their credit assessment strategies and improve customer targeting and segmentation. 

