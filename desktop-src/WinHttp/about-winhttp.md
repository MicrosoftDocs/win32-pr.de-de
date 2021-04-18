---
description: Die Microsoft Windows HTTP-Dienste (WinHTTP) bieten eine vom Server unterstützte, übergeordnete Oberfläche für die http/2-und 1,1-Internet Protokolle.
ms.assetid: 8337f699-3ec0-4397-acc2-6dc813f7542d
title: Informationen zu WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150c829410a1601a3ede7f115f4594276af7fead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347683"
---
# <a name="about-winhttp"></a>Informationen zu WinHTTP

> [!NOTE]
> Für App-Container und Systemdienste seit Windows 10, Version 1709, ist http/2 (siehe [RFC7540](https://tools.ietf.org/html/rfc7540)) standardmäßig aktiviert.

Die Microsoft Windows HTTP-Dienste (WinHTTP) bieten eine vom Server unterstützte, übergeordnete Oberfläche für die http/2-und 1,1-Internet Protokolle. WinHTTP wurde für Server Anwendungen, die mit HTTP-Servern kommunizieren, hauptsächlich in serverbasierten Szenarien verwendet.

[WinInet](/windows/desktop/WinInet/portal) wurde als HTTP-Client Plattform für interaktive Desktop Anwendungen konzipiert. WinInet zeigt eine Benutzeroberfläche für einige Vorgänge an, z. b. das Sammeln von Benutzer Anmelde Informationen. WinHTTP verarbeitet diese Vorgänge jedoch Programm gesteuert. Für Server Anwendungen, die HTTP-Client Dienste erfordern, sollte WinHTTP anstelle von WinInet verwendet werden. Weitere Informationen finden Sie unter [Portieren von WinINet-Anwendungen in WinHTTP](porting-wininet-applications-to-winhttp.md).

WinHTTP ist auch für die Verwendung in System Diensten und http-basierten Client Anwendungen konzipiert. Bei Anwendungen mit nur einem Benutzer, die FTP-Protokollfunktionen, die cookiepersistenz, das Caching, die automatische Handhabung von Anmelde Informationen, die Internet Explorer-Kompatibilität oder die Unterstützung für unterstützte Plattformen benötigen, [sollten Sie die](/windows/desktop/WinInet/portal)Verwendung von

Auf diese Schnittstelle kann über C/C++ über die WinHTTP-API (Application Programming Interface) oder über die [**iwinhttprequest**](iwinhttprequest-interface.md) -Schnittstelle und die [**iwinhttprequestevents**](iwinhttprequestevents-interface.md) -Schnittstelle zugegriffen werden. Auf WinHTTP kann auch von Skript-und Microsoft-Visual Basic über das WinHTTP-Objekt zugegriffen werden. Weitere Informationen und Beschreibungen der einzelnen Funktionen finden Sie in der Referenz zu WinHTTP-Funktionen für die jeweilige Sprache.

Ab Windows 8 bietet WinHTTP APIs zum Aktivieren von Verbindungen mit dem [WebSocket-Protokoll](https://tools.ietf.org/html/rfc6455)l, z. b. [**winhttpwebsocketsend**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend) und [**winhttpwebsocketreceive**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive).

> [!Caution]  
> WinHTTP ist nicht Wiedereintritts fähig, außer während des asynchronen Abschluss Rückrufs. Das heißt, während ein Thread einen Aufruf aussteht, der für eine der WinHTTP-Funktionen, wie z. b. WinHttpSendRequest, WinHttpReceiveResponse, winhttpquerydataavailable, winhttpsenddata oder winhttpschreitedata, aussteht, darf er nie ein zweites Mal aufgerufen werden Ein zweiter Aufruf könnte beispielsweise folgendermaßen aussehen: Wenn eine Anwendung einen asynchronen Prozedur Aufruf (APC) zu dem Thread in die Warteschlange einreiht, der WinHTTP aufruft, und wenn WinHTTP eine Warn Tabelle intern wartet, kann APC ausgeführt werden. Wenn die APC-Routine auch zum Aufrufen von WinHTTP durchgeführt wird, wird die WinHTTP-API wieder eingegeben, und der interne Zustand von WinHTTP kann beschädigt werden.

## <a name="winhttp-51-features"></a>WinHTTP 5,1-Features

Die folgenden Features wurden in Version 5,1 von WinHTTP hinzugefügt:

-   IPv6-Unterstützung.
-   AutoProxy-Funktionen.
-   HTTP/1.0-Protokoll einschließlich Unterstützung für Keep-Alive-Verbindungen (persistente Verbindungen) und Sitzungs Cookies.
-   Unterstützung für HTTP/1.1-Unterstützung für HTTP-Antworten.
-   Keep-Alive-Pooling anonymer Verbindungen über Sitzungen hinweg.
-   Secure Sockets Layer (SSL)-Funktionalität, einschließlich der Client Zertifikate. Folgende SSL-Protokolle werden unterstützt: SSL 2,0, SSL 3,0 und Transport Layer Security (TLS) 1,0.
-   Unterstützung für die Server-und Proxy Authentifizierung, einschließlich integrierter Unterstützung für Microsoft Passport 1,4 und das Aushandeln/ [Kerberos](../com/kerberos-v5-protocol.md) -Paket.
-   Automatische Verarbeitung von Umleitungen, sofern diese nicht unterdrückt werden.
-   Skript fähige Schnittstelle zusätzlich zur API.
-   Ablauf Verfolgungs Hilfsprogramm zum Beheben von Problemen.

Eine Reihe von [WinInet](/windows/desktop/WinInet/portal) -Funktionen werden in WinHTTP nicht unterstützt, einschließlich URL-Zwischenspeicherung und persistente Cookies, AutoProxy, automatische Unterstützung, Offline Unterstützung und File Transfer Protocol (FTP).

Weitere Informationen zu den Änderungen, die in Version 5,1 eingeführt wurden, finden Sie unter [What es New in WinHTTP 5,1](what-s-new-in-winhttp-5-1.md).

## <a name="getting-started-with-winhttp"></a>Einstieg in WinHTTP

Weitere Informationen zu WinHTTP finden Sie in den folgenden Themen.

* [WinInet und WinHTTP](/windows/desktop/wininet/wininet-vs-winhttp) vergleicht die beiden Technologien für den Zugriff auf http.
* [WinHTTP-Versionen](winhttp-versions.md) beschreiben den Versionsverlauf von WinHTTP.
* [Neues in WinHTTP 5,1](what-s-new-in-winhttp-5-1.md) beschreibt Änderungen und neue Features in WinHTTP 5,1.
* In der [Netzwerkterminologie](network-terminology.md) werden nützliche Konzepte und Terminologie im Zusammenhang mit Netzwerken im allgemeinen und insbesondere das HTTP-Protokoll beschrieben.
* Bei der [Auswahl einer WinHTTP-Schnittstelle](choosing-a-winhttp-interface.md) werden die C/C++-API und die COM-Schnittstelle für WinHTTP beschrieben.
* [WinHTTP-Sicherheitsüberlegungen](winhttp-security-considerations.md) beschreiben Sicherheitsprobleme, die bei der Verwendung von WinHTTP zu beachten sind.
* [Portieren von WinINet-Anwendungen auf WinHTTP](porting-wininet-applications-to-winhttp.md) : Beschreibt, wie Sie Ihre vorhandenen [WinInet](/windows/desktop/WinInet/portal) -Anwendungen so ändern, dass die WinHTTP-API verwendet wird.
