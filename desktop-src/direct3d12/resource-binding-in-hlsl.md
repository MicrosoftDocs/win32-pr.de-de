---
title: Ressourcenbindung in HLSL
description: In diesem Thema werden einige spezifische Features der Verwendung des HLSL-Shadermodells 5.1 (High Level Shader Language) mit Direct3D 12 beschrieben.
ms.assetid: 3CD4BDAD-8AE3-4DE0-B3F8-9C9F9E83BBE9
ms.localizationpriority: high
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 711ccdee71ff916445be68d03b84b7621aa04cf3
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550385"
---
# <a name="resource-binding-in-hlsl"></a><span data-ttu-id="bb3dd-103">Ressourcenbindung in HLSL</span><span class="sxs-lookup"><span data-stu-id="bb3dd-103">Resource binding in HLSL</span></span>

<span data-ttu-id="bb3dd-104">In diesem Thema werden einige spezifische Features der Verwendung des [HLSL-Shadermodells 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) (High Level Shader Language) mit Direct3D 12 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-104">This topic describes some specific features of using High Level Shader Language (HLSL) [Shader Model 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) with Direct3D 12.</span></span> <span data-ttu-id="bb3dd-105">Alle Direct3D 12-Hardware unterstützt shader Model 5.1, sodass die Unterstützung für dieses Modell nicht von der Hardwarefeatureebene abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-105">All Direct3D 12 hardware supports Shader Model 5.1, so support for this model does not depend on what the hardware feature level is.</span></span>

## <a name="resource-types-and-arrays"></a><span data-ttu-id="bb3dd-106">Ressourcentypen und Arrays</span><span class="sxs-lookup"><span data-stu-id="bb3dd-106">Resource types and arrays</span></span>

<span data-ttu-id="bb3dd-107">Die Ressourcensyntax des Shaders Model 5 (SM5.0) verwendet das Schlüsselwort , um wichtige Informationen zur Ressource an den `register` HLSL-Compiler weiter zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-107">Shader Model 5 (SM5.0) resource syntax uses the `register` keyword to relay important information about the resource to the HLSL compiler.</span></span> <span data-ttu-id="bb3dd-108">Die folgende Anweisung deklariert beispielsweise ein Array von vier Texturen, die an den Slots t3, t4, t5 und t6 gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-108">For example, the following statement declares an array of four textures bound at slots t3, t4, t5, and t6.</span></span> <span data-ttu-id="bb3dd-109">t3 ist der einzige Registerslot, der in der -Anweisung angezeigt wird und einfach der erste im Array von vier ist.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-109">t3 is the only register slot appearing in the statement, simply being the first in the array of four.</span></span>

``` syntax
Texture2D<float4> tex1[4] : register(t3)
```

<span data-ttu-id="bb3dd-110">Die Ressourcensyntax des Shadermodells 5.1 (SM5.1) in HLSL basiert auf der vorhandenen Syntax für Registerressourcen, um eine einfachere Portierung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-110">Shader Model 5.1 (SM5.1) resource syntax in HLSL is based on existing register resource syntax, to allow easier porting.</span></span> <span data-ttu-id="bb3dd-111">Direct3D 12-Ressourcen in HLSL sind an virtuelle Register innerhalb logischer Registerräume gebunden:</span><span class="sxs-lookup"><span data-stu-id="bb3dd-111">Direct3D 12 resources in HLSL are bound to virtual registers within logical register spaces:</span></span>

-   <span data-ttu-id="bb3dd-112">t – für Shaderressourcenansichten (SRV)</span><span class="sxs-lookup"><span data-stu-id="bb3dd-112">t – for shader resource views (SRV)</span></span>
-   <span data-ttu-id="bb3dd-113">s – für Sampler</span><span class="sxs-lookup"><span data-stu-id="bb3dd-113">s – for samplers</span></span>
-   <span data-ttu-id="bb3dd-114">u – für ungeordnete Zugriffsansichten (UAV)</span><span class="sxs-lookup"><span data-stu-id="bb3dd-114">u – for unordered access views (UAV)</span></span>
-   <span data-ttu-id="bb3dd-115">b – für konstante Pufferansichten (CBV)</span><span class="sxs-lookup"><span data-stu-id="bb3dd-115">b – for constant buffer views (CBV)</span></span>

<span data-ttu-id="bb3dd-116">Die Stammsignatur, die auf den Shader verweisen soll, muss mit den deklarierten Registerslots kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-116">The root signature referencing the shader must be compatible with the declared register slots.</span></span> <span data-ttu-id="bb3dd-117">Beispielsweise wäre der folgende Teil einer Stammsignatur mit der Verwendung von Texturslots t3 bis t6 kompatibel, da er eine Deskriptortabelle mit den Slots t0 bis t98 beschreibt.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-117">For example, the following portion of a root signature would be compatible with the use of texture slots t3 through t6, as it describes a descriptor table with slots t0 through t98.</span></span>

``` syntax
DescriptorTable( CBV(b1), SRV(t0,numDescriptors=99), CBV(b2) )
```

