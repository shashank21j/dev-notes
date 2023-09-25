# Quick reference to .gitignore file
## Creating a .gitignore file:

You can create a .gitignore file in the root directory of your repository. This file specifies the patterns of the filenames that should be excluded from your Git repository.

Comment:

Lines beginning with a # are comments and are not processed by Git.
```
\# This is a comment
```

## Ignore specific files:

Simply list their names:

```
secret.txt
password.md
```

## Ignore all files of a certain type:

Use a * wildcard:

```
*.log
```
This will ignore all files with the .log extension.

## Ignore all files in a specific folder:

```
node_modules/
build/
```

This will ignore all files in the node_modules and build directories.

## Negate a pattern:

If you want to track a specific file or type of files within an ignored folder, you can negate that pattern using the ! symbol:

```
*.log
!important.log
```

This will ignore all .log files except important.log.

## Ignore files but not directories:

```
doc/*.txt
```

This will ignore .txt files inside the doc directory but not the directory itself.

## Additional Notes
The .gitignore patterns are relative to the location of the .gitignore file.

Patterns specified in a .gitignore file within a directory will only affect that directory and its sub-directories.  

.gitignore files can be checked into the repository itself, allowing patterns to be shared with other users.

To ignore certain files globally (across all repositories), you can create a global .gitignore file. First, run:

```
git config --global core.excludesfile ~/.gitignore_global
```
Then, add your global patterns to ~/.gitignore_global.

Important: If a file is already tracked by Git before it's added to .gitignore, adding it to .gitignore will not remove it. To stop tracking a file that is currently tracked, use:

```
git rm --cached filename
```

## Common .gitignore Patterns
### For Node.js projects:

```
node_modules/
npm-debug.log
```

### For Python projects:

```
__pycache__/
*.pyc
*.pyo
```

### For Java projects:

```
*.class
target/
```

### For macOS:

```
.DS_Store
```