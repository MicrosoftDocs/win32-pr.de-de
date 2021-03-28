---
title: tex2Dgrad
description: Stichproben eine 2D-Textur mit einem Farbverlauf, um die MIP-Ebene auszuwählen. | tex2Dgrad
ms.assetid: a9ab7972-3480-4b37-aa10-c5cf811bdd0e
keywords:
- tex2Dgrad HLSL
topic_type:
- apiref
api_name:
- tex2Dgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74b20f1cf1f6f5d3b2873f4546dd57ef73b23dbb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981120"
---
# <a name="tex2dgrad"></a><span data-ttu-id="26015-105">tex2Dgrad</span><span class="sxs-lookup"><span data-stu-id="26015-105">tex2Dgrad</span></span>

<span data-ttu-id="26015-106">Stichproben eine 2D-Textur mit einem Farbverlauf, um die MIP-Ebene auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="26015-106">Samples a 2D texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="26015-107">Ret tex2Dgrad (s, t, DDX, ddY)</span><span class="sxs-lookup"><span data-stu-id="26015-107">ret tex2Dgrad(s, t, ddx, ddy)</span></span> |
|-------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="26015-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="26015-108">Parameters</span></span>



| <span data-ttu-id="26015-109">Element</span><span class="sxs-lookup"><span data-stu-id="26015-109">Item</span></span>                                                         | <span data-ttu-id="26015-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26015-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="26015-111"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="26015-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="26015-112">\[im \] samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="26015-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="26015-113"><span id="t"></span><span id="T"></span>*Bund*</span><span class="sxs-lookup"><span data-stu-id="26015-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="26015-114">\[in \] den Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="26015-114">\[in\] The texture coordinates.</span></span><br/>                                   |
| <span data-ttu-id="26015-115"><span id="ddx"></span><span id="DDX"></span>*DDX*</span><span class="sxs-lookup"><span data-stu-id="26015-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="26015-116">\[\]die Änderungs Rate der Oberflächengeometrie in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="26015-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="26015-117"><span id="ddy"></span><span id="DDY"></span>*tziger*</span><span class="sxs-lookup"><span data-stu-id="26015-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="26015-118">\[\]die Änderungs Rate der Oberflächengeometrie in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="26015-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="26015-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26015-119">Return Value</span></span>

<span data-ttu-id="26015-120">Der Wert der Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="26015-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="26015-121">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="26015-121">Type Description</span></span>



