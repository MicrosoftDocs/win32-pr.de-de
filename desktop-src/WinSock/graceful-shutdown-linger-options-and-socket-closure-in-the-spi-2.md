---
description: Es ist wichtig, zwischen dem Herunterfahren einer Socketverbindung und dem Schließen eines Sockets zu unterscheiden.
ms.assetid: f076b1ec-6b96-4386-8519-4728e0a2b1ff
title: Ordnungsgemäßes Herunterfahren, Lingeroptionen und Socketabschluss in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5791732404948fe59d3f5c15c2ac46cdbba8d8327fb3dc5f794be1f070a9eeff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132133"
---
# <a name="graceful-shutdown-linger-options-and-socket-closure-in-the-spi"></a>Ordnungsgemäßes Herunterfahren, Lingeroptionen und Socketabschluss in der SPI

Es ist wichtig, zwischen dem Herunterfahren einer Socketverbindung und dem Schließen eines Sockets zu unterscheiden. Das Herunterfahren einer Socketverbindung umfasst den Austausch von Protokollmeldungen zwischen den beiden Endpunkten. Dies wird nachfolgend als Abschaltungssequenz bezeichnet. Es werden zwei allgemeine Klassen von Sequenzen zum Herunterfahren definiert: ordnungsgemäß und abortiv. In einer sequenzierten Sequenz zum ordnungsgemäßen Herunterfahren können alle Daten, die in die Warteschlange eingereiht, aber noch nicht übertragen wurden, vor dem Schließen der Verbindung gesendet werden. Bei einem abgebrochenen Herunterfahren geht jede nicht angezeigte Daten verloren. Das Auftreten einer Sequenz zum Herunterfahren (ordnungsgemäß oder abortiv) kann auch verwendet werden, um den zugeordneten Anwendungen eine FD CLOSE-Angabe zu geben, \_ die anzeigt, dass ein Herunterfahren ausgeführt wird. Das Schließen eines Sockets bewirkt hingegen, dass die Zuordnung des Sockethandle freigegeben wird, sodass die Anwendung auf keinen Fall mehr auf den Socket verweisen oder diesen verwenden kann.

In Windows Sockets können sowohl die [**WSPShutdown-Funktion**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) als auch die [**WSPSendDisconnect-Funktion**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) verwendet werden, um eine Abschaltungssequenz zu initiieren, während die [**WSPCloseSocket-Funktion**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) verwendet wird, um die Zuordnung von Sockethandles freizugeben und alle zugeordneten Ressourcen freizugeben. Es entsteht jedoch ein gewisses Maß an Verwirrung durch die Tatsache, dass die **WSPCloseSocket-Funktion** implizit dazu führt, dass eine Abschaltungssequenz auftritt, wenn sie noch nicht erfolgt ist. Tatsächlich ist es eine recht gängige Programmierpraktiken geworden, sich auf dieses Feature zu verlassen und **WSPCloseSocket** zu verwenden, um sowohl die Abschaltungssequenz zu initiieren als auch die Zuordnung des Sockethandle zu heben.

Um diese Verwendung zu vereinfachen, stellt die Sockets-Schnittstelle Steuerelemente über den Socketoptionsmechanismus bereit, mit dem der Programmierer angeben kann, ob die implizite Herunterfahrsequenz ordnungsgemäß oder abortiv sein soll, und ob die Funktion verweilen soll, d. h. nicht sofort abgeschlossen werden soll, um eine ordnungsgemäße Beendigungssequenz zu ermöglichen.

Durch das Festlegen geeigneter Werte für die Socketoptionen SO \_ LINGER und SO \_ DONTLINGER können die folgenden Verhaltenstypen mit der [**WSPCloseSocket-Funktion**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) abgerufen werden.

-   Sequenz zum Abbrechen des Herunterfahrens, sofortige Rückgabe von [**WSPCloseSocket.**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))
-   Ordnungsgemäßes Herunterfahren, Rückgabe verzögern, bis die Sequenz zum Herunterfahren abgeschlossen ist oder ein angegebenes Zeitintervall verstrichen ist. Wenn das Zeitintervall abläuft, bevor die Sequenz zum ordnungsgemäßen Herunterfahren abgeschlossen wird, tritt eine abortive Shutdown-Sequenz auf, und [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) wird zurückgegeben.
-   Ordnungsgemäßes Herunterfahren, sofortige Rückgabe und Abschluss der Abschaltung im Hintergrund. Dies ist das Standardverhalten. Beachten Sie jedoch, dass die Anwendung nicht wissen kann, wann (oder ob) die Sequenz des ordnungsgemäßen Herunterfahrens abgeschlossen ist.

Eine Technik, die verwendet werden kann, um die Wahrscheinlichkeit von Problemen beim Beenden der Verbindung zu minimieren, besteht nicht darin, sich auf ein implizites Herunterfahren zu verlassen, das von [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))initiiert wird. Stattdessen wird eine der beiden expliziten Funktionen zum Herunterfahren [**(WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) oder [**WSPSendDisconnect)**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85))verwendet. Dies führt wiederum dazu, dass die Peeranwendung eine FD \_ CLOSE-Angabe empfängt, die angibt, dass alle ausstehenden Daten empfangen wurden. Um dies zu veranschaulichen, zeigt die folgende Tabelle die Funktionen, die von den Client- und Serverkomponenten einer Anwendung aufgerufen werden, wobei der Client für das Initiieren eines ordnungsgemäßen Herunterfahrens verantwortlich ist.

| Clientseitig                                                                                                                         | Serverseitig                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| (1) Ruft [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) (*s*, SD \_ SEND) auf, um das Ende der Sitzung zu signalisieren, und dieser Client verfügt nicht mehr über zu sendende Daten. |                                                                                                              |
|                                                                                                                                     | (2) Empfängt FD \_ CLOSE und gibt an, dass das ordnungsgemäße Herunterfahren ausgeführt wird und alle Daten empfangen wurden.        |
|                                                                                                                                     | (3) Sendet alle verbleibenden Antwortdaten.                                                                       |
| (5') Ruft FD READ ab \_ und ruft recv auf, um vom Server gesendete Antwortdaten abzurufen.                                                         | (4) Ruft [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85))(*s*, SD \_ SEND) auf, um anzugeben, dass der Server keine daten mehr senden muss. |
| (5) Empfängt die \_ FD CLOSE-Angabe.                                                                                                  | (4') Ruft [ **WSPCloseSocket** auf](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                      |
| (6) Ruft [ **WSPCloseSocket** auf](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                              |                                                                                                              |



 

Die Zeitsteuerungssequenz wird von Schritt (1) bis Schritt (6) zwischen dem Client und dem Server beibehalten, mit Ausnahme der Schritte (4') und (5'), die nur lokale Zeitliche Bedeutung haben, da Schritt (5) Schritt (5) auf clientseitiger Seite folgt, während Schritt (4) Schritt (4) auf serverseitiger Seite ohne Zeitliche Steuerungsbeziehung mit der Remotepartei folgt.

 

 
