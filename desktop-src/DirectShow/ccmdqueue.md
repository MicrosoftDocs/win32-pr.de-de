---
description: Die ccmdqueue-Klasse ist eine Basisklasse, die eine Warteschlange von cdeferredcommand-Objekten und Element Funktionen zum Hinzufügen, entfernen, Überprüfen des Status und zum Aufrufen der Befehle in der Warteschlange bereitstellt.
ms.assetid: 6bd0f0f3-3c56-47d2-9fd8-e2863a2afa33
title: Ccmdqueue-Klasse
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
ms.openlocfilehash: 78af7a975d54ba832bbdf1fb7f8027f87b747660
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123764"
---
# <a name="ccmdqueue-class"></a>Ccmdqueue-Klasse

Die- `CCmdQueue` Klasse ist eine Basisklasse, die eine Warteschlange von [**cdeferredcommand**](cdeferredcommand.md) -Objekten und Element Funktionen zum Hinzufügen, entfernen, Überprüfen des Status und zum Aufrufen der Befehle in der Warteschlange bereitstellt. Ein- `CCmdQueue` Objekt ist ein Teil eines Objekts, das [**iqueuecommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) -Methoden implementiert. Der Filter Graph-Manager implementiert **iqueuecommand** -Methoden, sodass Anwendungen Befehle zum Filter Diagramm in die Warteschlange stellen können. Filter, die die **iqueuecommand** -Schnittstelle implementieren, verwenden diese Klasse direkt. Wenn Sie **cdeferredcommand** -Objekte verwenden möchten, muss Ihre Warteschlange von dieser Klasse abgeleitet werden.

Es gibt zwei Synchronisierungs Modi: grob und genau. Im groben Modus wartet die Anwendung, bis eine angegebene Zeit erreicht ist, und führt dann den Befehl aus. Im exakten Modus wartet die Anwendung, bis die Verarbeitung in dem Beispiel beginnt, das zu diesem Zeitpunkt angezeigt wird, und führt dann den Befehl aus. Der Filter bestimmt, welcher implementiert wird. Der Filter Graph-Manager implementiert immer den groben Modus für Befehle, die im Filter Diagramm-Manager in die Warteschlange eingereiht werden.

Wenn Sie eine grobe Synchronisierung durchführen möchten, sollten Sie warten, bis ein Befehl fällig ist, und dann ausführen. Dazu rufen Sie [**ccmdqueue:: getduecommand**](ccmdqueue-getduecommand.md)auf. Wenn Sie mehrere Dinge abwarten müssen, müssen Sie das Ereignis Handle von [**ccmdqueue:: getduehandle**](ccmdqueue-getduehandle.md) abrufen und dann **ccmdqueue:: getduecommand** aufrufen, wenn dies signalisiert wird. die [**streamzeit**](stream-time.md) wird nur zwischen Aufrufen der Member " [**ccmdqueue:: Run**](ccmdqueue-run.md) " und " [**ccmdqueue:: EndRun**](ccmdqueue-endrun.md) " fortgeführt. Es gibt keine Garantie, dass ein Befehl bereit ist, wenn das Handle festgelegt ist. Jedes Mal, wenn das Ereignis signalisiert wird, wird die **getduecommand** -Member-Funktion aufgerufen (wahrscheinlich mit einem Timeout von null); Dies kann E Abort zurückgeben, \_ Wenn kein Befehl bereit ist.

Wenn Sie eine exakte Synchronisierung wünschen, müssen Sie die Funktion [**ccmdqueue:: getcommandduefor**](ccmdqueue-getcommandduefor.md) Member aufrufen und die zu verarbeitenden Beispiele als Parameter übergeben. Dadurch wird Folgendes zurückgegeben:

-   Ein Stream-Zeit-Befehl, der an oder vor der streamzeit liegt.
-   Ein Präsentationszeit Befehl, der an oder vor der Darstellung der streamzeit liegt. Dies geschieht nur zwischen den [**memmdqueue:: Run**](ccmdqueue-run.md) -und [**ccmdqueue:: EndRun**](ccmdqueue-endrun.md) -Member-Funktionen, da die Zuordnung von der streamzeit zur Präsentationszeit nicht bekannt ist.
-   Ein beliebiger Präsentationszeit-Befehl wird jetzt durchzuführen.

