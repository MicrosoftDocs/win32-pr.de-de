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
# <a name="uploading-different-types-of-resources"></a><span data-ttu-id="37a29-103">Hochladen verschiedener Ressourcentypen</span><span class="sxs-lookup"><span data-stu-id="37a29-103">Uploading different types of resources</span></span>

<span data-ttu-id="37a29-104">Zeigt, wie Sie einen Puffer verwenden, um sowohl konstante Pufferdaten als auch Scheitelpunktpufferdaten in die GPU hochzuladen, und wie Sie Daten ordnungsgemäß unterteilen und in Puffern platzieren.</span><span class="sxs-lookup"><span data-stu-id="37a29-104">Shows how to use one buffer to upload both constant buffer data and vertex buffer data to the GPU, and how to properly sub-allocate and place data within buffers.</span></span> <span data-ttu-id="37a29-105">Die Verwendung eines einzelnen Puffers erhöht die Flexibilität bei der Speicherauslastung und bietet Anwendungen eine strengere Kontrolle über die Speicherauslastung.</span><span class="sxs-lookup"><span data-stu-id="37a29-105">The use of a single buffer increases memory usage flexibility, and provides applications with tighter control over memory usage.</span></span> <span data-ttu-id="37a29-106">Zeigt außerdem die Unterschiede zwischen den Modellen Direct3D 11 und Direct3D 12 zum Hochladen verschiedener Ressourcentypen.</span><span class="sxs-lookup"><span data-stu-id="37a29-106">Also shows the differences between the Direct3D 11 and Direct3D 12 models for uploading different types of resources.</span></span>

## <a name="upload-different-types-of-resources"></a><span data-ttu-id="37a29-107">Hochladen ressourcentypen</span><span class="sxs-lookup"><span data-stu-id="37a29-107">Upload different types of resources</span></span>

<span data-ttu-id="37a29-108">In Direct3D 12 erstellen Sie einen Puffer, der verschiedene Arten von Ressourcendaten zum Hochladen aufnehmen soll, und Sie kopieren Ressourcendaten auf ähnliche Weise für verschiedene Ressourcendaten in den gleichen Puffer.</span><span class="sxs-lookup"><span data-stu-id="37a29-108">In Direct3D 12, you create one buffer to accommodate different types of resource data for uploading, and you copy resource data to the same buffer in a similar way for different resource data.</span></span> <span data-ttu-id="37a29-109">Anschließend werden einzelne Ansichten erstellt, um diese Ressourcendaten an die Grafikpipeline im Direct3D 12-Ressourcenbindungsmodell zu binden.</span><span class="sxs-lookup"><span data-stu-id="37a29-109">Individual views are then created to bind those resource data to the graphics pipeline in the Direct3D 12 resource binding model.</span></span>

<span data-ttu-id="37a29-110">In Direct3D 11 erstellen Sie separate Puffer für verschiedene Arten von Ressourcendaten (beachten Sie die verschiedenen, die unten im Direct3D 11-Beispielcode verwendet werden), binden jeden Ressourcenpuffer explizit an die Grafikpipeline und aktualisieren die Ressourcendaten mit verschiedenen Methoden basierend auf verschiedenen `BindFlags` Ressourcentypen.</span><span class="sxs-lookup"><span data-stu-id="37a29-110">In Direct3D 11, you create separate buffers for different types of resource data (note the different `BindFlags` used in the Direct3D 11 sample code below), explicitly binding each resource buffer to the graphics pipeline, and update the resource data with different methods based on different resource types.</span></span>

<span data-ttu-id="37a29-111">Sowohl in Direct3D 12 als auch in Direct3D 11 sollten Sie Ressourcen nur dann hochladen, wenn die CPU die Daten einmal schreibt, und die GPU liest sie einmal.</span><span class="sxs-lookup"><span data-stu-id="37a29-111">In both Direct3D 12 and Direct3D 11, you should use upload resources only where the CPU will write the data once, and the GPU will read it once.</span></span>

<span data-ttu-id="37a29-112">In einigen Fällen</span><span class="sxs-lookup"><span data-stu-id="37a29-112">In some cases,</span></span>
* <span data-ttu-id="37a29-113">Die GPU liest die Daten mehrmals, oder</span><span class="sxs-lookup"><span data-stu-id="37a29-113">the GPU will read the data multiple times, or</span></span>
* <span data-ttu-id="37a29-114">Die GPU liest die Daten nicht linear, oder</span><span class="sxs-lookup"><span data-stu-id="37a29-114">the GPU won't read the data linearly, or</span></span>
* <span data-ttu-id="37a29-115">das Rendering ist bereits erheblich gpu-eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="37a29-115">the rendering is significantly GPU-limited already.</span></span>

