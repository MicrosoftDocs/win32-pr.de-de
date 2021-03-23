---
title: N-Text-Schwerkraft Simulation mit mehreren Modulen
description: Das D3D12nBodyGravity-Beispiel veranschaulicht, wie Compute-Arbeit asynchron ausgeführt wird.
ms.assetid: B20C5575-0616-43F7-9AC9-5F802E5597B5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60782519de6f655882717c4ea657668129a6ce3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548661"
---
# <a name="multi-engine-n-body-gravity-simulation"></a>N-Text-Schwerkraft Simulation mit mehreren Modulen

Das **D3D12nBodyGravity** -Beispiel veranschaulicht, wie Compute-Arbeit asynchron ausgeführt wird. Das Beispiel startet eine Reihe von Threads, die jeweils über eine COMPUTE-Befehls Warteschlange verfügen, und plant Compute-Arbeit auf der GPU, die eine n-Text-Schwerkraft Simulation ausführt. Jeder Thread arbeitet mit zwei Puffer, die sich aus der Position und den Geschwindigkeitsdaten zusammen befinden. Bei jeder Iterationen liest der COMPUTE-Shader die aktuellen Positions-und Geschwindigkeitsdaten aus einem Puffer und schreibt die nächste Iterationen in den anderen Puffer. Wenn die Iterationen abgeschlossen sind, tauscht der COMPUTE-Shader aus, welcher Puffer der SRV zum Lesen von Positions-/Velocity-Daten ist. dabei handelt es sich um die UAV zum Schreiben von Positions-/Velocity-Updates durch Ändern des Ressourcen Zustands für jeden Puffer.

