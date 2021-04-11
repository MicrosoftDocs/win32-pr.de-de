---
description: ICEM12 überprüft, ob in einer modulesequence-Tabelle Standard Aktionen Sequenznummern aufweisen und benutzerdefinierte Aktionen baseaction-und After-Werte aufweisen.
ms.assetid: 1a168629-9865-4412-8317-8af8b9a7b8bd
title: ICEM12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37cbff2e29a85dd50ef1f044a43fdb8e48ffdd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041870"
---
# <a name="icem12"></a><span data-ttu-id="4a045-103">ICEM12</span><span class="sxs-lookup"><span data-stu-id="4a045-103">ICEM12</span></span>

<span data-ttu-id="4a045-104">ICEM12 überprüft, ob in einer modulesequence-Tabelle Standard Aktionen Sequenznummern aufweisen und benutzerdefinierte Aktionen baseaction-und After-Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4a045-104">ICEM12 verifies that in a ModuleSequence table, standard actions have sequence numbers and custom actions have BaseAction and After values.</span></span>

<span data-ttu-id="4a045-105">Dieses ICEM ist in der Datei "Mergemod. Cub" verfügbar, die im SDK für Windows Installer 2,0 und höher bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4a045-105">This ICEM is available in the Mergemod.cub file provided in the Windows Installer 2.0 SDK and later.</span></span> <span data-ttu-id="4a045-106">Weitere Informationen finden Sie unter [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="4a045-106">For details, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="result"></a><span data-ttu-id="4a045-107">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="4a045-107">Result</span></span>

<span data-ttu-id="4a045-108">ICEM12 gibt einen Fehler in den folgenden Fällen aus:</span><span class="sxs-lookup"><span data-stu-id="4a045-108">ICEM12 posts an error in the following cases:</span></span>

-   <span data-ttu-id="4a045-109">Es findet fest, dass das Modul eine [Standardaktion](standard-actions.md) ohne Sequenznummer enthält.</span><span class="sxs-lookup"><span data-stu-id="4a045-109">It finds the module contains a [standard action](standard-actions.md) without a sequence number.</span></span>
-   <span data-ttu-id="4a045-110">Es wird festgelegt, dass für eine Standardaktion Werte in den baseaction-oder After-Feldern der [moduleadminuisequence-Tabelle](moduleadminuisequence-table.md), [moduleadminexecutesequence-Tabelle](moduleadminexecutesequence-table.md), [moduleadvtexecutesequence](moduleadvtexecutesequence-table.md)-Tabelle, [moduleinstalluisequence](moduleinstalluisequence-table.md)-Tabelle oder [moduleinstallexecutesequence](moduleinstallexecutesequence-table.md)-Tabelle eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4a045-110">It finds that a standard action has values entered in the BaseAction or After fields of the [ModuleAdminUISequence table](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence table](moduleadminexecutesequence-table.md), [ModuleAdvtExecuteSequence table](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence table](moduleinstalluisequence-table.md), or [ModuleInstallExecuteSequence table](moduleinstallexecutesequence-table.md).</span></span>
-   <span data-ttu-id="4a045-111">Es findet das Modul, das eine [benutzerdefinierte Aktion](custom-actions.md) enthält, ohne dass Werte in die Reihenfolge, baseaction oder After-Felder der [moduleadminuisequence-Tabelle](moduleadminuisequence-table.md), [moduleadminexecutesequence](moduleadminexecutesequence-table.md)-Tabelle, [moduleadvtexecutesequence](moduleadvtexecutesequence-table.md)-Tabelle, [moduleinstalluisequence](moduleinstalluisequence-table.md)-Tabelle oder [moduleinstallexecutesequence](moduleinstallexecutesequence-table.md)-Tabelle</span><span class="sxs-lookup"><span data-stu-id="4a045-111">It finds the module contains a [custom action](custom-actions.md) without any values entered into the Sequence, BaseAction or After fields of the [ModuleAdminUISequence table](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence table](moduleadminexecutesequence-table.md), [ModuleAdvtExecuteSequence table](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence table](moduleinstalluisequence-table.md), or [ModuleInstallExecuteSequence table](moduleinstallexecutesequence-table.md).</span></span>

<span data-ttu-id="4a045-112">ICEM12 gibt eine Warnung aus, wenn eine benutzerdefinierte Aktion gefunden wird, für die eine Sequenznummer angegeben ist, in den Feldern baseaction oder After jedoch kein Wert.</span><span class="sxs-lookup"><span data-stu-id="4a045-112">ICEM12 posts a warning if it finds a custom action that has a Sequence number specified, but no value in the BaseAction or After fields.</span></span>

