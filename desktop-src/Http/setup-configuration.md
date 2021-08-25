---
title: Setupkonfiguration
description: Die Setupkonfiguration erfordert Administratorrechte und ist über Neustarts hinweg persistent.
ms.assetid: 96e9c069-829b-4615-b94b-3761bc541440
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d59065ff34e7998d9df0503f6ae7503d9d402def6053f8176ba5af5b6a9efa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996117"
---
# <a name="setup-configuration"></a>Setupkonfiguration

Die Setupkonfiguration erfordert Administratorrechte und ist über Neustarts hinweg persistent. In der Regel führt eine Setupanwendung, die mit Administratorrechten ausgeführt wird, eine solche persistente Konfiguration während des Setups durch, sodass Anwendungen dann mit niedrigeren Berechtigungen ausgeführt werden können, obwohl die permanente Konfiguration jederzeit erfolgen kann. Die Setupkonfiguration kann eine der folgenden vier Aktivitäten umfassen:

-   Erstellen einer URL-Reservierung. Mit der HTTP-API kann die Setupanwendung URL-Präfixe für Anforderungswarteschlangen reservieren, die bestimmten Anwendungen zugeordnet sind. Um eine URL zu reservieren, ruft die Setupanwendung die [**Funktion HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) auf, *deren ConfigId-Parameter* auf **HttpServiceConfigUrlAclInfo** festgelegt ist, und übergibt einen Zeiger im *pConfigInformation-Parameter* an eine [**\_ \_ \_ URLACL \_ SET-Struktur**](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_set) des HTTP-DIENSTs, die die Registrierungsinformationen enthält. Weitere Informationen finden Sie unter [Namespacereservierungen, Registrierungen und Routing.](namespace-reservations-registrations-and-routing.md)
-   Konfigurieren von SSL. Zum Konfigurieren von SSL ruft der Administrator die [**HttpSetServiceConfiguration-Funktion**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) auf, *deren ConfigId-Parameter* auf **HttpServiceConfigSSLCertInfo** festgelegt ist, und übergibt einen Zeiger im *pConfigInformation-Parameter* an eine [**HTTP SERVICE \_ \_ CONFIG SSL \_ \_ SET-Struktur,**](/windows/desktop/api/Http/ns-http-http_service_config_ssl_set) die die SSL-Zertifikatinformationen enthält.
-   Festlegen anderer persistenter HTTP-Serverkonfigurationen, z. B. der IP-Adressen, an denen der HTTP-Server lausiert, und des serverweiten Timeoutwerts. Weitere Informationen [finden Sie unter IP-Lauschenliste](ip-listen-list.md) [**und HTTP SERVICE \_ \_ CONFIG \_ TIMEOUT \_ SET**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set).

 

 




