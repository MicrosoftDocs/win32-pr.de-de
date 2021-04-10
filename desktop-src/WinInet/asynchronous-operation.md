---
title: Asynchroner Vorgang
description: Im asynchronen Modus kann eine Anwendung jede Funktion ausführen, die einen Kontextwert als einen ihrer Parameter enthält, und andere Befehle oder Funktionen weiterhin ausführen, während die Anwendung auf den Abschluss der Aufgabe wartet.
ms.assetid: 4b8ade00-deb3-4d9f-9ceb-5ba3296c8c68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a7e1d0cf84aa92691e1d926d771ea809d31a171
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728929"
---
# <a name="asynchronous-operation"></a>Asynchroner Vorgang

Die Zeit, die eine Anwendung benötigt, um auf eine Internet Ressource zuzugreifen, hängt von einer Reihe von Faktoren ab, z. b. der verwendeten Verbindung, dem Server, auf dem sich die Ressource befindet, und der Anzahl der Benutzer, die versuchen, auf die Ressource zuzugreifen. Bei Anwendungen, die mehrere Ressourcen herunterladen oder mehrere Tasks verarbeiten (einschließlich eines oder mehrerer Downloads), kann das warten auf den Abschluss der einzelnen Downloads, bevor Sie mit der nächsten Aufgabe fortfahren, äußerst ineffizient sein. Um die Zeitspanne zu verkürzen, die eine Anwendung warten muss, können viele der WinInet-Funktionen asynchron ausgeführt werden.

Im asynchronen Modus kann eine Anwendung jede Funktion ausführen, die einen Kontextwert als einen ihrer Parameter enthält, und andere Befehle oder Funktionen weiterhin ausführen, während die Anwendung auf den Abschluss der Aufgabe wartet. Während der Aufgabe abgeschlossen wird, wird eine von der Anwendung bereitgestellte Status Rückruffunktion über den Fortschritt der Aufgabe benachrichtigt und nachdem Sie abgeschlossen wurde. Zu diesem Zeitpunkt kann die Status Rückruffunktion andere Funktionen anrufen oder alle anderen erforderlichen Aufgaben ausführen, die von der Beendigung der Aufgabe abhängen.

Es gibt keinen Rückruf Thread, wenn Sie WinInet asynchron aufzurufen: ein-Befehl kann von einem Thread gestartet werden, aber jeder andere Thread kann den Rückruf empfangen.

