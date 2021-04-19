---
description: Die VBScript-Datei WiLstXfm.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. Dieses Skript Beispiel kann verwendet werden, um eine Transformations Datei anzuzeigen.
ms.assetid: c2e3dd56-b0e5-481a-b7b8-5000fa686850
title: Anzeigen einer Transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f4a858f8deb115de967da3b4d485b596f85cee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345688"
---
# <a name="view-a-transform"></a><span data-ttu-id="07835-104">Anzeigen einer Transformation</span><span class="sxs-lookup"><span data-stu-id="07835-104">View a Transform</span></span>

<span data-ttu-id="07835-105">Die VBScript-Datei WiLstXfm.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="07835-105">The VBScript file WiLstXfm.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="07835-106">Dieses Skript Beispiel kann verwendet werden, um eine Transformations Datei anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="07835-106">This script sample can be used to view a transform file.</span></span>

<span data-ttu-id="07835-107">Das Beispiel veranschaulicht die Verwendung von:</span><span class="sxs-lookup"><span data-stu-id="07835-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="07835-108">\_Transformview-Tabelle</span><span class="sxs-lookup"><span data-stu-id="07835-108">\_TransformView table</span></span>](-transformview-table.md)
-   [<span data-ttu-id="07835-109">**OpenDatabase-Methode (Installer-Objekt)**</span><span class="sxs-lookup"><span data-stu-id="07835-109">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="07835-110">[**Lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="07835-110">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="07835-111">**Applytransform-Methode**</span><span class="sxs-lookup"><span data-stu-id="07835-111">**ApplyTransform method**</span></span>](database-applytransform.md)
-   [<span data-ttu-id="07835-112">**OpenView-Methode**</span><span class="sxs-lookup"><span data-stu-id="07835-112">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="07835-113">[**Commit-Methode**](database-commit.md) des [ **Datenbankobjekts**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="07835-113">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>
-   [<span data-ttu-id="07835-114">**IsNull-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="07835-114">**IsNull property**</span></span>](record-isnull.md)
-   <span data-ttu-id="07835-115">[**StringData-Eigenschaft**](record-stringdata.md) des [ **Datensatz-Objekts**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="07835-115">[**StringData property**](record-stringdata.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="07835-116">Zum Verwenden dieses Beispiels ist die CScript.exe Version von Windows Script Host erforderlich.</span><span class="sxs-lookup"><span data-stu-id="07835-116">Using this sample requires the CScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="07835-117">Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie einen Befehl an der Eingabeaufforderung ein, indem Sie die folgende Syntax verwenden.</span><span class="sxs-lookup"><span data-stu-id="07835-117">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="07835-118">Hilfe wird angezeigt, wenn das erste Argument/?</span><span class="sxs-lookup"><span data-stu-id="07835-118">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="07835-119">oder, wenn zu wenige Argumente angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="07835-119">or if too few arguments are specified.</span></span> <span data-ttu-id="07835-120">Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] .</span><span class="sxs-lookup"><span data-stu-id="07835-120">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="07835-121">Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="07835-121">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="07835-122">**cscript WiLstXfm.vbs** Pfad zum Verweis auf die *\[ Daten Bank \] \[ Option \] \[ , die angezeigt \] werden* soll.</span><span class="sxs-lookup"><span data-stu-id="07835-122">**cscript WiLstXfm.vbs** *\[path to reference database\]\[option\]\[path to transform to be viewed\]*</span></span>

<span data-ttu-id="07835-123">Geben Sie den Pfad zum Verweis Windows Installer-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="07835-123">Specify the path to the reference Windows Installer database.</span></span> <span data-ttu-id="07835-124">Geben Sie eine Liste mit Pfaden zum Transformieren von Dateien an, die angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="07835-124">Specify a list of paths to transform files that are being viewed.</span></span> <span data-ttu-id="07835-125">Jedem Pfad in der Liste kann ein optionaler numerischer Wert vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="07835-125">Each path in the list may by preceded by an optional numeric value.</span></span> <span data-ttu-id="07835-126">Dieser Wert gibt eine Reihe von Fehlerbedingungen an, die unterdrückt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="07835-126">This value specifies a set of error conditions that are to be suppressed.</span></span> <span data-ttu-id="07835-127">Sie können diese Werte hinzufügen, um mehrere Bedingungen zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="07835-127">You may add these values together to suppress multiple conditions.</span></span> <span data-ttu-id="07835-128">Wenn keine numerische Option angegeben wird, werden alle Fehlerbedingungen unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="07835-128">If no numeric option is specified, all the error conditions are suppressed.</span></span> <span data-ttu-id="07835-129">Die Argumente in dieser Liste werden in der Reihenfolge von links nach rechts ausgeführt, in der Sie in der Befehlszeile angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="07835-129">The arguments in this list are executed in the left-to-right order in which they appear on the command line.</span></span>



| <span data-ttu-id="07835-130">Wert</span><span class="sxs-lookup"><span data-stu-id="07835-130">Value</span></span> | <span data-ttu-id="07835-131">Zu unterdrückenden Fehlerzustand</span><span class="sxs-lookup"><span data-stu-id="07835-131">Error condition to suppress</span></span>                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="07835-132">1</span><span class="sxs-lookup"><span data-stu-id="07835-132">1</span></span>     | <span data-ttu-id="07835-133">Hinzufügen einer Zeile, die bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="07835-133">Adding a row that already exists.</span></span>             |
| <span data-ttu-id="07835-134">2</span><span class="sxs-lookup"><span data-stu-id="07835-134">2</span></span>     | <span data-ttu-id="07835-135">Löschen einer Zeile, die nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="07835-135">Deleting a row that does not exist.</span></span>           |
| <span data-ttu-id="07835-136">4</span><span class="sxs-lookup"><span data-stu-id="07835-136">4</span></span>     | <span data-ttu-id="07835-137">Eine Tabelle, die bereits vorhanden ist, wird hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="07835-137">Adding a table that already exists.</span></span>           |
| <span data-ttu-id="07835-138">8</span><span class="sxs-lookup"><span data-stu-id="07835-138">8</span></span>     | <span data-ttu-id="07835-139">Löschen einer Tabelle, die nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="07835-139">Deleting a table that does not exist.</span></span>         |
| <span data-ttu-id="07835-140">16</span><span class="sxs-lookup"><span data-stu-id="07835-140">16</span></span>    | <span data-ttu-id="07835-141">Aktualisieren einer Zeile, die nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="07835-141">Updating a row that does not exist.</span></span>           |
| <span data-ttu-id="07835-142">256</span><span class="sxs-lookup"><span data-stu-id="07835-142">256</span></span>   | <span data-ttu-id="07835-143">Nicht übereinstimmende Datenbank-und Transformations-Codepages.</span><span class="sxs-lookup"><span data-stu-id="07835-143">Mismatch of database and transform codepages.</span></span> |



 

<span data-ttu-id="07835-144">Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="07835-144">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="07835-145">Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="07835-145">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



