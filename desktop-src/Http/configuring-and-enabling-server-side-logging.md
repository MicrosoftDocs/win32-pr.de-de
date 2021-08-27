---
title: Konfigurieren und Aktivieren der serverseitigen Protokollierung
description: Konfigurieren und Aktivieren der serverseitigen Protokollierung
ms.assetid: d67d8f9a-6d8a-43f2-a1ef-75f69c04b1ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c95856cf72379de44211f05bb78fb4c6839f77b2fd6c42b91b26068bc9c5d0d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050810"
---
# <a name="configuring-and-enabling-server-side-logging"></a>Konfigurieren und Aktivieren der serverseitigen Protokollierung

Die Anwendung aktiviert die Protokollierung in der Serversitzung oder der URL-Gruppe, bevor die Antwort mit [**HttpSendHttpResponse gesendet wird.**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) Das folgende Beispiel zeigt das Konfigurieren und Aktivieren der serverseitigen Protokollierung des W3C-Typs:

1.  Die Anwendung initialisiert die [**HTTP \_ LOGGING \_ INFO-Struktur**](/windows/desktop/api/Http/ns-http-http_logging_info) mit **HttpLoggingTypeW3C,** das im **Format-Member** angegeben ist, und einer Bitmaske der HTTP [**LOG \_ \_ FIELD-Konstanten**](http-log-field--constants.md) im **Fields-Member.**
2.  Die Anwendung ruft [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) oder [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) mit **httpServerLoggingProperty** auf, die im *Property-Parameter* angegeben ist, und einen Zeiger auf die [**HTTP LOGGING \_ \_ INFO-Struktur**](/windows/desktop/api/Http/ns-http-http_logging_info) im *pPropertyInformation-Parameter.*

Die Bitmaske der [**HTTP \_ LOG \_ FIELD-Konstanten**](http-log-field--constants.md) enthält die Felder, die möglicherweise in der W3C-Protokolldatei protokolliert werden. Beachten Sie, dass das Festlegen der **HttpServerLoggingProperty-Eigenschaft** für eine Serversitzung oder eine URL-Gruppe nicht bedeutet, dass HTTP-Antworten protokolliert werden. Die Protokollierung erfolgt auf Anforderungsbasis, wenn W3C im Aufruf von [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) oder [**HttpSendResponseEntityBody aktiviert ist.**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)

Um die W3C-Antwortprotokollierung pro Anforderung zu aktivieren, führt die Anwendung die folgenden Schritte aus:

1.  Die Anwendung initialisiert die Member der [**HTTP \_ LOG FIELDS \_ \_ DATA**](/windows/desktop/api/Http/ns-http-http_log_fields_data) mit den Feldinformationen, die für diese Antwort protokolliert werden.
2.  Der **Base.Type-Member** der [**HTTP LOG FIELDS \_ \_ \_ DATA-Struktur**](/windows/desktop/api/Http/ns-http-http_log_fields_data) sollte mit **HttpLogDataTypeFields initialisiert werden.** Das **Feld Base.Type** stellt die zukünftige Erweiterbarkeit der Struktur und API sicher.
3.  Die Anwendung ruft [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) oder [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) mit einem Zeiger auf die [**HTTP LOG FIELDS \_ \_ \_ DATA-Struktur**](/windows/desktop/api/Http/ns-http-http_log_fields_data) im *pLogData-Parameter* auf. Die Anwendung sollte den Zeiger in [**PHTTP \_ LOG DATA um \_ casten.**](/windows/desktop/api/Http/ns-http-http_log_data)

 

 




