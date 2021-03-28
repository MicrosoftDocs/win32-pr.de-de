---
title: RSQ (SM4-ASM)
description: Komponenten Weise wechselseitige Quadratwurzel.
ms.assetid: CDA3C2DF-2793-4CE3-87CE-4E0AA945A1BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc274f927151938be055150d5b17287f9be0004d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038358"
---
# <a name="rsq-sm4---asm"></a><span data-ttu-id="9bc6b-103">RSQ (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="9bc6b-103">rsq (sm4 - asm)</span></span>

<span data-ttu-id="9bc6b-104">Komponenten Weise wechselseitige Quadratwurzel.</span><span class="sxs-lookup"><span data-stu-id="9bc6b-104">Component-wise reciprocal square root.</span></span>



| <span data-ttu-id="9bc6b-105">RSQ \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="9bc6b-105">rsq\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="9bc6b-106">Element</span><span class="sxs-lookup"><span data-stu-id="9bc6b-106">Item</span></span>                                                            | <span data-ttu-id="9bc6b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9bc6b-107">Description</span></span>                                                                                      |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bc6b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9bc6b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9bc6b-109">\[in \] enthält die Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="9bc6b-109">\[in\] Contains the results of the operation.</span></span><br/> <span data-ttu-id="9bc6b-110">*dest* = 1.0 f/sqrt (*src0*)</span><span class="sxs-lookup"><span data-stu-id="9bc6b-110">*dest* = 1.0f / sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="9bc6b-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9bc6b-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9bc6b-112">\[in \] den Komponenten für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="9bc6b-112">\[in\] The components for the operation.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="9bc6b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9bc6b-113">Remarks</span></span>

<span data-ttu-id="9bc6b-114">Der maximale relative Fehler ist 2-21.</span><span class="sxs-lookup"><span data-stu-id="9bc6b-114">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="9bc6b-115">In der folgenden Tabelle werden die Ergebnisse angezeigt, die bei der Ausführung der Anweisung mit verschiedenen Klassen von Zahlen erzielt wurden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt</span><span class="sxs-lookup"><span data-stu-id="9bc6b-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="9bc6b-116">F bedeutet eine endliche reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="9bc6b-116">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="9bc6b-117">**src**</span><span class="sxs-lookup"><span data-stu-id="9bc6b-117">**src**</span></span>  | <span data-ttu-id="9bc6b-118">**-INF**</span><span class="sxs-lookup"><span data-stu-id="9bc6b-118">**-inf**</span></span> | <span data-ttu-id="9bc6b-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="9bc6b-119">**-F**</span></span> | <span data-ttu-id="9bc6b-120">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="9bc6b-120">**-denorm**</span></span> | <span data-ttu-id="9bc6b-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="9bc6b-121">**-0**</span></span> | <span data-ttu-id="9bc6b-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="9bc6b-122">**+0**</span></span> | <span data-ttu-id="9bc6b-123">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="9bc6b-123">**+denorm**</span></span> | <span data-ttu-id="9bc6b-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="9bc6b-124">**+F**</span></span> | <span data-ttu-id="9bc6b-125">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="9bc6b-125">**+inf**</span></span> | <span data-ttu-id="9bc6b-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="9bc6b-126">**NaN**</span></span> |
| <span data-ttu-id="9bc6b-127">**dest**</span><span class="sxs-lookup"><span data-stu-id="9bc6b-127">**dest**</span></span> | <span data-ttu-id="9bc6b-128">NaN</span><span class="sxs-lookup"><span data-stu-id="9bc6b-128">NaN</span></span>      | <span data-ttu-id="9bc6b-129">NaN</span><span class="sxs-lookup"><span data-stu-id="9bc6b-129">NaN</span></span>    | <span data-ttu-id="9bc6b-130">-inf</span><span class="sxs-lookup"><span data-stu-id="9bc6b-130">-inf</span></span>        | <span data-ttu-id="9bc6b-131">-inf</span><span class="sxs-lookup"><span data-stu-id="9bc6b-131">-inf</span></span>   | <span data-ttu-id="9bc6b-132">+inf</span><span class="sxs-lookup"><span data-stu-id="9bc6b-132">+inf</span></span>   | <span data-ttu-id="9bc6b-133">+inf</span><span class="sxs-lookup"><span data-stu-id="9bc6b-133">+inf</span></span>        | <span data-ttu-id="9bc6b-134">+ F</span><span class="sxs-lookup"><span data-stu-id="9bc6b-134">+F</span></span>     | <span data-ttu-id="9bc6b-135">+0</span><span class="sxs-lookup"><span data-stu-id="9bc6b-135">+0</span></span>       | <span data-ttu-id="9bc6b-136">NaN</span><span class="sxs-lookup"><span data-stu-id="9bc6b-136">NaN</span></span>     |



 

<span data-ttu-id="9bc6b-137">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="9bc6b-137">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9bc6b-138">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="9bc6b-138">Vertex Shader</span></span> | <span data-ttu-id="9bc6b-139">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="9bc6b-139">Geometry Shader</span></span> | <span data-ttu-id="9bc6b-140">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="9bc6b-140">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9bc6b-141">x</span><span class="sxs-lookup"><span data-stu-id="9bc6b-141">x</span></span>             | <span data-ttu-id="9bc6b-142">x</span><span class="sxs-lookup"><span data-stu-id="9bc6b-142">x</span></span>               | <span data-ttu-id="9bc6b-143">x</span><span class="sxs-lookup"><span data-stu-id="9bc6b-143">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9bc6b-144">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="9bc6b-144">Minimum Shader Model</span></span>

<span data-ttu-id="9bc6b-145">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9bc6b-145">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9bc6b-146">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="9bc6b-146">Shader Model</span></span>                                              | <span data-ttu-id="9bc6b-147">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="9bc6b-147">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9bc6b-148">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="9bc6b-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9bc6b-149">ja</span><span class="sxs-lookup"><span data-stu-id="9bc6b-149">yes</span></span>       |
| [<span data-ttu-id="9bc6b-150">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="9bc6b-150">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9bc6b-151">ja</span><span class="sxs-lookup"><span data-stu-id="9bc6b-151">yes</span></span>       |
| [<span data-ttu-id="9bc6b-152">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="9bc6b-152">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9bc6b-153">ja</span><span class="sxs-lookup"><span data-stu-id="9bc6b-153">yes</span></span>       |
| [<span data-ttu-id="9bc6b-154">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9bc6b-154">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9bc6b-155">nein</span><span class="sxs-lookup"><span data-stu-id="9bc6b-155">no</span></span>        |
| [<span data-ttu-id="9bc6b-156">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9bc6b-156">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9bc6b-157">nein</span><span class="sxs-lookup"><span data-stu-id="9bc6b-157">no</span></span>        |
| [<span data-ttu-id="9bc6b-158">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9bc6b-158">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9bc6b-159">nein</span><span class="sxs-lookup"><span data-stu-id="9bc6b-159">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9bc6b-160">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9bc6b-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bc6b-161">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9bc6b-161">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





