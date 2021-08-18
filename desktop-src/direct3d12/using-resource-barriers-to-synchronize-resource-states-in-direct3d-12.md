---
title: Verwenden von Ressourcenbarrieren zum Synchronisieren von Ressourcenzuständen in Direct3D 12
description: Um die CPU-Gesamtauslastung zu reduzieren und Multithreading und Vorverarbeitung von Treibern zu ermöglichen, überträgt Direct3D 12 die Verantwortung für die ressourcenspezifische Zustandsverwaltung vom Grafiktreiber in die Anwendung.
ms.assetid: 3AB3BF34-433C-400B-921A-55B23CCDA44F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f79d5463c2f27560049f785b5cc32fe42ae33927cba7d039b90638f3946531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989430"
---
# <a name="using-resource-barriers-to-synchronize-resource-states-in-direct3d-12"></a>Verwenden von Ressourcenbarrieren zum Synchronisieren von Ressourcenzuständen in Direct3D 12

Um die CPU-Gesamtauslastung zu reduzieren und Multithreading und Vorverarbeitung von Treibern zu ermöglichen, überträgt Direct3D 12 die Verantwortung für die ressourcenspezifische Zustandsverwaltung vom Grafiktreiber in die Anwendung. Ein Beispiel für den ressourcenspezifischen Zustand ist, ob auf eine Texturressource derzeit als über eine Shader-Ressourcenansicht oder als Renderzielansicht zugegriffen wird. In Direct3D 11 mussten Treiber diesen Zustand im Hintergrund nachverfolgen. Dies ist aus CPU-Sicht teuer und erschwert jede Art von Multithreadentwurf erheblich. In Microsoft Direct3D 12 wird der meiste Zustand pro Ressource von der Anwendung mit einer einzelnen API verwaltet: [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).

