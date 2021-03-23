---
title: Dynamische Indizierung mit HLSL 5.1
description: Das D3D12DynamicIndexing-Beispiel veranschaulicht einige der neuen HLSL-Features, die im Shader-Modell 5,1 verfügbar sind, insbesondere dynamische Indizierung und ungebundene Arrays, um das gleiche Mesh mehrmals zu rendern, wobei jedes Mal ein dynamisch ausgewähltes Material gerendert wird. Bei der dynamischen Indizierung können Shader jetzt in ein Array indizieren, ohne den Wert des Indexes zur Kompilierzeit zu kennen. In Kombination mit unbegrenzten Arrays wird dadurch eine weitere dereferenzierungsstufe und Flexibilität für Shader-Autoren und Kunst Pipelines hinzugefügt.
ms.assetid: 9821AEDF-E83D-4034-863A-2B820D9B7455
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e41892e7deff23c8d11f8be1c38dac3fcba1de9
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548679"
---
# <a name="dynamic-indexing-using-hlsl-51"></a><span data-ttu-id="8d3e2-105">Dynamische Indizierung mit HLSL 5.1</span><span class="sxs-lookup"><span data-stu-id="8d3e2-105">Dynamic Indexing using HLSL 5.1</span></span>

<span data-ttu-id="8d3e2-106">Das **D3D12DynamicIndexing** -Beispiel veranschaulicht einige der neuen HLSL-Features, die im Shader-Modell 5,1 verfügbar sind, insbesondere dynamische Indizierung und ungebundene Arrays, um das gleiche Mesh mehrmals zu rendern, wobei jedes Mal ein dynamisch ausgewähltes Material gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="8d3e2-106">The **D3D12DynamicIndexing** sample demonstrates some of the new HLSL features available in Shader Model 5.1 - particularly dynamic indexing and unbounded arrays - to render the same mesh multiple times, each time rendering it with a dynamically selected material.</span></span> <span data-ttu-id="8d3e2-107">Bei der dynamischen Indizierung können Shader jetzt in ein Array indizieren, ohne den Wert des Indexes zur Kompilierzeit zu kennen.</span><span class="sxs-lookup"><span data-stu-id="8d3e2-107">With dynamic indexing, shaders can now index into an array without knowing the value of the index at compile time.</span></span> <span data-ttu-id="8d3e2-108">In Kombination mit unbegrenzten Arrays wird dadurch eine weitere dereferenzierungsstufe und Flexibilität für Shader-Autoren und Kunst Pipelines hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8d3e2-108">When combined with unbounded arrays, this adds another level of indirection and flexibility for shader authors and art pipelines.</span></span>

