# voca-learning

# Project Structure

* src/components:

    * Flashcards.js: Core component for displaying vocabulary words and providing review functionality (mark as known, need to review).
    * WordCard.js: Visual representation of a single vocabulary word (includes word, meaning, example, etc.).
    * SearchBar.js: Allows users to search for specific words.
    * LearnedWords.js (Likely): A component to display a user's learned vocabulary.
    * ReviewQueue.js (Planned): A dedicated section for focused review of challenging words or words due for repetition.

* src/api:
    * auth.js: Contains authentication routes (register, login). Implementation details are unknown, as I don't have visibility.
    * words.js: API endpoints for:
        * Fetching words for initial learning
        * Updating word data after review (intervals, easiness factor – SM2 placeholder)
        * Fetching words due for review (based on spaced repetition)
    * users.js (Likely): Endpoints for managing user data (adding/removing learned words)
* src/models
    * User.js: Mongoose model to define user schema (username, password, learnedWords, etc.).
    * Word.js: Mongoose model to define word schema (word, meaning, example, pronunciation, translation, reviewInterval, nextReviewDate, easinessFactor – SM2).

# Functionality

* Core Learning:

    * Users can view vocabulary words in a structured format (WordCard).
    * Users can search for words.
    * Flashcard exercises for vocabulary review.
* Authentication (Limited Visibility)
    * User registration.
    * User login.
* Spaced Repetition (In Progress):

    * The foundation for spaced repetition logic exists in the API (placeholder functions).
    * SM2 Algorithm needs full implementation.

# To Be Implemented

* Detailed SM2 Implementation:
    * calculateNextInterval, calculateNextReviewDate, calculateEasinessFactor functions within your API.
* Frontend Integration of Spaced Repetition:
    * Send the quality rating (0-5) from the frontend during word reviews.
    * Update how words are fetched for flashcard exercises (fetch words due for review).
* Review Queue: Design and implement the ReviewQueue component.
* User Progress:
    * Displaying learned words.
    * Potentially: Stats or visualizations of a user's progress.

# Additional Considerations

* Error Handling: Implement robust error handling on both frontend and backend.
* UI/UX Enhancements: Focus on improving the overall user experience of the application (styling, feedback mechanisms, etc.).
* Advanced Features (Optional):
    * Audio pronunciation
    * Text-to-speech for pronunciation assistance
    * Image association with words
    * Quiz or game-like review modes
