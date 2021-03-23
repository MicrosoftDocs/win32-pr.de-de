---
title: Erstellen von Deskriptoren
description: Beschreibt und zeigt Beispiele für das Erstellen von Index-, Vertex-und konstantenpuffersichten. Shader-Ressource, Renderziel, unsortierter Zugriff, Streamausgabe-und tiefen Schablonen Ansichten; und Samplers. Alle Methoden zum Erstellen von Deskriptoren sind frei Thread.
ms.assetid: 0D360A7C-8A2F-49E1-A5CC-98C958B59D1C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aac9aab5dde0f5ca0864fcc1627ade984c6b6ccf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548677"
---
# <a name="creating-descriptors"></a>Erstellen von Deskriptoren

Beschreibt und zeigt Beispiele für das Erstellen von Index-, Vertex-und konstantenpuffersichten. Shader-Ressource, Renderziel, unsortierter Zugriff, Streamausgabe-und tiefen Schablonen Ansichten; und Samplers. Alle Methoden zum Erstellen von Deskriptoren sind frei Thread.

-   [Index Puffer Ansicht](#index-buffer-view)
-   [Vertex-Puffer Ansicht](#vertex-buffer-view)
-   [Shader-Ressourcenansicht](#shader-resource-view)
-   [Konstante Puffer Ansicht](#constant-buffer-view)
-   [Sampler](#sampler)
-   [Ansicht für ungeordnete Zugriffe](#unordered-access-view)
-   [Stream-Ausgabe Ansicht](#stream-output-view)
-   [Ansicht des Renderziels](#render-target-view)
-   [Ansicht der tiefen Schablone](#depth-stencil-view)
-   [Verwandte Themen](#related-topics)

## <a name="index-buffer-view"></a>Index Puffer Ansicht

Füllen Sie zum Erstellen einer Index Puffer Ansicht eine [**D3D12- \_ Index \_ Puffer \_ Ansichts**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_index_buffer_view) Struktur aus:

``` syntax
typedef struct D3D12_INDEX_BUFFER_VIEW
{
    D3D12_GPU_VIRTUAL_ADDRESS BufferLocation;
    UINT SizeInBytes;
    DXGI_FORMAT Format;
}   D3D12_INDEX_BUFFER_VIEW;
```

Legen Sie den Speicherort ( [**getgpuvirtualaddress**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress)) und die Größe des Puffers fest. Beachten Sie dabei, dass die \_ virtuelle D3D12 GPU- \_ \_ Adresse wie folgt definiert ist:

`typedef UINT64 D3D12_GPU_VIRTUAL_ADDRESS;`

Weitere Informationen finden Sie in der [**DXGI- \_ formatenum**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) . In der Regel kann für einen Index Puffer folgende Definition verwendet werden:

`const DXGI_FORMAT StandardIndexFormat = DXGI_FORMAT_R32_UINT;`

Schließlich wird [**ID3D12GraphicsCommandList:: iasetindexbuffer**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)aufgerufen.

Beispiel:


```C++
// Initialize the index buffer view.
m_indexBufferView.BufferLocation = m_indexBuffer->GetGPUVirtualAddress();
m_indexBufferView.SizeInBytes = SampleAssets::IndexDataSize;
m_indexBufferView.Format = SampleAssets::StandardIndexFormat;
```



## <a name="vertex-buffer-view"></a>Vertex-Puffer Ansicht

Füllen Sie eine [**D3D12 \_ Vertex- \_ Puffer \_ Ansichts**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view) Struktur aus, um eine Vertex-Puffer Ansicht zu erstellen:

``` syntax
typedef struct D3D12_VERTEX_BUFFER_VIEW {
    D3D12_GPU_VIRTUAL_ADDRESS BufferLocation;  
    UINT SizeInBytes;  
    UINT StrideInBytes;  
} D3D12_VERTEX_BUFFER_VIEW;
```

Legen Sie den Speicherort ( [**getgpuvirtualaddress**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress)) und die Größe des Puffers fest. Beachten Sie dabei, dass die \_ virtuelle D3D12 GPU- \_ \_ Adresse wie folgt definiert ist:

`typedef UINT64 D3D12_GPU_VIRTUAL_ADDRESS;`

Der Stride-Wert ist in der Regel die Größe einer einzelnen Scheitelpunkt Datenstruktur, z `sizeof(Vertex);` . b., und dann [**ID3D12GraphicsCommandList:: iasetvertexbuffers**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)aufrufen.

Beispiel:


```C++
// Initialize the vertex buffer view.
m_vertexBufferView.BufferLocation = m_vertexBuffer->GetGPUVirtualAddress();
m_vertexBufferView.SizeInBytes = SampleAssets::VertexDataSize;
m_vertexBufferView.StrideInBytes = SampleAssets::StandardVertexStride;
```



## <a name="shader-resource-view"></a>Shader-Ressourcenansicht

Füllen Sie zum Erstellen einer shaderressourcenansicht eine [**D3D12 \_ Shader \_ Resource \_ View \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc) -Struktur Struktur aus:

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

Das `ViewDimension` Feld ist auf 0 (null) oder einen Wert der [**D3D12- \_ Puffer- \_ SRV- \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags) -Enumeration festgelegt.

Zu den Aufständen und Strukturen, auf die von der [**D3D12- \_ Shader- \_ Ressourcen \_ Ansicht \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc) verwiesen wird, gehören:

-   [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**D3D12- \_ Puffer- \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_srv)
-   [**D3D12 \_ TEX1D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_srv)
-   [**D3D12 \_ TEX1D- \_ Array ( \_ SRV)**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [**D3D12 \_ TEX2D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [**D3D12 \_ TEX2D- \_ Array ( \_ SRV)**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2DMS \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_srv)
-   [**D3D12 \_ TEX2DMS- \_ Array ( \_ SRV)**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [**D3D12 \_ TEX3D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_srv)
-   [**D3D12 \_ Texcube- \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_srv)
-   [**D3D12 \_ Texcube- \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_array_srv)

Beachten Sie, dass "float" `ResourceMinLODClamp` zu Srvs für Tex1D/2D/3D/Cube hinzugefügt wurde. In D3D11 war es eine Eigenschaft einer Ressource, aber dies entsprach nicht der Implementierung von Hardware. `StructureByteStride` wurde zu Buffer Srvs hinzugefügt, wobei in D3D11 eine Eigenschaft der Ressource war. Wenn der Stride-Wert ungleich 0 (null) ist, gibt eine strukturierte Puffer Ansicht an, und das Format muss auf das DXGI-Format Unknown festgelegt werden \_ \_ .

Zum Schluss rufen Sie zum Erstellen der Shader-Ressourcen Ansicht [**ID3D12Device:: | ateshaderresourceview**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)auf.

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



## <a name="constant-buffer-view"></a>Konstante Puffer Ansicht

Füllen Sie zum Erstellen einer Konstanten Puffer Ansicht die Struktur [**einer \_ Konstanten \_ Puffer \_ Ansicht \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc) aus:

``` syntax
typedef struct D3D12_CONSTANT_BUFFER_VIEW_DESC {
  D3D12_GPU_VIRTUAL_ADDRESS BufferLocation;
  UINT   SizeInBytes;
} D3D12_CONSTANT_BUFFER_VIEW_DESC;
```

Dann rufe ich [**ID3D12Device:: kreateconstantbufferview auf**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview).

Beispiel:


```C++
// Describe and create a constant buffer view.
D3D12_CONSTANT_BUFFER_VIEW_DESC cbvDesc = {};
cbvDesc.BufferLocation = m_constantBuffer->GetGPUVirtualAddress();
cbvDesc.SizeInBytes = (sizeof(ConstantBuffer) + 255) & ~255;    // CB size is required to be 256-byte aligned.
m_device->CreateConstantBufferView(&cbvDesc, m_cbvHeap->GetCPUDescriptorHandleForHeapStart());
```



## <a name="sampler"></a>Sampler

Füllen Sie zum Erstellen eines Beispiels eine [**D3D12 \_ Sampler \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc) -Erstellungs Struktur aus:

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

Weitere Informationen zum Ausfüllen dieser Struktur finden Sie in den folgenden Auffüllungen:

-   [**D3D12- \_ Filter**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)
-   [**D3D12 \_ - \_ Filtertyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter_type)
-   [**D3D12 \_ - \_ Reduzierungs \_ Typen**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter_reduction_type)
-   [**D3D12- \_ Textur \_ Adress \_ Modus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode)
-   [**D3D12 \_ Vergleichs- \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func)

Nennen Sie schließlich [**ID3D12Device::**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createsampler)"".

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



## <a name="unordered-access-view"></a>Ansicht für ungeordnete Zugriffe

Füllen Sie zum Erstellen einer Ansicht mit ungeordneten Zugriffen eine nicht [**geordnete zugriffsansichts \_ \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc) Struktur aus:

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

Das- `ViewDimension` Feld ist auf 0 (null) oder einen Wert der [**D3D12 buffer- \_ \_ UAV- \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) -Enumeration festgelegt.

Weitere Informationen finden Sie in den folgenden Aufständen und Strukturen:

-   [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**D3D12- \_ Puffer- \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav)
-   [**D3D12 \_ TEX1D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [**D3D12 \_ TEX1D \_ array- \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [**D3D12 \_ TEX2D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [**D3D12 \_ TEX2D \_ array- \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)
-   [**D3D12 \_ TEX3D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

`StructureByteStride` wurde zu Puffer-UAVs hinzugefügt, wobei in D3D11 eine Eigenschaft der Ressource war. Wenn der Stride-Wert ungleich 0 (null) ist, gibt eine strukturierte Puffer Ansicht an, und das Format muss auf das DXGI-Format Unknown festgelegt werden \_ \_ .

Zum Schluss wird [**ID3D12Device:: | ateunorderedaccessview**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)aufgerufen.

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



## <a name="stream-output-view"></a>Stream-Ausgabe Ansicht

Füllen Sie zum Erstellen einer Stream-Ausgabe Ansicht eine [**D3D12 \_ Stream- \_ Ausgabe \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) -Struktur aus.

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

Klicken Sie dann auf [**ID3D12GraphicsCommandList:: sosettargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets).

## <a name="render-target-view"></a>Ansicht des Renderziels

Um eine renderzielansicht zu erstellen, füllen Sie die DESC-Struktur einer [**D3D12- \_ \_ renderzielsicht \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_view_desc) aus.

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

Das- `ViewDimension` Feld ist auf 0 (null) oder einen Wert der [**D3D12 \_ RTV- \_ Dimensions**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_rtv_dimension) Enumeration festgelegt.

Weitere Informationen finden Sie in den folgenden Aufständen und Strukturen:

-   [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**D3D12 \_ \_ -Puffer-RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_rtv)
-   [**D3D12 \_ TEX1D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [**D3D12 \_ TEX1D \_ array \_ -RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [**D3D12 \_ TEX2D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [**D3D12 \_ TEX2DMS \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_rtv)
-   [**D3D12 \_ TEX2D \_ array \_ -RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ TEX2DMS \_ array \_ -RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [**D3D12 \_ TEX3D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)

Zum Schluss wird [**ID3D12Device:: ":: kreaterendertargetview**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)" aufgerufen.

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



## <a name="depth-stencil-view"></a>Ansicht der tiefen Schablone

Füllen Sie zum Erstellen einer Ansicht der tiefen Schablone die Struktur der Struktur der [**D3D12- \_ tiefen \_ Schablone \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc) aus:

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

Das- `ViewDimension` Feld ist auf 0 (null) oder einen Wert der [**D3D12 DSV- \_ \_ Dimensions**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_dsv_dimension) Enumeration festgelegt. Informationen zu den Flageinstellungen finden Sie in der [**D3D12 \_ DSV- \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_dsv_flags) -Enumeration.

Weitere Informationen finden Sie in den folgenden Aufständen und Strukturen:

-   [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**D3D12 \_ TEX1D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [**D3D12 \_ TEX1D \_ array- \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [**D3D12 \_ TEX2D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [**D3D12 \_ TEX2D \_ array- \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [**D3D12 \_ TEX2DMS \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_dsv)
-   [**D3D12 \_ TEX2DMS \_ array- \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)

Zum Schluss wird [**ID3D12Device:: | atedepthstencilview**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdepthstencilview)aufgerufen.

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



## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Deskriptoren](descriptors.md)
</dt> <dt>

[Deskriptorheaps](descriptor-heaps.md)
</dt> </dl>

 

 