---
description: Ein wichtiges Problem beim Portieren von Anwendungen aus einer Berkeley Sockets-Umgebung in eine Windows-Umgebung ist die Blockierung. Dies bedeutet, dass eine Funktion aufgerufen wird, die erst zurückgegeben wird, wenn der zugehörige Vorgang abgeschlossen ist.
ms.assetid: 13aedad7-5f3b-4d73-b8e5-be3a095294bc
title: Windows Sockets 1,1 blockierende Routinen und einen Fortschritt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea6d45b4d25578505a3cb4ab4beb7c2c2fe90e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343761"
---
# <a name="windows-sockets-11-blocking-routines-and-einprogress"></a>Windows Sockets 1,1 blockierende Routinen und einen Fortschritt

Ein wichtiges Problem beim Portieren von Anwendungen aus einer Berkeley Sockets-Umgebung in eine Windows-Umgebung ist die Blockierung. Dies bedeutet, dass eine Funktion aufgerufen wird, die erst zurückgegeben wird, wenn der zugehörige Vorgang abgeschlossen ist. Ein Problem tritt auf, wenn der Vorgang eine beliebig lange Zeit in Anspruch nimmt: ein Beispiel ist eine [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv) -Funktion, die blockiert werden kann, bis Daten vom Peer System empfangen wurden. Das Standardverhalten im Berkeley Sockets-Modell besteht darin, dass ein Socket im Blockierungs Modus betrieben wird, es sei denn, der Programmierer fordert explizit an, dass Vorgänge als nicht blockierende behandelt werden. Windows Sockets 1,1-Umgebungen konnten keine präemptiven Zeitplanung annehmen. Daher wird dringend empfohlen, dass Programmierer die nicht blockierenden (asynchronen) Vorgänge verwenden, sofern dies mit Windows Sockets 1,1 möglich ist. Da dies nicht immer möglich war, wurden die im folgenden beschriebenen Funktionen zur Pseudo Blockierung bereitgestellt.

> [!Note]  
> Windows Sockets 2 wird nur mit präemptiven 32-Bit-Betriebssystemen ausgeführt, bei denen Deadlocks kein Problem darstellen. Für Windows Sockets 1,1 Empfohlene Programmierverfahren sind in Windows Sockets 2 nicht erforderlich.

 

Selbst bei einem blockierenden Socket sind einige Funktionen – [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind), [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)und [**getPeer Name**](/windows/desktop/api/winsock/nf-winsock-getpeername) – sofort fertiggestellt. Es gibt keinen Unterschied zwischen einem blockierenden und einem nicht blockierenden Vorgang für diese Funktionen. Andere Vorgänge, z. b. " [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv)", können sofort durchgeführt werden, oder es kann je nach den verschiedenen Transportbedingungen beliebig lange dauern. Bei Anwendung auf einen blockierenden Socket werden diese Vorgänge als blockierende Vorgänge bezeichnet. Die folgenden Funktionen können blockieren:

-   [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv)
-   [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)
-   [**Senden**](/windows/desktop/api/Winsock2/nf-winsock2-send)
-   [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto)

Mit 16-Bit-Windows Sockets 1,1 wird ein blockierender Vorgang, der nicht sofort ausgeführt werden kann, wie folgt durch Pseudo Blockierung behandelt.

Der Dienstanbieter initiiert den Vorgang und gibt dann eine Schleife ein, in der alle Windows-Meldungen gesendet werden (falls erforderlich, um den Prozessor an einen anderen Thread zu senden), und dann wird überprüft, ob die Windows Sockets-Funktion abgeschlossen ist. Wenn die Funktion abgeschlossen wurde oder [**wsacancelblockingcallaufgerufen**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall) wurde, wird die blockierende Funktion mit einem entsprechenden Ergebnis abgeschlossen.

Ein Dienstanbieter muss die Installation einer blockierenden Hookfunktion zulassen, von der keine Nachrichten verarbeitet werden, um die Möglichkeit zu vermeiden, dass wieder eintretende Nachrichten auftreten, während ein Blockierungs Vorgang aussteht. Die einfachste solche blockierende Hook-Funktion würde **false** zurückgeben. Wenn eine Windows Sockets-DLL von Nachrichten für den internen Vorgang abhängt, kann Sie " **Peer Message**(**hmywnd**...)" ausführen, bevor die Anwendung blockiert wird, die den Hook blockiert, sodass Sie Ihre Nachrichten abrufen kann, ohne dass sich dies auf den Rest des Systems auswirkt.

