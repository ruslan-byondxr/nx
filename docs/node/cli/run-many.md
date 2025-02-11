# run-many

Run task for multiple projects

## Usage

```bash
nx run-many
```

[Install `nx` globally]({{framework}}/getting-started/nx-setup#install-nx) to invoke the command directly using `nx`, or use `npx nx`, `yarn nx`, or `pnpx nx`.

### Examples

Test all projects.:

```bash
nx run-many --target=test --all
```

Test proj1 and proj2.:

```bash
nx run-many --target=test --projects=proj1,proj2
```

Test proj1 and proj2 in parallel.:

```bash
nx run-many --target=test --projects=proj1,proj2 --parallel --maxParallel=2
```

Build proj1 and proj2 and all their dependencies.:

```bash
nx run-many --target=test --projects=proj1,proj2 --with-deps
```

## Options

### all

Run the target on all projects in the workspace

### configuration

This is the configuration to use when performing tasks on projects

### exclude

Default: ``

Exclude certain projects from being processed

### help

Show help

### maxParallel

Max number of parallel processes. This flag is ignored if the parallel option is set to `false`. (default: 3)

### only-failed

Default: `false`

Only run the target on projects which previously failed

### parallel

Parallelize the command (default: false)

### projects

Projects to run (comma delimited)

### runner

Override the tasks runner in `nx.json`

### skip-nx-cache

Default: `false`

Rerun the tasks even when the results are available in the cache

### target

Task to run for affected projects

### verbose

Print additional error stack trace on failure

### version

Show version number

### with-deps

Default: `false`

Include dependencies of specified projects when computing what to run
