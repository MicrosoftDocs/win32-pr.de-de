---
title: Erstellen und Aufzeichnen von Befehlslisten und Paketen
description: In diesem Thema wird das Aufzeichnen von Befehlslisten und Paketen in Direct3D 12-apps beschrieben. Mit Befehlslisten und-Paketen können Sie sowohl Zeichnungs-als auch Zustands ändernde Aufrufe für die spätere Ausführung auf der GPU (Graphics Processing Unit) aufzeichnen.
ms.assetid: 0074B796-33A4-4AA1-A4E7-48A2A63F25B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ef2b54138cf3a08b85e3e8cc31f97cbe66abf6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548715"
---
# <a name="creating-and-recording-command-lists-and-bundles"></a>Erstellen und Aufzeichnen von Befehlslisten und Paketen

In diesem Thema wird das Aufzeichnen von Befehlslisten und Paketen in Direct3D 12-apps beschrieben. Mit Befehlslisten und-Paketen können Sie sowohl Zeichnungs-als auch Zustands ändernde Aufrufe für die spätere Ausführung auf der GPU (Graphics Processing Unit) aufzeichnen.

Über Befehlslisten hinaus nutzt die API Funktionen, die in GPU-Hardware vorhanden sind, indem Sie eine zweite Ebene von Befehlslisten hinzufügt, die als *Bündel* bezeichnet werden. Der Zweck von Paketen besteht darin, dass apps eine kleine Anzahl von API-Befehlen zur späteren Ausführung gruppieren können. Zum Zeitpunkt der Paket Erstellung führt der Treiber so viele Vorverarbeitungs Vorgänge aus, wie es möglich ist, diese zu einem späteren Zeitpunkt zu nutzen. Bündel sind so konzipiert, dass Sie beliebig oft verwendet und wieder verwendet werden. Befehlslisten werden hingegen in der Regel nur ein einziges Mal ausgeführt. Eine Befehlsliste *kann* jedoch mehrmals ausgeführt werden (vorausgesetzt, die Anwendung stellt sicher, dass die vorherigen Ausführungen abgeschlossen sind, bevor neue Ausführungen übermittelt werden).

In der Regel wird der Aufbau von API-Aufrufen in Paketen sowie API-Aufrufe und-Bündel in Befehlslisten und Befehlslisten in einem einzelnen Frame veranschaulicht. dabei wird die Wiederverwendung von **Bundle 1** in der **Befehlsliste 1** und in der **Befehlsliste 2** aufgezeigt, und die API-Methodennamen im Diagramm sind ebenso wie Beispiele. es können viele verschiedene API-Aufrufe verwendet werden.

![aufbauen von Befehlen, Paketen und Befehlslisten in Frames](images/gpu-workitems.png)

Es gibt unterschiedliche Einschränkungen für das Erstellen und Ausführen von Paketen und direkten Befehlslisten. diese Unterschiede werden in diesem Thema erläutert.

## <a name="creating-command-lists"></a>Erstellen von Befehlslisten

Direkte Befehlslisten und Bündel werden durch Aufrufen von [**ID3D12Device:: createcommandlist**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) oder [**ID3D12Device4:: CreateCommandList1**](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-createcommandlist1)erstellt.

Verwenden Sie [**ID3D12Device4:: CreateCommandList1**](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-createcommandlist1) , um eine geschlossene Befehlsliste zu erstellen, anstatt eine neue Liste zu erstellen und sofort zu schließen. Dadurch wird die Ineffizienz der Erstellung einer Liste mit einer Zuweisung und PSO vermieden, ohne Sie zu verwenden.

[**ID3D12Device:: kreatecommandlist**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) übernimmt die folgenden Parameter als Eingabe:

### <a name="d3d12_command_list_type"></a>D3D12 \_ - \_ Befehls \_ Auflistungstyp

Die [**D3D12 \_ Command \_ List \_ Type**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) -Enumeration gibt den Typ der Befehlsliste an, die erstellt wird. Dabei kann es sich um eine direkte Befehlsliste, ein Bündel, eine COMPUTE-Befehlsliste oder eine Kopier Befehlsliste handeln.

