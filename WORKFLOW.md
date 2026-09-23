# Git Catalog Sync Workflow

Name: Jayross P. Versales

## Task 1 – Create and Push the Grace Period Change
Updated `catalog.js` on the `feature/late-fee-policy` branch to add a 1-day grace period before late fees apply. Tested the change, committed it, and pushed it to the remote repository.

Evidence: `screenshots/task1.png`

## Task 2 – Simulate a Concurrent Change
Using Clone B, changed the late-fee calculation from `Math.floor()` to `Math.round()`. After committing the change, the push was rejected because the remote branch already contained newer changes.

Evidence: `screenshots/task2.png`

## Task 3 – Resolve the First Conflict
Integrated the remote grace-period change with the local rounding change. The conflict in `catalog.js` was manually resolved so that both changes were preserved. Tests passed before committing and pushing the merged result.

Evidence: `screenshots/task3.png`

## Task 4 – Create Another Concurrent Change
Using Clone C, added a maximum late-fee cap of $20. The local change was committed, but the first push was rejected because the remote branch had newer commits.

Evidence: `screenshots/task4.png`

## Task 5 – Resolve the Second Conflict
Resolved the conflict by combining the 1-day grace period, rounded late-fee calculation, and $20 maximum fee cap. The combined behavior was tested successfully before committing and pushing.

Evidence: `screenshots/task5.png`

## Task 6 – Rebase the Minimum Fee Change
Added a minimum late fee of $1 and rebased the local work onto the updated `feature/late-fee-policy` branch. After the rebase completed successfully, the tests passed and the updated branch was pushed.

Evidence: `screenshots/task6.png`

## Task 7 – Merge to Main and Tag the Final Version
Merged `feature/late-fee-policy` into `main`, ran the tests successfully, and pushed the updated `main` branch. The completed synchronized version was tagged as `v1.0-synced` and the tag was pushed to the remote repository.

Evidence: `screenshots/task7.png`

## Final Late Fee Policy
The final implementation:
- Provides a 1-day grace period.
- Rounds the calculated late fee.
- Applies a minimum late fee of $1 after the grace period.
- Caps the maximum late fee at $20.

This activity demonstrated Git branching, concurrent development, rejected pushes, conflict resolution, merging, rebasing, synchronization with a remote repository, and tagging.
