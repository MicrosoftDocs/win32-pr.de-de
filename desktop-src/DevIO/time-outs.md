---
description: Ein Handle für eine Kommunikations Ressource verfügt über einen zugeordneten Satz von Timeout Parametern, die sich auf das Verhalten von Lese-und Schreibvorgängen auswirken.
ms.assetid: 271d4c68-1f6d-4483-a9a1-703220de761f
title: Timeouts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db31fafc0f4d98832f1fb7fa5d22b32cba33d73
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748336"
---
# <a name="time-outs"></a>Timeouts

Ein Handle für eine Kommunikations Ressource verfügt über einen zugeordneten Satz von Timeout Parametern, die sich auf das Verhalten von Lese-und Schreibvorgängen auswirken. Timeouts können dazu führen, dass [**ein Vorgang zum**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) lesen, schreiben [**, schreiben**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)oder schreiben [**von Dateien abgeschlossen**](/windows/desktop/api/fileapi/nf-fileapi-readfile) [**wird, wenn**](/windows/desktop/api/fileapi/nf-fileapi-writefile)ein Timeout Intervall abläuft, auch wenn die angegebene Anzahl von Zeichen nicht gelesen oder geschrieben wurde. Er wird nicht als Fehler behandelt, wenn während eines Lese-oder Schreibvorgangs ein Timeout auftritt (d. h. der Rückgabewert der Lese-oder Schreibfunktion gibt einen Erfolg an). Die Anzahl der tatsächlich gelesenen oder geschriebenen Bytes wird von "read **File** " oder " **Write File** " (bzw. durch die Funktion " [**gedeverlappedresult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) " oder " [**fleiocompletionroutine**](/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine) ") gemeldet, wenn die e/a-Vorgänge als überlappende Operation ausgeführt wurden.

Wenn eine Anwendung eine Kommunikations Ressource öffnet, legt das System die Timeout Werte der Ressource auf die Werte fest, die bei der letzten Verwendung der Ressource wirksam wurden. Wenn die Kommunikations Ressource nie geöffnet wurde, legt das System die Timeout Werte auf einen Standardwert fest. In beiden Fällen sollte eine Anwendung die aktuellen Timeout Werte nach dem Öffnen der Ressource immer ermitteln und diese dann explizit so festlegen, dass Sie Ihren Anforderungen entspricht. Verwenden Sie die [**getcommtimeouts**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts) -Funktion, um die aktuellen Timeout Werte einer Kommunikations Ressource zu bestimmen. Wenn Sie die Timeout Werte ändern möchten, verwenden Sie die Funktion [**SetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts) .

Zwei Arten von Timeouts werden durch die Timeout Parameter aktiviert. Ein Intervall Timeout tritt auf, wenn die Zeit zwischen dem Empfang von zwei Zeichen eine angegebene Anzahl von Millisekunden überschreitet. Die zeitliche Steuerung beginnt, wenn das erste Zeichen empfangen wird, und wird neu gestartet, wenn jedes neue Zeichen empfangen wird. Ein Gesamt Timeout tritt auf, wenn die von einem Lesevorgang verbrauchte Gesamtzeit eine berechnete Anzahl von Millisekunden überschreitet. Die zeitliche Steuerung beginnt sofort, wenn der e/a-Vorgang beginnt. Schreibvorgänge unterstützen nur Timeout Zeiten. Lesevorgänge unterstützen sowohl das Intervall als auch das gesamte Timeout, das separat oder kombiniert verwendet werden kann.

Die Zeit (in Millisekunden) des gesamten Timeout Zeitraums für einen Lese-oder Schreibvorgang wird mithilfe des Multiplikators und konstanter Werte aus der [**COMMTIMEOUTS**](/windows/desktop/api/Winbase/ns-winbase-commtimeouts) -Struktur berechnet, die in der [**getcommtimeouts**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts) -oder [**SetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts) -Funktion angegeben ist. Die folgende Formel wird verwendet:


```C++
Timeout = (MULTIPLIER * number_of_bytes) + CONSTANT
```



Wenn Sie einen Multiplikator und eine Konstante verwenden, kann der gesamte Timeout Zeitraum variieren, abhängig von der angeforderten Datenmenge. Eine Anwendung kann nur die Konstante verwenden, indem der Multiplikator auf NULL festgelegt wird, oder es wird nur der Multiplikator verwendet, indem die Konstante auf NULL festgelegt wird. Wenn Konstante und Multiplikator NULL sind, wird das gesamte Timeout nicht verwendet.

