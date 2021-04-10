---
description: Wait Chain Traversal (WCT) ermöglicht es buggern, Anwendungs Abstürze und Deadlocks zu diagnostizieren.
ms.assetid: d266a663-b101-4936-9574-f6ce223419ae
title: Durchlaufen der Warteschlange
ms.topic: article
ms.date: 08/10/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: 842beb7d5470bc2b3e6e9c7c1150ff2aa1a4cf76
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/04/2021
ms.locfileid: "103859939"
---
# <a name="wait-chain-traversal"></a>Durchlaufen der Warteschlange

Wait Chain Traversal (WCT) ermöglicht es buggern, Anwendungs Abstürze und Deadlocks zu diagnostizieren.

Eine *warte Kette* ist eine abwechselnde Sequenz von Threads und Synchronisierungs Objekten, bei denen jeder Thread auf das nachfolgende Objekt wartet. Jedes-Objekt, das folgt, befindet sich wiederum im Besitz des nachfolgenden Threads in der Kette.

Ein Thread wartet auf ein Synchronisierungs Objekt ab dem Zeitpunkt, an dem der Thread das Objekt anfordert, bis der Thread ihn abgerufen hat. Diese "Sperre" ist im Besitz eines Threads ab dem Zeitpunkt, an dem der Thread den Thread erhält, bis der Thread ihn freigibt. Anders ausgedrückt: Wenn Thread 1 auf eine Sperre wartet, die Thread 2 gehört, wird Thread 1 für Thread 2 "warten".

WCT unterstützt die folgenden Synchronisierungs primitiven:

- [Erweiterter lokaler Prozedur Aufrufe (ALPC)](../etw/alpc.md)
- [Component Object Model (COM)](../com/the-component-object-model.md)
- [Kritische Abschnitte](../sync/critical-section-objects.md)
- [Mutexe](../sync/mutex-objects.md)
- [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage)
- [Warte](../sync/wait-functions.md) Vorgänge für [Prozesse und Threads](../procthread/processes-and-threads.md)

Wenn Sie die Warte Kette für einen oder mehrere Threads abrufen möchten, erstellen Sie eine WCT-Sitzung mithilfe der Funktionen [openthgetwaitchainsession](/windows/desktop/api/Wct/nf-wct-openthreadwaitchainsession) und [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) . WCT-Sitzungen werden durch ein Handle des Typs **hwct** dargestellt.

## <a name="sessions-can-be-synchronous-or-asynchronous"></a>Sitzungen können synchron oder asynchron sein.

Synchrone Sitzungen können nicht abgebrochen werden und blockieren den aufrufenden Thread, bis eine warte Kette abgerufen wurde.

Asynchrone Sitzungen blockieren den aufrufenden Thread nicht und können von der Anwendung mithilfe der [closethreadwaitchainsession](/windows/desktop/api/Wct/nf-wct-closethreadwaitchainsession) -Funktion abgebrochen werden. Ergebnisse von asynchronen Vorgängen werden über eine [waitchaincallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) -Rückruffunktion bereitgestellt, die von der Anwendung bereitgestellt wird.

Für asynchrone Sitzungen kann der Aufrufer über [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) einen Zeiger auf eine Kontext Datenstruktur angeben (derselbe Zeiger wird an die [waitchaincallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) -Rückruffunktion übergeben).

Die Kontext Datenstruktur ist Benutzer definiert und für WCT nicht transparent. Sie kann von der Anwendung verwendet werden, um Kontext zwischen einer WCT-Abfrage und einer Rückruffunktion zu kommunizieren. In der Regel übergeben Sie ein Ereignis Handle über diese Struktur. wenn der Rückruf ausgeführt wird, wird dieses Ereignis signalisiert, und ein Überwachungs Thread wird darüber informiert, dass die Abfrage abgeschlossen wurde.

Unter [using WCT finden Sie](using-wct.md) ein Beispiel für die Ausnahme der Warte Kette.

## <a name="related-topics"></a>Zugehörige Themen

[Verwenden von WCT](using-wct.md), [WCT-Referenz](wct-reference.md), [MSDN Magazine 2007 Juli-Bugslayer: Wait Chain Traversal](/archive/msdn-magazine/2007/july/bugslayer-wait-chain-traversal)