### <a name="id3d12commandallocator"></a>ID3D12CommandAllocator

Mit einer Befehls Zuweisung kann die APP den Arbeitsspeicher verwalten, der den Befehlslisten zugeordnet ist. Die Befehls Zuweisung wird durch Aufrufen von [**createcommandzucator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)erstellt. Beim Erstellen einer Befehlsliste muss der Befehls Listentyp der durch den [**D3D12- \_ Befehls \_ \_ Listentyp**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)angegebenen Zuweisung mit dem Typ der zu erstellenden Befehlsliste identisch sein. Eine angegebene Zuweisung kann nicht mehr als einer *aktuell* Auflistungs Befehlsliste zugeordnet werden, obwohl ein Befehls Zuweiser verwendet werden kann, um eine beliebige Anzahl von [**graphicscommandlist**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) -Objekten zu erstellen.

Um den von einer Befehls Zuweisung zugewiesenen Arbeitsspeicher freizugeben, ruft eine APP [**ID3D12CommandAllocator:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)auf. Dadurch kann die Zuweisung für neue Kommas wieder verwendet werden, aber die zugrunde liegende Größe wird nicht verringert. Aber bevor Sie dies tun, muss die APP sicherstellen, dass die GPU keine Befehlslisten ausführt, die mit der Zuweisung verknüpft sind. Andernfalls schlägt der-Befehl fehl. Beachten Sie außerdem, dass diese API nicht freigegeben ist und daher nicht gleichzeitig in mehreren Threads für denselben Zuweiser aufgerufen werden kann.

### <a name="id3d12pipelinestate"></a>ID3D12PipelineState

Der anfängliche Pipeline Status für die Befehlsliste. In Microsoft Direct3D 12 wird der größte Grafik Pipeline Status in einer Befehlsliste mit dem [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) -Objekt festgelegt. Eine App erstellt eine große Anzahl von diesen (in der Regel während der APP-Initialisierung), und anschließend wird der Status aktualisiert, indem das aktuell gebundene Zustands Objekt mithilfe von [**ID3D12GraphicsCommandList:: setpipelinestate**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)geändert wird. Weitere Informationen zu Pipeline Zustands Objekten finden Sie unter [Verwalten des Grafik Pipeline Zustands in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).

Beachten Sie, dass Pakete nicht den Pipeline Status erben, der durch vorherige Aufrufe in direkten Befehlslisten festgelegt wurde, die ihre übergeordneten Elemente sind

Wenn dieser Parameter NULL ist, wird ein Standardstatus verwendet.

## <a name="recording-command-lists"></a>Aufzeichnen von Befehlslisten

Unmittelbar nach der Erstellung befinden sich die Befehlslisten im Aufzeichnungs Zustand. Sie können auch eine vorhandene Befehlsliste wieder verwenden, indem Sie I [**D3D12GraphicsCommandList:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)aufrufen, wodurch auch die Befehlsliste im Aufzeichnungsstatus belassen wird. Anders als [**ID3D12CommandAllocator:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)können Sie **Reset** aufzurufen, während die Befehlsliste noch ausgeführt wird. Ein typisches Muster besteht darin, eine Befehlsliste zu übermitteln und Sie dann sofort zurückzusetzen, um den zugeordneten Arbeitsspeicher für eine andere Befehlsliste wiederzuverwenden. Beachten Sie, dass sich nur eine Befehlsliste, die den einzelnen Befehls Zuordnungen zugeordnet ist, gleichzeitig in einem Aufzeichnungs Zustand befinden kann.

Sobald sich eine Befehlsliste im Aufzeichnungs Zustand befindet, werden einfach Methoden der [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) -Schnittstelle aufgerufen, um der Liste Befehle hinzuzufügen. Viele dieser Methoden ermöglichen allgemeine Direct3D-Funktionen, die Microsoft Direct3D 11-Entwicklern vertraut werden. andere APIs sind für Direct3D 12 neu.

Nachdem Sie der Befehlsliste Befehle hinzugefügt haben, übertragen Sie die Befehlsliste aus dem Aufzeichnungs Zustand, indem Sie [**Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)aufrufen.

