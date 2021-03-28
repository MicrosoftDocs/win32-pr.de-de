---
title: texcubegrad
description: Verwendet einen Farbverlauf, um die MIP-Ebene auszuwählen. | texcubegrad
ms.assetid: ebc5e38a-e314-43b0-9a00-7e4147e24bf0
keywords:
- texcubegrad HLSL
topic_type:
- apiref
api_name:
- texCUBEgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 694382488754c221c59df72112678a5971e62c0b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104050754"
---
# <a name="texcubegrad"></a><span data-ttu-id="e0b3a-105">texcubegrad</span><span class="sxs-lookup"><span data-stu-id="e0b3a-105">texCUBEgrad</span></span>

<span data-ttu-id="e0b3a-106">Verwendet einen Farbverlauf, um die MIP-Ebene auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="e0b3a-106">Samples a cube texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="e0b3a-107">Ret texcubegrad (s, t, DDX, ddY)</span><span class="sxs-lookup"><span data-stu-id="e0b3a-107">ret texCUBEgrad(s, t, ddx, ddy)</span></span> |
|---------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="e0b3a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0b3a-108">Parameters</span></span>



| <span data-ttu-id="e0b3a-109">Element</span><span class="sxs-lookup"><span data-stu-id="e0b3a-109">Item</span></span>                                                         | <span data-ttu-id="e0b3a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0b3a-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e0b3a-111"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="e0b3a-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="e0b3a-112">\[im \] samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="e0b3a-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="e0b3a-113"><span id="t"></span><span id="T"></span>*Bund*</span><span class="sxs-lookup"><span data-stu-id="e0b3a-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="e0b3a-114">\[in \] der Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="e0b3a-114">\[in\] The texture coordinate.</span></span><br/>                                    |
| <span data-ttu-id="e0b3a-115"><span id="ddx"></span><span id="DDX"></span>*DDX*</span><span class="sxs-lookup"><span data-stu-id="e0b3a-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="e0b3a-116">\[\]die Änderungs Rate der Oberflächengeometrie in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="e0b3a-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="e0b3a-117"><span id="ddy"></span><span id="DDY"></span>*tziger*</span><span class="sxs-lookup"><span data-stu-id="e0b3a-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="e0b3a-118">\[\]die Änderungs Rate der Oberflächengeometrie in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="e0b3a-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="e0b3a-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0b3a-119">Return Value</span></span>

<span data-ttu-id="e0b3a-120">Der Wert der Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="e0b3a-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="e0b3a-121">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="e0b3a-121">Type Description</span></span>



| <span data-ttu-id="e0b3a-122">Name</span><span class="sxs-lookup"><span data-stu-id="e0b3a-122">Name</span></span> | <span data-ttu-id="e0b3a-123">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="e0b3a-123">In/Out</span></span> | [<span data-ttu-id="e0b3a-124">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="e0b3a-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="e0b3a-125">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="e0b3a-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="e0b3a-126">Size</span><span class="sxs-lookup"><span data-stu-id="e0b3a-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="e0b3a-127">s</span><span class="sxs-lookup"><span data-stu-id="e0b3a-127">s</span></span>    | <span data-ttu-id="e0b3a-128">in</span><span class="sxs-lookup"><span data-stu-id="e0b3a-128">in</span></span>     | [<span data-ttu-id="e0b3a-129">**Objekt**</span><span class="sxs-lookup"><span data-stu-id="e0b3a-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e0b3a-130">samplercube</span><span class="sxs-lookup"><span data-stu-id="e0b3a-130">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="e0b3a-131">1</span><span class="sxs-lookup"><span data-stu-id="e0b3a-131">1</span></span>    |
| <span data-ttu-id="e0b3a-132">t</span><span class="sxs-lookup"><span data-stu-id="e0b3a-132">t</span></span>    | <span data-ttu-id="e0b3a-133">in</span><span class="sxs-lookup"><span data-stu-id="e0b3a-133">in</span></span>     | [<span data-ttu-id="e0b3a-134">**ve**</span><span class="sxs-lookup"><span data-stu-id="e0b3a-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e0b3a-135">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="e0b3a-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e0b3a-136">3</span><span class="sxs-lookup"><span data-stu-id="e0b3a-136">3</span></span>    |
| <span data-ttu-id="e0b3a-137">DDX</span><span class="sxs-lookup"><span data-stu-id="e0b3a-137">ddx</span></span>  | <span data-ttu-id="e0b3a-138">in</span><span class="sxs-lookup"><span data-stu-id="e0b3a-138">in</span></span>     | [<span data-ttu-id="e0b3a-139">**ve**</span><span class="sxs-lookup"><span data-stu-id="e0b3a-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e0b3a-140">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="e0b3a-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e0b3a-141">3</span><span class="sxs-lookup"><span data-stu-id="e0b3a-141">3</span></span>    |
| <span data-ttu-id="e0b3a-142">tziger</span><span class="sxs-lookup"><span data-stu-id="e0b3a-142">ddy</span></span>  | <span data-ttu-id="e0b3a-143">in</span><span class="sxs-lookup"><span data-stu-id="e0b3a-143">in</span></span>     | [<span data-ttu-id="e0b3a-144">**ve**</span><span class="sxs-lookup"><span data-stu-id="e0b3a-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e0b3a-145">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="e0b3a-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e0b3a-146">3</span><span class="sxs-lookup"><span data-stu-id="e0b3a-146">3</span></span>    |
| <span data-ttu-id="e0b3a-147">TZI</span><span class="sxs-lookup"><span data-stu-id="e0b3a-147">ret</span></span>  | <span data-ttu-id="e0b3a-148">out</span><span class="sxs-lookup"><span data-stu-id="e0b3a-148">out</span></span>    | [<span data-ttu-id="e0b3a-149">**ve**</span><span class="sxs-lookup"><span data-stu-id="e0b3a-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e0b3a-150">**float**</span><span class="sxs-lookup"><span data-stu-id="e0b3a-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e0b3a-151">4</span><span class="sxs-lookup"><span data-stu-id="e0b3a-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e0b3a-152">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="e0b3a-152">Minimum Shader Model</span></span>

<span data-ttu-id="e0b3a-153">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e0b3a-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e0b3a-154">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="e0b3a-154">Shader Model</span></span>                                              | <span data-ttu-id="e0b3a-155">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="e0b3a-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="e0b3a-156">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="e0b3a-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e0b3a-157">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="e0b3a-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="e0b3a-158">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e0b3a-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e0b3a-159">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="e0b3a-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="e0b3a-160">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e0b3a-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e0b3a-161">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="e0b3a-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="e0b3a-162">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e0b3a-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e0b3a-163">nein</span><span class="sxs-lookup"><span data-stu-id="e0b3a-163">no</span></span>                       |



 

1.  <span data-ttu-id="e0b3a-164">Eine bedeutende Code Neuanordnung erfolgt, um Farbverlaufs Berechnungen außerhalb der Fluss Steuerung zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="e0b3a-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="e0b3a-165">Wenn die D3DPSHADERCAPS2 \_ 0-Obergrenze mit D3DD3DPSHADERCAPS2 \_ 0 \_ gradientinstructions festgelegt ist, ordnet der Compiler diese Funktion texldd zu.</span><span class="sxs-lookup"><span data-stu-id="e0b3a-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="see-also"></a><span data-ttu-id="e0b3a-166">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e0b3a-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0b3a-167">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="e0b3a-167">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

