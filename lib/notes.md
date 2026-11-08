 Cloned a repo and open it in Claude Code
Step 2: Run npm test — We saw two failing search tests (that's intentional)
Step 3: Opened lib/store.js and look for the matches function. That's where the bug lives.
The issue: the search is doing an exact match (===) when it should check if your term is contained anywhere in the note text.
Once you spot the line, the fix is just one character change. Tried it out and let me know once you've got the tests passing!
asked Claude: "Run the tests to confirm they pass, then stage my changes and commit them on a new branch with a corresponding message."