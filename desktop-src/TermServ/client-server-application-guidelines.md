---
title: Richtlinien für Client/Server-Anwendungen
description: Client/Server-Anwendungen dürfen nicht davon ausgehen, dass eine einzelne Computerverbindung einer einzelnen Benutzersitzung entspricht.
ms.assetid: 69822ef1-eca8-4302-b014-8e5894d52109
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd0c1a71256f3ab469bfeb1c08b2d096b56ac1b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338266"
---
# <a name="clientserver-application-guidelines"></a>Richtlinien für Client/Server-Anwendungen

Client/Server-Anwendungen dürfen nicht davon ausgehen, dass eine einzelne Computerverbindung einer einzelnen Benutzersitzung entspricht. Dies ist ein Sonderfall des in [IP-Adressen und Computer Namen](ip-addresses-and-computer-names.md)behandelten Problems.

Zum eindeutigen Identifizieren einer Client/Server-Verbindung muss jedes Client Modul einen eindeutigen Namen oder Bezeichner verwenden. Anwendungen können benannte Objekte oder Pipes, Sockets oder andere IPC-Methoden verwenden. Weitere Informationen finden Sie unter [Kernel Object Namespaces](kernel-object-namespaces.md).

Um Remotedesktopdienste kompatibel zu sein, muss das Servermodul in einer Client/Server-Anwendung in der Lage sein, mehrere Clients zu verarbeiten, die eine Verbindung über denselben Computer herstellen. Um dies zu erreichen, muss das Servermodul Clientverbindungen über eine klar definierte globale Schnittstelle (z. b. RPC oder Named Pipes) akzeptieren. Der Server und der Client müssen für jede Benutzersitzung einen anderen Kommunikationskanal aushandeln. Der Client muss eine Verbindung mit dem Server herstellen, indem er Protokolle verwendet, die diese Art von Vorgang (z. b. TCP/IP) problemlos unterstützen, wobei eine andere Socketverbindung für jede Client Anwendung verwendet werden kann.

Das Client Modul kann die [**processidtosessionid**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) -Funktion aufrufen, um den Bezeichner der Remotedesktopdienste Sitzung abzurufen. Der Client verwendet dann eine Form der prozessübergreifenden Kommunikation, um die Sitzungs-ID an das Servermodul zu übergeben. Die Client-und Server Module können dann den Sitzungs Bezeichner verwenden, um einen privaten Kommunikationskanal einzurichten. Das Servermodul kann z. b. einen Sitzungs Bezeichner verwenden, um auf Objekte im Namespace der Sitzung für Kernel Objekte zuzugreifen.

Außerdem kann das Servermodul die Sitzungs-ID in einem [**wzquerysessioninformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) -Befehl verwenden, um zusätzliche Informationen über den Client abzurufen. Das Servermodul kann auch die Sitzungs-ID in einem [**wtssendmessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea) -Befehl verwenden, um eine Meldung auf dem Client Terminal anzuzeigen. Das Servermodul kann auch zwei Ereignisse erstellen, um die Client Verbindung mit einer Sitzung zu überwachen und die Verbindung zu trennen. Dies muss jedoch auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) registriert werden. Weitere Informationen finden Sie unter über [Wachen von Sitzungs Verbindungen und Trennungen](monitoring-session-connections-and-disconnections.md).

Eingabe Aufforderungen für Benutzereingaben sind eine potenzielle Ursache für Probleme bei Client-/Server-Anwendungen. Wenn ein Dienst z. b. die [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) -Funktion aufruft, wird das Meldungs Feld auf dem Desktop des RD-Sitzungshost Servers und nicht auf dem Client Desktop angezeigt. Der Dienst kann die [**wtssendmessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea) -Funktion aufrufen, um eine Meldung auf einem Client Desktop anzuzeigen. Alternativ kann der Dienst Eingaben vom Client Modul anfordern, und das Client Modul kann die Benutzeroberfläche anzeigen und die resultierende Eingabe an den Dienst zurücksenden.

Prozesse, die aus mehreren Sitzungen erzeugt werden, können Daten über freigegebene Speicherblöcke an Daten senden und von Ihnen empfangen. Weitere Informationen finden Sie unter [Erstellen von benannten freigegebenen Arbeitsspeicher](/windows/desktop/Memory/creating-named-shared-memory). Shared Memory kann unter den folgenden Bedingungen nicht verwendet werden:

-   Die Prozesse, die den freigegebenen Speicherblock verwenden, wurden von mehreren Sitzungen erzeugt.
-   Die Sitzungen verwenden dieselben Anmelde Informationen für die Benutzerauthentifizierung.

 

 