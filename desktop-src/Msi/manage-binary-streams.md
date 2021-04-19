---
description: Die VBScript-Datei WiStream.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt.
ms.assetid: f96d1fdd-81c8-4fb2-a23e-fda49ace8bef
title: Binäre Streams verwalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877631a40157a5d286ef0c2575732a6d561eefb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360737"
---
# <a name="manage-binary-streams"></a><span data-ttu-id="8e0e7-103">Binäre Streams verwalten</span><span class="sxs-lookup"><span data-stu-id="8e0e7-103">Manage Binary Streams</span></span>

<span data-ttu-id="8e0e7-104">Die VBScript-Datei WiStream.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="8e0e7-104">The VBScript file WiStream.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="8e0e7-105">Dieses Beispiel zeigt, wie mithilfe von Skripts binäre Datenströme in einer Windows Installer Datenbank verwaltet werden können.</span><span class="sxs-lookup"><span data-stu-id="8e0e7-105">This sample shows how script can be used to manage binary streams in a Windows Installer database.</span></span> <span data-ttu-id="8e0e7-106">Das Beispiel kann verwendet werden, um komprimierte Datei Schränke in eine Datenbank einzugeben.</span><span class="sxs-lookup"><span data-stu-id="8e0e7-106">The sample may be used to enter compressed file cabinets into a database.</span></span> <span data-ttu-id="8e0e7-107">Dieses Beispiel veranschaulicht den Betrieb der [ \_ Streams-Tabelle](-streams-table.md) in der Windows Installer-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8e0e7-107">This sample demonstrates the operation of the [\_Streams table](-streams-table.md) in the Windows Installer database.</span></span>

<span data-ttu-id="8e0e7-108">Im Beispiel wird auch die Verwendung von veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="8e0e7-108">The sample also demonstrates the use of:</span></span>

-   [<span data-ttu-id="8e0e7-109">**OpenDatabase-Methode (Installer-Objekt)**</span><span class="sxs-lookup"><span data-stu-id="8e0e7-109">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="8e0e7-110">**Methode "kreaterecord"**</span><span class="sxs-lookup"><span data-stu-id="8e0e7-110">**CreateRecord method**</span></span>](installer-createrecord.md)
-   <span data-ttu-id="8e0e7-111">[**Lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="8e0e7-111">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="8e0e7-112">**OpenView-Methode**</span><span class="sxs-lookup"><span data-stu-id="8e0e7-112">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="8e0e7-113">[**Commit-Methode**](database-commit.md) des [ **Datenbankobjekts**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="8e0e7-113">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>
-   [<span data-ttu-id="8e0e7-114">**FETCH-Methode**</span><span class="sxs-lookup"><span data-stu-id="8e0e7-114">**Fetch method**</span></span>](view-fetch.md)
-   [<span data-ttu-id="8e0e7-115">**Modify-Methode**</span><span class="sxs-lookup"><span data-stu-id="8e0e7-115">**Modify method**</span></span>](view-modify.md)
-   <span data-ttu-id="8e0e7-116">[**Execute-Methode**](view-execute.md) des [ **View-Objekts**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="8e0e7-116">[**Execute method**](view-execute.md) of the [**View object**](view-object.md)</span></span>
-   [<span data-ttu-id="8e0e7-117">**StringData (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="8e0e7-117">**StringData property**</span></span>](record-stringdata.md)
-   <span data-ttu-id="8e0e7-118">[**SetStream-Methode**](record-setstream.md) des [ **Datensatz-Objekts**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="8e0e7-118">[**SetStream method**](record-setstream.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="8e0e7-119">Sie benötigen die CScript.exe oder WScript.exe Version von Windows Script Host, um dieses Beispiel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8e0e7-119">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="8e0e7-120">Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie mithilfe der folgenden Syntax eine Befehlszeile an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="8e0e7-120">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="8e0e7-121">Hilfe wird angezeigt, wenn das erste Argument/?</span><span class="sxs-lookup"><span data-stu-id="8e0e7-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="8e0e7-122">oder, wenn zu wenige Argumente angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8e0e7-122">or if too few arguments are specified.</span></span> <span data-ttu-id="8e0e7-123">Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] .</span><span class="sxs-lookup"><span data-stu-id="8e0e7-123">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="8e0e7-124">Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="8e0e7-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="8e0e7-125">**cscript WiStream.vbs \[ Pfad zum Daten Bank \] \[ Pfad zu Datei \] \[ Optionen Daten \] \[ Strom Name\]**</span><span class="sxs-lookup"><span data-stu-id="8e0e7-125">**cscript WiStream.vbs \[path to database\]\[path to file\]\[options\]\[stream name\]**</span></span>

<span data-ttu-id="8e0e7-126">Geben Sie den Pfad zur Windows Installer Datenbank an, die den Datenstrom empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="8e0e7-126">Specify the path to the Windows Installer database that is to receive the stream.</span></span> <span data-ttu-id="8e0e7-127">Geben Sie einen Pfad zu der Binärdatei an, die die Streamdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="8e0e7-127">Specify a path to the binary file containing the stream data.</span></span> <span data-ttu-id="8e0e7-128">Um die Datenströme in der Installerdatenbank aufzulisten, lassen Sie diesen Pfad Weg.</span><span class="sxs-lookup"><span data-stu-id="8e0e7-128">To list the streams in the installer database, omit this path.</span></span> <span data-ttu-id="8e0e7-129">Sie können einen optionalen Datenstrom Namen angeben. Wenn dieser Wert weggelassen wird, wird standardmäßig der Dateiname verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e0e7-129">You may specify an optional stream name, if this is omitted it defaults to the file name.</span></span>

<span data-ttu-id="8e0e7-130">Die folgende Option kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8e0e7-130">The following option may be specified.</span></span>



| <span data-ttu-id="8e0e7-131">Option</span><span class="sxs-lookup"><span data-stu-id="8e0e7-131">Option</span></span>              | <span data-ttu-id="8e0e7-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e0e7-132">Description</span></span>                                                                                     |
|---------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e0e7-133">keine Option angegeben.</span><span class="sxs-lookup"><span data-stu-id="8e0e7-133">no option specified</span></span> | <span data-ttu-id="8e0e7-134">Fügen Sie der Windows Installer Datenbank einen Stream hinzu.</span><span class="sxs-lookup"><span data-stu-id="8e0e7-134">Add a stream to the Windows Installer database.</span></span>                                                 |
| <span data-ttu-id="8e0e7-135">/d</span><span class="sxs-lookup"><span data-stu-id="8e0e7-135">/d</span></span>                  | <span data-ttu-id="8e0e7-136">Entfernen Sie einen Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="8e0e7-136">Remove a stream.</span></span> <span data-ttu-id="8e0e7-137">Auf dieses Optionsflag muss der Name des zu entfernenden subspeichers folgen.</span><span class="sxs-lookup"><span data-stu-id="8e0e7-137">This option flag must be followed by the name of the substorage being removed.</span></span> |



 

<span data-ttu-id="8e0e7-138">Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="8e0e7-138">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="8e0e7-139">Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="8e0e7-139">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