Befehls Zuweisungen können vergrößert werden, aber nicht Verkleinerungs Pooling und Wiederverwendung von Zuweisungen sollten berücksichtigt werden, um die Effizienz Ihrer APP zu maximieren. Sie können mehrere Listen in derselben Zuweisung aufzeichnen, bevor Sie zurückgesetzt werden, sofern nur eine Liste gleichzeitig zu einer bestimmten Zuweisung aufgezeichnet wird. Sie können jede Liste als Besitzer eines Teils der Zuweisung visualisieren, der angibt, welche [**ID3D12CommandQueue:: executecommandlists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) ausgeführt werden.

Eine einfache Zuweisungs Pooling-Strategie sollte auf ungefähr `numCommandLists * MaxFrameLatency` Zuordnungen abzielen. Wenn Sie z. b. 6 Listen aufzeichnen und bis zu 3 latente Frames zulassen, können Sie 18-20 Zuordnungen erwarten. Eine erweiterte Pooling-Strategie, die Zuweisungen für mehrere Listen im gleichen Thread wieder verwendet, kann auf `numRecordingThreads * MaxFrameLatency` Zuweisungen abzielen. Wenn im vorherigen Beispiel 2 Listen in Thread a, 2 in Thread B, 1 in Thread C und 1 in Thread D aufgezeichnet wurden, können Sie für 12-14-Zuweisungen realistischerweise als Ziel verwenden.

Verwenden Sie einen Fence, um zu bestimmen, wann eine bestimmte Zuweisung wieder verwendet werden kann.

Da Befehlslisten sofort nach der Ausführung zurückgesetzt werden können, können Sie in einem Pool zusammengefasst werden und nach jedem Aufrufen von [**ID3D12CommandQueue:: executecommandlists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)wieder dem Pool hinzugefügt werden.

## <a name="example"></a>Beispiel

Die folgenden Code Ausschnitte veranschaulichen das Erstellen und Aufzeichnen einer Befehlsliste. Beachten Sie, dass dieses Beispiel die folgenden Direct3D 12-Funktionen enthält:

-   Pipeline Zustands Objekte: Diese werden verwendet, um die meisten Zustandsparameter der Rendering-Pipeline innerhalb einer Befehlsliste festzulegen. Weitere Informationen finden Sie unter [Verwalten des Grafik Pipeline Zustands in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).
-   Deskriptorheap: Apps verwenden deskriptorheaps, um die Pipeline Bindung an Speicherressourcen zu verwalten.
-   Ressourcen Barriere: Dies wird verwendet, um den Übergang von Ressourcen von einem Zustand in einen anderen zu verwalten, z. b. von einer renderzielansicht zu einer shaderressourcenansicht. Weitere Informationen finden Sie unter [Verwenden von Ressourcen Barrieren zum Synchronisieren von Ressourcen Zuständen](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).

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



Nachdem eine Befehlsliste erstellt und aufgezeichnet wurde, kann Sie mithilfe einer Befehls Warteschlange ausgeführt werden. Weitere Informationen finden Sie unter [ausführen und Synchronisieren von Befehlslisten](executing-and-synchronizing-command-lists.md).

## <a name="reference-counting"></a>Verweisanzahl

Die meisten D3D12-APIs verwenden weiterhin die Verweis Zählung nach com-Konventionen. Eine wichtige Ausnahme sind die APIs der D3D12-Grafik Befehlsliste. Alle APIs auf [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) enthalten keine Verweise auf die Objekte, die an diese APIs weitergeleitet werden. Dies bedeutet, dass Anwendungen dafür verantwortlich sind, dass eine Befehlsliste nie zur Ausführung übermittelt wird, die auf eine zerstörte Ressource verweist.

## <a name="command-list-errors"></a>Befehlslisten Fehler

Bei den meisten APIs auf [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) werden keine Fehler zurückgegeben. Fehler, die während der Erstellung der Befehlsliste aufgetreten sind, werden bis [**ID3D12GraphicsCommandList:: Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)verzögert. Die einzige Ausnahme besteht darin, dass das DXGI- \_ Fehler \_ Gerät \_ entfernt wurde, das noch weiter zurückgestellt wird. Beachten Sie, dass sich dies von D3D11 unterscheidet, bei der viele Parameter Validierungs Fehler automatisch gelöscht und nie an den Aufrufer zurückgegeben werden.

