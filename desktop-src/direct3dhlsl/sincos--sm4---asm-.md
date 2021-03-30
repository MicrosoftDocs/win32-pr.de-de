---
title: SinCos (SM4-ASM)
description: Komponentenweise Sin (urta) und cos (-TA) für die TA im Bogenmaße.
ms.assetid: 81FDEC8F-2C1C-4C60-A6DA-699C798F8316
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2dd8fc3b011758f071cdcd273e34eb8a7f6421f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104992991"
---
# <a name="sincos-sm4---asm"></a><span data-ttu-id="47f01-103">SinCos (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="47f01-103">sincos (sm4 - asm)</span></span>

<span data-ttu-id="47f01-104">Komponentenweise Sin (urta) und cos (-TA) für die TA im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="47f01-104">Component-wise sin(theta) and cos(theta) for theta in radians.</span></span>



| <span data-ttu-id="47f01-105">SinCos \[ \_ Sat \] destsin \[ . mask \] , destcos \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="47f01-105">sincos\[\_sat\] destSIN\[.mask\], destCOS\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------------|



 



| <span data-ttu-id="47f01-106">Element</span><span class="sxs-lookup"><span data-stu-id="47f01-106">Item</span></span>                                                                                               | <span data-ttu-id="47f01-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47f01-107">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="47f01-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destsin*</span><span class="sxs-lookup"><span data-stu-id="47f01-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*</span></span><br/> | <span data-ttu-id="47f01-109">\[in \] der Adresse von Sin (*src0*), berechnet pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="47f01-109">\[in\] The address of sin(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="47f01-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destcos*</span><span class="sxs-lookup"><span data-stu-id="47f01-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*</span></span><br/> | <span data-ttu-id="47f01-111">\[in \] der Adresse von cos (*src0*), berechnet pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="47f01-111">\[in\] The address of cos(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="47f01-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="47f01-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                    | <span data-ttu-id="47f01-113">\[in \] den Komponenten, für die Sin und COS berechnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="47f01-113">\[in\] The components for which to compute sin and cos.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="47f01-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47f01-114">Remarks</span></span>

<span data-ttu-id="47f01-115">Wenn das Ergebnis nicht benötigt wird, können Sie *destsin* und *destcos* als NULL angeben, anstatt ein Register anzugeben.</span><span class="sxs-lookup"><span data-stu-id="47f01-115">If the result is not needed, you can specify *destSIN* and *destCOS* as NULL instead of specifying a register.</span></span>

<span data-ttu-id="47f01-116">Bei den Metrikwerten kann es sich um beliebige IEEE 32-Bit-Gleit Komma Werte handeln.</span><span class="sxs-lookup"><span data-stu-id="47f01-116">Theta values can be any IEEE 32-bit floating point values.</span></span>

<span data-ttu-id="47f01-117">Der absolute absolute Fehler ist 0,0008 im Intervall von-100 \* Pi bis + 100 \* Pi.</span><span class="sxs-lookup"><span data-stu-id="47f01-117">The maximum absolute error is 0.0008 in the interval from -100\*Pi to +100\*Pi.</span></span>

<span data-ttu-id="47f01-118">In der folgenden Tabelle werden die Ergebnisse angezeigt, die beim Ausführen der Anweisung mit verschiedenen Klassen von Zahlen abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="47f01-118">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="47f01-119">F bedeutet eine endliche reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="47f01-119">F means finite-real number.</span></span>



|             |          |              |             |        |        |             |              |          |         |
|-------------|----------|--------------|-------------|--------|--------|-------------|--------------|----------|---------|
| <span data-ttu-id="47f01-120">**src**</span><span class="sxs-lookup"><span data-stu-id="47f01-120">**src**</span></span>     | <span data-ttu-id="47f01-121">**-INF**</span><span class="sxs-lookup"><span data-stu-id="47f01-121">**-inf**</span></span> | <span data-ttu-id="47f01-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="47f01-122">**-F**</span></span>       | <span data-ttu-id="47f01-123">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="47f01-123">**-denorm**</span></span> | <span data-ttu-id="47f01-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="47f01-124">**-0**</span></span> | <span data-ttu-id="47f01-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="47f01-125">**+0**</span></span> | <span data-ttu-id="47f01-126">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="47f01-126">**+denorm**</span></span> | <span data-ttu-id="47f01-127">**+ F**</span><span class="sxs-lookup"><span data-stu-id="47f01-127">**+F**</span></span>       | <span data-ttu-id="47f01-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="47f01-128">**+inf**</span></span> | <span data-ttu-id="47f01-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="47f01-129">**NaN**</span></span> |
| <span data-ttu-id="47f01-130">**destsin**</span><span class="sxs-lookup"><span data-stu-id="47f01-130">**destSIN**</span></span> | <span data-ttu-id="47f01-131">NaN</span><span class="sxs-lookup"><span data-stu-id="47f01-131">NaN</span></span>      | <span data-ttu-id="47f01-132">\[-1 bis + 1\]</span><span class="sxs-lookup"><span data-stu-id="47f01-132">\[-1 to +1\]</span></span> | <span data-ttu-id="47f01-133">-0</span><span class="sxs-lookup"><span data-stu-id="47f01-133">-0</span></span>          | <span data-ttu-id="47f01-134">-0</span><span class="sxs-lookup"><span data-stu-id="47f01-134">-0</span></span>     | <span data-ttu-id="47f01-135">+0</span><span class="sxs-lookup"><span data-stu-id="47f01-135">+0</span></span>     | <span data-ttu-id="47f01-136">+0</span><span class="sxs-lookup"><span data-stu-id="47f01-136">+0</span></span>          | <span data-ttu-id="47f01-137">\[-1 bis + 1\]</span><span class="sxs-lookup"><span data-stu-id="47f01-137">\[-1 to +1\]</span></span> | <span data-ttu-id="47f01-138">NaN</span><span class="sxs-lookup"><span data-stu-id="47f01-138">NaN</span></span>      | <span data-ttu-id="47f01-139">NaN</span><span class="sxs-lookup"><span data-stu-id="47f01-139">NaN</span></span>     |
| <span data-ttu-id="47f01-140">**destcos**</span><span class="sxs-lookup"><span data-stu-id="47f01-140">**destCOS**</span></span> | <span data-ttu-id="47f01-141">NaN</span><span class="sxs-lookup"><span data-stu-id="47f01-141">NaN</span></span>      | <span data-ttu-id="47f01-142">\[-1 bis + 1\]</span><span class="sxs-lookup"><span data-stu-id="47f01-142">\[-1 to +1\]</span></span> | <span data-ttu-id="47f01-143">+1</span><span class="sxs-lookup"><span data-stu-id="47f01-143">+1</span></span>          | <span data-ttu-id="47f01-144">+1</span><span class="sxs-lookup"><span data-stu-id="47f01-144">+1</span></span>     | <span data-ttu-id="47f01-145">+1</span><span class="sxs-lookup"><span data-stu-id="47f01-145">+1</span></span>     | <span data-ttu-id="47f01-146">+1</span><span class="sxs-lookup"><span data-stu-id="47f01-146">+1</span></span>          | <span data-ttu-id="47f01-147">\[-1 bis + 1\]</span><span class="sxs-lookup"><span data-stu-id="47f01-147">\[-1 to +1\]</span></span> | <span data-ttu-id="47f01-148">NaN</span><span class="sxs-lookup"><span data-stu-id="47f01-148">NaN</span></span>      | <span data-ttu-id="47f01-149">NaN</span><span class="sxs-lookup"><span data-stu-id="47f01-149">NaN</span></span>     |



 

<span data-ttu-id="47f01-150">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="47f01-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="47f01-151">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="47f01-151">Vertex Shader</span></span> | <span data-ttu-id="47f01-152">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="47f01-152">Geometry Shader</span></span> | <span data-ttu-id="47f01-153">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="47f01-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="47f01-154">x</span><span class="sxs-lookup"><span data-stu-id="47f01-154">x</span></span>             | <span data-ttu-id="47f01-155">x</span><span class="sxs-lookup"><span data-stu-id="47f01-155">x</span></span>               | <span data-ttu-id="47f01-156">x</span><span class="sxs-lookup"><span data-stu-id="47f01-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="47f01-157">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="47f01-157">Minimum Shader Model</span></span>

<span data-ttu-id="47f01-158">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="47f01-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="47f01-159">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="47f01-159">Shader Model</span></span>                                              | <span data-ttu-id="47f01-160">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="47f01-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="47f01-161">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="47f01-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="47f01-162">ja</span><span class="sxs-lookup"><span data-stu-id="47f01-162">yes</span></span>       |
| [<span data-ttu-id="47f01-163">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="47f01-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="47f01-164">ja</span><span class="sxs-lookup"><span data-stu-id="47f01-164">yes</span></span>       |
| [<span data-ttu-id="47f01-165">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="47f01-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="47f01-166">ja</span><span class="sxs-lookup"><span data-stu-id="47f01-166">yes</span></span>       |
| [<span data-ttu-id="47f01-167">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47f01-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="47f01-168">nein</span><span class="sxs-lookup"><span data-stu-id="47f01-168">no</span></span>        |
| [<span data-ttu-id="47f01-169">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47f01-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="47f01-170">nein</span><span class="sxs-lookup"><span data-stu-id="47f01-170">no</span></span>        |
| [<span data-ttu-id="47f01-171">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47f01-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="47f01-172">nein</span><span class="sxs-lookup"><span data-stu-id="47f01-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="47f01-173">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="47f01-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47f01-174">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47f01-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