<span data-ttu-id="4a045-113">Beachten Sie, dass alle in der [Tabelle CustomAction](customaction-table.md) gefundenen Aktionen als benutzerdefinierte Aktionen angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="4a045-113">Note that all actions found in the [CustomAction table](customaction-table.md) are considered custom actions.</span></span> <span data-ttu-id="4a045-114">Alle anderen Aktionen werden als Standard Aktionen behandelt.</span><span class="sxs-lookup"><span data-stu-id="4a045-114">All other action are considered standard actions.</span></span>

## <a name="example"></a><span data-ttu-id="4a045-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4a045-115">Example</span></span>

<span data-ttu-id="4a045-116">ICEM12 veröffentlicht die folgenden Fehler-und Warnmeldungen für ein Modul, das die unten gezeigten Datenbankeinträge enthält:</span><span class="sxs-lookup"><span data-stu-id="4a045-116">ICEM12 posts the following error and warning messages for a module that contains the database entries shown below:</span></span>

``` syntax
Error. Custom actions should use the BaseAction and After fields and not use the 
Sequence field in the Module Sequence tables. The custom action 'Action1' uses the Sequence field 
and does not use the BaseAction and After fields in the ModuleInstallExecuteSequence table. 
    
Error. Custom actions should not leave the Sequence, BaseAction, and After fields 
of the Module Sequence tables all empty. The custom action 'Action3' leaves the Sequence, 
BaseAction, and After fields empty in the ModuleAdminExecuteSequence table.

Error. Standard actions should not use the BaseAction and After fields in Module 
Sequence tables. The standard action 'Action2' has a values entered in the BaseAction 
or After fields of the ModuleAdminExecuteSequence table.

Error. Standard actions must have a entry in the Sequence field of Module Sequence 
tables. The standard action 'Action2' does not have a Sequence value in the 
ModuleExecuteSequence table.
```

[<span data-ttu-id="4a045-117">CustomAction</span><span class="sxs-lookup"><span data-stu-id="4a045-117">CustomAction</span></span>](customaction-table.md)



| <span data-ttu-id="4a045-118">Aktion</span><span class="sxs-lookup"><span data-stu-id="4a045-118">Action</span></span>  | <span data-ttu-id="4a045-119">type</span><span class="sxs-lookup"><span data-stu-id="4a045-119">Type</span></span> | <span data-ttu-id="4a045-120">`Source`</span><span class="sxs-lookup"><span data-stu-id="4a045-120">Source</span></span>  | <span data-ttu-id="4a045-121">Ziel</span><span class="sxs-lookup"><span data-stu-id="4a045-121">Target</span></span>  |
|---------|------|---------|---------|
| <span data-ttu-id="4a045-122">Action1</span><span class="sxs-lookup"><span data-stu-id="4a045-122">Action1</span></span> | <span data-ttu-id="4a045-123">30</span><span class="sxs-lookup"><span data-stu-id="4a045-123">30</span></span>   | <span data-ttu-id="4a045-124">Quelle1</span><span class="sxs-lookup"><span data-stu-id="4a045-124">source1</span></span> | <span data-ttu-id="4a045-125">target1</span><span class="sxs-lookup"><span data-stu-id="4a045-125">target1</span></span> |
| <span data-ttu-id="4a045-126">Action3</span><span class="sxs-lookup"><span data-stu-id="4a045-126">Action3</span></span> | <span data-ttu-id="4a045-127">30</span><span class="sxs-lookup"><span data-stu-id="4a045-127">30</span></span>   | <span data-ttu-id="4a045-128">source3</span><span class="sxs-lookup"><span data-stu-id="4a045-128">source3</span></span> | <span data-ttu-id="4a045-129">target3</span><span class="sxs-lookup"><span data-stu-id="4a045-129">target3</span></span> |



 

[<span data-ttu-id="4a045-130">Moduleadminexecutesequence</span><span class="sxs-lookup"><span data-stu-id="4a045-130">ModuleAdminExecuteSequence</span></span>](moduleadminexecutesequence-table.md)



