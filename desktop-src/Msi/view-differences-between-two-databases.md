---
description: Die VBScript-Datei WiDiffDb.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. Dieses Beispielskript generiert eine temporäre Transformations Datei zwischen zwei Windows Installer-Datenbanken und zeigt die Transformation an.
ms.assetid: 9750ddc6-de8d-48e9-a984-892f0cf4ac3b
title: Anzeigen von Unterschieden zwischen zwei Datenbanken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b0c97afc0bd7145170209ed87497b6af90e64d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525874"
---
# <a name="view-differences-between-two-databases"></a><span data-ttu-id="ac150-104">Anzeigen von Unterschieden zwischen zwei Datenbanken</span><span class="sxs-lookup"><span data-stu-id="ac150-104">View Differences Between Two Databases</span></span>

<span data-ttu-id="ac150-105">Die VBScript-Datei WiDiffDb.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ac150-105">The VBScript file WiDiffDb.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="ac150-106">Dieses Beispielskript generiert eine temporäre Transformations Datei zwischen zwei Windows Installer-Datenbanken und zeigt die Transformation an.</span><span class="sxs-lookup"><span data-stu-id="ac150-106">This sample script generates a temporary transform file between two Windows Installer databases and displays the transform.</span></span>

<span data-ttu-id="ac150-107">Das Beispiel veranschaulicht die Verwendung von:</span><span class="sxs-lookup"><span data-stu-id="ac150-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="ac150-108">**OpenDatabase-Methode (Installer-Objekt)**</span><span class="sxs-lookup"><span data-stu-id="ac150-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="ac150-109">[**Lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="ac150-109">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="ac150-110">**OpenView-Methode**</span><span class="sxs-lookup"><span data-stu-id="ac150-110">**OpenView method**</span></span>](database-openview.md)
-   [<span data-ttu-id="ac150-111">**SummaryInformation (Eigenschaft) (Datenbankobjekt)**</span><span class="sxs-lookup"><span data-stu-id="ac150-111">**SummaryInformation property (Database Object)**</span></span>](database-summaryinformation.md)
-   [<span data-ttu-id="ac150-112">**GenerateTransform-Methode**</span><span class="sxs-lookup"><span data-stu-id="ac150-112">**GenerateTransform method**</span></span>](database-generatetransform.md)
-   [<span data-ttu-id="ac150-113">**Applytransform-Methode**</span><span class="sxs-lookup"><span data-stu-id="ac150-113">**ApplyTransform method**</span></span>](database-applytransform.md)
-   [<span data-ttu-id="ac150-114">**Datenbankobjekt**</span><span class="sxs-lookup"><span data-stu-id="ac150-114">**Database object**</span></span>](database-object.md)
-   <span data-ttu-id="ac150-115">[**Fetch-Methode**](view-fetch.md) des [ **View-Objekts**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="ac150-115">[**Fetch method**](view-fetch.md) of the [**View object**](view-object.md)</span></span>
-   [<span data-ttu-id="ac150-116">**IsNull-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="ac150-116">**IsNull property**</span></span>](record-isnull.md)
-   <span data-ttu-id="ac150-117">[**StringData-Eigenschaft**](record-stringdata.md) des [ **Datensatz-Objekts**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="ac150-117">[**StringData property**](record-stringdata.md) of the [**Record object**](record-object.md)</span></span>
-   [<span data-ttu-id="ac150-118">\_Transformview-Tabelle</span><span class="sxs-lookup"><span data-stu-id="ac150-118">\_TransformView table</span></span>](-transformview-table.md)

<span data-ttu-id="ac150-119">Zum Verwenden dieses Beispiels ist die CScript.exe Version von Windows Script Host erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ac150-119">Using this sample requires the CScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="ac150-120">Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie einen Befehl an der Eingabeaufforderung ein, indem Sie die folgende Syntax verwenden.</span><span class="sxs-lookup"><span data-stu-id="ac150-120">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="ac150-121">Hilfe wird angezeigt, wenn das erste Argument/?</span><span class="sxs-lookup"><span data-stu-id="ac150-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="ac150-122">oder, wenn zu wenige Argumente angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ac150-122">or if too few arguments are specified.</span></span> <span data-ttu-id="ac150-123">Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] .</span><span class="sxs-lookup"><span data-stu-id="ac150-123">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="ac150-124">Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="ac150-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="ac150-125">**cscript WiDiffDb.vbs** *\[ Pfad zum ursprünglichen Daten Bank \] \[ Pfad zur über \] arbeiteten Datenbank*</span><span class="sxs-lookup"><span data-stu-id="ac150-125">**cscript WiDiffDb.vbs** *\[path to original database\]\[path to revised database\]*</span></span>

<span data-ttu-id="ac150-126">Geben Sie den Pfad zur ursprünglichen Windows Installer Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="ac150-126">Specify the path to the original Windows Installer database.</span></span> <span data-ttu-id="ac150-127">Geben Sie den Pfad zur überarbeiteten Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="ac150-127">Specify the path to the revised database.</span></span> <span data-ttu-id="ac150-128">Im Beispielskript wird die Transformation angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ac150-128">The sample script will display the transform.</span></span>

<span data-ttu-id="ac150-129">Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="ac150-129">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="ac150-130">Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ac150-130">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



