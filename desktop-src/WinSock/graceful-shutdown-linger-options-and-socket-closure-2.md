---
description: Das folgende Material wird als Erläuterung für das Herunterfahren von Socketverbindungen zur Schließung der Sockets bereitgestellt. Es ist wichtig, den Unterschied zwischen dem Herunterfahren einer Socketverbindung und dem Schließen eines Sockets zu unterscheiden.
ms.assetid: 383747c3-dd3d-4a18-b4e8-2815d5e5c0c7
title: Ordnungsgemäßes Herunterfahren, Linger Optionen und Socket-Schließung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59f6791eaa803da561fc9f3c175b5270950cbec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214596"
---
# <a name="graceful-shutdown-linger-options-and-socket-closure"></a>Ordnungsgemäßes Herunterfahren, Linger Optionen und Socket-Schließung

Das folgende Material wird als Erläuterung für das Herunterfahren von Socketverbindungen zur Schließung der Sockets bereitgestellt. Es ist wichtig, den Unterschied zwischen dem Herunterfahren einer Socketverbindung und dem Schließen eines Sockets zu unterscheiden.

Das Herunterfahren einer Socketverbindung umfasst einen Austausch der Protokollmeldungen zwischen den beiden Endpunkten, die im folgenden als eine Shutdown-Sequenz bezeichnet werden. Zwei allgemeine Klassen von Shutdown-Sequenzen werden definiert: ordnungsgemäß und abgebrochen (auch als hart bezeichnet). In einer ordnungsgemäßen Shutdown-Sequenz können alle Daten, die in die Warteschlange eingereiht, aber noch nicht übertragen wurden, vor dem Schließen der Verbindung gesendet werden. Bei einem Abbruch werden alle nicht gesendeten Daten verloren gehen. Das Vorkommen einer Sequenz zum Herunterfahren (ordnungsgemäß oder abgebrochen) kann auch verwendet werden, um \_ die zugeordneten Anwendungen mit dem Hinweis zu versehen, dass ein Herunterfahren ausgeführt wird.

Das Schließen eines Sockets hingegen bewirkt, dass das Sockethandle freigegeben wird, sodass die Anwendung nicht mehr auf den Socket verweisen oder Sie verwenden kann.

In Windows Sockets können sowohl die [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) -Funktion als auch die [**wsasenddisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) -Funktion verwendet werden, um eine Sequenz für das Herunterfahren zu initiieren, während die [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) -Funktion verwendet wird, um die Zuordnung von Sockethandles freizugeben und alle zugeordneten Ressourcen freizugeben. Eine gewisse Verwirrung ergibt sich jedoch aus der Tatsache, dass die **closesocket** -Funktion implizit bewirkt, dass eine Shutdown-Sequenz auftritt, wenn Sie nicht bereits geschehen ist. Tatsächlich wurde sie zu einem eher gängigen Programmierverfahren, das sich auf dieses Feature verlassen und **closesocket** verwendet, um die Shutdown-Sequenz zu initiieren und das Sockethandle freizugeben.

Um diese Verwendung zu vereinfachen, stellt die Sockets-Schnittstelle für Steuerelemente über den socketoptions-Mechanismus bereit, mit dem der Programmierer angeben kann, ob die implizite Beendigungs Sequenz ordnungsgemäß oder abgebrochen werden soll, und ob die [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) -Funktion gestellend sein soll (der nicht sofort beendet wird), um Zeit für eine ordnungsgemäße Herunterfahr Sequenz zu ermöglichen. Diese wichtigen Unterschiede und die Auswirkungen der Verwendung von **closesocket** auf diese Weise sind immer noch nicht bekannt.

Wenn Sie geeignete Werte für die Socketoptionen für " \_ LINGER" und " \_ DontLinger" festlegen, können die folgenden Verhaltenstypen mit der [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) -Funktion abgerufen werden:

-   Abbruch Sequenz, sofortige Rückgabe von [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).
-   Ordnungsgemäßes Herunterfahren, verzögern der Rückgabe, bis das Herunterfahren entweder abgeschlossen oder ein angegebenes Zeitintervall abläuft. Wenn das Zeitintervall abläuft, bevor die ordnungsgemäße Herunterfahr Sequenz abgeschlossen ist, tritt eine Abbruch Sequenz auf, und [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) gibt zurück.
-   Ordnungsgemäßes Herunterfahren, sofortige Rückgabe – ermöglicht das Beenden der Sequenz im Hintergrund. Obwohl dies das Standardverhalten ist, kann die Anwendung nicht wissen, wann (oder ob) die ordnungsgemäße Herunterfahr Sequenz tatsächlich abgeschlossen ist.

Die Verwendung der Optionen "so \_ LINGER" und "so \_ DontLinger Socket" und der zugeordneten [**Linger**](/windows/desktop/api/winsock/ns-winsock-linger) -Struktur wird in den Referenz Abschnitten zu den Optionen für den [**Sol- \_ socketsocket**](sol-socket-socket-options.md) und der **Linger** -Struktur ausführlicher erläutert.

Eine Technik, die verwendet werden kann, um die Wahrscheinlichkeit zu minimieren, dass Probleme während der Verbindungs Löschung auftreten, besteht darin, zu verhindern, dass ein implizites Herunterfahren von [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)initiiert wird. Verwenden Sie stattdessen eine der beiden expliziten Funktionen zum Herunterfahren, [**herunter**](/windows/desktop/api/winsock/nf-winsock-shutdown) fahren oder [**wsasenddisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect). Dies bewirkt wiederum \_ , dass die Peer Anwendung einen "FD Close"-Hinweis erhält, der anzeigt, dass alle ausstehenden Daten empfangen wurden. Um dies zu veranschaulichen, zeigt die folgende Tabelle die Funktionen, die von den Client-und Serverkomponenten einer Anwendung aufgerufen werden, wobei der Client dafür verantwortlich ist, ein ordnungsgemäßes Herunterfahren zu initiieren.

| Clientseitig                                                                                                                | Serverseitig                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| (1) ruft [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown)(s, SD \_ Send) auf, um das Ende der Sitzung zu signalisieren, und der Client hat keine weiteren Daten zum Senden. |                                                                                                       |
|                                                                                                                            | (2) empfängt FD, was bedeutet, dass ein ordnungsgemäßes Herunterfahren ausgeführt \_ wird und alle Daten empfangen wurden. |
|                                                                                                                            | (3) sendet alle verbleibenden Antwortdaten.                                                                |
| (nur lokale Zeit Steuerungs Bedeutung) \_Ruft den FD-Lesevorgang ab und ruft [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv) auf, um vom Server gesendete Antwortdaten zu erhalten.  | (4) ruft [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown)(s, SD \_ Send) auf, um anzugeben, dass der Server keine weiteren Daten zum Senden hat.  |
| (5) empfängt die \_ Bestätigung von FD.                                                                                         | (nur lokale Zeit Steuerungs Bedeutung) Ruft [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) auf.                       |
| (6) ruft [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)auf.                                                                          |                                                                                                       |



 

 

 



