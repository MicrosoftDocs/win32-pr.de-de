---
title: Synchronisierung mit mehreren Modulen
description: In diesem Thema wird das Synchronisieren des Zugriffs auf die verschiedenen unabhängigen Engines in den meisten modernen GPUs erläutert.
ms.assetid: 93903F50-A6CA-41C2-863D-68D645586B4C
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: 2d250133d8cacb26d933d3774f397de4c949c72b7b58114759791c103d374c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987550"
---
# <a name="multi-engine-synchronization"></a>Synchronisierung mit mehreren Modulen

Die meisten modernen GPUs enthalten mehrere unabhängige Engines, die spezielle Funktionen bereitstellen. Viele verfügen über eine oder mehrere dedizierte Kopier-Engines und eine Compute-Engine, die sich in der Regel von der 3D-Engine unterscheidet. Jede dieser Engines kann Befehle parallel ausführen. Direct3D 12 bietet mithilfe von Warteschlangen und Befehlslisten differenzierten Zugriff auf die 3D-, Compute- und Kopier-Engines.

## <a name="gpu-engines"></a>GPU-Engines

Das folgende Diagramm zeigt die CPU-Threads eines Titels, die jeweils eine oder mehrere der Kopier-, Compute- und 3D-Warteschlangen auffüllen. Die 3D-Warteschlange kann alle drei GPU-Engines steuern. Die Computewarteschlange kann die Compute- und Kopier-Engines steuern. und die Kopierwarteschlange einfach die Kopier-Engine.

Da die verschiedenen Threads die Warteschlangen auffüllen, gibt es keine einfache Garantie für die Ausführungsreihenfolge, weshalb Synchronisierungsmechanismen erforderlich &mdash; sind, wenn der Titel sie erfordert.

![vier Threads, die Befehle an drei Warteschlangen senden](images/gpu-engines.png)

Die folgende Abbildung zeigt, wie ein Titel die Arbeit über mehrere GPU-Engines hinweg planen kann, einschließlich der engineübergreifenden Synchronisierung, falls erforderlich: Es zeigt die Engine-bezogenen Workloads mit engineübergreifenden Abhängigkeiten. In diesem Beispiel kopiert die Kopier-Engine zunächst einige Geometrien, die für das Rendering erforderlich sind. Die 3D-Engine wartet auf den Abschluss dieser Kopien und rendert eine Vorabüberlauffunktion für die Geometrie. Dies wird dann von der Compute-Engine genutzt. Die Ergebnisse der Compute-Engine [**Dispatch**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)werden zusammen mit mehreren Texturkopiervorgängen für die Kopier-Engine von der 3D-Engine für den endgültigen [**Draw-Aufruf**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) genutzt.

![Kopier-, Grafik- und Compute-Engines, die kommunizieren](images/gpu-sync.png)

Der folgende Pseudocode veranschaulicht, wie ein Titel eine solche Workload übermitteln kann.

``` syntax
// Get per-engine contexts. Note that multiple queues may be exposed
// per engine, however that design is not reflected here.
copyEngine = device->GetCopyEngineContext();
renderEngine = device->GetRenderEngineContext();
computeEngine = device->GetComputeEngineContext();
copyEngine->CopyResource(geometry, ...); // copy geometry
copyEngine->Signal(copyFence, 101);
copyEngine->CopyResource(tex1, ...); // copy textures
copyEngine->CopyResource(tex2, ...); // copy more textures
copyEngine->CopyResource(tex3, ...); // copy more textures
copyEngine->CopyResource(tex4, ...); // copy more textures
copyEngine->Signal(copyFence, 102);
renderEngine->Wait(copyFence, 101); // geometry copied
renderEngine->Draw(); // pre-pass using geometry only into rt1
renderEngine->Signal(renderFence, 201);
computeEngine->Wait(renderFence, 201); // prepass completed
computeEngine->Dispatch(); // lighting calculations on pre-pass (using rt1 as SRV)
computeEngine->Signal(computeFence, 301);
renderEngine->Wait(computeFence, 301); // lighting calculated into buf1
renderEngine->Wait(copyFence, 102); // textures copied
renderEngine->Draw(); // final render using buf1 as SRV, and tex[1-4] SRVs
```

