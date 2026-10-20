# Git Tic-Tac-Toe Template

A paired collaboration game. You and your partner play tic-tac-toe by editing, reviewing, committing, and sharing moves in a GitHub repository.

![Git Tic-Tac-Toe Turn Cycle](images/workflow.svg)

## Create the shared pair repository

1. One partner selects **Use this template** and creates one public repository for the pair.
2. In the new repository, invite the other partner as a collaborator.
3. Each partner opens that same pair repository in their own GitHub Codespace. Both people use the browser-based VS Code editor.

The repository's `main` branch is the clean starting point. It contains `BOARD.txt`, initialized with an empty 3×3 board. Do not play on or change `main`; play each match on its own branch.

## Start a match from `main`

Create a new branch for every match, using the next two-digit number: `match-01`, `match-02`, and so on. Always create the branch from the clean `main` branch so each match begins with the initialized board.

In VS Code, use the branch name in the lower-left status bar to select `main`, then choose **Create new branch**. Enter the next match name, such as `match-01`, and choose `main` as its starting point if prompted. Confirm that the status bar shows the match branch before editing. The first player publishes the branch using **Source Control → Publish Branch**; the partner selects that branch and pulls it before taking a turn.

For another match, select `main` again and create the next numbered branch from it. Do not create a rematch from a previous match branch, merge match branches into `main`, or reset the board by hand.

## Play and share a move

Both partners work on the same match branch in their own Codespaces. Take turns, and pull your partner's latest change before editing.

1. In **Source Control**, select **Pull**.
2. Open `BOARD.txt`. Change one empty square to your mark (`X` or `O`), then save.
3. Review the board's diff. Check that it contains only the legal move you intended.
4. Stage `BOARD.txt` with the **+** control.
5. Enter a clear commit message and select **Commit**.
6. Select **Push** in Source Control. Tell your partner the move is ready.
7. Your partner pulls, checks the board and commit, and takes the next turn.

Saving, staging, committing, and pushing are separate actions. Both partners should take turns editing and reviewing changes.

## Rehearse before the workshop

For the advance setup check, open this starter repository directly in your own Codespace and ask Copilot chat, “What does this repository do?” Confirm the response, then leave the editor and delete that Codespace from the GitHub Codespaces dashboard. This rehearsal does not require creating a template copy or pair repository. Do not commit or push during the rehearsal.

## If something goes wrong

- **The repository, branch, or board is missing:** Pause and ask the facilitator to check the repository and branch. Do not change `main` or create a replacement branch on your own.
- **A push is rejected:** Ask your partner and facilitator to check the current branch and incoming changes. Pull only after saving and reviewing your own work, then inspect the updated board before continuing.
- **A merge conflict appears naturally:** Keep the current work. Open the conflicted board in VS Code, review it with your partner, and agree on a legal board state. Remove conflict markers, review the complete diff, then stage, commit, and push the resolution. Ask the facilitator for help if you are unsure. Do not discard changes, reset the branch, or force-push.

There is no staged conflict exercise. Handle conflicts only if they arise during normal collaboration.
