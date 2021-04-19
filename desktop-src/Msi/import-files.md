---
description: Die VBScript-Datei WiImport.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. Dieses Beispiel zeigt, wie Sie ein Skript schreiben, um Tabellen in eine Windows Installer Datenbank zu importieren.
ms.assetid: 37580bd6-30c7-4239-9717-223a381ba021
title: Dateien importieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8508ee4e385e3edc737515f1b524de074489fb2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343762"
---
# <a name="import-files"></a><span data-ttu-id="d3b78-104">Dateien importieren</span><span class="sxs-lookup"><span data-stu-id="d3b78-104">Import Files</span></span>

<span data-ttu-id="d3b78-105">Die VBScript-Datei WiImport.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d3b78-105">The VBScript file WiImport.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="d3b78-106">Dieses Beispiel zeigt, wie Sie ein Skript schreiben, um Tabellen in eine Windows Installer Datenbank zu importieren.</span><span class="sxs-lookup"><span data-stu-id="d3b78-106">This sample shows how to write a script to import tables into a Windows Installer database.</span></span>

<span data-ttu-id="d3b78-107">Das Skript stellt eine Verbindung mit einem [**Installerobjekt**](installer-object.md) her, öffnet eine Datenbank, verarbeitet eine Liste von Dateien und führt einen Commit für die Änderungen aus, bevor die Datenbank geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="d3b78-107">The script connects to an [**Installer**](installer-object.md) object, opens a database, processes a list of files, and commits the changes before closing the database.</span></span>

<span data-ttu-id="d3b78-108">Das Beispiel veranschaulicht die Verwendung von:</span><span class="sxs-lookup"><span data-stu-id="d3b78-108">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="d3b78-109">**OpenDatabase-Methode (Installer-Objekt)**</span><span class="sxs-lookup"><span data-stu-id="d3b78-109">**OpenDatabase Method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="d3b78-110">[**Lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="d3b78-110">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="d3b78-111">**Import-Methode**</span><span class="sxs-lookup"><span data-stu-id="d3b78-111">**Import method**</span></span>](database-import.md)
-   <span data-ttu-id="d3b78-112">[**Commit-Methode**](database-commit.md) des [ **Datenbankobjekts**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="d3b78-112">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="d3b78-113">Sie benötigen die CScript.exe oder WScript.exe Version von Windows Script Host, um dieses Beispiel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d3b78-113">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="d3b78-114">Um CScript.exe zum Ausführen dieses Beispiels zu verwenden, verwenden Sie die folgende Syntax an der Eingabeaufforderung.</span><span class="sxs-lookup"><span data-stu-id="d3b78-114">To use CScript.exe to run this sample, use the following syntax at the command prompt.</span></span>

<span data-ttu-id="d3b78-115">**cscript WiImport.vbs \[ Pfad zu Daten Bank \] \[ Pfad zu Ordner \] \[ Optionen \] \[ Archivdatei Liste**\]</span><span class="sxs-lookup"><span data-stu-id="d3b78-115">**cscript WiImport.vbs \[path to database\]\[path to folder\]\[options\] \[archive file list**\]</span></span>

<span data-ttu-id="d3b78-116">Hilfe wird angezeigt, wenn das erste Argument/?</span><span class="sxs-lookup"><span data-stu-id="d3b78-116">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="d3b78-117">oder, wenn zu wenige Argumente angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d3b78-117">or if too few arguments are specified.</span></span> <span data-ttu-id="d3b78-118">Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ Pfad zur Datei \] . Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="d3b78-118">To redirect the output to a file, end the command line with VBS > \[path to file\].The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="d3b78-119">Geben Sie den Pfad zu einer Windows Installer-Datenbank an, die erstellt werden soll oder die importierten Tabellen empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="d3b78-119">Specify the path to a Windows installer database that is to be created or that is to receive the imported tables.</span></span> <span data-ttu-id="d3b78-120">Geben Sie den Pfad zum Ordner an, in dem die Archivdateien der zu importierenden Tabellen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d3b78-120">Specify the path to the folder containing the archive files of the tables that are being imported.</span></span> <span data-ttu-id="d3b78-121">Listet die Namen der Archivdateien auf, die importiert werden.</span><span class="sxs-lookup"><span data-stu-id="d3b78-121">List the names of the archive files that are being imported.</span></span> <span data-ttu-id="d3b78-122">Platzhalter Dateinamen, wie z \* . b. IDT, können verwendet werden, um mehrere Dateien zu importieren.</span><span class="sxs-lookup"><span data-stu-id="d3b78-122">Wildcard file names, such as \*.idt, can be used to import multiple files.</span></span>

<span data-ttu-id="d3b78-123">Die folgenden Optionen können an beliebiger Stelle in der Befehlszeile vor der Datei Liste angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d3b78-123">The following options may be specified anywhere on the command line before the file list.</span></span>



| <span data-ttu-id="d3b78-124">Option</span><span class="sxs-lookup"><span data-stu-id="d3b78-124">Option</span></span>              | <span data-ttu-id="d3b78-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3b78-125">Description</span></span>                                                                                                                          |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3b78-126">keine Option angegeben.</span><span class="sxs-lookup"><span data-stu-id="d3b78-126">no option specified</span></span> | <span data-ttu-id="d3b78-127">Importieren Sie die Liste der Tabellen Archivdateien aus dem angegebenen Ordner in die Windows Installer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d3b78-127">Import the list of table archive files from the specified folder into the Windows Installer database.</span></span>                                |
| <span data-ttu-id="d3b78-128">/c</span><span class="sxs-lookup"><span data-stu-id="d3b78-128">/c</span></span>                  | <span data-ttu-id="d3b78-129">Erstellen Sie eine Windows Installer Datenbank, und importieren Sie dann die Liste der Tabellen Archivdateien aus dem angegebenen Ordner in die neue Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d3b78-129">Create a Windows Installer database and then import the list of table archive files from the specified folder into the new database.</span></span> |



 

<span data-ttu-id="d3b78-130">Weitere Informationen finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md) für weitere Skript Beispiele.</span><span class="sxs-lookup"><span data-stu-id="d3b78-130">For more information, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) for additional scripting examples.</span></span> <span data-ttu-id="d3b78-131">Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d3b78-131">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="d3b78-132">Beachten Sie, dass [ein Lokalisierungs Beispiel](a-localization-example.md) auch das [importieren lokalisierter Fehler-und Aktions Text Tabellen](importing-localized-error-and-actiontext-tables.md)veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d3b78-132">Note that [A Localization Example](a-localization-example.md) also demonstrates [Importing Localized Error and ActionText Tables](importing-localized-error-and-actiontext-tables.md).</span></span>

 

 



