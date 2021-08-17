---
title: Asynchroner Vorgang
description: Im asynchronen Modus kann eine Anwendung jede Funktion ausführen, die einen Kontextwert als einen ihrer Parameter enthält, und sie kann weiterhin andere Befehle oder Funktionen ausführen, während die Anwendung wartet, bis die Funktion ihre Aufgabe abgeschlossen hat.
ms.assetid: 4b8ade00-deb3-4d9f-9ceb-5ba3296c8c68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e494b79b28b9aaf005fc6b1790d0cf84b07ceade6606f03ce03198426ac33d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562092"
---
# <a name="asynchronous-operation"></a>Asynchroner Vorgang

Wie lange es dauert, bis eine Anwendung auf eine Internetressource zugreift, hängt von einer Reihe von Faktoren ab, z. B. von der verwendeten Verbindung, dem Server, auf dem sich die Ressource befindet, und der Anzahl der Benutzer, die versuchen, auf die Ressource zuzugreifen. Bei Anwendungen, die mehrere Ressourcen herunterladen oder mehrere Aufgaben (einschließlich eines oder mehrerer Downloads) verarbeiten, kann das Warten auf den Abschluss jedes Downloads, bevor mit der nächsten Aufgabe fortgegangen wird, äußerst ineffizient sein. Um die Wartezeit einer Anwendung zu verringern, können viele winINet-Funktionen asynchron ausgeführt werden.

Im asynchronen Modus kann eine Anwendung jede Funktion ausführen, die einen Kontextwert als einen ihrer Parameter enthält, und sie kann weiterhin andere Befehle oder Funktionen ausführen, während die Anwendung wartet, bis die Funktion ihre Aufgabe abgeschlossen hat. Während der Task abgeschlossen ist, wird eine von der Anwendung bereitgestellte Statusrückruffunktion über den Fortschritt der Aufgabe und den Abschluss des Tasks benachrichtigt. Zu diesem Zeitpunkt kann die Statusrückruffunktion andere Funktionen aufrufen oder alle anderen erforderlichen Aufgaben ausführen, die vom Abschluss der Aufgabe abhängig waren.

Beim asynchronen Aufrufen von WinINet gibt es keine Afinität für Rückrufthreads: Ein Aufruf kann von einem Thread beginnen, aber jeder andere Thread kann den Rückruf empfangen.

