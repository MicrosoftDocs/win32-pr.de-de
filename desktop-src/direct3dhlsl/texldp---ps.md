---
title: texldp-PS
description: Projizierte Textur Lade Anweisung. Diese Anweisung dividiert die Eingabe Textur Koordinate durch das vierte Element (. a oder. w) direkt vor der Stichprobenentnahme.
ms.assetid: 82e62ba3-a9f5-4afb-8dca-4c54a00843eb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 045caf6ec922183893df252488946546602d2459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316394"
---
# <a name="texldp---ps"></a><span data-ttu-id="2f2bb-104">texldp-PS</span><span class="sxs-lookup"><span data-stu-id="2f2bb-104">texldp - ps</span></span>

<span data-ttu-id="2f2bb-105">Projizierte Textur Lade Anweisung.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-105">Projected texture load instruction.</span></span> <span data-ttu-id="2f2bb-106">Diese Anweisung dividiert die Eingabe Textur Koordinate durch das vierte Element (. a oder. w) direkt vor der Stichprobenentnahme.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-106">This instruction divides the input texture coordinate by the fourth element (.a or .w) just before sampling.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f2bb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f2bb-107">Syntax</span></span>



| <span data-ttu-id="2f2bb-108">texldp DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="2f2bb-108">texldp dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="2f2bb-109">where</span><span class="sxs-lookup"><span data-stu-id="2f2bb-109">where</span></span>

