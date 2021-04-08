---
description: ICE25 überprüft, ob eine MSI-Datei alle internen Zusammenschluss-Modul Abhängigkeiten und-Ausschlüsse erfüllt.
ms.assetid: e6e3ea44-a1d4-451a-b326-e8fb7ed4adeb
title: ICE25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d966c4c374d6e61e30b44a41ad88bed8bf907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866295"
---
# <a name="ice25"></a><span data-ttu-id="4dc9c-103">ICE25</span><span class="sxs-lookup"><span data-stu-id="4dc9c-103">ICE25</span></span>

<span data-ttu-id="4dc9c-104">ICE25 überprüft, ob eine MSI-Datei alle internen [Zusammenschluss-Modul](merge-modules.md) Abhängigkeiten und-Ausschlüsse erfüllt.</span><span class="sxs-lookup"><span data-stu-id="4dc9c-104">ICE25 validates that a .msi file satisfies all of its internal [merge module](merge-modules.md) dependencies and exclusions.</span></span> <span data-ttu-id="4dc9c-105">Ice überprüft Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4dc9c-105">ICE validates the following:</span></span>

-   <span data-ttu-id="4dc9c-106">Alle mergemodulabhängigkeiten, die in der [Tabelle "moduledependen"](moduledependency-table.md) der MSI-Datei angegeben sind, werden von mindestens einem in der [Tabelle "ModuleSignature](modulesignature-table.md)" aufgelisteten Mergemodul erfüllt.</span><span class="sxs-lookup"><span data-stu-id="4dc9c-106">That all merge module dependencies indicated in the .msi file's [ModuleDependency table](moduledependency-table.md) are satisfied by at least one merge module listed in the [ModuleSignature table](modulesignature-table.md).</span></span>
-   <span data-ttu-id="4dc9c-107">Keines der ausgeschlossenen Mergemodule in der [Tabelle "moduleausschluss](moduleexclusion-table.md) " ist mit den in der Tabelle " [ModuleSignature](modulesignature-table.md)" aufgelisteten Mergemodulen nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="4dc9c-107">That none of the excluded merge modules in the [ModuleExclusion table](moduleexclusion-table.md) are incompatible with the merge modules listed in the [ModuleSignature table](modulesignature-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="4dc9c-108">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="4dc9c-108">Result</span></span>

<span data-ttu-id="4dc9c-109">ICE25 gibt eine Fehlermeldung aus, wenn die MSI-Datei bereits mit einem inkompatiblen Mergemodul zusammengeführt wurde, oder wenn Sie nicht mit einem erforderlichen Mergemodul zusammengeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="4dc9c-109">ICE25 posts an error message if .msi file has previously been merged with an incompatible merge module or if it has not been merged with a necessary merge module.</span></span>

## <a name="example"></a><span data-ttu-id="4dc9c-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4dc9c-110">Example</span></span>

<span data-ttu-id="4dc9c-111">ICE25 veröffentlicht die folgenden Fehler für das gezeigte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="4dc9c-111">ICE25 posts the following errors for the example shown.</span></span>

``` syntax
Dependency failure: Need ModuleX@0 v2.0 
Module ModuleB@1033 v1.0 is excluded.
```

[<span data-ttu-id="4dc9c-112">ModuleSignature-Tabelle</span><span class="sxs-lookup"><span data-stu-id="4dc9c-112">ModuleSignature Table</span></span>](modulesignature-table.md)



| <span data-ttu-id="4dc9c-113">ModuleID</span><span class="sxs-lookup"><span data-stu-id="4dc9c-113">ModuleID</span></span> | <span data-ttu-id="4dc9c-114">Sprache</span><span class="sxs-lookup"><span data-stu-id="4dc9c-114">Language</span></span> | <span data-ttu-id="4dc9c-115">Version</span><span class="sxs-lookup"><span data-stu-id="4dc9c-115">Version</span></span> |
|----------|----------|---------|
| <span data-ttu-id="4dc9c-116">Modulea</span><span class="sxs-lookup"><span data-stu-id="4dc9c-116">ModuleA</span></span>  | <span data-ttu-id="4dc9c-117">0</span><span class="sxs-lookup"><span data-stu-id="4dc9c-117">0</span></span>        | <span data-ttu-id="4dc9c-118">1.0</span><span class="sxs-lookup"><span data-stu-id="4dc9c-118">1.0</span></span>     |
| <span data-ttu-id="4dc9c-119">Moduleb</span><span class="sxs-lookup"><span data-stu-id="4dc9c-119">ModuleB</span></span>  | <span data-ttu-id="4dc9c-120">1033</span><span class="sxs-lookup"><span data-stu-id="4dc9c-120">1033</span></span>     | <span data-ttu-id="4dc9c-121">1.0</span><span class="sxs-lookup"><span data-stu-id="4dc9c-121">1.0</span></span>     |



 

[<span data-ttu-id="4dc9c-122">Moduledepenptabelle</span><span class="sxs-lookup"><span data-stu-id="4dc9c-122">ModuleDependency Table</span></span>](moduledependency-table.md)



| <span data-ttu-id="4dc9c-123">ModuleID</span><span class="sxs-lookup"><span data-stu-id="4dc9c-123">ModuleID</span></span> | <span data-ttu-id="4dc9c-124">Modulelanguage</span><span class="sxs-lookup"><span data-stu-id="4dc9c-124">ModuleLanguage</span></span> | <span data-ttu-id="4dc9c-125">Requirements did</span><span class="sxs-lookup"><span data-stu-id="4dc9c-125">RequiredID</span></span> | <span data-ttu-id="4dc9c-126">Requirements-Sprache</span><span class="sxs-lookup"><span data-stu-id="4dc9c-126">RequiredLanguage</span></span> | <span data-ttu-id="4dc9c-127">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="4dc9c-127">RequiredVersion</span></span> |
|----------|----------------|------------|------------------|-----------------|
| <span data-ttu-id="4dc9c-128">Modulea</span><span class="sxs-lookup"><span data-stu-id="4dc9c-128">ModuleA</span></span>  | <span data-ttu-id="4dc9c-129">0</span><span class="sxs-lookup"><span data-stu-id="4dc9c-129">0</span></span>              | <span data-ttu-id="4dc9c-130">Modulex</span><span class="sxs-lookup"><span data-stu-id="4dc9c-130">ModuleX</span></span>    | <span data-ttu-id="4dc9c-131">0</span><span class="sxs-lookup"><span data-stu-id="4dc9c-131">0</span></span>                | <span data-ttu-id="4dc9c-132">2.0</span><span class="sxs-lookup"><span data-stu-id="4dc9c-132">2.0</span></span>             |



 

[<span data-ttu-id="4dc9c-133">Moduleausschluss-Tabelle</span><span class="sxs-lookup"><span data-stu-id="4dc9c-133">ModuleExclusion Table</span></span>](moduleexclusion-table.md)



| <span data-ttu-id="4dc9c-134">ModuleID</span><span class="sxs-lookup"><span data-stu-id="4dc9c-134">ModuleID</span></span> | <span data-ttu-id="4dc9c-135">Modulelanguage</span><span class="sxs-lookup"><span data-stu-id="4dc9c-135">ModuleLanguage</span></span> | <span data-ttu-id="4dc9c-136">Excludädid</span><span class="sxs-lookup"><span data-stu-id="4dc9c-136">ExcludedID</span></span> | <span data-ttu-id="4dc9c-137">Excludecodlanguage</span><span class="sxs-lookup"><span data-stu-id="4dc9c-137">ExcludedLanguage</span></span> | <span data-ttu-id="4dc9c-138">Excludedminversion</span><span class="sxs-lookup"><span data-stu-id="4dc9c-138">ExcludedMinVersion</span></span> | <span data-ttu-id="4dc9c-139">Excludedmaxversion</span><span class="sxs-lookup"><span data-stu-id="4dc9c-139">ExcludedMaxVersion</span></span> |
|----------|----------------|------------|------------------|--------------------|--------------------|
| <span data-ttu-id="4dc9c-140">Modulea</span><span class="sxs-lookup"><span data-stu-id="4dc9c-140">ModuleA</span></span>  | <span data-ttu-id="4dc9c-141">0</span><span class="sxs-lookup"><span data-stu-id="4dc9c-141">0</span></span>              | <span data-ttu-id="4dc9c-142">Moduleb</span><span class="sxs-lookup"><span data-stu-id="4dc9c-142">ModuleB</span></span>    | <span data-ttu-id="4dc9c-143">1033</span><span class="sxs-lookup"><span data-stu-id="4dc9c-143">1033</span></span>             |                    |                    |



 

## <a name="related-topics"></a><span data-ttu-id="4dc9c-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4dc9c-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dc9c-145">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="4dc9c-145">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



