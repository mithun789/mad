# IT2010 - MOBILE APPLICATION DEVELOPMENT
## FINAL EXAMINATION - SAMPLE PAPER

**Duration:** 2 Hours  
**Total Marks:** 100  
**Instructions:**
- This is a computer-based examination via NetExam
- All tutorial materials will be available during the exam
- One A4 reference sheet is allowed (printed or handwritten)
- Answer ALL questions
- Read questions carefully before answering

---

## QUESTION 01 - Knowledge Assessment (25 Marks)

### Part A: Multiple Choice Questions (10 Marks)
Select the correct answer(s). Each question carries 1 mark.

**1.** Which layer of Android architecture contains hardware drivers like camera and keyboard?
- A) Application Framework
- B) Libraries
- C) Linux Kernel
- D) Android Runtime

**2.** What is the correct sequence of Activity lifecycle methods when an app is launched?
- A) onCreate() → onStart() → onResume()
- B) onStart() → onCreate() → onResume()
- C) onCreate() → onResume() → onStart()
- D) onResume() → onStart() → onCreate()

**3.** Which of the following are advantages of using Fragments? (Select all that apply)
- A) Better memory management
- B) Easier data sharing with ViewModel
- C) Smoother navigation
- D) Automatic database synchronization

**4.** In the 60-30-10 color rule for UI design, what does the 10% represent?
- A) Background color
- B) Primary color
- C) Accent color for highlights and buttons
- D) Text color

**5.** Which keyword is used to declare a nullable variable in Kotlin?
- A) null
- B) ?
- C) nullable
- D) var?

**6.** What is the purpose of the R.java file in Android?
- A) Contains all Java code
- B) Contains resource IDs for all resources
- C) Runs the application
- D) Manages database connections

**7.** Which method is called when an Activity is no longer visible to the user?
- A) onPause()
- B) onStop()
- C) onDestroy()
- D) onInvisible()

**8.** What is the main difference between Dalvik Virtual Machine (DVM) and Android Runtime (ART)?
- A) DVM uses AOT compilation, ART uses JIT
- B) DVM uses JIT compilation, ART uses AOT
- C) DVM is faster than ART
- D) There is no difference

**9.** Which type of Intent specifies the component to start by name?
- A) Implicit Intent
- B) Explicit Intent
- C) Direct Intent
- D) Named Intent

**10.** In RecyclerView, which method determines how many items are in the list?
- A) getItemCount()
- B) getListSize()
- C) getItemSize()
- D) getTotalItems()

---

### Part B: Short Answer Questions (15 Marks)
Type your answer in the provided text box. Each question carries 1.5 marks.

**1.** What does AAPT stand for in Android development?

**2.** Name the method used to attach an observer to LiveData in an Activity.

**3.** Which Kotlin keyword is used to declare a variable whose value never changes?

**4.** What is the default orientation of LinearLayoutManager in RecyclerView?

**5.** Name the Activity lifecycle method called before the activity is destroyed.

**6.** What annotation is used to mark a function in Room DAO for inserting data?

**7.** In Form Validation, what sealed class state represents successful validation?

**8.** Which Android component is used to perform long-running background tasks?

**9.** What method is called when a Fragment's view is created?

**10.** According to UI/UX principles, which user group represents the majority and should be the primary focus? (Experts/Mainstreamers/Early Adopters)

---

## QUESTION 02 - UI/UX Design and Analysis (25 Marks)

**Note:** This question requires written explanations only. No coding or XML is required.

### Scenario:
You are designing a **Grocery Shopping Mobile App** for a supermarket chain. The app will be used by diverse customers including elderly users, busy professionals, and tech-savvy young adults. The app needs features like product browsing, shopping cart, order tracking, and payment.

**a)** The design team is debating between two approaches:
- **Approach A:** A feature-rich dashboard showing 12 different options (Weekly Deals, Categories, Search, Cart, Orders, Favorites, Recipes, Store Locator, Customer Service, Loyalty Points, Notifications, Settings)
- **Approach B:** A simple home screen with 4 core features (Search Products, View Cart, My Orders, Categories) with other features accessible through a menu

