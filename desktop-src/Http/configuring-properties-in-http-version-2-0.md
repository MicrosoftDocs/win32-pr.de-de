---
title: Konfigurieren von Eigenschaften
description: Konfigurieren von Eigenschaften
ms.assetid: 9d659887-a696-4344-9c71-a2cc6131d8b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 681d5707840634f86da41d3e67a1014e93b8450c668cae9ea6f3129a0fe021f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047454"
---
# <a name="configuring-properties"></a>Konfigurieren von Eigenschaften

Mit der HTTP Server-API der Version 2.0 können Anwendungen Anforderungswarteschlangen, Serversitzungen und URL-Gruppen manuell konfigurieren. Die Serversitzung ist das Objekt der obersten Ebene, das Konfigurationsinformationen enthält, die für alle url-Gruppen gelten, die darunter erstellt wurden. Die Anwendung erstellt eine Serversitzung mit mindestens einer URL-Gruppe darunter und ordnet die URL-Gruppe dann einer Anforderungswarteschlange zu.

Weitere Informationen zu bestimmten Konfigurationsobjekten in der HTTP Server Version 2.0-API finden Sie unter:

-   [Konfigurieren der Serversitzung](configuring-the-server-session.md)
-   [Konfigurieren der URL-Gruppe](configuring-the-url-group.md)
-   [Konfigurieren der HTTP-Server-API-Wide Timer](configuring-the-http-server-api-wide-timers.md)

Eigenschaften für die Konfigurationsobjekte werden mit [**httpSetServerSessionProperty,**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) und [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) festgelegt, wie im folgenden Diagramm dargestellt. Die Zuordnung zwischen der Anforderungswarteschlange und der URL-Gruppe kann bei Bedarf geändert werden, während die Zuordnung zwischen der Serversitzung und den URL-Gruppen nicht geändert werden kann. Die URL-Gruppen müssen einer Anforderungswarteschlange zugeordnet werden, um Anforderungen zu empfangen.

![Eigenschaften für die Konfigurationsobjekte](images/configpropinv2.png)

In der folgenden Tabelle sind die Eigenschaften aufgeführt, die für jedes Konfigurationsobjekt festgelegt werden können. Wenn keine Eigenschaftenkonfiguration von der Anwendung festgelegt wird, gelten im Allgemeinen die STANDARDkonfigurationen der HTTP-Server-API. Die konfigurationseigenschaften, die von der Anwendung in der Serversitzung festgelegt werden, überschreiben die HTTP-Server-API-weiten Konfigurationen. Die für die URL-Gruppe festgelegten Konfigurationen überschreiben die Serversitzungskonfigurationen, und die Konfigurationen der Anforderungswarteschlange überschreiben die Standardkonfigurationen der HTTP-Server-API.



| Configuration-Objekt | Eigenschaft                                                                                                                                                      |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Serversitzung       | HttpServerStateProperty HttpServerLoggingProperty HttpServerQosProperty HttpServerTimeoutsProperty HttpServerAuthenticationProperty                           |
| URL-Gruppe            | HttpServerStateProperty HttpServerAuthenticationProperty HttpServerLoggingProperty HttpServerQosProperty HttpServerBindingProperty HttpServerTimeoutsProperty |
| Anforderungs-Warteschlange        | HttpServerStateProperty HttpServerQueueLengthProperty HttpServer503VerbosityProperty                                                                          |



 

Die Serversitzungseigenschaften werden in der [HTTP \_ SERVER \_ PROPERTY-Enumeration](/windows/desktop/api/Http/ne-http-http_server_property) definiert. In der folgenden Tabelle sind die Eigenschaftenstrukturen aufgeführt, die für jeden Eigenschaftstyp festgelegt werden, und die STANDARDeinstellung der HTTP-Server-API, wenn diese Eigenschaften nicht von der Anwendung festgelegt werden.



| Eigenschaft                                                    | Struktur                                                                     | HTTP-Server-API-Standard    |
|-------------------------------------------------------------|-------------------------------------------------------------------------------|----------------------------|
| HttpServerAuthenticatonProperty                             | [**\_ \_ HTTP-SERVERAUTHENTIFIZIERUNGSINFORMATIONEN \_**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) | Keine Authentifizierung          |
| HttpServerLoggingProperty                                   | [**\_HTTP-PROTOKOLLIERUNGSINFORMATIONEN \_**](/windows/desktop/api/Http/ns-http-http_logging_info)                              | Keine Protokollierung                 |
| HttpServerQosProperty->HttpQosSettingTypeConnectionLimit | [**\_INFORMATIONEN ZUM HTTP-VERBINDUNGSLIMIT \_ \_**](/windows/desktop/api/Http/ns-http-http_connection_limit_info)           | Keine Begrenzung                   |
| HttpServerTimeoutsProperty                                  | [**INFORMATIONEN \_ ZUM HTTP-TIMEOUTLIMIT \_ \_**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info)                 | 120 s.                   |
| HttpServerQosProperty->HttpQosSettingTypeBandwidth       | [**\_INFORMATIONEN ZUM HTTP-BANDBREITENLIMIT \_ \_**](/windows/desktop/api/Http/ns-http-http_bandwidth_limit_info)             | Keine Begrenzung                   |
| HttpServerQueueLengthProperty                               | ULONG                                                                         | 1000                       |
| HttpServerStateProperty                                     | [**HTTP \_ STATE \_ INFO**](/windows/desktop/api/Http/ns-http-http_state_info)                                  | Aktiviert                    |
| HttpServer503VerbosityProperty                              | [**HTTP \_ 503 \_ RESPONSE \_ VERBOSITY**](/windows/desktop/api/Http/ne-http-http_503_response_verbosity)         | HttpResponseVerbosityBasic |
| HttpServerBindingProperty                                   | [**\_HTTP-BINDUNGSINFORMATIONEN \_**](/windows/desktop/api/Http/ns-http-http_binding_info)                              | Keine                       |



 

In der folgenden Tabelle sind die Mindest- und Höchstwerte für die HTTP-Server-API-Konfigurationen aufgeführt.



| Eigenschaft                                              | HTTP-Server-API – Maximum und Minimum                        |
|-------------------------------------------------------|------------------------------------------------------------|
| HttpServerQosProperty->HttpQosSettingTypeBandwidth | Min = MIN \_ ALLOWED \_ BANDWIDTH \_ THROTTLING RATE Max = \_ none |
| HttpServerQueueLengthProperty                         | Min = 0xA Max = 0xFFFF                                     |



 

 

 




