![Hackathon Logo](docs/images/hackathon.png?raw=true "Hackathon Logo")

# Sitecore Hackathon 2021

-   MUST READ: **[Submission requirements](SUBMISSION_REQUIREMENTS.md)**
-   [Entry form template](ENTRYFORM.md)
-   [Starter kit instructions](STARTERKIT_INSTRUCTIONS.md)

# Hackathon Submission Entry form

## Team name

Lame Horse

## Category

Best use of SPE to help Content authors and Marketers

## Description

This module enhances the Powershell Reports enabling marketers to run the following commands on the results:

-   Create Version for language
-   Download the results as a package
-   Publish the items
-   Remove versions
-   Compress Images using Tinify API

## Video link

⟹ Provide a video highlighing your Hackathon module submission and provide a link to the video. You can use any video hosting, file share or even upload the video to this repository. _Just remember to update the link below_

⟹ [Replace this Video link](#video-link)

## Pre-requisites and Dependencies

-   Sitecore 10.1 - Initial Release
-   Sitecore Management Services Module 2.0.0
-   Sitecore Powershel Extensions Module 6.2

## Installation instructions

1.  Install Sitecore Powershel Extensions Module 6.2
2.  Install the package LameHorse.Horseshoes.zip

## Development instructions

1.  Install Sitecore Management Services Module 2.0.0 and Sitecore Powershel Extensions Module 6.2 on Sitecore

2.  At the root folder of the source code run the following command line:

```powershell
dotnet tool restore
```

This command line will install locally Sitecore CLI version 2.0.0.

```
dotnet sitecore login --authority https://[prefix].identityserver --cm https://[prefix].sc --allow-write true
```

![Authentication Step 1](/docs/images/authentication-02.png "Authentication Step 1")

A new browser window will open asking to enter credentials and allow Sitecore CLI to access your instance.

![Authentication Step 2](/docs/images/authentication-01.png "Authentication Step 2")

![Authentication Step 3](/docs/images/authentication-03.png "Authentication Step 3")

![Authentication Step 4](/docs/images/authentication-04.png "Authentication Step 4")

![Authentication Step 4](/docs/images/authentication-05.png "Authentication Step 4")

3. Next run the following command line:

```powershell
dotnet sitecore ser push
```

This command line will push the serialized items from the file system into the Sitecore instance.

### Configuration

⟹ If there are any custom configuration that has to be set manually then remember to add all details here.

_Remove this subsection if your entry does not require any configuration that is not fully covered in the installation instructions already_

## Usage instructions

### Translate items listed in a Powershell report using Microsoft Cognitive Services (Translator)

The following example shows how you can use Microsoft Cognitive Services (Translator) to translate items listed in a Powershell report.
In Sitecore:

1. Click on the desktop icon
2. Next, click on **Reporting Tools** > **Content Audit** > **Items last updated**

![How to 6](/docs/images/how-to-06.png "How to 6")

3. In the Report Filter, select the criteria that yields any results.

![How to 7](/docs/images/how-to-07.png "How to 7")

4. In the **Items last updated** dialog, click on **Process Items**. The processing script dialog will show up.

![How to 8](/docs/images/how-to-08.png "How to 8")

5. In the **Select processing script** combobox, select the option **Processing/Create Version and Translate**. All the images will be sent to Tinify API and compressed.

6. In the **Translate version for the item** dialog, select a target language and click OK.

![How to 9](/docs/images/how-to-09.png "How to 9")

> Continuar daqui

## Shrink all images listed in a Powershell report

The following example shows how you can use Tinify to shrink all images listed in a Powershell report.
In Sitecore:

1. Click on the desktop icon.
2. Next, click on **Reporting Tools** > **Media Audit** > **Media items by size and type**.

![How to 1](/docs/images/how-to-01.png "How to 1")

3. In the **Report Filter** dialog, click **Proceed**.

![How to 2](/docs/images/how-to-02.png "How to 2")

4. In the **Media by size and type** dialog, click on **Process Items**. The processing script dialog will show up.

![How to 3](/docs/images/how-to-03.png "How to 3")

![How to 4](/docs/images/how-to-04.png "How to 4")

5. In the **Select processing script** combobox, select the option **Processing/Tinify Images**. All the images will be sent to Tinify API and compressed.

![How to 5](/docs/images/how-to-05.png "How to 5")

## Comments

If you'd like to make additional comments that is important for your module entry.
