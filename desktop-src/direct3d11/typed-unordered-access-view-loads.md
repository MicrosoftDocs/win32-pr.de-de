---
title: Typisierte nicht geordnete zugriffsansichts Ladungen
description: Die gegebene UAV-Auslastung (unsortierter Zugriffs Ansicht) ist die Fähigkeit eines Shaders, aus einer UAV mit einem bestimmten DXGI-Format zu lesen \_ .
ms.assetid: BA72BF21-8621-461D-8677-9DFB7D5BC6AA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0958b3563ab8001fd7b34ae62c9bcc37ad75c07a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315453"
---
# <a name="typed-unordered-access-view-loads"></a><span data-ttu-id="25952-103">Typisierte nicht geordnete zugriffsansichts Ladungen</span><span class="sxs-lookup"><span data-stu-id="25952-103">Typed Unordered Access View Loads</span></span>

<span data-ttu-id="25952-104">Die gegebene UAV-Auslastung (unsortierter Zugriffs Ansicht) ist die Fähigkeit eines Shaders, aus einer UAV mit einem bestimmten DXGI-Format zu lesen \_ .</span><span class="sxs-lookup"><span data-stu-id="25952-104">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific DXGI\_FORMAT.</span></span>

-   [<span data-ttu-id="25952-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="25952-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="25952-106">Unterstützte Formate und API-Aufrufe</span><span class="sxs-lookup"><span data-stu-id="25952-106">Supported formats and API calls</span></span>](#supported-formats-and-api-calls)
-   [<span data-ttu-id="25952-107">Verwenden von typisierten UAV-Ladungen aus HLSL</span><span class="sxs-lookup"><span data-stu-id="25952-107">Using typed UAV loads from HLSL</span></span>](#using-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="25952-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="25952-108">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="25952-109">Übersicht</span><span class="sxs-lookup"><span data-stu-id="25952-109">Overview</span></span>

<span data-ttu-id="25952-110">Eine ungeordnete Zugriffs Ansicht (UAV) ist eine Ansicht einer unsorierten Zugriffs Ressource (die auch Puffer, Texturen und Textur Arrays enthalten kann, ohne Multisampling).</span><span class="sxs-lookup"><span data-stu-id="25952-110">An unordered access view (UAV) is a view of an unordered access resource (which can include buffers, textures, and texture arrays, though without multi-sampling).</span></span> <span data-ttu-id="25952-111">Eine UAV ermöglicht Temporale ungeordnete Lese-/Schreibzugriffe aus mehreren Threads.</span><span class="sxs-lookup"><span data-stu-id="25952-111">A UAV allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="25952-112">Dies bedeutet, dass dieser Ressourcentyp gleichzeitig von mehreren Threads gelesen/geschrieben werden kann, ohne dass Speicher Konflikte entstehen.</span><span class="sxs-lookup"><span data-stu-id="25952-112">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span> <span data-ttu-id="25952-113">Dieser gleichzeitige Zugriff wird durch die Verwendung von [atomaren Funktionen](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions)gehandhabt.</span><span class="sxs-lookup"><span data-stu-id="25952-113">This simultaneous access is handled through the use of [Atomic Functions](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span></span>

<span data-ttu-id="25952-114">D3D12 und D3D 11.3 werden in der Liste der Formate erweitert, die mit typisierten UAV-Ladevorgängen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="25952-114">D3D12 and D3D11.3 expands on the list of formats that can be used with typed UAV loads.</span></span>

## <a name="supported-formats-and-api-calls"></a><span data-ttu-id="25952-115">Unterstützte Formate und API-Aufrufe</span><span class="sxs-lookup"><span data-stu-id="25952-115">Supported formats and API calls</span></span>

<span data-ttu-id="25952-116">Bisher unterstützten die folgenden drei Formate typisierte UAV-Ladungen und waren für die D3D 11.0-Hardware erforderlich.</span><span class="sxs-lookup"><span data-stu-id="25952-116">Previously, the following three formats supported typed UAV loads, and were required for D3D11.0 hardware.</span></span> <span data-ttu-id="25952-117">Sie werden für alle D3D 11.3-und D3D12-Hardware unterstützt.</span><span class="sxs-lookup"><span data-stu-id="25952-117">They are supported for all D3D11.3 and D3D12 hardware.</span></span>

-   <span data-ttu-id="25952-118">R32 \_ float</span><span class="sxs-lookup"><span data-stu-id="25952-118">R32\_FLOAT</span></span>
-   <span data-ttu-id="25952-119">R32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="25952-119">R32\_UINT</span></span>
-   <span data-ttu-id="25952-120">R32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="25952-120">R32\_SINT</span></span>

<span data-ttu-id="25952-121">Die folgenden Formate werden als Satz auf D3D12-oder D3D 11.3-Hardware unterstützt. Wenn eine solche unterstützt wird, werden alle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="25952-121">The following formats are supported as a set on D3D12 or D3D11.3 hardware, so if any one is supported, all are supported.</span></span>

-   <span data-ttu-id="25952-122">R32G32B32A32 \_ float</span><span class="sxs-lookup"><span data-stu-id="25952-122">R32G32B32A32\_FLOAT</span></span>
-   <span data-ttu-id="25952-123">R32G32B32A32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="25952-123">R32G32B32A32\_UINT</span></span>
-   <span data-ttu-id="25952-124">R32G32B32A32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="25952-124">R32G32B32A32\_SINT</span></span>
-   <span data-ttu-id="25952-125">R16G16B16A16 \_ float</span><span class="sxs-lookup"><span data-stu-id="25952-125">R16G16B16A16\_FLOAT</span></span>
-   <span data-ttu-id="25952-126">R16G16B16A16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="25952-126">R16G16B16A16\_UINT</span></span>
-   <span data-ttu-id="25952-127">R16G16B16A16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="25952-127">R16G16B16A16\_SINT</span></span>
-   <span data-ttu-id="25952-128">R8G8B8A8 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="25952-128">R8G8B8A8\_UNORM</span></span>
-   <span data-ttu-id="25952-129">R8G8B8A8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="25952-129">R8G8B8A8\_UINT</span></span>
-   <span data-ttu-id="25952-130">R8G8B8A8 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="25952-130">R8G8B8A8\_SINT</span></span>
-   <span data-ttu-id="25952-131">R16 \_ float</span><span class="sxs-lookup"><span data-stu-id="25952-131">R16\_FLOAT</span></span>
-   <span data-ttu-id="25952-132">R16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="25952-132">R16\_UINT</span></span>
-   <span data-ttu-id="25952-133">R16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="25952-133">R16\_SINT</span></span>
-   <span data-ttu-id="25952-134">R8- \_ unorm</span><span class="sxs-lookup"><span data-stu-id="25952-134">R8\_UNORM</span></span>
-   <span data-ttu-id="25952-135">R8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="25952-135">R8\_UINT</span></span>
-   <span data-ttu-id="25952-136">R8 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="25952-136">R8\_SINT</span></span>

<span data-ttu-id="25952-137">Die folgenden Formate werden optional und einzeln auf D3D12-und D3D 11.3-Hardware unterstützt. Daher muss eine einzelne Abfrage für jedes Format durchgeführt werden, um die Unterstützung zu testen.</span><span class="sxs-lookup"><span data-stu-id="25952-137">The following formats are optionally and individually supported on D3D12 and D3D11.3 hardware, so a single query would need to be made on each format to test for support.</span></span>

-   <span data-ttu-id="25952-138">R16G16B16A16 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="25952-138">R16G16B16A16\_UNORM</span></span>
-   <span data-ttu-id="25952-139">R16G16B16A16 \_ snorm</span><span class="sxs-lookup"><span data-stu-id="25952-139">R16G16B16A16\_SNORM</span></span>
-   <span data-ttu-id="25952-140">R32G32 \_ float</span><span class="sxs-lookup"><span data-stu-id="25952-140">R32G32\_FLOAT</span></span>
-   <span data-ttu-id="25952-141">R32G32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="25952-141">R32G32\_UINT</span></span>
-   <span data-ttu-id="25952-142">R32G32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="25952-142">R32G32\_SINT</span></span>
-   <span data-ttu-id="25952-143">R10G10B10A2 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="25952-143">R10G10B10A2\_UNORM</span></span>
-   <span data-ttu-id="25952-144">R10G10B10A2 \_ uint</span><span class="sxs-lookup"><span data-stu-id="25952-144">R10G10B10A2\_UINT</span></span>
-   <span data-ttu-id="25952-145">R11G11B10 \_ float</span><span class="sxs-lookup"><span data-stu-id="25952-145">R11G11B10\_FLOAT</span></span>
-   <span data-ttu-id="25952-146">R8G8B8A8 \_ snorm</span><span class="sxs-lookup"><span data-stu-id="25952-146">R8G8B8A8\_SNORM</span></span>
-   <span data-ttu-id="25952-147">R16G16 \_ float</span><span class="sxs-lookup"><span data-stu-id="25952-147">R16G16\_FLOAT</span></span>
-   <span data-ttu-id="25952-148">R16G16 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="25952-148">R16G16\_UNORM</span></span>
-   <span data-ttu-id="25952-149">R16G16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="25952-149">R16G16\_UINT</span></span>
-   <span data-ttu-id="25952-150">R16G16 \_ snorm</span><span class="sxs-lookup"><span data-stu-id="25952-150">R16G16\_SNORM</span></span>
-   <span data-ttu-id="25952-151">R16G16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="25952-151">R16G16\_SINT</span></span>
-   <span data-ttu-id="25952-152">R8G8 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="25952-152">R8G8\_UNORM</span></span>
-   <span data-ttu-id="25952-153">R8G8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="25952-153">R8G8\_UINT</span></span>
-   <span data-ttu-id="25952-154">R8G8 \_ snorm</span><span class="sxs-lookup"><span data-stu-id="25952-154">R8G8\_SNORM</span></span>
-   <span data-ttu-id="25952-155">8g8 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="25952-155">8G8\_SINT</span></span>
-   <span data-ttu-id="25952-156">R16 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="25952-156">R16\_UNORM</span></span>
-   <span data-ttu-id="25952-157">R16 \_ snorm</span><span class="sxs-lookup"><span data-stu-id="25952-157">R16\_SNORM</span></span>
-   <span data-ttu-id="25952-158">R8 \_ snorm</span><span class="sxs-lookup"><span data-stu-id="25952-158">R8\_SNORM</span></span>
-   <span data-ttu-id="25952-159">A8- \_ unorm</span><span class="sxs-lookup"><span data-stu-id="25952-159">A8\_UNORM</span></span>
-   <span data-ttu-id="25952-160">B5G6R5 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="25952-160">B5G6R5\_UNORM</span></span>
-   <span data-ttu-id="25952-161">B5G5R5A1 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="25952-161">B5G5R5A1\_UNORM</span></span>
-   <span data-ttu-id="25952-162">B4G4R4A4 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="25952-162">B4G4R4A4\_UNORM</span></span>

<span data-ttu-id="25952-163">Um die Unterstützung für weitere Formate zu ermitteln, müssen Sie [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) mit der [**D3D11 \_ Feature \_ Data \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) -Struktur als ersten Parameter aufrufen.</span><span class="sxs-lookup"><span data-stu-id="25952-163">To determine the support for any additional formats, call [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) with the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) structure as the first parameter.</span></span> <span data-ttu-id="25952-164">Das `TypedUAVLoadAdditionalFormats` Bit wird festgelegt, wenn die oben genannte Liste als Satz unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="25952-164">The `TypedUAVLoadAdditionalFormats` bit will be set if the "supported as a set" list above is supported.</span></span> <span data-ttu-id="25952-165">Erstellen Sie einen zweiten Rückruf von **checkfeaturesupport unter** Verwendung einer [**D3D11 \_ Feature \_ Data \_ Format \_ SUPPORT2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) -Struktur (Überprüfen der zurückgegebenen Struktur mit dem D3D12- \_ Format \_ SUPPORT2 \_ UAV \_ typisiertes Load- \_ Member des D3D11- [**\_ Formats \_ SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) Enum), um die Unterstützung in der Liste der optional unterstützten Formate zu ermitteln, z. b.:</span><span class="sxs-lookup"><span data-stu-id="25952-165">Make a second call to **CheckFeatureSupport**, using a [**D3D11\_FEATURE\_DATA\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) structure (checking the returned structure against the D3D12\_FORMAT\_SUPPORT2\_UAV\_TYPED\_LOAD member of the [**D3D11\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) enum) to determine support in the list of optionally supported formats above, for example:</span></span>

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

## <a name="using-typed-uav-loads-from-hlsl"></a><span data-ttu-id="25952-166">Verwenden von typisierten UAV-Ladungen aus HLSL</span><span class="sxs-lookup"><span data-stu-id="25952-166">Using typed UAV loads from HLSL</span></span>

<span data-ttu-id="25952-167">Bei typisierten UAVs ist das HLSL-Flag D3D \_ Shader \_ erfordert ein \_ typisiertes \_ UAV- \_ Laden \_ zusätzlicher \_ Formate.</span><span class="sxs-lookup"><span data-stu-id="25952-167">For typed UAVs, the HLSL flag is D3D\_SHADER\_REQUIRES\_TYPED\_UAV\_LOAD\_ADDITIONAL\_FORMATS.</span></span>

<span data-ttu-id="25952-168">Dies ist beispielsweise ein Shader-Code, der eine typisierte UAV-Auslastung verarbeitet:</span><span class="sxs-lookup"><span data-stu-id="25952-168">Here is example shader code to process a typed UAV load:</span></span>

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="related-topics"></a><span data-ttu-id="25952-169">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="25952-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25952-170">Direct3D 11,3-Features</span><span class="sxs-lookup"><span data-stu-id="25952-170">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="25952-171">Shadermodell 5,1</span><span class="sxs-lookup"><span data-stu-id="25952-171">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 