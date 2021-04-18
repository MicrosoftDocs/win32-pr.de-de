---
description: Komponenten sind häufig so konzipiert, dass Sie Initialisierungs Aufgaben ausführen, wenn Sie zum ersten Mal aufgerufen werden, anstatt Sie zu laden.
ms.assetid: 404c083c-7bee-44c2-b8e7-da1901b6ab2f
title: One-Time Initialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16f451e3c51716b4ff6f33b55d8d8602b5d5c28f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352566"
---
# <a name="one-time-initialization"></a>One-Time Initialisierung

Komponenten sind häufig so konzipiert, dass Sie Initialisierungs Aufgaben ausführen, wenn Sie zum ersten Mal aufgerufen werden, anstatt Sie zu laden. Die einmaligen Initialisierungs Funktionen stellen sicher, dass diese Initialisierung nur einmal erfolgt, auch wenn mehrere Threads die Initialisierung möglicherweise versuchen.

**Windows Server 2003 und Windows XP:** Anwendungen müssen eine eigene Synchronisierung für die einmalige Initialisierung mithilfe der [Interlocked-Funktionen](interlocked-variable-access.md) oder anderer Synchronisierungs Mechanismen bereitstellen. Die einmaligen Initialisierungs Funktionen sind ab Windows Vista und Windows Server 2008 verfügbar.

Die einmaligen Initialisierungs Funktionen bieten bedeutende Vorteile, um sicherzustellen, dass nur ein Thread die Initialisierung ausführt:

-   Sie sind für die Geschwindigkeit optimiert.
-   Sie erstellen die entsprechenden Barrieren für Prozessorarchitekturen, die Sie benötigen.
-   Sie unterstützen die gesperrte und parallele Initialisierung.
-   Sie vermeiden interne sperren, sodass der Code asynchron oder synchron ausgeführt werden kann.

Das System verwaltet den Initialisierungs Prozess über eine nicht transparente **Init \_ Once** -Struktur, die Daten und Zustandsinformationen enthält. Der Aufrufer ordnet diese Struktur zu und initialisiert Sie, indem entweder [**InitOnceInitialize**](/windows/win32/api/synchapi/nf-synchapi-initonceinitialize) aufgerufen wird (um die Struktur dynamisch zu initialisieren) oder die Konstante **Init \_ Once \_ static \_ Init** der Struktur Variablen zuzuweisen (um die Struktur statisch zu initialisieren). Anfänglich sind die in der einmaligen Initialisierungs Struktur gespeicherten Daten NULL, und Ihr Status ist nicht initialisiert.

Einmalige Initialisierungs Strukturen können nicht Prozess übergreifend gemeinsam verwendet werden.

Der Thread, der die Initialisierung ausführt, kann optional einen Kontext festlegen, der für den Aufrufer verfügbar ist, nachdem die Initialisierung beendet wurde. Der Kontext kann ein Synchronisierungs Objekt sein, oder es kann ein Wert oder eine Datenstruktur sein. Wenn der Kontext ein Wert ist, muss die von der **\_ nach Ordnung \_ \_ reservierten \_ Bits** mit niedriger Reihenfolge nach dem Wert 0 (null) sein. Wenn der Kontext eine Datenstruktur ist, muss die Datenstruktur **DWORD**-ausgerichtet sein. Der Kontext wird im *lpContext* -Ausgabeparameter der [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) -oder [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) -Funktion an den Aufrufer zurückgegeben.

Die einmalige Initialisierung kann synchron oder asynchron ausgeführt werden. Eine optionale Rückruffunktion kann für die synchrone einmalige Initialisierung verwendet werden.

## <a name="synchronous-one-time-initialization"></a>Synchrone einmalige Initialisierung

In den folgenden Schritten wird die synchrone einmalige Initialisierung beschrieben, bei der keine Rückruffunktion verwendet wird.

1.  Der erste Thread, der die [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) -Funktion aufruft, bewirkt, dass die einmalige Initialisierung beginnt. Für die synchrone einmalige Initialisierung muss **InitOnceBeginInitialize** ohne das " **Init \_ Once \_ Async** "-Flag aufgerufen werden.
2.  Nachfolgende Threads, die versuchen, eine Initialisierung durchführen, werden blockiert, bis der erste Thread entweder die Initialisierung abschließt oder Wenn der erste Thread ausfällt, kann der nächste Thread versuchen, die Initialisierung durchführen, usw.
3.  Wenn die Initialisierung abgeschlossen ist, ruft der Thread die [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) -Funktion auf. Der Thread kann optional ein Synchronisierungs Objekt (oder andere Kontext Daten) erstellen und im *lpContext* -Parameter der **InitOnceComplete** -Funktion angeben.
4.  Wenn die Initialisierung erfolgreich ist, wird der Zustand der einmaligen Initialisierungs Struktur in initialisiert geändert, und das *lpContext* -handle (sofern vorhanden) wird in der Initialisierungs Struktur gespeichert. Bei nachfolgenden Initialisierungs versuchen werden diese Kontext Daten zurückgegeben. Wenn die Initialisierung fehlschlägt, sind die Daten **null**.

