---
title: Erstellen von Deskriptorheaps
description: Zum Erstellen und Konfigurieren eines Deskriptor-Heaps müssen Sie einen Deskriptor-Heaptyp auswählen, bestimmen, wie viele Deskriptoren er enthält, und Flags festlegen, die angeben, ob er cpu- und/oder shader sichtbar ist.
ms.assetid: 58677023-692C-4BA4-90B7-D568F3DD3F73
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218d21d462dd393360e9ebfcb07ab5b35524b9d8d8c01c8ab1ef28ef90166eb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857990"
---
# <a name="creating-descriptor-heaps"></a>Erstellen von Deskriptorheaps

Zum Erstellen und Konfigurieren eines Deskriptor-Heaps müssen Sie einen Deskriptor-Heaptyp auswählen, bestimmen, wie viele Deskriptoren er enthält, und Flags festlegen, die angeben, ob er cpu- und/oder shader sichtbar ist.

-   [Deskriptor-Heaptypen](#descriptor-heap-types)
-   [Deskriptor-Heapeigenschaften](#descriptor-heap-properties)
-   [Deskriptorhandles](#descriptor-handles)
-   [Deskriptor-Heapmethoden](#descriptor-heap-methods)
-   [Minimaler Deskriptor-Heap-Wrapper](#minimal-descriptor-heap-wrapper)
-   [Zugehörige Themen](#related-topics)

## <a name="descriptor-heap-types"></a>Deskriptor-Heaptypen

Der Heaptyp wird von einem Member der [**D3D12 \_ DESCRIPTOR \_ HEAP TYPE-Enumerator \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) bestimmt:

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

## <a name="descriptor-heap-properties"></a>Deskriptor-Heapeigenschaften

Heapeigenschaften werden für die [**D3D12 \_ DESCRIPTOR \_ HEAP \_ DESC-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) festgelegt, die sowohl auf die [**D3D12 \_ DESCRIPTOR \_ HEAP \_ TYPE-**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) als auch [**auf die D3D12 \_ DESCRIPTOR \_ HEAP FLAGS-Enumeren \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags) verweist.

Das Flag D3D12 DESCRIPTOR HEAP FLAG SHADER VISIBLE kann optional für einen \_ \_ \_ \_ Deskriptorhap festgelegt werden, um anzugeben, dass es an eine Befehlsliste gebunden ist, um von \_ Shadern referenziert zu werden. Deskriptorheaps,  die ohne dieses Flag erstellt wurden, ermöglichen Es Anwendungen, Deskriptoren im CPU-Arbeitsspeicher vor dem Kopieren in einen shader sichtbaren Deskriptorheap aus Gründen der Einfachheit zu stagen. Es ist aber auch für Anwendungen in Ordnung, Deskriptoren direkt in Shader-sichtbaren Deskriptorhaps zu erstellen, ohne dass eine Stufe auf der CPU erforderlich ist.

Dieses Flag gilt nur für CBV, SRV, UAV und Sampler. Sie gilt nicht für andere Deskriptor-Heaptypen, da Shader nicht direkt auf die anderen Typen verweisen.

Beschreiben und erstellen Sie beispielsweise einen Samplerdeskriptor-Heap.


```C++
// Describe and create a sampler descriptor heap.
D3D12_DESCRIPTOR_HEAP_DESC samplerHeapDesc = {};
samplerHeapDesc.NumDescriptors = 1;
samplerHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER;
samplerHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;
ThrowIfFailed(m_device->CreateDescriptorHeap(&samplerHeapDesc, IID_PPV_ARGS(&m_samplerHeap)));
```



Beschreiben und erstellen Sie einen CBV-Deskriptordeskriptor-Heap (Constant Buffer View), eine Shader-Ressourcenansicht (SRV) und eine ungeordnete Zugriffsansicht (Unordered Access View, UAV).


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



## <a name="descriptor-handles"></a>Deskriptorhandles

Die [**STRUKTUREN D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) und [**D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) identifizieren bestimmte Deskriptoren in einem Deskriptorhap. Ein Handle ist ein wenig wie ein Zeiger, aber die Anwendung darf es nicht manuell dereferenzieren. Andernfalls ist das Verhalten nicht definiert. Die Verwendung der Handles muss über die API gehen. Ein Handle selbst kann frei kopiert oder an APIs übergeben werden, die Deskriptoren verwenden bzw. verwenden. Es gibt keine Ref-Zählung, daher muss die Anwendung sicherstellen, dass sie kein Handle verwendet, nachdem der zugrunde liegende Deskriptorhap gelöscht wurde.

Anwendungen können die Inkrementgröße der Deskriptoren für einen bestimmten Deskriptor-Heaptyp herausfinden, sodass sie Handles an jedem Speicherort in einem Deskriptorhap manuell generieren können, beginnend vom Handle bis zur Basis. Anwendungen dürfen inkrementierte Größen niemals hartcodieren und sollten sie immer für eine bestimmte Geräteinstanz abfragen. Andernfalls ist das Verhalten nicht definiert. Anwendungen dürfen auch nicht die inkrementierten Größen und Handles verwenden, um ihre eigene Untersuchung oder Bearbeitung von Deskriptor-Heapdaten zu tun, da die Ergebnisse daraus nicht definiert sind. Die Handles werden möglicherweise nicht als Zeiger, sondern als Proxys für Zeiger verwendet, um eine versehentliche Deleitung zu vermeiden.

> [!Note]
>
> Es gibt eine Hilfsstruktur, CD3DX12 GPU DESCRIPTOR HANDLE, definiert im Header \_ \_ \_ d3dx12.h, die die [**D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) erbt und Initialisierung und andere nützliche Vorgänge bietet. Ebenso wird die HILFSstruktur CD3DX12 CPU DESCRIPTOR HANDLE für die \_ \_ \_ [**D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) definiert.

 

Beide Hilfsstrukturen werden beim Auflisten von Befehlslisten verwendet.


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



## <a name="descriptor-heap-methods"></a>Deskriptor-Heapmethoden

Deskriptorheaps ([**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)) erben von [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable). Dies erzwingt die Verantwortung für die Verwaltung derResidenz von Deskriptorhaps für Anwendungen, genau wie Ressourcenhaps. Die Verwaltungsmethoden für die Residency gelten nur für shader-sichtbare Heaps, da die nicht shader sichtbaren Heaps nicht direkt für die GPU sichtbar sind.

Mit der [**ID3D12Device::GetDescriptorHandleIncrementSize-Methode**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize) können Anwendungen Handles manuell in einem Heap veroffen (handles werden an einer beliebigen Stelle in einem Deskriptor-Heap erzeugt). Das Handle des Heapstartspeicherorts stammt von [**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) / [**ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart). Das Deaktivieren erfolgt durch Hinzufügen der Inkrementgröße der Anzahl von Deskriptoren, die dem \* Deskriptor heap start versetzt werden soll. Beachten Sie, dass die Inkrementgröße nicht als Bytegröße gedacht werden kann, da Anwendungen Handles nicht dereferenzieren dürfen, als ob es sich um Arbeitsspeicher handelt. Der Arbeitsspeicher, auf den verwiesen wird, weist ein nicht standardisiertes Layout auf und kann auch für ein bestimmtes Gerät variieren.

[**GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) gibt ein CPU-Handle für CPU-sichtbare Deskriptorheaps zurück. Sie gibt ein NULL-Handle zurück (und die Debugebene gibt einen Fehler aus), wenn der Deskriptorhap nicht CPU-sichtbar ist.

[**GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart) gibt ein GPU-Handle für shader-sichtbare Deskriptorheaps zurück. Sie gibt ein NULL-Handle zurück (und die Debugebene gibt einen Fehler aus), wenn der Deskriptorhap nicht sichtbar ist.

Beispiel: Erstellen von Renderzielansichten zum Anzeigen von D2D-Text mithilfe eines 11on12-Geräts.


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



## <a name="minimal-descriptor-heap-wrapper"></a>Minimaler Deskriptor-Heap-Wrapper

Anwendungsentwickler möchten wahrscheinlich ihren eigenen Hilfscode für die Verwaltung von Deskriptorhandles und Heaps erstellen. Im Folgenden finden Sie ein einfaches Beispiel. Komplexere Wrapper könnten beispielsweise nachverfolgen, welche Arten von Deskriptoren sich in einem Heap befinden, und die Argumente für die Deskriptorerstellung speichern.

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

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deskriptorheaps](descriptor-heaps.md)
</dt> </dl>

 

 