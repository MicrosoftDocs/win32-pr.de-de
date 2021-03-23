---
title: Aufenthaltes
description: Ein Objekt gilt als residente, wenn es von der GPU zugänglich ist.
ms.assetid: 956F80D7-EEC8-4D88-B251-EE325614F31E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b842ce5b3e89c3877f50036e747a90f14104bce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548714"
---
# <a name="residency"></a>Aufenthaltes

Ein Objekt gilt als *residente* , wenn es von der GPU zugänglich ist.

-   [Residenz Budget](#residency-budget)
-   [Heap Ressourcen](#heap-resources)
-   [Wohnsitz Prioritäten](#residency-priorities)
    -   [Standardmäßiger Prioritäts Algorithmus](#default-priority-algorithm)
-   [Programmieren der Residenz Verwaltung](#programming-residency-management)
-   [Verwandte Themen](#related-topics)

## <a name="residency-budget"></a>Residenz Budget

GPUs unterstützen noch keine Seiten Fehler, sodass Anwendungen einen Commit für Daten in den physischen Speicher ausführen müssen, während die GPU darauf zugreifen kann. Dieser Prozess wird als "nehmen Sie einen Residenten" bezeichnet und muss sowohl für den physischen System Arbeitsspeicher als auch für den physischen diskreten Videospeicher ausgeführt werden. In D3D12 Kapseln die meisten API-Objekte eine gewisse Menge an GPU-zugreif baren Arbeitsspeicher. Der Speicher, auf den GPU zugegriffen werden kann, wird während der Erstellung des API-Objekts in den Speicher gebracht und bei der Zerstörung von API-Objekten entfernt.

Die Menge an physischem Arbeitsspeicher, der für den Prozess verfügbar ist, wird als Videospeicher Budget bezeichnet. Das Budget kann merklich schwanken, wenn sich Hintergrundprozesse reaktivieren und im Standbymodus befinden. und schwanken erheblich, wenn der Benutzer zu einer anderen Anwendung wechselt. Die Anwendung kann benachrichtigt werden, wenn sich das Budget ändert, und sowohl das aktuelle Budget als auch den aktuell verbrauchten Arbeitsspeicher abrufen. Wenn eine Anwendung nicht innerhalb Ihres Budgets bleibt, wird der Prozess zeitweise eingefroren, damit andere Anwendungen ausgeführt werden können und/oder die Erstellungs-APIs einen Fehler zurückgeben. Die [**IDXGIAdapter3**](/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) -Schnittstelle stellt die Methoden bereit, die diese Funktionalität betreffen, insbesondere [**queryvideomemoryinfo**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo) und [**registervideomemorybudgetchangenotificationevent**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent).

Anwendungen wird empfohlen, eine Reservierung zu verwenden, um die Menge an Arbeitsspeicher zu kennzeichnen, ohne dass Sie Sie nicht verwenden können. Im Idealfall ist die vom Benutzer angegebene "niedrige" Grafik Einstellung oder etwas noch niedrigerer Wert der richtige Wert für eine solche Reservierung. Wenn eine Reservierung festgelegt wird, erhält die Anwendung nie ein höheres Budget als in der Regel. Stattdessen helfen die Reservierungs Informationen dem Betriebssystem-Kernel, die Auswirkungen von großen Arbeitsspeicher Auslastungs Situationen schnell zu minimieren. Selbst die Reservierung ist nicht garantiert für die Anwendung verfügbar, wenn die Anwendung nicht die Vordergrund Anwendung ist.

## <a name="heap-resources"></a>Heap Ressourcen

Obwohl viele API-Objekte einen Arbeitsspeicher mit GPU-Zugriff Kapseln, werden Heaps & Ressourcen voraussichtlich die signifikanteste Art und Weise, wie der physische Speicher von Anwendungen genutzt und verwaltet wird. Bei einem Heap handelt es sich um die niedrigste einheitseinheit zum Verwalten des physischen Speichers. es ist also gut, sich mit den Wohnsitz Eigenschaften vertraut zu machen.

-   Heaps können nicht teilweise ansässig gemacht werden, aber es gibt Problem Umgehungen mit reservierten Ressourcen.
-   Heaps sollten als Teil eines bestimmten Pools eingeplant werden. Die UMA-Adapter verfügen über einen Pool, während diskrete Adapter über zwei Pools verfügen. Es ist zwar true, dass der Kernel einige Heaps auf diskreten Adaptern aus dem Videospeicher in den Systemspeicher verschieben kann, dies erfolgt jedoch nur als extrem letztes Mittel. Anwendungen sollten sich nicht auf das über-Budget-Verhalten des Kernels verlassen und sollten sich stattdessen auf eine gute Budgetverwaltung konzentrieren.
-   Heaps können aus der Residenz entfernt werden, sodass Ihre Inhalte an den Datenträger ausgelagert werden können. Die Zerstörung von Heaps ist jedoch eine zuverlässigere Methode, um die Residenz über alle Adapter Architekturen hinweg freizugeben. Bei Adaptern [**, bei**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-evict) denen das Feld " *maxgpuvirtualaddressbitsperprocess* " der [**Unterstützung für die \_ Unterstützung von D3D12 Feature \_ Data \_ GPU \_ Virtual \_ Address \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support) sich in der Nähe der budgetgröße befindet, wird die Residenz von
-   Heap Erstellung kann langsam sein. Es ist jedoch für die Verarbeitung im Hintergrund Thread optimiert. Es wird empfohlen, Heaps für Hintergrundthreads zu erstellen, um zu vermeiden, dass der Renderthread abgleitet. In D3D12 können mehrere Threads die Erstellung von Routinen gleichzeitig sicher aufrufen.

D3D12 bietet mehr Flexibilität und Orthogonalität im Ressourcenmodell, um mehr Optionen für Anwendungen zu ermöglichen. Es gibt drei allgemeine Arten von Ressourcen in D3D12: "Commit", "platziert" und "reserviert".

-   Mit zugesicherte Ressourcen werden gleichzeitig sowohl eine Ressource als auch ein Heap erstellt. Der Heap ist implizit, und es kann nicht direkt auf ihn zugegriffen werden. Der Heap wird entsprechend angepasst, um die gesamte Ressource im Heap zu suchen.
-   Platzierte Ressourcen ermöglichen die Platzierung einer Ressource bei einem Offset ungleich 0 (null) innerhalb eines Heaps. Offsets müssen in der Regel auf 64 KB ausgerichtet werden. in beiden Richtungen gibt es jedoch einige Ausnahmen. MSAA-Ressourcen erfordern eine Anpassung von 4 MB Offset und eine Offset Ausrichtung von 4 KB für kleine Texturen. Platzierte Ressourcen können nicht direkt verschoben oder einem anderen Heap neu zugeordnet werden. Sie ermöglichen jedoch eine einfache Verlagerung der Ressourcen Daten zwischen Heaps. Nachdem Sie eine neu platzierte Ressource in einem anderen Heap erstellt und die Ressourcen Daten kopiert haben, müssen neue Ressourcen Deskriptoren für den neuen Speicherort der Ressourcen Daten verwendet werden.
-   Reservierte Ressourcen sind nur verfügbar, wenn der Adapter die Kachel Ressourcenebene 1 oder höher unterstützt. Wenn Sie verfügbar sind, bieten Sie die gängigsten verfügbaren Methoden für die Aufenthalts Verwaltung an. aber nicht alle Adapter unterstützen Sie zurzeit. Sie ermöglichen die Neuzuordnung einer Ressource, ohne dass eine erneute Generierung von Ressourcen Deskriptoren, partielle Unterstützung der MIP-Ebene und Szenarios mit geringer Dichte erforderlich ist. Nicht alle Ressourcentypen werden auch dann unterstützt, wenn reservierte Ressourcen verfügbar sind. Daher ist ein vollständig allgemeiner Seiten basierter Residenz-Manager noch nicht möglich.

## <a name="residency-priorities"></a>Wohnsitz Prioritäten

Das Windows 10 Creators Update ermöglicht Entwicklern, zu beeinflussen, welche Heaps und Ressourcen bevorzugt bleiben, wenn die Arbeitsspeicher Auslastung erfordert, dass einige der Ressourcen herabgestuft werden. Dadurch können Entwickler bessere Anwendungen erstellen, indem Sie wissen nutzen, dass die Runtime nicht von der API-Verwendung ableiten kann. Es wird erwartet, dass Entwickler mit der Verwendung von Ressourcen in Bezug auf die Verwendung von Ressourcen in Bezug auf reservierte und gekachelte Ressourcen besser werden und die Prioritäten festlegen können.

Die Anwendung dieser Prioritäten muss einfacher sein als das durchführen zweier dynamischer Arbeitsspeicher Budgets, das manuelle herabstufen und herauf Stufen von Ressourcen für Sie, da Anwendungen dies bereits tun können. Daher ist der Entwurf der Residenz Prioritäts-API mit angemessenen Standard Prioritäten, die jedem Heap oder jeder Ressource als erstellt zugewiesen wurden, mit angemessenen Standard Prioritäten konsistent. Weitere Informationen finden Sie unter [**ID3D12Device1::**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority) -Enumeration und-Enumeration [**. \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_residency_priority)

Mit Prioritäten werden für Entwickler Folgendes erwartet:

-   Erhöhen Sie die Priorität einiger außergewöhnlicher Heaps, um die Auswirkungen auf die Leistung dieser Heaps besser zu verringern, die früher oder häufiger herabgestuft werden, als ihre natürlichen Zugriffsmuster erfordern würden. Diese Vorgehensweise wird von Anwendungen genutzt, die von Grafik-APIs wie Direct3D 11 oder OpenGL portiert werden, und das Ressourcen Verwaltungsmodell unterscheidet sich deutlich von Direct3D 12.
-   Überschreiben Sie fast alle Heap Prioritäten mit dem eigenen bucketisierungsschema der Anwendung, das entweder korrigiert wurde, basierend auf den Kenntnissen der Zugriffs Häufigkeit des Programmierers oder dynamisch. ein festes Schema ist einfacher zu verwalten als ein dynamisches Schema, kann aber weniger effektiv sein und erfordert, dass sich die Verwendung von Mustern im Verlauf der Entwicklung ändert. Diese Vorgehensweise wird davon ausgegangen, dass Anwendungen, die mit der Ressourcenverwaltung im Direct3D 12-Format erstellt werden, wie jene, die die Residenz Bibliothek (insbesondere dynamische Schemas) verwenden, genutzt werden.

### <a name="default-priority-algorithm"></a>Standardmäßiger Prioritäts Algorithmus

Eine Anwendung kann keine nützlichen Prioritäten für einen Heap angeben, den Sie zu verwalten versucht, ohne zuvor den Standardprioritäts Algorithmus zu überschreiben. Dies liegt daran, dass der Wert, der einem Heap eine bestimmte Priorität zuweist, von seiner relativen Priorität zu anderen priorisierten Heaps abgeleitet wird, die für denselben Arbeitsspeicher konkurrieren.

Die für das Erstellen von Standard Prioritäten gewählte Strategie besteht darin, Heaps in zwei Bucket zu kategorisieren, wodurch Heaps, die häufig von der GPU geschrieben werden, häufig über Heaps geschrieben werden.

Der Bucket mit hoher Priorität enthält Heaps und Ressourcen, die mit Flags erstellt werden, die Sie als Renderziele, tiefen Schablonen Puffer oder unsorderte Zugriffs Sichten (UAVs) identifizieren. Diesen werden Prioritätswerte in dem Bereich zugewiesen, beginnend bei der **D3D12 \_ Residenz \_ Priorität \_ High**. zur weiteren Priorisierung zwischen diesen Heaps und Ressourcen werden die niedrigsten 16 Bits der Priorität auf die Größe des Heaps oder der Ressource dividiert durch 10 MB (für extrem große Heaps mit einer Größe von 0xFFFF) festgelegt. Diese zusätzliche Priorisierung begünstigt größere Heaps und Ressourcen.

Der Bucket mit niedriger Priorität enthält alle anderen Heaps und Ressourcen, denen ein Prioritätswert von **D3D12 \_ Residenz \_ Priorität \_ Normal** zugewiesen wird. Es wird keine weitere Priorisierung zwischen diesen Heaps und Ressourcen versucht.

## <a name="programming-residency-management"></a>Programmieren der Residenz Verwaltung

Einfache Anwendungen sind möglicherweise in der Lage, nur dann zugesicherte Ressourcen zu erstellen, wenn nicht genügend Arbeitsspeicher vorhanden ist. Bei einem Fehler kann die Anwendung andere zugesicherte Ressourcen oder API-Objekte zerstören, um die erfolgreiche Ausführung von Ressourcen zu ermöglichen. Aber auch einfache Anwendungen werden dringend empfohlen, um negative Budgetänderungen zu überwachen und nicht verwendete API-Objekte ungefähr einmal im Rahmen zu zerstören.

Die Komplexität eines terminologieverwaltungdesigns wird bei der Optimierung von Adapter Architekturen oder bei der Einbindung von Residenz Prioritäten erhöht. Diskrete Budgetierung und Verwaltung von zwei Pools mit diskretem Arbeitsspeicher sind komplexer als die Verwaltung von nur einer, und das Zuweisen fester Prioritäten für eine umfangreiche Skalierung kann zu einer wart barkeits Belastung werden, wenn sich die Verwendung von Mustern weiterentwickelt. Das Übertragen von Texturen in den Systemspeicher erhöht die Komplexität, da sich die falsche Ressource im System Arbeitsspeicher schwerwiegend auf die Framerate auswirken kann. Außerdem gibt es keine einfache Funktionalität, um die Ressourcen zu identifizieren, die entweder von einer höheren GPU-Bandbreite oder einer geringeren GPU-Bandbreite profitieren würden.

Noch kompliziertere Entwürfe werden die Features des aktuellen Adapters Abfragen. Diese Informationen finden Sie [**unter D3D12 \_ Feature \_ Data \_ GPU \_ Virtual \_ Address \_ Support**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support), [**D3D12 \_ Feature \_ Data \_ Architecture**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture), [**D3D12 \_ Kachel \_ Resources \_ Tier**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)und [**D3D12 \_ Resource \_ Heap \_ Tier**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_heap_tier).

Mehrere Teile einer Anwendung werden wahrscheinlich mit unterschiedlichen Techniken beschleunigt. Beispielsweise können für einige große Texturen und selten ausgeübte Codepfade Ressourcen mit Commit verwendet werden, während viele Texturen mit einer Streaming-Eigenschaft festgelegt werden können und eine allgemeine Methode für die Ressourcenverwendung verwenden können.

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[Speicherverwaltung](memory-management.md)
</dt> </dl>

 

 