---
title: log (sm4 - asm)
description: Komponentenweise Protokollbasis 2.
ms.assetid: 6D28864A-C2BA-44AF-9E78-7C2B34F5E462
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88e4b89b4dcc085cf4fd4fda762d96fb71271af2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998317"
---
# <a name="log-sm4---asm"></a><span data-ttu-id="f7fdc-103">log (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="f7fdc-103">log (sm4 - asm)</span></span>

<span data-ttu-id="f7fdc-104">Komponentenweise Protokollbasis 2.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-104">Component-wise log base 2.</span></span>



| <span data-ttu-id="f7fdc-105">log \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle</span><span class="sxs-lookup"><span data-stu-id="f7fdc-105">log\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle</span></span> |
|----------------------------------------------------------|



 



| <span data-ttu-id="f7fdc-106">Element</span><span class="sxs-lookup"><span data-stu-id="f7fdc-106">Item</span></span>                                                            | <span data-ttu-id="f7fdc-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7fdc-107">Description</span></span>                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7fdc-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="f7fdc-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="f7fdc-109">\[in \] Die Adresse des Ergebnisses des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="f7fdc-110">dest = log2(src0)</span><span class="sxs-lookup"><span data-stu-id="f7fdc-110">dest = log2(src0)</span></span><br/> |
| <span data-ttu-id="f7fdc-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f7fdc-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="f7fdc-112">\[in \] Der Wert für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-112">\[in\] The value for the operation.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="f7fdc-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f7fdc-113">Remarks</span></span>

### <a name="restrictions"></a><span data-ttu-id="f7fdc-114">Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="f7fdc-114">Restrictions</span></span>

-   <span data-ttu-id="f7fdc-115">Folgt der Begrenzungstheore.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-115">Follows limit theory.</span></span>
-   <span data-ttu-id="f7fdc-116">Fehlertoleranz: Wenn *src0* \[ 0.5..2 ist, darf absolue error nicht mehr als \] 2-21 sein.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-116">Error tolerance: If *src0* is \[0.5..2\], absolue error must be no more than 2-21.</span></span> <span data-ttu-id="f7fdc-117">Wenn *src0* (0..0.5) oder (2..+INF) ist, darf der relative Fehler nicht mehr als \] 2-21 sein.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-117">If *src0* is (0..0.5) or (2..+INF\], relative error must be no more than 2-21.</span></span>

<span data-ttu-id="f7fdc-118">Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Zahlenklassen erzielt werden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-118">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="f7fdc-119">F bedeutet endliche reale Zahl.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-119">F means finite-real number.</span></span>



