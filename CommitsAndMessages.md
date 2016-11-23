# Commits and commit messages

## Message format

The commit message MUST be written in english and be imperative.

Messages SHOULD be readable as "When applied, this commit will..."

Messages must begin with a prefix defined in the section [Commit message prefixes](#commit-message-prefixes).

## Commit Signing

Each commit SHOULD be signed with a GPG key to verify the author of the commit.

## Commit message prefixes

The intention of a commit message prefixes is to see the purpose of the commit at first glance.

### Version 2

Format: `[short] [long] explanation`

Each commit MUST be annotated with at least one of the following prefix in short format:

```
[B] [BUGFIX] Change a bug, but do not any intended behavior or code style
[C] [CODESTYLE] Fix code style violation, reorder entries, but must not change any code or comment
[D] [DOCS] Add/fix/alter documentation or comments in the code
[F] [FEATURE] Add new functionality or alter behaviour to match a new requirement (e.g. new button, new action)
[M] [META] Add/alter/update metadata like keywords, authors, mails and URLs or files required for development like .editorconfig or dynamicReturnTypeMeta.json, Build toolchains etc.
[P] [PURGE] Remove files or code that are not used anymore
[R] [REFACTOR] Extract code to methods/variables, simplify code. Must not change behavior.
[S] [SECURITY] Fix an security issue by updating a module/package or fix in the own code
[T] [TESTS] Add/fix/alter tests
[U] [UPDATE] Alter static data like labels or project dependencies, but not the application code. Must not change behaviour.
[V] [VCS] Change versioning related stuff like an ignore file
```

Example: `[V] Add TypeScript build dependencies to the gitignore file`

It's now possible to use more than one prefix.

Example: `[F,P] Re-implement myFunction in the responsible class MyClass and remove unused legacy method dependencies`

### Version 1 (deprecated)

In the beginning these prefixes were used.

```
[BUGFIX] Change a Bug, but not behavior or code style
[CLEANUP] Remove Files or Code that are not used anymore
[FEATURE] Add new Feature (e.g. new button, new action)
[UPDATE] update dependencies and code interacting with dependencies
[SECURITY] Fix an security issue by updating a module/package or fix in the own code
[PREPARATION] e.g. Add a new dependency, file or directive that does not have an effect, yet.
[TEST] Add/fix/alter tests
[CODESTYLE] Fix code style violation, reorder entries, but must not change any code or comment
[COMMENT] Add/fix/alter comments in the code
[DOCS] Add/fix/alter documentation
[REFACTOR] Extract code to methods/variables, simplify code. Must not change behavior.
[TASK] Alter fixed data like constants or labels, but not code
[FOLLOWUP] Immediate Regression fix or Bugfix related to the previous commit
[API] Change visibility of methods or fields, private <> protected <> public
[TYPO] Fix a typo in exception or error messages not related to behaviour
[META] Add/alter/update metadata like keywords, authors, mails and URLs
[GIT] Change git related stuff like ignores
[DEV] Add files required for development like .editorconfig or dynamicReturnTypeMeta.json, Build toolchains etc.
```