<span data-ttu-id="37a29-116">In diesen Fällen ist es möglicherweise besser, [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) oder [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) zu verwenden, um die Uploadpufferdaten in eine Standardressource zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="37a29-116">In those cases, the better option might be to use [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) or [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) to copy the upload buffer data to a default resource.</span></span>

<span data-ttu-id="37a29-117">Eine Standardressource kann sich auf diskreten GPUs im physischen Videospeicher befinden.</span><span class="sxs-lookup"><span data-stu-id="37a29-117">A default resource can reside in physical video memory on discrete GPUs.</span></span>

### <a name="code-example-direct3d-11"></a><span data-ttu-id="37a29-118">Codebeispiel: Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="37a29-118">Code Example: Direct3D 11</span></span>

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

### <a name="code-example-direct3d-12"></a><span data-ttu-id="37a29-119">Codebeispiel: Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="37a29-119">Code Example: Direct3D 12</span></span>

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

<span data-ttu-id="37a29-120">Beachten Sie die Verwendung der [**Hilfsstrukturen**](cd3dx12-heap-properties.md) CD3DX12_HEAP_PROPERTIES und [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md).</span><span class="sxs-lookup"><span data-stu-id="37a29-120">Note the use of the helper structures [**CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) and [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md).</span></span>

## <a name="constants"></a><span data-ttu-id="37a29-121">Konstanten</span><span class="sxs-lookup"><span data-stu-id="37a29-121">Constants</span></span>

<span data-ttu-id="37a29-122">Verwenden Sie die folgenden APIs, um Konstanten, Scheitelungen und Indizes innerhalb eines Upload- oder Readback-Heaps zu setzen.</span><span class="sxs-lookup"><span data-stu-id="37a29-122">To set constants, vertices, and indexes within an upload or readback heap, use the following APIs.</span></span>

