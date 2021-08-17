---
description: Eine Effekttechnik wird mit der folgenden Syntax deklariert.
ms.assetid: 84f9b74d-8397-4cd5-91a0-7f910ba7b19e
title: Effekttechniksyntax (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3c0ff0c0f1b5e9c1fac4cdb12aac21e42d89771c0eae89d1cd9538d0281acee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914485"
---
# <a name="effect-technique-syntax-direct3d-10"></a>Effekttechniksyntax (Direct3D 10)

Eine Effekttechnik wird mit der folgenden Syntax deklariert.

technique10 *TechniqueName-Anmerkungen* \[  <  > \]

{

<dl>  \[  < *PassName-Anmerkungen* übergeben > \]  
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

\[in \] Optional. Eine oder mehrere vom Benutzer bereitgestellte Informationen (Metadaten), die vom Effektsystem ignoriert werden. Informationen zur Syntax finden Sie unter [Anmerkungssyntax (Direct3D 10).](d3d10-effect-annotation-syntax.md)

</dd> <dt>

<span id="pass"></span><span id="PASS"></span>bestehen
</dt> <dd>

Erforderliches Schlüsselwort.

</dd> <dt>

<span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*PassName*
</dt> <dd>

\[in \] Optional. Eine ASCII-Zeichenfolge, die den Namen des Durchlaufs eindeutig identifiziert.

</dd> <dt>

<span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*SetStateGroup*
</dt> <dd>

\[in \] Legen Sie eine oder mehrere Statusgruppen fest, z. B.:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>StateGroup</th>
<th>Syntax</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Blendzustand</td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<td>Tiefenschablonenzustand</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<td>Rasterizerstatus</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<td>Shaderstatus</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<col style="width: 100%" />
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
<col style="width: 100%" />
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

Effect-Zustandsgruppen werden im [Effect-Zustand](d3d10-effect-states.md)aufgelistet.

## <a name="examples"></a>Beispiele

In diesem Beispiel (aus dem [CubeMapGS-Beispiel)](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)wird der Blendingzustand festgelegt.


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



In diesem Beispiel wird der Rasterizerzustand so eingerichtet, dass ein Objekt in Wireframe gerendert wird.


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



In diesem Beispiel wird der Shaderzustand festgelegt (aus dem [BasicHLSL10-Beispiel).](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) , der einen Scheitelpunkt und einen Pixel-Shader verwendet.


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

[Effektformat](d3d10-effect-format.md)
</dt> </dl>

 

 



