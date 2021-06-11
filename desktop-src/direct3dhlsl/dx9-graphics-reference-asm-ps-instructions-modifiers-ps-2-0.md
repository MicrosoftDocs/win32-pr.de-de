---
title: Modifizierer für ps_2_0 und höher
description: Anweisungsmodifizierer beeinflussen das Ergebnis der Anweisung, bevor sie in das Zielregister geschrieben wird. Erfahren Sie mehr über Modifizierer für ps_2_0 und höher.
ms.assetid: eb2a8a1f-51bc-4516-b679-a8fb25b0dda0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc8ed91f8e103ebbab7c43ffe53201f0e1d5dfcf
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989285"
---
# <a name="modifiers-for-ps_2_0-and-above"></a><span data-ttu-id="908b2-104">Modifizierer für ps \_ 2 \_ 0 und höher</span><span class="sxs-lookup"><span data-stu-id="908b2-104">Modifiers for ps\_2\_0 and Above</span></span>

<span data-ttu-id="908b2-105">Anweisungsmodifizierer beeinflussen das Ergebnis der Anweisung, bevor sie in das Zielregister geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="908b2-105">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span>

<span data-ttu-id="908b2-106">Dieser Abschnitt enthält Referenzinformationen zu den Anweisungsmodifizierern, die von Version 2 0 und höher des Pixelshader implementiert \_ werden.</span><span class="sxs-lookup"><span data-stu-id="908b2-106">This section contains reference information for the instruction modifiers implemented by pixel shader version 2\_0 and above.</span></span>



