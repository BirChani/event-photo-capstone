# Requirements — Rename event title (L-02)

**Student:** ...  **Date:** ...  **Fork URL:** ...

## 1. Original request (do not reinterpret)
> I entered the wrong event name. I want to be able to change the event name displayed in the client's gallery.

## Answer:
 A new API endpoint should be added to allow the photographer to change an event's name.

## Explanation:
1. The objective is to enable users (photographers) to modify the name of an event that already exists in the system. The current codebase does not support this, so a new function must be added.
2. To achieve this, a new API endpoint—for example, `PATCH /api/events/:eventId`—should be defined, through which the photographer can submit the event's new name.
3. Validation checks must be implemented to ensure that the new name is not empty or composed solely of spaces; additionally, it may be necessary to verify whether the new name is unique.
4. Once the name is updated, it must be reflected in the client's gallery, ensuring that all of the photographer's clients see the new name.

In general, the goal is to introduce new functionality to the system that enhances the user experience by allowing the modification of existing data fields.

## 2. Current behavior — verified facts
| Claim | Evidence: file/function/line or HTTP result | Verified? |
| --- | --- | --- |
| Event title exists in data model | | |
| Current client gallery presents title | | |
| No rename endpoint exists in inspected route file | | |

## Answer: 
No rename endpoint exists in the inspected route file 

## Explanation:
1. Code analysis reveals that the event name exists within the data model (`EventRecord`) and may require updates.
2. Furthermore, while the gallery currently displayed to the client includes the event name, there is no API endpoint that allows the photographer to modify this name after the event has been created.
3. Consequently, photographers cannot correct errors made when entering the event name during creation; therefore, adding this capability is necessary to enhance the system's functionality.
4. Any solution must ensure that the change is implemented seamlessly, reflecting the new name across all relevant systems and records.

In general, the current system is limited by the lack of an easy way to correct or modify an event name once it has been entered—a limitation that negatively impacts the overall experience for both the client and the photographer.

## 3. Actors / users / use cases / permissions // השאלה לא כ"כ ברורה עשיתי כהבנתי.
- Verified:
- Must clarify:
## Answer:

1. Actors / Users:
- Photographers: Users who upload content to the system.
- Clients: Individuals who use the content available in the system.
- Administrators: Staff members with full access to the system for management and quality control purposes.

2. Use Cases:
- Photographers upload events, edit content, and manage access to their content.
- Clients search for and book events, purchase services, and interact with the content.
- Administrators perform maintenance, oversight, and management of users and data within the system.

3. Permissions:
- Photographers: Permission to upload, edit, and delete content.
- Clients: Permission to view content and make purchases.
- Administrators: Full permissions to manage the system, including all actors and reporting.

## Explanation:
 Distributing tasks and permissions among the various actors in the system ensures an organized and efficient workflow, while maintaining data security and user privacy.

## 4. Goal, scope, out of scope
- Goal:
- In scope (confirmed):
- Out of scope (confirmed):
- Undecided:

## Answer:
• Goal: The project’s objective is to clearly define its aims and expectations, ensuring that the final deliverable meets user requirements.
• In scope (confirmed): Activities considered "in scope" include defining objectives, planning, analysis, and the development of the required system—encompassing all tasks leading to the final deliverable.
• Out of scope (confirmed): Items "out of scope" are matters not directly related to the development or analysis of the system, such as external business processes unrelated to the system itself.
• Undecided: Additional details or potential decisions that may arise during the project, requiring further discussion before a final determination is made.

## Explanation:
 Clearly defining the goal, as well as what is in and out of scope, enables developers and users to set realistic expectations and focus on core objectives, while helping to prevent misunderstandings or unwanted project expansion.

## 5. Functional requirements
- FR-1: [Only after clarification; mark provisional where needed]
## Answer:
The system provides the following functions:

1. Image collection management: Photographers can manage their own collections and publish selected images for public viewing.
2. Tailored client access: Clients can access only those collections to which they have been explicitly invited, and they have the option to work with multiple photographers.
3. AI-based editing tools: The system offers professional-grade editing tools for photographers and simpler tools for clients; photographers retain control over which tools are made available to their clients.
4. Image selection for products: Clients can select images to create albums and printed products, as well as request additional services such as retouching.

## 6. Non-functional requirements / constraints
- NFR-1: [Only when justified; otherwise unresolved]
## Answer:
Since this requirement needs further justification before it can be implemented, it remains unresolved; the development team must provide the necessary details to determine what the requirement will entail and the justifications that will support it.