| <span data-ttu-id="4a045-131">Aktion</span><span class="sxs-lookup"><span data-stu-id="4a045-131">Action</span></span>  | <span data-ttu-id="4a045-132">Sequenz</span><span class="sxs-lookup"><span data-stu-id="4a045-132">Sequence</span></span> | <span data-ttu-id="4a045-133">Baseaction</span><span class="sxs-lookup"><span data-stu-id="4a045-133">BaseAction</span></span> | <span data-ttu-id="4a045-134">Nach</span><span class="sxs-lookup"><span data-stu-id="4a045-134">After</span></span> | <span data-ttu-id="4a045-135">Bedingung</span><span class="sxs-lookup"><span data-stu-id="4a045-135">Condition</span></span> |
|---------|----------|------------|-------|-----------|
| <span data-ttu-id="4a045-136">Action2</span><span class="sxs-lookup"><span data-stu-id="4a045-136">Action2</span></span> |          | <span data-ttu-id="4a045-137">Action1</span><span class="sxs-lookup"><span data-stu-id="4a045-137">Action1</span></span>    | <span data-ttu-id="4a045-138">1</span><span class="sxs-lookup"><span data-stu-id="4a045-138">1</span></span>     | <span data-ttu-id="4a045-139">true</span><span class="sxs-lookup"><span data-stu-id="4a045-139">true</span></span>      |
| <span data-ttu-id="4a045-140">Action3</span><span class="sxs-lookup"><span data-stu-id="4a045-140">Action3</span></span> |          |            |       | <span data-ttu-id="4a045-141">true</span><span class="sxs-lookup"><span data-stu-id="4a045-141">true</span></span>      |



 

[<span data-ttu-id="4a045-142">Moduleinstallexecutesequence</span><span class="sxs-lookup"><span data-stu-id="4a045-142">ModuleInstallExecuteSequence</span></span>](moduleinstallexecutesequence-table.md)



| <span data-ttu-id="4a045-143">Aktion</span><span class="sxs-lookup"><span data-stu-id="4a045-143">Action</span></span>  | <span data-ttu-id="4a045-144">Sequenz</span><span class="sxs-lookup"><span data-stu-id="4a045-144">Sequence</span></span> | <span data-ttu-id="4a045-145">Baseaction</span><span class="sxs-lookup"><span data-stu-id="4a045-145">BaseAction</span></span> | <span data-ttu-id="4a045-146">Nach</span><span class="sxs-lookup"><span data-stu-id="4a045-146">After</span></span> | <span data-ttu-id="4a045-147">Bedingung</span><span class="sxs-lookup"><span data-stu-id="4a045-147">Condition</span></span> |
|---------|----------|------------|-------|-----------|
| <span data-ttu-id="4a045-148">Action1</span><span class="sxs-lookup"><span data-stu-id="4a045-148">Action1</span></span> | <span data-ttu-id="4a045-149">1</span><span class="sxs-lookup"><span data-stu-id="4a045-149">1</span></span>        |            |       | <span data-ttu-id="4a045-150">true</span><span class="sxs-lookup"><span data-stu-id="4a045-150">true</span></span>      |



 

<span data-ttu-id="4a045-151">Versuchen Sie Folgendes, um diese Fehler zu beheben:</span><span class="sxs-lookup"><span data-stu-id="4a045-151">To fix these errors try the following:</span></span>

-   <span data-ttu-id="4a045-152">Entfernen Sie die Sequenznummer für die benutzerdefinierte Aktion Action1, und verwenden Sie stattdessen die Felder baseaction und After.</span><span class="sxs-lookup"><span data-stu-id="4a045-152">Remove the sequence number for the custom action Action1 and use the BaseAction and After fields instead.</span></span>
-   <span data-ttu-id="4a045-153">Geben Sie Werte in die Felder Sequence, baseaction oder After für die benutzerdefinierte Aktion Action3 ein.</span><span class="sxs-lookup"><span data-stu-id="4a045-153">Enter values into the Sequence, BaseAction, or After fields for the custom action Action3.</span></span> <span data-ttu-id="4a045-154">Lassen Sie die Felder baseaction und After für Standardaktion Action2 leer.</span><span class="sxs-lookup"><span data-stu-id="4a045-154">Leave the BaseAction and After fields empty for standard action Action2.</span></span>
-   <span data-ttu-id="4a045-155">Lassen Sie das Sequenz Feld für die Standardaktion Action2 nicht leer.</span><span class="sxs-lookup"><span data-stu-id="4a045-155">Do not leave the Sequence field empty for standard action Action2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a045-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4a045-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a045-157">Eisverweis für Mergemodul</span><span class="sxs-lookup"><span data-stu-id="4a045-157">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



