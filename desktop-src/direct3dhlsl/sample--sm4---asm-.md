---
title: Sample (SM4-ASM)
description: Stichproben von Daten aus dem angegebenen Element/der Textur mithilfe der angegebenen Adresse und des vom angegebenen Sampler identifizierten Filter Modus. | Sample (SM4-ASM)
ms.assetid: 9055D3EE-FD4A-418C-A743-D12E8BDF69FF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397aba4a165f13721e73f87da82cff3e8918e33b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961441"
---
# <a name="sample-sm4---asm"></a><span data-ttu-id="db863-104">Sample (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="db863-104">sample (sm4 - asm)</span></span>

<span data-ttu-id="db863-105">Stichproben von Daten aus dem angegebenen Element/der Textur mithilfe der angegebenen Adresse und des vom angegebenen Sampler identifizierten Filter Modus.</span><span class="sxs-lookup"><span data-stu-id="db863-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="db863-106">Sample \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource \[ . Swizzle \] , srcsampler</span><span class="sxs-lookup"><span data-stu-id="db863-106">sample\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler</span></span> |
|--------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="db863-107">Element</span><span class="sxs-lookup"><span data-stu-id="db863-107">Item</span></span>                                                                                                               | <span data-ttu-id="db863-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db863-108">Description</span></span>                                                                                        |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db863-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="db863-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="db863-110">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="db863-110">\[in\] The address of the result of the operation.</span></span><br/>                                      |
| <span data-ttu-id="db863-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*</span><span class="sxs-lookup"><span data-stu-id="db863-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="db863-112">\[in \] einem Satz von Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="db863-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="db863-113">Weitere Informationen finden Sie im Abschnitt **Hinweise**.</span><span class="sxs-lookup"><span data-stu-id="db863-113">For more information, see the **Remarks** section.</span></span><br/> |
| <span data-ttu-id="db863-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*</span><span class="sxs-lookup"><span data-stu-id="db863-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="db863-115">\[in \] einem Textur Register.</span><span class="sxs-lookup"><span data-stu-id="db863-115">\[in\] A texture register.</span></span> <span data-ttu-id="db863-116">Weitere Informationen finden Sie im Abschnitt **Hinweise**.</span><span class="sxs-lookup"><span data-stu-id="db863-116">For more information, see the **Remarks** section.</span></span><br/>           |
| <span data-ttu-id="db863-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*</span><span class="sxs-lookup"><span data-stu-id="db863-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="db863-118">\[in \] einem Samplerregister.</span><span class="sxs-lookup"><span data-stu-id="db863-118">\[in\] A sampler register.</span></span> <span data-ttu-id="db863-119">Weitere Informationen finden Sie im Abschnitt **Hinweise**.</span><span class="sxs-lookup"><span data-stu-id="db863-119">For more information, see the **Remarks** section.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="db863-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db863-120">Remarks</span></span>

<span data-ttu-id="db863-121">Die Quelldaten können von jedem Ressourcentyp (außer Puffern) stammen.</span><span class="sxs-lookup"><span data-stu-id="db863-121">The source data may come from any Resource Type, other than Buffers.</span></span>

<span data-ttu-id="db863-122">*srcaddress* bietet den Satz von Texturkoordinaten, die zum Ausführen des Beispiels erforderlich sind, als Gleit Komma Werte, die auf normalisierten Raum in der Textur verweisen.</span><span class="sxs-lookup"><span data-stu-id="db863-122">*srcAddress* provides the set of texture coordinates needed to perform the sample, as floating point values referencing normalized space in the texture.</span></span> <span data-ttu-id="db863-123">Adress Umbruch Modi (Wrap/Mirror/Clamp/Border usw.) werden für Texturkoordinaten außerhalb \[ von 0... 1 \] Bereich angewendet, der aus den samplerzuständen entnommen \# und nach dem Anwenden eines beliebigen Adress Offsets auf Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="db863-123">Address wrapping modes (wrap/mirror/clamp/border etc.) are applied for texture coordinates outside \[0...1\] range, taken from the sampler state (s\#), and applied after any address offset is applied to texture coordinates.</span></span>

