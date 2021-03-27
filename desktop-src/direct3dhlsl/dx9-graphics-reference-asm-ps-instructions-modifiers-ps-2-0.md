---
title: Modifiziererer für PS_2_0 und höher
description: Anweisungsmodifiziererer wirken sich auf das Ergebnis der Anweisung aus, bevor Sie in das Ziel Register geschrieben wird.
ms.assetid: eb2a8a1f-51bc-4516-b679-a8fb25b0dda0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7141576b80b7a05a3e61ee9a98fa36958b1d5530
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856984"
---
# <a name="modifiers-for-ps_2_0-and-above"></a><span data-ttu-id="7ce29-103">Modifiziererer für PS \_ 2 \_ 0 und höher</span><span class="sxs-lookup"><span data-stu-id="7ce29-103">Modifiers for ps\_2\_0 and Above</span></span>

<span data-ttu-id="7ce29-104">Anweisungsmodifiziererer wirken sich auf das Ergebnis der Anweisung aus, bevor Sie in das Ziel Register geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="7ce29-104">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span>

<span data-ttu-id="7ce29-105">Dieser Abschnitt enthält Referenzinformationen zu den Anweisungs Modifizierern, die von Pixel Shader Version 2 \_ 0 und höher implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="7ce29-105">This section contains reference information for the instruction modifiers implemented by pixel shader version 2\_0 and above.</span></span>



