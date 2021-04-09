---
title: Verarbeiten von Anforderungen
description: Verarbeitungsanforderungen umfassen vier Schritte.
ms.assetid: fb170d73-c26d-4bec-abed-b614b7dad322
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e820d425e44daab9d687d1d43b756b833582a092
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "103869347"
---
# <a name="processing-requests"></a>Verarbeiten von Anforderungen

Verarbeitungsanforderungen umfassen vier Schritte:

-   Empfangen einer Anforderung
-   Verarbeiten der Anforderung
-   Senden der Antwort
-   Abbrechen von Anforderungen, die nicht verarbeitet werden können

![Diagramm, in dem die Prozess Anforderungs Schleife angezeigt wird.](images/processloop.png)

## <a name="receiving-a-request"></a>Empfangen einer Anforderung

Die HTTP-Server-API stellt eine Anforderungs Struktur zum Speichern der analysierten eingehenden Anforderung bereit. Diese Struktur wird von der Anwendung zugeordnet und initialisiert, wenn eine eingehende Anforderung empfangen wird. Die Anwendung ruft die [**httpreceivehttprequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) -Funktion auf, um die Anforderung zu empfangen. Wenn der Anforderungs Puffer zu klein ist, um die Anforderung zu empfangen, kann die Anwendung die Puffergröße erhöhen und **httpreceivehttprequest** erneut abrufen, um die gesamte Anforderung zu empfangen.

Wenn die Anforderung Entitäts Text Daten enthält, die empfangen werden sollen, ruft die Anwendung [**httpreceiverequestentitybody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) mit der Anforderungs-ID auf, die während des Aufrufs von [**httpreceivehttprequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)im *prequestbuffer* -Parameter zurückgegeben wurde.

## <a name="handling-the-request"></a>Verarbeiten der Anforderung

Die Anwendung führt die anwendungsspezifische Verarbeitung der Anforderung durch und formuliert eine Antwort. Die HTTP-Server-API erzwingt keinen Timeout für diesen Prozess.

## <a name="sending-the-response"></a>Senden der Antwort

Wenn die Anwendung die Verarbeitung der Anforderung und das Formulieren der Antwort abgeschlossen hat, ruft Sie die [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) -Funktion auf, um die Antwort zu senden. Wenn die Antwort Entitäts Text Daten enthält, die gesendet werden sollen, ruft die Anwendung auch [httpsendresponseentitybody](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)auf.

## <a name="canceling-requests"></a>Abbrechen von Anforderungen

Nachdem die Anwendung eine Anforderungs-ID von Ihrem Aufruf an [**httpreceivehttprequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)erhalten hat, kann Sie die Anforderung jederzeit abbrechen, indem Sie [httpcancelhttprequest](/windows/desktop/api/Http/nf-http-httpcancelhttprequest)aufruft.

 

 




