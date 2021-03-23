---
title: Wichtige Änderungen von Direct3D 11 zu Direct3D 12
description: Direct3D 12 stellt eine bedeutende Abweichung vom Programmiermodell Direct3D 11 dar. Mit Direct3D 12 können apps näher an der Hardware heran liegen als je zuvor.
ms.assetid: CE5066C9-7EA6-437D-9EB0-AACFB6CFAD9E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be891d71d6c1f3a12d8d5aac3ec46785207ed31
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548650"
---
# <a name="important-changes-from-direct3d-11-to-direct3d-12"></a>Wichtige Änderungen von Direct3D 11 zu Direct3D 12

Direct3D 12 stellt eine bedeutende Abweichung vom Programmiermodell Direct3D 11 dar. Mit Direct3D 12 können apps näher an der Hardware heran liegen als je zuvor. Wenn Sie sich näher an der Hardware befinden, ist Direct3D 12 schneller und effizienter. Der Kompromiss der APP mit einer höheren Geschwindigkeit und Effizienz mit Direct3D 12 besteht jedoch darin, dass Sie für mehr Aufgaben verantwortlich sind als bei Direct3D 11.

-   [Explizite Synchronisierung](#explicit-synchronization)
-   [Verwaltung physischer Speicher Residenz](#physical-memory-residency-management)
-   [Pipeline Zustands Objekte](#pipeline-state-objects)
-   [Befehlslisten und Bündel](#command-lists-and-bundles)
-   [Deskriptorheaps und Tabellen](#descriptor-heaps-and-tables)
-   [Portieren von Direct3D 11](#porting-from-direct3d-11)
-   [Verwandte Themen](#related-topics)

Direct3D 12 ist eine Rückgabe auf Low-Level-Programmierung. Dadurch erhalten Sie mehr Kontrolle über die grafischen Elemente Ihrer Spiele und apps, indem Sie diese neuen Features einführen: Objekte zur Darstellung des Gesamtstatus der Pipeline, Befehlslisten und Bündel für die Arbeits Übermittlung sowie deskriptorheaps und Tabellen für den Ressourcen Zugriff.

Ihre APP ist mit Direct3D 12 schneller und effizienter geworden, aber Sie sind für mehr Aufgaben verantwortlich als bei Direct3D 11.

## <a name="explicit-synchronization"></a>Explizite Synchronisierung

-   In Direct3D 12 ist die CPU-GPU-Synchronisierung nun der expliziten Zuständigkeitsbereich der APP und wird nicht mehr implizit von der Laufzeit ausgeführt, wie es in Direct3D 11 der Fall ist. Dies bedeutet auch, dass Direct3D 12 keine automatische Prüfung auf Pipeline Risiken durchführt. Dies ist also die Verantwortung für die apps.
-   In Direct3D 12 sind Apps für das Pipelining von Datenaktualisierungen verantwortlich. Dies heißt, dass das Muster "Map/Lock-DISCARD" in Direct3D 11 in Direct3D 12 manuell ausgeführt werden muss. In Direct3D 11 gibt die Laufzeit einen Zeiger auf einen neuen Bereich des Arbeitsspeichers anstelle der alten Puffer Daten zurück, wenn die GPU den Puffer weiterhin verwendet, wenn Sie [**Verknüpfung id3d11devicecontext aus:: Map**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-map) mit [**D3D11 \_ map \_ Write \_ DISCARD**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_map)aufgerufen haben. Dadurch kann die GPU die alten Daten weiterhin verwenden, während die APP Daten in den neuen Puffer platziert. In der APP ist keine zusätzliche Speicherverwaltung erforderlich. der alte Puffer wird wieder verwendet oder automatisch zerstört, wenn die GPU damit fertig ist.
-   In Direct3D 12 werden alle dynamischen Updates (einschließlich konstanter Puffer, dynamischer Scheitelpunkt Puffer, dynamischer Texturen usw.) explizit von der APP gesteuert. Diese dynamischen Updates enthalten alle erforderlichen GPU-Zäune oder Pufferung. Die APP ist dafür verantwortlich, den Speicher verfügbar zu halten, bis Sie nicht mehr benötigt wird.
-   Direct3D 12 verwendet die Verweis Zählung im com-Stil nur für die Lebensdauer von Schnittstellen (mit dem schwachen Verweis Modell von Direct3D, das mit der Lebensdauer des Geräts verknüpft ist). Alle Arbeitsspeicher Lebensdauer für Ressourcen und Beschreibungen sind die einzige verantwortungsvolle Dauer der APP, die für die richtige Dauer gewährleistet ist, und keine Verweis Zählung. Direct3D 11 verwendet die Verweis Zählung, um auch die Lebensdauer von Schnittstellen Abhängigkeiten zu verwalten.

## <a name="physical-memory-residency-management"></a>Verwaltung physischer Speicher Residenz

Eine Direct3D 12-Anwendung muss Racebedingungen zwischen mehreren Warteschlangen, mehreren Adaptern und den CPU-Threads vermeiden. D3D12 synchronisiert die CPU und GPU nicht mehr und unterstützt keine praktischen Mechanismen für das Umbenennen von Ressourcen oder die mehrfach Pufferung. Die Zäune müssen verwendet werden, um zu verhindern, dass mehrere Verarbeitungseinheiten den Arbeitsspeicher überschreiben, bevor die Verarbeitung durch eine andere Verarbeitung abgeschlossen ist.

Die Anwendung Direct3D 12 muss sicherstellen, dass sich die Daten im Arbeitsspeicher befinden, während die GPU Sie liest. Der von den einzelnen Objekten verwendete Arbeitsspeicher wird während der Erstellung des Objekts als Residenter Speicher festgestellt. Anwendungen, die diese Methoden aufrufen, müssen mithilfe von Zäunen sicherstellen, dass die GPU nicht auf Objekte zugreift, die entfernt wurden.

Ressourcen Barrieren sind eine andere Art von Synchronisierung, die zum Synchronisieren von Ressourcen-und unter Quell Übergängen auf sehr granularer Ebene verwendet wird.

Weitere Informationen finden Sie unter [Speicherverwaltung in Direct3D 12](memory-management.md).

## <a name="pipeline-state-objects"></a>Pipeline Zustands Objekte

Direct3D 11 ermöglicht die Manipulation von Pipeline Zuständen durch einen großen Satz unabhängiger Objekte. So können z. b. der Status des eingabeassemblers, der Status eines Pixelshaders, der Status des Rasterizers und der Status der Ausgabe Zusammenführung unabhängig geändert Dieser Entwurf bietet eine bequeme und relativ allgemeine Darstellung der Grafik Pipeline, aber Sie nutzt nicht die Funktionen moderner Hardware, hauptsächlich, weil die verschiedenen Zustände häufig voneinander abhängig sind. Beispielsweise kombinieren viele GPUs den Pixelshader und den Ausgabe Zusammenführungs Zustand in eine einzelne Hardware Darstellung. Da diese Pipeline Stufen jedoch durch die API Direct3D 11 separat festgelegt werden können, kann der Anzeigetreiber keine Probleme des Pipeline Zustands auflösen, bis der Zustand abgeschlossen ist. Dies gilt nicht für die Draw-Zeit. Mit diesem Schema wird die Hardware Zustands Einrichtung verzögert. Dies bedeutet einen zusätzlichen Verwaltungsaufwand und weniger maximale zeichnen-Aufrufe pro Frame.

Direct3D 12 adressiert dieses Schema, indem ein Großteil des Pipeline Zustands in unveränderliche Pipeline Zustands Objekte (PSOs) vereinheitlicht wird, die bei der Erstellung endgültig erstellt werden. Hardware und Treiber können dann die PSO sofort in alle systemeigenen Hardware Anweisungen und Zustände konvertieren, die für die Ausführung von GPU-Arbeit erforderlich sind. Sie können weiterhin dynamisch ändern, welche PSO verwendet wird, aber zu diesem Zweck muss die Hardware nur die minimale Menge vorberechneter Zustände direkt in die Hardware Register kopieren, anstatt den Hardware Status im Handumdrehen zu berechnen. Durch die Verwendung von PSOs wird der Aufwand für zeichnen-Aufrufe erheblich reduziert, und es können viele weitere Draw-Aufrufe pro Frame erfolgen. Weitere Informationen zu PSOs finden Sie unter [Verwalten des Grafik Pipeline Zustands in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).

## <a name="command-lists-and-bundles"></a>Befehlslisten und Bündel

In Direct3D 11 erfolgt die gesamte Arbeits Übermittlung über den [unmittelbaren Kontext](/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-render), der einen einzelnen Stream von Befehlen darstellt, die an die GPU gesendet werden. Um die Multithread-Skalierung zu erreichen, haben Spiele auch [verzögerte Kontexte](/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-render) für Sie zur Verfügung. Verzögerte Kontexte in Direct3D 11 sind nicht perfekt auf Hardware Zuordnungen, sodass relativ wenig Arbeit durchgeführt werden kann.

Direct3D 12 führt ein neues Modell für die Arbeits Übermittlung auf der Grundlage von Befehlslisten ein, die alle Informationen enthalten, die zum Ausführen einer bestimmten Arbeitsauslastung auf der GPU benötigt werden. Jede neue Befehlsliste enthält Informationen wie die zu verwendende PSO, welche Textur-und Puffer Ressourcen benötigt werden, und die Argumente für alle Draw-Aufrufe. Da jede Befehlsliste eigenständig ist und keinen Zustand erbt, kann der Treiber alle notwendigen GPU-Befehle vorab und auf kostenlose Thread Weise vorab berechnen. Der einzige erforderliche serielle Prozess ist die abschließende Übermittlung von Befehlslisten an die GPU über die Befehls Warteschlange.

Zusätzlich zu den Befehlslisten führt Direct3D 12 auch eine zweite Arbeitsebene vor der Berechnung ein: *Bundles*. Im Gegensatz zu Befehlslisten, die vollständig eigenständig sind und in der Regel erstellt, einmal gesendet und verworfen werden, stellen Pakete eine Form der Zustands Vererbung dar, die die Wiederverwendung zulässt. Wenn ein Spiel z. b. zwei Zeichen Modelle mit unterschiedlichen Texturen zeichnen möchte, besteht ein Ansatz darin, eine Befehlsliste mit zwei Sätzen identischer zeichnen-Aufrufe aufzuzeichnen. Ein anderer Ansatz besteht jedoch darin, ein Bündel zu erfassen, das ein einzelnes Zeichen Modell zeichnet, und das Paket dann zweimal in der Befehlsliste mit unterschiedlichen Ressourcen wiederzugeben. Im letzteren Fall muss der Anzeigetreiber nur einmal die entsprechenden Anweisungen berechnen, und das Erstellen der Befehlsliste bedeutet im Wesentlichen zwei kostengünstige Funktionsaufrufe.

Weitere Informationen zu Befehlslisten und Paketen finden Sie unter [work Submission in Direct3D 12](command-queues-and-command-lists.md).

## <a name="descriptor-heaps-and-tables"></a>Deskriptorheaps und Tabellen

Die Ressourcen Bindung in Direct3D 11 ist hochgradig abstrahiert und komfortabel, lässt jedoch viele moderne Hardwarefunktionen unterausgelastet. In Direct3D 11 erstellen Spiele *Ansichts* Objekte von Ressourcen und binden diese Ansichten dann an mehrere *Slots* in verschiedenen Shader-Stufen in der Pipeline. Shader lesen wiederum Daten aus diesen expliziten Bindungs Slots, die zur zeichnungszeit korrigiert werden. Dieses Modell bedeutet, dass immer dann, wenn ein Spiel verschiedene Ressourcen verwendet, eine neue Ansicht an unterschiedliche Slots gebunden werden muss, und zeichnen erneut aufrufen. Dieser Fall steht auch für mehr Aufwand, der durch die vollständige Nutzung moderner Hardwarefunktionen vermieden werden kann.

Direct3D 12 ändert das Bindungs Modell, sodass es mit moderner Hardware identisch ist, und verbessert die Leistung erheblich. Anstatt eigenständige Ressourcen Sichten und explizite Zuordnung zu Slots zu benötigen, bietet Direct3D 12 einen deskriptorheap, in den Spiele ihre verschiedenen Ressourcen Ansichten erstellen. Dieses Schema bietet einen Mechanismus, mit dem die GPU die Hardware Native Ressourcen Beschreibung (Deskriptor) direkt in den Arbeitsspeicher schreiben muss. Um zu deklarieren, welche Ressourcen von der Pipeline für einen bestimmten zeichnen-Befehl verwendet werden sollen, geben Spiele eine oder mehrere deskriptortabellen an, die Unterbereiche des vollständigen deskriptorheaps darstellen. Da der deskriptorheap bereits mit den entsprechenden Hardware spezifischen deskriptordaten aufgefüllt wurde, ist das Ändern der deskriptortabellen ein extremkosten günstiger Vorgang.

Zusätzlich zu der verbesserten Leistung von deskriptorheaps und-Tabellen ermöglicht Direct3D 12 auch die dynamische Indizierung von Ressourcen in Shader, was eine nie dagewesene Flexibilität bietet und neue Renderingverfahren entsperrt. Beispielsweise codieren moderne verzögerte renderingmodule in der Regel einen Material-oder Objekt Bezeichner einer Art in den zwischen-g-Puffer. In Direct3D 11 müssen diese Module sorgfältig sein, um zu vermeiden, dass zu viele Materialien verwendet werden, da das Einschließen einer zu großen Anzahl in einem g-Puffer das abschließende renderdurchlauf erheblich verlangsamen kann. Mit dynamisch indizierbaren Ressourcen kann eine Szene mit tausend Materialien genau so schnell wie eine mit zehn Materialien fertiggestellt werden.

Weitere Informationen zu deskriptorheaps und Tabellen finden Sie unter [Ressourcen Bindung](resource-binding.md)und [Unterschiede im Bindungs Modell von Direct3D 11](binding-model.md).

## <a name="porting-from-direct3d-11"></a>Portieren von Direct3D 11

Das Portieren von Direct3D 11 ist ein beteiligter Prozess, der unter [Portieren von Direct3D 11 auf Direct3D 12](porting-from-direct3d-11-to-direct3d-12.md)beschrieben wird. Weitere Informationen finden Sie auch unter dem Bereich der Optionen bei der [Arbeit mit Direct3D 11, Direct3D 10 und Direct2D](direct3d-12-interop.md).

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Grundlegendes zu Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 