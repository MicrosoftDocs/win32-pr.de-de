---
title: texldl-vs
description: Beispiel für eine Textur mit einem bestimmten Sampler. Die jeweilige MipMap-Detailebene, für die ein Sampling durchgeführt wird, muss als vierte Komponente der Textur Koordinate angegeben werden. | texldl-vs
ms.assetid: 774c058d-7b3e-46a9-adce-c9a44efefd78
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: be9240f5307bb1e70b1f10cc1e392b92e5833fd8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104050768"
---
# <a name="texldl---vs"></a><span data-ttu-id="3020f-105">texldl-vs</span><span class="sxs-lookup"><span data-stu-id="3020f-105">texldl - vs</span></span>

<span data-ttu-id="3020f-106">Beispiel für eine Textur mit einem bestimmten Sampler.</span><span class="sxs-lookup"><span data-stu-id="3020f-106">Sample a texture with a particular sampler.</span></span> <span data-ttu-id="3020f-107">Die jeweilige MipMap-Detailebene, für die ein Sampling durchgeführt wird, muss als vierte Komponente der Textur Koordinate angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3020f-107">The particular mipmap level-of-detail being sampled has to be specified as the fourth component of the texture coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="3020f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3020f-108">Syntax</span></span>



| <span data-ttu-id="3020f-109">texldl DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="3020f-109">texldl dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="3020f-110">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="3020f-110">Where:</span></span>

-   <span data-ttu-id="3020f-111">DST ist ein Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="3020f-111">dst is a destination register.</span></span>
-   <span data-ttu-id="3020f-112">src0 ist ein Quell Register, das die Texturkoordinaten für das Textur Beispiel bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="3020f-112">src0 is a source register that provides the texture coordinates for the texture sample.</span></span>
-   <span data-ttu-id="3020f-113">Quelle1 identifiziert die Quell-Samplerregister \# , bei der \# angibt, welche Textur samplingnummer Stichproben geben soll.</span><span class="sxs-lookup"><span data-stu-id="3020f-113">src1 identifies the source sampler register (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="3020f-114">Der Sampler hat ihm eine Textur und einen Steuerelement Zustand zugeordnet, der durch die [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) -Enumeration definiert ist (z \_ . b. D3DSAMP MinFilter).</span><span class="sxs-lookup"><span data-stu-id="3020f-114">The sampler has associated with it a texture and a control state defined by the [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) enumeration (for example, D3DSAMP\_MINFILTER).</span></span>

## <a name="remarks"></a><span data-ttu-id="3020f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3020f-115">Remarks</span></span>



| <span data-ttu-id="3020f-116">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="3020f-116">Vertex shader versions</span></span> | <span data-ttu-id="3020f-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="3020f-117">1\_1</span></span> | <span data-ttu-id="3020f-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3020f-118">2\_0</span></span> | <span data-ttu-id="3020f-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3020f-119">2\_x</span></span> | <span data-ttu-id="3020f-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3020f-120">2\_sw</span></span> | <span data-ttu-id="3020f-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3020f-121">3\_0</span></span> | <span data-ttu-id="3020f-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3020f-122">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="3020f-123">texldl</span><span class="sxs-lookup"><span data-stu-id="3020f-123">texldl</span></span>                 |      |      |      |       | <span data-ttu-id="3020f-124">x</span><span class="sxs-lookup"><span data-stu-id="3020f-124">x</span></span>    | <span data-ttu-id="3020f-125">x</span><span class="sxs-lookup"><span data-stu-id="3020f-125">x</span></span>     |



 

