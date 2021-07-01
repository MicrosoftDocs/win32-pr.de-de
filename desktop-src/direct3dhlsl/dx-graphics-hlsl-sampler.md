---
title: Samplertyp
description: Verwenden Sie die folgende Syntax, um den Samplerzustand sowie den Samplervergleichsstatus zu deklarieren.
ms.assetid: 6534d343-d724-46e5-b300-2a29124a1a28
keywords:
- Samplertyp HLSL
topic_type:
- apiref
api_name:
- Sampler Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0206f7030d3b3a05570e74273d9510bb9c2592c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119575"
---
# <a name="sampler-type"></a>Samplertyp

Verwenden Sie die folgende Syntax, um den Samplerzustand sowie den Samplervergleichsstatus zu deklarieren.



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
<td>sampler <em>Name</em>  =  <em>SamplerType</em>{ Texture = <<em>texture_variable</em> > ;   [<em>state_name = state_value;</em>]   ... };</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Die Syntax für einen Sampler in Direct3D 10 und höher wurde geringfügig geändert, um Texturobjekte und Samplerarrays zu unterstützen.</p>

<table>
<tbody>
<tr class="odd">
<td><em>SamplerType Name[Index]</em>{ [<em>state_name = state_value;</em>]   ... };</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="sampler"></span><span id="SAMPLER"></span>Sampler
</dt> <dd>

Nur Direct3D 9. Erforderliches Schlüsselwort.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Namen*
</dt> <dd>

ASCII-Zeichenfolge, die den Namen der Samplervariablen eindeutig identifiziert.

</dd> <dt>

<span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[Index\]*
</dt> <dd>

Nur Direct3D 10 und höher. Optionale Arraygröße; eine positive ganze Zahl größer oder gleich 1.

</dd> <dt>

<span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*SamplerType*
</dt> <dd>

\[in Der Samplertyp, der einer der folgenden \] ist: *sampler*, *sampler1D*, *sampler2D*, *sampler3D*, *samplerCUBE*, *sampler \_ state*, *SamplerState*.

Unterschiede zwischen Direct3D 9 und Direct3D 10 und höher:

- Direct3D 10 und höher unterstützt einen zusätzlichen Samplertyp: *SamplerComparisonState*.



 

</dd> <dt>

<span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*Textur* = <*\_ Texturvariablen>;*
</dt> <dd>

Nur Direct3D 9. Eine Texturvariable. Das *Texture-Schlüsselwort* ist auf der linken Seite erforderlich. Der Variablenname gehört auf der rechten Seite des Ausdrucks innerhalb der eckigen Klammern.

</dd> <dt>

<span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*state \_ name = state \_ value*
</dt> <dd>

\[unter \] Optionale Zustandszuweisung(en). Die linke Seite einer Zuweisung ist ein Zustandsname, die rechte Seite der Zustandswert. Alle Zustandszuweisungen müssen innerhalb eines Anweisungsblocks (in eckigen Klammern) angezeigt werden. Jede Anweisung wird durch ein Semikolon getrennt. In der folgenden Tabelle sind die möglichen Statusnamen aufgeführt.


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



Die rechte Seite jedes Ausdrucks ist der Wert, der jedem Zustand zugewiesen ist. Die möglichen Statuswerte für Direct3D 11 finden Sie in der [**D3D11 \_ SAMPLER \_ DESC-Struktur.**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) Zwischen den Zustandsnamen und den Membern der -Struktur besteht eine 1:1-Beziehung. Siehe folgendes Beispiel.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Effekt implementieren, ist der Samplerzustand einer von mehreren Zustandstypen, die Sie möglicherweise in der Pipeline für das Rendering einrichten müssen. Eine Liste aller möglichen Zustände, die Sie in einem Effekt festlegen können, finden Sie unter:

-   Direct3D 10 verwendet [Zustandsgruppen.](/windows/desktop/direct3d10/d3d10-effect-states)
-   Direct3D 9 verwendet einzelne [Zustände.](/windows/desktop/direct3d9/effect-states)

## <a name="example"></a>Beispiel



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 10:<br/> Hier ist ein Teilbeispiel eines Direct3D 9-Samplers aus <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">dem BasicHLSL-Beispiel</a>.<br/> <span data-codelanguage=""></span>
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

<p>Hier ist ein Teilbeispiel eines Direct3D 10-Samplers aus <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">dem BasicHLSL10-Beispiel</a>.</p>
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



 

Hier ist ein teilielles Beispiel für das Deklarieren des Samplervergleichszustands und das Aufrufen eines Vergleichss samplers in Direct3D 10.


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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Datentypen (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

