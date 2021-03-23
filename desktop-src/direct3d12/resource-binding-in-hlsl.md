---
title: Ressourcen Bindung in HLSL
description: In diesem Thema werden einige spezifische Features der Verwendung des HLSL-Shader-Modells 5,1 (High Level Shader Language) mit Direct3D 12 beschrieben.
ms.assetid: 3CD4BDAD-8AE3-4DE0-B3F8-9C9F9E83BBE9
ms.localizationpriority: high
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 01039550f07de57fb7b2f1e815bced02e549c741
ms.sourcegitcommit: 60120d10c957815d79af566c72e5f4bcfaca4025
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/23/2021
ms.locfileid: "104837488"
---
# <a name="resource-binding-in-hlsl"></a><span data-ttu-id="e875c-103">Ressourcen Bindung in HLSL</span><span class="sxs-lookup"><span data-stu-id="e875c-103">Resource binding in HLSL</span></span>

<span data-ttu-id="e875c-104">In diesem Thema werden einige spezifische Features der Verwendung des HLSL- [Shader-Modells 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1) (High Level Shader Language) mit Direct3D 12 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e875c-104">This topic describes some specific features of using High Level Shader Language (HLSL) [Shader Model 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) with Direct3D 12.</span></span> <span data-ttu-id="e875c-105">Alle Direct3D 12-Hardware unterstützt das Shader-Modell 5,1. die Unterstützung für dieses Modell hängt daher nicht von der Hardware Funktionsebene ab.</span><span class="sxs-lookup"><span data-stu-id="e875c-105">All Direct3D 12 hardware supports Shader Model 5.1, so support for this model does not depend on what the hardware feature level is.</span></span>

## <a name="resource-types-and-arrays"></a><span data-ttu-id="e875c-106">Ressourcentypen und Arrays</span><span class="sxs-lookup"><span data-stu-id="e875c-106">Resource types and arrays</span></span>

<span data-ttu-id="e875c-107">Die Ressourcen Syntax von Shader Model 5 (SM 5.0) verwendet das- `register` Schlüsselwort, um wichtige Informationen über die Ressource an den HLSL-Compiler weiterzugeben.</span><span class="sxs-lookup"><span data-stu-id="e875c-107">Shader Model 5 (SM5.0) resource syntax uses the `register` keyword to relay important information about the resource to the HLSL compiler.</span></span> <span data-ttu-id="e875c-108">Die folgende Anweisung deklariert z. b. ein Array aus vier Texturen, die an Slots T3, T4, T5 und T6 gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="e875c-108">For example, the following statement declares an array of four textures bound at slots t3, t4, t5, and t6.</span></span> <span data-ttu-id="e875c-109">T3 ist der einzige in der-Anweisung angezeigte Registrierungs Slot, der einfach der erste im Array von vier ist.</span><span class="sxs-lookup"><span data-stu-id="e875c-109">t3 is the only register slot appearing in the statement, simply being the first in the array of four.</span></span>

``` syntax
Texture2D<float4> tex1[4] : register(t3)
```

<span data-ttu-id="e875c-110">Die Ressourcen Syntax von Shader Model 5,1 (SM 5.1) in HLSL basiert auf der vorhandenen Register Resource-Syntax, um das Portieren zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="e875c-110">Shader Model 5.1 (SM5.1) resource syntax in HLSL is based on existing register resource syntax, to allow easier porting.</span></span> <span data-ttu-id="e875c-111">Direct3D 12-Ressourcen in HLSL sind an virtuelle Register innerhalb logischer Register Plätze gebunden:</span><span class="sxs-lookup"><span data-stu-id="e875c-111">Direct3D 12 resources in HLSL are bound to virtual registers within logical register spaces:</span></span>

-   <span data-ttu-id="e875c-112">t – für Shader-Ressourcen Sichten (SRV)</span><span class="sxs-lookup"><span data-stu-id="e875c-112">t – for shader resource views (SRV)</span></span>
-   <span data-ttu-id="e875c-113">s – für Samplern</span><span class="sxs-lookup"><span data-stu-id="e875c-113">s – for samplers</span></span>
-   <span data-ttu-id="e875c-114">u – für ungeordnete Zugriffs Sichten (UAV)</span><span class="sxs-lookup"><span data-stu-id="e875c-114">u – for unordered access views (UAV)</span></span>
-   <span data-ttu-id="e875c-115">b – für konstantenpuffersichten (CBV)</span><span class="sxs-lookup"><span data-stu-id="e875c-115">b – for constant buffer views (CBV)</span></span>

<span data-ttu-id="e875c-116">Die Stamm Signatur, die auf den Shader verweist, muss mit den deklarierten Register Slots kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="e875c-116">The root signature referencing the shader must be compatible with the declared register slots.</span></span> <span data-ttu-id="e875c-117">Der folgende Teil einer Stamm Signatur ist beispielsweise mit der Verwendung von Textur Slots T3 bis T6 kompatibel, da er eine Deskriptortabelle mit Slots t0 bis T98 beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e875c-117">For example, the following portion of a root signature would be compatible with the use of texture slots t3 through t6, as it describes a descriptor table with slots t0 through t98.</span></span>

``` syntax
DescriptorTable( CBV(b1), SRV(t0,numDescriptors=99), CBV(b2) )
```

<span data-ttu-id="e875c-118">Eine Ressourcen Deklaration kann ein Skalar, ein 1D-Array oder ein mehrdimensionales Array sein:</span><span class="sxs-lookup"><span data-stu-id="e875c-118">A resource declaration may be a scalar, a 1D array, or a multidimensional array:</span></span>

``` syntax
Texture2D<float4> tex1 : register(t3,  space0)
Texture2D<float4> tex2[4] : register(t10)
Texture2D<float4> tex3[7][5][3] : register(t20, space1)
```

