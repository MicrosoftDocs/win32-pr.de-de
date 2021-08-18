---
title: N-Körper-Schwerkraftsimulation mit mehreren Modulen
description: Das Beispiel D3D12nBody Ctity veranschaulicht, wie Computearbeit asynchron ausgeführt wird.
ms.assetid: B20C5575-0616-43F7-9AC9-5F802E5597B5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da14e34bfc881e000eb4f4557a0dddef3cee3d0ab55343a9e5597a483af39adc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632044"
---
# <a name="multi-engine-n-body-gravity-simulation"></a>N-Körper-Schwerkraftsimulation mit mehreren Modulen

Das **Beispiel D3D12nBody Ctity** veranschaulicht, wie Computearbeit asynchron ausgeführt wird. Im Beispiel werden eine Reihe von Threads mit jeweils einer Computebefehlswarteschlange eingerichtet und Computearbeit auf der GPU geplant, die eine n-body-Schwerkraftsimulation ausführt. Jeder Thread arbeitet mit zwei Puffern mit Positions- und Geschwindigkeitsdaten. Bei jeder Iteration liest der Compute-Shader die aktuellen Positions- und Geschwindigkeitsdaten aus einem Puffer und schreibt die nächste Iteration in den anderen Puffer. Nach Abschluss der Iteration tauscht der Compute-Shader aus, welcher Puffer der SRV zum Lesen von Positions-/Geschwindigkeitsdaten ist und welcher UAV zum Schreiben von Positions-/Geschwindigkeitsaktualisierungen durch Ändern des Ressourcenzustands für jeden Puffer ist.

