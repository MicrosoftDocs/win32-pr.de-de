---
title: Client-/Serveranwendungsrichtlinien
description: Client-/Serveranwendungen dürfen nicht davon ausgehen, dass eine einzelne Computerverbindung einer einzelnen Benutzersitzung entspricht.
ms.assetid: 69822ef1-eca8-4302-b014-8e5894d52109
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 234d27f5bd024e2311307f39e4f86584747b59b874576e5cd5aa28e735b2945d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001618"
---
# <a name="clientserver-application-guidelines"></a>Client-/Serveranwendungsrichtlinien

Client-/Serveranwendungen dürfen nicht davon ausgehen, dass eine einzelne Computerverbindung einer einzelnen Benutzersitzung entspricht. Dies ist ein Sonderfall des Problems, das unter [IP-Adressen und Computernamen](ip-addresses-and-computer-names.md)erläutert wird.

Um eine Client-/Serververbindung eindeutig zu identifizieren, muss jedes Clientmodul einen eindeutigen Namen oder Bezeichner verwenden. Anwendungen können benannte Objekte oder Pipes, Sockets oder andere IPC-Methoden verwenden. Weitere Informationen finden Sie unter [Kernelobjektnamespaces.](kernel-object-namespaces.md)

Um Remotedesktopdienste kompatibel zu sein, muss das Servermodul in einer Client-/Serveranwendung mehrere Clients verarbeiten können, die eine Verbindung vom gleichen Computer herstellen. Hierzu muss das Servermodul Clientverbindungen über eine klar definierte globale Schnittstelle wie RPC oder Named Pipes akzeptieren. Server und Client müssen für jede Benutzersitzung einen anderen Kommunikationskanal aushandeln. Der Client muss eine Verbindung mit dem Server herstellen, indem Protokolle verwendet werden, die diese Art von Vorgang problemlos unterstützen, z. B. TCP/IP, wobei für jede Clientanwendung eine andere Socketverbindung verwendet werden kann.

Das Clientmodul kann die [**ProcessIdToSessionId-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) aufrufen, um den Bezeichner der Remotedesktopdienste Sitzung abzurufen. Der Client verwendet dann eine Form der prozessübergreifenden Kommunikation, um seinen Sitzungsbezeichner an das Servermodul zu übergeben. Die Client- und Servermodule können dann den Sitzungsbezeichner verwenden, um einen privaten Kommunikationskanal einzurichten. Beispielsweise kann das Servermodul einen Sitzungsbezeichner verwenden, um auf Objekte im Namespace der Sitzung für Kernelobjekte zuzugreifen.

Darüber hinaus kann das Servermodul den Sitzungsbezeichner in einem [**WTSQuerySessionInformation-Aufruf**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) verwenden, um zusätzliche Informationen zum Client abzurufen. Das Servermodul kann auch den Sitzungsbezeichner in einem [**WTSSendMessage-Aufruf**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea) verwenden, um eine Nachricht im Clientterminal anzuzeigen. Das Servermodul kann auch zwei Ereignisse erstellen, um die Clientverbindung mit einer Sitzung zu überwachen und die Verbindung mit einer Sitzung zu trennen. Sie muss jedoch auf dem server Remotedesktop-Sitzungshost (RD-Sitzungshost) registriert werden, um dies zu tun. Weitere Informationen finden Sie unter [Überwachen von Sitzungsverbindungen und Trennen von Verbindungen.](monitoring-session-connections-and-disconnections.md)

Eingabeaufforderungen sind eine potenzielle Ursache für Probleme bei Client-/Serveranwendungen. Wenn beispielsweise ein Dienst die [**MessageBox-Funktion**](/windows/desktop/api/winuser/nf-winuser-messagebox) aufruft, wird das Meldungsfeld auf dem Desktop des RD-Sitzungshost-Servers und nicht auf dem Clientdesktop angezeigt. Um eine Nachricht auf einem Clientdesktop anzuzeigen, kann der Dienst die [**WtsSendMessage-Funktion**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea) aufrufen. Alternativ kann der Dienst Eingaben vom Clientmodul anfordern, und das Clientmodul kann die Benutzeroberfläche anzeigen und die resultierende Eingabe an den Dienst zurücksenden.

Prozesse, die aus mehreren Sitzungen entstehen, können Daten über freigegebene Speicherblöcke aneinander senden und voneinander empfangen. Weitere Informationen finden Sie unter [Creating Named Shared Memory](/windows/desktop/Memory/creating-named-shared-memory). Freigegebener Arbeitsspeicher kann unter den folgenden Bedingungen nicht verwendet werden:

-   Die Prozesse, die den Shared Memory-Block verwenden, wurden von mehreren Sitzungen ausgelöst.
-   Die Sitzungen verwenden die gleichen Anmeldeinformationen für die Benutzerauthentifizierung.

 

 