-   [Verwenden der ResourceBarrier-API zum Verwalten des Zustands pro Ressource](#using-the-resourcebarrier-api-to-manage-per-resource-state)
    -   [Ressourcenzustände](#using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
    -   [Anfangszustände für Ressourcen](#initial-states-for-resources)
    -   [Einschränkungen für den Lese-/Schreibzustand der Ressource](#readwrite-resource-state-restrictions)
    -   [Ressourcenzustände für die Präsentation von Puffern](#resource-states-for-presenting-back-buffers)
    -   [Verwerfen von Ressourcen](#discarding-resources)
-   [Implizite Zustandsübergänge](#implicit-state-transitions)
    -   [Allgemeine Statusaufstufung](#common-state-promotion)
    -   [Zustandsverfall zu gemeinsamer](#state-decay-to-common)
    -   [Folgen für die Leistung](#performance-implications)
-   [Teilungsbarrieren](#split-barriers)
-   [Beispielszenario für Ressourcenbarrieren](#resource-barrier-example-scenario)
-   [Beispiel für allgemeine Zustandsaufstufung und -zerfall](#common-state-promotion-and-decay-sample)
-   [Beispiel für Teilungsbarrieren](#example-of-split-barriers)
-   [Zugehörige Themen](#related-topics)

## <a name="using-the-resourcebarrier-api-to-manage-per-resource-state"></a>Verwenden der ResourceBarrier-API zum Verwalten des Zustands pro Ressource

[**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) benachrichtigt den Grafiktreiber über Situationen, in denen der Treiber möglicherweise mehrere Zugriffe auf den Arbeitsspeicher synchronisieren muss, in dem eine Ressource gespeichert ist. Die -Methode wird mit einer oder mehr Ressourcenbarrierenbeschreibungsstrukturen aufgerufen, die den Typ der zu de declaredenden Ressourcenbarriere angeben.

Es gibt drei Arten von Ressourcenbarrieren:

-   **Übergangsbarriere:** Eine Übergangsbarriere gibt an, dass eine Reihe von Unterressourcen zwischen verschiedenen Verwendungen übergewechselt wird. Eine [**D3D12 \_ RESOURCE TRANSITION \_ \_ BARRIER-Struktur**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) wird verwendet, um die zu  überlagernde Unterressource sowie die Zustände vor und nach der Unterressource anzugeben. 

    Das System überprüft, ob Unterressourcenübergänge in einer Befehlsliste mit vorherigen Übergängen in derselben Befehlsliste konsistent sind. Die Debugebene verfolgt den Unterressourcenstatus weiter nach, um andere Fehler zu finden. Diese Überprüfung ist jedoch konservativ und nicht vollständig.

    Beachten Sie, dass Sie das Flag D3D12 \_ RESOURCE \_ BARRIER ALL \_ SUBRESOURCES verwenden können, um anzugeben, dass alle Unterressourcen innerhalb einer Ressource \_ übergangen werden.

-   **Aliasingbarriere:** Eine Aliasingbarriere gibt einen Übergang zwischen den Verwendungen von zwei verschiedenen Ressourcen an, die überlappende Zuordnungen zum gleichen Heap haben. Dies gilt sowohl für reservierte als auch für platzierte Ressourcen. Eine [**D3D12 \_ RESOURCE \_ ALIASING \_ BARRIER-Struktur**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) wird verwendet, um sowohl die *ressource before* als auch die *after-Ressource* anzugeben.

    Beachten Sie, dass eine oder beide Ressourcen NULL sein können, was darauf hinweist, dass jede gekachelte Ressource Aliasing verursachen kann. Weitere Informationen zur Verwendung von gekachelten Ressourcen finden Sie unter [Gekachelte Ressourcen](../direct3d11/tiled-resources.md) und [Volumenkachelressourcen.](volume-tiled-resources.md)

-   **UAV-Barriere (Unordered Access View,** ungeordnete Zugriffsansicht): Eine UAV-Barriere gibt an, dass alle UAV-Zugriffe (Sowohl Lese- als auch Schreibzugriffe) auf eine bestimmte Ressource zwischen zukünftigen UAV-Zugriffen (Sowohl Lese- als auch Schreibzugriff) abgeschlossen werden müssen. Es ist nicht erforderlich, dass eine App eine UAV-Barriere zwischen zwei Draw- oder Dispatch-Aufrufen einlädt, die nur aus einem UAV lesen. Außerdem ist es nicht notwendig, eine UAV-Barriere zwischen zwei Draw- oder Dispatch-Aufrufen zu setzen, die in dieselbe UAV schreiben, wenn die Anwendung weiß, dass es sicher ist, den UAV-Zugriff in beliebiger Reihenfolge auszuführen. Eine [**\_ \_ UAV \_ BARRIER-Struktur der D3D12-RESSOURCE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) wird verwendet, um die UAV-Ressource anzugeben, für die die Barriere gilt. Die Anwendung kann NULL für die UAV der Barriere angeben, was darauf hinweist, dass jeder UAV-Zugriff die Barriere erfordern könnte.

Wenn [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) mit einem Array von Ressourcenbarrierenbeschreibungen aufgerufen wird, verhält sich die API so, als ob sie einmal für jedes Element in der Reihenfolge aufgerufen würde, in der sie bereitgestellt wurden.

Zu jedem Zeitpunkt befindet sich eine Unterressource in genau einem Zustand, der durch den Satz von [**D3D12 \_ RESOURCE \_ STATES-Flags**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) bestimmt wird, die [**resourceBarrier bereitgestellt werden.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) Die Anwendung muss sicherstellen, dass *die Zustände vor* und *nach* aufeinander folgenden Aufrufen von **ResourceBarrier** zustimmen.

> [!TIP]
>
> Anwendungen sollten nach Möglichkeit mehrere Übergänge in einen API-Aufruf batchen.

 

### <a name="resource-states"></a>Ressourcenzustände

Die vollständige Liste der Ressourcenzustände, zwischen denen eine Ressource umstiegen kann, finden Sie im Referenzthema für die [**Enumeration D3D12 \_ RESOURCE \_ STATES.**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)

Informationen zu Split Resource Barriers finden Sie auch unter [**D3D12 \_ RESOURCE \_ BARRIER \_ FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).

### <a name="initial-states-for-resources"></a>Anfangszustände für Ressourcen

Ressourcen können mit einem beliebigen vom Benutzer angegebenen Anfangszustand erstellt werden (gültig für die Ressourcenbeschreibung), mit den folgenden Ausnahmen:

-   Hochladen Heaps müssen im Zustand D3D12 RESOURCE STATE GENERIC READ beginnen. Dies ist \_ \_ eine \_ \_ bitweise OR-Kombination aus:
    -   D3D12 \_ RESOURCE STATE VERTEX AND CONSTANT BUFFER (D3D12-RESSOURCENZUSTANDSVERTEX \_ UND \_ \_ \_ KONSTANTER \_ PUFFER)
    -   D3D12 \_ RESOURCE \_ STATE \_ INDEX \_ BUFFER
    -   D3D12 \_ RESOURCE \_ STATE \_ COPY \_ SOURCE
    -   RESSOURCE "D3D12 \_ RESOURCE STATE NON PIXEL \_ \_ \_ \_ \_ SHADER"
    -   RESSOURCE "D3D12 \_ RESOURCE \_ STATE PIXEL \_ \_ \_ SHADER"
    -   INDIREKTES \_ \_ D3D12-RESSOURCENZUSTANDSARGUMENT \_ \_
-   Readback-Heaps müssen im ZUSTAND D3D12 \_ RESOURCE \_ STATE COPY \_ \_ DEST gestartet werden.
-   Auslagerungskettenpuffer werden automatisch im ZUSTAND D3D12 \_ RESOURCE \_ STATE COMMON \_ gestartet.

Bevor ein Heap das Ziel eines GPU-Kopiervorgang sein kann, muss der Heap normalerweise zuerst in den Zustand D3D12 \_ RESOURCE \_ STATE COPY \_ \_ DEST überführen. Ressourcen, die auf UPLOAD-Heaps erstellt werden, müssen jedoch in beginnen und können sich nicht vom GENERISCHEN READ-Zustand ändern, da nur die \_ CPU schreibt. Umgekehrt müssen in READBACK-Heaps erstellte Ressourcen, für die ein Committed erstellt wurde, in beginnen und können sich nicht vom COPY \_ DEST-Zustand ändern.

### <a name="readwrite-resource-state-restrictions"></a>Einschränkungen für den Lese-/Schreibzustand der Ressource

Die Ressourcenzustandsverwendungsbits, die zum Beschreiben eines Ressourcenzustands verwendet werden, sind in schreibgeschützte Und Lese-/Schreibzustände unterteilt. Das Referenzthema für [**D3D12 \_ RESOURCE \_ STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) gibt die Lese-/Schreibzugriffsebene für jedes Bit in der Enumeration an.

Für jede Ressource kann nur ein Lese-/Schreibbit festgelegt werden. Wenn ein Schreibbit festgelegt ist, kann kein schreibgeschütztes Bit für diese Ressource festgelegt werden. Wenn kein Schreibbit festgelegt ist, kann eine beliebige Anzahl von Lesebits festgelegt werden.

### <a name="resource-states-for-presenting-back-buffers"></a>Ressourcenzustände für die Präsentation von Puffern

Bevor ein Hintergrundpuffer dargestellt wird, muss er sich im ZUSTAND D3D12 RESOURCE STATE COMMON (D3D12 \_ RESOURCE STATE \_ \_ COMMON) befindet. Beachten Sie, dass der Ressourcenzustand D3D12 RESOURCE STATE PRESENT ein Synonym für \_ \_ \_ D3D12 RESOURCE STATE COMMON ist und beide den Wert \_ \_ \_ 0 haben. Wenn [**IDXGISwapChain::P resent**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (oder [**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) für eine Ressource aufgerufen wird, die sich derzeit nicht in diesem Zustand befindet, wird eine Debugebenenwarnung ausgegeben.

### <a name="discarding-resources"></a>Verwerfen von Ressourcen

Alle Unterressourcen in einer Ressource müssen sich im Zustand RENDER TARGET oder DEPTH WRITE für Renderziele bzw. Tiefen-Schablonenressourcen befinden, wenn \_ \_ [**ID3D12GraphicsCommandList::D iscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) aufgerufen wird.

## <a name="implicit-state-transitions"></a>Implizite Zustandsübergänge

Ressourcen können nur aus D3D12 \_ RESOURCE STATE COMMON "promoted" \_ \_ werden. Ebenso werden Ressourcen nur in D3D12 \_ RESOURCE STATE COMMON "verfällt". \_ \_

### <a name="common-state-promotion"></a>Allgemeine Statusaufstufung

Alle Pufferressourcen sowie Texturen mit dem D3D12 RESOURCE FLAG ALLOW SIMULTANEOUS ACCESS-Flag werden implizit von \_ \_ \_ \_ \_ D3D12 RESOURCE STATE \_ COMMON \_ \_ \_ auf den relevanten Zustand beim ersten GPU-Zugriff hoch 2012, einschließlich GENERISCHER LESEzugriff, um alle Leseszenarios abdecken zu können. Auf jede Ressource im Common-Zustand kann so zugegriffen werden, als ob sie sich in einem einzigen Zustand mit

<dl> 1 WRITE-Flag oder  
1 oder mehr READ-Flags  
</dl>

Ressourcen können basierend auf der folgenden Tabelle aus dem COMMON-Status promotet werden:



| Statusflag                    | Puffer und Simultaneous-Access Texturen                             | Texturen ohne gleichzeitigen Zugriff                                     |
|-------------------------------|----------------------------------------------|--------------------------------------|
| \_SCHEITELPUNKT UND \_ KONSTANTER \_ PUFFER | Ja                                          | Nein                                   |
| INDEX \_ BUFFER                 | Ja                                          | Nein                                   |
| \_RENDERZIEL                | Ja                                          | Nein                                   |
| UNGEORDNETER \_ ZUGRIFF             | Ja                                          | Nein                                   |
| \_TIEFENSCHREIBEN                  | Nein<sup>\*</sup>                              | Nein                                   |
| \_TIEFENLESE                   | Nein<sup>\*</sup>                              | Nein                                   |
| \_ \_ SHADERRESSOURCE OHNE \_ PIXEL  | Ja                                          | Ja                                  |
| \_ \_ PIXEL-SHADER-RESSOURCE       | Ja                                          | Ja                                  |
| STREAM \_ OUT                   | Ja                                          | Nein                                   |
| INDIREKTES \_ ARGUMENT            | Ja                                          | Nein                                   |
| COPY \_ DEST                    | Ja                                          | Ja                                  |
| QUELLE \_ KOPIEREN                  | Ja                                          | Ja                                  |
| RESOLVE \_ DEST                 | Ja                                          | Nein                                   |
| RESOLVE \_ SOURCE               | Ja                                          | Nein                                   |
| PRÄDICATION                   | Ja                                          | Nein                                   |



 

<sup>\*</sup>Tiefen-Schablonenressourcen müssen Texturen ohne gleichzeitigen Zugriff sein und können daher nie implizit hoch promotet werden.

Wenn dieser Zugriff auftritt, verhält sich die Promotion wie eine implizite Ressourcenbarriere. Für nachfolgende Zugriffe sind Ressourcenbarrieren erforderlich, um den Ressourcenstatus bei Bedarf zu ändern. Beachten Sie, dass die Aufstufung von einem auf mehrere Lesestatus 2016 um 1.000.000.000 Lesestatus ist gültig, aber dies ist bei Schreibzuständen nicht der Fall.  
Wenn z. B. eine Ressource im allgemeinen Zustand in einem Draw-Aufruf zu EINER PIXELS-SHADER-RESSOURCE promotet wird, kann sie trotzdem auf NON_PIXEL \_ \_ \_ SHADER RESOURCE-Ressource | \_ \_PIXELS-SHADERRESSOURCE \_ in einem anderen Draw-Aufruf. Wenn sie jedoch in einem Schreibvorgang verwendet wird, z. B. einem Kopierziel, wird hier eine Übergangsbarriere für den Ressourcenzustand aus den kombinierten her promoted read states NON_PIXEL \_ SHADER \_ RESOURCE | DIE \_ PIXEL-SHADER-RESSOURCE \_ zum KOPIEREN \_ DEST ist erforderlich.  
Analog dazu ist beim Promote von COMMON zu COPY DEST weiterhin eine Barriere erforderlich, um von COPY DEST zu \_ RENDER TARGET zu \_ \_ überwechseln.

Beachten Sie, dass die Allgemeine Statusaufstufung "kostenlos" ist, da die GPU keine Synchronisierungswarteungen ausführen muss. Die -Promotion stellt die Tatsache dar, dass Ressourcen im COMMON-Zustand keine zusätzliche GPU-Arbeit oder Treibernachverfolgung erfordern sollten, um bestimmte Zugriffe zu unterstützen.

### <a name="state-decay-to-common"></a>Zustandsverfall zu gemeinsamer

Die Kehrseite der Allgemeinen Zustandsaufstufung ist der Rückfall zurück zu D3D12 \_ RESOURCE \_ STATE \_ COMMON. Ressourcen, die bestimmte Anforderungen erfüllen, gelten als zustandslos und kehren effektiv in den allgemeinen Zustand zurück, wenn die GPU die Ausführung eines [**ExecuteCommandLists-Vorgangs**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) beendet. Der Unterfall tritt nicht zwischen Befehlslisten auf, die zusammen im gleichen **ExecuteCommandLists-Aufruf ausgeführt** werden.

Die folgenden Ressourcen verfällt, wenn ein [**ExecuteCommandLists-Vorgang**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) auf der GPU abgeschlossen wird:

-   Ressourcen, auf die in einer Kopierwarteschlange zugegriffen wird, *oder*
-   Puffern von Ressourcen für einen beliebigen Warteschlangentyp *oder*
-   Texturressourcen für jeden Warteschlangentyp, für den das \_ D3D12-RESSOURCENFlag ALLOW SIMULTANEOUS ACCESS \_ festgelegt \_ \_ \_ ist, *oder*
-   Jede Ressource, die implizit in einen schreibgeschützten Zustand hoch 2.

Wie bei der Heraufstufung des allgemeinen Zustands ist der Verfall frei, da keine zusätzliche Synchronisierung erforderlich ist. Die Kombination von Common State Promotion und Decay kann dazu beitragen, viele unnötige [**ResourceBarrier-Übergänge**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) zu vermeiden. In einigen Fällen kann dies zu erheblichen Leistungsverbesserungen führen.

Puffer und Simultaneous-Access werden in den allgemeinen Zustand verfällt, unabhängig davon, ob sie explizit mithilfe von Ressourcenbarrieren oder implizit promotet wurden.

### <a name="performance-implications"></a>Folgen für die Leistung

Wenn Sie [**explizite ResourceBarrier-Übergänge**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) für Ressourcen im allgemeinen Zustand aufzeichnen, ist es richtig, entweder D3D12 RESOURCE STATE COMMON oder einen beliebigen aufstlegbaren Zustand als BeforeState-Wert in der \_ \_ \_ D3D12 RESOURCE TRANSITION  BARRIER-Struktur zu \_ \_ \_ verwenden. Dies ermöglicht eine herkömmliche Zustandsverwaltung, bei der der automatische Verfall von Puffern und Texturen mit gleichzeitigem Zugriff ignoriert wird. Dies ist jedoch möglicherweise nicht wünschenswert, da die Vermeidung von **ResourceBarrier-Übergangsaufrufen** mit Ressourcen, die bekannterfalls den allgemeinen Zustand haben, die Leistung erheblich verbessern kann. Ressourcenbarrieren können teuer sein. Sie sind darauf ausgelegt, Cache leeren, Änderungen am Speicherlayout und andere Synchronisierungen zu erzwingen, die für Ressourcen, die sich bereits im allgemeinen Zustand befinden, möglicherweise nicht erforderlich sind. Eine Befehlsliste, die eine Ressourcenbarriere von einem nicht gängigen Zustand zu einem anderen nicht gemeinsamen Zustand für eine Ressource verwendet, die sich derzeit im allgemeinen Zustand befindet, kann zu einem großen unned Overhead führen.

Vermeiden Sie außerdem [**explizite ResourceBarrier-Übergänge**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) zu D3D12 RESOURCE STATE COMMON, sofern dies nicht unbedingt erforderlich ist \_ \_ (z. B. befindet sich der nächste Zugriff in einer COPY-Befehlswarteschlange, die erfordert, dass ressourcen im allgemeinen Zustand \_ beginnen). Übermäßige Übergänge in den allgemeinen Zustand können die GPU-Leistung erheblich verlangsamen.

Zusammenfassend gilt: Versuchen Sie, sich auf die Heraufstufung und Denkung des allgemeinen Zustands zu verlassen, wenn ihre Semantik es Ihnen ohne Ausgabe von [**ResourceBarrier-Aufrufen zu**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) ersendet.

## <a name="split-barriers"></a>Teilungsbarrieren

Eine Ressourcenübergangsbarriere mit dem Flag D3D12 RESOURCE BARRIER FLAG BEGIN ONLY beginnt eine getrennte Barriere, und die Übergangsbarriere wird \_ \_ als \_ \_ \_ ausstehend bezeichnet. Während die Barriere aussteht, kann die (Untergeordnete)Ressource nicht von der GPU gelesen oder geschrieben werden. Die einzige gesetzliche Übergangsbarriere, die auf eine Ressource (Unter-)Ressource  mit  einer ausstehenden Barriere angewendet werden kann, ist eine mit denselben Vor- und Nachzuständen und dem Flag D3D12 RESOURCE BARRIER FLAG END ONLY, das den ausstehenden Übergang \_ absperrt. \_ \_ \_ \_

Teilungsbarrieren geben der GPU Hinweise darauf, dass eine Ressource im Zustand *A* später als Nächstes in Zustand *B* verwendet wird. Dadurch hat die GPU die Möglichkeit, die Workload für den Übergang zu optimieren und möglicherweise Ausführungsstags zu reduzieren oder zu beseitigen. Durch das Ausstellen der ausschließlichen Endbarriere wird sichergestellt, dass alle GPU-Übergangsarbeiten abgeschlossen sind, bevor sie mit dem nächsten Befehl ausgeführt werden.

Die Verwendung von Teilungsbarrieren kann zur Verbesserung der Leistung beitragen, insbesondere in Szenarien mit mehreren Engines oder bei ressourcenübergreifenden Lese-/Schreibzugriffen in einer oder mehreren Befehlslisten.

## <a name="resource-barrier-example-scenario"></a>Beispielszenario für Ressourcenbarrieren

Die folgenden Codeausschnitte zeigen die Verwendung der [**ResourceBarrier-Methode**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) in einem Multithreadingbeispiel.

Erstellen der Tiefen-Schablonenansicht und Übergang in einen schreibbaren Zustand.


```C++
// Create the depth stencil.
{
    CD3DX12_RESOURCE_DESC shadowTextureDesc(
        D3D12_RESOURCE_DIMENSION_TEXTURE2D,
        0,
        static_cast<UINT>(m_viewport.Width), 
        static_cast<UINT>(m_viewport.Height), 
        1,
        1,
        DXGI_FORMAT_D32_FLOAT,
        1, 
        0,
        D3D12_TEXTURE_LAYOUT_UNKNOWN,
        D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL | D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE);

    D3D12_CLEAR_VALUE clearValue;    // Performance tip: Tell the runtime at resource creation the desired clear value.
    clearValue.Format = DXGI_FORMAT_D32_FLOAT;
    clearValue.DepthStencil.Depth = 1.0f;
    clearValue.DepthStencil.Stencil = 0;

    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &shadowTextureDesc,
        D3D12_RESOURCE_STATE_DEPTH_WRITE,
        &clearValue,
        IID_PPV_ARGS(&m_depthStencil)));

    // Create the depth stencil view.
    m_device->CreateDepthStencilView(m_depthStencil.Get(), nullptr, m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
}
```



Erstellen der Scheitelpunktpufferansicht, zuerst ändern Sie sie von einem allgemeinen Zustand in ein Ziel und dann von einem Ziel in einen generischen lesbaren Zustand.


```C++
// Create the vertex buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_vertexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the vertex buffer.
        D3D12_SUBRESOURCE_DATA vertexData = {};
        vertexData.pData = pAssetData + SampleAssets::VertexDataOffset;
        vertexData.RowPitch = SampleAssets::VertexDataSize;
        vertexData.SlicePitch = vertexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy vertex buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_vertexBuffer.Get(), m_vertexBufferUpload.Get(), 0, 0, 1, &vertexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_vertexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER));

        PIXEndEvent(commandList.Get());
    }
```



Erstellen der Indexpufferansicht, zuerst ändern Sie sie von einem allgemeinen Zustand in ein Ziel und dann von einem Ziel in einen generischen lesbaren Zustand.


```C++
// Create the index buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_indexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_indexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the index buffer.
        D3D12_SUBRESOURCE_DATA indexData = {};
        indexData.pData = pAssetData + SampleAssets::IndexDataOffset;
        indexData.RowPitch = SampleAssets::IndexDataSize;
        indexData.SlicePitch = indexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy index buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_indexBuffer.Get(), m_indexBufferUpload.Get(), 0, 0, 1, &indexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_indexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_INDEX_BUFFER));

        PIXEndEvent(commandList.Get());
    }

    // Initialize the index buffer view.
    m_indexBufferView.BufferLocation = m_indexBuffer->GetGPUVirtualAddress();
    m_indexBufferView.SizeInBytes = SampleAssets::IndexDataSize;
    m_indexBufferView.Format = SampleAssets::StandardIndexFormat;
}
```



Erstellen von Texturen und Shader-Ressourcenansichten. Die Textur wird von einem allgemeinen Zustand in ein Ziel und dann von einem Ziel in eine Pixel-Shaderressource geändert.


```C++
    // Create each texture and SRV descriptor.
    const UINT srvCount = _countof(SampleAssets::Textures);
    PIXBeginEvent(commandList.Get(), 0, L"Copy diffuse and normal texture data to default resources...");
    for (int i = 0; i < srvCount; i++)
    {
        // Describe and create a Texture2D.
        const SampleAssets::TextureResource &tex = SampleAssets::Textures[i];
        CD3DX12_RESOURCE_DESC texDesc(
            D3D12_RESOURCE_DIMENSION_TEXTURE2D,
            0,
            tex.Width, 
            tex.Height, 
            1,
            static_cast<UINT16>(tex.MipLevels),
            tex.Format,
            1, 
            0,
            D3D12_TEXTURE_LAYOUT_UNKNOWN,
            D3D12_RESOURCE_FLAG_NONE);

        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
            D3D12_HEAP_FLAG_NONE,
            &texDesc,
            D3D12_RESOURCE_STATE_COPY_DEST,
            nullptr,
            IID_PPV_ARGS(&m_textures[i])));

        {
            const UINT subresourceCount = texDesc.DepthOrArraySize * texDesc.MipLevels;
            UINT64 uploadBufferSize = GetRequiredIntermediateSize(m_textures[i].Get(), 0, subresourceCount);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
                D3D12_HEAP_FLAG_NONE,
                &CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize),
                D3D12_RESOURCE_STATE_GENERIC_READ,
                nullptr,
                IID_PPV_ARGS(&m_textureUploads[i])));

            // Copy data to the intermediate upload heap and then schedule a copy 
            // from the upload heap to the Texture2D.
            D3D12_SUBRESOURCE_DATA textureData = {};
            textureData.pData = pAssetData + tex.Data->Offset;
            textureData.RowPitch = tex.Data->Pitch;
            textureData.SlicePitch = tex.Data->Size;

            UpdateSubresources(commandList.Get(), m_textures[i].Get(), m_textureUploads[i].Get(), 0, 0, subresourceCount, &textureData);
            commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_textures[i].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
        }

        // Describe and create an SRV.
        D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
        srvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
        srvDesc.Format = tex.Format;
        srvDesc.Texture2D.MipLevels = tex.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = 0;
        srvDesc.Texture2D.ResourceMinLODClamp = 0.0f;
        m_device->CreateShaderResourceView(m_textures[i].Get(), &srvDesc, cbvSrvHandle);

        // Move to the next descriptor slot.
        cbvSrvHandle.Offset(cbvSrvDescriptorSize);
    }
```



Beginnen eines Frames; dabei wird nicht nur [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) verwendet, um anzugeben, dass der Backbuffer als Renderziel verwendet werden soll, sondern auch die Frameressource (die **ResourceBarrier** im Tiefen-Schablonenpuffer aufruft).


```C++
// Assemble the CommandListPre command list.
void D3D12Multithreading::BeginFrame()
{
    m_pCurrentFrameResource->Init();

    // Indicate that the back buffer will be used as a render target.
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    // Clear the render target and depth stencil.
    const float clearColor[] = { 0.0f, 0.0f, 0.0f, 1.0f };
    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearDepthStencilView(m_dsvHeap->GetCPUDescriptorHandleForHeapStart(), D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPre]->Close());
}

// Assemble the CommandListMid command list.
void D3D12Multithreading::MidFrame()
{
    // Transition our shadow map from the shadow pass to readable in the scene pass.
    m_pCurrentFrameResource->SwapBarriers();

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListMid]->Close());
}
```



Beenden eines Frames, der angibt, dass der Hintergrundpuffer jetzt zur Anzeige verwendet wird.


```C++
// Assemble the CommandListPost command list.
void D3D12Multithreading::EndFrame()
{
    m_pCurrentFrameResource->Finish();

    // Indicate that the back buffer will now be used to present.
    m_pCurrentFrameResource->m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPost]->Close());
}
```



Beim Initialisieren einer Frameressource, die beim Start eines Frames aufgerufen wird, wird der Tiefen-Schablonenpuffer in schreibbar.


```C++
void FrameResource::Init()
{
    // Reset the command allocators and lists for the main thread.
    for (int i = 0; i < CommandListCount; i++)
    {
        ThrowIfFailed(m_commandAllocators[i]->Reset());
        ThrowIfFailed(m_commandLists[i]->Reset(m_commandAllocators[i].Get(), m_pipelineState.Get()));
    }

    // Clear the depth stencil buffer in preparation for rendering the shadow map.
    m_commandLists[CommandListPre]->ClearDepthStencilView(m_shadowDepthView, D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    // Reset the worker command allocators and lists.
    for (int i = 0; i < NumContexts; i++)
    {
        ThrowIfFailed(m_shadowCommandAllocators[i]->Reset());
        ThrowIfFailed(m_shadowCommandLists[i]->Reset(m_shadowCommandAllocators[i].Get(), m_pipelineStateShadowMap.Get()));

        ThrowIfFailed(m_sceneCommandAllocators[i]->Reset());
        ThrowIfFailed(m_sceneCommandLists[i]->Reset(m_sceneCommandAllocators[i].Get(), m_pipelineState.Get()));
    }
}
```



Barrieren werden im Rahmen getauscht, um die Schattenkarte von schreibbar in lesbar zu überschreiben.


```C++
void FrameResource::SwapBarriers()
{
    // Transition the shadow map from writeable to readable.
    m_commandLists[CommandListMid]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_DEPTH_WRITE, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
}
```



Finish wird aufgerufen, wenn ein Frame beendet wird und die Schattenkarte in einen gemeinsamen Zustand über geht.


```C++
void FrameResource::Finish()
{
    m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_DEPTH_WRITE));
}
```



## <a name="common-state-promotion-and-decay-sample"></a>Beispiel für allgemeine Zustandsaufstufung und -zerfall

``` syntax
    // Create a buffer resource using D3D12_RESOURCE_STATE_COMMON as the init state
    ID3D12Resource *pResource;
    CreateCommittedVertexBufferInCommonState(1024, &pResource);

    // Copy data to the buffer without the need for a barrier.
    // Promotes pResource state to D3D12_RESOURCE_STATE_COPY_DEST.
    pCommandList->CopyBufferRegion(pResource, 0, pOtherResource, 0, 1024); 

    // To use pResource as a vertex buffer a transition barrier is needed.
    // Note the StateBefore is D3D12_RESOURCE_STATE_COPY_DEST.
    D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TYPE_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_FLAG_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COPY_DEST;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    // Use pResource as a vertex buffer
    D3D12_VERTEX_BUFFER_VIEW vbView;
    vbView.BufferLocation = pResource->GetGPUVirtualAddress();
    vbView.SizeInBytes = 1024;
    vbView.StrideInBytes = sizeof(MyVertex);

    pCommandList->IASetVertexBuffers(0, 1, &vbView);
    pCommandList->Draw();

    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 
    pCommandList->Reset(pAllocator, pPipelineState);

    // Since the reset command list will be executed in a separate call to 
    // ExecuteCommandLists, the previous state of pResource
    // will have decayed to D3D12_RESOURCE_STATE_COMMON so, again, no barrier is needed
    pCommandList->CopyBufferRegion(pResource, 0, pDifferentResource, 0, 1024);

    FinishRecordingCommandList(pCommandList);
    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 

    WaitForQueue(pCommandQueue);

    // The previous ExecuteCommandLists call has finished so 
    // pResource has decayed to D3D12_RESOURCE_STATE_COMMON
```

## <a name="example-of-split-barriers"></a>Beispiel für Teilungsbarrieren

Das folgende Beispiel zeigt, wie Sie eine Teilungsbarriere verwenden, um Pipeline-Stags zu reduzieren. Der folgende Code verwendet keine Teilungsbarrieren:

``` syntax
 D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource
    OtherStuff(); // .. other gpu work

    // Transition pResource to PIXEL_SHADER_RESOURCE
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    Read(pResource); // ... read from pResource
```

Im folgenden Code werden getrennte Barrieren verwendet:

``` syntax
D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource

    // Done writing to pResource. Start barrier to PIXEL_SHADER_RESOURCE and
    // then do other work
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_BEGIN_ONLY;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    OtherStuff(); // .. other gpu work

    // Need to read from pResource so end barrier
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_END_ONLY;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    Read(pResource); // ... read from pResource
```

## <a name="related-topics"></a>Zugehörige Themen

[Videotutorials für erweitertes Lernen mit DirectX: Ressourcenbarrieren und Zustandsnachverfolgung](https://www.youtube.com/watch?v=nmB2XMasz2o)

[Synchronisierung mit mehreren Modulen](./user-mode-heap-synchronization.md)

[Arbeitsübermittlung in Direct3D 12](command-queues-and-command-lists.md)

[Ein Blick in D3D12-Ressourcenzustandsbarrieren](https://devblogs.microsoft.com/directx/a-look-inside-d3d12-resource-state-barriers/)

