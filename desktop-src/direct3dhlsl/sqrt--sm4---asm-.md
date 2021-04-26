---
title: sqrt (sm4 - asm)
description: Komponentenweise Quadratwurzel.
ms.assetid: B860D656-7F01-484F-909F-A5C9A61C52C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 628601e0a3a78784a5fd1a089ef7608a0cf9ca05
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996607"
---
# <a name="sqrt-sm4---asm"></a><span data-ttu-id="75258-103">sqrt (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="75258-103">sqrt (sm4 - asm)</span></span>

<span data-ttu-id="75258-104">Komponentenweise Quadratwurzel.</span><span class="sxs-lookup"><span data-stu-id="75258-104">Component-wise square root.</span></span>



| <span data-ttu-id="75258-105">sqrt \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="75258-105">sqrt\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="75258-106">Element</span><span class="sxs-lookup"><span data-stu-id="75258-106">Item</span></span>                                                            | <span data-ttu-id="75258-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75258-107">Description</span></span>                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="75258-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="75258-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="75258-109">\[in \] Das Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="75258-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="75258-110">*dest* = sqrt(*src0*)</span><span class="sxs-lookup"><span data-stu-id="75258-110">*dest* = sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="75258-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="75258-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="75258-112">\[in \] Die Komponenten, für die die Quadratwurzel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="75258-112">\[in\] The components for which to take the square root.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="75258-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="75258-113">Remarks</span></span>

<span data-ttu-id="75258-114">Die Genauigkeit beträgt 1 ulp.</span><span class="sxs-lookup"><span data-stu-id="75258-114">Precision is 1 ulp.</span></span>

<span data-ttu-id="75258-115">Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Zahlenklassen erzielt werden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt.</span><span class="sxs-lookup"><span data-stu-id="75258-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="75258-116">F bedeutet endliche reale Zahl.</span><span class="sxs-lookup"><span data-stu-id="75258-116">F means finite-real number.</span></span>



|          | <span data-ttu-id="75258-117">**-inf**</span><span class="sxs-lookup"><span data-stu-id="75258-117">**-inf**</span></span> | <span data-ttu-id="75258-118">**-F**</span><span class="sxs-lookup"><span data-stu-id="75258-118">**-F**</span></span> | <span data-ttu-id="75258-119">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="75258-119">**-denorm**</span></span> | <span data-ttu-id="75258-120">**-0**</span><span class="sxs-lookup"><span data-stu-id="75258-120">**-0**</span></span> | <span data-ttu-id="75258-121">**+0**</span><span class="sxs-lookup"><span data-stu-id="75258-121">**+0**</span></span> | <span data-ttu-id="75258-122">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="75258-122">**+denorm**</span></span> | <span data-ttu-id="75258-123">**+F**</span><span class="sxs-lookup"><span data-stu-id="75258-123">**+F**</span></span> | <span data-ttu-id="75258-124">**+inf**</span><span class="sxs-lookup"><span data-stu-id="75258-124">**+inf**</span></span> | <span data-ttu-id="75258-125">**NaN**</span><span class="sxs-lookup"><span data-stu-id="75258-125">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="75258-126">**Dest**</span><span class="sxs-lookup"><span data-stu-id="75258-126">**dest**</span></span> | <span data-ttu-id="75258-127">NaN</span><span class="sxs-lookup"><span data-stu-id="75258-127">NaN</span></span>      | <span data-ttu-id="75258-128">NaN</span><span class="sxs-lookup"><span data-stu-id="75258-128">NaN</span></span>    | <span data-ttu-id="75258-129">-0</span><span class="sxs-lookup"><span data-stu-id="75258-129">-0</span></span>          | <span data-ttu-id="75258-130">-0</span><span class="sxs-lookup"><span data-stu-id="75258-130">-0</span></span>     | <span data-ttu-id="75258-131">+0</span><span class="sxs-lookup"><span data-stu-id="75258-131">+0</span></span>     | <span data-ttu-id="75258-132">+0</span><span class="sxs-lookup"><span data-stu-id="75258-132">+0</span></span>          | <span data-ttu-id="75258-133">+F</span><span class="sxs-lookup"><span data-stu-id="75258-133">+F</span></span>     | <span data-ttu-id="75258-134">+inf</span><span class="sxs-lookup"><span data-stu-id="75258-134">+inf</span></span>     | <span data-ttu-id="75258-135">NaN</span><span class="sxs-lookup"><span data-stu-id="75258-135">NaN</span></span>     |



 

<span data-ttu-id="75258-136">Diese Anweisung gilt für die folgenden Shaderstufen:</span><span class="sxs-lookup"><span data-stu-id="75258-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="75258-137">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="75258-137">Vertex Shader</span></span> | <span data-ttu-id="75258-138">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="75258-138">Geometry Shader</span></span> | <span data-ttu-id="75258-139">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="75258-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="75258-140">x</span><span class="sxs-lookup"><span data-stu-id="75258-140">x</span></span>             | <span data-ttu-id="75258-141">x</span><span class="sxs-lookup"><span data-stu-id="75258-141">x</span></span>               | <span data-ttu-id="75258-142">x</span><span class="sxs-lookup"><span data-stu-id="75258-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="75258-143">Shader-Mindestmodell</span><span class="sxs-lookup"><span data-stu-id="75258-143">Minimum Shader Model</span></span>

<span data-ttu-id="75258-144">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="75258-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="75258-145">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="75258-145">Shader Model</span></span>                                              | <span data-ttu-id="75258-146">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="75258-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="75258-147">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="75258-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="75258-148">ja</span><span class="sxs-lookup"><span data-stu-id="75258-148">yes</span></span>       |
| [<span data-ttu-id="75258-149">Shadermodell 4.1</span><span class="sxs-lookup"><span data-stu-id="75258-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="75258-150">ja</span><span class="sxs-lookup"><span data-stu-id="75258-150">yes</span></span>       |
| [<span data-ttu-id="75258-151">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="75258-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="75258-152">ja</span><span class="sxs-lookup"><span data-stu-id="75258-152">yes</span></span>       |
| [<span data-ttu-id="75258-153">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="75258-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="75258-154">nein</span><span class="sxs-lookup"><span data-stu-id="75258-154">no</span></span>        |
| [<span data-ttu-id="75258-155">Shadermodell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="75258-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="75258-156">nein</span><span class="sxs-lookup"><span data-stu-id="75258-156">no</span></span>        |
| [<span data-ttu-id="75258-157">Shadermodell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="75258-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="75258-158">nein</span><span class="sxs-lookup"><span data-stu-id="75258-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="75258-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="75258-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75258-160">Shadermodell 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="75258-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





