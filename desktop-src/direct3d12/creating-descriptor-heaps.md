---
title: Erstellen von deskriptorheaps
description: Zum Erstellen und Konfigurieren eines deskriptorheaps müssen Sie einen deskriptorheap auswählen, die Anzahl der enthaltenen Deskriptoren bestimmen und Flags festlegen, die angeben, ob CPU-sichtbar und/oder Shader sichtbar sind.
ms.assetid: 58677023-692C-4BA4-90B7-D568F3DD3F73
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e472a0749634d5cbaa9cbf1cde5e11202d4c4f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548657"
---
# <a name="creating-descriptor-heaps"></a><span data-ttu-id="9a77a-103">Erstellen von deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="9a77a-103">Creating Descriptor Heaps</span></span>

<span data-ttu-id="9a77a-104">Zum Erstellen und Konfigurieren eines deskriptorheaps müssen Sie einen deskriptorheap auswählen, die Anzahl der enthaltenen Deskriptoren bestimmen und Flags festlegen, die angeben, ob CPU-sichtbar und/oder Shader sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="9a77a-104">To create and configure a descriptor heap, you must select a descriptor heap type, determine how many descriptors it contains, and set flags that indicate whether it is CPU visible and/or shader visible.</span></span>

-   [<span data-ttu-id="9a77a-105">Deskriptorheap-Typen</span><span class="sxs-lookup"><span data-stu-id="9a77a-105">Descriptor Heap types</span></span>](#descriptor-heap-types)
-   [<span data-ttu-id="9a77a-106">Deskriptorheap-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9a77a-106">Descriptor Heap Properties</span></span>](#descriptor-heap-properties)
-   [<span data-ttu-id="9a77a-107">Deskriptorhandles</span><span class="sxs-lookup"><span data-stu-id="9a77a-107">Descriptor Handles</span></span>](#descriptor-handles)
-   [<span data-ttu-id="9a77a-108">Deskriptorheap-Methoden</span><span class="sxs-lookup"><span data-stu-id="9a77a-108">Descriptor Heap Methods</span></span>](#descriptor-heap-methods)
-   [<span data-ttu-id="9a77a-109">Wrapper für minimalen deskriptorheap</span><span class="sxs-lookup"><span data-stu-id="9a77a-109">Minimal descriptor heap wrapper</span></span>](#minimal-descriptor-heap-wrapper)
-   [<span data-ttu-id="9a77a-110">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9a77a-110">Related topics</span></span>](#related-topics)

## <a name="descriptor-heap-types"></a><span data-ttu-id="9a77a-111">Deskriptorheap-Typen</span><span class="sxs-lookup"><span data-stu-id="9a77a-111">Descriptor Heap types</span></span>

<span data-ttu-id="9a77a-112">Der Typ des Heaps wird von einem Member der [**D3D12 \_ Descriptor \_ Heap \_ Type**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) -Enumeration bestimmt:</span><span class="sxs-lookup"><span data-stu-id="9a77a-112">The type of heap is determined by one member of the [**D3D12\_DESCRIPTOR\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) enum:</span></span>

``` syntax
typedef enum D3D12_DESCRIPTOR_HEAP_TYPE
{
    D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV,    // Constant buffer/Shader resource/Unordered access views
    D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER,        // Samplers
    D3D12_DESCRIPTOR_HEAP_TYPE_RTV,            // Render target view
    D3D12_DESCRIPTOR_HEAP_TYPE_DSV,            // Depth stencil view
    D3D12_DESCRIPTOR_HEAP_TYPE_NUM_TYPES       // Simply the number of descriptor heap types
} D3D12_DESCRIPTOR_HEAP_TYPE;
```

## <a name="descriptor-heap-properties"></a><span data-ttu-id="9a77a-113">Deskriptorheap-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9a77a-113">Descriptor Heap Properties</span></span>

<span data-ttu-id="9a77a-114">Heap Eigenschaften werden für die [**D3D12 \_ Descriptor \_ Heap \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) -Struktur festgelegt, die sowohl auf den [**D3D12 \_ Deskriptor- \_ heaptyp \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) als auch auf [**D3D12 \_ Descriptor \_ Heap \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags) -enumerationsenumerationsvorgänge verweist.</span><span class="sxs-lookup"><span data-stu-id="9a77a-114">Heap properties are set on the [**D3D12\_DESCRIPTOR\_HEAP\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) structure, which references both the [**D3D12\_DESCRIPTOR\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) and [**D3D12\_DESCRIPTOR\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags) enums.</span></span>

<span data-ttu-id="9a77a-115">Das Flag "Flag D3D12 \_ Deskriptor \_ Heap \_ Flag", das \_ \_ sichtbar ist, kann optional für einen deskriptorheap festgelegt werden, um anzugeben, dass es an eine Befehlsliste für den Verweis durch Shader gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="9a77a-115">The flag D3D12\_DESCRIPTOR\_HEAP\_FLAG\_SHADER\_VISIBLE can optionally be set on a descriptor heap to indicate it is be bound on a command list for reference by shaders.</span></span> <span data-ttu-id="9a77a-116">Deskriptorheaps, die *ohne* dieses Flag erstellt werden, ermöglichen es Anwendungen, Deskriptoren im CPU-Arbeitsspeicher bereitzustellen, bevor Sie Sie als praktische Kopie in den sichtbaren Shader-deskriptorheap kopieren.</span><span class="sxs-lookup"><span data-stu-id="9a77a-116">Descriptor heaps created *without* this flag allow applications the option to stage descriptors in CPU memory before copying them to a shader visible descriptor heap, as a convenience.</span></span> <span data-ttu-id="9a77a-117">Es ist jedoch auch für Anwendungen in Ordnung, Deskriptoren direkt in Shader sichtbare deskriptorheaps zu erstellen, ohne dass eine Bereitstellung auf der CPU erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9a77a-117">But it is also fine for applications to directly create descriptors into shader visible descriptor heaps with no requirement to stage anything on the CPU.</span></span>

<span data-ttu-id="9a77a-118">Dieses Flag gilt nur für CBV, SRV, UAV und Samplers.</span><span class="sxs-lookup"><span data-stu-id="9a77a-118">This flag only applies to CBV, SRV, UAV and samplers.</span></span> <span data-ttu-id="9a77a-119">Sie gilt nicht für andere deskriptorheap-Typen, da Shader nicht direkt auf die anderen Typen verweisen.</span><span class="sxs-lookup"><span data-stu-id="9a77a-119">It does not apply to other descriptor heap types since shaders do not directly reference the other types.</span></span>

<span data-ttu-id="9a77a-120">Beschreiben Sie z. b. einen sampldeskriptorheap, und erstellen Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="9a77a-120">For example, describe and create a sampler descriptor heap.</span></span>


```C++
// Describe and create a sampler descriptor heap.
D3D12_DESCRIPTOR_HEAP_DESC samplerHeapDesc = {};
samplerHeapDesc.NumDescriptors = 1;
samplerHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER;
samplerHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;
ThrowIfFailed(m_device->CreateDescriptorHeap(&samplerHeapDesc, IID_PPV_ARGS(&m_samplerHeap)));
```



<span data-ttu-id="9a77a-121">Beschreiben und erstellen Sie eine Konstante Puffer Ansicht (CBV), Shader-Ressourcen Ansicht (SRV) und den deskriptorheap für die ungeordnete Zugriffs Ansicht (UAV).</span><span class="sxs-lookup"><span data-stu-id="9a77a-121">Describe and create a constant buffer view (CBV), Shader resource view (SRV), and unordered access view (UAV) descriptor heap.</span></span>


```C++
// Describe and create a shader resource view (SRV) and unordered
// access view (UAV) descriptor heap.
D3D12_DESCRIPTOR_HEAP_DESC srvUavHeapDesc = {};
srvUavHeapDesc.NumDescriptors = DescriptorCount;
srvUavHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV;
srvUavHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;
ThrowIfFailed(m_device->CreateDescriptorHeap(&srvUavHeapDesc, IID_PPV_ARGS(&m_srvUavHeap)));

m_rtvDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
m_srvUavDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV);
```



## <a name="descriptor-handles"></a><span data-ttu-id="9a77a-122">Deskriptorhandles</span><span class="sxs-lookup"><span data-stu-id="9a77a-122">Descriptor Handles</span></span>

<span data-ttu-id="9a77a-123">Die [**D3D12 \_ GPU- \_ \_ Deskriptorhandle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) -und [**D3D12-CPU- \_ \_ \_ Deskriptorhandle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) -Strukturen identifizieren bestimmte Deskriptoren in einem deskriptorheap.</span><span class="sxs-lookup"><span data-stu-id="9a77a-123">The [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) and [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structures identify specific descriptors in a descriptor heap.</span></span> <span data-ttu-id="9a77a-124">Ein Handle ist etwas wie ein Zeiger, aber die Anwendung darf es nicht manuell dereferenzieren. Andernfalls ist das Verhalten nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="9a77a-124">A handle is a bit like a pointer, but the application must not dereference it manually; otherwise, the behavior is undefined.</span></span> <span data-ttu-id="9a77a-125">Die Verwendung der Handles muss die API überlaufen.</span><span class="sxs-lookup"><span data-stu-id="9a77a-125">The use of the handles must go through the API.</span></span> <span data-ttu-id="9a77a-126">Ein Handle selbst kann frei kopiert oder an APIs weitergegeben werden, die mit Deskriptoren arbeiten bzw. verwenden.</span><span class="sxs-lookup"><span data-stu-id="9a77a-126">A handle itself can be copied freely or passed into APIs that operate on/use descriptors.</span></span> <span data-ttu-id="9a77a-127">Es gibt keine Verweis Zählung, deshalb muss die Anwendung sicherstellen, dass Sie kein Handle verwendet, nachdem der zugrunde liegende deskriptorheap gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="9a77a-127">There is no ref counting, so the application must ensure that it does not use a handle after the underlying descriptor heap has been deleted.</span></span>

<span data-ttu-id="9a77a-128">Anwendungen können die Inkrement-Größe der Deskriptoren für einen bestimmten deskriptorheap-Typ ermitteln, sodass Sie Handles für jede Position in einem deskriptorheap manuell beginnend mit dem Handle bis zur Basis generieren können.</span><span class="sxs-lookup"><span data-stu-id="9a77a-128">Applications can find out the increment size of the descriptors for a given descriptor heap type, so that they can generate handles to any location in a descriptor heap manually starting from the handle to the base.</span></span> <span data-ttu-id="9a77a-129">Anwendungen müssen die Inkrement-Größen für Deskriptorhandles niemals hart codieren und sollten Sie immer für eine bestimmte Geräte Instanz Abfragen. Andernfalls ist das Verhalten nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="9a77a-129">Applications must never hardcode descriptor handle increment sizes, and should always query them for a given device instance; otherwise, the behavior is undefined.</span></span> <span data-ttu-id="9a77a-130">Anwendungen müssen die Inkrement-Größen und-Handles nicht verwenden, um eine eigene Prüfung oder Bearbeitung von deskriptorheap-Daten durchzuführen, da die Ergebnisse nicht definiert sind.</span><span class="sxs-lookup"><span data-stu-id="9a77a-130">Applications must also not use the increment sizes and handles to do their own examination or manipulation of descriptor heap data, as the results from doing so are undefined.</span></span> <span data-ttu-id="9a77a-131">Die Handles werden möglicherweise nicht als Zeiger verwendet, sondern eher als Proxys für Zeiger, um eine versehentliche Dereferenzierung zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="9a77a-131">The handles may not actually be used as pointers, but rather as proxies for pointers so as to avoid accidental dereferencing.</span></span>

> [!Note]
>
> <span data-ttu-id="9a77a-132">Es gibt eine hilfsstruktur, ein CD3DX12 \_ GPU- \_ \_ Deskriptorhandle, das in der Kopfzeile d3dx12. h definiert ist, die die [**D3D12 \_ GPU- \_ \_ Deskriptorhandle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) -Struktur erbt und Initialisierungs-und andere nützliche Vorgänge bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9a77a-132">There is a helper structure, CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, defined in the header d3dx12.h, which inherits the [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure and provides initialization and other useful operations.</span></span> <span data-ttu-id="9a77a-133">Auf ähnliche Weise \_ wird die hilfsstruktur des CD3DX12-CPU- \_ \_ Deskriptorhandles für die [**D3D12-CPU- \_ \_ \_ Deskriptorhandle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) -Struktur definiert.</span><span class="sxs-lookup"><span data-stu-id="9a77a-133">Similarly the CD3DX12\_CPU\_DESCRIPTOR\_HANDLE helper structure is defined for the [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure.</span></span>

 

<span data-ttu-id="9a77a-134">Beide Hilfsstrukturen werden beim Auffüllen von Befehlslisten verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a77a-134">Both of these helper structures are used when populating command lists.</span></span>


```C++
// Fill the command list with all the render commands and dependent state.
void D3D12nBodyGravity::PopulateCommandList()
{
    // Command list allocators can only be reset when the associated
    // command lists have finished execution on the GPU; apps should use
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_commandAllocators[m_frameIndex]->Reset());

    // However, when ExecuteCommandList() is called on a particular command
    // list, that command list can then be reset at any time and must be before
    // re-recording.
    ThrowIfFailed(m_commandList->Reset(m_commandAllocators[m_frameIndex].Get(), m_pipelineState.Get()));

    // Set necessary state.
    m_commandList->SetPipelineState(m_pipelineState.Get());
    m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());

    m_commandList->SetGraphicsRootConstantBufferView(RootParameterCB, m_constantBufferGS->GetGPUVirtualAddress() + m_frameIndex * sizeof(ConstantBufferGS));

    ID3D12DescriptorHeap* ppHeaps[] = { m_srvUavHeap.Get() };
    m_commandList->SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

    m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);
    m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_POINTLIST);
    m_commandList->RSSetScissorRects(1, &m_scissorRect);

    // Indicate that the back buffer will be used as a render target.
    m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, nullptr);

    // Record commands.
    const float clearColor[] = { 0.0f, 0.0f, 0.1f, 0.0f };
    m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);

    // Render the particles.
    float viewportHeight = static_cast<float>(static_cast<UINT>(m_viewport.Height) / m_heightInstances);
    float viewportWidth = static_cast<float>(static_cast<UINT>(m_viewport.Width) / m_widthInstances);
    for (UINT n = 0; n < ThreadCount; n++)
    {
        const UINT srvIndex = n + (m_srvIndex[n] == 0 ? SrvParticlePosVelo0 : SrvParticlePosVelo1);

        D3D12_VIEWPORT viewport;
        viewport.TopLeftX = (n % m_widthInstances) * viewportWidth;
        viewport.TopLeftY = (n / m_widthInstances) * viewportHeight;
        viewport.Width = viewportWidth;
        viewport.Height = viewportHeight;
        viewport.MinDepth = D3D12_MIN_DEPTH;
        viewport.MaxDepth = D3D12_MAX_DEPTH;
        m_commandList->RSSetViewports(1, &viewport);

        CD3DX12_GPU_DESCRIPTOR_HANDLE srvHandle(m_srvUavHeap->GetGPUDescriptorHandleForHeapStart(), srvIndex, m_srvUavDescriptorSize);
        m_commandList->SetGraphicsRootDescriptorTable(RootParameterSRV, srvHandle);

        m_commandList->DrawInstanced(ParticleCount, 1, 0, 0);
    }

    m_commandList->RSSetViewports(1, &m_viewport);

    // Indicate that the back buffer will now be used to present.
    m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_commandList->Close());
}
```



## <a name="descriptor-heap-methods"></a><span data-ttu-id="9a77a-135">Deskriptorheap-Methoden</span><span class="sxs-lookup"><span data-stu-id="9a77a-135">Descriptor Heap Methods</span></span>

<span data-ttu-id="9a77a-136">Deskriptorheaps ([**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)) erben von [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable).</span><span class="sxs-lookup"><span data-stu-id="9a77a-136">Descriptor heaps ([**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)) inherit from [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable).</span></span> <span data-ttu-id="9a77a-137">Dies erzwingt die Residenz Verwaltung von deskriptorheaps für Anwendungen, ebenso wie Ressourcen Heaps.</span><span class="sxs-lookup"><span data-stu-id="9a77a-137">This imposes the responsibility for the residency management of descriptor heaps on applications, just like resource heaps.</span></span> <span data-ttu-id="9a77a-138">Die terminologieverwaltungmethoden gelten nur für für Shader sichtbare Heaps, da die nicht-Shader-sichtbaren Heaps nicht direkt für die GPU sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="9a77a-138">The residency management methods only apply to shader visible heaps since the non shader visible heaps are not visible to the GPU directly.</span></span>

<span data-ttu-id="9a77a-139">Die [**ID3D12Device:: getdescriptorhandleinkrementsize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize) -Methode ermöglicht es Anwendungen, Handles manuell in einen Heap zu versetzen (wodurch Handles an beliebiger Stelle in einem deskriptorheap erzeugt werden).</span><span class="sxs-lookup"><span data-stu-id="9a77a-139">The [**ID3D12Device::GetDescriptorHandleIncrementSize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize) method allows applications to manually offset handles into a heap (producing handles into anywhere in a descriptor heap).</span></span> <span data-ttu-id="9a77a-140">Das Handle des Heap Start Speicher Orts stammt aus [**ID3D12DescriptorHeap:: getcpudescriptorlenker forheapstart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) / [**ID3D12DescriptorHeap:: getgpudescriptorlenker forheapstart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart).</span><span class="sxs-lookup"><span data-stu-id="9a77a-140">The heap start location’s handle comes from [**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)/[**ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart).</span></span> <span data-ttu-id="9a77a-141">Das Offsetting erfolgt durch Hinzufügen der Inkrement-Größe \* die Anzahl der Deskriptoren, die auf den deskriptorheap-Start versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="9a77a-141">Offsetting is done by adding the increment size \* the number of descriptors to offset to the descriptor heap start .</span></span> <span data-ttu-id="9a77a-142">Beachten Sie, dass die Inkrement-Größe nicht als Bytegröße betrachtet werden kann, da Anwendungen die Handles nicht dereferenzieren dürfen, als wären Sie Arbeitsspeicher – der Speicher, auf den verwiesen wird, verfügt über ein nicht standardisiertes Layout und kann sogar für ein bestimmtes Gerät variieren.</span><span class="sxs-lookup"><span data-stu-id="9a77a-142">Note that the increment size cannot be thought of as a byte size since applications must not dereference handles as if they are memory – the memory pointed to has a non-standardized layout and can vary even for a given device.</span></span>

<span data-ttu-id="9a77a-143">[**Getcpudescriptorlenker forheapstart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) gibt ein CPU-Handle für die CPU-sichtbaren deskriptorheaps zurück.</span><span class="sxs-lookup"><span data-stu-id="9a77a-143">[**GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) returns a CPU handle for CPU visible descriptor heaps.</span></span> <span data-ttu-id="9a77a-144">Es wird ein NULL-Handle zurückgegeben (und die debugschicht meldet einen Fehler), wenn der deskriptorheap nicht CPU-sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="9a77a-144">It returns a NULL handle (and the debug layer will report an error) if the descriptor heap is not CPU visible.</span></span>

<span data-ttu-id="9a77a-145">[**Getgpudescriptorlenker forheapstart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart) gibt ein GPU-Handle für die für Shader sichtbaren deskriptorheaps zurück.</span><span class="sxs-lookup"><span data-stu-id="9a77a-145">[**GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart) returns a GPU handle for shader visible descriptor heaps.</span></span> <span data-ttu-id="9a77a-146">Es wird ein NULL-Handle zurückgegeben (und die debugschicht meldet einen Fehler), wenn der deskriptorheap nicht als Shader sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="9a77a-146">It returns a NULL handle (and the debug layer will report an error) if the descriptor heap is not shader visible.</span></span>

<span data-ttu-id="9a77a-147">Beispielsweise erstellen Sie renderzielsichten, um D2D Text mit einem 11on12-Gerät anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9a77a-147">For example, creating render target views to display D2D text using an 11on12 device.</span></span>


```C++
    // Create descriptor heaps.
    {
        // Describe and create a render target view (RTV) descriptor heap.
        D3D12_DESCRIPTOR_HEAP_DESC rtvHeapDesc = {};
        rtvHeapDesc.NumDescriptors = FrameCount;
        rtvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_RTV;
        rtvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
        ThrowIfFailed(m_d3d12Device->CreateDescriptorHeap(&rtvHeapDesc, IID_PPV_ARGS(&m_rtvHeap)));

        m_rtvDescriptorSize = m_d3d12Device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
    }

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

        // Create a RTV, D2D render target, and a command allocator for each frame.
        for (UINT n = 0; n < FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
            m_d3d12Device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);

            // Create a wrapped 11On12 resource of this back buffer. Since we are 
            // rendering all D3D12 content first and then all D2D content, we specify 
            // the In resource state as RENDER_TARGET - because D3D12 will have last 
            // used it in this state - and the Out resource state as PRESENT. When 
            // ReleaseWrappedResources() is called on the 11On12 device, the resource 
            // will be transitioned to the PRESENT state.
            D3D11_RESOURCE_FLAGS d3d11Flags = { D3D11_BIND_RENDER_TARGET };
            ThrowIfFailed(m_d3d11On12Device->CreateWrappedResource(
                m_renderTargets[n].Get(),
                &d3d11Flags,
                D3D12_RESOURCE_STATE_RENDER_TARGET,
                D3D12_RESOURCE_STATE_PRESENT,
                IID_PPV_ARGS(&m_wrappedBackBuffers[n])
                ));

            // Create a render target for D2D to draw directly to this back buffer.
            ComPtr<IDXGISurface> surface;
            ThrowIfFailed(m_wrappedBackBuffers[n].As(&surface));
            ThrowIfFailed(m_d2dDeviceContext->CreateBitmapFromDxgiSurface(
                surface.Get(),
                &bitmapProperties,
                &m_d2dRenderTargets[n]
                ));

            rtvHandle.Offset(1, m_rtvDescriptorSize);

            ThrowIfFailed(m_d3d12Device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocators[n])));
        }
    
    }
```



## <a name="minimal-descriptor-heap-wrapper"></a><span data-ttu-id="9a77a-148">Wrapper für minimalen deskriptorheap</span><span class="sxs-lookup"><span data-stu-id="9a77a-148">Minimal descriptor heap wrapper</span></span>

<span data-ttu-id="9a77a-149">Anwendungsentwickler möchten wahrscheinlich ihren eigenen Hilfscode zum Verwalten von Deskriptorhandles und Heaps erstellen.</span><span class="sxs-lookup"><span data-stu-id="9a77a-149">Application developers will likely want to build their own helper code for managing descriptor handles and heaps.</span></span> <span data-ttu-id="9a77a-150">Unten ist ein einfaches Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9a77a-150">A basic example is shown below.</span></span> <span data-ttu-id="9a77a-151">Komplexere Wrapper können z. b. nachverfolgen, welche Arten von Deskriptoren sich in einem Heap befinden und die deskriptorerstellungs-Argumente speichern.</span><span class="sxs-lookup"><span data-stu-id="9a77a-151">More sophisticated wrappers could, for example, keep track of what types of descriptors are where in a heap and store the descriptor creation arguments.</span></span>

``` syntax
class CDescriptorHeapWrapper
{
public:
    CDescriptorHeapWrapper() { memset(this, 0, sizeof(*this)); }

    HRESULT Create(
        ID3D12Device* pDevice, 
        D3D12_DESCRIPTOR_HEAP_TYPE Type, 
        UINT NumDescriptors, 
        bool bShaderVisible = false)
    {
        D3D12_DESCRIPTOR_HEAP_DESC Desc;
        Desc.Type = Type;
        Desc.NumDescriptors = NumDescriptors;
        Desc.Flags = (bShaderVisible ? D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE : D3D12_DESCRIPTOR_HEAP_FLAG_NONE);
       
        HRESULT hr = pDevice->CreateDescriptorHeap(&Desc, 
                               __uuidof(ID3D12DescriptorHeap), 
                               (void**)&pDH);
        if (FAILED(hr)) return hr;

        hCPUHeapStart = pDH->GetCPUDescriptorHandleForHeapStart();
        hGPUHeapStart = pDH->GetGPUDescriptorHandleForHeapStart();

        HandleIncrementSize = pDevice->GetDescriptorHandleIncrementSize(Desc.Type);
        return hr;
    }
    operator ID3D12DescriptorHeap*() { return pDH; }

    D3D12_CPU_DESCRIPTOR_HANDLE hCPU(UINT index)
    {
        return hCPUHeapStart.MakeOffsetted(index,HandleIncrementSize); 
    }
    D3D12_GPU_DESCRIPTOR_HANDLE hGPU(UINT index) 
    {
        assert(Desc.Flags&D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE); 
        return hGPUHeapStart.MakeOffsetted(index,HandleIncrementSize); 
    }
    D3D12_DESCRIPTOR_HEAP_DESC Desc;
    CComPtr<ID3D12DescriptorHeap> pDH;
    D3D12_CPU_DESCRIPTOR_HANDLE hCPUHeapStart;
    D3D12_GPU_DESCRIPTOR_HANDLE hGPUHeapStart;
    UINT HandleIncrementSize;
};
```

## <a name="related-topics"></a><span data-ttu-id="9a77a-152">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9a77a-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a77a-153">Deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="9a77a-153">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 