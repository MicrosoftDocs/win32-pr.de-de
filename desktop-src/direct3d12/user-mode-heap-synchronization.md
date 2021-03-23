---
title: Multi-Engine-Synchronisierung
description: In diesem Thema wird die Synchronisierung des Zugriffs auf mehrere unabhängige Engines in den meisten modernen GPUs erläutert.
ms.assetid: 93903F50-A6CA-41C2-863D-68D645586B4C
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: d60704e411a1ba45dd4902ad9101a416391743dd
ms.sourcegitcommit: 622d149edf775af5a9633c2d12ccfddf7000b8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2020
ms.locfileid: "104548633"
---
# <a name="multi-engine-synchronization"></a>Multi-Engine-Synchronisierung

Die meisten modernen GPUs enthalten mehrere unabhängige Engines, die spezialisierte Funktionen bereitstellen. Viele verfügen über ein oder mehrere dedizierte Kopier Module und eine COMPUTE-Engine, die sich in der Regel von der 3D-Engine unterscheidet. Jedes dieser Engines kann Befehle parallel untereinander ausführen. Direct3D 12 bietet differenzierten Zugriff auf 3D-, COMPUTE-und Kopier Module mithilfe von Warteschlangen und Befehlslisten.

## <a name="gpu-engines"></a>GPU-Engines

Das folgende Diagramm zeigt die CPU-Threads eines Titels, von denen jede eine oder mehrere der Copy-, COMPUTE-und 3D-Warteschlangen füllt. Die 3D-Warteschlange kann alle drei GPU-Engines steuern. Die COMPUTE-Warteschlange kann die COMPUTE-und Kopier Module steuern. und die Kopier Warteschlange ist einfach die Kopier-Engine.

Da die verschiedenen Threads die Warteschlangen auffüllen, kann es keine einfache Garantie für die Ausführungsreihenfolge geben, daher ist es erforderlich, dass Synchronisierungs Mechanismen erforderlich sind, &mdash; Wenn der Titel Sie benötigt.

![vier Threads, die Befehle an drei Warteschlangen senden](images/gpu-engines.png)

In der folgenden Abbildung wird veranschaulicht, wie ein Titel die Arbeit über mehrere GPU-Engines hinweg planen kann, einschließlich der zwischen Modul Synchronisierung, falls erforderlich: Er zeigt die Workloads pro Engine mit Abhängigkeiten zwischen den Engines. In diesem Beispiel kopiert die Copy-Engine zuerst eine Geometrie, die für das Rendering erforderlich ist. Die 3D-Engine wartet auf den Abschluss dieser Kopien und rendert einen vorab Durchlauf über die Geometrie. Diese wird dann von der COMPUTE-Engine verwendet. Die Ergebnisse der Verteilung der computeengine werden zusammen mit mehreren Textur Kopier Vorgängen für die Kopier [**-Engine von**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)der 3D-Engine für den abschließenden [**Zeichnen**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) -Befehl genutzt.

![Kopieren, Grafiken und Compute-Engines kommunizieren](images/gpu-sync.png)

Der folgende Pseudo Code veranschaulicht, wie ein Titel eine solche Arbeitsauslastung übermitteln kann.

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

Der folgende Pseudo Code veranschaulicht die Synchronisierung zwischen den Kopier-und 3D-Engines, um eine Heap ähnliche Speicher Belegung über einen Ringpuffer zu erreichen. Titel haben die Flexibilität, das richtige Gleichgewicht zwischen der Maximierung der Parallelität (über einen großen Puffer) und der Reduzierung der Arbeitsspeicher Nutzung und Latenz (über einen kleinen Puffer) auszuwählen.

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

## <a name="multi-engine-scenarios"></a>Szenarios mit mehreren Engines

Mit Direct3D 12 können Sie versehentlich zu Ineffizienzen führen, die durch unerwartete Synchronisierungs Verzögerungen verursacht werden. Außerdem können Sie die Synchronisierung auf einer höheren Ebene einführen, bei der die erforderliche Synchronisierung mit größerer Sicherheit bestimmt werden kann. Ein zweites Problem ist, dass mehrere-Engine-Adressen teure Vorgänge expliziter machen müssen. Dies schließt Übergänge zwischen 3D und Video ein, die aufgrund der Synchronisierung zwischen mehreren Kernel Kontexten traditionell aufwendig waren.