<span data-ttu-id="bb3dd-118">Eine Ressourcendeklaration kann ein Skalar, ein 1D-Array oder ein mehrdimensionales Array sein:</span><span class="sxs-lookup"><span data-stu-id="bb3dd-118">A resource declaration may be a scalar, a 1D array, or a multidimensional array:</span></span>

``` syntax
Texture2D<float4> tex1 : register(t3,  space0)
Texture2D<float4> tex2[4] : register(t10)
Texture2D<float4> tex3[7][5][3] : register(t20, space1)
```

<span data-ttu-id="bb3dd-119">SM5.1 verwendet dieselben Ressourcentypen und Elementtypen wie SM5.0.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-119">SM5.1 uses the same resource types and element types as SM5.0 does.</span></span> <span data-ttu-id="bb3dd-120">SM5.1-Deklarationsgrenzwerte sind flexibler und nur durch die Laufzeit-/Hardwaregrenzwerte eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-120">SM5.1 declaration limits are more flexible, and constrained only by the runtime/hardware limits.</span></span> <span data-ttu-id="bb3dd-121">Das `space` Schlüsselwort gibt an, an welchen logischen Registerraum die deklarierte Variable gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-121">The `space` keyword specifies to which logical register space the declared variable is bound.</span></span> <span data-ttu-id="bb3dd-122">Wenn das `space` Schlüsselwort ausgelassen wird, wird der Standardspeicherplatzindex von 0 implizit dem Bereich zugewiesen (sodass sich der `tex2` obige Bereich in `space0` befindet).</span><span class="sxs-lookup"><span data-stu-id="bb3dd-122">If the `space` keyword is omitted, then the default space index of 0 is implicitly assigned to the range (so the `tex2` range above resides in `space0`).</span></span> <span data-ttu-id="bb3dd-123">`register(t3,  space0)` tritt niemals ein Konflikt mit `register(t3,  space1)` oder einem Array in einem anderen Bereich auf, das t3 enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-123">`register(t3,  space0)` will never conflict with `register(t3,  space1)`, nor with any array in another space that might include t3.</span></span>

<span data-ttu-id="bb3dd-124">Eine Arrayressource kann eine unbegrenzte Größe aufweisen, die deklariert wird, indem die erste Dimension als leer angegeben wird, oder 0:</span><span class="sxs-lookup"><span data-stu-id="bb3dd-124">An array resource may have an unbounded size, which is declared by specifying the very first dimension to be empty, or 0:</span></span>

``` syntax
Texture2D<float4> tex1[] : register(t0)
```

<span data-ttu-id="bb3dd-125">Die entsprechende Deskriptortabelle kann folgende sein:</span><span class="sxs-lookup"><span data-stu-id="bb3dd-125">The matching descriptor table could be:</span></span>

``` syntax
DescriptorTable( CBV(b1), UAV(u0, numDescriptors = 4), SRV(t0, numDescriptors=unbounded)
```

<span data-ttu-id="bb3dd-126">Ein ungebundenes Array in HLSL entspricht einer festen Zahl, `numDescriptors` die mit in der Deskriptortabelle festgelegt ist, und eine feste Größe in der HLSL stimmt mit einer ungebundenen Deklaration in der Deskriptortabelle überein.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-126">An unbounded array in HLSL does match a fixed number set with `numDescriptors` in the descriptor table, and a fixed size in the HLSL does match an unbounded declaration in the descriptor table.</span></span>

<span data-ttu-id="bb3dd-127">Mehrdimensionale Arrays sind zulässig, einschließlich einer unbegrenzten Größe.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-127">Multi-dimensional arrays are allowed, including of an unbounded size.</span></span> <span data-ttu-id="bb3dd-128">Diese mehrdimensionalen Arrays werden im Registerbereich flacher.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-128">These multidimensional arrays are flattened out in register space.</span></span>

``` syntax
Texture2D<float4> tex2[3000][10] : register(t0, space0); // t0-t29999 in space0
Texture2D<float4> tex3[0][5][3] : register(t5, space1)
```

<span data-ttu-id="bb3dd-129">Das Aliasing von Ressourcenbereichen ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-129">Aliasing of resource ranges is not allowed.</span></span> <span data-ttu-id="bb3dd-130">Anders ausgedrückt: Für jeden Ressourcentyp (t, s, u, b) dürfen deklarierte Registerbereiche nicht überlappen.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-130">In other words, for each resource type (t, s, u, b), declared register ranges mustn't overlap.</span></span> <span data-ttu-id="bb3dd-131">Dies schließt auch nicht gebundene Bereiche ein.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-131">That includes unbounded ranges, too.</span></span> <span data-ttu-id="bb3dd-132">Bereiche, die in unterschiedlichen Registerräumen deklariert werden, überlappen sich nie.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-132">Ranges declared in different register spaces never overlap.</span></span> <span data-ttu-id="bb3dd-133">Beachten Sie, dass sich "unbounded" `tex2` (oben) in befindet, während sich `space0` "unbounded" `tex3` in `space1` befindet, sodass sie sich nicht überlappen.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-133">Note that unbounded `tex2` (above) resides in `space0`, while unbounded `tex3` resides in `space1`, such that they don't overlap.</span></span>

