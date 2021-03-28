---
title: 'tex2D (HLSL-Referenz): Wählen Sie die MIP-Ebene aus.'
description: Stichproben eine 2D-Textur mit einem Farbverlauf, um die MIP-Ebene auszuwählen. | tex2D (HLSL-Referenz)
ms.assetid: 0e8c32ed-d174-4045-9cbf-6c04586ea5bb
keywords:
- tex2D HLSL
topic_type:
- apiref
api_name:
- tex2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5a642a92756f3f0774e5719aa1fcf9ec302eecb5
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982693"
---
# <a name="tex2d-hlsl-reference---select-the-mip-level"></a><span data-ttu-id="048e2-105">tex2D (HLSL-Referenz): Wählen Sie die MIP-Ebene aus.</span><span class="sxs-lookup"><span data-stu-id="048e2-105">tex2D (HLSL reference) - Select the mip level</span></span>

<span data-ttu-id="048e2-106">Stichproben eine 2D-Textur mit einem Farbverlauf, um die MIP-Ebene auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="048e2-106">Samples a 2D texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="048e2-107">Ret tex2D (s, t, DDX, ddY)</span><span class="sxs-lookup"><span data-stu-id="048e2-107">ret tex2D(s, t, ddx, ddy)</span></span> |
|---------------------------|



 

## <a name="parameters"></a><span data-ttu-id="048e2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="048e2-108">Parameters</span></span>



| <span data-ttu-id="048e2-109">Element</span><span class="sxs-lookup"><span data-stu-id="048e2-109">Item</span></span>                                                         | <span data-ttu-id="048e2-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="048e2-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="048e2-111"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="048e2-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="048e2-112">\[im \] samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="048e2-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="048e2-113"><span id="t"></span><span id="T"></span>*Bund*</span><span class="sxs-lookup"><span data-stu-id="048e2-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="048e2-114">\[in \] den Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="048e2-114">\[in\] The texture coordinates.</span></span><br/>                                   |
| <span data-ttu-id="048e2-115"><span id="ddx"></span><span id="DDX"></span>*DDX*</span><span class="sxs-lookup"><span data-stu-id="048e2-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="048e2-116">\[\]die Änderungs Rate der Oberflächengeometrie in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="048e2-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="048e2-117"><span id="ddy"></span><span id="DDY"></span>*tziger*</span><span class="sxs-lookup"><span data-stu-id="048e2-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="048e2-118">\[\]die Änderungs Rate der Oberflächengeometrie in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="048e2-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="048e2-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="048e2-119">Return Value</span></span>

<span data-ttu-id="048e2-120">Der Wert der Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="048e2-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="048e2-121">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="048e2-121">Type Description</span></span>



