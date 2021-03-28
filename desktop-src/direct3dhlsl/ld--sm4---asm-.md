---
title: LD (SM4-ASM)
description: Ruft Daten aus dem angegebenen Puffer oder der Textur ohne Filter (z. b. Punkt Stichproben) ab, wobei die angegebene ganzzahlige Adresse verwendet wird. Die Quelldaten können von jedem Ressourcentyp (außer texturecube) stammen.
ms.assetid: DEE9A55F-EDFE-478E-8169-5BF9C43E98AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaacc3d76d49cc2b3043d39036f0ff652d7b8794
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313685"
---
# <a name="ld-sm4---asm"></a><span data-ttu-id="0b77d-104">LD (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="0b77d-104">ld (sm4 - asm)</span></span>

<span data-ttu-id="0b77d-105">Ruft Daten aus dem angegebenen Puffer oder der Textur ohne Filter (z. b. Punkt Stichproben) ab, wobei die angegebene ganzzahlige Adresse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0b77d-105">Fetches data from the specified buffer or texture without any filtering (e.g. point sampling) using the provided integer address.</span></span> <span data-ttu-id="0b77d-106">Die Quelldaten können von jedem Ressourcentyp (außer texturecube) stammen.</span><span class="sxs-lookup"><span data-stu-id="0b77d-106">The source data may come from any resource type, other than TextureCube.</span></span>



| <span data-ttu-id="0b77d-107">LD \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="0b77d-107">ld\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------|



 



