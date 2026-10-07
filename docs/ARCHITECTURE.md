# Architecture overview

The app separates the public learning experience from backend orchestration and storage.

| Layer | Responsibility |
|---|---|
| Lovable frontend | Topic and interest inputs, learning cards, interactive quiz, feedback |
| Private application server | Validate requests and communicate with the retained backend |
| Apps Script backend | Enforce the shared demo allowance and handle feedback |
| Activepieces workflow | Coordinate Explainer, Critic, and Rewrite stages |
| Gemini | Generate and refine explanations |
| Google Sheets | Store request, output, quality-review, and feedback records |

The Explainer creates an initial learning card. The Critic reviews clarity, accuracy, analogy fit, usefulness, engagement, and safety. The Rewrite stage improves the final response using that review.

The static sample is rendered locally and makes no model request. User feedback belongs to a generated learning card so product observations remain tied to the corresponding explanation.

This public overview intentionally omits implementation source, private backend addresses, operational identifiers, and configuration values.