Wenn Sie für Beispiele, die möglicherweise im angehaltenen Modus verarbeitet werden, eine exakte Synchronisierung durchführen möchten, müssen Sie die Befehle zum Streamen von Daten verwenden

In allen Fällen bleiben Befehle in der Warteschlange, bis Sie aufgerufen oder abgebrochen werden. Die Einstellung und das Zurücksetzen des Ereignis Handles werden vollständig von diesem Warteschlangen Objekt verwaltet.



| Geschützte Datenmember                                 | BESCHREIBUNG                                                                                            |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| m- \_ Brunning                                            | Flag zum Ausführen des Zustands; Legen Sie beim Ausführen von **true** fest.                                                     |
| m \_ DW-Empfehlung                                            | Bezeichnerbezeichner von der Referenzuhr (null, wenn keine ausstehende Empfehlung besteht).                            |
| m \_ evdue                                               | Legt die Uhrzeit fest, zu der Befehle fällig werden.                                                               |
| m \_ listpresentation                                    | Speichert Befehle in der Präsentationszeit in der Warteschlange.                                                           |
| m \_ liststream                                          | Speichert Befehle in der streamzeit in der Warteschlange.                                                                 |
| m- \_ Sperre                                                | Schützt den Zugriff auf Listen.                                                                              |
| m \_ pclock                                              | Aktuelle Referenzuhr.                                                                               |
| m \_ streamtimeoffset                                    | Enthält den Zeit Offset des Streams, wenn **m- \_ Brunning** den Wert **true** aufweist.                                      |
| m \_ streamtimeoffset                                    | Enthält den Zeit Offset des Streams, wenn **m- \_ Brunning** den Wert **true** aufweist.                                      |
| Elementfunktionen                                       | BESCHREIBUNG                                                                                            |
| [**Ccmdqueue**](ccmdqueue-ccmdqueue.md)               | Erstellt ein **ccmdqueue** -Objekt.                                                                     |
| [**Prüfzeit**](ccmdqueue-checktime.md)               | Bestimmt, ob eine bestimmte Uhrzeit fällig ist.                                                                     |
| [**Getduehandle**](ccmdqueue-getduehandle.md)         | Ruft das Ereignis Handle ab, das signalisiert wird.                                                      |
| Über schreibbare Member-Funktionen                           | BESCHREIBUNG                                                                                            |
| [**EndRun**](ccmdqueue-endrun.md)                     | Wechselt zum beendeten oder angehaltenen Modus.                                                                    |
| [**Getcommandduefor**](ccmdqueue-getcommandduefor.md) | Ruft einen verzögerten Befehl ab, der zu einem bestimmten Zeitpunkt geplant wird.                                    |
| [**Getduecommand**](ccmdqueue-getduecommand.md)       | Ruft einen Zeiger auf den nächsten Befehl ab, der fällig ist.                                                   |
| [**Setze**](ccmdqueue-insert.md)                     | Fügt der Warteschlange das [**cdeferredcommand**](cdeferredcommand.md) -Objekt hinzu.                             |
| [**Neu**](ccmdqueue-new.md)                           | Initialisiert einen Befehl, der ausgeführt werden soll, und gibt ein neues [**cdeferredcommand**](cdeferredcommand.md) -Objekt zurück. |
| [**Aufgeh**](ccmdqueue-remove.md)                     | Entfernt das [**cdeferredcommand**](cdeferredcommand.md) -Objekt aus der Warteschlange.                        |
| [**Ausführen**](ccmdqueue-run.md)                           | Wechselt in den laufenden Modus.                                                                              |
| [**Setsyncsource**](ccmdqueue-setsyncsource.md)       | Legt die Uhrzeit für die zeitliche Steuerung fest.                                                                        |
| [**Settimerat**](ccmdqueue-settimeadvise.md)       | Richtet ein Timer-Ereignis mit der Referenzuhr ein.                                                        |



 

 

 



