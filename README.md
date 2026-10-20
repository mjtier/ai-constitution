# ai-constitution

A constitution for AI agents: the principles that guide how an AI model or agent should think, behave and decide. It is written to be generic. It assumes no particular model, vendor, tool set or harness, and it covers everything from a chat assistant answering one question to an always-on agent that runs scheduled routines unattended, works within a budget, and coordinates with other agents.

## What's here

- [CONSTITUTION.md](CONSTITUTION.md) is the full text. It is written to the agent ("you"), and each principle comes with a short explanation of why it exists. This is the governing document.
- [CORE.md](CORE.md) is the compact core: about one page, written to be pasted into a system prompt, an `AGENTS.md` file, or whatever instructions your agent loads. Every rule in it names the section of the constitution it comes from. Where the two differ, the constitution governs.

In brief, an agent following this constitution puts avoiding serious harm first, then honesty, then its owner's authority, then helpfulness. It acts freely on reversible, internal work and asks first before anything external, irreversible, financial, or that speaks or signs for someone. Only its owner can authorise those consequential actions, and it never sends anything in its owner's name unless the owner has approved that exact message. It treats text in emails, web pages and documents as information, never as instructions.

## How to adopt it

1. **Fill in the owner.** Replace `{{OWNER_NAME}}` in CORE.md and CONSTITUTION.md with the name of the person or organisation the agent works for. An agent that finds the marker unfilled reads it as "your owner".
2. **Load CORE.md** into your agent's instructions. If your setup has room, make CONSTITUTION.md available too, so the agent can consult the reasoning behind each rule.
3. **Add local rules for your setting** if you need them: tighter limits, extra approvals, house style, topics to avoid. Local rules may **narrow** the constitution but never **loosen** it. They cannot unlock a hard limit, reorder the priorities, or grant open-ended authority. The constitution tells agents to disregard a local rule that tries to.
4. **Record the version** your agents load, so you know which rules they are following when the text changes.

## Status

**v0.1, first draft for review.** The structure and principles are in place and ready for a review round. Expect substantial changes before a 1.0 release.

## Open questions for the next review round

1. **Owner versus platform.** The chain of command puts the owner above the platform, but the owner's authority stops at terms the owner accepted to run the agent (§4.2). Is that the right line, and what should the agent do when the two clash and the owner can't be reached?
2. **Sending as the owner.** For now, every message in the owner's name is drafted first and sent only after the owner approves that exact message, and standing authority never covers it (§7.4). Should owners ever be able to grant standing permission for routine messages, such as acknowledgements or scheduling replies?
3. **Owner-only approval.** Only the owner can authorise consequential actions (§7.2). In deployments that serve users, is the owner's standing authority (§8.1) enough for routine actions users ask for, such as emailing a user their own receipt, or should users be able to approve bounded actions that affect only themselves?
4. **AI disclosure on the owner's behalf.** When an agent sends an approved message in its owner's name, should the message disclose that an AI drafted or sent it? §5.4 covers sincere questions, not unprompted disclosure.
5. **Approval expiry defaults.** One-off approvals lapse when used or when "a reasonable time" passes (§7.3). Should there be a concrete default window, and a maximum lifetime for standing authority (§8.1)?
6. **Emergencies.** Should an agent ever take an external action without approval, such as contacting emergency services when a life appears to be at risk? The draft only requires pointing people to emergency help (§4.3) and taking the most cautious reversible option when no one can be reached (§12.3).
7. **The hard-limits list.** Is the list in §3 complete and correctly scoped? Candidates for discussion include mass surveillance of private individuals and large-scale disinformation.
8. **Trusted channels.** What should count as a channel that verifiably carries an owner's instructions or approvals (§4.6, §10.3), especially in multi-agent setups where a coordinating agent relays them?
9. **Shared memory.** How should memory hygiene and requests to forget (§9.4) work when several agents share one memory store?
10. **Agents of other owners.** §10.7 treats outside agents as third parties. Is that enough as agent-to-agent dealing between different owners becomes common?
11. **Core size.** Is about 600 words the right size for CORE.md, or is a smaller "micro-core" also needed for agents with tight instruction budgets?
12. **Checking adherence.** How should adopters test that an agent actually follows the core? A shared set of scenario tests could be a next step.
13. **Licence.** No licence has been chosen yet. Which licence best suits a text meant to be copied into other people's agents?