-   [Erstellen der Stammsignaturen](#create-the-root-signatures)
-   [Erstellen der SRV- und UAV-Puffer](#create-the-srv-and-uav-buffers)
-   [Erstellen der CBV- und Scheitelpunktpuffer](#create-the-cbv-and-vertex-buffers)
-   [Synchronisieren der Rendering- und Computethreads](#synchronize-the-rendering-and-compute-threads)
-   [Ausführen des Beispiels](#run-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="create-the-root-signatures"></a>Erstellen der Stammsignaturen

Zunächst erstellen wir sowohl eine Grafik als auch eine Computestammsignatur in der **LoadAssets-Methode.** Beide Stammsignaturen verfügen über eine Stammkonst constant buffer view (CBV) und eine Shader resource view (SRV)-Deskriptortabelle. Die Computestammsignatur verfügt auch über eine Unordered Access View (UAV)-Deskriptortabelle.

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



| Anruffluss                                                             | Parameter                                                            |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**\_CD3DX12-DESKRIPTORBEREICH \_**](cd3dx12-descriptor-range.md)        | [**\_D3D12-DESKRIPTORBEREICHSTYP \_ \_**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) |
| [**CD3DX12 \_ ROOT \_ PARAMETER**](cd3dx12-root-parameter.md)            | [**SICHTBARKEIT DES \_ D3D12-SHADERS \_**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [**CD3DX12 \_ ROOT \_ SIGNATURE \_ DESC**](cd3dx12-root-signature-desc.md) | [**D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))                                   |                                                                       |
| [**D3D12SerializeRootSignature**](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [**\_ \_ D3D-STAMMSIGNATURVERSION \_**](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [**CreateRootSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |
| [**CD3DX12 \_ ROOT \_ SIGNATURE \_ DESC**](cd3dx12-root-signature-desc.md) |                                                                       |
| [**D3D12SerializeRootSignature**](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [**\_ \_ D3D-STAMMSIGNATURVERSION \_**](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [**CreateRootSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |



 

## <a name="create-the-srv-and-uav-buffers"></a>Erstellen der SRV- und UAV-Puffer

Die SRV- und UAV-Puffer bestehen aus einem Array von Positions- und Geschwindigkeitsdaten.

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



| Anruffluss                       | Parameter |
|---------------------------------|------------|
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) |            |



 

## <a name="create-the-cbv-and-vertex-buffers"></a>Erstellen der CBV- und Scheitelpunktpuffer

Für die Grafikpipeline ist die CBV **eine** Struktur, die zwei Matrizen enthält, die vom Geometrie-Shader verwendet werden. Der Geometrie-Shader nimmt die Position jedes Partikels im System an und generiert ein Quader, um es mithilfe dieser Matrizen darstellen zu können.

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



| Anruffluss                       | Parameter |
|---------------------------------|------------|
| [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) |            |



 

Daher enthält der vom Vertex-Shader verwendete Scheitelpunktpuffer keine Positionsdaten.

``` syntax
 // "Vertex" definition for particles. Triangle vertices are generated 
       // by the geometry shader. Color data will be assigned to those 
       // vertices via this struct.
       struct ParticleVertex
       {
              XMFLOAT4 color;
       };
```



| Anruffluss                       | Parameter |
|---------------------------------|------------|
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) |            |



 

Für die Computepipeline ist  die CBV eine Struktur, die einige Konstanten enthält, die von der n-body-Schwerkraftsimulation im Compute-Shader verwendet werden.

``` syntax
 struct ConstantBufferCS
       {
              UINT param[4];
              float paramf[4];
       };
```

## <a name="synchronize-the-rendering-and-compute-threads"></a>Synchronisieren der Rendering- und Computethreads

Nachdem alle Puffer initialisiert wurden, beginnen die Rendering- und Computearbeit. Der Computethread ändert den Zustand der beiden Positions-/Geschwindigkeitspuffer zwischen SRV und UAV, während er die Simulation durch iteriert, und der Renderingthread muss sicherstellen, dass er die Arbeit an der Grafikpipeline geplant, die auf dem SRV ausgeführt wird. Fences werden verwendet, um den Zugriff auf die beiden Puffer zu synchronisieren.

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



| Anruffluss                                                              | Parameter |
|------------------------------------------------------------------------|------------|
| [**InterlockedExchange**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedexchange)                  |            |
| [**InterlockedGetValue**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)           |            |
| [**GetCompletedValue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)             |            |
| [**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                                |            |
| [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)                         |            |
| [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)  |            |
| [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) |            |



 

Um die Stichprobe etwas zu vereinfachen, wartet der Computethread, bis die GPU jede Iteration abgeschlossen hat, bevor weitere Computearbeit geplant wird. In der Praxis möchten Anwendungen die Computewarteschlange wahrscheinlich voll halten, um die maximale Leistung der GPU zu erzielen.

Im Computethread:

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



| Anruffluss                                                                   | Parameter |
|-----------------------------------------------------------------------------|------------|
| [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue)                            |            |
| [**ID3D12CommandAllocator**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator)                    |            |
| [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)              |            |
| [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)                                          |            |
| [**InterlockedGetValue**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)                |            |
| [**Schließen**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)                            |            |
| [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)                              |            |
| [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)       |            |
| [**InterlockedIncrement**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedincrement)                     |            |
| [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)                                 |            |
| [**SetEventOnCompletion**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)            |            |
| [**Waitforsingleobject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)                         |            |
| [**InterlockedGetValue**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)                |            |
| [**GetCompletedValue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)                  |            |
| [**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                                     |            |
| [**InterlockedExchange**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedexchange)                       |            |
| [**ID3D12CommandAllocator::Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)       |            |
| [**ID3D12GraphicsCommandList::Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset) |            |



 

## <a name="run-the-sample"></a>Ausführen des Beispiels

![Screenshot der endgültigen Simulation der Schwerkraft des n-Körpers](images/nbodygravity.png)

## <a name="related-topics"></a>Zugehörige Themen

[Exemplarische Vorgehensweisen zu D3D12-Code](d3d12-code-walk-throughs.md)

[Synchronisierung mit mehreren Modulen](./user-mode-heap-synchronization.md)