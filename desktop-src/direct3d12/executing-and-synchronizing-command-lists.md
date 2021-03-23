---
title: Ausführen und Synchronisieren von Befehlslisten
description: In Microsoft Direct3D 12 ist der unmittelbare Modus vorheriger Versionen nicht mehr vorhanden.
ms.assetid: D5013102-2302-4D66-8F59-079C03BA65FD
keywords:
- Befehlsliste
- Synchronisierung
- Ausführung
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ef910463ba3a771ac142d41309ae590884e3bc9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548756"
---
# <a name="executing-and-synchronizing-command-lists"></a>Ausführen und Synchronisieren von Befehlslisten

In Microsoft Direct3D 12 ist der unmittelbare Modus vorheriger Versionen nicht mehr vorhanden. Stattdessen erstellen apps Befehlslisten und Pakete und zeichnen dann Sätze von GPU-Befehlen auf. Befehls Warteschlangen werden verwendet, um auszuführende Befehlslisten zu übermitteln. Dieses Modell ermöglicht Entwicklern eine bessere Kontrolle über die effiziente Nutzung von GPU (Graphics Processing Unit) und CPU.

-   [Befehls Warteschlange](#command-queue-overview)
-   [Initialisieren einer Befehls Warteschlange](#initializing-a-command-queue)
-   [Ausführen von Befehlslisten](#executing-command-lists)
-   [Zugreifen auf Ressourcen aus mehreren Befehls Warteschlangen](#accessing-resources-from-multiple-command-queues)
-   [Synchronisieren der Befehlslisten Ausführung mithilfe von Befehlen der Befehls Warteschlange](#synchronizing-command-list-execution-using-command-queue-fences)
-   [Synchronisieren von Ressourcen, auf die über Befehls Warteschlangen zugegriffen](#synchronizing-resources-accessed-by-command-queues)
-   [Unterstützung der Befehls Warteschlange für Kachel Ressourcen](#command-queue-support-for-tiled-resources)
-   [Verwandte Themen](#related-topics)

## <a name="command-queue-overview"></a>Befehls Warteschlange

Direct3D 12-Befehls Warteschlangen ersetzen die Laufzeit-und Treiber Synchronisierung der Arbeits Übermittlung im unmittelbaren Modus, die zuvor nicht für den Entwickler verfügbar gemacht wurde, mit APIs für die explizite Verwaltung von Parallelität, Parallelität und Synchronisierung Befehls Warteschlangen bieten die folgenden Verbesserungen für Entwickler:

-   Ermöglicht Entwicklern die Vermeidung zufälliger Ineffizienzen, die durch eine unerwartete Synchronisierung verursacht werden
-   Ermöglicht es Entwicklern, die Synchronisierung auf einer höheren Ebene einzuführen, bei der die erforderliche Synchronisierung effizienter und präziser ermittelt werden kann. Dies bedeutet, dass die Laufzeit und der Grafiktreiber weniger Zeit für eine reaktive Engineering-Parallelität aufwenden.
-   Macht teure Vorgänge expliziter.

Diese Verbesserungen aktivieren oder verbessern die folgenden Szenarien:

-   Erhöhter Parallelität: Anwendungen können tiefere Warteschlangen für hintergrundworkloads verwenden, wie z. b. Video Decodierung, wenn Sie über separate Warteschlangen für Vordergrund arbeiten verfügen.
-   Asynchrone GPU-Arbeit mit niedriger Priorität: das Befehls Warteschlangen Modell ermöglicht die gleichzeitige Ausführung von GPU-arbeiten mit niedriger Priorität und atomarische Vorgänge, mit denen ein GPU-Thread die Ergebnisse eines anderen nicht synchronisierten Threads nutzen kann, ohne zu blockieren.
-   Computearbeit mit hoher Priorität: dieser Entwurf ermöglicht Szenarien, in denen das Unterbrechen von 3D-Rendering erforderlich ist, um eine kleine Menge von computeaufgaben mit hoher Priorität zu erledigen, damit das Ergebnis frühzeitig zur weiteren Verarbeitung auf der CPU abgerufen werden kann.

## <a name="initializing-a-command-queue"></a>Initialisieren einer Befehls Warteschlange

Befehls Warteschlangen können durch Aufrufen von [**ID3D12Device:: createcommandqueue**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)erstellt werden. Diese Methode nimmt einen [**D3D12 \_ - \_ Befehls \_ auflistentyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type) an, der angibt, welcher Typ von Warteschlange erstellt werden soll. Daher können Sie den Typ der Befehle an diese Warteschlange senden. Beachten Sie, dass Pakete nur von direkten Befehlslisten aufgerufen werden können und nicht direkt an eine Warteschlange übermittelt werden können. Folgende Warteschlangen Typen werden unterstützt:

-   [**D3D12 \_ Command \_ List \_ Type \_ Direct**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)
-   [**D3D12 \_ Befehls \_ List \_ Type \_ Compute**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)
-   [**D3D12 \_ - \_ Befehls \_ Auflistungstyp \_ Kopieren**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)

Im allgemeinen akzeptieren direkte Warteschlangen und Befehlslisten alle Befehle, computewarteschlangen und Befehlslisten, die COMPUTE-und Kopier bezogene Befehle akzeptieren, und Kopier Warteschlangen und Befehlslisten akzeptieren nur Kopier Befehle.

## <a name="executing-command-lists"></a>Ausführen von Befehlslisten

Nachdem Sie eine Befehlsliste aufgezeichnet und entweder die Standard Befehls Warteschlange abgerufen oder eine neue erstellt haben, führen Sie Befehlslisten durch Aufrufen von [**ID3D12CommandQueue:: executecommandlists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)aus.

Anwendungen können Befehlslisten an eine beliebige Befehls Warteschlange aus mehreren Threads übermitteln. Die Laufzeit führt die Serialisierung dieser Anforderungen in der Reihenfolge der Übermittlung durch.

Die Laufzeit überprüft die übermittelte Befehlsliste und löscht den Aufrufen von [**executecommandlists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) , wenn eine der Einschränkungen verletzt wird. Aufrufe werden aus den folgenden Gründen gelöscht:

-   Die angegebene Befehlsliste ist ein Bündel und keine direkte Befehlsliste.
-   [**ID3D12GraphicsCommandList:: Close**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close) wurde nicht in der angegebenen Befehlsliste aufgerufen, um die Aufzeichnung abzuschließen.
-   [**ID3D12CommandAllocator:: Reset**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandallocator-reset) wurde für den Befehls Zuweiser aufgerufen, der der Befehlsliste zugeordnet ist, seit Sie aufgezeichnet wurde. Weitere Informationen zu Befehls Zuweisungen finden Sie unter [Erstellen und Aufzeichnen von Befehlslisten und Paketen](recording-command-lists-and-bundles.md).
-   Der Fence der Befehls Warteschlange gibt an, dass eine vorherige Ausführung der Befehlsliste noch nicht abgeschlossen wurde. Die Zäune der Befehls Warteschlange werden im folgenden ausführlich erläutert.
-   Die vorher-und nachher-Zustände von Abfragen, die mit Aufrufen von [**ID3D12GraphicsCommandList:: beginquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) und [**ID3D12GraphicsCommandList:: endquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)festgelegt wurden, werden nicht ordnungsgemäß abgeglichen.
-   Die vorher-und After-Zustände von Ressourcen Übergangs Barrieren werden nicht ordnungsgemäß abgeglichen. Weitere Informationen finden Sie unter [Verwenden von Ressourcen Barrieren zum Synchronisieren von Ressourcen Zuständen](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).

## <a name="accessing-resources-from-multiple-command-queues"></a>Zugreifen auf Ressourcen aus mehreren Befehls Warteschlangen

Es gibt einige Regeln, die von der Laufzeit erzwungen werden, die den Zugriff von Ressourcen aus mehreren Befehls Warteschlangen einschränken. Nachfolgend sind diese Regeln aufgeführt:

<dl> 1. Eine Ressource kann nicht gleichzeitig aus mehreren Befehls Warteschlangen geschrieben werden. Wenn eine Ressource in einen beschreibbaren Zustand für eine Warteschlange gewechselt hat, wird Sie als exklusiv im Besitz dieser Warteschlange betrachtet und muss in einen Lese-oder gemeinsamen Zustand übergehen (siehe <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">**D3D12 \_ Resource \_ States**</a>), bevor Sie von einer anderen Warteschlange aufgerufen werden kann.  </dl>
<dl> 2. Im Lese Zustand kann eine Ressource auf der Grundlage ihres Lese Zustands gleichzeitig aus mehreren Befehls Warteschlangen gelesen werden. Dies gilt auch für prozessübergreifende Vorgänge. </dl>

Weitere Informationen zu Ressourcen Zugriffsbeschränkungen und zum Verwenden von Ressourcen Barrieren zum Synchronisieren des Zugriffs auf Ressourcen finden [Sie unter Verwenden von Ressourcen Sperren zum Synchronisieren von Ressourcen Zuständen](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).

## <a name="synchronizing-command-list-execution-using-command-queue-fences"></a>Synchronisieren der Befehlslisten Ausführung mithilfe von Befehlen der Befehls Warteschlange

Die Unterstützung mehrerer paralleler Befehls Warteschlangen in Direct3D 12 bietet Ihnen mehr Flexibilität und Kontrolle über die Priorisierung der asynchronen Arbeit auf der GPU. Dies bedeutet auch, dass Apps die Synchronisierung der Arbeit explizit verwalten müssen. Dies gilt insbesondere dann, wenn die Befehlslisten in einer Warteschlange von Ressourcen abhängen, die von einer anderen Befehls Warteschlange betrieben werden. Einige Beispiele hierfür sind z. b. das warten auf den Abschluss eines Vorgangs in einer computewarteschlange, damit das Ergebnis für einen Renderingvorgang in der 3D-Warteschlange verwendet werden kann und auf den Abschluss eines 3D-Vorgangs gewartet wird, damit ein Vorgang in der computewarteschlange auf eine Ressource zum Schreiben zugreifen kann Zum Aktivieren der Synchronisierung von Arbeit zwischen Warteschlangen verwendet Direct3D 12 das Konzept von Zäunen, die von der [**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence) -Schnittstelle in der API dargestellt werden.

Ein Fence ist eine ganze Zahl, die die aktuelle Arbeitseinheit darstellt, die verarbeitet wird. Wenn die APP den Fence durch Aufrufen von [**ID3D12CommandQueue:: Signal**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal)verschiebt, wird die ganze Zahl aktualisiert. Apps können den Wert eines Fence überprüfen und bestimmen, ob eine Arbeitseinheit abgeschlossen wurde, um zu entscheiden, ob ein nachfolgende Vorgang gestartet werden kann.

## <a name="synchronizing-resources-accessed-by-command-queues"></a>Synchronisieren von Ressourcen, auf die über Befehls Warteschlangen zugegriffen

In Direct3D 12 wird die Synchronisierung des Zustands einiger Ressourcen mit Ressourcen Barrieren implementiert. An jeder Ressourcen Barriere deklariert eine APP den Zustand "Before" und "After" einer Ressource. Ein gängiges Beispiel ist, dass eine Ressource zwischen einer Shader-Ressourcen Ansicht und einer renderzielansicht übergeht. In den meisten Fällen werden diese Ressourcen Barrieren innerhalb von Befehlslisten verwaltet. Wenn die debugschichten aktiviert sind, erzwingt das System, dass die vorher-und nach-Zustände aller Ressourcen einander entsprechen. Dadurch wird sichergestellt, dass die Ressource für einen bestimmten Vorgang bei einem Sperrungs Übergang den richtigen Status aufweist.

Weitere Informationen zum Synchronisieren des Ressourcen Zustands finden Sie unter [Verwenden von Ressourcen Sperren zum Synchronisieren von Ressourcen Zuständen](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).

## <a name="command-queue-support-for-tiled-resources"></a>Unterstützung der Befehls Warteschlange für Kachel Ressourcen

Methoden zum Verwalten von gekachelten Ressourcen, die über die [**ID3D11DeviceContext2**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) -Schnittstelle in Direct3D 11 verfügbar gemacht wurden, werden von der [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) -Schnittstelle in Direct3D 12 bereitgestellt. Diese Methoden umfassen:



| Methode                                                              | Beschreibung                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**Copytilemappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings)     | Kopiert Zuordnungen aus einer Ressource mit Kachel Kachel in eine gekachelte Ziel Ressource.<br/>                 |
| [**Updatetilemappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) | Aktualisiert Zuordnungen von Kachel Positionen in gekachelten Ressourcen an Speicherorte in einem Ressourcenheap.<br/> |



 

Weitere Informationen zum Verwenden von gekachelten Ressourcen in Direct3D 12-apps finden Sie unter [Direct3D11-Kachel Ressourcen](/windows/desktop/direct3d11/tiled-resources).

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Arbeits Übermittlung in Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

