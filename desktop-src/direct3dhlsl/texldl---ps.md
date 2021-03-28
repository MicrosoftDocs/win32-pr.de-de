---
title: texldl-PS
description: Beispiel für eine Textur mit einem bestimmten Sampler. Die jeweilige MipMap-Detailebene, für die ein Sampling durchgeführt wird, muss als vierte Komponente der Textur Koordinate angegeben werden. | texldl-PS
ms.assetid: f0ca8a1d-ac98-49ef-850a-c534e986c7ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6ab8a6f55ce5e069a01edb5d281bfe506c5fee6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981137"
---
# <a name="texldl---ps"></a><span data-ttu-id="1b9c4-105">texldl-PS</span><span class="sxs-lookup"><span data-stu-id="1b9c4-105">texldl - ps</span></span>

<span data-ttu-id="1b9c4-106">Beispiel für eine Textur mit einem bestimmten Sampler.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-106">Sample a texture with a particular sampler.</span></span> <span data-ttu-id="1b9c4-107">Die jeweilige MipMap-Detailebene, für die ein Sampling durchgeführt wird, muss als vierte Komponente der Textur Koordinate angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-107">The particular mipmap level-of-detail being sampled has to be specified as the fourth component of the texture coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b9c4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b9c4-108">Syntax</span></span>



| <span data-ttu-id="1b9c4-109">texldl DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="1b9c4-109">texldl dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="1b9c4-110">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="1b9c4-110">Where:</span></span>

