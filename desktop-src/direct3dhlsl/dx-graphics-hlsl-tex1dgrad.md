---
title: tex1Dgrad
description: Stichproben eine 1D-Textur mithilfe eines Farbverlaufs, um die MIP-Ebene auszuwählen. | tex1Dgrad
ms.assetid: 30a28985-4808-4ce6-a3b1-40a9f93cbd8d
keywords:
- tex1Dgrad HLSL
topic_type:
- apiref
api_name:
- tex1Dgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 195607c8b3fc1844e7d417bb37de7dd270d5a448
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352419"
---
# <a name="tex1dgrad"></a><span data-ttu-id="9b993-105">tex1Dgrad</span><span class="sxs-lookup"><span data-stu-id="9b993-105">tex1Dgrad</span></span>

<span data-ttu-id="9b993-106">Stichproben eine 1D-Textur mithilfe eines Farbverlaufs, um die MIP-Ebene auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="9b993-106">Samples a 1D texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="9b993-107">Ret tex1Dgrad (s, t, DDX, ddY)</span><span class="sxs-lookup"><span data-stu-id="9b993-107">ret tex1Dgrad(s, t, ddx, ddy)</span></span> |
|-------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="9b993-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b993-108">Parameters</span></span>



| <span data-ttu-id="9b993-109">Element</span><span class="sxs-lookup"><span data-stu-id="9b993-109">Item</span></span>                                                         | <span data-ttu-id="9b993-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b993-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9b993-111"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="9b993-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="9b993-112">\[im \] samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="9b993-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="9b993-113"><span id="t"></span><span id="T"></span>*Bund*</span><span class="sxs-lookup"><span data-stu-id="9b993-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="9b993-114">\[in \] der Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="9b993-114">\[in\] The texture coordinate.</span></span><br/>                                    |
| <span data-ttu-id="9b993-115"><span id="ddx"></span><span id="DDX"></span>*DDX*</span><span class="sxs-lookup"><span data-stu-id="9b993-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="9b993-116">\[\]die Änderungs Rate der Oberflächengeometrie in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="9b993-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="9b993-117"><span id="ddy"></span><span id="DDY"></span>*tziger*</span><span class="sxs-lookup"><span data-stu-id="9b993-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="9b993-118">\[\]die Änderungs Rate der Oberflächengeometrie in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="9b993-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="9b993-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9b993-119">Return Value</span></span>

<span data-ttu-id="9b993-120">Der Wert der Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="9b993-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="9b993-121">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="9b993-121">Type Description</span></span>



