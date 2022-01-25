# git-version-tool
Simple shell script to handle pretty versions of git commits easily

## pretty version rules

Pretty version is a commit with the structure like that:
```
<MAJOR>.<MINOR>.<FIX>

<TYPE>: <COMMENT>
```
Or for prerelease versions:
```
0.<MAJOR>.<MINOR>.<FIX>

<TYPE>: <COMMENT>
```

### Version number

The version number is constructed of 3 numbers -- a major, a minor, and a fix.

#### Major

Major is a version number that describes how many break commits are done.
Different major versions break things -- they are not back-compatible.

#### Minor

Minor is a version number that describes how many feat commits are done.
Different minor versions adds features -- they are always back-compatible.

#### Fix

Fix is a version number that describes how many fix commits are done.
Different fix versions fixes things or adds documentation -- they have the same features.

### Type

A type of commit describes what type of changes are made since last commit.

#### Break

The Break commits are commits that break back-compatibility of the program.
When the break commit is done, the major version increments, the minor and the fix versions are sets up to 0.

#### Feat

The Feat commits are commits that add new features to the program.
When the feat commit is done, the major version stays the same, minor version increments, the fix version are sets up to 0.

#### Fix

The Fix commits are commits that fix bugs of the program or add documentation.
When the fix commit is done, the major and the minor version stays the same, the fix version increments.

### Comment
The comment is a simple message in present simple that describes the changes brifely.
