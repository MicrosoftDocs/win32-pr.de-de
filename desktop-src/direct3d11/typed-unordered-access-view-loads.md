---
title: Typisiertes Laden von ungeordneten Zugriffsansichten
description: Erfahren Sie mehr über die typisierte Last der ungeordneten Zugriffsansicht (UAV) in Direct3D 11. UAV Typed Load ist die Möglichkeit für einen Shader, aus einem UAV mit einem bestimmten DXGI_FORMAT zu lesen.
ms.assetid: BA72BF21-8621-461D-8677-9DFB7D5BC6AA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c6d2cbfa51c8473dc3da51c5844c63bef944b50
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396285"
---
# <a name="typed-unordered-access-view-loads"></a><span data-ttu-id="01ef1-104">Typisiertes Laden von ungeordneten Zugriffsansichten</span><span class="sxs-lookup"><span data-stu-id="01ef1-104">Typed Unordered Access View Loads</span></span>

<span data-ttu-id="01ef1-105">Unordered Access View (UAV) Typed Load ist die Möglichkeit für einen Shader, aus einem UAV mit einem bestimmten DXGI-FORMAT zu \_ lesen.</span><span class="sxs-lookup"><span data-stu-id="01ef1-105">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific DXGI\_FORMAT.</span></span>