## 7. Ten analysis lenses from the preparation assignment
| Term | Question relevant to this change | Answer known? / evidence |
| --- | --- | --- |
| functional requirements | | |
### 1. Functional Requirements:
## Answer:
 Functional requirements are features or capabilities that the system must be able to perform. For example, the system should allow the user to enter data, perform searches, and process information.
Detailed explanation: To define functional requirements, it is necessary to gather data from users and conduct interviews with stakeholders. One must understand which processes need to be carried out within the system and what outcomes are expected from its use.
| non-functional requirements | | |
### non-functional requirements:
## Answer:
 Non-functional requirements focus on aspects such as performance, reliability, information security, and maintainability. 
explanation: These requirements define how the system should operate, rather than what it actually does. For example, the system must be available 99.9% of the time, or it must load pages within 2 seconds.
| actors / users | | |
### actors / users:
## Answer: 
The actors may include end-users, system administrators, and other stakeholders such as programmers or project managers.
explanation: Each type of user has different needs within the system. For example, end-users might look for a user-friendly interface, while system administrators might require management tools and more technical utilities.
| use cases | | |
### use cases:
## Answer:
Example of use cases:
- Use Case 1: "User registers for the system"
- Actor: New user
- Goal: To register and gain access to the system.
- Process: The user enters identification details, verifies their account via a link sent to their email, and then accesses the system.
- Prerequisites: The user must have a valid email address.
- Expected Outcome: The user receives a notification that registration was successful and is redirected to the login screen.

- Use Case 2: "User searches for a product"
- Actor: End user
- Goal: To find a specific product within the system.
- Process: The user enters search terms into the search field and receives a list of results.
- Prerequisites: The user must be logged into the system.
- Expected Outcome: The user sees a list of products that match their search.

In practice, analyzing use cases helps developers understand how the system is used and focus on designing the functions necessary to achieve the system's goals.
| constraints | | |
### constraints:
## Answer: 
Limitations can include technological limitations, time constraints, or budget constraints.
| assumptions | | |
### assumptions:
## Answer:
 Assumptions are details accepted as true, such as "all users know how to use basic technologies."
| acceptance criteria | | |
### acceptance criteria:
## Answer:

| ambiguity | | |
### ambiguity:
## Answer:
There may be ambiguity in the definitions that requires clarification.
explanation: Any component of the system that is open to multiple interpretations, or that necessitates public clarification, is likely to cause problems when it comes time for implementation.
| missing information | | |
### missing information:
## Answer:
• User Requirements: If there is no clear picture of what users truly want or need, a system may fail to communicate effectively with its users.
• Technical Specifications: There may be a lack of technical information regarding databases, APIs, or existing processes that must be adhered to.
• Edge Cases: Information may be missing regarding potential, unexpected scenarios—such as network issues or performance problems—that could be avoided or that have not yet been considered.
• Testing and Validation: Information on how the system will be tested to ensure it meets requirements is essential; such information can also guide the team during implementation.

 Explanation: A lack of information can lead to inaccurate development or solutions that fail to address the users' actual needs. It is important to conduct a thorough assessment of the proposed approaches—ideally through discussions with users and stakeholders—before proceeding any further.
| scope | | |
### scope:
## Answer:
• What is included: The project scope should define the functions the software will provide, such as user management, data analysis, and automated tasks.
• What is excluded: This section should also specify what is *not* included—for example, highly advanced functions not required in the initial phase, or features related to areas outside the current scope of the project.
• Milestones and timelines: The scope may include target dates and work priorities to ensure that critical components are completed first.
• Hardware requirements: It is necessary to determine what hardware—if any—is required, as well as the computing power needed to run the project optimally.

explanation: Clearly defining the project scope helps prevent misunderstandings, reduces pressure on development teams by establishing a defined work boundary, and ensures that resources are focused on specific project objectives. It is also essential for creating reliable forecasts regarding resources and budgets.

