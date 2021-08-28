---
title: HTTP-Servertasks
description: In der Regel werden HTTP-Serveraufgaben in einer bestimmten Reihenfolge ausgeführt. Das heißt, dass eine Aufgabe abgeschlossen und die Ausgabe abgerufen werden muss, bevor die nächste Aufgabe beginnt.
ms.assetid: 08f8e7e9-23b9-403f-b00c-8912919d65b1
keywords:
- HTTP-Servertasks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d89f72074ba870981421e228b0ff271505b3fce1e30cd49e79d58463570c0b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830060"
---
# <a name="http-server-tasks"></a>HTTP-Servertasks

In der Regel werden HTTP-Serveraufgaben in einer bestimmten Reihenfolge ausgeführt. Das heißt, dass eine Aufgabe abgeschlossen und die Ausgabe abgerufen werden muss, bevor die nächste Aufgabe beginnt.

Eine Aufgabenseite wird erstellt, um Beispielcode zu bestimmten Aufgaben anzuzeigen, die von einer HTTP-Serveranwendung ausgeführt werden. Eine Aufgabenseite enthält Links zur C-Erweiterungsdatei des HTTP-Serverbeispiels. Wenn Sie das PSDK auf Laufwerk C: \\ eines lokalen Computers installieren, wird die vollständige Serverbeispielanwendung unter C: \\ Programme Microsoft SDK Samples \\ \\ \\ netds http \\ server \\ installiert.

In der folgenden Liste sind die HTTP-Serveraufgaben aufgeführt:

-   [Initialisieren des HTTP-Diensts](#initialize-the-http-service)
-   [Registrieren der URLs zum Lauschen](#register-the-urls-to-listen-on)
-   [Aufrufen der Routine zum Empfangen einer Anforderung](#call-the-routine-to-receive-a-request)
-   [Empfangen der Anforderung](#receive-the-request)
-   [Verarbeiten der HTTP-Anforderung](#handle-the-http-request)
-   [Senden der HTTP-Antwort](#send-the-http-response)
-   [Senden der HTTP POST-Antwort](#send-the-http-post-response)
-   [Bereinigen der HTTP-Server-API](#clean-up-the-http-server-api)

## <a name="initialize-the-http-service"></a>Initialisieren des HTTP-Diensts

Der HTTP-Dienst wird mithilfe der [**HttpInitialize-Funktion initialisiert,**](/windows/desktop/api/Http/nf-http-httpinitialize) und das Handle für die Anforderungswarteschlange wird mit [**httpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle)erstellt. Der Server muss initialisiert werden, bevor andere Serverfunktionen aufgerufen werden können. Die Anforderungswarteschlange muss erstellt werden, bevor der Dienst URLs registrieren kann, um auf eingehende HTTP-Anforderungen zu lauschen.

Weitere Informationen und ein Codebeispiel finden Sie unter [Initialisieren des HTTP-Diensts.](http-server-sample-application.md)

## <a name="register-the-urls-to-listen-on"></a>Registrieren der URLs zum Lauschen

Damit die HTTP-Server-API auf eingehende Anforderungen lauscht, werden bestimmte URLs bei der API registriert, indem die [**HttpAddUrl-Funktion**](/windows/desktop/api/Http/nf-http-httpaddurl) aufgerufen wird. Eingehende Anforderungen, die diesen URLs entsprechen, werden an die in diesem Aufruf angegebene Anforderungswarteschlange weitergeleitet.

Weitere Informationen und ein Codebeispiel finden Sie unter [Registrieren der URLs zum Lauschen auf](http-server-sample-application.md).

## <a name="call-the-routine-to-receive-a-request"></a>Aufrufen der Routine zum Empfangen einer Anforderung

Die DoReceiveRequest-Funktion ordnet den Anforderungspuffer zu, initialisiert die Anforderungs-ID und startet die Schleife zum Empfangen von Anforderungen.

Weitere Informationen und ein Codebeispiel finden Sie unter [Aufrufen der Routine zum Empfangen einer Anforderung.](http-server-sample-application.md)

## <a name="receive-the-request"></a>Empfangen der Anforderung

Die HTTP-Server-API stellt eine Anforderungsstruktur zum Speichern der analysierten eingehenden Anforderung bereit. Diese Struktur wird von der Anwendung zugeordnet und initialisiert, wenn eine eingehende Anforderung empfangen wird. Die Anwendung ruft die [**HttpReceiveHttpRequest-Funktion**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) auf, um die Anforderung zu empfangen. Wenn der Anforderungspuffer zu klein ist, um die Anforderung zu empfangen, kann die Anwendung die Puffergröße erhöhen und **HttpReceiveHttpRequest** erneut aufrufen, um die gesamte Anforderung zu empfangen.

Weitere Informationen und ein Codebeispiel finden Sie unter [Empfangen einer Anforderung.](http-server-sample-application.md)

## <a name="handle-the-http-request"></a>Verarbeiten der HTTP-Anforderung

Die Beispielanwendung zeigt, wie die HTTP GET- und POST-Anforderungsverben behandelt werden. Die Anwendung sendet den Fehler 503 (**NOT \_ IMPLEMENTED**), wenn Verben in der Anforderung vorhanden sind, die von der Anwendung nicht verarbeitet werden.

Beachten Sie, dass die URL, die bei der Verarbeitung von Anforderungen verwendet werden soll, die verarbeitete URL ist, die im **CookedUrl-Member** der [**HTTP REQUEST \_ \_ V1-Struktur**](/windows/desktop/api/Http/ns-http-http_request_v1) enthalten ist. Verwenden Sie nicht die nicht verarbeitete URL im **pRawUrl-Member,** die ausschließlich zu Nachverfolgungs- und statistischen Zwecken dient.

Weitere Informationen und ein Codebeispiel finden Sie unter [Verarbeiten der HTTP-Anforderung.](http-server-sample-application.md)

## <a name="send-the-http-response"></a>Senden der HTTP-Antwort

Die Antwortstruktur wird zugeordnet und mit dem Statuscode und einem Grundphrase im INITIALIZE \_ HTTP \_ RESPONSE-Makro initialisiert. Ein bekannter HTTP-Header wird der Antwortstruktur im \_ ADD KNOWN \_ HEADER-Makro hinzugefügt, und der Entitätstext wird der Antwort aus einem Datenblock aus dem Arbeitsspeicher hinzugefügt. Die [**HttpSendHttpResponse-Funktion**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) wird aufgerufen, um die Antwort zu senden. In diesem Beispiel sendet die Anwendung eine einfache 200 OK-Antwort an die GET-Anforderung.

Weitere Informationen und ein Codebeispiel finden Sie unter [Senden einer HTTP-Antwort.](http-server-sample-application.md)

## <a name="send-the-http-post-response"></a>Senden der HTTP POST-Antwort

Die POST-Anforderung erfordert mehr Verarbeitung als die GET-Anforderung. Der Anforderungsentitätstext wird durch Aufrufen der [**HttpReceiveRequestEntityBody-Funktion**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) empfangen. Die Anwendung sendet die Antwort und den Antwortentitätstext in separaten Aufrufen an die HTTP-Server-API. Die Antwortheader werden mit [**httpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)gesendet. Der Entitätstext wird in einem Datenblock von einem Dateihandle mit der [**HttpSendResponseEntityBody-Funktion**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) gesendet.

Weitere Informationen und ein Codebeispiel finden Sie unter [Senden einer HTTP POST-Antwort.](http-server-sample-application.md)

## <a name="clean-up-the-http-server-api"></a>Bereinigen der HTTP-Server-API

Die Bereinigungsvorgänge für die HTTP-Server-API umfassen Folgendes:

-   Entfernen aller registrierten URLs.
-   Schließen des Handles für die Anforderungswarteschlange.
-   Beenden der von der HTTP-Server-API erstellten Ressourcen.

Die Anwendung ruft die [**HttpRemoveUrl-Funktion**](/windows/desktop/api/Http/nf-http-httpremoveurl) auf, um die Registrierung von URLs zu aufheben, die von der anfänglichen [**HttpAddUrl-Funktion**](/windows/desktop/api/Http/nf-http-httpaddurl) registriert wurden. Die Anwendung ruft auch [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) für jeden Aufruf von [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) mit übereinstimmenden Flageinstellungen auf. Dieser Aufruf beendet alle Ressourcen, die durch den Aufruf von **HttpInitialize** erstellt wurden.

Weitere Informationen und ein Codebeispiel finden Sie unter [Bereinigen der HTTP-Server-API.](http-server-sample-application.md)

 

 