<span data-ttu-id="bb3dd-134">Der Zugriff auf Ressourcen, die als Arrays deklariert wurden, ist so einfach wie das Indizieren.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-134">Accessing resources that have been declared as arrays is as simple as indexing them.</span></span>

``` syntax
Texture2D<float4> tex1[400] : register(t3);
sampler samp[7] : register(s0);
tex1[myMaterialID].Sample(samp[samplerID], texCoords);
```

<span data-ttu-id="bb3dd-135">Es gibt eine wichtige Standardeinschränkung für die Verwendung der Indizes ( `myMaterialID` und `samplerID` im obigen Code), da sie innerhalb einer [Welle](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology)nicht variieren dürfen.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-135">There's an important default restriction on the use of the indices (`myMaterialID` and `samplerID` in the code above) in that they're not allowed to vary within a [wave](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology).</span></span> <span data-ttu-id="bb3dd-136">Selbst das Ändern des Indexes basierend auf der Instanziierung zählt als variierend.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-136">Even changing the index based on instancing counts as varying.</span></span>

<span data-ttu-id="bb3dd-137">Wenn der Index variieren muss, geben Sie den `NonUniformResourceIndex` Qualifizierer für den Index an, z. B.:</span><span class="sxs-lookup"><span data-stu-id="bb3dd-137">If varying the index is required then specify the `NonUniformResourceIndex` qualifier on the index, for example:</span></span>

``` syntax
tex1[NonUniformResourceIndex(myMaterialID)].Sample(samp[NonUniformResourceIndex(samplerID)], texCoords);
```

<span data-ttu-id="bb3dd-138">Bei einigen Hardwarekomponenten generiert die Verwendung dieses Qualifizierers zusätzlichen Code, um die Richtigkeit (einschließlich threadübergreifender) zu erzwingen, jedoch mit geringen Leistungskosten.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-138">On some hardware the use of this qualifier generates additional code to enforce correctness (including across threads) but at a minor performance cost.</span></span> <span data-ttu-id="bb3dd-139">Wenn ein Index ohne diesen Qualifizierer und innerhalb eines Zeichnens/Dispatchs geändert wird, sind die Ergebnisse nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-139">If an index is changed without this qualifier and within a draw/dispatch the results are undefined.</span></span>

## <a name="descriptor-arrays-and-texture-arrays"></a><span data-ttu-id="bb3dd-140">Deskriptorarrays und Texturarrays</span><span class="sxs-lookup"><span data-stu-id="bb3dd-140">Descriptor arrays and texture arrays</span></span>

<span data-ttu-id="bb3dd-141">Texturarrays sind seit DirectX 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-141">Texture arrays have been available since DirectX 10.</span></span> <span data-ttu-id="bb3dd-142">Texturarrays erfordern einen Deskriptor, aber alle Arrayslices müssen das gleiche Format, die gleiche Breite, Höhe und MIP-Anzahl aufweisen.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-142">Texture arrays require one descriptor, however all the array slices must share the same format, width, height and mip count.</span></span> <span data-ttu-id="bb3dd-143">Außerdem muss das Array einen zusammenhängenden Bereich im virtuellen Adressraum belegen.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-143">Also, the array must occupy a contiguous range in virtual address space.</span></span> <span data-ttu-id="bb3dd-144">Der folgende Code zeigt ein Beispiel für den Zugriff auf ein Texturarray über einen Shader.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-144">The following code shows an example of accessing a texture array from a shader.</span></span>

``` syntax
Texture2DArray<float4> myTex2DArray : register(t0); // t0
float3 myCoord(1.0f,1.4f,2.2f); // 2.2f is array index (rounded to int)
color = myTex2DArray.Sample(mySampler, myCoord);
```

<span data-ttu-id="bb3dd-145">In einem Texturarray kann der Index frei variiert werden, ohne dass Qualifizierer wie benötigt `NonUniformResourceIndex` werden.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-145">In a texture array, the index can be varied freely, without any need for qualifiers such as `NonUniformResourceIndex`.</span></span>

<span data-ttu-id="bb3dd-146">Das entsprechende Deskriptorarray wäre:</span><span class="sxs-lookup"><span data-stu-id="bb3dd-146">The equivalent descriptor array would be:</span></span>

``` syntax
Texture2D<float4> myArrayOfTex2D[] : register(t0); // t0+
float2 myCoord(1.0f, 1.4f);
color = myArrayOfTex2D[2].Sample(mySampler,myCoord); // 2 is index
```

