---
description: Rufen Sie nach dem Erstellen einer Abfrage und dem Hinzufügen von Leistungsindikatoren die PdhCollectQueryData-Funktion auf, um die aktuellen Rohdaten für alle Leistungsindikatoren in der Abfrage abzurufen.
ms.assetid: 2534d387-a280-4716-9a9d-3e42f40e2f92
title: Sammeln von Leistungsdaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79f65280190e67e27783ea7e7387eac0e348aad1a53ad016df3010ae0bfd2ea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061238"
---
# <a name="collecting-performance-data"></a>Sammeln von Leistungsdaten

Rufen Sie nach dem [Erstellen einer Abfrage](creating-a-query.md) und dem Hinzufügen von Leistungsindikatoren die [**PdhCollectQueryData-Funktion**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) auf, um die aktuellen Rohdaten für alle Leistungsindikatoren in der Abfrage abzurufen.

Viele Indikatoren, z. B. Ratenzähler, erfordern zwei Datenstichproben, um einen formatierten Datenwert zu berechnen. PDH verwaltet Daten für das aktuelle Beispiel und das zuvor erfasste Beispiel. Im folgenden Verfahren wird beschrieben, wie Leistungsindikatorwerte erfasst werden, die zwei Stichproben erfordern, um einen anzeigebaren Wert zu berechnen.

**So erfassen Sie Indikatorwerte, die zwei Stichproben erfordern, um einen anzeigebaren Wert zu berechnen**

1.  Rufen Sie [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) auf, um das erste Beispiel zu erfassen.
2.  Rufen Sie die [**Sleep-Funktion**](/windows/desktop/api/synchapi/nf-synchapi-sleep) auf, um mindestens eine Sekunde zwischen Sammlungen zu warten.
3.  Rufen Sie [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) erneut auf, um das zweite Beispiel zu erfassen.
4.  Rufen Sie die [**PdhGetFormattedCounterValue-Funktion**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue) auf, um einen anzeigebaren Wert zu berechnen.
5.  Wiederholen Sie die Schritte 2 bis 4.

Als Alternative zum Implementieren einer Wartezeit selbst können Sie die [**PdhCollectQueryDataEx-Funktion**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydataex) aufrufen, die einen Zeitsteuerungsthread erstellt, der eine angegebene Zeitspanne wartet, das Beispiel erfasst und dann ein anwendungsdefiniertes Ereignis auslöst.

Wenn Sie Leistungsdaten aus einer Protokolldatei abfragen möchten, können Sie auch einen Zeitbereich definieren. Der Zeitbereich beschränkt die Abfrage auf die Stichproben, die innerhalb des Zeitbereichs erfasst wurden (jedes Beispiel enthält einen Zeitstempel für den Zeitpunkt der Erfassung). Weitere Informationen zum Festlegen und Abrufen von Zeitbereichen finden Sie unter [Festlegen eines Zeitbereichs für eine Abfrage.](setting-a-time-range-for-a-query.md)

Wenn Sie Leistungsdaten sammeln und in eine Protokolldatei schreiben möchten, rufen Sie die [**PdhUpdateLog-Funktion**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga) auf, anstatt [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)aufzurufen. Weitere Informationen finden Sie unter [Arbeiten mit Protokolldateien](working-with-log-files.md) und [Schreiben von Leistungsdaten in eine Protokolldatei.](writing-performance-data-to-a-log-file.md)

Ausführliche Informationen zum Berechnen eines sichtbaren Beispielwerts finden Sie unter [Anzeigen von Leistungsdaten.](displaying-performance-data.md)

## <a name="understanding-multiple-processor-counters"></a>Grundlegendes zu mehreren Prozessorleistungsindikatoren

Einige Leistungsindikatoren wurden für Einzelprozessorsysteme entwickelt und sind für Multiprozessorcomputer möglicherweise nicht genau. Beispielsweise ist ein Prozess auf 100 Prozent eines einzelnen Prozessors beschränkt. Die Threads können jedoch mehrere Prozessoren verwenden, die insgesamt mehr als 100 Prozent betragen.

Der \\ Leistungsindikatorwert "Prozessor( \_ Gesamt) \\ % Prozessorzeit" ist die durchschnittliche Nutzung aller Prozessoren. Wenn Sie beispielsweise über zwei Prozessoren verfügen, einen bei 100 Prozent und einen anderen mit 0 Prozent, meldet dieser Leistungsindikator 50 Prozent. Der Bereich liegt also zwischen 0 und 100.

Der \\ Leistungsindikatorwert "Process(X) \\ % Process Time" ist die Summe der Prozessorauslastung durch alle Threads von Prozess X. Wenn ein Prozess z. B. auf einem Computer mit zwei Prozessoren über zwei Threads verfügt, wobei einer 75 Prozent einer CPU und der andere 80 Prozent einer anderen CPU beansprucht, meldet dieser Leistungsindikator 155 Prozent. Der Bereich für diesen Leistungsindikator liegt zwischen 0 und 100 \* ProcessorCount.

**Windows Server 2003 und Windows XP: **

Sie können Werte außerhalb des erwarteten Wertebereichs für die CPU-Auslastung empfangen. Um den Prozentsatz der CPU-Auslastung zu berechnen, benötigt PDH zwei Stichproben (jeweils mit einem Rohwert und einem Zeitstempel). Da PDH nur den Instanznamen verwendet, um die Prozesse abzugleichen, kann es manchmal zwei Beispiele aus verschiedenen Prozessen verwenden. Wenn z. B. drei Prozesse entnommen werden und ein Prozess nach dem dritten Beispiel beendet wird, wird ein anderer Prozess in den Slot verschoben, der durch diesen beendeten Prozess frei geworden ist. Daher stellt ein formatierter Indikator einen falschen Wert bereit, wenn Sie das vierte Beispiel formatieren, da es das dritte Beispiel aus dem beendeten Prozess und das vierte Beispiel aus dem Prozess verwendet, der in den Slot des beendeten Prozesses verschoben wurde.

Die folgende Tabelle zeigt, wie dies auftreten kann, wenn ein Prozess beendet wird, während Daten gesammelt werden. Die Tabelle zeigt fünf Indikatorwertbeispiele für drei Instanzen von Prozess X. Die Stichproben werden in Intervallen von einer Sekunde gesammelt. Nachdem das dritte Beispiel erfasst wurde, wird Prozess X in Slot 1 beendet. Wenn Prozess X in Slot 1 beendet wird, wird Prozess X in Slot 2 in Slot 1 verschoben. Wenn Sie das vierte Beispiel für Prozess X in Slot 2 erfassen, ist der erste Wert jetzt 20 anstelle von 1.000, und der zweite Wert ist 1.500. Wenn Sie den Indikatorwert formatieren, erhalten Sie 1.480 Millisekunden anstelle der erwarteten 500 Millisekunden. Wenn Sie den fünften Beispielwert formatieren, sollten Sie den erwarteten Wert erhalten.

| Beispiel   | Slot 0 für Prozess X | Slot 1 für Prozess X           | Slot 2 für Prozess X                     |
|----------|----------------------|--------------------------------|------------------------------------------|
| Beispiel 1 | 0                    | 0                              | 0                                        |
| Beispiel 2 | 20                   | 10                             | 500                                      |
| Beispiel 3 | 40                   | 20                             | 1\.000                                    |
| Beispiel 4 | 60                   | 1.500 (aus dem vorherigen Slot 2) | Nicht zutreffend Jetzt im Slot 1 erfasst. |
| Beispiel 5 | 80                   | 2.000                          | Nicht zutreffend Jetzt im Slot 1 erfasst. |



 

 

 
