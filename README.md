# Requirement Analysis in Software Development.

This repository is dedicated to exploring the critical phase of Requirement Analysis in the software development lifecycle. Requirement Analysis involves understanding, documenting, and managing the expectations of stakeholders for a software project.

## What is Requirement Analysis?

Requirement Analysis is a fundamental phase in the Software Development Lifecycle (SDLC) that involves gathering, evaluating, and documenting the needs and expectations of stakeholders for a software system.
It sets the foundation for the project, ensuring the development team understands what needs to be built, why, and how it aligns with business goals.

## Why is Requirement Analysis Important?

- Clarity and Understanding: It helps in understanding what the stakeholders expect from the software, reducing ambiguity.
- Scope Definition: Clearly defines the scope of the project, which helps in preventing scope creep.
- Basis for Design and Development: Provides a solid foundation for designing and developing the system.
- Cost and Time Estimation: Facilitates accurate estimation of project cost, resources, and time.
- Quality Assurance: Ensures that the final product meets the specified requirements, leading to higher customer satisfaction.

## Key Activities in Requirement Analysis

1. **Requirement Gathering 🗂️**

- Interviews: Conducting interviews with stakeholders to gather detailed information about their needs and expectations.
- Surveys/Questionnaires: Distributing surveys to collect requirements from a larger audience.
- Workshops: Organizing workshops with stakeholders to discuss and gather requirements.
- Observation: Observing end-users in their working environment to understand their needs.
- Document Analysis: Reviewing existing documentation and systems to understand current functionalities and requirements.

2. **Requirement Elicitation**

- Brainstorming: Conducting brainstorming sessions to generate ideas and gather requirements.
- Focus Groups: Holding focus group discussions with selected stakeholders to gather detailed requirements.
- Prototyping: Creating prototypes to help stakeholders visualize the system and refine their requirements.

3. **Requirement Documentation**

- Requirement Specification Document: Creating a detailed document that lists all functional and non-functional requirements.
- User Stories: Writing user stories to describe functionalities from the user’s perspective.
- Use Cases: Creating use case diagrams to show interactions between users and the system.

4. **Requirement Analysis and Modeling 📊**

- Requirement Prioritization: Prioritizing requirements based on their importance and impact on the project.
- Feasibility Analysis: Assessing the feasibility of requirements in terms of technical, financial, and time constraints.
- Modeling: Creating models (e.g., data flow diagrams, entity-relationship diagrams) to visualize and analyze requirements.

5. **Requirement Validation ✅**

- Review and Approval: Reviewing the documented requirements with stakeholders to ensure accuracy and completeness.
- Acceptance Criteria: Defining clear acceptance criteria for each requirement to ensure they meet the expected standards.
- Traceability: Establishing traceability matrices to ensure all requirements are addressed during development and testing.

## Types of Requirements

- ## **Functional Requirements**
  Definition: Describe what the system should do.
  **Example from Case Study**

1. **Hotel Management Service**

Requirement: Allow hotel managers to update their hotel information, such as room availability, pricing, and offers.
Example: A manager updates the price for deluxe rooms in their hotel via the Hotel Management Portal.

2. **Customer Service**

Requirement: Enable customers to search for hotels based on location, availability, and preferences.
Example: A customer searches for hotels in "New York" with check-in and check-out dates.

3. **View Booking Service**

Requirement: Provide customers and hotel managers access to booking history, including past and current bookings.
Example: A customer checks their booking details for a stay in a hotel next month.

- ## **Non-Functional Requirements**
  Non-functional requirements define the quality attributes or constraints of the system. They focus on how the system performs its functions rather than the specific functionalities.

1. **Performance**

- Requirement: The system should handle up to 1 million API requests per second to manage high traffic during peak hours.
- Example: During a holiday sale, the system efficiently handles thousands of concurrent hotel bookings.

2. **Scalability**

Requirement: The system should scale horizontally by adding more servers to the load balancer.
Example: As user traffic increases, new servers are added to the cluster to handle additional requests.

3. **Reliability**

Requirement: Ensure data consistency between the master and slave databases.
Example: Updates made to the master database (e.g., room availability) are reflected in slave databases without delay.

4. **Security**

Requirement: All sensitive user data, such as payment details, must be encrypted during transmission and storage.
Example: Payment information is encrypted using SSL/TLS protocols to prevent unauthorized access.

5. **Response Time**

Requirement: APIs must respond within 200 milliseconds for all customer-facing services.
Example: When a user searches for a hotel, the results are displayed within 200ms.

6. **Maintainability**

Requirement: The system should allow seamless updates without downtime.
Example: A new feature is deployed to the Hotel Management Service without interrupting ongoing usage.

7. **Data Retention and Archiving**

Requirement: Archive old booking data into Cassandra for historical analysis and reduce database load.
Example: Booking records older than one year are automatically moved to Cassandra for archival purposes.

8. **Big Data Analysis**

Requirement: Use Hadoop to analyze booking patterns and customer preferences.
Example: The system identifies frequent travelers to New York and targets them with promotional offers.

## Use Case Diagrams

**What Are Use Case Diagrams?**
Use Case Diagrams are visual representations of the interactions between users (actors) and a system. They provide a high-level overview of the system's functionality by illustrating the relationships between various actors and their associated actions (use cases).

**Benefits of Use Case Diagrams:**

- Clear Communication: They help stakeholders understand the system's scope and interactions without technical complexity.
- Requirement Validation: Aid in verifying that all functional requirements are addressed.
- Simplified Design: Provide developers with a visual guide for implementing features and user interactions.
- Documentation: Serve as a useful reference throughout the software development lifecycle (SDLC).

**Use Case Diagram for the Booking System**
Below is a use case diagram for a booking management system, illustrating interactions between users and the system.

![useCase](/alx-booking-uc.png)

## Acceptance Criteria.

Acceptance criteria are conditions that a feature must meet to be accepted by the stakeholders.

### Benefits of Acceptance Criteria:

- Ensure all parties have a clear understanding of feature requirements.
- Provide a basis for testing and validation.
- Help in maintaining quality and meeting user expectations.

### Acceptance Criteria of Feature: Checkout

1. **Successful Checkout Process**

- Given: A user has selected a room and added it to the cart.
- When: The user clicks the "Checkout" button and provides all necessary information.
- Then: The system processes the booking, confirms payment, and displays a booking confirmation page with the booking ID.

2. **Validation of Required Fields**

- Given: A user is on the checkout page.
- When: The user submits the form without completing required fields (e.g., name, email, payment details).
- Then: The system displays appropriate validation error messages for each missing or invalid field.

3. **Payment Integration**

- Given: The user selects a payment method (e.g., credit card, PayPal).
- When: The user submits their payment details.
- Then: The system communicates with the payment gateway, validates the payment, and displays a success or failure message based on the result.

4. **Booking Confirmation**

- Given: The payment is successful.
- When: The system confirms the booking.
- Then: The user receives a confirmation page with:
  Booking ID
  Booking details (e.g., room type, dates, guest details)
  Payment summary
  An option to download or email the receipt.

5. **Cancellation Option**

- Given: The booking has been successfully created.
- When: The user views the confirmation page or their booking history.
- Then: The system provides an option to cancel the booking based on the cancellation policy.