<span data-ttu-id="db863-124">*srkresource* ist ein Textur Register (t \# ).</span><span class="sxs-lookup"><span data-stu-id="db863-124">*srcResource* is a texture register (t\#).</span></span> <span data-ttu-id="db863-125">Dies ist einfach ein Platzhalter für eine Textur, einschließlich des Rückgabe Datentyps der zu sammelnden Ressource.</span><span class="sxs-lookup"><span data-stu-id="db863-125">This is simply a placeholder for a texture, including the return data type of the resource being sampled.</span></span> <span data-ttu-id="db863-126">Alle diese Informationen werden in der Shader-Präambel deklariert.</span><span class="sxs-lookup"><span data-stu-id="db863-126">All of this information is declared in the Shader preamble.</span></span> <span data-ttu-id="db863-127">Die tatsächlich zu sammelnde Ressource ist an den Shader extern am Slot \# (für t \# ) gebunden.</span><span class="sxs-lookup"><span data-stu-id="db863-127">The actual resource to be sampled is bound to the Shader externally at slot \# (for t\#).</span></span>

<span data-ttu-id="db863-128">*srcsampler* ist ein Samplerregister.</span><span class="sxs-lookup"><span data-stu-id="db863-128">*srcSampler* is a sampler register (s).</span></span> <span data-ttu-id="db863-129">Dabei handelt es sich um einen Platzhalter für eine Auflistung von Filter Steuerelementen, wie z. b. Point-und linear-, Mipmapping-und Adress Wrapping Steuerung.</span><span class="sxs-lookup"><span data-stu-id="db863-129">This is simply a placeholder for a collection of filtering controls such as point vs. linear, mipmapping and address wrapping controls.</span></span>

<span data-ttu-id="db863-130">Der Satz der Informationen, die für die Hardware zum Durchführen der Stichprobenentnahme erforderlich sind, wird in zwei orthogonale Teile aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="db863-130">The set of information required for the hardware to perform sampling is split into two orthogonal pieces.</span></span> <span data-ttu-id="db863-131">Zuerst bietet das Textur Registerinformationen zum Quell Datentyp, z. b. Informationen darüber, ob die Textur sRGB-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="db863-131">First, the texture register provides source data type information including, for example, information about whether the texture contains SRGB data.</span></span> <span data-ttu-id="db863-132">Er verweist auch auf den tatsächlich ausgesuchten Speicher.</span><span class="sxs-lookup"><span data-stu-id="db863-132">It also references the actual memory being sampled.</span></span> <span data-ttu-id="db863-133">Zweitens definiert das Samplerregister den anzuwendenden Filter Modus.</span><span class="sxs-lookup"><span data-stu-id="db863-133">Second, the sampler register defines the filtering mode to apply.</span></span>

### <a name="array-resources"></a><span data-ttu-id="db863-134">Array Ressourcen</span><span class="sxs-lookup"><span data-stu-id="db863-134">Array Resources</span></span>

<span data-ttu-id="db863-135">Bei Texture1D Arrays wählt die *srcaddress* g-Komponente (POS-Swizzle) aus, aus welchem Array Slice Sie abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="db863-135">For Texture1D Arrays, the *srcAddress* g component (POS-swizzle) selects which Array Slice to fetch from.</span></span> <span data-ttu-id="db863-136">Dies wird immer als skalierter Gleit Komma Wert behandelt, nicht als der normalisierte Raum für standardmäßige Texturkoordinaten, und ein roundTo-Next-Wert wird auf den Wert angewendet, gefolgt von einer Klammer zum verfügbaren bufferarray-Bereich.</span><span class="sxs-lookup"><span data-stu-id="db863-136">This is always treated as a scaled float value, rather than the normalized space for standard texture coordinates, and a round-to-nearest even is applied on the value, followed by a clamp to the available BufferArray range.</span></span>

<span data-ttu-id="db863-137">Bei Texture2D Arrays wählt die *srcaddress* b-Komponente (POS-Swizzle) aus, aus welchem Array Slice abgerufen werden soll, andernfalls mit der gleichen Semantik, die für Texture1D Arrays beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="db863-137">For Texture2D Arrays, the *srcAddress* b component (POS-swizzle) selects which Array Slice to fetch from, otherwise using the same semantics described for Texture1D Arrays .</span></span>

### <a name="address-offset"></a><span data-ttu-id="db863-138">Adress Offset</span><span class="sxs-lookup"><span data-stu-id="db863-138">Address Offset</span></span>

<span data-ttu-id="db863-139">Das optionale \[ \_ aoffimmi (u, v, w)- \] Suffix (Address Offset by immediate Integer) gibt an, dass die Texturkoordinaten für die Stichprobe um einen Satz von angegebenen ganzzahligen ganzzahligen Werten für den unmittelbaren texspace versetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="db863-139">The optional \[\_aoffimmi(u,v,w)\] suffix (address offset by immediate integer) indicates that the texture coordinates for the sample are to be offset by a set of provided immediate texel space integer constant values.</span></span> <span data-ttu-id="db863-140">Bei den Literalwerten handelt es sich um einen Satz von 4 Bit 2-Komplement Nummern mit einem ganzzahligen Bereich von \[ 8, 7 \] .</span><span class="sxs-lookup"><span data-stu-id="db863-140">The literal values are a set of 4 bit 2's complement numbers, having integer range \[-8,7\].</span></span> <span data-ttu-id="db863-141">Dieser Modifizierer wird für alle Ressourcen definiert, einschließlich Texture1D/2D-Arrays und Texture3D, ist aber für texturecube nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="db863-141">This modifier is defined for all Resources, including Texture1D/2D Arrays and Texture3D, but it is undefined for TextureCube.</span></span>

<span data-ttu-id="db863-142">Die Hardware kann sofort wissen, dass eine Durchführung eines Umfangs von texeln über einen gemeinsamen Standort durch eine Reihe von Beispiel Anweisungen erfolgt.</span><span class="sxs-lookup"><span data-stu-id="db863-142">Hardware can take advantage of immediate knowledge that a traversal over some footprint of texels about a common location is being performed by a set of sample instructions.</span></span> <span data-ttu-id="db863-143">Dies kann mithilfe von \_ aoffimmi (u, v, w) übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="db863-143">This can be conveyed using \_aoffimmi(u,v,w).</span></span>

<span data-ttu-id="db863-144">Die Offsets werden den Texturkoordinaten in texesbereich relativ zu den einzelnen miplevel-Zeichen hinzugefügt, auf die zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="db863-144">The offsets are added to the texture coordinates, in texel space, relative to each miplevel being accessed.</span></span> <span data-ttu-id="db863-145">Obwohl Texturkoordinaten als normalisierte Gleit Komma Werte bereitgestellt werden, wendet der Offset einen ganzzahligen Wert für texturspace an.</span><span class="sxs-lookup"><span data-stu-id="db863-145">So even though texture coordinates are provided as normalized float values, the offset applies a texel-space integer offset.</span></span>

<span data-ttu-id="db863-146">Adress Offsets werden nicht an der Array Achse von Texture1D/2D-Arrays angewendet.</span><span class="sxs-lookup"><span data-stu-id="db863-146">Address offsets are not applied along the array axis of Texture1D/2D Arrays.</span></span>

<span data-ttu-id="db863-147">\_aoffimmi v, w-Komponenten werden für Texture1Ds ignoriert.</span><span class="sxs-lookup"><span data-stu-id="db863-147">\_aoffimmi v,w components are ignored for Texture1Ds.</span></span>

<span data-ttu-id="db863-148">\_die Komponente "aoffimmi w" wird für Texture2Ds ignoriert.</span><span class="sxs-lookup"><span data-stu-id="db863-148">\_aoffimmi w component is ignored for Texture2Ds.</span></span>

<span data-ttu-id="db863-149">Adress Umbruch Modi (Umbruch/Spiegelung/Klammer/Rahmen usw.) aus den samplerzuständen \# werden angewendet, nachdem alle Adress Offsets auf Texturkoordinaten angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="db863-149">Address wrapping modes (wrap/mirror/clamp/border etc.) from the sampler state (s\#) are applied after any address offset is applied to texture coordinates.</span></span>

### <a name="return-type-control"></a><span data-ttu-id="db863-150">Rückgabe-typsteuer Element</span><span class="sxs-lookup"><span data-stu-id="db863-150">Return Type Control</span></span>

<span data-ttu-id="db863-151">Das Datenformat, das vom Beispiel an das Ziel Register zurückgegeben wird, wird durch das Ressourcen Format (DXGI- \_ Format \* ) bestimmt, das an den *srkresource* -Parameter (t) gebunden ist \# .</span><span class="sxs-lookup"><span data-stu-id="db863-151">The data format returned by the sample to the destination register is determined by the resource format (DXGI\_FORMAT\*) bound to the *srcResource* parameter (t\#).</span></span> <span data-ttu-id="db863-152">Wenn z. b. das angegebene t an \# eine Ressource mit dem Format DXGI- \_ Format \_ A8B8G8R8 \_ unorm \_ sRGB gebunden wurde, konvertiert der Samplingvorgang samplingtexels von Gamma 2,0 in 1,0, wendet Filter an, und das Ergebnis wird als Gleit Komma Werte im Bereich \[ 0.. 1 in das Ziel Register geschrieben \] .</span><span class="sxs-lookup"><span data-stu-id="db863-152">For example, if the specified t\# was bound with a resource with format DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB, then the sampling operation will convert sampled texels from gamma 2.0 to 1.0, apply filtering, and the result will written to the destination register as floating point values in the range \[0..1\].</span></span>

<span data-ttu-id="db863-153">Zurückgegebene Werte sind 4 Vektoren (mit Format spezifischen Standardeinstellungen für Komponenten, die nicht im Format vorhanden sind).</span><span class="sxs-lookup"><span data-stu-id="db863-153">Returned values are 4-vectors (with format-specific defaults for components not present in the format).</span></span> <span data-ttu-id="db863-154">Der *Wert für* " *srkresource* " hängt davon ab, wie das aus dem Textur Beispiel/-Filter zurückgegebene Ergebnis der 4-Komponente ausgeblendet wird </span><span class="sxs-lookup"><span data-stu-id="db863-154">The swizzle on *srcResource* determines how to swizzle the 4-component result coming back from the texture sample/filter, after which .mask on *dest* determines which components in *dest* get updated.</span></span>

<span data-ttu-id="db863-155">Wenn **Sample** einen 32-Bit-Float-Wert in ein 32-Bit-Register liest, wobei Punkt Stichproben (keine Filterung) vorliegen, können DENORMAL-Werte geleert oder nicht geändert werden. andernfalls sind Zahlen unverändert.</span><span class="sxs-lookup"><span data-stu-id="db863-155">When **sample** reads a 32-bit float value into a 32-bit register, with point sampling (no filtering), it may or may not flush denormal values, but otherwise numbers are unmodified.</span></span> <span data-ttu-id="db863-156">Wenn die Ungewissheit mit den Wert Werten für die Punkt Stichproben Entnahme für eine Anwendung ein Problem ist, verwenden Sie die [LD](ld--sm4---asm-.md) -Anweisung, die sicherstellt, dass 32-Bit-Float-Werte unverändert gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="db863-156">If the uncertainty with point sampling denormal values is an issue for an application,use the [ld](ld--sm4---asm-.md) instruction, which guarantees that 32-bit float values are read unmodified.</span></span>

### <a name="lod-calculation"></a><span data-ttu-id="db863-157">LOD-Berechnung</span><span class="sxs-lookup"><span data-stu-id="db863-157">LOD Calculation</span></span>

<span data-ttu-id="db863-158">Ausführliche Informationen zur Berechnung von Ableitungen bei der Ermittlung der Lod für das Filtern finden Sie unter [DERIV \_ RTX](deriv-rtx--sm4---asm-.md) und [DERIV \_ Eigenschaft](deriv-rty--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="db863-158">For details on how derivatives are calculated in the process of determining LOD for filtering, see [deriv\_rtx](deriv-rtx--sm4---asm-.md) and [deriv\_rty](deriv-rty--sm4---asm-.md).</span></span> <span data-ttu-id="db863-159">Die **Beispiel** Anweisung berechnet implizit Ableitungen der Texturkoordinaten mithilfe derselben Definition, die von den **DERIV** -shaderanweisungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db863-159">The **sample** instruction implicitly computes derivatives on the texture coordinates using the same definition that the **deriv** Shader instructions use.</span></span> <span data-ttu-id="db863-160">Dies gilt nicht für die Anweisungen für eine [Beispiel- \_ l](sample-l--sm4---asm-.md) oder eine [Beispiel \_ -d](sample-d--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="db863-160">This does not apply to [sample\_l](sample-l--sm4---asm-.md) or [sample\_d](sample-d--sm4---asm-.md) instructions.</span></span> <span data-ttu-id="db863-161">Diese Anweisungen werden direkt von der Anwendung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="db863-161">For those instructions, LOD or derivatives are provided directly by the application.</span></span>

<span data-ttu-id="db863-162">Bei der **Beispiel** Anweisung können Implementierungen die gleiche Lod-Berechnung für alle 4 Pixel in einem 2 x 2-Stempel (aber keinen größeren Bereich) verwenden oder pro Pixel-Lod-Berechnungen durchführen.</span><span class="sxs-lookup"><span data-stu-id="db863-162">For the **sample** instruction, implementations can choose to share the same LOD calculation across all 4 pixels in a 2x2 stamp (but no larger area), or perform per-pixel LOD calculations.</span></span>

### <a name="miscellaneous-details"></a><span data-ttu-id="db863-163">Sonstige Details</span><span class="sxs-lookup"><span data-stu-id="db863-163">Miscellaneous Details</span></span>

<span data-ttu-id="db863-164">Für buffer & Texture1D werden *srcaddress* . GBA-Komponenten (POS-Swizzle) ignoriert.</span><span class="sxs-lookup"><span data-stu-id="db863-164">For Buffer & Texture1D, *srcAddress* .gba components (POS-swizzle) are ignored.</span></span> <span data-ttu-id="db863-165">Für Texture1D Arrays werden die *srcaddress* . BA-Komponenten (POS-Swizzle) ignoriert.</span><span class="sxs-lookup"><span data-stu-id="db863-165">For Texture1D Arrays, *srcAddress* .ba components (POS-swizzle) are ignored.</span></span> <span data-ttu-id="db863-166">Für Texture2Ds wird die *srcaddress* . a-Komponente (POS-Swizzle) ignoriert.</span><span class="sxs-lookup"><span data-stu-id="db863-166">For Texture2Ds, *srcAddress* .a component (POS-swizzle) is ignored.</span></span>

<span data-ttu-id="db863-167">Wenn Sie aus einem Eingabe Slot abrufen, an das nichts gebunden ist, wird 0 für alle Komponenten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="db863-167">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

### <a name="restrictions"></a><span data-ttu-id="db863-168">Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="db863-168">Restrictions</span></span>

-   <span data-ttu-id="db863-169">*srkresource* muss ein t- \# Register sein.</span><span class="sxs-lookup"><span data-stu-id="db863-169">*srcResource* must be a t\# register.</span></span> <span data-ttu-id="db863-170">*srkresource* kann kein constantbuffer-Wert sein, der nicht an t-Register gebunden werden kann \# .</span><span class="sxs-lookup"><span data-stu-id="db863-170">*srcResource* cannot be a ConstantBuffer, which cannot be bound to t\# registers.</span></span>
-   <span data-ttu-id="db863-171">*srcsampler* muss ein s- \# Register sein.</span><span class="sxs-lookup"><span data-stu-id="db863-171">*srcSampler* must be an s\# register.</span></span>
-   <span data-ttu-id="db863-172">Die relative Adressierung in *srkresource* oder *srcsampler* ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="db863-172">Relative addressing on *srcResource* or *srcSampler* is not permitted.</span></span>
-   <span data-ttu-id="db863-173">*srcaddress* muss ein Temp (r \# /x \# ), ein constantbuffer (CB \# ), ein Eingabe (v \# )-Register oder unmittelbare Werte sein.</span><span class="sxs-lookup"><span data-stu-id="db863-173">*srcAddress* must be a temp (r\#/x\#), constantBuffer (cb\#), input (v\#) register or immediate value(s).</span></span>
-   <span data-ttu-id="db863-174">*dest* muss ein Temp-(r \# /x \# ) oder Output (o \* \# )-Register sein.</span><span class="sxs-lookup"><span data-stu-id="db863-174">*dest* must be a temp (r\#/x\#) or output (o\*\#) register.</span></span>
-   <span data-ttu-id="db863-175">\_aoffimmi (u, v, w) ist für texturecubes nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="db863-175">\_aoffimmi(u,v,w) is not permitted for TextureCubes.</span></span>

<span data-ttu-id="db863-176">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="db863-176">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="db863-177">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="db863-177">Vertex Shader</span></span> | <span data-ttu-id="db863-178">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="db863-178">Geometry Shader</span></span> | <span data-ttu-id="db863-179">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="db863-179">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="db863-180">x</span><span class="sxs-lookup"><span data-stu-id="db863-180">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="db863-181">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="db863-181">Minimum Shader Model</span></span>

<span data-ttu-id="db863-182">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="db863-182">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="db863-183">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="db863-183">Shader Model</span></span>                                              | <span data-ttu-id="db863-184">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="db863-184">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="db863-185">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="db863-185">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="db863-186">ja</span><span class="sxs-lookup"><span data-stu-id="db863-186">yes</span></span>       |
| [<span data-ttu-id="db863-187">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="db863-187">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="db863-188">ja</span><span class="sxs-lookup"><span data-stu-id="db863-188">yes</span></span>       |
| [<span data-ttu-id="db863-189">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="db863-189">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="db863-190">ja</span><span class="sxs-lookup"><span data-stu-id="db863-190">yes</span></span>       |
| [<span data-ttu-id="db863-191">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db863-191">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="db863-192">nein</span><span class="sxs-lookup"><span data-stu-id="db863-192">no</span></span>        |
| [<span data-ttu-id="db863-193">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db863-193">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="db863-194">nein</span><span class="sxs-lookup"><span data-stu-id="db863-194">no</span></span>        |
| [<span data-ttu-id="db863-195">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db863-195">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="db863-196">nein</span><span class="sxs-lookup"><span data-stu-id="db863-196">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="db863-197">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="db863-197">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db863-198">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db863-198">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





