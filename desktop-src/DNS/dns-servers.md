---
title: DNS-Server
description: Ein DNS-Server ist ein Computer, der den Prozess der Namensauflösung in DNS abschließt.
ms.assetid: c7ce6e46-491c-482e-8d72-a79b911c3f68
keywords:
- DNS-Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 509ceeb811f221560540ae60f269c6ee1b05444f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712240"
---
# <a name="dns-servers"></a><span data-ttu-id="dcc66-104">DNS-Server</span><span class="sxs-lookup"><span data-stu-id="dcc66-104">DNS Servers</span></span>

<span data-ttu-id="dcc66-105">Ein *DNS-Server* ist ein Computer, der den Prozess der Namensauflösung in DNS abschließt.</span><span class="sxs-lookup"><span data-stu-id="dcc66-105">A *DNS Server* is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="dcc66-106">DNS-Server enthalten [*Zonendateien*](z-gly.md) , mit deren Hilfe Sie Namen in IP-Adressen und IP-Adressen in Namen auflösen können.</span><span class="sxs-lookup"><span data-stu-id="dcc66-106">DNS Servers contain [*zone files*](z-gly.md) that enable them to resolve names to IP addresses and IP addresses to names.</span></span> <span data-ttu-id="dcc66-107">Wenn eine Abfrage erfolgt, antwortet ein DNS-Server auf eine von drei Arten:</span><span class="sxs-lookup"><span data-stu-id="dcc66-107">When queried, a DNS Server will respond in one of three ways:</span></span>

-   <span data-ttu-id="dcc66-108">Der Server gibt die angeforderte Namensauflösung oder IP-Auflösungs Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="dcc66-108">The server returns the requested name-resolution or IP-resolution data.</span></span>
-   <span data-ttu-id="dcc66-109">Der Server gibt einen Zeiger auf einen anderen DNS-Server zurück, der die Anforderung bedienen kann.</span><span class="sxs-lookup"><span data-stu-id="dcc66-109">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="dcc66-110">Der Server gibt an, dass er nicht über die angeforderten Daten verfügt.</span><span class="sxs-lookup"><span data-stu-id="dcc66-110">The server indicates that it does not have the requested data.</span></span>

<span data-ttu-id="dcc66-111">DNS-Server können während der Vorbereitung der Rückgabe der angeforderten Auflösungs Daten möglicherweise andere DNS-Server Abfragen, aber darüber hinaus führen DNS-Server keine anderen Vorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="dcc66-111">DNS Servers might, during the course of preparing to return the requested resolution data, query other DNS Servers, but beyond that, DNS Servers do not perform any other operations.</span></span>

<span data-ttu-id="dcc66-112">Es gibt drei Hauptarten von DNS-Servern – primäre Server, sekundäre Server und Cache Server.</span><span class="sxs-lookup"><span data-stu-id="dcc66-112">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span>

## <a name="primary-server"></a><span data-ttu-id="dcc66-113">Primärer Server</span><span class="sxs-lookup"><span data-stu-id="dcc66-113">Primary Server</span></span>

<span data-ttu-id="dcc66-114">Der *primäre Server* ist der autorisierende Server für die Zone.</span><span class="sxs-lookup"><span data-stu-id="dcc66-114">The *primary server* is the authoritative server for the zone.</span></span> <span data-ttu-id="dcc66-115">Alle administrativen Aufgaben, die der Zone zugeordnet sind (z. b. das Erstellen von Unterdomänen innerhalb der Zone oder andere ähnliche administrative Aufgaben), müssen auf dem primären Server ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="dcc66-115">All administrative tasks associated with the zone (such as creating subdomains within the zone, or other similar administrative tasks) must be performed on the primary server.</span></span> <span data-ttu-id="dcc66-116">Außerdem müssen alle Änderungen, die der Zone oder Änderungen oder Erweiterungen in den Zonendateien zugeordnet sind, auf dem primären Server vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="dcc66-116">In addition, any changes associated with the zone or any modifications or additions to RRs in the zone files must be made on the primary server.</span></span> <span data-ttu-id="dcc66-117">Für eine beliebige Zone gibt es einen primären Server, außer wenn Sie Active Directory-Dienste und den Microsoft DNS-Server integrieren.</span><span class="sxs-lookup"><span data-stu-id="dcc66-117">For any given zone, there is one primary server, except when you integrate Active Directory services and Microsoft DNS Server.</span></span>

