---
title: Strategien für die Speicherverwaltung
description: Ein Speichermanager für Direct3D 12 kann mit allen unterstützten Unterstützungs Ebenen, für UMA-oder diskrete (nicht-UMA-) Adapter und mit einer beträchtlichen Bandbreite an Architektur Unterschiede zwischen GPU-Adaptern sehr schnell sehr kompliziert werden. Die empfohlene Strategie für die Direct3D 12-Speicherverwaltung, die in diesem Abschnitt beschrieben wird, ist "\ 0034; klassifizieren, Budget und Stream \ 0034;".
ms.assetid: BC9894F7-D496-46F2-A5C3-C7CA31FD4BA8
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dad04055a5acdeeeaead3a56f0bd04e64aa90fe0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548693"
---
# <a name="memory-management-strategies"></a>Strategien für die Speicherverwaltung

Ein Speichermanager für Direct3D 12 kann mit allen unterstützten Unterstützungs Ebenen, für UMA-oder diskrete (nicht-UMA-) Adapter und mit einer beträchtlichen Bandbreite an Architektur Unterschiede zwischen GPU-Adaptern sehr schnell sehr kompliziert werden.

Die empfohlene Strategie für die Direct3D 12-Speicherverwaltung, die in diesem Abschnitt beschrieben wird, ist "klassifizieren, Budget und Stream".