<span data-ttu-id="3020f-126">texldl sucht den Textur Satz in der Samplingphase, auf die von Quelle1 verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="3020f-126">texldl looks up the texture set at the sampler stage referenced by src1.</span></span> <span data-ttu-id="3020f-127">Die Detailebene wird aus src0. w ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="3020f-127">The level-of-detail is selected from src0.w.</span></span> <span data-ttu-id="3020f-128">Dieser Wert kann negativ sein. in diesem Fall ist die ausgewählte Detailstufe die "nullte 1" (größte Zuordnung) mit dem "MagFilter".</span><span class="sxs-lookup"><span data-stu-id="3020f-128">This value can be negative, in which case the level-of-detail selected is the "zeroth one" (biggest map) with the MAGFILTER.</span></span> <span data-ttu-id="3020f-129">Da src0. w ein Gleit Komma Wert ist, wird der Bruchteil-Wert verwendet, um zwischen zwei MIP-Ebenen zu interpolieren (wenn MipFilter linear ist).</span><span class="sxs-lookup"><span data-stu-id="3020f-129">Because src0.w is a floating point value, the fractional value is used to interpolate (if MIPFILTER is LINEAR) between two mip levels.</span></span> <span data-ttu-id="3020f-130">Die samplerzustände mipmaplodbias und MaxMipLevel werden berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="3020f-130">Sampler states MIPMAPLODBIAS and MAXMIPLEVEL are honored.</span></span> <span data-ttu-id="3020f-131">Weitere Informationen zu samplerzuständen finden Sie unter [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="3020f-131">For more information about sampler states, see [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="3020f-132">Wenn ein Shader-Programm eine Stichprobe von einem Sampler erstellt, der keinen Textur Satz hat, wird 0001 im Ziel Register abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3020f-132">If a shader program samples from a sampler that does not have a texture set, 0001 is obtained in the destination register.</span></span>

<span data-ttu-id="3020f-133">Dies ist eine Näherung zum Referenzgeräte Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="3020f-133">This is an approximation to the reference device algorithm.</span></span>


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
   LOD = MAX( MAXMIPLEVEL, LOD);
   tex = Lookup( Floor(LOD), Filter );
   if( MipFilter == LINEAR )
   {
      tex1 = Lookup( Ceil(LOD), Filter );                        
      tex = (1 - frac(src0.w))*tex + frac(src0.w)*tex1;
   }
}
```



<span data-ttu-id="3020f-134">Begrenzungen</span><span class="sxs-lookup"><span data-stu-id="3020f-134">Restrictions:</span></span>

-   <span data-ttu-id="3020f-135">Die Texturkoordinaten sollten nicht nach Textur Größe skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="3020f-135">The texture coordinates should not be scaled by texture size.</span></span>
-   <span data-ttu-id="3020f-136">DST muss ein [temporäres Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ) sein.</span><span class="sxs-lookup"><span data-stu-id="3020f-136">dst must be a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="3020f-137">DST kann eine Schreib Maske akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="3020f-137">dst can accept a write mask.</span></span> <span data-ttu-id="3020f-138">Siehe [Ziel Register Maskierung](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md).</span><span class="sxs-lookup"><span data-stu-id="3020f-138">See [Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md).</span></span>
-   <span data-ttu-id="3020f-139">Die Standardwerte für fehlende Komponenten sind entweder 0 oder 1 und hängen vom Textur Format ab.</span><span class="sxs-lookup"><span data-stu-id="3020f-139">Defaults for missing components are either 0 or 1, and depend on the texture format.</span></span>
-   <span data-ttu-id="3020f-140">Quelle1 muss ein [Sampler (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) sein \# .</span><span class="sxs-lookup"><span data-stu-id="3020f-140">src1 must be a [Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s\#).</span></span> <span data-ttu-id="3020f-141">Quelle1 darf keinen Negation-Modifizierer verwenden.</span><span class="sxs-lookup"><span data-stu-id="3020f-141">src1 may not use a negate modifier.</span></span> <span data-ttu-id="3020f-142">Quelle1 verwendet möglicherweise Swizzle, das nach der Stichprobenentnahme angewendet wird, bevor die Schreib Maske berücksichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="3020f-142">src1 may use swizzle, which is applied after sampling before the write mask is honored.</span></span> <span data-ttu-id="3020f-143">Der Sampler muss am Anfang des Shader (mit [DCL \_ -samplertype (SM3-vs ASM)](dcl-samplertype---vs.md)) deklariert worden sein.</span><span class="sxs-lookup"><span data-stu-id="3020f-143">The sampler must have been declared (using [dcl\_samplerType (sm3 - vs asm)](dcl-samplertype---vs.md)) at the beginning of the shader.</span></span>
-   <span data-ttu-id="3020f-144">Die Anzahl der Koordinaten, die zum Ausführen des Textur Beispiels erforderlich sind, hängt davon ab, wie der Sampler deklariert wurde.</span><span class="sxs-lookup"><span data-stu-id="3020f-144">The number of coordinates required to perform the texture sample depends on how the sampler was declared.</span></span> <span data-ttu-id="3020f-145">Wenn Sie als Cube deklariert wurde, ist eine Textur Koordinate mit drei Komponenten erforderlich (. RGB).</span><span class="sxs-lookup"><span data-stu-id="3020f-145">If it was declared as a cube, a three-component texture coordinate is required (.rgb).</span></span> <span data-ttu-id="3020f-146">Die Validierung erzwingt, dass die für texldl bereitgestellten Koordinaten für die für den Sampler deklarierte Textur Dimension ausreichend sind.</span><span class="sxs-lookup"><span data-stu-id="3020f-146">Validation enforces that coordinates provided to texldl Are sufficient for the texture dimension declared for the sampler.</span></span> <span data-ttu-id="3020f-147">Es ist jedoch nicht garantiert, dass die Anwendung tatsächlich eine Textur (über die API) mit Dimensionen festgelegt, die der für den Sampler deklarierten Dimension entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3020f-147">However, it is not guaranteed that the application actually set a texture (through the API) with dimensions equal to the dimension declared for the sampler.</span></span> <span data-ttu-id="3020f-148">In einem solchen Fall versucht die Laufzeit, Konflikte zu erkennen (möglicherweise nur im Debugmodus).</span><span class="sxs-lookup"><span data-stu-id="3020f-148">In such a case, the runtime will attempt to detect mismatches (possibly in debug only).</span></span> <span data-ttu-id="3020f-149">Das Sampling einer Textur mit weniger Dimensionen als in der Textur Koordinate vorhanden ist zulässig, und es wird davon ausgegangen, dass die zusätzlichen Texturkoordinaten Komponenten ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="3020f-149">Sampling a texture with fewer dimensions than are present in the texture coordinate will be allowed, and will be assumed to ignore the extra texture coordinate components.</span></span> <span data-ttu-id="3020f-150">Umgekehrt ist das Sampling einer Textur mit mehr Dimensionen als in der Textur Koordinate nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="3020f-150">Conversely, sampling a texture with more dimensions than are present in the texture coordinate is not allowed.</span></span>
-   <span data-ttu-id="3020f-151">Wenn src0 (Textur Koordinate) ein [temporäres Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ) ist, müssen die für die Suche (oben beschriebenen) erforderlichen Komponenten bereits geschrieben worden sein.</span><span class="sxs-lookup"><span data-stu-id="3020f-151">If the src0 (texture coordinate) is a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#), the components required for the lookup (described above) must have been previously written.</span></span>
-   <span data-ttu-id="3020f-152">Die Stichprobenentnahme nicht signierter RGB-Texturen führt zu float-Werten zwischen 0,0 und 1,0.</span><span class="sxs-lookup"><span data-stu-id="3020f-152">Sampling unsigned RGB textures will result in float values between 0.0 and 1.0.</span></span>
-   <span data-ttu-id="3020f-153">Die Stichproben signierter Texturen führen zu float-Werten zwischen-1,0 und 1,0.</span><span class="sxs-lookup"><span data-stu-id="3020f-153">Sampling signed textures will result in float values between -1.0 to 1.0.</span></span>
-   <span data-ttu-id="3020f-154">Beim Sampling von Gleit Komma Texturen bedeutet Float16, dass die Daten innerhalb von Max \_ . Float16 liegen.</span><span class="sxs-lookup"><span data-stu-id="3020f-154">When sampling floating point textures, Float16 means that the data will range within MAX\_FLOAT16.</span></span> <span data-ttu-id="3020f-155">Float32 bedeutet, dass der maximale Bereich der Pipeline verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3020f-155">Float32 means the maximum range of the pipeline will be used.</span></span> <span data-ttu-id="3020f-156">Die Stichprobenentnahme außerhalb eines Bereichs ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="3020f-156">Sampling outside of either range is undefined.</span></span>
-   <span data-ttu-id="3020f-157">Es gibt keine abhängige Lese Beschränkung.</span><span class="sxs-lookup"><span data-stu-id="3020f-157">There is no dependent read limit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3020f-158">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3020f-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3020f-159">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="3020f-159">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
