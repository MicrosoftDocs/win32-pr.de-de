---
title: Konfigurieren der HTTP-Server-API-Wide Timers
description: Konfigurieren der HTTP-Server-API-Wide Timers
ms.assetid: 34f80bac-a7c5-4949-9c15-ed63a3582e26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae91abb1c89419e99fa13273cd55b0783df3906a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206799"
---
# <a name="configuring-the-http-server-api-wide-timers"></a>Konfigurieren der HTTP-Server-API-Wide Timers

Der HTTP-Server-API-weite **headerwait** -und **idleconnection** -Timer werden durch Aufrufen der [**httpsetserviceconfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) -Funktion der Version 1,0 konfiguriert. Der *ConfigID* -Parameter ist auf " **httpserviceconfigtimeout** " festgelegt, und der *pconfiginformation* -Parameter gibt die [**http- \_ \_ Dienstkonfigurations- \_ Timeout \_ Satz**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set) Struktur an, die den festgelegten Timer und den Wert für den Timer enthält.

Das Konfigurieren der HTTP-Server-API-weiten Timeouts erfordert Administratorrechte, aber Abfragen nicht. Diese Konfigurationen werden für alle Anwendungen auf dem Computer festgelegt und bleiben erhalten, wenn der HTTP-Dienst neu gestartet oder der Computer neu gestartet wird. Um vorhandene API-weite Timeouts für http-Server abzufragen, ruft die Anwendung [**httpqueryserviceconfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration)auf.

 

 




