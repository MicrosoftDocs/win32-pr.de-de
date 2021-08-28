---
description: Komponenten sind häufig für die Durchführung von Initialisierungsaufgaben konzipiert, wenn sie zum ersten Mal aufgerufen werden, und nicht beim Laden.
ms.assetid: 404c083c-7bee-44c2-b8e7-da1901b6ab2f
title: One-Time Initialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e513c18be3fcce85c8d2cde16bbe11edcf6a1597bb06c37279ecaa8add6598
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073080"
---
# <a name="one-time-initialization"></a>One-Time Initialisierung

Komponenten sind häufig für die Durchführung von Initialisierungsaufgaben konzipiert, wenn sie zum ersten Mal aufgerufen werden, und nicht beim Laden. Die Einmalige Initialisierungsfunktionen stellen sicher, dass diese Initialisierung nur einmal erfolgt, auch wenn mehrere Threads versuchen können, die Initialisierung auszuführen.

**Windows Server 2003 und Windows XP:** Anwendungen müssen ihre eigene Synchronisierung für die einmalige Initialisierung bereitstellen, indem sie die ineinandergreifenden Funktionen oder [einen](interlocked-variable-access.md) anderen Synchronisierungsmechanismus verwenden. Die einmaligen Initialisierungsfunktionen sind ab Windows Vista und Windows Server 2008 verfügbar.

Die einmaligen Initialisierungsfunktionen bieten erhebliche Vorteile, um sicherzustellen, dass nur ein Thread die Initialisierung ausführt:

-   Sie sind für geschwindigkeitsoptimiert.
-   Sie schaffen die entsprechenden Barrieren für Prozessorarchitekturen, die sie erfordern.
-   Sie unterstützen sowohl die gesperrte als auch die parallele Initialisierung.
-   Sie vermeiden interne Sperren, damit der Code asynchron oder synchron ausgeführt werden kann.

Das System verwaltet den Initialisierungsprozess über eine nicht transparente **INIT \_ ONCE-Struktur,** die Daten und Zustandsinformationen enthält. Der Aufrufer ordnet diese Struktur zu und initialisiert sie, indem er [**entweder InitOnceInitialize**](/windows/win32/api/synchapi/nf-synchapi-initonceinitialize) aufruft (um die Struktur dynamisch zu initialisieren) oder die Konstante **INIT \_ ONCE STATIC \_ \_ INIT** der Strukturvariablen zu zuweisen (um die Struktur statisch zu initialisieren). Anfänglich sind die in der Einmaligen Initialisierungsstruktur gespeicherten Daten NULL, und ihr Zustand ist nicht initialisiert.

Einmalige Initialisierungsstrukturen können nicht prozessübergreifend gemeinsam genutzt werden.

Der Thread, der die Initialisierung ausführt, kann optional einen Kontext festlegen, der dem Aufrufer nach Abschluss der Initialisierung zur Verfügung steht. Der Kontext kann ein Synchronisierungsobjekt oder ein Wert oder eine Datenstruktur sein. Wenn es sich bei dem Kontext um einen Wert handelt, muss das **INIT \_ ONCE \_ CTX \_ RESERVED \_ BITS** in niedriger Reihenfolge 0 (null) sein. Wenn der Kontext eine Datenstruktur ist, muss die Datenstruktur **DWORD-ausgerichtet** sein. Der Kontext wird an den Aufrufer im *lpContext-Ausgabeparameter* der [**InitOnceBeginInitialize-**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) oder [**InitOnceExecuteOnce-Funktion**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) zurückgegeben.

Die einmalige Initialisierung kann synchron oder asynchron ausgeführt werden. Eine optionale Rückruffunktion kann für die synchrone einmalige Initialisierung verwendet werden.

## <a name="synchronous-one-time-initialization"></a>Synchrone einmalige Initialisierung

In den folgenden Schritten wird die synchrone einmalige Initialisierung beschrieben, bei der keine Rückruffunktion verwendet wird.

1.  Der erste Thread, der die [**InitOnceBeginInitialize-Funktion**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) aufruft, bewirkt erfolgreich, dass die einmalige Initialisierung beginnt. Für die synchrone einmalige Initialisierung muss **InitOnceBeginInitialize** ohne **das INIT \_ ONCE \_ ASYNC-Flag aufgerufen** werden.
2.  Nachfolgende Threads, die eine Initialisierung versuchen, werden blockiert, bis der erste Thread entweder die Initialisierung abgeschlossen hat oder fehlschlägt. Wenn beim ersten Thread ein Fehler auftritt, kann der nächste Thread die Initialisierung versuchen, und so weiter.
3.  Wenn die Initialisierung abgeschlossen ist, ruft der Thread die [**InitOnceComplete-Funktion**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) auf. Der Thread kann optional ein Synchronisierungsobjekt (oder andere Kontextdaten) erstellen und es im *lpContext-Parameter* der **InitOnceComplete-Funktion** angeben.
4.  Wenn die Initialisierung erfolgreich ist, wird der Zustand der einmaligen Initialisierungsstruktur in initialisiert geändert, und das *lpContext-Handle* (falls erforderlich) wird in der Initialisierungsstruktur gespeichert. Nachfolgende Initialisierungsversuche geben diese Kontextdaten zurück. Wenn bei der Initialisierung ein Fehler auftritt, sind die Daten **NULL.**

