---
title: Hochladen verschiedener Ressourcentypen
description: Zeigt, wie Sie einen Puffer verwenden, um sowohl konstante Pufferdaten als auch Scheitelpunktpufferdaten in die GPU hochzuladen, und wie Sie Daten ordnungsgemäß unterteilen und in Puffern platzieren.
ms.assetid: 255B0482-21D6-4276-8009-3F3891879CA1
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03d4755124bbadcdd255a6e99739b710845ab14
ms.sourcegitcommit: a30d0436a84986234df673c6def6694d5a8579f6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113563780"
---
# <a name="uploading-different-types-of-resources"></a>Hochladen verschiedener Ressourcentypen

Zeigt, wie Sie einen Puffer verwenden, um sowohl konstante Pufferdaten als auch Scheitelpunktpufferdaten in die GPU hochzuladen, und wie Sie Daten ordnungsgemäß unterteilen und in Puffern platzieren. Die Verwendung eines einzelnen Puffers erhöht die Flexibilität bei der Speicherauslastung und bietet Anwendungen eine strengere Kontrolle über die Speicherauslastung. Zeigt außerdem die Unterschiede zwischen den Modellen Direct3D 11 und Direct3D 12 zum Hochladen verschiedener Ressourcentypen.

## <a name="upload-different-types-of-resources"></a>Hochladen ressourcentypen

In Direct3D 12 erstellen Sie einen Puffer, der verschiedene Arten von Ressourcendaten zum Hochladen aufnehmen soll, und Sie kopieren Ressourcendaten auf ähnliche Weise für verschiedene Ressourcendaten in den gleichen Puffer. Anschließend werden einzelne Ansichten erstellt, um diese Ressourcendaten an die Grafikpipeline im Direct3D 12-Ressourcenbindungsmodell zu binden.

In Direct3D 11 erstellen Sie separate Puffer für verschiedene Arten von Ressourcendaten (beachten Sie die verschiedenen, die unten im Direct3D 11-Beispielcode verwendet werden), binden jeden Ressourcenpuffer explizit an die Grafikpipeline und aktualisieren die Ressourcendaten mit verschiedenen Methoden basierend auf verschiedenen `BindFlags` Ressourcentypen.

Sowohl in Direct3D 12 als auch in Direct3D 11 sollten Sie Ressourcen nur dann hochladen, wenn die CPU die Daten einmal schreibt, und die GPU liest sie einmal.

In einigen Fällen
* Die GPU liest die Daten mehrmals, oder
* Die GPU liest die Daten nicht linear, oder
* das Rendering ist bereits erheblich gpu-eingeschränkt.

In diesen Fällen ist es möglicherweise besser, [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) oder [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) zu verwenden, um die Uploadpufferdaten in eine Standardressource zu kopieren.

Eine Standardressource kann sich auf diskreten GPUs im physischen Videospeicher befinden.

### <a name="code-example-direct3d-11"></a>Codebeispiel: Direct3D 11

```cpp
// Direct3D 11: Separate buffers for each resource type.

void main()
{
    // ...

    // Create a constant buffer.
    float constantBufferData[] = ...;

    D3D11_BUFFER_DESC constantBufferDesc = {0};  
    constantBufferDesc.ByteWidth = sizeof(constantBufferData);  
    constantBufferDesc.Usage = D3D11_USAGE_DYNAMIC;  
    constantBufferDesc.BindFlags = D3D11_BIND_CONSTANT_BUFFER;  
    constantBufferDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;  

    ComPtr<ID3D11Buffer> constantBuffer;
    d3dDevice->CreateBuffer(  
        &constantBufferDesc,  
        NULL,
        &constantBuffer  
        );

    // Create a vertex buffer.
    float vertexBufferData[] = ...;

    D3D11_BUFFER_DESC vertexBufferDesc = { 0 };
    vertexBufferDesc.ByteWidth = sizeof(vertexBufferData);
    vertexBufferDesc.Usage = D3D11_USAGE_DYNAMIC;
    vertexBufferDesc.BindFlags = D3D11_BIND_VERTEX_BUFFER;

    ComPtr<ID3D11Buffer> vertexBuffer;
    d3dDevice->CreateBuffer(
        &vertexBufferDesc,
        NULL,
        &vertexBuffer
        );

    // ...
}

void DrawFrame()
{
    // ...

    // Bind buffers to the graphics pipeline.
    d3dDeviceContext->VSSetConstantBuffers(0, 1, constantBuffer.Get());
    d3dDeviceContext->IASetVertexBuffers(0, 1, vertexBuffer.Get(), ...);

    // Update the constant buffer.
    D3D11_MAPPED_SUBRESOURCE mappedResource;  
    d3dDeviceContext->Map(
        constantBuffer.Get(),
        0, 
        D3D11_MAP_WRITE_DISCARD,
        0,
        &mappedResource
        );
    memcpy(mappedResource.pData, constantBufferData,
        sizeof(contatnBufferData));
    d3dDeviceContext->Unmap(constantBuffer.Get(), 0);  

    // Update the vertex buffer.
    d3dDeviceContext->UpdateSubresource(
        vertexBuffer.Get(),
        0,
        NULL,
        vertexBufferData,
        sizeof(vertexBufferData),
        0
    );

    // ...
}
```

