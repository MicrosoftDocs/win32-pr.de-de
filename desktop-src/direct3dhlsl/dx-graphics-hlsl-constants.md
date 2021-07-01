---
title: Shaderkonstanten (HLSL)
description: In ShaderModell 4 werden Shaderkonst constants in mindestens einer Pufferressourcen im Arbeitsspeicher gespeichert.
ms.assetid: 89fe874a-8009-4901-bebe-2d9e45f894bb
keywords:
- cbuffer
- tbuffer
- konstanter Puffer
- Texturpuffer
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f314be4b8da98ff80bd7404c270479855e13fb6e
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129959"
---
# <a name="shader-constants-hlsl"></a><span data-ttu-id="a9186-107">Shaderkonstanten (HLSL)</span><span class="sxs-lookup"><span data-stu-id="a9186-107">Shader Constants (HLSL)</span></span>

<span data-ttu-id="a9186-108">In ShaderModell 4 werden Shaderkonst constants in mindestens einer Pufferressourcen im Arbeitsspeicher gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a9186-108">In Shader Model 4, shader constants are stored in one or more buffer resources in memory.</span></span> <span data-ttu-id="a9186-109">Sie können in zwei Arten von Puffern organisiert werden: Konstante Puffer (Cbuffer) und Texturpuffer (Tbuffer).</span><span class="sxs-lookup"><span data-stu-id="a9186-109">They can be organized into two types of buffers: constant buffers (cbuffers) and texture buffers (tbuffers).</span></span> <span data-ttu-id="a9186-110">Konstante Puffer sind für die Verwendung konstanter Variablen optimiert, was sich durch den Zugriff mit geringerer Latenz und eine häufigere Aktualisierung der CPU ausdingt.</span><span class="sxs-lookup"><span data-stu-id="a9186-110">Constant buffers are optimized for constant-variable usage, which is characterized by lower-latency access and more frequent update from the CPU.</span></span> <span data-ttu-id="a9186-111">Aus diesem Grund gelten zusätzliche Größen-, Layout- und Zugriffseinschränkungen für diese Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="a9186-111">For this reason, additional size, layout, and access restrictions apply to these resources.</span></span> <span data-ttu-id="a9186-112">Der Zugriff auf Texturpuffer erfolgt wie Texturen und verbessert die Leistung für beliebig indizierte Daten.</span><span class="sxs-lookup"><span data-stu-id="a9186-112">Texture buffers are accessed like textures and perform better for arbitrarily indexed data.</span></span> <span data-ttu-id="a9186-113">Unabhängig davon, welche Art von Ressource Sie verwenden, gibt es keine Beschränkung für die Anzahl konstanter Puffer oder Texturpuffer, die eine Anwendung erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="a9186-113">Regardless of which type of resource you use, there is no limit to the number of constant buffers or texture buffers an application can create.</span></span>

<span data-ttu-id="a9186-114">Das Deklarieren eines konstanten Puffers oder Texturpuffers sieht sehr ähnlich wie eine Strukturdeklaration in C aus, mit dem Hinzufügen der Schlüsselwörter **register** und **packoffset** zum manuellen Zuweisen von Registern oder Packen von Daten.</span><span class="sxs-lookup"><span data-stu-id="a9186-114">Declaring a constant buffer or a texture buffer looks very much like a structure declaration in C, with the addition of the **register** and **packoffset** keywords for manually assigning registers or packing data.</span></span>



|                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9186-115">*BufferType* \[ *Name* \] \[: **register**(b \# ) { \] *VariableDeclaration* \[ : **packoffset**(c \# .xyzw) \] ;      ... };</span><span class="sxs-lookup"><span data-stu-id="a9186-115">*BufferType* \[*Name*\] \[: **register**(b\#)\] {     *VariableDeclaration* \[: **packoffset**(c\#.xyzw)\];      ... };</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="a9186-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9186-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9186-117"><span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*</span><span class="sxs-lookup"><span data-stu-id="a9186-117"><span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*</span></span>
</dt> <dd>

<span data-ttu-id="a9186-118">\[in \] Der Puffertyp.</span><span class="sxs-lookup"><span data-stu-id="a9186-118">\[in\] The buffer type.</span></span>