Der folgende Pseudocode veranschaulicht die Synchronisierung zwischen den Kopier- und 3D-Engines, um eine heapähnliche Speicherbelegung über einen Ringpuffer zu erreichen. Titel haben die Flexibilität, das richtige Gleichgewicht zwischen der Maximierung der Parallelität (über einen großen Puffer) und der Reduzierung des Arbeitsspeicherverbrauchs und der Wartezeit (über einen kleinen Puffer) auszuwählen.

``` syntax
device->CreateBuffer(&ringCB);
for(int i=1;i++){
  if(i > length) copyEngine->Wait(fence1, i - length);
  copyEngine->Map(ringCB, value%length, WRITE, pData); // copy new data
  copyEngine->Signal(fence2, i);
  renderEngine->Wait(fence2, i);
  renderEngine->Draw(); // draw using copied data
  renderEngine->Signal(fence1, i);
}

// example for length = 3:
// copyEngine->Map();
// copyEngine->Signal(fence2, 1); // fence2 = 1  
// copyEngine->Map();
// copyEngine->Signal(fence2, 2); // fence2 = 2
// copyEngine->Map();
// copyEngine->Signal(fence2, 3); // fence2 = 3
// copy engine has exhausted the ring buffer, so must wait for render to consume it
// copyEngine->Wait(fence1, 1); // fence1 == 0, wait
// renderEngine->Wait(fence2, 1); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 1); // fence1 = 1, copy engine now unblocked
// renderEngine->Wait(fence2, 2); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 2); // fence1 = 2
// renderEngine->Wait(fence2, 3); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 3); // fence1 = 3
// now render engine is starved, and so must wait for the copy engine
// renderEngine->Wait(fence2, 4); // fence2 == 3, wait
```

## <a name="multi-engine-scenarios"></a>Szenarien mit mehreren Engines

Mit Direct3D 12 können Sie vermeiden, dass versehentlich Ineffizienzen auftreten, die durch unerwartete Synchronisierungsverzögerungen verursacht werden. Außerdem können Sie die Synchronisierung auf einer höheren Ebene einführen, wo die erforderliche Synchronisierung mit größerer Sicherheit bestimmt werden kann. Ein zweites Problem, bei dem mehrere Engine-Adressen adressiert werden, besteht darin, teure Vorgänge expliziter zu machen. Dazu gehören Übergänge zwischen 3D und Video, die aufgrund der Synchronisierung zwischen mehreren Kernelkontexten üblicherweise teuer waren.

Insbesondere können die folgenden Szenarien mit Direct3D 12 behandelt werden.

-   Gpu-Vorgänge mit asynchroner und niedriger Priorität. Dies ermöglicht die gleichzeitige Ausführung von GPU-Arbeitsvorgängen mit niedriger Priorität und atomaren Vorgängen, die es einem GPU-Thread ermöglichen, die Ergebnisse eines anderen nicht synchronisierten Threads ohne Blockierung zu nutzen.
-   Computearbeit mit hoher Priorität. Bei Der Hintergrundberechnung ist es möglich, das 3D-Rendering zu unterbrechen, um eine kleine Menge an Computeaufgaben mit hoher Priorität zu erledigen. Die Ergebnisse dieser Arbeit können frühzeitig für zusätzliche Verarbeitung auf der CPU abgerufen werden.
-   Computeaufgaben im Hintergrund. Eine separate Warteschlange mit niedriger Priorität für Computeworkloads ermöglicht es einer Anwendung, freie GPU-Zyklen zu nutzen, um Hintergrundberechnungen ohne negative Auswirkungen auf die primären Renderingaufgaben (oder andere) Aufgaben auszuführen. Hintergrundaufgaben können die Dekomprimierung von Ressourcen oder das Aktualisieren von Simulationen oder Beschleunigungsstrukturen umfassen. Hintergrundaufgaben sollten auf der CPU selten (etwa einmal pro Frame) synchronisiert werden, um zu vermeiden, dass die Vordergrundarbeit angehalten oder verlangsamt wird.
-   Streaming und Hochladen von Daten. Eine separate Kopierwarteschlange ersetzt die D3D11-Konzepte der anfänglichen Daten und der Aktualisierung von Ressourcen. Obwohl die Anwendung für weitere Details im Direct3D 12-Modell verantwortlich ist, ist diese Verantwortung mit Power power verbunden. Die Anwendung kann steuern, wie viel Systemarbeitsspeicher für das Puffern von Uploaddaten aufgewendet wird. Die App kann auswählen, wann und wie (CPU im Vergleich zu GPU, blockierend oder nicht blockierend) synchronisiert werden sollen. Außerdem kann sie den Fortschritt nachverfolgen und die Arbeitsmenge in der Warteschlange steuern.
-   Erhöhte Parallelität. Anwendungen können tiefere Warteschlangen für Hintergrundworkloads (z. B. Videodecodierung) verwenden, wenn sie über separate Warteschlangen für Vordergrundarbeit verfügen.

