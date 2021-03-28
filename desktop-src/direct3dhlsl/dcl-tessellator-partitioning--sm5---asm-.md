---
title: dcl_tessellator_partitioning (SM5-ASM)
description: Deklarieren Sie die Mosaik-Partitionierung in einem Hull-Shader-Deklarations Abschnitt.
ms.assetid: 6EA00C6B-A0DE-4CE4-8B52-1337CA92CA5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6f6091301f95dd2364debec2bf54c0966c0e64
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389590"
---
# <a name="dcl_tessellator_partitioning-sm5---asm"></a><span data-ttu-id="586af-103">DCL \_ \_ -Mosaik-Partitionierung (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="586af-103">dcl\_tessellator\_partitioning (sm5 - asm)</span></span>

<span data-ttu-id="586af-104">Deklarieren Sie die Mosaik-Partitionierung in einem Hull-Shader-Deklarations Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="586af-104">Declare the tessellator partitioning in a hull shader declaration section.</span></span>



| <span data-ttu-id="586af-105">DCL-Mosaik \_ Prozess- \_ Partitionierung {Partitionierungs \_ Ganzzahl </span><span class="sxs-lookup"><span data-stu-id="586af-105">dcl\_tessellator\_partitioning {partitioning\_integer</span></span>\| <span data-ttu-id="586af-106">Partitionierung \_ pow2 </span><span class="sxs-lookup"><span data-stu-id="586af-106">partitioning\_pow2</span></span>\|<span data-ttu-id="586af-107">Partitionierung von \_ Bruchteil/ \_ ungeraden </span><span class="sxs-lookup"><span data-stu-id="586af-107">partitioning\_fractional\_odd</span></span>\| <span data-ttu-id="586af-108">Partitionierung von \_ Bruchteilen \_ sogar}</span><span class="sxs-lookup"><span data-stu-id="586af-108">partitioning\_fractional\_even}</span></span> |
|---------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="586af-109">Element</span><span class="sxs-lookup"><span data-stu-id="586af-109">Item</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="586af-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="586af-110">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="586af-111"><span id="partitioning_integer__________________________________partitioning_pow2_partitioning_fractional_odd__________________________________partitioning_fractional_even"></span><span id="PARTITIONING_INTEGER__________________________________PARTITIONING_POW2_PARTITIONING_FRACTIONAL_ODD__________________________________PARTITIONING_FRACTIONAL_EVEN"></span>*Partitionierung von \_ ganzzahligen Partitionen \| \_ pow2 \| Partitionierung von \_ Bruchteil der \_ ungeraden \| \_ \_ Dezimalstellen sogar*</span><span class="sxs-lookup"><span data-stu-id="586af-111"><span id="partitioning_integer__________________________________partitioning_pow2_partitioning_fractional_odd__________________________________partitioning_fractional_even"></span><span id="PARTITIONING_INTEGER__________________________________PARTITIONING_POW2_PARTITIONING_FRACTIONAL_ODD__________________________________PARTITIONING_FRACTIONAL_EVEN"></span>*partitioning\_integer\| partitioning\_pow2\|partitioning\_fractional\_odd\| partitioning\_fractional\_even*</span></span><br/> | <span data-ttu-id="586af-112">\[in \] der Mosaik-Partitionierung.</span><span class="sxs-lookup"><span data-stu-id="586af-112">\[in\] The tessellator partitioning.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="586af-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="586af-113">Remarks</span></span>

<span data-ttu-id="586af-114">Aus Sicht der Hardware \_ verhält sich pow2 genauso wie eine \_ ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="586af-114">From the hardware point of view, \_pow2 behaves just like \_integer.</span></span> <span data-ttu-id="586af-115">Der HLSL-Shader-Autor und/oder-Kompilier Code ist für die Rundung von Tess Factors auf die Potenzen von 2 fest.</span><span class="sxs-lookup"><span data-stu-id="586af-115">It is up to the HLSL shader author and/or compilercode to round TessFactors to powers of 2.</span></span>

<span data-ttu-id="586af-116">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="586af-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="586af-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="586af-117">Vertex</span></span> | <span data-ttu-id="586af-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="586af-118">Hull</span></span>                 | <span data-ttu-id="586af-119">Domain</span><span class="sxs-lookup"><span data-stu-id="586af-119">Domain</span></span> | <span data-ttu-id="586af-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="586af-120">Geometry</span></span> | <span data-ttu-id="586af-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="586af-121">Pixel</span></span> | <span data-ttu-id="586af-122">Compute</span><span class="sxs-lookup"><span data-stu-id="586af-122">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="586af-123">Deklarations Abschnitt</span><span class="sxs-lookup"><span data-stu-id="586af-123">Declarations Section</span></span> |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="586af-124">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="586af-124">Minimum Shader Model</span></span>

<span data-ttu-id="586af-125">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="586af-125">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="586af-126">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="586af-126">Shader Model</span></span>                                              | <span data-ttu-id="586af-127">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="586af-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="586af-128">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="586af-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="586af-129">ja</span><span class="sxs-lookup"><span data-stu-id="586af-129">yes</span></span>       |
| [<span data-ttu-id="586af-130">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="586af-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="586af-131">nein</span><span class="sxs-lookup"><span data-stu-id="586af-131">no</span></span>        |
| [<span data-ttu-id="586af-132">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="586af-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="586af-133">nein</span><span class="sxs-lookup"><span data-stu-id="586af-133">no</span></span>        |
| [<span data-ttu-id="586af-134">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="586af-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="586af-135">nein</span><span class="sxs-lookup"><span data-stu-id="586af-135">no</span></span>        |
| [<span data-ttu-id="586af-136">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="586af-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="586af-137">nein</span><span class="sxs-lookup"><span data-stu-id="586af-137">no</span></span>        |
| [<span data-ttu-id="586af-138">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="586af-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="586af-139">nein</span><span class="sxs-lookup"><span data-stu-id="586af-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="586af-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="586af-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="586af-141">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="586af-141">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





