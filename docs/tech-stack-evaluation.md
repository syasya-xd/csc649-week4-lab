# Tech Stack Evaluation

## Project
AI Assisted Virtual Wardrobe and Personalised Outfit Recommendations System using Deep Learning

## Requirements that drive the decision

- FR1: The system shall allow users to add clothing items by capturing or uploading clothing images and storing them in their digital wardrobe.
- FR4: The system shall analyse clothing compatibility and colour characteristics, including skin-tone-aware colour compatibility, to generate suitable outfit combinations from the user's digital wardrobe.
- FR5: The system shall generate and rank personalised outfit recommendations using the proposed hybrid recommendation algorithm and allow users to save their preferred outfit combinations.
- NFR1: The system shall display the result of a clothing classification request within 5 seconds under normal network and device conditions.
- NFR3: The system shall provide an easy-to-use mobile interface that allows users to complete common tasks, such as adding clothing and viewing recommendations, with minimal navigation.

## Options

- Option A: Flutter mobile application + Firebase (Authentication, Firestore and Storage) + TensorFlow Lite for on-device clothing classification
- Option B: Flutter mobile application + Python FastAPI backend + PostgreSQL database + deep-learning model hosted on the backend
- Option C: React Native mobile application + Supabase (PostgreSQL, Authentication and Storage) + Python FastAPI backend for AI processing

## Decision matrix
Weight: how important the criterion is for YOUR project (1 = low, 5 = high).
Score: how well each option does (1 = poor, 5 = excellent).
Weighted score = weight x score. Add them up for each option.

| Criterion                         | Weight | A score | B score | C score |
|-----------------------------------|--------|---------|---------|---------|
| Fits my requirements              | 5      | 4       | 5       | 5       |
| Skills I already have             | 3      | 3       | 4       | 2       |
| Time to build before my deadline  | 5      | 4       | 3       | 3       |
| Free hosting and tools            | 4      | 5       | 4       | 5       |
| Performance and security needs    | 4      | 4       | 5       | 5       |
| Room to grow later                | 3      | 4       | 5       | 5       |
| **Total (weighted)**              |        | **97**  | **103** | **101** |

## Decision record

- **Context:** The project requires a mobile application that can manage clothing images, classify clothing items, store user preferences, and generate personalised outfit recommendations using deep learning. The system also needs to meet the required performance, usability and security requirements within the available FYP development time and budget.

- **Decision:** I chose **Option B: Flutter mobile application + Python FastAPI backend + PostgreSQL database + deep-learning model hosted on the backend**.

- **Reasons:** Option B achieved the highest weighted score of **103** in the decision matrix. It fits the project requirements well because Python provides a suitable environment for implementing the deep-learning clothing classification and personalised outfit recommendation components. The separate backend also provides flexibility for developing and improving the recommendation algorithm.

- **Consequences:** This option makes the development and modification of the AI and recommendation components easier because they can be handled separately from the mobile application. However, developing and maintaining a separate backend, database and mobile application makes the overall system more complex and increases the development workload.

- **Risks and next review:** The main risk is that developing and deploying a separate backend may require more time and technical effort than expected. If backend development becomes too difficult or threatens the FYP deadline, I will reconsider the technology stack and evaluate whether a simpler option would be more suitable.