---
title: Log (SM4-ASM)
description: Komponenten weises Protokoll Basis 2.
ms.assetid: 6D28864A-C2BA-44AF-9E78-7C2B34F5E462
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf99949e278ca302543437da346188b690789604
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038342"
---
# <a name="log-sm4---asm"></a><span data-ttu-id="f7ba0-103">Log (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="f7ba0-103">log (sm4 - asm)</span></span>

<span data-ttu-id="f7ba0-104">Komponenten weises Protokoll Basis 2.</span><span class="sxs-lookup"><span data-stu-id="f7ba0-104">Component-wise log base 2.</span></span>



| <span data-ttu-id="f7ba0-105">log \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle</span><span class="sxs-lookup"><span data-stu-id="f7ba0-105">log\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle</span></span> |
|----------------------------------------------------------|



 



| <span data-ttu-id="f7ba0-106">Element</span><span class="sxs-lookup"><span data-stu-id="f7ba0-106">Item</span></span>                                                            | <span data-ttu-id="f7ba0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7ba0-107">Description</span></span>                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7ba0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="f7ba0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="f7ba0-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="f7ba0-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="f7ba0-110">dest = log2 (src0)</span><span class="sxs-lookup"><span data-stu-id="f7ba0-110">dest = log2(src0)</span></span><br/> |
| <span data-ttu-id="f7ba0-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f7ba0-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="f7ba0-112">\[im \] Wert für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f7ba0-112">\[in\] The value for the operation.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="f7ba0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7ba0-113">Remarks</span></span>

### <a name="restrictions"></a><span data-ttu-id="f7ba0-114">Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="f7ba0-114">Restrictions</span></span>

-   <span data-ttu-id="f7ba0-115">Folgt der Limit-Theorie.</span><span class="sxs-lookup"><span data-stu-id="f7ba0-115">Follows limit theory.</span></span>
-   <span data-ttu-id="f7ba0-116">Fehlertoleranz: Wenn *src0* \[ 0,5.. 2 ist \] , darf der Absolue-Fehler nicht größer als 2-21 sein.</span><span class="sxs-lookup"><span data-stu-id="f7ba0-116">Error tolerance: If *src0* is \[0.5..2\], absolue error must be no more than 2-21.</span></span> <span data-ttu-id="f7ba0-117">Wenn *src0* (0.. 0,5) oder (2.. + inf) ist \] , darf der relative Fehler nicht größer als 2-21 sein.</span><span class="sxs-lookup"><span data-stu-id="f7ba0-117">If *src0* is (0..0.5) or (2..+INF\], relative error must be no more than 2-21.</span></span>

