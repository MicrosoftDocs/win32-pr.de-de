---
title: round_ne (sm4 – asm)
description: Gleitkommagerundet auf ganzzahligen Gleitkommawert. | round_ne (sm4 – asm)
ms.assetid: 2D1A0786-F7DB-4D69-9F56-82ECD1EE7ABA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f0efb2ff10b75e50ec05847dd25aa8448c760c7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993927"
---
# <a name="round_ne-sm4---asm"></a><span data-ttu-id="bfa74-104">round \_ ne (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="bfa74-104">round\_ne (sm4 - asm)</span></span>

<span data-ttu-id="bfa74-105">Gleitkommagerundet auf ganzzahligen Gleitkommawert.</span><span class="sxs-lookup"><span data-stu-id="bfa74-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="bfa74-106">round \_ ne \[ \_ sat \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="bfa74-106">round\_ne\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="bfa74-107">Element</span><span class="sxs-lookup"><span data-stu-id="bfa74-107">Item</span></span>                                                            | <span data-ttu-id="bfa74-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bfa74-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="bfa74-109"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="bfa74-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="bfa74-110">\[in \] Die Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="bfa74-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="bfa74-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="bfa74-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="bfa74-112">\[in \] Die Komponenten im Vorgang.</span><span class="sxs-lookup"><span data-stu-id="bfa74-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="bfa74-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bfa74-113">Remarks</span></span>

<span data-ttu-id="bfa74-114">Diese Anweisung führt eine komponentenweise Gleitkommarunde der Werte in *src0* aus und schreibt ganzzahlige Gleitkommawerte in *dest*.</span><span class="sxs-lookup"><span data-stu-id="bfa74-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span> <span data-ttu-id="bfa74-115">**round \_ ne** rundet auf die nächste Gerade.</span><span class="sxs-lookup"><span data-stu-id="bfa74-115">**round\_ne** rounds towards nearest even.</span></span>

<span data-ttu-id="bfa74-116">Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Zahlenklassen erzielt werden.</span><span class="sxs-lookup"><span data-stu-id="bfa74-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="bfa74-117">F bedeutet endliche reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="bfa74-117">F means finite-real number.</span></span>



| <span data-ttu-id="bfa74-118">**src**</span><span class="sxs-lookup"><span data-stu-id="bfa74-118">**src**</span></span>  | <span data-ttu-id="bfa74-119">**-inf**</span><span class="sxs-lookup"><span data-stu-id="bfa74-119">**-inf**</span></span> | <span data-ttu-id="bfa74-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="bfa74-120">**-F**</span></span> | <span data-ttu-id="bfa74-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="bfa74-121">**-denorm**</span></span> | <span data-ttu-id="bfa74-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="bfa74-122">**-0**</span></span> | <span data-ttu-id="bfa74-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="bfa74-123">**+0**</span></span> | <span data-ttu-id="bfa74-124">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="bfa74-124">**+denorm**</span></span> | <span data-ttu-id="bfa74-125">**+F**</span><span class="sxs-lookup"><span data-stu-id="bfa74-125">**+F**</span></span> | <span data-ttu-id="bfa74-126">**+inf**</span><span class="sxs-lookup"><span data-stu-id="bfa74-126">**+inf**</span></span> | <span data-ttu-id="bfa74-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="bfa74-127">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="bfa74-128">**Dest**</span><span class="sxs-lookup"><span data-stu-id="bfa74-128">**dest**</span></span> | <span data-ttu-id="bfa74-129">-inf</span><span class="sxs-lookup"><span data-stu-id="bfa74-129">-inf</span></span>     | <span data-ttu-id="bfa74-130">-F</span><span class="sxs-lookup"><span data-stu-id="bfa74-130">-F</span></span>     | <span data-ttu-id="bfa74-131">-0</span><span class="sxs-lookup"><span data-stu-id="bfa74-131">-0</span></span>          | <span data-ttu-id="bfa74-132">-0</span><span class="sxs-lookup"><span data-stu-id="bfa74-132">-0</span></span>     | <span data-ttu-id="bfa74-133">+0</span><span class="sxs-lookup"><span data-stu-id="bfa74-133">+0</span></span>     | <span data-ttu-id="bfa74-134">+0</span><span class="sxs-lookup"><span data-stu-id="bfa74-134">+0</span></span>          | <span data-ttu-id="bfa74-135">+F</span><span class="sxs-lookup"><span data-stu-id="bfa74-135">+F</span></span>     | <span data-ttu-id="bfa74-136">+inf</span><span class="sxs-lookup"><span data-stu-id="bfa74-136">+inf</span></span>     | <span data-ttu-id="bfa74-137">NaN</span><span class="sxs-lookup"><span data-stu-id="bfa74-137">NaN</span></span>     |



 

<span data-ttu-id="bfa74-138">Diese Anweisung gilt für die folgenden Shaderstufen:</span><span class="sxs-lookup"><span data-stu-id="bfa74-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bfa74-139">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="bfa74-139">Vertex Shader</span></span> | <span data-ttu-id="bfa74-140">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="bfa74-140">Geometry Shader</span></span> | <span data-ttu-id="bfa74-141">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="bfa74-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="bfa74-142">x</span><span class="sxs-lookup"><span data-stu-id="bfa74-142">x</span></span>             | <span data-ttu-id="bfa74-143">x</span><span class="sxs-lookup"><span data-stu-id="bfa74-143">x</span></span>               | <span data-ttu-id="bfa74-144">x</span><span class="sxs-lookup"><span data-stu-id="bfa74-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bfa74-145">Minimales Shadermodell</span><span class="sxs-lookup"><span data-stu-id="bfa74-145">Minimum Shader Model</span></span>

<span data-ttu-id="bfa74-146">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfa74-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bfa74-147">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="bfa74-147">Shader Model</span></span>                                              | <span data-ttu-id="bfa74-148">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="bfa74-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bfa74-149">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="bfa74-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bfa74-150">ja</span><span class="sxs-lookup"><span data-stu-id="bfa74-150">yes</span></span>       |
| [<span data-ttu-id="bfa74-151">Shadermodell 4.1</span><span class="sxs-lookup"><span data-stu-id="bfa74-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bfa74-152">ja</span><span class="sxs-lookup"><span data-stu-id="bfa74-152">yes</span></span>       |
| [<span data-ttu-id="bfa74-153">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="bfa74-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bfa74-154">ja</span><span class="sxs-lookup"><span data-stu-id="bfa74-154">yes</span></span>       |
| [<span data-ttu-id="bfa74-155">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bfa74-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bfa74-156">nein</span><span class="sxs-lookup"><span data-stu-id="bfa74-156">no</span></span>        |
| [<span data-ttu-id="bfa74-157">Shadermodell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bfa74-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bfa74-158">nein</span><span class="sxs-lookup"><span data-stu-id="bfa74-158">no</span></span>        |
| [<span data-ttu-id="bfa74-159">Shadermodell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bfa74-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bfa74-160">nein</span><span class="sxs-lookup"><span data-stu-id="bfa74-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bfa74-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bfa74-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfa74-162">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bfa74-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





