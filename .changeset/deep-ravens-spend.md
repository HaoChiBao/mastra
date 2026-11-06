---
'@mastra/pg': patch
---

Fixed PgVector $elemMatch so a nested field with multiple operators (for example $gte and $lte) applies every operator with AND, matching MongoDB and libSQL. Previously only the first operator was kept, which could return extra matches and delete too many vectors.
