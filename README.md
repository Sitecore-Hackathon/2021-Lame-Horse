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

[Sitecore Hackathon 2021 - Lame Horse Team
Video](https://youtu.be/S6i68yu3W3U)

## Pre-requisites and Dependencies

-   Sitecore 10.1 - Initial Release
-   Sitecore Management Services Module 2.0.0
-   Sitecore Powershel Extensions Module 6.2

## Installation instructions

1.  Install Sitecore Powershel Extensions Module 6.2
2.  Install the package [LameHorse.Horseshoes-1.0.zip](/sc.packages/LameHorse.Horseshoes-1.0.zip)

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

## Configuration

**Tinify**

You should create your own API key and update it in the item `/sitecore/system/Modules/PowerShell/Script Library/Horseshoes/Reporting/Processing/Tinify Images`. The API key can be created by accessing the link https://tinypng.com/developers. For the Hackathon, we left our own free tier API key configured so the judges can reuse them when evaluating the solution.

**Azure Cognitive Services**

You should create your own Microsoft Azure Cognitive Services (Translator) and update the key and location in the item `/sitecore/system/Modules/PowerShell/Script Library/Horseshoes/Reporting/Processing/Translate`. For the Hackathon, we left our free tier API key configured so the judges can reuse them when evaluating the solution.

## Usage instructions

### Shrink all images listed in a Powershell report

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

### Translate items listed in a Powershell report using Microsoft Azure Cognitive Services (Translator)

The following example shows how you can use Microsoft Cognitive Services (Translator) to translate items listed in a Powershell report.
In Sitecore:

1. Click on the desktop icon
2. Next, click on **Reporting Tools** > **Content Audit** > **Items last updated**

![How to 6](/docs/images/how-to-06.png "How to 6")

3. In the Report Filter, select the criteria that yields any results.

![How to 7](/docs/images/how-to-07.png "How to 7")

4. In the **Items last updated** dialog, click on **Process Items**. The processing script dialog will show up.

![How to 8](/docs/images/how-to-08.png "How to 8")

5. In the **Select processing script** combobox, select the option **Processing/Translate**. All the images will be sent to Tinify API and compressed.

6. In the **Translate item from English into any target language** dialog, select a target language and click OK.

![How to 9](/docs/images/how-to-09.png "How to 09")

The selected items will be translated into the target selected language.

![How to 9](/docs/images/how-to-10.png "How to 10")

### Create Empty version for language

1. Following the same procedure described above to generate a report with Powershell Extensions, In the **Select processing script** combobox, select the option **Processing/Create Version for language**.

![How to 11](/docs/images/how-to-11.png "How to 11")

2. In the **Create empty version for a given language** dialog, select the target language and click OK.

The selected items will have a new version created in the target selected language.

![How to 12](/docs/images/how-to-12.png "How to 12")

### Publish

1. Following the same procedure described above to generate a report with Powershell Extensions, In the **Select processing script** combobox, select the option **Processing/Publish**.

2. In the **Publish Items** dialog, select the publish option and click OK.

![How to 14](/docs/images/how-to-14.png "How to 14")

The selected items will be published accordingly.

### Remove versions from all languages but one

1. Following the same procedure described above to generate a report with Powershell Extensions, In the **Select processing script** combobox, select the option **Processing/Remove versions from all languages but one**.

![How to 15](/docs/images/how-to-15.png "How to 15")

2. In the **Remove all version from all languages but the selected** dialog, select the language you want to keep and click OK.

![How to 16](/docs/images/how-to-16.png "How to 16")

The selected items will have all languages removed except the one you've selected previously.

### Remove versions from language

1. Following the same procedure described above to generate a report with Powershell Extensions, In the **Select processing script** combobox, select the option **Processing/Remove versions from language**.

2. In the **Remove versions from language** dialog, select the language you want to have the versions removed and click OK.

The selected items will have all versions removed for the selected language.

### Replace string in fields

1. Following the same procedure described above to generate a report with Powershell Extensions, In the **Select processing script** combobox, select the option **Processing/Replace string in fields**.

2. In the **Replace string in fields** dialog, enter the old text in the field **Find** and the new text in the field **Replace**, and click OK.

![How to 17](/docs/images/how-to-17.png "How to 17")

The selected items will old text replaced in all fields.

![How to 18](/docs/images/how-to-18.png "How to 18")

### Download Package

1. Following the same procedure described above to generate a report with Powershell Extensions, In the **Select processing script** combobox, select the option **Processing/Download Package**.

2. In the **Download** dialog, click Download.

![How to 19](/docs/images/how-to-19.png "How to 19")

A Sitecore package will be downloaded with the items listed in the report.

## Comments

If you'd like to make additional comments that is important for your module entry.
