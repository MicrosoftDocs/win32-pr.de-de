---
title: Erstellen und Aufzeichnen von Befehlslisten und Paketen
description: In diesem Thema werden Aufzeichnungsbefehlslisten und -pakete in Direct3D 12-Apps beschrieben. Befehlslisten und -bündel ermöglichen Apps das Aufzeichnen von Zeichnungs- oder zustandsverändernden Aufrufen zur späteren Ausführung auf der Grafikprozessor (Graphics Processing Unit, GPU).
ms.assetid: 0074B796-33A4-4AA1-A4E7-48A2A63F25B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 480819cbd421b30cbf54a58578c02056d37d7e36bf2ead845c19e438df54cbb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850711"
---
# <a name="creating-and-recording-command-lists-and-bundles"></a>Erstellen und Aufzeichnen von Befehlslisten und Paketen

In diesem Thema werden Aufzeichnungsbefehlslisten und -pakete in Direct3D 12-Apps beschrieben. Befehlslisten und -bündel ermöglichen Apps das Aufzeichnen von Zeichnungs- oder zustandsverändernden Aufrufen zur späteren Ausführung auf der Grafikprozessor (Graphics Processing Unit, GPU).

Neben Befehlslisten nutzt die API die in GPU-Hardware verfügbaren Funktionen, indem eine zweite Ebene von Befehlslisten hinzugefügt wird, die als Bündel *bezeichnet werden.* Der Zweck von Paketen besteht im Zulassen, dass Apps eine kleine Anzahl von API-Befehlen zur späteren Ausführung gruppiert. Zum Zeitpunkt der Bündelerstellung führt der Treiber so viele Vorverarbeitungen durch, wie möglich sind, damit diese später kostengünstig ausgeführt werden können. Bundles sind so konzipiert, dass sie verwendet und mehrmals erneut verwendet werden können. Befehlslisten werden dagegen in der Regel nur einmal ausgeführt. Eine Befehlsliste  kann jedoch mehrmals ausgeführt werden (solange die Anwendung sicherstellt, dass die vorherigen Ausführungen abgeschlossen wurden, bevor neue Ausführungen zu übermitteln sind).

In der Regel wird die Erstellung von API-Aufrufen in Bündeln sowie API-Aufrufe und -Bündel in Befehlslisten und Befehlslisten in einem einzelnen Frame im folgenden Diagramm dargestellt. Dabei wird die Wiederverwendung von **Bundle 1** in Befehlsliste **1** und Befehlsliste **2** berücksichtigt, und die API-Methodennamen im Diagramm sind ebenso wie Beispiele. Viele verschiedene API-Aufrufe können verwendet werden.

![Erstellen von Befehlen, Paketen und Befehlslisten in Frames](images/gpu-workitems.png)

Es gibt unterschiedliche Einschränkungen beim Erstellen und Ausführen von Paketen und direkten Befehlslisten, und diese Unterschiede werden in diesem Thema beschrieben.

## <a name="creating-command-lists"></a>Erstellen von Befehlslisten

Direkte Befehlslisten und Pakete werden durch Aufrufen von [**ID3D12Device::CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) oder [**ID3D12Device4::CreateCommandList1 erstellt.**](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-createcommandlist1)

Verwenden [**Sie ID3D12Device4::CreateCommandList1,**](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-createcommandlist1) um eine geschlossene Befehlsliste zu erstellen, anstatt eine neue Liste zu erstellen und sofort zu schließen. Dadurch wird die Ineffizienz vermieden, eine Liste mit einer Zuweisung und einem PSO zu erstellen, ohne sie zu verwenden.

[**ID3D12Device::CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) verwendet die folgenden Parameter als Eingabe:

### <a name="d3d12_command_list_type"></a>BEFEHLSLISTENTYP "D3D12" \_ \_ \_

Die [**D3D12 \_ COMMAND LIST \_ \_ TYPE-Enumeration**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) gibt den Typ der Befehlsliste an, die erstellt wird. Dabei kann es sich um eine direkte Befehlsliste, ein Paket, eine Computebefehlsliste oder eine Kopierbefehlsliste geben.

### <a name="id3d12commandallocator"></a>ID3D12CommandAllocator