Anwendungen können \_ in den folgenden API-aufrufen erwarten, dass DXGI-Geräte \_ Fehler entfernt wurden:

-   Beliebige Ressourcen Erstellungs Methode
-   [**ID3D12Resource:: map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)
-   [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)
-   [**Getdeviceremovedreason**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)

## <a name="command-list-api-restrictions"></a>Einschränkungen der Befehlslisten-API

Einige Befehlslisten-APIs können nur für bestimmte Typen von Befehlslisten aufgerufen werden. Die folgende Tabelle zeigt, welche Befehlslisten-APIs für die einzelnen Befehlslisten Typen gültig sind. Außerdem wird gezeigt, welche APIs zum aufzurufen in einem [**D3D12-renderdurchlauf**](./direct3d-12-render-passes.md)gültig sind. 

| API-Name                                         | Grafiken | Compute | Kopieren | Bundle | In renderdurchlauf |
|--------------------------------------------------|:--------:|:-------:|:----:|:------:|:--------------:|
| Atomiccopybufferuint                             | ✓        | ✓       | ✓    |        |                |
| AtomicCopyBufferUINT64                           | ✓        | ✓       | ✓    |        |                |
| Beginquery                                       | ✓        |         |      |        | ✓              |
| Beginrenderpass                                  | ✓        |         |      |        |                |
| Buildraytracingaccelerationstructure             | ✓        | ✓       |      |        |                |
| ClearDepthStencilView                            | ✓        |         |      |        |                |
| ClearRenderTargetView                            | ✓        |         |      |        |                |
| Clearstate                                       | ✓        | ✓       |      |        |                |
| Clearunorderedaccessviewfloat                    | ✓        | ✓       |      |        |                |
| Clearunorderedaccessviewuint                     | ✓        | ✓       |      |        |                |
| Copybufferregion                                 | ✓        | ✓       | ✓    |        |                |
| Copyraytracingaccelerationstructure              | ✓        | ✓       |      |        |                |
| Copyresource                                     | ✓        | ✓       | ✓    |        |                |
| Copytextureregion                                | ✓        | ✓       | ✓    |        |                |
| Copytiles                                        | ✓        | ✓       | ✓    |        |                |
| Verwerfen von Quelle                                  | ✓        | ✓       |      |        |                |
| Dispatch                                         | ✓        | ✓       |      | ✓      |                |
| Dispatchrays                                     | ✓        | ✓       |      | ✓      |                |
| Drawindexedinstangeleitet                             | ✓        |         |      | ✓      | ✓              |
| Drawinstanzierte                                    | ✓        |         |      | ✓      | ✓              |
| Emitraytracingaccelerationstructurepostbuildinfo | ✓        | ✓       |      |        |                |
| Endquery                                         | ✓        | ✓       | ✓    |        | ✓              |
| Endrenderpass                                    | ✓        |         |      |        | ✓              |
| Executebundle                                    | ✓        |         |      |        | ✓              |
| Executin Direct                                  | ✓        | ✓       |      | ✓      | ✓              |
| Executemetacommand                               | ✓        | ✓       |      |        |                |
| Iasetindexbuffer                                 | ✓        |         |      | ✓      | ✓              |
| Iasetprimitivetopology                           | ✓        |         |      | ✓      | ✓              |
| Iasetvertexbuffers                               | ✓        |         |      | ✓      | ✓              |
| Initializemetacommand                            | ✓        | ✓       |      |        |                |
| Omsetblendfactor                                 | ✓        |         |      | ✓      | ✓              |
| Omsetdepthbounds                                 | ✓        |         |      | ✓      | ✓              |
| Omantrendertargets                               | ✓        |         |      |        |                |
| Omsetstencilref                                  | ✓        |         |      | ✓      | ✓              |
| Resolvequerydata                                 | ✓        | ✓       | ✓    |        |                |
| Resolvesubresource                               | ✓        |         |      |        |                |
| Resolvesubresourceregion                         | ✓        |         |      |        |                |
| Resourcebarrier                                  | ✓        | ✓       | ✓    |        | ✓              |
| Rssezcissorrects                                | ✓        |         |      |        | ✓              |
| Rssetshadingrate                                 | ✓        |         |      | ✓      | ✓              |
| Rssetshadingrateimage                            | ✓        |         |      | ✓      | ✓              |
| Rssetviewports                                   | ✓        |         |      |        | ✓              |
| SetComputeRoot32BitConstant                      | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRoot32BitConstants                     | ✓        | ✓       |      | ✓      | ✓              |
| Setcomputerootconstantbufferview                 | ✓        | ✓       |      | ✓      | ✓              |
| Setcomputerootdescriptor Table                    | ✓        | ✓       |      | ✓      | ✓              |
| Setcomputerootshaderresourceview                 | ✓        | ✓       |      | ✓      | ✓              |
| Setcomputerootsignature                          | ✓        | ✓       |      | ✓      | ✓              |
| Setcomputerootunorderedaccessview                | ✓        | ✓       |      | ✓      | ✓              |
| Setdescriptorheaps                               | ✓        | ✓       |      | ✓      | ✓              |
| SetGraphicsRoot32BitConstant                     | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRoot32BitConstants                    | ✓        |         |      | ✓      | ✓              |
| Setgraphicsrootconstantbufferview                | ✓        |         |      | ✓      | ✓              |
| Setgraphicsrootdescriptor Table                   | ✓        |         |      | ✓      | ✓              |
| Setgraphicsrootshaderresourceview                | ✓        |         |      | ✓      | ✓              |
| Setgraphicsrootsignature                         | ✓        |         |      | ✓      | ✓              |
| Setgraphicsrootunorderedaccessview               | ✓        |         |      | ✓      | ✓              |
| Setpipelinestate                                 | ✓        | ✓       |      | ✓      | ✓              |
| SetPipelineState1                                | ✓        | ✓       |      | ✓      |                |
| Setprediation                                   | ✓        | ✓       |      |        | ✓              |
| Setprotectedresourcesession                      | ✓        | ✓       | ✓    |        |                |
| Setsamplepositions                               | ✓        |         |      | ✓      | ✓              |
| Setviewinstancemask                              | ✓        |         |      | ✓      | ✓              |
| Sosettargets                                     | ✓        |         |      |        | ✓              |
| Schreibbufferimmediate                             | ✓        | ✓       | ✓    | ✓      | ✓              |

