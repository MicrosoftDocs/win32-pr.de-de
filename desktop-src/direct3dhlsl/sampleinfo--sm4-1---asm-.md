---
title: sampleinfo (SM 4.1-ASM)
description: Fragt die Anzahl der Stichproben in einer angegebenen shaderressourcenansicht oder im Rasterizer ab.
ms.assetid: 1F0968D7-01E9-4213-9F83-172B88374C3C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d307dbc8c79618a6401737874a9f6e060a899ccc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857812"
---
# <a name="sampleinfo-sm41---asm"></a><span data-ttu-id="aa2d1-103">sampleinfo (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="aa2d1-103">sampleinfo (sm4.1 - asm)</span></span>

<span data-ttu-id="aa2d1-104">Fragt die Anzahl der Stichproben in einer angegebenen shaderressourcenansicht oder im Rasterizer ab.</span><span class="sxs-lookup"><span data-stu-id="aa2d1-104">Queries the number of samples in a given shader resource view or in the rasterizer.</span></span>



| <span data-ttu-id="aa2d1-105">\[\_uint \] dest \[ . mask \] , srkresource \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="aa2d1-105">\[\_uint\] dest\[.mask\], srcResource\[.swizzle\]</span></span> |
|---------------------------------------------------|



 



| <span data-ttu-id="aa2d1-106">Element</span><span class="sxs-lookup"><span data-stu-id="aa2d1-106">Item</span></span>                                                                                                               | <span data-ttu-id="aa2d1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa2d1-107">Description</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="aa2d1-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="aa2d1-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="aa2d1-109">\[in \] der Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="aa2d1-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="aa2d1-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*</span><span class="sxs-lookup"><span data-stu-id="aa2d1-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="aa2d1-111">\[in \] der Shader-Ressource.</span><span class="sxs-lookup"><span data-stu-id="aa2d1-111">\[in\] The shader resource.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="aa2d1-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa2d1-112">Remarks</span></span>

<span data-ttu-id="aa2d1-113">Diese Anweisung gibt die Anzahl von Stichproben für die angegebene Ressource oder den Rasterizer zurück.</span><span class="sxs-lookup"><span data-stu-id="aa2d1-113">This instruction returns the number of samples for the given resource or the rasterizer.</span></span> <span data-ttu-id="aa2d1-114">Dies gilt nur für Ressourcen, die mit [**ld2dms**](ld2dms--sm4-1---asm-.md) geladen werden können, es sei denn, der Raster ist als *srcresource* angegeben.</span><span class="sxs-lookup"><span data-stu-id="aa2d1-114">It is valid only for resources that can be loaded using [**ld2dms**](ld2dms--sm4-1---asm-.md) unless the rasterizer is specified as *srcResource*.</span></span> <span data-ttu-id="aa2d1-115">*srkresource* kann ein t- \# Register (eine Shader-Ressourcen Ansicht) oder ein Raster-Register sein.</span><span class="sxs-lookup"><span data-stu-id="aa2d1-115">*srcResource* could be a t\# register (a shader resource view) or a rasterizer register.</span></span>

<span data-ttu-id="aa2d1-116">Die Anweisung berechnet den Vektor (samplecount, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="aa2d1-116">The instruction computes the vector (SampleCount,0,0,0).</span></span>

<span data-ttu-id="aa2d1-117">Das Swizzle in *srkresource* ermöglicht es, dass die zurückgegebenen Werte willkürlich durchlaufen werden, bevor Sie in das Ziel geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="aa2d1-117">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span> <span data-ttu-id="aa2d1-118">Der zurückgegebene Wert ist ein Gleit Komma Wert, es sei denn \_ , der uint-Modifizierer wird verwendet. in diesem Fall ist der zurückgegebene Wert Integer.</span><span class="sxs-lookup"><span data-stu-id="aa2d1-118">The returned value is floating point, unless the \_uint modifier is used, in which case the returned value is integer.</span></span> <span data-ttu-id="aa2d1-119">Wenn keine Ressource an den angegebenen Slot gebunden ist, wird 0 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="aa2d1-119">If there is no resource bound to the specified slot, 0 is returned.</span></span>

<span data-ttu-id="aa2d1-120">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="aa2d1-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="aa2d1-121">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="aa2d1-121">Vertex Shader</span></span> | <span data-ttu-id="aa2d1-122">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="aa2d1-122">Geometry Shader</span></span> | <span data-ttu-id="aa2d1-123">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="aa2d1-123">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="aa2d1-124">X</span><span class="sxs-lookup"><span data-stu-id="aa2d1-124">X</span></span>             | <span data-ttu-id="aa2d1-125">X</span><span class="sxs-lookup"><span data-stu-id="aa2d1-125">X</span></span>               | <span data-ttu-id="aa2d1-126">w</span><span class="sxs-lookup"><span data-stu-id="aa2d1-126">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="aa2d1-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="aa2d1-127">Minimum Shader Model</span></span>

<span data-ttu-id="aa2d1-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aa2d1-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="aa2d1-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="aa2d1-129">Shader Model</span></span>                                              | <span data-ttu-id="aa2d1-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="aa2d1-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="aa2d1-131">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="aa2d1-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="aa2d1-132">ja</span><span class="sxs-lookup"><span data-stu-id="aa2d1-132">yes</span></span>       |
| [<span data-ttu-id="aa2d1-133">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="aa2d1-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="aa2d1-134">ja</span><span class="sxs-lookup"><span data-stu-id="aa2d1-134">yes</span></span>       |
| [<span data-ttu-id="aa2d1-135">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="aa2d1-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="aa2d1-136">nein</span><span class="sxs-lookup"><span data-stu-id="aa2d1-136">no</span></span>        |
| [<span data-ttu-id="aa2d1-137">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa2d1-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="aa2d1-138">nein</span><span class="sxs-lookup"><span data-stu-id="aa2d1-138">no</span></span>        |
| [<span data-ttu-id="aa2d1-139">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa2d1-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="aa2d1-140">nein</span><span class="sxs-lookup"><span data-stu-id="aa2d1-140">no</span></span>        |
| [<span data-ttu-id="aa2d1-141">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa2d1-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="aa2d1-142">nein</span><span class="sxs-lookup"><span data-stu-id="aa2d1-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="aa2d1-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aa2d1-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa2d1-144">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa2d1-144">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