| <span data-ttu-id="0b77d-108">Element</span><span class="sxs-lookup"><span data-stu-id="0b77d-108">Item</span></span>                                                                                                               | <span data-ttu-id="0b77d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b77d-109">Description</span></span>                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b77d-110"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="0b77d-110"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="0b77d-111">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="0b77d-111">\[in\] The address of the result of the operation.</span></span><br/>                                                               |
| <span data-ttu-id="0b77d-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*</span><span class="sxs-lookup"><span data-stu-id="0b77d-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="0b77d-113">\[in \] den Texturkoordinaten, die zum Ausführen des Beispiels erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="0b77d-113">\[in\] The texture coordinates needed to perform the sample.</span></span><br/>                                                     |
| <span data-ttu-id="0b77d-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*</span><span class="sxs-lookup"><span data-stu-id="0b77d-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="0b77d-115">\[in \] einem Textur Register (t \# ), das als festgelegt werden muss, welches Textur oder Puffer abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b77d-115">\[in\] A texture register (t\#) which must have been declared identifying which Texture or Buffer to fetch from.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0b77d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b77d-116">Remarks</span></span>

<span data-ttu-id="0b77d-117">Diese Anweisung ist eine vereinfachte Alternative zur [Beispiel](sample--sm4---asm-.md) Anweisung.</span><span class="sxs-lookup"><span data-stu-id="0b77d-117">This instruction is a simplified alternative to the [sample](sample--sm4---asm-.md) instruction.</span></span> <span data-ttu-id="0b77d-118">Anders als bei **Sample** kann **LD** auch Daten aus Puffern abrufen.</span><span class="sxs-lookup"><span data-stu-id="0b77d-118">Unlike **sample**, **ld** is also capable of fetching data from buffers.</span></span> <span data-ttu-id="0b77d-119">**LD** kann auch aus Multisample-Ressourcen abrufen (nur auf dem Pixel-Shader).</span><span class="sxs-lookup"><span data-stu-id="0b77d-119">**ld** is can also fetch from multi-sample resources (on pixel shader only).</span></span>

<span data-ttu-id="0b77d-120">*srcaddress* bietet den Satz von Texturkoordinaten, die zum Ausführen des Beispiels in Form von Ganzzahlen ohne Vorzeichen benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="0b77d-120">*srcAddress* provides the set of texture coordinates needed to perform the sample in the form of unsigned integers.</span></span> <span data-ttu-id="0b77d-121">Wenn *srcaddress* außerhalb des Bereichs \[ 0... liegt ( \# texeln in Dimension-1) \] , dann wird das Verhalten außerhalb des gültigen Bereichs aufgerufen, wobei **LD** in allen nicht fehlenden Komponenten im Format von *srkresource* 0 (null) und die Standardeinstellung für fehlende Komponenten zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0b77d-121">If *srcAddress* is out of the range\[0...(\#texels in dimension -1)\], then out-of-bounds behavior is invoked, where **ld** returns 0 in all non-missing components of the format of the *srcResource*, and the default for missing components.</span></span> <span data-ttu-id="0b77d-122">Eine Anwendung, die eine flexiblere Kontrolle über das Adress Verhalten außerhalb des gültigen Bereichs hat, sollte stattdessen die **Beispiel** Anweisung verwenden, da Sie das als samplerzustand definierte Adress Umbruch-/Spiegelungs-/einspannen/Rahmen Verhalten berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="0b77d-122">An application wishing any more flexible control over out-of-range address behavior should use the **sample** instruction instead, as it honors address wrap/mirror/clamp/border behavior defined as sampler state.</span></span>

<span data-ttu-id="0b77d-123">*srcaddress. a* (POS-Swizzle) stellt immer eine MipMap-Ebene ohne Vorzeichen bereit.</span><span class="sxs-lookup"><span data-stu-id="0b77d-123">*srcAddress.a* (POS-swizzle) always provides an unsigned integer mipmap level.</span></span> <span data-ttu-id="0b77d-124">Wenn der Wert außerhalb des Bereichs \[ 0... liegt ( NUM miplevels in Resource-1) \] ), dann wird das Verhalten außerhalb des gültigen Bereichs aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0b77d-124">If the value is out of the range \[0...(num miplevels in resource-1)\]), then out-of-bounds behavior is invoked.</span></span> <span data-ttu-id="0b77d-125">Wenn die Ressource ein Puffer ist, der keine Mipmaps aufweisen kann, wird *srcaddress. a ignoriert.*</span><span class="sxs-lookup"><span data-stu-id="0b77d-125">If the resource is a buffer, which can not have any mipmaps, then *srcAddress.a* is ignored</span></span>

<span data-ttu-id="0b77d-126">*srcaddress. GB* (POS-Swizzle) wird für Puffer und texture1D (Non-Array) ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0b77d-126">*srcAddress.gb* (POS-swizzle) is ignored for buffers and texture1D (non-Array).</span></span> <span data-ttu-id="0b77d-127">*srcaddress. b* (POS-Swizzle) wird für texture1D Arrays und texture2Ds ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0b77d-127">*srcAddress.b* (POS-swizzle) is ignored for texture1D arrays and texture2Ds.</span></span>

<span data-ttu-id="0b77d-128">Bei texture1D Arrays stellt *srcaddress. g* (POS-Swizzle) den Array Index als Ganzzahl ohne Vorzeichen bereit.</span><span class="sxs-lookup"><span data-stu-id="0b77d-128">For texture1D arrays, *srcAddress.g* (POS-swizzle) provides the array index as an unsigned integer.</span></span> <span data-ttu-id="0b77d-129">, Wenn der Wert außerhalb des Bereichs der verfügbaren Array Indizes \[ 0 (null) liegt. Array Größe-1) \] , dann wird das Verhalten außerhalb des gültigen Bereichs aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0b77d-129">If the value is out of the range of available array indices \[0...(array size-1)\], then out-of-bounds behavior is invoked.</span></span>

<span data-ttu-id="0b77d-130">Für texture2D Arrays stellt *srcaddress. b* (POS-Swizzle) den Array Index bereit, andernfalls mit der gleichen Semantik wie für texture1D.</span><span class="sxs-lookup"><span data-stu-id="0b77d-130">For texture2D arrays, *srcAddress.b* (POS-swizzle) provides the array index, otherwise with same semantics as for texture1D.</span></span>

<span data-ttu-id="0b77d-131">Wenn Sie von *t \#* abrufen, an das nichts gebunden ist, wird 0 für alle Komponenten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0b77d-131">Fetching from *t\#* that has nothing bound to it returns 0 for all components.</span></span>

### <a name="address-offset"></a><span data-ttu-id="0b77d-132">Adress Offset</span><span class="sxs-lookup"><span data-stu-id="0b77d-132">Address Offset</span></span>

<span data-ttu-id="0b77d-133">Das optionale \[ \_ aoffimmi (u, v, w)- \] Suffix (Address Offset by immediate Integer) gibt an, dass die Texturkoordinaten für die **LD** durch eine Menge von bereitgestellten ganzzahligen ganzzahligen Werten des unmittelbaren texraums versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="0b77d-133">The optional \[\_aoffimmi(u,v,w)\] suffix (address offset by immediate integer) indicates that the texture coordinates for the **ld** are to be offset by a set of provided immediate texel space integer constant values.</span></span> <span data-ttu-id="0b77d-134">Bei den Literalwerten handelt es sich um einen Satz von 4 Bit 2-Komplement Nummern mit einem ganzzahligen Bereich von \[ 8, 7 \] .</span><span class="sxs-lookup"><span data-stu-id="0b77d-134">The literal values are a set of 4 bit 2's complement numbers, having integer range \[-8,7\].</span></span> <span data-ttu-id="0b77d-135">Dieser Modifizierer ist nur für texture1D/2D/3D definiert, einschließlich Arrays, nicht für Puffer.</span><span class="sxs-lookup"><span data-stu-id="0b77d-135">This modifier is defined only for texture1D/2D/3D, including arrays, and not for buffers.</span></span>

<span data-ttu-id="0b77d-136">Die Offsets werden den Texturkoordinaten in texesbereich relativ zu dem vom **LD** zugegriffen auf das miplevel hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0b77d-136">The offsets are added to the texture coordinates, in texel space, relative to the miplevel being accessed by the **ld**.</span></span>

<span data-ttu-id="0b77d-137">Adress Offsets werden nicht an der Array Achse von texture1D/2D-Arrays angewendet.</span><span class="sxs-lookup"><span data-stu-id="0b77d-137">Address offsets are not applied along the array axis of texture1D/2D arrays.</span></span>

<span data-ttu-id="0b77d-138">Die Komponenten " *\_ aoffimmi v" und "w* " werden bei texture1Ds ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0b77d-138">The *\_aoffimmi v,w* components are ignored for texture1Ds.</span></span>

<span data-ttu-id="0b77d-139">Die Komponente " *\_ aoffimmi w* " wird für texture2Ds ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0b77d-139">The *\_aoffimmi w* component is ignored for texture2Ds.</span></span>

<span data-ttu-id="0b77d-140">Da die Texturkoordinaten für **LD** ganze Zahlen ohne Vorzeichen sind, wird der Offset, wenn der Offset bewirkt, dass die Adresse unter 0 (null) wechselt, in eine große Adresse umbrochen und führt zu einem Zugriff außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="0b77d-140">Because the texture coordinates for **ld** are unsigned integers, if the offset causes the address to go below zero, it will wrap to a large address, and result in an out of bounds access.</span></span>

### <a name="return-type-control"></a><span data-ttu-id="0b77d-141">Rückgabe-typsteuer Element</span><span class="sxs-lookup"><span data-stu-id="0b77d-141">Return Type Control</span></span>

<span data-ttu-id="0b77d-142">Das Datenformat, das von **LD** an das Ziel Register zurückgegeben wird, wird auf die gleiche Weise wie für die **Beispiel** Anweisung bestimmt. Sie basiert auf dem Format, das an den *srkresource* -Parameter *( \# t*) gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="0b77d-142">The data format returned by **ld** to the destination register is determined in the same way as described for the **sample** instruction; it is based on the format bound to the *srcResource* parameter (*t\#*).</span></span>

<span data-ttu-id="0b77d-143">Wie bei der **Beispiel** Anweisung sind die zurückgegebenen Werte für **LD** vier Vektoren mit Format spezifischen Standardwerten für Komponenten, die nicht im-Format vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="0b77d-143">As with the **sample** instruction, returned values for **ld** are 4-vectors with format-specific defaults for components not present in the format.</span></span> <span data-ttu-id="0b77d-144">Der Wert für " *srkresource* " hängt davon ab, wie das aus der Textur Auslastung zurückgegebene Ergebnis der 4-Komponente durch die Verwendung von ". Mask" unter " *dest* " bestimmt wird, welche Komponenten in *dest* aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="0b77d-144">The swizzle on *srcResource* determines how to swizzle the 4-component result coming back from the texture load, after which .mask on *dest* determines which components in *dest* get updated.</span></span>

<span data-ttu-id="0b77d-145">Wenn ein 32-Bit-Float-Wert von *LD* in ein 32-Bit-Register gelesen wird, sind die Bits unverändert. Das heißt, die DENORMAL-Werte bleiben DENORMAL.</span><span class="sxs-lookup"><span data-stu-id="0b77d-145">When a 32-bit float value is read by *ld* into a 32-bit register, the bits are untouched; that is, denormal values remain denormal.</span></span> <span data-ttu-id="0b77d-146">Dies ist anders als bei der **Beispiel** Anweisung.</span><span class="sxs-lookup"><span data-stu-id="0b77d-146">This is unlike the **sample** instruction.</span></span>

### <a name="miscellaneous-details"></a><span data-ttu-id="0b77d-147">Sonstige Details</span><span class="sxs-lookup"><span data-stu-id="0b77d-147">Miscellaneous Details</span></span>

<span data-ttu-id="0b77d-148">Da der **LD** -Anweisung keine Filterung zugeordnet ist, gelten Konzepte wie Lod-Bias nicht für **LD**.</span><span class="sxs-lookup"><span data-stu-id="0b77d-148">As there is no filtering associated with the **ld** instruction, concepts like LOD bias do not apply to **ld**.</span></span> <span data-ttu-id="0b77d-149">Dementsprechend gibt es *keinen Sampler \# -* Parameter.</span><span class="sxs-lookup"><span data-stu-id="0b77d-149">Accordingly there is no sampler *s\#* parameter.</span></span>

### <a name="restrictions"></a><span data-ttu-id="0b77d-150">Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="0b77d-150">Restrictions</span></span>

-   <span data-ttu-id="0b77d-151">*srkresource* muss ein t \# -Register und kein texturecube-Element sein.</span><span class="sxs-lookup"><span data-stu-id="0b77d-151">*srcResource* must be a t\# register, and not a TextureCube.</span></span> <span data-ttu-id="0b77d-152">*srkresource* kann kein constantbuffer-Wert sein, der nicht an t-Register gebunden werden kann \# .</span><span class="sxs-lookup"><span data-stu-id="0b77d-152">*srcResource* cannot be a constantbuffer either, which cannot be bound to t\# registers.</span></span>
-   <span data-ttu-id="0b77d-153">Die relative Adressierung in *srkresource* ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="0b77d-153">Relative addressing on *srcResource* is not permitted.</span></span>
-   <span data-ttu-id="0b77d-154">*srcaddress* muss ein Temp-(r \# /x \# ), konstantes (CB \# ) oder Eingabe (v \# )-Register sein.</span><span class="sxs-lookup"><span data-stu-id="0b77d-154">*srcAddress* must be a temp (r\#/x\#), constant (cb\#) or input (v\#) register.</span></span>
-   <span data-ttu-id="0b77d-155">*dest* muss ein Temp-(r \# /x \# ) oder Output (o \* \# )-Register sein.</span><span class="sxs-lookup"><span data-stu-id="0b77d-155">*dest* must be a temp (r\#/x\#) or output (o\*\#) register.</span></span>

<span data-ttu-id="0b77d-156">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="0b77d-156">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0b77d-157">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="0b77d-157">Vertex Shader</span></span> | <span data-ttu-id="0b77d-158">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="0b77d-158">Geometry Shader</span></span> | <span data-ttu-id="0b77d-159">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="0b77d-159">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="0b77d-160">x</span><span class="sxs-lookup"><span data-stu-id="0b77d-160">x</span></span>             | <span data-ttu-id="0b77d-161">x</span><span class="sxs-lookup"><span data-stu-id="0b77d-161">x</span></span>               | <span data-ttu-id="0b77d-162">x</span><span class="sxs-lookup"><span data-stu-id="0b77d-162">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0b77d-163">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="0b77d-163">Minimum Shader Model</span></span>

<span data-ttu-id="0b77d-164">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0b77d-164">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0b77d-165">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="0b77d-165">Shader Model</span></span>                                              | <span data-ttu-id="0b77d-166">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="0b77d-166">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0b77d-167">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="0b77d-167">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0b77d-168">ja</span><span class="sxs-lookup"><span data-stu-id="0b77d-168">yes</span></span>       |
| [<span data-ttu-id="0b77d-169">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="0b77d-169">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0b77d-170">ja</span><span class="sxs-lookup"><span data-stu-id="0b77d-170">yes</span></span>       |
| [<span data-ttu-id="0b77d-171">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="0b77d-171">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0b77d-172">ja</span><span class="sxs-lookup"><span data-stu-id="0b77d-172">yes</span></span>       |
| [<span data-ttu-id="0b77d-173">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b77d-173">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0b77d-174">nein</span><span class="sxs-lookup"><span data-stu-id="0b77d-174">no</span></span>        |
| [<span data-ttu-id="0b77d-175">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b77d-175">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0b77d-176">nein</span><span class="sxs-lookup"><span data-stu-id="0b77d-176">no</span></span>        |
| [<span data-ttu-id="0b77d-177">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b77d-177">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0b77d-178">nein</span><span class="sxs-lookup"><span data-stu-id="0b77d-178">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0b77d-179">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0b77d-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b77d-180">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b77d-180">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





