---
description: ICEM02 überprüft, ob alle Modul Abhängigkeiten und-Ausschlüsse mit dem aktuellen Modul verknüpft sind.
ms.assetid: c7d77cb6-0ee6-4857-a749-7908e1c5fcda
title: ICEM02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a976132dbfad42e95f4141bc00adb48a544c1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214954"
---
# <a name="icem02"></a><span data-ttu-id="7a680-103">ICEM02</span><span class="sxs-lookup"><span data-stu-id="7a680-103">ICEM02</span></span>

<span data-ttu-id="7a680-104">ICEM02 überprüft, ob alle Modul Abhängigkeiten und-Ausschlüsse mit dem aktuellen Modul verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="7a680-104">ICEM02 verifies that all the module dependencies and exclusions are related to the current module.</span></span>

<span data-ttu-id="7a680-105">Das Mergemodul "ICES" wird in der Datei "Merge Module. Cub" mit dem Namen "Mergemod. Cub" und nicht in der CUB-Datei gespeichert, die die für die Paketüberprüfung verwendeten Verb</span><span class="sxs-lookup"><span data-stu-id="7a680-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="7a680-106">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="7a680-106">Result</span></span>

<span data-ttu-id="7a680-107">ICEM02 sendet Fehlermeldungen, wenn die Modul Datenbank versucht, Abhängigkeiten oder Ausschlüsse anzugeben, die nicht mit dem aktuellen Modul in Beziehung stehen.</span><span class="sxs-lookup"><span data-stu-id="7a680-107">ICEM02 posts error messages if the module database attempts to specify dependencies or exclusions that do not relate to the current module.</span></span> <span data-ttu-id="7a680-108">ICEM02 gibt eine Fehlermeldung aus, wenn die Modul Datenbank versucht, das aktuelle Modul als abhängig oder als von sich selbst ausgeschlossen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7a680-108">ICEM02 posts an error message if the module database attempts to specify the current module as dependent or as excluded by itself.</span></span>

## <a name="example"></a><span data-ttu-id="7a680-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7a680-109">Example</span></span>

<span data-ttu-id="7a680-110">ICEM02 gibt die folgenden Fehlermeldungen für ein Modul mit den unten gezeigten Datenbankeinträgen aus.</span><span class="sxs-lookup"><span data-stu-id="7a680-110">ICEM02 would post the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The dependency OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleDependency table creates a dependency for an unrelated module. A 
module can only define dependencies for itself

This module is listed as depending on itself!

The exclusion OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleExclusion table creates an excluded module for an unrelated 
module. A module can only define exclusions for itself.