Mit einer Befehlszuweisung kann die App den Arbeitsspeicher verwalten, der befehlslisten zugeordnet ist. Die Befehlszuweisung wird durch Aufrufen von [**CreateCommandAllocator erstellt.**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator) Beim Erstellen einer Befehlsliste muss der Befehlslistentyp der Zuweisung, der durch [**D3D12 \_ COMMAND \_ LIST \_ TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)angegeben wird, mit dem Typ der erstellten Befehlsliste übereinstimmen. Eine bestimmte Zuweisung kann nicht mehr  als einer befehlsliste zugeordnet werden, die derzeit eine Aufzeichnungsbefehlsliste auflistet, obwohl eine Befehlszuweisung verwendet werden kann, um eine beliebige Anzahl von [**GraphicsCommandList-Objekten zu**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) erstellen.

Um den von einer Befehlszuweisung zugewiesenen Arbeitsspeicher wieder verfügbar zu machen, ruft eine App [**ID3D12CommandAllocator::Reset auf.**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset) Dadurch kann die Zuweisung für neue Commmands wiederverwendet werden, die zugrunde liegende Größe wird jedoch nicht reduziert. Bevor dies jedoch der Fall ist, muss die App sicherstellen, dass die GPU keine Befehlslisten mehr ausgeführt, die der Zuweisung zugeordnet sind. Andernfalls kann der Aufruf nicht mehr werden. Beachten Sie außerdem, dass diese API kein Freethreading ist und daher nicht gleichzeitig über mehrere Threads auf derselben Zuweisung aufgerufen werden kann.

### <a name="id3d12pipelinestate"></a>ID3D12PipelineState

Der anfängliche Pipelinezustand für die Befehlsliste. In Microsoft Direct3D 12 wird der meiste Grafikpipelinezustand in einer Befehlsliste mithilfe des [**ID3D12PipelineState-Objekts**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) festgelegt. Eine App erstellt eine große Anzahl dieser Objekte, in der Regel während der App-Initialisierung, und dann wird der Zustand aktualisiert, indem das derzeit gebundene [**Zustandsobjekt mithilfe von ID3D12GraphicsCommandList::SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)geändert wird. Weitere Informationen zu Pipelinezustandsobjekten finden Sie unter [Verwalten des Grafikpipelinezustands in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).

Beachten Sie, dass Bundles nicht den Pipelinezustand erben, der durch vorherige Aufrufe in direkten Befehlslisten festgelegt wurde, die ihre übergeordneten Befehle sind.

Wenn dieser Parameter NULL ist, wird ein Standardzustand verwendet.

## <a name="recording-command-lists"></a>Aufzeichnungsbefehlslisten

Unmittelbar nach dem Erstellen befinden sich Befehlslisten im Aufzeichnungszustand. Sie können auch eine vorhandene Befehlsliste erneut verwenden, indem Sie I [**D3D12GraphicsCommandList::Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)aufrufen, wodurch auch die Befehlsliste im Aufzeichnungszustand belässt. Im [**Gegensatz zu ID3D12CommandAllocator::Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)können Sie **Reset** aufrufen, während die Befehlsliste noch ausgeführt wird. Ein typisches Muster ist das Übermitteln einer Befehlsliste und das anschließende sofortige Zurücksetzen, um den zugeordneten Arbeitsspeicher für eine andere Befehlsliste wiederzuverwenden. Beachten Sie, dass sich nur eine Befehlsliste, die den einzelnen Befehlszuweisungen zugeordnet ist, gleichzeitig in einem Aufzeichnungszustand finden kann.

Sobald sich eine Befehlsliste im Aufzeichnungszustand befindet, rufen Sie einfach Methoden der [**ID3D12GraphicsCommandList-Schnittstelle**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) auf, um der Liste Befehle hinzuzufügen. Viele dieser Methoden ermöglichen allgemeine Direct3D-Funktionen, die Microsoft Direct3D 11-Entwicklern bekannt sein werden. Andere APIs sind neu für Direct3D 12.

Nachdem Sie der Befehlsliste Befehle hinzugefügt haben, überwechseln Sie die Befehlsliste aus dem Aufzeichnungszustand, indem Sie [**Close aufrufen.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)

