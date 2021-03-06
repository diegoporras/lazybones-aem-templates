Adobe Consulting AEM Lazybones Templates
------------------------------------

This project contains project templates (right now just one) for creating Adobe
Experience Manager projects using the [Lazybones](https://github.com/pledbrook/lazybones) project creator. Lazybones is a far more interactive project creation
tool than Maven Archetypes. Using these templates allows you to both bootstrap your
AEM project with an appropriate structure, but also enable some of the core features
from [ACS AEM Commons](http://adobe-consulting-services.github.io/acs-aem-commons/).

# Installing Lazybones

In order to use this project's templates, you must first have lazybones installed. The easiest way to do this is with [gvm](http://gvmtool.net/):

    gvm install lazybones
    
You can also download the distribution package from [BinTray](https://bintray.com/pledbrook/lazybones-templates/lazybones), unzip it, and add it to your PATH.

# Using the Multimodule Template

Once you've done this configuration, you can run Lazybones:

    lazybones create aem-multimodule-project <directory name>

For example, to create a new project in the directory `my-project`, run

    lazybones create aem-multimodule-project my-project

This will prompt you to answer a number of questions about the project you want created.

## Options

Below are all of the options available in the current version. To specify an option on the command line, pass -P\<parameter name>=\<parameter value>

| Description                                               | Default                            | Parameter Name                 |
|-----------------------------------------------------------|------------------------------------|--------------------------------|
| Maven Group ID                                            | com.myco                           | groupId                        |
| Maven Artifact ID                                         | example-project                    | artifactId                     |
| Maven Version                                             | 0.0.1-SNAPSHOT                     | version                        |
| Project Name                                              | My AEM Project                     | projectName                    |
| Target AEM Version                                        | 6.0                                | aemVersion                     |
| Bundle Artifact ID                                        | example-project-bundle             | bundleArtifactId               |
| Content Package Artifact ID                               | example-project-content            | contentArtifactId              |
| Folder to create under `/apps`                            | my-aem-project                     | appsFolderName                 |
| Folder to use under `/content`                            | my-aem-project                     | contentFolderName              |
| Create a site design?                                     | yes                                | createDesign                   |
| Design folder name                                        | my-aem-project                     | designFolderName               |
| Create a main client library?                             | yes                                | createMainClientLib            |
| Create a dependencies client library                      | yes                                | createDependenciesClientLib    |
| Enable code quality checks?                               | yes                                | enableCodeQuality              |
| Set root mapping to `/welcome` (Classic UI)?              | yes in 5.6.1, no in 6.0            | reconfigureRootMapping         |
| Set Default Authoring UI to Classic? (6.0 only)           | yes                                | enableClassicAuthoringAsDefault |
| Include ACS AEM Commons?                                  | yes                                | includeAcsAemCommons           |
| Include ACS AEM Commons as a sub-package?                 | yes                                | includeAcsAemCommonsSubPackage |
| Enable ACS AEM Commons Error Handler?                     | yes                                | enableErrorHandler             |
| Default Error Page Path                                   | /content/my-aem-project/errors/404 | defaultErrorPath               |
| Define Error Page Folder for /content/my-aem-project ?    | no                                 | defineErrorPageFolder          |
| Error Page Folder for /content/my-aem-project             | errors                             | errorFolder                    |
| Enable ACS AEM Commons Pages Reference Provider?          | yes                                | enablePagesReferenceProvider   |
| Enable ACS AEM Commons Design Reference Provider?         | yes                                | enableDesignReferenceProvider  |
| Enable ACS AEM Commons Design Html Library Manager?       | yes                                | enableDhlm                     |
| Enable ACS AEM Commons Versioned Client Libraries?        | yes                                | enableVersionedClientLibs      |
| Create Environment-Specific Config Folders?               | yes                                | createRunModeConfigFolders     |
| Environment Names                                         | localdev,dev,qa,stage,prod         | envNames                       |
| Create Author and Publish Config Folders per Environment? | yes                                | createAuthorAndPublishPerEnv   |
| Using Sling Models?                                       | yes                                | usingSlingModels               |
| Sling Models Package                                      | ''                                 | slingModelsPackage             |
| Purge DAM Workflows?                                      | yes                                | purgeDamWorkflows              |
| DAM Workflow Retention Period (days)                      | 7                                  | purgeDamWorkflowRetention      |

# Links to ACS AEM Commons Features

Several of the prompts ask if you want to enable specific [ACS AEM Commons](http://adobe-consulting-services.github.io/acs-aem-commons/) features. Links to the feature documentation can be found below:

* [ACS AEM Commons Error Handler](http://adobe-consulting-services.github.io/acs-aem-commons/features/errorpagehandler.html)
* [ACS AEM Commons Pages Reference Provider](http://adobe-consulting-services.github.io/acs-aem-commons/features/reference-providers.html)
* [ACS AEM Commons Design Reference Provider](http://adobe-consulting-services.github.io/acs-aem-commons/features/reference-providers.html)
* [ACS AEM Commons Design Html Library Manager](http://adobe-consulting-services.github.io/acs-aem-commons/features/designer-clientlibsmanager.html)
* [ACS AEM Commons Versioned Clientlibs Rewriter](http://adobe-consulting-services.github.io/acs-aem-commons/features/versioned-clientlibs.html)