<span data-ttu-id="bb3dd-147">Beachten Sie, dass die umwendliche Verwendung eines float für den Arrayindex durch ersetzt `myArrayOfTex2D[2]` wird.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-147">Note the awkward use of a float for the array index is replaced with `myArrayOfTex2D[2]`.</span></span> <span data-ttu-id="bb3dd-148">Auch Deskriptorarrays bieten mehr Flexibilität bei den Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-148">Also descriptor arrays offer more flexibility with the dimensions.</span></span> <span data-ttu-id="bb3dd-149">Der Typ , ist dieses Beispiel, kann nicht variieren, aber Format, Breite, Höhe und MIP-Anzahl können je nach `Texture2D` Deskriptor variieren.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-149">The type, `Texture2D` is this example, cannot vary, but the format, width, height, and mip count can all vary with each descriptor.</span></span>

<span data-ttu-id="bb3dd-150">Es ist legitim, über ein Deskriptorarray von Texturarrays zu verfügen:</span><span class="sxs-lookup"><span data-stu-id="bb3dd-150">It is legitimate to have a descriptor array of texture arrays:</span></span>

``` syntax
Texture2DArray<float4> myArrayOfTex2DArrays[2] : register(t0);
```

<span data-ttu-id="bb3dd-151">Es ist nicht legitim, ein Array von -Strukturen zu deklarieren. Jede -Struktur, die Deskriptoren enthält, wird beispielsweise nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-151">It is not legitimate to declare an array of structures, each structure containing descriptors, for example the following code is not supported.</span></span>

``` syntax
struct myStruct {
    Texture2D                    a; 
    Texture2D                    b;
    ConstantBuffer<myConstants>  c;
};
myStruct foo[10000] : register(....);
```

<span data-ttu-id="bb3dd-152">Dies hätte das Speicherlayout **abcabcabc....** zugelassen, ist jedoch eine Sprachbeschränkung und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-152">This would have allowed the memory layout **abcabcabc....**, but is a language limitation and is not supported.</span></span> <span data-ttu-id="bb3dd-153">Eine unterstützte Methode wäre die folgende, obwohl das Speicherlayout in diesem Fall **aaa ist... Bbb... ...**.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-153">One supported method of doing this would be as follows, though the memory layout in this case is **aaa...bbb...ccc...**.</span></span>

``` syntax
Texture2D                     a[10000] : register(t0);
Texture2D                     b[10000] : register(t10000);
ConstantBuffer<myConstants>   c[10000] : register(b0);
```

<span data-ttu-id="bb3dd-154">Um das **Speicherlayout abcabcabc....** zu erreichen, verwenden Sie eine Deskriptortabelle ohne Verwendung der `myStruct` -Struktur.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-154">To achieve the **abcabcabc....** memory layout, use a descriptor table without use of the `myStruct` structure.</span></span>

## <a name="resource-aliasing"></a><span data-ttu-id="bb3dd-155">Ressourcenaliasing</span><span class="sxs-lookup"><span data-stu-id="bb3dd-155">Resource aliasing</span></span>

<span data-ttu-id="bb3dd-156">Die in den HLSL-Shadern angegebenen Ressourcenbereiche sind logische Bereiche.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-156">The resource ranges specified in the HLSL shaders are logical ranges.</span></span> <span data-ttu-id="bb3dd-157">Sie werden zur Laufzeit über den Stammsignaturmechanismus an konkrete Heapbereiche gebunden.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-157">They are be bound to concrete heap ranges at runtime via the root signature mechanism.</span></span> <span data-ttu-id="bb3dd-158">Normalerweise wird ein logischer Bereich einem Heapbereich zuordnungen, der sich nicht mit anderen Heapbereichen überschneidet.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-158">Normally, a logical range maps to a heap range that does not overlap with other heap ranges.</span></span> <span data-ttu-id="bb3dd-159">Der Stammsignaturmechanismus ermöglicht es jedoch, Heapbereiche kompatibler Typen mit Aliasen (Überlappungen) zu überlappen.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-159">However, the root signature mechanism makes it possible to alias (overlap) heap ranges of compatible types.</span></span> <span data-ttu-id="bb3dd-160">Beispielsweise können die Bereiche und aus dem obigen Beispiel dem gleichen (oder überlappenden) Heapbereich zugeordnet werden, was den Effekt hat, dass Texturen im `tex2` `tex3` HLSL-Programm aliasing werden.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-160">For example, `tex2` and `tex3` ranges from the above example may be mapped to the same (or overlapping) heap range, which has the effect of aliasing textures in the HLSL program.</span></span> <span data-ttu-id="bb3dd-161">Wenn ein solches Aliasing gewünscht ist, muss der Shader mit der OPTION D3D10 SHADER RESOURCES MAY ALIAS kompiliert \_ \_ \_ \_ werden, die mit der Option */res \_ may \_ alias* für das [Effect-Compiler Tool](../direct3dtools/fxc.md) (FXC) festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-161">If such aliasing is desired, the shader must be compiled with D3D10\_SHADER\_RESOURCES\_MAY\_ALIAS option, which is set by using the */res\_may\_alias* option for the [Effect-Compiler Tool](../direct3dtools/fxc.md) (FXC).</span></span> <span data-ttu-id="bb3dd-162">Die Option bewirkt, dass der Compiler richtigen Code erzeugt, indem bestimmte Lade-/Speicheroptimierungen unter der Annahme verhindert werden, dass Ressourcen alias verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-162">The option makes the compiler produce correct code by preventing certain load/store optimizations under the assumption that resources may alias.</span></span>

