### Some small version info/debugging scripts.

> Small scripts which checks the current (project) directory
> and print out the version based on the git repo and some version files.
> 
> Works currently only in the top directory of an project.

	➜ some-project git:(master) version -d

	"Real" (git-based) version:
	
	    0.0.0-16-b140fba
	
	Your software says:
	
	   	package.json: 0.1.0
	    bower.json: 0.1.0
	
	npm list --color=always:
	
	    some-project@0.1.0
	    ├── bower@1.2.6
	    ...
	
	bower --color list:
	
	    some-project#0.1.0
	    ├── requirejs#2.1.8
	    ├── ...

Options (for the version script):

* Use -a for automatically build (CI/CD)
* Use -d to check the dependencies (with colors)

Checkout the other commands which could be integrated in your scripts.

### What does real version mean?

It's a version string *based on the git repository*,
which is in my humble opinion the *"only real"* source for such
an information.

And yes, this strings works also fine (or better) for
[semantic versioning](http://semver.org/).

Maybe i will write sometime™ a blog entry why all the package manager files 
with a version string are so broken -- for me.
(Incl. and especially all these ```pom.xml```, ```package.json``` and so on.)

### Open for contributions

Feel free to ask me why or open an issue/pull request.
