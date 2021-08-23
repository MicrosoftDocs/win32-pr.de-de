---
description: Ein Handle für eine Kommunikationsressource verfügt über einen zugeordneten Satz von Time out-Parametern, die sich auf das Verhalten von Lese- und Schreibvorgängen auswirken.
ms.assetid: 271d4c68-1f6d-4483-a9a1-703220de761f
title: Timeouts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6226e8a2d13020bd4dc90a416e7ef359fbd919cf54e886c5e691e5fca2cdea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956789"
---
# <a name="time-outs"></a>Timeouts

Ein Handle für eine Kommunikationsressource verfügt über einen zugeordneten Satz von Time out-Parametern, die sich auf das Verhalten von Lese- und Schreibvorgängen auswirken. Time outs können dazu führen, dass ein [**ReadFile-,**](/windows/desktop/api/fileapi/nf-fileapi-readfile) [**ReadFileEx-,**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) [**WriteFile-**](/windows/desktop/api/fileapi/nf-fileapi-writefile)oder [**WriteFileEx-Vorgang**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) beendet wird, wenn ein Time out-Intervall abgeht, obwohl die angegebene Anzahl von Zeichen nicht gelesen oder geschrieben wurde. Sie wird nicht als Fehler behandelt, wenn während eines Lese- oder Schreibvorganges ein Time out auftritt (d. h., der Rückgabewert der Lese- oder Schreibfunktion gibt einen Erfolg an). Die Anzahl der tatsächlich gelesenen oder geschriebenen Bytes wird von **ReadFile** oder **WriteFile** gemeldet (oder von der [**GetOverlappedResult-**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) oder [**FileIOCompletionRoutine-Funktion,**](/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine) wenn die E/A als überlappende Operation ausgeführt wurde).

Wenn eine Anwendung eine Kommunikationsressource öffnet, legt das System die Time out-Werte der Ressource auf die Werte fest, die bei der letzten Verwendung der Ressource wirksam waren. Wenn die Kommunikationsressource noch nie geöffnet wurde, legt das System die Time out-Werte auf einen Standardwert fest. In beiden Fällen sollte eine Anwendung immer die aktuellen Time out-Werte nach dem Öffnen der Ressource bestimmen und diese dann explizit so festlegen, dass sie ihren Anforderungen entsprechen. Verwenden Sie die [**GetCommTimeouts-Funktion,**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts) um die aktuellen Timeoutwerte einer Kommunikationsressource zu bestimmen. Verwenden Sie die Funktion [**SetCommTimeouts,**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts) um die Timeoutwerte zu ändern.

Zwei Arten von Time outs werden durch die Time out-Parameter aktiviert. Ein Intervall-Time out tritt auf, wenn die Zeit zwischen dem Empfang von zwei Zeichen eine angegebene Anzahl von Millisekunden überschreitet. Die Zeitsteuerung beginnt, wenn das erste Zeichen empfangen wird, und wird neu gestartet, wenn jedes neue Zeichen empfangen wird. Ein Gesamtzeitüberschreitungsvorgang tritt auf, wenn die Gesamtzeit, die von einem Lesevorgang verbraucht wird, eine berechnete Anzahl von Millisekunden überschreitet. Die Zeitsteuerung beginnt sofort, wenn der E/A-Vorgang beginnt. Schreibvorgänge unterstützen nur die Gesamtanzahl von Time outs. Lesevorgänge unterstützen sowohl Intervall- als auch Gesamtzeitabstände, die separat oder kombiniert verwendet werden können.

Die Zeit des gesamten Timeoutzeitraums für einen Lese- oder Schreibvorgang in Millisekunden wird mithilfe des Multiplikators und konstanter Werte aus der [**COMMTIMEOUTS-Struktur**](/windows/desktop/api/Winbase/ns-winbase-commtimeouts) berechnet, die in der [**GetCommTimeouts-**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts) oder [**SetCommTimeouts-Funktion**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts) angegeben ist. Die folgende Formel wird verwendet:


```C++
Timeout = (MULTIPLIER * number_of_bytes) + CONSTANT
```



Wenn Sie sowohl einen Multiplikator als auch eine Konstante verwenden, kann der gesamte Time out-Zeitraum je nach angeforderter Datenmenge variieren. Eine Anwendung kann nur die Konstante verwenden, indem sie den Multiplikator auf 0 (null) oder nur den Multiplikator verwendet, indem die Konstante auf 0 (null) gesetzt wird. Wenn sowohl die Konstante als auch der Multiplikator 0 (null) sind, wird kein Time out verwendet.

