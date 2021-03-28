---
title: 'Texcube (HLSL-Referenz): Wählen Sie die MIP-Ebene aus.'
description: Verwendet einen Farbverlauf, um die MIP-Ebene auszuwählen. | Texcube (HLSL-Referenz)
ms.assetid: 5615f48b-eb0a-4de7-a441-51ec3cecf6fd
keywords:
- Texcube HLSL
topic_type:
- apiref
api_name:
- texCUBE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6286b4fedb94b9fd5c84c76171e9478f06e16ce4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982676"
---
# <a name="texcube-hlsl-reference---select-the-mip-level"></a><span data-ttu-id="0f4d7-105">Texcube (HLSL-Referenz): Wählen Sie die MIP-Ebene aus.</span><span class="sxs-lookup"><span data-stu-id="0f4d7-105">texCUBE (HLSL reference) - Select the mip level</span></span>

<span data-ttu-id="0f4d7-106">Verwendet einen Farbverlauf, um die MIP-Ebene auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="0f4d7-106">Samples a cube texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="0f4d7-107">Ret Texcube (s, t, DDX, ddY)</span><span class="sxs-lookup"><span data-stu-id="0f4d7-107">ret texCUBE(s, t, ddx, ddy)</span></span> |
|-----------------------------|



 

## <a name="parameters"></a><span data-ttu-id="0f4d7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f4d7-108">Parameters</span></span>



| <span data-ttu-id="0f4d7-109">Element</span><span class="sxs-lookup"><span data-stu-id="0f4d7-109">Item</span></span>                                                         | <span data-ttu-id="0f4d7-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f4d7-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0f4d7-111"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="0f4d7-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="0f4d7-112">\[im \] samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="0f4d7-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="0f4d7-113"><span id="t"></span><span id="T"></span>*Bund*</span><span class="sxs-lookup"><span data-stu-id="0f4d7-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="0f4d7-114">\[in \] der Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="0f4d7-114">\[in\] The texture coordinate.</span></span><br/>                                    |
| <span data-ttu-id="0f4d7-115"><span id="ddx"></span><span id="DDX"></span>*DDX*</span><span class="sxs-lookup"><span data-stu-id="0f4d7-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="0f4d7-116">\[\]die Änderungs Rate der Oberflächengeometrie in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="0f4d7-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="0f4d7-117"><span id="ddy"></span><span id="DDY"></span>*tziger*</span><span class="sxs-lookup"><span data-stu-id="0f4d7-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="0f4d7-118">\[\]die Änderungs Rate der Oberflächengeometrie in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="0f4d7-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="0f4d7-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f4d7-119">Return Value</span></span>

<span data-ttu-id="0f4d7-120">Der Wert der Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="0f4d7-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="0f4d7-121">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="0f4d7-121">Type Description</span></span>



