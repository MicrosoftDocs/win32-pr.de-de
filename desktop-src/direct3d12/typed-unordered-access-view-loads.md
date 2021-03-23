---
title: Typisierte UAV-Ladevorgänge (unsortierter Zugriffs Ansicht)
description: Die gegebene UAV-Auslastung (unsortierter Zugriffs Ansicht) ist die Fähigkeit eines Shaders, aus einer UAV mit einem bestimmten DXGI-Format zu lesen \_ .
ms.assetid: 6106D15E-EAF6-4583-B4F2-7CC7EE30DE15
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4adfd7511590a43b7f87507c5a1e0a2a87c925b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548674"
---
# <a name="typed-unordered-access-view-uav-loads"></a><span data-ttu-id="adadb-103">Typisierte UAV-Ladevorgänge (unsortierter Zugriffs Ansicht)</span><span class="sxs-lookup"><span data-stu-id="adadb-103">Typed unordered access view (UAV) loads</span></span>

<span data-ttu-id="adadb-104">Die gegebene UAV-Auslastung (unsortierter Zugriffs Ansicht) ist die Fähigkeit eines Shaders, aus einer UAV mit einem bestimmten [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)zu lesen.</span><span class="sxs-lookup"><span data-stu-id="adadb-104">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

-   [<span data-ttu-id="adadb-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="adadb-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="adadb-106">Unterstützte Formate und API-Aufrufe</span><span class="sxs-lookup"><span data-stu-id="adadb-106">Supported formats and API calls</span></span>](#supported-formats-and-api-calls)
-   [<span data-ttu-id="adadb-107">Verwenden von typisierten UAV-Ladungen aus HLSL</span><span class="sxs-lookup"><span data-stu-id="adadb-107">Using typed UAV loads from HLSL</span></span>](#using-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="adadb-108">Verwenden von unorm-und snorm-typisierten UAV-Ladungen aus HLSL</span><span class="sxs-lookup"><span data-stu-id="adadb-108">Using UNORM and SNORM typed UAV loads from HLSL</span></span>](#using-unorm-and-snorm-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="adadb-109">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="adadb-109">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="adadb-110">Überblick</span><span class="sxs-lookup"><span data-stu-id="adadb-110">Overview</span></span>

<span data-ttu-id="adadb-111">Eine ungeordnete Zugriffs Ansicht (UAV) ist eine Ansicht einer unsorierten Zugriffs Ressource (die auch Puffer, Texturen und Textur Arrays enthalten kann, ohne Multisampling).</span><span class="sxs-lookup"><span data-stu-id="adadb-111">An unordered access view (UAV) is a view of an unordered access resource (which can include buffers, textures, and texture arrays, though without multi-sampling).</span></span> <span data-ttu-id="adadb-112">Eine UAV ermöglicht Temporale ungeordnete Lese-/Schreibzugriffe aus mehreren Threads.</span><span class="sxs-lookup"><span data-stu-id="adadb-112">A UAV allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="adadb-113">Dies bedeutet, dass dieser Ressourcentyp gleichzeitig von mehreren Threads gelesen/geschrieben werden kann, ohne dass Speicher Konflikte entstehen.</span><span class="sxs-lookup"><span data-stu-id="adadb-113">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span> <span data-ttu-id="adadb-114">Dieser gleichzeitige Zugriff wird durch die Verwendung von [atomaren Funktionen](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions)gehandhabt.</span><span class="sxs-lookup"><span data-stu-id="adadb-114">This simultaneous access is handled through the use of [Atomic Functions](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span></span>

<span data-ttu-id="adadb-115">D3D12 (und D3D 11.3) erweitert die Liste der Formate, die mit typisierten UAV-Ladevorgängen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="adadb-115">D3D12 (and D3D11.3) expands on the list of formats that can be used with typed UAV loads.</span></span>

## <a name="supported-formats-and-api-calls"></a><span data-ttu-id="adadb-116">Unterstützte Formate und API-Aufrufe</span><span class="sxs-lookup"><span data-stu-id="adadb-116">Supported formats and API calls</span></span>

<span data-ttu-id="adadb-117">Bisher unterstützten die folgenden drei Formate typisierte UAV-Ladungen und waren für die D3D 11.0-Hardware erforderlich.</span><span class="sxs-lookup"><span data-stu-id="adadb-117">Previously, the following three formats supported typed UAV loads, and were required for D3D11.0 hardware.</span></span> <span data-ttu-id="adadb-118">Sie werden für alle D3D 11.3-und D3D12-Hardware unterstützt.</span><span class="sxs-lookup"><span data-stu-id="adadb-118">They are supported for all D3D11.3 and D3D12 hardware.</span></span>

-   <span data-ttu-id="adadb-119">R32 \_ float</span><span class="sxs-lookup"><span data-stu-id="adadb-119">R32\_FLOAT</span></span>
-   <span data-ttu-id="adadb-120">R32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="adadb-120">R32\_UINT</span></span>
-   <span data-ttu-id="adadb-121">R32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="adadb-121">R32\_SINT</span></span>

<span data-ttu-id="adadb-122">Die folgenden Formate werden als Satz auf D3D12-oder D3D 11.3-Hardware unterstützt. Wenn eine solche unterstützt wird, werden alle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="adadb-122">The following formats are supported as a set on D3D12 or D3D11.3 hardware, so if any one is supported, all are supported.</span></span>

-   <span data-ttu-id="adadb-123">R32G32B32A32 \_ float</span><span class="sxs-lookup"><span data-stu-id="adadb-123">R32G32B32A32\_FLOAT</span></span>
-   <span data-ttu-id="adadb-124">R32G32B32A32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="adadb-124">R32G32B32A32\_UINT</span></span>
-   <span data-ttu-id="adadb-125">R32G32B32A32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="adadb-125">R32G32B32A32\_SINT</span></span>
-   <span data-ttu-id="adadb-126">R16G16B16A16 \_ float</span><span class="sxs-lookup"><span data-stu-id="adadb-126">R16G16B16A16\_FLOAT</span></span>
-   <span data-ttu-id="adadb-127">R16G16B16A16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="adadb-127">R16G16B16A16\_UINT</span></span>
-   <span data-ttu-id="adadb-128">R16G16B16A16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="adadb-128">R16G16B16A16\_SINT</span></span>
-   <span data-ttu-id="adadb-129">R8G8B8A8 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="adadb-129">R8G8B8A8\_UNORM</span></span>
-   <span data-ttu-id="adadb-130">R8G8B8A8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="adadb-130">R8G8B8A8\_UINT</span></span>
-   <span data-ttu-id="adadb-131">R8G8B8A8 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="adadb-131">R8G8B8A8\_SINT</span></span>
-   <span data-ttu-id="adadb-132">R16 \_ float</span><span class="sxs-lookup"><span data-stu-id="adadb-132">R16\_FLOAT</span></span>
-   <span data-ttu-id="adadb-133">R16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="adadb-133">R16\_UINT</span></span>
-   <span data-ttu-id="adadb-134">R16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="adadb-134">R16\_SINT</span></span>
-   <span data-ttu-id="adadb-135">R8- \_ unorm</span><span class="sxs-lookup"><span data-stu-id="adadb-135">R8\_UNORM</span></span>
-   <span data-ttu-id="adadb-136">R8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="adadb-136">R8\_UINT</span></span>
-   <span data-ttu-id="adadb-137">R8 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="adadb-137">R8\_SINT</span></span>

<span data-ttu-id="adadb-138">Die folgenden Formate werden optional und einzeln auf D3D12-und D3D 11.3-Hardware unterstützt. Daher muss eine einzelne Abfrage für jedes Format durchgeführt werden, um die Unterstützung zu testen.</span><span class="sxs-lookup"><span data-stu-id="adadb-138">The following formats are optionally and individually supported on D3D12 and D3D11.3 hardware, so a single query would need to be made on each format to test for support.</span></span>

-   <span data-ttu-id="adadb-139">R16G16B16A16 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="adadb-139">R16G16B16A16\_UNORM</span></span>
-   <span data-ttu-id="adadb-140">R16G16B16A16 \_ snorm</span><span class="sxs-lookup"><span data-stu-id="adadb-140">R16G16B16A16\_SNORM</span></span>
-   <span data-ttu-id="adadb-141">R32G32 \_ float</span><span class="sxs-lookup"><span data-stu-id="adadb-141">R32G32\_FLOAT</span></span>
-   <span data-ttu-id="adadb-142">R32G32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="adadb-142">R32G32\_UINT</span></span>
-   <span data-ttu-id="adadb-143">R32G32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="adadb-143">R32G32\_SINT</span></span>
-   <span data-ttu-id="adadb-144">R10G10B10A2 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="adadb-144">R10G10B10A2\_UNORM</span></span>
-   <span data-ttu-id="adadb-145">R10G10B10A2 \_ uint</span><span class="sxs-lookup"><span data-stu-id="adadb-145">R10G10B10A2\_UINT</span></span>
-   <span data-ttu-id="adadb-146">R11G11B10 \_ float</span><span class="sxs-lookup"><span data-stu-id="adadb-146">R11G11B10\_FLOAT</span></span>
-   <span data-ttu-id="adadb-147">R8G8B8A8 \_ snorm</span><span class="sxs-lookup"><span data-stu-id="adadb-147">R8G8B8A8\_SNORM</span></span>
-   <span data-ttu-id="adadb-148">R16G16 \_ float</span><span class="sxs-lookup"><span data-stu-id="adadb-148">R16G16\_FLOAT</span></span>
-   <span data-ttu-id="adadb-149">R16G16 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="adadb-149">R16G16\_UNORM</span></span>
-   <span data-ttu-id="adadb-150">R16G16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="adadb-150">R16G16\_UINT</span></span>
-   <span data-ttu-id="adadb-151">R16G16 \_ snorm</span><span class="sxs-lookup"><span data-stu-id="adadb-151">R16G16\_SNORM</span></span>
-   <span data-ttu-id="adadb-152">R16G16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="adadb-152">R16G16\_SINT</span></span>
-   <span data-ttu-id="adadb-153">R8G8 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="adadb-153">R8G8\_UNORM</span></span>
-   <span data-ttu-id="adadb-154">R8G8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="adadb-154">R8G8\_UINT</span></span>
-   <span data-ttu-id="adadb-155">R8G8 \_ snorm</span><span class="sxs-lookup"><span data-stu-id="adadb-155">R8G8\_SNORM</span></span>
-   <span data-ttu-id="adadb-156">R8G8 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="adadb-156">R8G8\_SINT</span></span>
-   <span data-ttu-id="adadb-157">R16 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="adadb-157">R16\_UNORM</span></span>
-   <span data-ttu-id="adadb-158">R16 \_ snorm</span><span class="sxs-lookup"><span data-stu-id="adadb-158">R16\_SNORM</span></span>
-   <span data-ttu-id="adadb-159">R8 \_ snorm</span><span class="sxs-lookup"><span data-stu-id="adadb-159">R8\_SNORM</span></span>
-   <span data-ttu-id="adadb-160">A8- \_ unorm</span><span class="sxs-lookup"><span data-stu-id="adadb-160">A8\_UNORM</span></span>
-   <span data-ttu-id="adadb-161">B5G6R5 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="adadb-161">B5G6R5\_UNORM</span></span>
-   <span data-ttu-id="adadb-162">B5G5R5A1 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="adadb-162">B5G5R5A1\_UNORM</span></span>
-   <span data-ttu-id="adadb-163">B4G4R4A4 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="adadb-163">B4G4R4A4\_UNORM</span></span>

<span data-ttu-id="adadb-164">Um die Unterstützung für weitere Formate zu ermitteln, müssen Sie [**checkfeaturesupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) mit der [**D3D12 \_ Feature \_ Data \_ D3D12 \_ options**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) -Struktur als ersten Parameter aufrufen (siehe Funktions [Abfrage](capability-querying.md)).</span><span class="sxs-lookup"><span data-stu-id="adadb-164">To determine the support for any additional formats, call [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) with the [**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) structure as the first parameter (refer to [Capability Querying](capability-querying.md)).</span></span> <span data-ttu-id="adadb-165">Das Feld *typeduavloadadditionalformats* wird festgelegt, wenn die oben genannte Liste als Satz unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="adadb-165">The *TypedUAVLoadAdditionalFormats* field will be set if the "supported as a set" list above is supported.</span></span> <span data-ttu-id="adadb-166">Erstellen Sie einen zweiten aufrufungstyp **, indem Sie** eine [**D3D12 \_ Feature \_ Data \_ Format- \_ Unterstützungs**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) Struktur verwenden (Überprüfen der zurückgegebenen Struktur mit dem D3D12- \_ Format \_ SUPPORT2 \_ UAV \_ typisiertes \_ Load-Member des [**D3D12- \_ Formats \_ SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) Enum), um die Unterstützung in der Liste der optional unterstützten, oben aufgeführten Formate zu ermitteln, z. b.:</span><span class="sxs-lookup"><span data-stu-id="adadb-166">Make a second call to **CheckFeatureSupport**, using a [**D3D12\_FEATURE\_DATA\_FORMAT\_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) structure (checking the returned structure against the D3D12\_FORMAT\_SUPPORT2\_UAV\_TYPED\_LOAD member of the [**D3D12\_FORMAT\_SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) enum) to determine support in the list of optionally supported formats listed above, for example:</span></span>

``` syntax
D3D12_FEATURE_DATA_D3D12_OPTIONS FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Cannot assume other formats are supported, so we check:
        D3D12_FEATURE_DATA_FORMAT_SUPPORT FormatSupport = {DXGI_FORMAT_R32G32_FLOAT, D3D12_FORMAT_SUPPORT1_NONE, D3D12_FORMAT_SUPPORT2_NONE};
        hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_FORMAT_SUPPORT, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.Support2 & D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
        {
            // DXGI_FORMAT_R32G32_FLOAT supports UAV Typed Load!
        }
    }
}
```

## <a name="using-typed-uav-loads-from-hlsl"></a><span data-ttu-id="adadb-167">Verwenden von typisierten UAV-Ladungen aus HLSL</span><span class="sxs-lookup"><span data-stu-id="adadb-167">Using typed UAV loads from HLSL</span></span>

<span data-ttu-id="adadb-168">Bei typisierten UAVs ist das HLSL-Flag D3D \_ Shader \_ erfordert ein \_ typisiertes \_ UAV- \_ Laden \_ zusätzlicher \_ Formate.</span><span class="sxs-lookup"><span data-stu-id="adadb-168">For typed UAVs, the HLSL flag is D3D\_SHADER\_REQUIRES\_TYPED\_UAV\_LOAD\_ADDITIONAL\_FORMATS.</span></span>

<span data-ttu-id="adadb-169">Dies ist beispielsweise ein Shader-Code, der eine typisierte UAV-Auslastung verarbeitet:</span><span class="sxs-lookup"><span data-stu-id="adadb-169">Here is example shader code to process a typed UAV load:</span></span>

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="using-unorm-and-snorm-typed-uav-loads-from-hlsl"></a><span data-ttu-id="adadb-170">Verwenden von unorm-und snorm-typisierten UAV-Ladungen aus HLSL</span><span class="sxs-lookup"><span data-stu-id="adadb-170">Using UNORM and SNORM typed UAV loads from HLSL</span></span>

<span data-ttu-id="adadb-171">Wenn Sie typisierte UAV-Ladungen zum Lesen aus einer unorm-oder snorm-Ressource verwenden, müssen Sie den Elementtyp des HLSL-Objekts ordnungsgemäß als oder deklarieren `unorm` `snorm` .</span><span class="sxs-lookup"><span data-stu-id="adadb-171">When using typed UAV loads to read from a UNORM or SNORM resource, you must properly declare the element type of the HLSL object to be `unorm` or `snorm`.</span></span> <span data-ttu-id="adadb-172">Sie wird als nicht definiertes Verhalten angegeben, um den in HLSL deklarierten Elementtyp mit dem zugrunde liegenden Ressourcen Datentyp nicht abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="adadb-172">It is specified as undefined behavior to mismatch the element type declared in HLSL with the underlying resource data type.</span></span> <span data-ttu-id="adadb-173">Wenn Sie z. b. typisierte UAV-Ladevorgänge für eine Puffer Ressource mit R8 \_ unorm-Daten verwenden, müssen Sie den Elementtyp wie folgt deklarieren `unorm float` :</span><span class="sxs-lookup"><span data-stu-id="adadb-173">For example, if you are using typed UAV loads on a buffer resource with R8\_UNORM data, then you must declare the element type as `unorm float`:</span></span>

``` syntax
RWBuffer<unorm float> uav;
```

## <a name="related-topics"></a><span data-ttu-id="adadb-174">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="adadb-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adadb-175">Darstellung</span><span class="sxs-lookup"><span data-stu-id="adadb-175">Rendering</span></span>](rendering.md)
</dt> <dt>

[<span data-ttu-id="adadb-176">Ressourcen Bindung</span><span class="sxs-lookup"><span data-stu-id="adadb-176">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="adadb-177">Ressourcen Bindung in HLSL</span><span class="sxs-lookup"><span data-stu-id="adadb-177">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="adadb-178">Shadermodell 5,1</span><span class="sxs-lookup"><span data-stu-id="adadb-178">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="adadb-179">Angeben von Stamm Signaturen in HLSL</span><span class="sxs-lookup"><span data-stu-id="adadb-179">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 