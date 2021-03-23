---
title: Abfragen
description: In Direct3D 12 werden Abfragen in Arrays von Abfragen gruppiert, die als Abfrage Heap bezeichnet werden. Ein Abfrage Heap weist einen Typ auf, der die gültigen Abfrage Typen definiert, die mit diesem Heap verwendet werden können.
ms.assetid: d7403b5d-7e1b-4dd2-ae45-52e1153233c6
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22c4db895eb0d4a727db2e32757f7ab0f1f9b1e2
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "104548723"
---
# <a name="queries"></a>Abfragen

In Direct3D 12 werden Abfragen in Arrays von Abfragen gruppiert, die als Abfrage Heap bezeichnet werden. Ein Abfrage Heap weist einen Typ auf, der die gültigen Abfrage Typen definiert, die mit diesem Heap verwendet werden können.

-   [Unterschiede bei Abfragen von Direct3D 11 bis Direct3D 12](#differences-in-queries-from-direct3d-11-to-direct3d-12)
-   [Abfrage Heaps](#query-heaps)
-   [Erstellen von Abfrage Heaps](#creating-query-heaps)
-   [Extrahieren von Daten aus einer Abfrage](#extracting-data-from-a-query)
-   [Verwandte Themen](#related-topics)

## <a name="differences-in-queries-from-direct3d-11-to-direct3d-12"></a>Unterschiede bei Abfragen von Direct3D 11 bis Direct3D 12

Die folgenden Abfrage Typen sind in Direct3D 12 nicht mehr vorhanden, ihre Funktionalität wird in andere Prozesse integriert:

-   **Ereignis Abfragen** : Ereignis funktionell wird jetzt von Zäunen behandelt.
-   **Disjoint Zeitstempel-Abfragen** : GPU-Uhren können in Direct3D 12 auf einen stabilen Zustand festgelegt werden (siehe Abschnitt " [zeitlichen Steuerung](timing.md) "). Die GPU-Takt Vergleiche sind nicht sinnvoll, wenn die GPU zwischen den Zeitstempeln (als nicht zusammenhängende Abfrage bezeichnet) zusammengeführt hat. Mit stabiler Leistung sind zwei Zeitstempel-Abfragen, die von verschiedenen Befehlslisten ausgegeben werden, zuverlässig vergleichbar. Zwei Zeitstempel innerhalb derselben Befehlsliste sind immer zuverlässig vergleichbar.
-   **Stream Output Statistics-Abfragen** : in Direct3D 12 gibt es keine einzelne Stream-Ausgabe (so) Überlauf Abfrage für alle Ausgabedaten Ströme. Apps müssen mehrere einzelstreamabfragen ausgeben und dann die Ergebnisse korrelieren.
-   **Stream Output Statistics-Prädikat-und Okklusions-Prädikat Abfragen** -Abfragen (die in den Arbeitsspeicher schreiben) und [Prädikate](predication.md) (die aus dem Arbeitsspeicher gelesen werden) sind nicht mehr gekoppelt, sodass diese Abfrage Typen nicht mehr benötigt werden.

Direct3D 12 wurde ein neuer Abfragetyp für binäre Okklusion hinzugefügt. Dies ermöglicht prädikationstrategien, die nur darauf achten, ob ein Objekt vollständig oder nicht vollständig oder nicht (anstatt wie viele Pixel verdeckt wurden), um dies für das Gerät anzugeben, wodurch die Abfragen möglicherweise effizienter durchgeführt werden können.

## <a name="query-heaps"></a>Abfrage Heaps

Abfragen können aus einer Reihe von Typen ([**D3D12 \_ Query \_ Heap \_ Type**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type)) stammen und vor der Übermittlung an die GPU in Abfrage Heaps gruppiert werden.

Ein neuer Abfragetyp D3D12 \_ \_ \_ \_ die binäre Okklusion der Abfrage Typen ist verfügbar und verhält sich wie die D3D12- \_ abfragetypoksion \_ \_ , mit der Ausnahme, dass ein binäres 0/1-Ergebnis zurückgegeben wird: 0 gibt an, dass keine Stichproben Tiefe und Schablonen getestet wurden, 1 gibt an, dass mindestens eine Stichprobe Dies ermöglicht es, dass eine GPU-Leistungsoptimierung, die mit tiefen-/Stencil-Tests verknüpft ist, nicht beeinträchtigt wird.

## <a name="creating-query-heaps"></a>Erstellen von Abfrage Heaps

Die für das Erstellen von Abfrage Heaps relevanten APIs sind der [**\_ \_ \_ Enumerationstyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type)"enumerationsD3D12", die Struktur [**D3D12 \_ Abfrage \_ Heap- \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc)und die Methode " [**kreatequeryheap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap)".

Die Core-Laufzeit überprüft, ob der abfrageheap ein gültiger Member der [**D3D12 \_ Heap \_ Type**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) -Enumeration und die Anzahl größer als 0 ist.

Jedes einzelne Query-Element in einem Abfrage Heap kann separat gestartet und beendet werden.

Die APIs für die Verwendung der Abfrage Heaps sind der [](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) [**\_ \_ Enumerationstyp D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)und die Methoden beginquery und [**endquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery).

Der D3D12- \_ Abfragetyp \_ \_ timestamp ist die einzige Abfrage, die nur [**endquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) unterstützt. Alle anderen Abfrage Typen erfordern [**beginquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) und **endquery**.

Die debugschicht überprüft Folgendes:

-   Es ist unzulässig, eine Zeitstempel-Abfrage zu starten, die &mdash; Sie nur beenden können.
-   Es ist unzulässig, eine Abfrage zweimal zu starten, ohne Sie zu beenden (für ein bestimmtes Element). Bei Abfragen, die sowohl BEGIN als auch End erfordern, ist es unzulässig, eine Abfrage vor dem entsprechenden Begin (für ein bestimmtes Element) zu beenden.
-   Der an [**beginquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) übergebenen Abfragetyp muss mit dem Abfragetyp für [**endquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)identisch sein.

Die Core-Laufzeit überprüft Folgendes:

-   [**Beginquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) kann nicht für eine Zeitstempel-Abfrage aufgerufen werden.
-   Für die Abfrage Typen, die sowohl [**beginquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) als auch [**endquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) unterstützen (mit Ausnahme von timestamp), darf eine Abfrage für ein bestimmtes Element nicht die Befehlslisten Grenzen überschreiten.
-   *Elementindex* muss innerhalb des gültigen Bereichs liegen.
-   Der Abfragetyp ist ein gültiger Member der [**D3D12- \_ Abfragetyp \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type) -Enumeration.
-   Der Abfragetyp muss mit dem Abfrage Heap kompatibel sein. In der folgenden Tabelle wird der für jeden Abfragetyp erforderliche abfrageheap angezeigt:

    

    | Abfragetyp                                  | Abfrage heaptyp                                |
    |---------------------------------------------|------------------------------------------------|
    | D3D12 \_ - \_ abfragetypoksion \_               | D3D12- \_ Abfrage \_ Heap- \_ \_ typokklusion            |
    | D3D12 \_ - \_ \_ typbinär- \_ Okklusion       | D3D12- \_ Abfrage \_ Heap- \_ \_ typokklusion            |
    | D3D12 \_ - \_ Abfragetyp \_ Zeitstempel               | D3D12 \_ - \_ \_ \_ Zeitstempel des Abfrage Heap Typs            |
    | D3D12 \_ Pipeline Statistiken für Abfragetyp \_ \_ \_    | D3D12 \_ \_ \_ \_ Pipeline Statistiken des Abfrage Heap Typs \_ |
    | D3D12 \_ Query \_ Type \_ so \_ Statistics \_ STREAM0 | D3D12 \_ Query \_ Heap \_ Type \_ so \_ Statistics       |
    | D3D12 \_ Query \_ Type \_ so \_ Statistics \_ STREAM1 | D3D12 \_ Query \_ Heap \_ Type \_ so \_ Statistics       |
    | D3D12 \_ Query \_ Type \_ so \_ Statistics \_ STREAM2 | D3D12 \_ Query \_ Heap \_ Type \_ so \_ Statistics       |
    | D3D12 \_ Query \_ Type \_ so \_ Statistics \_ STREAM3 | D3D12 \_ Query \_ Heap \_ Type \_ so \_ Statistics       |

    

     

-   Der Abfragetyp wird vom Befehls Auflistungstyp unterstützt. In der folgenden Tabelle wird gezeigt, welche Abfragen für welche Befehlslisten Typen unterstützt werden.

    

    | Abfragetyp                                  | Unterstützte Befehlslisten Typen         |
    |---------------------------------------------|--------------------------------------|
    | D3D12 \_ - \_ abfragetypoksion \_               | Direkt                               |
    | D3D12 \_ - \_ \_ typbinär- \_ Okklusion       | Direkt                               |
    | D3D12 \_ - \_ Abfragetyp \_ Zeitstempel               | Direkt, COMPUTE und optional kopieren |
    | D3D12 \_ Pipeline Statistiken für Abfragetyp \_ \_ \_    | Direkt                               |
    | D3D12 \_ Query \_ Type \_ so \_ Statistics \_ STREAM0 | Direkt                               |
    | D3D12 \_ Query \_ Type \_ so \_ Statistics \_ STREAM1 | Direkt                               |
    | D3D12 \_ Query \_ Type \_ so \_ Statistics \_ STREAM2 | Direkt                               |
    | D3D12 \_ Query \_ Type \_ so \_ Statistics \_ STREAM3 | Direkt                               |

    

     

## <a name="extracting-data-from-a-query"></a>Extrahieren von Daten aus einer Abfrage

Die Methode zum Extrahieren von Daten aus einer Abfrage besteht darin, die [**resolvequerydata**](/windows/win32p/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata) -Methode zu verwenden. " **Resolvequerydata** " funktioniert mit allen Speichertypen (unabhängig davon, ob es sich um System Arbeitsspeicher oder lokale Gerätespeicher handelt), erfordert jedoch, dass die Ziel Ressource in [**D3D12_RESOURCE_STATE_COPY_DEST**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)ist. 

## <a name="related-topics"></a>Verwandte Themen

* [Zähler und Abfragen](counters-and-queries.md)
* [Exemplarische Vorgehensweise für prediationqueries](predication-queries.md)