<span data-ttu-id="e875c-119">SM 5.1 verwendet dieselben Ressourcentypen und Elementtypen wie SM 5.0.</span><span class="sxs-lookup"><span data-stu-id="e875c-119">SM5.1 uses the same resource types and element types as SM5.0 does.</span></span> <span data-ttu-id="e875c-120">Die SM 5.1-Deklarations Limits sind flexibler und werden nur durch die Lauf Zeit-/Hardwarelimits eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="e875c-120">SM5.1 declaration limits are more flexible, and constrained only by the runtime/hardware limits.</span></span> <span data-ttu-id="e875c-121">Das `space` Schlüsselwort gibt an, an welchen logischen Register Bereich die deklarierte Variable gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="e875c-121">The `space` keyword specifies to which logical register space the declared variable is bound.</span></span> <span data-ttu-id="e875c-122">Wenn das `space` Schlüsselwort weggelassen wird, wird der standardmäßige Speicherplatz Index 0 implizit dem Bereich zugewiesen (sodass sich der `tex2` obige Bereich in befindet `space0` ).</span><span class="sxs-lookup"><span data-stu-id="e875c-122">If the `space` keyword is omitted, then the default space index of 0 is implicitly assigned to the range (so the `tex2` range above resides in `space0`).</span></span> <span data-ttu-id="e875c-123">`register(t3,  space0)` führt niemals zu einem Konflikt mit `register(t3,  space1)` und mit einem Array in einem anderen Bereich, das T3 enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="e875c-123">`register(t3,  space0)` will never conflict with `register(t3,  space1)`, nor with any array in another space that might include t3.</span></span>

<span data-ttu-id="e875c-124">Eine Array Ressource kann eine unbegrenzte Größe aufweisen, die durch Angabe der ersten zu lefenden Dimension deklariert wird, oder 0:</span><span class="sxs-lookup"><span data-stu-id="e875c-124">An array resource may have an unbounded size, which is declared by specifying the very first dimension to be empty, or 0:</span></span>

``` syntax
Texture2D<float4> tex1[] : register(t0)
```

<span data-ttu-id="e875c-125">Die entsprechende Deskriptortabelle könnte wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="e875c-125">The matching descriptor table could be:</span></span>

``` syntax
DescriptorTable( CBV(b1), UAV(u0, numDescriptors = 4), SRV(t0, numDescriptors=unbounded)
```

<span data-ttu-id="e875c-126">Ein ungebundenes Array in HLSL entspricht einer festgelegten Anzahl von `numDescriptors` in der Deskriptortabelle, und eine festgelegte Größe im HLSL entspricht einer ungebundenen Deklaration in der Deskriptortabelle.</span><span class="sxs-lookup"><span data-stu-id="e875c-126">An unbounded array in HLSL does match a fixed number set with `numDescriptors` in the descriptor table, and a fixed size in the HLSL does match an unbounded declaration in the descriptor table.</span></span>

<span data-ttu-id="e875c-127">Mehrdimensionale Arrays, einschließlich einer unbegrenzten Größe, sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="e875c-127">Multi-dimensional arrays are allowed, including of an unbounded size.</span></span> <span data-ttu-id="e875c-128">Diese mehrdimensionalen Arrays werden im Register Bereich reduziert.</span><span class="sxs-lookup"><span data-stu-id="e875c-128">These multidimensional arrays are flattened out in register space.</span></span>

``` syntax
Texture2D<float4> tex2[3000][10] : register(t0, space0); // t0-t29999 in space0
Texture2D<float4> tex3[0][5][3] : register(t5, space1)
```

<span data-ttu-id="e875c-129">Das Aliasing von Ressourcen Bereichen ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="e875c-129">Aliasing of resource ranges is not allowed.</span></span> <span data-ttu-id="e875c-130">Mit anderen Worten: für jeden Ressourcentyp (t, s, u, b) dürfen sich deklarierte Register Bereiche nicht überlappen.</span><span class="sxs-lookup"><span data-stu-id="e875c-130">In other words, for each resource type (t, s, u, b), declared register ranges mustn't overlap.</span></span> <span data-ttu-id="e875c-131">Dies schließt auch unbegrenzte Bereiche ein.</span><span class="sxs-lookup"><span data-stu-id="e875c-131">That includes unbounded ranges, too.</span></span> <span data-ttu-id="e875c-132">Bereiche, die in verschiedenen Register Bereichen deklariert werden, überlappen sich niemals</span><span class="sxs-lookup"><span data-stu-id="e875c-132">Ranges declared in different register spaces never overlap.</span></span> <span data-ttu-id="e875c-133">Beachten Sie, dass `tex2` sich die unbegrenzte (oben) in befindet `space0` , während sich die unbegrenzte Grenze `tex3` in befindet `space1` , sodass Sie sich nicht überlappen.</span><span class="sxs-lookup"><span data-stu-id="e875c-133">Note that unbounded `tex2` (above) resides in `space0`, while unbounded `tex3` resides in `space1`, such that they don't overlap.</span></span>

<span data-ttu-id="e875c-134">Der Zugriff auf Ressourcen, die als Arrays deklariert wurden, ist so einfach wie die Indizierung.</span><span class="sxs-lookup"><span data-stu-id="e875c-134">Accessing resources that have been declared as arrays is as simple as indexing them.</span></span>

``` syntax
Texture2D<float4> tex1[400] : register(t3);
sampler samp[7] : register(s0);
tex1[myMaterialID].Sample(samp[samplerID], texCoords);
```