Critically evaluate both approaches considering:
- Target user groups (mainstream vs expert users)
- Mobile usage environments (shopping while in-store, at home planning)
- UI simplicity principles
- User emotional needs (feeling organized, not overwhelmed)

**Recommend the most suitable approach and justify your decision.** (10 Marks)

---

**b)** For the recommended approach, discuss how you would apply the **60-30-10 color rule** to design the app's color scheme. Consider:
- What the primary color (60%) should represent
- Where the secondary color (30%) should be used
- Purpose of the accent color (10%)
- How color choices affect user experience in a grocery shopping context

(7 Marks)

---

**c)** The app will display product listings. List and justify **FIVE appropriate UI elements** you would use for each product card in the listing. Consider elements for:
- Product information display
- User interaction (adding to cart, favorites)
- Visual appeal
- Accessibility

Explain why each element is necessary for a good user experience. (8 Marks)

---

## QUESTION 03 - Kotlin Development and Form Validation (25 Marks)

**Note:** Tutorial materials are available for reference during the exam.

**a)** Create a Kotlin data class named `Product` for the grocery shopping app with at least 5 properties that represent a product (e.g., product ID, name, price, category, stock quantity). Use appropriate data types. (5 Marks)

---

**b)** Define a Kotlin sealed class `OrderStatus` to represent three different states of an order:
- **Pending** (order received but not processed)
- **Shipped** (order dispatched with tracking number)
- **Delivered** (order completed with delivery date)

Then, write a function `getOrderStatusMessage()` that takes an OrderStatus parameter and returns an appropriate message string for each status type. (10 Marks)

---

**c)** You are implementing a checkout form where users enter their delivery details. Create a validation class that validates:

- **Phone Number:** Must not be empty, must start with "07", and must be exactly 10 digits
- **Address:** Must not be empty and must have at least 10 characters
- **Postal Code:** Must not be empty and must be exactly 5 digits

Use the `ValidationResult` sealed class pattern from the Form Validation tutorial:
```kotlin
sealed class ValidationResult {
    data class Empty(val errorMessage: String) : ValidationResult()
    data class Invalid(val errorMessage: String) : ValidationResult()
    object Valid : ValidationResult()
}
```

Write the validation class with three validation functions (one for each field). Include function headers and complete implementation. (10 Marks)

---

## QUESTION 04 - Kotlin Development and RecyclerView (25 Marks)

**Note:** Tutorial materials are available for reference during the exam.

**a)** You need to display a list of orders in the grocery app. Each order item should show:
- Order ID
- Order date
- Total amount
- Order status
- A "View Details" button

Create a data class `Order` with appropriate properties for the above information. (5 Marks)

---

**b)** Implement a `RecyclerView.Adapter` class named `OrderAdapter` to display the list of orders. Your implementation should include:

- ViewHolder inner class with view references
- Constructor that takes a list of orders and a click listener for the "View Details" button
- Override `onCreateViewHolder()` method
- Override `onBindViewHolder()` method to bind order data
- Override `getItemCount()` method
- Handle the "View Details" button click event

You may assume the layout file is named `item_order.xml` with appropriate view IDs. (12 Marks)

---

**c)** Implement a `ViewModel` class named `OrderViewModel` that:
- Uses Room DAO to fetch orders from the database
- Provides a function to get all orders sorted by date (most recent first)
- Returns data as `LiveData<List<Order>>`

Assume you have a DAO interface with a function:
```kotlin
@Query("SELECT * FROM orders ORDER BY orderDate DESC")
fun getAllOrdersSortedByDate(): LiveData<List<Order>>
```

Show how the ViewModel would use this DAO function. (8 Marks)

---

## END OF EXAMINATION

**Good luck!**

---

### Answer Space Guidelines:
- Part A MCQs: Select from dropdown/radio buttons
- Part B Short Answers: Text input box (single line)
- Questions 2, 3, 4: Multi-line text editor with syntax highlighting for code

### Time Management Suggestion:
- Question 1: 25-30 minutes
- Question 2: 35-40 minutes  
- Question 3: 25-30 minutes
- Question 4: 25-30 minutes
- Review: 5-10 minutes