# OrbisParent

This project is the root of all the OrbisGIS projects. 
It contains a parent pom with the dependency and plugin management and a basic `site.xml` file used for the reporting
 site generation.

### Building

To build with plugin/dependency version check, use the maven goal 
`versions:display-plugin-updates versions:display-dependency-updates`.
To generate the reporting site, use the maven goal `site:effective-site site site:deploy`.

### Versions

The version number should follow this pattern : `Major`.`Minor`.`Revision[-Qualifier]`

 - `Revision` is changed after each dependency/plugin/information update/addition.
 - `Minor` is changed after each dependency/plugin/information removal or replacement.
 - `Major` is changed after each structural change.
 - Optional `Qualifier` which can take one of these values :
   - `SNAPSHOT` for in-dev version. 
   - `RC-X` for release candidate version. All of its dependencies ou plugin should be at the RC or Release state.
   - Nothing for release version. All of its dependencies ou plugin should be at the Release state.
