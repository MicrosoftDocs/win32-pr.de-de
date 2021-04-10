---
description: Ein Prozess kann eine Reihe von Ereignissen überwachen, die in einer Kommunikations Ressource auftreten. Eine Anwendung kann z. b. die Ereignisüberwachung verwenden, um zu bestimmen, wann die CTS (Clear-to-Send) und DSR (Data-Set-Ready) den Status ändern.
ms.assetid: 5d2a7bf3-a972-474b-b8ca-da3351f1e59c
title: Kommunikations Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 466bd5076405427c7c348c1df3706cb7b5c3edc4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126805"
---
# <a name="communications-events"></a>Kommunikations Ereignisse

Ein Prozess kann eine Reihe von Ereignissen überwachen, die in einer Kommunikations Ressource auftreten. Eine Anwendung kann z. b. die Ereignisüberwachung verwenden, um zu bestimmen, wann die CTS (Clear-to-Send) und DSR (Data-Set-Ready) den Status ändern.

Ein Prozess kann Ereignisse für eine bestimmte Kommunikations Ressource überwachen, indem die [**setcommmask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) -Funktion verwendet wird, um eine Ereignis Maske zu erstellen. Zum Ermitteln der aktuellen Ereignis Maske für eine Kommunikations Ressource kann ein Prozess die [**getcommmask**](/windows/desktop/api/Winbase/nf-winbase-getcommmask) -Funktion verwenden. Die folgenden Werte geben Ereignisse an, die überwacht werden können.



| Wert           | Bedeutung                                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EV- \_ Pause**   | Bei der Eingabe wurde ein "break" erkannt.                                                                                                                                                                                                                    |
| **EV \_ CTS**     | Der Status des CTS-Signals (Clear-to-Send) wurde geändert.                                                                                                                                                                                                     |
| **EV- \_ DSR**     | Der Status des DSR-Signals (Data-Set-Ready) wurde geändert.                                                                                                                                                                                                    |
| **EV \_ Err**     | Zeilen Status Fehler. Zeilen Status Fehler sind **CE- \_ Frame**, **CE- \_ Überlauf** und **CE- \_ rxparität**.                                                                                                                                        |
| **EV- \_ Ring**    | Ein Ringindikator wurde erkannt.                                                                                                                                                                                                                    |
| **EV \_ RLSD**    | Der Status der RLSD (Receive-Line-Signal-Detect) hat sich geändert.                                                                                                                                                                                       |
| **EV \_ rxchar**  | Ein Zeichen wurde empfangen und im Eingabepuffer platziert.                                                                                                                                                                                          |
| **EV- \_ rxflag**  | Das Ereignis Zeichen wurde empfangen und im Eingabepuffer platziert. Das Ereignis Zeichen wird in der [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) -Struktur des Geräts angegeben, die mithilfe der [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) -Funktion auf einen seriellen Anschluss angewendet wird. |
| **EV \_ txempty** | Das letzte Zeichen im Ausgabepuffer wurde gesendet.                                                                                                                                                                                                 |



 

Nachdem eine Reihe von Ereignissen angegeben wurde, wird von einem Prozess die [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) -Funktion verwendet, um zu warten, bis eines der Ereignisse auftritt. **WaitCommEvent** kann synchron oder als überlappende Operation verwendet werden. Weitere Informationen zum Ausführen einer Funktion als überlappenden Vorgang finden Sie unter [Synchronisierung](/windows/desktop/Sync/synchronization).

Wenn eines der in der Ereignis Maske angegebenen Ereignisse auftritt, schließt der Prozess den warte Vorgang ab und legt eine Ereignis Masken Variable fest, um den Typ des erkannten Ereignisses anzugeben. Wenn [**setcommmask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) für eine Kommunikations Ressource aufgerufen wird, während ein warte Vorgang für diese Ressource aussteht, gibt [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) einen Fehler zurück.

Die [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) -Funktion erkennt Ereignisse, die seit dem letzten Aufrufen von [**setcommmask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) oder **WaitCommEvent** aufgetreten sind. Wenn Sie z. b. das **EV- \_ rxchar** -Ereignis als Ereignis für die Wartezeit-Ereignis Angabe angeben, wird ein Rückruf von **WaitCommEvent** erfüllt, wenn im Eingabepuffer des Treibers Zeichen vorhanden sind, die seit dem letzten Aufrufen von **WaitCommEvent** oder **setcommmask** eingetroffen sind. Daher wird bei Verwendung des folgenden Pseudo Codes für alle Zeichen, die zwischen T1 und T2 empfangen werden, der nächste Rückruf von **WaitCommEvent** erfüllt.


```C++
while (!bFinished) 
{ 
    WaitCommEvent(args)
 
T1: // Read bytes 
    // Process bytes 

T2: 
}
```



Beim Überwachen eines Ereignisses, das auftritt, wenn ein Signal (CTS, DSR usw.) den Status ändert, meldet [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) die Änderung, jedoch nicht den aktuellen Status. Um den aktuellen Status der CTS (Clear-to-Send), DSR (Data-Set-Ready), RLSD (Receive-Line-Signal-Detect) und Ring Indikator Signale abzufragen, kann ein Prozess die [**getcommwdemstatus**](/windows/desktop/api/Winbase/nf-winbase-getcommmodemstatus) -Funktion verwenden.

 

 