Wenn alle Parameter für das Lese-Time out 0 (null) sind, werden keine Lese-Time outs verwendet, und ein Lesevorgang wird erst abgeschlossen, wenn die angeforderte Anzahl von Bytes gelesen wurde oder ein Fehler auftritt. Wenn alle Time out-Parameter für Schreibzugriff 0 (null) sind, wird ein Schreibvorgang ebenso erst abgeschlossen, wenn die angeforderte Anzahl von Bytes geschrieben wurde oder ein Fehler auftritt.

Wenn der Time out-Parameter für das Leseintervall der **MAXDWORD-Wert** ist und beide Parameter für das Lesegefängnungsintervall null sind, wird ein Lesevorgang unmittelbar nach dem Lesen der im Eingabepuffer verfügbaren Zeichen abgeschlossen, auch wenn er leer ist.

Die Zeitsteuerung des Intervalls erzwingt, dass ein Lesevorgang bei einer Pause beim Empfang zurückkommen muss. Ein Prozess, der Intervall-Time outs verwendet, kann einen relativ kurzen Interval-Parameter festlegen, sodass er schnell auf kleine, isolierte Bursts von einem oder einigen Zeichen reagieren kann, aber dennoch große Puffer von Zeichen mit einem einzigen Aufruf erfassen kann, wenn Daten in einem stabilen Datenstrom empfangen werden.

Time outs für einen Schreibvorgang können nützlich sein, wenn die Übertragung durch eine Art von Flusssteuerung blockiert wird oder wenn die [**SetCommBreak-Funktion**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak) aufgerufen wurde, um die Zeichenübertragung zu blockieren.

In der folgenden Tabelle wird das Verhalten von Lesevorgängen basierend auf den Werten zusammengefasst, die für das Gesamt- und Intervall-Time out angegeben wurden.



| Gesamt | Intervall | Verhalten                                                                                                                                                                                 |
|-------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | 0        | Gibt zurück, wenn der Puffer vollständig gefüllt ist. Time outs werden nicht verwendet.                                                                                                                    |
| T     | 0        | Gibt zurück, wenn der Puffer vollständig gefüllt ist oder T Millisekunden seit beginn des Vorgangs verstrichen sind.                                                                   |
| 0     | J        | Gibt zurück, wenn der Puffer vollständig gefüllt ist oder wenn Y Millisekunden zwischen dem Empfang von zwei Zeichen verstrichen sind. Die Zeitsteuerung beginnt erst, wenn das erste Zeichen empfangen wird. |
| T     | J        | Gibt zurück, wenn der Puffer vollständig gefüllt ist oder wenn ein Time out auftritt.                                                                                                     |



 

> [!Note]  
> Diese Zeitliche Steuerung ist jedoch relativ zum System, das das physische Gerät steuert. Bei einem Remotegerät wie einem Modem ist die Zeitliche Steuerung relativ zum Serversystem, an das das Modem angeschlossen ist. Verzögerungen bei der Netzwerkweitergabe werden nicht mit einverhindert. Eine Clientanwendung kann z. B. ein Gesamteins time out angeben, das auf 500 Millisekunden berechnet wird. Wenn 500 Millisekunden auf dem Server verstrichen sind, wird ein Time out-Fehler an den Client zurückgegeben. Wenn eine Netzwerkweitergabeverzögerung von 50 Millisekunden vorliegt, wird der Client erst nach ungefähr 50 Millisekunden nach dem tatsächlichen Time out über das Time out benachrichtigt.

 

> [!Note]  
> Die Time out-Parameter beeinflussen das Verhalten von überlappenden Lese- und Schreibvorgängen auf einem Kommunikationsgerät. Bei überlappenden E/A-Daten kann die [**ReadFile-,**](/windows/desktop/api/fileapi/nf-fileapi-readfile) [**WriteFile-,**](/windows/desktop/api/fileapi/nf-fileapi-writefile) [**ReadFileEx-**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)oder [**WriteFileEx-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) zurückgeben, bevor der Vorgang abgeschlossen wurde. Die Time out-Parameter können bestimmen, wann der Vorgang abgeschlossen wurde.

 

 

 
