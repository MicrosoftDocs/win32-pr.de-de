---
title: Strategien für die Arbeitsspeicherverwaltung
description: Ein Speicher-Manager für Direct3D 12 kann sehr schnell mit allen verschiedenen Supportebenen, für UMA- oder diskrete Adapter (nicht UMA) und mit einem erheblichen Bereich von Architekturunterschieden zwischen GPU-Adaptern sehr kompliziert werden. Die empfohlene Strategie für die Direct3D 12-Speicherverwaltung, die in diesem Abschnitt beschrieben wird, ist \ 0034;Klassifizieren, Budget und Stream \ 0034;.
ms.assetid: BC9894F7-D496-46F2-A5C3-C7CA31FD4BA8
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7797b933a759afd0ccfb959672e5c595cefa21712f3488e61b4f99b8a57b0893
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123802"
---
# <a name="memory-management-strategies"></a>Strategien für die Arbeitsspeicherverwaltung

Ein Speicher-Manager für Direct3D 12 kann sehr schnell mit allen verschiedenen Supportebenen, für UMA- oder diskrete Adapter (nicht UMA) und mit einem erheblichen Bereich von Architekturunterschieden zwischen GPU-Adaptern sehr kompliziert werden.

Die empfohlene Strategie für die Direct3D 12-Speicherverwaltung, die in diesem Abschnitt beschrieben wird, ist "Klassifizieren, Budget und Streamen".

