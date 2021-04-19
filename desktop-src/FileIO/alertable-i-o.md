---
description: Warn Bare e/a ist die Methode, mit der Anwendungsthreads asynchrone e/a-Anforderungen verarbeiten, wenn Sie sich in einem wartungstabellenzustand befinden.
ms.assetid: d996f1cc-eeab-456b-818b-5307a79effd9
title: Warn Bare e/a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb830dfadb97051c47b2472eb3e7a3c2d6a0bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347026"
---
# <a name="alertable-io"></a>Warn Bare e/a

Warn Bare e/a ist die Methode, mit der Anwendungsthreads asynchrone e/a-Anforderungen verarbeiten, wenn Sie sich in einem wartungstabellenzustand befinden.

Um zu verstehen, wenn sich ein Thread in einem Warn baren Zustand befindet, sollten Sie das folgende Szenario in Erwägung ziehen:

1.  Ein Thread initiiert eine asynchrone Lese Anforderung durch Aufrufen von " [**lesefileex**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) " mit einem Zeiger auf eine Rückruffunktion.
2.  Der Thread initiiert eine asynchrone Schreib Anforderung, indem er "Write [**fileex**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) " mit einem Zeiger auf eine Rückruffunktion aufruft.
3.  Der Thread ruft eine Funktion auf, die eine Zeile mit Daten von einem Remote-Datenbankserver abruft.

In diesem Szenario werden die Aufrufe von "read [**fileex**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) " und " [**schreitefileex**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) " wahrscheinlich vor dem Funktionsaufruf in Schritt 3 zurückgegeben. Wenn dies der Fall ist, platziert der Kernel die Zeiger auf die Rückruf Funktionen in der asynchronen Prozedur aufrufswarteschlange (APC) des Threads. Der Kernel verwaltet diese Warteschlange speziell zum Speichern zurückgegebener e/a-Anforderungs Daten, bis Sie vom entsprechenden Thread verarbeitet werden kann.

Wenn das Abrufen der Zeile beendet ist und der Thread von der Funktion zurückgegeben wird, besteht die höchste Priorität darin, die zurückgegebenen e/a-Anforderungen in der Warteschlange zu verarbeiten, indem die Rückruf Funktionen aufgerufen werden. Zu diesem Zweck muss ein Warn Tabellen Status eingegeben werden. Ein Thread kann dies nur durch Aufrufen einer der folgenden Funktionen mit den entsprechenden Flags erreichen:

-   [**SleepEx**](/windows/desktop/api/synchapi/nf-synchapi-sleepex)
-   [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)
-   [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex)
-   [**Signalobjectandwait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)
-   [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex)

Wenn der Thread in einen Warn baren Status wechselt, treten die folgenden Ereignisse auf:

1.  Der Kernel überprüft die APC-Warteschlange des Threads. Wenn die Warteschlange Rückruf Funktionszeiger enthält, entfernt der Kernel den Zeiger aus der Warteschlange und sendet ihn an den Thread.
2.  Der Thread führt die Rückruffunktion aus.
3.  Die Schritte 1 und 2 werden für jeden Zeiger wiederholt, der in der Warteschlange verbleiben.
4.  Wenn die Warteschlange leer ist, gibt der Thread von der Funktion zurück, die ihn in einen Warn baren Zustand versetzt hat.

Wenn der Thread in diesem Szenario in einen wartungstabellenzustand wechselt, ruft er die an " [**getfileex**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) " und " [**Write fileex**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)" gesendeten Rückruf Funktionen auf und gibt dann von der Funktion zurück, die ihn in einen Warn baren Zustand versetzt hat.

Wenn ein Thread in einen Warn baren Zustand wechselt, während die zugehörige APC-Warteschlange leer ist, wird die Ausführung des Threads vom Kernel angehalten, bis eine der folgenden Aktionen auftritt:

-   Das Kernel Objekt, auf das gewartet wird, wird signalisiert.
-   Ein Rückruf Funktionszeiger wird in die APC-Warteschlange eingefügt.

Ein Thread, der Warn Bare e/a-Vorgänge verwendet, verarbeitet asynchrone e/a-Anforderungen effizienter als bei der einfachen Wartezeit auf das ereignisflag in der [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp enden Struktur, und der Warnbare e/a-Mechanismus ist weniger kompliziert als die zu verwendenden e/a-Abschlussports. [](i-o-completion-ports.md) Allerdings wird das Ergebnis der e/a-Anforderung nur an den Thread zurückgegeben, der die e/a-Anforderung initiiert hat. Für e/a-Abschlussports gilt diese Einschränkung nicht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Asynchrone Prozedur Aufrufe](/windows/desktop/Sync/asynchronous-procedure-calls)
</dt> </dl>

 

 
