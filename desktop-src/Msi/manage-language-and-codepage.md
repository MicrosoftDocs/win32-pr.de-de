---
description: Die VBScript-Datei WiLangID.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt.
ms.assetid: 319e9ffd-ff9f-4b4c-913e-2c571f2ec9ee
title: Verwalten von Sprache und Codepage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbfb96f04d75ed79f32c8a49fe58b8dcc86f184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369044"
---
# <a name="manage-language-and-codepage"></a><span data-ttu-id="406bb-103">Verwalten von Sprache und Codepage</span><span class="sxs-lookup"><span data-stu-id="406bb-103">Manage Language and Codepage</span></span>

<span data-ttu-id="406bb-104">Die VBScript-Datei WiLangID.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="406bb-104">The VBScript file WiLangID.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="406bb-105">Dieses Beispiel zeigt, wie mithilfe des Skripts auf die Sprachinformationen und Codepage eines Pakets zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="406bb-105">This sample shows how script is used to access a package's language information and codepage.</span></span> <span data-ttu-id="406bb-106">Weitere Informationen finden Sie unter [lokalisieren eines Windows Installer Pakets](localizing-a-windows-installer-package.md) und [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="406bb-106">For more information, see [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md) and [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>

<span data-ttu-id="406bb-107">Das Beispiel veranschaulicht die Verwendung von:</span><span class="sxs-lookup"><span data-stu-id="406bb-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="406bb-108">**OpenDatabase-Methode (Installer-Objekt)**</span><span class="sxs-lookup"><span data-stu-id="406bb-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="406bb-109">**Methode "kreaterecord"**</span><span class="sxs-lookup"><span data-stu-id="406bb-109">**CreateRecord method**</span></span>](installer-createrecord.md)
-   <span data-ttu-id="406bb-110">[**Lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="406bb-110">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="406bb-111">**OpenView-Methode**</span><span class="sxs-lookup"><span data-stu-id="406bb-111">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="406bb-112">[**SummaryInformation-Eigenschaft (Datenbankobjekt)**](database-summaryinformation.md) des [ **Datenbankobjekts**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="406bb-112">[**SummaryInformation property (Database Object)**](database-summaryinformation.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="406bb-113">Zum Verwenden dieses Beispiels ist die CScript.exe oder WScript.exe Version von Windows Script Host erforderlich.</span><span class="sxs-lookup"><span data-stu-id="406bb-113">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="406bb-114">Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie einen Befehl an der Eingabeaufforderung ein, indem Sie die folgende Syntax verwenden.</span><span class="sxs-lookup"><span data-stu-id="406bb-114">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="406bb-115">Hilfe wird angezeigt, wenn das erste Argument/?</span><span class="sxs-lookup"><span data-stu-id="406bb-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="406bb-116">oder, wenn zu wenige Argumente angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="406bb-116">or if too few arguments are specified.</span></span> <span data-ttu-id="406bb-117">Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] .</span><span class="sxs-lookup"><span data-stu-id="406bb-117">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="406bb-118">Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="406bb-118">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="406bb-119">**cscript-WiLangID.vbs \[ Pfad zu Datenbank- \] \[ Schlüsselwort \] \[ Wert\]**</span><span class="sxs-lookup"><span data-stu-id="406bb-119">**cscript WiLangID.vbs \[path to database\]\[keyword\]\[value\]**</span></span>

<span data-ttu-id="406bb-120">Geben Sie den Pfad für die Windows Installer-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="406bb-120">Specify the path to the Windows Installer database.</span></span> <span data-ttu-id="406bb-121">Um einen Wert zu ändern, geben Sie eines der folgenden Schlüsselwörter gefolgt vom neuen Wert an.</span><span class="sxs-lookup"><span data-stu-id="406bb-121">To change a value specify one of the following keywords followed by the new value.</span></span> <span data-ttu-id="406bb-122">Wenn kein Wert angegeben ist, gibt das Beispiel den aktuellen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="406bb-122">If no value is specified the sample returns the current value.</span></span>



| <span data-ttu-id="406bb-123">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="406bb-123">Keyword</span></span>      | <span data-ttu-id="406bb-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="406bb-124">Description</span></span>                                                                                                                                                                                |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="406bb-125">**Paket**</span><span class="sxs-lookup"><span data-stu-id="406bb-125">**Package**</span></span>  | <span data-ttu-id="406bb-126">Die Sprachversionen, die von der Datenbank unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="406bb-126">The language versions supported by the database.</span></span> <span data-ttu-id="406bb-127">Weitere Informationen finden Sie unter [**Template Summary**](template-summary.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="406bb-127">For information, see [**Template Summary**](template-summary.md) property.</span></span>                                                               |
| <span data-ttu-id="406bb-128">**Produkt**</span><span class="sxs-lookup"><span data-stu-id="406bb-128">**Product**</span></span>  | <span data-ttu-id="406bb-129">Die Sprache, die das Installationsprogramm für alle Zeichen folgen in der Benutzeroberfläche verwenden soll, die nicht in der Datenbank erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="406bb-129">Language the installer should use for any strings in the user interface that are not authored into the database.</span></span> <span data-ttu-id="406bb-130">Weitere Informationen finden Sie unter [**productlanguage**](productlanguage.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="406bb-130">For information, see [**ProductLanguage**](productlanguage.md) property.</span></span> |
| <span data-ttu-id="406bb-131">**Codepage**</span><span class="sxs-lookup"><span data-stu-id="406bb-131">**Codepage**</span></span> | <span data-ttu-id="406bb-132">Einzelne ANSI-Codepage für den Zeichen folgen Pool.</span><span class="sxs-lookup"><span data-stu-id="406bb-132">Single ANSI code page for the string pool.</span></span> <span data-ttu-id="406bb-133">Weitere Informationen finden Sie unter [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="406bb-133">For information, see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>                                       |



 

<span data-ttu-id="406bb-134">Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="406bb-134">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="406bb-135">Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="406bb-135">For sample utilities that do not require Windows Script Host see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="406bb-136">Weitere Informationen finden Sie unter [bestimmen der Codepage einer Installations Datenbank](determining-an-installation-database-s-code-page.md) und [Festlegen der Codepage einer Datenbank](setting-the-code-page-of-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="406bb-136">For more information, see [Determining an Installation Database's Code Page](determining-an-installation-database-s-code-page.md) and [Setting the Code Page of a Database](setting-the-code-page-of-a-database.md).</span></span>

 

 



