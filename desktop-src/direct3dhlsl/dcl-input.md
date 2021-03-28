---
title: dcl_input (SM4-ASM)
description: DCL \_ -Eingabe (SM4-ASM)
ms.assetid: 13456f2a-ee6c-42da-a9fe-670ab0fcbddf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 400a1d47b6e0f9d82ec662553c36629deb4b1f0b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993230"
---
# <a name="dcl_input-sm4---asm"></a><span data-ttu-id="97392-103">DCL \_ -Eingabe (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="97392-103">dcl\_input (sm4 - asm)</span></span>

<span data-ttu-id="97392-104">Deklariert ein Shader-Input-Register.</span><span class="sxs-lookup"><span data-stu-id="97392-104">Declares a shader-input register.</span></span>



| <span data-ttu-id="97392-105">DCL- \_ Eingabe *v \[ . mask \] \[ , InterpolationMode \]*</span><span class="sxs-lookup"><span data-stu-id="97392-105">dcl\_input v *N\[.mask\]\[, interpolationMode\]*</span></span> |
|-------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="97392-106">Element</span><span class="sxs-lookup"><span data-stu-id="97392-106">Item</span></span></th>
<th><span data-ttu-id="97392-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97392-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="97392-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N [. mask]</em></span><span class="sxs-lookup"><span data-stu-id="97392-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N[.mask]</em></span></span><br/></td>
<td><span data-ttu-id="97392-109">in Ein Scheitelpunkt Datenregister.</span><span class="sxs-lookup"><span data-stu-id="97392-109">[in] A vertex data register.</span></span> <br/>
<ul>
<li><span data-ttu-id="97392-110"><em>N</em> ist eine ganze Zahl, die die Registernummer identifiziert.</span><span class="sxs-lookup"><span data-stu-id="97392-110"><em>N</em> is an integer that identifies the register number.</span></span></li>
<li><span data-ttu-id="97392-111"><em>[. mask]</em> ist eine optionale Komponenten Maske (. xyzw), die angibt, welche der zu verwendenden Registrierungs Komponenten verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="97392-111"><em>[.mask]</em> is an optional component mask (.xyzw) that specifies which of the register components to use.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97392-112"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>InterpolationMode</em></span><span class="sxs-lookup"><span data-stu-id="97392-112"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em></span></span><br/></td>
<td><span data-ttu-id="97392-113">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="97392-113">[in] Optional.</span></span> <span data-ttu-id="97392-114">Der Interpolations Modus, der nur für Pixel-Shader-Eingabe Register berücksichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="97392-114">The interpolation mode, which is only honored on pixel shader input registers.</span></span> <span data-ttu-id="97392-115">Es kann sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="97392-115">It can be one of the following values:</span></span> <br/>
<ul>
<li><span data-ttu-id="97392-116">Constant-interpolieren nicht zwischen Register Werten.</span><span class="sxs-lookup"><span data-stu-id="97392-116">constant - do not interpolate between register values.</span></span></li>
<li><span data-ttu-id="97392-117">Linear-interpolieren linear zwischen den Register Werten.</span><span class="sxs-lookup"><span data-stu-id="97392-117">linear - interpolate linearly between register values.</span></span></li>
<li><span data-ttu-id="97392-118">linearcentroid-identisch mit linear, aber Schwerpunkt beim Multisampling.</span><span class="sxs-lookup"><span data-stu-id="97392-118">linearCentroid - same as linear but centroid clamped when multisampling.</span></span></li>
<li><span data-ttu-id="97392-119">linearnoperspektive-identisch mit linear, aber ohne Perspektiven Korrektur.</span><span class="sxs-lookup"><span data-stu-id="97392-119">linearNoperspective - same as linear but with no perspective correction.</span></span></li>
<li><span data-ttu-id="97392-120">linearnoperspectivecentroid-identisch mit linear, Schwerpunkt bei Multisampling, keine Perspektiven Korrektur.</span><span class="sxs-lookup"><span data-stu-id="97392-120">linearNoperspectiveCentroid - same as linear, centroid clamped when multisampling, no perspective correction.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-notes"></a><span data-ttu-id="97392-121">Interpolations Hinweise</span><span class="sxs-lookup"><span data-stu-id="97392-121">Interpolation Notes</span></span>