In Direct3D 12 ist das Konzept einer Befehlswarteschlange die API-Darstellung einer ungefähr seriellen Arbeitssequenz, die von der Anwendung übermittelt wird. Barrieren und andere Techniken ermöglichen die Ausführung dieser Arbeit in einer Pipeline oder in einer nicht ordnungsgemäßen Reihenfolge, aber die Anwendung sieht nur eine einzige Vervollständigungszeitachse. Dies entspricht dem unmittelbaren Kontext in D3D11.

## <a name="synchronization-apis"></a>Synchronisierungs-APIs

### <a name="devices-and-queues"></a>Geräte und Warteschlangen

Das Direct3D 12-Gerät verfügt über Methoden zum Erstellen und Abrufen von Befehlswarteschlangen verschiedener Typen und Prioritäten. Die meisten Anwendungen sollten die Standardbefehlswarteschlangen verwenden, da diese die gemeinsame Nutzung durch andere Komponenten ermöglichen. Anwendungen mit zusätzlichen Parallelitätsanforderungen können zusätzliche Warteschlangen erstellen. Warteschlangen werden durch den Befehlslistentyp angegeben, den sie nutzen.

Lesen Sie die folgenden Erstellungsmethoden von [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device).

-   [**CreateCommandQueue:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) Erstellt eine Befehlswarteschlange basierend auf Informationen in einer [**Direct3D 12 \_ COMMAND QUEUE \_ \_ DESC-Struktur.**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc)
-   [**CreateCommandList:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) Erstellt eine Befehlsliste vom Typ [**Direct3D 12 \_ COMMAND LIST \_ \_ TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).
-   [**CreateFence:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) erstellt einen Fence und notiert die Flags in [**Direct3D 12 \_ FENCE \_ FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags). Umgrenzungen werden verwendet, um Warteschlangen zu synchronisieren.

Warteschlangen aller Typen (3D, Compute und Kopiervorgang) verwenden dieselbe Schnittstelle und sind alle befehlslistenbasiert.

Lesen Sie die folgenden Methoden von [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue).

-   [**ExecuteCommandLists:**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) Übermittelt ein Array von Befehlslisten zur Ausführung. Jede Befehlsliste, die durch [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)definiert wird.
-   [**Signal:**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) Legt einen Fence-Wert fest, wenn die Warteschlange (die auf der GPU ausgeführt wird) einen bestimmten Punkt erreicht.
-   [**Wait:**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) Die Warteschlange wartet, bis die angegebene Umgrenzung den angegebenen Wert erreicht.

Beachten Sie, dass Pakete nicht von Warteschlangen genutzt werden und dieser Typ daher nicht zum Erstellen einer Warteschlange verwendet werden kann.

### <a name="fences"></a>Zäune

Die Multi-Engine-API stellt explizite APIs zum Erstellen und Synchronisieren mithilfe von Fences bereit. Ein Fence ist ein Synchronisierungskonstrukt, das durch einen UINT64-Wert gesteuert wird. Fence-Werte werden von der Anwendung festgelegt. Ein Signalvorgang ändert den Fence-Wert, und ein Wartevorgang blockiert, bis der Umgrenzungsvorgang den angeforderten Wert oder höher erreicht hat. Ein Ereignis kann ausgelöst werden, wenn ein Fence einen bestimmten Wert erreicht.

