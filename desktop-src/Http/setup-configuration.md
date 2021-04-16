---
title: Setup Konfiguration
description: Die Konfiguration des Setups erfordert Administratorrechte und ist bei Neustarts persistent.
ms.assetid: 96e9c069-829b-4615-b94b-3761bc541440
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43b543bfc81f963341d7b5f690f4b40312ee420
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515483"
---
# <a name="setup-configuration"></a>Setup Konfiguration

Die Konfiguration des Setups erfordert Administratorrechte und ist bei Neustarts persistent. In der Regel führt eine Setup Anwendung, die mit Administratorrechten ausgeführt wird, eine solche persistente Konfiguration während des Setups aus, sodass Anwendungen dann mit niedrigeren Berechtigungen ausgeführt werden können, obwohl eine persistente Konfiguration jederzeit möglich ist. Die Setup Konfiguration kann eine der folgenden vier Aktivitäten umfassen:

-   Erstellen einer URL-Reservierung. Die HTTP-API ermöglicht der Setup Anwendung das Reservieren von URL-Präfixen für Anforderungs Warteschlangen, die bestimmten Anwendungen zugeordnet sind. Um eine URL zu reservieren, ruft die Setup Anwendung die [**httpsetserviceconfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) -Funktion mit dem auf **httpserviceconfigurlaclinfo** festgelegten *ConfigID* -Parameter auf und übergibt einen Zeiger im *pconfiginformation* -Parameter an die Struktur der [**\_ \_ \_ urlacl- \_ Menge der HTTP-Dienst Konfiguration**](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_set) , die die Registrierungsinformationen enthält. Weitere Informationen finden Sie unter [Namespace Reservierungen, Registrierungen und Routing](namespace-reservations-registrations-and-routing.md).
-   Konfigurieren von SSL. Zum Konfigurieren von SSL ruft der Administrator die [**httpsetserviceconfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) -Funktion mit dem auf **httpserviceconfigsslcertinfo** festgelegten *ConfigID* -Parameter auf und übergibt einen Zeiger im *pconfiginformation* -Parameter an eine SSL-Set-Struktur der [**http- \_ Dienst \_ Konfiguration \_ \_**](/windows/desktop/api/Http/ns-http-http_service_config_ssl_set) , die die SSL-Zertifikat Informationen enthält.
-   Festlegen anderer HTTP-Server – Wide, persistente Konfigurationen, wie z. b. die IP-Adressen, die der HTTP-Server überwacht, und der Server weite Timeout Wert. Siehe [IP-](ip-listen-list.md) lausch Liste und [**\_ \_ Konfigurations \_ Timeout \_ für HTTP-Dienst**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set).

 

 




