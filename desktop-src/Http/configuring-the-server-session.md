---
title: Konfigurieren der Serversitzung
description: Konfigurieren der Serversitzung
ms.assetid: 1e4e9440-8d70-44df-90a7-2d5e25b2f680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d41c1606cce397c49a15c62dae10531edfde93f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090938"
---
# <a name="configuring-the-server-session"></a><span data-ttu-id="a9031-103">Konfigurieren der Serversitzung</span><span class="sxs-lookup"><span data-stu-id="a9031-103">Configuring the Server Session</span></span>

<span data-ttu-id="a9031-104">Die Serversitzungs-ID wird mit der [**HttpCreateServerSession-Funktion**](/windows/desktop/api/Http/nf-http-httpcreateserversession) erstellt und im Aufruf von [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)verwendet.</span><span class="sxs-lookup"><span data-stu-id="a9031-104">The server session ID is created with the [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) function, and used in the call to [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty).</span></span> <span data-ttu-id="a9031-105">Der *pPropertyInformation-Parameter* verweist auf die Konfigurationsstruktur für den festgelegten Eigenschaftentyp.</span><span class="sxs-lookup"><span data-stu-id="a9031-105">The *pPropertyInformation* parameter points to the configuration structure for the property type that is set.</span></span> <span data-ttu-id="a9031-106">Der *Parameter PropertyInformationLength* gibt die Größe der Konfigurationsstruktur in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="a9031-106">The *PropertyInformationLength* parameter specifies the size, in bytes, of the configuration structure.</span></span> <span data-ttu-id="a9031-107">Wenn Sie beispielsweise **httpServerTimeoutsProperty** festlegen, muss der **pPropertyInformation-Parameter** auf einen Puffer verweisen, der mindestens die Größe der [**HTTP \_ TIMEOUT \_ LIMIT \_ INFO-Struktur**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) aufweist.</span><span class="sxs-lookup"><span data-stu-id="a9031-107">For example, when setting the **HttpServerTimeoutsProperty** the **pPropertyInformation** parameter must point to a buffer that is at least the size of the [**HTTP\_TIMEOUT\_LIMIT\_INFO**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) structure.</span></span>

<span data-ttu-id="a9031-108">In der Regel erstellt eine HTTP-Anwendung eine einzelne Serversitzung und kann anwendungsweite Eigenschaften festlegen, z. B. eine globale Bandbreiteneinschränkungsgrenze, oder die zentralisierte Protokollierung für diese Serversitzung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a9031-108">Typically an HTTP application creates a single server session and may set application wide properties such as global bandwidth throttling limit or enable centralized logging on this server session.</span></span> <span data-ttu-id="a9031-109">[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) überschreibt die HTTP-Server-API-Konfigurationen für die aufrufende Anwendung. Sie wirkt sich nicht auf die HTTP-Server-API-weiten Eigenschaften aus.</span><span class="sxs-lookup"><span data-stu-id="a9031-109">[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) overrides the HTTP Server API configurations for the calling application; it does not affect the HTTP Server API-wide properties.</span></span> <span data-ttu-id="a9031-110">Die Serversitzungskonfigurationen werden durch Aufrufen von [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)abgefragt.</span><span class="sxs-lookup"><span data-stu-id="a9031-110">The server session configurations are queried by calling [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty).</span></span>

 

 