-   [<span data-ttu-id="8d3e2-109">Einrichten des Pixelshaders</span><span class="sxs-lookup"><span data-stu-id="8d3e2-109">Set up the pixel shader</span></span>](#set-up-the-pixel-shader)
-   [<span data-ttu-id="8d3e2-110">Einrichten der Stamm Signatur</span><span class="sxs-lookup"><span data-stu-id="8d3e2-110">Set up the root signature</span></span>](#set-up-the-root-signature)
-   [<span data-ttu-id="8d3e2-111">Erstellen der Texturen</span><span class="sxs-lookup"><span data-stu-id="8d3e2-111">Create the textures</span></span>](#create-the-textures)
-   [<span data-ttu-id="8d3e2-112">Hochladen der Textur Daten</span><span class="sxs-lookup"><span data-stu-id="8d3e2-112">Upload the texture data</span></span>](#upload-the-texture-data)
-   [<span data-ttu-id="8d3e2-113">Diffuses Textur laden</span><span class="sxs-lookup"><span data-stu-id="8d3e2-113">Load the diffuse texture</span></span>](#load-the-diffuse-texture)
-   [<span data-ttu-id="8d3e2-114">Erstellen eines Samplers</span><span class="sxs-lookup"><span data-stu-id="8d3e2-114">Create a sampler</span></span>](#create-a-sampler)
-   [<span data-ttu-id="8d3e2-115">Dynamisches Ändern des Stamm Parameter Indexes</span><span class="sxs-lookup"><span data-stu-id="8d3e2-115">Dynamically change the root parameter index</span></span>](#dynamically-change-the-root-parameter-index)
-   [<span data-ttu-id="8d3e2-116">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="8d3e2-116">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="8d3e2-117">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="8d3e2-117">Related topics</span></span>](#related-topics)

## <a name="set-up-the-pixel-shader"></a><span data-ttu-id="8d3e2-118">Einrichten des Pixelshaders</span><span class="sxs-lookup"><span data-stu-id="8d3e2-118">Set up the pixel shader</span></span>

<span data-ttu-id="8d3e2-119">Sehen wir uns zuerst den Shader an, der für dieses Beispiel ein Pixelshader ist.</span><span class="sxs-lookup"><span data-stu-id="8d3e2-119">Let's first look at the shader itself, which for this sample is a pixel shader.</span></span>

``` syntax
Texture2D        g_txDiffuse : register(t0);
Texture2D        g_txMats[]  : register(t1);
SamplerState     g_sampler   : register(s0);

struct PSSceneIn
{
    float4 pos : SV_Position;
    float2 tex : TEXCOORD0;
};

struct MaterialConstants
{
    uint matIndex;  // Dynamically set index for looking up from g_txMats[].
};
ConstantBuffer<MaterialConstants> materialConstants : register(b0, space0);

float4 PSSceneMain(PSSceneIn input) : SV_Target
{
    float3 diffuse = g_txDiffuse.Sample(g_sampler, input.tex).rgb;
    float3 mat = g_txMats[materialConstants.matIndex].Sample(g_sampler, input.tex).rgb;
    return float4(diffuse * mat, 1.0f);
}
```

<span data-ttu-id="8d3e2-120">Die Funktion für ungebundene Arrays wird durch das `g_txMats[]` Array veranschaulicht, da keine Array Größe angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8d3e2-120">The unbounded array feature is illustrated by the `g_txMats[]` array as it does not specify an array size.</span></span> <span data-ttu-id="8d3e2-121">Dynamische Indizierung wird zum Indizieren von `g_txMats[]` mit verwendet `matIndex` , das als Stamm Konstante definiert ist.</span><span class="sxs-lookup"><span data-stu-id="8d3e2-121">Dynamic indexing is used to index into `g_txMats[]` with `matIndex`, which is defined as a root constant.</span></span> <span data-ttu-id="8d3e2-122">Der Shader kennt die Größe oder das Array oder den Wert des Indexes zur Kompilierzeit nicht.</span><span class="sxs-lookup"><span data-stu-id="8d3e2-122">The shader has no knowledge of the size or the array or the value of the index at compile-time.</span></span> <span data-ttu-id="8d3e2-123">Beide Attribute werden in der Stamm Signatur des Pipeline Zustands Objekts definiert, das mit dem Shader verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8d3e2-123">Both attributes are defined in the root signature of the pipeline state object used with the shader.</span></span>

<span data-ttu-id="8d3e2-124">Um die Funktionen der dynamischen Indizierung in HLSL nutzen zu können, muss der Shader mit SM 5,1 kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="8d3e2-124">To take advantage of the dynamic indexing features in HLSL requires that the shader be compiled with SM 5.1.</span></span> <span data-ttu-id="8d3e2-125">Außerdem muss das Flag " **/enable \_ ungebundene \_ Deskriptor \_ Tables** " verwendet werden, um ungebundene Arrays zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d3e2-125">Additionally, to make use of unbounded arrays, the **/enable\_unbounded\_descriptor\_tables** flag must also be used.</span></span> <span data-ttu-id="8d3e2-126">Die folgenden Befehlszeilenoptionen werden verwendet, um diesen Shader mit dem [Effekt-Compilertool](/windows/desktop/direct3dtools/fxc) (FXC) zu kompilieren:</span><span class="sxs-lookup"><span data-stu-id="8d3e2-126">The following command line options are used to compile this shader with the [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC):</span></span>

``` syntax
fxc /Zi /E"PSSceneMain" /Od /Fo"dynamic_indexing_pixel.cso" /ps"_5_1" /nologo /enable_unbounded_descriptor_tables
```

## <a name="set-up-the-root-signature"></a><span data-ttu-id="8d3e2-127">Einrichten der Stamm Signatur</span><span class="sxs-lookup"><span data-stu-id="8d3e2-127">Set up the root signature</span></span>

<span data-ttu-id="8d3e2-128">Sehen wir uns nun die Definition der Stamm Signatur an, insbesondere, wie wir die Größe des unbegrenzten Arrays definieren und eine Stamm Konstante mit verknüpfen `matIndex` .</span><span class="sxs-lookup"><span data-stu-id="8d3e2-128">Now, let's look at the root signature definition, particularly, how we define the size of the unbounded array and link a root constant to `matIndex`.</span></span> <span data-ttu-id="8d3e2-129">Für den Pixelshader definieren wir drei Dinge: eine Deskriptortabelle für Srvs (unsere Texture2Ds), eine Deskriptortabelle für Samplers und eine einzelne Stamm Konstante.</span><span class="sxs-lookup"><span data-stu-id="8d3e2-129">For the pixel shader, we define three things: a descriptor table for SRVs (our Texture2Ds), a descriptor table for Samplers and a single root constant.</span></span> <span data-ttu-id="8d3e2-130">Die Deskriptortabelle für unsere Srvs enthält `CityMaterialCount + 1` Einträge.</span><span class="sxs-lookup"><span data-stu-id="8d3e2-130">The descriptor table for our SRVs contains `CityMaterialCount + 1` entries.</span></span> <span data-ttu-id="8d3e2-131">`CityMaterialCount` ist eine Konstante, die die Länge von definiert, `g_txMats[]` und + 1 ist für `g_txDiffuse` .</span><span class="sxs-lookup"><span data-stu-id="8d3e2-131">`CityMaterialCount` is a constant that defines the length of `g_txMats[]` and the + 1 is for `g_txDiffuse`.</span></span> <span data-ttu-id="8d3e2-132">Die Deskriptortabelle für unsere Samplers enthält nur einen Eintrag, und in der **loadassets** -Methode wird nur der 1 32-Bit-root-Konstante Wert über **initaskonstanten**(...) definiert.</span><span class="sxs-lookup"><span data-stu-id="8d3e2-132">The descriptor table for our Samplers contains only one entry and we only define one 32-bit root constant value via **InitAsConstants**(…)., in the **LoadAssets** method.</span></span>

``` syntax
 // Create the root signature.
    {
        CD3DX12_DESCRIPTOR_RANGE ranges[3];
        ranges[0].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SRV, 1 + CityMaterialCount, 0);  // Diffuse texture + array of materials.
        ranges[1].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER, 1, 0);
        ranges[2].Init(D3D12_DESCRIPTOR_RANGE_TYPE_CBV, 1, 0);

        CD3DX12_ROOT_PARAMETER rootParameters[4];
        rootParameters[0].InitAsDescriptorTable(1, &ranges[0], D3D12_SHADER_VISIBILITY_PIXEL);
        rootParameters[1].InitAsDescriptorTable(1, &ranges[1], D3D12_SHADER_VISIBILITY_PIXEL);
        rootParameters[2].InitAsDescriptorTable(1, &ranges[2], D3D12_SHADER_VISIBILITY_VERTEX);
        rootParameters[3].InitAsConstants(1, 0, 0, D3D12_SHADER_VISIBILITY_PIXEL);

        CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
        rootSignatureDesc.Init(_countof(rootParameters), rootParameters, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

        ComPtr<ID3DBlob> signature;
        ComPtr<ID3DBlob> error;
        ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
        ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));
    }
```



| <span data-ttu-id="8d3e2-133">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="8d3e2-133">Call flow</span></span>                                                             | <span data-ttu-id="8d3e2-134">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d3e2-134">Parameters</span></span>                                                            |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="8d3e2-135">**CD3DX12- \_ \_ Deskriptorbereich**</span><span class="sxs-lookup"><span data-stu-id="8d3e2-135">**CD3DX12\_DESCRIPTOR\_RANGE**</span></span>](cd3dx12-descriptor-range.md)        | [<span data-ttu-id="8d3e2-136">**D3D12- \_ \_ deskriptorbereichstyp \_**</span><span class="sxs-lookup"><span data-stu-id="8d3e2-136">**D3D12\_DESCRIPTOR\_RANGE\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) |
| [<span data-ttu-id="8d3e2-137">**CD3DX12 \_ root- \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="8d3e2-137">**CD3DX12\_ROOT\_PARAMETER**</span></span>](cd3dx12-root-parameter.md)            | [<span data-ttu-id="8d3e2-138">**D3D12- \_ Shader- \_ Sichtbarkeit**</span><span class="sxs-lookup"><span data-stu-id="8d3e2-138">**D3D12\_SHADER\_VISIBILITY**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [<span data-ttu-id="8d3e2-139">**CD3DX12 \_ Stamm \_ Signatur \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="8d3e2-139">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) | [<span data-ttu-id="8d3e2-140">**D3D12 \_ root \_ Signature- \_ Flags**</span><span class="sxs-lookup"><span data-stu-id="8d3e2-140">**D3D12\_ROOT\_SIGNATURE\_FLAGS**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| <span data-ttu-id="8d3e2-141">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8d3e2-141">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span>                                   |                                                                       |
| [<span data-ttu-id="8d3e2-142">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="8d3e2-142">**D3D12SerializeRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="8d3e2-143">**D3D \_ Stamm \_ Signatur \_ Version**</span><span class="sxs-lookup"><span data-stu-id="8d3e2-143">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="8d3e2-144">**"Kreaterootsignature"**</span><span class="sxs-lookup"><span data-stu-id="8d3e2-144">**CreateRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |



 

## <a name="create-the-textures"></a><span data-ttu-id="8d3e2-145">Erstellen der Texturen</span><span class="sxs-lookup"><span data-stu-id="8d3e2-145">Create the textures</span></span>

<span data-ttu-id="8d3e2-146">Der Inhalt von `g_txMats[]` sind prozedurale generierte Texturen, die in **loadassets** erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8d3e2-146">The contents of `g_txMats[]` are procedurally generated textures created in **LoadAssets**.</span></span> <span data-ttu-id="8d3e2-147">Jede Stadt, die in der Szene gerendert wird, hat dieselbe diffuse Textur, aber jede verfügt auch über eine eigene prozedurale generierte Textur.</span><span class="sxs-lookup"><span data-stu-id="8d3e2-147">Each city rendered in the scene shares the same diffuse texture but each also has its own procedurally generated texture.</span></span> <span data-ttu-id="8d3e2-148">Das Array von Texturen erstreckt sich über das Regenbogen Spektrum, um die Indizierungs Technik leicht visuell darzustellen.</span><span class="sxs-lookup"><span data-stu-id="8d3e2-148">The array of textures span the rainbow spectrum to easily visualize the indexing technique.</span></span>

``` syntax
 // Create the textures and sampler.
    {
        // Procedurally generate an array of textures to use as city materials.
        {
            // All of these materials use the same texture desc.
            D3D12_RESOURCE_DESC textureDesc = {};
            textureDesc.MipLevels = 1;
            textureDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
            textureDesc.Width = CityMaterialTextureWidth;
            textureDesc.Height = CityMaterialTextureHeight;
            textureDesc.Flags = D3D12_RESOURCE_FLAG_NONE;
            textureDesc.DepthOrArraySize = 1;
            textureDesc.SampleDesc.Count = 1;
            textureDesc.SampleDesc.Quality = 0;
            textureDesc.Dimension = D3D12_RESOURCE_DIMENSION_TEXTURE2D;

            // The textures evenly span the color rainbow so that each city gets
            // a different material.
            float materialGradStep = (1.0f / static_cast<float>(CityMaterialCount));

            // Generate texture data.
            vector<vector<unsigned char>> cityTextureData;
            cityTextureData.resize(CityMaterialCount);
            for (int i = 0; i < CityMaterialCount; ++i)
            {
                CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_DEFAULT);
                ThrowIfFailed(m_device->CreateCommittedResource(
                    &heapProps,
                    D3D12_HEAP_FLAG_NONE,
                    &textureDesc,
                    D3D12_RESOURCE_STATE_COPY_DEST,
                    nullptr,
                    IID_PPV_ARGS(&m_cityMaterialTextures[i])));

                // Fill the texture.
                float t = i * materialGradStep;
                cityTextureData[i].resize(CityMaterialTextureWidth * CityMaterialTextureHeight * CityMaterialTextureChannelCount);
                for (int x = 0; x < CityMaterialTextureWidth; ++x)
                {
                    for (int y = 0; y < CityMaterialTextureHeight; ++y)
                    {
                        // Compute the appropriate index into the buffer based on the x/y coordinates.
                        int pixelIndex = (y * CityMaterialTextureChannelCount * CityMaterialTextureWidth) + (x * CityMaterialTextureChannelCount);

                        // Determine this row's position along the rainbow gradient.
                        float tPrime = t + ((static_cast<float>(y) / static_cast<float>(CityMaterialTextureHeight)) * materialGradStep);

                        // Compute the RGB value for this position along the rainbow
                        // and pack the pixel value.
                        XMVECTOR hsl = XMVectorSet(tPrime, 0.5f, 0.5f, 1.0f);
                        XMVECTOR rgb = XMColorHSLToRGB(hsl);
                        cityTextureData[i][pixelIndex + 0] = static_cast<unsigned char>((255 * XMVectorGetX(rgb)));
                        cityTextureData[i][pixelIndex + 1] = static_cast<unsigned char>((255 * XMVectorGetY(rgb)));
                        cityTextureData[i][pixelIndex + 2] = static_cast<unsigned char>((255 * XMVectorGetZ(rgb)));
                        cityTextureData[i][pixelIndex + 3] = 255;
                    }
                }
            }
        }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8d3e2-149">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="8d3e2-149">Call flow</span></span></th>
<th><span data-ttu-id="8d3e2-150">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d3e2-150">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8d3e2-151"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc"><strong>D3D12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-151"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc"><strong>D3D12_RESOURCE_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="8d3e2-152"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-152"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span></span><br /><span data-ttu-id="8d3e2-153">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-153">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span></span><br /><span data-ttu-id="8d3e2-154">
<a href=""></a>[<strong>D3D12_RESOURCE_DIMENSION</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_dimension)</span><span class="sxs-lookup"><span data-stu-id="8d3e2-154">
<a href=""></a>[<strong>D3D12_RESOURCE_DIMENSION</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d3e2-155"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>"Kreatecommittedresource"</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-155"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="8d3e2-156"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-156"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br /><span data-ttu-id="8d3e2-157">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-157">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span></span><br /><span data-ttu-id="8d3e2-158">
<a href=""></a>[<strong>D3D12_HEAP_FLAG</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_heap_flags)</span><span class="sxs-lookup"><span data-stu-id="8d3e2-158">
<a href=""></a>[<strong>D3D12_HEAP_FLAG</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags)</span></span><br /><span data-ttu-id="8d3e2-159">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-159">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span></span><br /><span data-ttu-id="8d3e2-160">
<a href=""></a>[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="8d3e2-160">
<a href=""></a>[<strong>D3D12_RESOURCE_STATES</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d3e2-161"><a href="/windows/desktop/dxmath/xmvector-data-type"><strong>Xmvector</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-161"><a href="/windows/desktop/dxmath/xmvector-data-type"><strong>XMVECTOR</strong></a></span></span></td>
<td><dl><span data-ttu-id="8d3e2-162"><a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorset"><strong>Xmvector Set</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-162"><a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorset"><strong>XMVectorSet</strong></a></span></span><br /><span data-ttu-id="8d3e2-163">
<a href=""></a>[<strong>Xmcolorhsltor GB</strong>] (/windows/desktop/api/directxmath/nf-directxmath-xmcolorhsltorgb)</span><span class="sxs-lookup"><span data-stu-id="8d3e2-163">
<a href=""></a>[<strong>XMColorHSLToRGB</strong>](/windows/desktop/api/directxmath/nf-directxmath-xmcolorhsltorgb)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="upload-the-texture-data"></a><span data-ttu-id="8d3e2-164">Hochladen der Textur Daten</span><span class="sxs-lookup"><span data-stu-id="8d3e2-164">Upload the texture data</span></span>

<span data-ttu-id="8d3e2-165">Textur Daten werden über einen uploadheap in die GPU hochgeladen, und Srvs werden für jeden erstellt und in einem SRV-deskriptorheap gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8d3e2-165">Texture data is uploaded to the GPU via an upload heap and SRVs are created for each and stored in an SRV descriptor heap.</span></span>

``` syntax
         // Upload texture data to the default heap resources.
            {
                const UINT subresourceCount = textureDesc.DepthOrArraySize * textureDesc.MipLevels;
                const UINT64 uploadBufferStep = GetRequiredIntermediateSize(m_cityMaterialTextures[0].Get(), 0, subresourceCount); // All of our textures are the same size in this case.
                const UINT64 uploadBufferSize = uploadBufferStep * CityMaterialCount;
                CD3DX12_HEAP_PROPERTIES uploadHeap(D3D12_HEAP_TYPE_UPLOAD);
                auto uploadDesc = CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize);
                ThrowIfFailed(m_device->CreateCommittedResource(
                    &uploadHeap,
                    D3D12_HEAP_FLAG_NONE,
                    &uploadDesc,
                    D3D12_RESOURCE_STATE_GENERIC_READ,
                    nullptr,
                    IID_PPV_ARGS(&materialsUploadHeap)));

                for (int i = 0; i < CityMaterialCount; ++i)
                {
                    // Copy data to the intermediate upload heap and then schedule 
                    // a copy from the upload heap to the appropriate texture.
                    D3D12_SUBRESOURCE_DATA textureData = {};
                    textureData.pData = &cityTextureData[i][0];
                    textureData.RowPitch = static_cast<LONG_PTR>((CityMaterialTextureChannelCount * textureDesc.Width));
                    textureData.SlicePitch = textureData.RowPitch * textureDesc.Height;

                    UpdateSubresources(m_commandList.Get(), m_cityMaterialTextures[i].Get(), materialsUploadHeap.Get(), i * uploadBufferStep, 0, subresourceCount, &textureData);
                    auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_cityMaterialTextures[i].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE);
                    m_commandList->ResourceBarrier(1, &barrier);
                }
            }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8d3e2-166">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="8d3e2-166">Call flow</span></span></th>
<th><span data-ttu-id="8d3e2-167">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d3e2-167">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8d3e2-168"><a href="getrequiredintermediatesize.md"><strong>Getrequiredintermediatesize</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-168"><a href="getrequiredintermediatesize.md"><strong>GetRequiredIntermediateSize</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="8d3e2-169"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>"Kreatecommittedresource"</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-169"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="8d3e2-170"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-170"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br /><span data-ttu-id="8d3e2-171">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-171">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span></span><br /><span data-ttu-id="8d3e2-172">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-172">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span></span><br /><span data-ttu-id="8d3e2-173">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-173">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span></span><br /><span data-ttu-id="8d3e2-174">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-174">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d3e2-175"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data"><strong>D3D12_SUBRESOURCE_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-175"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data"><strong>D3D12_SUBRESOURCE_DATA</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="8d3e2-176"><a href="updatesubresources1.md"><strong>UpdateSubresources</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-176"><a href="updatesubresources1.md"><strong>UpdateSubresources</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8d3e2-177"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>Resourcebarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-177"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><dl><span data-ttu-id="8d3e2-178"><a href="/windows/desktop/direct3d12/cd3dx12-resource-barrier"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-178"><a href="/windows/desktop/direct3d12/cd3dx12-resource-barrier"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br /><span data-ttu-id="8d3e2-179">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-179">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="load-the-diffuse-texture"></a><span data-ttu-id="8d3e2-180">Diffuses Textur laden</span><span class="sxs-lookup"><span data-stu-id="8d3e2-180">Load the diffuse texture</span></span>

<span data-ttu-id="8d3e2-181">Die diffuse Textur g wird \_ `txDiffuse` auf ähnliche Weise hochgeladen und erhält auch einen eigenen SRV, aber die Textur Daten sind bereits in "occcity. bin" definiert.</span><span class="sxs-lookup"><span data-stu-id="8d3e2-181">The diffuse texture, g\_`txDiffuse`, is uploaded in a similar manner and also gets its own SRV, but the texture data is already defined in occcity.bin.</span></span>

``` syntax
// Load the occcity diffuse texture with baked-in ambient lighting.
        // This texture will be blended with a texture from the materials
        // array in the pixel shader.
        {
            D3D12_RESOURCE_DESC textureDesc = {};
            textureDesc.MipLevels = SampleAssets::Textures[0].MipLevels;
            textureDesc.Format = SampleAssets::Textures[0].Format;
            textureDesc.Width = SampleAssets::Textures[0].Width;
            textureDesc.Height = SampleAssets::Textures[0].Height;
            textureDesc.Flags = D3D12_RESOURCE_FLAG_NONE;
            textureDesc.DepthOrArraySize = 1;
            textureDesc.SampleDesc.Count = 1;
            textureDesc.SampleDesc.Quality = 0;
            textureDesc.Dimension = D3D12_RESOURCE_DIMENSION_TEXTURE2D;

            CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_DEFAULT);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &heapProps,
                D3D12_HEAP_FLAG_NONE,
                &textureDesc,
                D3D12_RESOURCE_STATE_COPY_DEST,
                nullptr,
                IID_PPV_ARGS(&m_cityDiffuseTexture)));

            const UINT subresourceCount = textureDesc.DepthOrArraySize * textureDesc.MipLevels;
            const UINT64 uploadBufferSize = GetRequiredIntermediateSize(m_cityDiffuseTexture.Get(), 0, subresourceCount);
            CD3DX12_HEAP_PROPERTIES uploadHeap(D3D12_HEAP_TYPE_UPLOAD);
            auto uploadDesc = CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &uploadHeap,
                D3D12_HEAP_FLAG_NONE,
                &uploadDesc,
                D3D12_RESOURCE_STATE_GENERIC_READ,
                nullptr,
                IID_PPV_ARGS(&textureUploadHeap)));

            // Copy data to the intermediate upload heap and then schedule 
            // a copy from the upload heap to the diffuse texture.
            D3D12_SUBRESOURCE_DATA textureData = {};
            textureData.pData = pMeshData + SampleAssets::Textures[0].Data[0].Offset;
            textureData.RowPitch = SampleAssets::Textures[0].Data[0].Pitch;
            textureData.SlicePitch = SampleAssets::Textures[0].Data[0].Size;

            UpdateSubresources(m_commandList.Get(), m_cityDiffuseTexture.Get(), textureUploadHeap.Get(), 0, 0, subresourceCount, &textureData);
            auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_cityDiffuseTexture.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE);
            m_commandList->ResourceBarrier(1, &barrier);
        }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8d3e2-182">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="8d3e2-182">Call flow</span></span></th>
<th><span data-ttu-id="8d3e2-183">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d3e2-183">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8d3e2-184"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc"><strong>D3D12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-184"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc"><strong>D3D12_RESOURCE_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="8d3e2-185"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-185"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span></span><br /><span data-ttu-id="8d3e2-186">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension"><strong>D3D12_RESOURCE_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-186">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension"><strong>D3D12_RESOURCE_DIMENSION</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d3e2-187"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>"Kreatecommittedresource"</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-187"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="8d3e2-188"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-188"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br /><span data-ttu-id="8d3e2-189">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-189">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span></span><br /><span data-ttu-id="8d3e2-190">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-190">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span></span><br /><span data-ttu-id="8d3e2-191">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-191">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span></span><br /><span data-ttu-id="8d3e2-192">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-192">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d3e2-193"><a href="getrequiredintermediatesize.md"><strong>Getrequiredintermediatesize</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-193"><a href="getrequiredintermediatesize.md"><strong>GetRequiredIntermediateSize</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="8d3e2-194"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>"Kreatecommittedresource"</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-194"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="8d3e2-195"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-195"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br /><span data-ttu-id="8d3e2-196">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-196">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span></span><br /><span data-ttu-id="8d3e2-197">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-197">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span></span><br /><span data-ttu-id="8d3e2-198">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-198">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span></span><br /><span data-ttu-id="8d3e2-199">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-199">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d3e2-200"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data"><strong>D3D12_SUBRESOURCE_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-200"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data"><strong>D3D12_SUBRESOURCE_DATA</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="8d3e2-201"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>Resourcebarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-201"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><dl><span data-ttu-id="8d3e2-202"><a href="/windows/desktop/direct3d12/cd3dx12-resource-barrier"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-202"><a href="/windows/desktop/direct3d12/cd3dx12-resource-barrier"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br /><span data-ttu-id="8d3e2-203">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-203">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="create-a-sampler"></a><span data-ttu-id="8d3e2-204">Erstellen eines Samplers</span><span class="sxs-lookup"><span data-stu-id="8d3e2-204">Create a sampler</span></span>

<span data-ttu-id="8d3e2-205">Schließlich wird für **loadassets** ein einzelner Sampler erstellt, um eine Stichprobe aus der diffusen Textur oder dem Textur Array zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8d3e2-205">Finally for **LoadAssets**, a single sampler is created to sample from either the diffuse texture or the texture array.</span></span>

``` syntax
 // Describe and create a sampler.
        D3D12_SAMPLER_DESC samplerDesc = {};
        samplerDesc.Filter = D3D12_FILTER_MIN_MAG_MIP_LINEAR;
        samplerDesc.AddressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
        samplerDesc.AddressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
        samplerDesc.AddressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
        samplerDesc.MinLOD = 0;
        samplerDesc.MaxLOD = D3D12_FLOAT32_MAX;
        samplerDesc.MipLODBias = 0.0f;
        samplerDesc.MaxAnisotropy = 1;
        samplerDesc.ComparisonFunc = D3D12_COMPARISON_FUNC_ALWAYS;
        m_device->CreateSampler(&samplerDesc, m_samplerHeap->GetCPUDescriptorHandleForHeapStart());

        // Create SRV for the city's diffuse texture.
        CD3DX12_CPU_DESCRIPTOR_HANDLE srvHandle(m_cbvSrvHeap->GetCPUDescriptorHandleForHeapStart(), 0, m_cbvSrvDescriptorSize);
        D3D12_SHADER_RESOURCE_VIEW_DESC diffuseSrvDesc = {};
        diffuseSrvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
        diffuseSrvDesc.Format = SampleAssets::Textures->Format;
        diffuseSrvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
        diffuseSrvDesc.Texture2D.MipLevels = 1;
        m_device->CreateShaderResourceView(m_cityDiffuseTexture.Get(), &diffuseSrvDesc, srvHandle);
        srvHandle.Offset(m_cbvSrvDescriptorSize);

        // Create SRVs for each city material.
        for (int i = 0; i < CityMaterialCount; ++i)
        {
            D3D12_SHADER_RESOURCE_VIEW_DESC materialSrvDesc = {};
            materialSrvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
            materialSrvDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
            materialSrvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
            materialSrvDesc.Texture2D.MipLevels = 1;
            m_device->CreateShaderResourceView(m_cityMaterialTextures[i].Get(), &materialSrvDesc, srvHandle);

            srvHandle.Offset(m_cbvSrvDescriptorSize);
        }   
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8d3e2-206">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="8d3e2-206">Call flow</span></span></th>
<th><span data-ttu-id="8d3e2-207">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d3e2-207">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8d3e2-208"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc"><strong>D3D12_SAMPLER_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-208"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc"><strong>D3D12_SAMPLER_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="8d3e2-209"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter"><strong>D3D12_FILTER</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-209"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter"><strong>D3D12_FILTER</strong></a></span></span><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode"></a><br />
<span data-ttu-id="8d3e2-210">D3D12_FLOAT32_MAX (<a href="constants.md"><strong>Konstanten</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="8d3e2-210">D3D12_FLOAT32_MAX (<a href="constants.md"><strong>Constants</strong></a>)</span></span><br /><span data-ttu-id="8d3e2-211">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func"><strong>D3D12_COMPARISON_FUNC</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-211">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func"><strong>D3D12_COMPARISON_FUNC</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d3e2-212"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createsampler"><strong>"Kreatesampler"</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-212"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createsampler"><strong>CreateSampler</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8d3e2-213"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-213"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="8d3e2-214"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>Getcpudescriptor Lenker forheapstart</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-214"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d3e2-215"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-215"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="8d3e2-216"><a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-216"><a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span></span><br /><span data-ttu-id="8d3e2-217">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-217">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d3e2-218"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>"Kreateshaderresourceview"</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-218"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="8d3e2-219"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-219"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="8d3e2-220"><a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-220"><a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span></span><br /><span data-ttu-id="8d3e2-221">
<a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-221">
<a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span></span><br /><span data-ttu-id="8d3e2-222">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-222">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d3e2-223"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>"Kreateshaderresourceview"</strong></a></span><span class="sxs-lookup"><span data-stu-id="8d3e2-223"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

## <a name="dynamically-change-the-root-parameter-index"></a><span data-ttu-id="8d3e2-224">Dynamisches Ändern des Stamm Parameter Indexes</span><span class="sxs-lookup"><span data-stu-id="8d3e2-224">Dynamically change the root parameter index</span></span>

<span data-ttu-id="8d3e2-225">Wenn wir die Szene jetzt Rendering haben, würden alle Städte identisch sein, da wir den Wert der Stamm Konstante nicht festgelegt haben `matIndex` .</span><span class="sxs-lookup"><span data-stu-id="8d3e2-225">If we were to render the scene now, all of the cities would appear the same, because we have not set the value of our root constant, `matIndex`.</span></span> <span data-ttu-id="8d3e2-226">Jeder Pixelshader würde in den nullten-Slot von indizieren, `g_txMats` und die Szene würde wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="8d3e2-226">Each pixel shader would index into the 0th slot of `g_txMats` and the scene would look like this:</span></span>

![Alle Städte werden in derselben Farbe angezeigt.](images/dynamicindexing-image1.png)

<span data-ttu-id="8d3e2-228">Der Wert der root-Konstante wird in **frameresource::P opulatecommandlists** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8d3e2-228">The value of the root constant is set in **FrameResource::PopulateCommandLists**.</span></span> <span data-ttu-id="8d3e2-229">In der Double **for** -Schleife, in der ein Draw-Befehl für jede Stadt aufgezeichnet wird, zeichnen wir einen [**SetGraphicsRoot32BitConstants**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants) auf, der den Stamm Parameter Index in Bezug auf die Stamm Signatur angibt – in diesem Fall 3 – den Wert des dynamischen Indexes und einen Offset – in diesem Fall 0.</span><span class="sxs-lookup"><span data-stu-id="8d3e2-229">In the double **for** loop where a draw command is recorded for each city, we record a call to [**SetGraphicsRoot32BitConstants**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants) specifying our root parameter index in regards to the root signature – in this case 3 – the value of the dynamic index and an offset – in this case 0.</span></span> <span data-ttu-id="8d3e2-230">Da die Länge von `g_txMats` gleich der Anzahl der von uns erstellenden Städte ist, wird der Wert des Indexes für jede Stadt inkrementell festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8d3e2-230">Since the length of `g_txMats` is equal to the number of cities we render, the value of the index is incrementally set for each city.</span></span>

``` syntax
 for (UINT i = 0; i < m_cityRowCount; i++)
    {
        for (UINT j = 0; j < m_cityColumnCount; j++)
        {
            pCommandList->SetPipelineState(pPso);

            // Set the city's root constant for dynamically indexing into the material array.
            pCommandList->SetGraphicsRoot32BitConstant(3, (i * m_cityColumnCount) + j, 0);

            // Set this city's CBV table and move to the next descriptor.
            pCommandList->SetGraphicsRootDescriptorTable(2, cbvSrvHandle);
            cbvSrvHandle.Offset(cbvSrvDescriptorSize);

            pCommandList->DrawIndexedInstanced(numIndices, 1, 0, 0, 0);
        }
    }
```



| <span data-ttu-id="8d3e2-231">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="8d3e2-231">Call flow</span></span>                                                                                          | <span data-ttu-id="8d3e2-232">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d3e2-232">Parameters</span></span> |
|----------------------------------------------------------------------------------------------------|------------|
| [<span data-ttu-id="8d3e2-233">**Setpipelinestate**</span><span class="sxs-lookup"><span data-stu-id="8d3e2-233">**SetPipelineState**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)                             |            |
| [<span data-ttu-id="8d3e2-234">**SetGraphicsRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="8d3e2-234">**SetGraphicsRoot32BitConstant**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstant)     |            |
| [<span data-ttu-id="8d3e2-235">**Setgraphicsrootdescriptor Table**</span><span class="sxs-lookup"><span data-stu-id="8d3e2-235">**SetGraphicsRootDescriptorTable**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable) |            |
| [<span data-ttu-id="8d3e2-236">**Drawindexedinstangeleitet**</span><span class="sxs-lookup"><span data-stu-id="8d3e2-236">**DrawIndexedInstanced**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)                     |            |

## <a name="run-the-sample"></a><span data-ttu-id="8d3e2-237">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="8d3e2-237">Run the sample</span></span>

<span data-ttu-id="8d3e2-238">Wenn wir nun die Szene Rendering, hat jede Stadt einen anderen Wert für, `matIndex` und es wird daher eine andere Textur angezeigt, von `g_txMats[]` der die Szene wie folgt aussieht:</span><span class="sxs-lookup"><span data-stu-id="8d3e2-238">Now when we render the scene, each city will have a different value for `matIndex` and will thus look up a different texture from `g_txMats[]` making the scene look like this:</span></span>

![Alle Städte werden in unterschiedlichen Farben angezeigt.](images/dynamicindexing-image2.png)

## <a name="related-topics"></a><span data-ttu-id="8d3e2-240">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="8d3e2-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d3e2-241">D3D12-Code Exemplarische Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="8d3e2-241">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)
</dt> <dt>

[<span data-ttu-id="8d3e2-242">Effekt-Compilertool</span><span class="sxs-lookup"><span data-stu-id="8d3e2-242">Effect-Compiler Tool</span></span>](/windows/desktop/direct3dtools/fxc)
</dt> <dt>

[<span data-ttu-id="8d3e2-243">HLSL-Shader-Modell 5,1 Features für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="8d3e2-243">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[<span data-ttu-id="8d3e2-244">Ressourcen Bindung in HLSL</span><span class="sxs-lookup"><span data-stu-id="8d3e2-244">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="8d3e2-245">Shadermodell 5,1</span><span class="sxs-lookup"><span data-stu-id="8d3e2-245">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="8d3e2-246">Angeben von Stamm Signaturen in HLSL</span><span class="sxs-lookup"><span data-stu-id="8d3e2-246">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>