Befehlszuweisungen können zunehmen, aber nicht verkleinert werden. Pooling- und Wiederverwendungszuweisungen sollten berücksichtigt werden, um die Effizienz Ihrer App zu steigern. Sie können mehrere Listen für dieselbe Zuweisung aufzeichnen, bevor sie zurückgesetzt wird, vorausgesetzt, nur eine Liste wird gleichzeitig für eine bestimmte Zuweisung aufzeichnen. Sie können jede Liste als Besitzen eines Teils der Zuweisung visualisieren, der angibt, welche [**ID3D12CommandQueue::ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) ausgeführt wird.

Eine einfache Zuweisungspoolstrategie sollte auf ungefähre `numCommandLists * MaxFrameLatency` Zuweisungen abzielen. Wenn Sie beispielsweise 6 Listen aufzeichnen und bis zu 3 latente Frames zulassen, können Sie mit 18 bis 20 Zuweisungen rechnen. Eine erweiterte Poolingstrategie, bei der Zuweisungen für mehrere Listen im gleichen Thread wiederverwendet werden, könnte auf `numRecordingThreads * MaxFrameLatency` Zuweisungen abzielen. Wenn im vorherigen Beispiel zwei Listen für Thread A, 2 für Thread B, 1 für Thread C und 1 für Thread D aufgezeichnet wurden, könnten Sie realistischerweise 12-14 Zuweisungen verwenden.

Verwenden Sie einen Fence, um zu bestimmen, wann eine bestimmte Zuweisung wiederverwendet werden kann.

Da Befehlslisten sofort nach der Ausführung zurückgesetzt werden können, können sie trivial in einem Pool zusammengelegt werden, indem sie nach jedem Aufruf von [**ID3D12CommandQueue::ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)wieder dem Pool hinzugefügt werden.

## <a name="example"></a>Beispiel

Die folgenden Codeausschnitte veranschaulichen die Erstellung und Aufzeichnung einer Befehlsliste. Beachten Sie, dass dieses Beispiel die folgenden Direct3D 12-Features enthält:

