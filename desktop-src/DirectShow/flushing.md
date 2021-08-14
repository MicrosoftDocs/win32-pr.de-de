---
description: Spülung
ms.assetid: 868218c4-3e1a-4da0-89fa-30a9848da0e8
title: Spülung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e70f610a68b2ca81afff736b3e7402d80e5d5675e429d1715ebebf5b640a362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401744"
---
# <a name="flushing"></a>Spülung

Während das Filterdiagramm ausgeführt wird, können beliebige Datenmengen durch das Diagramm verschoben werden. Einige davon befinden sich möglicherweise in Warteschlangen und warten auf die Zustellung. Es gibt Zeiten, in denen das Filterdiagramm diese ausstehenden Daten so schnell wie möglich entfernen und durch neue Daten ersetzen muss. Nach einem Suchbefehl generiert der Quellfilter beispielsweise Stichproben von einer neuen Position in der Quelle. Zur Minimierung der Latenz sollten Downstreamfilter alle Stichproben verwerfen, die vor dem Suchbefehl erstellt wurden. Der Prozess zum Verwerfen von Beispielen wird als *Leeren* von bezeichnet. Dadurch kann das Diagramm reaktionsfähiger sein, wenn Ereignisse den normalen Datenfluss ändern.

Das Leeren wird vom Pullmodell etwas anders behandelt als das Pushmodell. In diesem Artikel wird zunächst das Pushmodell beschrieben. anschließend werden die Unterschiede im Pullmodell beschrieben.

Das Leeren erfolgt in zwei Phasen.

-   Zunächst ruft der Quellfilter [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) auf dem Eingabepin des Downstreamfilters auf. Der Downstreamfilter beginnt mit dem Ablehnen von Stichproben aus upstream. Außerdem werden alle enthaltenen Stichproben verworfen, und der **BeginFlush-Aufruf** wird an den nächsten Filter gesendet.
-   Wenn der Quellfilter zum Senden neuer Daten bereit ist, ruft er [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) auf dem Eingabepin auf. Dies signalisiert dem Downstreamfilter, dass er neue Stichproben erhalten kann. Der Downstreamfilter sendet den **EndFlush-Aufruf** an den nächsten Filter.

In der **BeginFlush-Methode** führt der Eingabepin folgende Schritte aus:

1.  Ruft **BeginFlush** für nachgeschaltete Eingabepins auf.
2.  Lehnt alle weiteren Aufrufe ab, die Daten streamen, einschließlich **Receive** und **EndOfStream.**
3.  Entsperrt alle Upstreamfilter, die blockiert sind und auf ein Beispiel aus der Zuweisung des Filters warten. Einige Filter dekomprimieren ihre Zuweisungen für diesen Zweck.
4.  Beendet alle Wartezeiten, die das Streaming blockieren. Rendererfilter blockieren beispielsweise, wenn sie angehalten werden. Sie blockieren auch, wenn sie darauf warten, ein Beispiel zur richtigen Streamzeit zu rendern. Die Blockierung des Filters muss aufgehoben werden, damit Vorgeschaltete Stichproben in der Warteschlange übermittelt und abgelehnt werden können. Dieser Schritt stellt sicher, dass alle Upstreamfilter schließlich die Blockierung aufheben.

In der **EndFlush-Methode** führt der Eingabepin folgende Schritte aus:

1.  Wartet, bis alle in der Warteschlange enthaltenen Beispiele verworfen werden.
2.  Gibt alle gepufferten Daten frei. Dieser Schritt kann manchmal in der **BeginFlush-Methode** ausgeführt werden. **BeginFlush** wird jedoch nicht mit dem Streamingthread synchronisiert. Der Filter darf keine weiteren Daten zwischen dem Aufruf von **BeginFlush** und dem Aufruf von **EndFlush** verarbeiten oder puffern.
3.  Löscht alle ausstehenden EC \_ COMPLETE-Benachrichtigungen.
4.  Ruft **EndFlush** downstream auf.

An diesem Punkt kann der Filter erneut Beispiele akzeptieren. Alle Stichproben sind garantiert aktueller als die Leerung.

Im Pullmodell initiiert der Parserfilter das Leeren anstelle des Quellfilters. Sie ruft nicht nur **IPin::BeginFlush** und **IPin::EndFlush** im Downstreamfilter auf, sondern ruft auch [**IAsyncReader::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-beginflush) und [**IAsyncReader::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-endflush) auf dem *Ausgabepin* des Quellfilters auf. Wenn für den Quellfilter ausstehende Leseanforderungen stehen, werden diese verworfen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Leeren von Daten](flushing-data.md)
</dt> </dl>

 

 



