---
title: Konfigurieren der Server Sitzung
description: .
ms.assetid: 1e4e9440-8d70-44df-90a7-2d5e25b2f680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcf069b22992fa178798c7f28545e30217d0dada
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340411"
---
# <a name="configuring-the-server-session"></a><span data-ttu-id="db1ac-103">Konfigurieren der Server Sitzung</span><span class="sxs-lookup"><span data-stu-id="db1ac-103">Configuring the Server Session</span></span>

<span data-ttu-id="db1ac-104">Die Server Sitzungs-ID wird mit der [**httpkreateserversession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) -Funktion erstellt und im [**httpsetserversessionproperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)-Befehl verwendet.</span><span class="sxs-lookup"><span data-stu-id="db1ac-104">The server session ID is created with the [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) function, and used in the call to [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty).</span></span> <span data-ttu-id="db1ac-105">Der *ppropertyinformation* -Parameter verweist auf die Konfigurations Struktur für den Eigenschaftentyp, der festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="db1ac-105">The *pPropertyInformation* parameter points to the configuration structure for the property type that is set.</span></span> <span data-ttu-id="db1ac-106">Der *propertyinformationlength* -Parameter gibt die Größe der Konfigurations Struktur in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="db1ac-106">The *PropertyInformationLength* parameter specifies the size, in bytes, of the configuration structure.</span></span> <span data-ttu-id="db1ac-107">Wenn Sie z. b. **httpservertimeoutsproperty** festlegen, muss der **ppropertyinformation** -Parameter auf einen Puffer verweisen, der mindestens die Größe der Informationsstruktur für das [**http- \_ Timeout \_ Limit \_**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) hat.</span><span class="sxs-lookup"><span data-stu-id="db1ac-107">For example, when setting the **HttpServerTimeoutsProperty** the **pPropertyInformation** parameter must point to a buffer that is at least the size of the [**HTTP\_TIMEOUT\_LIMIT\_INFO**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) structure.</span></span>

<span data-ttu-id="db1ac-108">In der Regel erstellt eine HTTP-Anwendung eine einzelne Server Sitzung und kann Anwendungs weite Eigenschaften festlegen, wie z. b. das Limit für die globale Bandbreitendrosselung oder die zentralisierte Protokollierung für diese Server Sitzung.</span><span class="sxs-lookup"><span data-stu-id="db1ac-108">Typically an HTTP application creates a single server session and may set application wide properties such as global bandwidth throttling limit or enable centralized logging on this server session.</span></span> <span data-ttu-id="db1ac-109">[**Httpsetserversessionproperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) überschreibt die HTTP-Server-API-Konfigurationen für die aufrufende Anwendung. Dies hat keine Auswirkung auf die API-weiten http-Server-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="db1ac-109">[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) overrides the HTTP Server API configurations for the calling application; it does not affect the HTTP Server API-wide properties.</span></span> <span data-ttu-id="db1ac-110">Die Server Sitzungs Konfigurationen werden durch Aufrufen von " [**httpqueryserversessionproperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)" abgefragt.</span><span class="sxs-lookup"><span data-stu-id="db1ac-110">The server session configurations are queried by calling [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty).</span></span>

 

 




