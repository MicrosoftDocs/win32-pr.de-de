---
title: Server-Side Protokollierung
description: Die serverseitige Protokollierung ist in einer URL-Gruppe oder Server Sitzung verfügbar.
ms.assetid: e1fcd87f-382a-42bf-b53f-1e1cb1dbbfc5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b76548b296bcdbd343e4e259e0cf3c87537ef5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856492"
---
# <a name="server-side-logging"></a><span data-ttu-id="b51e3-103">Server-Side Protokollierung</span><span class="sxs-lookup"><span data-stu-id="b51e3-103">Server-Side Logging</span></span>

<span data-ttu-id="b51e3-104">Die serverseitige Protokollierung ist in einer URL-Gruppe oder Server Sitzung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b51e3-104">Server-side logging is available on a URL group or server session.</span></span> <span data-ttu-id="b51e3-105">Wenn die Protokollierung für eine Server Sitzung aktiviert ist, fungiert sie als zentralisierte Form der Protokollierung für alle URL-Gruppen in der Server Sitzung.</span><span class="sxs-lookup"><span data-stu-id="b51e3-105">When logging is enabled on a server session, it functions as centralized form of logging for all the URL groups under the server session.</span></span> <span data-ttu-id="b51e3-106">Wenn die Protokollierung für eine URL-Gruppe aktiviert ist, wird die Protokollierung nur bei Anforderungen ausgeführt, die an die URL-Gruppe weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="b51e3-106">When logging is enabled on a URL group, logging is performed only on requests that are routed to the URL Group.</span></span> <span data-ttu-id="b51e3-107">Die folgenden Protokollierungs Typen werden von der HTTP-Server-API unterstützt:</span><span class="sxs-lookup"><span data-stu-id="b51e3-107">The following types of logging are supported by the HTTP Server API:</span></span>

-   <span data-ttu-id="b51e3-108">[W3C-Protokollierung](w3c-logging.md): verfügbar in der Server Sitzung und der URL-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="b51e3-108">[W3C logging](w3c-logging.md): Available on the server session and URL group.</span></span>
-   <span data-ttu-id="b51e3-109">[NCSA-Protokollierung](ncsa-logging.md): verfügbar in der URL-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="b51e3-109">[NCSA logging](ncsa-logging.md): Available on the URL group.</span></span>
-   <span data-ttu-id="b51e3-110">[IIS-Protokollierung](iis-logging.md): verfügbar in der URL-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="b51e3-110">[IIS logging](iis-logging.md): Available on the URL group.</span></span>
-   <span data-ttu-id="b51e3-111">[Zentralisierte binäre Protokollierung](centralized-binary-logging.md): verfügbar in der Server Sitzung.</span><span class="sxs-lookup"><span data-stu-id="b51e3-111">[Centralized binary logging](centralized-binary-logging.md): Available on the server session.</span></span>

<span data-ttu-id="b51e3-112">Um das http-Protokollierungs Feature nutzen zu können, aktiviert und konfiguriert die Anwendung einen Protokollierungstyp für die Server Sitzung oder URL-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="b51e3-112">To take advantage of the HTTP logging feature, the application enables and configures one type of logging on the server session or URL group.</span></span> <span data-ttu-id="b51e3-113">Weitere Informationen finden Sie unter [Konfigurieren und Aktivieren der Server seitigen Protokollierung](configuring-and-enabling-server-side-logging.md) .</span><span class="sxs-lookup"><span data-stu-id="b51e3-113">For more information, see [Configuring and Enabling Server Side Logging](configuring-and-enabling-server-side-logging.md)</span></span>

 

 




