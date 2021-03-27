---
title: dcl_input_sv (SM4-ASM)
description: DCL- \_ Eingabe \_ SV (SM4-ASM)
ms.assetid: 59270148-e2eb-4525-a888-ad7e843d62a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 650196dff224259f48d1471f3005f95ec0de9c8b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719487"
---
# <a name="dcl_input_sv-sm4---asm"></a><span data-ttu-id="b3e26-103">DCL- \_ Eingabe \_ SV (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="b3e26-103">dcl\_input\_sv (sm4 - asm)</span></span>

<span data-ttu-id="b3e26-104">Deklariert ein Shader-Input-Register, das erwartet, dass ein [System Wert](dx-graphics-hlsl-semantics.md) aus einer vorherigen Phase bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b3e26-104">Declares a shader-input register that expects a [system-value](dx-graphics-hlsl-semantics.md) to be provided from a preceding stage.</span></span>



| <span data-ttu-id="b3e26-105">DCL- \_ Eingabe \_ SV v *N \[ . \] Mask*, *systemvaluename \[ , InterpolationMode \]*</span><span class="sxs-lookup"><span data-stu-id="b3e26-105">dcl\_input\_sv v *N\[.mask\]*, *systemValueName\[, interpolationMode\]*</span></span> |
|------------------------------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3e26-106">Element</span><span class="sxs-lookup"><span data-stu-id="b3e26-106">Item</span></span></th>
<th><span data-ttu-id="b3e26-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3e26-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3e26-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N [. mask]</em></span><span class="sxs-lookup"><span data-stu-id="b3e26-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N[.mask]</em></span></span><br/></td>
<td><span data-ttu-id="b3e26-109">in Ein Scheitelpunkt Datenregister.</span><span class="sxs-lookup"><span data-stu-id="b3e26-109">[in] A vertex data register.</span></span> <br/>
<ul>
<li><span data-ttu-id="b3e26-110"><em>N</em> ist eine ganze Zahl, die die Registernummer identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b3e26-110"><em>N</em> is an integer that identifies the register number.</span></span></li>
<li><span data-ttu-id="b3e26-111"><em>[. mask]</em> ist eine optionale Komponenten Maske (. xyzw), die angibt, welche der zu verwendenden Registrierungs Komponenten verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b3e26-111"><em>[.mask]</em> is an optional component mask (.xyzw) that specifies which of the register components to use.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3e26-112"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span><em>systemvaluename</em></span><span class="sxs-lookup"><span data-stu-id="b3e26-112"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span><em>systemValueName</em></span></span><br/></td>
<td><span data-ttu-id="b3e26-113">in Der Name des System Werts, bei dem es sich um eine Zeichenfolge (siehe <a href="dx-graphics-hlsl-semantics.md">System-Wert-Semantik</a>) ohne das &quot; &quot; Präfix SV_ handelt.</span><span class="sxs-lookup"><span data-stu-id="b3e26-113">[in] The system-value name which is a string (see <a href="dx-graphics-hlsl-semantics.md">system-value semantics</a>) without the &quot;SV_&quot; prefix.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3e26-114"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>InterpolationMode</em></span><span class="sxs-lookup"><span data-stu-id="b3e26-114"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em></span></span><br/></td>
<td><span data-ttu-id="b3e26-115">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="b3e26-115">[in] Optional.</span></span> <span data-ttu-id="b3e26-116">Der Interpolations Modus, der beeinflusst, wie Werte während der rasterisierung berechnet werden. der-Modus wird nur von einem Pixelshader verwendet.</span><span class="sxs-lookup"><span data-stu-id="b3e26-116">The interpolation mode which affects how values are calculated during rasterization; the mode is only used by a pixel shader.</span></span> <span data-ttu-id="b3e26-117">Es kann sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="b3e26-117">It can be one of the following values:</span></span> <br/>
<ul>
<li><span data-ttu-id="b3e26-118">Constant-interpolieren nicht zwischen Register Werten.</span><span class="sxs-lookup"><span data-stu-id="b3e26-118">constant - do not interpolate between register values.</span></span></li>
<li><span data-ttu-id="b3e26-119">Linear-interpolieren linear zwischen den Register Werten.</span><span class="sxs-lookup"><span data-stu-id="b3e26-119">linear - interpolate linearly between register values.</span></span></li>
<li><span data-ttu-id="b3e26-120">linearcentroid-identisch mit linear, aber Schwerpunkt beim Multisampling.</span><span class="sxs-lookup"><span data-stu-id="b3e26-120">linearCentroid - same as linear but centroid clamped when multisampling.</span></span></li>
<li><span data-ttu-id="b3e26-121">linearnoperspektive-identisch mit linear, aber ohne Perspektiven Korrektur.</span><span class="sxs-lookup"><span data-stu-id="b3e26-121">linearNoperspective - same as linear but with no perspective correction.</span></span></li>
<li><span data-ttu-id="b3e26-122">linearnoperspectivecentroid-identisch mit linear, aber ohne Perspektiven Korrektur und Schwerpunkt beim Multisampling.</span><span class="sxs-lookup"><span data-stu-id="b3e26-122">linearNoperspectiveCentroid - same as linear but with no perspective correction and centroid clamped when multisampling.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b3e26-123">Eine Komponenten Maske für eine System Wert Deklaration kann eine beliebige Teilmenge von \[ xyzw sein \] ; Deklarationen können sich möglicherweise nicht überlappen (jede Deklaration muss der Sequenz-xyzw entsprechen).</span><span class="sxs-lookup"><span data-stu-id="b3e26-123">A component mask for a system-value declaration can be any appropriate subset of \[xyzw\]; declarations may not overlap (each declaration must follow the sequence xyzw).</span></span> <span data-ttu-id="b3e26-124">Beim Deklarieren von skalaren System Werten (z. b. Clip Distance und Auslesen Distance) können Sie mehrere System Werte in einem einzelnen Register deklarieren.</span><span class="sxs-lookup"><span data-stu-id="b3e26-124">When declaring scalar system values (clip distance and cull distance for example), you can declare multiple system values in a single register.</span></span> <span data-ttu-id="b3e26-125">Stellen Sie in diesem Fall sicher, dass andere Modifizierer wie die Interpolations Modi Stimmen.</span><span class="sxs-lookup"><span data-stu-id="b3e26-125">If you do so, make sure other modifiers like the interpolation modes match.</span></span>

