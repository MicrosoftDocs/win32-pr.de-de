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
# <a name="uploading-different-types-of-resources"></a><span data-ttu-id="b75e7-103">Hochladen verschiedener Arten von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b75e7-103">Uploading Different Types of Resources</span></span>

<span data-ttu-id="b75e7-104">Zeigt, wie ein Puffer verwendet wird, um sowohl Konstante Puffer Daten als auch Vertex-Puffer Daten in die GPU hochzuladen und Daten in Puffern ordnungsgemäß zuzuordnen und zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="b75e7-104">Shows how to use one buffer to upload both constant buffer data and vertex buffer data to the GPU, and how to properly sub-allocate and place data within buffers.</span></span> <span data-ttu-id="b75e7-105">Die Verwendung eines einzelnen Puffers steigert die Flexibilität der Speicherauslastung und bietet Anwendungen eine strengere Kontrolle der Speicherauslastung.</span><span class="sxs-lookup"><span data-stu-id="b75e7-105">The use of one single buffer increases memory usage flexibility and provides applications with tighter control of memory usage.</span></span> <span data-ttu-id="b75e7-106">Zeigt außerdem die Unterschiede zwischen den D3D11-und D3D12-Modellen zum Hochladen unterschiedlicher Ressourcentypen.</span><span class="sxs-lookup"><span data-stu-id="b75e7-106">Also shows the differences between the D3D11 and D3D12 models for uploading different types of resources.</span></span>

