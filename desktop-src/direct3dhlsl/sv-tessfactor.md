---
title: SV_TessFactor
description: Definiert den Mosaik Betrag an jedem Rand eines Patches.
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
ms.openlocfilehash: 8fa49b19109985b590747098826199b33a32dd2d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104976216"
---
# <a name="sv_tessfactor"></a><span data-ttu-id="9595b-104">SV-Mosaik \_ Faktor</span><span class="sxs-lookup"><span data-stu-id="9595b-104">SV\_TessFactor</span></span>

<span data-ttu-id="9595b-105">Definiert den Mosaik Betrag an jedem Rand eines Patches.</span><span class="sxs-lookup"><span data-stu-id="9595b-105">Defines the tessellation amount on each edge of a patch.</span></span>

## <a name="type"></a><span data-ttu-id="9595b-106">Typ</span><span class="sxs-lookup"><span data-stu-id="9595b-106">Type</span></span>



|            |                |
|------------|----------------|
| <span data-ttu-id="9595b-107">Typ</span><span class="sxs-lookup"><span data-stu-id="9595b-107">Type</span></span>       | <span data-ttu-id="9595b-108">Eingabe Topologie</span><span class="sxs-lookup"><span data-stu-id="9595b-108">Input Topology</span></span> |
| <span data-ttu-id="9595b-109">float \[ 4\]</span><span class="sxs-lookup"><span data-stu-id="9595b-109">float\[4\]</span></span> | <span data-ttu-id="9595b-110">Quad-Patch</span><span class="sxs-lookup"><span data-stu-id="9595b-110">quad patch</span></span>     |
| <span data-ttu-id="9595b-111">float \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="9595b-111">float\[3\]</span></span> | <span data-ttu-id="9595b-112">Tri-Patch</span><span class="sxs-lookup"><span data-stu-id="9595b-112">tri patch</span></span>      |
| <span data-ttu-id="9595b-113">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="9595b-113">float\[2\]</span></span> | <span data-ttu-id="9595b-114">Isolation</span><span class="sxs-lookup"><span data-stu-id="9595b-114">isoline</span></span>        |



 

<span data-ttu-id="9595b-115">Mosaik Faktoren müssen als Array deklariert werden. Sie können nicht in einen einzigen Vektor gepackt werden.</span><span class="sxs-lookup"><span data-stu-id="9595b-115">Tessellation factors must be declared as an array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="9595b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9595b-116">Remarks</span></span>

<span data-ttu-id="9595b-117">Der Wert für den Mosaik Faktor muss während der Patch-konstantenfunktion des Hull-Shaders definiert werden.</span><span class="sxs-lookup"><span data-stu-id="9595b-117">The value for tessellation factor must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="9595b-118">Erforderlicher Ausgabewert für den Hull-Shader bei Verwendung von Quad-oder Tri-Patches.</span><span class="sxs-lookup"><span data-stu-id="9595b-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="9595b-119">Bei diesem Wert handelt es sich auch um einen erforderlichen Eingabe Wert für den Domänen-Shader, um die Daten Signaturen der patchkonstanten zwischen den Mosaik Stufen abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="9595b-119">This value is also a required input value for the domain shader to match the patch-constant data signatures between the tessellation stages.</span></span>

<span data-ttu-id="9595b-120">Bei einer Isolationsstufe ist der erste Wert in SV \_ Tess Factor der Mosaik Faktor für die Zeilen Dichte, der zweite Wert ist der Mosaik Faktor für die Zeilen Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="9595b-120">For an isoline, the first value in SV\_TessFactor is the line-density tessellation factor, the second value is the line-detail tessellation factor.</span></span>

### <a name="tri-patch-tessellation-factors"></a><span data-ttu-id="9595b-121">Drei Patch-Mosaik Faktoren</span><span class="sxs-lookup"><span data-stu-id="9595b-121">Tri Patch Tessellation Factors</span></span>

<span data-ttu-id="9595b-122">Die erste Komponente stellt den Tesselations Faktor für den u = = 0-Rand des Patches bereit.</span><span class="sxs-lookup"><span data-stu-id="9595b-122">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="9595b-123">Die zweite Komponente stellt den Tesselations Faktor für den v = = 0-Rand des Patches bereit.</span><span class="sxs-lookup"><span data-stu-id="9595b-123">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="9595b-124">Die dritte Komponente stellt den Tesselations Faktor für den w = = 0-Rand des Patches bereit.</span><span class="sxs-lookup"><span data-stu-id="9595b-124">The third component provides the tesselation factor for the w==0 edge of the patch.</span></span>

### <a name="quad-patch-tessellation-factors"></a><span data-ttu-id="9595b-125">Vier patchmosaik Faktoren</span><span class="sxs-lookup"><span data-stu-id="9595b-125">Quad Patch Tessellation Factors</span></span>

<span data-ttu-id="9595b-126">Die erste Komponente stellt den Tesselations Faktor für den u = = 0-Rand des Patches bereit.</span><span class="sxs-lookup"><span data-stu-id="9595b-126">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="9595b-127">Die zweite Komponente stellt den Tesselations Faktor für den v = = 0-Rand des Patches bereit.</span><span class="sxs-lookup"><span data-stu-id="9595b-127">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="9595b-128">Die dritte Komponente stellt den Tesselations Faktor für den u = = 1-Rand des Patches bereit.</span><span class="sxs-lookup"><span data-stu-id="9595b-128">The third component provides the tesselation factor for the u==1 edge of the patch.</span></span> <span data-ttu-id="9595b-129">Die vierte Komponente stellt den Tesselations Faktor für den v = = 1-Rand des Patches bereit.</span><span class="sxs-lookup"><span data-stu-id="9595b-129">The fourth component provides the tesselation factor for the v==1 edge of the patch.</span></span> <span data-ttu-id="9595b-130">Die Reihenfolge der Kanten ist im Uhrzeigersinn, beginnend ab dem "u = = 0"-Rand, der linken Seite des Patches und vom "v = = 0"-Rand, der am Anfang des Patches steht.</span><span class="sxs-lookup"><span data-stu-id="9595b-130">The ordering of the edges is clockwise, starting from the u==0 edge, which is the left side of the patch, and from the v==0 edge, which is the top of the patch.</span></span>

<span data-ttu-id="9595b-131">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="9595b-131">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9595b-132">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="9595b-132">Vertex</span></span> | <span data-ttu-id="9595b-133">Hülle</span><span class="sxs-lookup"><span data-stu-id="9595b-133">Hull</span></span> | <span data-ttu-id="9595b-134">Domain</span><span class="sxs-lookup"><span data-stu-id="9595b-134">Domain</span></span> | <span data-ttu-id="9595b-135">Geometrie</span><span class="sxs-lookup"><span data-stu-id="9595b-135">Geometry</span></span> | <span data-ttu-id="9595b-136">Pixel</span><span class="sxs-lookup"><span data-stu-id="9595b-136">Pixel</span></span> | <span data-ttu-id="9595b-137">Compute</span><span class="sxs-lookup"><span data-stu-id="9595b-137">Compute</span></span> |
|        | <span data-ttu-id="9595b-138">x</span><span class="sxs-lookup"><span data-stu-id="9595b-138">x</span></span>    | <span data-ttu-id="9595b-139">x</span><span class="sxs-lookup"><span data-stu-id="9595b-139">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="9595b-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9595b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9595b-141">Semantik</span><span class="sxs-lookup"><span data-stu-id="9595b-141">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="9595b-142">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="9595b-142">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