### <a name="code-example-direct3d-12"></a>Codebeispiel: Direct3D 12

```cpp
// Direct3D 12: One buffer to accommodate different types of resources

ComPtr<ID3D12Resource> m_spUploadBuffer;
UINT8* m_pDataBegin = nullptr;    // starting position of upload buffer
UINT8* m_pDataCur = nullptr;      // current position of upload buffer
UINT8* m_pDataEnd = nullptr;      // ending position of upload buffer

void main()
{
    //
    // Initialize an upload buffer
    //

    InitializeUploadBuffer(64 * 1024);

    // ...
}

void DrawFrame()
{
    // ...

    // Set vertices data to the upload buffer.

    float vertices[] = ...;
    UINT verticesOffset = 0;
    ThrowIfFailed(
        SetDataToUploadBuffer(
            vertices, sizeof(float), sizeof(vertices) / sizeof(float),
            sizeof(float), 
            verticesOffset
            ));

    // Set constant data to the upload buffer.

    float constants[] = ...;
    UINT constantsOffset = 0;
    ThrowIfFailed(
        SetDataToUploadBuffer(
            constants, sizeof(float), sizeof(constants) / sizeof(float), 
            D3D12_CONSTANT_BUFFER_DATA_PLACEMENT_ALIGNMENT, 
            constantsOffset
            ));

    // Create vertex buffer views for the new binding model.

    D3D12_VERTEX_BUFFER_VIEW vertexBufferViewDesc = {
        m_spUploadBuffer->GetGPUVirtualAddress() + verticesOffset,
        sizeof(vertices), // size
        sizeof(float) * 4,  // stride
    };

    commandList->IASetVertexBuffers( 
        0,
        1,
        &vertexBufferViewDesc,
        ));

    // Create constant buffer views for the new binding model.

    D3D12_CONSTANT_BUFFER_VIEW_DESC constantBufferViewDesc = {
        m_spUploadBuffer->GetGPUVirtualAddress() + constantsOffset,
        sizeof(constants) // size
         };

    d3dDevice->CreateConstantBufferView(
        &constantBufferViewDesc,
        ...
        ));

    // Continue command list building and execution ...
}

//
// Create an upload buffer and keep it always mapped.
//

HRESULT InitializeUploadBuffer(SIZE_T uSize)
{
    HRESULT hr = d3dDevice->CreateCommittedResource(
         &CD3DX12_HEAP_PROPERTIES( D3D12_HEAP_TYPE_UPLOAD ),    
               D3D12_HEAP_FLAG_NONE, 
               &CD3DX12_RESOURCE_DESC::Buffer( uSize ), 
               D3D12_RESOURCE_STATE_GENERIC_READ, nullptr,  
               IID_PPV_ARGS( &m_spUploadBuffer ) );

    if (SUCCEEDED(hr))
    {
        void* pData;
        //
        // No CPU reads will be done from the resource.
        //
        CD3DX12_RANGE readRange(0, 0);
        m_spUploadBuffer->Map( 0, &readRange, &pData ); 
        m_pDataCur = m_pDataBegin = reinterpret_cast< UINT8* >( pData );
        m_pDataEnd = m_pDataBegin + uSize;
    }
    return hr;
}

//
// Sub-allocate from the buffer, with offset aligned.
//

HRESULT SuballocateFromBuffer(SIZE_T uSize, UINT uAlign)
{
    m_pDataCur = reinterpret_cast< UINT8* >(
        Align(reinterpret_cast< SIZE_T >(m_pDataCur), uAlign)
        );

    return (m_pDataCur + uSize > m_pDataEnd) ? E_INVALIDARG : S_OK;
}

//
// Place and copy data to the upload buffer.
//

HRESULT SetDataToUploadBuffer(
    const void* pData, 
    UINT bytesPerData, 
    UINT dataCount, 
    UINT alignment, 
    UINT& byteOffset
    )
{
    SIZE_T byteSize = bytesPerData * dataCount;
    HRESULT hr = SuballocateFromBuffer(byteSize, alignment);
    if (SUCCEEDED(hr))
    {
        byteOffset = UINT(m_pDataCur - m_pDataBegin);
        memcpy(m_pDataCur, pData, byteSize); 
        m_pDataCur += byteSize;
    }
    return hr;
}

//
// Align uLocation to the next multiple of uAlign.
//

UINT Align(UINT uLocation, UINT uAlign)
{
    if ( (0 == uAlign) || (uAlign & (uAlign-1)) )
    {
        ThrowException("non-pow2 alignment");
    }

    return ( (uLocation + (uAlign-1)) & ~(uAlign-1) );
}
```

