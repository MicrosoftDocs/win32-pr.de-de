---
title: ld2dms (SM 4.1-ASM)
description: Liest einzelne Beispiele aus zweidimensionalen Multisample-Texturen.
ms.assetid: 8D92BFA8-4B22-46F3-876D-8D84BB3A96E7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9dd03b7c07f3fb25294dd0ad6aa382eb203560
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101090"
---
# <a name="ld2dms-sm41---asm"></a><span data-ttu-id="bda28-103">ld2dms (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="bda28-103">ld2dms (sm4.1 - asm)</span></span>

<span data-ttu-id="bda28-104">Liest einzelne Beispiele aus zweidimensionalen Multisample-Texturen.</span><span class="sxs-lookup"><span data-stu-id="bda28-104">Reads individual samples out of 2-dimensional multi-sample textures.</span></span>



| <span data-ttu-id="bda28-105">ld2dms \[ \_ aoffimmi (u, v) \] dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource \[ . Swizzle \] , sampleindex (skalare Operand)</span><span class="sxs-lookup"><span data-stu-id="bda28-105">ld2dms\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], sampleIndex (scalar operand)</span></span> |
|------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="bda28-106">Element</span><span class="sxs-lookup"><span data-stu-id="bda28-106">Item</span></span>                                                                                                               | <span data-ttu-id="bda28-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bda28-107">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bda28-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="bda28-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="bda28-109">\[in \] der Adresse des Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="bda28-109">\[in\] The address of result of the operation.</span></span> <br/>                                                                 |
| <span data-ttu-id="bda28-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*</span><span class="sxs-lookup"><span data-stu-id="bda28-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="bda28-111">\[in \] den Texturkoordinaten, die zum Ausführen des Beispiels erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="bda28-111">\[in\] The texture coordinates needed to perform the sample.</span></span><br/>                                                    |
| <span data-ttu-id="bda28-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*</span><span class="sxs-lookup"><span data-stu-id="bda28-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="bda28-113">\[in \] einem Textur Register (t \# ), das deklariert werden muss, um zu ermitteln, welche Textur oder welcher Puffer abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="bda28-113">\[in\] A texture register (t\#) which must have been declared identifying which Texture or Buffer to fetch from</span></span><br/> |
| <span data-ttu-id="bda28-114"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*Sample Index*</span><span class="sxs-lookup"><span data-stu-id="bda28-114"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span></span><br/> | <span data-ttu-id="bda28-115">\[in werden \] die Beispiele zum Lesen aus *srkresource* unterschieden.</span><span class="sxs-lookup"><span data-stu-id="bda28-115">\[in\] Idendifies the samples to read from *srcResource*.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="bda28-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bda28-116">Remarks</span></span>

<span data-ttu-id="bda28-117">Diese Anweisung ist eine vereinfachte Alternative zur [Beispiel](sample--sm4---asm-.md) Anweisung.</span><span class="sxs-lookup"><span data-stu-id="bda28-117">This instruction is a simplified alternative to the [sample](sample--sm4---asm-.md) instruction.</span></span> <span data-ttu-id="bda28-118">Er ruft Daten aus der angegebenen Textur ohne Filter (z. b. Punkt Stichproben) mithilfe der angegebenen Ganzzahl *srcaddress* und *sampleindex* ab.</span><span class="sxs-lookup"><span data-stu-id="bda28-118">It fetches data from the specified Texture without any filtering (e.g. point sampling) using the provided integer *srcAddress* and *sampleIndex*.</span></span>

<span data-ttu-id="bda28-119">*srcaddress* bietet den Satz von Texturkoordinaten, die zum Ausführen des Beispiels in Form von Ganzzahlen ohne Vorzeichen benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="bda28-119">*srcAddress* provides the set of texture coordinates needed to perform the sample in the form of unsigned integers.</span></span> <span data-ttu-id="bda28-120">Wenn *srcaddress* außerhalb des Bereichs \[ 0... liegt ( \# texeln in Dimension-1) \] , **ld2dms** gibt immer 0 (null) in allen Komponenten zurück, die im Format der Ressource vorhanden sind, und die Standardwerte (0, 0, 0, 1.0 f/0x00000001) für fehlende Komponenten.</span><span class="sxs-lookup"><span data-stu-id="bda28-120">If *srcAddress* is out of the range\[0...(\#texels in dimension -1)\], **ld2dms** always returns 0 in all components present in the format of the resource, and defaults (0,0,0,1.0f/0x00000001) for missing components.</span></span>

<span data-ttu-id="bda28-121">*sampleingedex* muss kein Literalwert sein.</span><span class="sxs-lookup"><span data-stu-id="bda28-121">*sampleIndex* does not have to be a literal.</span></span> <span data-ttu-id="bda28-122">Der Zähler für mehrere Stichproben muss nicht für die Textur Ressource angegeben werden, und er kann mit tiefen-oder Schablonen Ansichten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bda28-122">The multi-sample count does not have to be specified on the texture resource, and it works with depth or stencil views.</span></span>

<span data-ttu-id="bda28-123">Eine Anwendung, die eine flexiblere Kontrolle über das Adress Verhalten außerhalb des gültigen Bereichs hat, sollte stattdessen die **Beispiel** Anweisung verwenden, da Sie das als samplerzustand definierte Adress Umbruch-/Spiegelungs-/einspannen/Rahmen Verhalten berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="bda28-123">An application wishing any more flexible control over out-of-range address behavior should use the **sample** instruction instead, as it honors address wrap/mirror/clamp/border behavior defined as sampler state.</span></span>

<span data-ttu-id="bda28-124">*srcaddress. b* (Post-Swizzle) wird für Texture2Ds ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bda28-124">*srcAddress.b* (post-swizzle) is ignored for Texture2Ds.</span></span> <span data-ttu-id="bda28-125">, Wenn der Wert außerhalb des Bereichs der verfügbaren Array Indizes \[ 0 (null) liegt. Array Größe-1) \] , dann gibt **ld2dms** immer 0 (null) in allen Komponenten zurück, die im Format der Ressource vorhanden sind, und die Standardwerte (0, 0, 0, 1.0 f/0x00000001) für fehlende Komponenten.</span><span class="sxs-lookup"><span data-stu-id="bda28-125">If the value is out of the range of available array indices \[0...(array size-1)\], then **ld2dms** always returns 0 in all components present in the format of the resource, and defaults (0,0,0,1.0f/0x00000001) for missing components.</span></span>

<span data-ttu-id="bda28-126">Für Texture2D Arrays stellt *srcaddress. b* (Post-Swizzle) den Array Index bereit.</span><span class="sxs-lookup"><span data-stu-id="bda28-126">For Texture2D Arrays, *srcAddress.b* (post-swizzle) provides the array index.</span></span> <span data-ttu-id="bda28-127">Es hat das gleiche Verhalten wie Texture2D.</span><span class="sxs-lookup"><span data-stu-id="bda28-127">Oherwise it has the same behavior as Texture2D.</span></span>

<span data-ttu-id="bda28-128">*srcaddress. a* (Post-Swizzle) wird immer ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bda28-128">*srcAddress.a* (post-swizzle) is always ignored.</span></span> <span data-ttu-id="bda28-129">Der HLSL-Compiler gibt nichts an dieser Ausgabe aus.</span><span class="sxs-lookup"><span data-stu-id="bda28-129">The HLSL compiler will never output anything there.</span></span>

<span data-ttu-id="bda28-130">*srkresource* ist ein Textur Register (t \# ), das deklariert werden muss (22.3.11), und identifiziert, welche Textur abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="bda28-130">*srcResource* is a texture register (t\#) which must have been declared(22.3.11), identifying which Texture to fetch from.</span></span>

<span data-ttu-id="bda28-131">Wenn Sie von t abrufen \# , an das nichts gebunden ist, wird 0 für alle Komponenten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bda28-131">Fetching from t\# that has nothing bound to it returns 0 for all components.</span></span>

### <a name="address-offset"></a><span data-ttu-id="bda28-132">Adress Offset</span><span class="sxs-lookup"><span data-stu-id="bda28-132">Address Offset</span></span>

<span data-ttu-id="bda28-133">Das optionale \[ \_ aoffimmi (u, v, w)- \] Suffix (Address Offset by immediate Integer) gibt an, dass die Texturkoordinaten für die **ld2dms** durch eine Menge von bereitgestellten ganzzahligen ganzzahligen Werten für den unmittelbaren texspace versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="bda28-133">The optional \[\_aoffimmi(u,v,w)\] suffix (address offset by immediate integer) indicates that the texture coordinates for the **ld2dms** are to be offset by a set of provided immediate texel space integer constant values.</span></span> <span data-ttu-id="bda28-134">Bei den Literalwerten handelt es sich um einen Satz von 4 Bit 2-Komplement Nummern mit einem ganzzahligen Bereich von \[ 8, 7 \] .</span><span class="sxs-lookup"><span data-stu-id="bda28-134">The literal values are a set of 4 bit 2's complement numbers, having integer range \[-8,7\].</span></span>

<span data-ttu-id="bda28-135">Die Offsets werden den Texturkoordinaten in texspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bda28-135">The offsets are added to the texture coordinates, in texel space.</span></span>

<span data-ttu-id="bda28-136">Adress Offsets werden nicht an der Array Achse von Texture1D/2D-Arrays angewendet.</span><span class="sxs-lookup"><span data-stu-id="bda28-136">Address offsets are not applied along the array axis of Texture1D/2D Arrays.</span></span>

<span data-ttu-id="bda28-137">Die Komponenten " *\_ aoffimmi v" und "w* " werden bei Texture1Ds ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bda28-137">The *\_aoffimmi v,w* components are ignored for Texture1Ds.</span></span>

<span data-ttu-id="bda28-138">Die Komponente " *\_ aoffimmi w* " wird für Texture2Ds ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bda28-138">The *\_aoffimmi w* component is ignored for Texture2Ds.</span></span>

<span data-ttu-id="bda28-139">Da die Texturkoordinaten für **ld2dms** eine ganze Zahl ohne Vorzeichen sind, wird der Offset, wenn der Offset bewirkt, dass die Adresse unter 0 (null) wechselt, in eine große Adresse umschlossen und einen Out-of-Limit-Zugriff zur Folge hat, wie z. b. **LD** gibt 0 (null) in allen Komponenten zurück, die im Format der Ressource vorhanden sind</span><span class="sxs-lookup"><span data-stu-id="bda28-139">Because the texture coordinates for **ld2dms** are unsigned integers, if the offset causes the address to go below zero, it will wrap to a large address, and result in an out of bounds access, which like **ld** returns 0 in all components present in the format of the resource, and the defaults (0,0,0,1.0f/0x00000001) for missing components.</span></span>

### <a name="sample-number"></a><span data-ttu-id="bda28-140">Stichproben Nummer</span><span class="sxs-lookup"><span data-stu-id="bda28-140">Sample Number</span></span>

<span data-ttu-id="bda28-141">**ld2dms** ist für die Verwendung in einer beliebigen Ressource verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bda28-141">**ld2dms** is available for use on any resource.</span></span> <span data-ttu-id="bda28-142">**ld2dms** arbeitet mit Ausnahme von 2D-Multisample-Ressourcen identisch mit **LD** , indem der zusätzliche (0-basierte) *sampleindex* -Operand verwendet wird, um zu ermitteln, welches Beispiel aus der Ressource gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="bda28-142">**ld2dms** operates identically to **ld** except on 2D multsample resources, by using the additional (0-based) *sampleIndex* operand to identify which sample to read from the resource.</span></span>

<span data-ttu-id="bda28-143">Das Ergebnis der Angabe eines *samplindex* , der die Anzahl der Stichproben in der Ressource überschreitet, ist nicht definiert, aber es können keine Daten außerhalb des Adressraums des Geräte Kontexts zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bda28-143">The result of specifying a *sampleIndex* that exceeds the number of samples in the resource is undefined, but cannot return data outside of the address space of the device context.</span></span>

### <a name="return-type-control"></a><span data-ttu-id="bda28-144">Rückgabe-typsteuer Element</span><span class="sxs-lookup"><span data-stu-id="bda28-144">Return Type Control</span></span>

<span data-ttu-id="bda28-145">Das Datenformat, das von **ld2dms** an das Ziel Register zurückgegeben wird, wird auf die gleiche Weise wie für die **Beispiel** Anweisung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bda28-145">The data format returned by **ld2dms** to the destination register is determined in the same way as described for the **sample** instruction.</span></span> <span data-ttu-id="bda28-146">Sie basiert auf dem Format, das an den *srkresource* -Parameter (t) gebunden ist \# .</span><span class="sxs-lookup"><span data-stu-id="bda28-146">It is based on the format bound to the *srcResource* parameter (t\#).</span></span>

<span data-ttu-id="bda28-147">Wie bei der **Beispiel** Anweisung sind die zurückgegebenen Werte für **ld2dms** 4 Vektoren mit Format spezifischen Standardwerten für Komponenten, die nicht im-Format vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="bda28-147">As with the **sample** instruction, returned values for **ld2dms** are 4-vectors with format-specific defaults for components not present in the format.</span></span> <span data-ttu-id="bda28-148">Der Wert für " *srkresource* " hängt davon ab, wie das aus der Textur Auslastung zurückgegebene Ergebnis der 4-Komponente durch die Verwendung von ". Mask" unter " *dest* " bestimmt wird, welche Komponenten in *dest* aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="bda28-148">The swizzle on *srcResource* determines how to swizzle the 4-component result coming back from the texture load, after which .mask on *dest* determines which components in *dest* get updated.</span></span>

<span data-ttu-id="bda28-149">Wenn ein 32-Bit-Float-Wert von **ld2dms** in ein 32-Bit-Register gelesen wird, sind die Bits unverändert. Das heißt, die DENORMAL-Werte bleiben DENORMAL.</span><span class="sxs-lookup"><span data-stu-id="bda28-149">When a 32-bit float value is read by **ld2dms** into a 32-bit register, the bits are untouched; that is, denormal values remain denormal.</span></span> <span data-ttu-id="bda28-150">Dies ist anders als bei der **Beispiel** Anweisung.</span><span class="sxs-lookup"><span data-stu-id="bda28-150">This is unlike the **sample** instruction.</span></span>

### <a name="miscellaneous-details"></a><span data-ttu-id="bda28-151">Sonstige Details</span><span class="sxs-lookup"><span data-stu-id="bda28-151">Miscellaneous Details</span></span>

<span data-ttu-id="bda28-152">Da dieser Anweisung keine Filterung zugeordnet ist, gelten keine Konzepte wie Lod-Bias.</span><span class="sxs-lookup"><span data-stu-id="bda28-152">As there is no filtering associated with this instruction, concepts like LOD bias do not apply.</span></span> <span data-ttu-id="bda28-153">Dementsprechend gibt es keinen *Sampler \#* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="bda28-153">Accordingly there is no *sampler s\#* parameter.</span></span>

### <a name="restrictions"></a><span data-ttu-id="bda28-154">Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="bda28-154">Restrictions</span></span>

-   <span data-ttu-id="bda28-155">*srkresource* muss ein t \# -Register und kein texturecube, Texture1D oder Texture1DArray sein.</span><span class="sxs-lookup"><span data-stu-id="bda28-155">*srcResource* must be a t\# register, and not a TextureCube, Texture1D or Texture1DArray.</span></span> <span data-ttu-id="bda28-156">*srkresource* kann kein constantbuffer-Wert sein, der nicht an t-Register gebunden werden kann \# .</span><span class="sxs-lookup"><span data-stu-id="bda28-156">*srcResource* cannot be a ConstantBuffer, which cannot be bound to t\# registers.</span></span>
-   <span data-ttu-id="bda28-157">Die relative Adressierung in *srkresource* ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="bda28-157">Relative addressing on *srcResource* is not permitted.</span></span>
-   <span data-ttu-id="bda28-158">*srcaddress* und *sampleindex* müssen ein Temp-(r \# /x \# ), konstantes (CB \# ) oder Eingabe (v \# )-Register sein.</span><span class="sxs-lookup"><span data-stu-id="bda28-158">*srcAddress* and *sampleIndex* must be a temp (r\#/x\#), constant (cb\#) or input (v\#) register.</span></span>
-   <span data-ttu-id="bda28-159">*dest* muss ein Temp-(r \# /x \# ) oder Output (o \* \# )-Register sein.</span><span class="sxs-lookup"><span data-stu-id="bda28-159">*dest* must be a temp (r\#/x\#) or output (o\*\#) register.</span></span>

<span data-ttu-id="bda28-160">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="bda28-160">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bda28-161">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="bda28-161">Vertex Shader</span></span> | <span data-ttu-id="bda28-162">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="bda28-162">Geometry Shader</span></span> | <span data-ttu-id="bda28-163">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="bda28-163">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="bda28-164">x</span><span class="sxs-lookup"><span data-stu-id="bda28-164">x</span></span>             | <span data-ttu-id="bda28-165">x</span><span class="sxs-lookup"><span data-stu-id="bda28-165">x</span></span>               | <span data-ttu-id="bda28-166">x</span><span class="sxs-lookup"><span data-stu-id="bda28-166">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bda28-167">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="bda28-167">Minimum Shader Model</span></span>

<span data-ttu-id="bda28-168">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bda28-168">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bda28-169">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="bda28-169">Shader Model</span></span>                                              | <span data-ttu-id="bda28-170">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="bda28-170">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bda28-171">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="bda28-171">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bda28-172">ja</span><span class="sxs-lookup"><span data-stu-id="bda28-172">yes</span></span>       |
| [<span data-ttu-id="bda28-173">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="bda28-173">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bda28-174">ja</span><span class="sxs-lookup"><span data-stu-id="bda28-174">yes</span></span>       |
| [<span data-ttu-id="bda28-175">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="bda28-175">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bda28-176">nein</span><span class="sxs-lookup"><span data-stu-id="bda28-176">no</span></span>        |
| [<span data-ttu-id="bda28-177">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bda28-177">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bda28-178">nein</span><span class="sxs-lookup"><span data-stu-id="bda28-178">no</span></span>        |
| [<span data-ttu-id="bda28-179">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bda28-179">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bda28-180">nein</span><span class="sxs-lookup"><span data-stu-id="bda28-180">no</span></span>        |
| [<span data-ttu-id="bda28-181">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bda28-181">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bda28-182">nein</span><span class="sxs-lookup"><span data-stu-id="bda28-182">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bda28-183">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bda28-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bda28-184">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bda28-184">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





