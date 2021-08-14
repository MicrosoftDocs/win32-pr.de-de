---
title: Verarbeiten von Anforderungen
description: Die Verarbeitung von Anforderungen umfasst vier Schritte.
ms.assetid: fb170d73-c26d-4bec-abed-b614b7dad322
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea69ca4e431a4ff1841f08913b33bcb7dd57128f327aaeeac158fb62ea7a7b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996249"
---
# <a name="processing-requests"></a>Verarbeiten von Anforderungen

Die Verarbeitung von Anforderungen umfasst vier Schritte:

-   Empfangen einer Anforderung
-   Behandeln der Anforderung
-   Senden der Antwort
-   Abbrechen von Anforderungen, die nicht verarbeitet werden können

![Diagramm, das die Prozessanforderungsschleife zeigt.](images/processloop.png)

## <a name="receiving-a-request"></a>Empfangen einer Anforderung

Die HTTP-Server-API stellt eine Anforderungsstruktur zum Speichern der analysierten eingehenden Anforderung bereit. Diese Struktur wird von der Anwendung zugeordnet und initialisiert, wenn eine eingehende Anforderung empfangen wird. Die Anwendung ruft die [**HttpReceiveHttpRequest-Funktion auf,**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) um die Anforderung zu empfangen. Wenn der Anforderungspuffer zu klein ist, um die Anforderung zu empfangen, kann die Anwendung die Puffergröße erhöhen und **HttpReceiveHttpRequest** erneut aufrufen, um die gesamte Anforderung zu empfangen.

Wenn die Anforderung zu empfangende Entitätskörperdaten enthält, rufen die Anwendungen [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) mit der Anforderungs-ID auf, die während des Aufrufs von [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)im *pRequestBuffer-Parameter* zurückgegeben wird.

## <a name="handling-the-request"></a>Behandeln der Anforderung

Die Anwendung führt eine anwendungsspezifische Verarbeitung der Anforderung durch und formuliert eine Antwort. Die HTTP-Server-API erzwingt für diesen Prozess kein Timeout.

## <a name="sending-the-response"></a>Senden der Antwort

Wenn die Anwendung die Verarbeitung der Anforderung und das Formulieren der Antwort abgeschlossen hat, ruft sie die [**HttpSendHttpResponse-Funktion**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) auf, um die Antwort zu senden. Wenn die Antwort zu sendende Entitätskörperdaten enthält, ruft die Anwendung auch [HttpSendResponseEntityBody auf.](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)

## <a name="canceling-requests"></a>Abbrechen von Anforderungen

Nachdem die Anwendung eine Anforderungs-ID von ihrem Aufruf von [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)erhalten hat, kann sie die Anforderung jederzeit durch Aufrufen von [HttpCancelHttpRequest abbrechen.](/windows/desktop/api/Http/nf-http-httpcancelhttprequest)

 

 