Wenn in einer 16-Bit-Windows Sockets 1,1-Umgebung eine Windows-Meldung für einen Prozess empfangen wird, für den zurzeit ein Blockierungs Vorgang ausgeführt wird, besteht das Risiko, dass die Anwendung versucht, einen weiteren Windows Sockets-Rückruf auszugeben. Aufgrund der Schwierigkeiten bei der sicheren Verwaltung dieser Bedingung unterstützt Windows Sockets 1,1 dieses Anwendungsverhalten nicht. Es ist nicht zulässig, dass eine Anwendung mehr als einen aufzurufenden Windows Sockets-Funktions aufzurufen. Nur ein ausstehender Funktions Aufrufwert ist für eine bestimmte Aufgabe zulässig. Die einzigen Ausnahmen sind zwei Funktionen, die zur Unterstützung des Programmierers in dieser Situation bereitgestellt werden: [**WSAIsBlocking**](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) und [**wsacancelblockingcall.**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall)

Die [**WSAIsBlocking**](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) -Funktion kann jederzeit aufgerufen werden, um zu bestimmen, ob ein blockierender Windows Sockets 1,1-Aufruf ausgeführt wird. Ebenso kann die [**wsacancelblockingcall-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall) jederzeit aufgerufen werden, um einen aktiven blockierenden Aufruf abzubrechen. Jede andere Schachtelung von Windows Sockets-Funktionen schlägt mit dem Fehler "wsaerprogress" fehl.

Es sollte hervorgehoben werden, dass diese Einschränkung für blockierende und nicht blockierende Vorgänge gilt. Bei Windows Sockets 2-Anwendungen, die Version 2,0 oder höher zum Aufruf von [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup)aushandeln, wird keine Einschränkung für die Schachtelung von Vorgängen beendet. Vorgänge können in seltenen Fällen, z. b. während eines [**wsaaccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) -Rückrufs zur bedingten Akzeptanz, oder wenn ein Dienstanbieter wiederum eine Windows Sockets 2-Funktion aufruft.

Obwohl dieser Mechanismus für einfache Anwendungen ausreichend ist, kann er die komplexen Anforderungen für die Nachrichten Verteilung erweiterter Anwendungen (z. b. solche, die das MDI-Modell verwenden) nicht unterstützen. Bei solchen Anwendungen enthält die Windows Sockets-API die Funktion [**wsasetblockinghook**](/windows/desktop/api/winsock2/nf-winsock2-wsasetblockinghook), die es der Anwendung ermöglicht, eine spezielle Routine anzugeben, die anstelle der standardmäßigen nachrichtendispatchroutine aufgerufen werden kann, die in der vorherigen Diskussion beschrieben wird.

Der Windows Sockets-Anbieter Ruft den blockierenden Hook nur auf, wenn Folgendes zutrifft:

-   Die Routine ist eine, die so definiert ist, dass Sie blockiert werden kann.
-   Der angegebene Socket ist ein blockierender Socket.
-   Die Anforderung kann nicht sofort abgeschlossen werden.

Ein Socket ist standardmäßig auf "blockieren" festgelegt, aber die [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) -Funktion mit der Funktion " **atonbio** ioctl" oder " [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) " kann einen Socket in den nicht blockierenden Modus setzen.

Der blockierende Hook wird niemals aufgerufen, und die Anwendung muss sich nicht mit den erneuten Eintretens befassen, die der blockierende Hook einführen kann, wenn eine Anwendung diese Richtlinien befolgt:

-   Es werden nur nicht blockierende Sockets verwendet.
-   Dabei werden die Routinen " [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) " und "/" und " **WSAAsyncGetXbyY** " anstelle von " [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) " und " **getxbyy** " verwendet.

Wenn eine Windows Sockets 1,1-Anwendung einen asynchronen oder nicht blockierenden Vorgang aufruft, der einen Zeiger auf ein Speicher Objekt (z. b. einen Puffer oder eine globale Variable) als Argument annimmt, liegt es in der Verantwortung der Anwendung, sicherzustellen, dass das Objekt für Windows-Sockets während des Vorgangs verfügbar ist. Die Anwendung darf keine Windows-Funktion aufrufen, die sich auf die Zuordnung oder Adress Lebensfähigkeit des Beteiligten Arbeitsspeichers auswirken könnte.

 

 



