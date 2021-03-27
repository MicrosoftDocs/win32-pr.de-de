---
title: 'tex3D (HLSL-Referenz): Wählen Sie die MIP-Ebene aus.'
description: Stichproben eine 3D-Textur mithilfe eines Farbverlaufs, um die MIP-Ebene auszuwählen. | tex3D (HLSL-Referenz)
ms.assetid: b48a6791-61b7-4a13-9357-923910515164
keywords:
- tex3D HLSL
topic_type:
- apiref
api_name:
- tex3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 965c9229d4d54fafdb2da9a84119365075a3f903
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104219729"
---
# <a name="tex3d-hlsl-reference---select-the-mip-level"></a><span data-ttu-id="f1feb-105">tex3D (HLSL-Referenz): Wählen Sie die MIP-Ebene aus.</span><span class="sxs-lookup"><span data-stu-id="f1feb-105">tex3D (HLSL reference) - Select the mip level</span></span>

<span data-ttu-id="f1feb-106">Stichproben eine 3D-Textur mithilfe eines Farbverlaufs, um die MIP-Ebene auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="f1feb-106">Samples a 3D texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="f1feb-107">Ret tex3D (s, t, DDX, ddY)</span><span class="sxs-lookup"><span data-stu-id="f1feb-107">ret tex3D(s, t, ddx, ddy)</span></span> |
|---------------------------|



 

## <a name="parameters"></a><span data-ttu-id="f1feb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1feb-108">Parameters</span></span>



| <span data-ttu-id="f1feb-109">Element</span><span class="sxs-lookup"><span data-stu-id="f1feb-109">Item</span></span>                                                         | <span data-ttu-id="f1feb-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1feb-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f1feb-111"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="f1feb-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="f1feb-112">\[im \] samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="f1feb-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="f1feb-113"><span id="t"></span><span id="T"></span>*Bund*</span><span class="sxs-lookup"><span data-stu-id="f1feb-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="f1feb-114">\[in \] der Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="f1feb-114">\[in\] The texture coordinate.</span></span><br/>                                    |
| <span data-ttu-id="f1feb-115"><span id="ddx"></span><span id="DDX"></span>*DDX*</span><span class="sxs-lookup"><span data-stu-id="f1feb-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="f1feb-116">\[\]die Änderungs Rate der Oberflächengeometrie in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="f1feb-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="f1feb-117"><span id="ddy"></span><span id="DDY"></span>*tziger*</span><span class="sxs-lookup"><span data-stu-id="f1feb-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="f1feb-118">\[\]die Änderungs Rate der Oberflächengeometrie in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="f1feb-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="f1feb-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f1feb-119">Return Value</span></span>

<span data-ttu-id="f1feb-120">Der Wert der Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="f1feb-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="f1feb-121">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="f1feb-121">Type Description</span></span>