This module excludes itself from the target database!
```

[<span data-ttu-id="7a680-111">ModuleSignature-Tabelle</span><span class="sxs-lookup"><span data-stu-id="7a680-111">ModuleSignature Table</span></span>](modulesignature-table.md)



| <span data-ttu-id="7a680-112">ModuleID</span><span class="sxs-lookup"><span data-stu-id="7a680-112">ModuleID</span></span>         | <span data-ttu-id="7a680-113">Sprache</span><span class="sxs-lookup"><span data-stu-id="7a680-113">Language</span></span> | <span data-ttu-id="7a680-114">Version</span><span class="sxs-lookup"><span data-stu-id="7a680-114">Version</span></span> |
|------------------|----------|---------|
| <span data-ttu-id="7a680-115">MyModule. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="7a680-115">MyModule.*GUID1*</span></span> | <span data-ttu-id="7a680-116">1033</span><span class="sxs-lookup"><span data-stu-id="7a680-116">1033</span></span>     | <span data-ttu-id="7a680-117">1.0</span><span class="sxs-lookup"><span data-stu-id="7a680-117">1.0</span></span>     |



 

[<span data-ttu-id="7a680-118">Moduledepenptabelle</span><span class="sxs-lookup"><span data-stu-id="7a680-118">ModuleDependency Table</span></span>](moduledependency-table.md)



| <span data-ttu-id="7a680-119">ModuleID</span><span class="sxs-lookup"><span data-stu-id="7a680-119">ModuleID</span></span>            | <span data-ttu-id="7a680-120">Modulelanguage</span><span class="sxs-lookup"><span data-stu-id="7a680-120">ModuleLanguage</span></span> | <span data-ttu-id="7a680-121">Requirements did</span><span class="sxs-lookup"><span data-stu-id="7a680-121">RequiredID</span></span>          | <span data-ttu-id="7a680-122">Requirements-Sprache</span><span class="sxs-lookup"><span data-stu-id="7a680-122">RequiredLanguage</span></span> | <span data-ttu-id="7a680-123">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="7a680-123">RequiredVersion</span></span> |
|---------------------|----------------|---------------------|------------------|-----------------|
| <span data-ttu-id="7a680-124">Othermodule. *GUID2*</span><span class="sxs-lookup"><span data-stu-id="7a680-124">OtherModule.*GUID2*</span></span> | <span data-ttu-id="7a680-125">1033</span><span class="sxs-lookup"><span data-stu-id="7a680-125">1033</span></span>           | <span data-ttu-id="7a680-126">Othermodule. *GUID3*</span><span class="sxs-lookup"><span data-stu-id="7a680-126">OtherModule.*GUID3*</span></span> | <span data-ttu-id="7a680-127">0</span><span class="sxs-lookup"><span data-stu-id="7a680-127">0</span></span>                | <span data-ttu-id="7a680-128">1.0</span><span class="sxs-lookup"><span data-stu-id="7a680-128">1.0</span></span>             |
| <span data-ttu-id="7a680-129">MyModule. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="7a680-129">MyModule.*GUID1*</span></span>    | <span data-ttu-id="7a680-130">1033</span><span class="sxs-lookup"><span data-stu-id="7a680-130">1033</span></span>           | <span data-ttu-id="7a680-131">MyModule. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="7a680-131">MyModule.*GUID1*</span></span>    | <span data-ttu-id="7a680-132">1033</span><span class="sxs-lookup"><span data-stu-id="7a680-132">1033</span></span>             | <span data-ttu-id="7a680-133">1.2</span><span class="sxs-lookup"><span data-stu-id="7a680-133">1.2</span></span>             |



 

<span data-ttu-id="7a680-134">[Moduleausschluss-Tabelle](moduleexclusion-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="7a680-134">[ModuleExclusion Table](moduleexclusion-table.md) (partial)</span></span>



| <span data-ttu-id="7a680-135">ModuleID</span><span class="sxs-lookup"><span data-stu-id="7a680-135">ModuleID</span></span>            | <span data-ttu-id="7a680-136">Modulelanguage</span><span class="sxs-lookup"><span data-stu-id="7a680-136">ModuleLanguage</span></span> | <span data-ttu-id="7a680-137">Excludädid</span><span class="sxs-lookup"><span data-stu-id="7a680-137">ExcludedID</span></span>          | <span data-ttu-id="7a680-138">Excludecodlanguage</span><span class="sxs-lookup"><span data-stu-id="7a680-138">ExcludedLanguage</span></span> |
|---------------------|----------------|---------------------|------------------|
| <span data-ttu-id="7a680-139">Othermodule. *GUID2*</span><span class="sxs-lookup"><span data-stu-id="7a680-139">OtherModule.*GUID2*</span></span> | <span data-ttu-id="7a680-140">1033</span><span class="sxs-lookup"><span data-stu-id="7a680-140">1033</span></span>           | <span data-ttu-id="7a680-141">Othermodule. *GUID3*</span><span class="sxs-lookup"><span data-stu-id="7a680-141">OtherModule.*GUID3*</span></span> | <span data-ttu-id="7a680-142">0</span><span class="sxs-lookup"><span data-stu-id="7a680-142">0</span></span>                |
| <span data-ttu-id="7a680-143">MyModule. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="7a680-143">MyModule.*GUID1*</span></span>    | <span data-ttu-id="7a680-144">1033</span><span class="sxs-lookup"><span data-stu-id="7a680-144">1033</span></span>           | <span data-ttu-id="7a680-145">MyModule. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="7a680-145">MyModule.*GUID1*</span></span>    | <span data-ttu-id="7a680-146">1033</span><span class="sxs-lookup"><span data-stu-id="7a680-146">1033</span></span>             |



 

<span data-ttu-id="7a680-147">Das Mergemodul Ice postet den ersten Fehler, da der der ersten Zeile in der Tabelle "moduledepend", die keine erforderliche Abhängigkeit für das aktuelle Modul angibt, das in der Tabelle "ModuleSignature" angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7a680-147">The merge module ICE posts the first error because the of the first row in the ModuleDependency table, which does not specify a required dependency for the current module specified in the ModuleSignature table.</span></span> <span data-ttu-id="7a680-148">Die Abhängigkeiten eines Moduls können nur in einer eigenen moduledependen-Tabelle angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7a680-148">The dependencies of a module can only be specified in its own ModuleDependency table.</span></span> <span data-ttu-id="7a680-149">Wenn othermodule. *GUID3* ist für das aktuelle Modul erforderlich. ersetzen Sie die ersten beiden Spalten der Zeile durch die Daten aus der ModuleSignature-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7a680-149">If OtherModule.*GUID3* is required by the current module, replace the first two columns of the row with the data from the ModuleSignature table.</span></span> <span data-ttu-id="7a680-150">Wenn othermodule. *GUID3* ist für dieses Modul nicht erforderlich, löschen Sie diese Zeile.</span><span class="sxs-lookup"><span data-stu-id="7a680-150">If OtherModule.*GUID3* is not required by this module, delete this row.</span></span>

<span data-ttu-id="7a680-151">Das Mergemodul Ice postet den zweiten Fehler, da ein Modul keine Abhängigkeit von sich selbst angeben kann.</span><span class="sxs-lookup"><span data-stu-id="7a680-151">The merge module ICE posts the second error because a module cannot specify a dependency upon itself.</span></span>

<span data-ttu-id="7a680-152">Das Mergemodul Ice postet den dritten Fehler aufgrund der ersten Zeile in der Tabelle "moduleausschluss", die keinen erforderlichen Ausschluss für das aktuelle Modul angibt, das in der ModuleSignature-Tabelle angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7a680-152">The merge module ICE posts the third error because of the first row in the ModuleExclusion table, which does not specify a required exclusion for the current module specified in the ModuleSignature table.</span></span> <span data-ttu-id="7a680-153">Die Ausschlüsse eines Moduls können nur in einer eigenen moduleausschluss-Tabelle angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7a680-153">The exclusions of a module can only be specified in its own ModuleExclusion table.</span></span> <span data-ttu-id="7a680-154">, Wenn das aktuelle Modul othermodule ausschließt. *GUID3* ersetzen Sie die ersten beiden Spalten der Zeile durch die Daten aus der ModuleSignature-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7a680-154">If the current module excludes OtherModule.*GUID3*, replace the first two columns of the row with the data from the ModuleSignature table.</span></span> <span data-ttu-id="7a680-155">, Wenn das aktuelle Modul nicht othermodule ausschließt. *GUID3* löschen Sie diese Zeile.</span><span class="sxs-lookup"><span data-stu-id="7a680-155">If the current module does not exclude OtherModule.*GUID3*, delete this row.</span></span>

<span data-ttu-id="7a680-156">Das Mergemodul Ice postet den vierten Fehler, da ein Modul nicht angeben kann, dass es sich selbst ausschließt.</span><span class="sxs-lookup"><span data-stu-id="7a680-156">The merge module ICE posts the fourth error because a module cannot specify that it exclude itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a680-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7a680-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a680-158">Eisverweis für Mergemodul</span><span class="sxs-lookup"><span data-stu-id="7a680-158">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



