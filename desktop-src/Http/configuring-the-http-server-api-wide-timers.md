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
# <a name="configuring-the-http-server-api-wide-timers"></a><span data-ttu-id="e1db8-103">Konfigurieren der HTTP-Server-API-Wide Timers</span><span class="sxs-lookup"><span data-stu-id="e1db8-103">Configuring the HTTP Server API Wide Timers</span></span>

<span data-ttu-id="e1db8-104">Der HTTP-Server-API-weite **headerwait** -und **idleconnection** -Timer werden durch Aufrufen der [**httpsetserviceconfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) -Funktion der Version 1,0 konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="e1db8-104">The HTTP Server API-wide **HeaderWait** and **IdleConnection** timers are configured by calling the version 1.0 [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) function.</span></span> <span data-ttu-id="e1db8-105">Der *ConfigID* -Parameter ist auf " **httpserviceconfigtimeout** " festgelegt, und der *pconfiginformation* -Parameter gibt die [**http- \_ \_ Dienstkonfigurations- \_ Timeout \_ Satz**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set) Struktur an, die den festgelegten Timer und den Wert für den Timer enthält.</span><span class="sxs-lookup"><span data-stu-id="e1db8-105">The *ConfigId* parameter is set to **HttpServiceConfigTimeout** and the *pConfigInformation* parameter specifies the [**HTTP\_SERVICE\_CONFIG\_TIMEOUT\_SET**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set) structure that contains the timer that is set and the value for the timer.</span></span>

<span data-ttu-id="e1db8-106">Das Konfigurieren der HTTP-Server-API-weiten Timeouts erfordert Administratorrechte, aber Abfragen nicht.</span><span class="sxs-lookup"><span data-stu-id="e1db8-106">Configuring the HTTP Server API-wide timeouts requires administrative privileges, however querying them does not.</span></span> <span data-ttu-id="e1db8-107">Diese Konfigurationen werden für alle Anwendungen auf dem Computer festgelegt und bleiben erhalten, wenn der HTTP-Dienst neu gestartet oder der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e1db8-107">These configurations are set for all applications on the computer and they persist when the HTTP service is restarted or the computer is restarted.</span></span> <span data-ttu-id="e1db8-108">Um vorhandene API-weite Timeouts für http-Server abzufragen, ruft die Anwendung [**httpqueryserviceconfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration)auf.</span><span class="sxs-lookup"><span data-stu-id="e1db8-108">To query existing HTTP Server API-wide timeouts, the application calls [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration).</span></span>

 

 




