---
title: Allgemeine Ressourcen Attribute
description: Die für 16-Bit-Windows unterstützten Ressourcen Definitions Anweisungen enthalten eine Load-Load-Option, die das Lade-und Arbeitsspeicher Merkmal der Ressource angibt.
ms.assetid: 53740997-854b-447c-9ab1-de8e17c0de1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa15ae7207c80737e284151f0dfd3d7981935943
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338597"
---
# <a name="common-resource-attributes"></a><span data-ttu-id="72837-103">Allgemeine Ressourcen Attribute</span><span class="sxs-lookup"><span data-stu-id="72837-103">Common Resource Attributes</span></span>

<span data-ttu-id="72837-104">Die für 16-Bit-Windows unterstützten Ressourcen Definitions Anweisungen enthalten eine *Load-Load-* Option, die das Lade-und Arbeitsspeicher Merkmal der Ressource angibt.</span><span class="sxs-lookup"><span data-stu-id="72837-104">The resource-definition statements supported on 16-bit Windows include a *load-mem* option that specifies the loading and memory characteristics of the resource.</span></span> <span data-ttu-id="72837-105">Diese Attribute sind aus Gründen der Abwärtskompatibilität in Ressourcen Skripts zulässig, werden jedoch ignoriert.</span><span class="sxs-lookup"><span data-stu-id="72837-105">These attributes are permitted in resource scripts for backward compatibility, but they are ignored.</span></span> <span data-ttu-id="72837-106">Windows-Ressourcen werden geladen, wenn das entsprechende Modul geladen wird, und werden freigegeben, wenn das Modul entladen wird.</span><span class="sxs-lookup"><span data-stu-id="72837-106">Windows resources are loaded when the corresponding module is loaded, and are freed when the module is unloaded.</span></span>

## <a name="load-attributes"></a><span data-ttu-id="72837-107">Attribute laden</span><span class="sxs-lookup"><span data-stu-id="72837-107">Load Attributes</span></span>

<span data-ttu-id="72837-108">Die Load-Attribute geben an, wann die Ressource geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="72837-108">The load attributes specify when the resource is to be loaded.</span></span> <span data-ttu-id="72837-109">Der Load-Parameter muss eines der folgenden Attribute sein.</span><span class="sxs-lookup"><span data-stu-id="72837-109">The load parameter must be one of the following attributes.</span></span>



| <span data-ttu-id="72837-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="72837-110">Attribute</span></span>      | <span data-ttu-id="72837-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72837-111">Description</span></span>                                                                  |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="72837-112">**Vorab laden**</span><span class="sxs-lookup"><span data-stu-id="72837-112">**PRELOAD**</span></span>    | <span data-ttu-id="72837-113">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="72837-113">Ignored.</span></span> <span data-ttu-id="72837-114">In 16-Bit-Fenstern wird die Ressource mit der ausführbaren Datei geladen.</span><span class="sxs-lookup"><span data-stu-id="72837-114">In 16-bit Windows, the resource is loaded with the executable file.</span></span> |
| <span data-ttu-id="72837-115">**LOADONCALL**</span><span class="sxs-lookup"><span data-stu-id="72837-115">**LOADONCALL**</span></span> | <span data-ttu-id="72837-116">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="72837-116">Ignored.</span></span> <span data-ttu-id="72837-117">In 16-Bit-Fenstern wird die Ressource geladen, wenn Sie aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="72837-117">In 16-bit Windows, the resource is loaded when called.</span></span>              |



 

## <a name="memory-attributes"></a><span data-ttu-id="72837-118">Speicher Attribute</span><span class="sxs-lookup"><span data-stu-id="72837-118">Memory Attributes</span></span>

<span data-ttu-id="72837-119">Die Speicher Attribute geben an, ob die Ressource fest oder verschiebbar ist, ob Sie verworfen werden kann und ob Sie rein ist.</span><span class="sxs-lookup"><span data-stu-id="72837-119">The memory attributes specify whether the resource is fixed or movable, whether it is discardable, and whether it is pure.</span></span> <span data-ttu-id="72837-120">Der Speicher Parameter kann eines oder mehrere der folgenden Attribute sein.</span><span class="sxs-lookup"><span data-stu-id="72837-120">The memory parameter can be one or more of the following attributes.</span></span>



