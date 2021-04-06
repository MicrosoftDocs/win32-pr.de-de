---
title: HTTP-Server Tasks
description: In der Regel werden http-Server Aufgaben in einer bestimmten Reihenfolge ausgeführt. Das heißt, eine Aufgabe muss abgeschlossen werden, und die Ausgabe, die vor Beginn der nächsten Aufgabe abgerufen wird.
ms.assetid: 08f8e7e9-23b9-403f-b00c-8912919d65b1
keywords:
- HTTP-Server Tasks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22455dbda21aca32b26f586eed6e51cef7509af2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714585"
---
# <a name="http-server-tasks"></a>HTTP-Server Tasks

In der Regel werden http-Server Aufgaben in einer bestimmten Reihenfolge ausgeführt. Das heißt, eine Aufgabe muss abgeschlossen werden, und die Ausgabe, die vor Beginn der nächsten Aufgabe abgerufen wird.

Eine Aufgabenseite wird erstellt, um Beispielcode über bestimmte Aufgaben, die eine HTTP-Server Anwendung ausführt, darzustellen. Eine Aufgabenseite verweist auf die C-Erweiterungs Datei des HTTP-Server Beispiels. Wenn Sie das PSDK auf Laufwerk C: \\ eines lokalen Computers installieren, wird die komplette Server Beispielanwendung unter C: \\ Programme \\ Microsoft SDK \\ Samples \\ netds \\ http \\ Server installiert.

In der folgenden Liste sind die HTTP-Server Tasks aufgeführt:

