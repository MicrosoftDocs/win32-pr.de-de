---
title: Ausführen und Synchronisieren von Befehlslisten
description: In Microsoft Direct3D 12 ist der direkte Modus früherer Versionen nicht mehr vorhanden.
ms.assetid: D5013102-2302-4D66-8F59-079C03BA65FD
keywords:
- Befehlsliste
- Synchronisierung
- Ausführung
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b41677ee1bc17fb2a935f157d969352617c0d5c3c15eb38a76225b3a8c71e7f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118529140"
---
# <a name="executing-and-synchronizing-command-lists"></a>Ausführen und Synchronisieren von Befehlslisten

In Microsoft Direct3D 12 ist der direkte Modus früherer Versionen nicht mehr vorhanden. Stattdessen erstellen Apps Befehlslisten und Bündel und zeichnen dann Sätze von GPU-Befehlen auf. Befehlswarteschlangen werden verwendet, um Befehlslisten zu übermitteln, die ausgeführt werden sollen. Dieses Modell ermöglicht Entwicklern mehr Kontrolle über die effiziente Nutzung von GRAFIKPROZESSOR (Graphics Processing Unit, GPU) und CPU.

-   [Übersicht über die Befehlswarteschlange](#command-queue-overview)
-   [Initialisieren einer Befehlswarteschlange](#initializing-a-command-queue)
-   [Ausführen von Befehlslisten](#executing-command-lists)
-   [Zugreifen auf Ressourcen aus mehreren Befehlswarteschlangen](#accessing-resources-from-multiple-command-queues)
-   [Synchronisieren der Ausführung von Befehlslisten mit Befehlswarteschlangen-Umgrenzungen](#synchronizing-command-list-execution-using-command-queue-fences)
-   [Synchronisieren von Ressourcen, auf die von Befehlswarteschlangen zugegriffen wird](#synchronizing-resources-accessed-by-command-queues)
-   [Unterstützung der Befehlswarteschlange für gekachelte Ressourcen](#command-queue-support-for-tiled-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="command-queue-overview"></a>Übersicht über die Befehlswarteschlange

Direct3D 12-Befehlswarteschlangen ersetzen die Laufzeit- und Treibersynchronisierung der Unmittelbarmodus-Arbeitsübermittlung, die dem Entwickler zuvor nicht verfügbar gemacht wurde, durch APIs für die explizite Verwaltung von Parallelität, Parallelität und Synchronisierung. Befehlswarteschlangen bieten Entwicklern die folgenden Verbesserungen:

-   Ermöglicht Entwicklern, versehentliche Ineffizienzen zu vermeiden, die durch unerwartete Synchronisierung verursacht werden.
-   Ermöglicht Es Entwicklern, die Synchronisierung auf einer höheren Ebene einzuführen, wo die erforderliche Synchronisierung effizienter und genauer bestimmt werden kann. Dies bedeutet, dass die Runtime und der Grafiktreiber weniger Zeit für die reaktive Entwicklung von Parallelität aufwenden.
-   Macht teurere Vorgänge expliziter.

Diese Verbesserungen ermöglichen oder verbessern die folgenden Szenarien:

-   Erhöhte Parallelität: Anwendungen können tiefere Warteschlangen für Hintergrundworkloads verwenden, z. B. die Videodecodierung, wenn sie separate Warteschlangen für die Vordergrundarbeit haben.
-   Asynchrone und GPU-Arbeit mit niedriger Priorität: Das Befehlswarteschlangenmodell ermöglicht die gleichzeitige Ausführung von GPU-Vorgängen mit niedriger Priorität und atomaren Vorgängen, die es einem GPU-Thread ermöglichen, die Ergebnisse eines anderen nicht synchronisierten Threads ohne Blockierung zu nutzen.
-   Computearbeit mit hoher Priorität: Dieser Entwurf ermöglicht Szenarien, die eine Unterbrechung des 3D-Renderings erfordern, um eine kleine Menge an Computearbeit mit hoher Priorität zu erledigen, sodass das Ergebnis frühzeitig für zusätzliche Verarbeitung auf der CPU abgerufen werden kann.

## <a name="initializing-a-command-queue"></a>Initialisieren einer Befehlswarteschlange

Befehlswarteschlangen können durch Aufrufen von [**ID3D12Device::CreateCommandQueue**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)erstellt werden. Diese Methode verwendet einen [**D3D12 \_ COMMAND \_ LIST \_ TYPE,**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type) der angibt, welcher Warteschlangentyp erstellt werden soll und daher welcher Typ von Befehlen an diese Warteschlange übermittelt werden kann. Denken Sie daran, dass Pakete nur aus direkten Befehlslisten aufgerufen und nicht direkt an eine Warteschlange übermittelt werden können. Folgende Warteschlangentypen werden unterstützt:

-   [**D3D12 \_ COMMAND \_ LIST \_ TYPE \_ DIRECT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)
-   [**\_D3D12-BEFEHLSLISTENTYP \_ \_ \_ COMPUTE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)
-   [**\_D3D12-BEFEHLSLISTENTYP \_ \_ \_ KOPIEREN**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)

Im Allgemeinen akzeptieren DIRECT-Warteschlangen und Befehlslisten alle Befehle, COMPUTE-Warteschlangen und Befehlslisten Compute- und Kopierbefehle, und COPY-Warteschlangen und Befehlslisten akzeptieren nur Kopierbefehle.

## <a name="executing-command-lists"></a>Ausführen von Befehlslisten

Nachdem Sie eine Befehlsliste aufgezeichnet und entweder die Standardbefehlswarteschlange abgerufen oder eine neue erstellt haben, führen Sie Befehlslisten aus, indem Sie [**ID3D12CommandQueue::ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)aufrufen.

Anwendungen können Befehlslisten aus mehreren Threads an eine beliebige Befehlswarteschlange übermitteln. Die Runtime führt die Serialisierung dieser Anforderungen in der Reihenfolge der Übermittlung durch.

Die Runtime überprüft die übermittelte Befehlsliste und verwerfen den Aufruf von [**ExecuteCommandLists,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) wenn eine der Einschränkungen verletzt wird. Aufrufe werden aus folgenden Gründen gelöscht:

-   Die angegebene Befehlsliste ist ein Bündel, keine direkte Befehlsliste.
-   [**ID3D12GraphicsCommandList::Close**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close) wurde in der angegebenen Befehlsliste nicht aufgerufen, um die Aufzeichnung abzuschließen.
-   [**ID3D12CommandAllocator::Reset**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandallocator-reset) wurde für die Befehlsbelegung aufgerufen, die der Befehlsliste zugeordnet ist, seit sie aufgezeichnet wurde. Weitere Informationen zu Befehlszuweisungen finden Sie unter [Erstellen und Aufzeichnen von Befehlslisten und Paketen.](recording-command-lists-and-bundles.md)
-   Der Befehlswarteschlangen-Fence gibt an, dass eine vorherige Ausführung der Befehlsliste noch nicht abgeschlossen wurde. Befehlswarteschlangen-Umgrenzungen werden im Folgenden ausführlich erläutert.
-   Die Vor- und Nachher-Zustände von Abfragen, die mit Aufrufen von [**ID3D12GraphicsCommandList::BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) und [**ID3D12GraphicsCommandList::EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)festgelegt wurden, werden nicht ordnungsgemäß abgegleichen.
-   Die Vorher- und Nachher-Zustände von Ressourcenübergangsbarrieren werden nicht ordnungsgemäß abgegleichen. Weitere Informationen finden Sie unter [Verwenden von Ressourcenbarrieren zum Synchronisieren von Ressourcenzuständen.](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

## <a name="accessing-resources-from-multiple-command-queues"></a>Zugreifen auf Ressourcen aus mehreren Befehlswarteschlangen

Es gibt einige Regeln, die von der Laufzeit erzwungen werden, die den Zugriff auf Ressourcen aus mehreren Befehlswarteschlangen einschränken. Nachfolgend sind diese Regeln aufgeführt:

1. Eine Ressource kann nicht gleichzeitig aus mehreren Befehlswarteschlangen in geschrieben werden. Wenn eine Ressource in einen beschreibbaren Zustand in einer Warteschlange übergegangen ist, gilt sie als ausschließlich im Besitz dieser Warteschlange und muss in einen Lese- oder COMMON-Zustand (siehe [**D3D12_RESOURCE_STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)) übergehen, bevor von einer anderen Warteschlange darauf zugegriffen werden kann.

2. Wenn sich eine Ressource in einem Lesezustand befindet, kann sie basierend auf ihrem Lesezustand gleichzeitig aus mehreren Befehlswarteschlangen gelesen werden, einschließlich prozessübergreifender Warteschlangen.

Weitere Informationen zu Ressourcenzugriffseinschränkungen und zur Verwendung von Ressourcenbarrieren zum Synchronisieren des Zugriffs auf Ressourcen finden Sie unter [Verwenden von Ressourcenbarrieren zum Synchronisieren von Ressourcenzuständen.](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

## <a name="synchronizing-command-list-execution-using-command-queue-fences"></a>Synchronisieren der Ausführung von Befehlslisten mit Befehlswarteschlangen-Umgrenzungen

Die Unterstützung für mehrere parallele Befehlswarteschlangen in Direct3D 12 bietet Ihnen mehr Flexibilität und Kontrolle über die Priorisierung asynchroner Arbeit auf der GPU. Dieser Entwurf bedeutet auch, dass Apps die Arbeitssynchronisierung explizit verwalten müssen, insbesondere wenn die Befehlslisten in einer Warteschlange von Ressourcen abhängen, die von einer anderen Befehlswarteschlange betrieben werden. Beispiele hierfür sind das Warten auf den Abschluss eines Vorgangs in einer Computewarteschlange, damit das Ergebnis für einen Renderingvorgang in der 3D-Warteschlange verwendet werden kann, und das Warten auf den Abschluss eines 3D-Vorgangs, damit ein Vorgang in der Computewarteschlange auf eine Ressource zum Schreiben zugreifen kann. Um die Synchronisierung der Arbeit zwischen Warteschlangen zu ermöglichen, verwendet Direct3D 12 das Konzept der Fences, die in der API durch die [**ID3D12Fence-Schnittstelle**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence) dargestellt werden.

Ein Fence ist eine ganze Zahl, die die aktuelle Arbeitseinheit darstellt, die verarbeitet wird. Wenn die App den Umgrenzungsschritt durch Aufrufen von [**ID3D12CommandQueue::Signal**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal)fortsetzt, wird die ganze Zahl aktualisiert. Apps können den Wert eines Fences überprüfen und ermitteln, ob eine Arbeitseinheit abgeschlossen wurde, um zu entscheiden, ob ein nachfolgender Vorgang gestartet werden kann.

## <a name="synchronizing-resources-accessed-by-command-queues"></a>Synchronisieren von Ressourcen, auf die von Befehlswarteschlangen zugegriffen wird

In Direct3D 12 wird die Synchronisierung des Zustands einiger Ressourcen mit Ressourcenbarrieren implementiert. An jeder Ressourcenbarriere deklariert eine App den Vor- und Nachher-Status einer Ressource. Ein gängiges Beispiel ist der Übergang einer Ressource zwischen einer Shaderressourcenansicht und einer Renderzielansicht. Diese Ressourcenbarrieren werden größtenteils in Befehlslisten verwaltet. Wenn die Debugebenen aktiviert sind, erzwingt das System, dass der Vor- und Nachzustand aller Ressourcen übereinstimmt, wodurch sichergestellt wird, dass sich die Ressource bei einem Barriereübergang im richtigen Zustand für einen bestimmten Vorgang befindet.

Weitere Informationen zum Synchronisieren des Ressourcenzustands finden Sie unter [Verwenden von Ressourcenbarrieren zum Synchronisieren von Ressourcenzuständen.](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

## <a name="command-queue-support-for-tiled-resources"></a>Unterstützung der Befehlswarteschlange für gekachelte Ressourcen

Methoden zum Verwalten von gekachelten Ressourcen, die über die [**ID3D11DeviceContext2-Schnittstelle**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) in Direct3D 11 verfügbar gemacht wurden, werden von der [**ID3D12CommandQueue-Schnittstelle**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) in Direct3D 12 bereitgestellt. Diese Methoden umfassen:



| Methode                                                              | BESCHREIBUNG                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**CopyTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings)     | Kopiert Zuordnungen aus einer quellkachelten Ressource in eine zielkachelte Ressource.<br/>                 |
| [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) | Aktualisiert Zuordnungen von Kachelspeicherorten in gekachelten Ressourcen zu Speicherspeicherorten in einem Ressourcenheap.<br/> |



 

Weitere Informationen zur Verwendung von gekachelten Ressourcen in Direct3D 12-Apps finden Sie unter [Direct3D11 Tiled Resources](/windows/desktop/direct3d11/tiled-resources).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeitsübermittlung in Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

