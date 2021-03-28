---
title: texldb-PS
description: Unausgewogene Textur Lade Anweisung. Diese Anweisung verwendet das vierte Element (. a oder. w), um die Detailstufe der Textur Stichprobe direkt vor der Stichprobenentnahme zu überdenken.
ms.assetid: cafd72c9-b7bb-4e3f-8a8c-de26a4446864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 912c4c61f6c1f2b6bef46c7c5b6ea17223df5eb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101783"
---
# <a name="texldb---ps"></a><span data-ttu-id="b5c1d-104">texldb-PS</span><span class="sxs-lookup"><span data-stu-id="b5c1d-104">texldb - ps</span></span>

<span data-ttu-id="b5c1d-105">Unausgewogene Textur Lade Anweisung.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-105">Biased texture load instruction.</span></span> <span data-ttu-id="b5c1d-106">Diese Anweisung verwendet das vierte Element (. a oder. w), um die Detailstufe der Textur Stichprobe direkt vor der Stichprobenentnahme zu überdenken.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-106">This instruction uses the fourth element (.a or .w) to bias the texture-sampling level-of-detail just before sampling.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5c1d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5c1d-107">Syntax</span></span>



| <span data-ttu-id="b5c1d-108">texldb DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="b5c1d-108">texldb dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="b5c1d-109">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="b5c1d-109">Where:</span></span>

-   <span data-ttu-id="b5c1d-110">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-110">dst is the destination register.</span></span>
-   <span data-ttu-id="b5c1d-111">src0 ist ein Quell Register, das die Texturkoordinaten für das Textur Beispiel bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-111">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="b5c1d-112">Siehe [Texturkoordinaten Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="b5c1d-112">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="b5c1d-113">Quelle1 identifiziert den [Sampler (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , wobei \# angibt, welche Textur samplingnummer als Stichprobe angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-113">src1 identifies the [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="b5c1d-114">Der Sampler hat ihm eine Textur und einen samplerzustand zugeordnet, der durch [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype)definiert wird.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-114">The sampler has associated with it a texture and a sampler state defined by [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="b5c1d-115">Informationen zu den Einschränkungen bei der Verwendung von texldb finden Sie in der [texld-PS \_ 2 \_ 0-und up-](texld---ps-2-0.md) Anweisung.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-115">For the restrictions when using texldb, see the [texld - ps\_2\_0 and up](texld---ps-2-0.md) instruction.</span></span>

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="b5c1d-116">PS \_ 2 \_ 0 und PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b5c1d-116">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="b5c1d-117">DST muss ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) sein, und nur. xyzw Mask (Standard Maske) ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-117">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) and only .xyzw mask (default mask) is allowed.</span></span>

<span data-ttu-id="b5c1d-118">src0 muss entweder ein [Texturkoordinaten Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) oder ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) sein, ohne Modifizierer oder Swizzle.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-118">src0 must be either a [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t\#) or a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="b5c1d-119">Quelle1 muss ein [Sampler (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) sein \# , ohne Modifizierer oder Swizzle.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-119">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="b5c1d-120">Wenn das D3DD3DPSHADERCAPS2 \_ 0 \_ nodependentleselimit-Cap-Bit nicht festgelegt ist (in D3DPSHADERCAPS2 \_ 0), ist eine angegebene Textur Anweisung (texld, texldp, texldb, texldd) möglicherweise höchstens in dritter Reihenfolge abhängig.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-120">If the D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT cap bit is not set (in D3DPSHADERCAPS2\_0), a given texture instruction (texld, texldp, texldb, texldd) may be dependent upon, at most, third order.</span></span> <span data-ttu-id="b5c1d-121">Eine abhängige Textur Anweisung der ersten Bestellung ist eine Textur Anweisung, in der Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="b5c1d-121">A first-order dependent texture instruction is a texture instruction in which either:</span></span>

-   <span data-ttu-id="b5c1d-122">src0 ist ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="b5c1d-122">src0 is a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="b5c1d-123">DST wurde bereits geschrieben und wird nun erneut geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-123">dst was previously written, now being written again.</span></span>

<span data-ttu-id="b5c1d-124">Eine abhängige Textur Anweisung in zweiter Reihenfolge wird als Textur Anweisung definiert, die ein temporäres Register (r) liest oder in ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) schreibt, \# dessen Inhalt vor dem Ausführen der Textur Anweisung (möglicherweise indirekt) auf das Ergebnis einer abhängigen Textur Anweisung der ersten Bestellung angewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-124">A second-order dependent texture instruction is defined as a texture instruction that reads or writes to a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) whose contents, before executing the texture instruction, depend (perhaps indirectly) on the outcome of a first-order dependent texture instruction.</span></span> <span data-ttu-id="b5c1d-125">Eine (n) in der Reihenfolge abhängige Textur Anweisung wird von einer (n-1)<sup>th</sup>-<sup>Order-Textur</sup>Anweisung abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-125">An (n)<sup>th</sup>-order dependent texture instruction derives from an (n - 1)<sup>th</sup>-order texture instruction.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="b5c1d-126">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b5c1d-126">ps\_3\_0</span></span>

