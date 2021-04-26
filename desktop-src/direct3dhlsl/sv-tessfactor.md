---
title: SV_TessFactor
description: Definiert den Mosaikbetrag an jedem Rand eines Patches.
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
ms.openlocfilehash: 808365fbcba4a1180c1838b94a6c098aa4c6f9ac
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999057"
---
# <a name="sv_tessfactor"></a><span data-ttu-id="df621-104">SV \_ TessFactor</span><span class="sxs-lookup"><span data-stu-id="df621-104">SV\_TessFactor</span></span>

<span data-ttu-id="df621-105">Definiert den Mosaikbetrag an jedem Rand eines Patches.</span><span class="sxs-lookup"><span data-stu-id="df621-105">Defines the tessellation amount on each edge of a patch.</span></span>

## <a name="type"></a><span data-ttu-id="df621-106">Typ</span><span class="sxs-lookup"><span data-stu-id="df621-106">Type</span></span>



|            |                |
|------------|----------------|
| <span data-ttu-id="df621-107">Typ</span><span class="sxs-lookup"><span data-stu-id="df621-107">Type</span></span>       | <span data-ttu-id="df621-108">Eingabetopologie</span><span class="sxs-lookup"><span data-stu-id="df621-108">Input Topology</span></span> |
| <span data-ttu-id="df621-109">float \[ 4\]</span><span class="sxs-lookup"><span data-stu-id="df621-109">float\[4\]</span></span> | <span data-ttu-id="df621-110">Quad-Patch</span><span class="sxs-lookup"><span data-stu-id="df621-110">quad patch</span></span>     |
| <span data-ttu-id="df621-111">float \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="df621-111">float\[3\]</span></span> | <span data-ttu-id="df621-112">Tri Patch</span><span class="sxs-lookup"><span data-stu-id="df621-112">tri patch</span></span>      |
| <span data-ttu-id="df621-113">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="df621-113">float\[2\]</span></span> | <span data-ttu-id="df621-114">Isoline</span><span class="sxs-lookup"><span data-stu-id="df621-114">isoline</span></span>        |



 

<span data-ttu-id="df621-115">Mosaikfaktoren müssen als Array deklariert werden. sie können nicht in einen einzelnen Vektor gepackt werden.</span><span class="sxs-lookup"><span data-stu-id="df621-115">Tessellation factors must be declared as an array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="df621-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="df621-116">Remarks</span></span>

<span data-ttu-id="df621-117">Der Wert für den Mosaikfaktor muss während der Patchkonstantenfunktion des Hüllen-Shaders definiert werden.</span><span class="sxs-lookup"><span data-stu-id="df621-117">The value for tessellation factor must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="df621-118">Erforderlicher Ausgabewert für den Hüllen-Shader bei Verwendung von Quad- oder Tri-Patches.</span><span class="sxs-lookup"><span data-stu-id="df621-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="df621-119">Dieser Wert ist auch ein erforderlicher Eingabewert für den Domänen-Shader, um die patchkonstanten Datensignaturen zwischen den Mosaikstufen abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="df621-119">This value is also a required input value for the domain shader to match the patch-constant data signatures between the tessellation stages.</span></span>

<span data-ttu-id="df621-120">Bei einer Isolinie ist der erste Wert in SV \_ TessFactor der Mosaikfaktor für die Liniendichte, der zweite Wert der Mosaikfaktor für Liniendetails.</span><span class="sxs-lookup"><span data-stu-id="df621-120">For an isoline, the first value in SV\_TessFactor is the line-density tessellation factor, the second value is the line-detail tessellation factor.</span></span>

### <a name="tri-patch-tessellation-factors"></a><span data-ttu-id="df621-121">Tri Patch Tessellation Factors</span><span class="sxs-lookup"><span data-stu-id="df621-121">Tri Patch Tessellation Factors</span></span>

<span data-ttu-id="df621-122">Die erste Komponente stellt den Mosaikfaktor für den u==0-Rand des Patches bereit.</span><span class="sxs-lookup"><span data-stu-id="df621-122">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="df621-123">Die zweite Komponente stellt den Mosaikfaktor für den v==0-Rand des Patches bereit.</span><span class="sxs-lookup"><span data-stu-id="df621-123">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="df621-124">Die dritte Komponente stellt den Mosaikfaktor für den w==0-Rand des Patches dar.</span><span class="sxs-lookup"><span data-stu-id="df621-124">The third component provides the tesselation factor for the w==0 edge of the patch.</span></span>

### <a name="quad-patch-tessellation-factors"></a><span data-ttu-id="df621-125">Quad Patch Tessellation Factors</span><span class="sxs-lookup"><span data-stu-id="df621-125">Quad Patch Tessellation Factors</span></span>

<span data-ttu-id="df621-126">Die erste Komponente stellt den Mosaikfaktor für den u==0-Rand des Patches dar.</span><span class="sxs-lookup"><span data-stu-id="df621-126">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="df621-127">Die zweite Komponente stellt den Mosaikfaktor für den v==0-Rand des Patches dar.</span><span class="sxs-lookup"><span data-stu-id="df621-127">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="df621-128">Die dritte Komponente stellt den Mosaikfaktor für den u==1-Rand des Patches dar.</span><span class="sxs-lookup"><span data-stu-id="df621-128">The third component provides the tesselation factor for the u==1 edge of the patch.</span></span> <span data-ttu-id="df621-129">Die vierte Komponente stellt den Mosaikfaktor für den v==1-Rand des Patches dar.</span><span class="sxs-lookup"><span data-stu-id="df621-129">The fourth component provides the tesselation factor for the v==1 edge of the patch.</span></span> <span data-ttu-id="df621-130">Die Reihenfolge der Ränder ist im Uhrzeigersinn, beginnend mit der Kante u==0, die die linke Seite des Patches ist, und von der v==0-Kante, die der obere Rand des Patches ist.</span><span class="sxs-lookup"><span data-stu-id="df621-130">The ordering of the edges is clockwise, starting from the u==0 edge, which is the left side of the patch, and from the v==0 edge, which is the top of the patch.</span></span>

<span data-ttu-id="df621-131">Diese Funktion wird in den folgenden Shadertypen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="df621-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="df621-132">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="df621-132">Vertex</span></span> | <span data-ttu-id="df621-133">Rumpf</span><span class="sxs-lookup"><span data-stu-id="df621-133">Hull</span></span> | <span data-ttu-id="df621-134">Domain</span><span class="sxs-lookup"><span data-stu-id="df621-134">Domain</span></span> | <span data-ttu-id="df621-135">Geometrie</span><span class="sxs-lookup"><span data-stu-id="df621-135">Geometry</span></span> | <span data-ttu-id="df621-136">Pixel</span><span class="sxs-lookup"><span data-stu-id="df621-136">Pixel</span></span> | <span data-ttu-id="df621-137">Compute</span><span class="sxs-lookup"><span data-stu-id="df621-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="df621-138">x</span><span class="sxs-lookup"><span data-stu-id="df621-138">x</span></span>    | <span data-ttu-id="df621-139">x</span><span class="sxs-lookup"><span data-stu-id="df621-139">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="df621-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="df621-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df621-141">Semantik</span><span class="sxs-lookup"><span data-stu-id="df621-141">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="df621-142">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="df621-142">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




