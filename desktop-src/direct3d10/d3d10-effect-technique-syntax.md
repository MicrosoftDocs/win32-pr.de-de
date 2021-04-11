---
description: Eine Effekt Technik wird mit der folgenden Syntax deklariert.
ms.assetid: 84f9b74d-8397-4cd5-91a0-7f910ba7b19e
title: Effekt Technik Syntax (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f781a0e1ea247e9ffae02e6afc9de77c8e0c6b68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126560"
---
# <a name="effect-technique-syntax-direct3d-10"></a>Effekt Technik Syntax (Direct3D 10)

Eine Effekt Technik wird mit der folgenden Syntax deklariert.

technique10 *techniquename* \[ -Anmerkungen  <  > \]

{

<dl> Übergabe von *passname* \[ -Anmerkungen  <  > \]  
{
<dl> \[*Setstategroup*; \] \[ *Setstategroup*;\]  
...  
\[*Setstategroup*;\]
</dl> </dd> }  
</dl>

}

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="technique10"></span><span id="TECHNIQUE10"></span>technique10
</dt> <dd>

Erforderliches Schlüsselwort.

</dd> <dt>

<span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>*Techniquename*
</dt> <dd>

Dies ist optional. Eine ASCII-Zeichenfolge, die den Namen der Effekt Technik eindeutig identifiziert.

</dd> <dt>

<span id="Annotations"></span><span id="annotations"></span><span id="ANNOTATIONS"></span>*Anmerkungen*
</dt> <dd>

\[in \] optional. Ein oder mehrere Teile der vom Benutzer bereitgestellten Informationen (Metadaten), die vom Effektsystem ignoriert werden. Informationen zur Syntax finden Sie unter [Annotation-Syntax (Direct3D 10)](d3d10-effect-annotation-syntax.md).

</dd> <dt>

<span id="pass"></span><span id="PASS"></span>Tage
</dt> <dd>

Erforderliches Schlüsselwort.

</dd> <dt>

<span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*Passname*
</dt> <dd>

\[in \] optional. Eine ASCII-Zeichenfolge, die den Namen des bestanden eindeutig identifiziert.

</dd> <dt>

<span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*Setstategroup*
</dt> <dd>

\[Legen Sie in mindestens \] eine Statusgruppe fest, z. b.:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Umbenennen</th>
<th>Syntax</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Blend-Status</td>
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

<p>Die Argumentliste finden Sie unter [<strong>omsetblendstate</strong>] (/Windows/Desktop/API/d3d10/NF-d3d10-id3d10device-omsetblendstate).</p></td>
</tr>
<tr class="even">
<td>Status der tiefen Schablone</td>
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
<p>Weitere Informationen finden Sie unter <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetdepthstencilstate"><strong>omsetdepthstencilstate</strong></a> für die Argumentliste.</p></td>
</tr>
<tr class="odd">
<td>Status des Rasterizers</td>
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
<p>Die Argumentliste finden Sie unter [<strong>rssetstate</strong>] (/Windows/Desktop/API/d3d10/NF-d3d10-id3d10device-rssetstate).</p></td>
</tr>
<tr class="even">
<td>Shader-Status</td>
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
<p>Setxxxshader ist eine der Methoden <strong>setvertexshader</strong>, <strong>setgeometryshader</strong>oder <strong>setpixelshader</strong> (die den API-Methoden <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader"><strong>vssetshader</strong></a>, <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshader"><strong>gssetshader</strong></a>und <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshader"><strong>pssetshader</strong></a>ähneln).</p></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

Effekt Zustands Gruppen werden im [Zustand "wirksam](d3d10-effect-states.md)" aufgelistet.

## <a name="examples"></a>Beispiele

In diesem Beispiel (aus [cubemapgs](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)-Beispiel) wird der Mischungs Zustand festgelegt.


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



In diesem Beispiel wird der Status des Rasterizers zum Rendering eines Objekts in Wireframe eingerichtet.


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



In diesem Beispiel wird der Shader-Status (aus [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)) festgelegt. , der einen Scheitelpunkt und einen Pixel-Shader verwendet.


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

[Effekt Format](d3d10-effect-format.md)
</dt> </dl>

 

 



