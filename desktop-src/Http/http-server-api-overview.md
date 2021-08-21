---
title: Übersicht über die HTTP-Server-API
description: In diesem Thema wird eine typische Abfolge von Vorgängen beschrieben, die die HTTP-Server-API verwenden.
ms.assetid: 1245fd98-8370-4f1b-8c86-de9be5e678bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d24defe190c073f7ca359309baf6731d466459d9bb7cfbd9ffc05268ded11ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150333"
---
# <a name="http-server-api-overview"></a>Übersicht über die HTTP-Server-API

In der folgenden Liste ist eine typische Abfolge von Vorgängen aufgeführt, die die HTTP-Server-API verwenden:

-   Initialisieren Sie die HTTP-Server-API mithilfe der [**HttpInitialize-Funktion.**](/windows/desktop/api/Http/nf-http-httpinitialize)
-   Erstellen Sie mithilfe der [**HttpCreateHttpHandle-Funktion eine Anforderungswarteschlange.**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle)
-   Registrieren Sie eine oder mehrere URLs mithilfe der [**HttpAddUrl-Funktion.**](/windows/desktop/api/Http/nf-http-httpaddurl)
-   Empfangen Sie eingehende Anforderungen, die mithilfe der [**HttpReceiveHttpRequest-Funktion**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) an registrierte URLs geleitet werden, und senden Sie HTTP-Antworten für diese Anforderungen mithilfe der [**HttpSendHttpResponse-Funktion.**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)
-   (Optional) Wenn Sie eine Antwort senden, senden Sie mithilfe der [**HttpSendResponseEntityBody-Funktion einen zusätzlichen Entitätskörper.**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)
-   Führen Sie Bereinigungsvorgänge mithilfe der [**Funktionen HttpRemoveUrl,**](/windows/desktop/api/Http/nf-http-httpremoveurl) [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) und [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) aus.

Beachten Sie bei Vorgängen, die URLs verwenden, dass es sich um die verarbeitete URL handelt, die im **Vorurl-Member** der [**HTTP REQUEST \_ \_ V1-Struktur**](/windows/desktop/api/Http/ns-http-http_request_v1) enthalten ist, die verwendet werden soll. Verwenden Sie nicht die nicht verarbeitete URL im **pRawUrl-Member,** die ausschließlich zu Nachverfolgungs- und statistischen Zwecken dient.

Jede Anwendung erstellt eine eigene Anforderungswarteschlange. Eine Anwendung erhält ihr Anforderungswarteschlangenhandle von [**HttpCreateHttpHandle.**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) Dieses Handle wird an die [**HttpAddUrl-Funktion**](/windows/desktop/api/Http/nf-http-httpaddurl) übergeben, um der Anforderungswarteschlange eine URL hinzuzufügen. Die Anwendung empfängt eine Benachrichtigung über eine eingehende Anforderung und ruft sie aus der Anforderungswarteschlange ab, indem sie die [**HttpReceiveHttpRequest-Funktion**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) mit dem Anforderungswarteschlangenhand handle aufruft. Sie können diese Funktion verwenden, um entweder die Anforderungsheader oder die Header und den Entitätskörper zu empfangen. [**HttpReceiveHttpRequest gibt**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) auch einen Anforderungsbezeichner (RequestId) für die empfangene Anforderung zurück, der für das Anforderungshandle eindeutig ist.

> [!Note]  
> Es liegt in der Verantwortung der Anwendung, alle relevanten Anforderungsheader zu untersuchen, einschließlich Inhaltsaushandlungsheader, wenn sie verwendet werden, und Anforderungen je nach Inhalt des Headers zu fehlschlagen. Die HTTP-Server-API stellt nur sicher, dass jede Headerzeile ordnungsgemäß beendet wird und keine unzulässigen Zeichen enthält.

 

Verwenden Sie [**die HttpReceiveRequestEntityBody-Funktion**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) mit dem Handle für die Anforderungswarteschlange, um nachfolgende Teile des Entitätskörpers einer Anforderung abzurufen(sofern verfügbar).

> [!Note]  
> Die HTTP-Server-API decodiert blockierte Nachrichten auf der Empfangsseite, führt jedoch keine blockierte Codierung auf der Sendeseite aus. Wenn blocking auf der Sendeseite erforderlich ist, muss die Anwendung sie implementieren. Weitere Informationen zur blockierten Codierung finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

 

Verwenden Sie [**die HttpReceiveClientCertificate-Funktion**](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) mit Anwendungen, die URLs mithilfe eines sicheren Schemas **("https")** bedienen, um optional die Zertifikatinformationen des Clients abzurufen.

Antworten werden mit der [**HttpSendHttpResponse-Funktion**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) gesendet. Diese Funktion verwendet die RequestId aus der entsprechenden Anforderung, um die Antwort zu senden. Eine Antwort kann im Laufe der Zeit in mehreren API-Aufrufen gesendet werden, indem die [**HttpSendResponseEntityBody-Funktion**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) mit der RequestId aus der ursprünglich empfangenen Anforderung aufruft.

> [!Note]  
> Standardmäßig verwendet [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) "Microsoft-HTTPAPI/1.0" als "Server:"-Header. Wenn eine Anwendung einen Serverheader in einer Antwort angibt, wird dieser Wert als erster Teil des Serverheader platziert, gefolgt von einem Leerzeichen und dann "Microsoft-HTTPAPI/1.0".

 

Im Allgemeinen blendet die HTTP-Server-API Details zur Verbindungsverwaltung und deren Einrichtung und Abbruch von Anwendungen aus. Eine Anwendung kann jedoch optional die Beendigung einer Verbindung erkennen, indem sie [**HttpWaitForDisconnect aufruft.**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)

Anwendungen müssen mithilfe der folgenden Schritte bereinigt werden:

-   Wenn die Anwendung keine URL abhört oder darauf reagiert, wird die URL mithilfe der [**HttpRemoveURL-Funktion**](/windows/desktop/api/Http/nf-http-httpremoveurl) entfernt.
-   Wenn die Anwendung die Anforderungswarteschlange nicht mehr verwendet, schließen Sie das Anforderungswarteschlangenhandle mithilfe der [**CloseHandle-Funktion.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)
-   Wenn die Anwendung die VERWENDUNG der HTTP-Server-API abgeschlossen hat, rufen Sie die [**HttpTerminate-Funktion**](/windows/desktop/api/Http/nf-http-httpterminate) auf.

 

 