---
title: Wichtige Änderungen beim Wechsel von Direct3D 11 zu Direct3D 12
description: Direct3D 12 stellt eine erhebliche Abweichung vom Programmiermodell Direct3D 11 dar. Direct3D 12 ermöglicht Apps, sich der Hardware so nah wie nie zuvor zu machen.
ms.assetid: CE5066C9-7EA6-437D-9EB0-AACFB6CFAD9E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3afc5fe9a451addf1d1f7b9aeddf1f55ca40a22db99134ba71d8195c72ad2b13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123833"
---
# <a name="important-changes-from-direct3d-11-to-direct3d-12"></a>Wichtige Änderungen beim Wechsel von Direct3D 11 zu Direct3D 12

Direct3D 12 stellt eine erhebliche Abweichung vom Programmiermodell Direct3D 11 dar. Direct3D 12 ermöglicht Apps, sich der Hardware so nah wie nie zuvor zu machen. Da Direct3D 12 näher an der Hardware liegt, ist es schneller und effizienter. Der Trade-off Ihrer App mit höherer Geschwindigkeit und Effizienz bei Direct3D 12 besteht jedoch darin, dass Sie für mehr Aufgaben verantwortlich sind als bei Direct3D 11.

-   [Explizite Synchronisierung](#explicit-synchronization)
-   [Verwaltung der Physischen Speicherresidenz](#physical-memory-residency-management)
-   [Pipelinezustandsobjekte](#pipeline-state-objects)
-   [Befehlslisten und -bundles](#command-lists-and-bundles)
-   [Deskriptorheaps und Tabellen](#descriptor-heaps-and-tables)
-   [Portieren von Direct3D 11](#porting-from-direct3d-11)
-   [Zugehörige Themen](#related-topics)

Direct3D 12 ist eine Rückkehr zur Programmierung auf niedriger Ebene. Sie erhalten mehr Kontrolle über die grafischen Elemente Ihrer Spiele und Apps, indem Sie diese neuen Features einführen: Objekte zur Darstellung des Gesamtzustands der Pipeline, Befehlslisten und Bündel für die Übermittlung von Arbeit und Deskriptorheaps und Tabellen für den Ressourcenzugriff.

Ihre App hat die Geschwindigkeit und Effizienz mit Direct3D 12 erhöht, aber Sie sind für mehr Aufgaben verantwortlich als bei Direct3D 11.

## <a name="explicit-synchronization"></a>Explizite Synchronisierung

-   In Direct3D 12 liegt die CPU-GPU-Synchronisierung jetzt in der expliziten Verantwortung der App und wird nicht mehr implizit von der Laufzeit ausgeführt, wie in Direct3D 11. Dies bedeutet auch, dass direct3D 12 keine automatische Überprüfung auf Pipelinegefährdungen durchführt. Dies liegt also wieder in der Verantwortung der Apps.
-   In Direct3D 12 sind Apps für das Pipelining von Datenupdates verantwortlich. Das heißt, das Muster "Map/Lock-DISCARD" in Direct3D 11 muss manuell in Direct3D 12 ausgeführt werden. Wenn die GPU in Direct3D 11 weiterhin den Puffer verwendet, wenn Sie [**ID3D11DeviceContext::Map**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-map) mit [**D3D11 \_ MAP WRITE \_ \_ DISCARD**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_map)aufrufen, gibt die Runtime einen Zeiger auf einen neuen Speicherbereich anstelle der alten Pufferdaten zurück. Dadurch kann die GPU die alten Daten weiterhin verwenden, während die App Daten im neuen Puffer platziert. In der App ist keine zusätzliche Speicherverwaltung erforderlich. Der alte Puffer wird automatisch wiederverwendet oder zerstört, wenn die GPU damit fertig ist.
-   In Direct3D 12 werden alle dynamischen Updates (einschließlich konstanter Puffer, dynamischer Scheitelpunktpuffer, dynamischer Texturen usw.) explizit von der App gesteuert. Diese dynamischen Updates umfassen alle erforderlichen GPU-Umgrenzungen oder Pufferung. Die App ist dafür verantwortlich, den Arbeitsspeicher verfügbar zu halten, bis er nicht mehr benötigt wird.
-   Direct3D 12 verwendet die COM-Referenzzählung nur für die Lebensdauer von Schnittstellen (mithilfe des schwachen Referenzmodells von Direct3D, das an die Lebensdauer des Geräts gebunden ist). Alle Speicherlebensdauern für Ressourcen und Beschreibungen sind die einzige Verantwortung der App, die für die richtige Dauer beibehalten wird, und werden nicht als Verweis gezählt. Direct3D 11 verwendet die Verweiszählung, um auch die Lebensdauer von Schnittstellenabhängigkeiten zu verwalten.

## <a name="physical-memory-residency-management"></a>Verwaltung der Physischen Speicherresidenz

Eine Direct3D 12-Anwendung muss Racebedingungen zwischen mehreren Warteschlangen, mehreren Adaptern und den CPU-Threads verhindern. D3D12 synchronisiert cpu und GPU nicht mehr und unterstützt auch keine praktischen Mechanismen zum Umbenennen oder Mehrfachpuffern von Ressourcen. Um zu vermeiden, dass mehrere Verarbeitungseinheiten Arbeitsspeicher überschreiben, bevor eine andere Verarbeitungseinheit die Verwendung beendet, müssen Zäunen verwendet werden.

Die Direct3D 12-Anwendung muss sicherstellen, dass sich die Daten im Arbeitsspeicher befinden, während die GPU sie liest. Der von den einzelnen Objekten verwendete Arbeitsspeicher wird während der Erstellung des -Objekts als resident gemacht. Anwendungen, die diese Methoden aufrufen, müssen Zäunen verwenden, um sicherzustellen, dass die GPU nicht auf entfernte Objekte zugreift.

Ressourcenbarrieren sind ein weiterer erforderlicher Synchronisierungstyp, der zum Synchronisieren von Ressourcen- und Unterressourcenübergängen auf einer sehr präzisen Ebene verwendet wird.

Weitere Informationen finden Sie [unter Speicherverwaltung in Direct3D 12.](memory-management.md)

## <a name="pipeline-state-objects"></a>Pipelinezustandsobjekte

Direct3D 11 ermöglicht die Bearbeitung des Pipelinezustands durch einen großen Satz unabhängiger Objekte. Beispielsweise können der Status des Eingabeassemblers, der Pixelshaderzustand, der Rasterizerzustand und der Ausgabezusammenführungszustand unabhängig voneinander geändert werden. Dieser Entwurf bietet eine praktische und relativ hohe Darstellung der Grafikpipeline, nutzt jedoch nicht die Funktionen moderner Hardware, da die verschiedenen Zustände häufig voneinander abhängig sind. Viele GPUs kombinieren beispielsweise den Pixelshader und den Ausgabezusammenführungszustand in einer einzelnen Hardwaredarstellung. Da die Direct3D 11-API es jedoch ermöglicht, diese Pipelinestufen separat festzulegen, kann der Anzeigetreiber Probleme mit dem Pipelinezustand erst beheben, wenn der Zustand abgeschlossen ist, d. h. erst nach dem Zeichnen. Dieses Schema verzögert die Einrichtung des Hardwarezustands. Dies bedeutet zusätzlichen Mehraufwand und weniger maximale Draw-Aufrufe pro Frame.

Direct3D 12 löst dieses Schema, indem ein Großteil des Pipelinezustands in unveränderliche Pipelinezustandsobjekte (PSOs) vereinheitlicht wird, die bei der Erstellung abgeschlossen werden. Hardware und Treiber können die PSO dann sofort in die hardwarenativen Anweisungen und den Zustand konvertieren, die zum Ausführen von GPU-Aufgaben erforderlich sind. Sie können weiterhin dynamisch ändern, welcher PSO verwendet wird. Zu diesem Zweck muss die Hardware jedoch nur die minimale Menge an vorab berechneten Zuständen direkt in die Hardwareregister kopieren, anstatt den Hardwarezustand dynamisch zu berechnen. Durch die Verwendung von PSOs wird der Mehraufwand für Zeichnen-Aufrufe erheblich reduziert, und es können viele weitere Draw-Aufrufe pro Frame auftreten. Weitere Informationen zu PSOs finden Sie unter [Verwalten des Grafikpipelinezustands in Direct3D 12.](managing-graphics-pipeline-state-in-direct3d-12.md)

## <a name="command-lists-and-bundles"></a>Befehlslisten und -bundles

In Direct3D 11 erfolgt die gesamte Arbeitsübermittlung über den [unmittelbaren Kontext](/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-render), der einen einzelnen Stream von Befehlen darstellt, die an die GPU geleitet werden. Um eine Multithreadskalierung zu erreichen, stehen den Spielen auch [verzögerte Kontexte](/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-render) zur Verfügung. Verzögerte Kontexte in Direct3D 11 werden der Hardware nicht perfekt zugeordnet, sodass relativ wenig Arbeit in ihnen ausgeführt werden kann.

Direct3D 12 führt ein neues Modell für die Übermittlung von Arbeit basierend auf Befehlslisten ein, die die gesamten Informationen enthalten, die zum Ausführen einer bestimmten Workload auf der GPU erforderlich sind. Jede neue Befehlsliste enthält Informationen wie die zu verwendende PSO, die benötigten Textur- und Pufferressourcen und die Argumente für alle Draw-Aufrufe. Da jede Befehlsliste eigenständig ist und keinen Zustand erbt, kann der Treiber alle erforderlichen GPU-Befehle vorab und auf Freethreading-Weise berechnen. Der einzige erforderliche serielle Prozess ist die endgültige Übermittlung von Befehlslisten an die GPU über die Befehlswarteschlange.

Zusätzlich zu Befehlslisten führt Direct3D 12 auch eine zweite Ebene der Vorberechnung ein: *Bündel*. Im Gegensatz zu Befehlslisten, die vollständig eigenständig sind und in der Regel erstellt, einmal übermittelt und verworfen werden, bieten Bündel eine Form der Zustandsvererbung, die die Wiederverwendung ermöglicht. Wenn ein Spiel beispielsweise zwei Zeichenmodelle mit unterschiedlichen Texturen zeichnen möchte, besteht ein Ansatz darin, eine Befehlsliste mit zwei Sätzen identischer Draw-Aufrufe aufzuzeichnen. Ein anderer Ansatz besteht jedoch darin, ein Bündel zu "aufzeichnen", das ein einzelnes Zeichenmodell zeichnet, und dann das Bündel zweimal in der Befehlsliste mit unterschiedlichen Ressourcen wiederzuspielen. Im letzteren Fall muss der Anzeigetreiber nur einmal die entsprechenden Anweisungen berechnen, und das Erstellen der Befehlsliste ergibt im Wesentlichen zwei kostengünstige Funktionsaufrufe.

Weitere Informationen zu Befehlslisten und Paketen finden Sie unter [Work Submission in Direct3D 12](command-queues-and-command-lists.md).

## <a name="descriptor-heaps-and-tables"></a>Deskriptorheaps und Tabellen

Die Ressourcenbindung in Direct3D 11 ist stark abstrahiert und praktisch, aber viele moderne Hardwarefunktionen sind nicht ausgelastet. In Direct3D 11 erstellen Spiele *Ansichtsobjekte* von Ressourcen und binden diese Ansichten dann an mehrere *Slots* in verschiedenen Shaderstufen in der Pipeline. Shader lesen wiederum Daten aus diesen expliziten Bindungsslots, die zum Zeitpunkt des Zeichnens fixiert sind. Dieses Modell bedeutet, dass jedes Mal, wenn ein Spiel mit unterschiedlichen Ressourcen gezeichnet wird, verschiedene Ansichten erneut an verschiedene Slots gebunden und draw erneut aufgerufen werden muss. Dieser Fall stellt auch einen Mehraufwand dar, der durch die vollständige Nutzung moderner Hardwarefunktionen beseitigt werden kann.

Direct3D 12 ändert das Bindungsmodell entsprechend moderner Hardware und verbessert die Leistung erheblich. Anstatt eigenständige Ressourcenansichten und eine explizite Zuordnung zu Slots zu erfordern, bietet Direct3D 12 einen Deskriptorheap, in dem Spiele ihre verschiedenen Ressourcenansichten erstellen. Dieses Schema stellt einen Mechanismus bereit, mit dem die GPU die hardwarenative Ressourcenbeschreibung (Deskriptor) direkt im Voraus in den Arbeitsspeicher schreiben kann. Um zu deklarieren, welche Ressourcen von der Pipeline für einen bestimmten Draw-Aufruf verwendet werden sollen, geben Spiele eine oder mehrere Deskriptortabellen an, die Unterbereiche des vollständigen Deskriptorheaps darstellen. Da der Deskriptorheap bereits mit den entsprechenden hardwarespezifischen Deskriptordaten aufgefüllt wurde, ist das Ändern von Deskriptortabellen ein äußerst kostengünstiger Vorgang.

Zusätzlich zur verbesserten Leistung von Deskriptorheaps und -tabellen ermöglicht Direct3D 12 auch die dynamische Indizierung von Ressourcen in Shadern, was eine einzigartige Flexibilität bietet und neue Renderingtechniken ermöglicht. Moderne verzögerte Rendering-Engines codieren beispielsweise in der Regel einen Material- oder Objektbezeichner einer Art in den g-Zwischenpuffer. In Direct3D 11 müssen diese Engines darauf achten, dass sie nicht zu viele Materialien verwenden, da das Einschließen von zu vielen in einem G-Puffer den endgültigen Renderdurchlauf erheblich verlangsamen kann. Mit dynamisch indizierbaren Ressourcen kann eine Szene mit tausend Materialien genauso schnell abgeschlossen werden wie eine mit nur zehn.

Weitere Informationen zu Deskriptorheaps und -tabellen finden Sie unter [Ressourcenbindung](resource-binding.md)und [Unterschiede im Bindungsmodell von Direct3D 11.](binding-model.md)

## <a name="porting-from-direct3d-11"></a>Portieren von Direct3D 11

Das Portieren von Direct3D 11 ist ein beteiligter Prozess, der unter [Portieren von Direct3D 11 zu Direct3D 12](porting-from-direct3d-11-to-direct3d-12.md)beschrieben wird. Weitere Informationen finden Sie unter [Arbeiten mit Direct3D 11, Direct3D 10 und Direct2D.](direct3d-12-interop.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegendes zu Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 