-   [Ressourcentypen](#resource-types)
-   [Arbeitsspeicherbudget](#memory-budget)
-   [Klassifizierungsstrategie](#classification-strategy)
-   [Zugehörige Themen](#related-topics)

## <a name="resource-types"></a>Ressourcentypen

Das grundlegende Konzept einer "ressource mit Commit" (Erstellen von virtuellen und physischen Adressräumen, die im verwalteten physischen Speicher initialisiert werden) gibt es seit Direct3D 9, obwohl die virtuelle Adressierung (VA) und die physische Adressierung in Direct3D 12 getrennt werden können, damit die App den physischen Speicher sorgfältig verwalten kann.

Zusätzlich zu ressourcen, für die ein Commit ausgeführt wurde, ermöglicht das Heapkonstrukt von Direct3D 12 zwei andere Ressourcentypen: "placed" und "reserved". In Direct3D 11 wurde eine "reservierte" Ressource als "kachelte Ressource" bezeichnet.

Reservierte Ressourcen unterscheiden sich von platzierten Ressourcen darin, dass reservierte Ressourcen über einen eigenen eindeutigen virtuellen GPU-Adressraum verfügen. Dies ermöglicht vorab eine große Zuordnung von VA-Speicherplatz und ermöglicht dann die spätere Zuordnung von VA-Seiten zu bestimmten Abschnitten des Heaps, und die Anwendung konfiguriert die Anordnung im laufenden Betrieb neu. Der Va-Bereich ist zusammenhängend und kann platzsparend zugeordnet werden.

Die reservierte Ressource kann mit API-Aufrufen wie [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) auf Regionen im Heap verwiesen werden, und sie können von der App als "resident" bezeichnet werden, indem Seitentabellen im laufenden Betrieb aktualisiert werden. Wenn ein VA-Bereich NULL oder einem nicht residenten Heap zugeordnet wird, wird dieser Teil der Ressource als nicht resident betrachtet. Wenn ein VA-Bereich einem residenten Heap zugeordnet wird, wird dieser Teil der Ressource als resident betrachtet. Heaps befinden sich bei der Erstellung.

Platzierte Ressourcen sind ein viel einfacheres Design, da sie einfach ein Zeiger auf einen bestimmten Bereich eines Heaps sind (z. B. ein 1-Mb-Bereich für eine Textur in einem 5-Mb-Heap). Aliasingbarrieren ermöglichen die Verwendung überlappender platzierter Ressourcen (siehe [**CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) und [**ResourceBarrier**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)).

Reservierte Ressourcen sind nicht auf der gesamten Direct3D 12-Hardware verfügbar, und platzierte Ressourcen sind ein sinnvoller Fallback, obwohl platzierte Ressourcen zusammenhängend sein müssen und nicht teilweise resident sein dürfen.

## <a name="memory-budget"></a>Arbeitsspeicherbudget

Wenn Sie in Direct3D 12 einen Heap zuordnen, erstellen Sie den physischen Speicheraspekt einer Ressource, für die ein Commit ausgeführt wurde. Eine explizitere Speichersegmentauswahl ist in Direct3D 12 (Auswahl zwischen Video- und Systemspeicher) verfügbar. UMA-Adapter verfügen nur über ein einzelnes Speichersegment, Systemspeicher.

GPUs unterstützen keine Seitenfehler, sodass Entwickler sich bewusst sein müssen, dass sie keinen Commit durchführen, insbesondere bei Systemen mit nur 1 GB Systemarbeitsspeicher. Wenn eine App über einen Commit verfügt, verwendet das Betriebssystem eine grobe Planung von Prozessen nach bedarf des physischen Arbeitsspeichers. Der Scheduler friert Vordergrundprozesse ein und stellt im Wesentlichen einen Teil davon aus, um einen Hintergrundprozess einzublättern, der ausgeführt werden soll. Der verfügbare physische Arbeitsspeicher kann je nach dem, was der Benutzer im Hintergrund ausführt (z. B. das Ausführen eines Browsers oder das Ansehen eines Videos), erheblich variieren.

Die API für das Arbeitsspeicherbudget ist [**QueryVideoMemoryInfo.**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo) Bei diskreten Adaptern ist "local" der Videospeicher, "nicht lokal" der Systemspeicher. Für UMA-Adapter ist nicht lokal immer 0 (null). Eine Entwurfsfrage ist, ob Ihre Engine sowohl Budgets als auch nur das lokale Budget verwaltet. Die Verwaltung nur des lokalen Budgets ist einfacher, weist jedoch einige Einschränkungen auf. Angenommen, es gibt ein maximales lokales Budget von 1 GB, dann stammen alle Heaps von diesen 1 GB in einem UMA-System, und es gibt keinen Überlauf zum Systemspeicher (eindeutig, da keine vorhanden sind).

Da verwalteter Direct3D11-Arbeitsspeicher für Anwendungen verwendet wird, werden ungenutzte Ressourcen im Wesentlichen ausgelagerungt.

Wählen Sie die am besten geeigneten Ressourcendimensionen aus. Überlegen Sie, ob die Größe einer Ressource für die Situation geeignet ist, in der die Anwendung tatsächlich ausgeführt wird. Einige Benutzer können die Anwendung in einem Fenster oder mit einer Bildschirmauflösung von 800 x 600 ausführen.

## <a name="classification-strategy"></a>Klassifizierungsstrategie

Um Ressourcen in speichergebundenen Szenarien effektiv zu verwalten, sollten Sie die Klassifizierung von Ressourcen in Folgendes in Betracht ziehen:



| Klassifizierung      | Beispiele                                                                                         | Objekte und API-Features                                                                                           | Verwaltungshinweise                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kritisch            | Game UI                                                                                          | Befehlszuweisung, Befehlswarteschlangen, Abfrageheaps, Ressourcen und Ressourcenheaps.                                      | Diese Elemente sollten in nicht auslagerungsfähigem/immer ausgeführtem Arbeitsspeicher gespeichert werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Skaliert/optional    | Ebenenspezifische Modelle und Texturen, Tauschketten, Skyboxen, Modelle für Spielerfiguren der ersten Person | Ressourcen und Heaps. Ressourcen, für die ein Commit ausgeführt wurde, aber auch platzierte und reservierte Ressourcen funktionieren möglicherweise genauso gut.          | Integrieren Sie die Speicherresidenzbudgetierung in die Renderingalgorithmen. Wählen Sie die entsprechende Ebene der verfügbaren Details aus, und werten Sie weniger als einmal pro Frame erneut aus. Zu den Techniken gehören die Verwendung von Ressourcen variabler Größe und die Skalierung der Swapkette.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| Wiederverwendete Ressourcen   | Schattenpuffer, Ressourcen für verzögertes Rendering, Ressourcen nach der Verarbeitung, Beleuchtungsdatencaches    | Ressourcen und Heaps. Überlappende platzierte Ressourcen auf Heaps und Aliasingbarrieren.                                  | Verwenden Sie große Ressourcen oder Heapbereiche innerhalb eines Frames wieder, um die Anforderungen für den gesamten Frame zu erfüllen. Verwenden Sie die Technik der frameinternen Speicherwiederverwendung. In Direct3D 11 konnten Anwendungen nur Ressourcen mit demselben Typ und potenziell ausreichend großen Dimensionen wiederverwenden. Direct3D 12-Heaps ermöglichen überlappende Ressourcen für eine viel einfachere und umfangreichere Wiederverwendung.<br/>                                                                                                                                                                                                                              |
| Streamingressourcen | Gelände, Offene-Welt-Texturen und Geometrie                                                        | Ressourcen und Heaps. Freethreaderstellung, CPU-Hintergrundthreads und Warteschlangen und Listen für Hintergrundkopierbefehle. | Teilresidenz, die häufig auf Sichtbarkeit basiert (mithilfe der view-frustum- oder distance-basierten Auswertung), und die neu auszuwertende Residency benötigt jeden Frame.<br/> Die Technik der Verwendung einer partiellen Residencyverwaltung pro Kachel und der Wiederverwendung zwischen Frames ist verfügbar, wenn der GPU-Adapter reservierte Ressourcen in Heaps unterstützt.<br/> Mithilfe der Technik der Wiederverwendung des Speichers zwischen Frames kann die Teilressourcenresidenz erreicht werden, ist aber weniger optimal. Platzierte Ressourcen mit Heaps sollten eine schnellere Wiederverwendung ermöglichen, aber ressourcen, für die ein Commit ausgeführt wurde, können als Fallback verwendet werden.<br/> |



 

Je mehr Anwendungen den Großteil der Arbeit auf Streamingressourcen anwenden, desto mehr nutzen sie platzierte und reservierte Ressourcen, wodurch die wiederverwendete Arbeitsspeichernutzung zwischen diesen vier Klassifizierungen maximiert wird. Je mehr Anwendungen streamen, desto mehr budgetieren und priorisieren sie die Bandbreite.

In der Regel müssen bei Direct3D 12-Grafik-Engines ein vielfältigeres und dynamischeres Budget berücksichtigt werden, und zwar strenger als in der Vergangenheit. Die besten Anwendungen finden alle vier Kategorien im Budget, das dem Prozess zugeordnet ist, und skalieren das Spiel von der mobilen Hintergrund-App auf diskrete Budgets im Vollbildmodus. Viele Anwendungen haben jedoch wahrscheinlich Schwierigkeiten, wenn sie mit zu vielen kritischen Ressourcentypen beginnen. Direct3D 11-fähige Ressourcen können anonym erstellt werden und einen kritischen Status einnehmen, ohne die Leistung zu beeinträchtigen. Für Direct3D 12 müssen Entwickler jedoch sorgfältig in ihrer Gesamten Engine und Middleware nach zufällig erstellten Ressourcen suchen und sie einer der anderen Kategorien neu zuweisen.

Weitere Problembereiche sind Middlewarekomponenten, Benutzersteuerelemente und frameinternes Streaming. Middlewarekomponenten sind möglicherweise nicht für ein Budget verfügbar und müssen auch nicht eng zusammenarbeiten. Middlewarekomponenten könnten wahrscheinlich Features als Renderingtechniken verfügbar machen. und die Anwendung könnte sich darauf verlassen, Middleware und Engine-Einstellungen verfügbar zu machen. Entwickler können sich auf Direct3D 11 verlassen, um das Paging zu erledigen und die richtige Bildfrequenz zu erzielen. In einigen Fällen haben Direct3D 11-Anwendungen Ressourceninhalte in jedem Frame aus- und auslagerungsgerufen. und dies führte zu akzeptablen Frameraten für den Benutzer. Die meisten Engines streamen Ressourcendaten nur als Hintergrundaktivität, bei der kein ordnungsgemäßer Fallback auf das Intraframestreaming mit hoher Priorität erfolgt. Indem Engines aufgefordert werden, dies zu implementieren, werden einige der CPU-Mehraufwandsgewinne, die sie suchen, durch den Wechsel zu Direct3D 12 unterlaufen. Entwickler von Engines könnten erwägen, ihre Frames in Phasen zu teesen, um mehr Möglichkeiten für wiederverwendbare Ressourcen zu bieten. und arbeiten wahrscheinlich mit Middlewareanbietern zusammen, um platzierte Ressourcen und Heaps für die Wiederverwendung des Speichers innerhalb des Frames zu unterstützen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)
</dt> <dt>

[**CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)
</dt> <dt>

[Direct3D 12-Programmieranleitung](directx-12-programming-guide.md)
</dt> <dt>

[Speicherverwaltung](memory-management.md)
</dt> <dt>

[Ressourcenbindung](resource-binding.md)
</dt> </dl>

 