## <a name="divergence-and-derivatives"></a><span data-ttu-id="bb3dd-163">Abweichungen und Ableitungen</span><span class="sxs-lookup"><span data-stu-id="bb3dd-163">Divergence and derivatives</span></span>

<span data-ttu-id="bb3dd-164">SM5.1 erzwingt keine Einschränkungen für den Ressourcenindex. Das heißt, ` tex2[idx].Sample(…)` der Index-IDX kann eine Literalkonstante, eine Cbufferkonstante oder ein interpolierter Wert sein.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-164">SM5.1 does not impose limitations on the resource index; i.e.,` tex2[idx].Sample(…)` – the index idx can be a literal constant, a cbuffer constant, or an interpolated value.</span></span> <span data-ttu-id="bb3dd-165">Das Programmiermodell bietet zwar so große Flexibilität, aber es gibt Probleme, die Sie beachten sollten:</span><span class="sxs-lookup"><span data-stu-id="bb3dd-165">While the programming model provides such great flexibility, there are issues to be aware of:</span></span>

-   <span data-ttu-id="bb3dd-166">Wenn der Index auf einem Quader abweicht, sind die hardwareerschlossene Ableitung und abgeleitete Mengen wie LOD möglicherweise nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-166">If index diverges across a quad, the hardware-computed derivative and derived quantities such as LOD may be undefined.</span></span> <span data-ttu-id="bb3dd-167">Der HLSL-Compiler versucht in diesem Fall, eine Warnung auszugeben, verhindert jedoch nicht die Kompilierung eines Shaders.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-167">The HLSL compiler makes the best effort to issue a warning in this case, but will not prevent a shader from compiling.</span></span> <span data-ttu-id="bb3dd-168">Dieses Verhalten ähnelt dem Berechnen von Ableitungen bei der ablaufweisen Ablaufsteuerung.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-168">This behavior is similar to computing derivatives in divergent control flow.</span></span>
-   <span data-ttu-id="bb3dd-169">Wenn der Ressourcenindex uneinheitlich ist, verringert sich die Leistung im Vergleich zum Fall eines einheitlichen Indexes, da die Hardware Vorgänge für mehrere Ressourcen ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-169">If the resource index is divergent, the performance is diminished compared to the case of a uniform index, because the hardware needs to perform operations on several resources.</span></span> <span data-ttu-id="bb3dd-170">Ressourcenindizes, die möglicherweise unausweichlich sind, müssen mit der `NonUniformResourceIndex` -Funktion im HLSL-Code gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-170">Resource indexes that may be divergent must be marked with the `NonUniformResourceIndex` function in HLSL code.</span></span> <span data-ttu-id="bb3dd-171">Andernfalls sind Die Ergebnisse nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-171">Otherwise results are undefined.</span></span>

## <a name="uavs-in-pixel-shaders"></a><span data-ttu-id="bb3dd-172">UAVs in Pixel-Shadern</span><span class="sxs-lookup"><span data-stu-id="bb3dd-172">UAVs in pixel shaders</span></span>

<span data-ttu-id="bb3dd-173">SM5.1 erzwingt keine Einschränkungen für UAV-Bereiche in Pixel-Shadern, wie dies bei SM5.0 der Fall war.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-173">SM5.1 does not impose constraints on UAV ranges in pixel shaders as was the case for SM5.0.</span></span>

## <a name="constant-buffers"></a><span data-ttu-id="bb3dd-174">Konstantenpuffer</span><span class="sxs-lookup"><span data-stu-id="bb3dd-174">Constant Buffers</span></span>

<span data-ttu-id="bb3dd-175">Die Syntax der SM5.1-Konstantenpuffer (cbuffer) wurde von SM5.0 geändert, um Entwicklern das Indizieren konstanter Puffer zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-175">SM5.1 constant buffers (cbuffer) syntax has changed from SM5.0 to enable developers to index constant buffers.</span></span> <span data-ttu-id="bb3dd-176">Sm5.1 führt das Konstrukt "template" ein, um indizierbare Konstantenpuffer zu `ConstantBuffer` aktivieren:</span><span class="sxs-lookup"><span data-stu-id="bb3dd-176">To enable indexable constant buffers, SM5.1 introduces the `ConstantBuffer` “template” construct:</span></span>

``` syntax
struct Foo
{
    float4 a;
    int2 b;
};
ConstantBuffer<Foo> myCB1[2][3] : register(b2, space1);
ConstantBuffer<Foo> myCB2 : register(b0, space1);
```