| <span data-ttu-id="f7fdc-120">**src**</span><span class="sxs-lookup"><span data-stu-id="f7fdc-120">**src**</span></span>  | <span data-ttu-id="f7fdc-121">**-inf**</span><span class="sxs-lookup"><span data-stu-id="f7fdc-121">**-inf**</span></span> | <span data-ttu-id="f7fdc-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="f7fdc-122">**-F**</span></span> | <span data-ttu-id="f7fdc-123">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="f7fdc-123">**-denorm**</span></span> | <span data-ttu-id="f7fdc-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="f7fdc-124">**-0**</span></span> | <span data-ttu-id="f7fdc-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="f7fdc-125">**+0**</span></span> | <span data-ttu-id="f7fdc-126">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="f7fdc-126">**+denorm**</span></span> | <span data-ttu-id="f7fdc-127">**+F**</span><span class="sxs-lookup"><span data-stu-id="f7fdc-127">**+F**</span></span> | <span data-ttu-id="f7fdc-128">**+inf**</span><span class="sxs-lookup"><span data-stu-id="f7fdc-128">**+inf**</span></span> | <span data-ttu-id="f7fdc-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="f7fdc-129">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="f7fdc-130">**Dest**</span><span class="sxs-lookup"><span data-stu-id="f7fdc-130">**dest**</span></span> | <span data-ttu-id="f7fdc-131">NaN</span><span class="sxs-lookup"><span data-stu-id="f7fdc-131">NaN</span></span>      | <span data-ttu-id="f7fdc-132">NaN</span><span class="sxs-lookup"><span data-stu-id="f7fdc-132">NaN</span></span>    | <span data-ttu-id="f7fdc-133">-inf</span><span class="sxs-lookup"><span data-stu-id="f7fdc-133">-inf</span></span>        | <span data-ttu-id="f7fdc-134">-inf</span><span class="sxs-lookup"><span data-stu-id="f7fdc-134">-inf</span></span>   | <span data-ttu-id="f7fdc-135">-inf</span><span class="sxs-lookup"><span data-stu-id="f7fdc-135">-inf</span></span>   | <span data-ttu-id="f7fdc-136">-inf</span><span class="sxs-lookup"><span data-stu-id="f7fdc-136">-inf</span></span>        | <span data-ttu-id="f7fdc-137">F</span><span class="sxs-lookup"><span data-stu-id="f7fdc-137">F</span></span>      | <span data-ttu-id="f7fdc-138">+inf</span><span class="sxs-lookup"><span data-stu-id="f7fdc-138">+inf</span></span>     | <span data-ttu-id="f7fdc-139">NaN</span><span class="sxs-lookup"><span data-stu-id="f7fdc-139">NaN</span></span>     |



 

<span data-ttu-id="f7fdc-140">Diese Anweisung gilt für die folgenden Shaderstufen:</span><span class="sxs-lookup"><span data-stu-id="f7fdc-140">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f7fdc-141">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="f7fdc-141">Vertex Shader</span></span> | <span data-ttu-id="f7fdc-142">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="f7fdc-142">Geometry Shader</span></span> | <span data-ttu-id="f7fdc-143">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="f7fdc-143">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="f7fdc-144">x</span><span class="sxs-lookup"><span data-stu-id="f7fdc-144">x</span></span>             | <span data-ttu-id="f7fdc-145">x</span><span class="sxs-lookup"><span data-stu-id="f7fdc-145">x</span></span>               | <span data-ttu-id="f7fdc-146">x</span><span class="sxs-lookup"><span data-stu-id="f7fdc-146">x</span></span>            |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="f7fdc-147">Shader-Mindestmodell</span><span class="sxs-lookup"><span data-stu-id="f7fdc-147">Minimum Shader Model</span></span>

<span data-ttu-id="f7fdc-148">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f7fdc-149">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="f7fdc-149">Shader Model</span></span>                                              | <span data-ttu-id="f7fdc-150">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="f7fdc-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f7fdc-151">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="f7fdc-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f7fdc-152">ja</span><span class="sxs-lookup"><span data-stu-id="f7fdc-152">yes</span></span>       |
| [<span data-ttu-id="f7fdc-153">Shadermodell 4.1</span><span class="sxs-lookup"><span data-stu-id="f7fdc-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f7fdc-154">ja</span><span class="sxs-lookup"><span data-stu-id="f7fdc-154">yes</span></span>       |
| [<span data-ttu-id="f7fdc-155">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="f7fdc-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f7fdc-156">ja</span><span class="sxs-lookup"><span data-stu-id="f7fdc-156">yes</span></span>       |
| [<span data-ttu-id="f7fdc-157">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f7fdc-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f7fdc-158">nein</span><span class="sxs-lookup"><span data-stu-id="f7fdc-158">no</span></span>        |
| [<span data-ttu-id="f7fdc-159">Shadermodell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f7fdc-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f7fdc-160">nein</span><span class="sxs-lookup"><span data-stu-id="f7fdc-160">no</span></span>        |
| [<span data-ttu-id="f7fdc-161">Shadermodell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f7fdc-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f7fdc-162">nein</span><span class="sxs-lookup"><span data-stu-id="f7fdc-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f7fdc-163">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f7fdc-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7fdc-164">Shadermodell 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f7fdc-164">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





