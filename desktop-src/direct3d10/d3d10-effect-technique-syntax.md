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
# <a name="effect-technique-syntax-direct3d-10"></a><span data-ttu-id="1684b-103">Effekt Technik Syntax (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="1684b-103">Effect Technique Syntax (Direct3D 10)</span></span>

<span data-ttu-id="1684b-104">Eine Effekt Technik wird mit der folgenden Syntax deklariert.</span><span class="sxs-lookup"><span data-stu-id="1684b-104">An effect technique is declared with the following syntax.</span></span>

<span data-ttu-id="1684b-105">technique10 *techniquename* \[ -Anmerkungen  <  > \]</span><span class="sxs-lookup"><span data-stu-id="1684b-105">technique10 *TechniqueName* \[ <*Annotations* > \]</span></span>

<span data-ttu-id="1684b-106">{</span><span class="sxs-lookup"><span data-stu-id="1684b-106">{</span></span>

<dl> <span data-ttu-id="1684b-107">Übergabe von *passname* \[ -Anmerkungen  <  > \]</span><span class="sxs-lookup"><span data-stu-id="1684b-107">pass *PassName* \[ <*Annotations* > \]</span></span>  
<span data-ttu-id="1684b-108">{</span><span class="sxs-lookup"><span data-stu-id="1684b-108">{</span></span>
<dl> <span data-ttu-id="1684b-109">\[*Setstategroup*; \] \[ *Setstategroup*;\]</span><span class="sxs-lookup"><span data-stu-id="1684b-109">\[ *SetStateGroup*; \] \[ *SetStateGroup*; \]</span></span>  
<span data-ttu-id="1684b-110">...</span><span class="sxs-lookup"><span data-stu-id="1684b-110">...</span></span>  
<span data-ttu-id="1684b-111">\[*Setstategroup*;\]</span><span class="sxs-lookup"><span data-stu-id="1684b-111">\[ *SetStateGroup*; \]</span></span>
</dl> </dd> }  
</dl>

<span data-ttu-id="1684b-112">}</span><span class="sxs-lookup"><span data-stu-id="1684b-112">}</span></span>

## <a name="parameters"></a><span data-ttu-id="1684b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1684b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1684b-114"><span id="technique10"></span><span id="TECHNIQUE10"></span>technique10</span><span class="sxs-lookup"><span data-stu-id="1684b-114"><span id="technique10"></span><span id="TECHNIQUE10"></span>technique10</span></span>
</dt> <dd>

<span data-ttu-id="1684b-115">Erforderliches Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="1684b-115">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="1684b-116"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>*Techniquename*</span><span class="sxs-lookup"><span data-stu-id="1684b-116"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>*TechniqueName*</span></span>
</dt> <dd>

<span data-ttu-id="1684b-117">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="1684b-117">Optional.</span></span> <span data-ttu-id="1684b-118">Eine ASCII-Zeichenfolge, die den Namen der Effekt Technik eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1684b-118">An ASCII string that uniquely identifies the name of the effect technique.</span></span>

</dd> <dt>

<span data-ttu-id="1684b-119"><span id="Annotations"></span><span id="annotations"></span><span id="ANNOTATIONS"></span>*Anmerkungen*</span><span class="sxs-lookup"><span data-stu-id="1684b-119"><span id="Annotations"></span><span id="annotations"></span><span id="ANNOTATIONS"></span>*Annotations*</span></span>
</dt> <dd>

<span data-ttu-id="1684b-120">\[in \] optional.</span><span class="sxs-lookup"><span data-stu-id="1684b-120">\[in\] Optional.</span></span> <span data-ttu-id="1684b-121">Ein oder mehrere Teile der vom Benutzer bereitgestellten Informationen (Metadaten), die vom Effektsystem ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="1684b-121">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="1684b-122">Informationen zur Syntax finden Sie unter [Annotation-Syntax (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="1684b-122">For syntax, see [Annotation Syntax (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="1684b-123"><span id="pass"></span><span id="PASS"></span>Tage</span><span class="sxs-lookup"><span data-stu-id="1684b-123"><span id="pass"></span><span id="PASS"></span>pass</span></span>
</dt> <dd>

<span data-ttu-id="1684b-124">Erforderliches Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="1684b-124">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="1684b-125"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*Passname*</span><span class="sxs-lookup"><span data-stu-id="1684b-125"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*PassName*</span></span>
</dt> <dd>

<span data-ttu-id="1684b-126">\[in \] optional.</span><span class="sxs-lookup"><span data-stu-id="1684b-126">\[in\] Optional.</span></span> <span data-ttu-id="1684b-127">Eine ASCII-Zeichenfolge, die den Namen des bestanden eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1684b-127">An ASCII string that uniquely identifies the name of the pass.</span></span>

</dd> <dt>

<span data-ttu-id="1684b-128"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*Setstategroup*</span><span class="sxs-lookup"><span data-stu-id="1684b-128"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*SetStateGroup*</span></span>
</dt> <dd>

<span data-ttu-id="1684b-129">\[Legen Sie in mindestens \] eine Statusgruppe fest, z. b.:</span><span class="sxs-lookup"><span data-stu-id="1684b-129">\[in\] Set one or more state groups such as:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1684b-130">Umbenennen</span><span class="sxs-lookup"><span data-stu-id="1684b-130">StateGroup</span></span></th>
<th><span data-ttu-id="1684b-131">Syntax</span><span class="sxs-lookup"><span data-stu-id="1684b-131">Syntax</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1684b-132">Blend-Status</span><span class="sxs-lookup"><span data-stu-id="1684b-132">Blend State</span></span></td>
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

<p><span data-ttu-id="1684b-133">Die Argumentliste finden Sie unter [<strong>omsetblendstate</strong>] (/Windows/Desktop/API/d3d10/NF-d3d10-id3d10device-omsetblendstate).</span><span class="sxs-lookup"><span data-stu-id="1684b-133">See [<strong>OMSetBlendState</strong>](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetblendstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1684b-134">Status der tiefen Schablone</span><span class="sxs-lookup"><span data-stu-id="1684b-134">Depth-stencil State</span></span></td>
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
<p><span data-ttu-id="1684b-135">Weitere Informationen finden Sie unter <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetdepthstencilstate"><strong>omsetdepthstencilstate</strong></a> für die Argumentliste.</span><span class="sxs-lookup"><span data-stu-id="1684b-135">See <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetdepthstencilstate"><strong>OMSetDepthStencilState</strong></a> for the argument list.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1684b-136">Status des Rasterizers</span><span class="sxs-lookup"><span data-stu-id="1684b-136">Rasterizer State</span></span></td>
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
<p><span data-ttu-id="1684b-137">Die Argumentliste finden Sie unter [<strong>rssetstate</strong>] (/Windows/Desktop/API/d3d10/NF-d3d10-id3d10device-rssetstate).</span><span class="sxs-lookup"><span data-stu-id="1684b-137">See [<strong>RSSetState</strong>](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-rssetstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1684b-138">Shader-Status</span><span class="sxs-lookup"><span data-stu-id="1684b-138">Shader State</span></span></td>
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
<p><span data-ttu-id="1684b-139">oder</span><span class="sxs-lookup"><span data-stu-id="1684b-139">or</span></span></p>
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
<p><span data-ttu-id="1684b-140">oder</span><span class="sxs-lookup"><span data-stu-id="1684b-140">or</span></span></p>
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
<p><span data-ttu-id="1684b-141">Setxxxshader ist eine der Methoden <strong>setvertexshader</strong>, <strong>setgeometryshader</strong>oder <strong>setpixelshader</strong> (die den API-Methoden <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader"><strong>vssetshader</strong></a>, <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshader"><strong>gssetshader</strong></a>und <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshader"><strong>pssetshader</strong></a>ähneln).</span><span class="sxs-lookup"><span data-stu-id="1684b-141">SetXXXShader is one of <strong>SetVertexShader</strong>, <strong>SetGeometryShader</strong>, or <strong>SetPixelShader</strong> (which are similar to the API methods <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader"><strong>VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshader"><strong>GSSetShader</strong></a>, and <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshader"><strong>PSSetShader</strong></a>).</span></span></p></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

<span data-ttu-id="1684b-142">Effekt Zustands Gruppen werden im [Zustand "wirksam](d3d10-effect-states.md)" aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1684b-142">Effect state groups are listed in [effect state](d3d10-effect-states.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1684b-143">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1684b-143">Examples</span></span>

<span data-ttu-id="1684b-144">In diesem Beispiel (aus [cubemapgs](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)-Beispiel) wird der Mischungs Zustand festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1684b-144">This example (from [CubeMapGS sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) sets blending state.</span></span>


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



<span data-ttu-id="1684b-145">In diesem Beispiel wird der Status des Rasterizers zum Rendering eines Objekts in Wireframe eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="1684b-145">This example sets up the rasterizer state to render an object in wireframe.</span></span>


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



<span data-ttu-id="1684b-146">In diesem Beispiel wird der Shader-Status (aus [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)) festgelegt. , der einen Scheitelpunkt und einen Pixel-Shader verwendet.</span><span class="sxs-lookup"><span data-stu-id="1684b-146">This example sets shader state (from [BasicHLSL10 sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)); which uses a vertex and pixel shader.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1684b-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1684b-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1684b-148">Effekt Format</span><span class="sxs-lookup"><span data-stu-id="1684b-148">Effect Format</span></span>](d3d10-effect-format.md)
</dt> </dl>

 

 



