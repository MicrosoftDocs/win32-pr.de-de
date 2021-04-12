---
description: Generische Winsock-Multipoint-Funktionen unterstützen IP-Multicast.
ms.assetid: 32fffca8-4f13-495b-afb6-bb57a9cce553
title: Multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97c6b4ece06119d01e2661028f452985bb20b068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129160"
---
# <a name="multicast"></a><span data-ttu-id="cc554-103">Multicast</span><span class="sxs-lookup"><span data-stu-id="cc554-103">Multicast</span></span>

<span data-ttu-id="cc554-104">Generische Winsock-Multipoint-Funktionen unterstützen IP-Multicast.</span><span class="sxs-lookup"><span data-stu-id="cc554-104">Generic Winsock multipoint functions support IP multicast.</span></span> <span data-ttu-id="cc554-105">Allerdings müssen die TCP/IP-Transportanbieter, die Multicast unterstützen, auch den BSD-Stil (Berkeley Software Distribution) – Multicast Unterstützung bereitstellen, indem die entsprechenden Multicast Optionen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="cc554-105">However, the TCP/IP transport providers that support multicast must also provide Berkeley Software Distribution (BSD) style–multicast support by supporting the corresponding multicast options.</span></span> <span data-ttu-id="cc554-106">Dies vereinfacht das Portieren vorhandener Multicast Anwendungen auf Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="cc554-106">This simplifies the porting of existing multicast applications to Windows Sockets 2.</span></span>

 

 