<span data-ttu-id="e875c-135">Es gibt eine wichtige Standard Beschränkung für die Verwendung der Indizes ( `myMaterialID` und `samplerID` im obigen Code) darin, dass Sie innerhalb einer [Welle](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology)nicht variieren dürfen.</span><span class="sxs-lookup"><span data-stu-id="e875c-135">There's an important default restriction on the use of the indices (`myMaterialID` and `samplerID` in the code above) in that they're not allowed to vary within a [wave](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology).</span></span> <span data-ttu-id="e875c-136">Sogar das Ändern des Indexes auf der Grundlage der instanziierungsanzahl als unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="e875c-136">Even changing the index based on instancing counts as varying.</span></span>

<span data-ttu-id="e875c-137">Wenn Sie den Index variieren müssen, geben Sie den `NonUniformResourceIndex` Qualifizierer für den Index an, z. b.:</span><span class="sxs-lookup"><span data-stu-id="e875c-137">If varying the index is required then specify the `NonUniformResourceIndex` qualifier on the index, for example:</span></span>

``` syntax
tex1[NonUniformResourceIndex(myMaterialID)].Sample(samp[NonUniformResourceIndex(samplerID)], texCoords);
```

<span data-ttu-id="e875c-138">Bei bestimmter Hardware generiert die Verwendung dieses Qualifizierers zusätzlichen Code, um die Richtigkeit (auch Thread übergreifend) zu erzwingen, jedoch geringfügige Leistungseinbußen.</span><span class="sxs-lookup"><span data-stu-id="e875c-138">On some hardware the use of this qualifier generates additional code to enforce correctness (including across threads) but at a minor performance cost.</span></span> <span data-ttu-id="e875c-139">Wenn ein Index ohne diesen Qualifizierer geändert wird und innerhalb eines zeichnen/dispatchvorgangs die Ergebnisse nicht definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e875c-139">If an index is changed without this qualifier and within a draw/dispatch the results are undefined.</span></span>

## <a name="descriptor-arrays-and-texture-arrays"></a><span data-ttu-id="e875c-140">Deskriptorarrays und Textur Arrays</span><span class="sxs-lookup"><span data-stu-id="e875c-140">Descriptor arrays and texture arrays</span></span>

<span data-ttu-id="e875c-141">Textur Arrays sind seit DirectX 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e875c-141">Texture arrays have been available since DirectX 10.</span></span> <span data-ttu-id="e875c-142">Textur Arrays erfordern einen Deskriptor, aber alle Array Slices müssen das gleiche Format, Breite, Höhe und MIP-Anzahl aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e875c-142">Texture arrays require one descriptor, however all the array slices must share the same format, width, height and mip count.</span></span> <span data-ttu-id="e875c-143">Außerdem muss das Array einen zusammenhängenden Bereich im virtuellen Adressraum belegen.</span><span class="sxs-lookup"><span data-stu-id="e875c-143">Also, the array must occupy a contiguous range in virtual address space.</span></span> <span data-ttu-id="e875c-144">Der folgende Code zeigt ein Beispiel für den Zugriff auf ein Textur Array aus einem Shader.</span><span class="sxs-lookup"><span data-stu-id="e875c-144">The following code shows an example of accessing a texture array from a shader.</span></span>

``` syntax
Texture2DArray<float4> myTex2DArray : register(t0); // t0
float3 myCoord(1.0f,1.4f,2.2f); // 2.2f is array index (rounded to int)
color = myTex2DArray.Sample(mySampler, myCoord);
```

<span data-ttu-id="e875c-145">In einem Textur Array kann der Index frei variieren, ohne dass Qualifizierer wie z. b `NonUniformResourceIndex` . erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e875c-145">In a texture array, the index can be varied freely, without any need for qualifiers such as `NonUniformResourceIndex`.</span></span>

<span data-ttu-id="e875c-146">Das entsprechende deskriptorarray wäre wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e875c-146">The equivalent descriptor array would be:</span></span>

``` syntax
Texture2D<float4> myArrayOfTex2D[] : register(t0); // t0+
float2 myCoord(1.0f, 1.4f);
color = myArrayOfTex2D[2].Sample(mySampler,myCoord); // 2 is index
```

<span data-ttu-id="e875c-147">Beachten Sie, dass die umständliche Verwendung eines float-Arrays für den Array Index durch ersetzt wird `myArrayOfTex2D[2]` .</span><span class="sxs-lookup"><span data-stu-id="e875c-147">Note the awkward use of a float for the array index is replaced with `myArrayOfTex2D[2]`.</span></span> <span data-ttu-id="e875c-148">Außerdem bieten deskriptorarrays mehr Flexibilität in Bezug auf die Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="e875c-148">Also descriptor arrays offer more flexibility with the dimensions.</span></span> <span data-ttu-id="e875c-149">Der-Typ, `Texture2D` ist dieses Beispiel, kann nicht variieren, aber das Format, die Breite, die Höhe und die MIP-Anzahl können bei jedem Deskriptor variieren.</span><span class="sxs-lookup"><span data-stu-id="e875c-149">The type, `Texture2D` is this example, cannot vary, but the format, width, height, and mip count can all vary with each descriptor.</span></span>

<span data-ttu-id="e875c-150">Es ist legitim, ein deskriptorarray von Textur Arrays zu haben:</span><span class="sxs-lookup"><span data-stu-id="e875c-150">It is legitimate to have a descriptor array of texture arrays:</span></span>

``` syntax
Texture2DArray<float4> myArrayOfTex2DArrays[2] : register(t0);
```

<span data-ttu-id="e875c-151">Es ist nicht legitim, ein Array von Strukturen zu deklarieren, jede Struktur mit Deskriptoren, z. b. der folgende Code wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e875c-151">It is not legitimate to declare an array of structures, each structure containing descriptors, for example the following code is not supported.</span></span>

