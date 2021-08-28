---
description: Eine Effekttechnik wird mit der folgenden Syntax deklariert.
ms.assetid: 84f9b74d-8397-4cd5-91a0-7f910ba7b19e
title: Effect Technique Syntax (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 106abd47e1148ce30127733f113a1b43a0058f60
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625126"
---
# <a name="effect-technique-syntax-direct3d-10"></a>Effect Technique Syntax (Direct3D 10)

Eine Effekttechnik wird mit der folgenden Syntax deklariert.

technique10 *TechniqueName* \[  < *Annotations* > \]

{

<dl>  \[  < *PassName-Anmerkungen* > \]  
{
<dl> \[*SetStateGroup*; \] \[ *SetStateGroup*;\]  
...  
\[*SetStateGroup*;\]
</dl> </dd> }  
</dl>

}

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="technique10"></span><span id="TECHNIQUE10"></span>technique10
</dt> <dd>

Erforderliches Schlüsselwort.

</dd> <dt>

<span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>*TechniqueName*
</dt> <dd>

Optional. Eine ASCII-Zeichenfolge, die den Namen der Effekttechnik eindeutig identifiziert.

</dd> <dt>

<span id="Annotations"></span><span id="annotations"></span><span id="ANNOTATIONS"></span>*Anmerkungen*
</dt> <dd>

\[in \] Optional. Mindestens ein Teil der vom Benutzer bereitgestellten Informationen (Metadaten), die vom Effektsystem ignoriert werden. Informationen zur Syntax finden Sie unter [Anmerkungssyntax (Direct3D 10).](d3d10-effect-annotation-syntax.md)

</dd> <dt>

<span id="pass"></span><span id="PASS"></span>bestehen
</dt> <dd>

Erforderliches Schlüsselwort.

</dd> <dt>

<span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*PassName*
</dt> <dd>

\[in \] Optional. Eine ASCII-Zeichenfolge, die den Namen des Durchgangs eindeutig identifiziert.

</dd> <dt>

<span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*SetStateGroup*
</dt> <dd>

\[In \] Legen Sie eine oder mehrere Zustandsgruppen fest, z. B.:



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>StateGroup</th>
<th>Syntax</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Blend-Zustand</td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetBlendState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

<p>Die Argumentliste finden Sie unter [<strong>OMSetBlendState</strong>](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetblendstate).</p></td>
</tr>
<tr class="even">
<td>Tiefen-Schablonenzustand</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetDepthStencilState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>Die Argumentliste finden Sie unter <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetdepthstencilstate"><strong>OMSetDepthStencilState.</strong></a></p></td>
</tr>
<tr class="odd">
<td>Status des Rasterizers</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetRasterizerState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>Die Argumentliste finden Sie unter [<strong>RSSetState</strong>](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-rssetstate).</p></td>
</tr>
<tr class="even">
<td>Shaderzustand</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( CompileShader( shader_profile, ShaderFunction( args ) ) );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>oder</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( CompileShader( NULL ) );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>oder</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( NULL );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>SetXXXShader ist eine von <strong>SetVertexShader,</strong> <strong>SetGeometryShader</strong>oder <strong>SetPixelShader</strong> (die den API-Methoden <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader"><strong>VSSetShader,</strong></a> <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshader"><strong>GSSetShader</strong></a>und <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshader"><strong>PSSetShader</strong></a>ähneln).</p></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

Effektzustandsgruppen werden im [Effektzustand aufgelistet.](d3d10-effect-states.md)

## <a name="examples"></a>Beispiele

In diesem Beispiel (aus [dem CubeMapGS-Beispiel)](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)wird der Überblendungszustand definiert.


```
BlendState NoBlend
{ 
    BlendEnable[0] = False;
};

...

technique10
{
    pass p2 
    {
        ...
        SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    }
}
```



In diesem Beispiel wird der Rasterizerzustand so eingerichtet, dass ein Objekt im Wireframe gerendert wird.


```
RasterizerState rsWireframe { FillMode = WireFrame; };

...

technique10
{
    pass p1 
    {
        ....
        SetRasterizerState( rsWireframe );
    }
}
```



In diesem Beispiel wird der Shaderzustand (aus [dem BasicHLSL10-Beispiel )](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) , die einen Scheitelpunkt und einen Pixel-Shader verwendet.


```
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, RenderSceneVS( 1, true, true ) ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effect-Format](d3d10-effect-format.md)
</dt> </dl>

 

 



