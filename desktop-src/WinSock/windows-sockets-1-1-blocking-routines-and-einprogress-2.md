---
description: Ein hauptproblem beim Portieren von Anwendungen aus einer Sockets-Umgebung in eine Windows Umgebung ist das Blockieren. Das bedeutet, dass eine Funktion, die erst dann zurückgegeben wird, wenn der zugeordnete Vorgang abgeschlossen ist, aufruft.
ms.assetid: 13aedad7-5f3b-4d73-b8e5-be3a095294bc
title: Windows Sockets 1.1 Blockierende Routinen und EINPROGRESS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4028549862412b80d1343851fb2a147da804095821fdefab4b6aae0eb6ec5f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641220"
---
# <a name="windows-sockets-11-blocking-routines-and-einprogress"></a>Windows Sockets 1.1 Blockierende Routinen und EINPROGRESS

Ein hauptproblem beim Portieren von Anwendungen aus einer Sockets-Umgebung in eine Windows Umgebung ist das Blockieren. Das bedeutet, dass eine Funktion, die erst dann zurückgegeben wird, wenn der zugeordnete Vorgang abgeschlossen ist, aufruft. Ein Problem tritt auf, wenn der Vorgang beliebig lange dauert: Ein Beispiel ist eine [**recv-Funktion,**](/windows/desktop/api/winsock/nf-winsock-recv) die blockiert werden kann, bis Daten vom Peersystem empfangen wurden. Das Standardverhalten innerhalb des Socketmodells von Sockets besteht darin, dass ein Socket im Blockierungsmodus ausgeführt wird, es sei denn, der Programmierer fordert explizit an, dass Vorgänge als Nichtblockierung behandelt werden. Windows Sockets 1.1-Umgebungen konnten keine präemptive Planung vorausgehen. Daher wurde programmierern dringend empfohlen, die nicht blockierenden (asynchronen) Vorgänge mit Windows Sockets 1.1 zu verwenden, sofern dies überhaupt möglich ist. Da dies nicht immer möglich war, wurden die im Folgenden beschriebenen Pseudoblockierungsmöglichkeiten bereitgestellt.

> [!Note]  
> Windows Sockets 2 werden nur auf präemptiven 32-Bit-Betriebssystemen ausgeführt, bei denen Deadlocks kein Problem darstellen. Für Windows Sockets 1.1 empfohlene Programmiermethoden sind in Windows Sockets 2 nicht erforderlich.

 

Selbst bei einem blockierenden Socket werden einige Funktionen – [**binden**](/windows/desktop/api/winsock/nf-winsock-bind), [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)und [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) – sofort abgeschlossen. Es gibt keinen Unterschied zwischen einer Blockierung und einem Nichtblockierungsvorgang für diese Funktionen. Andere Vorgänge, z. [**B. recv,**](/windows/desktop/api/winsock/nf-winsock-recv)können sofort abgeschlossen werden oder je nach verschiedenen Transportbedingungen eine beliebige Zeit in Anspruch nehmen. Wenn diese Vorgänge auf einen blockierenden Socket angewendet werden, werden sie als blockierende Vorgänge bezeichnet. Die folgenden Funktionen können blockieren:

-   [**Recv**](/windows/desktop/api/winsock/nf-winsock-recv)
-   [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)
-   [**Senden**](/windows/desktop/api/Winsock2/nf-winsock2-send)
-   [**Sendto**](/windows/desktop/api/winsock/nf-winsock-sendto)

Bei 16-Bit-Windows Sockets 1.1 wird ein Blockierungsvorgang, der nicht sofort abgeschlossen werden kann, wie folgt durch Pseudoblockierung behandelt.

Der Dienstanbieter initiiert den Vorgang und gibt dann eine Schleife ein, in der alle Windows Nachrichten gesendet werden (wobei der Prozessor bei Bedarf an einen anderen Thread ausgegeben wird) und dann den Abschluss der Windows Sockets-Funktion überprüft. Wenn die Funktion abgeschlossen wurde oder [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall) aufgerufen wurde, wird die blockierende Funktion mit einem entsprechenden Ergebnis abgeschlossen.

Ein Dienstanbieter muss die Installation einer blockierenden Hookfunktion zulassen, die keine Nachrichten verarbeitet, um die Möglichkeit zu vermeiden, dass Wiedereinstiegsmeldungen während eines ausstehenden Blockierungsvorgangs möglich sind. Die einfachste solche blockierende Hookfunktion würde **FALSE** zurückgeben. Wenn eine Windows Sockets-DLL für den internen Vorgang von Nachrichten abhängig ist, kann sie **PeekMessage**(**hMyWnd**...) ausführen, bevor der blockierende Hook der Anwendung ausgeführt wird, damit sie ihre Nachrichten abrufen kann, ohne den Rest des Systems zu beeinträchtigen.

