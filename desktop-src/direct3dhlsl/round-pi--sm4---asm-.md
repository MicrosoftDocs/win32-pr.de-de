---
title: round_pi (sm4 - asm)
description: Gleitkomma rundet auf integraler Gleitkommazahl. | round_pi (sm4 - asm)
ms.assetid: AA4E4C2E-A4B0-4892-8660-1EF57767F4C4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b61282078b3639681eed756e2899d06744f0369e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997107"
---
# <a name="round_pi-sm4---asm"></a><span data-ttu-id="2892e-104">round \_ pi (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="2892e-104">round\_pi (sm4 - asm)</span></span>

<span data-ttu-id="2892e-105">Gleitkomma rundet auf integraler Gleitkommazahl.</span><span class="sxs-lookup"><span data-stu-id="2892e-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="2892e-106">round \_ pi \[ \_ sat \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="2892e-106">round\_pi\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="2892e-107">Element</span><span class="sxs-lookup"><span data-stu-id="2892e-107">Item</span></span>                                                            | <span data-ttu-id="2892e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2892e-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="2892e-109"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="2892e-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="2892e-110">\[in \] Die Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="2892e-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="2892e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2892e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="2892e-112">\[in \] Die Komponenten im Vorgang.</span><span class="sxs-lookup"><span data-stu-id="2892e-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="2892e-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2892e-113">Remarks</span></span>

<span data-ttu-id="2892e-114">Diese Anweisung führt eine komponentenweise Gleitkommarunde der Werte in *src0* aus und schreibt integrale Gleitkommawerte, *um zu dest zu schreiben.*</span><span class="sxs-lookup"><span data-stu-id="2892e-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span>

<span data-ttu-id="2892e-115">**Round \_ pi** rundet in Richtung +unendlich, häufig als ceil() bekannt.</span><span class="sxs-lookup"><span data-stu-id="2892e-115">**round\_pi** rounds towards +infinity, commonly known as ceil().</span></span>

<span data-ttu-id="2892e-116">Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Zahlenklassen erzielt werden.</span><span class="sxs-lookup"><span data-stu-id="2892e-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="2892e-117">F bedeutet endliche reale Zahl.</span><span class="sxs-lookup"><span data-stu-id="2892e-117">F means finite-real number.</span></span>



| <span data-ttu-id="2892e-118">**src**</span><span class="sxs-lookup"><span data-stu-id="2892e-118">**src**</span></span>  | <span data-ttu-id="2892e-119">**-inf**</span><span class="sxs-lookup"><span data-stu-id="2892e-119">**-inf**</span></span> | <span data-ttu-id="2892e-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="2892e-120">**-F**</span></span> | <span data-ttu-id="2892e-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="2892e-121">**-denorm**</span></span> | <span data-ttu-id="2892e-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="2892e-122">**-0**</span></span> | <span data-ttu-id="2892e-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="2892e-123">**+0**</span></span> | <span data-ttu-id="2892e-124">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="2892e-124">**+denorm**</span></span> | <span data-ttu-id="2892e-125">**+F**</span><span class="sxs-lookup"><span data-stu-id="2892e-125">**+F**</span></span> | <span data-ttu-id="2892e-126">**+inf**</span><span class="sxs-lookup"><span data-stu-id="2892e-126">**+inf**</span></span> | <span data-ttu-id="2892e-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="2892e-127">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="2892e-128">**Dest**</span><span class="sxs-lookup"><span data-stu-id="2892e-128">**dest**</span></span> | <span data-ttu-id="2892e-129">-inf</span><span class="sxs-lookup"><span data-stu-id="2892e-129">-inf</span></span>     | <span data-ttu-id="2892e-130">-F</span><span class="sxs-lookup"><span data-stu-id="2892e-130">-F</span></span>     | <span data-ttu-id="2892e-131">-0</span><span class="sxs-lookup"><span data-stu-id="2892e-131">-0</span></span>          | <span data-ttu-id="2892e-132">-0</span><span class="sxs-lookup"><span data-stu-id="2892e-132">-0</span></span>     | <span data-ttu-id="2892e-133">+0</span><span class="sxs-lookup"><span data-stu-id="2892e-133">+0</span></span>     | <span data-ttu-id="2892e-134">+0</span><span class="sxs-lookup"><span data-stu-id="2892e-134">+0</span></span>          | <span data-ttu-id="2892e-135">+F</span><span class="sxs-lookup"><span data-stu-id="2892e-135">+F</span></span>     | <span data-ttu-id="2892e-136">+inf</span><span class="sxs-lookup"><span data-stu-id="2892e-136">+inf</span></span>     | <span data-ttu-id="2892e-137">NaN</span><span class="sxs-lookup"><span data-stu-id="2892e-137">NaN</span></span>     |



 

<span data-ttu-id="2892e-138">Diese Anweisung gilt für die folgenden Shaderstufen:</span><span class="sxs-lookup"><span data-stu-id="2892e-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2892e-139">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="2892e-139">Vertex Shader</span></span> | <span data-ttu-id="2892e-140">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="2892e-140">Geometry Shader</span></span> | <span data-ttu-id="2892e-141">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="2892e-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2892e-142">x</span><span class="sxs-lookup"><span data-stu-id="2892e-142">x</span></span>             | <span data-ttu-id="2892e-143">x</span><span class="sxs-lookup"><span data-stu-id="2892e-143">x</span></span>               | <span data-ttu-id="2892e-144">x</span><span class="sxs-lookup"><span data-stu-id="2892e-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2892e-145">Shader-Mindestmodell</span><span class="sxs-lookup"><span data-stu-id="2892e-145">Minimum Shader Model</span></span>

<span data-ttu-id="2892e-146">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2892e-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2892e-147">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="2892e-147">Shader Model</span></span>                                              | <span data-ttu-id="2892e-148">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="2892e-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2892e-149">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="2892e-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2892e-150">ja</span><span class="sxs-lookup"><span data-stu-id="2892e-150">yes</span></span>       |
| [<span data-ttu-id="2892e-151">Shadermodell 4.1</span><span class="sxs-lookup"><span data-stu-id="2892e-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2892e-152">ja</span><span class="sxs-lookup"><span data-stu-id="2892e-152">yes</span></span>       |
| [<span data-ttu-id="2892e-153">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="2892e-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2892e-154">ja</span><span class="sxs-lookup"><span data-stu-id="2892e-154">yes</span></span>       |
| [<span data-ttu-id="2892e-155">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2892e-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2892e-156">nein</span><span class="sxs-lookup"><span data-stu-id="2892e-156">no</span></span>        |
| [<span data-ttu-id="2892e-157">Shadermodell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2892e-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2892e-158">nein</span><span class="sxs-lookup"><span data-stu-id="2892e-158">no</span></span>        |
| [<span data-ttu-id="2892e-159">Shadermodell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2892e-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2892e-160">nein</span><span class="sxs-lookup"><span data-stu-id="2892e-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2892e-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2892e-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2892e-162">Shadermodell 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2892e-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





