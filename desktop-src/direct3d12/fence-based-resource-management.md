---
title: Fence-Based Ressourcenverwaltung
description: Zeigt, wie die Lebensdauer von Ressourcen Daten verwaltet wird, indem der GPU-Status über Zäune nachverfolgt wird. Der Arbeitsspeicher kann mit der Verwendung von Zäunen, die die Verfügbarkeit von freiem Speicherplatz im Arbeitsspeicher sorgfältig verwalten, wie z. b. in einer Ringpuffer Implementierung für einen uploadheap
ms.assetid: A7AB6569-EC6B-4B1B-9266-D05B6DB3A27B
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aba8afd66f8a50a54b699c6a314ba148ebcef023
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103495"
---
# <a name="fence-based-resource-management"></a>Fence-Based Ressourcenverwaltung

Zeigt, wie die Lebensdauer von Ressourcen Daten verwaltet wird, indem der GPU-Status über Zäune nachverfolgt wird. Der Arbeitsspeicher kann mit der Verwendung von Zäunen, die die Verfügbarkeit von freiem Speicherplatz im Arbeitsspeicher sorgfältig verwalten, wie z. b. in einer Ringpuffer Implementierung für einen uploadheap

-   [Ring Puffer Szenario](#ring-buffer-scenario)
-   [Ring Puffer Beispiel](#ring-buffer-sample)
-   [Verwandte Themen](#related-topics)

## <a name="ring-buffer-scenario"></a>Ring Puffer Szenario

Im folgenden finden Sie ein Beispiel, in dem eine APP einen seltenen Bedarf für den Upload von Heap Speicher hat.

Ein Ringpuffer ist eine Möglichkeit zum Verwalten eines uploadheaps. Der Ringpuffer enthält die für die nächsten Frames erforderlichen Daten. Die APP verwaltet einen aktuellen Dateneingabe Zeiger und eine Frame Offset Warteschlange, um jeden Frame und den Start Offset von Ressourcen Daten für diesen Frame aufzuzeichnen.

Eine App erstellt einen Ringpuffer, der auf einem Puffer basiert, um Daten für jeden Frame in die GPU hochzuladen. Frame 2 wurde gerade gerendert, der Ringpuffer umschließt die Daten für Frame 4, alle für Frame 5 erforderlichen Daten sind vorhanden, und für Frame 6 muss ein großer konstanter Puffer unter zugewiesen werden.

**Abbildung 1** : die APP versucht, eine untergeordnete Zuordnungen für den Konstantenpuffer zu verwenden, sucht jedoch nicht genügend freien Speicherplatz.

![nicht genügend freier Arbeitsspeicher in diesem Ringpuffer.](images/ring-buffer-1.png)

**Abbildung 2** : durch das Absichern der APP wird festgestellt, dass Frame 3 gerendert wurde, die Warteschlange des Frame Offsets aktualisiert wird und der aktuelle Zustand des Ring Puffers lautet. der freie Arbeitsspeicher ist jedoch immer noch nicht groß genug, um dem Konstanten Puffer Rechnung zu tragen.

![nach dem Rendern von Frame 3 noch nicht genügend Arbeitsspeicher](images/ring-buffer-2.png)

**Abbildung 3** : aufgrund der Situation gibt es die CPU-Blockierung (über das Ende des endblocks), bis Frame 4 gerendert wurde. Dadurch wird der für Frame 4 zugewiesene Arbeitsspeicher freigegeben.

![Rendern von Frame 4 gibt weitere Informationen zum Ringpuffer frei.](images/ring-buffer-3.png)

**Abbildung 4** : der freie Speicherplatz ist nun groß genug für den konstanten Puffer, und die unter Zuordnung ist erfolgreich. die APP kopiert die großen Konstanten Puffer Daten in den Arbeitsspeicher, der zuvor von den Ressourcen Daten für die beiden Rahmen 3 und 4 verwendet wurde. Der aktuelle Eingabe Zeiger wird schließlich aktualisiert.

![der Ringpuffer enthält jetzt Platz aus Frame 6.](images/ring-buffer-4.png)

Wenn eine APP einen Ringpuffer implementiert, muss der Ringpuffer groß genug sein, um mit dem schlechteren Szenario der Größe von Ressourcen Daten umzugehen.

## <a name="ring-buffer-sample"></a>Ring Puffer Beispiel

Der folgende Beispielcode zeigt, wie ein Ringpuffer verwaltet werden kann, und es wird auf die untergeordnete Zuordnungs Routine geachtet, die das Abrufen und warten von Endpunkten behandelt. Der Einfachheit halber verwendet das Beispiel nicht \_ genügend Arbeits \_ Speicher, um die Details von "nicht genügend freiem Speicher im Heap" zu verbergen, da diese Logik (basierend auf *m \_ pdatacur* und Offsets innerhalb von *frameoffsetqueue*) nicht eng mit Heaps oder Zäunen verknüpft ist. Das Beispiel wird vereinfacht, um die Framerate anstelle der Speicherauslastung zu opfern.

Beachten Sie, dass die Ringpuffer Unterstützung ein gängiges Szenario ist. der Heap Entwurf schließt jedoch nicht die andere Verwendung aus, z. b. die Parametrisierung der Befehlsliste und die erneute Verwendung.

``` syntax
struct FrameResourceOffset
{
    UINT frameIndex;
    UINT8* pResourceOffset;
};
std::queue<FrameResourceOffset> frameOffsetQueue;

void DrawFrame()
{
    float vertices[] = ...;
    UINT verticesOffset = 0;
    ThrowIfFailed(
        SetDataToUploadHeap(
            vertices, sizeof(float), sizeof(vertices) / sizeof(float), 
            4, // Max alignment requirement for vertex data is 4 bytes.
            verticesOffset
            ));

    float constants[] = ...;
    UINT constantsOffset = 0;
    ThrowIfFailed(
        SetDataToUploadHeap(
            constants, sizeof(float), sizeof(constants) / sizeof(float), 
            D3D12_CONSTANT_BUFFER_DATA_PLACEMENT_ALIGNMENT,
            constantsOffset
            ));

    // Create vertex buffer views for the new binding model. 
    // Create constant buffer views for the new binding model. 
    // ...

    commandQueue->Execute(commandList);
    commandQueue->AdvanceFence();
}

HRESULT SuballocateFromHeap(SIZE_T uSize, UINT uAlign)
{
    if (NOT_SUFFICIENT_MEMORY(uSize, uAlign))
    {
        // Free up resources for frames processed by GPU; see Figure 2.
        UINT lastCompletedFrame = commandQueue->GetLastCompletedFence();
        FreeUpMemoryUntilFrame( lastCompletedFrame );

        while ( NOT_SUFFICIENT_MEMORY(uSize, uAlign)
            && !frameOffsetQueue.empty() )
        {
            // Block until a new frame is processed by GPU, then free up more memory; see Figure 3.
            UINT nextGPUFrame = frameOffsetQueue.front().frameIndex;
            commandQueue->SetEventOnFenceCompletion(nextGPUFrame, hEvent);
            WaitForSingleObject(hEvent, INFINITE);
            FreeUpMemoryUntilFrame( nextGPUFrame );
        }
    }

    if (NOT_SUFFICIENT_MEMORY(uSize, uAlign))
    {
        // Apps need to create a new Heap that is large enough for this resource.
        return E_HEAPNOTLARGEENOUGH;
    }
    else
    {
        // Update current data pointer for the new resource.
        m_pDataCur = reinterpret_cast<UINT8*>(
            Align(reinterpret_cast<SIZE_T>(m_pHDataCur), uAlign)
            );

        // Update frame offset queue if this is the first resource for a new frame; see Figure 4.
        UINT currentFrame = commandQueue->GetCurrentFence();
        if ( frameOffsetQueue.empty()
            || frameOffsetQueue.back().frameIndex < currentFrame )
        {
            FrameResourceOffset offset = {currentFrame, m_pDataCur};
            frameOffsetQueue.push(offset);
        }

        return S_OK;
    }
}

void FreeUpMemoryUntilFrame(UINT lastCompletedFrame)
{
    while ( !frameOffsetQueue.empty() 
        && frameOffsetQueue.first().frameIndex <= lastCompletedFrame )
    {
        frameOffsetQueue.pop();
    }
}
```

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence)
</dt> <dt>

[Untergeordnete Zuordnung innerhalb von Puffern](large-buffers.md)
</dt> </dl>

 

 




