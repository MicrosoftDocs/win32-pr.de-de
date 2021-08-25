---
description: Wait Chain Traversal (WCT) ermöglicht Debuggern das Diagnostizieren von Hängen und Deadlocks von Anwendungen.
ms.assetid: d266a663-b101-4936-9574-f6ce223419ae
title: Durchlaufen der Warteschlange
ms.topic: article
ms.date: 08/10/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: 695e5298d0f56d0c53afcd146b19b1fc3c6ccf25e4ec12aec7f2b6b74fb64243
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912310"
---
# <a name="wait-chain-traversal"></a>Durchlaufen der Warteschlange

Wait Chain Traversal (WCT) ermöglicht Debuggern das Diagnostizieren von Hängen und Deadlocks von Anwendungen.

Eine *Wartekette* ist eine abwechselnde Sequenz von Threads und Synchronisierungsobjekten, bei der jeder Thread auf das folgende Objekt wartet. Jedes objekt, das folgt, befindet sich wiederum im Besitz des nachfolgenden Threads in der Kette.

Ein Thread wartet ab dem Zeitpunkt, zu dem der Thread das Objekt anfordert, auf ein Synchronisierungsobjekt, bis der Thread es erhalten hat. Diese "Sperre" befindet sich im Besitz eines Threads ab dem Zeitpunkt, zu dem der Thread ihn erhält, bis der Thread ihn freigibt. Anders ausgedrückt: Wenn Thread 1 auf eine Sperre wartet, die thread 2 gehört, wartet Thread 1 auf Thread 2.

WCT unterstützt die folgenden Synchronisierungsprimitiven:

- [Advanced Local Procedure Call (ALPC)](../etw/alpc.md)
- [Component Object Model (COM)](../com/the-component-object-model.md)
- [Kritische Abschnitte](../sync/critical-section-objects.md)
- [Mutexe](../sync/mutex-objects.md)
- [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage)
- [Wartevorgänge](../sync/wait-functions.md) für [Prozesse und Threads](../procthread/processes-and-threads.md)

Um die Wartekette für einen oder mehrere Threads abzurufen, erstellen Sie eine WCT-Sitzung mithilfe der Funktionen [OpenThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-openthreadwaitchainsession) und [GetThreadWaitChain.](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) WCT-Sitzungen werden durch ein Handle vom Typ **HWCT** dargestellt.

## <a name="sessions-can-be-synchronous-or-asynchronous"></a>Sitzungen können synchron oder asynchron sein.

Synchrone Sitzungen können erst abgebrochen und blockiert werden, wenn eine Wartekette abgerufen wurde.

Asynchrone Sitzungen blockieren den aufrufenden Thread nicht und können von der Anwendung mithilfe der [CloseThreadWaitChainSession-Funktion](/windows/desktop/api/Wct/nf-wct-closethreadwaitchainsession) abgebrochen werden. Ergebnisse von asynchronen Vorgängen werden über eine von der Anwendung bereitgestellte [WaitChainCallback-Rückruffunktion](/windows/win32/api/wct/nc-wct-pwaitchaincallback) verfügbar gemacht.

Bei asynchronen Sitzungen kann der Aufrufer über [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) einen Zeiger auf eine Kontextdatenstruktur angeben (dieser Zeiger wird an die [Rückruffunktion WaitChainCallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) übergeben).

Die Kontextdatenstruktur ist benutzerdefiniert und für WCT nicht transparent. Sie kann von der Anwendung verwendet werden, um den Kontext zwischen einer WCT-Abfrage und einer Rückruffunktion zu kommunizieren. Normalerweise übergeben Sie ein Ereignishandle durch diese Struktur. Wenn der Rückruf ausgeführt wird, wird dieses Ereignis signalisiert, und ein Überwachungsthread wird darüber informiert, dass die Abfrage abgeschlossen wurde.

Ein Beispiel für den Wartekettendurchlauf finden Sie unter [Verwenden von WCT.](using-wct.md)

## <a name="related-topics"></a>Zugehörige Themen

[Verwenden von WCT,](using-wct.md) [WCT-Referenz,](wct-reference.md) [MSDN Magazine 2007 Juli – Bugslayer: Wait Chain Traversal](/archive/msdn-magazine/2007/july/bugslayer-wait-chain-traversal)