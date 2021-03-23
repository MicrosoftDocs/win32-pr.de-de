---
title: Beispiel Code in der D3D12-Referenz
description: Erläutert die Verwendung von Beispielcode in der Direct3D 12-Dokumentation.
ms.assetid: C2323482-D06D-43B7-9BDE-BFB9A6A6B70D
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d65dd8db64dd829a7a318717e44a64ea189c7a3
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548645"
---
# <a name="example-code-in-the-d3d12-reference"></a>Beispiel Code in der D3D12-Referenz

Erläutert die Verwendung von Beispielcode in der Direct3D 12-Dokumentation.

-   [Code Ausschnitt Codebeispiel](#example-snippet-code)
-   [Verwandte Themen](#related-topics)

## <a name="example-snippet-code"></a>Code Ausschnitt Codebeispiel

Der Beispielcode, der in der Direct3D 12-Referenz gezeigt wird, ist nicht Kompilier-oder ausführbaren Code, sondern ein Code Ausschnitt, der ein Beispiel für den Aufruf der API bereitstellt. In einigen Beispielen werden die globalen Variablen und Klassenmember aufgelistet, die von den Aufrufen verwendet werden. Beispiel:

Globale Pipeline Objekte.


```C++
D3D12_VIEWPORT m_viewport;
D3D12_RECT m_scissorRect;
ComPtr<IDXGISwapChain3> m_swapChain;
ComPtr<ID3D12Device> m_device;
ComPtr<ID3D12Resource> m_renderTargets[FrameCount];
ComPtr<ID3D12CommandAllocator> m_commandAllocator;
ComPtr<ID3D12CommandQueue> m_commandQueue;
ComPtr<ID3D12RootSignature> m_rootSignature;
ComPtr<ID3D12DescriptorHeap> m_rtvHeap;
ComPtr<ID3D12PipelineState> m_pipelineState;
ComPtr<ID3D12GraphicsCommandList> m_commandList;
UINT m_rtvDescriptorSize;
```



Auffüllen von Befehlslisten.


```C++
// Command list allocators can only be reset when the associated 
// command lists have finished execution on the GPU; apps should use 
// fences to determine GPU execution progress.
ThrowIfFailed(m_commandAllocator->Reset());

// However, when ExecuteCommandList() is called on a particular command 
// list, that command list can then be reset at any time and must be before 
// re-recording.
ThrowIfFailed(m_commandList->Reset(m_commandAllocator.Get(), m_pipelineState.Get()));

// Set necessary state.
m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());
m_commandList->RSSetViewports(1, &m_viewport);
m_commandList->RSSetScissorRects(1, &m_scissorRect);

// Indicate that the back buffer will be used as a render target.
auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET);
m_commandList->ResourceBarrier(1, &barrier);

CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, nullptr);

// Record commands.
const float clearColor[] = { 0.0f, 0.2f, 0.4f, 1.0f };
m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST);
m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);
m_commandList->DrawInstanced(3, 1, 0, 0);

// Indicate that the back buffer will now be used to present.
m_commandList->ResourceBarrier(1, &barrier);
barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT);
ThrowIfFailed(m_commandList->Close());
```



## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Erstellen einer einfachen Direct3D 12-Komponente](creating-a-basic-direct3d-12-component.md)
</dt> <dt>

[Direct3D 12-Referenz](direct3d-12-reference.md)
</dt> <dt>

[D3D12-Code Exemplarische Vorgehensweisen](d3d12-code-walk-throughs.md)
</dt> <dt>

[Funktionierende Beispiele](working-samples.md)
</dt> </dl>

 

 




