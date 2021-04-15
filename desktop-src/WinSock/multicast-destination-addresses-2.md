---
description: Beim Senden an eine Multicast Zieladresse erfordert das Microsoft IPv6-Protokoll normalerweise, dass für die Anwendung eine ausgehende Schnittstelle angegeben ist.
ms.assetid: dbfeaa1f-a7c5-4a15-90f0-4d1cdaf798e9
title: IPv6-Multicast Zieladressen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8aa516713fb47f6af03d8564c464a07a19cf0f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484934"
---
# <a name="ipv6-multicast-destination-addresses"></a><span data-ttu-id="11686-103">IPv6-Multicast Zieladressen</span><span class="sxs-lookup"><span data-stu-id="11686-103">IPv6 Multicast Destination Addresses</span></span>

<span data-ttu-id="11686-104">Beim Senden an eine Multicast Zieladresse erfordert das Microsoft IPv6-Protokoll normalerweise, dass für die Anwendung eine ausgehende Schnittstelle angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="11686-104">When sending to a multicast destination address, the Microsoft IPv6 protocol normally requires that the application have an outgoing interface specified.</span></span> <span data-ttu-id="11686-105">Dies erfolgt mit der **IPv6- \_ Multicast Option \_ if** Socket oder durch Binden des Sockets an eine bestimmte Quelladresse.</span><span class="sxs-lookup"><span data-stu-id="11686-105">This is done with the **IPV6\_MULTICAST\_IF** socket option or by binding the socket to a specific source address.</span></span>

<span data-ttu-id="11686-106">Sie können auch eine Standardschnittstelle für eine bestimmte Multicast Adresse, einen gesamten Multicast Adressbereich oder alle Multicast Adressen angeben.</span><span class="sxs-lookup"><span data-stu-id="11686-106">You can also specify a default interface for a specific multicast address, an entire multicast address scope, or all multicast addresses.</span></span> <span data-ttu-id="11686-107">Dies erfolgt mit einer Route, bei der das Multicast-Präfix für den Link zur gewünschten ausgehenden Schnittstelle platziert wird.</span><span class="sxs-lookup"><span data-stu-id="11686-107">This is done with a route that places the multicast prefix on-link to the desired outgoing interface.</span></span> <span data-ttu-id="11686-108">In den folgenden Beispielen wird gezeigt, wie dies angegeben werden kann:</span><span class="sxs-lookup"><span data-stu-id="11686-108">For following examples show how this can be specified:</span></span>

``` syntax
ipv6 rtu ff02::5/128 3
ipv6 rtu ff0e::/16 3
ipv6 rtu ff00::/8 3
```

 

 