``` syntax
struct myStruct {
    Texture2D                    a; 
    Texture2D                    b;
    ConstantBuffer<myConstants>  c;
};
myStruct foo[10000] : register(....);
```

<span data-ttu-id="e875c-152">Dies hätte das Speicher Layout **abcab.**.., aber eine sprach Einschränkung und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e875c-152">This would have allowed the memory layout **abcabcabc....**, but is a language limitation and is not supported.</span></span> <span data-ttu-id="e875c-153">Eine unterstützte Methode hierfür wäre wie folgt, obwohl das Speicher Layout in diesem Fall **AAA ist... BBB... CCC...**</span><span class="sxs-lookup"><span data-stu-id="e875c-153">One supported method of doing this would be as follows, though the memory layout in this case is **aaa...bbb...ccc...**.</span></span>

``` syntax
Texture2D                     a[10000] : register(t0);
Texture2D                     b[10000] : register(t10000);
ConstantBuffer<myConstants>   c[10000] : register(b0);
```

<span data-ttu-id="e875c-154">Um das Layout " **abcabcabc....** Memory" zu erreichen, verwenden Sie eine Deskriptortabelle, ohne die-Struktur zu verwenden `myStruct` .</span><span class="sxs-lookup"><span data-stu-id="e875c-154">To achieve the **abcabcabc....** memory layout, use a descriptor table without use of the `myStruct` structure.</span></span>

## <a name="resource-aliasing"></a><span data-ttu-id="e875c-155">Ressourcen Aliasing</span><span class="sxs-lookup"><span data-stu-id="e875c-155">Resource aliasing</span></span>

<span data-ttu-id="e875c-156">Die in den HLSL-Shadern angegebenen Ressourcen Bereiche sind logische Bereiche.</span><span class="sxs-lookup"><span data-stu-id="e875c-156">The resource ranges specified in the HLSL shaders are logical ranges.</span></span> <span data-ttu-id="e875c-157">Sie werden zur Laufzeit über den Stamm Signatur Mechanismus an konkrete Heap Bereiche gebunden.</span><span class="sxs-lookup"><span data-stu-id="e875c-157">They are be bound to concrete heap ranges at runtime via the root signature mechanism.</span></span> <span data-ttu-id="e875c-158">Normalerweise wird ein logischer Bereich einem Heap Bereich zugeordnet, der sich nicht mit anderen Heap Bereichen überlappt.</span><span class="sxs-lookup"><span data-stu-id="e875c-158">Normally, a logical range maps to a heap range that does not overlap with other heap ranges.</span></span> <span data-ttu-id="e875c-159">Der root Signature-Mechanismus ermöglicht jedoch das Alias (Überlappung) von Heap Bereichen kompatibler Typen.</span><span class="sxs-lookup"><span data-stu-id="e875c-159">However, the root signature mechanism makes it possible to alias (overlap) heap ranges of compatible types.</span></span> <span data-ttu-id="e875c-160">Beispielsweise `tex2` können und `tex3` Bereiche aus dem obigen Beispiel dem gleichen (oder überlappenden) Heap Bereich zugeordnet werden, der die Auswirkungen von Aliasing Texturen im HLSL-Programm hat.</span><span class="sxs-lookup"><span data-stu-id="e875c-160">For example, `tex2` and `tex3` ranges from the above example may be mapped to the same (or overlapping) heap range, which has the effect of aliasing textures in the HLSL program.</span></span> <span data-ttu-id="e875c-161">Wenn ein solches Alias gewünscht ist, muss der Shader mit der Option d3d10 \_ Shader \_ Resources \_ \_ Alias Alias kompiliert werden, die mithilfe der Option */Res \_ May \_ Alias* für das [Effekt-Compilertool](/windows/win32/direct3dtools/fxc) (FXC) festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e875c-161">If such aliasing is desired, the shader must be compiled with D3D10\_SHADER\_RESOURCES\_MAY\_ALIAS option, which is set by using the */res\_may\_alias* option for the [Effect-Compiler Tool](/windows/win32/direct3dtools/fxc) (FXC).</span></span> <span data-ttu-id="e875c-162">Die-Option bewirkt, dass der Compiler korrekten Code erzeugt, indem bestimmte Lade-/Speicheroptimierungen unter der Annahme vermieden werden, dass Ressourcen Alias sein dürfen.</span><span class="sxs-lookup"><span data-stu-id="e875c-162">The option makes the compiler produce correct code by preventing certain load/store optimizations under the assumption that resources may alias.</span></span>

## <a name="divergence-and-derivatives"></a><span data-ttu-id="e875c-163">Abweichung und Ableitungen</span><span class="sxs-lookup"><span data-stu-id="e875c-163">Divergence and derivatives</span></span>

<span data-ttu-id="e875c-164">SM 5.1 weist keine Einschränkungen für den Ressourcen Index auf. Das heißt, ` tex2[idx].Sample(…)` – der Index IDX kann eine Literalkonstante, eine cBuffer-Konstante oder ein interinterpolated-Wert sein.</span><span class="sxs-lookup"><span data-stu-id="e875c-164">SM5.1 does not impose limitations on the resource index; i.e.,` tex2[idx].Sample(…)` – the index idx can be a literal constant, a cbuffer constant, or an interpolated value.</span></span> <span data-ttu-id="e875c-165">Obwohl das Programmiermodell eine sehr hohe Flexibilität bietet, müssen Probleme beachtet werden:</span><span class="sxs-lookup"><span data-stu-id="e875c-165">While the programming model provides such great flexibility, there are issues to be aware of:</span></span>

