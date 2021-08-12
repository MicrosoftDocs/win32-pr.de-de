---
title: Zurücklesen von Daten über einen Puffer
description: Zum Zurücklesen von Daten aus der GPU (z. B. zum Erfassen eines Screenshots) verwenden Sie einen Rückleseheap.
ms.assetid: 2F515B2C-3317-4AA8-81E1-7762ED895F77
ms.localizationpriority: high
ms.topic: article
ms.date: 12/17/2018
ms.openlocfilehash: 56babd93ddd0f06ee331b19db4a4d8ba2dc5ecb314ec3d828e3e3f7c4f4f9a7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300873"
---
# <a name="read-back-data-via-a-buffer"></a>Zurücklesen von Daten über einen Puffer

Zum Zurücklesen von Daten aus der GPU (z. B. zum Erfassen eines Screenshots) verwenden Sie einen Rückleseheap. Diese Technik bezieht sich auf das [Hochladen von Texturdaten über einen Puffer](upload-and-readback-of-texture-data.md)mit einigen Unterschieden.

- Um Daten zurückzulesen, erstellen Sie einen Heap, wobei der **D3D12_HEAP_TYPE** auf [D3D12_HEAP_TYPE_READBACK](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)und nicht auf D3D12_HEAP_TYPE_UPLOAD festgelegt **ist.**
- Die Ressource auf dem zurückgelesenen Heap muss immer ein **D3D12_RESOURCE_DIMENSION_BUFFER** sein.
- Sie verwenden einen Fence, um zu erkennen, wann die GPU die Verarbeitung eines Frames abgeschlossen hat (wenn das Schreiben von Daten in Ihren Ausgabepuffer abgeschlossen ist). Dies ist wichtig, da die [**ID3D12Resource::Map-Methode**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) nicht mit der GPU synchronisiert wird (umgekehrt *wird* die Direct3D 11-Entsprechung synchronisiert). Direct3D **12-Zuordnungsaufrufe** verhalten sich so, als würden Sie die Direct3D 11-Entsprechung mit dem flag NO_OVERWRITE aufrufen.
- Nachdem die Daten bereit sind (einschließlich aller erforderlichen Ressourcenbarrieren), rufen Sie [**ID3D12Resource::Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) auf, um die Rücklesedaten für die CPU sichtbar zu machen.

## <a name="code-example"></a>Codebeispiel

Das folgende Codebeispiel zeigt die allgemeine Übersicht über den Prozess des Zurücklesens von Daten von der GPU auf die CPU über einen Puffer.

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

Eine vollständige Implementierung einer Screenshotroutine, die die Renderzieltextur liest und als Datei auf den Datenträger schreibt, finden Sie unter *DirectX Tool Kit for DX12* es [ScreenGrab](https://github.com/microsoft/DirectXTK12/blob/master/Src/ScreenGrab.cpp).

## <a name="related-topics"></a>Zugehörige Themen

* [Unterzuordnung innerhalb eines Puffers](large-buffers.md)