Wenn in einer 16-Bit-Windows Sockets 1.1-Umgebung eine Windows Nachricht für einen Prozess empfangen wird, für den ein Blockierungsvorgang ausgeführt wird, besteht das Risiko, dass die Anwendung versucht, einen weiteren Windows Sockets-Aufruf auszugeben. Aufgrund der Schwierigkeiten bei der sicheren Verwaltung dieser Bedingung unterstützt Windows Sockets 1.1 dieses Anwendungsverhalten nicht. Eine Anwendung darf nicht mehrere geschachtelte Windows Sockets-Funktionsaufrufe vornehmen. Für eine bestimmte Aufgabe ist nur ein ausstehender Funktionsaufruf zulässig. Die einzigen Ausnahmen sind zwei Funktionen, die zur Unterstützung des Programmierers in dieser Situation bereitgestellt werden: [**WSAIsBlocking**](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) und [**WSACancelBlockingCall.**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall)

Die [**WSAIsBlocking-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) kann jederzeit aufgerufen werden, um zu bestimmen, ob ein blockierender Windows Sockets 1.1-Aufruf ausgeführt wird. Auf ähnliche Weise kann die [**WSACancelBlockingCall-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall) jederzeit aufgerufen werden, um einen in Bearbeitung ausgeführten blockierenden Aufruf abzubrechen. Bei jeder anderen Schachtelung von Windows Sockets-Funktionen tritt der Fehler WSAEINPROGRESS auf.

Es sollte hervorgehoben werden, dass diese Einschränkung sowohl für blockierende als auch für nicht blockierende Vorgänge gilt. Für Windows Sockets 2-Anwendungen, die Version 2.0 oder höher zum Zeitpunkt des Aufrufs von [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup)aushandeln, wird keine Einschränkung für die Schachtelung von Vorgängen beendet. Vorgänge können unter seltenen Umständen geschachtelt werden, z. B. während eines [**WSAAccept-Rückrufs**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) für die bedingte Akzeptanz oder wenn ein Dienstanbieter wiederum eine Windows Sockets 2-Funktion aufruft.

Obwohl dieser Mechanismus für einfache Anwendungen ausreichend ist, kann er die komplexen Anforderungen an die Nachrichtendisponierung von erweiterten Anwendungen (z. B. Anwendungen, die das MDI-Modell verwenden) nicht unterstützen. Für solche Anwendungen enthält die Windows Sockets-API die Funktion [**WSASetBlockingHook,**](/windows/desktop/api/winsock2/nf-winsock2-wsasetblockinghook)mit der die Anwendung eine spezielle Routine angeben kann, die anstelle der in der vorherigen Erläuterung beschriebenen Standardroutine für die Nachrichtendis dispatch aufgerufen werden kann.

Der Windows Sockets-Anbieter ruft den blockierenden Hook nur dann auf, wenn alle der folgenden Punkte zutreffen:

-   Die Routine ist eine Routine, die als blockfähig definiert ist.
-   Der angegebene Socket ist ein blockierender Socket.
-   Die Anforderung kann nicht sofort abgeschlossen werden.

Ein Socket ist standardmäßig auf Blockieren festgelegt, aber die [**ioctlsocket-Funktion**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) mit der **FIONBIO-IOCTL-** oder [**WSAAsyncSelect-Funktion**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) kann einen Socket auf den Nichtblockierungsmodus festlegen.

Der blockierende Hook wird nie aufgerufen, und die Anwendung muss sich nicht um die Wiederholungsprobleme kümmern, die der blockierende Hook einführen kann, wenn eine Anwendung diese Richtlinien befolgt:

-   Es werden nur nicht blockierende Sockets verwendet.
-   Es verwendet die [**WSAAsyncSelect-**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) und/oder **WSAAsyncGetXByY-Routinen** anstelle von [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) und den **getXbyY-Routinen.**

Wenn eine Windows Sockets 1.1-Anwendung einen asynchronen oder nicht blockierenden Vorgang aufruft, der einen Zeiger auf ein Speicherobjekt (z. B. einen Puffer oder eine globale Variable) als Argument verwendet, ist die Anwendung dafür verantwortlich, sicherzustellen, dass das Objekt während des gesamten Vorgangs für Windows Sockets verfügbar ist. Die Anwendung darf keine Windows Funktion aufrufen, die sich auf die Zuordnung oder die Adresslebensfähigkeit des beteiligten Arbeitsspeichers auswirken kann.

 

 