-   <span data-ttu-id="e875c-166">Wenn der Index über ein vierfache abweicht, sind die von der Hardware berechnete Ableitung und abgeleiteten Mengen wie Lod möglicherweise nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="e875c-166">If index diverges across a quad, the hardware-computed derivative and derived quantities such as LOD may be undefined.</span></span> <span data-ttu-id="e875c-167">Der HLSL-Compiler unternimmt den besten Aufwand, in diesem Fall eine Warnung auszugeben, verhindert jedoch nicht, dass ein Shader kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="e875c-167">The HLSL compiler makes the best effort to issue a warning in this case, but will not prevent a shader from compiling.</span></span> <span data-ttu-id="e875c-168">Dieses Verhalten ähnelt dem Berechnen von Ableitungen in einer abweichenden Ablauf Steuerung.</span><span class="sxs-lookup"><span data-stu-id="e875c-168">This behavior is similar to computing derivatives in divergent control flow.</span></span>
-   <span data-ttu-id="e875c-169">Wenn der Ressourcen Index abweicht, wird die Leistung im Vergleich zur Groß-/Kleinschreibung eines einheitlichen Indexes verringert, da die Hardware Vorgänge für mehrere Ressourcen ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="e875c-169">If the resource index is divergent, the performance is diminished compared to the case of a uniform index, because the hardware needs to perform operations on several resources.</span></span> <span data-ttu-id="e875c-170">Ressourcen Indizes, die abweichen können, müssen mit der- `NonUniformResourceIndex` Funktion im HLSL-Code gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="e875c-170">Resource indexes that may be divergent must be marked with the `NonUniformResourceIndex` function in HLSL code.</span></span> <span data-ttu-id="e875c-171">Andernfalls sind die Ergebnisse nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="e875c-171">Otherwise results are undefined.</span></span>

## <a name="uavs-in-pixel-shaders"></a><span data-ttu-id="e875c-172">UAVs in Pixel-Shadern</span><span class="sxs-lookup"><span data-stu-id="e875c-172">UAVs in pixel shaders</span></span>

<span data-ttu-id="e875c-173">SM 5.1 erzwingt keine Einschränkungen für UAV-Bereiche in Pixel-Shadern, wie es bei SM 5.0 der Fall war.</span><span class="sxs-lookup"><span data-stu-id="e875c-173">SM5.1 does not impose constraints on UAV ranges in pixel shaders as was the case for SM5.0.</span></span>

## <a name="constant-buffers"></a><span data-ttu-id="e875c-174">Konstantenpuffer</span><span class="sxs-lookup"><span data-stu-id="e875c-174">Constant Buffers</span></span>

<span data-ttu-id="e875c-175">Die cBuffer-Syntax (SM 5.1 Constant Buffers) wurde von SM 5.0 geändert, damit Entwickler Konstante Puffer indizieren können.</span><span class="sxs-lookup"><span data-stu-id="e875c-175">SM5.1 constant buffers (cbuffer) syntax has changed from SM5.0 to enable developers to index constant buffers.</span></span> <span data-ttu-id="e875c-176">Um indizierbare Konstante Puffer zu aktivieren, führt SM 5.1 das `ConstantBuffer` "Template"-Konstrukt ein:</span><span class="sxs-lookup"><span data-stu-id="e875c-176">To enable indexable constant buffers, SM5.1 introduces the `ConstantBuffer` “template” construct:</span></span>

``` syntax
struct Foo
{
    float4 a;
    int2 b;
};
ConstantBuffer<Foo> myCB1[2][3] : register(b2, space1);
ConstantBuffer<Foo> myCB2 : register(b0, space1);
```

<span data-ttu-id="e875c-177">Der vorangehende Code deklariert die Konstante Puffer Variable `myCB1` vom Typ `Foo` und die Größe 6 und eine skalare Konstante Puffer Variable `myCB2` .</span><span class="sxs-lookup"><span data-stu-id="e875c-177">The preceding code declares constant buffer variable `myCB1` of type `Foo` and size 6, and a scalar, constant buffer variable `myCB2`.</span></span> <span data-ttu-id="e875c-178">Eine Konstante Puffer Variable kann nun wie folgt im Shader indiziert werden:</span><span class="sxs-lookup"><span data-stu-id="e875c-178">A constant buffer variable can now be indexed in the shader as:</span></span>

``` syntax
myCB1[i][j].a.xyzw
myCB2.b.yy
```

<span data-ttu-id="e875c-179">Die Felder "a" und "b" werden nicht zu globalen Variablen, sondern müssen als Felder behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="e875c-179">Fields ‘a’ and ‘b’ do not become global variables, but rather must be treated as fields.</span></span> <span data-ttu-id="e875c-180">Aus Gründen der Abwärtskompatibilität unterstützt SM 5.1 das alte cBuffer-Konzept für skalare cbuffers.</span><span class="sxs-lookup"><span data-stu-id="e875c-180">For backward compatibility, SM5.1 supports the old cbuffer concept for scalar cbuffers.</span></span> <span data-ttu-id="e875c-181">Mit der folgenden Anweisung werden "a" und "b" globale, schreibgeschützte Variablen als in SM 5.0 definiert.</span><span class="sxs-lookup"><span data-stu-id="e875c-181">The following statement makes ‘a’ and ‘b’ global, read-only variables as in SM5.0.</span></span> <span data-ttu-id="e875c-182">Ein solcher cBuffer im alten Stil kann jedoch nicht indizierbar sein.</span><span class="sxs-lookup"><span data-stu-id="e875c-182">However, such an old-style cbuffer cannot be indexable.</span></span>

``` syntax
cbuffer : register(b1)
{
    float4 a;
    int2 b;
};
```

<span data-ttu-id="e875c-183">Der Shader-Compiler unterstützt derzeit `ConstantBuffer` nur die Vorlage für benutzerdefinierte Strukturen.</span><span class="sxs-lookup"><span data-stu-id="e875c-183">Currently, the shader compiler supports the `ConstantBuffer` template for user-defined structures only.</span></span>

