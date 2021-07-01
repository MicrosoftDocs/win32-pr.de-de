---
title: SV_TessFactor
description: Definiert die Mosaikmenge an jedem Rand eines Patches.
ms.assetid: 970ff744-da5b-4933-866c-dd38b85fb48d
keywords:
- SV_TessFactor HLSL
topic_type:
- apiref
api_name:
- SV_TessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 308034fe607283ef9f1213cca1cabb4a7229765e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118895"
---
# <a name="sv_tessfactor"></a><span data-ttu-id="cd59b-104">SV \_ TessFactor</span><span class="sxs-lookup"><span data-stu-id="cd59b-104">SV\_TessFactor</span></span>

<span data-ttu-id="cd59b-105">Definiert die Mosaikmenge an jedem Rand eines Patches.</span><span class="sxs-lookup"><span data-stu-id="cd59b-105">Defines the tessellation amount on each edge of a patch.</span></span>

## <a name="type"></a><span data-ttu-id="cd59b-106">Typ</span><span class="sxs-lookup"><span data-stu-id="cd59b-106">Type</span></span>



|  <span data-ttu-id="cd59b-107">Typ</span><span class="sxs-lookup"><span data-stu-id="cd59b-107">Type</span></span>          |  <span data-ttu-id="cd59b-108">Eingabetopologie</span><span class="sxs-lookup"><span data-stu-id="cd59b-108">Input topology</span></span>              |
|------------|----------------|
| <span data-ttu-id="cd59b-109">float \[ 4\]</span><span class="sxs-lookup"><span data-stu-id="cd59b-109">float\[4\]</span></span> | <span data-ttu-id="cd59b-110">Quad Patch</span><span class="sxs-lookup"><span data-stu-id="cd59b-110">quad patch</span></span>     |
| <span data-ttu-id="cd59b-111">float \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="cd59b-111">float\[3\]</span></span> | <span data-ttu-id="cd59b-112">tri patch</span><span class="sxs-lookup"><span data-stu-id="cd59b-112">tri patch</span></span>      |
| <span data-ttu-id="cd59b-113">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="cd59b-113">float\[2\]</span></span> | <span data-ttu-id="cd59b-114">isoline</span><span class="sxs-lookup"><span data-stu-id="cd59b-114">isoline</span></span>        |



 

<span data-ttu-id="cd59b-115">Mosaikfaktoren müssen als Array deklariert werden. sie können nicht in einen einzelnen Vektor gepackt werden.</span><span class="sxs-lookup"><span data-stu-id="cd59b-115">Tessellation factors must be declared as an array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd59b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd59b-116">Remarks</span></span>

<span data-ttu-id="cd59b-117">Der Wert für den Mosaikfaktor muss während der Patchkonstationsfunktion des Hüllen-Shaders definiert werden.</span><span class="sxs-lookup"><span data-stu-id="cd59b-117">The value for tessellation factor must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="cd59b-118">Erforderlicher Ausgabewert für den Hüllen-Shader, wenn Quad- oder Tri-Patches verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd59b-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="cd59b-119">Dieser Wert ist auch ein erforderlicher Eingabewert für den Domänen-Shader, der mit den Patchkonstten-Datensignaturen zwischen den Mosaikstufen übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="cd59b-119">This value is also a required input value for the domain shader to match the patch-constant data signatures between the tessellation stages.</span></span>

<span data-ttu-id="cd59b-120">Bei einer Isoline ist der erste Wert in SV TessFactor der Mosaikfaktor der Liniendichte, der zweite Wert ist der Mosaikfaktor für \_ Zeilendetails.</span><span class="sxs-lookup"><span data-stu-id="cd59b-120">For an isoline, the first value in SV\_TessFactor is the line-density tessellation factor, the second value is the line-detail tessellation factor.</span></span>

