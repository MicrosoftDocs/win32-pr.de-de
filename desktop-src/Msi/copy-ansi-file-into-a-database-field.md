---
description: Die VBScript-Codebeispiel Datei WiTextIn.vbs in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt.
ms.assetid: ba6c6367-ebb1-4981-ae3a-bcff68aacdbf
title: ANSI-Datei in ein Datenbankfeld kopieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dc6c4d3a945177581a35bf6b19d89855abb5ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362547"
---
# <a name="copy-ansi-file-into-a-database-field"></a><span data-ttu-id="b3c49-103">ANSI-Datei in ein Datenbankfeld kopieren</span><span class="sxs-lookup"><span data-stu-id="b3c49-103">Copy ANSI File Into a Database Field</span></span>

<span data-ttu-id="b3c49-104">Die VBScript-Codebeispiel Datei WiTextIn.vbs in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b3c49-104">The VBScript code sample file WiTextIn.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="b3c49-105">Das Beispiel zeigt, wie ein-Skript verwendet werden kann, um eine Datei in ein Textfeld einer Windows Installer-Datenbank zu kopieren und die Verarbeitung von Primärschlüssel Daten zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="b3c49-105">The sample shows how a script can be used to copy a file into a text field of a Windows Installer database, and demonstrates the processing of primary key data.</span></span>

<span data-ttu-id="b3c49-106">Das Codebeispiel zeigt außerdem Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b3c49-106">The code sample also shows you the following:</span></span>

-   <span data-ttu-id="b3c49-107">[**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md) und die [**lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [**Installer-Objekts**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="b3c49-107">[**OpenDatabase method (Installer Object)**](installer-opendatabase.md) and the [**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="b3c49-108">[**OpenView-Methode**](database-openview.md), die [**Commit-Methode**](database-commit.md)und die [**primarykeys-Eigenschaft**](database-primarykeys.md) des Database- [**Objekts**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="b3c49-108">[**OpenView method**](database-openview.md), the [**Commit method**](database-commit.md), and the [**PrimaryKeys property**](database-primarykeys.md) of the [**Database Object**](database-object.md)</span></span>
-   <span data-ttu-id="b3c49-109">[**Fetch-Methode**](view-fetch.md) und die [**Modify-Methode**](view-modify.md) des View- [**Objekts**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="b3c49-109">[**Fetch method**](view-fetch.md) and the [**Modify method**](view-modify.md) of the [**View Object**](view-object.md)</span></span>
-   <span data-ttu-id="b3c49-110">[**StringData-Eigenschaft**](record-stringdata.md) und die Read [**Stream-Methode**](record-readstream.md) des [**Datensatz-Objekts**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="b3c49-110">[**StringData property**](record-stringdata.md) and [**ReadStream method**](record-readstream.md) of the [**Record Object**](record-object.md)</span></span>

<span data-ttu-id="b3c49-111">Um das Codebeispiel zu verwenden, benötigen Sie die CScript.exe oder WScript.exe Version von Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="b3c49-111">To use the code sample you need the CScript.exe or WScript.exe version of Windows Script Host.</span></span>

<span data-ttu-id="b3c49-112">**So verwenden Sie CScript.exe, um dieses Beispiel auszuführen**</span><span class="sxs-lookup"><span data-stu-id="b3c49-112">**To use CScript.exe to run this sample**</span></span>

-   <span data-ttu-id="b3c49-113">Geben Sie an der Eingabeaufforderung die folgende Syntax ein:</span><span class="sxs-lookup"><span data-stu-id="b3c49-113">At the command prompt, type the following syntax:</span></span>

    <span data-ttu-id="b3c49-114">**cscript WiTextIn.vbs \[ Pfad zum Daten Bank \] \[ Tabellennamen \] \[ Primärschlüssel Werte \] \[ Spaltenname \] \[ Pfad zu Datei\]**</span><span class="sxs-lookup"><span data-stu-id="b3c49-114">**cscript WiTextIn.vbs \[path to database\]\[table name\]\[primary key values\]\[column name\]\[path to file\]**</span></span>

> [!Note]  
> <span data-ttu-id="b3c49-115">Hilfe wird angezeigt, wenn das erste Argument/?</span><span class="sxs-lookup"><span data-stu-id="b3c49-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="b3c49-116">oder, wenn zu wenige Argumente angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b3c49-116">or if too few arguments are specified.</span></span>

 

<span data-ttu-id="b3c49-117">**So leiten Sie die Ausgabe in eine Datei um**</span><span class="sxs-lookup"><span data-stu-id="b3c49-117">**To redirect the output to a file**</span></span>

-   <span data-ttu-id="b3c49-118">Beenden Sie die Befehlszeile mit folgendem: **VSB > \[ Pfad zur Datei \] . T**</span><span class="sxs-lookup"><span data-stu-id="b3c49-118">End the command line with the following: **VBS > \[path to file\]. T**</span></span>

> [!Note]  
> <span data-ttu-id="b3c49-119">Im Beispiel wird der Wert 0 (null) für Erfolg zurückgegeben, 1 (eins), wenn die Hilfe aufgerufen wird, und 2 (zwei), wenn das Skript fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="b3c49-119">The sample returns a value of 0 (zero) for success, 1 (one) if Help is invoked, and 2 (two) if the script fails.</span></span>

 

<span data-ttu-id="b3c49-120">In der folgenden Liste sind die Elemente aufgeführt, die Sie angeben müssen:</span><span class="sxs-lookup"><span data-stu-id="b3c49-120">The following list identifies the items that you must specify:</span></span>

-   <span data-ttu-id="b3c49-121">Geben Sie den Pfad für die Windows Installer-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="b3c49-121">Specify the path to the Windows Installer database.</span></span>
-   <span data-ttu-id="b3c49-122">Geben Sie den Namen der Datenbanktabelle an.</span><span class="sxs-lookup"><span data-stu-id="b3c49-122">Specify the name of the database table.</span></span>
-   <span data-ttu-id="b3c49-123">Geben Sie alle Primärschlüssel Werte für die Zeile in der angegebenen Reihenfolge an, und verkettet mit Doppelpunkten.</span><span class="sxs-lookup"><span data-stu-id="b3c49-123">Specify all the primary key values for the row, in order, and concatenated with colons.</span></span>
-   <span data-ttu-id="b3c49-124">Geben Sie einen Spaltennamen an, der keine Schlüssel Spalte ist.</span><span class="sxs-lookup"><span data-stu-id="b3c49-124">Specify a column name that is not a key column.</span></span> <span data-ttu-id="b3c49-125">Dies ist die Spalte, die die Daten empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="b3c49-125">This is the column that you want to receive the data.</span></span>
-   <span data-ttu-id="b3c49-126">Geben Sie den Pfad zu der Textdatei an, die kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="b3c49-126">Specify the path to the text file that is being copied.</span></span>

> [!Note]  
> <span data-ttu-id="b3c49-127">Wenn das letzte Argument weggelassen wird, wird der aktuelle Wert im Feld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b3c49-127">If the last argument is omitted, the current value in the field is displayed.</span></span>

 

<span data-ttu-id="b3c49-128">Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="b3c49-128">For more scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="b3c49-129">Beispiel Hilfsprogramme, die den Windows Script Host nicht benötigen, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="b3c49-129">For sample utilities that do not require the Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



