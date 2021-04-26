---
title: rsq (sm4 - asm)
description: Komponentenweise reziprokische Quadratwurzel.
ms.assetid: CDA3C2DF-2793-4CE3-87CE-4E0AA945A1BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1528e9f187ff7d4fb6074d42a1c574686f3b22f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998167"
---
# <a name="rsq-sm4---asm"></a><span data-ttu-id="bb9ec-103">rsq (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="bb9ec-103">rsq (sm4 - asm)</span></span>

<span data-ttu-id="bb9ec-104">Komponentenweise reziprokische Quadratwurzel.</span><span class="sxs-lookup"><span data-stu-id="bb9ec-104">Component-wise reciprocal square root.</span></span>



| <span data-ttu-id="bb9ec-105">rsq \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="bb9ec-105">rsq\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="bb9ec-106">Element</span><span class="sxs-lookup"><span data-stu-id="bb9ec-106">Item</span></span>                                                            | <span data-ttu-id="bb9ec-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb9ec-107">Description</span></span>                                                                                      |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb9ec-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="bb9ec-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="bb9ec-109">\[in \] Enthält die Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="bb9ec-109">\[in\] Contains the results of the operation.</span></span><br/> <span data-ttu-id="bb9ec-110">*dest* = 1,0f /sqrt(*src0*)</span><span class="sxs-lookup"><span data-stu-id="bb9ec-110">*dest* = 1.0f / sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="bb9ec-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="bb9ec-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="bb9ec-112">\[in \] Die Komponenten für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="bb9ec-112">\[in\] The components for the operation.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="bb9ec-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bb9ec-113">Remarks</span></span>

<span data-ttu-id="bb9ec-114">Der maximale relative Fehler ist 2–21.</span><span class="sxs-lookup"><span data-stu-id="bb9ec-114">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="bb9ec-115">Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Zahlenklassen erzielt werden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt.</span><span class="sxs-lookup"><span data-stu-id="bb9ec-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="bb9ec-116">F bedeutet endliche reale Zahl.</span><span class="sxs-lookup"><span data-stu-id="bb9ec-116">F means finite-real number.</span></span>



| <span data-ttu-id="bb9ec-117">**src**</span><span class="sxs-lookup"><span data-stu-id="bb9ec-117">**src**</span></span>  | <span data-ttu-id="bb9ec-118">**-inf**</span><span class="sxs-lookup"><span data-stu-id="bb9ec-118">**-inf**</span></span> | <span data-ttu-id="bb9ec-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="bb9ec-119">**-F**</span></span> | <span data-ttu-id="bb9ec-120">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="bb9ec-120">**-denorm**</span></span> | <span data-ttu-id="bb9ec-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="bb9ec-121">**-0**</span></span> | <span data-ttu-id="bb9ec-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="bb9ec-122">**+0**</span></span> | <span data-ttu-id="bb9ec-123">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="bb9ec-123">**+denorm**</span></span> | <span data-ttu-id="bb9ec-124">**+F**</span><span class="sxs-lookup"><span data-stu-id="bb9ec-124">**+F**</span></span> | <span data-ttu-id="bb9ec-125">**+inf**</span><span class="sxs-lookup"><span data-stu-id="bb9ec-125">**+inf**</span></span> | <span data-ttu-id="bb9ec-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="bb9ec-126">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="bb9ec-127">**Dest**</span><span class="sxs-lookup"><span data-stu-id="bb9ec-127">**dest**</span></span> | <span data-ttu-id="bb9ec-128">NaN</span><span class="sxs-lookup"><span data-stu-id="bb9ec-128">NaN</span></span>      | <span data-ttu-id="bb9ec-129">NaN</span><span class="sxs-lookup"><span data-stu-id="bb9ec-129">NaN</span></span>    | <span data-ttu-id="bb9ec-130">-inf</span><span class="sxs-lookup"><span data-stu-id="bb9ec-130">-inf</span></span>        | <span data-ttu-id="bb9ec-131">-inf</span><span class="sxs-lookup"><span data-stu-id="bb9ec-131">-inf</span></span>   | <span data-ttu-id="bb9ec-132">+inf</span><span class="sxs-lookup"><span data-stu-id="bb9ec-132">+inf</span></span>   | <span data-ttu-id="bb9ec-133">+inf</span><span class="sxs-lookup"><span data-stu-id="bb9ec-133">+inf</span></span>        | <span data-ttu-id="bb9ec-134">+F</span><span class="sxs-lookup"><span data-stu-id="bb9ec-134">+F</span></span>     | <span data-ttu-id="bb9ec-135">+0</span><span class="sxs-lookup"><span data-stu-id="bb9ec-135">+0</span></span>       | <span data-ttu-id="bb9ec-136">NaN</span><span class="sxs-lookup"><span data-stu-id="bb9ec-136">NaN</span></span>     |



 

<span data-ttu-id="bb9ec-137">Diese Anweisung gilt für die folgenden Shaderstufen:</span><span class="sxs-lookup"><span data-stu-id="bb9ec-137">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bb9ec-138">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="bb9ec-138">Vertex Shader</span></span> | <span data-ttu-id="bb9ec-139">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="bb9ec-139">Geometry Shader</span></span> | <span data-ttu-id="bb9ec-140">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="bb9ec-140">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="bb9ec-141">x</span><span class="sxs-lookup"><span data-stu-id="bb9ec-141">x</span></span>             | <span data-ttu-id="bb9ec-142">x</span><span class="sxs-lookup"><span data-stu-id="bb9ec-142">x</span></span>               | <span data-ttu-id="bb9ec-143">x</span><span class="sxs-lookup"><span data-stu-id="bb9ec-143">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bb9ec-144">Shader-Mindestmodell</span><span class="sxs-lookup"><span data-stu-id="bb9ec-144">Minimum Shader Model</span></span>

<span data-ttu-id="bb9ec-145">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bb9ec-145">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bb9ec-146">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="bb9ec-146">Shader Model</span></span>                                              | <span data-ttu-id="bb9ec-147">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="bb9ec-147">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bb9ec-148">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="bb9ec-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bb9ec-149">ja</span><span class="sxs-lookup"><span data-stu-id="bb9ec-149">yes</span></span>       |
| [<span data-ttu-id="bb9ec-150">Shadermodell 4.1</span><span class="sxs-lookup"><span data-stu-id="bb9ec-150">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bb9ec-151">ja</span><span class="sxs-lookup"><span data-stu-id="bb9ec-151">yes</span></span>       |
| [<span data-ttu-id="bb9ec-152">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="bb9ec-152">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bb9ec-153">ja</span><span class="sxs-lookup"><span data-stu-id="bb9ec-153">yes</span></span>       |
| [<span data-ttu-id="bb9ec-154">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bb9ec-154">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bb9ec-155">nein</span><span class="sxs-lookup"><span data-stu-id="bb9ec-155">no</span></span>        |
| [<span data-ttu-id="bb9ec-156">Shadermodell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bb9ec-156">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bb9ec-157">nein</span><span class="sxs-lookup"><span data-stu-id="bb9ec-157">no</span></span>        |
| [<span data-ttu-id="bb9ec-158">Shadermodell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bb9ec-158">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bb9ec-159">nein</span><span class="sxs-lookup"><span data-stu-id="bb9ec-159">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bb9ec-160">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bb9ec-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb9ec-161">Shadermodell 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bb9ec-161">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