| <span data-ttu-id="048e2-122">Name</span><span class="sxs-lookup"><span data-stu-id="048e2-122">Name</span></span> | <span data-ttu-id="048e2-123">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="048e2-123">In/Out</span></span> | [<span data-ttu-id="048e2-124">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="048e2-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="048e2-125">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="048e2-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="048e2-126">Size</span><span class="sxs-lookup"><span data-stu-id="048e2-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="048e2-127">s</span><span class="sxs-lookup"><span data-stu-id="048e2-127">s</span></span>    | <span data-ttu-id="048e2-128">in</span><span class="sxs-lookup"><span data-stu-id="048e2-128">in</span></span>     | [<span data-ttu-id="048e2-129">**Objekt**</span><span class="sxs-lookup"><span data-stu-id="048e2-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="048e2-130">sampler2D</span><span class="sxs-lookup"><span data-stu-id="048e2-130">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="048e2-131">1</span><span class="sxs-lookup"><span data-stu-id="048e2-131">1</span></span>    |
| <span data-ttu-id="048e2-132">t</span><span class="sxs-lookup"><span data-stu-id="048e2-132">t</span></span>    | <span data-ttu-id="048e2-133">in</span><span class="sxs-lookup"><span data-stu-id="048e2-133">in</span></span>     | [<span data-ttu-id="048e2-134">**ve**</span><span class="sxs-lookup"><span data-stu-id="048e2-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="048e2-135">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="048e2-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="048e2-136">2</span><span class="sxs-lookup"><span data-stu-id="048e2-136">2</span></span>    |
| <span data-ttu-id="048e2-137">DDX</span><span class="sxs-lookup"><span data-stu-id="048e2-137">ddx</span></span>  | <span data-ttu-id="048e2-138">in</span><span class="sxs-lookup"><span data-stu-id="048e2-138">in</span></span>     | [<span data-ttu-id="048e2-139">**ve**</span><span class="sxs-lookup"><span data-stu-id="048e2-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="048e2-140">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="048e2-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="048e2-141">2</span><span class="sxs-lookup"><span data-stu-id="048e2-141">2</span></span>    |
| <span data-ttu-id="048e2-142">tziger</span><span class="sxs-lookup"><span data-stu-id="048e2-142">ddy</span></span>  | <span data-ttu-id="048e2-143">in</span><span class="sxs-lookup"><span data-stu-id="048e2-143">in</span></span>     | [<span data-ttu-id="048e2-144">**ve**</span><span class="sxs-lookup"><span data-stu-id="048e2-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="048e2-145">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="048e2-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="048e2-146">2</span><span class="sxs-lookup"><span data-stu-id="048e2-146">2</span></span>    |
| <span data-ttu-id="048e2-147">TZI</span><span class="sxs-lookup"><span data-stu-id="048e2-147">ret</span></span>  | <span data-ttu-id="048e2-148">out</span><span class="sxs-lookup"><span data-stu-id="048e2-148">out</span></span>    | [<span data-ttu-id="048e2-149">**ve**</span><span class="sxs-lookup"><span data-stu-id="048e2-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="048e2-150">**float**</span><span class="sxs-lookup"><span data-stu-id="048e2-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="048e2-151">4</span><span class="sxs-lookup"><span data-stu-id="048e2-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="048e2-152">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="048e2-152">Minimum Shader Model</span></span>

<span data-ttu-id="048e2-153">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="048e2-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="048e2-154">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="048e2-154">Shader Model</span></span>                                              | <span data-ttu-id="048e2-155">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="048e2-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="048e2-156">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="048e2-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="048e2-157">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="048e2-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="048e2-158">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="048e2-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="048e2-159">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="048e2-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="048e2-160">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="048e2-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="048e2-161">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="048e2-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="048e2-162">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="048e2-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="048e2-163">nein</span><span class="sxs-lookup"><span data-stu-id="048e2-163">no</span></span>                       |



 

1.  <span data-ttu-id="048e2-164">Eine bedeutende Code Neuanordnung erfolgt, um Farbverlaufs Berechnungen außerhalb der Fluss Steuerung zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="048e2-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="048e2-165">Wenn die D3DPSHADERCAPS2 \_ 0-Obergrenze mit D3DD3DPSHADERCAPS2 \_ 0 \_ gradientinstructions festgelegt ist, ordnet der Compiler diese Funktion texldd zu.</span><span class="sxs-lookup"><span data-stu-id="048e2-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="remarks"></a><span data-ttu-id="048e2-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="048e2-166">Remarks</span></span>

<span data-ttu-id="048e2-167">Wenn die Fluss Steuerung in einem Shader vorhanden ist, ist das Ergebnis einer in einem bestimmten Verzweigungs Pfad angeforderten gradientenberechnung mehrdeutig, wenn angrenzende Pixel getrennte Fluss Steuerungs Pfade nach unten durchlaufen können.</span><span class="sxs-lookup"><span data-stu-id="048e2-167">When flow control is present in a shader, the result of a gradient calculation requested inside a given branch path is ambiguous when adjacent pixels may go down separate flow control paths.</span></span> <span data-ttu-id="048e2-168">Daher wird die Verwendung eines pixelshadervorgangs als unzulässig angesehen, der eine gradientenberechnung an einem Speicherort anfordert, der sich innerhalb eines Fluss Steuerungs Konstrukts befindet, das für ein bestimmtes primitiv, das gerengt wird, in Pixel variieren kann.</span><span class="sxs-lookup"><span data-stu-id="048e2-168">Therefore, it is deemed illegal to use any pixel shader operation that requests a gradient calculation to occur at a location that is inside a flow control construct which could vary across pixels for a given primitive being rasterized.</span></span> <span data-ttu-id="048e2-169">Wenn eine Seite einer **if** -Anweisung mit dem Branch-Attribut eine Gradient-Funktion verwendet, kann ein Compilerfehler generiert werden.</span><span class="sxs-lookup"><span data-stu-id="048e2-169">If either side of an **if** statement with the branch attribute uses a gradient function a compiler error may be generated.</span></span> <span data-ttu-id="048e2-170">Siehe [if-Anweisung (DirectX HLSL)](dx-graphics-hlsl-if.md).</span><span class="sxs-lookup"><span data-stu-id="048e2-170">See [if Statement (DirectX HLSL)](dx-graphics-hlsl-if.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="048e2-171">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="048e2-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="048e2-172">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="048e2-172">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

