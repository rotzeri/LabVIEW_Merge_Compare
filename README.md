# GIT + LabVIEW: Quickly Resolving Conflicted VIs After a Merge

After merging two branches of LabVIEW code, how do you quickly resolve VIs in a conflicted state?

This is where the VI `Compare_IsSame_NoUI.vi` (available on GitHub - `LabVIEW_Merge_Compare`) comes in handy.

## Features

- Lists all VIs with unresolved conflicts.
- Launches LabVIEW VI Compare for each conflicted VI and opens both versions, showing where the differences are in the code. At this stage you can manually merge if required.
- After closing the VI Compare dialog, you get a prompt for resolving the conflict using either the **yours (mine)** or **theirs** VI. You can also choose not to resolve the conflict.
- `Compare_IsSame_NoUI.vi` executes the corresponding Git command to resolve the conflict automatically.
- Once all conflicts are resolved, all that remains is committing and pushing.

## Notes

I have added comments on both the front panel and block diagram to help with onboarding and usage of this VI. Please read those before running the VI.

The main setup requirement before running the VI is to have two separate folders, each containing one branch (version) of your LabVIEW project.

It can feel a bit tricky at first, but once you get used to the workflow, merging two GIT branches containing LabVIEW code becomes much smoother and faster.