-   [<span data-ttu-id="b75e7-107">Hochladen verschiedener Arten von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b75e7-107">Upload Different Types of Resources</span></span>](#upload-different-types-of-resources)
    -   [<span data-ttu-id="b75e7-108">Code Beispiel: D3D11</span><span class="sxs-lookup"><span data-stu-id="b75e7-108">Code Example: D3D11</span></span>](#code-example-d3d11)
    -   [<span data-ttu-id="b75e7-109">Code Beispiel: D3D12</span><span class="sxs-lookup"><span data-stu-id="b75e7-109">Code Example: D3D12</span></span>](#code-example-d3d12)
-   [<span data-ttu-id="b75e7-110">Konstanten</span><span class="sxs-lookup"><span data-stu-id="b75e7-110">Constants</span></span>](#constants)
-   [<span data-ttu-id="b75e7-111">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b75e7-111">Resources</span></span>](#uploading-different-types-of-resources)
-   [<span data-ttu-id="b75e7-112">Ressourcen Größen Reflektion</span><span class="sxs-lookup"><span data-stu-id="b75e7-112">Resource size reflection</span></span>](#resource-size-reflection)
-   [<span data-ttu-id="b75e7-113">Puffer Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="b75e7-113">Buffer alignment</span></span>](#buffer-alignment)
-   [<span data-ttu-id="b75e7-114">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b75e7-114">Related topics</span></span>](#related-topics)

## <a name="upload-different-types-of-resources"></a><span data-ttu-id="b75e7-115">Hochladen verschiedener Arten von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b75e7-115">Upload Different Types of Resources</span></span>

<span data-ttu-id="b75e7-116">In D3D12 erstellen Anwendungen einen Puffer, um unterschiedliche Arten von Ressourcen Daten zum Hochladen zu unterstützen und Ressourcen Daten auf ähnliche Weise für verschiedene Ressourcen Daten in denselben Puffer zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="b75e7-116">In D3D12, applications create one buffer to accommodate different types of resource data for uploading, and copy resource data to the same buffer in a similar way for different resource data.</span></span> <span data-ttu-id="b75e7-117">Anschließend werden einzelne Ansichten erstellt, um diese Ressourcen Daten an die Grafik Pipeline im neuen Ressourcen Bindungs Modell zu binden.</span><span class="sxs-lookup"><span data-stu-id="b75e7-117">Individual views are then created to bind those resource data to the graphics pipeline in the new resource binding model.</span></span>

<span data-ttu-id="b75e7-118">In D3D11 erstellen Anwendungen separate Puffer für verschiedene Typen von Ressourcen Daten (Beachten Sie die anderen `BindFlags` , die im folgenden Beispielcode für D3D11 verwendet werden), binden jeden Ressourcen Puffer explizit an die Grafik Pipeline und aktualisieren die Ressourcen Daten mit unterschiedlichen Methoden auf der Grundlage unterschiedlicher Ressourcentypen.</span><span class="sxs-lookup"><span data-stu-id="b75e7-118">In D3D11, applications create separate buffers for different types of resource data (note the different `BindFlags` used in the D3D11 sample code below), explicitly binding each resource buffer to the graphics pipeline, and update the resource data with different methods based on different resource types.</span></span>

<span data-ttu-id="b75e7-119">In D3D12 und D3D11 sollten Anwendungen nur uploadressourcen verwenden, bei denen die CPU die Daten einmal schreibt und die GPU Sie einmal liest.</span><span class="sxs-lookup"><span data-stu-id="b75e7-119">In both D3D12 and D3D11, applications should only use upload resources where the CPU will write the data once and the GPU will read it once.</span></span> <span data-ttu-id="b75e7-120">Wenn die GPU die Daten mehrmals liest, liest die GPU die Daten nicht linear, oder das Rendering ist bereits stark GPU-begrenzt.</span><span class="sxs-lookup"><span data-stu-id="b75e7-120">If the GPU will read the data multiple times, the GPU will not read the data linearly, or the rendering is significantly GPU-limited already.</span></span> <span data-ttu-id="b75e7-121">Die bessere Option ist möglicherweise die Verwendung von [**ID3D12GraphicsCommandList:: copytextureregion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) oder [**ID3D12GraphicsCommandList:: copybufferregion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) zum Kopieren der Upload-Puffer Daten in eine Standardressource.</span><span class="sxs-lookup"><span data-stu-id="b75e7-121">The better option may be to use [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) or [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) to copy the upload buffer data to a default resource.</span></span> <span data-ttu-id="b75e7-122">Eine Standardressource kann sich im physischen Videospeicher auf diskreten GPUs befinden.</span><span class="sxs-lookup"><span data-stu-id="b75e7-122">A default resource can reside in physical video memory on discrete GPUs.</span></span>

### <a name="code-example-d3d11"></a><span data-ttu-id="b75e7-123">Code Beispiel: D3D11</span><span class="sxs-lookup"><span data-stu-id="b75e7-123">Code Example: D3D11</span></span>

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

### <a name="code-example-d3d12"></a><span data-ttu-id="b75e7-124">Code Beispiel: D3D12</span><span class="sxs-lookup"><span data-stu-id="b75e7-124">Code Example: D3D12</span></span>

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

<span data-ttu-id="b75e7-125">Beachten Sie die Verwendung der Hilfsstrukturen [**CD3DX12 \_ Heap \_ Eigenschaften**](cd3dx12-heap-properties.md) und [**CD3DX12 \_ Resource \_ DESC**](cd3dx12-resource-desc.md).</span><span class="sxs-lookup"><span data-stu-id="b75e7-125">Note the use of the helper structures [**CD3DX12\_HEAP\_PROPERTIES**](cd3dx12-heap-properties.md) and [**CD3DX12\_RESOURCE\_DESC**](cd3dx12-resource-desc.md).</span></span>

## <a name="constants"></a><span data-ttu-id="b75e7-126">Konstanten</span><span class="sxs-lookup"><span data-stu-id="b75e7-126">Constants</span></span>

<span data-ttu-id="b75e7-127">Verwenden Sie die folgenden APIs, um Konstanten, Vertices und Indizes in einem Upload-oder Read-Back-Heap festzulegen:</span><span class="sxs-lookup"><span data-stu-id="b75e7-127">To set constants, vertices and indexes within an Upload or Readback heap, use the following APIs:</span></span>

-   [<span data-ttu-id="b75e7-128">**ID3D12Device:: kreateconstantbufferview**</span><span class="sxs-lookup"><span data-stu-id="b75e7-128">**ID3D12Device::CreateConstantBufferView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [<span data-ttu-id="b75e7-129">**ID3D12GraphicsCommandList:: iasetvertexbuffers**</span><span class="sxs-lookup"><span data-stu-id="b75e7-129">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [<span data-ttu-id="b75e7-130">**ID3D12GraphicsCommandList:: iasetindexbuffer**</span><span class="sxs-lookup"><span data-stu-id="b75e7-130">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a><span data-ttu-id="b75e7-131">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b75e7-131">Resources</span></span>

<span data-ttu-id="b75e7-132">Ressourcen sind das D3D-Konzept, das die Verwendung des physischen GPU-Speichers abstrahiert.</span><span class="sxs-lookup"><span data-stu-id="b75e7-132">Resources are the D3D concept which abstracts the usage of GPU physical memory.</span></span> <span data-ttu-id="b75e7-133">Ressourcen erfordern einen virtuellen GPU-Adressraum für den Zugriff auf den physischen Speicher.</span><span class="sxs-lookup"><span data-stu-id="b75e7-133">Resources require GPU virtual address space to access physical memory.</span></span> <span data-ttu-id="b75e7-134">Die Ressourcen Erstellung ist kostenlos.</span><span class="sxs-lookup"><span data-stu-id="b75e7-134">Resource creation is free-threaded.</span></span>

<span data-ttu-id="b75e7-135">Es gibt drei Arten von Ressourcen in Bezug auf die Erstellung und Flexibilität von virtuellen Adressen in D3D12:</span><span class="sxs-lookup"><span data-stu-id="b75e7-135">There are three types of resources with respect to virtual address creation and flexibility in D3D12:</span></span>

-   <span data-ttu-id="b75e7-136">Zugesicherte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b75e7-136">Committed resources</span></span>

    <span data-ttu-id="b75e7-137">Zugesicherte Ressourcen sind die häufigste Idee der D3D-Ressourcen in den Generationen.</span><span class="sxs-lookup"><span data-stu-id="b75e7-137">Committed resources are the most common idea of D3D resources over the generations.</span></span> <span data-ttu-id="b75e7-138">Durch das Erstellen einer solchen Ressource wird der virtuelle Adressbereich zugeordnet, ein impliziter Heap, der groß genug für die gesamte Ressource ist, und führt einen Commit für den virtuellen Adressbereich an den vom Heap gekapselten physischen Speicher aus</span><span class="sxs-lookup"><span data-stu-id="b75e7-138">Creating such a resource allocates virtual address range, an implicit heap large enough to fit the whole resource, and commits the virtual address range to the physical memory encapsulated by the heap.</span></span> <span data-ttu-id="b75e7-139">Die impliziten Heap Eigenschaften müssen an die funktionale Parität mit früheren D3D-Versionen angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="b75e7-139">The implicit heap properties must be passed to match functional parity with previous D3D versions.</span></span> <span data-ttu-id="b75e7-140">Weitere Informationen finden Sie unter [**ID3D12Device:: kreatecommittedresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span><span class="sxs-lookup"><span data-stu-id="b75e7-140">Refer to [**ID3D12Device::CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span></span>

-   <span data-ttu-id="b75e7-141">Reservierte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b75e7-141">Reserved resources</span></span>

    <span data-ttu-id="b75e7-142">Reservierte Ressourcen sind äquivalent zu D3D11-gekachelten Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b75e7-142">Reserved resources are equivalent to D3D11 tiled resources.</span></span> <span data-ttu-id="b75e7-143">Bei der Erstellung wird nur ein virtueller Adressbereich zugeordnet und keinem Heap zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b75e7-143">On their creation, only a virtual address range is allocated and not mapped to any heap.</span></span> <span data-ttu-id="b75e7-144">Diese Ressourcen werden den Heaps später von der Anwendung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b75e7-144">The application will map such resources to heaps later.</span></span> <span data-ttu-id="b75e7-145">Die Funktionen solcher Ressourcen sind momentan gegenüber D3D11 unverändert, da Sie einem Heap mit einer Kachel Granularität von 64 KB mit [**updatetilemappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="b75e7-145">The capabilities of such resources are currently unchanged over D3D11, as they can be mapped to a heap at a 64KB tile granularity with [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings).</span></span> <span data-ttu-id="b75e7-146">Weitere Informationen finden Sie unter [ **ID3D12Device:: up-eservedresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)</span><span class="sxs-lookup"><span data-stu-id="b75e7-146">Refer to [**ID3D12Device::CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)</span></span>

-   <span data-ttu-id="b75e7-147">Platzierte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b75e7-147">Placed resources</span></span>

    <span data-ttu-id="b75e7-148">Neu für D3D12: Anwendungen können Heaps unabhängig von Ressourcen erstellen.</span><span class="sxs-lookup"><span data-stu-id="b75e7-148">New for D3D12, applications may create heaps separate from resources.</span></span> <span data-ttu-id="b75e7-149">Anschließend kann die Anwendung mehrere Ressourcen innerhalb eines einzelnen Heaps suchen.</span><span class="sxs-lookup"><span data-stu-id="b75e7-149">Afterward, the application may locate multiple resources within a single heap.</span></span> <span data-ttu-id="b75e7-150">Dies kann ohne das Erstellen von gekachelten oder reservierten Ressourcen erfolgen, sodass die Funktionen für alle Ressourcentypen direkt von Anwendungen erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="b75e7-150">This can be done without creating tiled or reserved resources, enabling the capabilities for all resource types able to be created directly by applications.</span></span> <span data-ttu-id="b75e7-151">Mehrere Ressourcen können sich überlappen, und die Anwendung muss verwenden, `TiledResourceBarrier` um den physischen Speicher ordnungsgemäß wieder zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b75e7-151">Multiple resources may overlap, and the application must use the `TiledResourceBarrier` to re-use physical memory correctly.</span></span> <span data-ttu-id="b75e7-152">Weitere Informationen finden Sie unter [ **ID3D12Device:: kreateplacedresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource)</span><span class="sxs-lookup"><span data-stu-id="b75e7-152">Refer to [**ID3D12Device::CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource)</span></span>

## <a name="resource-size-reflection"></a><span data-ttu-id="b75e7-153">Ressourcen Größen Reflektion</span><span class="sxs-lookup"><span data-stu-id="b75e7-153">Resource size reflection</span></span>

<span data-ttu-id="b75e7-154">Anwendungen müssen die Reflektion der Ressourcen Größe verwenden, um zu verstehen, wie viel Raum Texturen mit unbekannten Textur Layouts in Heaps erfordern.</span><span class="sxs-lookup"><span data-stu-id="b75e7-154">Applications must use resource size reflection to understand how much room textures with unknown texture layouts require in heaps.</span></span> <span data-ttu-id="b75e7-155">Puffer werden auch unterstützt, aber meistens als praktische Hilfe.</span><span class="sxs-lookup"><span data-stu-id="b75e7-155">Buffers are also supported, but mostly as a convenience.</span></span>

<span data-ttu-id="b75e7-156">Anwendungen sollten sich von größeren Ausrichtungs Abweichungen bewusst sein, um Ressourcen stärker zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b75e7-156">Applications should be aware of major alignment discrepancies, to help pack resources more densely.</span></span>

<span data-ttu-id="b75e7-157">Beispielsweise gibt ein Array mit einem einzelnen Element mit einem 1-Byte-Puffer eine Größe von 64 KB und eine Ausrichtung von 64 KB zurück, da Puffer derzeit nur 64 KB ausrichten können.</span><span class="sxs-lookup"><span data-stu-id="b75e7-157">For example, a single-element array with a one-byte-buffer returns a Size of 64KB and an Alignment of 64KB, as buffers currently can only be 64KB aligned.</span></span>

<span data-ttu-id="b75e7-158">Außerdem wird ein Array mit drei Elementen mit zwei ausgerichteten Texturen mit einer Größe von 64 KB und eine texturale 4-MB-Struktur, die auf der Reihenfolge des Arrays basiert, unterschiedliche Größen melden.</span><span class="sxs-lookup"><span data-stu-id="b75e7-158">Also, a three element array with two single-texel 64KB aligned textures and a single-texel 4MB aligned texture reports differing sizes based on the order of the array.</span></span> <span data-ttu-id="b75e7-159">Wenn sich die 4 MB ausgerichteten Texturen in der Mitte befinden, liegt die resultierende Größe bei 12 MB.</span><span class="sxs-lookup"><span data-stu-id="b75e7-159">If the 4MB aligned textures is in the middle, the resulting Size is 12MB.</span></span> <span data-ttu-id="b75e7-160">Andernfalls beträgt die resultierende Größe 8 MB.</span><span class="sxs-lookup"><span data-stu-id="b75e7-160">Otherwise, the resulting Size is 8MB.</span></span> <span data-ttu-id="b75e7-161">Die zurückgegebene Ausrichtung beträgt immer 4 MB, die Obermenge aller Ausrichtungen im Ressourcen Array.</span><span class="sxs-lookup"><span data-stu-id="b75e7-161">The Alignment returned would always be 4MB, the super-set of all alignments in the resource array.</span></span>

<span data-ttu-id="b75e7-162">Verweisen Sie auf die folgenden APIs:</span><span class="sxs-lookup"><span data-stu-id="b75e7-162">Reference the following APIs:</span></span>

-   [<span data-ttu-id="b75e7-163">**D3D12 \_ Ressourcen \_ Zuordnungs \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="b75e7-163">**D3D12\_RESOURCE\_ALLOCATION\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
-   [<span data-ttu-id="b75e7-164">**Getresourcezucationinfo**</span><span class="sxs-lookup"><span data-stu-id="b75e7-164">**GetResourceAllocationInfo**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a><span data-ttu-id="b75e7-165">Puffer Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="b75e7-165">Buffer alignment</span></span>

<span data-ttu-id="b75e7-166">Einschränkungen der Puffer Ausrichtung wurden von D3D11 nicht geändert, insbesondere:</span><span class="sxs-lookup"><span data-stu-id="b75e7-166">Buffer alignment restrictions have not changed from D3D11, notably:</span></span>

-   <span data-ttu-id="b75e7-167">4 MB für Multisample-Texturen.</span><span class="sxs-lookup"><span data-stu-id="b75e7-167">4 MB for multi-sample textures.</span></span>
-   <span data-ttu-id="b75e7-168">64 KB für Single-Sample-Texturen und-Puffer.</span><span class="sxs-lookup"><span data-stu-id="b75e7-168">64 KB for single-sample textures and buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b75e7-169">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b75e7-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b75e7-170">Untergeordnete Zuordnung innerhalb von Puffern</span><span class="sxs-lookup"><span data-stu-id="b75e7-170">Suballocation Within Buffers</span></span>](large-buffers.md)
</dt> </dl>

 

 