## <a name="bundle-restrictions"></a>Bündel Einschränkungen

Mithilfe von Einschränkungen können Direct3D 12-Treiber den größten Teil der Arbeit, die Paketen zugeordnet ist, zum Zeitpunkt der Aufzeichnung ausführen, sodass die [**executebundle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) -API mit geringem Verwaltungsaufwand ausgeführt werden kann. Alle Pipeline Zustands Objekte, auf die von einem Paket verwiesen wird, müssen die gleichen renderzielformate, das tiefe Puffer Format und Beispiel Beschreibungen aufweisen.

Die folgenden Befehlslisten-API-Aufrufe sind in Befehlslisten, die mit dem Typ: D3D12 \_ Command \_ List \_ Type Bundle erstellt wurden, nicht zulässig \_ :

-   Beliebige Clear-Methode
-   Beliebige Kopiermethode
-   [**Verwerfen von Quelle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
-   [**Executebundle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle)
-   [**Resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)
-   [**Resolvesubresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
-   [**Setprediation**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)
-   [**Beginquery**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery)
-   [**Endquery**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)
-   [**Sosettargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets)
-   [**Omantrendertargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)
-   [**Rssetviewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports)
-   [**Rssezcissorrects**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)

[**Setdescriptorheaps**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) kann für ein Bündel aufgerufen werden, aber die Bündel deskriptorheaps müssen dem aufrufenden Befehlslisten deskriptorheap entsprechen.

Wenn eine dieser APIs für ein Bündel aufgerufen wird, löscht die Laufzeit den Aufruf. Die debugschicht gibt einen Fehler aus, wenn dies auftritt.

## <a name="related-topics"></a>Verwandte Themen

[Arbeits Übermittlung in Direct3D 12](command-queues-and-command-lists.md)