Wenn alle Timeouts für den Lesevorgang NULL sind, werden Lese Timeouts nicht verwendet, und ein Lesevorgang wird erst abgeschlossen, wenn die angeforderte Anzahl von Bytes gelesen wurde oder ein Fehler auftritt. Wenn alle Timeout Parameter für die Schreibweise NULL sind, wird ein Schreibvorgang nicht abgeschlossen, bis die angeforderte Anzahl von Bytes geschrieben oder ein Fehler auftritt.

Wenn der Wert für das Timeout für Lese Intervalle der Wert **MAXDWORD** ist und beide Timeout Parameter für alle lesen den Wert 0 (null) aufweisen, wird unmittelbar nach dem Lesen der Zeichen, die im Eingabepuffer verfügbar sind, ein Lesevorgang abgeschlossen, auch wenn er leer ist.

Die Intervall zeitliche Steuerung erzwingt, dass ein Lesevorgang zurückgegeben wird, wenn eine Pause Auftritt im Empfang vorhanden ist. Ein Prozess, der Intervall Timeouts verwendet, kann einen relativ kurzen Intervall Parameter festlegen, sodass er schnell auf kleine, isolierte Spitzen mit einem oder mehreren Zeichen reagieren kann, aber er kann dennoch große Puffer von Zeichen mit einem einzigen Aufruf erfassen, wenn Daten in einem stabilen Stream empfangen werden.

Timeouts für einen Schreibvorgang können nützlich sein, wenn die Übertragung durch eine Art Fluss Steuerung blockiert wird oder wenn die Funktion " [**setcommbreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak) " aufgerufen wurde, um die Zeichen Übertragung anzuhalten.

In der folgenden Tabelle wird das Verhalten von Lesevorgängen auf der Grundlage der für das Gesamt-und Intervall Timeout angegebenen Werte zusammengefasst.



| Gesamt | Intervall | Verhalten                                                                                                                                                                                 |
|-------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | 0        | Gibt zurück, wenn der Puffer vollständig ausgefüllt ist. Timeouts werden nicht verwendet.                                                                                                                    |
| T     | 0        | Gibt zurück, wenn der Puffer vollständig aufgefüllt ist, oder wenn T Millisekunden seit dem Beginn des Vorgangs verstrichen sind.                                                                   |
| 0     | J        | Gibt zurück, wenn der Puffer vollständig aufgefüllt ist, oder wenn Y Millisekunden zwischen dem Empfang von zwei Zeichen verstrichen sind. Die zeitliche Steuerung beginnt erst, wenn das erste Zeichen empfangen wird. |
| T     | J        | Gibt zurück, wenn der Puffer vollständig aufgefüllt ist, oder wenn eine der beiden Timeout Zeiten auftritt.                                                                                                     |



 

> [!Note]  
> Diese zeitliche Steuerung ist jedoch relativ zum System, das das physische Gerät steuert. Bei einem Remote Gerät (z. b. einem Modem) ist die zeitliche Steuerung relativ zum Server System, an das das Modem angefügt wird. Alle Netzwerk Weiterleitungs Verzögerungen werden in nicht berücksichtigt. Beispielsweise kann eine Client Anwendung ein Gesamt Timeout angeben, das 500 Millisekunden berechnet. Wenn 500 Millisekunden auf dem Server verstrichen sind, wird ein Timeout Fehler an den Client zurückgegeben. Wenn eine Netzwerk propagierungs Verzögerung von 50 Millisekunden vorliegt, wird der Client erst nach ungefähr 50 Millisekunden benachrichtigt, nachdem das Timeout tatsächlich aufgetreten ist.

 

> [!Note]  
> Die Timeout Parameter wirken sich auf das Verhalten von überlappenden Lese-und Schreibvorgängen auf einem Kommunikationsgerät aus. Mit überlappenden e/a-Vorgängen kann die Funktion "read [**File**](/windows/desktop/api/fileapi/nf-fileapi-readfile)", " [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile)", "read [**fileex**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)" oder " [**Write fileex**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) " zurückgeben, bevor der Vorgang abgeschlossen wurde. Durch die Timeout Parameter kann ermittelt werden, wann der Vorgang abgeschlossen wurde.

 

 

 
