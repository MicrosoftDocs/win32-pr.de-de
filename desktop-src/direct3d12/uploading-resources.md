---
title: Hochladen verschiedener Arten von Ressourcen
description: Zeigt, wie ein Puffer verwendet wird, um sowohl Konstante Puffer Daten als auch Vertex-Puffer Daten in die GPU hochzuladen und Daten in Puffern ordnungsgemäß zuzuordnen und zu platzieren.
ms.assetid: 255B0482-21D6-4276-8009-3F3891879CA1
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd2edca2cd9f4d3becf5036056a89f91c50f2c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104720"
---
# <a name="uploading-different-types-of-resources"></a>Hochladen verschiedener Arten von Ressourcen

Zeigt, wie ein Puffer verwendet wird, um sowohl Konstante Puffer Daten als auch Vertex-Puffer Daten in die GPU hochzuladen und Daten in Puffern ordnungsgemäß zuzuordnen und zu platzieren. Die Verwendung eines einzelnen Puffers steigert die Flexibilität der Speicherauslastung und bietet Anwendungen eine strengere Kontrolle der Speicherauslastung. Zeigt außerdem die Unterschiede zwischen den D3D11-und D3D12-Modellen zum Hochladen unterschiedlicher Ressourcentypen.

-   [Hochladen verschiedener Arten von Ressourcen](#upload-different-types-of-resources)
    -   [Code Beispiel: D3D11](#code-example-d3d11)
    -   [Code Beispiel: D3D12](#code-example-d3d12)
-   [Konstanten](#constants)
-   [Ressourcen](#uploading-different-types-of-resources)
-   [Ressourcen Größen Reflektion](#resource-size-reflection)
-   [Puffer Ausrichtung](#buffer-alignment)
-   [Verwandte Themen](#related-topics)

## <a name="upload-different-types-of-resources"></a>Hochladen verschiedener Arten von Ressourcen

In D3D12 erstellen Anwendungen einen Puffer, um unterschiedliche Arten von Ressourcen Daten zum Hochladen zu unterstützen und Ressourcen Daten auf ähnliche Weise für verschiedene Ressourcen Daten in denselben Puffer zu kopieren. Anschließend werden einzelne Ansichten erstellt, um diese Ressourcen Daten an die Grafik Pipeline im neuen Ressourcen Bindungs Modell zu binden.

In D3D11 erstellen Anwendungen separate Puffer für verschiedene Typen von Ressourcen Daten (Beachten Sie die anderen `BindFlags` , die im folgenden Beispielcode für D3D11 verwendet werden), binden jeden Ressourcen Puffer explizit an die Grafik Pipeline und aktualisieren die Ressourcen Daten mit unterschiedlichen Methoden auf der Grundlage unterschiedlicher Ressourcentypen.

In D3D12 und D3D11 sollten Anwendungen nur uploadressourcen verwenden, bei denen die CPU die Daten einmal schreibt und die GPU Sie einmal liest. Wenn die GPU die Daten mehrmals liest, liest die GPU die Daten nicht linear, oder das Rendering ist bereits stark GPU-begrenzt. Die bessere Option ist möglicherweise die Verwendung von [**ID3D12GraphicsCommandList:: copytextureregion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) oder [**ID3D12GraphicsCommandList:: copybufferregion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) zum Kopieren der Upload-Puffer Daten in eine Standardressource. Eine Standardressource kann sich im physischen Videospeicher auf diskreten GPUs befinden.

### <a name="code-example-d3d11"></a>Code Beispiel: D3D11

``` syntax
// D3D11: Separate buffers for each resource type.

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

### <a name="code-example-d3d12"></a>Code Beispiel: D3D12

``` syntax
// D3D12: One buffer to accommodate different types of resources

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

Beachten Sie die Verwendung der Hilfsstrukturen [**CD3DX12 \_ Heap \_ Eigenschaften**](cd3dx12-heap-properties.md) und [**CD3DX12 \_ Resource \_ DESC**](cd3dx12-resource-desc.md).

## <a name="constants"></a>Konstanten

Verwenden Sie die folgenden APIs, um Konstanten, Vertices und Indizes in einem Upload-oder Read-Back-Heap festzulegen:

-   [**ID3D12Device:: kreateconstantbufferview**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [**ID3D12GraphicsCommandList:: iasetvertexbuffers**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [**ID3D12GraphicsCommandList:: iasetindexbuffer**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a>Ressourcen

Ressourcen sind das D3D-Konzept, das die Verwendung des physischen GPU-Speichers abstrahiert. Ressourcen erfordern einen virtuellen GPU-Adressraum für den Zugriff auf den physischen Speicher. Die Ressourcen Erstellung ist kostenlos.

Es gibt drei Arten von Ressourcen in Bezug auf die Erstellung und Flexibilität von virtuellen Adressen in D3D12:

-   Zugesicherte Ressourcen

    Zugesicherte Ressourcen sind die häufigste Idee der D3D-Ressourcen in den Generationen. Durch das Erstellen einer solchen Ressource wird der virtuelle Adressbereich zugeordnet, ein impliziter Heap, der groß genug für die gesamte Ressource ist, und führt einen Commit für den virtuellen Adressbereich an den vom Heap gekapselten physischen Speicher aus Die impliziten Heap Eigenschaften müssen an die funktionale Parität mit früheren D3D-Versionen angepasst werden. Weitere Informationen finden Sie unter [**ID3D12Device:: kreatecommittedresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).

-   Reservierte Ressourcen

    Reservierte Ressourcen sind äquivalent zu D3D11-gekachelten Ressourcen. Bei der Erstellung wird nur ein virtueller Adressbereich zugeordnet und keinem Heap zugeordnet. Diese Ressourcen werden den Heaps später von der Anwendung zugeordnet. Die Funktionen solcher Ressourcen sind momentan gegenüber D3D11 unverändert, da Sie einem Heap mit einer Kachel Granularität von 64 KB mit [**updatetilemappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)zugeordnet werden können. Weitere Informationen finden Sie unter [ **ID3D12Device:: up-eservedresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)

-   Platzierte Ressourcen

    Neu für D3D12: Anwendungen können Heaps unabhängig von Ressourcen erstellen. Anschließend kann die Anwendung mehrere Ressourcen innerhalb eines einzelnen Heaps suchen. Dies kann ohne das Erstellen von gekachelten oder reservierten Ressourcen erfolgen, sodass die Funktionen für alle Ressourcentypen direkt von Anwendungen erstellt werden können. Mehrere Ressourcen können sich überlappen, und die Anwendung muss verwenden, `TiledResourceBarrier` um den physischen Speicher ordnungsgemäß wieder zu verwenden. Weitere Informationen finden Sie unter [ **ID3D12Device:: kreateplacedresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource)

## <a name="resource-size-reflection"></a>Ressourcen Größen Reflektion

Anwendungen müssen die Reflektion der Ressourcen Größe verwenden, um zu verstehen, wie viel Raum Texturen mit unbekannten Textur Layouts in Heaps erfordern. Puffer werden auch unterstützt, aber meistens als praktische Hilfe.

Anwendungen sollten sich von größeren Ausrichtungs Abweichungen bewusst sein, um Ressourcen stärker zu unterstützen.

Beispielsweise gibt ein Array mit einem einzelnen Element mit einem 1-Byte-Puffer eine Größe von 64 KB und eine Ausrichtung von 64 KB zurück, da Puffer derzeit nur 64 KB ausrichten können.

Außerdem wird ein Array mit drei Elementen mit zwei ausgerichteten Texturen mit einer Größe von 64 KB und eine texturale 4-MB-Struktur, die auf der Reihenfolge des Arrays basiert, unterschiedliche Größen melden. Wenn sich die 4 MB ausgerichteten Texturen in der Mitte befinden, liegt die resultierende Größe bei 12 MB. Andernfalls beträgt die resultierende Größe 8 MB. Die zurückgegebene Ausrichtung beträgt immer 4 MB, die Obermenge aller Ausrichtungen im Ressourcen Array.

Verweisen Sie auf die folgenden APIs:

-   [**D3D12 \_ Ressourcen \_ Zuordnungs \_ Informationen**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
-   [**Getresourcezucationinfo**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a>Puffer Ausrichtung

Einschränkungen der Puffer Ausrichtung wurden von D3D11 nicht geändert, insbesondere:

-   4 MB für Multisample-Texturen.
-   64 KB für Single-Sample-Texturen und-Puffer.

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Untergeordnete Zuordnung innerhalb von Puffern](large-buffers.md)
</dt> </dl>

 

 




