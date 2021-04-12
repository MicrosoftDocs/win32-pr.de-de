---
description: Es ist wichtig, zwischen dem Herunterfahren einer Socketverbindung und dem Schließen eines Sockets zu unterscheiden.
ms.assetid: f076b1ec-6b96-4386-8519-4728e0a2b1ff
title: Ordnungsgemäßes Herunterfahren, Linger Optionen und Socket-Schließung in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743cae48977421c08611c79053520799420e9e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526165"
---
# <a name="graceful-shutdown-linger-options-and-socket-closure-in-the-spi"></a>Ordnungsgemäßes Herunterfahren, Linger Optionen und Socket-Schließung in der SPI

Es ist wichtig, zwischen dem Herunterfahren einer Socketverbindung und dem Schließen eines Sockets zu unterscheiden. Das Herunterfahren einer Socketverbindung umfasst einen Austausch der Protokollmeldungen zwischen den beiden Endpunkten, die im folgenden als Shutdown-Sequenz bezeichnet werden. Zwei allgemeine Klassen von Shutdown-Sequenzen werden definiert: ordnungsgemäß und abgebrochen. In einer ordnungsgemäßen Shutdown-Sequenz können alle Daten, die in die Warteschlange eingereiht, aber noch nicht übertragen wurden, vor dem Schließen der Verbindung gesendet werden. Bei einem Abbruch werden alle nicht gesendeten Daten verloren gehen. Das Vorkommen einer Sequenz zum Herunterfahren (ordnungsgemäß oder abgebrochen) kann auch verwendet werden, um \_ die zugeordneten Anwendungen mit dem Hinweis zu versehen, dass ein Herunterfahren ausgeführt wird. Das Schließen eines Sockets hingegen bewirkt, dass das Sockethandle freigegeben wird, sodass die Anwendung nicht mehr auf den Socket verweisen oder Sie verwenden kann.

In Windows Sockets können sowohl die Funktion [**wspshutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) als auch die Funktion [**wspsenddisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) zum Initiieren einer Sequenz verwendet werden, während die [**wspclosesocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) -Funktion verwendet wird, um die Zuordnung von Sockethandles freizugeben und alle zugeordneten Ressourcen freizugeben. Es entsteht jedoch ein gewisses Maß an Verwirrung, da die **wspclosesocket** -Funktion implizit bewirkt, dass eine Shutdown-Sequenz auftritt, wenn Sie nicht bereits geschehen ist. Tatsächlich ist es ein eher gängiges Programmierverfahren, dieses Feature zu nutzen und **wspclosesocket** zu verwenden, um die Shutdown-Sequenz zu initiieren und das Sockethandle freizugeben.

Um diese Verwendung zu vereinfachen, stellt die Sockets-Schnittstelle Steuerelemente über den socketoptions-Mechanismus bereit, mit dem der Programmierer angeben kann, ob die implizite Beendigungs Sequenz ordnungsgemäß oder abgebrochen werden soll, und ob die Funktion nicht sofort beendet werden soll, um Zeit für eine ordnungsgemäße Herunterfahr Sequenz zuzulassen.

Wenn Sie geeignete Werte für die Socketoptionen für " \_ LINGER" und " \_ DontLinger" festlegen, können die folgenden Verhaltenstypen mit der [**wspclosesocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) -Funktion abgerufen werden.

-   Abgebrochenen Shutdown-Sequenz, sofortige Rückgabe von [**wspclosesocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)).
-   Ordnungsgemäßes Herunterfahren, verzögertes beenden, bis das Herunterfahren entweder abgeschlossen oder ein angegebenes Zeitintervall abläuft Wenn das Zeitintervall abläuft, bevor die ordnungsgemäße Herunterfahr Sequenz abgeschlossen ist, tritt eine Abbruch Sequenz auf, und [**wspclosesocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) gibt zurück.
-   Ordnungsgemäßes Herunterfahren, sofortige Rückgabe, und zulassen, dass die Shutdown-Sequenz im Hintergrund ausgeführt wird. Dies ist das Standardverhalten. Beachten Sie jedoch, dass die Anwendung nicht wissen kann, wann (oder ob) die ordnungsgemäße Herunterfahr Sequenz abgeschlossen ist.

Eine Technik, die verwendet werden kann, um die Wahrscheinlichkeit zu minimieren, dass Probleme während der Verbindungs Löschung auftreten, besteht nicht darin, dass ein implizites Herunterfahren von [**wspclosesocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))initiiert wird. Stattdessen wird eine der beiden expliziten Shutdown-Funktionen ([**wspshutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) oder [**wspsenddisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85))) verwendet. Dies führt wiederum dazu \_ , dass die Peer Anwendung eine Bestätigung der Bestätigung von FD erhält, die anzeigt, dass alle ausstehenden Daten empfangen wurden. Um dies zu veranschaulichen, zeigt die folgende Tabelle die Funktionen, die von den Client-und Serverkomponenten einer Anwendung aufgerufen werden, wobei der Client dafür verantwortlich ist, ein ordnungsgemäßes Herunterfahren zu initiieren.

| Clientseitig                                                                                                                         | Serverseitig                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| (1) ruft [**wspshutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) (*s*, SD \_ Send) auf, um das Ende der Sitzung zu signalisieren, und der Client hat keine weiteren Daten, die gesendet werden können. |                                                                                                              |
|                                                                                                                                     | (2) empfängt FD, was bedeutet, dass ein ordnungsgemäßes Herunterfahren ausgeführt \_ wird und alle Daten empfangen wurden.        |
|                                                                                                                                     | (3) sendet alle verbleibenden Antwortdaten.                                                                       |
| (5 ') ruft \_ den FD-Lese-und-Aufruf von empfangener ab, um vom Server gesendete Antwortdaten zu erhalten.                                                         | (4) ruft [**wspshutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85))(*s*, SD \_ Send) auf, um anzugeben, dass der Server keine Daten mehr enthält, die gesendet werden sollen. |
| (5) empfängt die \_ Bestätigung von FD.                                                                                                  | (4 ') ruft [ **wspclosesocket** auf](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                      |
| (6) ruft [ **wspclosesocket** auf.](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                              |                                                                                                              |



 

Die Zeit Steuerungs Sequenz wird von Schritt (1) zu Schritt (6) zwischen dem Client und dem Server verwaltet. mit Ausnahme der Schritte (4 ') und (5 '), die nur die lokale zeitliche Steuerung aufweisen, wenn Schritt (5) den Schritt (5 ') auf der Clientseite befolgt, während Step (4 ') auf der Serverseite auf den Schritt (4) folgt, ohne zeitliche Beziehungs Beziehung mit der Remote Partei.

 

 
