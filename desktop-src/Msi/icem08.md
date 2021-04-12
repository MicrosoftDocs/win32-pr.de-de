---
description: ICEM08 stellt sicher, dass ein Modul kein anderes Modul ausschließt, von dem es abhängt.
ms.assetid: 56d115b4-7410-4db2-a9af-bc6716f3358d
title: ICEM08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9767c6748f5a21d83bddb3b5fe93a0a8d7ea67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216943"
---
# <a name="icem08"></a><span data-ttu-id="7ed5a-103">ICEM08</span><span class="sxs-lookup"><span data-stu-id="7ed5a-103">ICEM08</span></span>

<span data-ttu-id="7ed5a-104">ICEM08 stellt sicher, dass ein Modul kein anderes Modul ausschließt, von dem es abhängt.</span><span class="sxs-lookup"><span data-stu-id="7ed5a-104">ICEM08 ensures that a module does not exclude another module that it depends on.</span></span>

## <a name="result"></a><span data-ttu-id="7ed5a-105">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="7ed5a-105">Result</span></span>

<span data-ttu-id="7ed5a-106">ICEM08 gibt einen Fehler aus, wenn ein Modul ein anderes Modul ausschließt, von dem es abhängt.</span><span class="sxs-lookup"><span data-stu-id="7ed5a-106">ICEM08 posts an error when a module excludes another module that it depends on.</span></span>

## <a name="example"></a><span data-ttu-id="7ed5a-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7ed5a-107">Example</span></span>

<span data-ttu-id="7ed5a-108">ICEM08 gibt die folgende Fehlermeldung für ein Modul mit den Datenbankeinträgen aus, die im Beispiel angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7ed5a-108">ICEM08 posts the following error message for a module containing the database entries shown in the example.</span></span>

``` syntax
Error: This module requires module ModuleB.<GUID> (1033v1.0) but also 
lists it as an exclusion.
```

[<span data-ttu-id="7ed5a-109">Moduledepenptabelle</span><span class="sxs-lookup"><span data-stu-id="7ed5a-109">ModuleDependency Table</span></span>](moduledependency-table.md)



| <span data-ttu-id="7ed5a-110">ModuleID</span><span class="sxs-lookup"><span data-stu-id="7ed5a-110">ModuleID</span></span>             | <span data-ttu-id="7ed5a-111">Modulelanguage</span><span class="sxs-lookup"><span data-stu-id="7ed5a-111">ModuleLanguage</span></span> | <span data-ttu-id="7ed5a-112">Requirements did</span><span class="sxs-lookup"><span data-stu-id="7ed5a-112">RequiredID</span></span>           | <span data-ttu-id="7ed5a-113">Requirements-Sprache</span><span class="sxs-lookup"><span data-stu-id="7ed5a-113">RequiredLanguage</span></span> | <span data-ttu-id="7ed5a-114">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="7ed5a-114">RequiredVersion</span></span> |
|----------------------|----------------|----------------------|------------------|-----------------|
| <span data-ttu-id="7ed5a-115">Modulea.<GUID></span><span class="sxs-lookup"><span data-stu-id="7ed5a-115">ModuleA.<GUID></span></span> | <span data-ttu-id="7ed5a-116">1033</span><span class="sxs-lookup"><span data-stu-id="7ed5a-116">1033</span></span>           | <span data-ttu-id="7ed5a-117">Moduleb.<GUID></span><span class="sxs-lookup"><span data-stu-id="7ed5a-117">ModuleB.<GUID></span></span> | <span data-ttu-id="7ed5a-118">1033</span><span class="sxs-lookup"><span data-stu-id="7ed5a-118">1033</span></span>             | <span data-ttu-id="7ed5a-119">1.0</span><span class="sxs-lookup"><span data-stu-id="7ed5a-119">1.0</span></span>             |



 

[<span data-ttu-id="7ed5a-120">Moduleausschluss-Tabelle</span><span class="sxs-lookup"><span data-stu-id="7ed5a-120">ModuleExclusion Table</span></span>](moduleexclusion-table.md)



| <span data-ttu-id="7ed5a-121">ModuleID</span><span class="sxs-lookup"><span data-stu-id="7ed5a-121">ModuleID</span></span>             | <span data-ttu-id="7ed5a-122">Modulelanguage</span><span class="sxs-lookup"><span data-stu-id="7ed5a-122">ModuleLanguage</span></span> | <span data-ttu-id="7ed5a-123">Excludädid</span><span class="sxs-lookup"><span data-stu-id="7ed5a-123">ExcludedID</span></span>           | <span data-ttu-id="7ed5a-124">Excludecodlanguage</span><span class="sxs-lookup"><span data-stu-id="7ed5a-124">ExcludedLanguage</span></span> | <span data-ttu-id="7ed5a-125">Excludedminversion</span><span class="sxs-lookup"><span data-stu-id="7ed5a-125">ExcludedMinVersion</span></span> | <span data-ttu-id="7ed5a-126">Excludedmaxversion</span><span class="sxs-lookup"><span data-stu-id="7ed5a-126">ExcludedMaxVersion</span></span> |
|----------------------|----------------|----------------------|------------------|--------------------|--------------------|
| <span data-ttu-id="7ed5a-127">Modulea.<GUID></span><span class="sxs-lookup"><span data-stu-id="7ed5a-127">ModuleA.<GUID></span></span> | <span data-ttu-id="7ed5a-128">1033</span><span class="sxs-lookup"><span data-stu-id="7ed5a-128">1033</span></span>           | <span data-ttu-id="7ed5a-129">Moduleb.<GUID></span><span class="sxs-lookup"><span data-stu-id="7ed5a-129">ModuleB.<GUID></span></span> | <span data-ttu-id="7ed5a-130">1033</span><span class="sxs-lookup"><span data-stu-id="7ed5a-130">1033</span></span>             |                    | <span data-ttu-id="7ed5a-131">1.0</span><span class="sxs-lookup"><span data-stu-id="7ed5a-131">1.0</span></span>                |



 

<span data-ttu-id="7ed5a-132">Um den Fehler zu beheben, entfernen Sie entweder die Abhängigkeit oder den Ausschluss.</span><span class="sxs-lookup"><span data-stu-id="7ed5a-132">To fix the error, remove either the dependency or the exclusion.</span></span> <span data-ttu-id="7ed5a-133">Wenn moduleb eine Abhängigkeit (Requirements did) von modulea ist, können Sie es nicht ausschließen (wie in der Spalte exluentdid der Tabelle moduleausschluss dargestellt).</span><span class="sxs-lookup"><span data-stu-id="7ed5a-133">If ModuleB is a dependency (RequiredID) of ModuleA, you cannot exclude it (as shown in the ExludedID column of the ModuleExclusion table).</span></span> <span data-ttu-id="7ed5a-134">Wenn Sie moduleb ausschließen müssen, müssen Sie die Abhängigkeit von modulea darauf entfernen.</span><span class="sxs-lookup"><span data-stu-id="7ed5a-134">If you must exclude ModuleB, then you must remove ModuleA's dependency on it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ed5a-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7ed5a-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ed5a-136">Eisverweis für Mergemodul</span><span class="sxs-lookup"><span data-stu-id="7ed5a-136">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



