---
description: Das folgende Material wird zur Verdeutlichung des Themas zum Herunterfahren von Socketverbindungen bereitgestellt, die die Sockets schließen. Es ist wichtig, den Unterschied zwischen dem Herunterfahren einer Socketverbindung und dem Schließen eines Sockets zu unterscheiden.
ms.assetid: 383747c3-dd3d-4a18-b4e8-2815d5e5c0c7
title: Graceful Shutdown, Linger Options, and Socket Closure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbab1dd06f6dff444cb5a0cde5dc69133aa14c1b8cad1e5da5416f8f8f19b37e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112236"
---
# <a name="graceful-shutdown-linger-options-and-socket-closure"></a>Graceful Shutdown, Linger Options, and Socket Closure

Das folgende Material wird zur Verdeutlichung des Themas zum Herunterfahren von Socketverbindungen bereitgestellt, die die Sockets schließen. Es ist wichtig, den Unterschied zwischen dem Herunterfahren einer Socketverbindung und dem Schließen eines Sockets zu unterscheiden.

Das Herunterfahren einer Socketverbindung umfasst einen Austausch von Protokollmeldungen zwischen den beiden Endpunkten, nachfolgend als Sequenz zum Herunterfahren bezeichnet. Es werden zwei allgemeine Klassen von Shutdownsequenzen definiert: graceful und abortive (auch als hard bezeichnet). In einer sequenz zum ordnungsgemäßen Herunterfahren können alle Daten, die in die Warteschlange gestellt, aber noch nicht übertragen wurden, gesendet werden, bevor die Verbindung geschlossen wird. Beim abbruchiven Herunterfahren gehen alle nicht zu sehenden Daten verloren. Das Auftreten einer Sequenz zum Herunterfahren (ordnungsgemäß oder abortiv) kann auch verwendet werden, um den zugeordneten Anwendungen einen FD CLOSE-Hinweis zu geben, der ankäischt, dass ein Herunterfahren \_ ausgeführt wird.

Das Schließen eines Sockets bewirkt hingegen, dass die Sockethandys nicht mehr zugewiesen werden, sodass die Anwendung nicht mehr auf den Socket verweisen oder den Socket in irgendeiner Weise verwenden kann.

In Windows Sockets können sowohl [](/windows/desktop/api/winsock/nf-winsock-shutdown) die Funktion zum Herunterfahren als auch die [**WSASendDisconnect-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) verwendet werden, um eine Sequenz zum Herunterfahren zu initiieren, während die [**closesocket-Funktion**](/windows/desktop/api/winsock/nf-winsock-closesocket) verwendet wird, um socket-Handles frei zu machen und alle zugeordneten Ressourcen frei zu geben. Einige Verwirrung entsteht jedoch aus der Tatsache, dass die **closesocket-Funktion** implizit bewirkt, dass eine Sequenz zum Herunterfahren auftritt, wenn sie noch nicht erfolgt ist. Tatsächlich ist es zu einer eher gängigen Programmierübung geworden, sich auf dieses Feature zu verlassen und **closesocket** zu verwenden, um sowohl die Sequenz zum Herunterfahren zu initiieren als auch die Verbindung mit dem Sockethandy zu beenden.

Um diese Verwendung zu erleichtern, stellt die Sockets-Schnittstelle Steuerelemente über den Socketoptionsmechanismus bereit, mit denen der Programmierer angeben kann, ob die Sequenz zum impliziten Herunterfahren ordnungsgemäß oder abortiv sein soll, und ob die [**closesocket-Funktion**](/windows/desktop/api/winsock/nf-winsock-closesocket) (die nicht sofort abgeschlossen ist) anhalten soll, um Zeit für den Abschluss einer ordnungsgemäßen Herunterfahrensequenz zu ermöglichen. Diese wichtigen Unterschiede und die Auswirkungen der Verwendung von **closesocket** auf diese Weise sind immer noch nicht allgemein bekannt.

