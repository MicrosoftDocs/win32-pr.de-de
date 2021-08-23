---
description: Ein Prozess kann eine Reihe von Ereignissen überwachen, die in einer Kommunikationsressource auftreten. Beispielsweise kann eine Anwendung die Ereignisüberwachung verwenden, um zu bestimmen, wann die CTS-Signale (Clear-to-Send) und DSR -Signale (data-set-ready) den Zustand ändern.
ms.assetid: 5d2a7bf3-a972-474b-b8ca-da3351f1e59c
title: Kommunikationsereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bcb257652723a2464ff66c862f574f6aeae621bc6459b55d250f785d0b0895
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815490"
---
# <a name="communications-events"></a>Kommunikationsereignisse

Ein Prozess kann eine Reihe von Ereignissen überwachen, die in einer Kommunikationsressource auftreten. Beispielsweise kann eine Anwendung die Ereignisüberwachung verwenden, um zu bestimmen, wann die CTS-Signale (Clear-to-Send) und DSR -Signale (data-set-ready) den Zustand ändern.

Ein Prozess kann Ereignisse für eine bestimmte Kommunikationsressource überwachen, indem er die [**Funktion SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) verwendet, um eine Ereignismaske zu erstellen. Um die aktuelle Ereignismaske für eine Kommunikationsressource zu bestimmen, kann ein Prozess die [**GetCommMask-Funktion**](/windows/desktop/api/Winbase/nf-winbase-getcommmask) verwenden. Die folgenden Werte geben Ereignisse an, die überwacht werden können.



| Wert           | Bedeutung                                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EV \_ BREAK**   | Bei der Eingabe wurde ein "break" erkannt.                                                                                                                                                                                                                    |
| **EV \_ CTS**     | Der Zustand des CTS-Signals (Clear-to-Send) wurde geändert.                                                                                                                                                                                                     |
| **EV \_ DSR**     | Das DSR-Signal (data-set-ready) hat den Zustand geändert.                                                                                                                                                                                                    |
| **EV \_ ERR**     | Ein Zeilenstatusfehler ist aufgetreten. Fehler beim Zeilenstatus sind **CE \_ FRAME,** **CE \_ OVERRUN** und **CE \_ RXPARITY.**                                                                                                                                        |
| **EV \_ RING**    | Ein Ringindikator wurde erkannt.                                                                                                                                                                                                                    |
| **EV \_ RLSD**    | Der Status des RLSD-Signals (Receive-Line Signal Detect) wurde geändert.                                                                                                                                                                                       |
| **EV \_ RXCHAR**  | Ein Zeichen wurde empfangen und im Eingabepuffer platziert.                                                                                                                                                                                          |
| **EV \_ RXFLAG**  | Das Ereigniszeichen wurde empfangen und im Eingabepuffer platziert. Das Ereigniszeichen wird in der [**DCB-Struktur**](/windows/desktop/api/Winbase/ns-winbase-dcb) des Geräts angegeben, das mithilfe der [**SetCommState-Funktion**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) auf einen seriellen Anschluss angewendet wird. |
| **EV \_ TXEMPTY** | Das letzte Zeichen im Ausgabepuffer wurde gesendet.                                                                                                                                                                                                 |



 

Nachdem eine Gruppe von Ereignissen angegeben wurde, verwendet ein Prozess die [**WaitCommEvent-Funktion,**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) um auf das Auftreten eines der Ereignisse zu warten. **WaitCommEvent** kann synchron oder als überlappende Operation verwendet werden. Weitere Informationen zum Ausführen einer Funktion als überlappende Operation finden Sie unter [Synchronization](/windows/desktop/Sync/synchronization).

Wenn eines der in der Ereignismaske angegebenen Ereignisse auftritt, schließt der Prozess den Wartevorgang ab und legt eine Ereignismaskenvariable fest, um den Typ des erkannten Ereignisses anzugeben. Wenn [**SetCommMask für**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) eine Kommunikationsressource aufgerufen wird, während eine Wartezeit für diese Ressource aussteht, gibt [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) einen Fehler zurück.

Die [**WaitCommEvent-Funktion**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) erkennt Ereignisse, die seit dem letzten Aufruf von [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) oder **WaitCommEvent aufgetreten sind.** Wenn Sie z. B. das **EV \_ RXCHAR-Ereignis** als Wartebesprechungsereignis angeben, wird ein Aufruf von **WaitCommEvent** erfüllt, wenn im Eingabepuffer des Treibers Zeichen enthalten sind, die seit dem letzten Aufruf von **WaitCommEvent** oder **SetCommMask eingetroffen sind.** Daher erfüllen alle zwischen T1 und T2 empfangenen Zeichen mit dem folgenden Pseudocode den nächsten Aufruf von **WaitCommEvent.**


```C++
while (!bFinished) 
{ 
    WaitCommEvent(args)
 
T1: // Read bytes 
    // Process bytes 

T2: 
}
```



Bei der Überwachung eines Ereignisses, das auftritt, wenn ein Signal (CTS, DSR, so weiter) den Zustand ändert, meldet [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) die Änderung, aber nicht den aktuellen Zustand. Zum Abfragen des aktuellen Zustands der Signale CTS (clear-to-send), DSR (data-set-ready), RLSD (receive-line-signal-detect) und Ringindikator kann ein Prozess die [**GetCommModemStatus-Funktion**](/windows/desktop/api/Winbase/nf-winbase-getcommmodemstatus) verwenden.

 

 