Insbesondere können die folgenden Szenarien mit Direct3D 12 adressiert werden.

-   GPU-Arbeit mit asynchroner und niedriger Priorität. Dies ermöglicht die gleichzeitige Ausführung von GPU-arbeiten mit niedriger Priorität und atomaren Vorgängen, die es einem GPU-Thread ermöglichen, die Ergebnisse eines anderen nicht synchronisierten Threads ohne Blockierung zu nutzen
-   Compute-Arbeit mit hoher Priorität. Mit background Compute ist es möglich, das 3D-Rendering zu unterbrechen, um eine kleine Menge von computeaufgaben mit hoher Priorität zu erledigen. Die Ergebnisse dieser Arbeit können frühzeitig zur weiteren Verarbeitung auf der CPU abgerufen werden.
-   Computearbeit im Hintergrund. Eine separate Warteschlange mit niedriger Priorität für computeworkloads ermöglicht es einer Anwendung, freie GPU-Zyklen zu verwenden, um eine Hintergrund Berechnung ohne negative Auswirkung auf die primären Renderingaufgaben auszuführen. Hintergrundaufgaben können die Dekomprimierung von Ressourcen oder das Aktualisieren von Simulationen oder beschleunigungsstrukturen umfassen. Hintergrundaufgaben sollten auf der CPU selten (ungefähr einmal pro Frame) synchronisiert werden, um das stecken bleiben oder verlangsamen der Vordergrund Arbeit zu vermeiden.
-   Streaming und Hochladen von Daten. Eine separate Kopier Warteschlange ersetzt die D3D11-Konzepte der Anfangsdaten und Aktualisierungs Ressourcen. Obwohl die Anwendung für weitere Details im Direct3D 12-Modell verantwortlich ist, ist diese Verantwortung in Kraft. Die Anwendung kann steuern, wie viel System Arbeitsspeicher für die Pufferung von uploaddaten aufgewendet wird. Die APP kann auswählen, wann und wie (CPU-und GPU-Leistung, Blockierung und nicht Blockierung) synchronisiert werden soll, und kann den Fortschritt nachverfolgen und die Menge der in der Warteschlange befindlichen Aufgaben steuern
-   Erhöhung der Parallelität. Anwendungen können tiefere Warteschlangen für hintergrundworkloads (z. b. Video Decodierung) verwenden, wenn Sie über separate Warteschlangen für Vordergrund arbeiten verfügen.

In Direct3D 12 ist das Konzept einer Befehls Warteschlange die API-Darstellung einer ungefähr seriellen Abfolge von Arbeitsaufgaben, die von der Anwendung übermittelt wird. Mithilfe von Barrieren und anderen Techniken können diese Aufgaben in einer Pipeline oder außerhalb der Reihenfolge ausgeführt werden, aber die Anwendung sieht nur eine einzelne Vervollständigungs Zeitachse. Dies entspricht dem unmittelbaren Kontext in D3D11.

## <a name="synchronization-apis"></a>Synchronisierungs-APIs

### <a name="devices-and-queues"></a>Geräte und Warteschlangen

Das Gerät Direct3D 12 verfügt über Methoden zum Erstellen und Abrufen von Befehls Warteschlangen mit unterschiedlichen Typen und Prioritäten. Die meisten Anwendungen sollten die standardmäßigen Befehls Warteschlangen verwenden, da diese die gemeinsame Verwendung durch andere Komponenten ermöglichen. Anwendungen mit zusätzlichen Parallelitäts Anforderungen können zusätzliche Warteschlangen erstellen. Warteschlangen werden durch den von Ihnen genutzten Befehls Auflistungstyp angegeben.

Weitere Informationen finden Sie in den folgenden Erstellungs Methoden [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device).