-   [Vorteile](#benefits)
-   [Szenarios](#scenarios)
-   [Verwandte Themen](#related-topics)

## <a name="benefits"></a>Vorteile

Der asynchrone Betrieb bietet mehrere Vorteile. Beispiel:

-   Gleichzeitiges Herunterladen mehrerer Internetressourcen.

    Sie können gleichzeitig eine Verbindung mit mehreren Internetressourcen herstellen und diese herunterladen, sobald sie verfügbar sind.

-   Erhöhen der Leistung Ihrer Anwendung.

    Eine Anwendung, die die WinINet-Funktionen asynchron verwendet, muss nicht warten, bis die Anforderung abgeschlossen ist. Daher kann die Anwendung andere Aufgaben ausführen, die nicht von der Anforderung abhängig sind, wodurch die Gesamtleistung der Anwendung verbessert wird.

-   Überwachen Sie den Fortschritt des Downloads.

    Die Statusrückruffunktion empfängt Benachrichtigungen, während sie eine Anforderung verarbeitet. Bei Bedarf kann Ihre Anwendung die von dieser Statusrückruffunktion bereitgestellten Informationen verwenden, um den Benutzer über den Fortschritt des Vorgangs auf dem Laufenden zu halten oder Anforderungen zu unterbrechen, deren Abschluss zu lange dauert.

## <a name="scenarios"></a>Szenarien

Angenommen, Ihre Anwendung muss die Kaffeepreise von den Standorten Downfall Coffee & Coffee und Fourth Coffee herunterladen und die Preise vergleichen. Die Vierte Coffee-Website hat in der Regel eine langsamere Antwortzeit, daher sollte Ihre Anwendung zuerst die Informationen von Downfall Coffee & Coffee herunterladen.

Es werden zwei Versionen der Anwendung entwickelt. Eine funktioniert synchron, indem zuerst die Preise von der Downfall Coffee & Coffee-Website und dann die Preise von der Fourth Coffee-Website heruntergeladen werden. Die zweite funktioniert asynchron, indem Anforderungen an beide Websites gesendet und die Preise heruntergeladen werden, sobald sie verfügbar sind.

Die folgende Tabelle zeigt, was passieren würde, wenn die Vierte Coffee-Website an einem bestimmten Tag schneller wäre.



| Ereignis                                                            | Synchrone Version                        | Asynchrone Version                                     |
|------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------------|
| Starten                                                            | Senden einer Anforderung an Downfall Coffee & Coffee Coffee      | Senden von Anforderungen an Downfall Coffee & Coffee und Fourth Coffee |
| Anforderung von der asynchronen Version an Fourth Coffee abgeschlossen | Wartend                                    | Herunterladen der Preise von Fourth Coffee                       |
| Request to Downfall Coffee & Coffee Completed (Anforderung an Downfall Coffee & Coffee Coffee abgeschlossen)                       | Laden Sie die Preise von Downfall Coffee & Coffee herunter. | Laden Sie die Preise von Downfall Coffee & Coffee herunter.               |
| Nach dem Ausfall von Coffee & Die Preise von Tee werden heruntergeladen.              | Senden einer Anforderung an Fourth Coffee              | Vergleichen von Preisen                                           |
| Vergleich der asynchronen Version abgeschlossen                      | Wartend                                    | Vorgang abgeschlossen                                       |
| Anforderung von der synchronen Version an Fourth Coffee abgeschlossen  | Herunterladen der Preise von Fourth Coffee         | –                                                      |
| Nach dem Herunterladen der Preise von Fourth Coffee                      | Vergleichen von Preisen                             | –                                                      |
| Vergleich der synchronen Version abgeschlossen                       | Vorgang abgeschlossen                         | –                                                      |



 

Ein weiteres Beispiel wäre ein Webbrowser wie Microsoft Internet Explorer. Wenn der Browser eine Seite herunterlädt, müssen häufig andere Ressourcen wie Bilder und Sounddateien heruntergeladen werden. Im asynchronen Modus können die Seite und die zugehörigen Ressourcen gleichzeitig angefordert und heruntergeladen werden, sobald sie verfügbar sind, anstatt die Seite und jede Ressource einzeln anzufordern und herunterzuladen.

## <a name="related-topics"></a>Verwandte Themen

Die folgenden Links sind verknüpft.

Tutorials

-   [Erstellen von Statusrückruffunktionen](creating-status-callback-functions.md)

Funktionen, die zum Einrichten eines asynchronen Vorgangs erforderlich sind

-   [**InternetÖffnen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)
-   [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)

Funktionen, die asynchron verwendet werden können

-   [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)
-   [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)
-   [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)
-   [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya)
-   [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)
-   [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)
-   [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)
-   [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)
-   [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)
-   [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya)
-   [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea)
-   [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)
-   [**HttpEndRequest**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta)
-   [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)
-   [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa)
-   [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)
-   [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)
-   [**InternetReadFileEx**](/windows/desktop/api/Wininet/nf-wininet-internetreadfileexa)

> [!Note]  
> Die Funktionen [**FtpCreateDirectory,**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) [**FtpRemoveDirectory,**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) [**FtpSetCurrentDirectory,**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) [**FtpGetCurrentDirectory,**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)und [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) verwenden den Kontextwert, der im Aufruf der [**InternetConnect-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) bereitgestellt wird.

 

> [!Note]  
> WinINet unterstützt keine Serverimplementierungen. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP-Dienste (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 