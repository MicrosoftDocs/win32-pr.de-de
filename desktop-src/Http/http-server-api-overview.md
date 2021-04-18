---
title: Übersicht über die HTTP Server-API
description: In diesem Thema wird eine typische Abfolge von Vorgängen identifiziert, die die HTTP-Server-API verwenden.
ms.assetid: 1245fd98-8370-4f1b-8c86-de9be5e678bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c99af3e4914c5496c2adea10b3ac658f75f3018
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338053"
---
# <a name="http-server-api-overview"></a>Übersicht über die HTTP Server-API

In der folgenden Liste wird eine typische Abfolge von Vorgängen identifiziert, die die HTTP-Server-API verwenden:

-   Initialisieren Sie die HTTP-Server-API mithilfe der [**httpinitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) -Funktion.
-   Erstellen Sie eine Anforderungs Warteschlange, indem Sie die [**httpkreatehttphandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) -Funktion verwenden.
-   Registrieren Sie eine oder mehrere URLs mithilfe der [**httpaddurl**](/windows/desktop/api/Http/nf-http-httpaddurl) -Funktion.
-   Empfangen eingehender Anforderungen, die mithilfe der [**httpreceivehttprequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) -Funktion an registrierte URLs weitergeleitet werden, und Senden von HTTP-Antworten für diese Anforderungen mithilfe der [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) -Funktion.
-   Optionale Senden Sie beim Senden einer Antwort einen zusätzlichen Entitäts Text mithilfe der [**httpsendresponmenentitybody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) -Funktion.
-   Ausführen von Bereinigungs Vorgängen mithilfe der Funktionen " [**httpremoveurl**](/windows/desktop/api/Http/nf-http-httpremoveurl)", " [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) " und " [**httpbeendbar**](/windows/desktop/api/Http/nf-http-httpterminate) ".

Beachten Sie bei Vorgängen, die URLs verwenden, dass es sich um die verarbeitete URL handelt, die im **cookedurl** -Member der zu verwendenden [**http- \_ Anforderung \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) -Struktur enthalten ist. Verwenden Sie nicht die nicht verarbeitete URL im **prawurl** -Member, der ausschließlich zu nach Verfolgungs-und statistischen Zwecken dient.

Jede Anwendung erstellt eine eigene Anforderungs Warteschlange. Eine Anwendung erhält das Anforderungs Warteschlangen Handle von [**httpkreatehttphandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle). Sie übergibt dieses Handle an die [**httpaddurl**](/windows/desktop/api/Http/nf-http-httpaddurl) -Funktion, um der Anforderungs Warteschlange eine URL hinzuzufügen. Die Anwendung empfängt eine Benachrichtigung über eine eingehende Anforderung und ruft Sie aus der Anforderungs Warteschlange ab, indem die Funktion [**httpreceivehttprequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) mit dem Handle der Anforderungs Warteschlange aufgerufen wird. Sie können diese Funktion verwenden, um entweder die Anforderungs Header oder die Header und den Entitäts Text zu empfangen. [**Httpreceivehttprequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) gibt auch einen Anforderungs Bezeichner (RequestId) für die empfangene Anforderung zurück, die für das Anforderungs handle eindeutig ist.

> [!Note]  
> Es liegt in der Verantwortung der Anwendung, alle relevanten Anforderungs Header zu untersuchen, einschließlich Content-Aushandlungs Header, wenn Sie verwendet werden, und nach Bedarf Anforderungs Fehler basierend auf dem Header Inhalt zu überprüfen. Die HTTP-Server-API stellt nur sicher, dass jede Kopfzeile ordnungsgemäß beendet wird und keine ungültigen Zeichen enthält.

 

Verwenden Sie die [**httpreceiverequestentitybody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) -Funktion mit dem Handle der Anforderungs Warteschlange, um nachfolgende Teile des Entitäts Texts einer Anforderung abzurufen (sofern vorhanden).

> [!Note]  
> Die HTTP-Server-API decodiert segmentierte Nachrichten auf der Empfangsseite, führt jedoch keine segmentierte Codierung auf der Sendeseite aus. Wenn Segmentierung auf der Sendeseite erforderlich ist, muss Sie von der Anwendung implementiert werden. Weitere Informationen zur segmentierten Codierung finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

 

Verwenden Sie die Funktion [**httpreceiveclientcertificate**](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) mit Anwendungen, die URLs mithilfe eines sicheren Schemas ("**https**") verarbeiten, um optional die Zertifikat Informationen des Clients abzurufen.

Antworten werden mit der [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) -Funktion gesendet. Diese Funktion verwendet das RequestId-Element aus der entsprechenden Anforderung, um die Antwort zu senden. Eine Antwort kann in mehreren API-aufrufen über einen bestimmten Zeitraum gesendet werden, indem die [**httpsendresponseentitybody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) -Funktion mit der RequestId aus der ursprünglich empfangenen Anforderung aufgerufen wird.

> [!Note]  
> Standardmäßig verwendet [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) "Microsoft-Httpapi/1.0" als "Server:"-Header. Wenn eine Anwendung einen Server Header in einer Antwort angibt, wird dieser Wert als erster Teil des Server Headers, gefolgt von einem Leerzeichen und dann "Microsoft-Httpapi/1.0" platziert.

 

Im allgemeinen blendet die HTTP-Server-API Details der Verbindungs Verwaltung und ihrer Einrichtung und Löschung von Anwendungen aus. Eine Anwendung kann jedoch optional das Beenden einer Verbindung durch Aufrufen von [**httpwaitfordisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)erkennen.

Anwendungen müssen mithilfe der folgenden Schritte bereinigt werden:

-   Wenn die Anwendung eine URL nicht überwacht oder antwortet, wird die URL mithilfe der [**httpremoveurl**](/windows/desktop/api/Http/nf-http-httpremoveurl) -Funktion entfernt.
-   Wenn die Anwendung mit der Anforderungs Warteschlange fertig ist, schließen Sie das Anforderungs Warteschlangen Handle mithilfe der [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) -Funktion.
-   Wenn die Anwendung mit der HTTP-Server-API fertig ist, können Sie die [**httpend**](/windows/desktop/api/Http/nf-http-httpterminate) -Funktion verwenden.

 

 