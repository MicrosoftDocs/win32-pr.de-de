---
title: Konfigurieren von Eigenschaften
description: Konfigurieren von Eigenschaften
ms.assetid: 9d659887-a696-4344-9c71-a2cc6131d8b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f898467f92f669596b4a8b1a4e68581c343ea883
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388282"
---
# <a name="configuring-properties"></a>Konfigurieren von Eigenschaften

Die HTTP-Server Version 2,0-API ermöglicht es Anwendungen, Anforderungs Warteschlangen, Server Sitzungen und URL-Gruppen manuell zu konfigurieren. Die Server Sitzung ist das Objekt der obersten Ebene, das Konfigurationsinformationen enthält, die für alle unter Ihnen erstellten URL-Gruppen gelten. Die Anwendung erstellt eine Server Sitzung mit einer oder mehreren URL-Gruppen darunter und ordnet die URL-Gruppe dann einer Anforderungs Warteschlange zu.

Weitere Informationen zu bestimmten Konfigurationsobjekten in der HTTP Server-API, Version 2,0, finden Sie unter:

-   [Konfigurieren der Server Sitzung](configuring-the-server-session.md)
-   [Konfigurieren der URL-Gruppe](configuring-the-url-group.md)
-   [Konfigurieren der HTTP-Server-API-Wide Timers](configuring-the-http-server-api-wide-timers.md)

Eigenschaften für die Konfigurationsobjekte werden wie in der folgenden Abbildung dargestellt mit der [**httpsetserversessionproperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty), der [**httpseturlgroupproperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) und der [**httpsetrequestqueueproperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) festgelegt. Die Zuordnung zwischen der Anforderungs Warteschlange und der URL-Gruppe kann bei Bedarf geändert werden, während die Zuordnung zwischen der Server Sitzung und den URL-Gruppen nicht geändert werden kann. Die URL-Gruppen müssen mit einer Anforderungs Warteschlange verknüpft werden, um Anforderungen zu empfangen.

![Eigenschaften für die Konfigurationsobjekte](images/configpropinv2.png)

In der folgenden Tabelle werden die Eigenschaften aufgelistet, die für jedes Konfigurationsobjekt festgelegt werden können. Wenn von der Anwendung keine Eigenschaften Konfiguration festgelegt wird, gelten im Allgemeinen die Standardkonfigurationen der HTTP-Server-API. Die Konfigurations Eigenschaften, die von der Anwendung in der Server Sitzung festgelegt werden, überschreiben die API-weiten http-Server-Konfigurationen. Die Konfigurationen, die für die URL-Gruppe festgelegt sind, überschreiben die Server Sitzungs Konfigurationen, und die Konfigurationen der Anforderungs Warteschlange setzen die Standardkonfigurationen der http



| Configuration-Objekt | Eigenschaft                                                                                                                                                      |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Server Sitzung       | Httpserverstateproperty httpserverloggingproperty httpserverqosproperty httpservertimeoutsproperty httpserverauthenticationproperty                           |
| URL-Gruppe            | Httpserverstateproperty httpserverauthenticationproperty httpserverloggingproperty httpserverqosproperty httpserverqosproperty httpserverqosproperty httpservertimeoutsproperty |
| Anforderungs-Warteschlange        | Httpserverstateproperty httpserverqueuelengthproperty HttpServer503VerbosityProperty                                                                          |



 

Die Server Sitzungs Eigenschaften werden in der [http- \_ Server \_ Eigenschaft](/windows/desktop/api/Http/ne-http-http_server_property) Enumeration definiert. In der folgenden Tabelle werden die Eigenschaften Strukturen aufgelistet, die für jeden Eigenschaftentyp und die HTTP-Server-API-Standardeinstellung festgelegt werden, wenn diese Eigenschaften nicht durch die Anwendung festgelegt



| Eigenschaft                                                    | Struktur                                                                     | HTTP-Server-API-Standard    |
|-------------------------------------------------------------|-------------------------------------------------------------------------------|----------------------------|
| Httpserverauthentialisionproperty                             | [**HTTP- \_ Server \_ Authentifizierungs \_ Informationen**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) | Keine Authentifizierung          |
| Httpserverloggingproperty                                   | [**HTTP- \_ Protokollierungs \_ Informationen**](/windows/desktop/api/Http/ns-http-http_logging_info)                              | Keine Protokollierung                 |
| Httpserverqosproperty->httpqossettingtypeconnectionlimit | [**HTTP- \_ Verbindungs \_ Limit- \_ Informationen**](/windows/desktop/api/Http/ns-http-http_connection_limit_info)           | Keine Begrenzung                   |
| Httpservertimeoutsproperty                                  | [**Informationen zum HTTP- \_ Timeout \_ Limit \_**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info)                 | 120 Sek.                   |
| Httpserverqosproperty->httpqossettingtypebandwidth       | [**Informationen zur HTTP- \_ Bandbreiten \_ Beschränkung \_**](/windows/desktop/api/Http/ns-http-http_bandwidth_limit_info)             | Keine Begrenzung                   |
| Httpserverqueuelengthproperty                               | ULONG                                                                         | 1000                       |
| Httpserverstateproperty                                     | [**HTTP- \_ Status \_ Informationen**](/windows/desktop/api/Http/ns-http-http_state_info)                                  | Aktiviert                    |
| HttpServer503VerbosityProperty                              | [**HTTP \_ 503- \_ Antwort \_ Ausführlichkeit**](/windows/desktop/api/Http/ne-http-http_503_response_verbosity)         | Httpresponseverbositybasic |
| Httpserverbindingproperty                                   | [**HTTP- \_ Bindungs \_ Informationen**](/windows/desktop/api/Http/ns-http-http_binding_info)                              | Keine                       |



 

In der folgenden Tabelle sind die minimalen und maximalen Werte für die HTTP-Server-API-Konfigurationen aufgeführt.



| Eigenschaft                                              | HTTP-Server-API Maximum und minimal                        |
|-------------------------------------------------------|------------------------------------------------------------|
| Httpserverqosproperty->httpqossettingtypebandwidth | Min = minimale \_ zulässige \_ Bandbreiten \_ Drosselung \_ Max = None |
| Httpserverqueuelengthproperty                         | Min = 0xa Max = 0xFFFF                                     |



 

 

 