<span data-ttu-id="97392-122">Standardmäßig werden Vertex-Attribute bei der Durchführung von Multisampling-Antialiasing von einem Pixel Center interpoliert.</span><span class="sxs-lookup"><span data-stu-id="97392-122">By default, vertex attributes are interpolated from a pixel center when performing multisample antialiasing.</span></span> <span data-ttu-id="97392-123">Wenn ein Pixel Center nicht abgedeckt wird, wird ein Attribut vor der interpolung zu einem Pixel Center hoch-</span><span class="sxs-lookup"><span data-stu-id="97392-123">If a pixel center is not covered, an attribute is extrapolated to a pixel center before interpolation.</span></span>

<span data-ttu-id="97392-124">Bei einem Pixel, das nicht vollständig abgedeckt ist, oder bei einem Attribut, das kein Pixel Center abdeckt, können Sie eine Schwerpunkt-Stichprobenentnahme angeben, die erzwingt, dass die Stichprobenentnahme irgendwo innerhalb des betroffenen Bereichs des Pixels erfolgt.</span><span class="sxs-lookup"><span data-stu-id="97392-124">For a pixel that is not fully covered or an attribute that does not cover a pixel center, you can specify centroid sampling which forces sampling to occur somewhere within the covered area of the pixel.</span></span> <span data-ttu-id="97392-125">Da eine Beispiel Maske (sofern verwendet) vor dem Berechnen des Schwerpunkts angewendet wird, kann der von der Beispiel Maske maskierte Beispiel Speicherort nicht als Schwerpunkt ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="97392-125">Because a sample mask (if used) is applied before the centroid is computed, any sample location masked out by the sample mask cannot be chosen as a centroid location.</span></span>

<span data-ttu-id="97392-126">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="97392-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="97392-127">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="97392-127">Vertex Shader</span></span> | <span data-ttu-id="97392-128">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="97392-128">Geometry Shader</span></span> | <span data-ttu-id="97392-129">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="97392-129">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="97392-130">x</span><span class="sxs-lookup"><span data-stu-id="97392-130">x</span></span>             | <span data-ttu-id="97392-131">x</span><span class="sxs-lookup"><span data-stu-id="97392-131">x</span></span>               | <span data-ttu-id="97392-132">x</span><span class="sxs-lookup"><span data-stu-id="97392-132">x</span></span>            |



 

<span data-ttu-id="97392-133">Verwenden Sie [DCL \_ input \_ SV (SM4-ASM)](dcl-input-sv.md), um die Eingabe als System Wert zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="97392-133">To identify the input as a system value, use [dcl\_input\_sv (sm4 - asm)](dcl-input-sv.md).</span></span>

<span data-ttu-id="97392-134">Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="97392-134">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="97392-135">Beispiel</span><span class="sxs-lookup"><span data-stu-id="97392-135">Example</span></span>

<span data-ttu-id="97392-136">Hier einige Beispiele.</span><span class="sxs-lookup"><span data-stu-id="97392-136">Here are some examples.</span></span>


```
dcl_input v3.xyz

dcl_input v0.x, linearCentroid
```



## <a name="minimum-shader-model"></a><span data-ttu-id="97392-137">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="97392-137">Minimum Shader Model</span></span>

<span data-ttu-id="97392-138">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="97392-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="97392-139">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="97392-139">Shader Model</span></span>                                              | <span data-ttu-id="97392-140">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="97392-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="97392-141">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="97392-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="97392-142">ja</span><span class="sxs-lookup"><span data-stu-id="97392-142">yes</span></span>       |
| [<span data-ttu-id="97392-143">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="97392-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="97392-144">ja</span><span class="sxs-lookup"><span data-stu-id="97392-144">yes</span></span>       |
| [<span data-ttu-id="97392-145">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="97392-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="97392-146">ja</span><span class="sxs-lookup"><span data-stu-id="97392-146">yes</span></span>       |
| [<span data-ttu-id="97392-147">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="97392-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="97392-148">nein</span><span class="sxs-lookup"><span data-stu-id="97392-148">no</span></span>        |
| [<span data-ttu-id="97392-149">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="97392-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="97392-150">nein</span><span class="sxs-lookup"><span data-stu-id="97392-150">no</span></span>        |
| [<span data-ttu-id="97392-151">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="97392-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="97392-152">nein</span><span class="sxs-lookup"><span data-stu-id="97392-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="97392-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="97392-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97392-154">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="97392-154">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





