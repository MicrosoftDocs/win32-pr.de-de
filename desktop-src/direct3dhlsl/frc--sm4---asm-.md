---
title: frc (sm4 - asm)
description: Komponentenweises Extrahieren der Bruchkomponente.
ms.assetid: 17C88BCE-7F2F-446C-9BB4-860098B5E42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f59b747f38fb970b92b5e48610873efe781d63d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993917"
---
# <a name="frc-sm4---asm"></a><span data-ttu-id="d2533-103">frc (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="d2533-103">frc (sm4 - asm)</span></span>

<span data-ttu-id="d2533-104">Komponentenweises Extrahieren der Bruchkomponente.</span><span class="sxs-lookup"><span data-stu-id="d2533-104">Component-wise, extract fractional component.</span></span>



| <span data-ttu-id="d2533-105">frc \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="d2533-105">frc\[\_sat\] dest\[.mask\], \[-\] src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="d2533-106">Element</span><span class="sxs-lookup"><span data-stu-id="d2533-106">Item</span></span>                                                            | <span data-ttu-id="d2533-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2533-107">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2533-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="d2533-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d2533-109">\[in \] Die Adresse des Ergebnisses des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="d2533-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="d2533-110">*dest*  =  *src0*  -  [round \_ ni](round-ni--sm4---asm-.md)(*src0*)</span><span class="sxs-lookup"><span data-stu-id="d2533-110">*dest* = *src0* - [round\_ni](round-ni--sm4---asm-.md)(*src0*)</span></span><br/> |
| <span data-ttu-id="d2533-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d2533-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d2533-112">\[in \] Die Komponente im Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d2533-112">\[in\] The component in the operation.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="d2533-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d2533-113">Remarks</span></span>

<span data-ttu-id="d2533-114">Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Zahlenklassen erzielt werden.</span><span class="sxs-lookup"><span data-stu-id="d2533-114">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



| <span data-ttu-id="d2533-115">**src**</span><span class="sxs-lookup"><span data-stu-id="d2533-115">**src**</span></span>  | <span data-ttu-id="d2533-116">**-inf**</span><span class="sxs-lookup"><span data-stu-id="d2533-116">**-inf**</span></span> | <span data-ttu-id="d2533-117">**-F**</span><span class="sxs-lookup"><span data-stu-id="d2533-117">**-F**</span></span>     | <span data-ttu-id="d2533-118">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="d2533-118">**-denorm**</span></span> | <span data-ttu-id="d2533-119">**-0**</span><span class="sxs-lookup"><span data-stu-id="d2533-119">**-0**</span></span> | <span data-ttu-id="d2533-120">**+0**</span><span class="sxs-lookup"><span data-stu-id="d2533-120">**+0**</span></span> | <span data-ttu-id="d2533-121">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="d2533-121">**+denorm**</span></span> | <span data-ttu-id="d2533-122">**+F**</span><span class="sxs-lookup"><span data-stu-id="d2533-122">**+F**</span></span>     | <span data-ttu-id="d2533-123">**+inf**</span><span class="sxs-lookup"><span data-stu-id="d2533-123">**+inf**</span></span> | <span data-ttu-id="d2533-124">**NaN**</span><span class="sxs-lookup"><span data-stu-id="d2533-124">**NaN**</span></span> |
|----------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| <span data-ttu-id="d2533-125">**Dest**</span><span class="sxs-lookup"><span data-stu-id="d2533-125">**dest**</span></span> | <span data-ttu-id="d2533-126">NaN</span><span class="sxs-lookup"><span data-stu-id="d2533-126">NaN</span></span>      | <span data-ttu-id="d2533-127">\[+0 bis 1)</span><span class="sxs-lookup"><span data-stu-id="d2533-127">\[+0 to 1)</span></span> | <span data-ttu-id="d2533-128">+0</span><span class="sxs-lookup"><span data-stu-id="d2533-128">+0</span></span>          | <span data-ttu-id="d2533-129">+0</span><span class="sxs-lookup"><span data-stu-id="d2533-129">+0</span></span>     | <span data-ttu-id="d2533-130">+0</span><span class="sxs-lookup"><span data-stu-id="d2533-130">+0</span></span>     | <span data-ttu-id="d2533-131">+0</span><span class="sxs-lookup"><span data-stu-id="d2533-131">+0</span></span>          | <span data-ttu-id="d2533-132">\[+0 bis 1)</span><span class="sxs-lookup"><span data-stu-id="d2533-132">\[+0 to 1)</span></span> | <span data-ttu-id="d2533-133">NaN</span><span class="sxs-lookup"><span data-stu-id="d2533-133">NaN</span></span>      | <span data-ttu-id="d2533-134">NaN</span><span class="sxs-lookup"><span data-stu-id="d2533-134">NaN</span></span>     |



 

<span data-ttu-id="d2533-135">F bedeutet endliche reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="d2533-135">F means finite-real number.</span></span>

<span data-ttu-id="d2533-136">Diese Anweisung gilt für die folgenden Shaderstufen:</span><span class="sxs-lookup"><span data-stu-id="d2533-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d2533-137">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="d2533-137">Vertex Shader</span></span> | <span data-ttu-id="d2533-138">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="d2533-138">Geometry Shader</span></span> | <span data-ttu-id="d2533-139">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="d2533-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d2533-140">x</span><span class="sxs-lookup"><span data-stu-id="d2533-140">x</span></span>             | <span data-ttu-id="d2533-141">x</span><span class="sxs-lookup"><span data-stu-id="d2533-141">x</span></span>               | <span data-ttu-id="d2533-142">x</span><span class="sxs-lookup"><span data-stu-id="d2533-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d2533-143">Minimales Shadermodell</span><span class="sxs-lookup"><span data-stu-id="d2533-143">Minimum Shader Model</span></span>

<span data-ttu-id="d2533-144">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d2533-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d2533-145">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="d2533-145">Shader Model</span></span>                                              | <span data-ttu-id="d2533-146">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="d2533-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d2533-147">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="d2533-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d2533-148">ja</span><span class="sxs-lookup"><span data-stu-id="d2533-148">yes</span></span>       |
| [<span data-ttu-id="d2533-149">Shadermodell 4.1</span><span class="sxs-lookup"><span data-stu-id="d2533-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d2533-150">ja</span><span class="sxs-lookup"><span data-stu-id="d2533-150">yes</span></span>       |
| [<span data-ttu-id="d2533-151">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="d2533-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d2533-152">ja</span><span class="sxs-lookup"><span data-stu-id="d2533-152">yes</span></span>       |
| [<span data-ttu-id="d2533-153">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d2533-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d2533-154">nein</span><span class="sxs-lookup"><span data-stu-id="d2533-154">no</span></span>        |
| [<span data-ttu-id="d2533-155">Shadermodell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d2533-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d2533-156">nein</span><span class="sxs-lookup"><span data-stu-id="d2533-156">no</span></span>        |
| [<span data-ttu-id="d2533-157">Shadermodell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d2533-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d2533-158">nein</span><span class="sxs-lookup"><span data-stu-id="d2533-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d2533-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d2533-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2533-160">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d2533-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





