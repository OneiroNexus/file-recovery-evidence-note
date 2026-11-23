# Recovery Compass

**What a second observation can establish after a file transfer**

**Aaron Michael Weis** · Oneiron Holdings LLC · [ORCID](https://orcid.org/0009-0002-1906-148X)  
Technical note · source draft dated 10 November 2026 · public research edition v0.1.0

## Abstract

After a folder move, a familiar name can conceal a stale copy, an unreadable file, or a missing subdirectory. This note separates three observations about an ordinary file: where it was expected, what bytes were observed there, and what remained unread. It illustrates how that distinction changes a transfer report. The examples are fictional. The note describes an interpretation of evidence and leaves recovery choices to the file owner.

## Four observations from one move

Imagine moving a project containing a sketch, a budget, an audio take, and a long recording. A second inspection finds the following.

| Expected item | Observation at the destination | What the owner can conclude |
|---|---|---|
| Sketch | The expected relative path contains the same bytes as the retained reference. | A matching copy was observed at that path during inspection. |
| Budget | The path exists, but its content differs. | There is a conflict to resolve. The evidence does not select the authoritative version. |
| Audio take | The expected path is absent. Matching content appears under another name. | The second path is a candidate copy. It could also be a duplicate created earlier. |
| Long recording | A read failed during the check. | The content comparison is incomplete. The file stays on the follow-up list. |

A path answers where the program looked. A content fingerprint describes the bytes the program could read. The history of how those bytes arrived is another question. Keeping the three separate lets an owner investigate the budget and recording without reopening an entire transfer.

## What counts as complete

State the source and destination, the time of observation, which entries were in scope, and which checks failed. A report about ordinary files’ main byte streams has a limited reach. It cannot by itself establish that permissions, alternate streams, directory links, special files, or application state survived. Files changing during a scan make its observation time material. An unreadable path should never add to a count of successfully verified files.

A digest comparison is especially useful when followed by a decision appropriate to the evidence. A match elsewhere can justify inspecting that candidate. Only the owner can say whether a differently named copy belongs to the same history or which conflicting version to keep.

## A small evaluation

A reproducible evaluation can start with four invented files matching the table. Establish the expected result before running a candidate verifier. Test whether it distinguishes same-path matches from different-path candidates, preserves conflicts, and accounts for read failures. Report operating system, filesystem and tested file types. A fixture without an actual read error cannot support a claim about error handling. Large files and filesystem-specific behavior need separate observations.

The practical stopping rule is simple. Finish the comparison for one transfer, preserve the unresolved list, and let the owner choose what to inspect next. That list can be a valuable result even when some files remain unread.

## Contributions and scope

Aaron Michael Weis conducted the underlying work and developed the reporting approach. The source note was prepared with AI assistance. Codex edited this paper-only edition. It uses fictional examples and reports no recovery rate or deployment result. [Paper license](LICENSE)
