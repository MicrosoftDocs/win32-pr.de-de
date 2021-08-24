---
title: Abfragen
description: In Direct3D 12 werden Abfragen in Arrays von Abfragen gruppiert, die als Abfrageheap bezeichnet werden. Ein Abfrageheap verfügt über einen Typ, der die gültigen Abfragetypen definiert, die mit diesem Heap verwendet werden können.
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

In Direct3D 12 werden Abfragen in Arrays von Abfragen gruppiert, die als Abfrageheap bezeichnet werden. Ein Abfrageheap verfügt über einen Typ, der die gültigen Abfragetypen definiert, die mit diesem Heap verwendet werden können.

-   [Unterschiede bei Abfragen von Direct3D 11 zu Direct3D 12](#differences-in-queries-from-direct3d-11-to-direct3d-12)
-   [Abfrageheaps](#query-heaps)
-   [Erstellen von Abfrageheaps](#creating-query-heaps)
-   [Extrahieren von Daten aus einer Abfrage](#extracting-data-from-a-query)
-   [Zugehörige Themen](#related-topics)

## <a name="differences-in-queries-from-direct3d-11-to-direct3d-12"></a>Unterschiede bei Abfragen von Direct3D 11 zu Direct3D 12

Die folgenden Abfragetypen sind in Direct3D 12 nicht mehr vorhanden, da ihre Funktionalität in andere Prozesse integriert wird:

-   **Ereignisabfragen:** Das Ereignis wird jetzt funktional von Fences verarbeitet.
-   **Unzusammenhängende Zeitstempelabfragen:** GPU-Uhren können in Direct3D 12 auf einen stabilen Zustand festgelegt werden (siehe Abschnitt [Zeitsteuerung).](timing.md) GPU-Uhrvergleiche sind nicht sinnvoll, wenn sich die GPU zwischen den Zeitstempeln (als unzusammenhängende Abfrage bezeichnet) im Leerlauf befindet. Mit stabiler Leistung sind zwei Zeitstempelabfragen, die aus verschiedenen Befehlslisten ausgegeben werden, zuverlässig vergleichbar. Zwei Zeitstempel innerhalb derselben Befehlsliste sind immer zuverlässig vergleichbar.
-   Abfragen von **Datenstromausgabestatistiken:** In Direct3D 12 gibt es keine Überlaufabfrage für einzelne Datenstromausgaben (So) für alle Ausgabestreams. Apps müssen mehrere Einzelstreamabfragen ausstellen und dann die Ergebnisse korrelieren.
-   **Datenstromausgabestatistik-Prädikat- und Okklusionsprädikatabfragen** : Abfragen (die in den Arbeitsspeicher schreiben) und [Prädikation](predication.md) (lese aus dem Arbeitsspeicher) sind nicht mehr gekoppelt, sodass diese Abfragetypen nicht mehr benötigt werden.

Direct3D 12 wurde ein neuer binärer Verdeckungsabfragetyp hinzugefügt. Dies ermöglicht Prädikationsstrategien, bei denen nur darauf geachtet wird, ob ein Objekt vollständig verdeckungsfähig war (anstatt wie viele Pixel verdeckt wurden), um dies dem Gerät anzuzeigen, wodurch die Abfragen möglicherweise effizienter ausgeführt werden können.

## <a name="query-heaps"></a>Abfrageheaps

Abfragen können aus einer Reihe von Typen [**(D3D12 \_ QUERY \_ HEAP \_ TYPE)**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type)stammen und werden in Abfrageheaps gruppiert, bevor sie an die GPU übermittelt werden.

Ein neuer Abfragetyp D3D12 \_ QUERY \_ TYPE BINARY \_ \_ OCCLUSION ist verfügbar und verhält sich wie D3D12 \_ QUERY TYPE \_ \_ OCCLUSION, gibt jedoch ein binäres 0/1-Ergebnis zurück: 0 gibt an, dass keine Stichproben Tiefen- und Schablonentests bestanden haben, 1 gibt an, dass mindestens eine Stichprobe Tiefen- und Schablonentests bestanden hat. Dadurch können Verdeckungsabfragen keine Auswirkungen auf gpu-Leistungsoptimierungen im Zusammenhang mit Tiefen-/Schablonentests haben.

## <a name="creating-query-heaps"></a>Erstellen von Abfrageheaps

Die APIs, die für die Erstellung von Abfrageheaps relevant sind, sind die Enumeration [**D3D12 \_ QUERY \_ HEAP \_ TYPE,**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type)die Struktur [**D3D12 \_ QUERY HEAP \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc)und die [**Methode CreateQueryHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap).

Die Kernlaufzeit überprüft, ob der Abfrageheaptyp ein gültiger Member der [**D3D12 \_ HEAP \_ TYPE-Enumeration**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) ist und ob die Anzahl größer als 0 ist.

Jedes einzelne Abfrageelement innerhalb eines Abfrageheaps kann separat gestartet und beendet werden.

Die APIs für die Verwendung der Abfrageheaps sind die Enumeration [**D3D12 \_ QUERY \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)und die Methoden [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) und [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery).

D3D12 \_ QUERY \_ TYPE \_ TIMESTAMP ist die einzige Abfrage, die nur [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) unterstützt. Alle anderen Abfragetypen erfordern [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) und **EndQuery.**

Die Debugebene überprüft Folgendes:

-   Es ist unzulässig, eine Zeitstempelabfrage zu starten, &mdash; die Sie nur beenden können.
-   Es ist unzulässig, eine Abfrage zweimal zu starten, ohne sie zu beenden (für ein bestimmtes Element). Bei Abfragen, die sowohl begin als auch end erfordern, ist es unzulässig, eine Abfrage vor dem entsprechenden Anfang (für ein bestimmtes Element) zu beenden.
-   Der an [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) übergebene Abfragetyp muss mit dem Abfragetyp übereinstimmen, der an [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)übergeben wird.

Die Kernlaufzeit überprüft Folgendes:

-   [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) kann nicht für eine Zeitstempelabfrage aufgerufen werden.
-   Für die Abfragetypen, die sowohl [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) als auch [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) unterstützen (alle außer timestamp), darf eine Abfrage für ein bestimmtes Element keine Befehlslistengrenzen umfassen.
-   *ElementIndex* muss innerhalb des Bereichs liegen.
-   Der Abfragetyp ist ein gültiger Member der [**D3D12 \_ QUERY \_ TYPE-Enumeration.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)
-   Der Abfragetyp muss mit dem Abfrageheap kompatibel sein. Die folgende Tabelle zeigt den Für jeden Abfragetyp erforderlichen Abfrageheaptyp:

    

    | Abfragetyp                                  | Abfrageheaptyp                                |
    |---------------------------------------------|------------------------------------------------|
    | D3D12-ABFRAGETYP \_ \_ \_ OCCLUSION               | \_D3D12-ABFRAGEHEAPTYP \_ \_ \_ OCCLUSION            |
    | D3D12-ABFRAGETYP \_ \_ \_ \_ BINÄRE VERDECKUNG       | \_D3D12-ABFRAGEHEAPTYP \_ \_ \_ OCCLUSION            |
    | D3D12-ABFRAGETYP \_ \_ \_ TIMESTAMP               | \_D3D12-ABFRAGEHEAPTYP \_ \_ \_ TIMESTAMP            |
    | \_ \_ \_ D3D12-ABFRAGETYP – \_ PIPELINESTATISTIKEN    | PIPELINESTATISTIKEN ZUM \_ D3D12-ABFRAGEHEAPTYP \_ \_ \_ \_ |
    | D3D12-ABFRAGETYP \_ \_ SO STATISTICS \_ \_ \_ STREAM0 | D3D12 \_ QUERY \_ HEAP \_ TYPE \_ SO \_ STATISTICS       |
    | D3D12-ABFRAGETYP \_ \_ SO STATISTICS \_ \_ \_ STREAM1 | D3D12 \_ QUERY \_ HEAP \_ TYPE \_ SO \_ STATISTICS       |
    | D3D12-ABFRAGETYP \_ \_ SO STATISTICS \_ \_ \_ STREAM2 | D3D12 \_ QUERY \_ HEAP \_ TYPE \_ SO \_ STATISTICS       |
    | D3D12-ABFRAGETYP \_ \_ SO STATISTICS \_ \_ \_ STREAM3 | D3D12 \_ QUERY \_ HEAP \_ TYPE \_ SO \_ STATISTICS       |

    

     

-   Der Abfragetyp wird vom Befehlslistentyp unterstützt. Die folgende Tabelle zeigt, welche Abfragen für welche Befehlslistentypen unterstützt werden.

    

    | Abfragetyp                                  | Unterstützte Befehlslistentypen         |
    |---------------------------------------------|--------------------------------------|
    | D3D12-ABFRAGETYP \_ \_ \_ OCCLUSION               | Direkt                               |
    | D3D12-ABFRAGETYP \_ \_ \_ \_ BINÄRE VERDECKUNG       | Direkt                               |
    | D3D12-ABFRAGETYP \_ \_ \_ TIMESTAMP               | Direkt, Compute und optional Kopieren |
    | \_ \_ \_ D3D12-ABFRAGETYP – \_ PIPELINESTATISTIKEN    | Direkt                               |
    | D3D12-ABFRAGETYP \_ \_ SO STATISTICS \_ \_ \_ STREAM0 | Direkt                               |
    | D3D12-ABFRAGETYP \_ \_ SO STATISTICS \_ \_ \_ STREAM1 | Direkt                               |
    | D3D12-ABFRAGETYP \_ \_ SO STATISTICS \_ \_ \_ STREAM2 | Direkt                               |
    | D3D12-ABFRAGETYP \_ \_ SO STATISTICS \_ \_ \_ STREAM3 | Direkt                               |

    

     

## <a name="extracting-data-from-a-query"></a>Extrahieren von Daten aus einer Abfrage

Die Methode zum Extrahieren von Daten aus einer Abfrage ist die Verwendung der [**ResolveQueryData-Methode.**](/windows/win32p/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata) **ResolveQueryData** funktioniert mit allen Speichertypen (unabhängig davon, ob es sich um Systemspeicher oder lokalen Gerätespeicher handelt), erfordert jedoch, dass sich die Zielressource in [**D3D12_RESOURCE_STATE_COPY_DEST**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)befindet. 

## <a name="related-topics"></a>Zugehörige Themen

* [Leistungsindikatoren und Abfragen](counters-and-queries.md)
* [Exemplarische Informationen zu Prädikationsabfragen](predication-queries.md)