<span data-ttu-id="e875c-184">Aus Kompatibilitätsgründen kann der HLSL-Compiler automatisch Ressourcen Register für in deklarierte Bereiche zuweisen `space0` .</span><span class="sxs-lookup"><span data-stu-id="e875c-184">For compatibility reasons, the HLSL compiler may automatically assign resource registers for ranges declared in `space0`.</span></span> <span data-ttu-id="e875c-185">Wenn "Space" in der Register-Klausel weggelassen wird, wird der Standardwert `space0` verwendet.</span><span class="sxs-lookup"><span data-stu-id="e875c-185">If ‘space’ is omitted in the register clause, the default `space0` is used.</span></span> <span data-ttu-id="e875c-186">Der Compiler verwendet zum Zuweisen der Register die Heuristik zum Zuweisen der Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="e875c-186">The compiler uses the first-hole-fits heuristic to assign the registers.</span></span> <span data-ttu-id="e875c-187">Die Zuweisung kann über die reflektionsapi abgerufen werden, die erweitert wurde, um das Feld " *Space* " für Leerzeichen hinzuzufügen, während das Feld " *bindpoint* " die untere Grenze des Ressourcen Registrierungs Bereichs angibt.</span><span class="sxs-lookup"><span data-stu-id="e875c-187">The assignment can be retrieved via the reflection API, which has been extended to add the *Space* field for space, while the *BindPoint* field indicates the lower bound of the resource register range.</span></span>

## <a name="bytecode-changes-in-sm51"></a><span data-ttu-id="e875c-188">Bytecode-Änderungen in SM 5.1</span><span class="sxs-lookup"><span data-stu-id="e875c-188">Bytecode changes in SM5.1</span></span>

<span data-ttu-id="e875c-189">Mit SM 5.1 wird die Deklaration von Ressourcen Registern und die referenzierte Verwendung in Anweisungen geändert.</span><span class="sxs-lookup"><span data-stu-id="e875c-189">SM5.1 changes how resource registers are declared and referenced in instructions.</span></span> <span data-ttu-id="e875c-190">Die Syntax umfasst das Deklarieren einer Register "Variablen", ähnlich wie bei Gruppen Shared Memory-Registern:</span><span class="sxs-lookup"><span data-stu-id="e875c-190">The syntax involves declaring a register “variable”, similar to how it is done for group shared memory registers:</span></span>

``` syntax
Texture2D<float4> tex0          : register(t5,  space0);
Texture2D<float4> tex1[][5][3]  : register(t10, space0);
Texture2D<float4> tex2[8]       : register(t0,  space1);
SamplerState samp0              : register(s5, space0);

float4 main(float4 coord : COORD) : SV_TARGET
{
    float4 r = coord;
    r += tex0.Sample(samp0, r.xy);
    r += tex2[r.x].Sample(samp0, r.xy);
    r += tex1[r.x][r.y][r.z].Sample(samp0, r.xy);
    return r;
}
```

<span data-ttu-id="e875c-191">Dies wird Disassemblierung zu:</span><span class="sxs-lookup"><span data-stu-id="e875c-191">This will disassemble to:</span></span>

``` syntax
// Resource Bindings:
//
// Name                                 Type  Format         Dim    ID   HLSL Bind     Count
// ------------------------------ ---------- ------- ----------- -----   --------- ---------
// samp0                             sampler      NA          NA     S0    a5            1
// tex0                              texture  float4          2d     T0    t5            1
// tex1[0][5][3]                     texture  float4          2d     T1   t10        unbounded
// tex2[8]                           texture  float4          2d     T2    t0.space1     8
//
//
//
// Input signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// COORD                    0   xyzw        0     NONE   float   xyzw
//
//
// Output signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// SV_TARGET                0   xyzw        0   TARGET   float   xyzw
//
ps_5_1
dcl_globalFlags refactoringAllowed
dcl_sampler s0[5:5], mode_default, space=0
dcl_resource_texture2d (float,float,float,float) t0[5:5], space=0
dcl_resource_texture2d (float,float,float,float) t1[10:*], space=0
dcl_resource_texture2d (float,float,float,float) t2[0:7], space=1
dcl_input_ps linear v0.xyzw
dcl_output o0.xyzw
dcl_temps 2
sample r0.xyzw, v0.xyxx, t0[0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, v0.xyzw
ftou r1.x, r0.x
sample r1.xyzw, r0.xyxx, t2[r1.x + 0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, r1.xyzw
ftou r1.xyz, r0.zyxz
imul null, r1.yz, r1.zzyz, l(0, 15, 3, 0)
iadd r1.y, r1.z, r1.y
iadd r1.x, r1.x, r1.y
sample r1.xyzw, r0.xyxx, t1[r1.x + 10].xyzw, s0[5]
add o0.xyzw, r0.xyzw, r1.xyzw
ret
// Approximately 12 instruction slots are used.
```

<span data-ttu-id="e875c-192">Jeder Shader-Ressourcenbereich verfügt jetzt über eine ID (Name), die für den Shader-Bytecode eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="e875c-192">Each shader resource range now has an ID (a name) that is unique to the shader bytecode.</span></span> <span data-ttu-id="e875c-193">Beispielsweise wird das tex1 (T10)-Textur Array im Shader-Bytecode zu 't 1 '.</span><span class="sxs-lookup"><span data-stu-id="e875c-193">For example, tex1 (t10) texture array becomes ‘T1’ in the shader bytecode.</span></span> <span data-ttu-id="e875c-194">Das Erteilen von eindeutigen IDs für jeden Ressourcenbereich ermöglicht zwei Dinge:</span><span class="sxs-lookup"><span data-stu-id="e875c-194">Giving unique IDs to each resource range allows two things:</span></span>

