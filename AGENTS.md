# General guidelines

Unless explicitly asked to complete a task independently, acknowledge when you are stuck and ask the user for help rather than continuing indefinitely. A good indicator is having made a plan, attempted implementation, and reworked the solution more than twice without achieving the desired result.

# Running commands

Rather than using common utilities like prettier, eslint, tsc with `npx {utility}`, prefer using project defined scripts with additional arguments, for example:
`npm run typecheck -- ...additional arguments go here`
`npm run lint -- additional arguments`
If the project doesn't expose such commands, you should add them to the package.json first and then use them.

# Delegation and context preservation

Primary agents are explicitly instructed to delegate substantial research, planning, implementation, diagnosis, review, and verification. Handle small, localized tasks directly when delegation would add more overhead than value. The primary owns scoping, user decisions, and concise synthesis rather than duplicate execution.

- Use `explore` only for mechanical repository discovery: locating files, symbols, references, patterns, and straightforward call paths.
- Use `general` for judgment-heavy research, planning, diagnosis, architecture and security analysis, code review, and verification. It is read-only and can research external sources.
- Use `builder` for implementation and fixes when the current agent permits it. Respect Plan mode and other editing restrictions.
- Before delegating, inspect only enough to define a clear, self-contained task with its goal, constraints, relevant paths, and expected output. Do not solve the task before handing it off.
- Prefer foreground delegation when the next useful action depends on its result. Use background only when there is concrete, necessary, non-overlapping work to perform concurrently; do not invent busywork while waiting.
- Do not repeat delegated investigations or independently inspect the same material. Verify narrowly only when a specific claim is unsupported, contradictory, or consequentially uncertain; continue the child for missing evidence when appropriate.
- Request concise conclusions, supporting file references or source links, and material uncertainties rather than raw search output or lengthy transcripts.
- Reuse the existing child session for related follow-up work.
- Subagents perform their assigned work directly and do not delegate further.

For external research, use web search and fetch. For library or API questions, check sources against the version installed in the project.
