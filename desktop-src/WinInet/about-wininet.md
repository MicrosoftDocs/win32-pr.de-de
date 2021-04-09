---
title: Informationen zu WinInet
description: Mit der Windows Internet (WinInet) Application Programming Interface (API) kann Ihre Anwendung mit FTP-und HTTP-Protokollen interagieren, um auf Internet Ressourcen zuzugreifen.
ms.assetid: 0a06f2af-957a-4dff-a8cc-187370181b5c
keywords:
- Informationen zu WinInet WinInet
- WinInet WinInet, Informationen zu
- WinInet WinInet, Startseite
- Windows Internet Wininet
- Internet, Windows Internet Wininet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4513e5c3912a483fd4dbef96f452c5712717c8a5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "103948470"
---
# <a name="about-wininet"></a>Informationen zu WinInet

> [!NOTE]
> Für App-Container seit Windows 10, Version 1709, ist http/2 (siehe [RFC7540](https://tools.ietf.org/html/rfc7540)) standardmäßig aktiviert.

Mit der Windows Internet (WinInet) Application Programming Interface (API) kann Ihre Anwendung mit FTP-und HTTP-Protokollen interagieren, um auf Internet Ressourcen zuzugreifen. Bei der Weiterentwicklung von Standards behandeln diese Funktionen die Änderungen in den zugrunde liegenden Protokollen, sodass Sie konsistentes Verhalten gewährleisten können.

**Windows XP und Windows Server 2003 R2 und früher:** Auch aktivierte Anwendungen können mit Gopher interagieren.

Weitere Informationen finden Sie unter

-   [WinInet im Vergleich zu WinHTTP](wininet-vs-winhttp.md)
-   [HINTERNET-Handles](appendix-a-hinternet-handles.md)
-   [Unterstützung von IP-Version 6](ip-version-6-support.md)
-   [Inhalts \_ Codierung](content-encoding.md)
-   [Zwischenspeichern](caching.md)
-   [Allgemeine Funktionen](common-functions.md)
-   [FTP-Sitzungen](ftp-sessions.md)
-   [HTTP-Sitzungen](http-sessions.md)
-   [HTTP-Cookies](http-cookies.md)
-   [Asynchroner Vorgang](asynchronous-operation.md)
-   [Behandeln der Authentifizierung](handling-authentication.md)
-   [Behandeln von Uniform Resource Locators](handling-uniform-resource-locators.md)
-   [Sicherheits \_ Richtlinie](security-guidelines.md)

## <a name="internet-protocols"></a>Internet Protokolle

Die beiden primären Internet Protokolle sind FTP und http. Weitere Informationen zu diesen Protokollen finden Sie in den RFC-Dokumenten (Request for Comments) für FTP und http:

-   [RFC 959](https://www.ietf.org/rfc/rfc0959.txt), *File Transfer Protocol (FTP)*.
-   [RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt), *Hypertext Transfer Protocol-HTTP/1.0*.
-   [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), *Hypertext Transfer Protocol-HTTP/1.1*.

> [!NOTE]  
> (Diese Ressourcen sind in einigen Sprachen und Ländern möglicherweise nicht verfügbar.)

**Windows XP und Windows Server 2003 R2 und früher:** Das Gopher-Protokoll wurde ebenfalls unterstützt. Weitere Informationen finden Sie unter [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt), *dem Internet Gopher-Protokoll*.
