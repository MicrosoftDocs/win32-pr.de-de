---
title: rcp (sm5 - asm)
description: Komponentenweise reziprok.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa37499a981bae86333b071c2e96a37ccb8ac1a6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998247"
---
# <a name="rcp-sm5---asm"></a><span data-ttu-id="6cd91-103">rcp (sm5 - asm)</span><span class="sxs-lookup"><span data-stu-id="6cd91-103">rcp (sm5 - asm)</span></span>

<span data-ttu-id="6cd91-104">Komponentenweise reziprok.</span><span class="sxs-lookup"><span data-stu-id="6cd91-104">Component-wise reciprocal.</span></span>



| <span data-ttu-id="6cd91-105">rcp \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="6cd91-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="6cd91-106">Element</span><span class="sxs-lookup"><span data-stu-id="6cd91-106">Item</span></span>                                                            | <span data-ttu-id="6cd91-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6cd91-107">Description</span></span>                                                                         |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6cd91-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="6cd91-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="6cd91-109">\[in \] Die Adresse der Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="6cd91-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="6cd91-110">*dest*  =  **1.0f**  /  *src0*.</span><span class="sxs-lookup"><span data-stu-id="6cd91-110">*dest* = **1.0f** / *src0*.</span></span><br/> |
| <span data-ttu-id="6cd91-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6cd91-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="6cd91-112">\[in \] Die Zahl, von der der Kehrwert annimmt wird.</span><span class="sxs-lookup"><span data-stu-id="6cd91-112">\[in\] The number to take the reciprocal of.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="6cd91-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6cd91-113">Remarks</span></span>

<span data-ttu-id="6cd91-114">Verwenden Sie diese Anweisung, um die Genauigkeit des Kehrwerts zu verringern, unabhängig von den strengen Anforderungen für die Division.</span><span class="sxs-lookup"><span data-stu-id="6cd91-114">Use this instruction for reduced precision reciprocal, independent of the strict requirements for divide.</span></span>

<span data-ttu-id="6cd91-115">Der maximale relative Fehler ist 2–21.</span><span class="sxs-lookup"><span data-stu-id="6cd91-115">Maximum relative error is 2-21.</span></span> <span data-ttu-id="6cd91-116">(Die Fehlertoleranz stimmt nur mit rsq überein))</span><span class="sxs-lookup"><span data-stu-id="6cd91-116">(The error tolerance just matches rsq)</span></span>

<span data-ttu-id="6cd91-117">Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Zahlenklassen erzielt werden.</span><span class="sxs-lookup"><span data-stu-id="6cd91-117">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



| <span data-ttu-id="6cd91-118">*src*</span><span class="sxs-lookup"><span data-stu-id="6cd91-118">*src*</span></span>  | <span data-ttu-id="6cd91-119">**-inf**</span><span class="sxs-lookup"><span data-stu-id="6cd91-119">**-inf**</span></span> | <span data-ttu-id="6cd91-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="6cd91-120">**-F**</span></span> | <span data-ttu-id="6cd91-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="6cd91-121">**-denorm**</span></span> | <span data-ttu-id="6cd91-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="6cd91-122">**-0**</span></span> | <span data-ttu-id="6cd91-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="6cd91-123">**+0**</span></span> | <span data-ttu-id="6cd91-124">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="6cd91-124">**+denorm**</span></span> | <span data-ttu-id="6cd91-125">**+F**</span><span class="sxs-lookup"><span data-stu-id="6cd91-125">**+F**</span></span> | <span data-ttu-id="6cd91-126">**+inf**</span><span class="sxs-lookup"><span data-stu-id="6cd91-126">**+inf**</span></span> | <span data-ttu-id="6cd91-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="6cd91-127">**NaN**</span></span> |
|--------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="6cd91-128">*Dest*</span><span class="sxs-lookup"><span data-stu-id="6cd91-128">*dest*</span></span> | <span data-ttu-id="6cd91-129">-0</span><span class="sxs-lookup"><span data-stu-id="6cd91-129">-0</span></span>       | <span data-ttu-id="6cd91-130">-F</span><span class="sxs-lookup"><span data-stu-id="6cd91-130">-F</span></span>     | <span data-ttu-id="6cd91-131">-inf</span><span class="sxs-lookup"><span data-stu-id="6cd91-131">-inf</span></span>        | <span data-ttu-id="6cd91-132">-inf</span><span class="sxs-lookup"><span data-stu-id="6cd91-132">-inf</span></span>   | <span data-ttu-id="6cd91-133">+inf</span><span class="sxs-lookup"><span data-stu-id="6cd91-133">+inf</span></span>   | <span data-ttu-id="6cd91-134">+inf</span><span class="sxs-lookup"><span data-stu-id="6cd91-134">+inf</span></span>        | <span data-ttu-id="6cd91-135">+F</span><span class="sxs-lookup"><span data-stu-id="6cd91-135">+F</span></span>     | <span data-ttu-id="6cd91-136">+0</span><span class="sxs-lookup"><span data-stu-id="6cd91-136">+0</span></span>       | <span data-ttu-id="6cd91-137">NaN</span><span class="sxs-lookup"><span data-stu-id="6cd91-137">NaN</span></span>     |



 

