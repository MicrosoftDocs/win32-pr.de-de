---
title: sincos (sm4 - asm)
description: Komponentenweise sin(theta) und cos(theta) für theta im Bogenmaß.
ms.assetid: 81FDEC8F-2C1C-4C60-A6DA-699C798F8316
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c03118ff9a1fc2d958eaa6eb1a550a6dbf672a2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997017"
---
# <a name="sincos-sm4---asm"></a><span data-ttu-id="d59c7-103">sincos (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="d59c7-103">sincos (sm4 - asm)</span></span>

<span data-ttu-id="d59c7-104">Komponentenweise sin(theta) und cos(theta) für theta im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="d59c7-104">Component-wise sin(theta) and cos(theta) for theta in radians.</span></span>



| <span data-ttu-id="d59c7-105">sincos \[ \_ sat \] destSIN \[ \] .mask, destCOS \[ \] .mask, \[ - \] src0 abs \[ \_ \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="d59c7-105">sincos\[\_sat\] destSIN\[.mask\], destCOS\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------------|



 



| <span data-ttu-id="d59c7-106">Element</span><span class="sxs-lookup"><span data-stu-id="d59c7-106">Item</span></span>                                                                                               | <span data-ttu-id="d59c7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d59c7-107">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="d59c7-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*</span><span class="sxs-lookup"><span data-stu-id="d59c7-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*</span></span><br/> | <span data-ttu-id="d59c7-109">\[in \] Die Adresse von sin(*src0*), berechnet pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="d59c7-109">\[in\] The address of sin(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="d59c7-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*</span><span class="sxs-lookup"><span data-stu-id="d59c7-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*</span></span><br/> | <span data-ttu-id="d59c7-111">\[in \] Die Adresse von cos(*src0*), berechnet pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="d59c7-111">\[in\] The address of cos(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="d59c7-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d59c7-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                    | <span data-ttu-id="d59c7-113">\[in \] Die Komponenten, für die sin und cos berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="d59c7-113">\[in\] The components for which to compute sin and cos.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="d59c7-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d59c7-114">Remarks</span></span>

<span data-ttu-id="d59c7-115">Wenn das Ergebnis nicht benötigt wird, können Sie *destSIN* und *destCOS* als NULL angeben, anstatt ein Register anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d59c7-115">If the result is not needed, you can specify *destSIN* and *destCOS* as NULL instead of specifying a register.</span></span>

<span data-ttu-id="d59c7-116">Thetawerte können beliebige IEEE 32-Bit-Gleitkommawerte sein.</span><span class="sxs-lookup"><span data-stu-id="d59c7-116">Theta values can be any IEEE 32-bit floating point values.</span></span>

<span data-ttu-id="d59c7-117">Der maximale absolute Fehler beträgt 0,0008 im Intervall von -100 \* Pi bis +100 \* Pi.</span><span class="sxs-lookup"><span data-stu-id="d59c7-117">The maximum absolute error is 0.0008 in the interval from -100\*Pi to +100\*Pi.</span></span>

<span data-ttu-id="d59c7-118">Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Zahlenklassen erzielt werden.</span><span class="sxs-lookup"><span data-stu-id="d59c7-118">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="d59c7-119">F bedeutet endliche reale Zahl.</span><span class="sxs-lookup"><span data-stu-id="d59c7-119">F means finite-real number.</span></span>



| <span data-ttu-id="d59c7-120">**src**</span><span class="sxs-lookup"><span data-stu-id="d59c7-120">**src**</span></span>     | <span data-ttu-id="d59c7-121">**-inf**</span><span class="sxs-lookup"><span data-stu-id="d59c7-121">**-inf**</span></span> | <span data-ttu-id="d59c7-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="d59c7-122">**-F**</span></span>       | <span data-ttu-id="d59c7-123">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="d59c7-123">**-denorm**</span></span> | <span data-ttu-id="d59c7-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="d59c7-124">**-0**</span></span> | <span data-ttu-id="d59c7-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="d59c7-125">**+0**</span></span> | <span data-ttu-id="d59c7-126">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="d59c7-126">**+denorm**</span></span> | <span data-ttu-id="d59c7-127">**+F**</span><span class="sxs-lookup"><span data-stu-id="d59c7-127">**+F**</span></span>       | <span data-ttu-id="d59c7-128">**+inf**</span><span class="sxs-lookup"><span data-stu-id="d59c7-128">**+inf**</span></span> | <span data-ttu-id="d59c7-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="d59c7-129">**NaN**</span></span> |
|-------------|----------|--------------|-------------|--------|--------|-------------|--------------|----------|---------|
| <span data-ttu-id="d59c7-130">**destSIN**</span><span class="sxs-lookup"><span data-stu-id="d59c7-130">**destSIN**</span></span> | <span data-ttu-id="d59c7-131">NaN</span><span class="sxs-lookup"><span data-stu-id="d59c7-131">NaN</span></span>      | <span data-ttu-id="d59c7-132">\[-1 bis +1\]</span><span class="sxs-lookup"><span data-stu-id="d59c7-132">\[-1 to +1\]</span></span> | <span data-ttu-id="d59c7-133">-0</span><span class="sxs-lookup"><span data-stu-id="d59c7-133">-0</span></span>          | <span data-ttu-id="d59c7-134">-0</span><span class="sxs-lookup"><span data-stu-id="d59c7-134">-0</span></span>     | <span data-ttu-id="d59c7-135">+0</span><span class="sxs-lookup"><span data-stu-id="d59c7-135">+0</span></span>     | <span data-ttu-id="d59c7-136">+0</span><span class="sxs-lookup"><span data-stu-id="d59c7-136">+0</span></span>          | <span data-ttu-id="d59c7-137">\[-1 bis +1\]</span><span class="sxs-lookup"><span data-stu-id="d59c7-137">\[-1 to +1\]</span></span> | <span data-ttu-id="d59c7-138">NaN</span><span class="sxs-lookup"><span data-stu-id="d59c7-138">NaN</span></span>      | <span data-ttu-id="d59c7-139">NaN</span><span class="sxs-lookup"><span data-stu-id="d59c7-139">NaN</span></span>     |
| <span data-ttu-id="d59c7-140">**destCOS**</span><span class="sxs-lookup"><span data-stu-id="d59c7-140">**destCOS**</span></span> | <span data-ttu-id="d59c7-141">NaN</span><span class="sxs-lookup"><span data-stu-id="d59c7-141">NaN</span></span>      | <span data-ttu-id="d59c7-142">\[-1 bis +1\]</span><span class="sxs-lookup"><span data-stu-id="d59c7-142">\[-1 to +1\]</span></span> | <span data-ttu-id="d59c7-143">+1</span><span class="sxs-lookup"><span data-stu-id="d59c7-143">+1</span></span>          | <span data-ttu-id="d59c7-144">+1</span><span class="sxs-lookup"><span data-stu-id="d59c7-144">+1</span></span>     | <span data-ttu-id="d59c7-145">+1</span><span class="sxs-lookup"><span data-stu-id="d59c7-145">+1</span></span>     | <span data-ttu-id="d59c7-146">+1</span><span class="sxs-lookup"><span data-stu-id="d59c7-146">+1</span></span>          | <span data-ttu-id="d59c7-147">\[-1 bis +1\]</span><span class="sxs-lookup"><span data-stu-id="d59c7-147">\[-1 to +1\]</span></span> | <span data-ttu-id="d59c7-148">NaN</span><span class="sxs-lookup"><span data-stu-id="d59c7-148">NaN</span></span>      | <span data-ttu-id="d59c7-149">NaN</span><span class="sxs-lookup"><span data-stu-id="d59c7-149">NaN</span></span>     |



 

<span data-ttu-id="d59c7-150">Diese Anweisung gilt für die folgenden Shaderstufen:</span><span class="sxs-lookup"><span data-stu-id="d59c7-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d59c7-151">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="d59c7-151">Vertex Shader</span></span> | <span data-ttu-id="d59c7-152">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="d59c7-152">Geometry Shader</span></span> | <span data-ttu-id="d59c7-153">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="d59c7-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d59c7-154">x</span><span class="sxs-lookup"><span data-stu-id="d59c7-154">x</span></span>             | <span data-ttu-id="d59c7-155">x</span><span class="sxs-lookup"><span data-stu-id="d59c7-155">x</span></span>               | <span data-ttu-id="d59c7-156">x</span><span class="sxs-lookup"><span data-stu-id="d59c7-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d59c7-157">Shader-Mindestmodell</span><span class="sxs-lookup"><span data-stu-id="d59c7-157">Minimum Shader Model</span></span>

<span data-ttu-id="d59c7-158">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d59c7-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d59c7-159">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="d59c7-159">Shader Model</span></span>                                              | <span data-ttu-id="d59c7-160">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="d59c7-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d59c7-161">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="d59c7-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d59c7-162">ja</span><span class="sxs-lookup"><span data-stu-id="d59c7-162">yes</span></span>       |
| [<span data-ttu-id="d59c7-163">Shadermodell 4.1</span><span class="sxs-lookup"><span data-stu-id="d59c7-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d59c7-164">ja</span><span class="sxs-lookup"><span data-stu-id="d59c7-164">yes</span></span>       |
| [<span data-ttu-id="d59c7-165">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="d59c7-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d59c7-166">ja</span><span class="sxs-lookup"><span data-stu-id="d59c7-166">yes</span></span>       |
| [<span data-ttu-id="d59c7-167">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d59c7-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d59c7-168">nein</span><span class="sxs-lookup"><span data-stu-id="d59c7-168">no</span></span>        |
| [<span data-ttu-id="d59c7-169">Shadermodell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d59c7-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d59c7-170">nein</span><span class="sxs-lookup"><span data-stu-id="d59c7-170">no</span></span>        |
| [<span data-ttu-id="d59c7-171">Shadermodell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d59c7-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d59c7-172">nein</span><span class="sxs-lookup"><span data-stu-id="d59c7-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d59c7-173">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d59c7-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d59c7-174">Shadermodell 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d59c7-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