| <span data-ttu-id="a9186-119">BufferType</span><span class="sxs-lookup"><span data-stu-id="a9186-119">BufferType</span></span> | <span data-ttu-id="a9186-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9186-120">Description</span></span>     |
|------------|-----------------|
| <span data-ttu-id="a9186-121">cbuffer</span><span class="sxs-lookup"><span data-stu-id="a9186-121">cbuffer</span></span>    | <span data-ttu-id="a9186-122">konstanter Puffer</span><span class="sxs-lookup"><span data-stu-id="a9186-122">constant buffer</span></span> |
| <span data-ttu-id="a9186-123">tbuffer</span><span class="sxs-lookup"><span data-stu-id="a9186-123">tbuffer</span></span>    | <span data-ttu-id="a9186-124">Texturpuffer</span><span class="sxs-lookup"><span data-stu-id="a9186-124">texture buffer</span></span>  |



 

</dd> <dt>

<span data-ttu-id="a9186-125"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Namen*</span><span class="sxs-lookup"><span data-stu-id="a9186-125"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="a9186-126">\[in \] Optional, ASCII-Zeichenfolge, die einen eindeutigen Puffernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="a9186-126">\[in\] Optional, ASCII string containing a unique buffer name.</span></span>

</dd> <dt>

<span data-ttu-id="a9186-127"><span id="register_b__"></span><span id="REGISTER_B__"></span>**register**(b \# )</span><span class="sxs-lookup"><span data-stu-id="a9186-127"><span id="register_b__"></span><span id="REGISTER_B__"></span>**register**(b\#)</span></span>
</dt> <dd>

<span data-ttu-id="a9186-128">\[im \] Optional-Schlüsselwort, das zum manuellen Packen konstanter Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a9186-128">\[in\] Optional keyword, used to manually pack constant data.</span></span> <span data-ttu-id="a9186-129">Konstanten können in einem Register nur in einem konstanten Puffer gepackt werden, wobei das Startregister durch die Registernummer ( ) angegeben *\#* wird.</span><span class="sxs-lookup"><span data-stu-id="a9186-129">Constants can be packed in a register only in a constant buffer, where the starting register is given by the register number (*\#*).</span></span>

</dd> <dt>

<span data-ttu-id="a9186-130"><span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*</span><span class="sxs-lookup"><span data-stu-id="a9186-130"><span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*</span></span>
</dt> <dd>

<span data-ttu-id="a9186-131">\[in \] Variable-Deklaration, ähnlich einer Struktur-Memberdeklaration.</span><span class="sxs-lookup"><span data-stu-id="a9186-131">\[in\] Variable declaration, similar to a structure member declaration.</span></span> <span data-ttu-id="a9186-132">Dies kann ein beliebiger HLSL-Typ oder ein Effektobjekt sein (mit Ausnahme einer Textur oder eines Samplerobjekts).</span><span class="sxs-lookup"><span data-stu-id="a9186-132">This can be any HLSL type or effect object (except a texture or a sampler object).</span></span>

</dd> <dt>

<span data-ttu-id="a9186-133"><span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c \# .xyzw)</span><span class="sxs-lookup"><span data-stu-id="a9186-133"><span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c\#.xyzw)</span></span>
</dt> <dd>

<span data-ttu-id="a9186-134">\[im \] Optional-Schlüsselwort, das zum manuellen Packen konstanter Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a9186-134">\[in\] Optional keyword, used to manually pack constant data.</span></span> <span data-ttu-id="a9186-135">Konstanten können in einem beliebigen konstanten Puffer gepackt werden, wobei die Registernummer durch ( ) angegeben *\#* wird.</span><span class="sxs-lookup"><span data-stu-id="a9186-135">Constants can be packed in any constant buffer, where the register number is given by (*\#*).</span></span> <span data-ttu-id="a9186-136">Das Packen von Unterkomponenten (mit xyzw swizzling) ist für Konstanten verfügbar, deren Größe in ein einzelnes Register passt (nicht über eine Registergrenze hinaus).</span><span class="sxs-lookup"><span data-stu-id="a9186-136">Sub-component packing (using xyzw swizzling) is available for constants whose size fit within a single register (do not cross a register boundary).</span></span> <span data-ttu-id="a9186-137">Beispielsweise konnte ein float4-Element nicht in ein einzelnes Register gepackt werden, das mit der y-Komponente beginnt, da es nicht in ein Vier-Komponenten-Register passen würde.</span><span class="sxs-lookup"><span data-stu-id="a9186-137">For instance, a float4 could not be packed in a single register starting with the y-component because it would not fit in a four-component register.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9186-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9186-138">Remarks</span></span>

<span data-ttu-id="a9186-139">Konstante Puffer verringern die Bandbreite, die zum Aktualisieren von Shaderkonstten erforderlich ist, indem shader-Konstanten gleichzeitig gruppiert und ein Commit für diese konstanten Konstanten ermöglicht wird, anstatt einzelne Aufrufe zum getrennten Commit jeder Konstante zu tätigen.</span><span class="sxs-lookup"><span data-stu-id="a9186-139">Constant buffers reduce the bandwidth required to update shader constants by allowing shader constants to be grouped together and committed at the same time rather than making individual calls to commit each constant separately.</span></span>

<span data-ttu-id="a9186-140">Ein konstanter Puffer ist eine spezialisierte Pufferressource, auf die wie ein Puffer zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="a9186-140">A constant buffer is a specialized buffer resource that is accessed like a buffer.</span></span> <span data-ttu-id="a9186-141">Jeder konstante Puffer kann bis zu 4.096 [Vektoren halten.](dx-graphics-hlsl-vector.md) Jeder Vektor enthält bis zu vier 32-Bit-Werte.</span><span class="sxs-lookup"><span data-stu-id="a9186-141">Each constant buffer can hold up to 4096 [vectors](dx-graphics-hlsl-vector.md); each vector contains up to four 32-bit values.</span></span> <span data-ttu-id="a9186-142">Sie können bis zu 14 konstante Puffer pro Pipelinephase binden (zwei zusätzliche Slots sind für die interne Verwendung reserviert).</span><span class="sxs-lookup"><span data-stu-id="a9186-142">You can bind up to 14 constant buffers per pipeline stage (2 additional slots are reserved for internal use).</span></span>

<span data-ttu-id="a9186-143">Ein Texturpuffer ist eine spezialisierte Pufferressource, auf die wie eine Textur zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="a9186-143">A texture buffer is a specialized buffer resource that is accessed like a texture.</span></span> <span data-ttu-id="a9186-144">Der Texturzugriff (im Vergleich zum Pufferzugriff) kann eine bessere Leistung für beliebig indizierte Daten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a9186-144">Texture access (as compared with buffer access) can have better performance for arbitrarily indexed data.</span></span> <span data-ttu-id="a9186-145">Sie können bis zu 128 Texturpuffer pro Pipelinephase binden.</span><span class="sxs-lookup"><span data-stu-id="a9186-145">You can bind up to 128 texture buffers per pipeline stage.</span></span>

<span data-ttu-id="a9186-146">Eine Pufferressource ist so konzipiert, dass der Mehraufwand für das Festlegen von Shaderkonst constants minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="a9186-146">A buffer resource is designed to minimize the overhead of setting shader constants.</span></span> <span data-ttu-id="a9186-147">Das Effektframework (siehe [**ID3D10Effect Interface**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) verwaltet aktualisierungskonstierte und Texturpuffer, oder Sie können die Direct3D-API verwenden, um Puffer zu aktualisieren (weitere Informationen finden Sie unter Kopieren und Zugreifen auf Ressourcendaten [(Direct3D 10).](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping)</span><span class="sxs-lookup"><span data-stu-id="a9186-147">The effect framework (see [**ID3D10Effect Interface**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) will manage updating constant and texture buffers, or you can use the Direct3D API to update buffers (see [Copying and Accessing Resource Data (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) for information).</span></span> <span data-ttu-id="a9186-148">Eine Anwendung kann auch Daten aus einem anderen Puffer (z. B. einem Renderziel oder einem Streamausgabeziel) in einen konstanten Puffer kopieren.</span><span class="sxs-lookup"><span data-stu-id="a9186-148">An application can also copy data from another buffer (such as a render target or a stream-output target) into a constant buffer.</span></span>

<span data-ttu-id="a9186-149">Weitere Informationen zur Verwendung konstanter Puffer in einer D3D10-Anwendung finden Sie unter [Ressourcentypen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) und Erstellen von Pufferressourcen [(Direct3D 10).](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating)</span><span class="sxs-lookup"><span data-stu-id="a9186-149">For more info on using constant buffers in a D3D10 application, see [Resource Types (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) and [Creating Buffer Resources (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span></span>

<span data-ttu-id="a9186-150">Weitere Informationen zur Verwendung konstanter Puffer in einer D3D11-Anwendung finden Sie unter [Introduction to Buffers in Direct3D 11 (Einführung in Puffer in Direct3D 11)](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) und [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to)(Erstellen eines konstanten Puffers).</span><span class="sxs-lookup"><span data-stu-id="a9186-150">For morel info on using constant buffers in a D3D11 application, see [Introduction to Buffers in Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) and [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span></span>

<span data-ttu-id="a9186-151">Ein konstanter Puffer erfordert nicht, [dass eine](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) Sicht an die Pipeline gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="a9186-151">A constant buffer does not require a [view](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) to be bound to the pipeline.</span></span> <span data-ttu-id="a9186-152">Ein Texturpuffer erfordert jedoch eine Ansicht und muss an einen Texturslot gebunden sein (oder bei Verwendung eines Effekts an [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) gebunden sein).</span><span class="sxs-lookup"><span data-stu-id="a9186-152">A texture buffer, however, requires a view and must be bound to a texture slot (or must be bound with [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) when using an effect).</span></span>

<span data-ttu-id="a9186-153">Es gibt zwei Möglichkeiten, Konstantendaten zu packen: die Schlüsselwörter [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) und [packoffset (DirectX HLSL).](dx-graphics-hlsl-variable-packoffset.md)</span><span class="sxs-lookup"><span data-stu-id="a9186-153">There are two ways to pack constants data: using the [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) and [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) keywords.</span></span>

<span data-ttu-id="a9186-154">Unterschiede zwischen Direct3D 9 und Direct3D 10 und 11:</span><span class="sxs-lookup"><span data-stu-id="a9186-154">Differences between Direct3D 9 and Direct3D 10 and 11:</span></span>

- <span data-ttu-id="a9186-155">Im Gegensatz zur automatischen Zuordnung von Konstanten in Direct3D 9, die keine Packung durchführen und stattdessen jede Variable einem Satz von float4-Registern zugewiesen haben, folgen HLSL-Konstantenvariablen den Füllregeln in Direct3D 10 und 11.</span><span class="sxs-lookup"><span data-stu-id="a9186-155">Unlike the auto-allocation of constants in Direct3D 9, which did not perform packing and instead assigned each variable to a set of float4 registers, HLSL constant variables follow packing rules in Direct3D 10 and 11.</span></span>



 

### <a name="organizing-constant-buffers"></a><span data-ttu-id="a9186-156">Organisieren konstanter Puffer</span><span class="sxs-lookup"><span data-stu-id="a9186-156">Organizing constant buffers</span></span>

<span data-ttu-id="a9186-157">Konstante Puffer verringern die Bandbreite, die zum Aktualisieren von Shaderkonstten erforderlich ist, indem shader-Konstanten gleichzeitig gruppiert und ein Commit für diese konstanten Konstanten ermöglicht wird, anstatt einzelne Aufrufe zum getrennten Commit jeder Konstante zu tätigen.</span><span class="sxs-lookup"><span data-stu-id="a9186-157">Constant buffers reduce the bandwidth required to update shader constants by allowing shader constants to be grouped together and committed at the same time rather than making individual calls to commit each constant separately.</span></span>

<span data-ttu-id="a9186-158">Die beste Möglichkeit zur effizienten Nutzung von Konstantenpuffern ist die Organisation von Shadervariablen in Konstantenpuffern anhand der Updatehäufigkeit.</span><span class="sxs-lookup"><span data-stu-id="a9186-158">The best way to efficiently use constant buffers is to organize shader variables into constant buffers based on their frequency of update.</span></span> <span data-ttu-id="a9186-159">Dadurch kann eine Anwendung die bandbreite minimieren, die zum Aktualisieren von Shaderkonst constants erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a9186-159">This allows an application to minimize the bandwidth required for updating shader constants.</span></span> <span data-ttu-id="a9186-160">Beispielsweise kann ein Shader zwei konstante Puffer deklarieren und die Daten in jedem basierend auf der Aktualisierungshäufigkeit organisieren: Daten, die pro Objekt aktualisiert werden müssen (z. B. eine Weltmatrix), werden in einem konstanten Puffer gruppiert, der für jedes Objekt aktualisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a9186-160">For example, a shader might declare two constant buffers and organize the data in each based on their frequency of update: data that needs to be updated on a per-object basis (like a world matrix) is grouped into a constant buffer which could be updated for each object.</span></span> <span data-ttu-id="a9186-161">Dies ist getrennt von Daten, die eine Szene charakterisieren, und wird daher wahrscheinlich viel seltener aktualisiert (wenn sich die Szene ändert).</span><span class="sxs-lookup"><span data-stu-id="a9186-161">This is separate from data that characterizes a scene and is therefore likely to be updated much less often (when the scene changes).</span></span>


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



### <a name="default-constant-buffers"></a><span data-ttu-id="a9186-162">Standardkonst constant buffers (Standardkonst constant buffers)</span><span class="sxs-lookup"><span data-stu-id="a9186-162">Default constant buffers</span></span>

<span data-ttu-id="a9186-163">Es sind zwei Standardkonst constant-Puffer verfügbar: $Global und $Param.</span><span class="sxs-lookup"><span data-stu-id="a9186-163">There are two default constant buffers available, $Global and $Param.</span></span> <span data-ttu-id="a9186-164">Variablen, die im globalen Bereich platziert werden, werden dem $Global cbuffer implizit hinzugefügt. Dabei wird die gleiche Füllmethode verwendet, die auch für cbuffers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a9186-164">Variables that are placed in the global scope are added implicitly to the $Global cbuffer, using the same packing method that is used for cbuffers.</span></span> <span data-ttu-id="a9186-165">Einheitliche Parameter in der Parameterliste einer Funktion werden im $Param angezeigt, wenn ein Shader außerhalb des Effektframework kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="a9186-165">Uniform parameters in the parameter list of a function appear in the $Param constant buffer when a shader is compiled outside of the effects framework.</span></span> <span data-ttu-id="a9186-166">Bei der Kompilierung innerhalb des Effektframework müssen alle Uniformen in Variablen auflösen, die im globalen Gültigkeitsbereich definiert sind.</span><span class="sxs-lookup"><span data-stu-id="a9186-166">When compiled inside the effects framework, all uniforms must resolve to variables defined in the global scope.</span></span>

## <a name="examples"></a><span data-ttu-id="a9186-167">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9186-167">Examples</span></span>

<span data-ttu-id="a9186-168">Hier sehen Sie ein Beispiel aus [dem Skinning10-Beispiel,](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) bei dem es sich um einen Texturpuffer handelt, der aus einem Array von Matrizen besteht.</span><span class="sxs-lookup"><span data-stu-id="a9186-168">Here is an example from [Skinning10 Sample](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) that is a texture buffer made up of an array of matrices.</span></span>


```
tbuffer tbAnimMatrices
{
    matrix g_mTexBoneWorld[MAX_BONE_MATRICES];
};
      
```



<span data-ttu-id="a9186-169">Diese Beispieldeklaration weist manuell einen konstanten Puffer zu, um bei einem bestimmten Register zu beginnen, und packt auch bestimmte Elemente nach Unterkomponenten.</span><span class="sxs-lookup"><span data-stu-id="a9186-169">This example declaration manually assigns a constant buffer to start at a particular register, and also packs particular elements by subcomponents.</span></span>


```
cbuffer MyBuffer : register(b3)
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
      
```



## <a name="related-topics"></a><span data-ttu-id="a9186-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a9186-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9186-171">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="a9186-171">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

