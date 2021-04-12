---
description: Nachdem Sie eine Abfrage erstellt und Leistungsindikatoren hinzugefügt haben, rufen Sie die pdhcollectquerydata-Funktion auf, um die aktuellen Rohdaten für alle Zähler in der Abfrage abzurufen.
ms.assetid: 2534d387-a280-4716-9a9d-3e42f40e2f92
title: Sammeln von Leistungsdaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99bd2c0e22553245e87d3844694051c88c57895
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345519"
---
# <a name="collecting-performance-data"></a>Sammeln von Leistungsdaten

Nachdem Sie [eine Abfrage erstellt](creating-a-query.md) und Leistungsindikatoren hinzugefügt haben, rufen Sie die [**pdhcollectquerydata**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) -Funktion auf, um die aktuellen Rohdaten für alle Zähler in der Abfrage abzurufen.

Viele Leistungsindikatoren, wie z. b. Raten Indikatoren, erfordern zwei Daten Beispiele, um einen formatierten Datenwert zu berechnen. PDH verwaltet Daten für das aktuelle Beispiel und das zuvor gesammelte Beispiel. Im folgenden Verfahren wird beschrieben, wie Leistungswerte erfasst werden, die zwei Beispiele zum Berechnen eines anzeigbaren Werts erfordern.

**So erfassen Sie Leistungswerte, die zwei Beispiele zum Berechnen eines anzeigbaren Werts erfordern**

1.  Nennen Sie [**pdhcollectquerydata**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) , um das erste Beispiel zu erfassen.
2.  Ruft die [**Standbyfunktion auf**](/windows/desktop/api/synchapi/nf-synchapi-sleep) , um mindestens eine Sekunde zwischen den Auflistungen zu warten.
3.  Nennen Sie [**pdhcollectquerydata**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) erneut, um das zweite Beispiel zu erfassen.
4.  Rufen Sie die [**pdhgetformattedcountervalue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue) -Funktion auf, um einen anzeigbaren Wert zu berechnen.
5.  Wiederholen Sie die Schritte 2 bis 4.

Als Alternative zur Implementierung einer Wartezeit selbst können Sie die [**pdhcollectquerydataex**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydataex) -Funktion aufrufen, die einen Zeit Steuerungs Thread erstellt, der einen bestimmten Zeitraum wartet, das Beispiel sammelt und dann ein Anwendungs definiertes Ereignis auslöst.

Wenn Sie Leistungsdaten aus einer Protokolldatei Abfragen möchten, können Sie auch einen Zeitbereich definieren. Der Zeitbereich schränkt die Abfrage auf die Stichproben ein, die im Zeitbereich erfasst wurden (jedes Beispiel enthält einen Zeitstempel für den Zeitpunkt der Erfassung). Weitere Informationen zum Festlegen und Abrufen von Zeit Bereichen finden Sie unter [Festlegen eines Zeit Bereichs für eine Abfrage](setting-a-time-range-for-a-query.md).

Wenn Sie Leistungsdaten erfassen und in eine Protokolldatei schreiben möchten, rufen Sie die [**pdhupdatelog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga) -Funktion auf, anstatt [**pdhcollectquerydata**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)aufzurufen. Weitere Informationen finden Sie unter [Arbeiten mit Protokolldateien](working-with-log-files.md) und [Schreiben von Leistungsdaten in eine Protokolldatei](writing-performance-data-to-a-log-file.md).

Ausführliche Informationen zum Berechnen eines anzeigbaren Beispiel Werts finden Sie unter [Anzeigen von Leistungsdaten](displaying-performance-data.md).

## <a name="understanding-multiple-processor-counters"></a>Grundlegendes zu mehreren Prozessor Zählern

Einige Leistungsindikatoren wurden für einzelne Prozessorsysteme entwickelt und sind möglicherweise für Multiprozessorcomputer nicht exakt. Ein Prozess ist beispielsweise auf 100 Prozent eines einzelnen Prozessors beschränkt. Allerdings können die Threads mehrere Prozessoren verwenden, die insgesamt mehr als 100 Prozent betragen.

Der \\ Leistungswert "Prozessor ( \_ gesamt) \\ % Prozessorzeit" ist die durchschnittliche Auslastung aller Prozessoren. Wenn Sie z. b. über zwei Prozessoren verfügen, eine mit 100 Prozent und eine andere mit 0 Prozent, meldet dieser Wert 50 Prozent. Der Bereich liegt also zwischen 0 und 100.

Der \\ Wert "Process (X) \\ % Prozesszeit" ist die Summe der Prozessorauslastung durch alle Threads von Prozess X. Wenn ein Prozess z. b. auf einem Computer mit zwei Prozessoren über zwei Threads verfügt, wobei eine CPU 75 Prozent der CPU und die andere 80 Prozent einer anderen CPU beansprucht, meldet dieser Wert 155 Prozent. Der Bereich für diesen Zähler liegt zwischen 0 und 100 \* ProcessorCount.

* * Windows Server 2003 und Windows XP: * *

Sie können Werte außerhalb des erwarteten Wertebereichs für die CPU-Auslastung erhalten. Um den Prozentsatz der CPU-Auslastung zu berechnen, benötigt PDH zwei Stichproben (jeweils mit einem Rohwert und einem Zeitstempel). Da PDH nur den Instanznamen verwendet, um die Prozesse abzugleichen, kann manchmal zwei Beispiele aus unterschiedlichen Prozessen verwendet werden. Wenn z. b. drei Prozesse erfasst werden und ein Prozess nach dem dritten Beispiel beendet wird, wird ein anderer Prozess in den von diesem beendeten Prozess frei werdenden Slot verschoben. Folglich gibt ein formatierter Leistungs Bewert einen falschen Wert an, wenn Sie das vierte Beispiel formatieren, da er das dritte Beispiel aus dem beendeten Prozess und das vierte Beispiel aus dem Prozess verwendet, der in den Slot des beendeten Prozesses verschoben wurde.

In der folgenden Tabelle wird gezeigt, wie dies auftreten kann, wenn ein Prozess beendet wird, während Daten gesammelt werden. In der Tabelle werden fünf Beispiele für Leistungs Proben für drei Instanzen von Prozess X angezeigt. Die Beispiele werden in Intervallen von einer Sekunde gesammelt. Nachdem das dritte Beispiel erfasst wurde, wird Process X in Slot 1 beendet. Wenn Process x in Slot 1 beendet wird, wechselt Process x in Slot 2 in Slot 1. Wenn Sie das vierte Beispiel für Process X in Slot 2 erfassen, ist der erste Wert jetzt 20 anstelle von 1.000, und der zweite Wert ist 1.500. Wenn Sie den Wert des Zählers formatieren, erhalten Sie 1.480 Millisekunden anstelle der erwarteten 500 Millisekunden. Wenn Sie den fünften Beispiel Wert formatieren, sollten Sie den erwarteten Wert erhalten.

| Beispiel   | Slot 0 für Prozess X | Slot 1 für Prozess X           | Slot 2 für Prozess X                     |
|----------|----------------------|--------------------------------|------------------------------------------|
| Beispiel 1 | 0                    | 0                              | 0                                        |
| Beispiel 2 | 20                   | 10                             | 500                                      |
| Beispiel 3 | 40                   | 20                             | 1\.000                                    |
| Beispiel 4 | 60                   | 1.500 (aus dem ersten Slot 2) | Nicht zutreffend Nun in Slot 1 erfasst. |
| Beispiel 5 | 80                   | 2\.000                          | Nicht zutreffend Nun in Slot 1 erfasst. |



 

 

 