| <span data-ttu-id="0f4d7-122">Name</span><span class="sxs-lookup"><span data-stu-id="0f4d7-122">Name</span></span> | <span data-ttu-id="0f4d7-123">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="0f4d7-123">In/Out</span></span> | [<span data-ttu-id="0f4d7-124">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="0f4d7-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="0f4d7-125">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="0f4d7-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="0f4d7-126">Size</span><span class="sxs-lookup"><span data-stu-id="0f4d7-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="0f4d7-127">s</span><span class="sxs-lookup"><span data-stu-id="0f4d7-127">s</span></span>    | <span data-ttu-id="0f4d7-128">in</span><span class="sxs-lookup"><span data-stu-id="0f4d7-128">in</span></span>     | [<span data-ttu-id="0f4d7-129">**Objekt**</span><span class="sxs-lookup"><span data-stu-id="0f4d7-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0f4d7-130">samplercube</span><span class="sxs-lookup"><span data-stu-id="0f4d7-130">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="0f4d7-131">1</span><span class="sxs-lookup"><span data-stu-id="0f4d7-131">1</span></span>    |
| <span data-ttu-id="0f4d7-132">t</span><span class="sxs-lookup"><span data-stu-id="0f4d7-132">t</span></span>    | <span data-ttu-id="0f4d7-133">in</span><span class="sxs-lookup"><span data-stu-id="0f4d7-133">in</span></span>     | [<span data-ttu-id="0f4d7-134">**ve**</span><span class="sxs-lookup"><span data-stu-id="0f4d7-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0f4d7-135">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="0f4d7-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0f4d7-136">3</span><span class="sxs-lookup"><span data-stu-id="0f4d7-136">3</span></span>    |
| <span data-ttu-id="0f4d7-137">DDX</span><span class="sxs-lookup"><span data-stu-id="0f4d7-137">ddx</span></span>  | <span data-ttu-id="0f4d7-138">in</span><span class="sxs-lookup"><span data-stu-id="0f4d7-138">in</span></span>     | [<span data-ttu-id="0f4d7-139">**ve**</span><span class="sxs-lookup"><span data-stu-id="0f4d7-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0f4d7-140">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="0f4d7-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0f4d7-141">3</span><span class="sxs-lookup"><span data-stu-id="0f4d7-141">3</span></span>    |
| <span data-ttu-id="0f4d7-142">tziger</span><span class="sxs-lookup"><span data-stu-id="0f4d7-142">ddy</span></span>  | <span data-ttu-id="0f4d7-143">in</span><span class="sxs-lookup"><span data-stu-id="0f4d7-143">in</span></span>     | [<span data-ttu-id="0f4d7-144">**ve**</span><span class="sxs-lookup"><span data-stu-id="0f4d7-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0f4d7-145">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="0f4d7-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0f4d7-146">3</span><span class="sxs-lookup"><span data-stu-id="0f4d7-146">3</span></span>    |
| <span data-ttu-id="0f4d7-147">TZI</span><span class="sxs-lookup"><span data-stu-id="0f4d7-147">ret</span></span>  | <span data-ttu-id="0f4d7-148">out</span><span class="sxs-lookup"><span data-stu-id="0f4d7-148">out</span></span>    | [<span data-ttu-id="0f4d7-149">**ve**</span><span class="sxs-lookup"><span data-stu-id="0f4d7-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0f4d7-150">**float**</span><span class="sxs-lookup"><span data-stu-id="0f4d7-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0f4d7-151">4</span><span class="sxs-lookup"><span data-stu-id="0f4d7-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0f4d7-152">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="0f4d7-152">Minimum Shader Model</span></span>

<span data-ttu-id="0f4d7-153">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0f4d7-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0f4d7-154">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="0f4d7-154">Shader Model</span></span>                                              | <span data-ttu-id="0f4d7-155">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="0f4d7-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="0f4d7-156">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="0f4d7-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0f4d7-157">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="0f4d7-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="0f4d7-158">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f4d7-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0f4d7-159">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="0f4d7-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="0f4d7-160">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f4d7-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0f4d7-161">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="0f4d7-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="0f4d7-162">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f4d7-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0f4d7-163">nein</span><span class="sxs-lookup"><span data-stu-id="0f4d7-163">no</span></span>                       |



 

1.  <span data-ttu-id="0f4d7-164">Eine bedeutende Code Neuanordnung erfolgt, um Farbverlaufs Berechnungen außerhalb der Fluss Steuerung zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="0f4d7-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="0f4d7-165">Wenn die D3DPSHADERCAPS2 \_ 0-Obergrenze mit D3DD3DPSHADERCAPS2 \_ 0 \_ gradientinstructions festgelegt ist, ordnet der Compiler diese Funktion texldd zu.</span><span class="sxs-lookup"><span data-stu-id="0f4d7-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="see-also"></a><span data-ttu-id="0f4d7-166">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0f4d7-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f4d7-167">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="0f4d7-167">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