-   Pipelinezustandsobjekte: Diese werden verwendet, um die meisten Zustandsparameter der Renderpipeline aus einer Befehlsliste zu bestimmen. Weitere Informationen finden Sie unter [Verwalten des Grafikpipelinezustands in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).
-   Deskriptor-Heap: Apps verwenden Deskriptorhaps, um die Pipelinebindung an Arbeitsspeicherressourcen zu verwalten.
-   Ressourcenbarriere: Wird verwendet, um den Übergang von Ressourcen von einem Zustand in einen anderen zu verwalten, z. B. von einer Renderzielansicht zu einer Shaderressourcenansicht. Weitere Informationen finden Sie unter [Verwenden von Ressourcenbarrieren zum Synchronisieren von Ressourcenzuständen.](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

Beispiel:


```C++
void D3D12HelloTriangle::LoadAssets()
{
    // Create an empty root signature.
    {
        CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
        rootSignatureDesc.Init(0, nullptr, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

        ComPtr<ID3DBlob> signature;
        ComPtr<ID3DBlob> error;
        ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
        ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));
    }

    // Create the pipeline state, which includes compiling and loading shaders.
    {
        ComPtr<ID3DBlob> vertexShader;
        ComPtr<ID3DBlob> pixelShader;

#if defined(_DEBUG)
        // Enable better shader debugging with the graphics debugging tools.
        UINT compileFlags = D3DCOMPILE_DEBUG | D3DCOMPILE_SKIP_OPTIMIZATION;
#else
        UINT compileFlags = 0;
#endif

        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "VSMain", "vs_5_0", compileFlags, 0, &vertexShader, nullptr));
        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "PSMain", "ps_5_0", compileFlags, 0, &pixelShader, nullptr));

        // Define the vertex input layout.
        D3D12_INPUT_ELEMENT_DESC inputElementDescs[] =
        {
            { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 },
            { "COLOR", 0, DXGI_FORMAT_R32G32B32A32_FLOAT, 0, 12, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 }
        };

        // Describe and create the graphics pipeline state object (PSO).
        D3D12_GRAPHICS_PIPELINE_STATE_DESC psoDesc = {};
        psoDesc.InputLayout = { inputElementDescs, _countof(inputElementDescs) };
        psoDesc.pRootSignature = m_rootSignature.Get();
        psoDesc.VS = { reinterpret_cast<UINT8*>(vertexShader->GetBufferPointer()), vertexShader->GetBufferSize() };
        psoDesc.PS = { reinterpret_cast<UINT8*>(pixelShader->GetBufferPointer()), pixelShader->GetBufferSize() };
        psoDesc.RasterizerState = CD3DX12_RASTERIZER_DESC(D3D12_DEFAULT);
        psoDesc.BlendState = CD3DX12_BLEND_DESC(D3D12_DEFAULT);
        psoDesc.DepthStencilState.DepthEnable = FALSE;
        psoDesc.DepthStencilState.StencilEnable = FALSE;
        psoDesc.SampleMask = UINT_MAX;
        psoDesc.PrimitiveTopologyType = D3D12_PRIMITIVE_TOPOLOGY_TYPE_TRIANGLE;
        psoDesc.NumRenderTargets = 1;
        psoDesc.RTVFormats[0] = DXGI_FORMAT_R8G8B8A8_UNORM;
        psoDesc.SampleDesc.Count = 1;
        ThrowIfFailed(m_device->CreateGraphicsPipelineState(&psoDesc, IID_PPV_ARGS(&m_pipelineState)));
    }

    // Create the command list.
    ThrowIfFailed(m_device->CreateCommandList(0, D3D12_COMMAND_LIST_TYPE_DIRECT, m_commandAllocator.Get(), m_pipelineState.Get(), IID_PPV_ARGS(&m_commandList)));

    // Command lists are created in the recording state, but there is nothing
    // to record yet. The main loop expects it to be closed, so close it now.
    ThrowIfFailed(m_commandList->Close());

    // Create the vertex buffer.
    {
        // Define the geometry for a triangle.
        Vertex triangleVertices[] =
        {
            { { 0.0f, 0.25f * m_aspectRatio, 0.0f }, { 1.0f, 0.0f, 0.0f, 1.0f } },
            { { 0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 1.0f, 0.0f, 1.0f } },
            { { -0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 0.0f, 1.0f, 1.0f } }
        };

        const UINT vertexBufferSize = sizeof(triangleVertices);

        // Note: using upload heaps to transfer static data like vert buffers is not 
        // recommended. Every time the GPU needs it, the upload heap will be marshalled 
        // over. Please read up on Default Heap usage. An upload heap is used here for 
        // code simplicity and because there are very few verts to actually transfer.
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(vertexBufferSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBuffer)));

        // Copy the triangle data to the vertex buffer.
        UINT8* pVertexDataBegin;
        CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
        ThrowIfFailed(m_vertexBuffer->Map(0, &readRange, reinterpret_cast<void**>(&pVertexDataBegin)));
        memcpy(pVertexDataBegin, triangleVertices, sizeof(triangleVertices));
        m_vertexBuffer->Unmap(0, nullptr);

        // Initialize the vertex buffer view.
        m_vertexBufferView.BufferLocation = m_vertexBuffer->GetGPUVirtualAddress();
        m_vertexBufferView.StrideInBytes = sizeof(Vertex);
        m_vertexBufferView.SizeInBytes = vertexBufferSize;
    }

    // Create synchronization objects and wait until assets have been uploaded to the GPU.
    {
        ThrowIfFailed(m_device->CreateFence(0, D3D12_FENCE_FLAG_NONE, IID_PPV_ARGS(&m_fence)));
        m_fenceValue = 1;

        // Create an event handle to use for frame synchronization.
        m_fenceEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);
        if (m_fenceEvent == nullptr)
        {
            ThrowIfFailed(HRESULT_FROM_WIN32(GetLastError()));
        }

        // Wait for the command list to execute; we are reusing the same command 
        // list in our main loop but for now, we just want to wait for setup to 
        // complete before continuing.
        WaitForPreviousFrame();
    }
}
```



Nachdem eine Befehlsliste erstellt und aufgezeichnet wurde, kann sie mithilfe einer Befehlswarteschlange ausgeführt werden. Weitere Informationen finden Sie unter [Ausführen und Synchronisieren von Befehlslisten.](executing-and-synchronizing-command-lists.md)

## <a name="reference-counting"></a>Verweisanzahl

Die meisten D3D12-APIs verwenden weiterhin die Verweiszählung, die den COM-Konventionen folgt. Eine wichtige Ausnahme sind die D3D12-Grafikbefehlslisten-APIs. Alle APIs in [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) enthalten keine Verweise auf die Objekte, die an diese APIs übergeben werden. Dies bedeutet, dass Anwendungen dafür verantwortlich sind, sicherzustellen, dass nie eine Befehlsliste zur Ausführung übermittelt wird, die auf eine zerstörte Ressource verweist.

## <a name="command-list-errors"></a>Fehler bei der Befehlsliste

Die meisten APIs in [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) geben keine Fehler zurück. Fehler, die während der Erstellung der Befehlsliste auftreten, werden bis [**ID3D12GraphicsCommandList::Close verzögert.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close) Die einzige Ausnahme ist DXGI \_ ERROR \_ DEVICE \_ REMOVED, die noch weiter zurückgestellt wird. Beachten Sie, dass sich dies von D3D11 unterscheiden, bei dem viele Parametervalidierungsfehler automatisch gelöscht und nie an den Aufrufer zurückgegeben werden.

Anwendungen können mit DXGI DEVICE \_ \_ REMOVED-Fehlern in den folgenden API-Aufrufen rechnen:

-   Eine beliebige Methode zum Erstellen von Ressourcen
-   [**ID3D12Resource::Map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)
-   [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)
-   [**GetDeviceRemovedReason**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)

## <a name="command-list-api-restrictions"></a>API-Einschränkungen der Befehlsliste

Einige Befehlslisten-APIs können nur für bestimmte Typen von Befehlslisten aufgerufen werden. Die folgende Tabelle zeigt, welche Befehlslisten-APIs für jeden Befehlslistentyp gültig sind. Außerdem wird gezeigt, welche APIs in einem [**D3D12-Renderpass aufruft werden können.**](./direct3d-12-render-passes.md) 

| API-Name                                         | Grafiken | Compute | Kopieren | Bundle | In Renderpass |
|--------------------------------------------------|:--------:|:-------:|:----:|:------:|:--------------:|
| AtomicCopyBufferUINT                             | ✓        | ✓       | ✓    |        |                |
| AtomicCopyBufferUINT64                           | ✓        | ✓       | ✓    |        |                |
| BeginQuery                                       | ✓        |         |      |        | ✓              |
| BeginRenderPass                                  | ✓        |         |      |        |                |
| BuildRaytracingAccelerationStructure             | ✓        | ✓       |      |        |                |
| ClearDepthStencilView                            | ✓        |         |      |        |                |
| ClearRenderTargetView                            | ✓        |         |      |        |                |
| ClearState                                       | ✓        | ✓       |      |        |                |
| ClearUnorderedAccessViewFloat                    | ✓        | ✓       |      |        |                |
| ClearUnorderedAccessViewUint                     | ✓        | ✓       |      |        |                |
| CopyBufferRegion                                 | ✓        | ✓       | ✓    |        |                |
| CopyRaytracingAccelerationStructure              | ✓        | ✓       |      |        |                |
| CopyResource                                     | ✓        | ✓       | ✓    |        |                |
| CopyTextureRegion                                | ✓        | ✓       | ✓    |        |                |
| CopyTiles                                        | ✓        | ✓       | ✓    |        |                |
| DiscardResource                                  | ✓        | ✓       |      |        |                |
| Dispatch                                         | ✓        | ✓       |      | ✓      |                |
| DispatchRays                                     | ✓        | ✓       |      | ✓      |                |
| DrawIndexedInstanced                             | ✓        |         |      | ✓      | ✓              |
| DrawInstanced                                    | ✓        |         |      | ✓      | ✓              |
| EmitRaytracingAccelerationStructurePostbuildInfo | ✓        | ✓       |      |        |                |
| EndQuery                                         | ✓        | ✓       | ✓    |        | ✓              |
| EndRenderPass                                    | ✓        |         |      |        | ✓              |
| ExecuteBundle                                    | ✓        |         |      |        | ✓              |
| ExecuteIndirect                                  | ✓        | ✓       |      | ✓      | ✓              |
| ExecuteMetaCommand                               | ✓        | ✓       |      |        |                |
| IASetIndexBuffer                                 | ✓        |         |      | ✓      | ✓              |
| IASetPrimitiveTopology                           | ✓        |         |      | ✓      | ✓              |
| IASetVertexBuffers                               | ✓        |         |      | ✓      | ✓              |
| InitializeMetaCommand                            | ✓        | ✓       |      |        |                |
| OMSetBlendFactor                                 | ✓        |         |      | ✓      | ✓              |
| OMSetDepthBounds                                 | ✓        |         |      | ✓      | ✓              |
| OMSetRenderTargets                               | ✓        |         |      |        |                |
| OMSetStencilRef                                  | ✓        |         |      | ✓      | ✓              |
| ResolveQueryData                                 | ✓        | ✓       | ✓    |        |                |
| ResolveSubresource                               | ✓        |         |      |        |                |
| ResolveSubresourceRegion                         | ✓        |         |      |        |                |
| ResourceBarrier                                  | ✓        | ✓       | ✓    |        | ✓              |
| RSSetScissorRects                                | ✓        |         |      |        | ✓              |
| RSSetShadingRate                                 | ✓        |         |      | ✓      | ✓              |
| RSSetShadingRateImage                            | ✓        |         |      | ✓      | ✓              |
| RSSetViewports                                   | ✓        |         |      |        | ✓              |
| SetComputeRoot32BitConstant                      | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRoot32BitConstants                     | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootConstantBufferView                 | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootDescriptorTable                    | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootShaderResourceView                 | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootSignature                          | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootUnorderedAccessView                | ✓        | ✓       |      | ✓      | ✓              |
| SetDescriptorHeaps                               | ✓        | ✓       |      | ✓      | ✓              |
| SetGraphicsRoot32BitConstant                     | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRoot32BitConstants                    | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootConstantBufferView                | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootDescriptorTable                   | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootShaderResourceView                | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootSignature                         | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootUnorderedAccessView               | ✓        |         |      | ✓      | ✓              |
| SetPipelineState                                 | ✓        | ✓       |      | ✓      | ✓              |
| SetPipelineState1                                | ✓        | ✓       |      | ✓      |                |
| SetPredication                                   | ✓        | ✓       |      |        | ✓              |
| SetProtectedResourceSession                      | ✓        | ✓       | ✓    |        |                |
| SetSamplePositions                               | ✓        |         |      | ✓      | ✓              |
| SetViewInstanceMask                              | ✓        |         |      | ✓      | ✓              |
| SOSetTargets                                     | ✓        |         |      |        | ✓              |
| WriteBufferImmediate                             | ✓        | ✓       | ✓    | ✓      | ✓              |

## <a name="bundle-restrictions"></a>Bündeleinschränkungen

Einschränkungen ermöglichen Es Direct3D 12-Treibern, den Großteil der Arbeit im Zusammenhang mit Paketen zur Aufzeichnungszeit auszuführen, sodass die [**ExecuteBundle-API**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) mit geringem Mehraufwand ausgeführt werden kann. Alle Pipelinezustandsobjekte, auf die von einem Bündel verwiesen wird, müssen die gleichen Renderzielformate, dasselbe Tiefenpufferformat und die gleichen Beispielbeschreibungen haben.

Die folgenden API-Aufrufe der Befehlsliste sind in Befehlslisten, die mit dem Typ erstellt wurden, nicht zulässig: D3D12 \_ COMMAND \_ LIST TYPE \_ \_ BUNDLE:

-   Beliebige Clear-Methode
-   Beliebige Copy-Methode
-   [**DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
-   [**ExecuteBundle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle)
-   [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)
-   [**ResolveSubresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
-   [**SetPredication**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)
-   [**BeginQuery**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery)
-   [**EndQuery**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)
-   [**SOSetTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets)
-   [**OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)
-   [**RSSetViewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports)
-   [**RSSetScissorRects**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)

[**SetDescriptorHeaps**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) kann für ein Paket aufgerufen werden, aber die Bundledeskriptorheaps müssen mit dem aufrufenden Befehlslistendeskriptorheap übereinstimmen.

Wenn eine dieser APIs für ein Paket aufgerufen wird, wird der Aufruf von der Runtime nicht mehr ausgeführt. Die Debugebene gibt bei jedem Auftreten einen Fehler aus.

## <a name="related-topics"></a>Zugehörige Themen

[Arbeitsübermittlung in Direct3D 12](command-queues-and-command-lists.md)