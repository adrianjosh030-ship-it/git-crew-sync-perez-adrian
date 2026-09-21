Why was the push rejected?

Git blocked the push because the remote feature/overtime-pay branch had new commits that the local branch didn't had yet, so the local copy was out of date. Instead allowing a update that would overwrite those missing history, Git needed the remote changes to be merged first before accepting the push.



How did the merge conflict got resolved?

Because both clones had edited the calculatePay() function independently, Git couldn't auto reconcile the two versions. The fix involved to manually merge both changes by hand, making a final version which preserved both the overtime-pay logic and the rounding logic.



Why rebase was used in Task 4?

it allowed the local commit to applied on top of the newest version of remote feature/overtime-pay branch, so the update can pull in remote changes without losing local work. Any conflicts that came up during the process was fixed manually before rebase finish.



Why force push should be avoided?

Force pushing risks to wipe out commits already in the remote that other people might depend on it. Doing a standard push after rebase is a safer route, since it keeps the shared commit history intact and stops you from accidentally erasing your teammate contributions.

