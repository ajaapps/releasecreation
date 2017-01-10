# releasecreation

'releasecreation' is a temporary github repository to test release creation workflows.
Latest release is version v1.0.

We specifically would like to see if the procedure, offered by the
github web interface, generates a lightweight git tag.  The procedure
is documented here: [Creating
Releases](https://help.github.com/articles/creating-releases/)

Besides that it is interesting to check wether a release package is
generated if we push a locally created git tag.


## conclusion

Creating a release via the webinterface automatically also creates a
lightweight tag.

Creating and a leightweight tag locally, then pushing it,
generates a release on github. This includes also the automatic
creation of downloadable
packages (.zip and .tar.gz).

If one does not want to use the web interface, the
following steps can be used to create a release on github:

1. locally edit and commit to master branch
2. do a last commit, bumping the version number in the source code
3. create a lightweight tag `git tag v1.19`
4. push the commits and the tag to remote: `git push ; git push origin v1.19`