<span data-ttu-id="6cd91-138">Diese Anweisung gilt für die folgenden Shaderstufen:</span><span class="sxs-lookup"><span data-stu-id="6cd91-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6cd91-139">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="6cd91-139">Vertex</span></span> | <span data-ttu-id="6cd91-140">Rumpf</span><span class="sxs-lookup"><span data-stu-id="6cd91-140">Hull</span></span> | <span data-ttu-id="6cd91-141">Domain</span><span class="sxs-lookup"><span data-stu-id="6cd91-141">Domain</span></span> | <span data-ttu-id="6cd91-142">Geometrie</span><span class="sxs-lookup"><span data-stu-id="6cd91-142">Geometry</span></span> | <span data-ttu-id="6cd91-143">Pixel</span><span class="sxs-lookup"><span data-stu-id="6cd91-143">Pixel</span></span> | <span data-ttu-id="6cd91-144">Compute</span><span class="sxs-lookup"><span data-stu-id="6cd91-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6cd91-145">X</span><span class="sxs-lookup"><span data-stu-id="6cd91-145">X</span></span>      | <span data-ttu-id="6cd91-146">X</span><span class="sxs-lookup"><span data-stu-id="6cd91-146">X</span></span>    | <span data-ttu-id="6cd91-147">X</span><span class="sxs-lookup"><span data-stu-id="6cd91-147">X</span></span>      | <span data-ttu-id="6cd91-148">X</span><span class="sxs-lookup"><span data-stu-id="6cd91-148">X</span></span>        | <span data-ttu-id="6cd91-149">X</span><span class="sxs-lookup"><span data-stu-id="6cd91-149">X</span></span>     | <span data-ttu-id="6cd91-150">X</span><span class="sxs-lookup"><span data-stu-id="6cd91-150">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6cd91-151">Minimales Shadermodell</span><span class="sxs-lookup"><span data-stu-id="6cd91-151">Minimum Shader Model</span></span>

<span data-ttu-id="6cd91-152">Diese Anweisung wird in den folgenden Shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="6cd91-152">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6cd91-153">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="6cd91-153">Shader Model</span></span>                                              | <span data-ttu-id="6cd91-154">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="6cd91-154">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6cd91-155">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="6cd91-155">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6cd91-156">ja</span><span class="sxs-lookup"><span data-stu-id="6cd91-156">yes</span></span>       |
| [<span data-ttu-id="6cd91-157">Shadermodell 4.1</span><span class="sxs-lookup"><span data-stu-id="6cd91-157">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6cd91-158">nein</span><span class="sxs-lookup"><span data-stu-id="6cd91-158">no</span></span>        |
| [<span data-ttu-id="6cd91-159">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="6cd91-159">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6cd91-160">nein</span><span class="sxs-lookup"><span data-stu-id="6cd91-160">no</span></span>        |
| [<span data-ttu-id="6cd91-161">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6cd91-161">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6cd91-162">nein</span><span class="sxs-lookup"><span data-stu-id="6cd91-162">no</span></span>        |
| [<span data-ttu-id="6cd91-163">Shadermodell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6cd91-163">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6cd91-164">nein</span><span class="sxs-lookup"><span data-stu-id="6cd91-164">no</span></span>        |
| [<span data-ttu-id="6cd91-165">Shadermodell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6cd91-165">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6cd91-166">nein</span><span class="sxs-lookup"><span data-stu-id="6cd91-166">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6cd91-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6cd91-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cd91-168">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6cd91-168">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





