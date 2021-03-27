---
title: 10level9 ID3D11Device Methoden
description: In diesem Abschnitt werden die Unterschiede zwischen den einzelnen 10level9-featureebenen und der D3D \_ \_ Featureebene \_ 11 \_ 0 und höher für die ID3D11Device-Methoden aufgeführt.
ms.assetid: c3bc32a9-8d97-430b-be6a-b4935d7ac56c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400c7f321981f13b3e184a25139782c8a9d9a2ba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390758"
---
# <a name="10level9-id3d11device-methods"></a><span data-ttu-id="19830-103">10level9 ID3D11Device Methoden</span><span class="sxs-lookup"><span data-stu-id="19830-103">10Level9 ID3D11Device Methods</span></span>

<span data-ttu-id="19830-104">In diesem Abschnitt werden die Unterschiede zwischen den einzelnen 10level9-featureebenen und der D3D \_ \_ Featureebene \_ 11 \_ 0 und höher für die [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -Methoden aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="19830-104">This section lists the differences between each 10Level9 feature level and the D3D\_FEATURE\_LEVEL\_11\_0 and higher feature level for the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) methods.</span></span>

-   [<span data-ttu-id="19830-105">ID3D11Device:: checkcounter</span><span class="sxs-lookup"><span data-stu-id="19830-105">ID3D11Device::CheckCounter</span></span>](#id3d11devicecheckcounter)
-   [<span data-ttu-id="19830-106">ID3D11Device:: checkformatsupport</span><span class="sxs-lookup"><span data-stu-id="19830-106">ID3D11Device::CheckFormatSupport</span></span>](#id3d11devicecheckformatsupport)
-   [<span data-ttu-id="19830-107">ID3D11Device:: checkmultisamplequalitylevels</span><span class="sxs-lookup"><span data-stu-id="19830-107">ID3D11Device::CheckMultisampleQualityLevels</span></span>](#id3d11devicecheckmultisamplequalitylevels)
-   [<span data-ttu-id="19830-108">ID3D11Device:: kreateblendstate</span><span class="sxs-lookup"><span data-stu-id="19830-108">ID3D11Device::CreateBlendState</span></span>](#id3d11devicecreateblendstate)
-   [<span data-ttu-id="19830-109">ID3D11Device:: CreateBlendState1</span><span class="sxs-lookup"><span data-stu-id="19830-109">ID3D11Device::CreateBlendState1</span></span>](#id3d11devicecreateblendstate1)
-   [<span data-ttu-id="19830-110">ID3D11Device:: up Buffer</span><span class="sxs-lookup"><span data-stu-id="19830-110">ID3D11Device::CreateBuffer</span></span>](#id3d11devicecreatebuffer)
-   [<span data-ttu-id="19830-111">ID3D11Device:: kreatecounter</span><span class="sxs-lookup"><span data-stu-id="19830-111">ID3D11Device::CreateCounter</span></span>](#id3d11devicecreatecounter)
-   [<span data-ttu-id="19830-112">ID3D11Device:: "dashboardepthstencilview"</span><span class="sxs-lookup"><span data-stu-id="19830-112">ID3D11Device::CreateDepthStencilView</span></span>](#id3d11devicecreatedepthstencilview)
-   [<span data-ttu-id="19830-113">ID3D11Device:: kreatedomainshader</span><span class="sxs-lookup"><span data-stu-id="19830-113">ID3D11Device::CreateDomainShader</span></span>](#id3d11devicecreatedomainshader)
-   [<span data-ttu-id="19830-114">ID3D11Device:: kreategeometryshader</span><span class="sxs-lookup"><span data-stu-id="19830-114">ID3D11Device::CreateGeometryShader</span></span>](#id3d11devicecreategeometryshader)
-   [<span data-ttu-id="19830-115">ID3D11Device:: kreategeometryshaderwithstreamoutput</span><span class="sxs-lookup"><span data-stu-id="19830-115">ID3D11Device::CreateGeometryShaderWithStreamOutput</span></span>](#id3d11devicecreategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="19830-116">ID3D11Device:: kreatehullshader</span><span class="sxs-lookup"><span data-stu-id="19830-116">ID3D11Device::CreateHullShader</span></span>](#id3d11devicecreatehullshader)
-   [<span data-ttu-id="19830-117">ID3D11Device:: kreatinput Layout</span><span class="sxs-lookup"><span data-stu-id="19830-117">ID3D11Device::CreateInputLayout</span></span>](#id3d11devicecreateinputlayout)
-   [<span data-ttu-id="19830-118">ID3D11Device:: kreatepixelshader</span><span class="sxs-lookup"><span data-stu-id="19830-118">ID3D11Device::CreatePixelShader</span></span>](#id3d11devicecreatepixelshader)
-   [<span data-ttu-id="19830-119">ID3D11Device:: kreatepredicate</span><span class="sxs-lookup"><span data-stu-id="19830-119">ID3D11Device::CreatePredicate</span></span>](#id3d11devicecreatepredicate)
-   [<span data-ttu-id="19830-120">ID3D11Device:: kreatequery</span><span class="sxs-lookup"><span data-stu-id="19830-120">ID3D11Device::CreateQuery</span></span>](#id3d11devicecreatequery)
-   [<span data-ttu-id="19830-121">ID3D11Device:: kreaterasterizerstate</span><span class="sxs-lookup"><span data-stu-id="19830-121">ID3D11Device::CreateRasterizerState</span></span>](#id3d11devicecreaterasterizerstate)
-   [<span data-ttu-id="19830-122">ID3D11Device:: kreaterendertargetview</span><span class="sxs-lookup"><span data-stu-id="19830-122">ID3D11Device::CreateRenderTargetView</span></span>](#id3d11devicecreaterendertargetview)
-   [<span data-ttu-id="19830-123">ID3D11Device:: kreatesamplerstate</span><span class="sxs-lookup"><span data-stu-id="19830-123">ID3D11Device::CreateSamplerState</span></span>](#id3d11devicecreatesamplerstate)
-   [<span data-ttu-id="19830-124">ID3D11Device:: kreateshaderresourceview</span><span class="sxs-lookup"><span data-stu-id="19830-124">ID3D11Device::CreateShaderResourceView</span></span>](#id3d11devicecreateshaderresourceview)
-   [<span data-ttu-id="19830-125">ID3D11Device:: CreateTexture1D</span><span class="sxs-lookup"><span data-stu-id="19830-125">ID3D11Device::CreateTexture1D</span></span>](#id3d11devicecreatetexture1d)
-   [<span data-ttu-id="19830-126">ID3D11Device:: CreateTexture2D</span><span class="sxs-lookup"><span data-stu-id="19830-126">ID3D11Device::CreateTexture2D</span></span>](#id3d11devicecreatetexture2d)
-   [<span data-ttu-id="19830-127">ID3D11Device:: CreateTexture3D</span><span class="sxs-lookup"><span data-stu-id="19830-127">ID3D11Device::CreateTexture3D</span></span>](#id3d11devicecreatetexture3d)
-   [<span data-ttu-id="19830-128">ID3D11Device:: kreateunorderedaccessview</span><span class="sxs-lookup"><span data-stu-id="19830-128">ID3D11Device::CreateUnorderedAccessView</span></span>](#id3d11devicecreateunorderedaccessview)
-   [<span data-ttu-id="19830-129">ID3D11Device:: kreatevertexshader</span><span class="sxs-lookup"><span data-stu-id="19830-129">ID3D11Device::CreateVertexShader</span></span>](#id3d11devicecreatevertexshader)
-   [<span data-ttu-id="19830-130">ID3D11Device:: opensharedresource</span><span class="sxs-lookup"><span data-stu-id="19830-130">ID3D11Device::OpenSharedResource</span></span>](#id3d11deviceopensharedresource)
-   [<span data-ttu-id="19830-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="19830-131">Related topics</span></span>](#related-topics)

## <a name="id3d11devicecheckcounter"></a><span data-ttu-id="19830-132">ID3D11Device:: checkcounter</span><span class="sxs-lookup"><span data-stu-id="19830-132">ID3D11Device::CheckCounter</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="19830-133">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-133">Feature Level</span></span></th>
<th><span data-ttu-id="19830-134">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="19830-134">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19830-135">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="19830-135">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="19830-136">Geräte abhängige Leistungsindikatoren werden optional unterstützt.</span><span class="sxs-lookup"><span data-stu-id="19830-136">Device-dependent counters are optionally supported.</span></span> <span data-ttu-id="19830-137">Verwenden Sie <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>ID3D11Device:: checkcounterinfo</strong></a> , um die Unterstützung zu ermitteln. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="19830-137">Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>ID3D11Device::CheckCounterInfo</strong></a> to determine support.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="19830-138">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="19830-138">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="19830-139">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="19830-139">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecheckformatsupport"></a><span data-ttu-id="19830-140">ID3D11Device:: checkformatsupport</span><span class="sxs-lookup"><span data-stu-id="19830-140">ID3D11Device::CheckFormatSupport</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="19830-141">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-141">Feature Level</span></span></th>
<th><span data-ttu-id="19830-142">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="19830-142">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19830-143">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="19830-143">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="19830-144">Siehe Formatunterstützung nach <a href="overviews-direct3d-11-devices-downlevel-intro.md">Featureebene</a>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="19830-144">See format support by <a href="overviews-direct3d-11-devices-downlevel-intro.md">feature level</a>${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="19830-145">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="19830-145">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="19830-146">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="19830-146">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecheckmultisamplequalitylevels"></a><span data-ttu-id="19830-147">ID3D11Device:: checkmultisamplequalitylevels</span><span class="sxs-lookup"><span data-stu-id="19830-147">ID3D11Device::CheckMultisampleQualityLevels</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="19830-148">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-148">Feature Level</span></span></th>
<th><span data-ttu-id="19830-149">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="19830-149">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19830-150">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="19830-150">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="19830-151">Funktionsebenen stellen keine Garantie bezüglich der MSAA-Unterstützung dar. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="19830-151">Feature levels make no guarantees concerning MSAA support.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="19830-152">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="19830-152">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="19830-153">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="19830-153">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateblendstate"></a><span data-ttu-id="19830-154">ID3D11Device:: kreateblendstate</span><span class="sxs-lookup"><span data-stu-id="19830-154">ID3D11Device::CreateBlendState</span></span>



| <span data-ttu-id="19830-155">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-155">Feature Level</span></span>              | <span data-ttu-id="19830-156">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="19830-156">Behavior Differences</span></span>                                                                                                                                                                                                                                                                                                                                             |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19830-157">D3D \_ \_ Featureebene \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="19830-157">D3D\_FEATURE\_LEVEL\_9\_1</span></span>  | <span data-ttu-id="19830-158">Alpha atocoverageenable muss den Wert **false** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="19830-158">AlphaToCoverageEnable must be **FALSE**.</span></span><br/> <span data-ttu-id="19830-159">Die ersten vier blendenables müssen alle den gleichen Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="19830-159">The first four BlendEnables must all have the same value.</span></span><br/> <span data-ttu-id="19830-160">D3D11 \_ Blend \_ src \_ Alpha ASAT wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="19830-160">D3D11\_BLEND\_SRC\_ALPHASAT not supported.</span></span><br/> <span data-ttu-id="19830-161">Die Farbmischung aus zwei Quellen wird nicht unterstützt (srcblend oder destblend mit Quelle1 im Namen).</span><span class="sxs-lookup"><span data-stu-id="19830-161">Dual-source color blend not supported (any SrcBlend or DestBlend with SRC1 in the name)</span></span><br/>                                                                                |
| <span data-ttu-id="19830-162">D3D \_ \_ Featureebene \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="19830-162">D3D\_FEATURE\_LEVEL\_9\_2</span></span>  | <span data-ttu-id="19830-163">Alpha atocoverageenable muss den Wert **false** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="19830-163">AlphaToCoverageEnable must be **FALSE**.</span></span><br/> <span data-ttu-id="19830-164">Die ersten vier blendenables müssen alle den gleichen Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="19830-164">The first four BlendEnables must all have the same value.</span></span><br/> <span data-ttu-id="19830-165">Die ersten vier rendertargetschreitemasks müssen alle denselben Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="19830-165">The first four RenderTargetWriteMasks must all have the same value.</span></span><br/> <span data-ttu-id="19830-166">D3D11 \_ Blend \_ src \_ Alpha ASAT wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="19830-166">D3D11\_BLEND\_SRC\_ALPHASAT not supported.</span></span><br/> <span data-ttu-id="19830-167">Die Farbmischung aus zwei Quellen wird nicht unterstützt (srcblend oder destblend mit Quelle1 im Namen).</span><span class="sxs-lookup"><span data-stu-id="19830-167">Dual-source color blend not supported (any SrcBlend or DestBlend with SRC1 in the name)</span></span><br/> |
| <span data-ttu-id="19830-168">D3D \_ \_ Featureebene \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="19830-168">D3D\_FEATURE\_LEVEL\_9\_3</span></span>  | <span data-ttu-id="19830-169">Alpha atocoverageenable muss den Wert **false** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="19830-169">AlphaToCoverageEnable must be **FALSE**.</span></span><br/> <span data-ttu-id="19830-170">Die ersten vier blendenables müssen alle den gleichen Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="19830-170">The first four BlendEnables must all have the same value.</span></span><br/> <span data-ttu-id="19830-171">D3D11 \_ Blend \_ src \_ Alpha ASAT wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="19830-171">D3D11\_BLEND\_SRC\_ALPHASAT not supported.</span></span><br/> <span data-ttu-id="19830-172">Die Farbmischung aus zwei Quellen wird nicht unterstützt (srcblend oder destblend mit Quelle1 im Namen).</span><span class="sxs-lookup"><span data-stu-id="19830-172">Dual-source color blend not supported (any SrcBlend or DestBlend with SRC1 in the name)</span></span><br/>                                                                                |
| <span data-ttu-id="19830-173">D3D \_ \_ Featureebene \_ 10 \_ 0</span><span class="sxs-lookup"><span data-stu-id="19830-173">D3D\_FEATURE\_LEVEL\_10\_0</span></span> | <span data-ttu-id="19830-174">Hinzufügen von Alpha-zu-Abdeckung</span><span class="sxs-lookup"><span data-stu-id="19830-174">Adds alpha-to-coverage</span></span>                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="id3d11devicecreateblendstate1"></a><span data-ttu-id="19830-175">ID3D11Device:: CreateBlendState1</span><span class="sxs-lookup"><span data-stu-id="19830-175">ID3D11Device::CreateBlendState1</span></span>



| <span data-ttu-id="19830-176">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-176">Feature Level</span></span>              | <span data-ttu-id="19830-177">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="19830-177">Behavior Differences</span></span>                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19830-178">D3D \_ \_ Featureebene \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="19830-178">D3D\_FEATURE\_LEVEL\_9\_1</span></span>  | <span data-ttu-id="19830-179">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="19830-179">Unsupported</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="19830-180">D3D \_ \_ Featureebene \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="19830-180">D3D\_FEATURE\_LEVEL\_9\_2</span></span>  | <span data-ttu-id="19830-181">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="19830-181">Unsupported</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="19830-182">D3D \_ \_ Featureebene \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="19830-182">D3D\_FEATURE\_LEVEL\_9\_3</span></span>  | <span data-ttu-id="19830-183">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="19830-183">Unsupported</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="19830-184">D3D \_ \_ Featureebene \_ 10 \_ 0</span><span class="sxs-lookup"><span data-stu-id="19830-184">D3D\_FEATURE\_LEVEL\_10\_0</span></span> | <span data-ttu-id="19830-185">Der *outputmergerlogicop* -Member wurde den [**D3D11 \_ Feature \_ Data D3D11- \_ \_ Optionen**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options)hinzugefügt, um die Unterstützung für logische Vorgänge zu bestimmen (bitweise logische Operationen zwischen der Ausgabe des Pixelshaders und dem Rendern des Ziel Inhalts). Weitere Informationen finden Sie unter [**D3D11 \_ Rendering \_ Target \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1)).</span><span class="sxs-lookup"><span data-stu-id="19830-185">The *OutputMergerLogicOp* member has been added to [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options), to determine support for logical operations (bitwise logic operations between pixel shader output and render target contents, refer to [**D3D11\_RENDER\_TARGET\_BLEND\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1)).</span></span> |



 

## <a name="id3d11devicecreatebuffer"></a><span data-ttu-id="19830-186">ID3D11Device:: up Buffer</span><span class="sxs-lookup"><span data-stu-id="19830-186">ID3D11Device::CreateBuffer</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="19830-187">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-187">Feature Level</span></span></th>
<th><span data-ttu-id="19830-188">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="19830-188">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19830-189">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="19830-189">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td><span data-ttu-id="19830-190">Puffer können keine renderzielsichten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="19830-190">Buffers can't have render target views.</span></span><br/> <span data-ttu-id="19830-191">Puffer müssen genau eine D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER oder D3D11_BIND_CONSTANT_BUFFER aufweisen.</span><span class="sxs-lookup"><span data-stu-id="19830-191">Buffers must have exactly one of D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER, or D3D11_BIND_CONSTANT_BUFFER.</span></span><br/> <span data-ttu-id="19830-192">Ermöglicht nur Index Puffer mit dem DXGI_FORMAT_R16_UINT-Format.</span><span class="sxs-lookup"><span data-stu-id="19830-192">Only allows index buffers with the DXGI_FORMAT_R16_UINT format.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19830-193">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="19830-193">D3D_FEATURE_LEVEL_9_2</span></span></td>
<td rowspan="2"> <span data-ttu-id="19830-194">Puffer können keine renderzielsichten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="19830-194">Buffers can't have render target views.</span></span><br/> <span data-ttu-id="19830-195">Puffer müssen genau eine D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER oder D3D11_BIND_CONSTANT_BUFFER aufweisen.</span><span class="sxs-lookup"><span data-stu-id="19830-195">Buffers must have exactly one of D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER, or D3D11_BIND_CONSTANT_BUFFER.</span></span><br/> <span data-ttu-id="19830-196">Ermöglicht Index Puffer mit den DXGI_FORMAT_R16_UINT-und DXGI_FORMAT_R32_UINT Formaten wie D3D_FEATURE_LEVEL_10_0 und höher.</span><span class="sxs-lookup"><span data-stu-id="19830-196">Allows index buffers with the DXGI_FORMAT_R16_UINT and DXGI_FORMAT_R32_UINT formats like D3D_FEATURE_LEVEL_10_0 and higher.</span></span> <br/> <span data-ttu-id="19830-197">$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="19830-197">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19830-198">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="19830-198">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatecounter"></a><span data-ttu-id="19830-199">ID3D11Device:: kreatecounter</span><span class="sxs-lookup"><span data-stu-id="19830-199">ID3D11Device::CreateCounter</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="19830-200">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-200">Feature Level</span></span></th>
<th><span data-ttu-id="19830-201">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="19830-201">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19830-202">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="19830-202">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="19830-203">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="19830-203">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="19830-204">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="19830-204">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="19830-205">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="19830-205">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatedepthstencilview"></a><span data-ttu-id="19830-206">ID3D11Device:: "dashboardepthstencilview"</span><span class="sxs-lookup"><span data-stu-id="19830-206">ID3D11Device::CreateDepthStencilView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="19830-207">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-207">Feature Level</span></span></th>
<th><span data-ttu-id="19830-208">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="19830-208">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19830-209">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="19830-209">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="19830-210">Unterstützt keine zweiseitige Schablone. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="19830-210">Does not support two-sided stencil.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="19830-211">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="19830-211">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="19830-212">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="19830-212">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatedomainshader"></a><span data-ttu-id="19830-213">ID3D11Device:: kreatedomainshader</span><span class="sxs-lookup"><span data-stu-id="19830-213">ID3D11Device::CreateDomainShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="19830-214">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-214">Feature Level</span></span></th>
<th><span data-ttu-id="19830-215">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="19830-215">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19830-216">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="19830-216">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="19830-217">Wird auf keiner 9. \*-oder 10. \*-Funktionsebene unterstützt.</span><span class="sxs-lookup"><span data-stu-id="19830-217">Not supported on any 9.\* or 10.\* feature level.</span></span> <span data-ttu-id="19830-218">$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="19830-218">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="19830-219">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="19830-219">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="19830-220">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="19830-220">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="19830-221">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="19830-221">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="19830-222">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="19830-222">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreategeometryshader"></a><span data-ttu-id="19830-223">ID3D11Device:: kreategeometryshader</span><span class="sxs-lookup"><span data-stu-id="19830-223">ID3D11Device::CreateGeometryShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="19830-224">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-224">Feature Level</span></span></th>
<th><span data-ttu-id="19830-225">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="19830-225">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19830-226">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="19830-226">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="19830-227">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="19830-227">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="19830-228">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="19830-228">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="19830-229">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="19830-229">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreategeometryshaderwithstreamoutput"></a><span data-ttu-id="19830-230">ID3D11Device:: kreategeometryshaderwithstreamoutput</span><span class="sxs-lookup"><span data-stu-id="19830-230">ID3D11Device::CreateGeometryShaderWithStreamOutput</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="19830-231">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-231">Feature Level</span></span></th>
<th><span data-ttu-id="19830-232">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="19830-232">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19830-233">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="19830-233">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="19830-234">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="19830-234">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="19830-235">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="19830-235">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="19830-236">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="19830-236">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatehullshader"></a><span data-ttu-id="19830-237">ID3D11Device:: kreatehullshader</span><span class="sxs-lookup"><span data-stu-id="19830-237">ID3D11Device::CreateHullShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="19830-238">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-238">Feature Level</span></span></th>
<th><span data-ttu-id="19830-239">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="19830-239">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19830-240">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="19830-240">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="19830-241">Wird auf keiner 9. \*-oder 10. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="19830-241">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="19830-242">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="19830-242">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="19830-243">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="19830-243">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="19830-244">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="19830-244">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="19830-245">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="19830-245">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateinputlayout"></a><span data-ttu-id="19830-246">ID3D11Device:: kreatinput Layout</span><span class="sxs-lookup"><span data-stu-id="19830-246">ID3D11Device::CreateInputLayout</span></span>



| <span data-ttu-id="19830-247">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-247">Feature Level</span></span>             | <span data-ttu-id="19830-248">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="19830-248">Behavior Differences</span></span>                                                                                              |
|---------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19830-249">D3D \_ \_ Featureebene \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="19830-249">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="19830-250">Unterstützt keine D3D11 \_ - \_ Eingaben \_ pro \_ Instanzdaten.</span><span class="sxs-lookup"><span data-stu-id="19830-250">Does not support D3D11\_INPUT\_PER\_INSTANCE\_DATA</span></span>                                                                |
| <span data-ttu-id="19830-251">D3D \_ \_ Featureebene \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="19830-251">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="19830-252">Unterstützt keine D3D11 \_ - \_ Eingaben \_ pro \_ Instanzdaten.</span><span class="sxs-lookup"><span data-stu-id="19830-252">Does not support D3D11\_INPUT\_PER\_INSTANCE\_DATA</span></span>                                                                |
| <span data-ttu-id="19830-253">D3D \_ \_ Featureebene \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="19830-253">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="19830-254">Der Vertex-Stream 0 (null) muss über D3D11 \_ input \_ pro \_ Scheitelpunkt \_ Daten verfügen, wenn Datenströme D3D11- \_ Eingaben \_ pro \_ Scheitelpunkt \_ Daten aufweisen</span><span class="sxs-lookup"><span data-stu-id="19830-254">Vertex stream zero must have D3D11\_INPUT\_PER\_VERTEX\_DATA, if any streams have D3D11\_INPUT\_PER\_VERTEX\_DATA</span></span> |



 

<span data-ttu-id="19830-255">Ausführliche Informationen dazu, welche Formate für Scheitelpunkt Daten auf den einzelnen featureebenen verwendet werden können, finden Sie im Diagramm Formatunterstützung nach [Funktionsebene](overviews-direct3d-11-devices-downlevel-intro.md) .</span><span class="sxs-lookup"><span data-stu-id="19830-255">See the format support by [feature level chart](overviews-direct3d-11-devices-downlevel-intro.md) for details on what formats can be used for vertex data at each feature level.</span></span>

## <a name="id3d11devicecreatepixelshader"></a><span data-ttu-id="19830-256">ID3D11Device:: kreatepixelshader</span><span class="sxs-lookup"><span data-stu-id="19830-256">ID3D11Device::CreatePixelShader</span></span>



| <span data-ttu-id="19830-257">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-257">Feature Level</span></span>             | <span data-ttu-id="19830-258">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="19830-258">Behavior Differences</span></span>                                    |
|---------------------------|---------------------------------------------------------|
| <span data-ttu-id="19830-259">D3D \_ \_ Featureebene \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="19830-259">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="19830-260">Muss PS \_ 4 \_ 0 \_ Ebene \_ 9 \_ 1 verwenden</span><span class="sxs-lookup"><span data-stu-id="19830-260">Must use ps\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="19830-261">D3D \_ \_ Featureebene \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="19830-261">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="19830-262">Muss PS \_ 4 \_ 0 \_ Ebene \_ 9 \_ 1 verwenden</span><span class="sxs-lookup"><span data-stu-id="19830-262">Must use ps\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="19830-263">D3D \_ \_ Featureebene \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="19830-263">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="19830-264">Muss PS \_ 4 \_ 0 \_ Ebene \_ 9 \_ 3 oder PS \_ 4 \_ 0 \_ Ebene \_ 9 \_ 1 verwenden</span><span class="sxs-lookup"><span data-stu-id="19830-264">Must use ps\_4\_0\_level\_9\_3 or ps\_4\_0\_level\_9\_1</span></span> |



 

## <a name="id3d11devicecreatepredicate"></a><span data-ttu-id="19830-265">ID3D11Device:: kreatepredicate</span><span class="sxs-lookup"><span data-stu-id="19830-265">ID3D11Device::CreatePredicate</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="19830-266">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-266">Feature Level</span></span></th>
<th><span data-ttu-id="19830-267">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="19830-267">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19830-268">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="19830-268">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="19830-269">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="19830-269">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="19830-270">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="19830-270">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="19830-271">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="19830-271">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatequery"></a><span data-ttu-id="19830-272">ID3D11Device:: kreatequery</span><span class="sxs-lookup"><span data-stu-id="19830-272">ID3D11Device::CreateQuery</span></span>



| <span data-ttu-id="19830-273">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-273">Feature Level</span></span>             | <span data-ttu-id="19830-274">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="19830-274">Behavior Differences</span></span>                                                                                                                                  |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19830-275">D3D \_ \_ Featureebene \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="19830-275">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="19830-276">Ereignis Abfragen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="19830-276">Event queries are supported.</span></span> <span data-ttu-id="19830-277">Timestamp-Abfragen sind optional: Aufrufen von " [**kreatequery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) " zum Ermitteln der Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="19830-277">Timestamp queries are optional: call [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) to determine support.</span></span>               |
| <span data-ttu-id="19830-278">D3D \_ \_ Featureebene \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="19830-278">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="19830-279">Ereignis-und oksions Abfragen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="19830-279">Event and occlusion queries are supported.</span></span> <span data-ttu-id="19830-280">Timestamp-Abfragen sind optional: Aufrufen von " [**kreatequery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) " zum Ermitteln der Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="19830-280">Timestamp queries are optional: call [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) to determine support.</span></span> |
| <span data-ttu-id="19830-281">D3D \_ \_ Featureebene \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="19830-281">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="19830-282">Ereignis-und oksions Abfragen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="19830-282">Event and occlusion queries are supported.</span></span> <span data-ttu-id="19830-283">Timestamp-Abfragen sind optional: Aufrufen von " [**kreatequery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) " zum Ermitteln der Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="19830-283">Timestamp queries are optional: call [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) to determine support.</span></span> |



 

## <a name="id3d11devicecreaterasterizerstate"></a><span data-ttu-id="19830-284">ID3D11Device:: kreaterasterizerstate</span><span class="sxs-lookup"><span data-stu-id="19830-284">ID3D11Device::CreateRasterizerState</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="19830-285">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-285">Feature Level</span></span></th>
<th><span data-ttu-id="19830-286">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="19830-286">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19830-287">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="19830-287">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="19830-288">"Depthclipable" muss " <strong>true</strong>" sein.</span><span class="sxs-lookup"><span data-stu-id="19830-288">DepthClipEnable must be <strong>TRUE</strong>.</span></span> <span data-ttu-id="19830-289">Depthbiasclamp muss auf 0 festgelegt werden. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="19830-289">DepthBiasClamp must be set to 0.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="19830-290">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="19830-290">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="19830-291">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="19830-291">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreaterendertargetview"></a><span data-ttu-id="19830-292">ID3D11Device:: kreaterendertargetview</span><span class="sxs-lookup"><span data-stu-id="19830-292">ID3D11Device::CreateRenderTargetView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="19830-293">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-293">Feature Level</span></span></th>
<th><span data-ttu-id="19830-294">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="19830-294">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19830-295">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="19830-295">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="19830-296">Die renderzielsichten von Texture2D-Objekten können nur unterstützt werden. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="19830-296">Can only support render target views of Texture2D objects.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="19830-297">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="19830-297">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="19830-298">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="19830-298">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatesamplerstate"></a><span data-ttu-id="19830-299">ID3D11Device:: kreatesamplerstate</span><span class="sxs-lookup"><span data-stu-id="19830-299">ID3D11Device::CreateSamplerState</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="19830-300">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-300">Feature Level</span></span></th>
<th><span data-ttu-id="19830-301">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="19830-301">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19830-302">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="19830-302">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td><span data-ttu-id="19830-303">Der Vergleichs Filter wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="19830-303">Comparison filter is not supported.</span></span><br/> <span data-ttu-id="19830-304">Die Rahmenfarbe muss innerhalb von [0, 1] liegen.</span><span class="sxs-lookup"><span data-stu-id="19830-304">Border color must be within [0,1]</span></span><br/> <span data-ttu-id="19830-305">Min. Lod kann nicht in Bruchzahlen stehen.</span><span class="sxs-lookup"><span data-stu-id="19830-305">Min LOD cannot be fractional</span></span><br/> <span data-ttu-id="19830-306">Der maximale Lod-Wert muss FLT_MAX</span><span class="sxs-lookup"><span data-stu-id="19830-306">Max LOD must be FLT_MAX</span></span><br/> <span data-ttu-id="19830-307">Maximale Anisotropie ist 2.</span><span class="sxs-lookup"><span data-stu-id="19830-307">Maximum anisotropy is 2.</span></span><br/> <span data-ttu-id="19830-308">D3D11_TEXTURE_ADDRESS_MIRRORONCE nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="19830-308">D3D11_TEXTURE_ADDRESS_MIRRORONCE not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19830-309">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="19830-309">D3D_FEATURE_LEVEL_9_2</span></span></td>
<td rowspan="2"> <span data-ttu-id="19830-310">Der Vergleichs Filter wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="19830-310">Comparison filter is not supported.</span></span><br/> <span data-ttu-id="19830-311">Die Rahmenfarbe muss innerhalb von [0, 1] liegen.</span><span class="sxs-lookup"><span data-stu-id="19830-311">Border color must be within [0,1]</span></span><br/> <span data-ttu-id="19830-312">Min. Lod kann nicht in Bruchzahlen stehen.</span><span class="sxs-lookup"><span data-stu-id="19830-312">Min LOD cannot be fractional</span></span><br/> <span data-ttu-id="19830-313">Der maximale Lod-Wert muss FLT_MAX</span><span class="sxs-lookup"><span data-stu-id="19830-313">Max LOD must be FLT_MAX</span></span><br/> <span data-ttu-id="19830-314">Die maximale Anzahl von Anisotropie beträgt 16.</span><span class="sxs-lookup"><span data-stu-id="19830-314">Maximum anisotropy is 16.</span></span><br/> <span data-ttu-id="19830-315">$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="19830-315">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19830-316">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="19830-316">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateshaderresourceview"></a><span data-ttu-id="19830-317">ID3D11Device:: kreateshaderresourceview</span><span class="sxs-lookup"><span data-stu-id="19830-317">ID3D11Device::CreateShaderResourceView</span></span>



| <span data-ttu-id="19830-318">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-318">Feature Level</span></span>             | <span data-ttu-id="19830-319">"Wstdetailedmip Plus miplevels" muss die niedrigste "LOD" (kleinste unter Quelle) enthalten.</span><span class="sxs-lookup"><span data-stu-id="19830-319">MostDetailedMip plus MipLevels must include lowest LOD (smallest subresource</span></span> | <span data-ttu-id="19830-320">Die Ansicht muss alle Ressourcen Array Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="19830-320">View must include all resource array elements</span></span> |
|---------------------------|------------------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="19830-321">D3D \_ \_ Featureebene \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="19830-321">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="19830-322">Ja</span><span class="sxs-lookup"><span data-stu-id="19830-322">Yes</span></span>                                                                          | <span data-ttu-id="19830-323">ja</span><span class="sxs-lookup"><span data-stu-id="19830-323">yes</span></span>                                           |
| <span data-ttu-id="19830-324">D3D \_ \_ Featureebene \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="19830-324">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="19830-325">Ja</span><span class="sxs-lookup"><span data-stu-id="19830-325">Yes</span></span>                                                                          | <span data-ttu-id="19830-326">Ja</span><span class="sxs-lookup"><span data-stu-id="19830-326">Yes</span></span>                                           |
| <span data-ttu-id="19830-327">D3D \_ \_ Featureebene \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="19830-327">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="19830-328">Ja</span><span class="sxs-lookup"><span data-stu-id="19830-328">Yes</span></span>                                                                          | <span data-ttu-id="19830-329">Ja</span><span class="sxs-lookup"><span data-stu-id="19830-329">Yes</span></span>                                           |



 

## <a name="id3d11devicecreatetexture1d"></a><span data-ttu-id="19830-330">ID3D11Device:: CreateTexture1D</span><span class="sxs-lookup"><span data-stu-id="19830-330">ID3D11Device::CreateTexture1D</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="19830-331">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-331">Feature Level</span></span></th>
<th><span data-ttu-id="19830-332">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="19830-332">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19830-333">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="19830-333">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="19830-334">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="19830-334">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="19830-335">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="19830-335">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="19830-336">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="19830-336">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatetexture2d"></a><span data-ttu-id="19830-337">ID3D11Device:: CreateTexture2D</span><span class="sxs-lookup"><span data-stu-id="19830-337">ID3D11Device::CreateTexture2D</span></span>

<span data-ttu-id="19830-338">Für Texture2D-Ressourcen gelten Grenzwerte für Breite und Höhe, die sich über die [Funktionsebenen](overviews-direct3d-11-devices-downlevel-intro.md)unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="19830-338">Texture2D resources have limits on their width and height that differ across [feature levels](overviews-direct3d-11-devices-downlevel-intro.md).</span></span> <span data-ttu-id="19830-339">In den featurestufen 9 \_ 3 ist die folgende garantierte minimieren, und einzelne Implementierungen können die Anforderungen überschreiten.</span><span class="sxs-lookup"><span data-stu-id="19830-339">In feature levels 9\_3, the following are guaranteed minima, and individual implementations may exceed the requirements.</span></span>



| <span data-ttu-id="19830-340">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-340">Feature Level</span></span>             | <span data-ttu-id="19830-341">Wenn mipcount > 1, müssen Dimensionen eine ganzzahlige Potenz von zwei sein.</span><span class="sxs-lookup"><span data-stu-id="19830-341">If MipCount > 1, Dimensions must be integral power of two</span></span> | <span data-ttu-id="19830-342">Mindestens unterstützte Textur Dimension</span><span class="sxs-lookup"><span data-stu-id="19830-342">Minimum supported texture dimension</span></span> | <span data-ttu-id="19830-343">Cubetexturen-Dimensionen müssen eine Potenz von zwei sein.</span><span class="sxs-lookup"><span data-stu-id="19830-343">Cube textures dimensions must be power of two</span></span> | <span data-ttu-id="19830-344">Wenn "misc \_ texturecube" festgelegt ist, lautet arraySize:</span><span class="sxs-lookup"><span data-stu-id="19830-344">If MISC\_TEXTURECUBE is set, the ArraySize is:</span></span> | <span data-ttu-id="19830-345">Wenn "misc \_ texturecube" nicht festgelegt ist, ist "arraySize".</span><span class="sxs-lookup"><span data-stu-id="19830-345">If MISC\_TEXTURECUBE is not set, the ArraySize is.</span></span> |
|---------------------------|--------------------------------------------------------------|-------------------------------------|-----------------------------------------------|------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="19830-346">D3D \_ \_ Featureebene \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="19830-346">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="19830-347">Ja</span><span class="sxs-lookup"><span data-stu-id="19830-347">Yes</span></span>                                                          | <span data-ttu-id="19830-348">2048</span><span class="sxs-lookup"><span data-stu-id="19830-348">2048</span></span>                                | <span data-ttu-id="19830-349">Ja</span><span class="sxs-lookup"><span data-stu-id="19830-349">Yes</span></span>                                           | <span data-ttu-id="19830-350">6</span><span class="sxs-lookup"><span data-stu-id="19830-350">6</span></span>                                              | <span data-ttu-id="19830-351">1</span><span class="sxs-lookup"><span data-stu-id="19830-351">1</span></span>                                                  |
| <span data-ttu-id="19830-352">D3D \_ \_ Featureebene \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="19830-352">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="19830-353">Ja</span><span class="sxs-lookup"><span data-stu-id="19830-353">Yes</span></span>                                                          | <span data-ttu-id="19830-354">2048</span><span class="sxs-lookup"><span data-stu-id="19830-354">2048</span></span>                                | <span data-ttu-id="19830-355">Ja</span><span class="sxs-lookup"><span data-stu-id="19830-355">Yes</span></span>                                           | <span data-ttu-id="19830-356">6</span><span class="sxs-lookup"><span data-stu-id="19830-356">6</span></span>                                              | <span data-ttu-id="19830-357">1</span><span class="sxs-lookup"><span data-stu-id="19830-357">1</span></span>                                                  |
| <span data-ttu-id="19830-358">D3D \_ \_ Featureebene \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="19830-358">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="19830-359">Ja</span><span class="sxs-lookup"><span data-stu-id="19830-359">Yes</span></span>                                                          | <span data-ttu-id="19830-360">4096</span><span class="sxs-lookup"><span data-stu-id="19830-360">4096</span></span>                                | <span data-ttu-id="19830-361">Ja</span><span class="sxs-lookup"><span data-stu-id="19830-361">Yes</span></span>                                           | <span data-ttu-id="19830-362">6</span><span class="sxs-lookup"><span data-stu-id="19830-362">6</span></span>                                              | <span data-ttu-id="19830-363">1</span><span class="sxs-lookup"><span data-stu-id="19830-363">1</span></span>                                                  |



 

<span data-ttu-id="19830-364">In der vorherigen Tabelle lautet der vollständige Name von **misc \_ texturecube** [**D3D11 \_ Resource \_ misc \_ texturecube**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag).</span><span class="sxs-lookup"><span data-stu-id="19830-364">In the previous table, the full name of **MISC\_TEXTURECUBE** is [**D3D11\_RESOURCE\_MISC\_TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag).</span></span>

<span data-ttu-id="19830-365">Folgendes gilt für alle 9 \_ \* [Funktionsebenen](overviews-direct3d-11-devices-downlevel-intro.md):</span><span class="sxs-lookup"><span data-stu-id="19830-365">The following are true for all 9\_\* [feature levels](overviews-direct3d-11-devices-downlevel-intro.md):</span></span>

-   <span data-ttu-id="19830-366">Bei Verwendung von "D3D11 \_ Usage \_ default" oder "D3D11 \_ Usage" kann " \_ bindflags" nicht gleich NULL sein.</span><span class="sxs-lookup"><span data-stu-id="19830-366">When using D3D11\_USAGE\_DEFAULT or D3D11\_USAGE\_IMMUTABLE, BindFlags cannot be zero.</span></span>
-   <span data-ttu-id="19830-367">Bei Verwendung der D3D11 \_ Bind- \_ tiefen \_ Schablone muss miplevels 1 sein.</span><span class="sxs-lookup"><span data-stu-id="19830-367">When using D3D11\_BIND\_DEPTH\_STENCIL, MipLevels must be 1.</span></span>
-   <span data-ttu-id="19830-368">Bei Verwendung der D3D11 \_ Bind- \_ Shader- \_ Ressource muss sampledebug. Count 1 sein.</span><span class="sxs-lookup"><span data-stu-id="19830-368">When using D3D11\_BIND\_SHADER\_RESOURCE, SampleDesc.Count must be 1.</span></span>
-   <span data-ttu-id="19830-369">Wenn D3D11 \_ Bind \_ vorhanden ist, kann die Ressource keine D3D11 \_ Bind- \_ Shader-Ressource aufweisen \_ .</span><span class="sxs-lookup"><span data-stu-id="19830-369">When using D3D11\_BIND\_PRESENT, resource cannot have D3D11\_BIND\_SHADER\_RESOURCE.</span></span>
-   <span data-ttu-id="19830-370">Bei Verwendung von "d3d10 \_ DDI \_ Resource \_ misc \_ Shared" kann das Format nicht im DXGI- \_ Format vorliegen \_ R8G8B8A8 \_ unorm-oder DXGI- \_ Format \_ R8G8B8A8 \_ unorm \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="19830-370">When using D3D10\_DDI\_RESOURCE\_MISC\_SHARED, Format cannot be DXGI\_FORMAT\_R8G8B8A8\_UNORM or DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB.</span></span>

## <a name="id3d11devicecreatetexture3d"></a><span data-ttu-id="19830-371">ID3D11Device:: CreateTexture3D</span><span class="sxs-lookup"><span data-stu-id="19830-371">ID3D11Device::CreateTexture3D</span></span>



| <span data-ttu-id="19830-372">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-372">Feature Level</span></span>             | <span data-ttu-id="19830-373">Maximale Dimension (beliebige Achse)</span><span class="sxs-lookup"><span data-stu-id="19830-373">Maximum Dimension (any axis)</span></span> | <span data-ttu-id="19830-374">Dimensionen müssen eine Potenz von zwei sein.</span><span class="sxs-lookup"><span data-stu-id="19830-374">Dimensions must be power of two</span></span> |
|---------------------------|------------------------------|---------------------------------|
| <span data-ttu-id="19830-375">D3D \_ \_ Featureebene \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="19830-375">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="19830-376">256</span><span class="sxs-lookup"><span data-stu-id="19830-376">256</span></span>                          | <span data-ttu-id="19830-377">Ja</span><span class="sxs-lookup"><span data-stu-id="19830-377">Yes</span></span>                             |
| <span data-ttu-id="19830-378">D3D \_ \_ Featureebene \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="19830-378">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="19830-379">512</span><span class="sxs-lookup"><span data-stu-id="19830-379">512</span></span>                          | <span data-ttu-id="19830-380">Ja</span><span class="sxs-lookup"><span data-stu-id="19830-380">Yes</span></span>                             |
| <span data-ttu-id="19830-381">D3D \_ \_ Featureebene \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="19830-381">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="19830-382">512</span><span class="sxs-lookup"><span data-stu-id="19830-382">512</span></span>                          | <span data-ttu-id="19830-383">Ja</span><span class="sxs-lookup"><span data-stu-id="19830-383">Yes</span></span>                             |



 

<span data-ttu-id="19830-384">Wenn Resource D3D11 \_ Usage \_ default oder D3D11 \_ Usage \_ unveränderlich ist, kann bindflags nicht gleich NULL sein.</span><span class="sxs-lookup"><span data-stu-id="19830-384">If resource is D3D11\_USAGE\_DEFAULT or D3D11\_USAGE\_IMMUTABLE, BindFlags cannot be zero.</span></span>

## <a name="id3d11devicecreateunorderedaccessview"></a><span data-ttu-id="19830-385">ID3D11Device:: kreateunorderedaccessview</span><span class="sxs-lookup"><span data-stu-id="19830-385">ID3D11Device::CreateUnorderedAccessView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="19830-386">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-386">Feature Level</span></span></th>
<th><span data-ttu-id="19830-387">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="19830-387">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19830-388">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="19830-388">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="19830-389">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="19830-389">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="19830-390">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="19830-390">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="19830-391">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="19830-391">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatevertexshader"></a><span data-ttu-id="19830-392">ID3D11Device:: kreatevertexshader</span><span class="sxs-lookup"><span data-stu-id="19830-392">ID3D11Device::CreateVertexShader</span></span>



| <span data-ttu-id="19830-393">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-393">Feature Level</span></span>             | <span data-ttu-id="19830-394">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="19830-394">Behavior Differences</span></span>                                    |
|---------------------------|---------------------------------------------------------|
| <span data-ttu-id="19830-395">D3D \_ \_ Featureebene \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="19830-395">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="19830-396">Muss vs \_ 4 \_ 0 \_ Ebene \_ 9 \_ 1 verwenden</span><span class="sxs-lookup"><span data-stu-id="19830-396">Must use vs\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="19830-397">D3D \_ \_ Featureebene \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="19830-397">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="19830-398">Muss vs \_ 4 \_ 0 \_ Ebene \_ 9 \_ 1 verwenden</span><span class="sxs-lookup"><span data-stu-id="19830-398">Must use vs\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="19830-399">D3D \_ \_ Featureebene \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="19830-399">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="19830-400">Muss vs \_ 4 \_ 0 \_ Level \_ 9 \_ 3 oder vs \_ 4 \_ 0 \_ Level \_ 9 \_ 1 verwenden.</span><span class="sxs-lookup"><span data-stu-id="19830-400">Must use vs\_4\_0\_level\_9\_3 or vs\_4\_0\_level\_9\_1</span></span> |



 

## <a name="id3d11deviceopensharedresource"></a><span data-ttu-id="19830-401">ID3D11Device:: opensharedresource</span><span class="sxs-lookup"><span data-stu-id="19830-401">ID3D11Device::OpenSharedResource</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="19830-402">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="19830-402">Feature Level</span></span></th>
<th><span data-ttu-id="19830-403">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="19830-403">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19830-404">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="19830-404">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"> <span data-ttu-id="19830-405">Verwenden Sie <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device:: checkfeaturesupport</strong></a> mit dem <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2</strong></a> Wert und der <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a> Struktur, um zu bestimmen, ob ein Format freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="19830-405">Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device::CheckFeatureSupport</strong></a> with the <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2</strong></a> value and the <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a> structure to determine if a format can be shared.</span></span> <span data-ttu-id="19830-406">Wenn das Format freigegeben werden kann, gibt <strong>checkfeaturesupport</strong> das <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2_SHAREABLE</strong></a> -Flag zurück.</span><span class="sxs-lookup"><span data-stu-id="19830-406">If the format can be shared, <strong>CheckFeatureSupport</strong> returns the <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2_SHAREABLE</strong></a> flag.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="19830-407">[<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>] (/Windows/Desktop/API/dxgiformat/ne-dxgiformat-dxgi_format) und <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> sind bei Verwendung von Featureebene 9 niemals freistellbar, auch wenn das Gerät optionale Funktions Unterstützung für <strong>D3D11_FORMAT_SUPPORT_SHAREABLE</strong>angibt.</span><span class="sxs-lookup"><span data-stu-id="19830-407">[<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) and <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> are never shareable when using feature level 9, even if the device indicates optional feature support for <strong>D3D11_FORMAT_SUPPORT_SHAREABLE</strong>.</span></span> <span data-ttu-id="19830-408">Der Versuch, freigegebene Ressourcen mit DXGI-Formaten <strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong> und <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> zu erstellen, schlägt immer fehl, es sei denn, die Funktionsebene ist 10_0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="19830-408">Attempting to create shared resources with DXGI formats <strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong> and <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> will always fail unless the feature level is 10_0 or higher.</span></span>
</blockquote>
<br/> <span data-ttu-id="19830-409">$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="19830-409">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="19830-410">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="19830-410">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="19830-411">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="19830-411">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="19830-412">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="19830-412">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19830-413">10level9-Referenz</span><span class="sxs-lookup"><span data-stu-id="19830-413">10Level9 Reference</span></span>](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

