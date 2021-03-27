---
title: Effekt Zustands Gruppen (Direct3D 11)
description: Effekt Zustände sind Name-Wert-Paare in Form eines Ausdrucks.
ms.assetid: 87883483-4fa6-4362-807e-53b79b7d1370
keywords:
- Auswirkung, Zustands Gruppen (Direct3D 11)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58def71b6362706eb831129b1d222ef3d1cc9341
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948768"
---
# <a name="effect-state-groups-direct3d-11"></a><span data-ttu-id="cbccf-104">Effekt Zustands Gruppen (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="cbccf-104">Effect State Groups (Direct3D 11)</span></span>

<span data-ttu-id="cbccf-105">Effekt Zustände sind Name-Wert-Paare in Form eines Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="cbccf-105">Effect states are name value pairs in the form of an expression.</span></span>

-   [<span data-ttu-id="cbccf-106">Blend-Status</span><span class="sxs-lookup"><span data-stu-id="cbccf-106">Blend State</span></span>](#blend-state)
-   [<span data-ttu-id="cbccf-107">Tiefen-und Schablonen Zustand</span><span class="sxs-lookup"><span data-stu-id="cbccf-107">Depth and Stencil State</span></span>](#depth-and-stencil-state)
-   [<span data-ttu-id="cbccf-108">Status des Rasterizers</span><span class="sxs-lookup"><span data-stu-id="cbccf-108">Rasterizer State</span></span>](#rasterizer-state)
-   [<span data-ttu-id="cbccf-109">Samplerstatus</span><span class="sxs-lookup"><span data-stu-id="cbccf-109">Sampler State</span></span>](#sampler-state)
-   [<span data-ttu-id="cbccf-110">Effekt Objektstatus</span><span class="sxs-lookup"><span data-stu-id="cbccf-110">Effect Object State</span></span>](#effect-object-state)
-   [<span data-ttu-id="cbccf-111">Definieren und Verwenden von Zustands Objekten</span><span class="sxs-lookup"><span data-stu-id="cbccf-111">Defining and using state objects</span></span>](#defining-and-using-state-objects)
-   [<span data-ttu-id="cbccf-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cbccf-112">Related topics</span></span>](#related-topics)

## <a name="blend-state"></a><span data-ttu-id="cbccf-113">Blend-Status</span><span class="sxs-lookup"><span data-stu-id="cbccf-113">Blend State</span></span>



|                                                                                                                       |                                                           |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="cbccf-114">Alpha atocoverageenableblendenablesrcblenddestblendblendop srcblendalphadestblendalphablendopalpharendertargetwrite temask</span><span class="sxs-lookup"><span data-stu-id="cbccf-114">ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK</span></span> | <span data-ttu-id="cbccf-115">Mitglieder von [ **D3D11 \_ Blend- \_ ABSC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="cbccf-115">Members of [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span></span> |



 

## <a name="depth-and-stencil-state"></a><span data-ttu-id="cbccf-116">Tiefen-und Schablonen Zustand</span><span class="sxs-lookup"><span data-stu-id="cbccf-116">Depth and Stencil State</span></span>



|                                                                                                                                                                |                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="cbccf-117">Depthenabledepthschreitemaskdepthfuncstencilenablestencilsynchmaskstencilschreitemask</span><span class="sxs-lookup"><span data-stu-id="cbccf-117">DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK</span></span>                                                                                 | <span data-ttu-id="cbccf-118">Mitglieder der [ **D3D11- \_ tiefen \_ Schablone \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="cbccf-118">Members of [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span></span>    |
| <span data-ttu-id="cbccf-119">Frontfakestincilfailfrontfakestincilzfailfrontfabackfakestincilfailbackfakestincilzfailbackfakestbeiendestinfazfailbackfac</span><span class="sxs-lookup"><span data-stu-id="cbccf-119">FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC</span></span> | <span data-ttu-id="cbccf-120">Mitglied von [ **D3D11 \_ tiefen \_ Schablone (encilop \_** )](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="cbccf-120">Member of [**D3D11\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span></span> |



 

## <a name="rasterizer-state"></a><span data-ttu-id="cbccf-121">Status des Rasterizers</span><span class="sxs-lookup"><span data-stu-id="cbccf-121">Rasterizer State</span></span>



|                                                                                                                                 |                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cbccf-122">FillMode</span><span class="sxs-lookup"><span data-stu-id="cbccf-122">FILLMODE</span></span>                                                                                                                        | [<span data-ttu-id="cbccf-123">**D3D11 \_ Füll \_ Modus**</span><span class="sxs-lookup"><span data-stu-id="cbccf-123">**D3D11\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_fill_mode)                        |
| <span data-ttu-id="cbccf-124">CullMode</span><span class="sxs-lookup"><span data-stu-id="cbccf-124">CULLMODE</span></span>                                                                                                                        | [<span data-ttu-id="cbccf-125">**D3D11- \_ cull- \_ Modus**</span><span class="sxs-lookup"><span data-stu-id="cbccf-125">**D3D11\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cull_mode)                        |
| <span data-ttu-id="cbccf-126">frontcounterclockwisedepthbiasdepthbiasklamslopescaleddepthbias zclipenablescissorenablemultisampleenableantialiasedlineenable</span><span class="sxs-lookup"><span data-stu-id="cbccf-126">FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE</span></span> | <span data-ttu-id="cbccf-127">Mitglieder des [ **D3D11 \_ Rasterizer \_** -Moduls](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="cbccf-127">Members of [**D3D11\_RASTERIZER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span></span> |



 

## <a name="sampler-state"></a><span data-ttu-id="cbccf-128">Samplerstatus</span><span class="sxs-lookup"><span data-stu-id="cbccf-128">Sampler State</span></span>



|                                                                                                     |                                                               |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="cbccf-129">Filter adressu adressensu adressu adressw miplodbias MaxAnisotropy comparisonfunc BorderColor minlod maxlod</span><span class="sxs-lookup"><span data-stu-id="cbccf-129">Filter AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD</span></span> | <span data-ttu-id="cbccf-130">Mitglieder des [ **D3D11 \_ - \_ samplerentsc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="cbccf-130">Members of [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span></span> |



 

<span data-ttu-id="cbccf-131">Beispiele hierfür finden Sie unter [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) .</span><span class="sxs-lookup"><span data-stu-id="cbccf-131">See [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="cbccf-132">Effekt Objektstatus</span><span class="sxs-lookup"><span data-stu-id="cbccf-132">Effect Object State</span></span>



| <span data-ttu-id="cbccf-133">This Effect-Objekt</span><span class="sxs-lookup"><span data-stu-id="cbccf-133">This Effect Object</span></span>                          | <span data-ttu-id="cbccf-134">Entsprechung</span><span class="sxs-lookup"><span data-stu-id="cbccf-134">Maps to</span></span>                                                             |
|---------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cbccf-135">Rasterizerstate</span><span class="sxs-lookup"><span data-stu-id="cbccf-135">RASTERIZERSTATE</span></span>                             | <span data-ttu-id="cbccf-136">Ein [Rasterizer State](#rasterizer-state) State-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cbccf-136">A [Rasterizer State](#rasterizer-state) state object.</span></span>               |
| <span data-ttu-id="cbccf-137">Depthstencilstate</span><span class="sxs-lookup"><span data-stu-id="cbccf-137">DEPTHSTENCILSTATE</span></span>                           | <span data-ttu-id="cbccf-138">Ein [tiefen-und Schablonen Zustands](#depth-and-stencil-state) Objekt.</span><span class="sxs-lookup"><span data-stu-id="cbccf-138">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="cbccf-139">Blendstate</span><span class="sxs-lookup"><span data-stu-id="cbccf-139">BLENDSTATE</span></span>                                  | <span data-ttu-id="cbccf-140">Ein [Blend](#blend-state) -Zustands Objekt.</span><span class="sxs-lookup"><span data-stu-id="cbccf-140">A [Blend State](#blend-state) state object.</span></span>                         |
| <span data-ttu-id="cbccf-141">Titellink</span><span class="sxs-lookup"><span data-stu-id="cbccf-141">VERTEXSHADER</span></span>                                | <span data-ttu-id="cbccf-142">Ein kompiliertes Vertex-Shader-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cbccf-142">A compiled vertex shader object.</span></span>                                    |
| <span data-ttu-id="cbccf-143">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="cbccf-143">PIXELSHADER</span></span>                                 | <span data-ttu-id="cbccf-144">Ein kompiliertes Pixel-Shader-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cbccf-144">A compiled pixel shader object.</span></span>                                     |
| <span data-ttu-id="cbccf-145">Geometryshader</span><span class="sxs-lookup"><span data-stu-id="cbccf-145">GEOMETRYSHADER</span></span>                              | <span data-ttu-id="cbccf-146">Ein kompiliertes Geometry-Shader-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cbccf-146">A compiled geometry shader object.</span></span>                                  |
| <span data-ttu-id="cbccf-147">DS \_ stencilrefab \_ blendfactor ab \_ samplemask</span><span class="sxs-lookup"><span data-stu-id="cbccf-147">DS\_STENCILREFAB\_BLENDFACTORAB\_SAMPLEMASK</span></span> | <span data-ttu-id="cbccf-148">Mitglieder von [**Bibliothek d3dx11 \_ Pass \_**](d3dx11-pass-desc.md)(Debug).</span><span class="sxs-lookup"><span data-stu-id="cbccf-148">Members of [**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md).</span></span>          |



 

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="cbccf-149">Definieren und Verwenden von Zustands Objekten</span><span class="sxs-lookup"><span data-stu-id="cbccf-149">Defining and using state objects</span></span>

<span data-ttu-id="cbccf-150">Zustands Objekte werden in FX-Dateien im folgenden Format deklariert.</span><span class="sxs-lookup"><span data-stu-id="cbccf-150">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="cbccf-151">Stateobjecttype ist einer der oben aufgeführten Zustände und der Name eines beliebigen Members, der einen nicht standardmäßigen Wert hat.</span><span class="sxs-lookup"><span data-stu-id="cbccf-151">StateObjectType is one of the states listed above and MemberName is the name of any member that will have a non-default value.</span></span>


```
StateObjectType ObjectName {
  MemberName = value;
  ...
  MemberName = value;
};
    
```



<span data-ttu-id="cbccf-152">Wenn Sie z. b. ein Blend-Zustands Objekt mit Alpha atocoverageenable und blendenable \[ 0 \] auf **false** einrichten möchten, wird der folgende Code verwendet.</span><span class="sxs-lookup"><span data-stu-id="cbccf-152">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE** the following code would be used.</span></span>


```
BlendState NoBlend {
  AlphaToCoverageEnable = FALSE;
  BlendEnable[0] = FALSE;
};
    
```



<span data-ttu-id="cbccf-153">Das State-Objekt wird auf eine Technik Übergabe mithilfe einer der setstategroup-Funktionen angewendet, die unter [Effekt Technik Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="cbccf-153">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md).</span></span> <span data-ttu-id="cbccf-154">Wenn Sie z. b. das oben beschriebene blendstate-Objekt anwenden möchten, wird der folgende Code verwendet.</span><span class="sxs-lookup"><span data-stu-id="cbccf-154">For example, to apply the BlendState object described above the following code would be used.</span></span>


```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    
```



## <a name="related-topics"></a><span data-ttu-id="cbccf-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cbccf-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbccf-156">Syntax der Effekt Technik</span><span class="sxs-lookup"><span data-stu-id="cbccf-156">Effect Technique Syntax</span></span>](d3d11-effect-technique-syntax.md)
</dt> <dt>

[<span data-ttu-id="cbccf-157">Effekt Format (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="cbccf-157">Effect Format (Direct3D 11)</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 