<span data-ttu-id="bb3dd-177">Der vorangehende Code deklariert eine konstante Puffervariable `myCB1` vom Typ und der Größe `Foo` 6 sowie eine skalare konstante Puffervariable `myCB2` .</span><span class="sxs-lookup"><span data-stu-id="bb3dd-177">The preceding code declares constant buffer variable `myCB1` of type `Foo` and size 6, and a scalar, constant buffer variable `myCB2`.</span></span> <span data-ttu-id="bb3dd-178">Eine konstante Puffervariable kann jetzt im Shader wie die folgende indiziert werden:</span><span class="sxs-lookup"><span data-stu-id="bb3dd-178">A constant buffer variable can now be indexed in the shader as:</span></span>

``` syntax
myCB1[i][j].a.xyzw
myCB2.b.yy
```

<span data-ttu-id="bb3dd-179">Die Felder "a" und "b" werden nicht zu globalen Variablen, sondern müssen als Felder behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-179">Fields ‘a’ and ‘b’ do not become global variables, but rather must be treated as fields.</span></span> <span data-ttu-id="bb3dd-180">Aus Gründen der Abwärtskompatibilität unterstützt SM5.1 das alte Cbufferkonzept für skalare Cbuffer.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-180">For backward compatibility, SM5.1 supports the old cbuffer concept for scalar cbuffers.</span></span> <span data-ttu-id="bb3dd-181">Die folgende Anweisung macht "a" und "b" zu globalen, schreibgeschützten Variablen wie in SM5.0.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-181">The following statement makes ‘a’ and ‘b’ global, read-only variables as in SM5.0.</span></span> <span data-ttu-id="bb3dd-182">Ein solches Cbuffer im alten Stil kann jedoch nicht indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-182">However, such an old-style cbuffer cannot be indexable.</span></span>

``` syntax
cbuffer : register(b1)
{
    float4 a;
    int2 b;
};
```

<span data-ttu-id="bb3dd-183">Derzeit unterstützt der Shadercompiler die `ConstantBuffer` Vorlage nur für benutzerdefinierte Strukturen.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-183">Currently, the shader compiler supports the `ConstantBuffer` template for user-defined structures only.</span></span>

<span data-ttu-id="bb3dd-184">Aus Kompatibilitätsgründen kann der HLSL-Compiler automatisch Ressourcenregister für Bereiche zuweisen, die in deklariert `space0` sind.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-184">For compatibility reasons, the HLSL compiler may automatically assign resource registers for ranges declared in `space0`.</span></span> <span data-ttu-id="bb3dd-185">Wenn "space" in der register-Klausel weggelassen wird, wird der `space0` Standardwert verwendet.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-185">If ‘space’ is omitted in the register clause, the default `space0` is used.</span></span> <span data-ttu-id="bb3dd-186">Der Compiler verwendet die Heuristik first-fits, um die Register zu zuweisen.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-186">The compiler uses the first-hole-fits heuristic to assign the registers.</span></span> <span data-ttu-id="bb3dd-187">Die Zuweisung kann über die Reflektions-API abgerufen  werden, die erweitert wurde, um das Feld Space für den Raum hinzuzufügen, während das *BindPoint-Feld* die untere Grenze des Ressourcenregisterbereichs angibt.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-187">The assignment can be retrieved via the reflection API, which has been extended to add the *Space* field for space, while the *BindPoint* field indicates the lower bound of the resource register range.</span></span>

## <a name="bytecode-changes-in-sm51"></a><span data-ttu-id="bb3dd-188">Bytecodeänderungen in SM5.1</span><span class="sxs-lookup"><span data-stu-id="bb3dd-188">Bytecode changes in SM5.1</span></span>

<span data-ttu-id="bb3dd-189">SM5.1 ändert, wie Ressourcenregister deklariert und in anweisungen referenziert werden.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-189">SM5.1 changes how resource registers are declared and referenced in instructions.</span></span> <span data-ttu-id="bb3dd-190">Die Syntax umfasst das Deklarieren einer Registervariablen, ähnlich wie bei Gruppen-Shared Memory-Registern:</span><span class="sxs-lookup"><span data-stu-id="bb3dd-190">The syntax involves declaring a register “variable”, similar to how it is done for group shared memory registers:</span></span>

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

<span data-ttu-id="bb3dd-191">Dadurch wird die Disassemblierung für:</span><span class="sxs-lookup"><span data-stu-id="bb3dd-191">This will disassemble to:</span></span>

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

<span data-ttu-id="bb3dd-192">Jeder Shaderressourcenbereich verfügt jetzt über eine ID (einen Namen), die für den Shader-Bytecode eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-192">Each shader resource range now has an ID (a name) that is unique to the shader bytecode.</span></span> <span data-ttu-id="bb3dd-193">Beispielsweise wird das Texturarray tex1 (t10) im Shader-Bytecode zu "T1".</span><span class="sxs-lookup"><span data-stu-id="bb3dd-193">For example, tex1 (t10) texture array becomes ‘T1’ in the shader bytecode.</span></span> <span data-ttu-id="bb3dd-194">Die Angabe eindeutiger IDs für jeden Ressourcenbereich ermöglicht zwei Dinge:</span><span class="sxs-lookup"><span data-stu-id="bb3dd-194">Giving unique IDs to each resource range allows two things:</span></span>

