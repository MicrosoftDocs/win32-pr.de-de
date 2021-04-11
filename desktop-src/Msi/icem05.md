---
description: ICEM05 überprüft, ob das Mergemodul den Komponenten im Modul ordnungsgemäß zugeordnet ist. Eine fehlerhafte Zuordnung einer Komponente zu einem Modul bewirkt, dass die Komponente fälschlicherweise der Zieldatenbank zugeordnet wird.
ms.assetid: 1bf4041e-b198-4897-8719-8505fd8180ec
title: ICEM05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e62ca481ef836c2675c381817fe2242e37384818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042148"
---
# <a name="icem05"></a><span data-ttu-id="d539a-104">ICEM05</span><span class="sxs-lookup"><span data-stu-id="d539a-104">ICEM05</span></span>

<span data-ttu-id="d539a-105">ICEM05 überprüft, ob das Mergemodul den Komponenten im Modul ordnungsgemäß zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d539a-105">ICEM05 verifies that the merge module is correctly associated with components in the module.</span></span> <span data-ttu-id="d539a-106">Eine fehlerhafte Zuordnung einer Komponente zu einem Modul bewirkt, dass die Komponente fälschlicherweise der Zieldatenbank zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="d539a-106">Incorrectly associating a component with a module causes the component to be incorrectly associated with the target database.</span></span>

<span data-ttu-id="d539a-107">Das Mergemodul "ICES" wird in der Datei "Merge Module. Cub" mit dem Namen "Mergemod. Cub" und nicht in der CUB-Datei gespeichert, die die für die Paketüberprüfung verwendeten Verb</span><span class="sxs-lookup"><span data-stu-id="d539a-107">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="d539a-108">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="d539a-108">Result</span></span>

<span data-ttu-id="d539a-109">ICEM05 gibt einen Fehler aus, wenn die Modul Datenbank Komponenten und das Modul fälschlicherweise zuordnet.</span><span class="sxs-lookup"><span data-stu-id="d539a-109">ICEM05 posts an error if the module database incorrectly associates components and the module.</span></span>

## <a name="example"></a><span data-ttu-id="d539a-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d539a-110">Example</span></span>

