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
# <a name="sampler-type"></a>Samplertyp

Verwenden Sie die folgende Syntax, um den samplerstatus und den samplervergleichstatus zu deklarieren.



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 10 und höher:<br/> Hier ist die Syntax für einen Sampler in Direct3D 9.<br/> 
<table>
<tbody>
<tr class="odd">
<td><em></em>  =  <em>samplername samplertype</em>{Texture = <<em>texture_variable</em> > ;   [<em>state_name = state_value;</em>]   ... };</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Die Syntax für einen Sampler in Direct3D 10 und höher wird leicht geändert, um Textur Objekte und samplingarrays zu unterstützen.</p>

<table>
<tbody>
<tr class="odd">
<td><em>Samplertype-Name [index]</em>{[<em>state_name = state_value;</em>]   ... };</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="sampler"></span><span id="SAMPLER"></span>Sammel
</dt> <dd>

Nur Direct3D 9. Erforderliches Schlüsselwort.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Benennen*
</dt> <dd>

ASCII-Zeichenfolge, die den Namen der samplvariablen eindeutig identifiziert.

</dd> <dt>

<span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[Sin\]*
</dt> <dd>

Nur Direct3D 10 und höher. Optionale Array Größe; eine positive ganze Zahl, die größer oder gleich 1 ist.

</dd> <dt>

<span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*Samplertype*
</dt> <dd>

\[im \] samplertyp, der eines der folgenden ist: *Sampler*, *sampler1D*, *sampler2D*, *sampler3D*, *samplercube*, *Sampler \_ State*, *samplerstate*.



|                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 10 und höher:<br/> Direct3D 10 und höher unterstützt einen zusätzlichen *samplertyp: samplercomparisonstate*.<br/> |



 

</dd> <dt>

<span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*Texture* = <*Textur \_ Variable*>;
</dt> <dd>

Nur Direct3D 9. Eine Textur Variable. Auf der linken Seite ist das *Textur* Schlüsselwort erforderlich. der Variablenname gehört auf der rechten Seite des Ausdrucks innerhalb der spitzen Klammern.

</dd> <dt>

<span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*State \_ Name = State \_ value*
</dt> <dd>

\[in der \] optionalen Zustands Zuweisung (en). Die linke Seite einer Zuweisung ist ein Zustands Name, die Rechte Seite ist der Zustandswert. Alle Zustands Zuweisungen müssen innerhalb eines Anweisungsblocks (in geschweiften Klammern) vorkommen. Jede-Anweisung ist durch ein Semikolon getrennt. In der folgenden Tabelle sind die möglichen Zustands Namen aufgelistet.


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



Die Rechte Seite jedes Ausdrucks ist der Wert, der jedem Zustand zugewiesen wird. Die möglichen Zustands Werte für Direct3D 11 finden Sie in der [**D3D11 \_ Sampler \_**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) -Struktur. Zwischen den Zustands Namen und den Membern der-Struktur besteht eine 1 bis 1-Beziehung. Siehe folgendes Beispiel.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Effekt implementieren, ist der samplerstatus einer von mehreren Zustandstypen, die Sie möglicherweise in der Pipeline zum Rendern einrichten müssen. Eine Liste mit allen möglichen Zuständen, die Sie in einem Effekt festlegen können, finden Sie unter:

-   Direct3D 10 verwendet [Statusgruppen](/windows/desktop/direct3d10/d3d10-effect-states).
-   Direct3D 9 verwendet einzelne [Zustände](/windows/desktop/direct3d9/effect-states).

## <a name="example"></a>Beispiel



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 10:<br/> Im folgenden finden Sie ein Beispiel für einen Direct3D 9-Sampler aus dem <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">basichlsl</a>-Beispiel.<br/> <span data-codelanguage=""></span>
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

<p>Im folgenden finden Sie ein Beispiel für einen Direct3D 10-Sampler aus dem <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">BasicHLSL10</a>-Beispiel.</p>
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



 

Im folgenden finden Sie ein partielles Beispiel für das Deklarieren des samplervergleichzustands und das Aufrufen eines Vergleichs Samplers in Direct3D 10.


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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Datentypen (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

