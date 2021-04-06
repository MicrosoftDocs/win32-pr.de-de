---
title: Verwalten von DNS-Servern
description: Ein DNS-Server ist ein Computer, der den Prozess der Namensauflösung in DNS abschließt.
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe97e8b8b02e9d2198e49d0574b2d3fb8bc87df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712426"
---
# <a name="managing-dns-servers"></a><span data-ttu-id="dc812-103">Verwalten von DNS-Servern</span><span class="sxs-lookup"><span data-stu-id="dc812-103">Managing DNS Servers</span></span>

<span data-ttu-id="dc812-104">Ein DNS-Server ist ein Computer, der den Prozess der Namensauflösung in DNS abschließt.</span><span class="sxs-lookup"><span data-stu-id="dc812-104">A DNS Server is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="dc812-105">DNS-Server enthalten Dateien, so genannte *Zonendateien*, die es Ihnen ermöglichen, Namen in IP-Adressen aufzulösen (oder umgekehrt).</span><span class="sxs-lookup"><span data-stu-id="dc812-105">DNS Servers contain files, called *zone files*, that enable them to resolve names to IP addresses (or vice versa).</span></span> <span data-ttu-id="dc812-106">Beim Abfragen antwortet ein DNS-Server auf eine von drei Arten:</span><span class="sxs-lookup"><span data-stu-id="dc812-106">When queried, a DNS Server responds in one of three ways:</span></span>

-   <span data-ttu-id="dc812-107">Der Server gibt die angeforderte Namensauflösung oder IP-Auflösungsinformationen zurück.</span><span class="sxs-lookup"><span data-stu-id="dc812-107">The server returns the requested name-resolution or IP-resolution information.</span></span>
-   <span data-ttu-id="dc812-108">Der Server gibt einen Zeiger auf einen anderen DNS-Server zurück, der die Anforderung bedienen kann.</span><span class="sxs-lookup"><span data-stu-id="dc812-108">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="dc812-109">Der Server gibt an, dass er nicht über die angeforderten Informationen verfügt.</span><span class="sxs-lookup"><span data-stu-id="dc812-109">The server indicates that it does not have the requested information.</span></span>

<span data-ttu-id="dc812-110">DNS-Server können während der Vorbereitung der Rückgabe der angeforderten Auflösungsinformationen möglicherweise andere DNS-Server Abfragen.</span><span class="sxs-lookup"><span data-stu-id="dc812-110">DNS Servers might, during the course of preparing to return the requested resolution information, query other DNS Servers.</span></span> <span data-ttu-id="dc812-111">Darüber hinaus führen DNS-Server keine Vorgänge aus, die nicht in der vorherigen Liste aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="dc812-111">But beyond that, DNS Servers do not perform any operations other than those mentioned in the previous list.</span></span>

<span data-ttu-id="dc812-112">Es gibt drei Hauptarten von DNS-Servern – primäre Server, sekundäre Server und Cache Server.</span><span class="sxs-lookup"><span data-stu-id="dc812-112">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span> <span data-ttu-id="dc812-113">Weitere Informationen zu diesen DNS-Servern finden Sie unter [DNS-Server](dns-servers.md) .</span><span class="sxs-lookup"><span data-stu-id="dc812-113">See [DNS Servers](dns-servers.md) for more information on these DNS Servers.</span></span>

## <a name="administration-steps"></a><span data-ttu-id="dc812-114">Verwaltungsschritte</span><span class="sxs-lookup"><span data-stu-id="dc812-114">Administration Steps</span></span>

<span data-ttu-id="dc812-115">Der DNS-WMI-Anbieter ermöglicht die Verwaltung von DNS-Servern vom Server selbst oder von Remote Hosts aus.</span><span class="sxs-lookup"><span data-stu-id="dc812-115">The DNS WMI Provider enables the administration of DNS Servers from the server itself, or from remote hosts.</span></span> <span data-ttu-id="dc812-116">Die folgenden allgemeinen Schritte zum Verwalten eines DNS-Servers mit dem DNS-WMI-Anbieter sind erforderlich:</span><span class="sxs-lookup"><span data-stu-id="dc812-116">The general steps necessary to administer a DNS Server using the DNS WMI Provider are:</span></span>

-   <span data-ttu-id="dc812-117">Herstellen einer Verbindung mit dem DNS-WMI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="dc812-117">Connecting to the DNS WMI Provider</span></span>
-   <span data-ttu-id="dc812-118">Eine Serverinstanz wird erhalten.</span><span class="sxs-lookup"><span data-stu-id="dc812-118">Getting a server instance</span></span>
-   <span data-ttu-id="dc812-119">Auflisten oder Ändern einer Server Eigenschaft oder Verwenden einer Methode</span><span class="sxs-lookup"><span data-stu-id="dc812-119">Listing or modifying a server property, or using a method</span></span>

<span data-ttu-id="dc812-120">Um zu veranschaulichen, wie diese Verwaltungsschritte implementiert werden, werden Beispiele bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="dc812-120">To illustrate how to implement those administration steps, examples are provided.</span></span> <span data-ttu-id="dc812-121">Die folgenden Aufgaben sind mit den zugehörigen Skript Beispielen verknüpft.</span><span class="sxs-lookup"><span data-stu-id="dc812-121">The following tasks are linked to their associated scripting samples.</span></span>

-   [<span data-ttu-id="dc812-122">Beenden eines DNS-Servers</span><span class="sxs-lookup"><span data-stu-id="dc812-122">Stopping a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="dc812-123">Starten eines DNS-Servers</span><span class="sxs-lookup"><span data-stu-id="dc812-123">Starting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="dc812-124">Neustarten eines DNS-Servers</span><span class="sxs-lookup"><span data-stu-id="dc812-124">Restarting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="dc812-125">Hinzufügen einer IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="dc812-125">Adding an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="dc812-126">Entfernen einer IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="dc812-126">Removing an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="dc812-127">Auflisten von DNS-Server Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc812-127">Listing DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="dc812-128">Anzeigen von DNS-Server Eigenschafts Typen</span><span class="sxs-lookup"><span data-stu-id="dc812-128">Displaying DNS Server Property Types</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="dc812-129">Ändern von DNS-Server Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc812-129">Modifying DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 