In den folgenden Schritten wird die synchrone einmalige Initialisierung beschrieben, die eine Rückruffunktion verwendet.

1.  Der erste Thread, der die [**InitOnceExecuteOnce-Funktion**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) erfolgreich aufruft, übergibt einen Zeiger auf eine anwendungsdefinierte [*InitOnceCallback-Rückruffunktion*](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn) und alle für die Rückruffunktion erforderlichen Daten. Wenn der Aufruf erfolgreich ist, wird die *InitOnceCallback-Rückruffunktion* ausgeführt.
2.  Nachfolgende Threads, die eine Initialisierung versuchen, werden blockiert, bis der erste Thread entweder die Initialisierung abgeschlossen hat oder fehlschlägt. Wenn beim ersten Thread ein Fehler auftritt, kann der nächste Thread die Initialisierung versuchen, und so weiter.
3.  Wenn die Initialisierung abgeschlossen ist, gibt die Rückruffunktion zurück. Die Rückruffunktion kann optional ein Synchronisierungsobjekt (oder andere Kontextdaten) erstellen und es im *Kontextausgabeparameter* angeben.
4.  Wenn die Initialisierung erfolgreich ist, wird der Zustand der Struktur für die einmalige Initialisierung in initialisiert geändert, und das *Context-Handle* (sofern diese ist) wird in der Initialisierungsstruktur gespeichert. Nachfolgende Initialisierungsversuche geben diese Kontextdaten zurück. Wenn bei der Initialisierung ein Fehler auftritt, sind die Daten **NULL.**

## <a name="asynchronous-one-time-initialization"></a>Asynchrone einmalige Initialisierung

In den folgenden Schritten wird die asynchrone einmalige Initialisierung beschrieben.

1.  Wenn mehrere Threads gleichzeitig versuchen, die Initialisierung durch Aufrufen [**von InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) mit **INIT \_ ONCE \_ ASYNC** zu starten, ist die Funktion für alle Threads erfolgreich, und der *Parameter fPending* ist auf **TRUE festgelegt.** Bei der Initialisierung ist nur ein Thread erfolgreich. Andere gleichzeitige Versuche ändern den Initialisierungszustand nicht.
2.  Wenn [**InitOnceBeginInitialize zurückgegeben**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) wird, gibt der *fPending-Parameter* den Initialisierungsstatus an:
    -   Wenn *fPending* **auf FALSE festgelegt ist,** war bei der Initialisierung ein Thread erfolgreich. Andere Threads sollten alle erstellten Kontextdaten bereinigen und die Kontextdaten im *lpContext-Ausgabeparameter* von [**InitOnceBeginInitialize verwenden.**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize)
    -   Wenn *fPending* **true ist,** wurde die Initialisierung noch nicht abgeschlossen, und andere Threads sollten fortgesetzt werden.
3.  Jeder Thread ruft die [**InitOnceComplete-Funktion**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) auf. Der Thread kann optional ein Synchronisierungsobjekt (oder andere Kontextdaten) erstellen und es im *lpContext-Parameter* von **InitOnceComplete angeben.**
4.  Wenn [**InitOnceComplete zurückgegeben wird,**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) gibt der Rückgabewert an, ob der aufrufende Thread bei der Initialisierung erfolgreich war.
    -   Wenn [**InitOnceComplete erfolgreich ist,**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) war der aufrufende Thread bei der Initialisierung erfolgreich. Der Zustand der einmaligen Initialisierungsstruktur wird in initialisiert geändert, und das *lpContext-Handle* (falls erforderlich) wird in der Initialisierungsstruktur gespeichert.
    -   Wenn [**InitOnceComplete fehlschlägt,**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) ist bei der Initialisierung ein anderer Thread erfolgreich. Der aufrufende Thread sollte alle erstellten Kontextdaten bereinigen und [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) mit **INIT \_ ONCE CHECK \_ \_ ONLY** aufrufen, um alle Kontextdaten abzurufen, die in der Struktur für die einmalige Initialisierung gespeichert sind.

## <a name="calling-one-time-initialization-from-multiple-sites"></a>Aufrufen One-Time Initialisierung von mehreren Standorten

Die einmalige Initialisierung, die durch eine einzelne **INIT \_ ONCE-Struktur** geschützt wird, kann von mutiple-Standorten aus durchgeführt werden. Von jedem Standort können unterschiedliche Rückrufe übergeben werden, und die Synchronisierung mit und ohne Rückruf kann gemischt werden. Die Initialisierung ist immer noch so gut, dass sie nur einmal erfolgreich ist.

Die asynchrone und synchrone Initialisierung kann jedoch nicht gemischt werden: Sobald die asynchrone Initialisierung versucht wurde, würden Versuche, die synchrone Initialisierung zu starten, fehlschlagen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden One-Time Initialisierung](using-one-time-initialization.md)
</dt> </dl>

 

 
