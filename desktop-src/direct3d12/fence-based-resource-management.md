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
# <a name="fence-based-resource-management"></a><span data-ttu-id="72ced-104">Fence-Based Ressourcenverwaltung</span><span class="sxs-lookup"><span data-stu-id="72ced-104">Fence-Based Resource Management</span></span>

<span data-ttu-id="72ced-105">Zeigt, wie die Lebensdauer von Ressourcen Daten verwaltet wird, indem der GPU-Status über Zäune nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="72ced-105">Shows how to manage resource data life-span by tracking GPU progress via fences.</span></span> <span data-ttu-id="72ced-106">Der Arbeitsspeicher kann mit der Verwendung von Zäunen, die die Verfügbarkeit von freiem Speicherplatz im Arbeitsspeicher sorgfältig verwalten, wie z. b. in einer Ringpuffer Implementierung für einen uploadheap</span><span class="sxs-lookup"><span data-stu-id="72ced-106">Memory can be effectively re-used with fences carefully managing the availability of free space in memory, such as in a ring buffer implementation for an Upload heap.</span></span>

-   [<span data-ttu-id="72ced-107">Ring Puffer Szenario</span><span class="sxs-lookup"><span data-stu-id="72ced-107">Ring buffer scenario</span></span>](#ring-buffer-scenario)
-   [<span data-ttu-id="72ced-108">Ring Puffer Beispiel</span><span class="sxs-lookup"><span data-stu-id="72ced-108">Ring buffer sample</span></span>](#ring-buffer-sample)
-   [<span data-ttu-id="72ced-109">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="72ced-109">Related topics</span></span>](#related-topics)

## <a name="ring-buffer-scenario"></a><span data-ttu-id="72ced-110">Ring Puffer Szenario</span><span class="sxs-lookup"><span data-stu-id="72ced-110">Ring buffer scenario</span></span>

<span data-ttu-id="72ced-111">Im folgenden finden Sie ein Beispiel, in dem eine APP einen seltenen Bedarf für den Upload von Heap Speicher hat.</span><span class="sxs-lookup"><span data-stu-id="72ced-111">The following is an example in which an app experiences a rare demand for upload heap memory.</span></span>

<span data-ttu-id="72ced-112">Ein Ringpuffer ist eine Möglichkeit zum Verwalten eines uploadheaps.</span><span class="sxs-lookup"><span data-stu-id="72ced-112">A ring buffer is one way to manage an upload heap.</span></span> <span data-ttu-id="72ced-113">Der Ringpuffer enthält die für die nächsten Frames erforderlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="72ced-113">The ring buffer holds data required for the next few frames.</span></span> <span data-ttu-id="72ced-114">Die APP verwaltet einen aktuellen Dateneingabe Zeiger und eine Frame Offset Warteschlange, um jeden Frame und den Start Offset von Ressourcen Daten für diesen Frame aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="72ced-114">The app maintains a current data input pointer, and a frame offset queue to record each frame and starting offset of resource data for that frame.</span></span>

<span data-ttu-id="72ced-115">Eine App erstellt einen Ringpuffer, der auf einem Puffer basiert, um Daten für jeden Frame in die GPU hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="72ced-115">An app creates a ring-buffer based upon a buffer to upload data to the GPU for each frame.</span></span> <span data-ttu-id="72ced-116">Frame 2 wurde gerade gerendert, der Ringpuffer umschließt die Daten für Frame 4, alle für Frame 5 erforderlichen Daten sind vorhanden, und für Frame 6 muss ein großer konstanter Puffer unter zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="72ced-116">Currently frame 2 has been rendered, the ring buffer wraps around the data for frame 4, all the data required for frame 5 is present, and a large constant buffer required for frame 6 needs to be sub-allocated.</span></span>

<span data-ttu-id="72ced-117">**Abbildung 1** : die APP versucht, eine untergeordnete Zuordnungen für den Konstantenpuffer zu verwenden, sucht jedoch nicht genügend freien Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="72ced-117">**Figure 1** : the app tries to sub-allocate for the constant buffer, but finds insufficient free memory.</span></span>

![nicht genügend freier Arbeitsspeicher in diesem Ringpuffer.](images/ring-buffer-1.png)

<span data-ttu-id="72ced-119">**Abbildung 2** : durch das Absichern der APP wird festgestellt, dass Frame 3 gerendert wurde, die Warteschlange des Frame Offsets aktualisiert wird und der aktuelle Zustand des Ring Puffers lautet. der freie Arbeitsspeicher ist jedoch immer noch nicht groß genug, um dem Konstanten Puffer Rechnung zu tragen.</span><span class="sxs-lookup"><span data-stu-id="72ced-119">**Figure 2** : through fence polling, the app discovers that frame 3 has been rendered, the frame offset queue is then updated, and the current state of the ring buffer follows - however, free memory is still not large enough to accommodate the constant buffer.</span></span>

![nach dem Rendern von Frame 3 noch nicht genügend Arbeitsspeicher](images/ring-buffer-2.png)

<span data-ttu-id="72ced-121">**Abbildung 3** : aufgrund der Situation gibt es die CPU-Blockierung (über das Ende des endblocks), bis Frame 4 gerendert wurde. Dadurch wird der für Frame 4 zugewiesene Arbeitsspeicher freigegeben.</span><span class="sxs-lookup"><span data-stu-id="72ced-121">**Figure 3** : given the situation, the CPU blocks itself (via fence waiting) until frame 4 has been rendered, which frees up the memory sub-allocated for frame 4.</span></span>

![Rendern von Frame 4 gibt weitere Informationen zum Ringpuffer frei.](images/ring-buffer-3.png)

<span data-ttu-id="72ced-123">**Abbildung 4** : der freie Speicherplatz ist nun groß genug für den konstanten Puffer, und die unter Zuordnung ist erfolgreich. die APP kopiert die großen Konstanten Puffer Daten in den Arbeitsspeicher, der zuvor von den Ressourcen Daten für die beiden Rahmen 3 und 4 verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="72ced-123">**Figure 4** : now free memory is large enough for the constant buffer, and sub-allocation succeeds; the app copies the big constant buffer data to memory previously used by resource data for both frames 3 and 4.</span></span> <span data-ttu-id="72ced-124">Der aktuelle Eingabe Zeiger wird schließlich aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="72ced-124">The current input pointer is finally updated.</span></span>

![der Ringpuffer enthält jetzt Platz aus Frame 6.](images/ring-buffer-4.png)

<span data-ttu-id="72ced-126">Wenn eine APP einen Ringpuffer implementiert, muss der Ringpuffer groß genug sein, um mit dem schlechteren Szenario der Größe von Ressourcen Daten umzugehen.</span><span class="sxs-lookup"><span data-stu-id="72ced-126">If an app implements a ring buffer, the ring buffer must be large enough to cope with the worse-case scenario of the sizes of resource data.</span></span>

## <a name="ring-buffer-sample"></a><span data-ttu-id="72ced-127">Ring Puffer Beispiel</span><span class="sxs-lookup"><span data-stu-id="72ced-127">Ring buffer sample</span></span>

<span data-ttu-id="72ced-128">Der folgende Beispielcode zeigt, wie ein Ringpuffer verwaltet werden kann, und es wird auf die untergeordnete Zuordnungs Routine geachtet, die das Abrufen und warten von Endpunkten behandelt.</span><span class="sxs-lookup"><span data-stu-id="72ced-128">The following sample code shows how a ring buffer can be managed, paying attention to the sub-allocation routine that handles fence polling and waiting.</span></span> <span data-ttu-id="72ced-129">Der Einfachheit halber verwendet das Beispiel nicht \_ genügend Arbeits \_ Speicher, um die Details von "nicht genügend freiem Speicher im Heap" zu verbergen, da diese Logik (basierend auf *m \_ pdatacur* und Offsets innerhalb von *frameoffsetqueue*) nicht eng mit Heaps oder Zäunen verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="72ced-129">For simplicity, the sample uses NOT\_SUFFICIENT\_MEMORY to hide the details of “not sufficient free memory found in the heap” since that logic (based on *m\_pDataCur* and offsets inside *FrameOffsetQueue*) is not tightly related to heaps or fences.</span></span> <span data-ttu-id="72ced-130">Das Beispiel wird vereinfacht, um die Framerate anstelle der Speicherauslastung zu opfern.</span><span class="sxs-lookup"><span data-stu-id="72ced-130">The sample is simplified to sacrifice frame rate instead of memory utilization.</span></span>

<span data-ttu-id="72ced-131">Beachten Sie, dass die Ringpuffer Unterstützung ein gängiges Szenario ist. der Heap Entwurf schließt jedoch nicht die andere Verwendung aus, z. b. die Parametrisierung der Befehlsliste und die erneute Verwendung.</span><span class="sxs-lookup"><span data-stu-id="72ced-131">Note that, ring-buffer support is expected to be a popular scenario; however, the heap design does not preclude other usage, such as command list parameterization and re-use.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="72ced-132">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="72ced-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72ced-133">**ID3D12Fence**</span><span class="sxs-lookup"><span data-stu-id="72ced-133">**ID3D12Fence**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence)
</dt> <dt>

[<span data-ttu-id="72ced-134">Untergeordnete Zuordnung innerhalb von Puffern</span><span class="sxs-lookup"><span data-stu-id="72ced-134">Suballocation Within Buffers</span></span>](large-buffers.md)
</dt> </dl>

 

 