-   [<span data-ttu-id="01ef1-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="01ef1-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="01ef1-107">Unterstützte Formate und API-Aufrufe</span><span class="sxs-lookup"><span data-stu-id="01ef1-107">Supported formats and API calls</span></span>](#supported-formats-and-api-calls)
-   [<span data-ttu-id="01ef1-108">Verwenden von typisierten UAV-Ladevorgängen aus HLSL</span><span class="sxs-lookup"><span data-stu-id="01ef1-108">Using typed UAV loads from HLSL</span></span>](#using-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="01ef1-109">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="01ef1-109">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="01ef1-110">Übersicht</span><span class="sxs-lookup"><span data-stu-id="01ef1-110">Overview</span></span>

<span data-ttu-id="01ef1-111">Eine ungeordnete Zugriffsansicht (UAV) ist eine Ansicht einer ungeordneten Zugriffsressource (die Puffer, Texturen und Texturarrays enthalten kann, jedoch ohne Mehrfachsampling).</span><span class="sxs-lookup"><span data-stu-id="01ef1-111">An unordered access view (UAV) is a view of an unordered access resource (which can include buffers, textures, and texture arrays, though without multi-sampling).</span></span> <span data-ttu-id="01ef1-112">Ein UAV ermöglicht temporal ungeordneten Lese-/Schreibzugriff von mehreren Threads.</span><span class="sxs-lookup"><span data-stu-id="01ef1-112">A UAV allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="01ef1-113">Dies bedeutet, dass dieser Ressourcentyp von mehreren Threads gleichzeitig gelesen/geschrieben werden kann, ohne Speicherkonflikte zu generieren.</span><span class="sxs-lookup"><span data-stu-id="01ef1-113">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span> <span data-ttu-id="01ef1-114">Dieser gleichzeitige Zugriff wird durch die Verwendung von [Atomic Functions](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions)verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="01ef1-114">This simultaneous access is handled through the use of [Atomic Functions](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span></span>

<span data-ttu-id="01ef1-115">D3D12 und D3D11.3 erweitern die Liste der Formate, die mit typisierten UAV-Ladevorgängen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="01ef1-115">D3D12 and D3D11.3 expands on the list of formats that can be used with typed UAV loads.</span></span>

## <a name="supported-formats-and-api-calls"></a><span data-ttu-id="01ef1-116">Unterstützte Formate und API-Aufrufe</span><span class="sxs-lookup"><span data-stu-id="01ef1-116">Supported formats and API calls</span></span>

<span data-ttu-id="01ef1-117">Zuvor unterstützten die folgenden drei Formate typisierte UAV-Ladevorgänge und waren für D3D11.0-Hardware erforderlich.</span><span class="sxs-lookup"><span data-stu-id="01ef1-117">Previously, the following three formats supported typed UAV loads, and were required for D3D11.0 hardware.</span></span> <span data-ttu-id="01ef1-118">Sie werden für alle D3D11.3- und D3D12-Hardware unterstützt.</span><span class="sxs-lookup"><span data-stu-id="01ef1-118">They are supported for all D3D11.3 and D3D12 hardware.</span></span>

-   <span data-ttu-id="01ef1-119">R32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="01ef1-119">R32\_FLOAT</span></span>
-   <span data-ttu-id="01ef1-120">R32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="01ef1-120">R32\_UINT</span></span>
-   <span data-ttu-id="01ef1-121">R32 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="01ef1-121">R32\_SINT</span></span>

<span data-ttu-id="01ef1-122">Die folgenden Formate werden als Satz auf D3D12- oder D3D11.3-Hardware unterstützt. Wenn also eines unterstützt wird, werden alle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="01ef1-122">The following formats are supported as a set on D3D12 or D3D11.3 hardware, so if any one is supported, all are supported.</span></span>

-   <span data-ttu-id="01ef1-123">R32G32B32A32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="01ef1-123">R32G32B32A32\_FLOAT</span></span>
-   <span data-ttu-id="01ef1-124">R32G32B32A32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="01ef1-124">R32G32B32A32\_UINT</span></span>
-   <span data-ttu-id="01ef1-125">R32G32B32A32 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="01ef1-125">R32G32B32A32\_SINT</span></span>
-   <span data-ttu-id="01ef1-126">R16G16B16A16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="01ef1-126">R16G16B16A16\_FLOAT</span></span>
-   <span data-ttu-id="01ef1-127">R16G16B16A16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="01ef1-127">R16G16B16A16\_UINT</span></span>
-   <span data-ttu-id="01ef1-128">R16G16B16A16 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="01ef1-128">R16G16B16A16\_SINT</span></span>
-   <span data-ttu-id="01ef1-129">R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="01ef1-129">R8G8B8A8\_UNORM</span></span>
-   <span data-ttu-id="01ef1-130">R8G8B8A8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="01ef1-130">R8G8B8A8\_UINT</span></span>
-   <span data-ttu-id="01ef1-131">R8G8B8A8 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="01ef1-131">R8G8B8A8\_SINT</span></span>
-   <span data-ttu-id="01ef1-132">R16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="01ef1-132">R16\_FLOAT</span></span>
-   <span data-ttu-id="01ef1-133">R16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="01ef1-133">R16\_UINT</span></span>
-   <span data-ttu-id="01ef1-134">R16 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="01ef1-134">R16\_SINT</span></span>
-   <span data-ttu-id="01ef1-135">R8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="01ef1-135">R8\_UNORM</span></span>
-   <span data-ttu-id="01ef1-136">R8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="01ef1-136">R8\_UINT</span></span>
-   <span data-ttu-id="01ef1-137">R8 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="01ef1-137">R8\_SINT</span></span>

<span data-ttu-id="01ef1-138">Die folgenden Formate werden optional und einzeln auf D3D12- und D3D11.3-Hardware unterstützt, sodass eine einzelne Abfrage für jedes Format durchgeführt werden muss, um die Unterstützung zu testen.</span><span class="sxs-lookup"><span data-stu-id="01ef1-138">The following formats are optionally and individually supported on D3D12 and D3D11.3 hardware, so a single query would need to be made on each format to test for support.</span></span>

-   <span data-ttu-id="01ef1-139">R16G16B16A16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="01ef1-139">R16G16B16A16\_UNORM</span></span>
-   <span data-ttu-id="01ef1-140">R16G16B16A16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="01ef1-140">R16G16B16A16\_SNORM</span></span>
-   <span data-ttu-id="01ef1-141">R32G32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="01ef1-141">R32G32\_FLOAT</span></span>
-   <span data-ttu-id="01ef1-142">R32G32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="01ef1-142">R32G32\_UINT</span></span>
-   <span data-ttu-id="01ef1-143">R32G32 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="01ef1-143">R32G32\_SINT</span></span>
-   <span data-ttu-id="01ef1-144">R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="01ef1-144">R10G10B10A2\_UNORM</span></span>
-   <span data-ttu-id="01ef1-145">R10G10B10A2 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="01ef1-145">R10G10B10A2\_UINT</span></span>
-   <span data-ttu-id="01ef1-146">R11G11B10 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="01ef1-146">R11G11B10\_FLOAT</span></span>
-   <span data-ttu-id="01ef1-147">R8G8B8A8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="01ef1-147">R8G8B8A8\_SNORM</span></span>
-   <span data-ttu-id="01ef1-148">R16G16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="01ef1-148">R16G16\_FLOAT</span></span>
-   <span data-ttu-id="01ef1-149">R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="01ef1-149">R16G16\_UNORM</span></span>
-   <span data-ttu-id="01ef1-150">R16G16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="01ef1-150">R16G16\_UINT</span></span>
-   <span data-ttu-id="01ef1-151">R16G16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="01ef1-151">R16G16\_SNORM</span></span>
-   <span data-ttu-id="01ef1-152">R16G16 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="01ef1-152">R16G16\_SINT</span></span>
-   <span data-ttu-id="01ef1-153">R8G8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="01ef1-153">R8G8\_UNORM</span></span>
-   <span data-ttu-id="01ef1-154">R8G8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="01ef1-154">R8G8\_UINT</span></span>
-   <span data-ttu-id="01ef1-155">R8G8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="01ef1-155">R8G8\_SNORM</span></span>
-   <span data-ttu-id="01ef1-156">8G8 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="01ef1-156">8G8\_SINT</span></span>
-   <span data-ttu-id="01ef1-157">R16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="01ef1-157">R16\_UNORM</span></span>
-   <span data-ttu-id="01ef1-158">R16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="01ef1-158">R16\_SNORM</span></span>
-   <span data-ttu-id="01ef1-159">R8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="01ef1-159">R8\_SNORM</span></span>
-   <span data-ttu-id="01ef1-160">A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="01ef1-160">A8\_UNORM</span></span>
-   <span data-ttu-id="01ef1-161">B5G6R5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="01ef1-161">B5G6R5\_UNORM</span></span>
-   <span data-ttu-id="01ef1-162">B5G5R5A1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="01ef1-162">B5G5R5A1\_UNORM</span></span>
-   <span data-ttu-id="01ef1-163">B4G4R4A4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="01ef1-163">B4G4R4A4\_UNORM</span></span>

<span data-ttu-id="01ef1-164">Um die Unterstützung für zusätzliche Formate zu ermitteln, rufen Sie [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) mit der [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS2-Struktur**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) als ersten Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="01ef1-164">To determine the support for any additional formats, call [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) with the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) structure as the first parameter.</span></span> <span data-ttu-id="01ef1-165">Das `TypedUAVLoadAdditionalFormats` Bit wird festgelegt, wenn die obige Liste "supported as a set" unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="01ef1-165">The `TypedUAVLoadAdditionalFormats` bit will be set if the "supported as a set" list above is supported.</span></span> <span data-ttu-id="01ef1-166">Führen Sie einen zweiten Aufruf von **CheckFeatureSupport** durch, indem Sie eine [**D3D11 \_ FEATURE DATA FORMAT \_ \_ \_ SUPPORT2-Struktur**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) verwenden (überprüfen Sie die zurückgegebene Struktur anhand des \_ \_ \_ UAV \_ TYPED LOAD-Members D3D12 FORMAT SUPPORT2 der \_ [**D3D11 \_ FORMAT \_ SUPPORT2-Enumeration),**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) um die Unterstützung in der Liste der optional unterstützten Formate oben zu ermitteln, z. B.:</span><span class="sxs-lookup"><span data-stu-id="01ef1-166">Make a second call to **CheckFeatureSupport**, using a [**D3D11\_FEATURE\_DATA\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) structure (checking the returned structure against the D3D12\_FORMAT\_SUPPORT2\_UAV\_TYPED\_LOAD member of the [**D3D11\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) enum) to determine support in the list of optionally supported formats above, for example:</span></span>

``` syntax
D3D11_FEATURE_DATA_D3D11_OPTIONS2 FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_D3D11_OPTIONS2, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Can not assume other formats are supported, so we check:
        D3D11_FEATURE_DATA_FORMAT_SUPPORT2 FormatSupport;
        ZeroMemory(&FormatSupport, sizeof(FormatSupport));
        FormatSupport.InFormat = DXGI_FORMAT_R32G32_FLOAT;
        hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_FORMAT_SUPPORT2, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.OutFormatSupport2 & D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
        {
            // DXGI_FORMAT_R32G32_FLOAT supports UAV Typed Load!
        }
    }
}
```

## <a name="using-typed-uav-loads-from-hlsl"></a><span data-ttu-id="01ef1-167">Verwenden von typisierten UAV-Ladevorgängen aus HLSL</span><span class="sxs-lookup"><span data-stu-id="01ef1-167">Using typed UAV loads from HLSL</span></span>

<span data-ttu-id="01ef1-168">Für typisierte UAVs ist das HLSL-Flag \_ D3D-SHADER \_ erfordert \_ TYPISIERTE \_ UAV-LADEFORMATE. \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="01ef1-168">For typed UAVs, the HLSL flag is D3D\_SHADER\_REQUIRES\_TYPED\_UAV\_LOAD\_ADDITIONAL\_FORMATS.</span></span>

<span data-ttu-id="01ef1-169">Hier ist ein Beispiel-Shadercode zum Verarbeiten einer typisierten UAV-Last:</span><span class="sxs-lookup"><span data-stu-id="01ef1-169">Here is example shader code to process a typed UAV load:</span></span>

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="related-topics"></a><span data-ttu-id="01ef1-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="01ef1-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01ef1-171">Direct3D 11.3-Features</span><span class="sxs-lookup"><span data-stu-id="01ef1-171">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="01ef1-172">Shadermodell 5.1</span><span class="sxs-lookup"><span data-stu-id="01ef1-172">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 