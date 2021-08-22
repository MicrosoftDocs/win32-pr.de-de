---
title: Inhaltscodierung
description: Ab Windows Server 2008 und Windows Vista kann die Anwendung WinINet an die Durchführung der Inhaltsdecodierung für die GZIP- und Deflate-Inhaltscodierungsschemas weiterveransenden.
ms.assetid: 136f22a6-e5ca-41c5-8651-6e132655d268
keywords:
- Inhaltscodierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1a91120e4ea01c4636c8d9942e968a0d69aeed50b6a037b31aa0241f3e933c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132883"
---
# <a name="content-encoding"></a>Inhaltscodierung

Wie im HTTP-Protokoll (RFC 2616) angegeben, können Anwendungen anfordern, dass der Server HTTP-Antworten im codierten Format zurück gibt. Vor Windows Server 2008 und Windows Vista wurden Anforderungen mit Inhaltscodierung zur Verarbeitung auf ihrer Ebene an die Anwendung gesendet. Ab Windows Server 2008 und Windows Vista kann die Anwendung WinINet an die Durchführung der Inhaltsdecodierung für die GZIP- und Deflate-Inhaltscodierungsschemas weiterveransenden.

Um die Inhaltsdecodierung zu aktivieren, legt die Anwendung die Decodierungsoption fest, mit der WinINet die Decodierung in ihrem Namen anfing. Durch die Aktivierung der Decodierung wird jedoch nicht garantiert, dass WinINet die Inhaltsdecodierung durchführen wird, und die Anwendung sollte für die Decodierung vorbereitet sein. WinINet entfernt den Inhaltscodierungsheader aus der Antwort, wenn die Inhaltsdecodierung erfolgreich ausgeführt wird. Von Anwendungen wird erwartet, dass sie die Inhaltsdecodierung unabhängig davon verarbeiten, ob die Decodierungsoption aktiviert oder deaktiviert ist, wenn der Inhaltscodierungsheader in der Antwort vorhanden ist.

Wenn die Decodierung aktiviert ist, muss die Anwendung die Liste der unterstützten Codierungen im Accept-Encoding der Anforderung angeben. Der Accept-Encoding-Header erfing den Server jedoch nicht, eine codierte Antwort zu senden. WinINet sendet Antworten, die nicht mit der Liste der zulässigen Codierungen übereinstimmen, zurück an die Anwendung.

In der folgenden Liste werden die Bedingungen beschrieben, unter denen WinINet die Inhaltsdecodierung durchführen wird, wenn die Option aktiviert ist:

-   Der Accept-Encoding-Header muss in der Anforderung vorhanden sein und die Codierungsschemas gzip, deflate oder gzip und deflate angeben.
-   Das im Content-Encoding-Header angegebene Codierungsschema muss mit einem der im Accept-Encoding angegebenen Codierungsschemas übereinstimmen.
-   Der Content-Encoding-Header in der Antwort gibt nur ein Codierungsschema an.
-   Die Antwort darf nur einen Content-Encoding-Header enthalten. WinINet decodiert Inhalte, die mit nur einem Codierungsschema codiert sind.
-   Der Cache-Control darf nicht die No-Transform-Direktive enthalten.
-   Der Content-Range-Header darf in der Antwort nicht vorhanden sein.

## <a name="setting-the-decompression-option"></a>Festlegen der Dekomprimierungsoption

Die Decodierungsoption kann für das Sitzungshand handle, das Anforderungshand handle oder das Verbindungshandy festgelegt werden. Das Handle, für das die Decodierungsoption festgelegt ist, definiert den Bereich der Decodierungsoption. Wenn Sie beispielsweise die Decodierung für die Sitzung festlegen, wird das Decodieren aller Verbindungen und Anforderungen ermöglicht, die unter diesem Handle erstellt wurden.

Zum Festlegen der Decodierungsoption ruft die Anwendung [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) mit dem von [**InternetOpen,**](/windows/desktop/api/Wininet/nf-wininet-internetopena) [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)oder [**HttpOpenRequest zurückgegebenen Handle auf.**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) Die **OPTION INTERNET OPTION HTTP \_ \_ \_ DECODING** wird im *dwOption-Parameter* angegeben, und der *lpBuffer-Parameter* zeigt auf eine boolesche Variable, die auf TRUE festgelegt ist. Um die Decodierung zu deaktivieren, ruft die Anwendung **InternetSetOption** mit der **OPTION INTERNET OPTION HTTP \_ \_ \_ DECODING** auf, und die boolesche Variable ist auf FALSE festgelegt.

Wenn die Decodierungsoption festgelegt ist, führt WinINet eine Decodierung für die Anforderung durch, wenn die [**Anwendung InternetReadFile aufruft.**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) Wenn WinINet bei der Inhaltsdecodierung einen Fehler auft, schlägt der Aufruf von **InternetReadFile** mit dem Fehler **\_ INTERNET \_ DECODING \_ FAILED fehl.** Wenn die Decodierung fehlschlägt, hat die Anwendung zwei Optionen: Sie kann den Accept-Encoding-Header entfernen und die Anforderung erneut senden, oder sie kann die **OPTION INTERNET OPTION HTTP \_ \_ \_ DECODING** für die Anforderung auf FALSE festlegen und die Anforderung dann erneut senden. Wenn die Decodierungsoption auf FALSE festgelegt ist, muss die Anwendung den Content-Encoding-Header überprüfen und alle Decodierungen auf Anwendungsebene durchführen.

> [!Note]  
> WinINet unterstützt keine Serverimplementierung. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP Services (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 