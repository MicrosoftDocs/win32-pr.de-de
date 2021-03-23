---
title: Ressourcen Bindung in HLSL
description: In diesem Thema werden einige spezifische Features der Verwendung des HLSL-Shader-Modells 5,1 (High Level Shader Language) mit Direct3D 12 beschrieben.
ms.assetid: 3CD4BDAD-8AE3-4DE0-B3F8-9C9F9E83BBE9
ms.localizationpriority: high
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 749fed319f9ffe840f2b06512e337efa28081e24
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548710"
---
# <a name="resource-binding-in-hlsl"></a><span data-ttu-id="60ec6-103">Ressourcen Bindung in HLSL</span><span class="sxs-lookup"><span data-stu-id="60ec6-103">Resource binding in HLSL</span></span>

<span data-ttu-id="60ec6-104">In diesem Thema werden einige spezifische Features der Verwendung des HLSL- [Shader-Modells 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1) (High Level Shader Language) mit Direct3D 12 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="60ec6-104">This topic describes some specific features of using High Level Shader Language (HLSL) [Shader Model 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) with Direct3D 12.</span></span> <span data-ttu-id="60ec6-105">Alle Direct3D 12-Hardware unterstützt das Shader-Modell 5,1. die Unterstützung für dieses Modell hängt daher nicht von der Hardware Funktionsebene ab.</span><span class="sxs-lookup"><span data-stu-id="60ec6-105">All Direct3D 12 hardware supports Shader Model 5.1, so support for this model does not depend on what the hardware feature level is.</span></span>

