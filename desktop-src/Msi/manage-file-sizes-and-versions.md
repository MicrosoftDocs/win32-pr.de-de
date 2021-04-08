---
description: Die VBScript-Datei WiFilVer.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. Das Beispiel zeigt, wie Sie ein Skript zum melden oder Aktualisieren der Dateiversion, der Größe und der Sprachinformationen verwenden können.
ms.assetid: 21550eea-c30b-4738-9201-ab500356fabf
title: Verwalten von Dateigrößen und-Versionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426acf71956d87fe1458447119d79bc142f1ee75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752776"
---
# <a name="manage-file-sizes-and-versions"></a><span data-ttu-id="4aad0-104">Verwalten von Dateigrößen und-Versionen</span><span class="sxs-lookup"><span data-stu-id="4aad0-104">Manage File Sizes and Versions</span></span>

<span data-ttu-id="4aad0-105">Die VBScript-Datei WiFilVer.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="4aad0-105">The VBScript file WiFilVer.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="4aad0-106">Das Beispiel zeigt, wie Sie ein Skript zum melden oder Aktualisieren der Dateiversion, der Größe und der Sprachinformationen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="4aad0-106">The sample shows you how you can use a script to report or update the file version, size, and language information.</span></span>

<span data-ttu-id="4aad0-107">Das Beispiel zeigt auch Windows Installer Aktionen, den Zugriff auf eine Windows Installer Datenbank und die Verwendung der folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="4aad0-107">The sample also shows you Windows Installer actions, how to access a Windows Installer database, and the use of the following:</span></span>

