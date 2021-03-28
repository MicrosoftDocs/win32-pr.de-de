---
title: FRC (SM4-ASM)
description: Komponenten Weise extrahieren Sie eine Bruchteile Komponente.
ms.assetid: 17C88BCE-7F2F-446C-9BB4-860098B5E42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4abcfd56e7d6051e9c476097b3e5eef4d97563e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976432"
---
# <a name="frc-sm4---asm"></a><span data-ttu-id="d2534-103">FRC (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d2534-103">frc (sm4 - asm)</span></span>

<span data-ttu-id="d2534-104">Komponenten Weise extrahieren Sie eine Bruchteile Komponente.</span><span class="sxs-lookup"><span data-stu-id="d2534-104">Component-wise, extract fractional component.</span></span>



| <span data-ttu-id="d2534-105">FRC \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="d2534-105">frc\[\_sat\] dest\[.mask\], \[-\] src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="d2534-106">Element</span><span class="sxs-lookup"><span data-stu-id="d2534-106">Item</span></span>                                                            | <span data-ttu-id="d2534-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2534-107">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2534-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d2534-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d2534-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="d2534-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="d2534-110">*dest*  =  *src0*  -  [Round \_ NI](round-ni--sm4---asm-.md)(*src0*)</span><span class="sxs-lookup"><span data-stu-id="d2534-110">*dest* = *src0* - [round\_ni](round-ni--sm4---asm-.md)(*src0*)</span></span><br/> |
| <span data-ttu-id="d2534-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d2534-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d2534-112">\[in \] der-Komponente im-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d2534-112">\[in\] The component in the operation.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="d2534-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2534-113">Remarks</span></span>

<span data-ttu-id="d2534-114">In der folgenden Tabelle werden die Ergebnisse angezeigt, die beim Ausführen der Anweisung mit verschiedenen Klassen von Zahlen abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="d2534-114">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



|          |          |            |             |        |        |             |            |          |         |
|----------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| <span data-ttu-id="d2534-115">**src**</span><span class="sxs-lookup"><span data-stu-id="d2534-115">**src**</span></span>  | <span data-ttu-id="d2534-116">**-INF**</span><span class="sxs-lookup"><span data-stu-id="d2534-116">**-inf**</span></span> | <span data-ttu-id="d2534-117">**-F**</span><span class="sxs-lookup"><span data-stu-id="d2534-117">**-F**</span></span>     | <span data-ttu-id="d2534-118">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="d2534-118">**-denorm**</span></span> | <span data-ttu-id="d2534-119">**-0**</span><span class="sxs-lookup"><span data-stu-id="d2534-119">**-0**</span></span> | <span data-ttu-id="d2534-120">**+0**</span><span class="sxs-lookup"><span data-stu-id="d2534-120">**+0**</span></span> | <span data-ttu-id="d2534-121">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="d2534-121">**+denorm**</span></span> | <span data-ttu-id="d2534-122">**+ F**</span><span class="sxs-lookup"><span data-stu-id="d2534-122">**+F**</span></span>     | <span data-ttu-id="d2534-123">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="d2534-123">**+inf**</span></span> | <span data-ttu-id="d2534-124">**NaN**</span><span class="sxs-lookup"><span data-stu-id="d2534-124">**NaN**</span></span> |
| <span data-ttu-id="d2534-125">**dest**</span><span class="sxs-lookup"><span data-stu-id="d2534-125">**dest**</span></span> | <span data-ttu-id="d2534-126">NaN</span><span class="sxs-lookup"><span data-stu-id="d2534-126">NaN</span></span>      | <span data-ttu-id="d2534-127">\[+ 0 bis 1)</span><span class="sxs-lookup"><span data-stu-id="d2534-127">\[+0 to 1)</span></span> | <span data-ttu-id="d2534-128">+0</span><span class="sxs-lookup"><span data-stu-id="d2534-128">+0</span></span>          | <span data-ttu-id="d2534-129">+0</span><span class="sxs-lookup"><span data-stu-id="d2534-129">+0</span></span>     | <span data-ttu-id="d2534-130">+0</span><span class="sxs-lookup"><span data-stu-id="d2534-130">+0</span></span>     | <span data-ttu-id="d2534-131">+0</span><span class="sxs-lookup"><span data-stu-id="d2534-131">+0</span></span>          | <span data-ttu-id="d2534-132">\[+ 0 bis 1)</span><span class="sxs-lookup"><span data-stu-id="d2534-132">\[+0 to 1)</span></span> | <span data-ttu-id="d2534-133">NaN</span><span class="sxs-lookup"><span data-stu-id="d2534-133">NaN</span></span>      | <span data-ttu-id="d2534-134">NaN</span><span class="sxs-lookup"><span data-stu-id="d2534-134">NaN</span></span>     |



 

<span data-ttu-id="d2534-135">F bedeutet eine endliche reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="d2534-135">F means finite-real number.</span></span>

<span data-ttu-id="d2534-136">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="d2534-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d2534-137">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="d2534-137">Vertex Shader</span></span> | <span data-ttu-id="d2534-138">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="d2534-138">Geometry Shader</span></span> | <span data-ttu-id="d2534-139">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="d2534-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d2534-140">x</span><span class="sxs-lookup"><span data-stu-id="d2534-140">x</span></span>             | <span data-ttu-id="d2534-141">x</span><span class="sxs-lookup"><span data-stu-id="d2534-141">x</span></span>               | <span data-ttu-id="d2534-142">x</span><span class="sxs-lookup"><span data-stu-id="d2534-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d2534-143">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="d2534-143">Minimum Shader Model</span></span>

<span data-ttu-id="d2534-144">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d2534-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d2534-145">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="d2534-145">Shader Model</span></span>                                              | <span data-ttu-id="d2534-146">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="d2534-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d2534-147">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="d2534-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d2534-148">ja</span><span class="sxs-lookup"><span data-stu-id="d2534-148">yes</span></span>       |
| [<span data-ttu-id="d2534-149">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="d2534-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d2534-150">ja</span><span class="sxs-lookup"><span data-stu-id="d2534-150">yes</span></span>       |
| [<span data-ttu-id="d2534-151">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="d2534-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d2534-152">ja</span><span class="sxs-lookup"><span data-stu-id="d2534-152">yes</span></span>       |
| [<span data-ttu-id="d2534-153">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d2534-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d2534-154">nein</span><span class="sxs-lookup"><span data-stu-id="d2534-154">no</span></span>        |
| [<span data-ttu-id="d2534-155">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d2534-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d2534-156">nein</span><span class="sxs-lookup"><span data-stu-id="d2534-156">no</span></span>        |
| [<span data-ttu-id="d2534-157">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d2534-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d2534-158">nein</span><span class="sxs-lookup"><span data-stu-id="d2534-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d2534-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d2534-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2534-160">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d2534-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