-   [<span data-ttu-id="60ec6-106">Ressourcentypen und Arrays</span><span class="sxs-lookup"><span data-stu-id="60ec6-106">Resource types and arrays</span></span>](#resource-types-and-arrays)
-   [<span data-ttu-id="60ec6-107">Deskriptorarrays und Textur Arrays</span><span class="sxs-lookup"><span data-stu-id="60ec6-107">Descriptor arrays and texture arrays</span></span>](#descriptor-arrays-and-texture-arrays)
-   [<span data-ttu-id="60ec6-108">Ressourcen Aliasing</span><span class="sxs-lookup"><span data-stu-id="60ec6-108">Resource aliasing</span></span>](#resource-aliasing)
-   [<span data-ttu-id="60ec6-109">Abweichung und Ableitungen</span><span class="sxs-lookup"><span data-stu-id="60ec6-109">Divergence and derivatives</span></span>](#divergence-and-derivatives)
-   [<span data-ttu-id="60ec6-110">UAVs in Pixel-Shadern</span><span class="sxs-lookup"><span data-stu-id="60ec6-110">UAVs in pixel shaders</span></span>](#uavs-in-pixel-shaders)
-   [<span data-ttu-id="60ec6-111">Konstantenpuffer</span><span class="sxs-lookup"><span data-stu-id="60ec6-111">Constant Buffers</span></span>](#constant-buffers)
-   [<span data-ttu-id="60ec6-112">Bytecode-Änderungen in SM 5.1</span><span class="sxs-lookup"><span data-stu-id="60ec6-112">Bytecode changes in SM5.1</span></span>](#bytecode-changes-in-sm51)
-   [<span data-ttu-id="60ec6-113">Beispiele für HLSL-Deklarationen</span><span class="sxs-lookup"><span data-stu-id="60ec6-113">Example HLSL Declarations</span></span>](#example-hlsl-declarations)
-   [<span data-ttu-id="60ec6-114">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="60ec6-114">Related topics</span></span>](#related-topics)

## <a name="resource-types-and-arrays"></a><span data-ttu-id="60ec6-115">Ressourcentypen und Arrays</span><span class="sxs-lookup"><span data-stu-id="60ec6-115">Resource types and arrays</span></span>

<span data-ttu-id="60ec6-116">Die Ressourcen Syntax von Shader Model 5 (SM 5.0) verwendet das- `register` Schlüsselwort, um wichtige Informationen über die Ressource an den HLSL-Compiler weiterzugeben.</span><span class="sxs-lookup"><span data-stu-id="60ec6-116">Shader Model 5 (SM5.0) resource syntax uses the `register` keyword to relay important information about the resource to the HLSL compiler.</span></span> <span data-ttu-id="60ec6-117">Die folgende Anweisung deklariert z. b. ein Array aus vier Texturen, die an Slots T3, T4, T5 und T6 gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="60ec6-117">For example, the following statement declares an array of four textures bound at slots t3, t4, t5, and t6.</span></span> <span data-ttu-id="60ec6-118">T3 ist der einzige in der-Anweisung angezeigte Registrierungs Slot, der einfach der erste im Array von vier ist.</span><span class="sxs-lookup"><span data-stu-id="60ec6-118">t3 is the only register slot appearing in the statement, simply being the first in the array of four.</span></span>

``` syntax
Texture2D<float4> tex1[4] : register(t3)
```

<span data-ttu-id="60ec6-119">Die Ressourcen Syntax von Shader Model 5,1 (SM 5.1) in HLSL basiert auf der vorhandenen Register Resource-Syntax, um das Portieren zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="60ec6-119">Shader Model 5.1 (SM5.1) resource syntax in HLSL is based on existing register resource syntax, to allow easier porting.</span></span> <span data-ttu-id="60ec6-120">Direct3D 12-Ressourcen in HLSL sind an virtuelle Register innerhalb logischer Register Plätze gebunden:</span><span class="sxs-lookup"><span data-stu-id="60ec6-120">Direct3D 12 resources in HLSL are bound to virtual registers within logical register spaces:</span></span>

-   <span data-ttu-id="60ec6-121">t – für Shader-Ressourcen Sichten (SRV)</span><span class="sxs-lookup"><span data-stu-id="60ec6-121">t – for shader resource views (SRV)</span></span>
-   <span data-ttu-id="60ec6-122">s – für Samplern</span><span class="sxs-lookup"><span data-stu-id="60ec6-122">s – for samplers</span></span>
-   <span data-ttu-id="60ec6-123">u – für ungeordnete Zugriffs Sichten (UAV)</span><span class="sxs-lookup"><span data-stu-id="60ec6-123">u – for unordered access views (UAV)</span></span>
-   <span data-ttu-id="60ec6-124">b – für konstantenpuffersichten (CBV)</span><span class="sxs-lookup"><span data-stu-id="60ec6-124">b – for constant buffer views (CBV)</span></span>

<span data-ttu-id="60ec6-125">Die Stamm Signatur, die auf den Shader verweist, muss mit den deklarierten Register Slots kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="60ec6-125">The root signature referencing the shader must be compatible with the declared register slots.</span></span> <span data-ttu-id="60ec6-126">Der folgende Teil einer Stamm Signatur ist beispielsweise mit der Verwendung von Textur Slots T3 bis T6 kompatibel, da er eine Deskriptortabelle mit Slots t0 bis T98 beschreibt.</span><span class="sxs-lookup"><span data-stu-id="60ec6-126">For example, the following portion of a root signature would be compatible with the use of texture slots t3 through t6, as it describes a descriptor table with slots t0 through t98.</span></span>

``` syntax
DescriptorTable( CBV(b1), SRV(t0,numDescriptors=99), CBV(b2) )
```

<span data-ttu-id="60ec6-127">Eine Ressourcen Deklaration kann ein Skalar, ein 1D-Array oder ein mehrdimensionales Array sein:</span><span class="sxs-lookup"><span data-stu-id="60ec6-127">A resource declaration may be a scalar, a 1D array, or a multidimensional array:</span></span>

``` syntax
Texture2D<float4> tex1 : register(t3,  space0)
Texture2D<float4> tex2[4] : register(t10)
Texture2D<float4> tex3[7][5][3] : register(t20, space1)
```

<span data-ttu-id="60ec6-128">SM 5.1 verwendet dieselben Ressourcentypen und Elementtypen wie SM 5.0.</span><span class="sxs-lookup"><span data-stu-id="60ec6-128">SM5.1 uses the same resource types and element types as SM5.0 does.</span></span> <span data-ttu-id="60ec6-129">Die SM 5.1-Deklarations Limits sind flexibler und werden nur durch die Lauf Zeit-/Hardwarelimits eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="60ec6-129">SM5.1 declaration limits are more flexible, and constrained only by the runtime/hardware limits.</span></span> <span data-ttu-id="60ec6-130">Das `space` Schlüsselwort gibt an, an welchen logischen Register Bereich die deklarierte Variable gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="60ec6-130">The `space` keyword specifies to which logical register space the declared variable is bound.</span></span> <span data-ttu-id="60ec6-131">Wenn das `space` Schlüsselwort weggelassen wird, wird der standardmäßige Speicherplatz Index 0 implizit dem Bereich zugewiesen (sodass sich der `tex2` obige Bereich in befindet `space0` ).</span><span class="sxs-lookup"><span data-stu-id="60ec6-131">If the `space` keyword is omitted, then the default space index of 0 is implicitly assigned to the range (so the `tex2` range above resides in `space0`).</span></span> <span data-ttu-id="60ec6-132">`register(t3,  space0)` führt niemals zu einem Konflikt mit `register(t3,  space1)` und mit einem Array in einem anderen Bereich, das T3 enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="60ec6-132">`register(t3,  space0)` will never conflict with `register(t3,  space1)`, nor with any array in another space that might include t3.</span></span>

<span data-ttu-id="60ec6-133">Eine Array Ressource kann eine unbegrenzte Größe aufweisen, die durch Angabe der ersten zu lefenden Dimension deklariert wird, oder 0:</span><span class="sxs-lookup"><span data-stu-id="60ec6-133">An array resource may have an unbounded size, which is declared by specifying the very first dimension to be empty, or 0:</span></span>

``` syntax
Texture2D<float4> tex1[] : register(t0)
```

<span data-ttu-id="60ec6-134">Die entsprechende Deskriptortabelle könnte wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="60ec6-134">The matching descriptor table could be:</span></span>

``` syntax
DescriptorTable( CBV(b1), UAV(u0, numDescriptors = 4), SRV(t0, numDescriptors=unbounded)
```

<span data-ttu-id="60ec6-135">Ein ungebundenes Array in HLSL entspricht einer festgelegten Anzahl von `numDescriptors` in der Deskriptortabelle, und eine festgelegte Größe im HLSL entspricht einer ungebundenen Deklaration in der Deskriptortabelle.</span><span class="sxs-lookup"><span data-stu-id="60ec6-135">An unbounded array in HLSL does match a fixed number set with `numDescriptors` in the descriptor table, and a fixed size in the HLSL does match an unbounded declaration in the descriptor table.</span></span>

<span data-ttu-id="60ec6-136">Mehrdimensionale Arrays, einschließlich einer unbegrenzten Größe, sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="60ec6-136">Multi-dimensional arrays are allowed, including of an unbounded size.</span></span> <span data-ttu-id="60ec6-137">Diese mehrdimensionalen Arrays werden im Register Bereich reduziert.</span><span class="sxs-lookup"><span data-stu-id="60ec6-137">These multidimensional arrays are flattened out in register space.</span></span>

``` syntax
Texture2D<float4> tex2[3000][10] : register(t0, space0); // t0-t29999 in space0
Texture2D<float4> tex3[0][5][3] : register(t5, space1)
```

<span data-ttu-id="60ec6-138">Das Aliasing von Ressourcen Bereichen ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="60ec6-138">Aliasing of resource ranges is not allowed.</span></span> <span data-ttu-id="60ec6-139">Mit anderen Worten: für jeden Ressourcentyp (t, s, u, b) dürfen sich deklarierte Register Bereiche nicht überlappen.</span><span class="sxs-lookup"><span data-stu-id="60ec6-139">In other words, for each resource type (t, s, u, b), declared register ranges mustn't overlap.</span></span> <span data-ttu-id="60ec6-140">Dies schließt auch unbegrenzte Bereiche ein.</span><span class="sxs-lookup"><span data-stu-id="60ec6-140">That includes unbounded ranges, too.</span></span> <span data-ttu-id="60ec6-141">Bereiche, die in verschiedenen Register Bereichen deklariert werden, überlappen sich niemals</span><span class="sxs-lookup"><span data-stu-id="60ec6-141">Ranges declared in different register spaces never overlap.</span></span> <span data-ttu-id="60ec6-142">Beachten Sie, dass `tex2` sich die unbegrenzte (oben) in befindet `space0` , während sich die unbegrenzte Grenze `tex3` in befindet `space1` , sodass Sie sich nicht überlappen.</span><span class="sxs-lookup"><span data-stu-id="60ec6-142">Note that unbounded `tex2` (above) resides in `space0`, while unbounded `tex3` resides in `space1`, such that they don't overlap.</span></span>

<span data-ttu-id="60ec6-143">Der Zugriff auf Ressourcen, die als Arrays deklariert wurden, ist so einfach wie die Indizierung.</span><span class="sxs-lookup"><span data-stu-id="60ec6-143">Accessing resources that have been declared as arrays is as simple as indexing them.</span></span>

``` syntax
Texture2D<float4> tex1[400] : register(t3);
sampler samp[7] : register(s0);
tex1[myMaterialID].Sample(samp[samplerID], texCoords);
```

<span data-ttu-id="60ec6-144">Es gibt eine wichtige Standard Beschränkung für die Verwendung der Indizes ( `myMaterialID` und `samplerID` im obigen Code) darin, dass Sie innerhalb einer [Welle](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology)nicht variieren dürfen.</span><span class="sxs-lookup"><span data-stu-id="60ec6-144">There's an important default restriction on the use of the indices (`myMaterialID` and `samplerID` in the code above) in that they're not allowed to vary within a [wave](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology).</span></span> <span data-ttu-id="60ec6-145">Sogar das Ändern des Indexes auf der Grundlage der instanziierungsanzahl als unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="60ec6-145">Even changing the index based on instancing counts as varying.</span></span>

<span data-ttu-id="60ec6-146">Wenn Sie den Index variieren müssen, geben Sie den `NonUniformResourceIndex` Qualifizierer für den Index an, z. b.:</span><span class="sxs-lookup"><span data-stu-id="60ec6-146">If varying the index is required then specify the `NonUniformResourceIndex` qualifier on the index, for example:</span></span>

``` syntax
tex1[NonUniformResourceIndex(myMaterialID)].Sample(samp[NonUniformResourceIndex(samplerID)], texCoords);
```

<span data-ttu-id="60ec6-147">Bei bestimmter Hardware generiert die Verwendung dieses Qualifizierers zusätzlichen Code, um die Richtigkeit (auch Thread übergreifend) zu erzwingen, jedoch geringfügige Leistungseinbußen.</span><span class="sxs-lookup"><span data-stu-id="60ec6-147">On some hardware the use of this qualifier generates additional code to enforce correctness (including across threads) but at a minor performance cost.</span></span> <span data-ttu-id="60ec6-148">Wenn ein Index ohne diesen Qualifizierer geändert wird und innerhalb eines zeichnen/dispatchvorgangs die Ergebnisse nicht definiert sind.</span><span class="sxs-lookup"><span data-stu-id="60ec6-148">If an index is changed without this qualifier and within a draw/dispatch the results are undefined.</span></span>

## <a name="descriptor-arrays-and-texture-arrays"></a><span data-ttu-id="60ec6-149">Deskriptorarrays und Textur Arrays</span><span class="sxs-lookup"><span data-stu-id="60ec6-149">Descriptor arrays and texture arrays</span></span>

<span data-ttu-id="60ec6-150">Textur Arrays sind seit DirectX 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="60ec6-150">Texture arrays have been available since DirectX 10.</span></span> <span data-ttu-id="60ec6-151">Textur Arrays erfordern einen Deskriptor, aber alle Array Slices müssen das gleiche Format, Breite, Höhe und MIP-Anzahl aufweisen.</span><span class="sxs-lookup"><span data-stu-id="60ec6-151">Texture arrays require one descriptor, however all the array slices must share the same format, width, height and mip count.</span></span> <span data-ttu-id="60ec6-152">Außerdem muss das Array einen zusammenhängenden Bereich im virtuellen Adressraum belegen.</span><span class="sxs-lookup"><span data-stu-id="60ec6-152">Also, the array must occupy a contiguous range in virtual address space.</span></span> <span data-ttu-id="60ec6-153">Der folgende Code zeigt ein Beispiel für den Zugriff auf ein Textur Array aus einem Shader.</span><span class="sxs-lookup"><span data-stu-id="60ec6-153">The following code shows an example of accessing a texture array from a shader.</span></span>

``` syntax
float3 myCoord(1.0f,1.4f,2.2f); // 2.2f is array index (rounded to int)
color = myTex2DArray.Sample(mySampler, myCoord);
```

<span data-ttu-id="60ec6-154">In einem Textur Array kann der Index frei variieren, ohne dass Qualifizierer wie z. b `NonUniformResourceIndex` . erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="60ec6-154">In a texture array, the index can be varied freely, without any need for qualifiers such as `NonUniformResourceIndex`.</span></span>

<span data-ttu-id="60ec6-155">Das entsprechende deskriptorarray wäre wie folgt:</span><span class="sxs-lookup"><span data-stu-id="60ec6-155">The equivalent descriptor array would be:</span></span>

``` syntax
Texture2D<float4> myTex2DArray[] : register(t0); // t0+
float2 myCoord(1.0f, 1.4f);
color = myTex2D[2].Sample(mySampler,myCoord); // 2 is index
```

<span data-ttu-id="60ec6-156">Beachten Sie, dass die umständliche Verwendung eines float-Arrays für den Array Index durch ersetzt wird `myTex2D[2]` .</span><span class="sxs-lookup"><span data-stu-id="60ec6-156">Note the awkward use of a float for the array index is replaced with `myTex2D[2]`.</span></span> <span data-ttu-id="60ec6-157">Außerdem bieten deskriptorarrays mehr Flexibilität in Bezug auf die Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="60ec6-157">Also descriptor arrays offer more flexibility with the dimensions.</span></span> <span data-ttu-id="60ec6-158">Der-Typ, `Texture2D` ist dieses Beispiel, kann nicht variieren, aber das Format, die Breite, die Höhe und die MIP-Anzahl können bei jedem Deskriptor variieren.</span><span class="sxs-lookup"><span data-stu-id="60ec6-158">The type, `Texture2D` is this example, cannot vary, but the format, width, height, and mip count can all vary with each descriptor.</span></span>

<span data-ttu-id="60ec6-159">Es ist legitim, ein deskriptorarray von Textur Arrays zu haben:</span><span class="sxs-lookup"><span data-stu-id="60ec6-159">It is legitimate to have a descriptor array of texture arrays:</span></span>

``` syntax
Texture2DArray<float4> myTex2DArrayOfArrays[2] : register(t0);
```

<span data-ttu-id="60ec6-160">Es ist nicht legitim, ein Array von Strukturen zu deklarieren, jede Struktur mit Deskriptoren, z. b. der folgende Code wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="60ec6-160">It is not legitimate to declare an array of structures, each structure containing descriptors, for example the following code is not supported.</span></span>

``` syntax
struct myStruct {
    Texture2D                    a; 
    Texture2D                    b;
    ConstantBuffer<myConstants>  c;
};
myStruct foo[10000] : register(....);
```

<span data-ttu-id="60ec6-161">Dies hätte das Speicher Layout **abcab.**.., aber eine sprach Einschränkung und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="60ec6-161">This would have allowed the memory layout **abcabcabc....**, but is a language limitation and is not supported.</span></span> <span data-ttu-id="60ec6-162">Eine unterstützte Methode hierfür wäre wie folgt, obwohl das Speicher Layout in diesem Fall **AAA ist... BBB... CCC...**</span><span class="sxs-lookup"><span data-stu-id="60ec6-162">One supported method of doing this would be as follows, though the memory layout in this case is **aaa...bbb...ccc...**.</span></span>

``` syntax
Texture2D                     a[10000] : register(t0);
Texture2D                     b[10000] : register(t10000);
ConstantBuffer<myConstants>   c[10000] : register(b0);
```

<span data-ttu-id="60ec6-163">Um das Layout " **abcabcabc....** Memory" zu erreichen, verwenden Sie eine Deskriptortabelle, ohne die-Struktur zu verwenden `myStruct` .</span><span class="sxs-lookup"><span data-stu-id="60ec6-163">To achieve the **abcabcabc....** memory layout, use a descriptor table without use of the `myStruct` structure.</span></span>

## <a name="resource-aliasing"></a><span data-ttu-id="60ec6-164">Ressourcen Aliasing</span><span class="sxs-lookup"><span data-stu-id="60ec6-164">Resource aliasing</span></span>

<span data-ttu-id="60ec6-165">Die in den HLSL-Shadern angegebenen Ressourcen Bereiche sind logische Bereiche.</span><span class="sxs-lookup"><span data-stu-id="60ec6-165">The resource ranges specified in the HLSL shaders are logical ranges.</span></span> <span data-ttu-id="60ec6-166">Sie werden zur Laufzeit über den Stamm Signatur Mechanismus an konkrete Heap Bereiche gebunden.</span><span class="sxs-lookup"><span data-stu-id="60ec6-166">They are be bound to concrete heap ranges at runtime via the root signature mechanism.</span></span> <span data-ttu-id="60ec6-167">Normalerweise wird ein logischer Bereich einem Heap Bereich zugeordnet, der sich nicht mit anderen Heap Bereichen überlappt.</span><span class="sxs-lookup"><span data-stu-id="60ec6-167">Normally, a logical range maps to a heap range that does not overlap with other heap ranges.</span></span> <span data-ttu-id="60ec6-168">Der root Signature-Mechanismus ermöglicht jedoch das Alias (Überlappung) von Heap Bereichen kompatibler Typen.</span><span class="sxs-lookup"><span data-stu-id="60ec6-168">However, the root signature mechanism makes it possible to alias (overlap) heap ranges of compatible types.</span></span> <span data-ttu-id="60ec6-169">Beispielsweise `tex2` können und `tex3` Bereiche aus dem obigen Beispiel dem gleichen (oder überlappenden) Heap Bereich zugeordnet werden, der die Auswirkungen von Aliasing Texturen im HLSL-Programm hat.</span><span class="sxs-lookup"><span data-stu-id="60ec6-169">For example, `tex2` and `tex3` ranges from the above example may be mapped to the same (or overlapping) heap range, which has the effect of aliasing textures in the HLSL program.</span></span> <span data-ttu-id="60ec6-170">Wenn ein solches Alias gewünscht ist, muss der Shader mit der Option d3d10 \_ Shader \_ Resources \_ \_ Alias Alias kompiliert werden, die mithilfe der Option */Res \_ May \_ Alias* für das [Effekt-Compilertool](/windows/desktop/direct3dtools/fxc) (FXC) festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="60ec6-170">If such aliasing is desired, the shader must be compiled with D3D10\_SHADER\_RESOURCES\_MAY\_ALIAS option, which is set by using the */res\_may\_alias* option for the [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC).</span></span> <span data-ttu-id="60ec6-171">Die-Option bewirkt, dass der Compiler korrekten Code erzeugt, indem bestimmte Lade-/Speicheroptimierungen unter der Annahme vermieden werden, dass Ressourcen Alias sein dürfen.</span><span class="sxs-lookup"><span data-stu-id="60ec6-171">The option makes the compiler produce correct code by preventing certain load/store optimizations under the assumption that resources may alias.</span></span>

## <a name="divergence-and-derivatives"></a><span data-ttu-id="60ec6-172">Abweichung und Ableitungen</span><span class="sxs-lookup"><span data-stu-id="60ec6-172">Divergence and derivatives</span></span>

<span data-ttu-id="60ec6-173">SM 5.1 weist keine Einschränkungen für den Ressourcen Index auf. Das heißt, ` tex2[idx].Sample(…)` – der Index IDX kann eine Literalkonstante, eine cBuffer-Konstante oder ein interinterpolated-Wert sein.</span><span class="sxs-lookup"><span data-stu-id="60ec6-173">SM5.1 does not impose limitations on the resource index; i.e.,` tex2[idx].Sample(…)` – the index idx can be a literal constant, a cbuffer constant, or an interpolated value.</span></span> <span data-ttu-id="60ec6-174">Obwohl das Programmiermodell eine sehr hohe Flexibilität bietet, müssen Probleme beachtet werden:</span><span class="sxs-lookup"><span data-stu-id="60ec6-174">While the programming model provides such great flexibility, there are issues to be aware of:</span></span>

-   <span data-ttu-id="60ec6-175">Wenn der Index über ein vierfache abweicht, sind die von der Hardware berechnete Ableitung und abgeleiteten Mengen wie Lod möglicherweise nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="60ec6-175">If index diverges across a quad, the hardware-computed derivative and derived quantities such as LOD may be undefined.</span></span> <span data-ttu-id="60ec6-176">Der HLSL-Compiler unternimmt den besten Aufwand, in diesem Fall eine Warnung auszugeben, verhindert jedoch nicht, dass ein Shader kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="60ec6-176">The HLSL compiler makes the best effort to issue a warning in this case, but will not prevent a shader from compiling.</span></span> <span data-ttu-id="60ec6-177">Dieses Verhalten ähnelt dem Berechnen von Ableitungen in einer abweichenden Ablauf Steuerung.</span><span class="sxs-lookup"><span data-stu-id="60ec6-177">This behavior is similar to computing derivatives in divergent control flow.</span></span>
-   <span data-ttu-id="60ec6-178">Wenn der Ressourcen Index abweicht, wird die Leistung im Vergleich zur Groß-/Kleinschreibung eines einheitlichen Indexes verringert, da die Hardware Vorgänge für mehrere Ressourcen ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="60ec6-178">If the resource index is divergent, the performance is diminished compared to the case of a uniform index, because the hardware needs to perform operations on several resources.</span></span> <span data-ttu-id="60ec6-179">Ressourcen Indizes, die abweichen können, müssen mit der- `NonUniformResourceIndex` Funktion im HLSL-Code gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="60ec6-179">Resource indexes that may be divergent must be marked with the `NonUniformResourceIndex` function in HLSL code.</span></span> <span data-ttu-id="60ec6-180">Andernfalls sind die Ergebnisse nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="60ec6-180">Otherwise results are undefined.</span></span>

## <a name="uavs-in-pixel-shaders"></a><span data-ttu-id="60ec6-181">UAVs in Pixel-Shadern</span><span class="sxs-lookup"><span data-stu-id="60ec6-181">UAVs in pixel shaders</span></span>

<span data-ttu-id="60ec6-182">SM 5.1 erzwingt keine Einschränkungen für UAV-Bereiche in Pixel-Shadern, wie es bei SM 5.0 der Fall war.</span><span class="sxs-lookup"><span data-stu-id="60ec6-182">SM5.1 does not impose constraints on UAV ranges in pixel shaders as was the case for SM5.0.</span></span>

## <a name="constant-buffers"></a><span data-ttu-id="60ec6-183">Konstantenpuffer</span><span class="sxs-lookup"><span data-stu-id="60ec6-183">Constant Buffers</span></span>

<span data-ttu-id="60ec6-184">Die cBuffer-Syntax (SM 5.1 Constant Buffers) wurde von SM 5.0 geändert, damit Entwickler Konstante Puffer indizieren können.</span><span class="sxs-lookup"><span data-stu-id="60ec6-184">SM5.1 constant buffers (cbuffer) syntax has changed from SM5.0 to enable developers to index constant buffers.</span></span> <span data-ttu-id="60ec6-185">Um indizierbare Konstante Puffer zu aktivieren, führt SM 5.1 das `ConstantBuffer` "Template"-Konstrukt ein:</span><span class="sxs-lookup"><span data-stu-id="60ec6-185">To enable indexable constant buffers, SM5.1 introduces the `ConstantBuffer` “template” construct:</span></span>

``` syntax
struct Foo
{
    float4 a;
    int2 b;
};
ConstantBuffer<Foo> myCB1[2][3] : register(b2, space1);
ConstantBuffer<Foo> myCB2 : register(b0, space1);
```

<span data-ttu-id="60ec6-186">Der vorangehende Code deklariert die Konstante Puffer Variable `myCB1` vom Typ `Foo` und die Größe 6 und eine skalare Konstante Puffer Variable `myCB2` .</span><span class="sxs-lookup"><span data-stu-id="60ec6-186">The preceding code declares constant buffer variable `myCB1` of type `Foo` and size 6, and a scalar, constant buffer variable `myCB2`.</span></span> <span data-ttu-id="60ec6-187">Eine Konstante Puffer Variable kann nun wie folgt im Shader indiziert werden:</span><span class="sxs-lookup"><span data-stu-id="60ec6-187">A constant buffer variable can now be indexed in the shader as:</span></span>

``` syntax
myCB1[i][j].a.xyzw
myCB2.b.yy
```

<span data-ttu-id="60ec6-188">Die Felder "a" und "b" werden nicht zu globalen Variablen, sondern müssen als Felder behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="60ec6-188">Fields ‘a’ and ‘b’ do not become global variables, but rather must be treated as fields.</span></span> <span data-ttu-id="60ec6-189">Aus Gründen der Abwärtskompatibilität unterstützt SM 5.1 das alte cBuffer-Konzept für skalare cbuffers.</span><span class="sxs-lookup"><span data-stu-id="60ec6-189">For backward compatibility, SM5.1 supports the old cbuffer concept for scalar cbuffers.</span></span> <span data-ttu-id="60ec6-190">Mit der folgenden Anweisung werden "a" und "b" globale, schreibgeschützte Variablen als in SM 5.0 definiert.</span><span class="sxs-lookup"><span data-stu-id="60ec6-190">The following statement makes ‘a’ and ‘b’ global, read-only variables as in SM5.0.</span></span> <span data-ttu-id="60ec6-191">Ein solcher cBuffer im alten Stil kann jedoch nicht indizierbar sein.</span><span class="sxs-lookup"><span data-stu-id="60ec6-191">However, such an old-style cbuffer cannot be indexable.</span></span>

``` syntax
cbuffer : register(b1)
{
    float4 a;
    int2 b;
};
```

<span data-ttu-id="60ec6-192">Der Shader-Compiler unterstützt derzeit `ConstantBuffer` nur die Vorlage für benutzerdefinierte Strukturen.</span><span class="sxs-lookup"><span data-stu-id="60ec6-192">Currently, the shader compiler supports the `ConstantBuffer` template for user-defined structures only.</span></span>

<span data-ttu-id="60ec6-193">Aus Kompatibilitätsgründen kann der HLSL-Compiler automatisch Ressourcen Register für in deklarierte Bereiche zuweisen `space0` .</span><span class="sxs-lookup"><span data-stu-id="60ec6-193">For compatibility reasons, the HLSL compiler may automatically assign resource registers for ranges declared in `space0`.</span></span> <span data-ttu-id="60ec6-194">Wenn "Space" in der Register-Klausel weggelassen wird, wird der Standardwert `space0` verwendet.</span><span class="sxs-lookup"><span data-stu-id="60ec6-194">If ‘space’ is omitted in the register clause, the default `space0` is used.</span></span> <span data-ttu-id="60ec6-195">Der Compiler verwendet zum Zuweisen der Register die Heuristik zum Zuweisen der Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="60ec6-195">The compiler uses the first-hole-fits heuristic to assign the registers.</span></span> <span data-ttu-id="60ec6-196">Die Zuweisung kann über die reflektionsapi abgerufen werden, die erweitert wurde, um das Feld " *Space* " für Leerzeichen hinzuzufügen, während das Feld " *bindpoint* " die untere Grenze des Ressourcen Registrierungs Bereichs angibt.</span><span class="sxs-lookup"><span data-stu-id="60ec6-196">The assignment can be retrieved via the reflection API, which has been extended to add the *Space* field for space, while the *BindPoint* field indicates the lower bound of the resource register range.</span></span>

## <a name="bytecode-changes-in-sm51"></a><span data-ttu-id="60ec6-197">Bytecode-Änderungen in SM 5.1</span><span class="sxs-lookup"><span data-stu-id="60ec6-197">Bytecode changes in SM5.1</span></span>

<span data-ttu-id="60ec6-198">Mit SM 5.1 wird die Deklaration von Ressourcen Registern und die referenzierte Verwendung in Anweisungen geändert.</span><span class="sxs-lookup"><span data-stu-id="60ec6-198">SM5.1 changes how resource registers are declared and referenced in instructions.</span></span> <span data-ttu-id="60ec6-199">Die Syntax umfasst das Deklarieren einer Register "Variablen", ähnlich wie bei Gruppen Shared Memory-Registern:</span><span class="sxs-lookup"><span data-stu-id="60ec6-199">The syntax involves declaring a register “variable”, similar to how it is done for group shared memory registers:</span></span>

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

<span data-ttu-id="60ec6-200">Dies wird Disassemblierung zu:</span><span class="sxs-lookup"><span data-stu-id="60ec6-200">This will disassemble to:</span></span>

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

<span data-ttu-id="60ec6-201">Jeder Shader-Ressourcenbereich verfügt jetzt über eine ID (Name), die für den Shader-Bytecode eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="60ec6-201">Each shader resource range now has an ID (a name) that is unique to the shader bytecode.</span></span> <span data-ttu-id="60ec6-202">Beispielsweise wird das tex1 (T10)-Textur Array im Shader-Bytecode zu 't 1 '.</span><span class="sxs-lookup"><span data-stu-id="60ec6-202">For example, tex1 (t10) texture array becomes ‘T1’ in the shader bytecode.</span></span> <span data-ttu-id="60ec6-203">Das Erteilen von eindeutigen IDs für jeden Ressourcenbereich ermöglicht zwei Dinge:</span><span class="sxs-lookup"><span data-stu-id="60ec6-203">Giving unique IDs to each resource range allows two things:</span></span>

-   <span data-ttu-id="60ec6-204">Identifizieren Sie eindeutig den Ressourcenbereich (siehe DCL \_ Resource \_ Texture2D), der in einer Anweisung indiziert wird (siehe Beispiel Anweisung).</span><span class="sxs-lookup"><span data-stu-id="60ec6-204">Unambiguously identify which resource range (see dcl\_resource\_texture2d) is being indexed in an instruction (see sample instruction).</span></span>
-   <span data-ttu-id="60ec6-205">Anfügen eines Satzes von Attributen an die Deklaration, z. b. Elementtyp, Stride-Größe, Raster Betriebsmodus usw.</span><span class="sxs-lookup"><span data-stu-id="60ec6-205">Attaching a set of attributes to the declaration, e.g., element type, stride size, raster operation mode, etc.</span></span>

<span data-ttu-id="60ec6-206">Beachten Sie, dass die ID des Bereichs nicht mit der HLSL-Deklaration in der unteren Grenze verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="60ec6-206">Note that the ID of the range is not related to the HLSL lower bound declaration.</span></span>

<span data-ttu-id="60ec6-207">Die Reihenfolge der reflektionsressourcenbindungen (im oberen Bereich) und der Shader-Deklarations Anweisungen (DCL \_ \* ) sind die gleichen, die Sie beim Identifizieren der Entsprechung zwischen HLSL-Variablen und Bytecode-IDs unterstützen.</span><span class="sxs-lookup"><span data-stu-id="60ec6-207">The order of reflection resource bindings (listing at the top) and shader declaration instructions (dcl\_\*) is the same to aid in identifying the correspondence between HLSL variables and bytecode IDs.</span></span>

<span data-ttu-id="60ec6-208">Jede Deklarations Anweisung in SM 5.1 verwendet einen 3D-Operanden, um Folgendes zu definieren: Range ID, Lower und Upper Bounds.</span><span class="sxs-lookup"><span data-stu-id="60ec6-208">Each declaration instruction in SM5.1 uses a 3D operand to define: range ID, lower and upper bounds.</span></span> <span data-ttu-id="60ec6-209">Ein zusätzliches Token wird ausgegeben, um den Register Bereich anzugeben.</span><span class="sxs-lookup"><span data-stu-id="60ec6-209">An additional token is emitted to specify the register space.</span></span> <span data-ttu-id="60ec6-210">Andere Token können ebenfalls ausgegeben werden, um zusätzliche Eigenschaften des Bereichs zu übermitteln, z. b. die cBuffer-Anweisung oder die strukturierte Puffer Deklarations Anweisung, die die Größe des cBuffer oder der Struktur ausgibt.</span><span class="sxs-lookup"><span data-stu-id="60ec6-210">Other tokens may be emitted as well to convey additional properties of the range, e.g., cbuffer or structured buffer declaration instruction emits the size of the cbuffer or structure.</span></span> <span data-ttu-id="60ec6-211">Die genauen Codierungs Details finden Sie in d3d12TokenizedProgramFormat. h und **D3D10ShaderBinary:: cshadercodeparser**.</span><span class="sxs-lookup"><span data-stu-id="60ec6-211">The exact details of encoding can be found in d3d12TokenizedProgramFormat.h and **D3D10ShaderBinary::CShaderCodeParser**.</span></span>

<span data-ttu-id="60ec6-212">In den Anweisungen von SM 5.1 werden im Rahmen der Anweisung (wie in SM 5.0) keine zusätzlichen Ressourcen Operanden Informationen ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="60ec6-212">SM5.1 instructions will not emit additional resource operand information as part of the instruction (as in SM5.0).</span></span> <span data-ttu-id="60ec6-213">Diese Informationen befinden sich nun in den Deklarations Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="60ec6-213">This information is now in the declaration instructions.</span></span> <span data-ttu-id="60ec6-214">In SM 5.0 erforderte das Indizieren von Ressourcen, dass Ressourcen Attribute in erweiterten Opcode-Token beschrieben werden müssen, da die Indizierung die Zuordnung zur Deklaration verdeckt hat.</span><span class="sxs-lookup"><span data-stu-id="60ec6-214">In SM5.0, instructions indexing resources required resource attributes to be described in extended opcode tokens, since indexing obfuscated the association to the declaration.</span></span> <span data-ttu-id="60ec6-215">In SM 5.1 ist jede ID (z. b. 't 1 ') eindeutig einer einzelnen Deklaration zugeordnet, die die erforderlichen Ressourcen Informationen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="60ec6-215">In SM5.1, each ID (such as ‘t1’) is unambiguously associated with a single declaration that describes the required resource information.</span></span> <span data-ttu-id="60ec6-216">Daher werden die erweiterten Opcode-Token, die für Anweisungen zum Beschreiben von Ressourcen Informationen verwendet werden, nicht mehr ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="60ec6-216">Therefore, the extended opcode tokens used on instructions to describe resource information are no longer emitted.</span></span>

<span data-ttu-id="60ec6-217">In nicht Deklarations Anweisungen ist ein Ressourcen Operand für Samplers, Srvs und UAVs ein 2D-Operand.</span><span class="sxs-lookup"><span data-stu-id="60ec6-217">In non-declaration instructions, a resource operand for samplers, SRVs, and UAVs is a 2D operand.</span></span> <span data-ttu-id="60ec6-218">Der erste Index ist eine Literalkonstante, die die Bereichs-ID angibt.</span><span class="sxs-lookup"><span data-stu-id="60ec6-218">The first index is a literal constant that specifies the range ID.</span></span> <span data-ttu-id="60ec6-219">Der zweite Index stellt den linearisierten Wert des Indexes dar.</span><span class="sxs-lookup"><span data-stu-id="60ec6-219">The second index represents the linearized value of the index.</span></span> <span data-ttu-id="60ec6-220">Der Wert wird relativ zum Anfang des entsprechenden Register Bereichs (nicht relativ zum Anfang des logischen Bereichs) berechnet, um die Korrelation mit der Stamm Signatur zu verbessern und die Treiber-compilerlast für die Anpassung des Indexes zu verringern.</span><span class="sxs-lookup"><span data-stu-id="60ec6-220">The value is computed relative to the beginning of the corresponding register space (not relative to the beginning of the logical range) to better correlate with the root signature and to reduce the driver compiler burden of adjusting the index.</span></span>

<span data-ttu-id="60ec6-221">Ein Ressourcen Operand für cbvs ist ein 3D-Operand, der Folgendes enthält: literalid des Bereichs, Index des Konstanten Puffers, Offset in der jeweiligen Instanz des Konstanten Puffers.</span><span class="sxs-lookup"><span data-stu-id="60ec6-221">A resource operand for CBVs is a 3D operand, containing: literal ID of the range, index of the constant buffer, offset into the particular instance of constant buffer.</span></span>

## <a name="example-hlsl-declarations"></a><span data-ttu-id="60ec6-222">Beispiele für HLSL-Deklarationen</span><span class="sxs-lookup"><span data-stu-id="60ec6-222">Example HLSL Declarations</span></span>

<span data-ttu-id="60ec6-223">HLSL-Programme müssen nichts über Stamm Signaturen wissen.</span><span class="sxs-lookup"><span data-stu-id="60ec6-223">HLSL programs do not need to know anything about root signatures.</span></span> <span data-ttu-id="60ec6-224">Sie können dem virtuellen "Register"-Bindungs Bereich (t \# für Srvs, u \# für UAVs, b \# für cbvs, s \# für Samplers) Bindungen zuweisen, oder Sie müssen sich auf den Compiler stützen, um Zuweisungen auszuwählen (und die resultierenden Zuordnungen mithilfe der Shader-Reflektion später abzufragen).</span><span class="sxs-lookup"><span data-stu-id="60ec6-224">They can assign bindings to the virtual “register” binding space, t\# for SRVs, u\# for UAVs, b\# for CBVs, s\# for samplers, or rely on the compiler to pick assignments (and query the resulting mappings using shader reflection afterwards).</span></span> <span data-ttu-id="60ec6-225">Die Stamm Signatur ordnet deskriptortabellen, Stamm Deskriptoren und Stamm Konstanten diesem virtuellen Register Bereich zu.</span><span class="sxs-lookup"><span data-stu-id="60ec6-225">The root signature maps descriptor tables, root descriptors, and root constants to this virtual register space.</span></span>

<span data-ttu-id="60ec6-226">Im folgenden sind einige Beispiel Deklarationen dargestellt, die ein HLSL-Shader aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="60ec6-226">The following are some example declarations an HLSL shader might have.</span></span> <span data-ttu-id="60ec6-227">Beachten Sie, dass es keine Verweise auf Stamm Signaturen oder deskriptortabellen gibt.</span><span class="sxs-lookup"><span data-stu-id="60ec6-227">Note that there are no references to root signatures or descriptor tables.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="60ec6-228">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="60ec6-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60ec6-229">Dynamische Indizierung mit HLSL 5.1</span><span class="sxs-lookup"><span data-stu-id="60ec6-229">Dynamic Indexing using HLSL 5.1</span></span>](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[<span data-ttu-id="60ec6-230">Effekt-Compilertool</span><span class="sxs-lookup"><span data-stu-id="60ec6-230">Effect-Compiler Tool</span></span>](/windows/desktop/direct3dtools/fxc)
</dt> <dt>

[<span data-ttu-id="60ec6-231">HLSL-Shader-Modell 5,1 Features für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="60ec6-231">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[<span data-ttu-id="60ec6-232">Geordnete Ansichten des Rasterizers</span><span class="sxs-lookup"><span data-stu-id="60ec6-232">Rasterizer Ordered Views</span></span>](rasterizer-order-views.md)
</dt> <dt>

[<span data-ttu-id="60ec6-233">Ressourcen Bindung</span><span class="sxs-lookup"><span data-stu-id="60ec6-233">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="60ec6-234">Stamm Signaturen</span><span class="sxs-lookup"><span data-stu-id="60ec6-234">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="60ec6-235">Shadermodell 5,1</span><span class="sxs-lookup"><span data-stu-id="60ec6-235">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="60ec6-236">Von Shader angegebener Schablone-Verweis Wert</span><span class="sxs-lookup"><span data-stu-id="60ec6-236">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)
</dt> <dt>

[<span data-ttu-id="60ec6-237">Angeben von Stamm Signaturen in HLSL</span><span class="sxs-lookup"><span data-stu-id="60ec6-237">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 