| <span data-ttu-id="26015-122">Name</span><span class="sxs-lookup"><span data-stu-id="26015-122">Name</span></span> | <span data-ttu-id="26015-123">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="26015-123">In/Out</span></span> | [<span data-ttu-id="26015-124">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="26015-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="26015-125">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="26015-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="26015-126">Size</span><span class="sxs-lookup"><span data-stu-id="26015-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="26015-127">s</span><span class="sxs-lookup"><span data-stu-id="26015-127">s</span></span>    | <span data-ttu-id="26015-128">in</span><span class="sxs-lookup"><span data-stu-id="26015-128">in</span></span>     | [<span data-ttu-id="26015-129">**Objekt**</span><span class="sxs-lookup"><span data-stu-id="26015-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="26015-130">sampler2D</span><span class="sxs-lookup"><span data-stu-id="26015-130">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="26015-131">1</span><span class="sxs-lookup"><span data-stu-id="26015-131">1</span></span>    |
| <span data-ttu-id="26015-132">t</span><span class="sxs-lookup"><span data-stu-id="26015-132">t</span></span>    | <span data-ttu-id="26015-133">in</span><span class="sxs-lookup"><span data-stu-id="26015-133">in</span></span>     | [<span data-ttu-id="26015-134">**ve**</span><span class="sxs-lookup"><span data-stu-id="26015-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="26015-135">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="26015-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="26015-136">2</span><span class="sxs-lookup"><span data-stu-id="26015-136">2</span></span>    |
| <span data-ttu-id="26015-137">DDX</span><span class="sxs-lookup"><span data-stu-id="26015-137">ddx</span></span>  | <span data-ttu-id="26015-138">in</span><span class="sxs-lookup"><span data-stu-id="26015-138">in</span></span>     | [<span data-ttu-id="26015-139">**ve**</span><span class="sxs-lookup"><span data-stu-id="26015-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="26015-140">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="26015-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="26015-141">2</span><span class="sxs-lookup"><span data-stu-id="26015-141">2</span></span>    |
| <span data-ttu-id="26015-142">tziger</span><span class="sxs-lookup"><span data-stu-id="26015-142">ddy</span></span>  | <span data-ttu-id="26015-143">in</span><span class="sxs-lookup"><span data-stu-id="26015-143">in</span></span>     | [<span data-ttu-id="26015-144">**ve**</span><span class="sxs-lookup"><span data-stu-id="26015-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="26015-145">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="26015-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="26015-146">2</span><span class="sxs-lookup"><span data-stu-id="26015-146">2</span></span>    |
| <span data-ttu-id="26015-147">TZI</span><span class="sxs-lookup"><span data-stu-id="26015-147">ret</span></span>  | <span data-ttu-id="26015-148">out</span><span class="sxs-lookup"><span data-stu-id="26015-148">out</span></span>    | [<span data-ttu-id="26015-149">**ve**</span><span class="sxs-lookup"><span data-stu-id="26015-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="26015-150">**float**</span><span class="sxs-lookup"><span data-stu-id="26015-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="26015-151">4</span><span class="sxs-lookup"><span data-stu-id="26015-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="26015-152">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="26015-152">Minimum Shader Model</span></span>

<span data-ttu-id="26015-153">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="26015-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="26015-154">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="26015-154">Shader Model</span></span>                                              | <span data-ttu-id="26015-155">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="26015-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="26015-156">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="26015-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="26015-157">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="26015-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="26015-158">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="26015-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="26015-159">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="26015-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="26015-160">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="26015-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="26015-161">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="26015-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="26015-162">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="26015-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="26015-163">nein</span><span class="sxs-lookup"><span data-stu-id="26015-163">no</span></span>                       |



 

1.  <span data-ttu-id="26015-164">Eine bedeutende Code Neuanordnung erfolgt, um Farbverlaufs Berechnungen außerhalb der Fluss Steuerung zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="26015-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="26015-165">Wenn die D3DPSHADERCAPS2 \_ 0-Obergrenze mit D3DD3DPSHADERCAPS2 \_ 0 \_ gradientinstructions festgelegt ist, ordnet der Compiler diese Funktion texldd zu.</span><span class="sxs-lookup"><span data-stu-id="26015-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="remarks"></a><span data-ttu-id="26015-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26015-166">Remarks</span></span>

<span data-ttu-id="26015-167">Wenn die Fluss Steuerung in einem Shader vorhanden ist, ist das Ergebnis einer in einem bestimmten Verzweigungs Pfad angeforderten gradientenberechnung mehrdeutig, wenn angrenzende Pixel getrennte Fluss Steuerungs Pfade nach unten durchlaufen können.</span><span class="sxs-lookup"><span data-stu-id="26015-167">When flow control is present in a shader, the result of a gradient calculation requested inside a given branch path is ambiguous when adjacent pixels may go down separate flow control paths.</span></span> <span data-ttu-id="26015-168">Daher wird die Verwendung eines pixelshadervorgangs als unzulässig angesehen, der eine gradientenberechnung an einem Speicherort anfordert, der sich innerhalb eines Fluss Steuerungs Konstrukts befindet, das für ein bestimmtes primitiv, das gerengt wird, in Pixel variieren kann.</span><span class="sxs-lookup"><span data-stu-id="26015-168">Therefore, it is deemed illegal to use any pixel shader operation that requests a gradient calculation to occur at a location that is inside a flow control construct which could vary across pixels for a given primitive being rasterized.</span></span> <span data-ttu-id="26015-169">Wenn eine Seite einer **if** -Anweisung mit dem Branch-Attribut eine Gradient-Funktion verwendet, kann ein Compilerfehler generiert werden.</span><span class="sxs-lookup"><span data-stu-id="26015-169">If either side of an **if** statement with the branch attribute uses a gradient function a compiler error may be generated.</span></span> <span data-ttu-id="26015-170">Siehe [if-Anweisung (DirectX HLSL)](dx-graphics-hlsl-if.md).</span><span class="sxs-lookup"><span data-stu-id="26015-170">See [if Statement (DirectX HLSL)](dx-graphics-hlsl-if.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="26015-171">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="26015-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26015-172">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="26015-172">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

