# Croatian Tutor — GitHub persistence test

This repository is a minimal proof of concept for a portable Croatian tutor.

## Goal
The tutor should work across chats, accounts and model providers. Conversations are ephemeral; learning state is permanent.

## What this test proves
- Curriculum/context can live in GitHub.
- A tutor can read the learner profile and current state before a lesson.
- Every learning attempt can be stored as an append-only event.
- A derived progress file can be updated after a session.
- Another model/session can continue from the repository state.

## Minimal workflow
1. Read `AGENTS.md`, `learner/profile.md`, and `state/progress.json`.
2. Teach/review according to the due items and current focus.
3. Ask the learner to actively produce Croatian, not only recognize it.
4. Give concise corrective feedback.
5. Write one new event under `events/`.
6. Update `state/progress.json` with the new derived state.

This is intentionally small. It tests the architecture, not the full textbook curriculum.