In den folgenden Schritten wird die synchrone einmalige Initialisierung beschrieben, die eine Rückruffunktion verwendet.

1.  Der erste Thread, der die [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) -Funktion erfolgreich aufruft, übergibt einen Zeiger auf eine Anwendungs definierte [*InitOnceCallback*](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn) -Rückruffunktion und alle Daten, die von der Rückruffunktion benötigt werden. Wenn der-Vorgang erfolgreich ist, wird die *InitOnceCallback* -Rückruffunktion ausgeführt.
2.  Nachfolgende Threads, die versuchen, eine Initialisierung durchführen, werden blockiert, bis der erste Thread entweder die Initialisierung abschließt oder Wenn der erste Thread ausfällt, kann der nächste Thread versuchen, die Initialisierung durchführen, usw.
3.  Wenn die Initialisierung abgeschlossen ist, gibt die Rückruffunktion zurück. Die Rückruffunktion kann optional ein Synchronisierungs Objekt (oder andere Kontext Daten) erstellen und in seinem *Kontext* Ausgabeparameter angeben.
4.  Wenn die Initialisierung erfolgreich ist, wird der Zustand der einmaligen Initialisierungs Struktur in initialisiert geändert, und das *Kontext* handle (sofern vorhanden) wird in der Initialisierungs Struktur gespeichert. Bei nachfolgenden Initialisierungs versuchen werden diese Kontext Daten zurückgegeben. Wenn die Initialisierung fehlschlägt, sind die Daten **null**.

## <a name="asynchronous-one-time-initialization"></a>Asynchrone einmalige Initialisierung

In den folgenden Schritten wird die asynchrone einmalige Initialisierung beschrieben.

1.  Wenn mehrere Threads gleichzeitig versuchen, die Initialisierung durch Aufrufen von [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) with **Init \_ Once \_ Async** zu starten, ist die Funktion für alle Threads erfolgreich, wobei der Parameter *fPending* auf **true** festgelegt ist. Nur ein einziger Thread wird bei der Initialisierung tatsächlich erfolgreich ausgeführt. andere gleichzeitige Versuche ändern den Initialisierungs Status nicht.
2.  Wenn [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) zurückgegeben wird, gibt der Parameter " *fPending* " den Initialisierungs Status an:
    -   Wenn " *fPending* " den Wert " **false**" aufweist, wurde ein Thread erfolgreich initialisiert. Andere Threads sollten alle Kontext Daten bereinigen, die Sie erstellt haben, und die Kontext Daten im *lpContext* -Ausgabeparameter von [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize)verwenden.
    -   Wenn " *Ausstehend* " den Wert " **true**" aufweist, wurde die Initialisierung noch nicht abgeschlossen und andere Threads sollten fortgesetzt
3.  Jeder Thread ruft die [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) -Funktion auf. Der Thread kann optional ein Synchronisierungs Objekt (oder andere Kontext Daten) erstellen und im *lpContext* -Parameter von **InitOnceComplete** angeben.
4.  Wenn [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) zurückgibt, gibt der Rückgabewert an, ob der aufrufende Thread bei der Initialisierung erfolgreich war.
    -   Wenn [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) erfolgreich ist, ist der aufrufende Thread bei der Initialisierung erfolgreich. Der Zustand der einmaligen Initialisierungs Struktur wird in initialisiert geändert, und das *lpContext* -handle (sofern vorhanden) wird in der Initialisierungs Struktur gespeichert.
    -   Wenn [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) fehlschlägt, wurde ein anderer Thread erfolgreich initialisiert. Der aufrufende Thread sollte alle Kontext Daten bereinigen, die er erstellt hat, und [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) mit init aufrufen, um die in der einmaligen Initialisierungs Struktur gespeicherten Kontext Daten abzurufen. **\_ \_ \_**

## <a name="calling-one-time-initialization-from-multiple-sites"></a>Aufrufen One-Time Initialisierung von mehreren Standorten

Die einmalige Initialisierung, die durch eine einzelne **Init \_ Once** -Struktur geschützt wird, kann von mehreren Standorten aus ausgeführt werden. es kann ein anderer Rückruf von jeder Site und die Synchronisierung mit und ohne Rückruf gemischt werden. Die Initialisierung wird immer noch für die gleichzeitige Durchführung garantiert.

Die asynchrone und synchrone Initialisierung kann jedoch nicht gemischt werden: Wenn versucht wird, die asynchrone Initialisierung zu starten, treten beim Versuch, die synchrone Initialisierung zu starten, Fehler

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der One-Time Initialisierung](using-one-time-initialization.md)
</dt> </dl>

 

 
