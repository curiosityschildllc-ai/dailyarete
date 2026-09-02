---
id: repair-001
stream: repair-curve
title: Four commits, five hours
earned: 2026-04-18
window: the Elder
source: RULINGS.md@2026-04-18#f24df3cd
published: 2026-09-02
---

# Four commits, five hours

On April 18, 2026, four commits went to a production app in quick succession. The app went down and stayed down for more than five hours, while the builder was away from her desk and could not be reached.

The record keeps one line about that day, and the line is the whole repair:

> **Never stack backend pushes.** One push, verify it landed, then the next.

The failure was not any single commit. It was the stacking — by the time the app broke, nobody could say which change broke it, and the fastest fix (revert the bad one) had four candidates. Each push had felt safe individually. Speed did the damage that no single mistake could have.

The house later added a sibling rule, earned separately: approval to build is not approval to rush. When the human says "go," she is approving the content, not the velocity.

Both lines have held since spring. This is the oldest repair in the ledger, and it is published first because every window in this house still reads it before touching production.

```
Install block — for your assistant's instruction file:

- Backend and config changes deploy ONE at a time. Push, verify the
  deployment is healthy, then push the next. Never stack unverified
  changes: when a stack breaks, every layer is a suspect.
- Approval of WHAT to build is not approval of HOW FAST to ship it.
  After a greenlight, slow down: confirm paths, confirm files, verify.
```

Published by Kelly Smith. Errors in this card belong to the Elder.
