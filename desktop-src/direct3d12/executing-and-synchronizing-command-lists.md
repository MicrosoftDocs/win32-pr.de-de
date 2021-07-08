---
title: Ausführen und Synchronisieren von Befehlslisten
description: In Microsoft Direct3D 12 ist der unmittelbaren Modus vorheriger Versionen nicht mehr vorhanden.
ms.assetid: D5013102-2302-4D66-8F59-079C03BA65FD
keywords:
- Befehlsliste
- Synchronisierung
- Ausführung
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d5362d0f093c7c1034e03d396ad28c40d4d600
ms.sourcegitcommit: 170bc12e9724d00cecbb96d57c7226c51e135dee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "113489179"
---
# <a name="executing-and-synchronizing-command-lists"></a>Ausführen und Synchronisieren von Befehlslisten

In Microsoft Direct3D 12 ist der unmittelbaren Modus vorheriger Versionen nicht mehr vorhanden. Stattdessen erstellen Apps Befehlslisten und Bündel und zeichnen dann Gruppen von GPU-Befehlen auf. Befehlswarteschlangen werden zum Übermitteln von Befehlslisten verwendet, die ausgeführt werden sollen. Dieses Modell ermöglicht Entwicklern mehr Kontrolle über die effiziente Nutzung von Grafikprozessor (GRAPHICS Processing Unit, GPU) und CPU.