-   <span data-ttu-id="bb3dd-195">Identifizieren Sie eindeutig, welcher Ressourcenbereich (siehe dcl resource texture2d) in einer Anweisung indiziert wird \_ \_ (siehe Beispielanweisung).</span><span class="sxs-lookup"><span data-stu-id="bb3dd-195">Unambiguously identify which resource range (see dcl\_resource\_texture2d) is being indexed in an instruction (see sample instruction).</span></span>
-   <span data-ttu-id="bb3dd-196">Anfügen einer Gruppe von Attributen an die Deklaration, z. B. Elementtyp, Stridegröße, Rasterbetriebsmodus usw.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-196">Attaching a set of attributes to the declaration, e.g., element type, stride size, raster operation mode, etc.</span></span>

<span data-ttu-id="bb3dd-197">Beachten Sie, dass die ID des Bereichs nicht mit der HLSL-Untergrenze-Deklaration verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-197">Note that the ID of the range is not related to the HLSL lower bound declaration.</span></span>

<span data-ttu-id="bb3dd-198">Die Reihenfolge der Reflektionsressourcenbindungen (auflistung oben) und anweisungen für die Shaderdeklaration (dcl) ist identisch, um die Übereinstimmung zwischen \_ \* HLSL-Variablen und Bytecode-IDs zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-198">The order of reflection resource bindings (listing at the top) and shader declaration instructions (dcl\_\*) is the same to aid in identifying the correspondence between HLSL variables and bytecode IDs.</span></span>

<span data-ttu-id="bb3dd-199">Jede Deklarationsanweisung in SM5.1 verwendet einen 3D-Operanden, um die Bereichs-ID, die untere und die obere Grenze zu definieren.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-199">Each declaration instruction in SM5.1 uses a 3D operand to define: range ID, lower and upper bounds.</span></span> <span data-ttu-id="bb3dd-200">Ein zusätzliches Token wird ausgegeben, um den Registerbereich anzugeben.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-200">An additional token is emitted to specify the register space.</span></span> <span data-ttu-id="bb3dd-201">Es können auch andere Token ausgegeben werden, um zusätzliche Eigenschaften des Bereichs zu vermitteln, z. B. gibt die Cbuffer- oder structured buffer declaration-Anweisung die Größe des Cbuffers oder der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-201">Other tokens may be emitted as well to convey additional properties of the range, e.g., cbuffer or structured buffer declaration instruction emits the size of the cbuffer or structure.</span></span> <span data-ttu-id="bb3dd-202">Die genauen Details der Codierung finden Sie unter d3d12TokenizedProgramFormat.h und **D3D10ShaderBinary::CShaderCodeParser**.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-202">The exact details of encoding can be found in d3d12TokenizedProgramFormat.h and **D3D10ShaderBinary::CShaderCodeParser**.</span></span>

<span data-ttu-id="bb3dd-203">SM5.1-Anweisungen geben keine zusätzlichen Ressourcenoperndeninformationen als Teil der Anweisung aus (wie in SM5.0).</span><span class="sxs-lookup"><span data-stu-id="bb3dd-203">SM5.1 instructions will not emit additional resource operand information as part of the instruction (as in SM5.0).</span></span> <span data-ttu-id="bb3dd-204">Diese Informationen sind jetzt in den Deklarationsanweisungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-204">This information is now in the declaration instructions.</span></span> <span data-ttu-id="bb3dd-205">In SM5.0 erforderten Anweisungen zum Indizieren von Ressourcen, dass Ressourcenattribute in erweiterten Opcodetoken beschrieben werden mussten, da die Indizierung die Zuordnung zur Deklaration verschleierte.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-205">In SM5.0, instructions indexing resources required resource attributes to be described in extended opcode tokens, since indexing obfuscated the association to the declaration.</span></span> <span data-ttu-id="bb3dd-206">In SM5.1 ist jede ID (z.B. "t1") eindeutig einer einzelnen Deklaration zugeordnet, die die erforderlichen Ressourceninformationen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-206">In SM5.1, each ID (such as ‘t1’) is unambiguously associated with a single declaration that describes the required resource information.</span></span> <span data-ttu-id="bb3dd-207">Daher werden die erweiterten Opcodetoken, die in Anweisungen zum Beschreiben von Ressourceninformationen verwendet werden, nicht mehr ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-207">Therefore, the extended opcode tokens used on instructions to describe resource information are no longer emitted.</span></span>

