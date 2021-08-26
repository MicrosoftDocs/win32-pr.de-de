---
title: Erstellen von Deskriptoren
description: Beschreibt und zeigt Beispiele zum Erstellen von Index-, Scheitelpunkt- und Konstantenpufferansichten. Shaderressource, Renderziel, ungeordneter Zugriff, Streamausgabe und Tiefenschablonenansichten; und Sampler. Alle Methoden zum Erstellen von Deskriptoren sind frei gethreadt.
ms.assetid: 0D360A7C-8A2F-49E1-A5CC-98C958B59D1C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 915cf1d92165f6d802bf4e8698180675a3edb32bd77da0510f4d9b52d6e044b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069710"
---
# <a name="creating-descriptors"></a>Erstellen von Deskriptoren

Beschreibt und zeigt Beispiele zum Erstellen von Index-, Scheitelpunkt- und Konstantenpufferansichten. Shaderressource, Renderziel, ungeordneter Zugriff, Streamausgabe und Tiefenschablonenansichten; und Sampler. Alle Methoden zum Erstellen von Deskriptoren sind frei gethreadt.

-   [Indexpufferansicht](#index-buffer-view)
-   [Vertexpufferansicht](#vertex-buffer-view)
-   [Shader-Ressourcenansicht](#shader-resource-view)
-   [Konstantenpufferansicht](#constant-buffer-view)
-   [Sampler](#sampler)
-   [Ungeordnete Zugriffsansicht](#unordered-access-view)
-   [Streamausgabeansicht](#stream-output-view)
-   [Renderzielansicht](#render-target-view)
-   [Tiefenschablonenansicht](#depth-stencil-view)
-   [Zugehörige Themen](#related-topics)

## <a name="index-buffer-view"></a>Indexpufferansicht

Um eine Indexpufferansicht zu erstellen, füllen Sie eine [**D3D12 \_ INDEX \_ BUFFER \_ VIEW-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_index_buffer_view) aus:

``` syntax
typedef struct D3D12_INDEX_BUFFER_VIEW
{
    D3D12_GPU_VIRTUAL_ADDRESS BufferLocation;
    UINT SizeInBytes;
    DXGI_FORMAT Format;
}   D3D12_INDEX_BUFFER_VIEW;
```

Legen Sie den Speicherort [**(GetGPUVirtualAddress)**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress)und die Größe des Puffers fest, und notieren Sie, dass D3D12 \_ GPU VIRTUAL ADDRESS wie folgt definiert \_ \_ ist:

`typedef UINT64 D3D12_GPU_VIRTUAL_ADDRESS;`

Weitere Informationen finden Sie in der [**DXGI \_ FORMAT-Enumeration.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) In der Regel kann für einen Indexpuffer die folgende Definition verwendet werden:

`const DXGI_FORMAT StandardIndexFormat = DXGI_FORMAT_R32_UINT;`

Rufen Sie abschließend [**ID3D12GraphicsCommandList::IASetIndexBuffer auf.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

Beispiel:


```C++
// Initialize the index buffer view.
m_indexBufferView.BufferLocation = m_indexBuffer->GetGPUVirtualAddress();
m_indexBufferView.SizeInBytes = SampleAssets::IndexDataSize;
m_indexBufferView.Format = SampleAssets::StandardIndexFormat;
```



## <a name="vertex-buffer-view"></a>Vertexpufferansicht

Um eine Scheitelpunktpufferansicht zu erstellen, füllen Sie eine [**D3D12 \_ VERTEX \_ BUFFER \_ VIEW-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view) aus:

``` syntax
typedef struct D3D12_VERTEX_BUFFER_VIEW {
    D3D12_GPU_VIRTUAL_ADDRESS BufferLocation;  
    UINT SizeInBytes;  
    UINT StrideInBytes;  
} D3D12_VERTEX_BUFFER_VIEW;
```

Legen Sie den Speicherort [**(GetGPUVirtualAddress)**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress)und die Größe des Puffers fest, und notieren Sie, dass D3D12 \_ GPU VIRTUAL ADDRESS wie folgt definiert \_ \_ ist:

`typedef UINT64 D3D12_GPU_VIRTUAL_ADDRESS;`

Der Schritt ist in der Regel die Größe einer einzelnen Vertexdatenstruktur, z. B. `sizeof(Vertex);` , und rufen Sie dann [**ID3D12GraphicsCommandList::IASetVertexBuffers auf.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)

Beispiel:


```C++
// Initialize the vertex buffer view.
m_vertexBufferView.BufferLocation = m_vertexBuffer->GetGPUVirtualAddress();
m_vertexBufferView.SizeInBytes = SampleAssets::VertexDataSize;
m_vertexBufferView.StrideInBytes = SampleAssets::StandardVertexStride;
```



## <a name="shader-resource-view"></a>Shader-Ressourcenansicht

Um eine Shaderressourcenansicht zu erstellen, füllen Sie eine [**D3D12 \_ SHADER \_ RESOURCE VIEW \_ \_ DESC-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc) aus:

``` syntax
typedef struct D3D12_SHADER_RESOURCE_VIEW_DESC  
    {  
    DXGI_FORMAT Format;  
    D3D12_SRV_DIMENSION ViewDimension;  
    UINT Shader4ComponentMapping;  
    union   
        {  
        D3D12_BUFFER_SRV Buffer;  
        D3D12_TEX1D_SRV Texture1D;  
        D3D12_TEX1D_ARRAY_SRV Texture1DArray;  
        D3D12_TEX2D_SRV Texture2D;  
        D3D12_TEX2D_ARRAY_SRV Texture2DArray;  
        D3D12_TEX2DMS_SRV Texture2DMS;  
        D3D12_TEX2DMS_ARRAY_SRV Texture2DMSArray;  
        D3D12_TEX3D_SRV Texture3D;  
        D3D12_TEXCUBE_SRV TextureCube;  
        D3D12_TEXCUBE_ARRAY_SRV TextureCubeArray;  
        }   ;  
    }   D3D12_SHADER_RESOURCE_VIEW_DESC; 
```

Das `ViewDimension` Feld ist auf 0 (null) oder einen Wert der Enumeration [**D3D12 \_ BUFFER \_ SRV \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags) festgelegt.

Die Enumerationen und Strukturen, auf die von [**D3D12 \_ SHADER \_ RESOURCE VIEW \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc) verwiesen wird, sind:

-   [**\_DXGI-FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**D3D12 \_ BUFFER \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_srv)
-   [**D3D12 \_ TEX1D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_srv)
-   [**D3D12 \_ TEX1D \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [**D3D12 \_ TEX2D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2DMS \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_srv)
-   [**D3D12 \_ TEX2DMS \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [**D3D12 \_ TEX3D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_srv)
-   [**D3D12 \_ TEXCUBE \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_srv)
-   [**D3D12 \_ TEXCUBE \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_array_srv)

Beachten Sie unten, dass float `ResourceMinLODClamp` zu SRVs für Tex1D/2D/3D/Cube hinzugefügt wurde. In D3D11 war es eine Eigenschaft einer Ressource, aber dies stimmte nicht mit der Implementierung in der Hardware überein. `StructureByteStride` wurde Puffer-SRVs hinzugefügt, wobei es sich in D3D11 um eine Eigenschaft der Ressource handelte. Wenn der Schritt ungleich 0 (null) ist, gibt dies eine strukturierte Pufferansicht an, und das Format muss auf DXGI FORMAT UNKNOWN festgelegt \_ \_ werden.

Rufen Sie zum Erstellen der Shaderressourcenansicht schließlich [**ID3D12Device::CreateShaderResourceView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)auf.

Beispiel:


```C++
// Describe and create an SRV.
D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
srvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
srvDesc.Format = tex.Format;
srvDesc.Texture2D.MipLevels = tex.MipLevels;
srvDesc.Texture2D.MostDetailedMip = 0;
srvDesc.Texture2D.ResourceMinLODClamp = 0.0f;
m_device->CreateShaderResourceView(m_textures[i].Get(), &srvDesc, cbvSrvHandle);
```



## <a name="constant-buffer-view"></a>Konstantenpufferansicht

Füllen Sie zum Erstellen einer konstanten Pufferansicht eine [**D3D12 \_ CONSTANT BUFFER VIEW \_ \_ \_ DESC-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc) aus:

``` syntax
typedef struct D3D12_CONSTANT_BUFFER_VIEW_DESC {
  D3D12_GPU_VIRTUAL_ADDRESS BufferLocation;
  UINT   SizeInBytes;
} D3D12_CONSTANT_BUFFER_VIEW_DESC;
```

Rufen Sie dann [**ID3D12Device::CreateConstantBufferView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)auf.

Beispiel:


```C++
// Describe and create a constant buffer view.
D3D12_CONSTANT_BUFFER_VIEW_DESC cbvDesc = {};
cbvDesc.BufferLocation = m_constantBuffer->GetGPUVirtualAddress();
cbvDesc.SizeInBytes = (sizeof(ConstantBuffer) + 255) & ~255;    // CB size is required to be 256-byte aligned.
m_device->CreateConstantBufferView(&cbvDesc, m_cbvHeap->GetCPUDescriptorHandleForHeapStart());
```



## <a name="sampler"></a>Sampler

Füllen Sie zum Erstellen eines Beispiels eine [**D3D12 \_ SAMPLER \_ DESC-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc) aus:

``` syntax
typedef struct D3D12_SAMPLER_DESC
{
    D3D12_FILTER Filter;
    D3D12_TEXTURE_ADDRESS_MODE AddressU;
    D3D12_TEXTURE_ADDRESS_MODE AddressV;
    D3D12_TEXTURE_ADDRESS_MODE AddressW;
    FLOAT MipLODBias;
    UINT MaxAnisotropy;
    D3D12_COMPARISON_FUNC ComparisonFunc;
    FLOAT BorderColor[4]; // RGBA
    FLOAT MinLOD;
    FLOAT MaxLOD;
} D3D12_SAMPLER_DESC;
```

Informationen zum Ausfüllen dieser Struktur finden Sie in den folgenden Enumerationen:

-   [**D3D12-FILTER \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)
-   [**\_D3D12-FILTERTYP \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter_type)
-   [**D3D12 \_ FILTER \_ REDUCTION \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter_reduction_type)
-   [**D3D12 \_ \_ TEXTURADRESSMODUS \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode)
-   [**\_D3D12-VERGLEICHS-FUNC \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func)

Rufen Sie abschließend [**ID3D12Device::CreateSampler**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createsampler)auf.

Beispiel:


```C++
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
```



## <a name="unordered-access-view"></a>Ungeordnete Zugriffsansicht

Um eine ungeordnete Zugriffsansicht zu erstellen, füllen Sie eine [**D3D12 \_ UNORDERED \_ ACCESS VIEW \_ \_ DESC-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc) aus:

``` syntax
typedef struct D3D12_UNORDERED_ACCESS_VIEW_DESC
{
    DXGI_FORMAT Format;
    D3D12_UAV_DIMENSION ViewDimension;

    union
    {
        D3D12_BUFFER_UAV Buffer;
        D3D12_TEX1D_UAV Texture1D;
        D3D12_TEX1D_ARRAY_UAV Texture1DArray;
        D3D12_TEX2D_UAV Texture2D;
        D3D12_TEX2D_ARRAY_UAV Texture2DArray;
        D3D12_TEX3D_UAV Texture3D;
    };
} D3D12_UNORDERED_ACCESS_VIEW_DESC;
```

Das `ViewDimension` Feld ist auf 0 (null) oder einen Wert der Enumeration [**D3D12 \_ BUFFER \_ UAV \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) festgelegt.

Weitere Informationen finden Sie in den folgenden Enumerationen und Strukturen:

-   [**\_DXGI-FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**D3D12 \_ BUFFER \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav)
-   [**D3D12 \_ TEX1D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [**D3D12 \_ TEX1D \_ ARRAY \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [**D3D12 \_ TEX2D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)
-   [**D3D12 \_ TEX3D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

`StructureByteStride` wurde Puffer-UAVs hinzugefügt, wobei es sich in D3D11 um eine Eigenschaft der Ressource handelte. Wenn der Schritt ungleich 0 (null) ist, gibt dies eine strukturierte Pufferansicht an, und das Format muss auf DXGI FORMAT UNKNOWN festgelegt \_ \_ werden.

Rufen Sie abschließend [**ID3D12Device::CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)auf.

Beispiel:


```C++
// Create the unordered access views (UAVs) that store the results of the compute work.
CD3DX12_CPU_DESCRIPTOR_HANDLE processedCommandsHandle(m_cbvSrvUavHeap->GetCPUDescriptorHandleForHeapStart(), ProcessedCommandsOffset, m_cbvSrvUavDescriptorSize);
for (UINT frame = 0; frame < FrameCount; frame++)
{
    // Allocate a buffer large enough to hold all of the indirect commands
    // for a single frame as well as a UAV counter.
    commandBufferDesc = CD3DX12_RESOURCE_DESC::Buffer(CommandBufferSizePerFrame + sizeof(UINT), D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS);
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &commandBufferDesc,
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_processedCommandBuffers[frame])));

    D3D12_UNORDERED_ACCESS_VIEW_DESC uavDesc = {};
    uavDesc.Format = DXGI_FORMAT_UNKNOWN;
    uavDesc.ViewDimension = D3D12_UAV_DIMENSION_BUFFER;
    uavDesc.Buffer.FirstElement = 0;
    uavDesc.Buffer.NumElements = TriangleCount;
    uavDesc.Buffer.StructureByteStride = sizeof(IndirectCommand);
    uavDesc.Buffer.CounterOffsetInBytes = CommandBufferSizePerFrame;
    uavDesc.Buffer.Flags = D3D12_BUFFER_UAV_FLAG_NONE;

    m_device->CreateUnorderedAccessView(            
        m_processedCommandBuffers[frame].Get(),
        m_processedCommandBuffers[frame].Get(),
        &uavDesc,
        processedCommandsHandle);

    processedCommandsHandle.Offset(CbvSrvUavDescriptorCountPerFrame, m_cbvSrvUavDescriptorSize);
}

// Allocate a buffer that can be used to reset the UAV counters and initialize it to 0.
ThrowIfFailed(m_device->CreateCommittedResource(
    &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
    D3D12_HEAP_FLAG_NONE,
    &CD3DX12_RESOURCE_DESC::Buffer(sizeof(UINT)),
    D3D12_RESOURCE_STATE_GENERIC_READ,
    
    nullptr,
    IID_PPV_ARGS(&m_processedCommandBufferCounterReset)));

UINT8* pMappedCounterReset = nullptr;
CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
ThrowIfFailed(m_processedCommandBufferCounterReset->Map(0, &readRange, reinterpret_cast<void**>(&pMappedCounterReset)));
ZeroMemory(pMappedCounterReset, sizeof(UINT));
m_processedCommandBufferCounterReset->Unmap(0, nullptr);
```



## <a name="stream-output-view"></a>Streamausgabeansicht

Um eine Streamausgabeansicht zu erstellen, füllen Sie eine [**D3D12 \_ STREAM \_ OUTPUT \_ DESC-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) aus.

``` syntax
typedef struct D3D12_STREAM_OUTPUT_DESC  
    {  
    _Field_size_full_(NumEntries)  const D3D12_SO_DECLARATION_ENTRY *pSODeclaration;  
    UINT NumEntries;  
    _Field_size_full_(NumStrides)  const UINT *pBufferStrides;  
    UINT NumStrides;  
    UINT RasterizedStream;  
    }   D3D12_STREAM_OUTPUT_DESC;  
```

Rufen Sie dann [**ID3D12GraphicsCommandList::SOSetTargets auf.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets)

## <a name="render-target-view"></a>Renderzielansicht

Um eine Renderzielansicht zu erstellen, füllen Sie eine [**D3D12 \_ RENDER TARGET VIEW \_ \_ \_ DESC-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_view_desc) aus.

``` syntax
typedef struct D3D12_RENDER_TARGET_VIEW_DESC
{
    DXGI_FORMAT Format;
    D3D12_RTV_DIMENSION ViewDimension;

    union
    {
        D3D12_BUFFER_RTV Buffer;
        D3D12_TEX1D_RTV Texture1D;
        D3D12_TEX1D_ARRAY_RTV Texture1DArray;
        D3D12_TEX2D_RTV Texture2D;
        D3D12_TEX2D_ARRAY_RTV Texture2DArray;
        D3D12_TEX2DMS_RTV Texture2DMS;
        D3D12_TEX2DMS_ARRAY_RTV Texture2DMSArray;
        D3D12_TEX3D_RTV Texture3D;
    };
} D3D12_RENDER_TARGET_VIEW_DESC;
```

Das `ViewDimension` Feld ist auf 0 (null) oder einen Wert der Enumeration [**D3D12 \_ RTV \_ DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_rtv_dimension) festgelegt.

Weitere Informationen finden Sie in den folgenden Enumerationen und Strukturen:

-   [**\_DXGI-FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**D3D12 \_ BUFFER \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_rtv)
-   [**D3D12 \_ TEX1D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [**D3D12 \_ TEX1D \_ ARRAY \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [**D3D12 \_ TEX2D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [**D3D12 \_ TEX2DMS \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_rtv)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ TEX2DMS \_ ARRAY \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [**D3D12 \_ TEX3D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)

Rufen Sie abschließend [**ID3D12Device::CreateRenderTargetView auf.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)

Beispiel:

```C++
// Create descriptor heaps.
{
    // Describe and create a render target view (RTV) descriptor heap.
    D3D12_DESCRIPTOR_HEAP_DESC rtvHeapDesc = {};
    rtvHeapDesc.NumDescriptors = FrameCount;
    rtvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_RTV;
    rtvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
    ThrowIfFailed(m_device->CreateDescriptorHeap(&rtvHeapDesc, IID_PPV_ARGS(&m_rtvHeap)));

    m_rtvDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
}

// Create frame resources.
{
    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

    // Create a RTV for each frame.
    for (UINT n = 0; n < FrameCount; n++)
    {
        ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
        m_device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);
        rtvHandle.Offset(1, m_rtvDescriptorSize);
    }
```



## <a name="depth-stencil-view"></a>Tiefenschablonenansicht

Um eine Tiefenschablonenansicht zu erstellen, füllen Sie eine [**D3D12 \_ DEPTH \_ STENCIL \_ VIEW \_ DESC-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc) aus:

``` syntax
typedef struct D3D12_DEPTH_STENCIL_VIEW_DESC  
    {  
    DXGI_FORMAT Format;  
    D3D12_DSV_DIMENSION ViewDimension;  
    D3D12_DSV_FLAGS Flags;  
    union   
        {  
        D3D12_TEX1D_DSV Texture1D;  
        D3D12_TEX1D_ARRAY_DSV Texture1DArray;  
        D3D12_TEX2D_DSV Texture2D;  
        D3D12_TEX2D_ARRAY_DSV Texture2DArray;  
        D3D12_TEX2DMS_DSV Texture2DMS;  
        D3D12_TEX2DMS_ARRAY_DSV Texture2DMSArray;  
        }   ;  
    }   D3D12_DEPTH_STENCIL_VIEW_DESC;  
```

Das `ViewDimension` Feld ist auf 0 (null) oder einen Wert der [**D3D12 \_ DSV \_ DIMENSION-Enumeration**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_dsv_dimension) festgelegt. Die Flageinstellungen finden Sie in der [**D3D12 \_ DSV \_ FLAGS-Enumeration.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_dsv_flags)

Weitere Informationen finden Sie in den folgenden Aufzählen und Strukturen:

-   [**\_DXGI-FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**D3D12 \_ TEX1D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [**D3D12 \_ TEX1D \_ ARRAY \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [**D3D12 \_ TEX2D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [**D3D12 \_ TEX2DMS \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_dsv)
-   [**D3D12 \_ TEX2DMS \_ ARRAY \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)

Rufen Sie abschließend [**ID3D12Device::CreateDepthStencilView auf.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdepthstencilview)

Beispiel:


```C++
// Create the depth stencil view.
{
    D3D12_DEPTH_STENCIL_VIEW_DESC depthStencilDesc = {};
    depthStencilDesc.Format = DXGI_FORMAT_D32_FLOAT;
    depthStencilDesc.ViewDimension = D3D12_DSV_DIMENSION_TEXTURE2D;
    depthStencilDesc.Flags = D3D12_DSV_FLAG_NONE;

    D3D12_CLEAR_VALUE depthOptimizedClearValue = {};
    depthOptimizedClearValue.Format = DXGI_FORMAT_D32_FLOAT;
    depthOptimizedClearValue.DepthStencil.Depth = 1.0f;
    depthOptimizedClearValue.DepthStencil.Stencil = 0;

    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Tex2D(DXGI_FORMAT_D32_FLOAT, m_width, m_height, 1, 0, 1, 0, D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL),
        D3D12_RESOURCE_STATE_DEPTH_WRITE,
        &depthOptimizedClearValue,
        IID_PPV_ARGS(&m_depthStencil)
        ));

    m_device->CreateDepthStencilView(m_depthStencil.Get(), &depthStencilDesc, m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deskriptoren](descriptors.md)
</dt> <dt>

[Deskriptorheaps](descriptor-heaps.md)
</dt> </dl>

 

 