-   <span data-ttu-id="4aad0-108">[**Installer. OpenDatabase**](installer-opendatabase.md) -Methode des [ **Installer-Objekts**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="4aad0-108">[**Installer.OpenDatabase**](installer-opendatabase.md) method of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="4aad0-109">[**Installer. File Attribute**](installer-fileattributes.md) (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4aad0-109">[**Installer.FileAttributes**](installer-fileattributes.md) property</span></span>
-   <span data-ttu-id="4aad0-110">[**Installer. flehash**](installer-filehash.md) -Methode</span><span class="sxs-lookup"><span data-stu-id="4aad0-110">[**Installer.FileHash**](installer-filehash.md) method</span></span>
-   <span data-ttu-id="4aad0-111">[**Installer. FileVersion**](installer-fileversion.md) -Methode</span><span class="sxs-lookup"><span data-stu-id="4aad0-111">[**Installer.FileVersion**](installer-fileversion.md) method</span></span>
-   <span data-ttu-id="4aad0-112">[**Installer. lasterrorrecord**](installer-lasterrorrecord.md) -Methode des [ **Installer-Objekts**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="4aad0-112">[**Installer.LastErrorRecord**](installer-lasterrorrecord.md) method of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="4aad0-113">[**Database. OpenView**](database-openview.md) -Methode</span><span class="sxs-lookup"><span data-stu-id="4aad0-113">[**Database.OpenView**](database-openview.md) method</span></span>
-   <span data-ttu-id="4aad0-114">[**Database. SummaryInformation**](database-summaryinformation.md) -Eigenschaft des [ **Database-Objekts**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="4aad0-114">[**Database.SummaryInformation**](database-summaryinformation.md) property of the [**Database Object**](database-object.md)</span></span>
-   <span data-ttu-id="4aad0-115">[**Session. doaction**](session-doaction.md) -Methode</span><span class="sxs-lookup"><span data-stu-id="4aad0-115">[**Session.DoAction**](session-doaction.md) method</span></span>
-   [<span data-ttu-id="4aad0-116">**Session. Property**</span><span class="sxs-lookup"><span data-stu-id="4aad0-116">**Session.Property**</span></span>](session-session.md)
-   <span data-ttu-id="4aad0-117">[**Session. SourcePath**](session-sourcepath.md) (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4aad0-117">[**Session.SourcePath**](session-sourcepath.md) property</span></span>
-   <span data-ttu-id="4aad0-118">[**Session. Mode**](session-mode.md) -Eigenschaft des [ **Session-Objekts**](session-object.md)</span><span class="sxs-lookup"><span data-stu-id="4aad0-118">[**Session.Mode**](session-mode.md) property of the [**Session Object**](session-object.md)</span></span>
-   <span data-ttu-id="4aad0-119">[**Record. StringData**](record-stringdata.md) (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4aad0-119">[**Record.StringData**](record-stringdata.md) property</span></span>
-   <span data-ttu-id="4aad0-120">[**Record. IntegerData**](record-integerdata.md) -Eigenschaft des [ **Datensatz-Objekts**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="4aad0-120">[**Record.IntegerData**](record-integerdata.md) property of the [**Record Object**](record-object.md)</span></span>

<span data-ttu-id="4aad0-121">Zum Verwenden dieses Beispiels ist die CScript.exe oder WScript.exe Version von Windows Script Host erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4aad0-121">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="4aad0-122">Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie einen Befehl an der Eingabeaufforderung ein, indem Sie die folgende Syntax verwenden:</span><span class="sxs-lookup"><span data-stu-id="4aad0-122">To use CScript.exe to run this sample, type a command at the command prompt by using the following syntax:</span></span>

<span data-ttu-id="4aad0-123">**cscript-WiFilVer.vbs \[ Pfad zu \] \[ optionalen Quell Speicherorten der Datenbank\]**</span><span class="sxs-lookup"><span data-stu-id="4aad0-123">**cscript WiFilVer.vbs \[path to database\]\[optional source locations\]**</span></span>

<span data-ttu-id="4aad0-124">Beachten Sie auch Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4aad0-124">Also be aware of the following:</span></span>

-   <span data-ttu-id="4aad0-125">Hilfe wird angezeigt, wenn das erste Argument/?</span><span class="sxs-lookup"><span data-stu-id="4aad0-125">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="4aad0-126">oder, wenn zu wenige Argumente angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4aad0-126">or if too few arguments are specified.</span></span>
-   <span data-ttu-id="4aad0-127">Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] .</span><span class="sxs-lookup"><span data-stu-id="4aad0-127">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span>
-   <span data-ttu-id="4aad0-128">Im Beispiel wird der Wert 0 (null) für Erfolg zurückgegeben, 1 (eins), wenn die Hilfe aufgerufen wird, und 2 (zwei), wenn das Skript fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="4aad0-128">The sample returns a value of 0 (zero) for success, 1 (one) if help is invoked, and 2 (two) if the script fails.</span></span>

<span data-ttu-id="4aad0-129">Geben Sie die Windows Installer Datenbank an, die Sie aktualisieren möchten. diese muss sich im Stammverzeichnis der Quelldatei befinden.</span><span class="sxs-lookup"><span data-stu-id="4aad0-129">Specify the Windows Installer database that you want to be updated, which must be located at the source file root.</span></span> <span data-ttu-id="4aad0-130">Sie können jedoch Datenquellen für die Datenbank an separaten Speicherorten angeben.</span><span class="sxs-lookup"><span data-stu-id="4aad0-130">However, you can specify sources for the database at separate locations.</span></span> <span data-ttu-id="4aad0-131">Wenn die Quelle komprimiert ist, werden alle Dateien im Stamm geöffnet.</span><span class="sxs-lookup"><span data-stu-id="4aad0-131">If the source is compressed, all the files are opened at the root.</span></span>

<span data-ttu-id="4aad0-132">Die folgenden Optionen können an beliebiger Stelle in der Befehlszeile angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4aad0-132">The following options can be specified at any location on the command line.</span></span>



| <span data-ttu-id="4aad0-133">Option</span><span class="sxs-lookup"><span data-stu-id="4aad0-133">Option</span></span>                | <span data-ttu-id="4aad0-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4aad0-134">Description</span></span>                                                                              |
|-----------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aad0-135">*keine Option angegeben.*</span><span class="sxs-lookup"><span data-stu-id="4aad0-135">*no option specified*</span></span> | <span data-ttu-id="4aad0-136">Zeigen Sie die Dateiinformationen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="4aad0-136">Display the file information of the database.</span></span>                                            |
| <span data-ttu-id="4aad0-137">/U</span><span class="sxs-lookup"><span data-stu-id="4aad0-137">/u</span></span>                    | <span data-ttu-id="4aad0-138">Aktualisieren Sie die Dateigröße, die Version und die Sprachinformationen in der Datenbank aus der Quelle.</span><span class="sxs-lookup"><span data-stu-id="4aad0-138">Update the file size, version, and language information in the database from the source.</span></span> |



 

<span data-ttu-id="4aad0-139">Weitere Informationen finden Sie unter [Windows Installer von Skript Beispielen](windows-installer-scripting-examples.md) und [Windows Installer Entwicklungs Tools](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="4aad0-139">For more information, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) and [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



