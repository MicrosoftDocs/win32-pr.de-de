---
title: DNS-Server
description: Erfahren Sie mehr über DNS-Server. Ein DNS-Server ist ein Computer, der den Prozess der Namensauflösung in DNS ab schließt.
ms.assetid: c7ce6e46-491c-482e-8d72-a79b911c3f68
keywords:
- DNS-Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fe2415c50cdd2472b20e8f14123afa2aa919d26
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011253"
---
# <a name="dns-servers"></a><span data-ttu-id="a7aba-105">DNS-Server</span><span class="sxs-lookup"><span data-stu-id="a7aba-105">DNS Servers</span></span>

<span data-ttu-id="a7aba-106">Ein *DNS-Server* ist ein Computer, der den Prozess der Namensauflösung in DNS ab schließt.</span><span class="sxs-lookup"><span data-stu-id="a7aba-106">A *DNS Server* is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="a7aba-107">DNS-Server enthalten [*Zonendateien,*](z-gly.md) die es ihnen ermöglichen, Namen in IP-Adressen und IP-Adressen in Namen aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="a7aba-107">DNS Servers contain [*zone files*](z-gly.md) that enable them to resolve names to IP addresses and IP addresses to names.</span></span> <span data-ttu-id="a7aba-108">Bei der Abfrage antwortet ein DNS-Server auf eine von drei Arten:</span><span class="sxs-lookup"><span data-stu-id="a7aba-108">When queried, a DNS Server will respond in one of three ways:</span></span>

-   <span data-ttu-id="a7aba-109">Der Server gibt die angeforderten Namensauflösungs- oder IP-Auflösungsdaten zurück.</span><span class="sxs-lookup"><span data-stu-id="a7aba-109">The server returns the requested name-resolution or IP-resolution data.</span></span>
-   <span data-ttu-id="a7aba-110">Der Server gibt einen Zeiger auf einen anderen DNS-Server zurück, der die Anforderung ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="a7aba-110">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="a7aba-111">Der Server gibt an, dass er nicht über die angeforderten Daten verfügt.</span><span class="sxs-lookup"><span data-stu-id="a7aba-111">The server indicates that it does not have the requested data.</span></span>

<span data-ttu-id="a7aba-112">DNS-Server können während der Vorbereitung der Rückgabe der angeforderten Auflösungsdaten andere DNS-Server abfragen. Darüber hinaus führen DNS-Server jedoch keine anderen Vorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="a7aba-112">DNS Servers might, during the course of preparing to return the requested resolution data, query other DNS Servers, but beyond that, DNS Servers do not perform any other operations.</span></span>

<span data-ttu-id="a7aba-113">Es gibt drei Hauptarten von DNS-Servern: primäre Server, sekundäre Server und Cacheserver.</span><span class="sxs-lookup"><span data-stu-id="a7aba-113">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span>

## <a name="primary-server"></a><span data-ttu-id="a7aba-114">Primärer Server</span><span class="sxs-lookup"><span data-stu-id="a7aba-114">Primary Server</span></span>

<span data-ttu-id="a7aba-115">Der *primäre Server* ist der autoritative Server für die Zone.</span><span class="sxs-lookup"><span data-stu-id="a7aba-115">The *primary server* is the authoritative server for the zone.</span></span> <span data-ttu-id="a7aba-116">Alle administrativen Aufgaben, die der Zone zugeordnet sind (z. B. das Erstellen von Unterdomänen innerhalb der Zone oder andere ähnliche administrative Aufgaben), müssen auf dem primären Server ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a7aba-116">All administrative tasks associated with the zone (such as creating subdomains within the zone, or other similar administrative tasks) must be performed on the primary server.</span></span> <span data-ttu-id="a7aba-117">Darüber hinaus müssen alle Änderungen, die der Zone zugeordnet sind, oder Änderungen oder Ergänzungen von RRs in den Zonendateien auf dem primären Server vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="a7aba-117">In addition, any changes associated with the zone or any modifications or additions to RRs in the zone files must be made on the primary server.</span></span> <span data-ttu-id="a7aba-118">Für jede bestimmte Zone gibt es einen primären Server, außer wenn Sie Active Directory-Dienste und Microsoft DNS-Server integrieren.</span><span class="sxs-lookup"><span data-stu-id="a7aba-118">For any given zone, there is one primary server, except when you integrate Active Directory services and Microsoft DNS Server.</span></span>