<span data-ttu-id="bb3dd-208">In Anweisungen ohne Deklaration ist ein Ressourcenopernd für Sampler, SRVs und UAVs ein 2D-Operand.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-208">In non-declaration instructions, a resource operand for samplers, SRVs, and UAVs is a 2D operand.</span></span> <span data-ttu-id="bb3dd-209">Der erste Index ist eine Literalkonstante, die die Bereichs-ID angibt.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-209">The first index is a literal constant that specifies the range ID.</span></span> <span data-ttu-id="bb3dd-210">Der zweite Index stellt den linearisierten Wert des Indexes dar.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-210">The second index represents the linearized value of the index.</span></span> <span data-ttu-id="bb3dd-211">Der Wert wird relativ zum Anfang des entsprechenden Registerraums (nicht relativ zum Anfang des logischen Bereichs) berechnet, um eine bessere Korrelation mit der Stammsignatur zu erreichen und die Treibercompilerlast durch das Anpassen des Indexes zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-211">The value is computed relative to the beginning of the corresponding register space (not relative to the beginning of the logical range) to better correlate with the root signature and to reduce the driver compiler burden of adjusting the index.</span></span>

<span data-ttu-id="bb3dd-212">Ein Ressourcenopernd für CBVs ist ein 3D-Operand, der Folgendes enthält: Literal-ID des Bereichs, Index des Konstantenpuffers, Offset in die jeweilige Instanz des konstanten Puffers.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-212">A resource operand for CBVs is a 3D operand, containing: literal ID of the range, index of the constant buffer, offset into the particular instance of constant buffer.</span></span>

## <a name="example-hlsl-declarations"></a><span data-ttu-id="bb3dd-213">HLSL-Beispieldeklarationen</span><span class="sxs-lookup"><span data-stu-id="bb3dd-213">Example HLSL Declarations</span></span>

<span data-ttu-id="bb3dd-214">HLSL-Programme müssen nichts über Stammsignaturen wissen.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-214">HLSL programs do not need to know anything about root signatures.</span></span> <span data-ttu-id="bb3dd-215">Sie können Bindungen dem virtuellen "Register"-Bindungsbereich zuweisen, t \# für SRVs, u \# für UAVs, b \# für CBVs, s \# für Sampler oder auf den Compiler, um Zuweisungen zu wählen (und anschließend die resultierenden Zuordnungen mithilfe von Shaderreflektion abzufragen).</span><span class="sxs-lookup"><span data-stu-id="bb3dd-215">They can assign bindings to the virtual “register” binding space, t\# for SRVs, u\# for UAVs, b\# for CBVs, s\# for samplers, or rely on the compiler to pick assignments (and query the resulting mappings using shader reflection afterwards).</span></span> <span data-ttu-id="bb3dd-216">Die Stammsignatur ordnet Deskriptortabellen, Stammdeskriptoren und Stammkonstanten diesem virtuellen Registerbereich zu.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-216">The root signature maps descriptor tables, root descriptors, and root constants to this virtual register space.</span></span>

<span data-ttu-id="bb3dd-217">Im Folgenden finden Sie einige Beispieldeklarationen, die ein HLSL-Shader möglicherweise hat.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-217">The following are some example declarations an HLSL shader might have.</span></span> <span data-ttu-id="bb3dd-218">Beachten Sie, dass es keine Verweise auf Stammsignaturen oder Deskriptortabellen gibt.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-218">Note that there are no references to root signatures or descriptor tables.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="bb3dd-219">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bb3dd-219">Related topics</span></span>

* [<span data-ttu-id="bb3dd-220">Dynamische Indizierung mit HLSL 5.1</span><span class="sxs-lookup"><span data-stu-id="bb3dd-220">Dynamic Indexing using HLSL 5.1</span></span>](dynamic-indexing-using-hlsl-5-1.md)
* [<span data-ttu-id="bb3dd-221">Effect-Compiler-Tool</span><span class="sxs-lookup"><span data-stu-id="bb3dd-221">Effect-Compiler Tool</span></span>](../direct3dtools/fxc.md)
* [<span data-ttu-id="bb3dd-222">HLSL-Shadermodell 5.1-Features für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="bb3dd-222">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](../direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12.md)
* [<span data-ttu-id="bb3dd-223">Geordnete Rasterizeransichten</span><span class="sxs-lookup"><span data-stu-id="bb3dd-223">Rasterizer Ordered Views</span></span>](rasterizer-order-views.md)
* [<span data-ttu-id="bb3dd-224">Ressourcenbindung</span><span class="sxs-lookup"><span data-stu-id="bb3dd-224">Resource Binding</span></span>](resource-binding.md)
* [<span data-ttu-id="bb3dd-225">Stammsignaturen</span><span class="sxs-lookup"><span data-stu-id="bb3dd-225">Root Signatures</span></span>](root-signatures.md)
* [<span data-ttu-id="bb3dd-226">Shadermodell 5.1</span><span class="sxs-lookup"><span data-stu-id="bb3dd-226">Shader Model 5.1</span></span>](../direct3dhlsl/shader-model-5-1.md)
* [<span data-ttu-id="bb3dd-227">Von Shader festgelegter Schablonenreferenzwert</span><span class="sxs-lookup"><span data-stu-id="bb3dd-227">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)
* [<span data-ttu-id="bb3dd-228">Festlegen von Stammsignaturen in HLSL</span><span class="sxs-lookup"><span data-stu-id="bb3dd-228">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)