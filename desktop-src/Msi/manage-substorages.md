---
description: Die VBScript-Datei WiSubStg.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt.
ms.assetid: a0248dfb-e406-4ce6-ab11-1e428aa67af4
title: Verwalten von substorages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01876efdb85bdc89df1b4d64332d44674e5e860e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348978"
---
# <a name="manage-substorages"></a><span data-ttu-id="ae8d6-103">Verwalten von substorages</span><span class="sxs-lookup"><span data-stu-id="ae8d6-103">Manage Substorages</span></span>

<span data-ttu-id="ae8d6-104">Die VBScript-Datei WiSubStg.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ae8d6-104">The VBScript file WiSubStg.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="ae8d6-105">In diesem Beispiel wird gezeigt, wie Sie mithilfe von Skripts substorages in einer Windows Installer Datenbank verwalten können.</span><span class="sxs-lookup"><span data-stu-id="ae8d6-105">This sample shows how script can be used to manage substorages in a Windows Installer database.</span></span> <span data-ttu-id="ae8d6-106">Eine Transformation kann zu einer vorhandenen Windows Installer Datenbank als unter Speicher hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ae8d6-106">A transform can be added to an existing Windows Installer database as a substorage.</span></span>

<span data-ttu-id="ae8d6-107">Das Beispiel veranschaulicht die Verwendung von:</span><span class="sxs-lookup"><span data-stu-id="ae8d6-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="ae8d6-108">\_Tabelle "Storages"</span><span class="sxs-lookup"><span data-stu-id="ae8d6-108">\_Storages table</span></span>](-storages-table.md)
-   [<span data-ttu-id="ae8d6-109">**OpenDatabase-Methode (Installer-Objekt)**</span><span class="sxs-lookup"><span data-stu-id="ae8d6-109">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="ae8d6-110">**Methode "kreaterecord"**</span><span class="sxs-lookup"><span data-stu-id="ae8d6-110">**CreateRecord method**</span></span>](installer-createrecord.md)
-   <span data-ttu-id="ae8d6-111">[**Lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="ae8d6-111">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="ae8d6-112">**OpenView-Methode**</span><span class="sxs-lookup"><span data-stu-id="ae8d6-112">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="ae8d6-113">[**Commit-Methode**](database-commit.md) des [ **Datenbankobjekts**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="ae8d6-113">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>
-   [<span data-ttu-id="ae8d6-114">**FETCH-Methode**</span><span class="sxs-lookup"><span data-stu-id="ae8d6-114">**Fetch method**</span></span>](view-fetch.md)
-   [<span data-ttu-id="ae8d6-115">**Modify-Methode**</span><span class="sxs-lookup"><span data-stu-id="ae8d6-115">**Modify method**</span></span>](view-modify.md)
-   <span data-ttu-id="ae8d6-116">[**Execute-Methode**](view-execute.md) des [ **View-Objekts**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="ae8d6-116">[**Execute method**](view-execute.md) of the [**View object**](view-object.md)</span></span>
-   [<span data-ttu-id="ae8d6-117">**StringData (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="ae8d6-117">**StringData property**</span></span>](record-stringdata.md)
-   <span data-ttu-id="ae8d6-118">[**SetStream-Methode**](record-setstream.md) des [ **Datensatz-Objekts**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="ae8d6-118">[**SetStream method**](record-setstream.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="ae8d6-119">Sie benötigen die CScript.exe oder WScript.exe Version von Windows Script Host, um dieses Beispiel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae8d6-119">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="ae8d6-120">Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie mithilfe der folgenden Syntax eine Befehlszeile an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="ae8d6-120">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="ae8d6-121">Hilfe wird angezeigt, wenn das erste Argument/?</span><span class="sxs-lookup"><span data-stu-id="ae8d6-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="ae8d6-122">oder, wenn zu wenige Argumente angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ae8d6-122">or if too few arguments are specified.</span></span> <span data-ttu-id="ae8d6-123">Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] .</span><span class="sxs-lookup"><span data-stu-id="ae8d6-123">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="ae8d6-124">Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="ae8d6-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="ae8d6-125">**cscript WiSubStg.vbs \[ Pfad zu Daten Bank \] \[ Pfad zu Datei \] \[ Optionen \] \[ unter Speicher Name\]**</span><span class="sxs-lookup"><span data-stu-id="ae8d6-125">**cscript WiSubStg.vbs \[path to database\]\[path to file\]\[options\]\[substorage name\]**</span></span>

<span data-ttu-id="ae8d6-126">Geben Sie den Pfad zur Windows Installer Datenbank an, um unter Speicher hinzuzufügen oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="ae8d6-126">Specify the path to the Windows Installer database to add or remove substorage.</span></span> <span data-ttu-id="ae8d6-127">Geben Sie einen Pfad zur Transformation oder Datenbankdatei an, die als unter Speicher hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="ae8d6-127">Specify a path to the transform or database file that is being added as substorage.</span></span> <span data-ttu-id="ae8d6-128">Zum Auflisten der substorages in der Windows Installer-Datenbank lassen Sie den Pfad zu dieser Datei aus.</span><span class="sxs-lookup"><span data-stu-id="ae8d6-128">To list the substorages in the Windows Installer database, omit the path to this file.</span></span> <span data-ttu-id="ae8d6-129">Sie können einen optionalen unter Speicher Namen angeben. Wenn dieser Wert ausgelassen wird, wird der Name des unter Speichers standardmäßig auf den Dateinamen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ae8d6-129">You may specify an optional substorage name, if this is omitted the substorage name defaults to the file name.</span></span>

<span data-ttu-id="ae8d6-130">Die folgende Option kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ae8d6-130">The following option may be specified.</span></span>



| <span data-ttu-id="ae8d6-131">Option</span><span class="sxs-lookup"><span data-stu-id="ae8d6-131">Option</span></span>              | <span data-ttu-id="ae8d6-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae8d6-132">Description</span></span>                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae8d6-133">keine Option angegeben.</span><span class="sxs-lookup"><span data-stu-id="ae8d6-133">no option specified</span></span> | <span data-ttu-id="ae8d6-134">Fügen Sie der Windows Installer Datenbank einen unter Speicher hinzu.</span><span class="sxs-lookup"><span data-stu-id="ae8d6-134">Add a substorage to the Windows Installer database.</span></span>                                                 |
| <span data-ttu-id="ae8d6-135">/d</span><span class="sxs-lookup"><span data-stu-id="ae8d6-135">/d</span></span>                  | <span data-ttu-id="ae8d6-136">Entfernen Sie einen unter Speicher.</span><span class="sxs-lookup"><span data-stu-id="ae8d6-136">Remove a substorage.</span></span> <span data-ttu-id="ae8d6-137">Auf dieses Optionsflag muss der Name des zu entfernenden subspeichers folgen.</span><span class="sxs-lookup"><span data-stu-id="ae8d6-137">This option flag must be followed by the name of the substorage to be removed.</span></span> |



 

<span data-ttu-id="ae8d6-138">Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="ae8d6-138">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="ae8d6-139">Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ae8d6-139">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="ae8d6-140">Beachten Sie, dass [ein Beispiel für eine Lokalisierung](a-localization-example.md) die [Einbettung von Anpassungs Transformationen als unter Speicher](embedding-customization-transforms-as-substorage.md)veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="ae8d6-140">Note that [A Localization Example](a-localization-example.md) demonstrates [Embedding Customization Transforms as Substorage](embedding-customization-transforms-as-substorage.md).</span></span>

 

 



