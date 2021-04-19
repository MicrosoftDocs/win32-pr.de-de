---
description: Gibt ein Präfix an, das mit Schnittstelle \# 4 verknüpft ist.
ms.assetid: cc3aa99d-cf45-460c-bdc1-3e9a19806fe4
title: IPv6-Site Präfixe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed8a21c59f9b6727c98ccb7fdacf4e9ec6ea5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345102"
---
# <a name="ipv6-site-prefixes"></a><span data-ttu-id="5c3d6-103">IPv6-Site Präfixe</span><span class="sxs-lookup"><span data-stu-id="5c3d6-103">IPv6 Site Prefixes</span></span>

<span data-ttu-id="5c3d6-104">Der IPv6-RTU-Befehl ermöglicht die Konfiguration veröffentlichter on-Link-Präfixe mit der Präfix Länge eines Standorts.</span><span class="sxs-lookup"><span data-stu-id="5c3d6-104">The ipv6 rtu command allows published on-link prefixes to be configured with a site prefix length.</span></span> <span data-ttu-id="5c3d6-105">Wenn angegeben, wird die Site Präfix Länge in Routerankündigungen in eine Präfix Informations Option eingefügt.</span><span class="sxs-lookup"><span data-stu-id="5c3d6-105">If specified, the site prefix length is put into a prefix information option in router advertisements.</span></span> <span data-ttu-id="5c3d6-106">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="5c3d6-106">For example:</span></span>

``` syntax
ipv6 rtu 2002:836b:9820:2::/64 4 pub life 1800 spl 48
```

<span data-ttu-id="5c3d6-107">Gibt ein Präfix an, das mit Schnittstelle \# 4 verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="5c3d6-107">specifies a prefix that is on-link to interface \#4.</span></span> <span data-ttu-id="5c3d6-108">Das Präfix wird veröffentlicht. Dies bedeutet, dass es in Routerankündigungen enthalten ist, wenn Schnittstelle \# 4 eine Werbe Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="5c3d6-108">The prefix is published, meaning that it is included in router advertisements if interface \#4 is an advertising interface.</span></span> <span data-ttu-id="5c3d6-109">Die Gültigkeitsdauer in der Option für die Präfix Informationen beträgt 1800 Sekunden (30 Minuten).</span><span class="sxs-lookup"><span data-stu-id="5c3d6-109">The lifetime in the prefix information option is 1800 seconds (30 minutes).</span></span> <span data-ttu-id="5c3d6-110">Die Präfix Länge der Site in der Option für Präfix Informationen ist 48.</span><span class="sxs-lookup"><span data-stu-id="5c3d6-110">The site prefix length in the prefix information option is 48.</span></span>

<span data-ttu-id="5c3d6-111">Der Empfang einer Präfix Informations Option, die ein Site Präfix angibt, bewirkt, dass ein Eintrag in der Site Prefix-Tabelle erstellt wird, der mit dem IPv6-SPT-Befehl angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5c3d6-111">The receipt of a prefix information option that specifies a site prefix causes an entry to be created in the site prefix table, which can be displayed by using the ipv6 spt command.</span></span> <span data-ttu-id="5c3d6-112">Die Site-Präfix Tabelle wird verwendet, um ungeeignete Site lokale Adressen von den von [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) und verwandten Funktionen zurückgegebenen Adressen zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="5c3d6-112">The site prefix table is used to remove inappropriate site-local addresses from those returned by the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and related functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c3d6-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5c3d6-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c3d6-114">IPv6-Verbindungs lokale und Standort lokale Adressen</span><span class="sxs-lookup"><span data-stu-id="5c3d6-114">IPv6 Link-local and Site-local Addresses</span></span>](link-local-and-site-local-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="5c3d6-115">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="5c3d6-115">Netsh.exe</span></span>](netsh-exe.md)
</dt> </dl>

 

 



