---
title: samplepos (SM 4.1-ASM)
description: Fragt die Position eines Beispiels in einer angegebenen shaderressourcenansicht oder im Rasterizer ab.
ms.assetid: 5A53B342-3A1D-4016-ABF2-CA6236D562C9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910a542dafddb8b855e218f8702c746220780d6e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389583"
---
# <a name="samplepos-sm41---asm"></a><span data-ttu-id="380d3-103">samplepos (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="380d3-103">samplepos (sm4.1 - asm)</span></span>

<span data-ttu-id="380d3-104">Fragt die Position eines Beispiels in einer angegebenen shaderressourcenansicht oder im Rasterizer ab.</span><span class="sxs-lookup"><span data-stu-id="380d3-104">Queries the position of a sample in a given shader resource view or in the rasterizer.</span></span>



| <span data-ttu-id="380d3-105">samplepos dest \[ . mask \] , srkresource \[ . Swizzle \] , sampleindex (skalare Operand)</span><span class="sxs-lookup"><span data-stu-id="380d3-105">samplepos dest\[.mask\], srcResource\[.swizzle\], sampleIndex (scalar operand)</span></span> |
|--------------------------------------------------------------------------------|



 



| <span data-ttu-id="380d3-106">Element</span><span class="sxs-lookup"><span data-stu-id="380d3-106">Item</span></span>                                                                                                               | <span data-ttu-id="380d3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="380d3-107">Description</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="380d3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="380d3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="380d3-109">\[in \] der Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="380d3-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="380d3-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*</span><span class="sxs-lookup"><span data-stu-id="380d3-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="380d3-111">\[in \] der Shader-Ressource.</span><span class="sxs-lookup"><span data-stu-id="380d3-111">\[in\] The shader resource.</span></span><br/>                         |
| <span data-ttu-id="380d3-112"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*Sample Index*</span><span class="sxs-lookup"><span data-stu-id="380d3-112"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span></span><br/> | <span data-ttu-id="380d3-113">\[im \] Index des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="380d3-113">\[in\] The index of the sample.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="380d3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="380d3-114">Remarks</span></span>

<span data-ttu-id="380d3-115">Diese Anweisung gibt die 2D-Beispiel Position von Sample *sampleindex* für die angegebene Ressource zurück.</span><span class="sxs-lookup"><span data-stu-id="380d3-115">This instruction returns the 2D sample position of sample *sampleIndex* for the given resource.</span></span> <span data-ttu-id="380d3-116">Dies gilt nur für Ressourcen, die mit [**ld2dms**](ld2dms--sm4-1---asm-.md) geladen werden können, es sei denn, der Raster ist als *srcresource* angegeben.</span><span class="sxs-lookup"><span data-stu-id="380d3-116">It is valid only for resources that can be loaded using [**ld2dms**](ld2dms--sm4-1---asm-.md) unless the rasterizer is specified as *srcResource*.</span></span>

<span data-ttu-id="380d3-117">*srkresource* kann ein t- \# Register (eine Shader-Ressourcen Ansicht) oder ein Raster-Register sein.</span><span class="sxs-lookup"><span data-stu-id="380d3-117">*srcResource* can be a t\# register (a shader resource view) or a rasterizer register.</span></span>

<span data-ttu-id="380d3-118">Die Anweisung berechnet den Gleit Komma Vektor (XPosition, YPosition, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="380d3-118">The instruction computes the floating point vector (Xposition, Yposition, 0, 0).</span></span>

<span data-ttu-id="380d3-119">Das Swizzle in *srkresource* ermöglicht es, dass die zurückgegebenen Werte willkürlich durchlaufen werden, bevor Sie in das Ziel geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="380d3-119">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span> <span data-ttu-id="380d3-120">Die Beispiel Position ist relativ zum Mittelpunkt des Pixels, basierend auf dem Pixelkoordinaten System.</span><span class="sxs-lookup"><span data-stu-id="380d3-120">The sample position is relative to the pixel's center, based on the Pixel Coordinate System.</span></span>

<span data-ttu-id="380d3-121">Wenn *sampleingedex* außerhalb des gültigen Bereichs liegt, wird ein Vektor NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="380d3-121">If *sampleIndex* is out of bounds a zero vector is returned.</span></span> <span data-ttu-id="380d3-122">Wenn keine Ressource an den angegebenen Slot gebunden ist, wird 0 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="380d3-122">If there is no resource bound to the specified slot, 0 is returned.</span></span>

<span data-ttu-id="380d3-123">**samplepos** können für Dinge wie benutzerdefinierte aufgelösten Elemente in Shader-Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="380d3-123">**samplepos** can be used for things like custom resolves in shader code.</span></span>

<span data-ttu-id="380d3-124">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="380d3-124">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="380d3-125">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="380d3-125">Vertex Shader</span></span> | <span data-ttu-id="380d3-126">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="380d3-126">Geometry Shader</span></span> | <span data-ttu-id="380d3-127">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="380d3-127">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="380d3-128">x</span><span class="sxs-lookup"><span data-stu-id="380d3-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="380d3-129">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="380d3-129">Minimum Shader Model</span></span>

<span data-ttu-id="380d3-130">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="380d3-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="380d3-131">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="380d3-131">Shader Model</span></span>                                              | <span data-ttu-id="380d3-132">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="380d3-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="380d3-133">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="380d3-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="380d3-134">ja</span><span class="sxs-lookup"><span data-stu-id="380d3-134">yes</span></span>       |
| [<span data-ttu-id="380d3-135">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="380d3-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="380d3-136">ja</span><span class="sxs-lookup"><span data-stu-id="380d3-136">yes</span></span>       |
| [<span data-ttu-id="380d3-137">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="380d3-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="380d3-138">nein</span><span class="sxs-lookup"><span data-stu-id="380d3-138">no</span></span>        |
| [<span data-ttu-id="380d3-139">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="380d3-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="380d3-140">nein</span><span class="sxs-lookup"><span data-stu-id="380d3-140">no</span></span>        |
| [<span data-ttu-id="380d3-141">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="380d3-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="380d3-142">nein</span><span class="sxs-lookup"><span data-stu-id="380d3-142">no</span></span>        |
| [<span data-ttu-id="380d3-143">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="380d3-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="380d3-144">nein</span><span class="sxs-lookup"><span data-stu-id="380d3-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="380d3-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="380d3-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="380d3-146">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="380d3-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





