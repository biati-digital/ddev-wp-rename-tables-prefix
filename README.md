# ddev-wp-rename-tables-prefix
A db command for DDEV to rename tables prefix of WordPress installations

### Installation:

```
ddev get biati-digital/ddev-wp-rename-tables-prefix
```

### Usage

There are several ways to run the command but the most simple way is:

`ddev wp-rename-tables-prefix --to=new_`

If you only provide `--to`, the command will try to get the current table prefix directly from the database. If the current table prefix can not be found you can provide it.

`ddev wp-rename-tables-prefix --from=old_ --to=new_`

### Options

- **--from** the old table prefix, if not added the command will try to get it from the database
- **--to** the new table prefix, required
- **--silent** you can set `--silent=true` to disable multiple messages that are printed when running the command.

You can run `ddev help wp-rename-tables-prefix` for help

### Limitations

The command has not been tested in multisites installations

Before running the command make sure to create a database snapshot `ddev snapshot` just in case.