-   [Ressourcentypen](#resource-types)
-   [Arbeitsspeicher Budget](#memory-budget)
-   [Klassifizierungs Strategie](#classification-strategy)
-   [Verwandte Themen](#related-topics)

## <a name="resource-types"></a>Ressourcentypen

Das grundlegende Konzept einer "zugesicherten Ressource" (Erstellen virtueller und physischer Adressräume, die in verwaltetem physischem Arbeitsspeicher initialisiert wurden) liegt seit Direct3D 9, obwohl die virtuelle Adressierung (VA) und die physische Adressierung in Direct3D 12 auseinander geführt werden können, um der APP die sorgfältige Verwaltung von physischem Speicher zu ermöglichen.

Zusätzlich zu den Ressourcen, für die ein Commit ausgeführt wurde, aktiviert das Heap Konstrukt von Direct3D 12 zwei weitere Arten von Ressourcen: "platziert" und "reserviert". In Direct3D 11 wurde eine "reservierte" Ressource als "gekachelte Ressource" bezeichnet.

Reservierte Ressourcen unterscheiden sich von den platzierten Ressourcen darin, dass reservierte Ressourcen über einen eigenen eindeutigen virtuellen GPU-Adressraum verfügen. Dies ermöglicht eine große Zuweisung des VA-Raums im Vordergrund und ermöglicht dann die Zuordnung von VA-Seiten zu bestimmten Abschnitten des Heaps später, und die Anwendung konfiguriert die Anordnung im Handumdrehen neu. Der VA-Raum ist zusammenhängend und kann nur spärlich zugeordnet werden.

Die reservierte Ressource kann so erstellt werden, dass Sie mit API-aufrufen (z. b. [**updatetilemappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) ) auf Regionen im Heap verweist, und Sie können durch die app in den Betrieb gebracht werden, indem Sie Seitentabellen dynamisch aktualisieren. Wenn ein VA-Bereich NULL oder einem nicht Residenten Heap zugeordnet ist, wird dieser Teil der Ressource als nicht Residenter Heap betrachtet. Wenn ein VA-Bereich einem Residenten Heap zugeordnet ist, wird dieser Teil der Ressource als ansässig betrachtet. Heaps sind bei der Erstellung ansässig.

Platzierte Ressourcen sind ein viel einfacheres Design, das einfach ein Zeiger auf einen bestimmten Bereich eines Heaps ist (z. b. ein 1-MB-Bereich für eine Textur in einem 5-MB-Heap). Aliasing-Barrieren ermöglichen die Verwendung von überlappenden Ressourcen (siehe [**createplacedresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) und [**resourcebarrier**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)).

Reservierte Ressourcen sind nicht auf allen Direct3D 12-Hardware verfügbar, und platzierte Ressourcen sind ein angemessener Fallback, obwohl die platzierten Ressourcen zusammenhängend sein müssen und nicht teilweise Residenten sind.

## <a name="memory-budget"></a>Arbeitsspeicher Budget

In Direct3D 12 Wenn Sie einen Heap zuordnen, erstellen Sie den physischen Speicher Aspekt einer zugegebenen Ressource. Eine explizite Speichersegment Auswahl ist in Direct3D 12 verfügbar (zwischen Video-und System Arbeitsspeicher auswählen). Die UMA-Adapter verfügen nur über ein einzelnes Speichersegment, System Arbeitsspeicher.

GPUs unterstützen keine Seiten Fehler, daher müssen Entwickler darauf achten, dass Sie nicht über einen Commit verfügen, insbesondere für Systeme mit nur 1 GB System Arbeitsspeicher. Wenn eine APP über einen Commit ausgeführt wird, verwendet das Betriebssystem eine zusammen gestufte Zeitplanung der Prozesse nach Bedarf an physischem Arbeitsspeicher. Der Planer fixiert Vordergrund Prozesse und führt im Wesentlichen eine Seite aus, um einen Hintergrundprozess auszuführen, der ausgeführt werden soll. Der verfügbare physische Speicher kann stark variieren, je nachdem, was der Benutzer im Hintergrund durchführt (z. b. das Ausführen eines Browsers oder das Ansehen eines Videos).

Das Budget für die API für den Arbeitsspeicher ist [**queryvideomemoryinfo**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo). Bei diskreten Adaptern "local" ist der Videospeicher "Non-local" der System Arbeitsspeicher. Bei Uma-Adaptern ist Non-local immer 0 (null). Eine Entwurfs Frage ist, ob Ihre Engine sowohl das Budget als auch das lokale Budget verwalten wird. Nur das lokale Budget zu verwalten, ist einfacher, aber es sind einige Einschränkungen zu beachten. angenommen, es gibt ein maximales lokales Budget von 1 GB. dann stammen alle Heaps aus den 1 GB in einem UMA-System, und es gibt keinen Überlauf in den Systemspeicher (weil keine vorhanden sind).

Da Direct3D11 verwalteter Arbeitsspeicher für Anwendungen verwendet wird, werden im Grunde nicht verwendete Ressourcen ausgelagert.

Wählen Sie die am besten geeigneten Ressourcen Dimensionen aus. Überprüfen Sie, ob die Größe einer Ressource für die Situation geeignet ist, in der die Anwendung tatsächlich ausgeführt wird. Einige Benutzer können die Anwendung in einem Fenster oder mit einer Bildschirmauflösung von 800X600 ausführen.

## <a name="classification-strategy"></a>Klassifizierungs Strategie

Um Ressourcen in Speicher gebundenen Szenarien effektiv zu verwalten, sollten Sie die Ressourcen in folgende Kategorien klassifiziert werden:



| Klassifizierung      | Beispiele                                                                                         | Objekte und API-Features                                                                                           | Hinweise zur Verwaltung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kritisch            | Spiel Benutzeroberfläche                                                                                          | Befehls Zuweisung, Befehls Warteschlangen, Abfrage Heaps, Ressourcen und Ressourcen Heaps.                                      | Diese Elemente sollten in einem nicht von einem Speicher abrechenbaren/immer zugebelegten Speicher vorhanden sein.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Skaliert/optional    | Ebenenspezifische Modelle und Texturen, Austausch Ketten, Himmels Felder, Player Zeichen Modelle für die erste Person | Ressourcen und Heaps. Zugesicherte Ressourcen, aber auch platzierte und reservierte Ressourcen können ebenfalls funktionieren.          | Integrieren Sie die Budget für die Speicher Residenz in die Rendering-Algorithmen. Wählen Sie die geeignete Ebene des verfügbaren Details aus, und evaluieren Sie weniger als einmal pro Frame. Zu den Techniken gehören die Verwendung von Ressourcen variabler Größen und die Skalierung der Austausch Kette.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| Wiederverwendete Ressourcen   | Schatten Puffer, verzögerte Renderingressourcen, nachträglich verarbeitete Ressourcen, Beleuchtung von Daten Caches    | Ressourcen und Heaps. Überlappende Ressourcen auf Heaps und Aliasing-Barrieren.                                  | Verwenden Sie große Ressourcen oder Heap Bereiche innerhalb eines Frames, um die Anforderungen für den gesamten Frame zu verringern. Verwenden Sie die Technik der Wiederverwendung im Rahmen des Frame Speichers. In Direct3D 11 konnten Anwendungen nur Ressourcen mit demselben Typ und potenziell ausreichend großen Dimensionen wieder verwenden. Direct3D 12 Heaps ermöglichen überlappende Ressourcen für eine wesentlich einfachere und bessere Wiederverwendung.<br/>                                                                                                                                                                                                                              |
| Streaming-Ressourcen | Gelände, Open-World-Texturen und Geometrie                                                        | Ressourcen und Heaps. Freithreaderstellung, CPU-Hintergrundthreads und Befehls Warteschlangen und-Listen für den Hintergrund Kopiervorgang. | Teilweiser Wohnsitz, der in der Regel auf Sichtbarkeit basiert (mit der "View-Frustum" oder der Entfernungs basierten Auswertung), und die Neuauswertung der Residenz erfordert jeden Frame.<br/> Die Vorgehensweise bei der Verwendung einer pro-Kachel-partiellen Residenz Verwaltung und der Wiederverwendung zwischen Frame ist verfügbar, wenn der GPU-Adapter reservierte Ressourcen innerhalb von Heaps unterstützt.<br/> Mithilfe des Verfahrens zur erneuten Verwendung des Frame übergreifenden Speichers kann eine Teil Quell Residenz unterstützt werden, ist jedoch weniger optimal. Bei der Platzierung von Ressourcen mit Heaps sollten Sie eine schnellere Wiederverwendung ermöglichen, aber zugesicherte Ressourcen können als Fallback verwendet werden.<br/> |



 

Die mehr Anwendungen werden für die meisten Aufgaben auf Streamingressourcen ausgerichtet, umso mehr werden Sie in die Lage versetzt, die bereitgestellt und reservierte Ressourcen zu nutzen, um die Wiederverwendung von Arbeitsspeicher zwischen diesen vier Klassifizierungen zu maximieren. Der Stream "Weitere Anwendungen", umso mehr werden Sie als Budget und Priorisieren der Bandbreite.

In der Regel müssen Grafik-Engines mit Direct3D 12 ein vielfältigeres und dynamisches Budget berücksichtigen, und es ist strenger als in der Vergangenheit. Die besten Anwendungen suchen alle vier Kategorien in dem Budget, das für den Prozess gilt, und skaliert die Spiel Wiedergabe von der Hintergrund Mobile App auf das diskrete voll Bild Budget. Viele Anwendungen treten jedoch wahrscheinlich in Schwierigkeiten, indem Sie mit zu vielen kritischen Kategorietypen von Ressourcen beginnen. Direct3D 11 aktivierte Ressourcen werden anonym erstellt und belegen den Status "kritisch", ohne dass die Leistung beeinträchtigt wird. Für Direct3D 12 müssen Entwickler jedoch sorgfältig nach zufällig erstellten Ressourcen in der gesamten Engine und Middleware suchen und Sie dann erneut einer der anderen Kategorien zuweisen.

Andere Problembereiche sind middlewarekomponenten, Benutzer Steuerelemente und Inner Frame Streaming. Middlewarekomponenten werden möglicherweise nicht einem Budget ausgesetzt und müssen nicht eng zusammenarbeiten. Middlewarekomponenten könnten Features als Renderingverfahren verfügbar machen. und die Anwendung könnte sich darauf verlassen, dass Middleware und Engine-Einstellungen verfügbar gemacht werden. Entwickler können sich auf Direct3D 11 verlassen, um das Paging durchzuführen und die richtige Framerate zu erzielen. In einigen Fällen haben Direct3D 11-Anwendungen möglicherweise Ressourcen Inhalte in und aus jedem Frame ausgelagert. Dies führte zu akzeptablen Frameraten für den Benutzer. Die meisten Engines streamen Ressourcen Daten nur als Hintergrund Aktivität, bei der es keinen ordnungsgemäßen Fall Back zu einem Frame Streaming mit hoher Priorität gibt. Die Implementierung von Modulen zur Implementierung von führt zu einem gewissen CPU-Overhead, den Sie durch den Umstieg auf Direct3D 12 erreichen. Engine-Entwickler können Ihre Frames in Phasen durcharbeiten, um mehr Möglichkeiten für wiederverwendbare Ressourcen bereitzustellen. und unterstützen wahrscheinlich auch Middleware-Anbieter, um die Platzierung von Ressourcen und Heaps für die Wiederverwendung von Interframe-Arbeitsspeicher zu unterstützen.

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[**"Kreatecommittedresource"**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)
</dt> <dt>

[**"Kreatereservedresource"**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)
</dt> <dt>

[Direct3D 12-Programmier Handbuch](directx-12-programming-guide.md)
</dt> <dt>

[Speicherverwaltung](memory-management.md)
</dt> <dt>

[Ressourcen Bindung](resource-binding.md)
</dt> </dl>

 