-   <span data-ttu-id="2f2bb-110">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-110">dst is the destination register.</span></span>
-   <span data-ttu-id="2f2bb-111">src0 ist ein Quell Register, das die Texturkoordinaten für das Textur Beispiel bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-111">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="2f2bb-112">Siehe [Texturkoordinaten Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="2f2bb-112">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="2f2bb-113">Quelle1 identifiziert den [Sampler (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , wobei \# angibt, welche Textur samplingnummer als Stichprobe angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-113">src1 identifies the [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="2f2bb-114">Der Sampler hat ihm eine Textur und einen samplerzustand zugeordnet, der durch [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype)definiert wird.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-114">The sampler has associated with it a texture and a sampler state defined by [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="2f2bb-115">Informationen zu den Einschränkungen bei der Verwendung von texldp finden Sie unter [texld](texld---ps-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="2f2bb-115">For the set of restrictions when using texldp, see [texld](texld---ps-2-0.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2f2bb-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f2bb-116">Remarks</span></span>

<span data-ttu-id="2f2bb-117">texldp führt eine Projektion der aus src0 gelesenen Koordinaten vor der Durchführung des Beispiels aus.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-117">texldp performs projection on the coordinates read from src0 before performing the sample.</span></span> <span data-ttu-id="2f2bb-118">Jede Textur Koordinate wird durch src0. w dividiert, dann wird die Textur als Stichprobe verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-118">Each texture coordinate is divided by src0.w, then the texture is sampled.</span></span> <span data-ttu-id="2f2bb-119">Wenn texldp abgeschlossen ist, ist der Inhalt von src0 nicht betroffen (es sei denn, DST ist dasselbe Register).</span><span class="sxs-lookup"><span data-stu-id="2f2bb-119">When texldp completes, the contents of src0 are unaffected (unless dst is the same register).</span></span> <span data-ttu-id="2f2bb-120">Eine Alternative zur Verwendung von texldp besteht darin, die Projektions Division im Shader manuell auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-120">An alternative to using texldp is to manually perform the projection division in the shader.</span></span> <span data-ttu-id="2f2bb-121">Die Durchführung der Division im Shader-Code ist jedoch in der Regel langsamer als bei der Ausführung durch die texldp-Anweisung. vermeiden Sie daher eine solche zusätzliche Mathematik, wenn möglich.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-121">However, performing the division in shader code is usually slower than when performed by the texldp instruction, so avoid such additional math when possible.</span></span>

<span data-ttu-id="2f2bb-122">Die Anzahl der Koordinaten, die erforderlich sind, damit src0 das Textur Beispiel durchführen kann, hängt davon ab, wie Quelle1 deklariert wurde, sowie der. w-Komponente.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-122">The number of coordinates required for src0 to perform the texture sample depends on how src1 was declared, plus the .w component.</span></span> <span data-ttu-id="2f2bb-123">[ \_ Samplertypen werden mit DCL samplertype (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)deklariert.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-123">Sampler types are declared with [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md).</span></span> <span data-ttu-id="2f2bb-124">Wenn Quelle1 als 2D-Sampler deklariert ist, muss src0. xyw-Koordinaten enthalten. Wenn Quelle1 entweder als Cube-Sampler oder als volumesampler deklariert ist, muss src0. xyzw-Koordinaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-124">If src1 is declared as a 2D sampler, then src0 must contain .xyw coordinates; if src1 is declared as either a cube sampler or a volume sampler, then src0 must contain .xyzw coordinates.</span></span> <span data-ttu-id="2f2bb-125">Die Stichprobenentnahme einer 2D-Textur mit xyzw-Koordinaten ist zulässig (die. z-Koordinate wird ignoriert).</span><span class="sxs-lookup"><span data-stu-id="2f2bb-125">Sampling a 2D texture with .xyzw coordinates is allowed (the .z coordinate is ignored).</span></span>

<span data-ttu-id="2f2bb-126">Wenn die Quell Textur weniger als vier Komponenten enthält, werden die fehlenden Komponenten als Standardwerte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-126">If the source texture contains fewer than four components, defaults are placed in the missing components.</span></span> <span data-ttu-id="2f2bb-127">Standardwerte sind vom Textur Format abhängig, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-127">Defaults depend on the texture format as shown in the following table.</span></span>



| <span data-ttu-id="2f2bb-128">Textur Format</span><span class="sxs-lookup"><span data-stu-id="2f2bb-128">Texture Format</span></span>                                                                                          | <span data-ttu-id="2f2bb-129">Standardwerte für fehlende Komponenten</span><span class="sxs-lookup"><span data-stu-id="2f2bb-129">Default Values for missing components</span></span> |
|---------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="2f2bb-130">D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ L8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5</span><span class="sxs-lookup"><span data-stu-id="2f2bb-130">D3DFMT\_R5G6B5, D3DFMT\_R8G8B8, D3DFMT\_L8, D3DFMT\_L16, D3DFMT\_R3G3B2, D3DFMT\_CxV8U8, D3DFMT\_L6V5U5</span></span> | <span data-ttu-id="2f2bb-131">A = 1,0</span><span class="sxs-lookup"><span data-stu-id="2f2bb-131">A = 1.0</span></span>                               |
| <span data-ttu-id="2f2bb-132">D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT \_ G16R16F, D3DFMT \_ G32R32F</span><span class="sxs-lookup"><span data-stu-id="2f2bb-132">D3DFMT\_V8U8, D3DFMT\_V16U16, D3DFMT\_G16R16, D3DFMT\_G16R16F, D3DFMT\_G32R32F</span></span>                          | <span data-ttu-id="2f2bb-133">B = a = 1,0</span><span class="sxs-lookup"><span data-stu-id="2f2bb-133">B = A = 1.0</span></span>                           |
| <span data-ttu-id="2f2bb-134">D3DFMT \_ a8</span><span class="sxs-lookup"><span data-stu-id="2f2bb-134">D3DFMT\_A8</span></span>                                                                                              | <span data-ttu-id="2f2bb-135">R = G = B = 0,0</span><span class="sxs-lookup"><span data-stu-id="2f2bb-135">R = G = B = 0.0</span></span>                       |
| <span data-ttu-id="2f2bb-136">D3DFMT \_ R16F, D3DFMT \_ R32F</span><span class="sxs-lookup"><span data-stu-id="2f2bb-136">D3DFMT\_R16F, D3DFMT\_R32F</span></span>                                                                              | <span data-ttu-id="2f2bb-137">G = B = a = 1,0</span><span class="sxs-lookup"><span data-stu-id="2f2bb-137">G = B = A = 1.0</span></span>                       |
| <span data-ttu-id="2f2bb-138">Alle tiefen/Schablonen Formate</span><span class="sxs-lookup"><span data-stu-id="2f2bb-138">All depth/stencil formats</span></span>                                                                               | <span data-ttu-id="2f2bb-139">R = B = 0,0, A = 1,0</span><span class="sxs-lookup"><span data-stu-id="2f2bb-139">R = B = 0.0, A = 1.0</span></span>                  |



 

<span data-ttu-id="2f2bb-140">Diese Anweisung wird in den folgenden Versionen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="2f2bb-140">This instruction is supported in the following versions:</span></span>



| <span data-ttu-id="2f2bb-141">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="2f2bb-141">Pixel shader versions</span></span> | <span data-ttu-id="2f2bb-142">1\_1</span><span class="sxs-lookup"><span data-stu-id="2f2bb-142">1\_1</span></span> | <span data-ttu-id="2f2bb-143">1\_2</span><span class="sxs-lookup"><span data-stu-id="2f2bb-143">1\_2</span></span> | <span data-ttu-id="2f2bb-144">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="2f2bb-144">1\_3</span></span> | <span data-ttu-id="2f2bb-145">1\_4</span><span class="sxs-lookup"><span data-stu-id="2f2bb-145">1\_4</span></span> | <span data-ttu-id="2f2bb-146">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2f2bb-146">2\_0</span></span> | <span data-ttu-id="2f2bb-147">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2f2bb-147">2\_x</span></span> | <span data-ttu-id="2f2bb-148">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2f2bb-148">2\_sw</span></span> | <span data-ttu-id="2f2bb-149">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2f2bb-149">3\_0</span></span> | <span data-ttu-id="2f2bb-150">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2f2bb-150">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="2f2bb-151">texldp</span><span class="sxs-lookup"><span data-stu-id="2f2bb-151">texldp</span></span>                |      |      |      |      | <span data-ttu-id="2f2bb-152">x</span><span class="sxs-lookup"><span data-stu-id="2f2bb-152">x</span></span>    | <span data-ttu-id="2f2bb-153">x</span><span class="sxs-lookup"><span data-stu-id="2f2bb-153">x</span></span>    | <span data-ttu-id="2f2bb-154">x</span><span class="sxs-lookup"><span data-stu-id="2f2bb-154">x</span></span>     | <span data-ttu-id="2f2bb-155">x</span><span class="sxs-lookup"><span data-stu-id="2f2bb-155">x</span></span>    | <span data-ttu-id="2f2bb-156">x</span><span class="sxs-lookup"><span data-stu-id="2f2bb-156">x</span></span>     |



 

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="2f2bb-157">PS \_ 2 \_ 0 und PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2f2bb-157">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="2f2bb-158">DST muss ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) sein, und nur. xyzw Mask (Standard Maske) ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-158">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) and only .xyzw mask (default mask) is allowed.</span></span>

