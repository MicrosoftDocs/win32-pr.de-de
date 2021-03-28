---
title: Samplertyp
description: Verwenden Sie die folgende Syntax, um den samplerstatus und den samplervergleichstatus zu deklarieren.
ms.assetid: 6534d343-d724-46e5-b300-2a29124a1a28
keywords:
- Sampltyp HLSL
topic_type:
- apiref
api_name:
- Sampler Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe3cd51c81617632d240dd06df5c8f61b103bf91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039016"
---
# <a name="sampler-type"></a><span data-ttu-id="52df5-104">Samplertyp</span><span class="sxs-lookup"><span data-stu-id="52df5-104">Sampler Type</span></span>

<span data-ttu-id="52df5-105">Verwenden Sie die folgende Syntax, um den samplerstatus und den samplervergleichstatus zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="52df5-105">Use the following syntax to declare sampler state as well as sampler-comparison state.</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="52df5-106">Unterschiede zwischen Direct3D 9 und Direct3D 10 und höher:</span><span class="sxs-lookup"><span data-stu-id="52df5-106">Differences between Direct3D 9 and Direct3D 10 and later:</span></span><br/> <span data-ttu-id="52df5-107">Hier ist die Syntax für einen Sampler in Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="52df5-107">Here is the syntax for a sampler in Direct3D 9.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="52df5-108"><em></em>  =  <em>samplername samplertype</em>{Texture = <<em>texture_variable</em> > ;   [<em>state_name = state_value;</em>]   ... };</span><span class="sxs-lookup"><span data-stu-id="52df5-108">sampler <em>Name</em> = <em>SamplerType</em>{   Texture = <<em>texture_variable</em>>;   [<em>state_name = state_value;</em>]   ... };</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="52df5-109">Die Syntax für einen Sampler in Direct3D 10 und höher wird leicht geändert, um Textur Objekte und samplingarrays zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="52df5-109">The syntax for a sampler in Direct3D 10 and later is changed slightly to support texture objects and sampler arrays.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="52df5-110"><em>Samplertype-Name [index]</em>{[<em>state_name = state_value;</em>]   ... };</span><span class="sxs-lookup"><span data-stu-id="52df5-110"><em>SamplerType Name[Index]</em>{   [<em>state_name = state_value;</em>]   ... };</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="parameters"></a><span data-ttu-id="52df5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="52df5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52df5-112"><span id="sampler"></span><span id="SAMPLER"></span>Sammel</span><span class="sxs-lookup"><span data-stu-id="52df5-112"><span id="sampler"></span><span id="SAMPLER"></span>sampler</span></span>
</dt> <dd>

<span data-ttu-id="52df5-113">Nur Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="52df5-113">Direct3D 9 only.</span></span> <span data-ttu-id="52df5-114">Erforderliches Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="52df5-114">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="52df5-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Benennen*</span><span class="sxs-lookup"><span data-stu-id="52df5-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="52df5-116">ASCII-Zeichenfolge, die den Namen der samplvariablen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="52df5-116">ASCII string that uniquely identifies the sampler variable name.</span></span>

</dd> <dt>

<span data-ttu-id="52df5-117"><span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[Sin\]*</span><span class="sxs-lookup"><span data-stu-id="52df5-117"><span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[Index\]*</span></span>
</dt> <dd>

<span data-ttu-id="52df5-118">Nur Direct3D 10 und höher.</span><span class="sxs-lookup"><span data-stu-id="52df5-118">Direct3D 10 and later only.</span></span> <span data-ttu-id="52df5-119">Optionale Array Größe; eine positive ganze Zahl, die größer oder gleich 1 ist.</span><span class="sxs-lookup"><span data-stu-id="52df5-119">Optional array size; a positive integer greater than or equal to 1.</span></span>

</dd> <dt>

<span data-ttu-id="52df5-120"><span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*Samplertype*</span><span class="sxs-lookup"><span data-stu-id="52df5-120"><span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*SamplerType*</span></span>
</dt> <dd>