| <span data-ttu-id="7ce29-106">Name</span><span class="sxs-lookup"><span data-stu-id="7ce29-106">Name</span></span>                                     | <span data-ttu-id="7ce29-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ce29-107">Syntax</span></span>     | <span data-ttu-id="7ce29-108">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7ce29-108">2\_0</span></span> | <span data-ttu-id="7ce29-109">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7ce29-109">2\_x</span></span> | <span data-ttu-id="7ce29-110">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7ce29-110">2\_sw</span></span> | <span data-ttu-id="7ce29-111">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7ce29-111">3\_0</span></span> | <span data-ttu-id="7ce29-112">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7ce29-112">3\_sw</span></span> |
|------------------------------------------|------------|------|------|-------|------|-------|
| [<span data-ttu-id="7ce29-113">Schwerpunkt</span><span class="sxs-lookup"><span data-stu-id="7ce29-113">Centroid</span></span>](#centroid)                    | <span data-ttu-id="7ce29-114">\_Schwerpunkt</span><span class="sxs-lookup"><span data-stu-id="7ce29-114">\_centroid</span></span> | <span data-ttu-id="7ce29-115">x</span><span class="sxs-lookup"><span data-stu-id="7ce29-115">x</span></span>    | <span data-ttu-id="7ce29-116">x</span><span class="sxs-lookup"><span data-stu-id="7ce29-116">x</span></span>    | <span data-ttu-id="7ce29-117">x</span><span class="sxs-lookup"><span data-stu-id="7ce29-117">x</span></span>     | <span data-ttu-id="7ce29-118">x</span><span class="sxs-lookup"><span data-stu-id="7ce29-118">x</span></span>    | <span data-ttu-id="7ce29-119">x</span><span class="sxs-lookup"><span data-stu-id="7ce29-119">x</span></span>     |
| [<span data-ttu-id="7ce29-120">Partielle \_ Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="7ce29-120">Partial\_Precision</span></span>](#partial-precision) | <span data-ttu-id="7ce29-121">\_Trupp</span><span class="sxs-lookup"><span data-stu-id="7ce29-121">\_pp</span></span>       | <span data-ttu-id="7ce29-122">x</span><span class="sxs-lookup"><span data-stu-id="7ce29-122">x</span></span>    | <span data-ttu-id="7ce29-123">x</span><span class="sxs-lookup"><span data-stu-id="7ce29-123">x</span></span>    | <span data-ttu-id="7ce29-124">x</span><span class="sxs-lookup"><span data-stu-id="7ce29-124">x</span></span>     | <span data-ttu-id="7ce29-125">x</span><span class="sxs-lookup"><span data-stu-id="7ce29-125">x</span></span>    | <span data-ttu-id="7ce29-126">x</span><span class="sxs-lookup"><span data-stu-id="7ce29-126">x</span></span>     |
| [<span data-ttu-id="7ce29-127">Sättigen</span><span class="sxs-lookup"><span data-stu-id="7ce29-127">Saturate</span></span>](#saturate)                    | <span data-ttu-id="7ce29-128">\_gesetzt</span><span class="sxs-lookup"><span data-stu-id="7ce29-128">\_sat</span></span>      | <span data-ttu-id="7ce29-129">x</span><span class="sxs-lookup"><span data-stu-id="7ce29-129">x</span></span>    | <span data-ttu-id="7ce29-130">x</span><span class="sxs-lookup"><span data-stu-id="7ce29-130">x</span></span>    | <span data-ttu-id="7ce29-131">x</span><span class="sxs-lookup"><span data-stu-id="7ce29-131">x</span></span>     | <span data-ttu-id="7ce29-132">x</span><span class="sxs-lookup"><span data-stu-id="7ce29-132">x</span></span>    | <span data-ttu-id="7ce29-133">x</span><span class="sxs-lookup"><span data-stu-id="7ce29-133">x</span></span>     |



 

## <a name="centroid"></a><span data-ttu-id="7ce29-134">Schwerpunkt</span><span class="sxs-lookup"><span data-stu-id="7ce29-134">Centroid</span></span>

<span data-ttu-id="7ce29-135">Der Schwerpunkt-Modifizierer ist ein optionaler Modifizierer, der die Attribut interpolung innerhalb des Gültigkeits Bereichs des primitiven aufbindet, wenn ein Multisampling-Pixel Center nicht vom primitiven abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="7ce29-135">The centroid modifier is an optional modifier that clamps attribute interpolation within the range of the primitive when a multisample pixel center is not covered by the primitive.</span></span> <span data-ttu-id="7ce29-136">Dies kann in [Centroid-Stichproben](https://msdn.microsoft.com/library/ee415231(VS.85).aspx)angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7ce29-136">This can be seen in [Centroid Sampling](https://msdn.microsoft.com/library/ee415231(VS.85).aspx).</span></span>

<span data-ttu-id="7ce29-137">Sie können den Schwerpunkt-Modifizierer auf eine Assemblyanweisung anwenden, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="7ce29-137">You can apply the centroid modifier to an assembly instruction as shown here:</span></span>


```
dcl_texcoord0_centroid v0
```



<span data-ttu-id="7ce29-138">Sie können auch den Schwerpunkt-Modifizierer auf eine Semantik anwenden, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="7ce29-138">You can also apply the centroid modifier to a semantic as shown here:</span></span>


```
float4 TexturePointCentroidPS( float4 TexCoord : TEXCOORD0_centroid ) : COLOR0
{
    return tex2D( PointSampler, TexCoord );
}
```



<span data-ttu-id="7ce29-139">Darüber hinaus wird für jedes [Eingabe Farb Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v), das \# mit einer Farb Semantik deklariert wurde, der Schwerpunkt automatisch angewendet.</span><span class="sxs-lookup"><span data-stu-id="7ce29-139">In addition, any [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) declared with a color semantic will automatically have centroid applied.</span></span> <span data-ttu-id="7ce29-140">Aus Attributen berechnete Farbverläufe, bei denen es sich um einen Schwerpunkt Wert handelt, sind nicht unbedingt genau.</span><span class="sxs-lookup"><span data-stu-id="7ce29-140">Gradients computed from attributes that are centroid sampled are not guaranteed to be accurate.</span></span>

## <a name="partial-precision"></a><span data-ttu-id="7ce29-141">Partielle Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="7ce29-141">Partial Precision</span></span>

<span data-ttu-id="7ce29-142">Der Anweisungs Modifizierer partielle Genauigkeit \_ gibt Bereiche an, in denen partielle Genauigkeit zulässig ist, vorausgesetzt, dass die zugrunde liegende Implementierung dies unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7ce29-142">The partial precision instruction modifier (\_pp) indicates areas where partial precision is acceptable, provided that the underlying implementation supports it.</span></span> <span data-ttu-id="7ce29-143">Implementierungen können den-Modifizierer jederzeit ignorieren und die betroffenen Vorgänge mit vollständiger Genauigkeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="7ce29-143">Implementations are always free to ignore the modifier and perform the affected operations in full precision.</span></span>

<span data-ttu-id="7ce29-144">Der \_ PP-Modifizierer kann in zwei Kontexten vorkommen:</span><span class="sxs-lookup"><span data-stu-id="7ce29-144">The \_pp modifier can occur in two contexts:</span></span>

-   <span data-ttu-id="7ce29-145">In einer Texturkoordinaten Deklaration, die das Übergeben von Texturkoordinaten an den Pixelshader in Form mit teilweiser Genauigkeit ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="7ce29-145">On a texture coordinate declaration to enable passing texture coordinates to the pixel shader in partial-precision form.</span></span> <span data-ttu-id="7ce29-146">Dies ermöglicht z. b. die Verwendung von Texturkoordinaten, um Farbdaten an den Pixelshader zu übertragen. Dies kann bei einigen Implementierungen mit einer partiellen Genauigkeit schneller erfolgen als mit der vollständigen Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="7ce29-146">This allows, for example, the use of texture coordinates to relay color data to the pixel shader, which may be faster with partial precision than with full precision in some implementations.</span></span> <span data-ttu-id="7ce29-147">Wenn dieser Modifizierer nicht vorhanden ist, müssen die Texturkoordinaten vollständig übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="7ce29-147">In the absence of this modifier, texture coordinates must be passed in full precision.</span></span>
-   <span data-ttu-id="7ce29-148">In jeder Anweisung einschließlich Textur Ladeanweisungen.</span><span class="sxs-lookup"><span data-stu-id="7ce29-148">On any instruction including texture load instructions.</span></span> <span data-ttu-id="7ce29-149">Dies gibt an, dass die Implementierung die Anweisung mit teilweiser Genauigkeit ausführen und ein partielles Genauigkeits Ergebnis speichern darf.</span><span class="sxs-lookup"><span data-stu-id="7ce29-149">This indicates that the implementation is allowed to execute the instruction with partial precision and store a partial precision result.</span></span> <span data-ttu-id="7ce29-150">Wenn kein expliziter Modifizierer vorhanden ist, muss die Anweisung mit vollständiger Genauigkeit (unabhängig von der Eingabe Genauigkeit) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7ce29-150">In the absence of an explicit modifier, the instruction must be performed at full precision (regardless of the input precision).</span></span>

<span data-ttu-id="7ce29-151">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="7ce29-151">Examples:</span></span>


```
dcl_texcoord0_pp t1
cmp_pp r0, r1, r2, r3
```



## <a name="saturate"></a><span data-ttu-id="7ce29-152">Sättigung</span><span class="sxs-lookup"><span data-stu-id="7ce29-152">Saturate</span></span>

<span data-ttu-id="7ce29-153">Der Bezeichner der bearbeitungsanweisungsmodifizierer ( \_ Sat) füllt das Anweisungs Ergebnis \[ vor dem \] Schreiben in das Ziel Register (oder bindet es) bis zum Bereich 0, 1.</span><span class="sxs-lookup"><span data-stu-id="7ce29-153">The saturate instruction modifier (\_sat) saturates (or clamps) the instruction result to the range \[0, 1\] before writing to the destination register.</span></span>

<span data-ttu-id="7ce29-154">Der \_ Sat-Anweisungs Modifizierer kann mit einer beliebigen Anweisung außer [FRC-PS](frc---ps.md), [SinCos-PS](sincos---ps.md)und allen Textanweisungen verwendet werden \* .</span><span class="sxs-lookup"><span data-stu-id="7ce29-154">The \_sat instruction modifier can be used with any instruction except [frc - ps](frc---ps.md), [sincos - ps](sincos---ps.md), and any tex\* instructions.</span></span>

<span data-ttu-id="7ce29-155">Für PS \_ 2 \_ 0, PS \_ 2 \_ x und PS \_ 2 \_ SW \_ kann der Sat-Anweisungs Modifizierer nicht mit Anweisungen verwendet werden, die in Ausgabe Register geschrieben werden ([Ausgabe Farbregister](dx9-graphics-reference-asm-ps-registers-output-color.md) oder [Ausgabe tiefen Register](dx9-graphics-reference-asm-ps-registers-output-depth.md)).</span><span class="sxs-lookup"><span data-stu-id="7ce29-155">For ps\_2\_0, ps\_2\_x, and ps\_2\_sw, the \_sat instruction modifier cannot be used with instructions writing to any output registers ([Output Color Register](dx9-graphics-reference-asm-ps-registers-output-color.md) or [Output Depth Register](dx9-graphics-reference-asm-ps-registers-output-depth.md)).</span></span> <span data-ttu-id="7ce29-156">Diese Einschränkung gilt nicht für PS \_ 3 \_ 0 und höher.</span><span class="sxs-lookup"><span data-stu-id="7ce29-156">This restriction does not apply to ps\_3\_0 and above.</span></span>

<span data-ttu-id="7ce29-157">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7ce29-157">Example:</span></span>


```
dp3_sat r0, v0, c1
```



## <a name="related-topics"></a><span data-ttu-id="7ce29-158">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7ce29-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ce29-159">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="7ce29-159">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




