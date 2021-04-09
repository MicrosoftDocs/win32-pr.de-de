---
title: Inhaltscodierung
description: Ab Windows Server 2008 und Windows Vista kann die Anwendung WinInet zum Durchführen der Decodierung von Inhalten für die GZIP-Datei und zum deflate von Inhalts Codierungs Schemas leiten.
ms.assetid: 136f22a6-e5ca-41c5-8651-6e132655d268
keywords:
- Inhaltscodierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b089ae2aa4cbacdfc9b6ebefe5cbdfc1bfc10e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039474"
---
# <a name="content-encoding"></a>Inhaltscodierung

Wie im HTTP-Protokoll (RFC 2616) angegeben, können Anwendungen anfordern, dass der Server HTTP-Antworten im codierten Format zurückgibt. Vor Windows Server 2008 und Windows Vista wurden Anforderungen mit Inhalts Codierung zur Verarbeitung auf ihrer Ebene an die Anwendung gesendet. Ab Windows Server 2008 und Windows Vista kann die Anwendung WinInet zum Durchführen der Decodierung von Inhalten für die GZIP-Datei und zum deflate von Inhalts Codierungs Schemas leiten.

Um die Decodierung von Inhalten zu aktivieren, legt die Anwendung die Decodierung fest Durch das Aktivieren der Decodierung ist jedoch nicht sichergestellt, dass Wininet die Decodierung von Inhalten ausführt, und die Anwendung sollte darauf vorbereitet sein, Decodierung auszuführen. WinInet entfernt den Content-Encoding-Header aus der Antwort, wenn die Inhalts Decodierung erfolgreich ausgeführt wurde. Anwendungen sollten die Decodierung von Inhalten unabhängig davon verarbeiten, ob die Decodierungs Option aktiviert oder deaktiviert ist, wenn der Content-Encoding-Header in der Antwort vorhanden ist.

Wenn die Decodierung aktiviert ist, muss die Anwendung die Liste der unterstützten Codierungen im Accept-Encoding-Header der Anforderung angeben. Der Accept-Encoding-Header bewirkt jedoch nicht, dass der Server eine codierte Antwort sendet. WinInet sendet Antworten, die nicht der Liste der zulässigen Codierungen entsprechen, zurück an die Anwendung.

In der folgenden Liste werden die Bedingungen beschrieben, unter denen WININET die Decodierung von Inhalten durchführt, wenn die Option aktiviert ist:

-   Der Accept-Encoding-Header muss in der Anforderung vorhanden sein, und er muss die gzip-, deflate-oder beide gzip-und Deflate-Codierungs Schemas angeben.
-   Das im Content-Encoding-Header angegebene Codierungsschema muss mit einem der im Accept-Encoding-Header angegebenen Codierungs Schemas identisch sein.
-   Der Content-Encoding-Header in der Antwort gibt nur ein Codierungsschema an.
-   Die Antwort darf nur einen Content-Encoding-Header enthalten. WinInet decodiert Inhalt, der nur mit einem Codierungsschema codiert ist.
-   Der Cache-Control-Header darf nicht die No-Transform-Direktive enthalten.
-   Der Content-Range-Header darf nicht in der Antwort vorhanden sein.

## <a name="setting-the-decompression-option"></a>Festlegen der dekomprimierungsoption

Die Decodierung kann für das Sitzungs handle, das Anforderungs handle oder das Verbindungs Handle festgelegt werden. Das Handle, für das die Decodierungs Option festgelegt ist, definiert den Bereich der Decodierungs Option. Beispielsweise wird durch das Festlegen von Decodierung für die Sitzung das Decodieren von allen Verbindungen und Anforderungen aktiviert, die unter diesem Handle erstellt werden.

Um die Decodierungs Option festzulegen, ruft die Anwendung [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) mit dem Handle auf, das von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)oder [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)zurückgegeben wurde. Die **Option \_ \_ http- \_ Decodierung der Internet Option** wird im Parameter *dwOption* angegeben, und der *lpBuffer* -Parameter verweist auf eine boolesche Variable, die auf true festgelegt ist. Zum Deaktivieren der Decodierung Ruft die Anwendung **InternetSetOption** mit der Option **http- \_ \_ \_ Decodierung der Internet Option** auf, und die boolesche Variable ist auf false festgelegt.

Wenn die Decodierungs Option festgelegt ist, führt WinInet eine Decodierung der Anforderung aus, wenn die Anwendung [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)aufruft. Wenn WinInet beim Ausführen der Decodierung von Inhalten einen Fehler feststellt, schlägt der **internetreadfile** -Befehl mit einem **Fehler \_ \_ \_** fehl Wenn die Decodierung fehlschlägt, verfügt die Anwendung über zwei Optionen: Sie kann den Accept-Encoding-Header entfernen und die Anforderung erneut senden. Alternativ kann die Option **\_ http- \_ \_ Decodierung der Internet Option** für die Anforderung auf false festgelegt und die Anforderung erneut gesendet werden. Wenn die Decodierungs Option auf false festgelegt ist, muss die Anwendung den Content-Encoding-Header überprüfen und jede Decodierung auf Anwendungsebene durchführen.

> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 