-   <span data-ttu-id="e875c-195">Identifizieren Sie eindeutig den Ressourcenbereich (siehe DCL \_ Resource \_ Texture2D), der in einer Anweisung indiziert wird (siehe Beispiel Anweisung).</span><span class="sxs-lookup"><span data-stu-id="e875c-195">Unambiguously identify which resource range (see dcl\_resource\_texture2d) is being indexed in an instruction (see sample instruction).</span></span>
-   <span data-ttu-id="e875c-196">Anfügen eines Satzes von Attributen an die Deklaration, z. b. Elementtyp, Stride-Größe, Raster Betriebsmodus usw.</span><span class="sxs-lookup"><span data-stu-id="e875c-196">Attaching a set of attributes to the declaration, e.g., element type, stride size, raster operation mode, etc.</span></span>

<span data-ttu-id="e875c-197">Beachten Sie, dass die ID des Bereichs nicht mit der HLSL-Deklaration in der unteren Grenze verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="e875c-197">Note that the ID of the range is not related to the HLSL lower bound declaration.</span></span>

<span data-ttu-id="e875c-198">Die Reihenfolge der reflektionsressourcenbindungen (im oberen Bereich) und der Shader-Deklarations Anweisungen (DCL \_ \* ) sind die gleichen, die Sie beim Identifizieren der Entsprechung zwischen HLSL-Variablen und Bytecode-IDs unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e875c-198">The order of reflection resource bindings (listing at the top) and shader declaration instructions (dcl\_\*) is the same to aid in identifying the correspondence between HLSL variables and bytecode IDs.</span></span>

<span data-ttu-id="e875c-199">Jede Deklarations Anweisung in SM 5.1 verwendet einen 3D-Operanden, um Folgendes zu definieren: Range ID, Lower und Upper Bounds.</span><span class="sxs-lookup"><span data-stu-id="e875c-199">Each declaration instruction in SM5.1 uses a 3D operand to define: range ID, lower and upper bounds.</span></span> <span data-ttu-id="e875c-200">Ein zusätzliches Token wird ausgegeben, um den Register Bereich anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e875c-200">An additional token is emitted to specify the register space.</span></span> <span data-ttu-id="e875c-201">Andere Token können ebenfalls ausgegeben werden, um zusätzliche Eigenschaften des Bereichs zu übermitteln, z. b. die cBuffer-Anweisung oder die strukturierte Puffer Deklarations Anweisung, die die Größe des cBuffer oder der Struktur ausgibt.</span><span class="sxs-lookup"><span data-stu-id="e875c-201">Other tokens may be emitted as well to convey additional properties of the range, e.g., cbuffer or structured buffer declaration instruction emits the size of the cbuffer or structure.</span></span> <span data-ttu-id="e875c-202">Die genauen Codierungs Details finden Sie in d3d12TokenizedProgramFormat. h und **D3D10ShaderBinary:: cshadercodeparser**.</span><span class="sxs-lookup"><span data-stu-id="e875c-202">The exact details of encoding can be found in d3d12TokenizedProgramFormat.h and **D3D10ShaderBinary::CShaderCodeParser**.</span></span>

<span data-ttu-id="e875c-203">In den Anweisungen von SM 5.1 werden im Rahmen der Anweisung (wie in SM 5.0) keine zusätzlichen Ressourcen Operanden Informationen ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="e875c-203">SM5.1 instructions will not emit additional resource operand information as part of the instruction (as in SM5.0).</span></span> <span data-ttu-id="e875c-204">Diese Informationen befinden sich nun in den Deklarations Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="e875c-204">This information is now in the declaration instructions.</span></span> <span data-ttu-id="e875c-205">In SM 5.0 erforderte das Indizieren von Ressourcen, dass Ressourcen Attribute in erweiterten Opcode-Token beschrieben werden müssen, da die Indizierung die Zuordnung zur Deklaration verdeckt hat.</span><span class="sxs-lookup"><span data-stu-id="e875c-205">In SM5.0, instructions indexing resources required resource attributes to be described in extended opcode tokens, since indexing obfuscated the association to the declaration.</span></span> <span data-ttu-id="e875c-206">In SM 5.1 ist jede ID (z. b. 't 1 ') eindeutig einer einzelnen Deklaration zugeordnet, die die erforderlichen Ressourcen Informationen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e875c-206">In SM5.1, each ID (such as ‘t1’) is unambiguously associated with a single declaration that describes the required resource information.</span></span> <span data-ttu-id="e875c-207">Daher werden die erweiterten Opcode-Token, die für Anweisungen zum Beschreiben von Ressourcen Informationen verwendet werden, nicht mehr ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="e875c-207">Therefore, the extended opcode tokens used on instructions to describe resource information are no longer emitted.</span></span>

<span data-ttu-id="e875c-208">In nicht Deklarations Anweisungen ist ein Ressourcen Operand für Samplers, Srvs und UAVs ein 2D-Operand.</span><span class="sxs-lookup"><span data-stu-id="e875c-208">In non-declaration instructions, a resource operand for samplers, SRVs, and UAVs is a 2D operand.</span></span> <span data-ttu-id="e875c-209">Der erste Index ist eine Literalkonstante, die die Bereichs-ID angibt.</span><span class="sxs-lookup"><span data-stu-id="e875c-209">The first index is a literal constant that specifies the range ID.</span></span> <span data-ttu-id="e875c-210">Der zweite Index stellt den linearisierten Wert des Indexes dar.</span><span class="sxs-lookup"><span data-stu-id="e875c-210">The second index represents the linearized value of the index.</span></span> <span data-ttu-id="e875c-211">Der Wert wird relativ zum Anfang des entsprechenden Register Bereichs (nicht relativ zum Anfang des logischen Bereichs) berechnet, um die Korrelation mit der Stamm Signatur zu verbessern und die Treiber-compilerlast für die Anpassung des Indexes zu verringern.</span><span class="sxs-lookup"><span data-stu-id="e875c-211">The value is computed relative to the beginning of the corresponding register space (not relative to the beginning of the logical range) to better correlate with the root signature and to reduce the driver compiler burden of adjusting the index.</span></span>

