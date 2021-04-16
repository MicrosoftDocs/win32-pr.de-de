---
description: Lak
ms.assetid: 868218c4-3e1a-4da0-89fa-30a9848da0e8
title: Lak
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 575f311020c2c7a567e544b80ba323a29051cc38
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522400"
---
# <a name="flushing"></a>Lak

Während das Filter Diagramm ausgeführt wird, können beliebige Datenmengen durch das Diagramm verschoben werden. Einige davon befinden sich möglicherweise in Warteschlangen, die darauf warten, übermittelt zu werden. In manchen Zeiten muss das Filter Diagramm diese ausstehenden Daten so schnell wie möglich entfernen und durch neue Daten ersetzen. Nach einem Seek-Befehl generiert der Quell Filter beispielsweise Beispiele aus einer neuen Position in der Quelle. Um die Latenz zu minimieren, sollten downstreamfilter alle Beispiele verwerfen, die vor dem Seek-Befehl erstellt wurden. Der Prozess zum Verwerfen von Beispielen *wird als* Leerung bezeichnet. Dadurch kann der Graph reaktionsfähiger werden, wenn Ereignisse den normalen Datenfluss ändern.

Das leeren wird durch das Pull-Modell etwas anders gehandhabt als das Push-Modell. In diesem Artikel wird zunächst das Pushmodell beschrieben. Anschließend werden die Unterschiede im Pull-Modell beschrieben.

Das leeren erfolgt in zwei Phasen.

-   Zuerst ruft der Quell Filter [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) in der Eingabe-PIN des downstreamfilters auf. Der downstreamfilter beginnt mit dem ablehnen von Beispielen aus dem Upstream. Außerdem werden alle darin enthaltenen Stichproben verworfen und der **beginflush** -Befehl Downstream an den nächsten Filter gesendet.
-   Wenn der Quell Filter bereit ist, neue Daten zu senden, ruft er [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) für die Eingabe-PIN auf. Dies signalisiert dem Downstream-Filter, dass neue Beispiele empfangen werden können. Der Downstream-Filter sendet den **endflush** -aufrufbefehl an den nächsten Filter.

In der **beginflush** -Methode führt die Eingabe-PIN Folgendes aus:

1.  Ruft **beginflush** für nachgeschaltete Eingabe Pins auf.
2.  Lehnt alle weiteren Aufrufe ab, die Daten streamen, einschließlich **Receive** und **EndOf Stream**.
3.  Hebt die Blockierung aller upstreamfilter auf, die blockiert werden, um auf eine Stichprobe aus der Zuweisung des Filters zu warten. Einige Filter nehmen zu diesem Zweck die Zuweisung ihrer Zuweisungen vor.
4.  Beendet von allen warte Vorgängen, die Streaming blockieren. Beispielsweise blockieren rendererfilter, wenn Sie angehalten werden. Außerdem blockieren Sie, wenn Sie darauf warten, ein Beispiel zur richtigen streamzeit zu erzeugen. Die Blockierung des Filters muss aufgehoben werden, sodass Beispiele in der Warteschlange eingereiht und abgelehnt werden können. Mit diesem Schritt wird sichergestellt, dass alle upstreamfilter schließlich die Blockierung

In der **endflush** -Methode führt die Eingabe-PIN Folgendes aus:

1.  Wartet darauf, dass alle in der Warteschlange befindlichen Stichproben verworfen werden.
2.  Gibt alle gepufferten Daten frei. Dieser Schritt kann manchmal in der **beginflush** -Methode ausgeführt werden. **Beginflush** wird jedoch nicht mit dem streamingthread synchronisiert. Der Filter darf keine weiteren Daten zwischen dem Aufrufen von **beginflush** und dem Aufrufen von **endflush** verarbeiten oder Puffern.
3.  Löscht alle ausstehenden "EC Complete"- \_ Benachrichtigungen.
4.  Ruft **endflush** Downstream ab.

An diesem Punkt kann der Filter erneut Beispiele akzeptieren. Es ist sichergestellt, dass alle Beispiele aktueller sind als die Leerungen.

Im Pull-Modell initiiert der Parserfilter das leeren anstelle des Quell Filters. Er ruft nicht nur **IPin:: beginflush** und **IPin:: endflush** für den downstreamfilter auf, sondern ruft auch [**iasynkreader:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-beginflush) und [**iasynkreader:: endflush**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-endflush) in der *Ausgabe* -PIN des Quell Filters auf. Wenn der Quell Filter ausstehende Lese Anforderungen aufweist, werden diese verworfen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Leeren von Daten](flushing-data.md)
</dt> </dl>

 

 



