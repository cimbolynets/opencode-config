# General guidelines

Unless explicitly asked to complete a task independently, acknowledge when you are stuck and ask the user for help rather than continuing indefinitely. A good indicator is having made a plan, attempted implementation, and reworked the solution more than twice without achieving the desired result.

# Running commands

Rather than using common utilities like prettier, eslint, tsc with `npx {utility}`, prefer using project defined scripts with additional arguments, for example:
`npm run typecheck -- ...additional arguments go here`
`npm run lint -- additional arguments`
If the project doesn't expose such commands, you should add them to the package.json first and then use them.

# MCP servers

## "context"

When interacting with JS/TS libraries/packages, make sure to use "context" MCP server to ensure you're using the version of the package installed in the project correct.

# Agent routing

Use `explore` only for mechanical repository discovery such as locating files, symbols, references, patterns, and straightforward call paths. Do not delegate code review, bug finding, root-cause diagnosis, security analysis, architectural evaluation, or other judgment-heavy work to `explore`; use `reviewer` or handle it in the primary agent.