Durch Festlegen geeigneter Werte für die Socketoptionen SO LINGER und SO DONTLINGER können mit der \_ \_ [**closesocket-Funktion**](/windows/desktop/api/winsock/nf-winsock-closesocket) die folgenden Verhaltensmuster ermittelt werden:

-   Sequenz zum abbrechen des Herunterfahrens, sofortige Rückgabe [**von closesocket.**](/windows/desktop/api/winsock/nf-winsock-closesocket)
-   Graceful shutdown, delaying return until either shutdown sequence complete or a specified time interval verstreichen. Wenn das Zeitintervall abläuft, bevor die Sequenz zum ordnungsgemäßen Herunterfahren abgeschlossen ist, wird eine Sequenz zum abbrechen des Herunterfahrens ausgeführt, und [**closesocket wird**](/windows/desktop/api/winsock/nf-winsock-closesocket) zurückgegeben.
-   Ordnungsgemäß heruntergefahren, sofortige Rückgabe – damit die Sequenz des Herunterfahrens im Hintergrund abgeschlossen werden kann. Obwohl dies das Standardverhalten ist, kann die Anwendung nicht wissen, wann (oder ob) die Sequenz zum ordnungsgemäßen Herunterfahren tatsächlich abgeschlossen wird.

Die Verwendung der So-LINGER- und SO DONTLINGER-Socketoptionen und der zugeordneten linger-Struktur wird in den Referenzabschnitten zu SOL SOCKET Socket Options und der \_ \_ **linger-Struktur** [**\_**](sol-socket-socket-options.md) [](/windows/desktop/api/winsock/ns-winsock-linger) ausführlicher erläutert.

Eine Technik, die verwendet werden kann, um die Wahrscheinlichkeit von Problemen zu minimieren, die während des Verbindungsabbruchs auftreten, besteht in der Vermeidung, dass ein implizites Herunterfahren durch [**closesocket initiiert wird.**](/windows/desktop/api/winsock/nf-winsock-closesocket) Verwenden Sie stattdessen eine der beiden expliziten Herunterfahrensfunktionen, [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) oder [**WSASendDisconnect.**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) Dadurch wird wiederum eine FD CLOSE-Angabe von der Peeranwendung empfangen, die angibt, dass alle ausstehenden \_ Daten empfangen wurden. Um dies zu veranschaulichen, zeigt die folgende Tabelle die Funktionen, die von den Client- und Serverkomponenten einer Anwendung aufgerufen werden, wobei der Client für das Initiieren eines ordnungsgemäßen Herunterfahrens verantwortlich ist.

| Clientseitig                                                                                                                | Serverseitig                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| (1) Ruft das [**Herunterfahren**](/windows/desktop/api/winsock/nf-winsock-shutdown)(s, SD SEND) auf, um das Ende der Sitzung zu signalisieren, und der Client hat \_ keine daten mehr zu senden. |                                                                                                       |
|                                                                                                                            | (2) Empfängt FD CLOSE, was angibt, dass das ordnungsgemäß heruntergefahren wird und \_ alle Daten empfangen wurden. |
|                                                                                                                            | (3) Sendet alle verbleibenden Antwortdaten.                                                                |
| (nur lokale Zeitsteuerungs-Signifikanz) Ruft FD \_ READ ab und ruft [**recv auf,**](/windows/desktop/api/winsock/nf-winsock-recv) um alle Antwortdaten zu erhalten, die vom Server gesendet werden.  | (4) Ruft das [**Herunterfahren**](/windows/desktop/api/winsock/nf-winsock-shutdown)(s, SD SEND) auf, um anzugeben, \_ dass der Server über keine zu sendenden Daten mehr verfügt.  |
| (5) Empfängt die FD \_ CLOSE-Angabe.                                                                                         | (nur lokale Zeitsteuerungs-Signifikanz) Ruft [**closesocket auf.**](/windows/desktop/api/winsock/nf-winsock-closesocket)                       |
| (6) Ruft [**closesocket auf.**](/windows/desktop/api/winsock/nf-winsock-closesocket)                                                                          |                                                                                                       |



 

 

 



