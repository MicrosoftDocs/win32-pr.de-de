---
title: Asynchroner Vorgang
description: Im asynchronen Modus kann eine Anwendung jede Funktion ausführen, die einen Kontextwert als einen ihrer Parameter enthält, und kann weitere Befehle oder Funktionen ausführen, während die Anwendung wartet, bis die Funktion ihre Aufgabe abgeschlossen hat.
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

Die Zeit, die eine Anwendung für den Zugriff auf eine Internetressource benötigt, hängt von einer Reihe von Faktoren ab, z. B. der verwendeten Verbindung, dem Server, auf dem sich die Ressource befindet, und der Anzahl der Benutzer, die versuchen, auf die Ressource zu zugreifen. Für Anwendungen, die mehrere Ressourcen herunterladen oder mehrere Aufgaben (einschließlich eines oder mehrerer Downloads) verarbeiten, kann das Warten auf den Abschluss jedes Downloads vor dem Wechsel zur nächsten Aufgabe äußerst ineffizient sein. Um die Wartezeit einer Anwendung zu verringern, können viele WinINet-Funktionen asynchron ausgeführt werden.

Im asynchronen Modus kann eine Anwendung jede Funktion ausführen, die einen Kontextwert als einen ihrer Parameter enthält, und kann weitere Befehle oder Funktionen ausführen, während die Anwendung wartet, bis die Funktion ihre Aufgabe abgeschlossen hat. Während die Aufgabe abgeschlossen ist, wird eine von der Anwendung bereitgestellte Statusrückruffunktion über den Status der Aufgabe und deren Abschluss benachrichtigt. Zu diesem Zeitpunkt kann die Statusrückruffunktion andere Funktionen aufrufen oder andere erforderliche Aufgaben ausführen, die vom Abschluss der Aufgabe abhängig waren.

Wenn Sie WinINet asynchron aufrufen, ist kein Rückrufthread definiert: Ein Aufruf kann von einem Thread aus beginnen, aber jeder andere Thread kann den Rückruf empfangen.

-   [Vorteile](#benefits)
-   [Szenarios](#scenarios)
-   [Verwandte Themen](#related-topics)

## <a name="benefits"></a>Vorteile

Der asynchrone Betrieb hat mehrere Vorteile. Beispiel:

-   Gleichzeitiges Herunterladen mehrerer Internetressourcen.

    Sie können gleichzeitig eine Verbindung mit mehreren Internetressourcen herstellen und diese herunterladen, sobald sie verfügbar sind.

-   Steigern der Leistung Ihrer Anwendung.

    Eine Anwendung, die die WinINet-Funktionen asynchron verwendet, muss nicht warten, bis die Anforderung abgeschlossen ist, sodass die Anwendung andere Aufgaben ausführen kann, die nicht von der Anforderung abhängig sind, wodurch die Gesamtleistung der Anwendung verbessert wird.

-   Überwachen Sie den Fortschritt des Downloads.

    Die Statusrückruffunktion empfängt Benachrichtigungen, während sie eine Anforderung verarbeitet. Bei Bedarf kann Ihre Anwendung die von dieser Statusrückruffunktion bereitgestellten Informationen verwenden, um den Benutzer über den Fortschritt des Vorgangs auf dem Laufenden zu halten oder Anforderungen zu unterbrechen, deren Abschluss zu lange dauern soll.

## <a name="scenarios"></a>Szenarien

Angenommen, Ihre Anwendung muss die Kaffeepreise von downfall Coffee & Tee und der Vierten Kaffee-Website herunterladen und die Preise vergleichen. Die Fourth Coffee-Website hat in der Regel eine langsamere Antwortzeit, sodass Ihre Anwendung die Informationen zuerst von Downfall Coffee & Tee herunterladen sollte.

Es werden zwei Versionen der Anwendung entwickelt. Eins funktioniert synchron, und zuerst werden die Preise von der Website Downfall Coffee & Tee und dann die Preise von der Fourth Coffee-Website heruntergeladen. Das zweite funktioniert asynchron und sendet Anforderungen an beide Websites und downloadt die Preise, sobald sie verfügbar sind.

Die folgende Tabelle veranschaulicht, was passieren würde, wenn die Website "Fourth Coffee" an einem bestimmten Tag schneller wäre.



| Ereignis                                                            | Synchrone Version                        | Asynchrone Version                                     |
|------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------------|
| Starten                                                            | Senden einer Anforderung an Downfall Coffee & Tee      | Senden von Anforderungen an Downfall Coffee & Coffee und Fourth Coffee |
| Anforderung von der asynchronen Version an Fourth Coffee abgeschlossen | Wartend                                    | Herunterladen von Preisen von Fourth Coffee                       |
| Anforderung zum Ausfall von Coffee & Tee abgeschlossen                       | Laden Sie die Preise von Downfall Coffee & Tee herunter. | Laden Sie die Preise von Downfall Coffee & Tee herunter.               |
| Nach dem Ausfall von Coffee & tee es prices are downloaded              | Senden einer Anforderung an Fourth Coffee              | Vergleich der Preise                                           |
| Vergleich der asynchronen Version abgeschlossen                      | Wartend                                    | Vorgang abgeschlossen                                       |
| Anforderung von der synchronen Version an Fourth Coffee abgeschlossen  | Herunterladen von Preisen von Fourth Coffee         | –                                                      |
| Nach dem Herunterladen der Preise für Fourth Coffee                      | Vergleich der Preise                             | –                                                      |
| Vergleich der synchronen Version abgeschlossen                       | Vorgang abgeschlossen                         | –                                                      |



 

Ein weiteres Beispiel wäre ein Webbrowser wie Microsoft Internet Explorer. Wenn der Browser eine Seite herunterlädt, müssen häufig andere Ressourcen wie Bilder und Sounddateien heruntergeladen werden. Im asynchronen Modus können die Seite und die zugehörigen Ressourcen gleichzeitig angefordert und heruntergeladen werden, sobald sie verfügbar sind, anstatt die Seite und jede Ressource nacheinander an- und herunterzuladen.

## <a name="related-topics"></a>Verwandte Themen

Im Folgenden finden Sie verwandte Links.

Tutorials

-   [Erstellen von Statusrückruffunktionen](creating-status-callback-functions.md)

Funktionen, die zum Einrichten eines asynchronen Vorgangs erforderlich sind

-   [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)
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
> Die [**Funktionen FtpCreateDirectory,**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) [**FtpRemoveDirectory,**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) [**FtpSetCurrentDirectory,**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) [**FtpGetCurrentDirectory,**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)und [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) verwenden den Kontextwert, der im Aufruf der [**InternetConnect-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) angegeben wird.

 

> [!Note]  
> WinINet unterstützt keine Serverimplementierung. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP Services (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 