Beachten Sie die Verwendung der [**Hilfsstrukturen**](cd3dx12-heap-properties.md) CD3DX12_HEAP_PROPERTIES und [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md).

## <a name="constants"></a>Konstanten

Verwenden Sie die folgenden APIs, um Konstanten, Scheitelungen und Indizes innerhalb eines Upload- oder Readback-Heaps zu setzen.

-   [**ID3D12Device::CreateConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [**ID3D12GraphicsCommandList::IASetVertexBuffers**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [**ID3D12GraphicsCommandList::IASetIndexBuffer**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a>Ressourcen

Ressourcen sind das Direct3D-Konzept, das die Nutzung des physischen GPU-Speichers abstrahiert. Ressourcen benötigen virtuellen GPU-Adressraum für den Zugriff auf physischen Speicher. Die Ressourcenerstellung wird im Freethreading ausgeführt.

Es gibt drei Arten von Ressourcen in Bezug auf die Erstellung virtueller Adressen und die Flexibilität in Direct3D 12.

### <a name="committed-resources"></a>Ressourcen, für die ein Committed (Ressourcen

Die gängigste Idee von Direct3D-Ressourcen über die Generationen hinweg sind ressourcenverankerte Ressourcen. Beim Erstellen einer solchen Ressource wird ein virtueller Adressbereich, ein impliziter Heap, der groß genug ist, um die gesamte Ressource zu passen, und der virtuelle Adressbereich in den physischen Speicher, der vom Heap gekapselt wird, zuteilen. Die impliziten Heapeigenschaften müssen übergeben werden, damit sie mit der funktionalen Parität mit früheren Direct3D-Versionen übereinstimmen. Weitere Informationen [**finden Sie unter ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).

### <a name="reserved-resources"></a>Reservierte Ressourcen

Reservierte Ressourcen entsprechen gekachelten Direct3D 11-Ressourcen. Bei der Erstellung wird nur ein virtueller Adressbereich zugeordnet und keinen Heap zugeordnet. Die Anwendung wird diese Ressourcen später Heaps zuordnen. Die Funktionen solcher Ressourcen sind derzeit unverändert gegenüber Direct3D 11, da sie einem Heap mit einer Kachelgranularität von 64 KB mit [**UpdateTileMappings zugeordnet werden können.**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) Weitere Informationen [**finden Sie unter ID3D12Device::CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).

### <a name="placed-resources"></a>Platzierte Ressourcen

Neu für Direct3D 12: Sie können Heaps getrennt von Ressourcen erstellen. Anschließend können Sie mehrere Ressourcen innerhalb eines einzelnen Heaps finden. Sie können dies tun, ohne gekachelte oder reservierte Ressourcen zu erstellen, sodass die Funktionen für alle Ressourcentypen direkt von Ihrer Anwendung erstellt werden können. Mehrere Ressourcen können sich überlappen, und Sie müssen [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) verwenden, um physischen Speicher ordnungsgemäß wieder zu verwenden. Weitere Informationen [**finden Sie unter ID3D12Device::CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource).

## <a name="resource-size-reflection"></a>Reflektion der Ressourcengröße

Sie müssen die Reflektion der Ressourcengröße verwenden, um zu verstehen, wie viel Raumtexturen mit unbekannten Texturlayouts in Heaps erfordern. Puffer werden ebenfalls unterstützt, aber größtenteils zur Vereinfachung.

Sie sollten sich größere Abweichungen bei der Ausrichtung bewusst sein, um ressourcenverdichter zu packen.

Beispielsweise gibt ein Einelementarray mit einem 1-Byte-Puffer eine Größe von 64 KB und eine *Ausrichtung* von 64 KB zurück, da Puffer nur 64 KB ausgerichtet sein können. 

Außerdem meldet ein Array mit drei Elemente mit zwei mit einem einzelnen Texel 64 KB ausgerichteten Texturen und einer mit einem einzelnen Texel ausgerichteten Textur mit 4 MB unterschiedliche Größen basierend auf der Reihenfolge des Arrays. Wenn sich die 4 MB ausgerichteten Texturen in der Mitte befindet, beträgt die resultierende *Größe* 12 MB. Andernfalls beträgt die resultierende Größe 8 MB. Die zurückgegebene Ausrichtung wäre immer 4 MB, die Obermenge aller Ausrichtungen im Ressourcenarray.

Verweisen Sie auf die folgenden APIs.

- [**D3D12- \_ \_ RESSOURCENZUORDNUNGSINFORMATIONEN \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
- [**GetResourceAllocationInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a>Pufferausrichtung

Einschränkungen der Pufferausrichtung haben sich nicht von Direct3D 11 geändert, insbesondere:

- 4 MB für Texturen mit mehreren Stichproben.
- 64 KB für Einzelbeispieltexturen und Puffer.

## <a name="related-topics"></a>Zugehörige Themen

* [Unterzuordnung innerhalb von Puffern](large-buffers.md)