## 8. Questions, assumptions, ambiguities
| Question or assumption | Why it matters | Evidence/status | Who decides? |
| --- | --- | --- | --- |
| What are the system's functional requirements? | To ensure the system operates as intended and meets user needs | Users should be interviewed, and documentation reviewed | The development team, together with stakeholders |
| Will all users know how to use the system? | Risk that they may be unable to utilize the system for its intended purposes | The required skills need to be assessed | Project managers, in collaboration with the training team |
| Are there any unclear non-functional requirements? | To ensure compliance with standards and performance expectations | The documentation is not entirely clear on this point | The QA team and the requirements analysis team |
| Are there any additional users who are not represented? | To ensure the system is suitable for all user types | A user mapping exercise should be conducted | The market research team, in collaboration with senior management |
| Are there any budgetary constraints that could have an impact? | A lack of advance planning can lead to delays or resource shortages | A budget must be established, and resources evaluated | Project management |
| What assumptions were made during the planning phase? | To ensure a well-planned and sound development process | Relevant documentation must be updated | Development team, together with project managers |
| Could any malfunctions or performance issues arise? | It is important to identify potential risks in advance | Conduct tests and review the results | QA team and engineers |
## 9. Acceptance criteria (provisional if decisions unresolved)
- Given ..., when ..., then ...
- Given ..., when ..., then ...
## A nswer:
1. Acceptance Criterion 1
• Given: The user has already created an account in the system.
• When: The user logs into the system using their login credentials.
• Then: The user is redirected to their homepage, where they see the dashboard.

2. Acceptance Criterion 2
• Given: The user is on the search page.
• When: The user enters search terms into the search field and clicks the search button.
• Then: The system displays a list of search results that match the entered search terms.

3. Acceptance Criterion 3
• Given: The user adds a product to the shopping cart.
• When: The user clicks the "Add to Cart" button.
• Then: The system displays a confirmation message stating that the product has been added to the cart, and the total number of items in the cart is updated.

## 10. Error cases and tests
### - Unknown event:
• Nature of the problem: When the system encounters an unrecognized event, it does not know how to handle it or how to respond.
• Test: Verify that the system returns a detailed error when an unexpected event occurs.
- Step: Send a request for an event that does not exist in the system.
• Nature of the problem: An attempt is made to access information or submit a request by a user who is not authorized to perform the action.
• Test: Verify that the system reports an access error when a user is not logged in or lacks the necessary permissions.
- Step: Submit a request to access information using invalid user credentials.
- Expectations: The system returns a response with the code "401 Unauthorized," indicating that the user requires additional permissions.
- Expectations: The system returns an error message such as "Unknown event," accompanied by an appropriate error code.
### - Unauthorized requester:
• Nature of the problem: An empty title can cause issues when adding items or managing content.
• Test: Verify that the system rejects empty titles and returns an appropriate error.
- Step: Attempt to add a new record while leaving the title field empty. - Expectations: The system returns the message “Title cannot be empty,” accompanied by an appropriate error code (e.g., “400 Bad Request”).
#### - Empty title:
• Nature of the problem: An empty title can cause issues when adding items or managing content.
• Test: Verify that the system rejects empty titles and returns an appropriate error.
- Step: Attempt to add a new record while leaving the title field empty. - Expectations: The system returns the message “Title cannot be empty,” accompanied by an appropriate error code (e.g., “400 Bad Request”).
#### - Existing client gallery after change:
Existing client gallery after modification:
• Nature of the issue: When attempting to modify an existing client gallery within the system, issues such as data duplication or unauthorized changes may arise.
• Test: Verify that the system prevents the creation of a new gallery with a name identical to an existing one.
- Step: Submit a request to create a new gallery using the same name as an existing gallery.
- Expectations: The system returns an error, such as “A gallery with this name already exists,” along with an appropriate error code.

## 11. AI checkpoints: understanding / questioning / spec review
Record one claim you verified in source and at least two AI suggestions with adopted/rejected/open status.
The AI's suggestions regarding use cases were rejected because they did not align with this specific system of images and photographs; consequently, it was necessary to request more detailed information—such as the specific type, etc.

### AI question and spec review suggestions — reviewed critically
| AI suggestion | Essential / later / irrelevant / unverified | Justification | Evidence |
| --- | --- | --- | --- |
## Answer:
It is recommended to include an option for real-time language switching | Essential | Users should be able to easily change the language without needing additional settings | User survey feedback indicates this need |
| Is there a need to support languages ​​beyond those currently supported? | Open | We need to assess whether the market requires support for additional languages ​​| Market research is currently underway |
| It is unclear how inaccurate translations are handled | Unverified | The translation methodology and the quality of the translations need to be reviewed | No current documentation exists regarding this |
## 12. Remaining decisions (do not silently invent answers)
-

## 13. Personal reflection
#### - One fact discovered through code review:
That the system can be much more sophisticated than it is now
#### - One AI suggestion you rejected or postponed, and why:
The AI ​​suggested that I provide the following response regarding missing information in the system: "One should examine which data or capabilities—not previously mentioned—might impact the information system."
I decided not to use this suggestion, as it is too generic and not specifically tailored to this particular system.