-   [Übersicht über die Befehlswarteschlange](#command-queue-overview)
-   [Initialisieren einer Befehlswarteschlange](#initializing-a-command-queue)
-   [Ausführen von Befehlslisten](#executing-command-lists)
-   [Zugreifen auf Ressourcen aus mehreren Befehlswarteschlangen](#accessing-resources-from-multiple-command-queues)
-   [Synchronisieren der Befehlslistenausführung mithilfe von Befehlswarteschlangen-Fences](#synchronizing-command-list-execution-using-command-queue-fences)
-   [Synchronisieren von Ressourcen, auf die von Befehlswarteschlangen zugegriffen wird](#synchronizing-resources-accessed-by-command-queues)
-   [Unterstützung von Befehlswarteschlangen für gekachelte Ressourcen](#command-queue-support-for-tiled-resources)
-   [Verwandte Themen](#related-topics)

## <a name="command-queue-overview"></a>Übersicht über die Befehlswarteschlange

Direct3D 12-Befehlswarteschlangen ersetzen die Laufzeit- und Treibersynchronisierung der Direktmodus-Arbeitsübermittlung, die dem Entwickler zuvor nicht zur Verfügung gestellt wurde, durch APIs für die explizite Verwaltung von Parallelität, Parallelität und Synchronisierung. Befehlswarteschlangen bieten Entwicklern die folgenden Verbesserungen:

-   Ermöglicht Es Entwicklern, versehentliche Ineffizienzen zu vermeiden, die durch unerwartete Synchronisierung verursacht werden.
-   Ermöglicht Entwicklern, die Synchronisierung auf einer höheren Ebene einzuführen, auf der die erforderliche Synchronisierung effizienter und genauer bestimmt werden kann. Dies bedeutet, dass die Runtime und der Grafiktreiber weniger Zeit damit verbringen, reaktiv Parallelität zu erstellen.
-   Macht teure Vorgänge expliziter.

Diese Verbesserungen ermöglichen oder verbessern die folgenden Szenarien:

-   Erhöhte Parallelität: Anwendungen können tiefere Warteschlangen für Hintergrundworkloads wie die Videodecodierung verwenden, wenn sie separate Warteschlangen für die Arbeit im Vordergrund haben.
-   Asynchrone GPU-Arbeit mit niedriger Priorität: Das Befehlswarteschlangenmodell ermöglicht die gleichzeitige Ausführung von GPU-Arbeitsvorgängen mit niedriger Priorität und atomaren Vorgängen, die es einem GPU-Thread ermöglichen, die Ergebnisse eines anderen nicht synchronisierten Threads ohne Blockierung zu nutzen.
-   Computearbeit mit hoher Priorität: Dieser Entwurf ermöglicht Szenarien, bei denen das 3D-Rendering unterbrochen werden muss, um eine geringe Menge an Computearbeit mit hoher Priorität zu verarbeiten, damit das Ergebnis frühzeitig für eine zusätzliche Verarbeitung auf der CPU erzielt werden kann.

## <a name="initializing-a-command-queue"></a>Initialisieren einer Befehlswarteschlange

Befehlswarteschlangen können durch Aufrufen von [**ID3D12Device::CreateCommandQueue erstellt werden.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) Diese Methode verwendet einen [**D3D12 \_ COMMAND \_ LIST \_ TYPE,**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type) der angibt, welcher Warteschlangentyp erstellt werden soll und welcher Befehlstyp an diese Warteschlange übermittelt werden kann. Denken Sie daran, dass Bundles nur über direkte Befehlslisten aufgerufen und nicht direkt an eine Warteschlange übermittelt werden können. Die folgenden Warteschlangentypen werden unterstützt:

-   [**D3D12 \_ COMMAND \_ LIST \_ TYPE \_ DIRECT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)
-   [**D3D12 \_ \_ BEFEHLSLISTENTYP \_ \_ COMPUTE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)
-   [**D3D12 \_ BEFEHLSLISTE \_ \_ TYP \_ KOPIEREN**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)

Im Allgemeinen akzeptieren DIRECT-Warteschlangen und Befehlslisten alle Befehle, COMPUTE-Warteschlangen und Befehlslisten akzeptieren Compute- und Kopierbefehle, und COPY-Warteschlangen und Befehlslisten akzeptieren nur Kopierbefehle.

## <a name="executing-command-lists"></a>Ausführen von Befehlslisten

Nachdem Sie eine Befehlsliste aufgezeichnet und entweder die Standardbefehlswarteschlange abgerufen oder eine neue erstellt haben, führen Sie Befehlslisten aus, indem Sie [**ID3D12CommandQueue::ExecuteCommandLists aufrufen.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)

Anwendungen können Befehlslisten aus mehreren Threads an eine beliebige Befehlswarteschlange übermitteln. Die Runtime führt die Serialisierung dieser Anforderungen in der Reihenfolge der Übermittlung durch.

Die Runtime überprüft die übermittelte Befehlsliste und gibt den Aufruf von [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) zurück, wenn eine der Einschränkungen verletzt wird. Aufrufe werden aus den folgenden Gründen gelöscht:

-   Die angegebene Befehlsliste ist ein Paket, keine direkte Befehlsliste.
-   [**ID3D12GraphicsCommandList::Close**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close) wurde in der angegebenen Befehlsliste nicht aufgerufen, um die Aufzeichnung abschließen zu können.
-   [**ID3D12CommandAllocator::Reset**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandallocator-reset) wurde für die Befehlszuweisung aufgerufen, die der Befehlsliste zugeordnet ist, seit sie aufgezeichnet wurde. Weitere Informationen zu Befehlszuweisungen finden Sie unter Erstellen und Aufzeichnen [von Befehlslisten und Paketen.](recording-command-lists-and-bundles.md)
-   Der Fence der Befehlswarteschlange gibt an, dass eine vorherige Ausführung der Befehlsliste noch nicht abgeschlossen wurde. Befehlswarteschlangen-Fences werden unten ausführlich erläutert.
-   Die Zustände vor und nach Abfragen, die mit Aufrufen von [**ID3D12GraphicsCommandList::BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) und [**ID3D12GraphicsCommandList::EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)festgelegt werden, werden nicht ordnungsgemäß abgefragt.
-   Die Zustände vor und nach dem Übergang von Ressourcen werden nicht ordnungsgemäß übereinstimmen. Weitere Informationen finden Sie unter [Verwenden von Ressourcenbarrieren zum Synchronisieren von Ressourcenzuständen.](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

## <a name="accessing-resources-from-multiple-command-queues"></a>Zugreifen auf Ressourcen aus mehreren Befehlswarteschlangen

Es gibt eine Reihe von Regeln, die von der Runtime festgelegt werden, die den Zugriff auf Ressourcen aus mehreren Befehlswarteschlangen einschränken. Nachfolgend sind diese Regeln aufgeführt:

1. Eine Ressource kann nicht gleichzeitig aus mehreren Befehlswarteschlangen in geschrieben werden. Wenn eine Ressource in einen schreibbaren Zustand in einer Warteschlange übergeführt wurde, gilt sie als ausschließlich im Besitz dieser Warteschlange und muss in einen Lese- oder COMMON-Zustand (siehe [**D3D12_RESOURCE_STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)) überwechseln, bevor eine andere Warteschlange darauf zugreifen kann.

2. In einem Lesezustand kann eine Ressource basierend auf ihrem Lesezustand gleichzeitig aus mehreren Befehlswarteschlangen gelesen werden, auch prozessübergreifend.

Weitere Informationen zu Ressourcenzugriffseinschränkungen und zur Verwendung von Ressourcenbarrieren zum Synchronisieren des Zugriffs auf Ressourcen finden Sie unter Verwenden von [Ressourcenbarrieren zum Synchronisieren von Ressourcenzuständen.](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

## <a name="synchronizing-command-list-execution-using-command-queue-fences"></a>Synchronisieren der Befehlslistenausführung mithilfe von Befehlswarteschlangen-Fences

Die Unterstützung mehrerer paralleler Befehlswarteschlangen in Direct3D 12 bietet Ihnen mehr Flexibilität und Kontrolle über die Priorisierung asynchroner Arbeit auf der GPU. Dieser Entwurf bedeutet auch, dass Apps die Synchronisierung der Arbeit explizit verwalten müssen, insbesondere wenn die Befehlslisten in einer Warteschlange von Ressourcen abhängen, die von einer anderen Befehlswarteschlange betrieben werden. Beispiele hierfür sind das Warten auf den Abschluss eines Vorgangs in einer Computewarteschlange, sodass das Ergebnis für einen Renderingvorgang in der 3D-Warteschlange verwendet werden kann, und das Warten auf den Abschluss eines 3D-Vorgangs, damit ein Vorgang in der Computewarteschlange auf eine Ressource zum Schreiben zugreifen kann. Um die Synchronisierung der Arbeit zwischen Warteschlangen zu ermöglichen, verwendet Direct3D 12 das Konzept der Umhängungen, die in der API durch die [**ID3D12Fence-Schnittstelle**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence) dargestellt werden.

Ein Fence ist eine ganze Zahl, die die aktuelle Arbeitseinheit darstellt, die verarbeitet wird. Wenn die App den Fence durch Aufrufen von [**ID3D12CommandQueue::Signal**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal)übergibt, wird die ganze Zahl aktualisiert. Apps können den Wert eines Fence überprüfen und ermitteln, ob eine Arbeitseinheit abgeschlossen wurde, um zu entscheiden, ob ein nachfolgender Vorgang gestartet werden kann.

## <a name="synchronizing-resources-accessed-by-command-queues"></a>Synchronisieren von Ressourcen, auf die von Befehlswarteschlangen zugegriffen wird

In Direct3D 12 wird die Synchronisierung des Zustands einiger Ressourcen mit Ressourcenbarrieren implementiert. Bei jeder Ressourcenbarriere deklariert eine App die Zustände vor und nach einer Ressource. Ein gängiges Beispiel ist der Übergang einer Ressource zwischen einer Shaderressourcenansicht und einer Renderzielansicht. Diese Ressourcenbarrieren werden größtenfalls in Befehlslisten verwaltet. Wenn die Debugebenen aktiviert sind, erzwingt das System, dass die Zustände vor und nach allen Ressourcen übereinstimmen, um zu gewährleisten, dass sich die Ressource bei einem Übergang zu einer Barriere im richtigen Zustand befindet.

Weitere Informationen zum Synchronisieren des Ressourcenzustands finden Sie unter [Verwenden von Ressourcenbarrieren zum Synchronisieren von Ressourcenzuständen.](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

## <a name="command-queue-support-for-tiled-resources"></a>Unterstützung von Befehlswarteschlangen für gekachelte Ressourcen

Methoden zum Verwalten von gekachelten Ressourcen, die über die [**ID3D11DeviceContext2-Schnittstelle**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) in Direct3D 11 verfügbar gemacht wurden, werden von der [**ID3D12CommandQueue-Schnittstelle**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) in Direct3D 12 bereitgestellt. Diese Methoden umfassen:



| Methode                                                              | Beschreibung                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**CopyTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings)     | Kopiert Zuordnungen aus einer gekachelten Quellressource in eine gekachelte Zielressource.<br/>                 |
| [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) | Aktualisiert Zuordnungen von Kachelspeicherorten in gekachelten Ressourcen zu Speicherspeicherorten in einem Ressourcenhap.<br/> |



 

Weitere Informationen zur Verwendung von gekachelten Ressourcen in Direct3D 12-Apps finden Sie unter [Direct3D11 Tiled Resources](/windows/desktop/direct3d11/tiled-resources).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeitsübermittlung in Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