## <a name="secondary-servers"></a><span data-ttu-id="a7aba-119">Sekundäre Server</span><span class="sxs-lookup"><span data-stu-id="a7aba-119">Secondary Servers</span></span>

<span data-ttu-id="a7aba-120">*Sekundäre Server* sind DNS-Sicherungsserver.</span><span class="sxs-lookup"><span data-stu-id="a7aba-120">*Secondary servers* are backup DNS Servers.</span></span> <span data-ttu-id="a7aba-121">Sekundäre Server empfangen alle ihre Zonendateien aus den Zonendateien des primären Servers in einer Zonenübertragung.</span><span class="sxs-lookup"><span data-stu-id="a7aba-121">Secondary servers receive all of their zone files from the primary server zone files in a zone transfer.</span></span> <span data-ttu-id="a7aba-122">Für jede Zone können mehrere sekundäre Server vorhanden [](l-gly.md)sein– so viele wie nötig, um Lastenausgleich, [*Fehlertoleranz*](f-gly.md)und Datenverkehrsreduzierung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a7aba-122">Multiple secondary servers can exist for any given zone — as many as necessary to provide [*load balancing*](l-gly.md), [*fault tolerance*](f-gly.md), and traffic reduction.</span></span> <span data-ttu-id="a7aba-123">Darüber hinaus kann jeder DNS-Server ein sekundärer Server für mehrere Zonen sein.</span><span class="sxs-lookup"><span data-stu-id="a7aba-123">Additionally, any given DNS Server can be a secondary server for multiple zones.</span></span>

<span data-ttu-id="a7aba-124">Zusätzlich zu primären und sekundären DNS-Servern können zusätzliche DNS-Serverrollen verwendet werden, wenn solche Server für eine DNS-Infrastruktur geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="a7aba-124">In addition to primary and secondary DNS Servers, additional DNS Server roles can be used when such servers are appropriate for a DNS infrastructure.</span></span> <span data-ttu-id="a7aba-125">Bei diesen zusätzlichen Servern handelt es sich um [*Zwischenspeicherungsserver und -forwarder.*](f-gly.md)</span><span class="sxs-lookup"><span data-stu-id="a7aba-125">These additional servers are caching servers and [*forwarders*](f-gly.md).</span></span>

## <a name="caching-servers"></a><span data-ttu-id="a7aba-126">Zwischenspeichern von Servern</span><span class="sxs-lookup"><span data-stu-id="a7aba-126">Caching Servers</span></span>

<span data-ttu-id="a7aba-127">[*Zwischenspeichern von*](c-gly.md)Servern, die auch als Server mit ausschließlicher Zwischenspeicherung bekannt sind, wird wie von ihrem Namen vorgeschlagen ausgeführt. Sie stellen nur zwischengespeicherte Abfragedienste für DNS-Antworten zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="a7aba-127">[*Caching servers*](c-gly.md), also known as caching-only servers, perform as their name suggests; they provide only cached-query service for DNS responses.</span></span> <span data-ttu-id="a7aba-128">Anstatt Zonendateien wie andere sekundäre Server zu verwalten, führen dns-Server Zwischenspeicherungsabfragen aus, speichern die Antworten zwischen und geben die Ergebnisse an den abfragenden Client zurück.</span><span class="sxs-lookup"><span data-stu-id="a7aba-128">Rather than maintaining zone files like other secondary servers do, caching DNS Servers perform queries, cache the answers, and return the results to the querying client.</span></span> <span data-ttu-id="a7aba-129">Der Hauptunterschied zwischen Zwischenspeicherungsservern und anderen sekundären Servern besteht in der Beibehaltung von Zonendateien durch andere sekundäre Server (und gegebenenfalls der Erstellung von Zonenübertragungen, wodurch der Übertragung zugeordneter Netzwerkdatenverkehr generiert wird). Dies gilt nicht für Cacheserver.</span><span class="sxs-lookup"><span data-stu-id="a7aba-129">The primary difference between caching servers and other secondary servers is that other secondary servers maintain zone files (and do zone transfers when appropriate, thereby generating network traffic associated with the transfer), caching servers do not.</span></span>

 

 




