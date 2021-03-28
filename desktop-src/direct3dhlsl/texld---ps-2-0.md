---
title: texld-PS_2_0 und aufwärts
description: Beispiel für eine Textur bei einem bestimmten Sampler mithilfe der angegebenen Texturkoordinaten. Diese Anweisung unterscheidet sich von der texld-PS \_ 1 4-Anweisung, die \_ in Pixel-Shader, Version 1 4, verwendet wird \_ .
ms.assetid: 2b0d02b4-d9dd-4388-aa86-03b27bc4fdc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b71990e230290403bca2a5af11eeca11b093402f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516886"
---
# <a name="texld---ps_2_0-and-up"></a><span data-ttu-id="56f15-104">texld-PS \_ 2 \_ 0 und aufwärts</span><span class="sxs-lookup"><span data-stu-id="56f15-104">texld - ps\_2\_0 and up</span></span>

<span data-ttu-id="56f15-105">Beispiel für eine Textur bei einem bestimmten Sampler mithilfe der angegebenen Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="56f15-105">Sample a texture at a particular sampler, using provided texture coordinates.</span></span> <span data-ttu-id="56f15-106">Diese Anweisung unterscheidet sich von der [texld-PS \_ 1 \_ 4-](texld---ps-1-4.md) Anweisung, die in Pixel-Shader, Version 1 4, verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="56f15-106">This instruction is different from the [texld - ps\_1\_4](texld---ps-1-4.md) instruction used in pixel shader version 1\_4.</span></span>

## <a name="syntax"></a><span data-ttu-id="56f15-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="56f15-107">Syntax</span></span>



| <span data-ttu-id="56f15-108">texld DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="56f15-108">texld dst, src0, src1</span></span> |
|-----------------------|



 

<span data-ttu-id="56f15-109">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="56f15-109">Where:</span></span>