<span data-ttu-id="e875c-212">Ein Ressourcen Operand für cbvs ist ein 3D-Operand, der Folgendes enthält: literalid des Bereichs, Index des Konstanten Puffers, Offset in der jeweiligen Instanz des Konstanten Puffers.</span><span class="sxs-lookup"><span data-stu-id="e875c-212">A resource operand for CBVs is a 3D operand, containing: literal ID of the range, index of the constant buffer, offset into the particular instance of constant buffer.</span></span>

## <a name="example-hlsl-declarations"></a><span data-ttu-id="e875c-213">Beispiele für HLSL-Deklarationen</span><span class="sxs-lookup"><span data-stu-id="e875c-213">Example HLSL Declarations</span></span>

<span data-ttu-id="e875c-214">HLSL-Programme müssen nichts über Stamm Signaturen wissen.</span><span class="sxs-lookup"><span data-stu-id="e875c-214">HLSL programs do not need to know anything about root signatures.</span></span> <span data-ttu-id="e875c-215">Sie können dem virtuellen "Register"-Bindungs Bereich (t \# für Srvs, u \# für UAVs, b \# für cbvs, s \# für Samplers) Bindungen zuweisen, oder Sie müssen sich auf den Compiler stützen, um Zuweisungen auszuwählen (und die resultierenden Zuordnungen mithilfe der Shader-Reflektion später abzufragen).</span><span class="sxs-lookup"><span data-stu-id="e875c-215">They can assign bindings to the virtual “register” binding space, t\# for SRVs, u\# for UAVs, b\# for CBVs, s\# for samplers, or rely on the compiler to pick assignments (and query the resulting mappings using shader reflection afterwards).</span></span> <span data-ttu-id="e875c-216">Die Stamm Signatur ordnet deskriptortabellen, Stamm Deskriptoren und Stamm Konstanten diesem virtuellen Register Bereich zu.</span><span class="sxs-lookup"><span data-stu-id="e875c-216">The root signature maps descriptor tables, root descriptors, and root constants to this virtual register space.</span></span>

<span data-ttu-id="e875c-217">Im folgenden sind einige Beispiel Deklarationen dargestellt, die ein HLSL-Shader aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="e875c-217">The following are some example declarations an HLSL shader might have.</span></span> <span data-ttu-id="e875c-218">Beachten Sie, dass es keine Verweise auf Stamm Signaturen oder deskriptortabellen gibt.</span><span class="sxs-lookup"><span data-stu-id="e875c-218">Note that there are no references to root signatures or descriptor tables.</span></span>

``` syntax
Texture2D foo[5] : register(t2);
Buffer bar : register(t7);
RWBuffer dataLog : register(u1);

Sampler samp : register(s0);

struct Data
{
    UINT index;
    float4 color;
};
ConstantBuffer<Data> myData : register(b0);

Texture2D terrain[] : register(t8); // Unbounded array
Texture2D misc[] : register(t0,space1); // Another unbounded array 
                                        // space1 avoids overlap with above t#

struct MoreData
{
    float4x4 xform;
};
ConstantBuffer<MoreData> myMoreData : register(b1);

struct Stuff
{
    float2 factor;
    UINT drawID;
};
ConstantBuffer<Stuff> myStuff[][3][8]  : register(b2, space3)
```

## <a name="related-topics"></a><span data-ttu-id="e875c-219">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e875c-219">Related topics</span></span>

* [<span data-ttu-id="e875c-220">Dynamische Indizierung mit HLSL 5.1</span><span class="sxs-lookup"><span data-stu-id="e875c-220">Dynamic Indexing using HLSL 5.1</span></span>](dynamic-indexing-using-hlsl-5-1.md)
* [<span data-ttu-id="e875c-221">Effekt-Compilertool</span><span class="sxs-lookup"><span data-stu-id="e875c-221">Effect-Compiler Tool</span></span>](/windows/win32/direct3dtools/fxc)
* [<span data-ttu-id="e875c-222">HLSL-Shader-Modell 5,1 Features für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e875c-222">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](/windows/win32/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
* [<span data-ttu-id="e875c-223">Geordnete Rasterizeransichten</span><span class="sxs-lookup"><span data-stu-id="e875c-223">Rasterizer Ordered Views</span></span>](rasterizer-order-views.md)
* [<span data-ttu-id="e875c-224">Ressourcen Bindung</span><span class="sxs-lookup"><span data-stu-id="e875c-224">Resource Binding</span></span>](resource-binding.md)
* [<span data-ttu-id="e875c-225">Stammsignaturen</span><span class="sxs-lookup"><span data-stu-id="e875c-225">Root Signatures</span></span>](root-signatures.md)
* [<span data-ttu-id="e875c-226">Shadermodell 5,1</span><span class="sxs-lookup"><span data-stu-id="e875c-226">Shader Model 5.1</span></span>](/windows/win32/direct3dhlsl/shader-model-5-1)
* [<span data-ttu-id="e875c-227">Von Shader festgelegter Schablonenreferenzwert</span><span class="sxs-lookup"><span data-stu-id="e875c-227">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)
* [<span data-ttu-id="e875c-228">Festlegen von Stammsignaturen in HLSL</span><span class="sxs-lookup"><span data-stu-id="e875c-228">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
