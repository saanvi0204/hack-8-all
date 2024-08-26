# Codeforces User Persona Segmentation

On platforms like Codeforces, a user's rating is often seen as a primary indicator of their skill level. However, rating alone doesn’t provide a full picture of a user’s journey or learning needs. Ratings can be inconsistent due to factors like irregular contest participation, rating inflation, or temporary slumps. To create accurate user personas, we need to look beyond just ratings and consider other factors as well.
This project focuses on retrieving data from Codeforces user handles and applying machine learning model to categorize users into distinct personas. These personas can be leveraged by ed-tech platforms to recommend personalized learning paths, based on each user’s achievements.

Approach:

Data Collection: We scraped Codeforces data for various user handles, retrieving details such as:
•	Rating
•	Number of problems solved
•	Number of problems solved in last month
•	First contest year
•	No of rated contests
Data Preprocessing:
The collected data was cleaned and pre-processed to handle missing values and normalize features.
K-means Clustering:
Elbow Method is used to choose optimal number of clusters for K-means clustering algorithm which was then used to group users into seven personas. The model was trained using features as mentioned above.

Defining the personas:
Explorer (Cluster number 6): Low rating, less number of problems solved and contests attended and recent date of joining contests, we can say that the user is new to competitive programming.
Seeker (Cluster number 1): Average rating, modest number of problems solved and contests given as well as recent year of joining contest indicates that this user is learning basic concepts.
Contest Regular (Cluster number 5): High Rating, large number of questions solved and contests given indicates practice but perhaps saturation
Strategist (Cluster number 3): High Rating, modest number of questions solved and contests given, early joining and low number of questions solved last month indicating good logic but a loss of interest
Visionary (Cluster Number 0): Very high rating, higher number of questions solved indicating good logic
Achiever (Cluster Number 2): Millimetres away from perfection
Mastermind (Cluster Number 4): Already achieved perfection

Use Case: Personalized Learning Recommendations
The personas can be integrated into ed-tech platforms to recommend courses tailored to improve weaknesses, training plans for upcoming contests, roadmaps for advancing in their programming journey.
Applications and Future Work
This approach can be extended to other competitive programming platforms or adapted for broader educational contexts. Future improvements could include integrating additional features like user engagement metrics or implementing a dynamic recommendation engine based on real-time performance updates.