<span data-ttu-id="2f2bb-159">src0 muss entweder ein [Texturkoordinaten Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) oder ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) sein, ohne Modifizierer oder Swizzle.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-159">src0 must be either a [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t\#) or a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="2f2bb-160">Quelle1 muss ein [Sampler (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) sein \# , ohne Modifizierer oder Swizzle.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-160">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="2f2bb-161">Wenn das D3DD3DPSHADERCAPS2 \_ 0 \_ nodependentleselimit-Cap-Bit nicht festgelegt ist (in D3DPSHADERCAPS2 \_ 0), ist eine angegebene Textur Anweisung ([texld](texld---ps-1-4.md), texldp, [texldb-PS](texldb---ps.md), [texldd](texldd---ps.md) ) möglicherweise höchstens in dritter Reihenfolge abhängig.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-161">If the D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT cap bit is not set (in D3DPSHADERCAPS2\_0), a given texture instruction ([texld](texld---ps-1-4.md), texldp, [texldb - ps](texldb---ps.md), [texldd](texldd---ps.md) ) may be dependent upon, at most, third order.</span></span> <span data-ttu-id="2f2bb-162">Eine abhängige Textur Anweisung der ersten Bestellung ist eine Textur Anweisung, in der Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="2f2bb-162">A first-order dependent texture instruction is a texture instruction in which either:</span></span>

-   <span data-ttu-id="2f2bb-163">src0 ist ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# )</span><span class="sxs-lookup"><span data-stu-id="2f2bb-163">src0 is a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#)</span></span>
-   <span data-ttu-id="2f2bb-164">DST wurde bereits geschrieben und wird nun erneut geschrieben.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-164">dst was previously written, now being written again.</span></span>

<span data-ttu-id="2f2bb-165">Eine abhängige Textur Anweisung in zweiter Reihenfolge wird als Textur Anweisung definiert, die ein temporäres Register (r) liest oder in ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) schreibt, \# dessen Inhalt vor dem Ausführen der Textur Anweisung (möglicherweise indirekt) auf das Ergebnis einer abhängigen Textur Anweisung der ersten Bestellung angewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-165">A second-order dependent texture instruction is defined as a texture instruction that reads or writes to a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) whose contents, before executing the texture instruction, depend (perhaps indirectly) on the outcome of a first-order dependent texture instruction.</span></span> <span data-ttu-id="2f2bb-166">Eine (n) in der Reihenfolge abhängige Textur Anweisung wird von einer (n-1)<sup>th</sup>-<sup>Order-Textur</sup>Anweisung abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-166">An (n)<sup>th</sup>-order dependent texture instruction derives from an (n - 1)<sup>th</sup>-order texture instruction.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="2f2bb-167">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2f2bb-167">ps\_3\_0</span></span>

<span data-ttu-id="2f2bb-168">Bei PS \_ 3 \_ 0 muss Quelle1 ein [Sampler (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# ohne Modifizierer sein.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-168">For ps\_3\_0, src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier.</span></span> <span data-ttu-id="2f2bb-169">"Swizzle" ist auf Quelle1 zulässig. wenn diese Anwendung angewendet wird, werden die Ergebnisse der Textur Suche vor dem Schreiben in den DST vorgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2f2bb-169">Swizzle is allowed on src1, and when applied, the texture lookup results are pre-swizzled before written to dst.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f2bb-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2f2bb-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f2bb-171">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="2f2bb-171">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 