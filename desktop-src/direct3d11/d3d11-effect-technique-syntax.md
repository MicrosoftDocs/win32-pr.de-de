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
# <a name="effect-technique-syntax-direct3d-11"></a><span data-ttu-id="4d064-113">Effekt Technik Syntax (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="4d064-113">Effect Technique Syntax (Direct3D 11)</span></span>

<span data-ttu-id="4d064-114">Eine Effekt Technik wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.</span><span class="sxs-lookup"><span data-stu-id="4d064-114">An effect technique is declared with the syntax described in this section.</span></span>

<span data-ttu-id="4d064-115">Techniqueversion *techniquename* \[ -Anmerkungen  <  > \]</span><span class="sxs-lookup"><span data-stu-id="4d064-115">TechniqueVersion *TechniqueName* \[ <*Annotations* > \]</span></span>

<span data-ttu-id="4d064-116">{</span><span class="sxs-lookup"><span data-stu-id="4d064-116">{</span></span>

<dl> <span data-ttu-id="4d064-117">Übergabe von *passname* \[ -Anmerkungen  <  > \]</span><span class="sxs-lookup"><span data-stu-id="4d064-117">pass *PassName* \[ <*Annotations* > \]</span></span>  
<span data-ttu-id="4d064-118">{</span><span class="sxs-lookup"><span data-stu-id="4d064-118">{</span></span>
<dl> <span data-ttu-id="4d064-119">\[*Setstategroup*; \] \[ *Setstategroup*;\]</span><span class="sxs-lookup"><span data-stu-id="4d064-119">\[ *SetStateGroup*; \] \[ *SetStateGroup*; \]</span></span>  
<span data-ttu-id="4d064-120">...</span><span class="sxs-lookup"><span data-stu-id="4d064-120">...</span></span>  
<span data-ttu-id="4d064-121">\[*Setstategroup*;\]</span><span class="sxs-lookup"><span data-stu-id="4d064-121">\[ *SetStateGroup*; \]</span></span>
</dl> </dd> }  
</dl>

<span data-ttu-id="4d064-122">}</span><span class="sxs-lookup"><span data-stu-id="4d064-122">}</span></span>

## <a name="parameters"></a><span data-ttu-id="4d064-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d064-123">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d064-124">Element</span><span class="sxs-lookup"><span data-stu-id="4d064-124">Item</span></span></th>
<th><span data-ttu-id="4d064-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d064-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d064-126"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>Techniqueversion</span><span class="sxs-lookup"><span data-stu-id="4d064-126"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span></span><br/></td>
<td><span data-ttu-id="4d064-127">Entweder technique10 oder technique11.</span><span class="sxs-lookup"><span data-stu-id="4d064-127">Either technique10 or technique11.</span></span> <span data-ttu-id="4d064-128">Bei Techniken, die neue Funktionen für Direct3D 11 verwenden (5_0 Shaders, bindinterfaces usw.), muss technique11 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4d064-128">Techniques which use functionality new to Direct3D 11 (5_0 shaders, BindInterfaces, etc) must use technique11.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d064-129"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span><em>Techniquename</em></span><span class="sxs-lookup"><span data-stu-id="4d064-129"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span><em>TechniqueName</em></span></span><br/></td>
<td><span data-ttu-id="4d064-130">Optional.</span><span class="sxs-lookup"><span data-stu-id="4d064-130">Optional.</span></span> <span data-ttu-id="4d064-131">Eine ASCII-Zeichenfolge, die den Namen der Effekt Technik eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4d064-131">An ASCII string that uniquely identifies the name of the effect technique.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d064-132"><span id="______________Annotations__"></span><span id="______________annotations__"></span><span id="______________ANNOTATIONS__"></span> <<em>Anmerkungen</em> ></span><span class="sxs-lookup"><span data-stu-id="4d064-132"><span id="______________Annotations__"></span><span id="______________annotations__"></span><span id="______________ANNOTATIONS__"></span> <<em>Annotations</em> ></span></span><br/></td>
<td><span data-ttu-id="4d064-133">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="4d064-133">[in] Optional.</span></span> <span data-ttu-id="4d064-134">Ein oder mehrere Teile der vom Benutzer bereitgestellten Informationen (Metadaten), die vom Effektsystem ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="4d064-134">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="4d064-135">Informationen zur Syntax finden Sie unter <a href="d3d11-effect-annotation-syntax.md">Annotation-Syntax (Direct3D 11)</a>.</span><span class="sxs-lookup"><span data-stu-id="4d064-135">For syntax, see <a href="d3d11-effect-annotation-syntax.md">Annotation Syntax (Direct3D 11)</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d064-136"><span id="pass"></span><span id="PASS"></span>Tage</span><span class="sxs-lookup"><span data-stu-id="4d064-136"><span id="pass"></span><span id="PASS"></span>pass</span></span><br/></td>
<td><span data-ttu-id="4d064-137">Erforderliches Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="4d064-137">Required keyword.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d064-138"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span><em>Passname</em></span><span class="sxs-lookup"><span data-stu-id="4d064-138"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span><em>PassName</em></span></span><br/></td>
<td><span data-ttu-id="4d064-139">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="4d064-139">[in] Optional.</span></span> <span data-ttu-id="4d064-140">Eine ASCII-Zeichenfolge, die den Namen des bestanden eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4d064-140">An ASCII string that uniquely identifies the name of the pass.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d064-141"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span><em>Setstategroup</em></span><span class="sxs-lookup"><span data-stu-id="4d064-141"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span><em>SetStateGroup</em></span></span><br/></td>
<td><span data-ttu-id="4d064-142">in Legen Sie mindestens eine Statusgruppe fest, z. b.:</span><span class="sxs-lookup"><span data-stu-id="4d064-142">[in] Set one or more state groups such as:</span></span> <br/> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d064-143">Umbenennen</span><span class="sxs-lookup"><span data-stu-id="4d064-143">StateGroup</span></span></th>
<th><span data-ttu-id="4d064-144">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d064-144">Syntax</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d064-145">Blend-Status</span><span class="sxs-lookup"><span data-stu-id="4d064-145">Blend State</span></span></td>
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

<p><span data-ttu-id="4d064-146">Die Argumentliste finden Sie unter [<strong>Verknüpfung id3d11devicecontext aus:: omsetblendstate</strong>] (/Windows/Desktop/API/D3D11/NF-d3d11-id3d11devicecontext-omsetblendstate).</span><span class="sxs-lookup"><span data-stu-id="4d064-146">See [<strong>ID3D11DeviceContext::OMSetBlendState</strong>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d064-147">Status der tiefen Schablone</span><span class="sxs-lookup"><span data-stu-id="4d064-147">Depth-stencil State</span></span></td>
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
<p><span data-ttu-id="4d064-148">Weitere Informationen finden Sie unter <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate"><strong>Verknüpfung id3d11devicecontext aus:: omsetdepthstencilstate</strong></a> für die Argumentliste.</span><span class="sxs-lookup"><span data-stu-id="4d064-148">See <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate"><strong>ID3D11DeviceContext::OMSetDepthStencilState</strong></a> for the argument list.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d064-149">Status des Rasterizers</span><span class="sxs-lookup"><span data-stu-id="4d064-149">Rasterizer State</span></span></td>
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
<p><span data-ttu-id="4d064-150">Die Argumentliste finden Sie unter [<strong>Verknüpfung id3d11devicecontext aus:: rssetstate</strong>] (/Windows/Desktop/API/D3D11/NF-d3d11-id3d11devicecontext-rssetstate).</span><span class="sxs-lookup"><span data-stu-id="4d064-150">See [<strong>ID3D11DeviceContext::RSSetState</strong>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d064-151">Shader-Status</span><span class="sxs-lookup"><span data-stu-id="4d064-151">Shader State</span></span></td>
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
<p><span data-ttu-id="4d064-152">Setxxxshader ist einer der setvertexshader, setdomainshader, sethullshader, setgeometryshader, setpixelshader oder setcomputeshader (ähnlich den API-Methoden <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader"><strong>Verknüpfung id3d11devicecontext aus:: vssetshader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader"><strong>Verknüpfung id3d11devicecontext aus::D ssetshader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader"><strong>Verknüpfung id3d11devicecontext aus:: hssetshader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetshader"><strong>Verknüpfung id3d11devicecontext aus:: gssetshader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader"><strong>Verknüpfung id3d11devicecontext aus::P ssetshader</strong></a> und <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetshader"><strong>Verknüpfung id3d11devicecontext aus:: cssetshader</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="4d064-152">SetXXXShader is one of SetVertexShader, SetDomainShader, SetHullShader, SetGeometryShader, SetPixelShader or SetComputeShader (which are similar to the API methods <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader"><strong>ID3D11DeviceContext::VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader"><strong>ID3D11DeviceContext::DSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader"><strong>ID3D11DeviceContext::HSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetshader"><strong>ID3D11DeviceContext::GSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader"><strong>ID3D11DeviceContext::PSSetShader</strong></a> and <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetshader"><strong>ID3D11DeviceContext::CSSetShader</strong></a>).</span></span></p>
<p><span data-ttu-id="4d064-153">Shader ist eine Shader-Variable, die auf vielerlei Weise abgerufen werden kann:</span><span class="sxs-lookup"><span data-stu-id="4d064-153">Shader is a shader variable, which can be obtained in many ways:</span></span></p>
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
<td><span data-ttu-id="4d064-154">Renderzielstatus</span><span class="sxs-lookup"><span data-stu-id="4d064-154">Render Target State</span></span></td>
<td><span data-ttu-id="4d064-155">Enthält einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="4d064-155">One of:</span></span>
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
<p><span data-ttu-id="4d064-156">Vergleichbar mit <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets"><strong>Verknüpfung id3d11devicecontext aus:: omabtrendertargets</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4d064-156">Similar to <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets"><strong>ID3D11DeviceContext::OMSetRenderTargets</strong></a>.</span></span></p></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="4d064-157">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d064-157">Examples</span></span>

<span data-ttu-id="4d064-158">Dieses Beispiel legt den Mischungs Zustand fest.</span><span class="sxs-lookup"><span data-stu-id="4d064-158">This example sets blending state.</span></span>


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



<span data-ttu-id="4d064-159">In diesem Beispiel wird der Status des Rasterizers zum Rendering eines Objekts in Wireframe eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="4d064-159">This example sets up the rasterizer state to render an object in wireframe.</span></span>


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



<span data-ttu-id="4d064-160">In diesem Beispiel wird der Shader-Status festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4d064-160">This example sets shader state.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="4d064-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4d064-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d064-162">Effekt Format</span><span class="sxs-lookup"><span data-stu-id="4d064-162">Effect Format</span></span>](d3d11-effect-format.md)
</dt> <dt>

[<span data-ttu-id="4d064-163">Effekt Gruppen Syntax (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="4d064-163">Effect Group Syntax (Direct3D 11)</span></span>](d3d11-effect-group-syntax.md)
</dt> <dt>

[<span data-ttu-id="4d064-164">Effekt Zustands Gruppen</span><span class="sxs-lookup"><span data-stu-id="4d064-164">Effect State Groups</span></span>](d3d11-effect-states.md)
</dt> </dl>

 

 





