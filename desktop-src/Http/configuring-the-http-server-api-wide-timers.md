---
title: Konfigurieren der HTTP-Server-API-Wide Timer
description: Konfigurieren der HTTP-Server-API-Wide Timer
ms.assetid: 34f80bac-a7c5-4949-9c15-ed63a3582e26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0eb5fc40bedd51884830893673b3bae2341a21110fa2c3b33878dba7a4aef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047350"
---
# <a name="configuring-the-http-server-api-wide-timers"></a>Konfigurieren der HTTP-Server-API-Wide Timer

Die HTTP-Server-API-weiten **HeaderWait-** und **IdleConnection-Timer** werden durch Aufrufen der [**HttpSetServiceConfiguration-Funktion**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) der Version 1.0 konfiguriert. Der *ConfigId-Parameter* ist auf **HttpServiceConfigTimeout** festgelegt, und der *pConfigInformation-Parameter* gibt die [**HTTP SERVICE \_ \_ CONFIG \_ TIMEOUT \_ SET-Struktur**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set) an, die den festgelegten Timer und den Wert für den Timer enthält.

Zum Konfigurieren der HTTP-Server-API-weiten Timeouts sind Administratorrechte erforderlich, das Abfragen ist jedoch nicht erforderlich. Diese Konfigurationen werden für alle Anwendungen auf dem Computer festgelegt und bleiben erhalten, wenn der HTTP-Dienst neu gestartet oder der Computer neu gestartet wird. Zum Abfragen vorhandener HTTP Server-API-weiter Timeouts ruft die Anwendung [**HttpQueryServiceConfiguration auf.**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration)

 

 




