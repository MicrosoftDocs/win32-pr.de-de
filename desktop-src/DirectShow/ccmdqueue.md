---
description: Die CCmdQueue-Klasse ist eine Basisklasse, die eine Warteschlange von CDeferredCommand-Objekten und Memberfunktionen zum Hinzufügen, Entfernen, Überprüfen des Status und Aufrufen der Befehle in der Warteschlange bietet.
ms.assetid: 6bd0f0f3-3c56-47d2-9fd8-e2863a2afa33
title: CCmdQueue-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5aac6f7315df58a39d119c72fc481816bdc40aab3c449852041b7a490f22f44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074404"
---
# <a name="ccmdqueue-class"></a>CCmdQueue-Klasse

Die -Klasse ist eine Basisklasse, die eine Warteschlange von `CCmdQueue` [**CDeferredCommand-Objekten**](cdeferredcommand.md) und Memberfunktionen zum Hinzufügen, Entfernen, Überprüfen des Status und Aufrufen der Befehle in der Warteschlange bietet. Ein `CCmdQueue` -Objekt ist Ein Teil eines -Objekts, das [**IQueueCommand-Methoden**](/windows/desktop/api/Control/nn-control-iqueuecommand) implementiert. Der Filterdiagramm-Manager implementiert **IQueueCommand-Methoden,** damit Anwendungen Befehle in die Warteschlange des Filterdiagramms einreiht können. Filter, die die **IQueueCommand-Schnittstelle** implementieren, verwenden diese Klasse direkt. Wenn Sie **CDeferredCommand-Objekte** verwenden möchten, muss Ihre Warteschlange von dieser Klasse abgeleitet werden.

Es gibt zwei Modi der Synchronisierung: "grob" und "genau". Im nicht einfachen Modus wartet die Anwendung, bis eine angegebene Zeit eintrifft, und führt dann den Befehl aus. Im genauen Modus wartet die Anwendung, bis die Verarbeitung des zu diesem Zeitpunkt angezeigten Beispiels beginnt, und führt dann den Befehl aus. Der Filter bestimmt, welcher implementiert wird. Der Filterdiagramm-Manager implementiert immer den unformatierten Modus für Befehle, die im Filterdiagramm-Manager in die Warteschlange gestellt werden.

Wenn Sie eine grobe Synchronisierung wünschen, möchten Sie wahrscheinlich warten, bis ein Befehl fällig ist, und ihn dann ausführen. Rufen Sie hierzu [**CCmdQueue::GetDueCommand auf.**](ccmdqueue-getduecommand.md) Wenn Sie mehrere Dinge warten müssen, rufen Sie das Ereignishandle von [**CCmdQueue::GetDueHandle**](ccmdqueue-getduehandle.md) ab, und rufen Sie **dann CCmdQueue::GetDueCommand** auf, wenn dies signalisiert wird. [**Die Streamzeit**](stream-time.md) wird nur zwischen Aufrufen der [**Memberfunktionen CCmdQueue::Run**](ccmdqueue-run.md) und [**CCmdQueue::EndRun**](ccmdqueue-endrun.md) überschreitungen. Es gibt keine Garantie dafür, dass ein Befehl bereit ist, wenn das Handle festgelegt ist. Rufen Sie bei jeder Signalisierung des Ereignisses die **GetDueCommand-Memberfunktion** auf (wahrscheinlich mit einem Time out von 0). Dies kann E \_ ABORT zurückgeben, wenn kein Befehl bereit ist.

Wenn Sie eine genaue Synchronisierung wünschen, rufen Sie die [**Memberfunktion CCmdQueue::GetCommandDueFor**](ccmdqueue-getcommandduefor.md) auf, und übergeben Sie die Zu verarbeitenden Beispiele als Parameter. Dadurch wird Folgendes zurückgegeben:

-   Ein Streamzeitbefehl, der bei oder vor dieser Streamzeit fällig ist.
-   Ein Präsentationszeitbefehl, der bei oder vor der Präsentation der Streamzeit fällig ist. Führen Sie dies nur zwischen den [**Memberfunktionen CCmdQueue::Run**](ccmdqueue-run.md) und [**CCmdQueue::EndRun**](ccmdqueue-endrun.md) durch, da die Zuordnung von der Streamzeit zur Präsentationszeit nicht bekannt ist.
-   Alle derzeit fälligen Präsentationszeitbefehle.