<span data-ttu-id="f7ba0-118">In der folgenden Tabelle werden die Ergebnisse angezeigt, die bei der Ausführung der Anweisung mit verschiedenen Klassen von Zahlen erzielt wurden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt</span><span class="sxs-lookup"><span data-stu-id="f7ba0-118">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="f7ba0-119">F bedeutet eine endliche reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="f7ba0-119">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="f7ba0-120">**src**</span><span class="sxs-lookup"><span data-stu-id="f7ba0-120">**src**</span></span>  | <span data-ttu-id="f7ba0-121">**-INF**</span><span class="sxs-lookup"><span data-stu-id="f7ba0-121">**-inf**</span></span> | <span data-ttu-id="f7ba0-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="f7ba0-122">**-F**</span></span> | <span data-ttu-id="f7ba0-123">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="f7ba0-123">**-denorm**</span></span> | <span data-ttu-id="f7ba0-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="f7ba0-124">**-0**</span></span> | <span data-ttu-id="f7ba0-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="f7ba0-125">**+0**</span></span> | <span data-ttu-id="f7ba0-126">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="f7ba0-126">**+denorm**</span></span> | <span data-ttu-id="f7ba0-127">**+ F**</span><span class="sxs-lookup"><span data-stu-id="f7ba0-127">**+F**</span></span> | <span data-ttu-id="f7ba0-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="f7ba0-128">**+inf**</span></span> | <span data-ttu-id="f7ba0-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="f7ba0-129">**NaN**</span></span> |
| <span data-ttu-id="f7ba0-130">**dest**</span><span class="sxs-lookup"><span data-stu-id="f7ba0-130">**dest**</span></span> | <span data-ttu-id="f7ba0-131">NaN</span><span class="sxs-lookup"><span data-stu-id="f7ba0-131">NaN</span></span>      | <span data-ttu-id="f7ba0-132">NaN</span><span class="sxs-lookup"><span data-stu-id="f7ba0-132">NaN</span></span>    | <span data-ttu-id="f7ba0-133">-inf</span><span class="sxs-lookup"><span data-stu-id="f7ba0-133">-inf</span></span>        | <span data-ttu-id="f7ba0-134">-inf</span><span class="sxs-lookup"><span data-stu-id="f7ba0-134">-inf</span></span>   | <span data-ttu-id="f7ba0-135">-inf</span><span class="sxs-lookup"><span data-stu-id="f7ba0-135">-inf</span></span>   | <span data-ttu-id="f7ba0-136">-inf</span><span class="sxs-lookup"><span data-stu-id="f7ba0-136">-inf</span></span>        | <span data-ttu-id="f7ba0-137">F</span><span class="sxs-lookup"><span data-stu-id="f7ba0-137">F</span></span>      | <span data-ttu-id="f7ba0-138">+inf</span><span class="sxs-lookup"><span data-stu-id="f7ba0-138">+inf</span></span>     | <span data-ttu-id="f7ba0-139">NaN</span><span class="sxs-lookup"><span data-stu-id="f7ba0-139">NaN</span></span>     |



 

<span data-ttu-id="f7ba0-140">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="f7ba0-140">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f7ba0-141">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="f7ba0-141">Vertex Shader</span></span> | <span data-ttu-id="f7ba0-142">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="f7ba0-142">Geometry Shader</span></span> | <span data-ttu-id="f7ba0-143">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="f7ba0-143">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="f7ba0-144">x</span><span class="sxs-lookup"><span data-stu-id="f7ba0-144">x</span></span>             | <span data-ttu-id="f7ba0-145">x</span><span class="sxs-lookup"><span data-stu-id="f7ba0-145">x</span></span>               | <span data-ttu-id="f7ba0-146">x</span><span class="sxs-lookup"><span data-stu-id="f7ba0-146">x</span></span>            |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="f7ba0-147">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="f7ba0-147">Minimum Shader Model</span></span>

<span data-ttu-id="f7ba0-148">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f7ba0-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f7ba0-149">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="f7ba0-149">Shader Model</span></span>                                              | <span data-ttu-id="f7ba0-150">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="f7ba0-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f7ba0-151">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="f7ba0-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f7ba0-152">ja</span><span class="sxs-lookup"><span data-stu-id="f7ba0-152">yes</span></span>       |
| [<span data-ttu-id="f7ba0-153">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="f7ba0-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f7ba0-154">ja</span><span class="sxs-lookup"><span data-stu-id="f7ba0-154">yes</span></span>       |
| [<span data-ttu-id="f7ba0-155">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="f7ba0-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f7ba0-156">ja</span><span class="sxs-lookup"><span data-stu-id="f7ba0-156">yes</span></span>       |
| [<span data-ttu-id="f7ba0-157">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f7ba0-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f7ba0-158">nein</span><span class="sxs-lookup"><span data-stu-id="f7ba0-158">no</span></span>        |
| [<span data-ttu-id="f7ba0-159">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f7ba0-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f7ba0-160">nein</span><span class="sxs-lookup"><span data-stu-id="f7ba0-160">no</span></span>        |
| [<span data-ttu-id="f7ba0-161">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f7ba0-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f7ba0-162">nein</span><span class="sxs-lookup"><span data-stu-id="f7ba0-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f7ba0-163">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f7ba0-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7ba0-164">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f7ba0-164">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





