---
description: Automatische Tunnelung mit IPv4-kompatiblen Adressen und IPv6-zu-IPv4-Verbindungen arbeiten über eine Route für ein Präfix, das mit Schnittstelle 2 verknüpft ist \# . Die 32 Bits nach dem Präfix werden extrahiert und als IPv4-Zieladresse für das gekapselte Paket verwendet.
ms.assetid: 92261a1b-2b7f-4a76-b98a-2631dc303618
title: Automatisches IPv6-Tunnelung und IPv6-zu-IPv4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede1179902a7ec3276058e078d56e069603e54a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348183"
---
# <a name="ipv6-automatic-tunneling-and-6to4"></a><span data-ttu-id="9732b-104">Automatisches IPv6-Tunnelung und IPv6-zu-IPv4</span><span class="sxs-lookup"><span data-stu-id="9732b-104">IPv6 Automatic Tunneling and 6to4</span></span>

<span data-ttu-id="9732b-105">Automatische Tunnelung mit IPv4-kompatiblen Adressen und IPv6-zu-IPv4-Verbindungen arbeiten über eine Route für ein Präfix, das mit Schnittstelle 2 verknüpft ist \# .</span><span class="sxs-lookup"><span data-stu-id="9732b-105">Automatic tunneling with IPv4-compatible addresses and 6to4 both work through a route for a prefix that is on-link to interface \#2.</span></span> <span data-ttu-id="9732b-106">Die 32 Bits nach dem Präfix werden extrahiert und als IPv4-Zieladresse für das gekapselte Paket verwendet.</span><span class="sxs-lookup"><span data-stu-id="9732b-106">The 32 bits following the prefix are extracted and used as an IPv4 destination address for the encapsulated packet.</span></span>

<span data-ttu-id="9732b-107">Bei der automatischen Tunnelung wird das Präfix::/96 verwendet, das standardmäßig aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9732b-107">Automatic tunneling uses the ::/96 prefix, which is enabled by default.</span></span> <span data-ttu-id="9732b-108">Sie kann deaktiviert werden, indem Sie die Route für::/96 entfernen.</span><span class="sxs-lookup"><span data-stu-id="9732b-108">It can be disabled by removing the route for ::/96.</span></span>

<span data-ttu-id="9732b-109">IPv6-zu-IPv4 verwendet das Präfix 2002::/16, das nicht standardmäßig aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9732b-109">6to4 uses the 2002::/16 prefix, which is not enabled by default.</span></span>

 

 



