---
title: tex3Dgrad
description: Stichproben eine 3D-Textur mithilfe eines Farbverlaufs, um die MIP-Ebene auszuwählen. | tex3Dgrad
ms.assetid: 230c42cc-31b7-4f57-ade4-14f069094d46
keywords:
- tex3Dgrad HLSL
topic_type:
- apiref
api_name:
- tex3Dgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4cd8188b7f39cc2b79eb2e961857732cd8dae9f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981569"
---
# <a name="tex3dgrad"></a><span data-ttu-id="693ed-105">tex3Dgrad</span><span class="sxs-lookup"><span data-stu-id="693ed-105">tex3Dgrad</span></span>

<span data-ttu-id="693ed-106">Stichproben eine 3D-Textur mithilfe eines Farbverlaufs, um die MIP-Ebene auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="693ed-106">Samples a 3D texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="693ed-107">Ret tex3Dgrad (s, t, DDX, ddY)</span><span class="sxs-lookup"><span data-stu-id="693ed-107">ret tex3Dgrad(s, t, ddx, ddy)</span></span> |
|-------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="693ed-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="693ed-108">Parameters</span></span>



| <span data-ttu-id="693ed-109">Element</span><span class="sxs-lookup"><span data-stu-id="693ed-109">Item</span></span>                                                         | <span data-ttu-id="693ed-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="693ed-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="693ed-111"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="693ed-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="693ed-112">\[im \] samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="693ed-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="693ed-113"><span id="t"></span><span id="T"></span>*Bund*</span><span class="sxs-lookup"><span data-stu-id="693ed-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="693ed-114">\[in \] der Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="693ed-114">\[in\] The texture coordinate.</span></span><br/>                                    |
| <span data-ttu-id="693ed-115"><span id="ddx"></span><span id="DDX"></span>*DDX*</span><span class="sxs-lookup"><span data-stu-id="693ed-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="693ed-116">\[\]die Änderungs Rate der Oberflächengeometrie in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="693ed-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="693ed-117"><span id="ddy"></span><span id="DDY"></span>*tziger*</span><span class="sxs-lookup"><span data-stu-id="693ed-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="693ed-118">\[\]die Änderungs Rate der Oberflächengeometrie in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="693ed-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="693ed-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="693ed-119">Return Value</span></span>

<span data-ttu-id="693ed-120">Der Wert der Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="693ed-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="693ed-121">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="693ed-121">Type Description</span></span>