| <span data-ttu-id="72837-121">Attribut</span><span class="sxs-lookup"><span data-stu-id="72837-121">Attribute</span></span>       | <span data-ttu-id="72837-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72837-122">Description</span></span>                                                                                                                               |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72837-123">**FIXED**</span><span class="sxs-lookup"><span data-stu-id="72837-123">**FIXED**</span></span>       | <span data-ttu-id="72837-124">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="72837-124">Ignored.</span></span> <span data-ttu-id="72837-125">In 16-Bit-Fenstern verbleibt die Ressource an einem Speicherort mit fester Größe.</span><span class="sxs-lookup"><span data-stu-id="72837-125">In 16-bit Windows, the resource remains at a fixed memory location.</span></span>                                                              |
| <span data-ttu-id="72837-126">**Moveable**</span><span class="sxs-lookup"><span data-stu-id="72837-126">**MOVEABLE**</span></span>    | <span data-ttu-id="72837-127">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="72837-127">Ignored.</span></span> <span data-ttu-id="72837-128">In 16-Bit-Fenstern kann die Ressource ggf. verschoben werden, um Arbeitsspeicher zu komprimieren.</span><span class="sxs-lookup"><span data-stu-id="72837-128">In 16-bit Windows, the resource can be moved if necessary to compact memory.</span></span>                                                     |
| <span data-ttu-id="72837-129">**Entfernbare**</span><span class="sxs-lookup"><span data-stu-id="72837-129">**DISCARDABLE**</span></span> | <span data-ttu-id="72837-130">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="72837-130">Ignored.</span></span> <span data-ttu-id="72837-131">In 16-Bit-Fenstern kann die Ressource verworfen werden, wenn Sie nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="72837-131">In 16-bit Windows, the resource can be discarded if no longer needed.</span></span>                                                            |
| <span data-ttu-id="72837-132">**Rein**</span><span class="sxs-lookup"><span data-stu-id="72837-132">**PURE**</span></span>        | <span data-ttu-id="72837-133">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="72837-133">Ignored.</span></span> <span data-ttu-id="72837-134">Wird für die Kompatibilität mit vorhandenen Ressourcen Skripts akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="72837-134">Accepted for compatibility with existing resource scripts.</span></span>                                                                       |
| <span data-ttu-id="72837-135">**Unreinen**</span><span class="sxs-lookup"><span data-stu-id="72837-135">**IMPURE**</span></span>      | <span data-ttu-id="72837-136">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="72837-136">Ignored.</span></span> <span data-ttu-id="72837-137">Wird für die Kompatibilität mit vorhandenen Ressourcen Skripts akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="72837-137">Accepted for compatibility with existing resource scripts.</span></span>                                                                       |
| <span data-ttu-id="72837-138">**Genu**</span><span class="sxs-lookup"><span data-stu-id="72837-138">**SHARED**</span></span>      | <span data-ttu-id="72837-139">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="72837-139">Ignored.</span></span> <span data-ttu-id="72837-140">In 16-Bit-Fenstern wird Shared für reguläre Module ignoriert.</span><span class="sxs-lookup"><span data-stu-id="72837-140">In 16-bit Windows, SHARED is ignored for regular modules.</span></span> <span data-ttu-id="72837-141">Für eine Ressource aus einem Windows-Rom-Modul wird der Arbeitsspeicher freigegeben.</span><span class="sxs-lookup"><span data-stu-id="72837-141">For a resource from a ROM Windows module, the memory is shared.</span></span>        |
| <span data-ttu-id="72837-142">**Nicht freigegebene**</span><span class="sxs-lookup"><span data-stu-id="72837-142">**NONSHARED**</span></span>   | <span data-ttu-id="72837-143">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="72837-143">Ignored.</span></span> <span data-ttu-id="72837-144">In 16-Bit-Fenstern wird NonShared für reguläre Module ignoriert.</span><span class="sxs-lookup"><span data-stu-id="72837-144">In 16-bit Windows, NONSHARED is ignored for regular modules.</span></span> <span data-ttu-id="72837-145">Für eine Ressource aus einem Windows-Rom-Modul wird der Arbeitsspeicher nicht freigegeben.</span><span class="sxs-lookup"><span data-stu-id="72837-145">For a resource from a ROM Windows module, the memory is not shared.</span></span> |



 

 

 