Wenn Sie eine genaue Synchronisierung für Beispiele wünschen, die möglicherweise im angehaltenen Modus verarbeitet werden, müssen Sie Streamzeitbefehle verwenden.

In allen Fällen bleiben Befehle in der Warteschlange, bis sie aufgerufen oder abgebrochen werden. Das Festlegen und Zurücksetzen des Ereignishandpunkts wird vollständig von diesem Warteschlangenobjekt verwaltet.



| Geschützte Datenmember                                 | Beschreibung                                                                                            |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| m \_ bRunning                                            | Flag für den Ausführungszustand; Legen Sie **true** fest, wenn Sie ausführen.                                                     |
| m \_ dwAdvise                                            | Geben Sie einen Bezeichner aus der Referenzuhr an (null, wenn keine ausstehenden Hinweise verfügbar sind).                            |
| m \_ evDue                                               | Legt die Uhrzeit fest, zu der Befehle fällig sind.                                                               |
| m \_ listPresentation                                    | Speichert Befehle in der Warteschlange zur Präsentationszeit.                                                           |
| m \_ listStream                                          | Speichert Befehle in der Streamzeit in der Warteschlange.                                                                 |
| \_m-Sperre                                                | Schützt den Zugriff auf Listen.                                                                              |
| m \_ pClock                                              | Aktuelle Referenzuhr.                                                                               |
| m \_ StreamTimeOffset                                    | Enthält den Streamzeitoffset, wenn **m \_ bRunning** true **ist.**                                      |
| m \_ StreamTimeOffset                                    | Enthält den Streamzeitoffset, wenn **m \_ bRunning** true **ist.**                                      |
| Elementfunktionen                                       | Beschreibung                                                                                            |
| [**CCmdQueue**](ccmdqueue-ccmdqueue.md)               | Erstellt ein **CCmdQueue-Objekt.**                                                                     |
| [**CheckTime**](ccmdqueue-checktime.md)               | Bestimmt, ob eine bestimmte Zeit fällig ist.                                                                     |
| [**GetDueHandle**](ccmdqueue-getduehandle.md)         | Ruft das Ereignishand handle ab, das signalisiert wird.                                                      |
| Überschreibbare Memberfunktionen                           | Beschreibung                                                                                            |
| [**EndRun**](ccmdqueue-endrun.md)                     | Wechselt in den beendeten oder angehaltenen Modus.                                                                    |
| [**GetCommandDueFor**](ccmdqueue-getcommandduefor.md) | Ruft einen verzögerten Befehl ab, der zu einem bestimmten Zeitpunkt geplant ist.                                    |
| [**GetDueCommand**](ccmdqueue-getduecommand.md)       | Ruft einen Zeiger auf den nächsten Befehl ab, der fällig ist.                                                   |
| [**Einfügen**](ccmdqueue-insert.md)                     | Fügt der [**Warteschlange das CDeferredCommand-Objekt**](cdeferredcommand.md) hinzu.                             |
| [**Neu**](ccmdqueue-new.md)                           | Initialisiert einen auszuführenden Befehl und gibt ein neues [**CDeferredCommand-Objekt**](cdeferredcommand.md) zurück. |
| [**Entfernen**](ccmdqueue-remove.md)                     | Entfernt das [**CDeferredCommand-Objekt**](cdeferredcommand.md) aus der Warteschlange.                        |
| [**Ausführung**](ccmdqueue-run.md)                           | Wechselt in den Ausführungsmodus.                                                                              |
| [**SetSyncSource**](ccmdqueue-setsyncsource.md)       | Legt die Uhr fest, die für die Zeitlichsteuerung verwendet wird.                                                                        |
| [**SetTimeAdvise**](ccmdqueue-settimeadvise.md)       | Richtet ein Timerereignis mit der Referenzuhr ein.                                                        |



 

 

 