-   [Vorteile](#benefits)
-   [Szenarios](#scenarios)
-   [Verwandte Themen](#related-topics)

## <a name="benefits"></a>Vorteile

Es gibt mehrere Vorteile, die asynchron funktionieren. Beispiel:

-   Mehrere Internet Ressourcen werden gleichzeitig heruntergeladen.

    Sie können gleichzeitig eine Verbindung mit mehreren Internet Ressourcen herstellen und Sie herunterladen, sobald Sie verfügbar werden.

-   Erhöhen der Leistung Ihrer Anwendung.

    Eine Anwendung, die die WinInet-Funktionen asynchron verwendet, muss nicht warten, bis die Anforderung abgeschlossen ist, sodass die Anwendung andere Tasks ausführen kann, die nicht von der Anforderung abhängen, wodurch die Gesamtleistung der Anwendung verbessert wird.

-   Überwachen Sie den Fortschritt des Downloads.

    Die Status Rückruffunktion empfängt bei der Verarbeitung einer Anforderung Benachrichtigungen. Bei Bedarf kann die Anwendung die von dieser Status Rückruffunktion bereitgestellten Informationen verwenden, um den Benutzer über den Fortschritt des Vorgangs zu informieren oder Anforderungen zu unterbrechen, die zu lange dauern.

## <a name="scenarios"></a>Szenarien

Nehmen wir an, Ihre Anwendung muss Kaffeepreise von der & für das Herunterladen von Kaffee und die vierten Kaffee-Websites herunterladen und die Preise vergleichen. Die vierte Coffee-Website hat normalerweise eine langsamere Reaktionszeit, sodass Ihre Anwendung die Informationen von "bei Kaffee & Tee" zuerst herunterladen sollte.

Zwei Versionen der Anwendung werden entwickelt. Ein solcher arbeitet synchron und lädt zuerst die Preise von der Seite Coffee & Tea herunter, und dann die Preise von der vierten Kaffee Website. Die zweite Funktion arbeitet asynchron, sendet Anforderungen an beide Standorte und lädt die Preise herunter, wenn Sie verfügbar werden.

In der folgenden Tabelle wird veranschaulicht, was passiert, wenn die vierte Kaffee Website an einem bestimmten Tag schneller war.



| Ereignis                                                            | Synchrone Version                        | Asynchrone Version                                     |
|------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------------|
| Start                                                            | Anforderung zum Absenden von Kaffee & Tee senden      | Senden von Anforderungen an den Absturz von Kaffee & Tee und Fourth Coffee |
| Anforderung von der asynchronen Version an den vierten Kaffee abgeschlossen | Warten                                    | Preise von Fourth Coffee herunterladen                       |
| Anforderung zum Durchlaufen von Kaffee & Tee abgeschlossen                       | Preise von "bei Kaffee & Tee herunterladen" herunterladen | Preise von "bei Kaffee & Tee herunterladen" herunterladen               |
| Nach dem Herunterladen von Kaffee & die Preise von Tea heruntergeladen.              | Anforderung an vierten Kaffee senden              | Preise vergleichen                                           |
| Vergleich der asynchronen Version abgeschlossen                      | Warten                                    | Vorgang beendet                                       |
| Anforderung von synchroner Version zum vierten Kaffee abgeschlossen  | Preise von Fourth Coffee herunterladen         | –                                                      |
| Nachdem die Preise für den vierten Kaffee heruntergeladen wurden                      | Preise vergleichen                             | –                                                      |
| Vergleich der synchronen Version abgeschlossen                       | Vorgang beendet                         | –                                                      |



 

Ein weiteres Beispiel wäre ein Webbrowser wie z. b. Microsoft Internet Explorer. Wenn der Browser eine Seite herunterlädt, müssen häufig andere Ressourcen wie Bilder und Audiodateien heruntergeladen werden. Im asynchronen Modus können die Seite und die zugehörigen Ressourcen gleichzeitig angefordert und heruntergeladen werden, wenn Sie verfügbar werden, anstatt die Seite und die einzelnen Ressourcen einzeln anzufordern und herunterzuladen.

## <a name="related-topics"></a>Verwandte Themen

Im folgenden finden Sie verknüpfte Links.

Tutorials

-   [Erstellen von Status Rückruf Funktionen](creating-status-callback-functions.md)

Zum Einrichten des asynchronen Vorgangs erforderliche Funktionen

-   [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)
-   [**Internetsetstatus Callback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)

Funktionen, die asynchron verwendet werden können

-   [**Ftpkreatedirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)
-   [**Ftpdeletefile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)
-   [**Ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)
-   [**Ftpgetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya)
-   [**Ftpgetfile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)
-   [**Ftpopumfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)
-   [**Ftpputfile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)
-   [**Ftpremuvedirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)
-   [**Ftprenamefile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)
-   [**Ftpsetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya)
-   [**Gopherfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea)
-   [**Gopheropenfile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)
-   [**Httpdrequest**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta)
-   [**Httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)
-   [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa)
-   [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)
-   [**InternetOpenURL**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)
-   [**Internetreadfileex**](/windows/desktop/api/Wininet/nf-wininet-internetreadfileexa)

> [!Note]  
> Die Funktionen [**ftpkreatedirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya), [**ftpremumuvedirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya), [**ftpsetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya), [**ftpgetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya), [**ftpdeletefile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)und [**ftprenamefile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) verwenden den Kontextwert, der im Aufrufen der [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) -Funktion bereitgestellt wird.

 

> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 