| <span data-ttu-id="f1feb-122">Name</span><span class="sxs-lookup"><span data-stu-id="f1feb-122">Name</span></span> | <span data-ttu-id="f1feb-123">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="f1feb-123">In/Out</span></span> | [<span data-ttu-id="f1feb-124">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="f1feb-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="f1feb-125">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="f1feb-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="f1feb-126">Size</span><span class="sxs-lookup"><span data-stu-id="f1feb-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="f1feb-127">s</span><span class="sxs-lookup"><span data-stu-id="f1feb-127">s</span></span>    | <span data-ttu-id="f1feb-128">in</span><span class="sxs-lookup"><span data-stu-id="f1feb-128">in</span></span>     | [<span data-ttu-id="f1feb-129">**Objekt**</span><span class="sxs-lookup"><span data-stu-id="f1feb-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="f1feb-130">sampler3D</span><span class="sxs-lookup"><span data-stu-id="f1feb-130">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="f1feb-131">1</span><span class="sxs-lookup"><span data-stu-id="f1feb-131">1</span></span>    |
| <span data-ttu-id="f1feb-132">t</span><span class="sxs-lookup"><span data-stu-id="f1feb-132">t</span></span>    | <span data-ttu-id="f1feb-133">in</span><span class="sxs-lookup"><span data-stu-id="f1feb-133">in</span></span>     | [<span data-ttu-id="f1feb-134">**ve**</span><span class="sxs-lookup"><span data-stu-id="f1feb-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="f1feb-135">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="f1feb-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f1feb-136">3</span><span class="sxs-lookup"><span data-stu-id="f1feb-136">3</span></span>    |
| <span data-ttu-id="f1feb-137">DDX</span><span class="sxs-lookup"><span data-stu-id="f1feb-137">ddx</span></span>  | <span data-ttu-id="f1feb-138">in</span><span class="sxs-lookup"><span data-stu-id="f1feb-138">in</span></span>     | [<span data-ttu-id="f1feb-139">**ve**</span><span class="sxs-lookup"><span data-stu-id="f1feb-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="f1feb-140">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="f1feb-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f1feb-141">3</span><span class="sxs-lookup"><span data-stu-id="f1feb-141">3</span></span>    |
| <span data-ttu-id="f1feb-142">tziger</span><span class="sxs-lookup"><span data-stu-id="f1feb-142">ddy</span></span>  | <span data-ttu-id="f1feb-143">in</span><span class="sxs-lookup"><span data-stu-id="f1feb-143">in</span></span>     | [<span data-ttu-id="f1feb-144">**ve**</span><span class="sxs-lookup"><span data-stu-id="f1feb-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="f1feb-145">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="f1feb-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f1feb-146">3</span><span class="sxs-lookup"><span data-stu-id="f1feb-146">3</span></span>    |
| <span data-ttu-id="f1feb-147">TZI</span><span class="sxs-lookup"><span data-stu-id="f1feb-147">ret</span></span>  | <span data-ttu-id="f1feb-148">out</span><span class="sxs-lookup"><span data-stu-id="f1feb-148">out</span></span>    | [<span data-ttu-id="f1feb-149">**ve**</span><span class="sxs-lookup"><span data-stu-id="f1feb-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="f1feb-150">**float**</span><span class="sxs-lookup"><span data-stu-id="f1feb-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f1feb-151">4</span><span class="sxs-lookup"><span data-stu-id="f1feb-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f1feb-152">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="f1feb-152">Minimum Shader Model</span></span>

<span data-ttu-id="f1feb-153">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f1feb-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f1feb-154">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="f1feb-154">Shader Model</span></span>                                              | <span data-ttu-id="f1feb-155">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="f1feb-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="f1feb-156">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="f1feb-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f1feb-157">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="f1feb-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="f1feb-158">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f1feb-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f1feb-159">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="f1feb-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="f1feb-160">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f1feb-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f1feb-161">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="f1feb-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="f1feb-162">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f1feb-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f1feb-163">nein</span><span class="sxs-lookup"><span data-stu-id="f1feb-163">no</span></span>                       |



 

1.  <span data-ttu-id="f1feb-164">Eine bedeutende Code Neuanordnung erfolgt, um Farbverlaufs Berechnungen außerhalb der Fluss Steuerung zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="f1feb-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="f1feb-165">Wenn die D3DPSHADERCAPS2 \_ 0-Obergrenze mit D3DD3DPSHADERCAPS2 \_ 0 \_ gradientinstructions festgelegt ist, ordnet der Compiler diese Funktion texldd zu.</span><span class="sxs-lookup"><span data-stu-id="f1feb-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1feb-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1feb-166">Remarks</span></span>

<span data-ttu-id="f1feb-167">Wenn die Fluss Steuerung in einem Shader vorhanden ist, ist das Ergebnis einer in einem bestimmten Verzweigungs Pfad angeforderten gradientenberechnung mehrdeutig, wenn angrenzende Pixel getrennte Fluss Steuerungs Pfade nach unten durchlaufen können.</span><span class="sxs-lookup"><span data-stu-id="f1feb-167">When flow control is present in a shader, the result of a gradient calculation requested inside a given branch path is ambiguous when adjacent pixels may go down separate flow control paths.</span></span> <span data-ttu-id="f1feb-168">Daher wird die Verwendung eines pixelshadervorgangs als unzulässig angesehen, der eine gradientenberechnung an einem Speicherort anfordert, der sich innerhalb eines Fluss Steuerungs Konstrukts befindet, das für ein bestimmtes primitiv, das gerengt wird, in Pixel variieren kann.</span><span class="sxs-lookup"><span data-stu-id="f1feb-168">Therefore, it is deemed illegal to use any pixel shader operation that requests a gradient calculation to occur at a location that is inside a flow control construct which could vary across pixels for a given primitive being rasterized.</span></span> <span data-ttu-id="f1feb-169">Wenn eine Seite einer **if** -Anweisung mit dem Branch-Attribut eine Gradient-Funktion verwendet, kann ein Compilerfehler generiert werden.</span><span class="sxs-lookup"><span data-stu-id="f1feb-169">If either side of an **if** statement with the branch attribute uses a gradient function a compiler error may be generated.</span></span> <span data-ttu-id="f1feb-170">Siehe [if-Anweisung (DirectX HLSL)](dx-graphics-hlsl-if.md).</span><span class="sxs-lookup"><span data-stu-id="f1feb-170">See [if Statement (DirectX HLSL)](dx-graphics-hlsl-if.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f1feb-171">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f1feb-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1feb-172">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="f1feb-172">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

