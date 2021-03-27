---
title: Shaderkonstanten (HLSL)
description: In Shader Model 4 werden Shader-Konstanten in mindestens einer Puffer Ressource im Arbeitsspeicher gespeichert.
ms.assetid: 89fe874a-8009-4901-bebe-2d9e45f894bb
keywords:
- cBuffer
- tBuffer
- konstanter Puffer
- Textur Puffer
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1b78da747a248bf4bb5774add1bf97f14f048c4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739432"
---
# <a name="shader-constants-hlsl"></a><span data-ttu-id="c2794-107">Shaderkonstanten (HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2794-107">Shader Constants (HLSL)</span></span>

<span data-ttu-id="c2794-108">In Shader Model 4 werden Shader-Konstanten in mindestens einer Puffer Ressource im Arbeitsspeicher gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c2794-108">In Shader Model 4, shader constants are stored in one or more buffer resources in memory.</span></span> <span data-ttu-id="c2794-109">Sie können in zwei Puffer Typen organisiert werden: Konstante Puffer (cbuffers) und Textur Puffer (tbuffers).</span><span class="sxs-lookup"><span data-stu-id="c2794-109">They can be organized into two types of buffers: constant buffers (cbuffers) and texture buffers (tbuffers).</span></span> <span data-ttu-id="c2794-110">Konstante Puffer sind für die Verwendung konstanter Variablen optimiert, die durch den Zugriff auf geringere Latenz und häufigere Updates von der CPU gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="c2794-110">Constant buffers are optimized for constant-variable usage, which is characterized by lower-latency access and more frequent update from the CPU.</span></span> <span data-ttu-id="c2794-111">Aus diesem Grund gelten für diese Ressourcen zusätzliche Größen-, Layout-und Zugriffsbeschränkungen.</span><span class="sxs-lookup"><span data-stu-id="c2794-111">For this reason, additional size, layout, and access restrictions apply to these resources.</span></span> <span data-ttu-id="c2794-112">Textur Puffer werden wie Texturen aufgerufen und erzielen bei beliebig indizierten Daten eine bessere Leistung.</span><span class="sxs-lookup"><span data-stu-id="c2794-112">Texture buffers are accessed like textures and perform better for arbitrarily indexed data.</span></span> <span data-ttu-id="c2794-113">Unabhängig davon, welchen Ressourcentyp Sie verwenden, gibt es keine Beschränkung für die Anzahl der Konstanten Puffer oder Textur Puffer, die eine Anwendung erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="c2794-113">Regardless of which type of resource you use, there is no limit to the number of constant buffers or texture buffers an application can create.</span></span>

<span data-ttu-id="c2794-114">Das Deklarieren eines konstanten Puffers oder eines Textur Puffers ähnelt einer Struktur Deklaration in C, mit dem Hinzufügen der Schlüsselwörter " **Register** " und " **packoffset** " zum manuellen Zuweisen von Registern oder Packen von Daten.</span><span class="sxs-lookup"><span data-stu-id="c2794-114">Declaring a constant buffer or a texture buffer looks very much like a structure declaration in C, with the addition of the **register** and **packoffset** keywords for manually assigning registers or packing data.</span></span>



|                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2794-115">*Buffertype* \[ *Name* \] \[: **Register**(b \# ) \] { *variabledeclaration* \[ : **packoffset**(c \# . xyzw) \] ;      ... };</span><span class="sxs-lookup"><span data-stu-id="c2794-115">*BufferType* \[*Name*\] \[: **register**(b\#)\] {     *VariableDeclaration* \[: **packoffset**(c\#.xyzw)\];      ... };</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="c2794-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2794-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2794-117"><span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*Buffertype*</span><span class="sxs-lookup"><span data-stu-id="c2794-117"><span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*</span></span>
</dt> <dd>

<span data-ttu-id="c2794-118">\[im \] Puffertyp.</span><span class="sxs-lookup"><span data-stu-id="c2794-118">\[in\] The buffer type.</span></span>