-   [Initialisieren des HTTP-Dienstanbieter](#initialize-the-http-service)
-   [Die zu überwachenden URLs registrieren](#register-the-urls-to-listen-on)
-   [Aufrufen der Routine zum Empfangen einer Anforderung](#call-the-routine-to-receive-a-request)
-   [Anforderung empfangen](#receive-the-request)
-   [Verarbeiten der HTTP-Anforderung](#handle-the-http-request)
-   [Senden der HTTP-Antwort](#send-the-http-response)
-   [Senden der HTTP-Post-Antwort](#send-the-http-post-response)
-   [Bereinigen der HTTP-Server-API](#clean-up-the-http-server-api)

## <a name="initialize-the-http-service"></a>Initialisieren des HTTP-Dienstanbieter

Der HTTP-Dienst wird mit der [**httpinitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) -Funktion initialisiert, und das Handle für die Anforderungs Warteschlange wird mithilfe von [**httpkreatehttphandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle)erstellt. Der Server muss initialisiert werden, bevor andere Serverfunktionen aufgerufen werden können. Die Anforderungs Warteschlange muss erstellt werden, bevor der Dienst URLs registrieren kann, um auf eingehende HTTP-Anforderungen zu lauschen.

Weitere Informationen und ein Codebeispiel finden Sie unter [Initialisieren des HTTP-Dienstanbieter](http-server-sample-application.md).

## <a name="register-the-urls-to-listen-on"></a>Die zu überwachenden URLs registrieren

Damit die HTTP-Server-API auf eingehende Anforderungen lauscht, werden bestimmte URLs durch Aufrufen der [**httpaddurl**](/windows/desktop/api/Http/nf-http-httpaddurl) -Funktion bei der API registriert. Eingehende Anforderungen, die diesen URLs entsprechen, werden an die in diesem-Befehl angegebene Anforderungs Warteschlange weitergeleitet.

Weitere Informationen und ein Codebeispiel finden Sie unter [Registrieren der URLs, die](http-server-sample-application.md)überwacht werden sollen.

## <a name="call-the-routine-to-receive-a-request"></a>Aufrufen der Routine zum Empfangen einer Anforderung

Die doreceiverequest-Funktion ordnet den Anforderungs Puffer zu, initialisiert die Anforderungs-ID und startet die Schleife zum Empfangen von Anforderungen.

Weitere Informationen und ein Codebeispiel finden Sie unter [Aufrufen der Routine, um eine Anforderung zu empfangen](http-server-sample-application.md).

## <a name="receive-the-request"></a>Anforderung empfangen

Die HTTP-Server-API stellt eine Anforderungs Struktur zum Speichern der analysierten eingehenden Anforderung bereit. Diese Struktur wird von der Anwendung zugeordnet und initialisiert, wenn eine eingehende Anforderung empfangen wird. Die Anwendung ruft die [**httpreceivehttprequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) -Funktion auf, um die Anforderung zu empfangen. Wenn der Anforderungs Puffer zu klein ist, um die Anforderung zu empfangen, kann die Anwendung die Puffergröße erhöhen und **httpreceivehttprequest** erneut abrufen, um die gesamte Anforderung zu empfangen.

Weitere Informationen und ein Codebeispiel finden Sie unter [receive a request](http-server-sample-application.md).

## <a name="handle-the-http-request"></a>Verarbeiten der HTTP-Anforderung

Die Beispielanwendung zeigt, wie HTTP Get-und Post-Anforderungs Verben behandelt werden. Die Anwendung sendet einen Fehler vom Typ 503 (**nicht \_ implementiert**), wenn Verben in der Anforderung vorhanden sind, die von der Anwendung nicht verarbeitet werden.

Beachten Sie, dass die URL, die bei der Verarbeitung von Anforderungen verwendet wird, die verarbeitete URL ist, die im **cookedurl** -Member der [**http- \_ Anforderung \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) -Struktur enthalten ist. Verwenden Sie nicht die nicht verarbeitete URL im **prawurl** -Member, der ausschließlich zu nach Verfolgungs-und statistischen Zwecken dient.

Weitere Informationen und ein Codebeispiel finden Sie unter [Umgang mit der HTTP-Anforderung](http-server-sample-application.md).

## <a name="send-the-http-response"></a>Senden der HTTP-Antwort

Die Antwort Struktur wird zugeordnet und mit dem Statuscode und einem Reason-Ausdruck im Makro "http-Antwort initialisieren" initialisiert \_ \_ . Ein bekannter HTTP-Header wird der Antwort Struktur im Add \_ known \_ Header-Makro hinzugefügt, und der Entitäts Text wird der Antwort aus einem Datenblock aus dem Arbeitsspeicher hinzugefügt. Die [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) -Funktion wird aufgerufen, um die Antwort zu senden. In diesem Beispiel sendet die Anwendung eine einfache 200 OK-Antwort an die Get-Anforderung.

Weitere Informationen und ein Codebeispiel finden Sie unter [Senden einer HTTP-Antwort](http-server-sample-application.md).

## <a name="send-the-http-post-response"></a>Senden der HTTP-Post-Antwort

Die Post-Anforderung erfordert mehr Verarbeitungsvorgänge als die Get-Anforderung. Der Anforderungs Entitäts Text wird durch Aufrufen der [**httpreceiverequestentitybody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) -Funktion empfangen. Die Anwendung sendet die Antwort und den Antwort Entitäts Text in separaten Aufrufen an die HTTP-Server-API. Die Antwortheader werden mit [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)gesendet. Der Entitäts Text wird in einem Datenblock von einem Datei Handle mit der [**httpsendresponabentitybody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) -Funktion gesendet.

Weitere Informationen und ein Codebeispiel finden Sie unter [Senden einer HTTP Post-Antwort](http-server-sample-application.md).

## <a name="clean-up-the-http-server-api"></a>Bereinigen der HTTP-Server-API

Die Bereinigungs Vorgänge für die HTTP-Server-API umfassen Folgendes:

-   Alle registrierten URLs werden entfernt.
-   Schließen des Handles für die Anforderungs Warteschlange.
-   Beenden der von der HTTP-Server-API erstellten Ressourcen.

Die Anwendung ruft die [**httpremoveurl**](/windows/desktop/api/Http/nf-http-httpremoveurl) -Funktion auf, um die von der ursprünglichen [**httpaddurl**](/windows/desktop/api/Http/nf-http-httpaddurl) -Funktion registrierten URLs aufzuheben. Die Anwendung ruft auch [**httpend**](/windows/desktop/api/Http/nf-http-httpterminate) für jeden Aufruf von [**httpinitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) mit passenden Flageinstellungen auf. Dieser Befehl beendet alle Ressourcen, die durch den **httpinitialize**-Rückruf erstellt wurden.

Weitere Informationen und ein Codebeispiel finden Sie unter [Bereinigen der HTTP-Server-API](http-server-sample-application.md).

 

 




