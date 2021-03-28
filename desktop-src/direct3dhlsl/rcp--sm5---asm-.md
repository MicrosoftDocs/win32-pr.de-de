---
title: rcp (SM5-ASM)
description: Komponenten weiser Wechsel.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbaa2ffc29a4c3373009d9dec1b895710186e67
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516514"
---
# <a name="rcp-sm5---asm"></a><span data-ttu-id="34f5e-103">rcp (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="34f5e-103">rcp (sm5 - asm)</span></span>

<span data-ttu-id="34f5e-104">Komponenten weiser Wechsel.</span><span class="sxs-lookup"><span data-stu-id="34f5e-104">Component-wise reciprocal.</span></span>



| <span data-ttu-id="34f5e-105">RCP \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="34f5e-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="34f5e-106">Element</span><span class="sxs-lookup"><span data-stu-id="34f5e-106">Item</span></span>                                                            | <span data-ttu-id="34f5e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34f5e-107">Description</span></span>                                                                         |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="34f5e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="34f5e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="34f5e-109">\[in \] der Adresse der Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="34f5e-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="34f5e-110">*dest*  =  **1.0 f**  /  *src0*.</span><span class="sxs-lookup"><span data-stu-id="34f5e-110">*dest* = **1.0f** / *src0*.</span></span><br/> |
| <span data-ttu-id="34f5e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="34f5e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="34f5e-112">\[in \] der Zahl, von der die gegenseitige übernommen wird.</span><span class="sxs-lookup"><span data-stu-id="34f5e-112">\[in\] The number to take the reciprocal of.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="34f5e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34f5e-113">Remarks</span></span>

<span data-ttu-id="34f5e-114">Verwenden Sie diese Anweisung für die gegenseitige geringere Genauigkeit, unabhängig von den strengen Anforderungen für die Teilung.</span><span class="sxs-lookup"><span data-stu-id="34f5e-114">Use this instruction for reduced precision reciprocal, independent of the strict requirements for divide.</span></span>

<span data-ttu-id="34f5e-115">Der maximale relative Fehler ist 2-21.</span><span class="sxs-lookup"><span data-stu-id="34f5e-115">Maximum relative error is 2-21.</span></span> <span data-ttu-id="34f5e-116">(Die Fehlertoleranz stimmt nur mit RSQ überein.)</span><span class="sxs-lookup"><span data-stu-id="34f5e-116">(The error tolerance just matches rsq)</span></span>

<span data-ttu-id="34f5e-117">In der folgenden Tabelle werden die Ergebnisse angezeigt, die beim Ausführen der Anweisung mit verschiedenen Klassen von Zahlen abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="34f5e-117">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



|        |          |        |             |        |        |             |        |          |         |
|--------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="34f5e-118">*src*</span><span class="sxs-lookup"><span data-stu-id="34f5e-118">*src*</span></span>  | <span data-ttu-id="34f5e-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="34f5e-119">**-inf**</span></span> | <span data-ttu-id="34f5e-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="34f5e-120">**-F**</span></span> | <span data-ttu-id="34f5e-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="34f5e-121">**-denorm**</span></span> | <span data-ttu-id="34f5e-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="34f5e-122">**-0**</span></span> | <span data-ttu-id="34f5e-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="34f5e-123">**+0**</span></span> | <span data-ttu-id="34f5e-124">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="34f5e-124">**+denorm**</span></span> | <span data-ttu-id="34f5e-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="34f5e-125">**+F**</span></span> | <span data-ttu-id="34f5e-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="34f5e-126">**+inf**</span></span> | <span data-ttu-id="34f5e-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="34f5e-127">**NaN**</span></span> |
| <span data-ttu-id="34f5e-128">*dest*</span><span class="sxs-lookup"><span data-stu-id="34f5e-128">*dest*</span></span> | <span data-ttu-id="34f5e-129">-0</span><span class="sxs-lookup"><span data-stu-id="34f5e-129">-0</span></span>       | <span data-ttu-id="34f5e-130">-F</span><span class="sxs-lookup"><span data-stu-id="34f5e-130">-F</span></span>     | <span data-ttu-id="34f5e-131">-inf</span><span class="sxs-lookup"><span data-stu-id="34f5e-131">-inf</span></span>        | <span data-ttu-id="34f5e-132">-inf</span><span class="sxs-lookup"><span data-stu-id="34f5e-132">-inf</span></span>   | <span data-ttu-id="34f5e-133">+inf</span><span class="sxs-lookup"><span data-stu-id="34f5e-133">+inf</span></span>   | <span data-ttu-id="34f5e-134">+inf</span><span class="sxs-lookup"><span data-stu-id="34f5e-134">+inf</span></span>        | <span data-ttu-id="34f5e-135">+ F</span><span class="sxs-lookup"><span data-stu-id="34f5e-135">+F</span></span>     | <span data-ttu-id="34f5e-136">+0</span><span class="sxs-lookup"><span data-stu-id="34f5e-136">+0</span></span>       | <span data-ttu-id="34f5e-137">NaN</span><span class="sxs-lookup"><span data-stu-id="34f5e-137">NaN</span></span>     |



 

