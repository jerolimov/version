### Some small version info/debugging scripts.

> Small scripts which checks the current (project) directory
> and print out the version based on the git repo and some version files.
> 
> Works currently only in the top directory of an project.

	➜ some-project git:(master) version -d

	"Real" (git-based) version:
	
	    0.0.0-16-b140fba (master)
	
	Your software says:
	
	   	package.json: 0.1.0
	    bower.json: 0.1.0
	
	npm list --color=always:
	
	    some-project@0.1.0
	    ├── bower@1.2.6
	    ├── ...
	
	bower --color list:
	
	    some-project#0.1.0
	    ├── requirejs#2.1.8
	    ├── ...

Options (for the version script):

* Use -a for automatically build (CI/CD)
* Use -d to check the dependencies (with colors)

Checkout the other commands which could be integrated in your scripts.

### Output format of the "real" version?

It's based on/inspired by the `git describe` command.
But this command works also if there is no tag yet.
Call `version` or `version-git` directly.

	Format: $tag or "0.0.0" [-commit counts with hash] [-dirty]

	# Unreleased yet (zero tags) without/with uncommited changes
	0.0.0-58-159ff48
	0.0.0-58-159ff48-dirty
	
	# The release (tagged commit) without/with uncommited changes
	0.17.0
	0.17.0-dirty
	
	# Release with new commits without/with uncommited changes
	0.17.0-58-159ff48
	0.17.0-58-159ff48-dirty
	

### What does "real" version mean?

It's a version string *based on the git repository*,
which is in my humble opinion *the only ""real"* source for such
an information.

And yes, this strings works also fine (or better) for
[semantic versioning](http://semver.org/).

Maybe i will write sometime™ a blog entry why all the package manager files 
with a version string are so broken -- for me.
(Incl. and especially all these `pom.xml`, `package.json` and so on.)

### Open for contributions

Feel free to ask me why or open an issue/pull request.