-   <span data-ttu-id="56f15-110">DST ist ein Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="56f15-110">dst is a destination register.</span></span>
-   <span data-ttu-id="56f15-111">src0 ist ein Quell Register, das die Texturkoordinaten für das Textur Beispiel bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="56f15-111">src0 is a source register that provides the texture coordinates for the texture sample.</span></span>
-   <span data-ttu-id="56f15-112">Quelle1 identifiziert den [Sampler (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , wobei \# angibt, welche Textur samplingnummer als Stichprobe angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="56f15-112">src1 identifies the [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="56f15-113">Der Sampler hat ihm eine Textur und einen samplerzustand zugeordnet, der durch [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype)definiert wird.</span><span class="sxs-lookup"><span data-stu-id="56f15-113">The sampler has associated with it a texture and a sampler state defined by [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="56f15-114">PS \_ 2 \_ 0 und PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="56f15-114">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="56f15-115">DST muss ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) sein, und nur. xyzw Mask (Standard Maske) ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="56f15-115">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) and only .xyzw mask (default mask) is allowed.</span></span>

<span data-ttu-id="56f15-116">src0 muss entweder ein [Texturkoordinaten Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) oder ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) sein, ohne Modifizierer oder Swizzle.</span><span class="sxs-lookup"><span data-stu-id="56f15-116">src0 must be either a [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t\#) or a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="56f15-117">Quelle1 muss ein [Sampler (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) sein \# , ohne Modifizierer oder Swizzle.</span><span class="sxs-lookup"><span data-stu-id="56f15-117">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="56f15-118">Wenn das D3DD3DPSHADERCAPS2 \_ 0 \_ nodependentleselimit-Cap-Bit nicht festgelegt ist (in D3DPSHADERCAPS2 \_ 0), ist eine angegebene Textur Anweisung ([texld](texld---ps-1-4.md), [texldp](texldp---ps.md), [texldb-PS](texldb---ps.md), [texldd](texldd---ps.md) ) möglicherweise höchstens in dritter Reihenfolge abhängig.</span><span class="sxs-lookup"><span data-stu-id="56f15-118">If the D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT cap bit is not set (in D3DPSHADERCAPS2\_0), a given texture instruction ([texld](texld---ps-1-4.md), [texldp](texldp---ps.md), [texldb - ps](texldb---ps.md), [texldd](texldd---ps.md) ) may be dependent upon, at most, third order.</span></span> <span data-ttu-id="56f15-119">Eine abhängige Textur Anweisung der ersten Bestellung ist eine Textur Anweisung, in der Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="56f15-119">A first-order dependent texture instruction is a texture instruction in which either:</span></span>

-   <span data-ttu-id="56f15-120">src0 ist ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="56f15-120">src0 is a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="56f15-121">DST wurde bereits geschrieben und wird nun erneut geschrieben.</span><span class="sxs-lookup"><span data-stu-id="56f15-121">dst was previously written, now being written again.</span></span>

<span data-ttu-id="56f15-122">Eine abhängige Textur Anweisung in zweiter Reihenfolge wird als Textur Anweisung definiert, die ein temporäres Register (r) liest oder in ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) schreibt, \# dessen Inhalt vor dem Ausführen der Textur Anweisung (möglicherweise indirekt) auf das Ergebnis einer abhängigen Textur Anweisung der ersten Bestellung angewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="56f15-122">A second-order dependent texture instruction is defined as a texture instruction that reads or writes to a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) whose contents, before executing the texture instruction, depend (perhaps indirectly) on the outcome of a first-order dependent texture instruction.</span></span> <span data-ttu-id="56f15-123">Eine (n) in der Reihenfolge abhängige Textur Anweisung wird von einer (n-1)<sup>th</sup>-<sup>Order-Textur</sup>Anweisung abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="56f15-123">An (n)<sup>th</sup>-order dependent texture instruction derives from an (n - 1)<sup>th</sup>-order texture instruction.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="56f15-124">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="56f15-124">ps\_3\_0</span></span>

<span data-ttu-id="56f15-125">Quelle1 muss ein [Sampler (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# ohne Modifizierer sein.</span><span class="sxs-lookup"><span data-stu-id="56f15-125">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier.</span></span> <span data-ttu-id="56f15-126">Swizzle ist für src0 oder Quelle1 zulässig.</span><span class="sxs-lookup"><span data-stu-id="56f15-126">Swizzle is allowed on src0 or src1.</span></span> <span data-ttu-id="56f15-127">Das Swizzle wird vor der Textur Suche auf die Textur Koordinate angewendet.</span><span class="sxs-lookup"><span data-stu-id="56f15-127">The swizzle is applied to the texture coordintates before texture lookup.</span></span>

## <a name="remarks"></a><span data-ttu-id="56f15-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56f15-128">Remarks</span></span>

<span data-ttu-id="56f15-129">Diese Anweisung wird in den folgenden Versionen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="56f15-129">This instruction is supported in the following versions:</span></span>



| <span data-ttu-id="56f15-130">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="56f15-130">Pixel shader versions</span></span> | <span data-ttu-id="56f15-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="56f15-131">1\_1</span></span> | <span data-ttu-id="56f15-132">1\_2</span><span class="sxs-lookup"><span data-stu-id="56f15-132">1\_2</span></span> | <span data-ttu-id="56f15-133">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="56f15-133">1\_3</span></span> | <span data-ttu-id="56f15-134">1\_4</span><span class="sxs-lookup"><span data-stu-id="56f15-134">1\_4</span></span> | <span data-ttu-id="56f15-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="56f15-135">2\_0</span></span> | <span data-ttu-id="56f15-136">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="56f15-136">2\_x</span></span> | <span data-ttu-id="56f15-137">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="56f15-137">2\_sw</span></span> | <span data-ttu-id="56f15-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="56f15-138">3\_0</span></span> | <span data-ttu-id="56f15-139">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="56f15-139">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="56f15-140">texld</span><span class="sxs-lookup"><span data-stu-id="56f15-140">texld</span></span>                 |      |      |      |      | <span data-ttu-id="56f15-141">x</span><span class="sxs-lookup"><span data-stu-id="56f15-141">x</span></span>    | <span data-ttu-id="56f15-142">x</span><span class="sxs-lookup"><span data-stu-id="56f15-142">x</span></span>    | <span data-ttu-id="56f15-143">x</span><span class="sxs-lookup"><span data-stu-id="56f15-143">x</span></span>     | <span data-ttu-id="56f15-144">x</span><span class="sxs-lookup"><span data-stu-id="56f15-144">x</span></span>    | <span data-ttu-id="56f15-145">x</span><span class="sxs-lookup"><span data-stu-id="56f15-145">x</span></span>     |



 

<span data-ttu-id="56f15-146">Die Anzahl der Koordinaten, die erforderlich sind, damit src0 das Textur Beispiel durchführen kann, hängt davon ab, wie Quelle1 deklariert wurde, sowie der. w-Komponente.</span><span class="sxs-lookup"><span data-stu-id="56f15-146">The number of coordinates required for src0 to perform the texture sample depends on how src1 was declared, plus the .w component.</span></span> <span data-ttu-id="56f15-147">[ \_ Samplertypen werden mit DCL samplertype (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)deklariert.</span><span class="sxs-lookup"><span data-stu-id="56f15-147">Sampler types are declared with [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md).</span></span> <span data-ttu-id="56f15-148">Wenn Quelle1 als 2D-Sampler deklariert ist, muss src0. XY-Koordinaten enthalten. Wenn Quelle1 entweder als Cube-Sampler oder als volumesampler deklariert ist, muss src0 die. XYZ-Koordinaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="56f15-148">If src1 is declared as a 2D sampler, then src0 must contain .xy coordinates; if src1 is declared as either a cube sampler or a volume sampler, then src0 must contain .xyz coordinates.</span></span> <span data-ttu-id="56f15-149">Das Sampling einer Textur mit weniger Dimensionen als in der Textur Koordinate vorhanden ist zulässig, da die zusätzlichen Texturkoordinaten Komponenten ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="56f15-149">Sampling a texture with fewer dimensions than are present in the texture coordinate is allowed since the extra texture coordinate component(s) are ignored.</span></span>

<span data-ttu-id="56f15-150">Wenn die Quell Textur weniger als vier Komponenten enthält, werden die fehlenden Komponenten als Standardwerte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="56f15-150">If the source texture contains fewer than four components, defaults are placed in the missing components.</span></span> <span data-ttu-id="56f15-151">Standardwerte hängen vom Textur Format ab, wie in der folgenden Tabelle gezeigt:</span><span class="sxs-lookup"><span data-stu-id="56f15-151">Defaults depend on the texture format as shown in the following table:</span></span>



| <span data-ttu-id="56f15-152">Textur Format</span><span class="sxs-lookup"><span data-stu-id="56f15-152">Texture Format</span></span>                                                                                          | <span data-ttu-id="56f15-153">Standardwerte</span><span class="sxs-lookup"><span data-stu-id="56f15-153">Default Values</span></span>       |
|---------------------------------------------------------------------------------------------------------|----------------------|
| <span data-ttu-id="56f15-154">D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ L8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5</span><span class="sxs-lookup"><span data-stu-id="56f15-154">D3DFMT\_R5G6B5, D3DFMT\_R8G8B8, D3DFMT\_L8, D3DFMT\_L16, D3DFMT\_R3G3B2, D3DFMT\_CxV8U8, D3DFMT\_L6V5U5</span></span> | <span data-ttu-id="56f15-155">A = 1,0</span><span class="sxs-lookup"><span data-stu-id="56f15-155">A = 1.0</span></span>              |
| <span data-ttu-id="56f15-156">D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT \_ G16R16F, D3DFMT \_ G32R32F</span><span class="sxs-lookup"><span data-stu-id="56f15-156">D3DFMT\_V8U8, D3DFMT\_V16U16, D3DFMT\_G16R16, D3DFMT\_G16R16F, D3DFMT\_G32R32F</span></span>                          | <span data-ttu-id="56f15-157">B = a = 1,0</span><span class="sxs-lookup"><span data-stu-id="56f15-157">B = A = 1.0</span></span>          |
| <span data-ttu-id="56f15-158">D3DFMT \_ a8</span><span class="sxs-lookup"><span data-stu-id="56f15-158">D3DFMT\_A8</span></span>                                                                                              | <span data-ttu-id="56f15-159">R = G = B = 0,0</span><span class="sxs-lookup"><span data-stu-id="56f15-159">R = G = B = 0.0</span></span>      |
| <span data-ttu-id="56f15-160">D3DFMT \_ R16F, D3DFMT \_ R32F</span><span class="sxs-lookup"><span data-stu-id="56f15-160">D3DFMT\_R16F, D3DFMT\_R32F</span></span>                                                                              | <span data-ttu-id="56f15-161">G = B = a = 1,0</span><span class="sxs-lookup"><span data-stu-id="56f15-161">G = B = A = 1.0</span></span>      |
| <span data-ttu-id="56f15-162">Alle tiefen/Schablonen Formate</span><span class="sxs-lookup"><span data-stu-id="56f15-162">All depth/stencil formats</span></span>                                                                               | <span data-ttu-id="56f15-163">R = B = 0,0, A = 1,0</span><span class="sxs-lookup"><span data-stu-id="56f15-163">R = B = 0.0, A = 1.0</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="56f15-164">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="56f15-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56f15-165">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="56f15-165">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 