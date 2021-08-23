---
title: Fence-basierte Ressourcenverwaltung
description: Zeigt, wie Sie die Lebensdauer von Ressourcendaten verwalten, indem Sie den GPU-Fortschritt über Fences nachverfolgen. Arbeitsspeicher kann effektiv mit Fences erneut verwendet werden, um die Verfügbarkeit von freiem Speicherplatz im Arbeitsspeicher sorgfältig zu verwalten, z. B. in einer Ringpufferimplementierung für einen Hochladen Heap.
ms.assetid: A7AB6569-EC6B-4B1B-9266-D05B6DB3A27B
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cbfd9231e3013099c8382072049f1ae1478e28f00830e89fb4ecef1b835ce58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119728890"
---
# <a name="fence-based-resource-management"></a>Fence-basierte Ressourcenverwaltung

Zeigt, wie Sie die Lebensdauer von Ressourcendaten verwalten, indem Sie den GPU-Fortschritt über Fences nachverfolgen. Arbeitsspeicher kann effektiv mit Fences erneut verwendet werden, um die Verfügbarkeit von freiem Speicherplatz im Arbeitsspeicher sorgfältig zu verwalten, z. B. in einer Ringpufferimplementierung für einen Hochladen Heap.

-   [Ringpufferszenario](#ring-buffer-scenario)
-   [Ringpufferbeispiel](#ring-buffer-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="ring-buffer-scenario"></a>Ringpufferszenario

Im Folgenden finden Sie ein Beispiel, in dem für eine App ein seltener Bedarf an Upload-Heapspeicher besteht.

Ein Ringpuffer ist eine Möglichkeit, einen Upload-Heap zu verwalten. Der Ringpuffer enthält daten, die für die nächsten Frames erforderlich sind. Die App verwaltet einen aktuellen Dateneingabezeiger und eine Frameoffsetwarteschlange, um jeden Frame und den Startoffset der Ressourcendaten für diesen Frame zu erfassen.

Eine App erstellt einen Ringpuffer basierend auf einem Puffer, um Daten für jeden Frame in die GPU hochzuladen. Derzeit wurde Frame 2 gerendert, der Ringpuffer umhingt die Daten für Frame 4, alle für Frame 5 erforderlichen Daten sind vorhanden, und ein großer konstanter Puffer, der für Frame 6 erforderlich ist, muss unter zugeordnet werden.

**Abbildung 1:** Die App versucht, den konstanten Puffer unterzuteilen, findet jedoch nicht genügend freien Arbeitsspeicher.

![Unzureichender freier Arbeitsspeicher in diesem Ringpuffer](images/ring-buffer-1.png)

**Abbildung 2:** Durch fence polling stellt die App fest, dass Frame 3 gerendert wurde, die Frameoffsetwarteschlange dann aktualisiert wird und der aktuelle Zustand des Ringpuffers folgt. Der freie Arbeitsspeicher ist jedoch immer noch nicht groß genug, um den konstanten Puffer aufnehmen zu können.

![nach dem Rendern von Frame 3 noch nicht genügend Arbeitsspeicher](images/ring-buffer-2.png)

**Abbildung 3:** Angesichts der Situation blockiert sich die CPU selbst (über den Fence Waiting), bis Frame 4 gerendert wurde, wodurch der für Frame 4 unter zugeordnete Arbeitsspeicher frei wird.

![Renderingframe 4 gibt mehr vom Ringpuffer frei](images/ring-buffer-3.png)

**Abbildung 4:** Jetzt ist der freie Arbeitsspeicher groß genug für den konstanten Puffer, und die Unterzuordnung ist erfolgreich. Die App kopiert die großen konstanten Pufferdaten in den Arbeitsspeicher, der zuvor von Ressourcendaten für die Frames 3 und 4 verwendet wurde. Der aktuelle Eingabezeiger wird schließlich aktualisiert.

![Jetzt ist Platz aus Frame 6 im Ringpuffer](images/ring-buffer-4.png)

Wenn eine App einen Ringpuffer implementiert, muss der Ringpuffer groß genug sein, um mit dem schlechteren Szenario der Größen von Ressourcendaten umgehen zu können.

## <a name="ring-buffer-sample"></a>Ringpufferbeispiel

Der folgende Beispielcode zeigt, wie ein Ringpuffer verwaltet werden kann, und achten Sie dabei auf die Unterzuordnungsroutine, die das Abrufen und Warten von Fence verarbeitet. Der Einfachheit halber verwendet das Beispiel NICHT GENÜGEND ARBEITSSPEICHER, um die Details von "nicht genügend freiem Arbeitsspeicher im Heap" auszublenden, da diese Logik (basierend auf \_ \_ m *\_ pDataCur* und Offsets in *FrameOffsetQueue)* nicht eng mit Heaps oder Fences verknüpft ist. Das Beispiel wird vereinfacht, um die Bildfrequenz anstelle der Arbeitsspeicherauslastung zu erhöhen.

Beachten Sie, dass die Ringpufferunterstützung ein beliebtes Szenario sein wird. Der Heapentwurf schließt jedoch keine andere Verwendung aus, z. B. die Parametrisierung und Erneutverwendung von Befehlslisten.

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

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence)
</dt> <dt>

[Unterzuweisung innerhalb von Puffern](large-buffers.md)
</dt> </dl>

 

 