-   [Erstellen der Stamm Signaturen](#create-the-root-signatures)
-   [Erstellen der SRV-und UAV-Puffer](#create-the-srv-and-uav-buffers)
-   [Erstellen der CBV-und Vertex-Puffer](#create-the-cbv-and-vertex-buffers)
-   [Synchronisieren der Rendering-und Compute-Threads](#synchronize-the-rendering-and-compute-threads)
-   [Ausführen des Beispiels](#run-the-sample)
-   [Verwandte Themen](#related-topics)

## <a name="create-the-root-signatures"></a>Erstellen der Stamm Signaturen

Wir beginnen damit, in der **loadassets** -Methode sowohl eine Grafik als auch eine COMPUTE-Stamm Signatur zu erstellen. Beide Stamm Signaturen haben eine CBV (root Constant Buffer View) und eine Tabelle der Tabelle "Shader Resource View" (SRV). Die COMPUTE-Stamm Signatur verfügt auch über eine benutzerdefinierte UAV-Deskriptortabelle (ungeordnete Zugriffs Ansicht).

``` syntax
 // Create the root signatures.
       {
              CD3DX12_DESCRIPTOR_RANGE ranges[2];
              ranges[0].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SRV, 1, 0);
              ranges[1].Init(D3D12_DESCRIPTOR_RANGE_TYPE_UAV, 1, 0);

              CD3DX12_ROOT_PARAMETER rootParameters[RootParametersCount];
              rootParameters[RootParameterCB].InitAsConstantBufferView(0, 0, D3D12_SHADER_VISIBILITY_ALL);
              rootParameters[RootParameterSRV].InitAsDescriptorTable(1, &ranges[0], D3D12_SHADER_VISIBILITY_VERTEX);
              rootParameters[RootParameterUAV].InitAsDescriptorTable(1, &ranges[1], D3D12_SHADER_VISIBILITY_ALL);

              // The rendering pipeline does not need the UAV parameter.
              CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
              rootSignatureDesc.Init(_countof(rootParameters) - 1, rootParameters, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

              ComPtr<ID3DBlob> signature;
              ComPtr<ID3DBlob> error;
              ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
              ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));

              // Create compute signature. Must change visibility for the SRV.
              rootParameters[RootParameterSRV].ShaderVisibility = D3D12_SHADER_VISIBILITY_ALL;

              CD3DX12_ROOT_SIGNATURE_DESC computeRootSignatureDesc(_countof(rootParameters), rootParameters, 0, nullptr);
              ThrowIfFailed(D3D12SerializeRootSignature(&computeRootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));

              ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_computeRootSignature)));
       }
```



| Aufruffluss                                                             | Parameter                                                            |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**CD3DX12- \_ \_ Deskriptorbereich**](cd3dx12-descriptor-range.md)        | [**D3D12- \_ \_ deskriptorbereichstyp \_**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) |
| [**CD3DX12 \_ root- \_ Parameter**](cd3dx12-root-parameter.md)            | [**D3D12- \_ Shader- \_ Sichtbarkeit**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [**CD3DX12 \_ Stamm \_ Signatur \_ DESC**](cd3dx12-root-signature-desc.md) | [**D3D12 \_ root \_ Signature- \_ Flags**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))                                   |                                                                       |
| [**D3D12SerializeRootSignature**](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [**D3D \_ Stamm \_ Signatur \_ Version**](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [**"Kreaterootsignature"**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |
| [**CD3DX12 \_ Stamm \_ Signatur \_ DESC**](cd3dx12-root-signature-desc.md) |                                                                       |
| [**D3D12SerializeRootSignature**](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [**D3D \_ Stamm \_ Signatur \_ Version**](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [**"Kreaterootsignature"**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |



 

## <a name="create-the-srv-and-uav-buffers"></a>Erstellen der SRV-und UAV-Puffer

Die SRV-und UAV-Puffer bestehen aus einem Array von Positions-und Geschwindigkeitsdaten.

``` syntax
 // Position and velocity data for the particles in the system.
       // Two buffers full of Particle data are utilized in this sample.
       // The compute thread alternates writing to each of them.
       // The render thread renders using the buffer that is not currently
       // in use by the compute shader.
       struct Particle
       {
              XMFLOAT4 position;
              XMFLOAT4 velocity;
       };
```



| Aufruffluss                       | Parameter |
|---------------------------------|------------|
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) |            |



 

## <a name="create-the-cbv-and-vertex-buffers"></a>Erstellen der CBV-und Vertex-Puffer

Bei der Grafik Pipeline ist die CBV eine **Struktur** , die zwei Matrizen enthält, die vom Geometry-Shader verwendet werden. Der Geometry-Shader nimmt die Position jedes Partikels im System an und generiert ein Vierfach, um es mithilfe dieser Matrizen darzustellen.

``` syntax
 struct ConstantBufferGS
       {
              XMMATRIX worldViewProjection;
              XMMATRIX inverseView;

              // Constant buffers are 256-byte aligned in GPU memory. Padding is added
              // for convenience when computing the struct's size.
              float padding[32];
       };
```



| Aufruffluss                       | Parameter |
|---------------------------------|------------|
| [**Xmmatrix**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) |            |



 

Folglich enthält der Vertex-Puffer, der vom Vertex-Shader verwendet wird, keine Positionsdaten.

``` syntax
 // "Vertex" definition for particles. Triangle vertices are generated 
       // by the geometry shader. Color data will be assigned to those 
       // vertices via this struct.
       struct ParticleVertex
       {
              XMFLOAT4 color;
       };
```



| Aufruffluss                       | Parameter |
|---------------------------------|------------|
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) |            |



 

Bei der COMPUTE-Pipeline ist die CBV eine **Struktur** , die einige Konstanten enthält, die von der n-Text-Gravitations Simulation im COMPUTE-Shader verwendet werden.

``` syntax
 struct ConstantBufferCS
       {
              UINT param[4];
              float paramf[4];
       };
```

## <a name="synchronize-the-rendering-and-compute-threads"></a>Synchronisieren der Rendering-und Compute-Threads

Nachdem alle Puffer initialisiert wurden, werden das Rendering und die Compute-Arbeit gestartet. Der computethread ändert den Status der beiden Positions-/Velocity-Puffer zwischen SRV und UAV, während er die Simulation durchläuft, und der Renderingthread muss sicherstellen, dass er die Arbeit an der Grafik Pipeline plant, die auf dem SRV ausgeführt wird. Mithilfe von Zäunen wird der Zugriff auf die beiden Puffer synchronisiert.

Im Renderthread:

``` syntax
// Render the scene.
void D3D12nBodyGravity::OnRender()
{
       // Let the compute thread know that a new frame is being rendered.
       for (int n = 0; n < ThreadCount; n++)
       {
              InterlockedExchange(&m_renderContextFenceValues[n], m_renderContextFenceValue);
       }

       // Compute work must be completed before the frame can render or else the SRV 
       // will be in the wrong state.
       for (UINT n = 0; n < ThreadCount; n++)
       {
              UINT64 threadFenceValue = InterlockedGetValue(&m_threadFenceValues[n]);
              if (m_threadFences[n]->GetCompletedValue() < threadFenceValue)
              {
                     // Instruct the rendering command queue to wait for the current 
                     // compute work to complete.
                     ThrowIfFailed(m_commandQueue->Wait(m_threadFences[n].Get(), threadFenceValue));
              }
       }

       // Record all the commands we need to render the scene into the command list.
       PopulateCommandList();

       // Execute the command list.
       ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
       m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

       // Present the frame.
       ThrowIfFailed(m_swapChain->Present(0, 0));

       MoveToNextFrame();
}
```



| Aufruffluss                                                              | Parameter |
|------------------------------------------------------------------------|------------|
| [**InterlockedExchange**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedexchange)                  |            |
| [**Interlockedgetvalue**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)           |            |
| [**Getcompletedvalue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)             |            |
| [**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                                |            |
| [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)                         |            |
| [**Executecommandlists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)  |            |
| [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) |            |



 

Um das Beispiel etwas zu vereinfachen, wartet der computethread, bis die GPU jede Iterationen abschließt, bevor eine weitere computearbeit geplant wird. In der Praxis möchten Anwendungen wahrscheinlich die computewarteschlange vollständig aufbewahren, um eine maximale Leistung von der GPU zu erzielen.

Im COMPUTE-Thread:

``` syntax
DWORD D3D12nBodyGravity::AsyncComputeThreadProc(int threadIndex)
{
       ID3D12CommandQueue* pCommandQueue = m_computeCommandQueue[threadIndex].Get();
       ID3D12CommandAllocator* pCommandAllocator = m_computeAllocator[threadIndex].Get();
       ID3D12GraphicsCommandList* pCommandList = m_computeCommandList[threadIndex].Get();
       ID3D12Fence* pFence = m_threadFences[threadIndex].Get();

       while (0 == InterlockedGetValue(&m_terminating))
       {
              // Run the particle simulation.
              Simulate(threadIndex);

              // Close and execute the command list.
              ThrowIfFailed(pCommandList->Close());
              ID3D12CommandList* ppCommandLists[] = { pCommandList };

              pCommandQueue->ExecuteCommandLists(1, ppCommandLists);

              // Wait for the compute shader to complete the simulation.
              UINT64 threadFenceValue = InterlockedIncrement(&m_threadFenceValues[threadIndex]);
              ThrowIfFailed(pCommandQueue->Signal(pFence, threadFenceValue));
              ThrowIfFailed(pFence->SetEventOnCompletion(threadFenceValue, m_threadFenceEvents[threadIndex]));
              WaitForSingleObject(m_threadFenceEvents[threadIndex], INFINITE);

              // Wait for the render thread to be done with the SRV so that
              // the next frame in the simulation can run.
              UINT64 renderContextFenceValue = InterlockedGetValue(&m_renderContextFenceValues[threadIndex]);
              if (m_renderContextFence->GetCompletedValue() < renderContextFenceValue)
              {
                     ThrowIfFailed(pCommandQueue->Wait(m_renderContextFence.Get(), renderContextFenceValue));
                     InterlockedExchange(&m_renderContextFenceValues[threadIndex], 0);
              }

              // Swap the indices to the SRV and UAV.
              m_srvIndex[threadIndex] = 1 - m_srvIndex[threadIndex];

              // Prepare for the next frame.
              ThrowIfFailed(pCommandAllocator->Reset());
              ThrowIfFailed(pCommandList->Reset(pCommandAllocator, m_computeState.Get()));
       }

       return 0;
}
```



| Aufruffluss                                                                   | Parameter |
|-----------------------------------------------------------------------------|------------|
| [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue)                            |            |
| [**ID3D12CommandAllocator**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator)                    |            |
| [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)              |            |
| [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)                                          |            |
| [**Interlockedgetvalue**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)                |            |
| [**Schließen**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)                            |            |
| [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)                              |            |
| [**Executecommandlists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)       |            |
| [**InterlockedIncrement**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedincrement)                     |            |
| [**Aussendet**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)                                 |            |
| [**"Abschlusventoncompletion"**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)            |            |
| [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)                         |            |
| [**Interlockedgetvalue**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)                |            |
| [**Getcompletedvalue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)                  |            |
| [**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                                     |            |
| [**InterlockedExchange**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedexchange)                       |            |
| [**ID3D12CommandAllocator:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)       |            |
| [**ID3D12GraphicsCommandList:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset) |            |



 

## <a name="run-the-sample"></a>Ausführen des Beispiels

![Screenshot der abschließenden n-Text Schwerpunkt Simulation](images/nbodygravity.png)

## <a name="related-topics"></a>Verwandte Themen

[D3D12-Code Exemplarische Vorgehensweisen](d3d12-code-walk-throughs.md)

[Multi-Engine-Synchronisierung](./user-mode-heap-synchronization.md)