<span data-ttu-id="34f5e-138">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="34f5e-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="34f5e-139">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="34f5e-139">Vertex</span></span> | <span data-ttu-id="34f5e-140">Hülle</span><span class="sxs-lookup"><span data-stu-id="34f5e-140">Hull</span></span> | <span data-ttu-id="34f5e-141">Domain</span><span class="sxs-lookup"><span data-stu-id="34f5e-141">Domain</span></span> | <span data-ttu-id="34f5e-142">Geometrie</span><span class="sxs-lookup"><span data-stu-id="34f5e-142">Geometry</span></span> | <span data-ttu-id="34f5e-143">Pixel</span><span class="sxs-lookup"><span data-stu-id="34f5e-143">Pixel</span></span> | <span data-ttu-id="34f5e-144">Compute</span><span class="sxs-lookup"><span data-stu-id="34f5e-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="34f5e-145">X</span><span class="sxs-lookup"><span data-stu-id="34f5e-145">X</span></span>      | <span data-ttu-id="34f5e-146">X</span><span class="sxs-lookup"><span data-stu-id="34f5e-146">X</span></span>    | <span data-ttu-id="34f5e-147">X</span><span class="sxs-lookup"><span data-stu-id="34f5e-147">X</span></span>      | <span data-ttu-id="34f5e-148">X</span><span class="sxs-lookup"><span data-stu-id="34f5e-148">X</span></span>        | <span data-ttu-id="34f5e-149">X</span><span class="sxs-lookup"><span data-stu-id="34f5e-149">X</span></span>     | <span data-ttu-id="34f5e-150">X</span><span class="sxs-lookup"><span data-stu-id="34f5e-150">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="34f5e-151">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="34f5e-151">Minimum Shader Model</span></span>

<span data-ttu-id="34f5e-152">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="34f5e-152">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="34f5e-153">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="34f5e-153">Shader Model</span></span>                                              | <span data-ttu-id="34f5e-154">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="34f5e-154">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="34f5e-155">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="34f5e-155">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="34f5e-156">ja</span><span class="sxs-lookup"><span data-stu-id="34f5e-156">yes</span></span>       |
| [<span data-ttu-id="34f5e-157">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="34f5e-157">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="34f5e-158">nein</span><span class="sxs-lookup"><span data-stu-id="34f5e-158">no</span></span>        |
| [<span data-ttu-id="34f5e-159">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="34f5e-159">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="34f5e-160">nein</span><span class="sxs-lookup"><span data-stu-id="34f5e-160">no</span></span>        |
| [<span data-ttu-id="34f5e-161">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="34f5e-161">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="34f5e-162">nein</span><span class="sxs-lookup"><span data-stu-id="34f5e-162">no</span></span>        |
| [<span data-ttu-id="34f5e-163">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="34f5e-163">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="34f5e-164">nein</span><span class="sxs-lookup"><span data-stu-id="34f5e-164">no</span></span>        |
| [<span data-ttu-id="34f5e-165">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="34f5e-165">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="34f5e-166">nein</span><span class="sxs-lookup"><span data-stu-id="34f5e-166">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="34f5e-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="34f5e-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34f5e-168">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="34f5e-168">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





