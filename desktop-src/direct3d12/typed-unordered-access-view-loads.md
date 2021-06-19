---
title: Geladene typierte ungeordnete Zugriffsansicht (UAV)
description: Erfahren Sie mehr über die vom UAV (Unordered Access View) typierte Last in Direct3D 12. UAV Typed Load (UAV-typiertes Laden) ist die Fähigkeit eines Shaders, aus einem UAV mit einem bestimmten DXGI_FORMAT.
ms.assetid: 6106D15E-EAF6-4583-B4F2-7CC7EE30DE15
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96128354132a58e0b8648fba2b4e1e6babb95535
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394765"
---
# <a name="typed-unordered-access-view-uav-loads"></a><span data-ttu-id="1b4c2-104">Geladene typierte ungeordnete Zugriffsansicht (UAV)</span><span class="sxs-lookup"><span data-stu-id="1b4c2-104">Typed unordered access view (UAV) loads</span></span>

<span data-ttu-id="1b4c2-105">Unordered Access View (UAV) Typed Load ist die Fähigkeit eines Shaders, aus einem UAV mit einem bestimmten [**DXGI-FORMAT zu \_ lesen.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="1b4c2-105">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

-   [<span data-ttu-id="1b4c2-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="1b4c2-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="1b4c2-107">Unterstützte Formate und API-Aufrufe</span><span class="sxs-lookup"><span data-stu-id="1b4c2-107">Supported formats and API calls</span></span>](#supported-formats-and-api-calls)
-   [<span data-ttu-id="1b4c2-108">Verwenden von typierten UAV-Auslastungen von HLSL</span><span class="sxs-lookup"><span data-stu-id="1b4c2-108">Using typed UAV loads from HLSL</span></span>](#using-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="1b4c2-109">Verwenden von UNORM- und SNORM-typisierten UAV-Lasten von HLSL</span><span class="sxs-lookup"><span data-stu-id="1b4c2-109">Using UNORM and SNORM typed UAV loads from HLSL</span></span>](#using-unorm-and-snorm-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="1b4c2-110">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1b4c2-110">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="1b4c2-111">Übersicht</span><span class="sxs-lookup"><span data-stu-id="1b4c2-111">Overview</span></span>

<span data-ttu-id="1b4c2-112">Eine ungeordnete Zugriffsansicht (UAV) ist eine Ansicht einer ungeordneten Zugriffsressource (die Puffer, Texturen und Texturarrays enthalten kann, jedoch ohne Mehrfachstichproben).</span><span class="sxs-lookup"><span data-stu-id="1b4c2-112">An unordered access view (UAV) is a view of an unordered access resource (which can include buffers, textures, and texture arrays, though without multi-sampling).</span></span> <span data-ttu-id="1b4c2-113">Ein UAV ermöglicht den zeitlich ungeordneten Lese-/Schreibzugriff von mehreren Threads.</span><span class="sxs-lookup"><span data-stu-id="1b4c2-113">A UAV allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="1b4c2-114">Dies bedeutet, dass dieser Ressourcentyp gleichzeitig von mehreren Threads gelesen/geschrieben werden kann, ohne Arbeitsspeicherkonflikte zu generieren.</span><span class="sxs-lookup"><span data-stu-id="1b4c2-114">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span> <span data-ttu-id="1b4c2-115">Dieser gleichzeitige Zugriff wird mithilfe von [Atomic Functions verarbeitet.](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions)</span><span class="sxs-lookup"><span data-stu-id="1b4c2-115">This simultaneous access is handled through the use of [Atomic Functions](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span></span>

<span data-ttu-id="1b4c2-116">D3D12 (und D3D11.3) erweitert die Liste der Formate, die mit typierten UAV-Auslastungen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="1b4c2-116">D3D12 (and D3D11.3) expands on the list of formats that can be used with typed UAV loads.</span></span>

## <a name="supported-formats-and-api-calls"></a><span data-ttu-id="1b4c2-117">Unterstützte Formate und API-Aufrufe</span><span class="sxs-lookup"><span data-stu-id="1b4c2-117">Supported formats and API calls</span></span>

<span data-ttu-id="1b4c2-118">Zuvor unterstützten die folgenden drei Formate typierte UAV-Auslastungen und waren für D3D11.0-Hardware erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1b4c2-118">Previously, the following three formats supported typed UAV loads, and were required for D3D11.0 hardware.</span></span> <span data-ttu-id="1b4c2-119">Sie werden für alle D3D11.3- und D3D12-Hardware unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1b4c2-119">They are supported for all D3D11.3 and D3D12 hardware.</span></span>

-   <span data-ttu-id="1b4c2-120">R32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-120">R32\_FLOAT</span></span>
-   <span data-ttu-id="1b4c2-121">R32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-121">R32\_UINT</span></span>
-   <span data-ttu-id="1b4c2-122">R32 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-122">R32\_SINT</span></span>

<span data-ttu-id="1b4c2-123">Die folgenden Formate werden als Set auf D3D12- oder D3D11.3-Hardware unterstützt. Wenn also eins unterstützt wird, werden alle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1b4c2-123">The following formats are supported as a set on D3D12 or D3D11.3 hardware, so if any one is supported, all are supported.</span></span>

-   <span data-ttu-id="1b4c2-124">R32G32B32A32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-124">R32G32B32A32\_FLOAT</span></span>
-   <span data-ttu-id="1b4c2-125">R32G32B32A32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-125">R32G32B32A32\_UINT</span></span>
-   <span data-ttu-id="1b4c2-126">R32G32B32A32 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-126">R32G32B32A32\_SINT</span></span>
-   <span data-ttu-id="1b4c2-127">R16G16B16A16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-127">R16G16B16A16\_FLOAT</span></span>
-   <span data-ttu-id="1b4c2-128">R16G16B16A16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-128">R16G16B16A16\_UINT</span></span>
-   <span data-ttu-id="1b4c2-129">R16G16B16A16 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-129">R16G16B16A16\_SINT</span></span>
-   <span data-ttu-id="1b4c2-130">R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="1b4c2-130">R8G8B8A8\_UNORM</span></span>
-   <span data-ttu-id="1b4c2-131">R8G8B8A8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-131">R8G8B8A8\_UINT</span></span>
-   <span data-ttu-id="1b4c2-132">R8G8B8A8 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-132">R8G8B8A8\_SINT</span></span>
-   <span data-ttu-id="1b4c2-133">R16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-133">R16\_FLOAT</span></span>
-   <span data-ttu-id="1b4c2-134">R16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-134">R16\_UINT</span></span>
-   <span data-ttu-id="1b4c2-135">R16 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-135">R16\_SINT</span></span>
-   <span data-ttu-id="1b4c2-136">R8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="1b4c2-136">R8\_UNORM</span></span>
-   <span data-ttu-id="1b4c2-137">R8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-137">R8\_UINT</span></span>
-   <span data-ttu-id="1b4c2-138">R8 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-138">R8\_SINT</span></span>

<span data-ttu-id="1b4c2-139">Die folgenden Formate werden optional und einzeln auf D3D12- und D3D11.3-Hardware unterstützt, sodass für jedes Format eine einzelne Abfrage durchgeführt werden muss, um die Unterstützung zu testen.</span><span class="sxs-lookup"><span data-stu-id="1b4c2-139">The following formats are optionally and individually supported on D3D12 and D3D11.3 hardware, so a single query would need to be made on each format to test for support.</span></span>

-   <span data-ttu-id="1b4c2-140">R16G16B16A16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="1b4c2-140">R16G16B16A16\_UNORM</span></span>
-   <span data-ttu-id="1b4c2-141">R16G16B16A16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="1b4c2-141">R16G16B16A16\_SNORM</span></span>
-   <span data-ttu-id="1b4c2-142">R32G32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-142">R32G32\_FLOAT</span></span>
-   <span data-ttu-id="1b4c2-143">R32G32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-143">R32G32\_UINT</span></span>
-   <span data-ttu-id="1b4c2-144">R32G32 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-144">R32G32\_SINT</span></span>
-   <span data-ttu-id="1b4c2-145">R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="1b4c2-145">R10G10B10A2\_UNORM</span></span>
-   <span data-ttu-id="1b4c2-146">R10G10B10A2 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-146">R10G10B10A2\_UINT</span></span>
-   <span data-ttu-id="1b4c2-147">R11G11B10 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-147">R11G11B10\_FLOAT</span></span>
-   <span data-ttu-id="1b4c2-148">R8G8B8A8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="1b4c2-148">R8G8B8A8\_SNORM</span></span>
-   <span data-ttu-id="1b4c2-149">R16G16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-149">R16G16\_FLOAT</span></span>
-   <span data-ttu-id="1b4c2-150">R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="1b4c2-150">R16G16\_UNORM</span></span>
-   <span data-ttu-id="1b4c2-151">R16G16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-151">R16G16\_UINT</span></span>
-   <span data-ttu-id="1b4c2-152">R16G16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="1b4c2-152">R16G16\_SNORM</span></span>
-   <span data-ttu-id="1b4c2-153">R16G16 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-153">R16G16\_SINT</span></span>
-   <span data-ttu-id="1b4c2-154">R8G8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="1b4c2-154">R8G8\_UNORM</span></span>
-   <span data-ttu-id="1b4c2-155">R8G8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-155">R8G8\_UINT</span></span>
-   <span data-ttu-id="1b4c2-156">R8G8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="1b4c2-156">R8G8\_SNORM</span></span>
-   <span data-ttu-id="1b4c2-157">R8G8 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="1b4c2-157">R8G8\_SINT</span></span>
-   <span data-ttu-id="1b4c2-158">R16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="1b4c2-158">R16\_UNORM</span></span>
-   <span data-ttu-id="1b4c2-159">R16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="1b4c2-159">R16\_SNORM</span></span>
-   <span data-ttu-id="1b4c2-160">R8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="1b4c2-160">R8\_SNORM</span></span>
-   <span data-ttu-id="1b4c2-161">A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="1b4c2-161">A8\_UNORM</span></span>
-   <span data-ttu-id="1b4c2-162">B5G6R5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="1b4c2-162">B5G6R5\_UNORM</span></span>
-   <span data-ttu-id="1b4c2-163">B5G5R5A1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="1b4c2-163">B5G5R5A1\_UNORM</span></span>
-   <span data-ttu-id="1b4c2-164">B4G4R4A4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="1b4c2-164">B4G4R4A4\_UNORM</span></span>

<span data-ttu-id="1b4c2-165">Um die Unterstützung für zusätzliche Formate zu ermitteln, rufen Sie [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) mit der [**D3D12 \_ FEATURE DATA \_ \_ D3D12 \_ OPTIONS-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) als ersten Parameter auf (siehe [Capability Querying](capability-querying.md)).</span><span class="sxs-lookup"><span data-stu-id="1b4c2-165">To determine the support for any additional formats, call [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) with the [**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) structure as the first parameter (refer to [Capability Querying](capability-querying.md)).</span></span> <span data-ttu-id="1b4c2-166">Das *Feld TypedUAVLoadAdditionalFormats* wird festgelegt, wenn die obige Liste "Supported as a set" unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="1b4c2-166">The *TypedUAVLoadAdditionalFormats* field will be set if the "supported as a set" list above is supported.</span></span> <span data-ttu-id="1b4c2-167">Führen Sie einen zweiten Aufruf von **CheckFeatureSupport** mithilfe einer [**D3D12 \_ FEATURE DATA FORMAT \_ \_ \_ SUPPORT-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) durch (überprüfen Sie die zurückgegebene Struktur anhand des \_ \_ \_ UAV \_ TYPED LOAD-Members \_ [**D3D12 \_ FORMAT \_ SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) in der Liste der oben aufgeführten optional unterstützten Formate, z. B.:</span><span class="sxs-lookup"><span data-stu-id="1b4c2-167">Make a second call to **CheckFeatureSupport**, using a [**D3D12\_FEATURE\_DATA\_FORMAT\_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) structure (checking the returned structure against the D3D12\_FORMAT\_SUPPORT2\_UAV\_TYPED\_LOAD member of the [**D3D12\_FORMAT\_SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) enum) to determine support in the list of optionally supported formats listed above, for example:</span></span>

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

## <a name="using-typed-uav-loads-from-hlsl"></a><span data-ttu-id="1b4c2-168">Verwenden von typierten UAV-Auslastungen von HLSL</span><span class="sxs-lookup"><span data-stu-id="1b4c2-168">Using typed UAV loads from HLSL</span></span>

<span data-ttu-id="1b4c2-169">Für typierte UAVs ist das HLSL-Flag \_ D3D-SHADER \_ ERFORDERT \_ TYPIERTE \_ \_ UAV-LADE \_ ZUSÄTZLICHE \_ FORMATE.</span><span class="sxs-lookup"><span data-stu-id="1b4c2-169">For typed UAVs, the HLSL flag is D3D\_SHADER\_REQUIRES\_TYPED\_UAV\_LOAD\_ADDITIONAL\_FORMATS.</span></span>

<span data-ttu-id="1b4c2-170">Hier ist ein Shader-Beispielcode zum Verarbeiten einer typierten UAV-Last:</span><span class="sxs-lookup"><span data-stu-id="1b4c2-170">Here is example shader code to process a typed UAV load:</span></span>

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="using-unorm-and-snorm-typed-uav-loads-from-hlsl"></a><span data-ttu-id="1b4c2-171">Verwenden von UNORM- und SNORM-typisierten UAV-Lasten von HLSL</span><span class="sxs-lookup"><span data-stu-id="1b4c2-171">Using UNORM and SNORM typed UAV loads from HLSL</span></span>

<span data-ttu-id="1b4c2-172">Wenn Sie typisiert UAV-Lasten zum Lesen aus einer UNORM- oder SNORM-Ressource verwenden, müssen Sie den Elementtyp des HLSL-Objekts ordnungsgemäß als oder `unorm` `snorm` deklarieren.</span><span class="sxs-lookup"><span data-stu-id="1b4c2-172">When using typed UAV loads to read from a UNORM or SNORM resource, you must properly declare the element type of the HLSL object to be `unorm` or `snorm`.</span></span> <span data-ttu-id="1b4c2-173">Es wird als nicht definiertes Verhalten angegeben, um einen Konflikt zwischen dem in HLSL deklarierten Elementtyp und dem zugrunde liegenden Ressourcendatentyp zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="1b4c2-173">It is specified as undefined behavior to mismatch the element type declared in HLSL with the underlying resource data type.</span></span> <span data-ttu-id="1b4c2-174">Wenn Sie beispielsweise typisiert UAV-Lasten für eine Pufferressource mit R8-UNORM-Daten verwenden, müssen Sie den Elementtyp als \_ `unorm float` deklarieren:</span><span class="sxs-lookup"><span data-stu-id="1b4c2-174">For example, if you are using typed UAV loads on a buffer resource with R8\_UNORM data, then you must declare the element type as `unorm float`:</span></span>

``` syntax
RWBuffer<unorm float> uav;
```

## <a name="related-topics"></a><span data-ttu-id="1b4c2-175">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1b4c2-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b4c2-176">Darstellung</span><span class="sxs-lookup"><span data-stu-id="1b4c2-176">Rendering</span></span>](rendering.md)
</dt> <dt>

[<span data-ttu-id="1b4c2-177">Ressourcenbindung</span><span class="sxs-lookup"><span data-stu-id="1b4c2-177">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="1b4c2-178">Ressourcenbindung in HLSL</span><span class="sxs-lookup"><span data-stu-id="1b4c2-178">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="1b4c2-179">Shadermodell 5.1</span><span class="sxs-lookup"><span data-stu-id="1b4c2-179">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="1b4c2-180">Festlegen von Stammsignaturen in HLSL</span><span class="sxs-lookup"><span data-stu-id="1b4c2-180">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 