| <span data-ttu-id="908b2-107">Name</span><span class="sxs-lookup"><span data-stu-id="908b2-107">Name</span></span>                                     | <span data-ttu-id="908b2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="908b2-108">Syntax</span></span>     | <span data-ttu-id="908b2-109">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="908b2-109">2\_0</span></span> | <span data-ttu-id="908b2-110">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="908b2-110">2\_x</span></span> | <span data-ttu-id="908b2-111">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="908b2-111">2\_sw</span></span> | <span data-ttu-id="908b2-112">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="908b2-112">3\_0</span></span> | <span data-ttu-id="908b2-113">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="908b2-113">3\_sw</span></span> |
|------------------------------------------|------------|------|------|-------|------|-------|
| [<span data-ttu-id="908b2-114">Schwerpunkt</span><span class="sxs-lookup"><span data-stu-id="908b2-114">Centroid</span></span>](#centroid)                    | <span data-ttu-id="908b2-115">\_Schwerpunkt</span><span class="sxs-lookup"><span data-stu-id="908b2-115">\_centroid</span></span> | <span data-ttu-id="908b2-116">x</span><span class="sxs-lookup"><span data-stu-id="908b2-116">x</span></span>    | <span data-ttu-id="908b2-117">x</span><span class="sxs-lookup"><span data-stu-id="908b2-117">x</span></span>    | <span data-ttu-id="908b2-118">x</span><span class="sxs-lookup"><span data-stu-id="908b2-118">x</span></span>     | <span data-ttu-id="908b2-119">x</span><span class="sxs-lookup"><span data-stu-id="908b2-119">x</span></span>    | <span data-ttu-id="908b2-120">x</span><span class="sxs-lookup"><span data-stu-id="908b2-120">x</span></span>     |
| [<span data-ttu-id="908b2-121">Partielle \_ Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="908b2-121">Partial\_Precision</span></span>](#partial-precision) | <span data-ttu-id="908b2-122">\_Pp</span><span class="sxs-lookup"><span data-stu-id="908b2-122">\_pp</span></span>       | <span data-ttu-id="908b2-123">x</span><span class="sxs-lookup"><span data-stu-id="908b2-123">x</span></span>    | <span data-ttu-id="908b2-124">x</span><span class="sxs-lookup"><span data-stu-id="908b2-124">x</span></span>    | <span data-ttu-id="908b2-125">x</span><span class="sxs-lookup"><span data-stu-id="908b2-125">x</span></span>     | <span data-ttu-id="908b2-126">x</span><span class="sxs-lookup"><span data-stu-id="908b2-126">x</span></span>    | <span data-ttu-id="908b2-127">x</span><span class="sxs-lookup"><span data-stu-id="908b2-127">x</span></span>     |
| [<span data-ttu-id="908b2-128">Sättigen</span><span class="sxs-lookup"><span data-stu-id="908b2-128">Saturate</span></span>](#saturate)                    | <span data-ttu-id="908b2-129">\_sat</span><span class="sxs-lookup"><span data-stu-id="908b2-129">\_sat</span></span>      | <span data-ttu-id="908b2-130">x</span><span class="sxs-lookup"><span data-stu-id="908b2-130">x</span></span>    | <span data-ttu-id="908b2-131">x</span><span class="sxs-lookup"><span data-stu-id="908b2-131">x</span></span>    | <span data-ttu-id="908b2-132">x</span><span class="sxs-lookup"><span data-stu-id="908b2-132">x</span></span>     | <span data-ttu-id="908b2-133">x</span><span class="sxs-lookup"><span data-stu-id="908b2-133">x</span></span>    | <span data-ttu-id="908b2-134">x</span><span class="sxs-lookup"><span data-stu-id="908b2-134">x</span></span>     |



 

## <a name="centroid"></a><span data-ttu-id="908b2-135">Schwerpunkt</span><span class="sxs-lookup"><span data-stu-id="908b2-135">Centroid</span></span>

<span data-ttu-id="908b2-136">Der Schwerpunktmodifizierer ist ein optionaler Modifizierer, der die Attributinterpolation innerhalb des Bereichs des Primitiven einbindet, wenn ein Multisample-Pixelmittelpunkt nicht vom Primitiven abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="908b2-136">The centroid modifier is an optional modifier that clamps attribute interpolation within the range of the primitive when a multisample pixel center is not covered by the primitive.</span></span> <span data-ttu-id="908b2-137">Dies ist unter [Schwerpunktstichproben zu](https://msdn.microsoft.com/library/ee415231(VS.85).aspx)sehen.</span><span class="sxs-lookup"><span data-stu-id="908b2-137">This can be seen in [Centroid Sampling](https://msdn.microsoft.com/library/ee415231(VS.85).aspx).</span></span>

<span data-ttu-id="908b2-138">Sie können den Schwerpunktmodifizierer wie hier gezeigt auf eine Assemblyanweisung anwenden:</span><span class="sxs-lookup"><span data-stu-id="908b2-138">You can apply the centroid modifier to an assembly instruction as shown here:</span></span>


```
dcl_texcoord0_centroid v0
```



<span data-ttu-id="908b2-139">Sie können den Schwerpunktmodifizierer auch auf eine Semantik anwenden, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="908b2-139">You can also apply the centroid modifier to a semantic as shown here:</span></span>


```
float4 TexturePointCentroidPS( float4 TexCoord : TEXCOORD0_centroid ) : COLOR0
{
    return tex2D( PointSampler, TexCoord );
}
```



<span data-ttu-id="908b2-140">Darüber hinaus wird für jedes [Eingabefarbregister](dx9-graphics-reference-asm-ps-registers-input-color.md) (v ), das \# mit einer Farbsemantik deklariert wird, automatisch ein Schwerpunkt angewendet.</span><span class="sxs-lookup"><span data-stu-id="908b2-140">In addition, any [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) declared with a color semantic will automatically have centroid applied.</span></span> <span data-ttu-id="908b2-141">Farbverläufe, die aus Attributen berechnet werden, für die Schwerpunktstichproben erstellt werden, sind nicht garantiert genau.</span><span class="sxs-lookup"><span data-stu-id="908b2-141">Gradients computed from attributes that are centroid sampled are not guaranteed to be accurate.</span></span>

## <a name="partial-precision"></a><span data-ttu-id="908b2-142">Partielle Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="908b2-142">Partial Precision</span></span>

<span data-ttu-id="908b2-143">Der Anweisungsmodifizierer für partielle Genauigkeit ( \_ pp) gibt Bereiche an, in denen partielle Genauigkeit akzeptabel ist, vorausgesetzt, die zugrunde liegende Implementierung unterstützt dies.</span><span class="sxs-lookup"><span data-stu-id="908b2-143">The partial precision instruction modifier (\_pp) indicates areas where partial precision is acceptable, provided that the underlying implementation supports it.</span></span> <span data-ttu-id="908b2-144">Implementierungen können den Modifizierer immer ignorieren und die betroffenen Vorgänge mit voller Genauigkeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="908b2-144">Implementations are always free to ignore the modifier and perform the affected operations in full precision.</span></span>

<span data-ttu-id="908b2-145">Der \_ pp-Modifizierer kann in zwei Kontexten auftreten:</span><span class="sxs-lookup"><span data-stu-id="908b2-145">The \_pp modifier can occur in two contexts:</span></span>

-   <span data-ttu-id="908b2-146">In einer Texturkoordinatendeklaration, um die Übergabe von Texturkoordinaten an den Pixelshader in Form von teilweiser Genauigkeit zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="908b2-146">On a texture coordinate declaration to enable passing texture coordinates to the pixel shader in partial-precision form.</span></span> <span data-ttu-id="908b2-147">Dies ermöglicht beispielsweise die Verwendung von Texturkoordinaten, um Farbdaten an den Pixelshader weiterzuleiten, was in einigen Implementierungen mit teilweiser Genauigkeit schneller als mit vollständiger Genauigkeit sein kann.</span><span class="sxs-lookup"><span data-stu-id="908b2-147">This allows, for example, the use of texture coordinates to relay color data to the pixel shader, which may be faster with partial precision than with full precision in some implementations.</span></span> <span data-ttu-id="908b2-148">Wenn dieser Modifizierer nicht vorhanden ist, müssen Texturkoordinaten mit voller Genauigkeit übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="908b2-148">In the absence of this modifier, texture coordinates must be passed in full precision.</span></span>
-   <span data-ttu-id="908b2-149">Für jede Anweisung, einschließlich Anweisungen zum Laden von Texturen.</span><span class="sxs-lookup"><span data-stu-id="908b2-149">On any instruction including texture load instructions.</span></span> <span data-ttu-id="908b2-150">Dies gibt an, dass die Implementierung die Anweisung mit teilweiser Genauigkeit ausführen und ein Ergebnis mit teilweiser Genauigkeit speichern darf.</span><span class="sxs-lookup"><span data-stu-id="908b2-150">This indicates that the implementation is allowed to execute the instruction with partial precision and store a partial precision result.</span></span> <span data-ttu-id="908b2-151">Wenn kein expliziter Modifizierer vorhanden ist, muss die Anweisung mit voller Genauigkeit ausgeführt werden (unabhängig von der Eingabegenauigkeit).</span><span class="sxs-lookup"><span data-stu-id="908b2-151">In the absence of an explicit modifier, the instruction must be performed at full precision (regardless of the input precision).</span></span>

<span data-ttu-id="908b2-152">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="908b2-152">Examples:</span></span>


```
dcl_texcoord0_pp t1
cmp_pp r0, r1, r2, r3
```



## <a name="saturate"></a><span data-ttu-id="908b2-153">Sättigung</span><span class="sxs-lookup"><span data-stu-id="908b2-153">Saturate</span></span>

<span data-ttu-id="908b2-154">Der Saturate-Anweisungsmodifizierer ( \_ sat) sättigt (oder klammscht) das Anweisungsergebnis auf den Bereich \[ 0, 1, \] bevor er in das Zielregister schreibt.</span><span class="sxs-lookup"><span data-stu-id="908b2-154">The saturate instruction modifier (\_sat) saturates (or clamps) the instruction result to the range \[0, 1\] before writing to the destination register.</span></span>

<span data-ttu-id="908b2-155">Der \_ Sat-Anweisungsmodifizierer kann mit jeder Anweisung außer [frc - ps](frc---ps.md), [sincos - ps](sincos---ps.md)und beliebigen Texanweisungen verwendet \* werden.</span><span class="sxs-lookup"><span data-stu-id="908b2-155">The \_sat instruction modifier can be used with any instruction except [frc - ps](frc---ps.md), [sincos - ps](sincos---ps.md), and any tex\* instructions.</span></span>

<span data-ttu-id="908b2-156">Für ps \_ 2 \_ 0, ps \_ 2 \_ x und ps \_ 2 sw kann der \_ \_ Sat-Anweisungsmodifizierer nicht mit Anweisungen verwendet werden, die in Ausgaberegister schreiben ([Ausgabefarbregister](dx9-graphics-reference-asm-ps-registers-output-color.md) oder [Ausgabetieferegister](dx9-graphics-reference-asm-ps-registers-output-depth.md)).</span><span class="sxs-lookup"><span data-stu-id="908b2-156">For ps\_2\_0, ps\_2\_x, and ps\_2\_sw, the \_sat instruction modifier cannot be used with instructions writing to any output registers ([Output Color Register](dx9-graphics-reference-asm-ps-registers-output-color.md) or [Output Depth Register](dx9-graphics-reference-asm-ps-registers-output-depth.md)).</span></span> <span data-ttu-id="908b2-157">Diese Einschränkung gilt nicht für PS \_ 3 \_ 0 und höher.</span><span class="sxs-lookup"><span data-stu-id="908b2-157">This restriction does not apply to ps\_3\_0 and above.</span></span>

<span data-ttu-id="908b2-158">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="908b2-158">Example:</span></span>


```
dp3_sat r0, v0, c1
```



## <a name="related-topics"></a><span data-ttu-id="908b2-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="908b2-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="908b2-160">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="908b2-160">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




