---
title: Informationen zu WinINet
description: Die Windows Internet (WinINet) Application Programming Interface (API) ermöglicht Es Ihrer Anwendung, mit FTP- und HTTP-Protokollen zu interagieren, um auf Internetressourcen zuzugreifen.
ms.assetid: 0a06f2af-957a-4dff-a8cc-187370181b5c
keywords:
- Informationen zu WinINet WinINet
- WinINet WinINet , Informationen
- WinINet WinINet , Startseite
- Windows Internet WinINet
- Internet, Windows Internet WinINet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be38840c33735a1e064e9bdc5e044651130d6e15a6fe22d004a2e8d7c29bf140
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051868"
---
# <a name="about-wininet"></a>Informationen zu WinINet

> [!NOTE]
> Für App-Container seit Windows 10, Version 1709, IST HTTP/2 (siehe [RFC7540](https://tools.ietf.org/html/rfc7540)) standardmäßig aktiviert.

Die Windows Internet (WinINet) Application Programming Interface (API) ermöglicht Es Ihrer Anwendung, mit FTP- und HTTP-Protokollen zu interagieren, um auf Internetressourcen zuzugreifen. Mit der Weiterentwicklung von Standards verarbeiten diese Funktionen die Änderungen in den zugrunde liegenden Protokollen, sodass sie ein konsistentes Verhalten aufrechterhalten können.

**Windows XP und Windows Server 2003 R2 und früher:** Außerdem können Anwendungen mit Gopher interagieren.

Weitere Informationen finden Sie unter

-   [WinINet im Vergleich zu WinHTTP](wininet-vs-winhttp.md)
-   [HINTERNET-Handles](appendix-a-hinternet-handles.md)
-   [UNTERSTÜTZUNG FÜR IP-Version 6](ip-version-6-support.md)
-   [\_Inhaltscodierung](content-encoding.md)
-   [Zwischenspeichern](caching.md)
-   [Allgemeine Funktionen](common-functions.md)
-   [FTP-Sitzungen](ftp-sessions.md)
-   [HTTP-Sitzungen](http-sessions.md)
-   [HTTP-Cookies](http-cookies.md)
-   [Asynchroner Vorgang](asynchronous-operation.md)
-   [Behandeln der Authentifizierung](handling-authentication.md)
-   [Behandeln von einheitlichen Ressourcenlocators](handling-uniform-resource-locators.md)
-   [\_Sicherheitsrichtlinie](security-guidelines.md)

## <a name="internet-protocols"></a>Internetprotokolle

Die beiden primären Internetprotokolle sind FTP und HTTP. Weitere Informationen zu diesen Protokollen finden Sie in den RFC-Dokumenten (Request For Comments) für FTP und HTTP:

-   [RFC 959](https://www.ietf.org/rfc/rfc0959.txt) *, File Transfer Protocol (FTP)*.
-   [RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt), *Hypertext Transfer Protocol – HTTP/1.0*.
-   [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), *Hypertext Transfer Protocol – HTTP/1.1*.

> [!NOTE]  
> (Diese Ressourcen sind in einigen Sprachen und Ländern möglicherweise nicht verfügbar.)

**Windows XP und Windows Server 2003 R2 und früher:** Das Gopher-Protokoll wurde ebenfalls unterstützt. Siehe [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt), *The Internet Gopher Protocol*.
