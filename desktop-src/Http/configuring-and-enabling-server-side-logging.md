---
title: Konfigurieren und Aktivieren der Server seitigen Protokollierung
description: Konfigurieren und Aktivieren der Server seitigen Protokollierung
ms.assetid: d67d8f9a-6d8a-43f2-a1ef-75f69c04b1ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e56247ee306d5a8804663e00162224df1d3f3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388285"
---
# <a name="configuring-and-enabling-server-side-logging"></a>Konfigurieren und Aktivieren der Server seitigen Protokollierung

Die Anwendung aktiviert die Protokollierung für die Server Sitzung oder die URL-Gruppe vor dem Senden der Antwort mit [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse). Das folgende Beispiel zeigt, wie Sie die serverseitige Protokollierung des W3C-Typs konfigurieren und aktivieren:

1.  Die Anwendung initialisiert die [**http- \_ Protokollierungs \_ Informations**](/windows/desktop/api/Http/ns-http-http_logging_info) Struktur mit **HttpLoggingTypeW3C** , die im **formatmember** angegeben ist, und eine Bitmaske der HTTP-  [**\_ Protokoll \_ Feld**](http-log-field--constants.md) Konstanten im Feld Element.
2.  Die Anwendung ruft [**httpsetserversessionproperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) oder [**httpseturlgroupproperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) auf, wobei **httpserverloggingproperty** im *Property* -Parameter angegeben ist, und ein Zeiger auf die [**http- \_ Protokollierungs \_**](/windows/desktop/api/Http/ns-http-http_logging_info) Informationsstruktur im *ppropertyinformation* -Parameter.

Die Bitmaske der [**http- \_ Protokoll \_ Feld**](http-log-field--constants.md) Konstanten enthält die Felder, die möglicherweise in der W3C-Protokolldatei protokolliert werden. Beachten Sie, dass das Festlegen der **httpserverloggingproperty** -Eigenschaft für eine Server Sitzung oder eine URL-Gruppe nicht bedeutet, dass HTTP-Antworten protokolliert werden. Die Protokollierung erfolgt pro Anforderung, wenn W3C im Befehl [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) oder [**httpsendresponabentitybody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)aktiviert ist.

Um die W3C-Antwort Protokollierung pro Anforderung zu aktivieren, führt die Anwendung die folgenden Schritte aus:

1.  Die Anwendung initialisiert die Member der [**http \_ Log Fields \_ - \_ Daten**](/windows/desktop/api/Http/ns-http-http_log_fields_data) mit den Feldinformationen, die für diese Antwort protokolliert werden.
2.  Der **base. Type** -Member der [**http \_ log \_ Fields- \_ Daten**](/windows/desktop/api/Http/ns-http-http_log_fields_data) Struktur sollte mit **httplogdatatypeer Fields** initialisiert werden. Das **base. Type** -Feld gewährleistet die zukünftige Erweiterbarkeit der Struktur und API.
3.  Die Anwendung ruft [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) oder [**httpsendresponseentitybody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) mit einem Zeiger auf die [**http \_ log \_ Fields- \_ Daten**](/windows/desktop/api/Http/ns-http-http_log_fields_data) Struktur im *plogdata* -Parameter auf. Die Anwendung muss den Zeiger in die [**Phttp- \_ Protokoll \_ Daten**](/windows/desktop/api/Http/ns-http-http_log_data)umwandeln.

 

 