<span data-ttu-id="d539a-111">ICEM05 gibt die folgenden Fehlermeldungen für ein Modul mit den unten gezeigten Datenbankeinträgen aus.</span><span class="sxs-lookup"><span data-stu-id="d539a-111">ICEM05 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The component Component2.OtherModule.GUID2.1033 in the 
ModuleComponents table does not belong to this Merge Module.
The component Component1.MyModule.GUID1.1033 in the ModuleComponents 
table is not listed in the Component table.
The component 'Component3' in the Component table is not listed in the 
ModuleComponents table.
```

[<span data-ttu-id="d539a-112">ModuleSignature-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d539a-112">ModuleSignature Table</span></span>](modulesignature-table.md)



| <span data-ttu-id="d539a-113">ModuleID</span><span class="sxs-lookup"><span data-stu-id="d539a-113">ModuleID</span></span>         | <span data-ttu-id="d539a-114">Sprache</span><span class="sxs-lookup"><span data-stu-id="d539a-114">Language</span></span> | <span data-ttu-id="d539a-115">Version</span><span class="sxs-lookup"><span data-stu-id="d539a-115">Version</span></span> |
|------------------|----------|---------|
| <span data-ttu-id="d539a-116">MyModule. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="d539a-116">MyModule.*GUID1*</span></span> | <span data-ttu-id="d539a-117">1033</span><span class="sxs-lookup"><span data-stu-id="d539a-117">1033</span></span>     | <span data-ttu-id="d539a-118">1.0</span><span class="sxs-lookup"><span data-stu-id="d539a-118">1.0</span></span>     |



 

[<span data-ttu-id="d539a-119">**Modulecomponents-Tabelle**</span><span class="sxs-lookup"><span data-stu-id="d539a-119">**ModuleComponents Table**</span></span>](modulecomponents-table.md)



| <span data-ttu-id="d539a-120">Komponente</span><span class="sxs-lookup"><span data-stu-id="d539a-120">Component</span></span>  | <span data-ttu-id="d539a-121">ModuleID</span><span class="sxs-lookup"><span data-stu-id="d539a-121">ModuleID</span></span>            | <span data-ttu-id="d539a-122">Sprache</span><span class="sxs-lookup"><span data-stu-id="d539a-122">Language</span></span> |
|------------|---------------------|----------|
| <span data-ttu-id="d539a-123">Component1</span><span class="sxs-lookup"><span data-stu-id="d539a-123">Component1</span></span> | <span data-ttu-id="d539a-124">MyModule. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="d539a-124">MyModule.*GUID1*</span></span>    | <span data-ttu-id="d539a-125">1033</span><span class="sxs-lookup"><span data-stu-id="d539a-125">1033</span></span>     |
| <span data-ttu-id="d539a-126">Component2</span><span class="sxs-lookup"><span data-stu-id="d539a-126">Component2</span></span> | <span data-ttu-id="d539a-127">Othermodule. *GUID2*</span><span class="sxs-lookup"><span data-stu-id="d539a-127">OtherModule.*GUID2*</span></span> | <span data-ttu-id="d539a-128">1033</span><span class="sxs-lookup"><span data-stu-id="d539a-128">1033</span></span>     |



 

<span data-ttu-id="d539a-129">[Komponenten Tabelle](component-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="d539a-129">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="d539a-130">Komponente</span><span class="sxs-lookup"><span data-stu-id="d539a-130">Component</span></span>  | <span data-ttu-id="d539a-131">ComponentID</span><span class="sxs-lookup"><span data-stu-id="d539a-131">ComponentID</span></span> |
|------------|-------------|
| <span data-ttu-id="d539a-132">Component3</span><span class="sxs-lookup"><span data-stu-id="d539a-132">Component3</span></span> | <span data-ttu-id="d539a-133">*GUID4*</span><span class="sxs-lookup"><span data-stu-id="d539a-133">*GUID4*</span></span>     |
| <span data-ttu-id="d539a-134">Component2</span><span class="sxs-lookup"><span data-stu-id="d539a-134">Component2</span></span> | <span data-ttu-id="d539a-135">*GUID5*</span><span class="sxs-lookup"><span data-stu-id="d539a-135">*GUID5*</span></span>     |



 

<span data-ttu-id="d539a-136">Das Modul "Mergemodul" meldet den ersten Fehler, weil die modulecomponents-Tabelle versucht, eine Komponente einem anderen Modul zuzuordnen, das nicht das aktuelle Modul ist, das in der Tabelle "ModuleSignature" angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d539a-136">The merge module ICE reports the first error because the ModuleComponents table attempts to associate a component with another module that is not the current module specified in the ModuleSignature table.</span></span> <span data-ttu-id="d539a-137">Um dieses Problem zu beheben, ändern Sie die Spalten ModuleID und Sprache des Datensatzes modulecomponents für Component2 in den Wert für das aktuelle Modul MyModule. *Guid1*.</span><span class="sxs-lookup"><span data-stu-id="d539a-137">To fix this, change the ModuleID and Language columns of the ModuleComponents record for Component2 to that for the current module, MyModule.*GUID1*.</span></span>

<span data-ttu-id="d539a-138">Das Modul "Mergemodul" gibt den zweiten Fehler an, da der erste Datensatz in der Tabelle "modulecomponents" versucht, dem Modul Component1 zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="d539a-138">The merge module ICE reports the second error because the first record in the ModuleComponents table attempts to associate Component1 with the module.</span></span> <span data-ttu-id="d539a-139">Diese Komponente ist nicht in der Komponenten Tabelle des Mergemoduls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d539a-139">This component does not exist in the Component Table of the merge module.</span></span> <span data-ttu-id="d539a-140">Ein Modul kann nur mit einer Komponente verknüpft werden, die im Modul vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d539a-140">A module can only be associated with a component that exists in the module.</span></span> <span data-ttu-id="d539a-141">Um dieses Problem zu beheben, entfernen Sie den Datensatz für die nicht vorhandene Komponente.</span><span class="sxs-lookup"><span data-stu-id="d539a-141">To fix this, remove the record for the non-existent component.</span></span>

<span data-ttu-id="d539a-142">Das Modul "Mergemodul" meldet den dritten Fehler, da das Modul versucht, der Zieldatenbank Component3 hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d539a-142">The merge module ICE reports the third error because the module attempts to add Component3 to the target database.</span></span> <span data-ttu-id="d539a-143">Diese Komponente wurde dem Modul in der Tabelle "modulecomponents" nicht zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d539a-143">This component has not been associated with the module in the ModuleComponents table.</span></span> <span data-ttu-id="d539a-144">Fügen Sie der Tabelle modulecomponents einen Datensatz für Component3 hinzu, um diesen Fehler zu beheben.</span><span class="sxs-lookup"><span data-stu-id="d539a-144">To fix this error, add a record for Component3 to the ModuleComponents table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d539a-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d539a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d539a-146">Eisverweis für Mergemodul</span><span class="sxs-lookup"><span data-stu-id="d539a-146">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