-   [<span data-ttu-id="37a29-123">**ID3D12Device::CreateConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="37a29-123">**ID3D12Device::CreateConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [<span data-ttu-id="37a29-124">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span><span class="sxs-lookup"><span data-stu-id="37a29-124">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [<span data-ttu-id="37a29-125">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="37a29-125">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a><span data-ttu-id="37a29-126">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="37a29-126">Resources</span></span>

<span data-ttu-id="37a29-127">Ressourcen sind das Direct3D-Konzept, das die Nutzung des physischen GPU-Speichers abstrahiert.</span><span class="sxs-lookup"><span data-stu-id="37a29-127">Resources are the Direct3D concept that abstracts the usage of GPU physical memory.</span></span> <span data-ttu-id="37a29-128">Ressourcen benötigen virtuellen GPU-Adressraum für den Zugriff auf physischen Speicher.</span><span class="sxs-lookup"><span data-stu-id="37a29-128">Resources require GPU virtual address space to access physical memory.</span></span> <span data-ttu-id="37a29-129">Die Ressourcenerstellung wird im Freethreading ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37a29-129">Resource creation is free-threaded.</span></span>

<span data-ttu-id="37a29-130">Es gibt drei Arten von Ressourcen in Bezug auf die Erstellung virtueller Adressen und die Flexibilität in Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="37a29-130">There are three types of resources with respect to virtual address creation and flexibility in Direct3D 12.</span></span>

### <a name="committed-resources"></a><span data-ttu-id="37a29-131">Ressourcen, für die ein Committed (Ressourcen</span><span class="sxs-lookup"><span data-stu-id="37a29-131">Committed resources</span></span>

<span data-ttu-id="37a29-132">Die gängigste Idee von Direct3D-Ressourcen über die Generationen hinweg sind ressourcenverankerte Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="37a29-132">Committed resources are the most common idea of Direct3D resources over the generations.</span></span> <span data-ttu-id="37a29-133">Beim Erstellen einer solchen Ressource wird ein virtueller Adressbereich, ein impliziter Heap, der groß genug ist, um die gesamte Ressource zu passen, und der virtuelle Adressbereich in den physischen Speicher, der vom Heap gekapselt wird, zuteilen.</span><span class="sxs-lookup"><span data-stu-id="37a29-133">Creating such a resource allocates virtual address range, an implicit heap large enough to fit the whole resource, and commits the virtual address range to the physical memory encapsulated by the heap.</span></span> <span data-ttu-id="37a29-134">Die impliziten Heapeigenschaften müssen übergeben werden, damit sie mit der funktionalen Parität mit früheren Direct3D-Versionen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="37a29-134">The implicit heap properties must be passed to match functional parity with previous Direct3D versions.</span></span> <span data-ttu-id="37a29-135">Weitere Informationen [**finden Sie unter ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span><span class="sxs-lookup"><span data-stu-id="37a29-135">Refer to [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span></span>

### <a name="reserved-resources"></a><span data-ttu-id="37a29-136">Reservierte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="37a29-136">Reserved resources</span></span>

<span data-ttu-id="37a29-137">Reservierte Ressourcen entsprechen gekachelten Direct3D 11-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="37a29-137">Reserved resources are equivalent to Direct3D 11 tiled resources.</span></span> <span data-ttu-id="37a29-138">Bei der Erstellung wird nur ein virtueller Adressbereich zugeordnet und keinen Heap zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="37a29-138">On their creation, only a virtual address range is allocated, and not mapped to any heap.</span></span> <span data-ttu-id="37a29-139">Die Anwendung wird diese Ressourcen später Heaps zuordnen.</span><span class="sxs-lookup"><span data-stu-id="37a29-139">The application will map such resources to heaps later.</span></span> <span data-ttu-id="37a29-140">Die Funktionen solcher Ressourcen sind derzeit unverändert gegenüber Direct3D 11, da sie einem Heap mit einer Kachelgranularität von 64 KB mit [**UpdateTileMappings zugeordnet werden können.**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)</span><span class="sxs-lookup"><span data-stu-id="37a29-140">The capabilities of such resources are currently unchanged from Direct3D 11, as they can be mapped to a heap at a 64KB tile granularity with [**UpdateTileMappings**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings).</span></span> <span data-ttu-id="37a29-141">Weitere Informationen [**finden Sie unter ID3D12Device::CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).</span><span class="sxs-lookup"><span data-stu-id="37a29-141">Refer to [**ID3D12Device::CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).</span></span>

### <a name="placed-resources"></a><span data-ttu-id="37a29-142">Platzierte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="37a29-142">Placed resources</span></span>

<span data-ttu-id="37a29-143">Neu für Direct3D 12: Sie können Heaps getrennt von Ressourcen erstellen.</span><span class="sxs-lookup"><span data-stu-id="37a29-143">New for Direct3D 12, you can create heaps separate from resources.</span></span> <span data-ttu-id="37a29-144">Anschließend können Sie mehrere Ressourcen innerhalb eines einzelnen Heaps finden.</span><span class="sxs-lookup"><span data-stu-id="37a29-144">Afterward, you can locate multiple resources within a single heap.</span></span> <span data-ttu-id="37a29-145">Sie können dies tun, ohne gekachelte oder reservierte Ressourcen zu erstellen, sodass die Funktionen für alle Ressourcentypen direkt von Ihrer Anwendung erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="37a29-145">You can do that without creating tiled or reserved resources, enabling the capabilities for all resource types able to be created directly by your application.</span></span> <span data-ttu-id="37a29-146">Mehrere Ressourcen können sich überlappen, und Sie müssen [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) verwenden, um physischen Speicher ordnungsgemäß wieder zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="37a29-146">Multiple resources might overlap, and you must use the [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) to re-use physical memory correctly.</span></span> <span data-ttu-id="37a29-147">Weitere Informationen [**finden Sie unter ID3D12Device::CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource).</span><span class="sxs-lookup"><span data-stu-id="37a29-147">Refer to [**ID3D12Device::CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource).</span></span>

## <a name="resource-size-reflection"></a><span data-ttu-id="37a29-148">Reflektion der Ressourcengröße</span><span class="sxs-lookup"><span data-stu-id="37a29-148">Resource size reflection</span></span>

<span data-ttu-id="37a29-149">Sie müssen die Reflektion der Ressourcengröße verwenden, um zu verstehen, wie viel Raumtexturen mit unbekannten Texturlayouts in Heaps erfordern.</span><span class="sxs-lookup"><span data-stu-id="37a29-149">You must use resource size reflection to understand how much space textures with unknown texture layouts require in heaps.</span></span> <span data-ttu-id="37a29-150">Puffer werden ebenfalls unterstützt, aber größtenteils zur Vereinfachung.</span><span class="sxs-lookup"><span data-stu-id="37a29-150">Buffers are also supported, but mostly as a convenience.</span></span>

<span data-ttu-id="37a29-151">Sie sollten sich größere Abweichungen bei der Ausrichtung bewusst sein, um ressourcenverdichter zu packen.</span><span class="sxs-lookup"><span data-stu-id="37a29-151">You should be aware of major alignment discrepancies, to help pack resources more densely.</span></span>

<span data-ttu-id="37a29-152">Beispielsweise gibt ein Einelementarray mit einem 1-Byte-Puffer eine Größe von 64 KB und eine *Ausrichtung* von 64 KB zurück, da Puffer nur 64 KB ausgerichtet sein können. </span><span class="sxs-lookup"><span data-stu-id="37a29-152">For example, a single-element array with a one-byte-buffer returns a *Size* of 64KB, and an *Alignment* of 64KB, because buffers can be only 64KB-aligned.</span></span>

<span data-ttu-id="37a29-153">Außerdem meldet ein Array mit drei Elemente mit zwei mit einem einzelnen Texel 64 KB ausgerichteten Texturen und einer mit einem einzelnen Texel ausgerichteten Textur mit 4 MB unterschiedliche Größen basierend auf der Reihenfolge des Arrays.</span><span class="sxs-lookup"><span data-stu-id="37a29-153">Also, a three element array with two single-texel 64KB aligned textures and a single-texel 4MB aligned texture reports differing sizes based on the order of the array.</span></span> <span data-ttu-id="37a29-154">Wenn sich die 4 MB ausgerichteten Texturen in der Mitte befindet, beträgt die resultierende *Größe* 12 MB.</span><span class="sxs-lookup"><span data-stu-id="37a29-154">If the 4MB aligned textures is in the middle, then the resulting *Size* is 12MB.</span></span> <span data-ttu-id="37a29-155">Andernfalls beträgt die resultierende Größe 8 MB.</span><span class="sxs-lookup"><span data-stu-id="37a29-155">Otherwise, the resulting Size is 8MB.</span></span> <span data-ttu-id="37a29-156">Die zurückgegebene Ausrichtung wäre immer 4 MB, die Obermenge aller Ausrichtungen im Ressourcenarray.</span><span class="sxs-lookup"><span data-stu-id="37a29-156">The Alignment returned would always be 4MB, the superset of all alignments in the resource array.</span></span>

<span data-ttu-id="37a29-157">Verweisen Sie auf die folgenden APIs.</span><span class="sxs-lookup"><span data-stu-id="37a29-157">Reference the following APIs.</span></span>

- [<span data-ttu-id="37a29-158">**D3D12- \_ \_ RESSOURCENZUORDNUNGSINFORMATIONEN \_**</span><span class="sxs-lookup"><span data-stu-id="37a29-158">**D3D12\_RESOURCE\_ALLOCATION\_INFO**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
- [<span data-ttu-id="37a29-159">**GetResourceAllocationInfo**</span><span class="sxs-lookup"><span data-stu-id="37a29-159">**GetResourceAllocationInfo**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a><span data-ttu-id="37a29-160">Pufferausrichtung</span><span class="sxs-lookup"><span data-stu-id="37a29-160">Buffer alignment</span></span>

<span data-ttu-id="37a29-161">Einschränkungen der Pufferausrichtung haben sich nicht von Direct3D 11 geändert, insbesondere:</span><span class="sxs-lookup"><span data-stu-id="37a29-161">Buffer alignment restrictions have not changed from Direct3D 11, notably:</span></span>

- <span data-ttu-id="37a29-162">4 MB für Texturen mit mehreren Stichproben.</span><span class="sxs-lookup"><span data-stu-id="37a29-162">4 MB for multi-sample textures.</span></span>
- <span data-ttu-id="37a29-163">64 KB für Einzelbeispieltexturen und Puffer.</span><span class="sxs-lookup"><span data-stu-id="37a29-163">64 KB for single-sample textures and buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37a29-164">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="37a29-164">Related topics</span></span>

* [<span data-ttu-id="37a29-165">Unterzuordnung innerhalb von Puffern</span><span class="sxs-lookup"><span data-stu-id="37a29-165">Suballocation within buffers</span></span>](large-buffers.md)
