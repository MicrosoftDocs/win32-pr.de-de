---
description: Microsoft Windows HTTP Services (WinHTTP) bietet Ihnen eine servergestützte, high-level-Schnittstelle zu den Http/2- und 1.1-Internetprotokollen.
ms.assetid: 8337f699-3ec0-4397-acc2-6dc813f7542d
title: Informationen zu WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19df8ac8073cfca4fd74fd5d024712cc3fc59c770c3d9ad0ab1386bc0642d72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570290"
---
# <a name="about-winhttp"></a>Informationen zu WinHTTP

> [!NOTE]
> Für App-Container und Systemdienste Windows 10 Version 1709 ist HTTP/2 (siehe [RFC7540)](https://tools.ietf.org/html/rfc7540)standardmäßig aktiviert.

Microsoft Windows HTTP Services (WinHTTP) bietet Ihnen eine servergestützte, high-level-Schnittstelle zu den Http/2- und 1.1-Internetprotokollen. WinHTTP ist für die Verwendung in erster Linie in serverbasierten Szenarien durch Serveranwendungen konzipiert, die mit HTTP-Servern kommunizieren.

[WinINet](/windows/desktop/WinInet/portal) wurde als HTTP-Clientplattform für interaktive Desktopanwendungen entwickelt. WinINet zeigt eine Benutzeroberfläche für einige Vorgänge an, z. B. das Sammeln von Benutzeranmeldeinformationen. WinHTTP verarbeitet diese Vorgänge jedoch programmgesteuert. Serveranwendungen, die HTTP-Clientdienste erfordern, sollten WinHTTP anstelle von WinINet verwenden. Weitere Informationen finden Sie unter [Portieren von WinINet-Anwendungen zu WinHTTP.](porting-wininet-applications-to-winhttp.md)

WinHTTP ist auch für die Verwendung in Systemdiensten und HTTP-basierten Clientanwendungen konzipiert. Anwendungen mit nur einem Benutzer, die FTP-Protokollfunktionen, Cookiepersistenz, Zwischenspeicherung, automatische Dialogbehandlung für Anmeldeinformationen, Internet Explorer-Kompatibilität oder Plattformunterstützung auf downlevelr Ebene erfordern, sollten jedoch die Verwendung von [WinINet in](/windows/desktop/WinInet/portal)Betracht ziehen.

Auf diese Schnittstelle kann über C/C++ entweder über die WinHTTP-Anwendungsprogrammierschnittstelle (APPLICATION Programming Interface, API) oder über die [**Schnittstellen IWinHttpRequest**](iwinhttprequest-interface.md) und [**IWinHttpRequestEvents zugegriffen**](iwinhttprequestevents-interface.md) werden. Auf WinHTTP kann auch über Skripts und Microsoft Visual Basic WinHTTP-Objekt zugegriffen werden. Weitere Informationen und Beschreibungen der einzelnen Funktionen finden Sie in der WinHTTP-Funktionsreferenz für die spezifische Sprache.

Ab Windows 8 stellt WinHTTP APIs zum Aktivieren von Verbindungen mithilfe des [WebSocket-Protokolls](https://tools.ietf.org/html/rfc6455)l zur Verfügung, z. B. [**WinHttpWebSocketSend**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend) und [**WinHttpWebSocketReceive.**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)

> [!Caution]  
> WinHTTP ist nur während des asynchronen Abschlussrückrufs ein reentrant. Das heißt, während für einen Thread ein Aufruf an eine der WinHTTP-Funktionen wie WinHttpSendRequest, WinHttpReceiveResponse, WinHttpQueryDataAvailable, WinHttpSendData oder WinHttpWriteData aussteht, darf winHTTP erst ein zweites Mal aufgerufen werden, wenn der erste Aufruf abgeschlossen ist. Ein Szenario, in dem ein zweiter Aufruf erfolgen kann, ist wie folgt: Wenn eine Anwendung einen asynchronen Prozeduraufruf (APC) in die Warteschlange des Threads einreiht, der WinHTTP aufruft, und wenn WinHTTP intern eine wartbare Wartezeit ausführt, kann der APC ausgeführt werden. Wenn die APC-Routine auch WinHTTP aufruft, wird die WinHTTP-API erneut ein- und der interne Zustand von WinHTTP kann beschädigt werden.

## <a name="winhttp-51-features"></a>WinHTTP 5.1-Features

Die folgenden Features wurden in Version 5.1 von WinHTTP hinzugefügt:

-   IPv6-Unterstützung.
-   AutoProxy-Funktionen.
-   HTTP/1.0-Protokoll, einschließlich Unterstützung für Keep-Alive-Verbindungen (persistente) Verbindungen und Sitzungscookies.
-   Http/1.1-Unterstützung für die blockierte Übertragung von HTTP-Antworten.
-   Sitzungsübergreifendes Keep-Alive-Pooling anonymer Verbindungen.
-   Secure Sockets Layer (SSL), einschließlich Clientzertifikaten. Folgende SSL-Protokolle werden unterstützt: SSL 2.0, SSL 3.0 und Transport Layer Security (TLS) 1.0.
-   Unterstützung der Server- und Proxyauthentifizierung, einschließlich integrierter Unterstützung für Microsoft Passport 1.4 und das [Negotiate/Kerberos-Paket.](../com/kerberos-v5-protocol.md)
-   Automatische Behandlung von Umleitungen, sofern nicht unterdrückt.
-   Skriptfähige Schnittstelle zusätzlich zur API.
-   Ablaufverfolgungs-Hilfsprogramm zur Problembehandlung.

Eine Reihe von [WinINet-Features](/windows/desktop/WinInet/portal) werden in WinHTTP nicht unterstützt, einschließlich URL-Zwischenspeicherung und persistenter Cookies, autoproxy, autodialing, Offlineunterstützung und File Transfer Protocol (FTP).

Weitere Informationen zu Änderungen, die in Version 5.1 eingeführt wurden, finden Sie unter [Neuerungen in WinHTTP 5.1.](what-s-new-in-winhttp-5-1.md)

## <a name="getting-started-with-winhttp"></a>Erste Schritte mit WinHTTP

Weitere Informationen zu WinHTTP finden Sie in den folgenden Themen.

* [WinINet und WinHTTP vergleichen](/windows/desktop/wininet/wininet-vs-winhttp) die beiden Technologien für den Zugriff auf HTTP.
* [WinHTTP-Versionen](winhttp-versions.md) beschreibt den Versionsverlauf von WinHTTP.
* [Neuerungen in WinHTTP 5.1](what-s-new-in-winhttp-5-1.md) beschreibt Änderungen und neue Features in WinHTTP 5.1.
* [Die Netzwerkterminologie](network-terminology.md) beschreibt nützliche Konzepte und Terminologie im Zusammenhang mit Netzwerken im Allgemeinen und dem HTTP-Protokoll im Besonderen.
* [Wenn Sie eine WinHTTP-Schnittstelle auswählen,](choosing-a-winhttp-interface.md) werden die C/C++-API und die COM-Schnittstelle für WinHTTP beschrieben.
* [In den Überlegungen zur WinHTTP-Sicherheit](winhttp-security-considerations.md) werden Sicherheitsprobleme beschrieben, die bei der Verwendung von WinHTTP berücksichtigt werden müssen.
* [Unter Portieren von WinINet-Anwendungen zu WinHTTP wird](porting-wininet-applications-to-winhttp.md) beschrieben, wie Sie Ihre vorhandenen [WinINet-Anwendungen](/windows/desktop/WinInet/portal) so ändern, dass sie die WinHTTP-API verwenden.
