---
description: Die VBScript-Datei WiExport.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt.
ms.assetid: 3ff7bd48-cb22-4d5b-a607-39eaeb67c55b
title: Dateien exportieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1512650ee144fc00c2de851051b9bbb4d98a21e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343401"
---
# <a name="export-files"></a><span data-ttu-id="162d9-103">Dateien exportieren</span><span class="sxs-lookup"><span data-stu-id="162d9-103">Export Files</span></span>

<span data-ttu-id="162d9-104">Die VBScript-Datei WiExport.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="162d9-104">The VBScript file WiExport.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="162d9-105">Dieses Beispiel zeigt, wie Sie ein Skript schreiben, um Tabellen in eine Windows Installer Datenbank zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="162d9-105">This sample shows how to write script to export tables into a Windows Installer database.</span></span> <span data-ttu-id="162d9-106">Das Skript Beispiel stellt eine Verbindung mit einem [**Installer**](installer-object.md) -Objekt her, öffnet eine Datenbank und exportiert Tabellen in Archivdateien.</span><span class="sxs-lookup"><span data-stu-id="162d9-106">The script sample connects to an [**Installer**](installer-object.md) object, opens a database and exports tables to archive files.</span></span>

<span data-ttu-id="162d9-107">Das Beispiel veranschaulicht die Verwendung von:</span><span class="sxs-lookup"><span data-stu-id="162d9-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="162d9-108">**OpenDatabase-Methode (Installer-Objekt)**</span><span class="sxs-lookup"><span data-stu-id="162d9-108">**OpenDatabase Method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="162d9-109">[**Lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="162d9-109">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="162d9-110">**Export Methode**</span><span class="sxs-lookup"><span data-stu-id="162d9-110">**Export method**</span></span>](database-export.md)
-   <span data-ttu-id="162d9-111">[**OpenView-Methode**](database-openview.md) des [ **Datenbankobjekts**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="162d9-111">[**OpenView method**](database-openview.md) of the [**Database object**](database-object.md)</span></span>
-   <span data-ttu-id="162d9-112">[**Fetch-Methode**](view-fetch.md) des [ **View-Objekts**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="162d9-112">[**Fetch method**](view-fetch.md) of the [**View object**](view-object.md)</span></span>
-   <span data-ttu-id="162d9-113">[**StringData-Eigenschaft**](record-stringdata.md) des [ **Datensatz-Objekts**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="162d9-113">[**StringData property**](record-stringdata.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="162d9-114">Sie benötigen die CScript.exe oder WScript.exe Version von Windows Script Host, um dieses Beispiel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="162d9-114">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="162d9-115">Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie mithilfe der folgenden Syntax eine Befehlszeile an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="162d9-115">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="162d9-116">Hilfe wird angezeigt, wenn das erste Argument/?</span><span class="sxs-lookup"><span data-stu-id="162d9-116">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="162d9-117">oder, wenn zu wenige Argumente angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="162d9-117">or if too few arguments are specified.</span></span> <span data-ttu-id="162d9-118">Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] .</span><span class="sxs-lookup"><span data-stu-id="162d9-118">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="162d9-119">Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="162d9-119">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="162d9-120">**cscript WiExport.vbs \[ Pfad zur \] \[ \] \[ \] \[ Liste der Tabellennamen der Ordneroptionen\]**</span><span class="sxs-lookup"><span data-stu-id="162d9-120">**cscript WiExport.vbs \[path to database\]\[path to folder\]\[options\]\[table name list\]**</span></span>

<span data-ttu-id="162d9-121">Geben Sie den Pfad zur Installer-Datenbank an, aus der die Tabellen exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="162d9-121">Specify the path to the installer database from which the tables are being exported.</span></span> <span data-ttu-id="162d9-122">Geben Sie den Pfad zu dem Ordner an, in den die exportierten Archivdateien kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="162d9-122">Specify the path to the folder into which the exported archive files are to be copied.</span></span> <span data-ttu-id="162d9-123">Listet die Namen der zu exportierenden [Datenbanktabellen](database-tables.md) auf.</span><span class="sxs-lookup"><span data-stu-id="162d9-123">List the case-sensitive names of the [database tables](database-tables.md) being exported.</span></span> <span data-ttu-id="162d9-124">Geben \* Sie "" an, um alle Tabellen einschließlich " \_ SummaryInformation" zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="162d9-124">Specify '\*' to export all the tables including \_SummaryInformation.</span></span>

<span data-ttu-id="162d9-125">Die folgenden Optionen können an beliebiger Stelle in der Befehlszeile vor der Liste der Tabellennamen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="162d9-125">The following options may be specified anywhere on the command line before the table name list.</span></span>



| <span data-ttu-id="162d9-126">Option</span><span class="sxs-lookup"><span data-stu-id="162d9-126">Option</span></span>              | <span data-ttu-id="162d9-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="162d9-127">Description</span></span>                                            |
|---------------------|--------------------------------------------------------|
| <span data-ttu-id="162d9-128">keine Option angegeben.</span><span class="sxs-lookup"><span data-stu-id="162d9-128">no option specified</span></span> | <span data-ttu-id="162d9-129">Exportierte Archivdateien haben möglicherweise einen langen Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="162d9-129">Exported archive files may have a long file name.</span></span>      |
| <span data-ttu-id="162d9-130">/s</span><span class="sxs-lookup"><span data-stu-id="162d9-130">/s</span></span>                  | <span data-ttu-id="162d9-131">Erzwingen Sie, dass exportierte Archivdateien kurze Dateinamen haben.</span><span class="sxs-lookup"><span data-stu-id="162d9-131">Force exported archive files to have short file names.</span></span> |



 

<span data-ttu-id="162d9-132">Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="162d9-132">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="162d9-133">Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="162d9-133">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