<span data-ttu-id="b5c1d-127">Quelle1 muss ein [Sampler (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# ohne Modifizierer sein.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-127">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier.</span></span> <span data-ttu-id="b5c1d-128">"Swizzle" ist auf Quelle1 zulässig. wenn diese Anwendung angewendet wird, werden die Ergebnisse der Textur Suche vor dem Schreiben in den DST vorgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-128">Swizzle is allowed on src1, and when applied, the texture lookup results are pre-swizzled before written to dst.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5c1d-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5c1d-129">Remarks</span></span>



| <span data-ttu-id="b5c1d-130">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="b5c1d-130">Pixel shader versions</span></span> | <span data-ttu-id="b5c1d-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="b5c1d-131">1\_1</span></span> | <span data-ttu-id="b5c1d-132">1\_2</span><span class="sxs-lookup"><span data-stu-id="b5c1d-132">1\_2</span></span> | <span data-ttu-id="b5c1d-133">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b5c1d-133">1\_3</span></span> | <span data-ttu-id="b5c1d-134">1\_4</span><span class="sxs-lookup"><span data-stu-id="b5c1d-134">1\_4</span></span> | <span data-ttu-id="b5c1d-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b5c1d-135">2\_0</span></span> | <span data-ttu-id="b5c1d-136">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b5c1d-136">2\_x</span></span> | <span data-ttu-id="b5c1d-137">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b5c1d-137">2\_sw</span></span> | <span data-ttu-id="b5c1d-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b5c1d-138">3\_0</span></span> | <span data-ttu-id="b5c1d-139">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b5c1d-139">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b5c1d-140">texldb</span><span class="sxs-lookup"><span data-stu-id="b5c1d-140">texldb</span></span>                |      |      |      |      | <span data-ttu-id="b5c1d-141">x</span><span class="sxs-lookup"><span data-stu-id="b5c1d-141">x</span></span>    | <span data-ttu-id="b5c1d-142">x</span><span class="sxs-lookup"><span data-stu-id="b5c1d-142">x</span></span>    | <span data-ttu-id="b5c1d-143">x</span><span class="sxs-lookup"><span data-stu-id="b5c1d-143">x</span></span>     | <span data-ttu-id="b5c1d-144">x</span><span class="sxs-lookup"><span data-stu-id="b5c1d-144">x</span></span>    | <span data-ttu-id="b5c1d-145">x</span><span class="sxs-lookup"><span data-stu-id="b5c1d-145">x</span></span>     |



 

<span data-ttu-id="b5c1d-146">texldb Bias die MipMap-Detailebene, die normalerweise als Teil des Beispiel Prozesses durch den (signierten) Wert in src0. w berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-146">texldb biases the mipmap level-of-detail, computed normally as part of the sample process by the (signed) value in src0.w.</span></span> <span data-ttu-id="b5c1d-147">Positive Bias-Werte führen dazu, dass kleinere Mipmaps ausgewählt werden und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-147">Positive bias values will result in smaller mipmaps being selected and vice versa.</span></span> <span data-ttu-id="b5c1d-148">Für PS \_ 2 \_ 0 und PS \_ 2 \_ x können sich die biaswerte im Bereich von \[ -3,0, + 3,0 befinden \] .</span><span class="sxs-lookup"><span data-stu-id="b5c1d-148">For ps\_2\_0 and ps\_2\_x, bias values can be within the range \[-3.0, +3.0\].</span></span> <span data-ttu-id="b5c1d-149">Bei PS \_ 3 \_ 0 können sich die Werte für die Anzahl der Werte im Bereich von \[ -16,0, + 15,0 befinden \] .</span><span class="sxs-lookup"><span data-stu-id="b5c1d-149">For ps\_3\_0, bias values can be within the range \[-16.0, +15.0\].</span></span> <span data-ttu-id="b5c1d-150">Durch biaswerte außerhalb dieser Bereiche werden nicht definierte Ergebnisse erzeugt.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-150">Bias values outside these ranges produce undefined results.</span></span> <span data-ttu-id="b5c1d-151">Der samplerstatus D3DSAMP \_ mipmaplodbias wird immer noch berücksichtigt, und der texldb-Bias wird diesem hinzugefügt, jedoch pro Pixel.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-151">The sampler state D3DSAMP\_MIPMAPLODBIAS is still honored, and the texldb bias is added to this, but on a per-pixel basis.</span></span> <span data-ttu-id="b5c1d-152">Nachdem der ebenengrad ausführlich berechnet wurde, \_ wird D3DSAMP MaxMipLevel weiterhin berücksichtigt, und das Textur Beispiel wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-152">After the biased level-of-detail is computed, D3DSAMP\_MAXMIPLEVEL is still honored and the texture sample occurs.</span></span> <span data-ttu-id="b5c1d-153">Nach der texldb ist der Inhalt von src0 nicht betroffen (es sei denn, DST ist dasselbe Register).</span><span class="sxs-lookup"><span data-stu-id="b5c1d-153">After texldb, the contents of src0 are unaffected (unless dst is the same register).</span></span>

<span data-ttu-id="b5c1d-154">Die Anzahl der Koordinaten, die erforderlich sind, damit src0 das Textur Beispiel durchführen kann, hängt davon ab, wie Quelle1 deklariert wurde, sowie der. w-Komponente.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-154">The number of coordinates required for src0 to perform the texture sample depends on how src1 was declared, plus the .w component.</span></span> <span data-ttu-id="b5c1d-155">[ \_ Samplertypen werden mit DCL samplertype (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)deklariert.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-155">Sampler types are declared with [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md).</span></span> <span data-ttu-id="b5c1d-156">Wenn Quelle1 als 2D-Sampler deklariert ist, muss src0. xyw-Koordinaten enthalten. Wenn Quelle1 entweder als Cube-Sampler oder als volumesampler deklariert ist, muss src0. xyzw-Koordinaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-156">If src1 is declared as a 2D sampler, then src0 must contain .xyw coordinates; if src1 is declared as either a cube sampler or a volume sampler, then src0 must contain .xyzw coordinates.</span></span> <span data-ttu-id="b5c1d-157">Die Stichprobenentnahme einer 2D-Textur mit xyzw-Koordinaten ist zulässig (die. z-Koordinate wird ignoriert).</span><span class="sxs-lookup"><span data-stu-id="b5c1d-157">Sampling a 2D texture with .xyzw coordinates is allowed (the .z coordinate is ignored).</span></span>

<span data-ttu-id="b5c1d-158">Wenn die Quell Textur weniger als vier Komponenten enthält, werden die fehlenden Komponenten als Standardwerte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-158">If the source texture contains fewer than four components, defaults are placed in the missing components.</span></span> <span data-ttu-id="b5c1d-159">Standardwerte hängen vom Textur Format ab, wie in der folgenden Tabelle gezeigt:</span><span class="sxs-lookup"><span data-stu-id="b5c1d-159">Defaults depend on the texture format as shown in the following table:</span></span>



| <span data-ttu-id="b5c1d-160">Textur Format</span><span class="sxs-lookup"><span data-stu-id="b5c1d-160">Texture Format</span></span>                                                                                          | <span data-ttu-id="b5c1d-161">Standardwerte</span><span class="sxs-lookup"><span data-stu-id="b5c1d-161">Default Values</span></span>       |
|---------------------------------------------------------------------------------------------------------|----------------------|
| <span data-ttu-id="b5c1d-162">D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ L8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5</span><span class="sxs-lookup"><span data-stu-id="b5c1d-162">D3DFMT\_R5G6B5, D3DFMT\_R8G8B8, D3DFMT\_L8, D3DFMT\_L16, D3DFMT\_R3G3B2, D3DFMT\_CxV8U8, D3DFMT\_L6V5U5</span></span> | <span data-ttu-id="b5c1d-163">A = 1,0</span><span class="sxs-lookup"><span data-stu-id="b5c1d-163">A = 1.0</span></span>              |
| <span data-ttu-id="b5c1d-164">D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT \_ G16R16F, D3DFMT \_ G32R32F</span><span class="sxs-lookup"><span data-stu-id="b5c1d-164">D3DFMT\_V8U8, D3DFMT\_V16U16, D3DFMT\_G16R16, D3DFMT\_G16R16F, D3DFMT\_G32R32F</span></span>                          | <span data-ttu-id="b5c1d-165">B = a = 1,0</span><span class="sxs-lookup"><span data-stu-id="b5c1d-165">B = A = 1.0</span></span>          |
| <span data-ttu-id="b5c1d-166">D3DFMT \_ a8</span><span class="sxs-lookup"><span data-stu-id="b5c1d-166">D3DFMT\_A8</span></span>                                                                                              | <span data-ttu-id="b5c1d-167">R = G = B = 0,0</span><span class="sxs-lookup"><span data-stu-id="b5c1d-167">R = G = B = 0.0</span></span>      |
| <span data-ttu-id="b5c1d-168">D3DFMT \_ R16F, D3DFMT \_ R32F</span><span class="sxs-lookup"><span data-stu-id="b5c1d-168">D3DFMT\_R16F, D3DFMT\_R32F</span></span>                                                                              | <span data-ttu-id="b5c1d-169">G = B = a = 1,0</span><span class="sxs-lookup"><span data-stu-id="b5c1d-169">G = B = A = 1.0</span></span>      |
| <span data-ttu-id="b5c1d-170">Alle tiefen/Schablonen Formate</span><span class="sxs-lookup"><span data-stu-id="b5c1d-170">All depth/stencil formats</span></span>                                                                               | <span data-ttu-id="b5c1d-171">R = B = 0,0, A = 1,0</span><span class="sxs-lookup"><span data-stu-id="b5c1d-171">R = B = 0.0, A = 1.0</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b5c1d-172">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b5c1d-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5c1d-173">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="b5c1d-173">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 