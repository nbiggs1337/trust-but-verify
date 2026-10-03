# Trust, but Verify. Then Verify the Verify.

## Idea

On a long task, one agent is not enough of a check. We have been spawning three, numbered from zero: **agent 0**, **agent 1**, and **agent 2**.

## Problem

A long task is a chain. Steps get skipped, softened, or marked done.

- If agent 0 grades its own work, it agrees with itself.
- Two agents can share the same shortcut: one does less, the other calls that enough.
- The chain still looks finished.

## Solution

Three agents. Three jobs. No shared grade.

1. **Agent 0** does the job.
2. **Agent 1** checks that the job was actually done.
3. **Agent 2** does not redo the job, and it does not grade agent 0 on its own. It checks that agent 0's result and agent 1's verification agree.

The third pass is spent on whether the first two agree, not on a third trip through the work.

## Theory

A check that shares context with the worker inherits the worker's misses. A second pass from the same agent is not a second opinion. Two separate checks can still land on the same shortcut. Agent 2 is there to catch that, by looking at the two results apart from both of them.

A fourth agent, agent 3, can check that agreement again. Useful, and it costs another run. **So far three is the cut that stays worth the cost.** Past that, the spend is on checking the check of the check.

## Practice

Spawn 0, 1, and 2 at the start, not after the chain has already been called done.

- Agent 0 owns the artifact.
- Agent 1 owns a pass or a fail against that artifact, with the miss named.
- Agent 2 owns a pass or a fail on whether those two agree.
- **A fail sends the chain back.**
- A pass names what was checked. It is not a note that the work seemed fine.

These prompts are a basic demonstration of the idea, and a practice that has been working. They are not a script to keep pasting unchanged. As agents get stronger, the wording should change. The split should not: one does the job, one checks the job, one checks that those two agree.

Fill-in prompts: [Spawn prompts](docs/spawn-prompts.md).