| <span data-ttu-id="693ed-122">Name</span><span class="sxs-lookup"><span data-stu-id="693ed-122">Name</span></span> | <span data-ttu-id="693ed-123">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="693ed-123">In/Out</span></span> | [<span data-ttu-id="693ed-124">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="693ed-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="693ed-125">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="693ed-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="693ed-126">Size</span><span class="sxs-lookup"><span data-stu-id="693ed-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="693ed-127">s</span><span class="sxs-lookup"><span data-stu-id="693ed-127">s</span></span>    | <span data-ttu-id="693ed-128">in</span><span class="sxs-lookup"><span data-stu-id="693ed-128">in</span></span>     | [<span data-ttu-id="693ed-129">**Objekt**</span><span class="sxs-lookup"><span data-stu-id="693ed-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="693ed-130">sampler3D</span><span class="sxs-lookup"><span data-stu-id="693ed-130">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="693ed-131">1</span><span class="sxs-lookup"><span data-stu-id="693ed-131">1</span></span>    |
| <span data-ttu-id="693ed-132">t</span><span class="sxs-lookup"><span data-stu-id="693ed-132">t</span></span>    | <span data-ttu-id="693ed-133">in</span><span class="sxs-lookup"><span data-stu-id="693ed-133">in</span></span>     | [<span data-ttu-id="693ed-134">**ve**</span><span class="sxs-lookup"><span data-stu-id="693ed-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="693ed-135">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="693ed-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="693ed-136">3</span><span class="sxs-lookup"><span data-stu-id="693ed-136">3</span></span>    |
| <span data-ttu-id="693ed-137">DDX</span><span class="sxs-lookup"><span data-stu-id="693ed-137">ddx</span></span>  | <span data-ttu-id="693ed-138">in</span><span class="sxs-lookup"><span data-stu-id="693ed-138">in</span></span>     | [<span data-ttu-id="693ed-139">**ve**</span><span class="sxs-lookup"><span data-stu-id="693ed-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="693ed-140">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="693ed-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="693ed-141">3</span><span class="sxs-lookup"><span data-stu-id="693ed-141">3</span></span>    |
| <span data-ttu-id="693ed-142">tziger</span><span class="sxs-lookup"><span data-stu-id="693ed-142">ddy</span></span>  | <span data-ttu-id="693ed-143">in</span><span class="sxs-lookup"><span data-stu-id="693ed-143">in</span></span>     | [<span data-ttu-id="693ed-144">**ve**</span><span class="sxs-lookup"><span data-stu-id="693ed-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="693ed-145">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="693ed-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="693ed-146">3</span><span class="sxs-lookup"><span data-stu-id="693ed-146">3</span></span>    |
| <span data-ttu-id="693ed-147">TZI</span><span class="sxs-lookup"><span data-stu-id="693ed-147">ret</span></span>  | <span data-ttu-id="693ed-148">out</span><span class="sxs-lookup"><span data-stu-id="693ed-148">out</span></span>    | [<span data-ttu-id="693ed-149">**ve**</span><span class="sxs-lookup"><span data-stu-id="693ed-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="693ed-150">**float**</span><span class="sxs-lookup"><span data-stu-id="693ed-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="693ed-151">4</span><span class="sxs-lookup"><span data-stu-id="693ed-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="693ed-152">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="693ed-152">Minimum Shader Model</span></span>

<span data-ttu-id="693ed-153">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="693ed-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="693ed-154">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="693ed-154">Shader Model</span></span>                                              | <span data-ttu-id="693ed-155">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="693ed-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="693ed-156">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="693ed-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="693ed-157">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="693ed-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="693ed-158">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="693ed-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="693ed-159">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="693ed-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="693ed-160">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="693ed-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="693ed-161">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="693ed-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="693ed-162">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="693ed-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="693ed-163">nein</span><span class="sxs-lookup"><span data-stu-id="693ed-163">no</span></span>                       |



 

1.  <span data-ttu-id="693ed-164">Eine bedeutende Code Neuanordnung erfolgt, um Farbverlaufs Berechnungen außerhalb der Fluss Steuerung zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="693ed-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="693ed-165">Wenn die D3DPSHADERCAPS2 \_ 0-Obergrenze mit D3DD3DPSHADERCAPS2 \_ 0 \_ gradientinstructions festgelegt ist, ordnet der Compiler diese Funktion texldd zu.</span><span class="sxs-lookup"><span data-stu-id="693ed-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="remarks"></a><span data-ttu-id="693ed-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="693ed-166">Remarks</span></span>

<span data-ttu-id="693ed-167">Wenn die Fluss Steuerung in einem Shader vorhanden ist, ist das Ergebnis einer in einem bestimmten Verzweigungs Pfad angeforderten gradientenberechnung mehrdeutig, wenn angrenzende Pixel getrennte Fluss Steuerungs Pfade nach unten durchlaufen können.</span><span class="sxs-lookup"><span data-stu-id="693ed-167">When flow control is present in a shader, the result of a gradient calculation requested inside a given branch path is ambiguous when adjacent pixels may go down separate flow control paths.</span></span> <span data-ttu-id="693ed-168">Daher wird die Verwendung eines pixelshadervorgangs als unzulässig angesehen, der eine gradientenberechnung an einem Speicherort anfordert, der sich innerhalb eines Fluss Steuerungs Konstrukts befindet, das für ein bestimmtes primitiv, das gerengt wird, in Pixel variieren kann.</span><span class="sxs-lookup"><span data-stu-id="693ed-168">Therefore, it is deemed illegal to use any pixel shader operation that requests a gradient calculation to occur at a location that is inside a flow control construct which could vary across pixels for a given primitive being rasterized.</span></span> <span data-ttu-id="693ed-169">Wenn eine Seite einer **if** -Anweisung mit dem Branch-Attribut eine Gradient-Funktion verwendet, kann ein Compilerfehler generiert werden.</span><span class="sxs-lookup"><span data-stu-id="693ed-169">If either side of an **if** statement with the branch attribute uses a gradient function a compiler error may be generated.</span></span> <span data-ttu-id="693ed-170">Siehe [if-Anweisung (DirectX HLSL)](dx-graphics-hlsl-if.md).</span><span class="sxs-lookup"><span data-stu-id="693ed-170">See [if Statement (DirectX HLSL)](dx-graphics-hlsl-if.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="693ed-171">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="693ed-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="693ed-172">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="693ed-172">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