## <a name="secondary-servers"></a><span data-ttu-id="dcc66-118">Sekundäre Server</span><span class="sxs-lookup"><span data-stu-id="dcc66-118">Secondary Servers</span></span>

<span data-ttu-id="dcc66-119">*Sekundäre Server* sind Sicherungs-DNS-Server.</span><span class="sxs-lookup"><span data-stu-id="dcc66-119">*Secondary servers* are backup DNS Servers.</span></span> <span data-ttu-id="dcc66-120">Sekundäre Server erhalten alle Ihre Zonendateien aus den Zonendateien des primären Servers in einer Zonen Übertragung.</span><span class="sxs-lookup"><span data-stu-id="dcc66-120">Secondary servers receive all of their zone files from the primary server zone files in a zone transfer.</span></span> <span data-ttu-id="dcc66-121">Für eine beliebige Zone können mehrere sekundäre Server vorhanden sein – so viele, wie Sie für den [*Lastenausgleich*](l-gly.md), die [*Fehlertoleranz*](f-gly.md)und die Verringerung des Datenverkehrs erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="dcc66-121">Multiple secondary servers can exist for any given zone — as many as necessary to provide [*load balancing*](l-gly.md), [*fault tolerance*](f-gly.md), and traffic reduction.</span></span> <span data-ttu-id="dcc66-122">Außerdem kann es sich bei einem DNS-Server um einen sekundären Server für mehrere Zonen handeln.</span><span class="sxs-lookup"><span data-stu-id="dcc66-122">Additionally, any given DNS Server can be a secondary server for multiple zones.</span></span>

<span data-ttu-id="dcc66-123">Zusätzlich zu primären und sekundären DNS-Servern können zusätzliche DNS-Server Rollen verwendet werden, wenn solche Server für eine DNS-Infrastruktur geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="dcc66-123">In addition to primary and secondary DNS Servers, additional DNS Server roles can be used when such servers are appropriate for a DNS infrastructure.</span></span> <span data-ttu-id="dcc66-124">Diese zusätzlichen Server sind [*Caching-Server*](f-gly.md)und-Weiterleitungen.</span><span class="sxs-lookup"><span data-stu-id="dcc66-124">These additional servers are caching servers and [*forwarders*](f-gly.md).</span></span>

## <a name="caching-servers"></a><span data-ttu-id="dcc66-125">Zwischenspeichern von Servern</span><span class="sxs-lookup"><span data-stu-id="dcc66-125">Caching Servers</span></span>

<span data-ttu-id="dcc66-126">Zwischen speichernde [*Server*](c-gly.md), die auch als nur für das Caching bezeichnete Server bezeichnet werden, werden wie Ihr Name vorgeschlagen. Sie stellen nur den Cache-Query-Dienst für DNS-Antworten bereit.</span><span class="sxs-lookup"><span data-stu-id="dcc66-126">[*Caching servers*](c-gly.md), also known as caching-only servers, perform as their name suggests; they provide only cached-query service for DNS responses.</span></span> <span data-ttu-id="dcc66-127">Anstatt Zonendateien wie andere sekundäre Server zu verwalten, führen zwischen Speicherungs-DNS-Server Abfragen aus, speichern die Antworten zwischen und geben die Ergebnisse an den Abfrage Client zurück.</span><span class="sxs-lookup"><span data-stu-id="dcc66-127">Rather than maintaining zone files like other secondary servers do, caching DNS Servers perform queries, cache the answers, and return the results to the querying client.</span></span> <span data-ttu-id="dcc66-128">Der Hauptunterschied zwischen Cache Servern und anderen sekundären Servern besteht darin, dass andere sekundäre Server Zonendateien verwalten (und ggf. Zonenübertragungen durchführen, um den Netzwerk Datenverkehr zu erzeugen), nicht zwischen Speicherungs Servern.</span><span class="sxs-lookup"><span data-stu-id="dcc66-128">The primary difference between caching servers and other secondary servers is that other secondary servers maintain zone files (and do zone transfers when appropriate, thereby generating network traffic associated with the transfer), caching servers do not.</span></span>

 

 




