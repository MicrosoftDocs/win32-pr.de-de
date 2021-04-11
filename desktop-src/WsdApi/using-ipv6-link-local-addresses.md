---
description: IPv6-Link-Local-Adressierung in SOAP-Nachrichten stellt eine eindeutige Herausforderung dar, da IPv6-Link-Local-Adressen erfordern, dass eine Bereichs-ID sinnvoll ist, die Bereichs-ID jedoch nur für den lokalen Computer Bedeutung ist.
ms.assetid: 63495335-e447-4564-b669-0896c7aac63f
title: Verwenden von IPv6-Link-Local-Adressen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c89356042e8a71b0af19337b7013b8abd1e8a354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130389"
---
# <a name="using-ipv6-link-local-addresses"></a><span data-ttu-id="6bd55-103">Verwenden von IPv6-Link-Local-Adressen</span><span class="sxs-lookup"><span data-stu-id="6bd55-103">Using IPv6 Link-Local Addresses</span></span>

<span data-ttu-id="6bd55-104">IPv6-Link-Local-Adressierung in SOAP-Nachrichten stellt eine eindeutige Herausforderung dar, da IPv6-Link-Local-Adressen erfordern, dass eine Bereichs-ID sinnvoll ist, die Bereichs-ID jedoch nur für den lokalen Computer Bedeutung ist.</span><span class="sxs-lookup"><span data-stu-id="6bd55-104">IPv6 link-local addressing in SOAP messages provides a unique challenge, as IPv6 link-local addresses require a scope ID to be meaningful, but the scope ID only has meaning for the local machine.</span></span> <span data-ttu-id="6bd55-105">Alle Client-und Geräte Implementierungen müssen die Bereichs-ID entfernen, bevor Sie eine IPv6-Link-Local-Adresse in einer SOAP-Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="6bd55-105">All client and device implementations must remove the scope ID before sending an IPv6 link-local address in a SOAP message.</span></span> <span data-ttu-id="6bd55-106">Wenn eine IPv6-Link-Local-Adresse in einer Nachricht empfangen wird, muss außerdem die Schnittstelle bekannt sein, auf der die Nachricht empfangen wurde, damit die gesamte Verknüpfungs lokale Adresse mit der Bereichs-ID rekonstruiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6bd55-106">Additionally, when an IPv6 link-local address is received in a message, the interface the message was received on must be known so the complete link local address with scope ID can be reconstructed.</span></span>

 

 