### <a name="tri-patch-tessellation-factors"></a><span data-ttu-id="cd59b-121">Tri Patch Tessellation Factors</span><span class="sxs-lookup"><span data-stu-id="cd59b-121">Tri Patch Tessellation Factors</span></span>

<span data-ttu-id="cd59b-122">Die erste Komponente stellt den Mosaikfaktor für den u==0-Rand des Patches dar.</span><span class="sxs-lookup"><span data-stu-id="cd59b-122">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="cd59b-123">Die zweite Komponente stellt den Mosaikfaktor für den v==0-Rand des Patches dar.</span><span class="sxs-lookup"><span data-stu-id="cd59b-123">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="cd59b-124">Die dritte Komponente stellt den Mosaikfaktor für den w==0-Rand des Patches dar.</span><span class="sxs-lookup"><span data-stu-id="cd59b-124">The third component provides the tesselation factor for the w==0 edge of the patch.</span></span>

### <a name="quad-patch-tessellation-factors"></a><span data-ttu-id="cd59b-125">Quad Patch Tessellation Factors</span><span class="sxs-lookup"><span data-stu-id="cd59b-125">Quad Patch Tessellation Factors</span></span>

<span data-ttu-id="cd59b-126">Die erste Komponente stellt den Mosaikfaktor für den u==0-Rand des Patches dar.</span><span class="sxs-lookup"><span data-stu-id="cd59b-126">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="cd59b-127">Die zweite Komponente stellt den Mosaikfaktor für den v==0-Rand des Patches dar.</span><span class="sxs-lookup"><span data-stu-id="cd59b-127">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="cd59b-128">Die dritte Komponente stellt den Mosaikfaktor für den u==1-Rand des Patches dar.</span><span class="sxs-lookup"><span data-stu-id="cd59b-128">The third component provides the tesselation factor for the u==1 edge of the patch.</span></span> <span data-ttu-id="cd59b-129">Die vierte Komponente stellt den Mosaikfaktor für den v==1-Rand des Patches dar.</span><span class="sxs-lookup"><span data-stu-id="cd59b-129">The fourth component provides the tesselation factor for the v==1 edge of the patch.</span></span> <span data-ttu-id="cd59b-130">Die Reihenfolge der Ränder ist im Uhrzeigersinn, beginnend mit der Kante u==0, die die linke Seite des Patches ist, und von der v==0-Kante, die der obere Rand des Patches ist.</span><span class="sxs-lookup"><span data-stu-id="cd59b-130">The ordering of the edges is clockwise, starting from the u==0 edge, which is the left side of the patch, and from the v==0 edge, which is the top of the patch.</span></span>

<span data-ttu-id="cd59b-131">Diese Funktion wird in den folgenden Shadertypen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="cd59b-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="cd59b-132">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="cd59b-132">Vertex</span></span> | <span data-ttu-id="cd59b-133">Rumpf</span><span class="sxs-lookup"><span data-stu-id="cd59b-133">Hull</span></span> | <span data-ttu-id="cd59b-134">Domain</span><span class="sxs-lookup"><span data-stu-id="cd59b-134">Domain</span></span> | <span data-ttu-id="cd59b-135">Geometrie</span><span class="sxs-lookup"><span data-stu-id="cd59b-135">Geometry</span></span> | <span data-ttu-id="cd59b-136">Pixel</span><span class="sxs-lookup"><span data-stu-id="cd59b-136">Pixel</span></span> | <span data-ttu-id="cd59b-137">Compute</span><span class="sxs-lookup"><span data-stu-id="cd59b-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="cd59b-138">x</span><span class="sxs-lookup"><span data-stu-id="cd59b-138">x</span></span>    | <span data-ttu-id="cd59b-139">x</span><span class="sxs-lookup"><span data-stu-id="cd59b-139">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="cd59b-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd59b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd59b-141">Semantik</span><span class="sxs-lookup"><span data-stu-id="cd59b-141">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="cd59b-142">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="cd59b-142">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




