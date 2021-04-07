---
title: Ressourcen Einträge
description: Ein Ressourcen Daten Satz, der häufig als RR bezeichnet wird, ist die Eintrags Einheit in DNS-Zonendateien. RRS sind die grundlegenden Bausteine von Hostnamen-und IP-Informationen und werden verwendet, um alle DNS-Abfragen aufzulösen.
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05b667b95a8ede32018e1aad7de375e77a890487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712798"
---
# <a name="resource-records"></a><span data-ttu-id="7c81c-103">Ressourcen Einträge</span><span class="sxs-lookup"><span data-stu-id="7c81c-103">Resource Records</span></span>

<span data-ttu-id="7c81c-104">Ein Ressourcen Daten Satz, der häufig als RR bezeichnet wird, ist die Eintrags Einheit in DNS-Zonendateien. RRS sind die grundlegenden Bausteine von Hostnamen-und IP-Informationen und werden verwendet, um alle DNS-Abfragen aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="7c81c-104">A resource record, commonly referred to as an RR, is the unit of information entry in DNS zone files; RRs are the basic building blocks of host-name and IP information and are used to resolve all DNS queries.</span></span> <span data-ttu-id="7c81c-105">Ressourcen Einträge sind so viele Typen vorhanden, dass erweiterte Namensauflösungsdienste bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7c81c-105">Resource records exist as many types to provide extended name-resolution services.</span></span>

<span data-ttu-id="7c81c-106">Verschiedene Arten von RRS haben unterschiedliche Formate, da Sie unterschiedliche Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="7c81c-106">Different types of RRs have different formats, as they contain different data.</span></span> <span data-ttu-id="7c81c-107">Im allgemeinen weisen viele RRS jedoch ein allgemeines Format auf, wie im folgenden Beispiel für Adress Ressourcen Einträge veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="7c81c-107">In general, however, many RRs share a common format, as the following address resource records example illustrates.</span></span> <span data-ttu-id="7c81c-108">Im folgenden fiktiven Beispiel werden die Felder in einem Ressourcen Daten Satz erläutert:</span><span class="sxs-lookup"><span data-stu-id="7c81c-108">The following fictional example explains the fields found in an A resource record:</span></span>

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   <span data-ttu-id="7c81c-109">Das erste Feld (Microsoft.com) bezeichnet den Besitzer.</span><span class="sxs-lookup"><span data-stu-id="7c81c-109">The first field (microsoft.com) denotes the owner.</span></span>
-   <span data-ttu-id="7c81c-110">Das zweite Feld (600) ist der Gültigkeitsdauer Parameter (Time-to-Live, TTL) in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="7c81c-110">The second field (600) is the time-to-live (TTL) parameter, in seconds.</span></span>
-   <span data-ttu-id="7c81c-111">Das dritte Feld (in) ist das Klassenfeld, das die Protokollfamilie darstellt, die sich fast immer in für die Internet Klasse befindet.</span><span class="sxs-lookup"><span data-stu-id="7c81c-111">The third field (IN) is the class field that represents the protocol family, which is almost always IN, for Internet class.</span></span>
-   <span data-ttu-id="7c81c-112">Das vierte Feld (A) ist der Typ der Ressource, die der RR darstellt.</span><span class="sxs-lookup"><span data-stu-id="7c81c-112">The fourth field (A) is the type of resource the RR is representing.</span></span>
-   <span data-ttu-id="7c81c-113">Das fünfte Feld (150.150.150.1) ist die Ressourcen Daten bzw. rdata.</span><span class="sxs-lookup"><span data-stu-id="7c81c-113">The fifth field (150.150.150.1) is the resource data, or RDATA.</span></span> <span data-ttu-id="7c81c-114">Dieses Feld ist ein Variablentyp, der Informationen bereitstellt, die für den Ressourcentyp geeignet sind. in diesem Fall handelt es sich um eine 32-Bit-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="7c81c-114">This field is a variable type that provides information appropriate for the type of resource; in this case, it's a 32-bit IP address.</span></span>

<span data-ttu-id="7c81c-115">Die folgenden Ressourcen Daten Satz Typen werden häufig in DNS verwendet:</span><span class="sxs-lookup"><span data-stu-id="7c81c-115">The following resource record types are commonly used in DNS:</span></span>

-   <span data-ttu-id="7c81c-116">Autoritäts Anfang (SOA)</span><span class="sxs-lookup"><span data-stu-id="7c81c-116">Start of authority (SOA)</span></span>
-   <span data-ttu-id="7c81c-117">Namen Server (NS)</span><span class="sxs-lookup"><span data-stu-id="7c81c-117">Name server (NS)</span></span>
-   <span data-ttu-id="7c81c-118">[*Zeiger Daten Satz*](p-gly.md) (PTR)</span><span class="sxs-lookup"><span data-stu-id="7c81c-118">[*Pointer record*](p-gly.md) (PTR)</span></span>
-   <span data-ttu-id="7c81c-119">Adresse (A)</span><span class="sxs-lookup"><span data-stu-id="7c81c-119">Address (A)</span></span>
-   <span data-ttu-id="7c81c-120">IPv6-Adresse (AAAA)</span><span class="sxs-lookup"><span data-stu-id="7c81c-120">IPv6 Address (AAAA)</span></span>
-   <span data-ttu-id="7c81c-121">E-Mail-Austausch (MX)</span><span class="sxs-lookup"><span data-stu-id="7c81c-121">Mail exchange (MX)</span></span>
-   <span data-ttu-id="7c81c-122">[*Kanonischer Name*](c-gly.md) (CNAME)</span><span class="sxs-lookup"><span data-stu-id="7c81c-122">[*Canonical name*](c-gly.md) (CNAME)</span></span>
-   <span data-ttu-id="7c81c-123">Windows Internet Naming Service (WINS)</span><span class="sxs-lookup"><span data-stu-id="7c81c-123">Windows Internet Naming Service (WINS)</span></span>
-   <span data-ttu-id="7c81c-124">WINS-Reverse-Suche (WINSR)</span><span class="sxs-lookup"><span data-stu-id="7c81c-124">WINS Reverse Look up (WINSR)</span></span>

<span data-ttu-id="7c81c-125">Es gibt zahlreiche andere Ressourcen Daten Satz Typen in DNS.</span><span class="sxs-lookup"><span data-stu-id="7c81c-125">There are many other resource record types in DNS.</span></span> <span data-ttu-id="7c81c-126">Weitere Informationen finden Sie unter [DNS-WMI-Anbieter Referenz](dns-wmi-provider-reference.md).</span><span class="sxs-lookup"><span data-stu-id="7c81c-126">For more information, see [DNS WMI Provider Reference](dns-wmi-provider-reference.md).</span></span>

 

 




