---
description: Die VBScript-Datei WiUseXfm.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. In diesem Beispiel wird gezeigt, wie mithilfe eines Skripts eine Transformation auf eine Windows Installer Datenbank angewendet werden kann.
ms.assetid: e647388e-5211-463d-9e3e-b502af01fc0c
title: Anwenden einer Transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e86acc495fc2a0bb8dff562832e58d29483256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864487"
---
# <a name="apply-a-transform"></a><span data-ttu-id="c12f1-104">Anwenden einer Transformation</span><span class="sxs-lookup"><span data-stu-id="c12f1-104">Apply a Transform</span></span>

<span data-ttu-id="c12f1-105">Die VBScript-Datei WiUseXfm.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c12f1-105">The VBScript file WiUseXfm.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="c12f1-106">In diesem Beispiel wird gezeigt, wie mithilfe eines Skripts eine Transformation auf eine Windows Installer Datenbank angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c12f1-106">This sample shows how script can be used to apply a transform to a Windows Installer database.</span></span>

<span data-ttu-id="c12f1-107">Im Beispiel wird die Verwendung von veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c12f1-107">The sample demonstrates the use of</span></span>

-   [<span data-ttu-id="c12f1-108">**OpenDatabase-Methode (Installer-Objekt)**</span><span class="sxs-lookup"><span data-stu-id="c12f1-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="c12f1-109">[**Lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="c12f1-109">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="c12f1-110">**Applytransform-Methode**</span><span class="sxs-lookup"><span data-stu-id="c12f1-110">**ApplyTransform method**</span></span>](database-applytransform.md)
-   <span data-ttu-id="c12f1-111">[**Commit-Methode**](database-commit.md) des [ **Datenbankobjekts**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="c12f1-111">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="c12f1-112">Sie benötigen die CScript.exe oder WScript.exe Version von Windows Script Host, um dieses Beispiel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c12f1-112">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="c12f1-113">Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie mithilfe der folgenden Syntax eine Befehlszeile an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="c12f1-113">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="c12f1-114">Hilfe wird angezeigt, wenn das erste Argument/?</span><span class="sxs-lookup"><span data-stu-id="c12f1-114">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="c12f1-115">oder, wenn zu wenige Argumente angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c12f1-115">or if too few arguments are specified.</span></span> <span data-ttu-id="c12f1-116">Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] .</span><span class="sxs-lookup"><span data-stu-id="c12f1-116">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="c12f1-117">Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="c12f1-117">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="c12f1-118">**cscript WiUseXfm.vbs \[ Pfad zum ursprünglichen Daten Bank \] \[ Pfad zum Transformieren von Datei \] \[ Optionen\]**</span><span class="sxs-lookup"><span data-stu-id="c12f1-118">**cscript WiUseXfm.vbs \[path to original database\]\[path to transform file\]\[options\]**</span></span>

<span data-ttu-id="c12f1-119">Geben Sie den Pfad für die Windows Installer-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="c12f1-119">Specify the path to the Windows Installer database.</span></span> <span data-ttu-id="c12f1-120">Geben Sie den Pfad zur Transformations Datei an.</span><span class="sxs-lookup"><span data-stu-id="c12f1-120">Specify the path to the transform file.</span></span> <span data-ttu-id="c12f1-121">Wenn der Pfad zur Transformations Datei weggelassen wird, werden die beiden Datenbanken nur verglichen.</span><span class="sxs-lookup"><span data-stu-id="c12f1-121">If the path to the transform file is omitted, the two databases are only compared.</span></span> <span data-ttu-id="c12f1-122">Das dritte Argument ist ein optionaler numerischer Wert, der einen Satz von Fehlerbedingungen angibt, die unterdrückt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c12f1-122">The third argument is an optional numeric value that specifies a set of error conditions that are to be suppressed.</span></span> <span data-ttu-id="c12f1-123">Fügen Sie diese Werte hinzu, um mehrere Bedingungen zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="c12f1-123">Add these values together to suppress multiple conditions.</span></span>



| <span data-ttu-id="c12f1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c12f1-124">Value</span></span> | <span data-ttu-id="c12f1-125">Zu unterdrückenden Fehlerzustand</span><span class="sxs-lookup"><span data-stu-id="c12f1-125">Error condition to suppress</span></span>                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="c12f1-126">1</span><span class="sxs-lookup"><span data-stu-id="c12f1-126">1</span></span>     | <span data-ttu-id="c12f1-127">Hinzufügen einer Zeile, die bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c12f1-127">Adding a row that already exists.</span></span>             |
| <span data-ttu-id="c12f1-128">2</span><span class="sxs-lookup"><span data-stu-id="c12f1-128">2</span></span>     | <span data-ttu-id="c12f1-129">Löschen einer Zeile, die nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c12f1-129">Deleting a row that does not exist.</span></span>           |
| <span data-ttu-id="c12f1-130">4</span><span class="sxs-lookup"><span data-stu-id="c12f1-130">4</span></span>     | <span data-ttu-id="c12f1-131">Eine Tabelle, die bereits vorhanden ist, wird hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c12f1-131">Adding a table that already exists.</span></span>           |
| <span data-ttu-id="c12f1-132">8</span><span class="sxs-lookup"><span data-stu-id="c12f1-132">8</span></span>     | <span data-ttu-id="c12f1-133">Löschen einer Tabelle, die nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c12f1-133">Deleting a table that does not exist.</span></span>         |
| <span data-ttu-id="c12f1-134">16</span><span class="sxs-lookup"><span data-stu-id="c12f1-134">16</span></span>    | <span data-ttu-id="c12f1-135">Aktualisieren einer Zeile, die nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c12f1-135">Updating a row that does not exist.</span></span>           |
| <span data-ttu-id="c12f1-136">256</span><span class="sxs-lookup"><span data-stu-id="c12f1-136">256</span></span>   | <span data-ttu-id="c12f1-137">Nicht übereinstimmende Datenbank-und Transformations-Codepages.</span><span class="sxs-lookup"><span data-stu-id="c12f1-137">Mismatch of database and transform codepages.</span></span> |



 

<span data-ttu-id="c12f1-138">Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="c12f1-138">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="c12f1-139">Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="c12f1-139">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



