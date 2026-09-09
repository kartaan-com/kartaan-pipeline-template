# Your Kartaan pipeline

This is the template you copy to make your own repository. **It holds one file
and no code.**

## What to do

1. Press **Use this template** at the top of this page, then **Create a new
   repository**.
2. Choose **Private**. This repository will hold keys to your Amazon and Google
   accounts.
3. Name it `kartaan-pipeline`.
4. Install the **Kartaan AutoSync** app on it when Kartaan asks you to.

That is all. Kartaan puts your keys in for you and never sees the repository
again.

## What is in here

`.github/workflows/autosync.yml`. It is eleven lines of instruction and no
fetching code at all: it says *run Kartaan's fetching, this version, at this hour*,
and hands over the keys you have stored.

**The code it runs is not copied into your repository.** It is sourced from
Kartaan every night, so a fix Kartaan makes reaches you without you doing
anything. A copy would be frozen the day it was made.

**It names a version, never "the latest".** One bad change on Kartaan's side
cannot reach you until somebody deliberately moves you to a newer version.

## What this can and cannot do to your repository

It reads. That is all it is allowed to do — the permission is written into the
file and you can read it there.

**It cannot change any file in your repository, including this workflow.**
Anything able to rewrite that file could rewrite where your keys are sent, so
nothing is given that power: not Kartaan's server, not the nightly job.

## Your keys

They live in **Settings → Secrets and variables → Actions**, on your own
repository, and nowhere else. Not in a file, not in this workflow, not in a
message. Kartaan writes them there once and cannot read them back.

## If nothing happens

The job runs once a day and can also be started by hand: **Actions → Auto-sync →
Run workflow**.

If it finishes in a few seconds saying *"No platform is connected on this
repository"*, your keys are not set yet. That is the job telling you the truth
rather than failing.