-   [**Erstellungscommandqueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : erstellt eine Befehls Warteschlange basierend auf Informationen in der DESC-Struktur einer [**Direct3D 12- \_ Befehls \_ Warteschlange \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) .
-   " [**Kreatecommandlist**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) ": erstellt eine Befehlsliste vom Typ " [**Direct3D 12 \_ Command \_ List \_ Type**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)".
-   [**Kreatefence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) : erstellt einen Fence und notiert die Flags in [**Direct3D 12- \_ fence- \_ Flags**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags). Zum Synchronisieren von Warteschlangen werden Zäune verwendet.

Warteschlangen aller Typen (3D, COMPUTE und Copy) verwenden die gleiche Schnittstelle und sind alle auf der Befehlsliste basierende.

Weitere Informationen finden Sie in den folgenden Methoden von [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue).

-   [**Executecommandlists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) : übermittelt ein Array von Befehlslisten zur Ausführung. Jede durch [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)definierte Befehlsliste.
-   [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) : legt einen Fence Wert fest, wenn die Warteschlange (die auf der GPU ausgeführt wird) einen bestimmten Punkt erreicht.
-   [**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) : die Warteschlange wartet, bis der angegebene Fence den angegebenen Wert erreicht.

Beachten Sie, dass Pakete nicht von Warteschlangen genutzt werden. Daher kann dieser Typ nicht zum Erstellen einer Warteschlange verwendet werden.

### <a name="fences"></a>Zäune

Die Multi-Engine-API stellt explizite APIs zum Erstellen und Synchronisieren mithilfe von Zäunen bereit. Ein Fence ist ein Synchronisierungs Konstrukt, das von einem UINT64-Wert gesteuert wird. Die Fence Werte werden von der Anwendung festgelegt. Durch einen Signal Vorgang werden der Fence-Wert und ein warte Vorgangs Block geändert, bis der Fence den angeforderten Wert erreicht hat. Ein Ereignis kann ausgelöst werden, wenn ein Fence einen bestimmten Wert erreicht.

Weitere Informationen finden Sie in den Methoden der [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) -Schnittstelle.

-   [**Getcompletedvalue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) : gibt den aktuellen Wert des Fence zurück.
-   [](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) "Enumerationsvervollständigen": bewirkt, dass ein Ereignis ausgelöst wird, wenn der Fence einen bestimmten Wert erreicht.
-   [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) : legt den Fence auf den angegebenen Wert fest.

Durch Zäune wird der CPU-Zugriff auf den aktuellen Fence-Wert und CPU-warte Vorgänge und-Signale ermöglicht.

Die [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) -Methode der [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) -Schnittstelle aktualisiert einen Fence von der CPU-Seite. Dieses Update erfolgt sofort. Die [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) -Methode auf [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) aktualisiert einen Fence von der GPU-Seite. Dieses Update erfolgt, nachdem alle anderen Vorgänge in der Befehls Warteschlange abgeschlossen wurden.

Alle Knoten in einem Setup mit mehreren Engines können alle Endpunkte lesen und darauf reagieren, die den richtigen Wert erreichen.

Anwendungen legen ihre eigenen Fence-Werte fest. ein guter Ausgangspunkt könnte einen Fence einmal pro Frame erhöhen.

Ein fence *kann* *zurück* gesetzt werden. Dies bedeutet, dass der Fence-Wert nicht allein erhöht werden muss. Wenn ein **Signal** Vorgang in eine Warteschlange für zwei unterschiedliche Befehls Warteschlangen eingereiht wird, oder wenn zwei CPU-Threads beide als **Signal** an einem Fence aufrufen, kann es zu einem Wettlauf kommen, um zu bestimmen, welches **Signal** zuletzt abgeschlossen wurde, und welcher Fence Wert dem Wert entspricht. Wenn ein Fence regger zurückgesetzt wird, werden alle neuen warte Vorgänge (einschließlich der Anforderungen an den "Abgleich" **) mit dem** neuen niedrigeren Fence-Wert verglichen und daher möglicherweise nicht erfüllt, auch wenn der Fence-Wert zuvor hoch genug war, um Sie zu erfüllen. Wenn ein racevorgang stattfindet, *wird* zwischen einem Wert, der einen ausstehenden warte Vorgang erfüllt, und einem niedrigeren Wert, der nicht ist, der Warte Vorgang unabhängig davon, welcher Wert später verbleibt, erfüllt.

Die Fence-APIs bieten leistungsstarke Synchronisierungs Funktionen, können aber potenziell schwer zu debuggende Probleme führen. Es wird empfohlen, dass jeder Fence nur verwendet wird, um den Fortschritt in einer Zeitachse anzugeben, um die Ausführung von Races zwischen Signal

### <a name="copy-and-compute-command-lists"></a>Befehlslisten "Kopieren" und "Compute"

Alle drei Typen der Befehlsliste verwenden die [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) -Schnittstelle, es wird jedoch nur eine Teilmenge der Methoden für kopieren und berechnen unterstützt.

In den Befehlslisten "Kopieren" und "Compute" können folgende Methoden verwendet werden.

-   [**Schließen**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
-   [**Copybufferregion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**Copyresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**Copytextureregion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**Copytiles**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
-   [**Resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

Compute-Befehlslisten können auch die folgenden Methoden verwenden.

-   [**Clearstate**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
-   [**Clearunorderedaccessviewfloat**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [**Clearunorderedaccessviewuint**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [**Verwerfen von Quelle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
-   [**Dispatch**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [**Executin Direct**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)
-   [**SetComputeRoot32BitConstant**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [**SetComputeRoot32BitConstants**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
-   [**Setcomputerootconstantbufferview**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [**Setcomputerootdescriptor Table**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
-   [**Setcomputerootshaderresourceview**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [**Setcomputerootsignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
-   [**Setcomputerootunorderedaccessview**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [**Setdescriptorheaps**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
-   [**Setpipelinestate**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
-   [**Setprediation**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

Compute-Befehlslisten müssen eine COMPUTE-PSO festlegen, wenn [**setpipelinestate**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)aufgerufen wird.

Bündel können nicht mit COMPUTE-oder Kopier Befehlslisten oder-Warteschlangen verwendet werden.

## <a name="pipelined-compute-and-graphics-example"></a>Beispiel für eine Pipeline und Grafiken mit Pipelines

Dieses Beispiel zeigt, wie die Fence-Synchronisierung verwendet werden kann, um eine Pipeline von computeaufgaben in einer Warteschlange (auf die von verwiesen wird) zu erstellen `pComputeQueue` , die von Grafiken in der Warteschlange genutzt wird `pGraphicsQueue` Die COMPUTE-und Grafik Vorgänge werden mit der Grafik Warteschlange zusammengefasst, die das Ergebnis der computearbeit aus mehreren Frames zurückgibt, und ein CPU-Ereignis wird verwendet, um die Gesamtsumme der Arbeitsauslastung insgesamt zu drosseln.

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

Um diese Pipeline zu unterstützen, muss ein Puffer mit `ComputeGraphicsLatency+1` unterschiedlichen Kopien der Daten vorhanden sein, die von der computewarteschlange an die Grafik Warteschlange übergeben werden. In den Befehlslisten müssen UAVs und Dereferenzierung verwendet werden, um die entsprechende "Version" der Daten im Puffer zu lesen und zu schreiben. Die computewarteschlange muss warten, bis die Grafik Warteschlange das Lesen aus den Daten für Frame N abgeschlossen hat, bevor Frame geschrieben werden kann `N+ComputeGraphicsLatency` .

Beachten Sie, dass die Menge an computewarteschlangen, die relativ zur CPU verwendet werden, nicht direkt von der erforderlichen Puffer Menge abhängig ist. in der Warteschlange von GPU funktioniert die Menge des verfügbaren Puffer Platzes jedoch weniger wertvoll.

Eine alternative Methode, um die Dereferenzierung zu vermeiden, besteht darin, mehrere Befehlslisten zu erstellen, die den "umbenannten" Versionen der Daten entsprechen. Im nächsten Beispiel wird dieses Verfahren verwendet, während das vorherige Beispiel erweitert wird, damit die COMPUTE-und Grafik Warteschlangen asynchron ausgeführt werden können.

## <a name="asynchronous-compute-and-graphics-example"></a>Beispiel für asynchrone COMPUTE und Grafiken

Im nächsten Beispiel wird das asynchrone Rendering von Grafiken aus der computewarteschlange ermöglicht. Zwischen den beiden Phasen besteht immer noch eine Fixed-Menge an gepufferten Daten, die Grafik Arbeit erfolgt jedoch unabhängig voneinander und verwendet das aktuellste Ergebnis der computephase, wenn sich die Grafik Arbeit in der Warteschlange befindet. Dies wäre hilfreich, wenn die Grafik Arbeit von einer anderen Quelle, z. b. Benutzereingaben, aktualisiert wurde. Es müssen mehrere Befehlslisten vorhanden sein, damit die `ComputeGraphicsLatency` Rahmen der Grafik Arbeit gleichzeitig aktiv sein können, und die Funktion `UpdateGraphicsCommandList` stellt das Aktualisieren der Befehlsliste dar, um die neuesten Eingabedaten einzubeziehen und aus den Compute-Daten aus dem entsprechenden Puffer zu lesen.

Die computewarteschlange muss immer noch warten, bis die Grafik Warteschlange mit den pipepuffern fertiggestellt ist, aber es wird ein Dritter fence ( `pGraphicsComputeFence` ) eingeführt, sodass der Fortschritt von Grafiken, die Compute-Arbeit und Grafik Fortschritt im Allgemeinen lesen, verfolgt werden kann Dies spiegelt die Tatsache wider, dass jetzt aufeinander folgende Grafik Frames aus demselben computeergebnis lesen oder ein computeergebnis überspringen könnten. Ein effizienterer, aber etwas komplizierteres Design würde nur den einzelnen Grafik Zaun verwenden und eine Zuordnung zu den von den einzelnen Grafik Frames verwendeten computeframes speichern.

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

## <a name="multi-queue-resource-access"></a>Ressourcen Zugriff mit mehreren Warteschlangen

Für den Zugriff auf eine Ressource in mehr als einer Warteschlange muss eine Anwendung den folgenden Regeln entsprechen.

-   Der Ressourcen Zugriff (siehe [**Direct3D 12 \_ Resource \_ States**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)) wird durch Queue Type class not Queue Object festgelegt. Es gibt zwei Typklassen von Queue: Compute/3D Queue ist eine Typklasse, Copy ist eine zweite Typklasse. Daher kann eine Ressource, die eine Barriere für den \_ Ressourcen Zustand "nicht Pixel- \_ Shader" in \_ einer 3D-Warteschlange aufweist, in diesem Zustand in jeder 3D-oder computewarteschlange verwendet werden, je nach Synchronisierungs Anforderungen, bei denen die meisten Schreibvorgänge serialisiert werden müssen. Die Ressourcen Zustände, die von den beiden Typklassen gemeinsam genutzt werden (Kopier \_ Quelle und Kopie \_ dest), werden für jede Typklasse als unterschiedliche Zustände angesehen. Wenn also eine Ressource in einer Kopier Warteschlange zum Kopieren dest wechselt, kann \_ Sie nicht als Kopier Ziel aus 3D-oder computewarteschlangen und umgekehrt aufgerufen werden.

    Zusammenfassend.

    -   Ein Warteschlangen Objekt ist eine beliebige einzelne Warteschlange.
    -   Eine Warteschlange "Type" ist eine dieser drei: COMPUTE, 3D und Copy.
    -   Eine Warteschlange "Type class" ist eine der folgenden beiden: Compute/3D und Copy.

-   Die als Ausgangszustände verwendeten kopierflags (Kopie \_ dest und Copy \_ Source) stellen Zustände in der 3D/Compute Type-Klasse dar. Um eine Ressource anfänglich in einer Kopier Warteschlange zu verwenden, sollte Sie im allgemeinen Zustand beginnen. Der gemeinsame Zustand kann für alle Verwendungen in einer Kopier Warteschlange mithilfe der impliziten Zustandsübergänge verwendet werden. 
-   Obwohl der Ressourcen Status über alle Compute-und 3D-Warteschlangen hinweg gemeinsam genutzt wird, ist es nicht zulässig, gleichzeitig in verschiedene Warteschlangen in die Ressource zu schreiben. "Gleichzeitig" bedeutet "nicht synchronisiert", was bedeutet, dass die nicht synchronisierte Ausführung auf bestimmter Hardware nicht möglich ist. Die folgenden Regeln gelten.

    -   Nur eine Warteschlange kann gleichzeitig in eine Ressource schreiben.
    -   Mehrere Warteschlangen können aus der Ressource lesen, solange Sie nicht die vom Writer geänderten Bytes lesen (das Lesen von gleichzeitig geschriebenen Bytes erzeugt nicht definierte Ergebnisse).
    -   Ein Fence muss verwendet werden, um nach dem Schreiben zu synchronisieren, bevor eine andere Warteschlange die geschriebenen Bytes lesen oder Schreibzugriffe ausführen kann.

-   Die angezeigten backpuffer müssen sich im Status "Direct3D 12" im \_ Ressourcen Status "Allgemein" befinden \_ \_ . 

## <a name="related-topics"></a>Verwandte Themen

[Direct3D 12-Programmieranleitung](directx-12-programming-guide.md)

[Verwenden von Ressourcen Barrieren zum Synchronisieren von Ressourcen Zuständen in Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

[Arbeitsspeicherverwaltung in Direct3D 12](memory-management.md)