Weitere Informationen finden Sie in den Methoden der [**ID3D12Fence-Schnittstelle.**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)

-   [**GetCompletedValue:**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) Gibt den aktuellen Wert des Fences zurück.
-   [**SetEventOnCompletion:**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) Bewirkt, dass ein Ereignis ausgelöst wird, wenn der Fence einen bestimmten Wert erreicht.
-   [**Signal:**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) Legt die Umgrenzung auf den angegebenen Wert fest.

Fences ermöglichen CPU-Zugriff auf den aktuellen Fence-Wert sowie CPU-Warte- und -Signale.

Die [**Signal-Methode**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) auf der [**ID3D12Fence-Schnittstelle**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) aktualisiert einen Fence von der CPU-Seite. Dieses Update erfolgt sofort. Die [**Signal-Methode**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) für [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) aktualisiert einen Fence von der GPU-Seite. Dieses Update tritt auf, nachdem alle anderen Vorgänge in der Befehlswarteschlange abgeschlossen wurden.

Alle Knoten in einem Setup mit mehreren Engines können jeden Fence lesen und darauf reagieren, der den richtigen Wert erreicht.

Anwendungen legen ihre eigenen Umgrenzungswerte fest. Ein guter Ausgangspunkt kann sein, einen Umgrenzungsgrenzwert einmal pro Frame zu erhöhen.

Ein *Umgrenzungsschutz kann* *neu eingegrenzt* werden. Dies bedeutet, dass der Fence-Wert nicht ausschließlich erhöht werden muss. Wenn ein **Signalvorgang** in zwei verschiedenen Befehlswarteschlangen in die Warteschlange eingereiht wird oder zwei CPU-Threads **signal** an einem Fence aufrufen, kann es zu einem Race kommen, um zu bestimmen, welches **Signal** zuletzt abgeschlossen wird. Daher ist der Fence-Wert der, der verbleibt. Wenn ein Fence erneut eingegrenzt wird, werden alle neuen Warteanforderungen (einschließlich **SetEventOnCompletion-Anforderungen)** mit dem neuen niedrigeren Fence-Wert verglichen und daher möglicherweise nicht erfüllt, auch wenn der Fence-Wert zuvor hoch genug war, um sie zu erfüllen. Wenn ein Race auftritt, zwischen einem Wert, der einen ausstehenden Wartewert erfüllt, und einem niedrigeren Wert, der dies nicht tut, *wird* der Wartewert unabhängig davon erfüllt, welcher Wert danach verbleibt.

Die Fence-APIs bieten leistungsstarke Synchronisierungsfunktionen, können aber potenziell schwierig zu debuggende Probleme darstellen. Es wird empfohlen, dass jeder Umgrenzungsschutz nur verwendet wird, um den Fortschritt auf einer Zeitachse anzugeben, um Fahrten zwischen Signalisierungssignalen zu verhindern.

### <a name="copy-and-compute-command-lists"></a>Kopieren und Berechnen von Befehlslisten

Alle drei Typen von Befehlslisten verwenden die [**ID3D12GraphicsCommandList-Schnittstelle,**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) aber nur eine Teilmenge der Methoden wird für Kopieren und Berechnen unterstützt.

Kopier- und Computebefehlslisten können die folgenden Methoden verwenden.