| <span data-ttu-id="9b993-122">Name</span><span class="sxs-lookup"><span data-stu-id="9b993-122">Name</span></span> | <span data-ttu-id="9b993-123">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="9b993-123">In/Out</span></span> | [<span data-ttu-id="9b993-124">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="9b993-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="9b993-125">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="9b993-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="9b993-126">Size</span><span class="sxs-lookup"><span data-stu-id="9b993-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="9b993-127">s</span><span class="sxs-lookup"><span data-stu-id="9b993-127">s</span></span>    | <span data-ttu-id="9b993-128">in</span><span class="sxs-lookup"><span data-stu-id="9b993-128">in</span></span>     | [<span data-ttu-id="9b993-129">**Objekt**</span><span class="sxs-lookup"><span data-stu-id="9b993-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="9b993-130">sampler1D</span><span class="sxs-lookup"><span data-stu-id="9b993-130">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="9b993-131">1</span><span class="sxs-lookup"><span data-stu-id="9b993-131">1</span></span>    |
| <span data-ttu-id="9b993-132">t</span><span class="sxs-lookup"><span data-stu-id="9b993-132">t</span></span>    | <span data-ttu-id="9b993-133">in</span><span class="sxs-lookup"><span data-stu-id="9b993-133">in</span></span>     | [<span data-ttu-id="9b993-134">**ve**</span><span class="sxs-lookup"><span data-stu-id="9b993-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="9b993-135">**float**</span><span class="sxs-lookup"><span data-stu-id="9b993-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9b993-136">1</span><span class="sxs-lookup"><span data-stu-id="9b993-136">1</span></span>    |
| <span data-ttu-id="9b993-137">DDX</span><span class="sxs-lookup"><span data-stu-id="9b993-137">ddx</span></span>  | <span data-ttu-id="9b993-138">in</span><span class="sxs-lookup"><span data-stu-id="9b993-138">in</span></span>     | [<span data-ttu-id="9b993-139">**ve**</span><span class="sxs-lookup"><span data-stu-id="9b993-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="9b993-140">**float**</span><span class="sxs-lookup"><span data-stu-id="9b993-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9b993-141">1</span><span class="sxs-lookup"><span data-stu-id="9b993-141">1</span></span>    |
| <span data-ttu-id="9b993-142">tziger</span><span class="sxs-lookup"><span data-stu-id="9b993-142">ddy</span></span>  | <span data-ttu-id="9b993-143">in</span><span class="sxs-lookup"><span data-stu-id="9b993-143">in</span></span>     | [<span data-ttu-id="9b993-144">**ve**</span><span class="sxs-lookup"><span data-stu-id="9b993-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="9b993-145">**float**</span><span class="sxs-lookup"><span data-stu-id="9b993-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9b993-146">1</span><span class="sxs-lookup"><span data-stu-id="9b993-146">1</span></span>    |
| <span data-ttu-id="9b993-147">TZI</span><span class="sxs-lookup"><span data-stu-id="9b993-147">ret</span></span>  | <span data-ttu-id="9b993-148">out</span><span class="sxs-lookup"><span data-stu-id="9b993-148">out</span></span>    | [<span data-ttu-id="9b993-149">**ve**</span><span class="sxs-lookup"><span data-stu-id="9b993-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="9b993-150">**float**</span><span class="sxs-lookup"><span data-stu-id="9b993-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9b993-151">4</span><span class="sxs-lookup"><span data-stu-id="9b993-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9b993-152">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="9b993-152">Minimum Shader Model</span></span>

<span data-ttu-id="9b993-153">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b993-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9b993-154">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="9b993-154">Shader Model</span></span>                                              | <span data-ttu-id="9b993-155">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="9b993-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="9b993-156">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="9b993-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9b993-157">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="9b993-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="9b993-158">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b993-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9b993-159">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="9b993-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="9b993-160">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b993-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9b993-161">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="9b993-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="9b993-162">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b993-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9b993-163">nein</span><span class="sxs-lookup"><span data-stu-id="9b993-163">no</span></span>                       |



 

1.  <span data-ttu-id="9b993-164">Eine bedeutende Code Neuanordnung erfolgt, um Farbverlaufs Berechnungen außerhalb der Fluss Steuerung zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="9b993-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="9b993-165">Wenn die D3DPSHADERCAPS2 \_ 0-Obergrenze mit D3DD3DPSHADERCAPS2 \_ 0 \_ gradientinstructions festgelegt ist, ordnet der Compiler diese Funktion texldd zu.</span><span class="sxs-lookup"><span data-stu-id="9b993-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b993-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b993-166">Remarks</span></span>

<span data-ttu-id="9b993-167">Wenn die Fluss Steuerung in einem Shader vorhanden ist, ist das Ergebnis einer in einem bestimmten Verzweigungs Pfad angeforderten gradientenberechnung mehrdeutig, wenn angrenzende Pixel getrennte Fluss Steuerungs Pfade nach unten durchlaufen können.</span><span class="sxs-lookup"><span data-stu-id="9b993-167">When flow control is present in a shader, the result of a gradient calculation requested inside a given branch path is ambiguous when adjacent pixels may go down separate flow control paths.</span></span> <span data-ttu-id="9b993-168">Daher wird die Verwendung eines pixelshadervorgangs als unzulässig angesehen, der eine gradientenberechnung an einem Speicherort anfordert, der sich innerhalb eines Fluss Steuerungs Konstrukts befindet, das für ein bestimmtes primitiv, das gerengt wird, in Pixel variieren kann.</span><span class="sxs-lookup"><span data-stu-id="9b993-168">Therefore, it is deemed illegal to use any pixel shader operation that requests a gradient calculation to occur at a location that is inside a flow control construct which could vary across pixels for a given primitive being rasterized.</span></span> <span data-ttu-id="9b993-169">Wenn eine Seite einer **if** -Anweisung mit dem Branch-Attribut eine Gradient-Funktion verwendet, kann ein Compilerfehler generiert werden.</span><span class="sxs-lookup"><span data-stu-id="9b993-169">If either side of an **if** statement with the branch attribute uses a gradient function a compiler error may be generated.</span></span> <span data-ttu-id="9b993-170">Siehe [if-Anweisung (DirectX HLSL)](dx-graphics-hlsl-if.md).</span><span class="sxs-lookup"><span data-stu-id="9b993-170">See [if Statement (DirectX HLSL)](dx-graphics-hlsl-if.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9b993-171">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9b993-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b993-172">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="9b993-172">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

