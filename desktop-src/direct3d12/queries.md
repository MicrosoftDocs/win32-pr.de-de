---
title: Abfragen
description: In Direct3D 12 werden Abfragen in Arrays von Abfragen gruppiert, die als Abfragehap bezeichnet werden. Ein Abfragehap verfügt über einen Typ, der die gültigen Typen von Abfragen definiert, die mit diesem Heap verwendet werden können.
ms.assetid: d7403b5d-7e1b-4dd2-ae45-52e1153233c6
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71279c09b59b417535f3155683747ac4c153d7d0fd9f668f79cab9b63ca79805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119241950"
---
# <a name="queries"></a>Abfragen

In Direct3D 12 werden Abfragen in Arrays von Abfragen gruppiert, die als Abfragehap bezeichnet werden. Ein Abfragehap verfügt über einen Typ, der die gültigen Typen von Abfragen definiert, die mit diesem Heap verwendet werden können.

-   [Unterschiede bei Abfragen von Direct3D 11 zu Direct3D 12](#differences-in-queries-from-direct3d-11-to-direct3d-12)
-   [Abfragehaps](#query-heaps)
-   [Erstellen von Abfragehaps](#creating-query-heaps)
-   [Extrahieren von Daten aus einer Abfrage](#extracting-data-from-a-query)
-   [Zugehörige Themen](#related-topics)

## <a name="differences-in-queries-from-direct3d-11-to-direct3d-12"></a>Unterschiede bei Abfragen von Direct3D 11 zu Direct3D 12

Die folgenden Abfragetypen sind in Direct3D 12 nicht mehr vorhanden, und ihre Funktionalität wird in andere Prozesse integriert:

-   **Ereignisabfragen:** Das Ereignis wird jetzt funktional von Fences verarbeitet.
-   **Unteilige Zeitstempelabfragen:** GPU-Uhren können in Direct3D 12 auf einen stabilen Zustand festgelegt werden (siehe Abschnitt [Timing).](timing.md) GPU-Uhrvergleiche sind nicht sinnvoll, wenn die GPU überhaupt zwischen den Zeitstempeln (als disjoint-Abfrage bezeichnet) im Leerlauf war. Mit stabiler Leistung sind zwei Zeitstempelabfragen, die von verschiedenen Befehlslisten ausgegeben werden, zuverlässig vergleichbar. Zwei Zeitstempel innerhalb derselben Befehlsliste sind immer zuverlässig vergleichbar.
-   **Streamen von Ausgabestatistikabfragen:** In Direct3D 12 gibt es keine überlaufbasierte Streamausgabeabfrage (SO) für alle Ausgabestreams. Apps müssen mehrere Einzelstreamabfragen ausführen und dann die Ergebnisse korrelieren.
-   Prädikat- und **Okklusions-Prädikatabfragen** für Streamausgabestatistiken: Abfragen (die in den Arbeitsspeicher schreiben) und [Prädication](predication.md) (die aus dem Arbeitsspeicher lesen) sind nicht mehr gekoppelt, sodass diese Abfragetypen nicht mehr benötigt werden.

Direct3D 12 wurde ein neuer Abfragetyp für die binäre Verdecken hinzugefügt. Dies ermöglicht Prädication-Strategien, die nur darauf achten, ob ein Objekt vollständig verblendet war (und nicht wie viele Pixel verblendet wurden), um dies dem Gerät anzuzeigen, was die Abfragen möglicherweise effizienter ausführen kann.

## <a name="query-heaps"></a>Abfragehaps

Abfragen können aus einer Reihe von Typen [**(D3D12 \_ QUERY \_ HEAP \_ TYPE)**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type)sein und werden in Abfragehaps unterteilt, bevor sie an die GPU übermittelt werden.

Ein neuer Abfragetyp D3D12 QUERY TYPE BINARY OCCLUSION ist verfügbar und verhält sich wie \_ \_ \_ \_ D3D12 QUERY TYPE OCCLUSION, gibt jedoch ein binäres \_ \_ \_ 0/1-Ergebnis zurück: 0 gibt an, dass keine Stichproben die Tiefen- und Schablonentests bestanden haben. 1 gibt an, dass mindestens ein Beispiel die Tiefen- und Schablonentests bestanden hat. Dadurch können Okklusionsabfragen keine GPU-Leistungsoptimierung beeinträchtigen, die mit Tiefen-/Schablonentests verbunden ist.

## <a name="creating-query-heaps"></a>Erstellen von Abfragehaps

Die für das Erstellen von Abfrageheaps relevanten APIs sind die Enum [**D3D12 \_ QUERY \_ HEAP \_ TYPE,**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type)die Struktur [**D3D12 \_ QUERY \_ HEAP \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc)und die [**CreateQueryHeap-Methode.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap)

Die Kernlaufzeit überprüft, ob der Abfragehaptyp ein gültiger Member der [**\_ HEAP \_ TYPE-Enumeration D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) ist und ob die Anzahl größer als 0 ist.

Jedes einzelne Abfrageelement innerhalb eines Abfragehaps kann separat gestartet und beendet werden.

Die APIs für die Verwendung der Abfragehaps sind die Enum [**D3D12 \_ QUERY \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)und die [**Methoden BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) und [**EndQuery.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)

D3D12 \_ QUERY \_ TYPE \_ TIMESTAMP ist die einzige Abfrage, die [**nur EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) unterstützt. Alle anderen Abfragetypen erfordern [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) und **EndQuery.**

Die Debugebene überprüft Folgendes:

-   Es ist unzulässig, eine Zeitstempelabfrage zu &mdash; starten, die Sie nur beenden können.
-   Es ist unzulässig, eine Abfrage zweimal zu starten, ohne sie zu beenden (für ein bestimmtes Element). Für Abfragen, die sowohl begin als auch end erfordern, ist es unzulässig, eine Abfrage vor dem entsprechenden Anfang (für ein bestimmtes Element) zu beenden.
-   Der an [**BeginQuery übergebene**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) Abfragetyp muss mit dem Abfragetyp übereinstimmen, der an [**EndQuery übergeben wird.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)

Die Kernlaufzeit überprüft Folgendes:

-   [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) kann nicht für eine Zeitstempelabfrage aufgerufen werden.
-   Für die Abfragetypen, die [**beginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) und [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) unterstützen (alle außer timestamp), darf eine Abfrage für ein bestimmtes Element keine Befehlslistengrenzen umfassen.
-   *ElementIndex* muss innerhalb des Bereichs liegen.
-   Der Abfragetyp ist ein gültiger Member der [**D3D12 \_ QUERY TYPE-Aufenumerung. \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)
-   Der Abfragetyp muss mit dem Abfragehap kompatibel sein. Die folgende Tabelle zeigt den Abfragehaptyp, der für jeden Abfragetyp erforderlich ist:

    

    | Abfragetyp                                  | Abfragehaptyp                                |
    |---------------------------------------------|------------------------------------------------|
    | D3D12 \_ QUERY \_ TYPE \_ OCCLUSION               | D3D12 \_ QUERY \_ HEAP \_ TYPE \_ OCCLUSION            |
    | D3D12 \_ QUERY \_ TYPE \_ BINARY \_ OCCLUSION       | D3D12 \_ QUERY \_ HEAP \_ TYPE \_ OCCLUSION            |
    | D3D12 \_ QUERY \_ TYPE \_ TIMESTAMP               | D3D12 \_ QUERY \_ HEAP \_ TYPE \_ TIMESTAMP            |
    | PIPELINESTATISTIK DES \_ D3D12-ABFRAGETYPS \_ \_ \_    | D3D12 \_ QUERY \_ HEAP \_ TYPE \_ PIPELINE \_ STATISTICS |
    | D3D12-ABFRAGETYP, \_ \_ SODASS STATISTICS \_ \_ \_ STREAM0 | D3D12 \_ QUERY \_ HEAP \_ TYPE \_ SO \_ STATISTICS       |
    | D3D12-ABFRAGETYP \_ \_ SO STATISTICS \_ \_ \_ STREAM1 | D3D12 \_ QUERY \_ HEAP \_ TYPE \_ SO \_ STATISTICS       |
    | D3D12-ABFRAGETYP \_ \_ SO STATISTICS \_ \_ \_ STREAM2 | D3D12 \_ QUERY \_ HEAP \_ TYPE \_ SO \_ STATISTICS       |
    | D3D12-ABFRAGETYP \_ \_ SO STATISTICS \_ \_ \_ STREAM3 | D3D12 \_ QUERY \_ HEAP \_ TYPE \_ SO \_ STATISTICS       |

    

     

-   Der Abfragetyp wird vom Befehlslistentyp unterstützt. Die folgende Tabelle zeigt, welche Abfragen für welche Befehlslistentypen unterstützt werden.

    

    | Abfragetyp                                  | Unterstützte Befehlslistentypen         |
    |---------------------------------------------|--------------------------------------|
    | D3D12 \_ QUERY \_ TYPE \_ OCCLUSION               | Direkt                               |
    | D3D12 \_ QUERY \_ TYPE \_ BINARY \_ OCCLUSION       | Direkt                               |
    | D3D12 \_ QUERY \_ TYPE \_ TIMESTAMP               | Direkt, Compute und optional Kopieren |
    | PIPELINESTATISTIK DES \_ D3D12-ABFRAGETYPS \_ \_ \_    | Direkt                               |
    | D3D12-ABFRAGETYP, \_ \_ SODASS STATISTICS \_ \_ \_ STREAM0 | Direkt                               |
    | D3D12-ABFRAGETYP \_ \_ SO STATISTICS \_ \_ \_ STREAM1 | Direkt                               |
    | D3D12-ABFRAGETYP \_ \_ SO STATISTICS \_ \_ \_ STREAM2 | Direkt                               |
    | D3D12-ABFRAGETYP \_ \_ SO STATISTICS \_ \_ \_ STREAM3 | Direkt                               |

    

     

## <a name="extracting-data-from-a-query"></a>Extrahieren von Daten aus einer Abfrage

Die Methode zum Extrahieren von Daten aus einer Abfrage ist die [**Verwendung der ResolveQueryData-Methode.**](/windows/win32p/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata) **ResolveQueryData** funktioniert mit allen Speichertypen (unabhängig davon, ob es sich um Systemspeicher oder lokalen Speicher des Geräts handelt), erfordert jedoch, dass sich die Zielressource in [**D3D12_RESOURCE_STATE_COPY_DEST.**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) 

## <a name="related-topics"></a>Zugehörige Themen

* [Leistungsindikatoren und Abfragen](counters-and-queries.md)
* [Exemplarische Vorgehensweise für Prädication-Abfragen](predication-queries.md)