<span data-ttu-id="52df5-121">\[im \] samplertyp, der eines der folgenden ist: *Sampler*, *sampler1D*, *sampler2D*, *sampler3D*, *samplercube*, *Sampler \_ State*, *samplerstate*.</span><span class="sxs-lookup"><span data-stu-id="52df5-121">\[in\] The sampler type, which is one of the following: *sampler*, *sampler1D*, *sampler2D*, *sampler3D*, *samplerCUBE*, *sampler\_state*, *SamplerState*.</span></span>



|                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52df5-122">Unterschiede zwischen Direct3D 9 und Direct3D 10 und höher:</span><span class="sxs-lookup"><span data-stu-id="52df5-122">Differences between Direct3D 9 and Direct3D 10 and later:</span></span><br/> <span data-ttu-id="52df5-123">Direct3D 10 und höher unterstützt einen zusätzlichen *samplertyp: samplercomparisonstate*.</span><span class="sxs-lookup"><span data-stu-id="52df5-123">Direct3D 10 and later supports one additional sampler type: *SamplerComparisonState*.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="52df5-124"><span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*Texture* = <*Textur \_ Variable*>;</span><span class="sxs-lookup"><span data-stu-id="52df5-124"><span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*Texture* = <*texture\_variable*>;</span></span>
</dt> <dd>

<span data-ttu-id="52df5-125">Nur Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="52df5-125">Direct3D 9 only.</span></span> <span data-ttu-id="52df5-126">Eine Textur Variable.</span><span class="sxs-lookup"><span data-stu-id="52df5-126">A texture variable.</span></span> <span data-ttu-id="52df5-127">Auf der linken Seite ist das *Textur* Schlüsselwort erforderlich. der Variablenname gehört auf der rechten Seite des Ausdrucks innerhalb der spitzen Klammern.</span><span class="sxs-lookup"><span data-stu-id="52df5-127">The *Texture* keyword is required on the left-hand side; the variable name belongs on the right-hand side of the expression within the angle brackets.</span></span>

</dd> <dt>

<span data-ttu-id="52df5-128"><span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*State \_ Name = State \_ value*</span><span class="sxs-lookup"><span data-stu-id="52df5-128"><span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*state\_name = state\_value*</span></span>
</dt> <dd>

<span data-ttu-id="52df5-129">\[in der \] optionalen Zustands Zuweisung (en).</span><span class="sxs-lookup"><span data-stu-id="52df5-129">\[in\] Optional state assignment(s).</span></span> <span data-ttu-id="52df5-130">Die linke Seite einer Zuweisung ist ein Zustands Name, die Rechte Seite ist der Zustandswert.</span><span class="sxs-lookup"><span data-stu-id="52df5-130">The left hand side of an assignment is a state name, the right hand side is the state value.</span></span> <span data-ttu-id="52df5-131">Alle Zustands Zuweisungen müssen innerhalb eines Anweisungsblocks (in geschweiften Klammern) vorkommen.</span><span class="sxs-lookup"><span data-stu-id="52df5-131">All state assignments must appear within a statement block (in curly brackets).</span></span> <span data-ttu-id="52df5-132">Jede-Anweisung ist durch ein Semikolon getrennt.</span><span class="sxs-lookup"><span data-stu-id="52df5-132">Each statement is separated with a semicolon.</span></span> <span data-ttu-id="52df5-133">In der folgenden Tabelle sind die möglichen Zustands Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="52df5-133">The following table lists the possible state names.</span></span>


```
// sampler state
AddressU
AddressV
AddressW
BorderColor
Filter
MaxAnisotropy
MaxLOD
MinLOD
MipLODBias

// sampler-comparison state
ComparisonFunc
```



