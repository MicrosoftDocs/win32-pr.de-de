---
title: Effektzustandsgruppen (Direct3D 11)
description: Effektzustände sind Name-Wert-Paare in Form eines Ausdrucks.
ms.assetid: 87883483-4fa6-4362-807e-53b79b7d1370
keywords:
- Effect, Zustandsgruppen (Direct3D 11)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a757926d8c4c259adc94f505a778cf73233b5a
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335334"
---
# <a name="effect-state-groups-direct3d-11"></a><span data-ttu-id="6b636-104">Effektzustandsgruppen (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="6b636-104">Effect State Groups (Direct3D 11)</span></span>

<span data-ttu-id="6b636-105">Effektzustände sind Name-Wert-Paare in Form eines Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="6b636-105">Effect states are name value pairs in the form of an expression.</span></span>

-   [<span data-ttu-id="6b636-106">Blend-Zustand</span><span class="sxs-lookup"><span data-stu-id="6b636-106">Blend State</span></span>](#blend-state)
-   [<span data-ttu-id="6b636-107">Tiefen- und Schablonenzustand</span><span class="sxs-lookup"><span data-stu-id="6b636-107">Depth and Stencil State</span></span>](#depth-and-stencil-state)
-   [<span data-ttu-id="6b636-108">Status des Rasterizers</span><span class="sxs-lookup"><span data-stu-id="6b636-108">Rasterizer State</span></span>](#rasterizer-state)
-   [<span data-ttu-id="6b636-109">Samplerzustand</span><span class="sxs-lookup"><span data-stu-id="6b636-109">Sampler State</span></span>](#sampler-state)
-   [<span data-ttu-id="6b636-110">Effect-Objektzustand</span><span class="sxs-lookup"><span data-stu-id="6b636-110">Effect Object State</span></span>](#effect-object-state)
-   [<span data-ttu-id="6b636-111">Definieren und Verwenden von Zustandsobjekten</span><span class="sxs-lookup"><span data-stu-id="6b636-111">Defining and using state objects</span></span>](#defining-and-using-state-objects)
-   [<span data-ttu-id="6b636-112">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="6b636-112">Related topics</span></span>](#related-topics)

## <a name="blend-state"></a><span data-ttu-id="6b636-113">Blend-Zustand</span><span class="sxs-lookup"><span data-stu-id="6b636-113">Blend State</span></span>



| <span data-ttu-id="6b636-114">Auswirkungszustand</span><span class="sxs-lookup"><span data-stu-id="6b636-114">Effect state</span></span>                                                                                                                      | <span data-ttu-id="6b636-115">Group</span><span class="sxs-lookup"><span data-stu-id="6b636-115">Group</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="6b636-116">ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK</span><span class="sxs-lookup"><span data-stu-id="6b636-116">ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK</span></span> | <span data-ttu-id="6b636-117">Elemente von [ **D3D11 \_ BLEND \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="6b636-117">Members of [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span></span> |



 

## <a name="depth-and-stencil-state"></a><span data-ttu-id="6b636-118">Tiefen- und Schablonenzustand</span><span class="sxs-lookup"><span data-stu-id="6b636-118">Depth and Stencil State</span></span>



|  <span data-ttu-id="6b636-119">Auswirkungszustand</span><span class="sxs-lookup"><span data-stu-id="6b636-119">Effect state</span></span>                                                                                                                                                              | <span data-ttu-id="6b636-120">Group</span><span class="sxs-lookup"><span data-stu-id="6b636-120">Group</span></span>                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="6b636-121">DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK</span><span class="sxs-lookup"><span data-stu-id="6b636-121">DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK</span></span>                                                                                 | <span data-ttu-id="6b636-122">Elemente von [ **D3D11 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="6b636-122">Members of [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span></span>    |
| <span data-ttu-id="6b636-123">FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC</span><span class="sxs-lookup"><span data-stu-id="6b636-123">FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC</span></span> | <span data-ttu-id="6b636-124">Member von [ **D3D11 \_ DEPTH \_ STENCILOP \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="6b636-124">Member of [**D3D11\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span></span> |



 

## <a name="rasterizer-state"></a><span data-ttu-id="6b636-125">Rasterizerstatus</span><span class="sxs-lookup"><span data-stu-id="6b636-125">Rasterizer State</span></span>



| <span data-ttu-id="6b636-126">Auswirkungszustand</span><span class="sxs-lookup"><span data-stu-id="6b636-126">Effect state</span></span>                                                                                                                                | <span data-ttu-id="6b636-127">Group</span><span class="sxs-lookup"><span data-stu-id="6b636-127">Group</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6b636-128">Fillmode</span><span class="sxs-lookup"><span data-stu-id="6b636-128">FILLMODE</span></span>                                                                                                                        | [<span data-ttu-id="6b636-129">**\_ \_ D3D11-FÜLLMODUS**</span><span class="sxs-lookup"><span data-stu-id="6b636-129">**D3D11\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_fill_mode)                        |
| <span data-ttu-id="6b636-130">CULLMODE</span><span class="sxs-lookup"><span data-stu-id="6b636-130">CULLMODE</span></span>                                                                                                                        | [<span data-ttu-id="6b636-131">**D3D11 \_ \_ CULL-MODUS**</span><span class="sxs-lookup"><span data-stu-id="6b636-131">**D3D11\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cull_mode)                        |
| <span data-ttu-id="6b636-132">FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSSCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE</span><span class="sxs-lookup"><span data-stu-id="6b636-132">FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE</span></span> | <span data-ttu-id="6b636-133">Member von [ **D3D11 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="6b636-133">Members of [**D3D11\_RASTERIZER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span></span> |



 

## <a name="sampler-state"></a><span data-ttu-id="6b636-134">Samplerstatus</span><span class="sxs-lookup"><span data-stu-id="6b636-134">Sampler State</span></span>



| <span data-ttu-id="6b636-135">Auswirkungszustand</span><span class="sxs-lookup"><span data-stu-id="6b636-135">Effect state</span></span>                                                                                                    | <span data-ttu-id="6b636-136">Group</span><span class="sxs-lookup"><span data-stu-id="6b636-136">Group</span></span>                                                              |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="6b636-137">Filter AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD</span><span class="sxs-lookup"><span data-stu-id="6b636-137">Filter AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD</span></span> | <span data-ttu-id="6b636-138">Member von [ **D3D11 \_ SAMPLER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="6b636-138">Members of [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span></span> |



 

<span data-ttu-id="6b636-139">Beispiele finden Sie unter [Sampler Type (DirectX HLSL) (Sampler-Typ (DirectX HLSL)).](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler)</span><span class="sxs-lookup"><span data-stu-id="6b636-139">See [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="6b636-140">Effect-Objektzustand</span><span class="sxs-lookup"><span data-stu-id="6b636-140">Effect Object State</span></span>



| <span data-ttu-id="6b636-141">Dieses Effect-Objekt</span><span class="sxs-lookup"><span data-stu-id="6b636-141">This Effect Object</span></span>                          | <span data-ttu-id="6b636-142">Entsprechung</span><span class="sxs-lookup"><span data-stu-id="6b636-142">Maps to</span></span>                                                             |
|---------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6b636-143">RASTERIZERSTATE</span><span class="sxs-lookup"><span data-stu-id="6b636-143">RASTERIZERSTATE</span></span>                             | <span data-ttu-id="6b636-144">Ein [Zustandsobjekt des Rasterizerzustands.](#rasterizer-state)</span><span class="sxs-lookup"><span data-stu-id="6b636-144">A [Rasterizer State](#rasterizer-state) state object.</span></span>               |
| <span data-ttu-id="6b636-145">DEPTHSTENCILSTATE</span><span class="sxs-lookup"><span data-stu-id="6b636-145">DEPTHSTENCILSTATE</span></span>                           | <span data-ttu-id="6b636-146">Ein [Tiefen- und Schablonenzustandsobjekt.](#depth-and-stencil-state)</span><span class="sxs-lookup"><span data-stu-id="6b636-146">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="6b636-147">BLENDSTATE</span><span class="sxs-lookup"><span data-stu-id="6b636-147">BLENDSTATE</span></span>                                  | <span data-ttu-id="6b636-148">Ein [Blend State-Zustandsobjekt.](#blend-state)</span><span class="sxs-lookup"><span data-stu-id="6b636-148">A [Blend State](#blend-state) state object.</span></span>                         |
| <span data-ttu-id="6b636-149">VERTEXSHADER</span><span class="sxs-lookup"><span data-stu-id="6b636-149">VERTEXSHADER</span></span>                                | <span data-ttu-id="6b636-150">Ein kompiliertes Vertex-Shaderobjekt.</span><span class="sxs-lookup"><span data-stu-id="6b636-150">A compiled vertex shader object.</span></span>                                    |
| <span data-ttu-id="6b636-151">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="6b636-151">PIXELSHADER</span></span>                                 | <span data-ttu-id="6b636-152">Ein kompiliertes Pixel-Shaderobjekt.</span><span class="sxs-lookup"><span data-stu-id="6b636-152">A compiled pixel shader object.</span></span>                                     |
| <span data-ttu-id="6b636-153">GEOMETRYSHADER</span><span class="sxs-lookup"><span data-stu-id="6b636-153">GEOMETRYSHADER</span></span>                              | <span data-ttu-id="6b636-154">Ein kompiliertes Geometrie-Shaderobjekt.</span><span class="sxs-lookup"><span data-stu-id="6b636-154">A compiled geometry shader object.</span></span>                                  |
| <span data-ttu-id="6b636-155">DS \_ STENCILREFAB \_ BLENDFACTORAB \_ SAMPLEMASK</span><span class="sxs-lookup"><span data-stu-id="6b636-155">DS\_STENCILREFAB\_BLENDFACTORAB\_SAMPLEMASK</span></span> | <span data-ttu-id="6b636-156">Member von [**D3DX11 \_ PASS \_ DESC**](d3dx11-pass-desc.md).</span><span class="sxs-lookup"><span data-stu-id="6b636-156">Members of [**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md).</span></span>          |



 

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="6b636-157">Definieren und Verwenden von Zustandsobjekten</span><span class="sxs-lookup"><span data-stu-id="6b636-157">Defining and using state objects</span></span>

<span data-ttu-id="6b636-158">Zustandsobjekte werden in FX-Dateien im folgenden Format deklariert.</span><span class="sxs-lookup"><span data-stu-id="6b636-158">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="6b636-159">StateObjectType ist einer der oben aufgeführten Zustände, und MemberName ist der Name jedes Mitglieds, das einen nicht standardmäßigen Wert hat.</span><span class="sxs-lookup"><span data-stu-id="6b636-159">StateObjectType is one of the states listed above and MemberName is the name of any member that will have a non-default value.</span></span>


```
StateObjectType ObjectName {
  MemberName = value;
  ...
  MemberName = value;
};
    
```



<span data-ttu-id="6b636-160">Wenn Sie beispielsweise ein Blend-Zustandsobjekt einrichten möchten, bei dem AlphaToCoverageEnable und BlendEnable 0 auf FALSE festgelegt sind, wird der folgende \[ \] Code verwendet. </span><span class="sxs-lookup"><span data-stu-id="6b636-160">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE** the following code would be used.</span></span>


```
BlendState NoBlend {
  AlphaToCoverageEnable = FALSE;
  BlendEnable[0] = FALSE;
};
    
```



<span data-ttu-id="6b636-161">Das Zustandsobjekt wird mithilfe einer der Unter Effect [Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md)beschriebenen SetStateGroup-Funktionen auf einen Technikpass angewendet.</span><span class="sxs-lookup"><span data-stu-id="6b636-161">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md).</span></span> <span data-ttu-id="6b636-162">Um beispielsweise das oben beschriebene BlendState-Objekt anzuwenden, wird der folgende Code verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b636-162">For example, to apply the BlendState object described above the following code would be used.</span></span>


```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    
```



## <a name="related-topics"></a><span data-ttu-id="6b636-163">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6b636-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b636-164">Syntax der Effekttechnik</span><span class="sxs-lookup"><span data-stu-id="6b636-164">Effect Technique Syntax</span></span>](d3d11-effect-technique-syntax.md)
</dt> <dt>

[<span data-ttu-id="6b636-165">Effect-Format (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="6b636-165">Effect Format (Direct3D 11)</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 