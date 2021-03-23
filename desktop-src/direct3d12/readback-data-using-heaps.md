---
title: Zurück Lesen von Daten über einen Puffer
description: Wenn Sie Daten aus der GPU zurück lesen möchten (z. b. um einen Screenshot aufzuzeichnen), verwenden Sie einen lesebackheap.
ms.assetid: 2F515B2C-3317-4AA8-81E1-7762ED895F77
ms.localizationpriority: high
ms.topic: article
ms.date: 12/17/2018
ms.openlocfilehash: 752d97d517a48a38adabc7c8fe51d11d47c1d8d3
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548717"
---
# <a name="read-back-data-via-a-buffer"></a>Zurück Lesen von Daten über einen Puffer

Wenn Sie Daten aus der GPU zurück lesen möchten (z. b. um einen Screenshot aufzuzeichnen), verwenden Sie einen lesebackheap. Diese Technik bezieht sich auf das [Hochladen von Textur Daten über einen Puffer](upload-and-readback-of-texture-data.md)mit wenigen unterschieden.

- Zum Lesen von Daten erstellen Sie einen Heap, bei dem die **D3D12_HEAP_TYPE** auf [D3D12_HEAP_TYPE_READBACK](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)festgelegt ist, anstatt auf **D3D12_HEAP_TYPE_UPLOAD**.
- Die Ressource auf dem Read-Back-Heap muss immer ein **D3D12_RESOURCE_DIMENSION_BUFFER** sein.
- Sie verwenden einen Fence, um zu erkennen, wann die GPU die Verarbeitung eines Frames abgeschlossen hat (wenn das Schreiben von Daten in den Ausgabepuffer abgeschlossen ist). Dies ist wichtig, da die [**ID3D12Resource:: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) -Methode nicht mit der GPU synchronisiert wird ( *umgekehrt wird die Entsprechung* von Direct3D 11 synchronisiert). Direct3D 12  Zuordnungs Aufrufe Verhalten sich so, als hätten Sie die Direct3D 11-Entsprechung mit dem NO_OVERWRITE-Flag aufgerufen.
- Nachdem die Daten bereit sind (einschließlich der erforderlichen Ressourcen Barriere), müssen Sie [**ID3D12Resource:: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) anrufen, um die Daten für die Daten der CPU sichtbar zu machen.

## <a name="code-example"></a>Codebeispiel

Das folgende Codebeispiel zeigt den allgemeinen Überblick über das Lesen von Daten aus der GPU zur CPU über einen Puffer.

```cppwinrt

// The output buffer (created below) is on a default heap, so only the GPU can access it.

D3D12_HEAP_PROPERTIES defaultHeapProperties{ CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT) };
D3D12_RESOURCE_DESC outputBufferDesc{ CD3DX12_RESOURCE_DESC::Buffer(outputBufferSize, D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS) };
winrt::com_ptr<::ID3D12Resource> outputBuffer;
winrt::check_hresult(d3d12Device->CreateCommittedResource(
    &defaultHeapProperties,
    D3D12_HEAP_FLAG_NONE,
    &outputBufferDesc,
    D3D12_RESOURCE_STATE_COPY_DEST,
    nullptr,
    __uuidof(outputBuffer),
    outputBuffer.put_void()));

// The readback buffer (created below) is on a readback heap, so that the CPU can access it.

D3D12_HEAP_PROPERTIES readbackHeapProperties{ CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_READBACK) };
D3D12_RESOURCE_DESC readbackBufferDesc{ CD3DX12_RESOURCE_DESC::Buffer(outputBufferSize) };
winrt::com_ptr<::ID3D12Resource> readbackBuffer;
winrt::check_hresult(d3d12Device->CreateCommittedResource(
    &readbackHeapProperties,
    D3D12_HEAP_FLAG_NONE,
    &readbackBufferDesc,
    D3D12_RESOURCE_STATE_COPY_DEST,
    nullptr,
    __uuidof(readbackBuffer),
    readbackBuffer.put_void()));

{
    D3D12_RESOURCE_BARRIER outputBufferResourceBarrier
    {
        CD3DX12_RESOURCE_BARRIER::Transition(
            outputBuffer.get(),
            D3D12_RESOURCE_STATE_COPY_DEST,
            D3D12_RESOURCE_STATE_COPY_SOURCE)
    };
    commandList->ResourceBarrier(1, &outputBufferResourceBarrier);
}

commandList->CopyResource(readbackBuffer.get(), outputBuffer.get());

// Code goes here to close, execute (and optionally reset) the command list, and also
// to use a fence to wait for the command queue.

// The code below assumes that the GPU wrote FLOATs to the buffer.

D3D12_RANGE readbackBufferRange{ 0, outputBufferSize };
FLOAT * pReadbackBufferData{};
winrt::check_hresult(
    readbackBuffer->Map
    (
        0,
        &readbackBufferRange,
        reinterpret_cast<void**>(&pReadbackBufferData)
    )
);

// Code goes here to access the data via pReadbackBufferData.

D3D12_RANGE emptyRange{ 0, 0 };
readbackBuffer->Unmap
(
    0,
    &emptyRange
);
```

Eine vollständige Implementierung einer Screenshot-Routine, die die renderzieltextur liest und als Datei auf den Datenträger schreibt, finden Sie unter *DirectX-Toolkit für* den [screengriff](https://github.com/microsoft/DirectXTK12/blob/master/Src/ScreenGrab.cpp)von DX12.

## <a name="related-topics"></a>Verwandte Themen

* [Untergeordnete Zuordnung innerhalb eines Puffers](large-buffers.md)