| <span data-ttu-id="c2794-119">Buffertype</span><span class="sxs-lookup"><span data-stu-id="c2794-119">BufferType</span></span> | <span data-ttu-id="c2794-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2794-120">Description</span></span>     |
|------------|-----------------|
| <span data-ttu-id="c2794-121">cBuffer</span><span class="sxs-lookup"><span data-stu-id="c2794-121">cbuffer</span></span>    | <span data-ttu-id="c2794-122">konstanter Puffer</span><span class="sxs-lookup"><span data-stu-id="c2794-122">constant buffer</span></span> |
| <span data-ttu-id="c2794-123">tBuffer</span><span class="sxs-lookup"><span data-stu-id="c2794-123">tbuffer</span></span>    | <span data-ttu-id="c2794-124">Textur Puffer</span><span class="sxs-lookup"><span data-stu-id="c2794-124">texture buffer</span></span>  |



 

</dd> <dt>

<span data-ttu-id="c2794-125"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Benennen*</span><span class="sxs-lookup"><span data-stu-id="c2794-125"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="c2794-126">\[in \] Optionaler ASCII-Zeichenfolge, die einen eindeutigen Puffer Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="c2794-126">\[in\] Optional, ASCII string containing a unique buffer name.</span></span>

</dd> <dt>

<span data-ttu-id="c2794-127"><span id="register_b__"></span><span id="REGISTER_B__"></span>**registrieren**(b \# )</span><span class="sxs-lookup"><span data-stu-id="c2794-127"><span id="register_b__"></span><span id="REGISTER_B__"></span>**register**(b\#)</span></span>
</dt> <dd>

<span data-ttu-id="c2794-128">\[im \] optionalen Schlüsselwort wird verwendet, um konstante Daten manuell zu verpacken.</span><span class="sxs-lookup"><span data-stu-id="c2794-128">\[in\] Optional keyword, used to manually pack constant data.</span></span> <span data-ttu-id="c2794-129">Konstanten können nur in einem konstanten Puffer in ein Register gepackt werden, wobei das Start Register von der Registernummer () angegeben wird *\#* .</span><span class="sxs-lookup"><span data-stu-id="c2794-129">Constants can be packed in a register only in a constant buffer, where the starting register is given by the register number (*\#*).</span></span>

</dd> <dt>

<span data-ttu-id="c2794-130"><span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*Variabledeclaration*</span><span class="sxs-lookup"><span data-stu-id="c2794-130"><span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*</span></span>
</dt> <dd>

<span data-ttu-id="c2794-131">\[in der \] Variablen Deklaration, ähnlich wie eine Strukturmember-Deklaration.</span><span class="sxs-lookup"><span data-stu-id="c2794-131">\[in\] Variable declaration, similar to a structure member declaration.</span></span> <span data-ttu-id="c2794-132">Dabei kann es sich um einen beliebigen HLSL-Typ oder ein Effekt Objekt handeln (mit Ausnahme einer Textur oder eines samplerobjekts)</span><span class="sxs-lookup"><span data-stu-id="c2794-132">This can be any HLSL type or effect object (except a texture or a sampler object).</span></span>

</dd> <dt>

<span data-ttu-id="c2794-133"><span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c \# . xyzw)</span><span class="sxs-lookup"><span data-stu-id="c2794-133"><span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c\#.xyzw)</span></span>
</dt> <dd>

<span data-ttu-id="c2794-134">\[im \] optionalen Schlüsselwort wird verwendet, um konstante Daten manuell zu verpacken.</span><span class="sxs-lookup"><span data-stu-id="c2794-134">\[in\] Optional keyword, used to manually pack constant data.</span></span> <span data-ttu-id="c2794-135">Konstanten können in jedem Konstanten Puffer verpackt werden, wobei die Registernummer durch () angegeben wird *\#* .</span><span class="sxs-lookup"><span data-stu-id="c2794-135">Constants can be packed in any constant buffer, where the register number is given by (*\#*).</span></span> <span data-ttu-id="c2794-136">Das Komprimieren von unter Komponenten (unter Verwendung von xyzw swizzling) ist für Konstanten verfügbar, deren Größe in ein einzelnes Register passt (keine Register Grenze überschreiten).</span><span class="sxs-lookup"><span data-stu-id="c2794-136">Sub-component packing (using xyzw swizzling) is available for constants whose size fit within a single register (do not cross a register boundary).</span></span> <span data-ttu-id="c2794-137">Beispielsweise konnte ein float4 nicht in einem einzelnen Register gepackt werden, beginnend mit der y-Komponente, da es nicht in ein vier-Komponenten-Register passt.</span><span class="sxs-lookup"><span data-stu-id="c2794-137">For instance, a float4 could not be packed in a single register starting with the y-component because it would not fit in a four-component register.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2794-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2794-138">Remarks</span></span>

<span data-ttu-id="c2794-139">Konstantenpuffer reduzieren die erforderliche Bandbreite, um shaderkonstanten zu aktualisieren, indem Sie zulassen, dass Shader-Konstanten gleichzeitig gruppiert und ein Commit ausgeführt werden, anstatt einzelne Aufrufe zum separaten Commit der einzelnen Konstanten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c2794-139">Constant buffers reduce the bandwidth required to update shader constants by allowing shader constants to be grouped together and committed at the same time rather than making individual calls to commit each constant separately.</span></span>

<span data-ttu-id="c2794-140">Ein konstanter Puffer ist eine spezialisierte Puffer Ressource, auf die wie ein Puffer zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="c2794-140">A constant buffer is a specialized buffer resource that is accessed like a buffer.</span></span> <span data-ttu-id="c2794-141">Jeder Konstante Puffer kann bis zu 4096 [Vektoren](dx-graphics-hlsl-vector.md)enthalten. Jeder Vektor enthält bis zu 4 32-Bit-Werte.</span><span class="sxs-lookup"><span data-stu-id="c2794-141">Each constant buffer can hold up to 4096 [vectors](dx-graphics-hlsl-vector.md); each vector contains up to four 32-bit values.</span></span> <span data-ttu-id="c2794-142">Sie können bis zu 14 Konstante Puffer pro Pipeline-Stufe binden (2 zusätzliche Slots sind für die interne Verwendung reserviert).</span><span class="sxs-lookup"><span data-stu-id="c2794-142">You can bind up to 14 constant buffers per pipeline stage (2 additional slots are reserved for internal use).</span></span>

<span data-ttu-id="c2794-143">Ein Textur Puffer ist eine spezialisierte Puffer Ressource, auf die wie eine Textur zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="c2794-143">A texture buffer is a specialized buffer resource that is accessed like a texture.</span></span> <span data-ttu-id="c2794-144">Der Textur Zugriff (im Vergleich zum Puffer Zugriff) kann bei beliebig indizierten Daten eine bessere Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c2794-144">Texture access (as compared with buffer access) can have better performance for arbitrarily indexed data.</span></span> <span data-ttu-id="c2794-145">Sie können bis zu 128 Textur Puffer pro Pipeline-Phase binden.</span><span class="sxs-lookup"><span data-stu-id="c2794-145">You can bind up to 128 texture buffers per pipeline stage.</span></span>

<span data-ttu-id="c2794-146">Eine Puffer Ressource ist so konzipiert, dass der Aufwand für das Festlegen von shaderkonstanten minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="c2794-146">A buffer resource is designed to minimize the overhead of setting shader constants.</span></span> <span data-ttu-id="c2794-147">Das Effect-Framework (siehe [**ID3D10Effect Interface**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) verwaltet das Aktualisieren von Konstanten und Textur Puffern, oder Sie können die Direct3D-API verwenden, um Puffer zu aktualisieren (Weitere Informationen finden Sie unter [Kopieren und Zugreifen auf Ressourcen Daten (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) ).</span><span class="sxs-lookup"><span data-stu-id="c2794-147">The effect framework (see [**ID3D10Effect Interface**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) will manage updating constant and texture buffers, or you can use the Direct3D API to update buffers (see [Copying and Accessing Resource Data (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) for information).</span></span> <span data-ttu-id="c2794-148">Eine Anwendung kann auch Daten aus einem anderen Puffer (z. b. einem Renderziel oder einem streamausgabeziel) in einen konstanten Puffer kopieren.</span><span class="sxs-lookup"><span data-stu-id="c2794-148">An application can also copy data from another buffer (such as a render target or a stream-output target) into a constant buffer.</span></span>

<span data-ttu-id="c2794-149">Weitere Informationen zur Verwendung konstanter Puffer in einer d3d10-Anwendung finden Sie unter [Ressourcentypen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) und [Erstellen von Puffer Ressourcen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span><span class="sxs-lookup"><span data-stu-id="c2794-149">For more info on using constant buffers in a D3D10 application, see [Resource Types (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) and [Creating Buffer Resources (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span></span>

<span data-ttu-id="c2794-150">Informationen zur Verwendung konstanter Puffer in einer D3D11-Anwendung finden Sie unter [Einführung in Puffer in Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) und Gewusst [wie: Erstellen eines konstanten Puffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span><span class="sxs-lookup"><span data-stu-id="c2794-150">For morel info on using constant buffers in a D3D11 application, see [Introduction to Buffers in Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) and [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span></span>

<span data-ttu-id="c2794-151">Für einen konstanten Puffer ist es nicht erforderlich, dass eine [Ansicht](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) an die Pipeline gebunden wird.</span><span class="sxs-lookup"><span data-stu-id="c2794-151">A constant buffer does not require a [view](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) to be bound to the pipeline.</span></span> <span data-ttu-id="c2794-152">Ein Textur Puffer erfordert jedoch eine Sicht, die an einen Textur Slot gebunden werden muss (oder bei Verwendung eines Effekts mit [**settexturebuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) gebunden werden muss).</span><span class="sxs-lookup"><span data-stu-id="c2794-152">A texture buffer, however, requires a view and must be bound to a texture slot (or must be bound with [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) when using an effect).</span></span>

<span data-ttu-id="c2794-153">Es gibt zwei Möglichkeiten, Konstanten Daten zu verpacken: mithilfe der Schlüsselwörter [Register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) und [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) .</span><span class="sxs-lookup"><span data-stu-id="c2794-153">There are two ways to pack constants data: using the [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) and [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) keywords.</span></span>



|                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2794-154">Unterschiede zwischen Direct3D 9 und Direct3D 10 und 11:</span><span class="sxs-lookup"><span data-stu-id="c2794-154">Differences between Direct3D 9 and Direct3D 10 and 11:</span></span><br/> <span data-ttu-id="c2794-155">Anders als bei der automatischen Zuordnung von Konstanten in Direct3D 9, die keine Komprimierung durchgeführt und stattdessen jede Variable einem Satz von float4 Registern zugewiesen haben, folgen die HLSL-Konstanten Variablen den Verpackungs Regeln in Direct3D 10 und 11.</span><span class="sxs-lookup"><span data-stu-id="c2794-155">Unlike the auto-allocation of constants in Direct3D 9, which did not perform packing and instead assigned each variable to a set of float4 registers, HLSL constant variables follow packing rules in Direct3D 10 and 11.</span></span><br/> |



 

### <a name="organizing-constant-buffers"></a><span data-ttu-id="c2794-156">Organisieren konstanter Puffer</span><span class="sxs-lookup"><span data-stu-id="c2794-156">Organizing constant buffers</span></span>

<span data-ttu-id="c2794-157">Konstantenpuffer reduzieren die erforderliche Bandbreite, um shaderkonstanten zu aktualisieren, indem Sie zulassen, dass Shader-Konstanten gleichzeitig gruppiert und ein Commit ausgeführt werden, anstatt einzelne Aufrufe zum separaten Commit der einzelnen Konstanten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c2794-157">Constant buffers reduce the bandwidth required to update shader constants by allowing shader constants to be grouped together and committed at the same time rather than making individual calls to commit each constant separately.</span></span>

<span data-ttu-id="c2794-158">Die beste Möglichkeit zur effizienten Nutzung von Konstantenpuffern ist die Organisation von Shadervariablen in Konstantenpuffern anhand der Updatehäufigkeit.</span><span class="sxs-lookup"><span data-stu-id="c2794-158">The best way to efficiently use constant buffers is to organize shader variables into constant buffers based on their frequency of update.</span></span> <span data-ttu-id="c2794-159">Dadurch kann eine Anwendung die erforderliche Bandbreite zum Aktualisieren von shaderkonstanten minimieren.</span><span class="sxs-lookup"><span data-stu-id="c2794-159">This allows an application to minimize the bandwidth required for updating shader constants.</span></span> <span data-ttu-id="c2794-160">Ein Shader kann z. b. zwei Konstante Puffer deklarieren und die Daten auf der Grundlage ihrer Aktualisierungshäufigkeit organisieren: Daten, die pro Objekt aktualisiert werden müssen (z. b. eine Weltmatrix), werden in einen konstanten Puffer gruppiert, der für jedes Objekt aktualisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c2794-160">For example, a shader might declare two constant buffers and organize the data in each based on their frequency of update: data that needs to be updated on a per-object basis (like a world matrix) is grouped into a constant buffer which could be updated for each object.</span></span> <span data-ttu-id="c2794-161">Dies ist von Daten getrennt, die eine Szene charakterisieren und daher wahrscheinlich viel seltener aktualisiert werden (wenn sich die Szene ändert).</span><span class="sxs-lookup"><span data-stu-id="c2794-161">This is separate from data that characterizes a scene and is therefore likely to be updated much less often (when the scene changes).</span></span>


```
cbuffer myObject
{       
    float4x4 matWorld;
    float3   vObjectPosition;
    int      arrayIndex;
}
 
cbuffer myScene
{
    float3   vSunPosition;
    float4x4 matView;
}
        
```



### <a name="default-constant-buffers"></a><span data-ttu-id="c2794-162">Standardmäßige Konstante Puffer</span><span class="sxs-lookup"><span data-stu-id="c2794-162">Default constant buffers</span></span>

<span data-ttu-id="c2794-163">Es sind zwei standardmäßige Konstante Puffer verfügbar, $Global und $param.</span><span class="sxs-lookup"><span data-stu-id="c2794-163">There are two default constant buffers available, $Global and $Param.</span></span> <span data-ttu-id="c2794-164">Variablen, die im globalen Gültigkeitsbereich abgelegt werden, werden dem $Global cBuffer implizit hinzugefügt. dabei wird dieselbe Verpackungsmethode verwendet, die für cbuffers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2794-164">Variables that are placed in the global scope are added implicitly to the $Global cbuffer, using the same packing method that is used for cbuffers.</span></span> <span data-ttu-id="c2794-165">Einheitliche Parameter in der Parameterliste einer Funktion werden im $param Konstanten Puffer angezeigt, wenn ein Shader außerhalb des Effects-Frameworks kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="c2794-165">Uniform parameters in the parameter list of a function appear in the $Param constant buffer when a shader is compiled outside of the effects framework.</span></span> <span data-ttu-id="c2794-166">Bei der Kompilierung innerhalb des Effects-Frameworks müssen alle Uniformen in Variablen aufgelöst werden, die im globalen Gültigkeitsbereich definiert sind.</span><span class="sxs-lookup"><span data-stu-id="c2794-166">When compiled inside the effects framework, all uniforms must resolve to variables defined in the global scope.</span></span>

## <a name="examples"></a><span data-ttu-id="c2794-167">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2794-167">Examples</span></span>

<span data-ttu-id="c2794-168">Im folgenden finden Sie ein Beispiel aus [Skinning10 Sample](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) , bei dem es sich um einen Textur Puffer handelt, der aus einem Array von Matrizen besteht.</span><span class="sxs-lookup"><span data-stu-id="c2794-168">Here is an example from [Skinning10 Sample](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) that is a texture buffer made up of an array of matrices.</span></span>


```
tbuffer tbAnimMatrices
{
    matrix g_mTexBoneWorld[MAX_BONE_MATRICES];
};
      
```



<span data-ttu-id="c2794-169">Diese Beispiel Deklaration weist manuell einen konstanten Puffer zu, um bei einem bestimmten Register zu beginnen, und packt auch bestimmte Elemente nach unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="c2794-169">This example declaration manually assigns a constant buffer to start at a particular register, and also packs particular elements by subcomponents.</span></span>


```
cbuffer MyBuffer : register(b3)
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
      
```



## <a name="related-topics"></a><span data-ttu-id="c2794-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c2794-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2794-171">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="c2794-171">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

