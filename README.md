# how-to-npm
lessons at how-to-npm
how-to-npm

A module to teach you how to module.
PREREQUISITES
To use this project, you'll need NodeJS. Visit http://www.nodejs.org to download and learn more!

USAGE
npm i -g how-to-npm
how-to-npm

00 Install npm
The first thing we're going to do is make sure that your npm version is up to date.

     Run `how-to-npm verify`

Some helpful commands:

     npm help ............ Get help with npm
     how-to-npm print .... Re-display the current exercise
     how-to-npm verify ... Verify that you have finished an exercise
     how-to-npm solution . Show the solution for the current exercise

01 Dev Environment
    1.mkdir <name directory> -make a new directory 
    2.cd - into it
    3.npm init- to create a package.json file (You will be prompted
     to answer a number of questions. You can just press enter to accept the
     default for each question.)
02 Login
    1.npm whoami-To see who you're logged in as
    2.npm adduser-To create your account
03 Start a progect
    1.npm init --scope=<username> , and replace <username> with the user
     you created in the last lesson.
04 Install A Module
    The first thing that most people do with npm is install a dependency.
     Dependencies are fetched from the registry, and unpacked in the `node_modules`
     folder.
     To install a module, use the `npm install <modulename>` command.
     
     1.npm install @linclark/pkg - install module @linclark/pkg
05 Listing Dependencies
    1.npm ls -shows you what you have installed (your dependencies)/If there are
     any problems npm will alert you by returning an "!ERR" message

06 npm Test
    every module and project will have a test script that runs to make
     sure everything is good.  In order to help remind you to do this, npm
     puts an "always failing" test in there by default /If you wanted to actually run any tests you'd written in `test.js` with the "test" script, you'd run `npm test`. The docs for npm's scripts property can be found here: https://docs.npmjs.com/misc/scripts
     
     1.create a file called `test.js`
     2.edit your `package.json` file to make your scripts section look like
     this instead:

       "scripts": {
         "test": "node test.js"
       }
07 Package Niceties
    If you type `npm install`, you'll see
     something like this:

         npm WARN package.json %ID% No description
         npm WARN package.json %ID% No repository field.
         npm WARN package.json %ID% No README data
   
   1.create a README.md file, with a few words in it
   2.add a "repository" field in your package.json file, with a url
     where people can access the code(You can edit your package.json file by hand, or run `npm init` again)

08 Publish
it's very easy for all npm users to publish their modules and share them with the world.
Packages get into the registry by using the `npm publish` command
     
     1.npm publish

09 Version
Every package in npm has a version number associated with it.  As you release updates to your package, these updates get an updated version number.
Version numbers in npm follow a standard called "SemVer".  This stands for "Semantic Version".  The specification for this standard can be found at http://semver.org.

     The tl;dr version is that for a version like this:

       1.2.3
       ^ ^ ^
       | | `-- Patch version. Update for every change.
       | `---- Minor version. Update for API additions.
       `------ Major version. Update for breaking API changes.
npm has a special command called `npm version` which will update your package.json file for you, and also commit the change to git if your project is a git repository.  You can learn more at `npm help version`.
Or, if you don't trust the machines, you can open up your package.json file by hand, and put some new numbers in the "version" field.
The npm registry won't let you publish a new release of your package without updating the version number!  Ever!  So, get used to the idea of bumping the version whenever you want to publish, even if the change is really minor.

1.npm version - Update your version number

10 Publish Again
 1.how-to-npm verify

11 Dist Tag
1.npm ls - To find out the name of your current package/version
2.npm dist-tag add new-directory@1.0.2 beta - will add a new tag (npm dist-tag add <pkg>@<version> [<tag>] )

12 Dist Tag Removal
Let's delete all the tags that we can, and also point "latest" at something other than the most recent release

1.npm dist-tag ls  - Show all of the dist-tags for a package, defaulting to the package in the current prefix
2.npm dist-tag rm new-directory test - Clear a tag that is no longer in use from the package(npm dist-tag rm <pkg> <tag> )

12 Outdated
each release is a unique
     combination of a name and a version, we can detect compatible releases
     programmatically with the `npm outdated` command

1.outdated (npm outdated don`t work)
2.how-to-npm verify PKG-  where `PKG` is the name of the package that is out of date

14 Update
 1.npm install  - up to date 

15 Rm
1.npm rm - Remove all the deps (or npm uninstall)you can also use `--save` when removing packages, to also remove them from your package.json file.

16 Finale
1.how-to-npm verify