<span data-ttu-id="52df5-134">Die Rechte Seite jedes Ausdrucks ist der Wert, der jedem Zustand zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="52df5-134">The right side of each expression is the value assigned to each state.</span></span> <span data-ttu-id="52df5-135">Die möglichen Zustands Werte für Direct3D 11 finden Sie in der [**D3D11 \_ Sampler \_**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="52df5-135">See the [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) structure for the possible state values for Direct3D 11.</span></span> <span data-ttu-id="52df5-136">Zwischen den Zustands Namen und den Membern der-Struktur besteht eine 1 bis 1-Beziehung.</span><span class="sxs-lookup"><span data-stu-id="52df5-136">There is a 1 to 1 relationship between the state names and the members of the structure.</span></span> <span data-ttu-id="52df5-137">Siehe folgendes Beispiel.</span><span class="sxs-lookup"><span data-stu-id="52df5-137">See the following example.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52df5-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52df5-138">Remarks</span></span>

<span data-ttu-id="52df5-139">Wenn Sie einen Effekt implementieren, ist der samplerstatus einer von mehreren Zustandstypen, die Sie möglicherweise in der Pipeline zum Rendern einrichten müssen.</span><span class="sxs-lookup"><span data-stu-id="52df5-139">When you implement an effect, sampler state is one of several types of state that you might need to set up in the pipeline for rendering.</span></span> <span data-ttu-id="52df5-140">Eine Liste mit allen möglichen Zuständen, die Sie in einem Effekt festlegen können, finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="52df5-140">For a list of all the possible states that you can set in an effect, see:</span></span>

-   <span data-ttu-id="52df5-141">Direct3D 10 verwendet [Statusgruppen](/windows/desktop/direct3d10/d3d10-effect-states).</span><span class="sxs-lookup"><span data-stu-id="52df5-141">Direct3D 10 uses [state groups](/windows/desktop/direct3d10/d3d10-effect-states).</span></span>
-   <span data-ttu-id="52df5-142">Direct3D 9 verwendet einzelne [Zustände](/windows/desktop/direct3d9/effect-states).</span><span class="sxs-lookup"><span data-stu-id="52df5-142">Direct3D 9 uses individual [states](/windows/desktop/direct3d9/effect-states).</span></span>

## <a name="example"></a><span data-ttu-id="52df5-143">Beispiel</span><span class="sxs-lookup"><span data-stu-id="52df5-143">Example</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="52df5-144">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="52df5-144">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="52df5-145">Im folgenden finden Sie ein Beispiel für einen Direct3D 9-Sampler aus dem <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">basichlsl</a>-Beispiel.</span><span class="sxs-lookup"><span data-stu-id="52df5-145">Here is a partial example of a Direct3D 9 sampler from <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">BasicHLSL Sample</a>.</span></span><br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>sampler MeshTextureSampler = 
sampler_state
{
    Texture = <g_MeshTexture>;
    MipFilter = LINEAR;
    MinFilter = LINEAR;
    MagFilter = LINEAR;
};</code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="52df5-146">Im folgenden finden Sie ein Beispiel für einen Direct3D 10-Sampler aus dem <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">BasicHLSL10</a>-Beispiel.</span><span class="sxs-lookup"><span data-stu-id="52df5-146">Here is a partial example of a Direct3D 10 sampler from <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">BasicHLSL10 Sample</a>.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="52df5-147">Im folgenden finden Sie ein partielles Beispiel für das Deklarieren des samplervergleichzustands und das Aufrufen eines Vergleichs Samplers in Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="52df5-147">Here is a partial example of declaring sampler-comparison state, and calling a comparison sampler in Direct3D 10.</span></span>


```
SamplerComparisonState ShadowSampler
{
   // sampler state
   Filter = COMPARISON_MIN_MAG_LINEAR_MIP_POINT;
   AddressU = MIRROR;
   AddressV = MIRROR;

   // sampler comparison state
   ComparisonFunc = LESS;
};
        
float3 vModProjUV;
  ...
float fShadow = g_ShadowMap.SampleCmpLevelZero( ShadowSampler, vModProjUV.xy, vModProjUV.z);
```



## <a name="see-also"></a><span data-ttu-id="52df5-148">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="52df5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52df5-149">Datentypen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="52df5-149">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