-   <span data-ttu-id="1b9c4-111">DST ist ein Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-111">dst is a destination register.</span></span>
-   <span data-ttu-id="1b9c4-112">src0 ist ein Quell Register, das die Texturkoordinaten für das Textur Beispiel bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-112">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="1b9c4-113">Siehe [Texturkoordinaten Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="1b9c4-113">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="1b9c4-114">Quelle1 identifiziert die Quell-Samplerregister \# , bei der \# angibt, welche Textur samplingnummer Stichproben geben soll.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-114">src1 identifies the source sampler register (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="1b9c4-115">Der Sampler hat ihm eine Textur und einen Steuerelement Zustand zugeordnet, der durch die [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) -Enumeration definiert ist (z \_ . b. D3DSAMP MinFilter).</span><span class="sxs-lookup"><span data-stu-id="1b9c4-115">The sampler has associated with it a texture and a control state defined by the [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) enumeration (for example, D3DSAMP\_MINFILTER).</span></span>

## <a name="remarks"></a><span data-ttu-id="1b9c4-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b9c4-116">Remarks</span></span>



| <span data-ttu-id="1b9c4-117">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="1b9c4-117">Pixel shader versions</span></span> | <span data-ttu-id="1b9c4-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="1b9c4-118">1\_1</span></span> | <span data-ttu-id="1b9c4-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="1b9c4-119">1\_2</span></span> | <span data-ttu-id="1b9c4-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1b9c4-120">1\_3</span></span> | <span data-ttu-id="1b9c4-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="1b9c4-121">1\_4</span></span> | <span data-ttu-id="1b9c4-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1b9c4-122">2\_0</span></span> | <span data-ttu-id="1b9c4-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="1b9c4-123">2\_x</span></span> | <span data-ttu-id="1b9c4-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="1b9c4-124">2\_sw</span></span> | <span data-ttu-id="1b9c4-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1b9c4-125">3\_0</span></span> | <span data-ttu-id="1b9c4-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="1b9c4-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="1b9c4-127">texldl</span><span class="sxs-lookup"><span data-stu-id="1b9c4-127">texldl</span></span>                |      |      |      |      |      |      |       | <span data-ttu-id="1b9c4-128">x</span><span class="sxs-lookup"><span data-stu-id="1b9c4-128">x</span></span>    | <span data-ttu-id="1b9c4-129">x</span><span class="sxs-lookup"><span data-stu-id="1b9c4-129">x</span></span>     |



 

<span data-ttu-id="1b9c4-130">texldl sucht den Textur Satz in der Samplingphase, auf die von Quelle1 verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-130">texldl looks up the texture set at the sampler stage referenced by src1.</span></span> <span data-ttu-id="1b9c4-131">Die Detailebene wird aus src0. w ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-131">The level-of-detail is selected from src0.w.</span></span> <span data-ttu-id="1b9c4-132">Dieser Wert kann negativ sein. in diesem Fall handelt es sich bei der ausgewählten Detailebene um die nullten (größte Karte) mit dem MagFilter.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-132">This value can be negative in which case the level-of-detail selected is the zeroth one (biggest map) with the MAGFILTER.</span></span> <span data-ttu-id="1b9c4-133">Da src0. w ein Gleit Komma Wert ist, wird der Bruchteil-Wert verwendet, um zwischen zwei MIP-Ebenen zu interpolieren (wenn MipFilter linear ist).</span><span class="sxs-lookup"><span data-stu-id="1b9c4-133">Since src0.w is a floating point value, the fractional value is used to interpolate (if MIPFILTER is LINEAR) between two mip levels.</span></span> <span data-ttu-id="1b9c4-134">Die samplerzustände mipmaplodbias und MaxMipLevel werden berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-134">Sampler states MIPMAPLODBIAS and MAXMIPLEVEL are honored.</span></span> <span data-ttu-id="1b9c4-135">Weitere Informationen zu samplerzuständen finden Sie unter [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="1b9c4-135">For more information about sampler states, see [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="1b9c4-136">Wenn ein Shader-Programm eine Stichprobe von einem Sampler durchführt, der keinen Textur Satz hat, wird 0001 im Ziel Register abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-136">If a shader program samples from a sampler that does not have a texture set, then 0001 is obtained in the destination register.</span></span>

<span data-ttu-id="1b9c4-137">Im folgenden finden Sie einen groben Algorithmus, dem das Referenzgerät folgt:</span><span class="sxs-lookup"><span data-stu-id="1b9c4-137">The following is a rough algorithm that the reference device follows:</span></span>


```
LOD = src0.w + LODBIAS;
if (LOD <= 0 )
{
   LOD = 0;
   Filter = MagFilter;
   tex = Lookup( MAX(MAXMIPLEVEL, LOD), Filter );
}
else
{
   Filter = MinFilter;
   LOD = MAX( MAXMIPLEVEL, LOD );
   tex = Lookup( Floor(LOD), Filter );
   if( MipFilter == LINEAR )
   {
      tex1 = Lookup( Ceil(LOD), Filter );                        
      tex = (1 - frac(src0.w))*tex + frac(src0.w)*tex1;
   }
}
```



<span data-ttu-id="1b9c4-138">Begrenzungen</span><span class="sxs-lookup"><span data-stu-id="1b9c4-138">Restrictions:</span></span>

-   <span data-ttu-id="1b9c4-139">Die Texturkoordinaten sollten nicht nach Textur Größe skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-139">The texture coordinates should not be scaled by texture size.</span></span>
-   <span data-ttu-id="1b9c4-140">DST muss ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) sein.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-140">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="1b9c4-141">DST kann einen Schreib Versuch akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-141">dst can accept a writemask.</span></span> <span data-ttu-id="1b9c4-142">Siehe [Ziel Registrierung schreiben Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span><span class="sxs-lookup"><span data-stu-id="1b9c4-142">See [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>
-   <span data-ttu-id="1b9c4-143">Die Standardwerte für fehlende Komponenten sind entweder 0 oder 1 und hängen vom Textur Format ab.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-143">Defaults for missing components are either 0 or 1, and depend on the texture format.</span></span>
-   <span data-ttu-id="1b9c4-144">Quelle1 muss ein [Sampler (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) sein \# .</span><span class="sxs-lookup"><span data-stu-id="1b9c4-144">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#).</span></span> <span data-ttu-id="1b9c4-145">Quelle1 darf keinen Negation-Modifizierer verwenden (siehe [Ziel-Register Schreib Maske](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)).</span><span class="sxs-lookup"><span data-stu-id="1b9c4-145">src1 may not use a negate modifier (see [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)).</span></span> <span data-ttu-id="1b9c4-146">Quelle1 verwendet möglicherweise "Swizzle" (siehe [Quell Register "Schwenken](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)"), das nach dem Sampling angewendet wird, jedoch vor der Schreib Maske (siehe Ziel-Register Schreib Maske) berücksichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-146">src1 may use swizzle (see [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)), which is applied after sampling, but before the write mask (see Destination Register Write Mask) is honored.</span></span> <span data-ttu-id="1b9c4-147">Der Sampler muss am Anfang des Shader (mit [DCL- \_ samplertype (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)) deklariert worden sein.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-147">The sampler must have been declared (using [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md)) at the beginning of the shader.</span></span>
-   <span data-ttu-id="1b9c4-148">Die Anzahl der Koordinaten, die zum Ausführen des Textur Beispiels erforderlich sind, hängt davon ab, wie der Sampler deklariert wurde.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-148">The number of coordinates required to perform the texture sample depends on how the sampler was declared.</span></span> <span data-ttu-id="1b9c4-149">Wenn Sie als Cube deklariert wurde, ist eine Textur Koordinate mit drei Komponenten erforderlich (. RGB).</span><span class="sxs-lookup"><span data-stu-id="1b9c4-149">If it was declared as a cube, a three-component texture coordinate is required (.rgb).</span></span> <span data-ttu-id="1b9c4-150">Die Validierung erzwingt, dass für die Tex-LDL bereitgestellte Koordinaten \_ für die für den Sampler deklarierte Textur Dimension ausreichend sind.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-150">Validation enforces that coordinates provided to tex\_ldl Are sufficient for the texture dimension declared for the sampler.</span></span> <span data-ttu-id="1b9c4-151">Es ist jedoch nicht sichergestellt, dass die Anwendung tatsächlich eine Textur (über die API) mit Dimensionen festlegt, die der für den Sampler deklarierten Dimension entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-151">However, it is not guaranteed that the application actually sets a texture (through the API) with dimensions equal to the dimension declared for the sampler.</span></span> <span data-ttu-id="1b9c4-152">In einem solchen Fall versucht die Laufzeit, Konflikte zu erkennen (möglicherweise nur im Debugmodus).</span><span class="sxs-lookup"><span data-stu-id="1b9c4-152">In such a case, the runtime will attempt to detect mismatches (possibly in debug only).</span></span> <span data-ttu-id="1b9c4-153">Das Sampling einer Textur mit weniger Dimensionen, als in der Textur Koordinate vorhanden sind, wird zugelassen, und es wird davon ausgegangen, dass die zusätzlichen Texturkoordinaten Komponenten ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-153">Sampling a texture with fewer dimensions than are present in the texture coordinate will be allowed and assumed to ignore the extra texture coordinate components.</span></span> <span data-ttu-id="1b9c4-154">Umgekehrt ist das Sampling einer Textur mit mehr Dimensionen als in der Textur Koordinate nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-154">Conversely, sampling a texture with more dimensions than are present in the texture coordinate is illegal.</span></span>
-   <span data-ttu-id="1b9c4-155">Wenn src0 (Textur Koordinate) [temporär registriert](dx9-graphics-reference-asm-ps-registers-temporary.md)ist, müssen die für die Suche (oben beschriebenen) erforderlichen Komponenten bereits geschrieben worden sein.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-155">If the src0 (texture coordinate) is [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md), the components required for the lookup (described above) must have been previously written.</span></span>
-   <span data-ttu-id="1b9c4-156">Die Stichprobenentnahme nicht signierter RGB-Texturen führt zu float-Werten zwischen 0,0 und 1,0.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-156">Sampling unsigned RGB textures will result in float values between 0.0 and 1.0.</span></span>
-   <span data-ttu-id="1b9c4-157">Die Stichproben signierter Texturen führen zu float-Werten zwischen-1,0 und 1,0.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-157">Sampling signed textures will result in float values between -1.0 to 1.0.</span></span>
-   <span data-ttu-id="1b9c4-158">Beim Sampling von Gleit Komma Texturen bedeutet Float16, dass die Daten innerhalb von Max \_ . Float16 liegen.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-158">When sampling floating-point textures, Float16 means that the data will range within MAX\_FLOAT16.</span></span> <span data-ttu-id="1b9c4-159">Float32 bedeutet, dass der maximale Bereich der Pipeline verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-159">Float32 means the maximum range of the pipeline will be used.</span></span> <span data-ttu-id="1b9c4-160">Die Stichprobenentnahme außerhalb eines Bereichs ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-160">Sampling outside of either range is undefined.</span></span>
-   <span data-ttu-id="1b9c4-161">Es gibt keine abhängige Lese Beschränkung.</span><span class="sxs-lookup"><span data-stu-id="1b9c4-161">There is no dependent read limit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b9c4-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1b9c4-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b9c4-163">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="1b9c4-163">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
