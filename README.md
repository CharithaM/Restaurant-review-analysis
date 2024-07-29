This project is a sentiment analysis and review management system for a restaurant, implemented using Python, machine learning, and Tkinter for the graphical user interface. The system allows users to submit reviews about various food items, and it determines the sentiment of the reviews (positive or negative). The project has two main interfaces: one for customers to submit reviews and another for the owner to view and manage the reviews.

## Key Components:

### Data Preparation and Sentiment Analysis:

1. **Data Loading and Preprocessing**:
   - The project uses the `Restaurant_Reviews.tsv` dataset containing restaurant reviews.
   - Reviews are preprocessed by removing non-alphabetic characters, converting to lowercase, removing stop words, and applying stemming.

2. **Feature Extraction**:
   - The `CountVectorizer` is used to convert the cleaned reviews into a matrix of token counts.

3. **Model Training**:
   - A Naive Bayes classifier (`MultinomialNB`) is trained on the preprocessed reviews to predict the sentiment (positive or negative).

### Database Management:

4. **SQLite Database**:
   - A SQLite database (`food_reviews.db`) is used to store food items and their review statistics (positive reviews, negative reviews, positive rate, negative rate).
   - The database is initialized with a predefined list of food items.

### GUI with Tkinter:

5. **Main Window**:
   - The main window offers two options: Customer and Owner interfaces.

6. **Customer Interface**:
   - Customers can select food items from a list and submit their reviews.
   - The submitted reviews are analyzed using the trained sentiment analysis model.
   - The review counts and rates for each food item are updated in the SQLite database.

7. **Owner Interface**:
   - The owner can view the review statistics of all food items by entering a password.
   - The owner can also reset the review counts for all food items.

### User Experience Enhancements:

8. **Sound Effects**:
   - Button clicks play a sound for better user interaction.

9. **Styled Widgets**:
   - The interface elements such as buttons, labels, and entry fields are styled for better visual appeal and user experience.

### Additional Features:

10. **Clear Reviews**:
    - The owner can clear all reviews and reset the statistics in the database.

11. **Password Protection**:
    - The owner interface is protected by a password to prevent unauthorized access.

### Usage:
- **For Customers**: Select the food items, enter a review, and submit it. The system will analyze the review and update the review statistics accordingly.
- **For Owners**: Enter the password to view the review statistics of all food items and clear the reviews if needed.

This project demonstrates the integration of machine learning for sentiment analysis, database management for storing review statistics, and a graphical user interface for user interactions, making it a comprehensive solution for managing restaurant reviews.
