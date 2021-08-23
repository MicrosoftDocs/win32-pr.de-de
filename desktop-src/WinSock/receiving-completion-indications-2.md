---
description: 'Für den Empfang von Vervollständigungsanzeigen stehen mehrere Optionen zur Verfügung, wodurch Anwendungen ein angemessenes Maß an Flexibilität erhalten. Dazu gehören: Warten (oder Blockieren) auf Ereignisobjekten, Abrufereignisobjekte und Socket-E/A-Abschlussroutinen.'
ms.assetid: 071cf198-6b4c-445e-9bd9-044f57f994a3
title: Empfangen von Vervollständigungsanzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be0ea3d46707eb31d803362f327c309d3c9d948812c0eb3a810e31b896e895e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569250"
---
# <a name="receiving-completion-indications"></a>Empfangen von Vervollständigungsanzeigen

Für den Empfang von Vervollständigungsanzeigen stehen mehrere Optionen zur Verfügung, wodurch Anwendungen ein angemessenes Maß an Flexibilität erhalten. Dazu gehören: Warten (oder Blockieren) auf Ereignisobjekten, Abrufereignisobjekte und Socket-E/A-Abschlussroutinen.

## <a name="blocking-and-waiting-for-completion-indication"></a>Blockieren und Warten auf Abschlussanzeige

Anwendungen können blockieren, während darauf gewartet wird, dass ein oder mehrere Ereignisobjekte mithilfe der [**WSAWaitForMultipleEvents-Funktion festgelegt**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) werden. In Windows Implementierungen wird der Prozess oder Thread tatsächlich blockiert. Da Windows Sockets 2-Ereignisobjekte als Windows-Ereignisse implementiert werden, kann auch die native Windows-Funktion [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects) für diesen Zweck verwendet werden. Dies ist besonders nützlich, wenn der Thread sowohl auf Socket- als auch auf Nichtsocketereignisse warten muss.

## <a name="polling-for-completion-indication"></a>Abruf der Vervollständigungsanzeige

Anwendungen, die nicht blockieren möchten, können die [**WSAGetOverlappedResult-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) verwenden, um den Abschlussstatus eines bestimmten Ereignisobjekts zu erhalten. Diese Funktion gibt an, ob der überlappende Vorgang abgeschlossen wurde, und ordnet bei Abschluss an, dass die [**WSAGetLastError-Funktion**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) den Fehlerstatus des überlappenden Vorgangs abruft.

## <a name="using-socket-io-completion-routines"></a>Verwenden von Socket-E/A-Vervollständigungsroutinen

Die Funktionen, die verwendet werden, um überlappende E/A zu initiieren ( [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)), verwenden *alle lpCompletionRoutine* als optionalen Eingabeparameter. Dies ist ein Zeiger auf eine anwendungsspezifische Funktion, die aufgerufen wird, nachdem ein erfolgreich initiierter überlappende E/A-Vorgang abgeschlossen wurde (erfolgreich oder anderweitig). Die Vervollständigungsroutine folgt den gleichen Regeln wie für Windows-E/A-Vervollständigungsroutinen. Das heißt, die Vervollständigungsroutine wird erst aufgerufen, wenn sich der Thread in einem wartbaren Wartezustand befindet, z. B. wenn die [**Funktion WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) mit dem festgelegten Flag aufgerufen `fAlertable` wird. Eine Anwendung, die die Abschlussroutinenoption für eine bestimmte überlappende E/A-Anforderung verwendet, verwendet möglicherweise nicht die Warteoption [**WSAGetOverlappedResult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) für dieselbe überlappende E/A-Anforderung.

Mit den Transporten kann eine Anwendung Sende- und Empfangsvorgänge innerhalb des Kontexts der Socket-E/A-Abschlussroutine aufrufen und garantieren, dass E/A-Abschlussroutinen für einen bestimmten Socket nicht geschachtelt werden. Dadurch können zeitempfindliche Datenübertragungen vollständig innerhalb eines präemptiven Kontexts erfolgen.

## <a name="summary-of-overlapped-completion-indication-mechanisms"></a>Zusammenfassung der überlappenden Vervollständigungsanzeigemechanismen

Die spezielle überlappende E/A-Vervollständigungsanzeige, die für einen bestimmten überlappenden Vorgang verwendet werden soll, wird durch die Angabe bestimmt, ob die Anwendung einen Zeiger auf eine Vervollständigungsfunktion, ob auf eine [**WSAOVERLAPPED-Struktur**](/windows/desktop/api/Winsock2/ns-winsock2-wsaoverlapped) verwiesen wird, und durch den Wert des **hEvent-Members** innerhalb der **WSAOVERLAPPED-Struktur** (sofern angegeben). Die folgende Tabelle fasst die Vervollständigungssemantik für einen überlappenden Socket zusammen und zeigt die verschiedenen Kombinationen von *lpOverlapped,* **hEvent** und *lpCompletionRoutine:*

| *lpOverlapped* | hEvent         | *lpCompletionRoutine* | Vervollständigungsanzeige                                                                                                                                                                                                    |
|----------------|----------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NULL           | Nicht zutreffend | Wird ignoriert.               | Der Vorgang wird synchron abgeschlossen. Es verhält sich so, als wäre es ein nicht überladener Socket.                                                                                                                                      |
| ! Null          | NULL           | NULL                  | Der Vorgang wird überlappend abgeschlossen, aber es gibt Windows sockets 2-unterstützten Vervollständigungsmechanismus. In diesem Fall kann der Vervollständigungsportmechanismus (sofern unterstützt) verwendet werden. Andernfalls wird keine Abschlussbenachrichtigung angezeigt. |
| ! Null          | ! Null          | NULL                  | Operation completes overlaped, notification by signaling event object. (Vorgang abgeschlossen überlappend, Benachrichtigung durch Signalisierung des Ereignisobjekts.                                                                                                                                                  |
| ! Null          | Wird ignoriert.        | ! Null                 | Der Vorgang schließt überlappende Benachrichtigungen ab, indem die Abschlussroutine geplant wird.                                                                                                                                           |



 

 

 
