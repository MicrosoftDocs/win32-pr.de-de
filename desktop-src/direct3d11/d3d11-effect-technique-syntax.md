---
title: Effekt Technik Syntax (Direct3D 11)
description: Eine Effekt Technik wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.
ms.assetid: 54a6ebd1-a6b4-473b-bf53-a3323445de71
keywords:
- technique11, Direct3D 11-Effekt
- Pass, Direct3D 11-Effekt
- Compileshader, Direct3D 11 Auswirkung
- Setstategroup, Direct3D 11 Auswirkung
- Setblendstate, Direct3D 11 Auswirkung
- Setdepthstencilstate, Direct3D 11 Auswirkung
- "\"Tartrasterizerstate\", \"Direct3D 11\"-Effekt"
- Setvertexshader, Direct3D 11-Effekt
- Setgeometryshader, Direct3D 11-Effekt
- Setpixelshader, Direct3D 11-Effekt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73fb668f308869ef9cca5cce99d522f18a287f3c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101110"
---
# <a name="effect-technique-syntax-direct3d-11"></a>Effekt Technik Syntax (Direct3D 11)

Eine Effekt Technik wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.

Techniqueversion *techniquename* \[ -Anmerkungen  <  > \]

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



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>Techniqueversion<br/></td>
<td>Entweder technique10 oder technique11. Bei Techniken, die neue Funktionen für Direct3D 11 verwenden (5_0 Shaders, bindinterfaces usw.), muss technique11 verwendet werden.<br/></td>
</tr>
<tr class="even">
<td><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span><em>Techniquename</em><br/></td>
<td>Optional. Eine ASCII-Zeichenfolge, die den Namen der Effekt Technik eindeutig identifiziert.<br/></td>
</tr>
<tr class="odd">
<td><span id="______________Annotations__"></span><span id="______________annotations__"></span><span id="______________ANNOTATIONS__"></span> <<em>Anmerkungen</em> ><br/></td>
<td>[in] Optional. Ein oder mehrere Teile der vom Benutzer bereitgestellten Informationen (Metadaten), die vom Effektsystem ignoriert werden. Informationen zur Syntax finden Sie unter <a href="d3d11-effect-annotation-syntax.md">Annotation-Syntax (Direct3D 11)</a>.<br/></td>
</tr>
<tr class="even">
<td><span id="pass"></span><span id="PASS"></span>Tage<br/></td>
<td>Erforderliches Schlüsselwort.<br/></td>
</tr>
<tr class="odd">
<td><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span><em>Passname</em><br/></td>
<td>[in] Optional. Eine ASCII-Zeichenfolge, die den Namen des bestanden eindeutig identifiziert.<br/></td>
</tr>
<tr class="even">
<td><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span><em>Setstategroup</em><br/></td>
<td>in Legen Sie mindestens eine Statusgruppe fest, z. b.: <br/> 
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

<p>Die Argumentliste finden Sie unter [<strong>Verknüpfung id3d11devicecontext aus:: omsetblendstate</strong>] (/Windows/Desktop/API/D3D11/NF-d3d11-id3d11devicecontext-omsetblendstate).</p></td>
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
<p>Weitere Informationen finden Sie unter <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate"><strong>Verknüpfung id3d11devicecontext aus:: omsetdepthstencilstate</strong></a> für die Argumentliste.</p></td>
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
<p>Die Argumentliste finden Sie unter [<strong>Verknüpfung id3d11devicecontext aus:: rssetstate</strong>] (/Windows/Desktop/API/D3D11/NF-d3d11-id3d11devicecontext-rssetstate).</p></td>
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
<td><pre><code>SetXXXShader( Shader );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>Setxxxshader ist einer der setvertexshader, setdomainshader, sethullshader, setgeometryshader, setpixelshader oder setcomputeshader (ähnlich den API-Methoden <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader"><strong>Verknüpfung id3d11devicecontext aus:: vssetshader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader"><strong>Verknüpfung id3d11devicecontext aus::D ssetshader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader"><strong>Verknüpfung id3d11devicecontext aus:: hssetshader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetshader"><strong>Verknüpfung id3d11devicecontext aus:: gssetshader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader"><strong>Verknüpfung id3d11devicecontext aus::P ssetshader</strong></a> und <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetshader"><strong>Verknüpfung id3d11devicecontext aus:: cssetshader</strong></a>).</p>
<p>Shader ist eine Shader-Variable, die auf vielerlei Weise abgerufen werden kann:</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( CompileShader( shader_profile, ShaderFunction( args ) ) );
SetXXXShader( CompileShader( NULL ) );
SetXXXShader( NULL );
SetXXXShader( myShaderVar );
SetXXXShader( myShaderArray[2] );
SetXXXShader( myShaderArray[uIndex] );
SetGeometryShader( ConstructGSWithSO( Shader, strStream0 ) );
SetGeometryShader( ConstructGSWithSO( Shader, strStream0, strStream1, strStream2, strStream3, RastStream ) );</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>Renderzielstatus</td>
<td>Enthält einen der folgenden Werte:
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetRenderTargets( RTV0, DSV );
SetRenderTargets( RTV0, RTV1, DSV );
...
SetRenderTargets( RTV0, RTV1, RTV2, RTV3, RTV4, RTV5, RTV6, RTV7, DSV );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>Vergleichbar mit <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets"><strong>Verknüpfung id3d11devicecontext aus:: omabtrendertargets</strong></a>.</p></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a>Beispiele

Dieses Beispiel legt den Mischungs Zustand fest.


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



In diesem Beispiel wird der Shader-Status festgelegt.


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

[Effekt Format](d3d11-effect-format.md)
</dt> <dt>

[Effekt Gruppen Syntax (Direct3D 11)](d3d11-effect-group-syntax.md)
</dt> <dt>

[Effekt Zustands Gruppen](d3d11-effect-states.md)
</dt> </dl>

 

 