<span data-ttu-id="b3e26-126">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="b3e26-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b3e26-127">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="b3e26-127">Vertex Shader</span></span> | <span data-ttu-id="b3e26-128">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="b3e26-128">Geometry Shader</span></span> | <span data-ttu-id="b3e26-129">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="b3e26-129">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b3e26-130">x</span><span class="sxs-lookup"><span data-stu-id="b3e26-130">x</span></span>             | <span data-ttu-id="b3e26-131">x</span><span class="sxs-lookup"><span data-stu-id="b3e26-131">x</span></span>               | <span data-ttu-id="b3e26-132">x</span><span class="sxs-lookup"><span data-stu-id="b3e26-132">x</span></span>            |



 

<span data-ttu-id="b3e26-133">Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b3e26-133">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="b3e26-134">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b3e26-134">Example</span></span>

<span data-ttu-id="b3e26-135">Hier einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="b3e26-135">Here are some examples:</span></span>


```
// valid
dcl_input v0.y, linear
dcl_input_sv v0.w, clipDistance
dcl_input_sv v0.z, cullDistance
```




```
// invalid declarations
dcl_input v0.y, linear
dcl_input_sv v0.x, clipDistance  // the y component was previously declared, this declaration must use 
                                 // either the z or w component

dcl_input v0.y, linearNoPerspective                  // the interpolation mode is linear-no-perspective
dcl_input_sv v0.z, renderTargetArrayIndex, constant  // the interpolation modes is constant
                                                     // the interpolation modes must match
```



## <a name="minimum-shader-model"></a><span data-ttu-id="b3e26-136">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="b3e26-136">Minimum Shader Model</span></span>

<span data-ttu-id="b3e26-137">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b3e26-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b3e26-138">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="b3e26-138">Shader Model</span></span>                                              | <span data-ttu-id="b3e26-139">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="b3e26-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b3e26-140">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="b3e26-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b3e26-141">ja</span><span class="sxs-lookup"><span data-stu-id="b3e26-141">yes</span></span>       |
| [<span data-ttu-id="b3e26-142">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="b3e26-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b3e26-143">ja</span><span class="sxs-lookup"><span data-stu-id="b3e26-143">yes</span></span>       |
| [<span data-ttu-id="b3e26-144">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="b3e26-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b3e26-145">ja</span><span class="sxs-lookup"><span data-stu-id="b3e26-145">yes</span></span>       |
| [<span data-ttu-id="b3e26-146">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b3e26-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b3e26-147">nein</span><span class="sxs-lookup"><span data-stu-id="b3e26-147">no</span></span>        |
| [<span data-ttu-id="b3e26-148">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b3e26-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b3e26-149">nein</span><span class="sxs-lookup"><span data-stu-id="b3e26-149">no</span></span>        |
| [<span data-ttu-id="b3e26-150">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b3e26-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b3e26-151">nein</span><span class="sxs-lookup"><span data-stu-id="b3e26-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b3e26-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b3e26-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3e26-153">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b3e26-153">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





