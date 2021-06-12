---
title: Ressourcendatensätze
description: Erfahren Sie mehr über Ressourcendatensätze. Ein Ressourceneintrag ist die Informationseinheit in DNS-Zonendateien, die zum Auflösen aller DNS-Abfragen verwendet wird.
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84bd000e2d88884bbb387748eaced1d0d58a324
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010673"
---
# <a name="resource-records"></a><span data-ttu-id="15fd1-104">Ressourcendatensätze</span><span class="sxs-lookup"><span data-stu-id="15fd1-104">Resource Records</span></span>

<span data-ttu-id="15fd1-105">Ein Ressourceneintrag, der häufig als RR bezeichnet wird, ist die Informationseinheit in DNS-Zonendateien. RRs sind die grundlegenden Bausteine von Hostnamen und IP-Informationen und werden verwendet, um alle DNS-Abfragen aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="15fd1-105">A resource record, commonly referred to as an RR, is the unit of information entry in DNS zone files; RRs are the basic building blocks of host-name and IP information and are used to resolve all DNS queries.</span></span> <span data-ttu-id="15fd1-106">Ressourcendatensätze sind so viele Typen vorhanden, dass erweiterte Namensauflösungsdienste zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="15fd1-106">Resource records exist as many types to provide extended name-resolution services.</span></span>

<span data-ttu-id="15fd1-107">Verschiedene Typen von RRs haben unterschiedliche Formate, da sie unterschiedliche Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="15fd1-107">Different types of RRs have different formats, as they contain different data.</span></span> <span data-ttu-id="15fd1-108">Im Allgemeinen verwenden viele RRs jedoch ein gemeinsames Format, wie im folgenden Beispiel für Adressressourcendatensätze veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="15fd1-108">In general, however, many RRs share a common format, as the following address resource records example illustrates.</span></span> <span data-ttu-id="15fd1-109">Im folgenden fiktiven Beispiel werden die Felder in einem A-Ressourcendatensatz erläutert:</span><span class="sxs-lookup"><span data-stu-id="15fd1-109">The following fictional example explains the fields found in an A resource record:</span></span>

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   <span data-ttu-id="15fd1-110">Das erste Feld (microsoft.com) gibt den Besitzer an.</span><span class="sxs-lookup"><span data-stu-id="15fd1-110">The first field (microsoft.com) denotes the owner.</span></span>
-   <span data-ttu-id="15fd1-111">Das zweite Feld (600) ist der Parameter für die Gültigkeitsdauer (Time-to-Live, TTL) in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="15fd1-111">The second field (600) is the time-to-live (TTL) parameter, in seconds.</span></span>
-   <span data-ttu-id="15fd1-112">Das dritte Feld (IN) ist das Klassenfeld, das die Protokollfamilie (fast immer IN) für die Internetklasse darstellt.</span><span class="sxs-lookup"><span data-stu-id="15fd1-112">The third field (IN) is the class field that represents the protocol family, which is almost always IN, for Internet class.</span></span>
-   <span data-ttu-id="15fd1-113">Das vierte Feld (A) ist der Typ der Ressource, die RR darstellt.</span><span class="sxs-lookup"><span data-stu-id="15fd1-113">The fourth field (A) is the type of resource the RR is representing.</span></span>
-   <span data-ttu-id="15fd1-114">Das fünfte Feld (150.150.150.1) ist die Ressourcendaten oder RDATA.</span><span class="sxs-lookup"><span data-stu-id="15fd1-114">The fifth field (150.150.150.1) is the resource data, or RDATA.</span></span> <span data-ttu-id="15fd1-115">Dieses Feld ist ein Variablentyp, der Informationen bereitstellt, die für den Typ der Ressource geeignet sind. In diesem Fall handelt es sich um eine 32-Bit-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="15fd1-115">This field is a variable type that provides information appropriate for the type of resource; in this case, it's a 32-bit IP address.</span></span>

<span data-ttu-id="15fd1-116">Die folgenden Ressourceneintragstypen werden häufig in DNS verwendet:</span><span class="sxs-lookup"><span data-stu-id="15fd1-116">The following resource record types are commonly used in DNS:</span></span>

-   <span data-ttu-id="15fd1-117">Autoritätsstart (SOA)</span><span class="sxs-lookup"><span data-stu-id="15fd1-117">Start of authority (SOA)</span></span>
-   <span data-ttu-id="15fd1-118">Namensserver (NS)</span><span class="sxs-lookup"><span data-stu-id="15fd1-118">Name server (NS)</span></span>
-   <span data-ttu-id="15fd1-119">[*Zeigerdatensatz*](p-gly.md) (PTR)</span><span class="sxs-lookup"><span data-stu-id="15fd1-119">[*Pointer record*](p-gly.md) (PTR)</span></span>
-   <span data-ttu-id="15fd1-120">Adresse (A)</span><span class="sxs-lookup"><span data-stu-id="15fd1-120">Address (A)</span></span>
-   <span data-ttu-id="15fd1-121">IPv6-Adresse (AAAA)</span><span class="sxs-lookup"><span data-stu-id="15fd1-121">IPv6 Address (AAAA)</span></span>
-   <span data-ttu-id="15fd1-122">E-Mail-Austausch (MX)</span><span class="sxs-lookup"><span data-stu-id="15fd1-122">Mail exchange (MX)</span></span>
-   <span data-ttu-id="15fd1-123">[*Kanonischer Name*](c-gly.md) (CNAME)</span><span class="sxs-lookup"><span data-stu-id="15fd1-123">[*Canonical name*](c-gly.md) (CNAME)</span></span>
-   <span data-ttu-id="15fd1-124">Windows Internet Naming Service (WINS)</span><span class="sxs-lookup"><span data-stu-id="15fd1-124">Windows Internet Naming Service (WINS)</span></span>
-   <span data-ttu-id="15fd1-125">WINS Reverse Look up (WINSR)</span><span class="sxs-lookup"><span data-stu-id="15fd1-125">WINS Reverse Look up (WINSR)</span></span>

<span data-ttu-id="15fd1-126">Es gibt viele andere Ressourceneintragstypen in DNS.</span><span class="sxs-lookup"><span data-stu-id="15fd1-126">There are many other resource record types in DNS.</span></span> <span data-ttu-id="15fd1-127">Weitere Informationen finden Sie unter [DNS-WMI-Anbieterreferenz.](dns-wmi-provider-reference.md)</span><span class="sxs-lookup"><span data-stu-id="15fd1-127">For more information, see [DNS WMI Provider Reference](dns-wmi-provider-reference.md).</span></span>

 

 