-   [**Schließen**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
-   [**CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**CopyResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**CopyTiles**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**Zurücksetzen**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
-   [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

Computebefehlslisten können auch die folgenden Methoden verwenden.

-   [**ClearState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
-   [**ClearUnorderedAccessViewFloat**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [**ClearUnorderedAccessViewUint**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [**DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
-   [**Dispatch**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [**ExecuteIndirect**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)
-   [**SetComputeRoot32BitConstant**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [**SetComputeRoot32BitConstants**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
-   [**SetComputeRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [**SetComputeRootDescriptorTable**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
-   [**SetComputeRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [**SetComputeRootSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
-   [**SetComputeRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [**SetDescriptorHeaps**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
-   [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
-   [**SetPredication**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

Computebefehlslisten müssen beim Aufrufen von [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)eine Compute-PSO festlegen.

Bundles können nicht mit Compute- oder Kopierbefehlslisten oder Warteschlangen verwendet werden.

## <a name="pipelined-compute-and-graphics-example"></a>Pipeline-Compute- und Grafikbeispiel

Dieses Beispiel zeigt, wie die Fence-Synchronisierung verwendet werden kann, um eine Pipeline von Computearbeit in einer Warteschlange zu erstellen (auf die von verwiesen `pComputeQueue` wird), die von Grafikarbeiten in der Warteschlange genutzt `pGraphicsQueue` wird. Die Compute- und Grafikarbeit wird mit der Grafikwarteschlange, die das Ergebnis der Computearbeit von mehreren Frames zurück verbraucht, in pipelined, und ein CPU-Ereignis wird verwendet, um die gesamt in die Warteschlange eingereihte Gesamtarbeit zu drosseln.

```cpp
void PipelinedComputeGraphics()
{
    const UINT CpuLatency = 3;
    const UINT ComputeGraphicsLatency = 2;

    HANDLE handle = CreateEvent(nullptr, FALSE, FALSE, nullptr);

    UINT64 FrameNumber = 0;

    while (1)
    {
        if (FrameNumber > ComputeGraphicsLatency)
        {
            pComputeQueue->Wait(pGraphicsFence,
                FrameNumber - ComputeGraphicsLatency);
        }

        if (FrameNumber > CpuLatency)
        {
            pComputeFence->SetEventOnFenceCompletion(
                FrameNumber - CpuLatency,
                handle);
            WaitForSingleObject(handle, INFINITE);
        }

        ++FrameNumber;

        pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
        pComputeQueue->Signal(pComputeFence, FrameNumber);
        if (FrameNumber > ComputeGraphicsLatency)
        {
            UINT GraphicsFrameNumber = FrameNumber - ComputeGraphicsLatency;
            pGraphicsQueue->Wait(pComputeFence, GraphicsFrameNumber);
            pGraphicsQueue->ExecuteCommandLists(1, &pGraphicsCommandList);
            pGraphicsQueue->Signal(pGraphicsFence, GraphicsFrameNumber);
        }
    }
}
```

Um dieses Pipelining zu unterstützen, muss ein Puffer mit verschiedenen Kopien der Daten vorhanden sein, `ComputeGraphicsLatency+1` die von der Computewarteschlange an die Grafikwarteschlange übergeben werden. Die Befehlslisten müssen UAVs und dekonserieren, um aus der entsprechenden "Version" der Daten im Puffer zu lesen und zu schreiben. Die Computewarteschlange muss warten, bis die Grafikwarteschlange das Lesen aus den Daten für Frame N abgeschlossen hat, bevor sie Frame schreiben `N+ComputeGraphicsLatency` kann.

Beachten Sie, dass die Menge der Computewarteschlange relativ zur CPU nicht direkt von der menge der erforderlichen Pufferung abhängt. Das Queuing der GPU-Arbeit über die Menge des verfügbaren Pufferspeichers hinaus ist jedoch weniger nützlich.

Ein alternativer Mechanismus zur Vermeidung von Dekonsensierung besteht darin, mehrere Befehlslisten zu erstellen, die den einzelnen "umbenannten" Versionen der Daten entsprechen. Im nächsten Beispiel wird dieses Verfahren verwendet, während das vorherige Beispiel erweitert wird, damit die Compute- und Grafikwarteschlangen asynchroner ausgeführt werden können.

## <a name="asynchronous-compute-and-graphics-example"></a>Beispiel für asynchrone Compute- und Grafikfunktionen

Im nächsten Beispiel können Grafiken asynchron aus der Computewarteschlange gerendert werden. Es gibt immer noch eine feste Menge gepufferter Daten zwischen den beiden Phasen, aber die Grafikarbeit wird jetzt unabhängig fortgesetzt und verwendet das aktuellste Ergebnis der Computephase, wie auf der CPU bekannt, wenn die Grafikarbeit in die Warteschlange eingereiht wird. Dies wäre nützlich, wenn die Grafikarbeit von einer anderen Quelle aktualisiert wird, z. B. benutzereingaben. Es müssen mehrere Befehlslisten vorhanden sein, damit die `ComputeGraphicsLatency` Frames der Grafikarbeit gleichzeitig verarbeitet werden können, und die Funktion `UpdateGraphicsCommandList` stellt das Aktualisieren der Befehlsliste dar, sodass die neuesten Eingabedaten eingeschlossen und aus den Computedaten aus dem entsprechenden Puffer gelesen werden.

Die Computewarteschlange muss weiterhin warten, bis die Grafikwarteschlange mit den Pipepuffern abgeschlossen ist. Es wird jedoch ein dritter Umgrenzungsschritt `pGraphicsComputeFence` () eingeführt, damit der Fortschritt der Grafikleseleistung im Vergleich zum Grafikfortschritt im Allgemeinen nachverfolgt werden kann. Dies spiegelt die Tatsache wider, dass aufeinanderfolgende Grafikframes nun aus demselben Computeergebnis lesen oder ein Computeergebnis überspringen könnten. Ein effizienteres, aber etwas komplizierteres Design würde nur den einzelnen Grafikfeingrenzung verwenden und eine Zuordnung zu den Computeframes speichern, die von den einzelnen Grafikrahmen verwendet werden.

```cpp
void AsyncPipelinedComputeGraphics()
{
    const UINT CpuLatency{ 3 };
    const UINT ComputeGraphicsLatency{ 2 };

    // The compute fence is at index 0; the graphics fence is at index 1.
    ID3D12Fence* rgpFences[]{ pComputeFence, pGraphicsFence };
    HANDLE handles[2];
    handles[0] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    handles[1] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    UINT FrameNumbers[]{ 0, 0 };

    ID3D12GraphicsCommandList* rgpGraphicsCommandLists[CpuLatency];
    CreateGraphicsCommandLists(ARRAYSIZE(rgpGraphicsCommandLists),
        rgpGraphicsCommandLists);

    // Graphics needs to wait for the first compute frame to complete; this is the
    // only wait that the graphics queue will perform.
    pGraphicsQueue->Wait(pComputeFence, 1);

    while (true)
    {
        for (auto i = 0; i < 2; ++i)
        {
            if (FrameNumbers[i] > CpuLatency)
            {
                rgpFences[i]->SetEventOnCompletion(
                    FrameNumbers[i] - CpuLatency,
                    handles[i]);
            }
            else
            {
                ::SetEvent(handles[i]);
            }
        }


        auto WaitResult = ::WaitForMultipleObjects(2, handles, FALSE, INFINITE);
        if (WaitResult > WAIT_OBJECT_0 + 1) continue;
        auto Stage = WaitResult - WAIT_OBJECT_0;
        ++FrameNumbers[Stage];

        switch (Stage)
        {
        case 0:
        {
            if (FrameNumbers[Stage] > ComputeGraphicsLatency)
            {
                pComputeQueue->Wait(pGraphicsComputeFence,
                    FrameNumbers[Stage] - ComputeGraphicsLatency);
            }
            pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
            pComputeQueue->Signal(pComputeFence, FrameNumbers[Stage]);
            break;
        }
        case 1:
        {
            // Recall that the GPU queue started with a wait for pComputeFence, 1
            UINT64 CompletedComputeFrames = min(1,
                pComputeFence->GetCompletedValue());
            UINT64 PipeBufferIndex =
                (CompletedComputeFrames - 1) % ComputeGraphicsLatency;
            UINT64 CommandListIndex = (FrameNumbers[Stage] - 1) % CpuLatency;
            // Update graphics command list based on CPU input and using the appropriate
            // buffer index for data produced by compute.
            UpdateGraphicsCommandList(PipeBufferIndex,
                rgpGraphicsCommandLists[CommandListIndex]);

            // Signal *before* new rendering to indicate what compute work
            // the graphics queue is DONE with
            pGraphicsQueue->Signal(pGraphicsComputeFence, CompletedComputeFrames - 1);
            pGraphicsQueue->ExecuteCommandLists(1,
                rgpGraphicsCommandLists + PipeBufferIndex);
            pGraphicsQueue->Signal(pGraphicsFence, FrameNumbers[Stage]);
            break;
        }
        }
    }
}
```

## <a name="multi-queue-resource-access"></a>Ressourcenzugriff mit mehreren Warteschlangen

Um auf eine Ressource in mehr als einer Warteschlange zuzugreifen, muss eine Anwendung die folgenden Regeln einhalten.

-   Der Ressourcenzugriff (siehe [**Direct3D 12 \_ RESOURCE \_ STATES)**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)wird von der Warteschlangentypklasse und nicht vom Warteschlangenobjekt bestimmt. Es gibt zwei Typklassen der Warteschlange: Compute-/3D-Warteschlange ist eine Typklasse, Copy ist eine zweite Typklasse. Daher kann eine Ressource mit einer Barriere für den \_ NON PIXEL \_ \_ SHADER-RESSOURCENstatus in einer 3D-Warteschlange in diesem Zustand in jeder 3D- oder Compute-Warteschlange verwendet werden. Dies unterliegt den Synchronisierungsanforderungen, die erfordern, dass die meisten Schreibvorgänge serialisiert werden müssen. Die Ressourcenzustände, die von den beiden Typklassen (COPY SOURCE und COPY DEST) gemeinsam genutzt \_ \_ werden, werden für jede Typklasse als unterschiedliche Status betrachtet. Wenn also eine Ressource in einer Kopierwarteschlange auf COPY DEST umgestellt \_ wird, ist sie nicht als Kopierziel aus 3D- oder Computewarteschlangen zugänglich und umgekehrt.

    Zusammenfassung:

    -   Ein Warteschlangenobjekt ist eine beliebige einzelne Warteschlange.
    -   Ein Warteschlangentyp ist einer der folgenden drei Typen: Compute, 3D und Copy.
    -   Eine "Typklasse" der Warteschlange ist eine dieser beiden Optionen: Compute/3D und Copy.

-   Die COPY-Flags (COPY \_ DEST und COPY SOURCE), die \_ als Anfangszustände verwendet werden, stellen Zustände in der 3D/Compute-Typklasse dar. Um eine Ressource anfänglich in einer Kopierwarteschlange zu verwenden, sollte sie im Status COMMON gestartet werden. Der COMMON-Zustand kann für alle Verwendungen in einer Kopierwarteschlange mithilfe der impliziten Zustandsübergänge verwendet werden. 
-   Obwohl der Ressourcenzustand für alle Compute- und 3D-Warteschlangen freigegeben ist, ist es nicht zulässig, gleichzeitig in die Ressource in verschiedenen Warteschlangen zu schreiben. "Gleichzeitig" bedeutet hier, dass die nicht synchronisierte Ausführung auf einigen Hardwarekomponenten nicht möglich ist. Es gelten die folgenden Regeln.

    -   Nur eine Warteschlange kann gleichzeitig in eine Ressource schreiben.
    -   Mehrere Warteschlangen können aus der Ressource lesen, solange sie die vom Writer geänderten Bytes nicht lesen (das gleichzeitige Lesen von Bytes führt zu nicht definierten Ergebnissen).
    -   Ein Fence muss nach dem Schreiben synchronisiert werden, bevor eine andere Warteschlange die geschriebenen Bytes lesen oder schreibzugriffen kann.

-   Die angezeigten Hintergrundpuffer müssen sich im Zustand Direct3D 12 \_ RESOURCE \_ STATE COMMON \_ befinden. 

## <a name="related-topics"></a>Zugehörige Themen

[Direct3D 12-Programmierhandbuch](directx-12-programming-guide.md)

[Verwenden von Ressourcenbarrieren zum Synchronisieren von Ressourcenzuständen in Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

[Speicherverwaltung in Direct3D 12](memory-management.md)
