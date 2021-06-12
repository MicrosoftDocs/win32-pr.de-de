---
title: Verwalten von DNS-Servern
description: Erfahren Sie mehr über das Verwalten von DNS-Servern. Ein DNS-Server ist ein Computer, der den Prozess der Namensauflösung in DNS ab schließt.
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d797e05bc326b35e48173082d9b36a2b334fd9
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010773"
---
# <a name="managing-dns-servers"></a><span data-ttu-id="7a15d-104">Verwalten von DNS-Servern</span><span class="sxs-lookup"><span data-stu-id="7a15d-104">Managing DNS Servers</span></span>

<span data-ttu-id="7a15d-105">Ein DNS-Server ist ein Computer, der den Prozess der Namensauflösung in DNS ab schließt.</span><span class="sxs-lookup"><span data-stu-id="7a15d-105">A DNS Server is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="7a15d-106">DNS-Server enthalten Dateien, die als *Zonendateien* bezeichnet werden, die es ihnen ermöglichen, Namen in IP-Adressen aufzulösen (oder umgekehrt).</span><span class="sxs-lookup"><span data-stu-id="7a15d-106">DNS Servers contain files, called *zone files*, that enable them to resolve names to IP addresses (or vice versa).</span></span> <span data-ttu-id="7a15d-107">Bei der Abfrage antwortet ein DNS-Server auf eine von drei Arten:</span><span class="sxs-lookup"><span data-stu-id="7a15d-107">When queried, a DNS Server responds in one of three ways:</span></span>

-   <span data-ttu-id="7a15d-108">Der Server gibt die angeforderten Informationen zur Namensauflösung oder IP-Auflösung zurück.</span><span class="sxs-lookup"><span data-stu-id="7a15d-108">The server returns the requested name-resolution or IP-resolution information.</span></span>
-   <span data-ttu-id="7a15d-109">Der Server gibt einen Zeiger auf einen anderen DNS-Server zurück, der die Anforderung ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="7a15d-109">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="7a15d-110">Der Server gibt an, dass er nicht über die angeforderten Informationen verfügt.</span><span class="sxs-lookup"><span data-stu-id="7a15d-110">The server indicates that it does not have the requested information.</span></span>

<span data-ttu-id="7a15d-111">DNS-Server können während der Vorbereitung der Rückgabe der angeforderten Auflösungsinformationen andere DNS-Server abfragen.</span><span class="sxs-lookup"><span data-stu-id="7a15d-111">DNS Servers might, during the course of preparing to return the requested resolution information, query other DNS Servers.</span></span> <span data-ttu-id="7a15d-112">Darüber hinaus führen DNS-Server jedoch nur die in der vorherigen Liste erwähnten Vorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="7a15d-112">But beyond that, DNS Servers do not perform any operations other than those mentioned in the previous list.</span></span>

<span data-ttu-id="7a15d-113">Es gibt drei Hauptarten von DNS-Servern: primäre Server, sekundäre Server und Cacheserver.</span><span class="sxs-lookup"><span data-stu-id="7a15d-113">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span> <span data-ttu-id="7a15d-114">Weitere [Informationen zu diesen DNS-Servern](dns-servers.md) finden Sie unter DNS-Server.</span><span class="sxs-lookup"><span data-stu-id="7a15d-114">See [DNS Servers](dns-servers.md) for more information on these DNS Servers.</span></span>

## <a name="administration-steps"></a><span data-ttu-id="7a15d-115">Verwaltungsschritte</span><span class="sxs-lookup"><span data-stu-id="7a15d-115">Administration Steps</span></span>

<span data-ttu-id="7a15d-116">Der DNS-WMI-Anbieter ermöglicht die Verwaltung von DNS-Servern vom Server selbst oder von Remotehosts.</span><span class="sxs-lookup"><span data-stu-id="7a15d-116">The DNS WMI Provider enables the administration of DNS Servers from the server itself, or from remote hosts.</span></span> <span data-ttu-id="7a15d-117">Die allgemeinen Schritte, die zum Verwalten eines DNS-Servers mithilfe des DNS-WMI-Anbieters erforderlich sind, sind:</span><span class="sxs-lookup"><span data-stu-id="7a15d-117">The general steps necessary to administer a DNS Server using the DNS WMI Provider are:</span></span>

-   <span data-ttu-id="7a15d-118">Herstellen einer Verbindung mit dem DNS-WMI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="7a15d-118">Connecting to the DNS WMI Provider</span></span>
-   <span data-ttu-id="7a15d-119">Abrufen einer Serverinstanz</span><span class="sxs-lookup"><span data-stu-id="7a15d-119">Getting a server instance</span></span>
-   <span data-ttu-id="7a15d-120">Auflisten oder Ändern einer Servereigenschaft oder Verwenden einer Methode</span><span class="sxs-lookup"><span data-stu-id="7a15d-120">Listing or modifying a server property, or using a method</span></span>

<span data-ttu-id="7a15d-121">Um zu veranschaulichen, wie diese Verwaltungsschritte implementiert werden, werden Beispiele bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7a15d-121">To illustrate how to implement those administration steps, examples are provided.</span></span> <span data-ttu-id="7a15d-122">Die folgenden Aufgaben sind mit den zugehörigen Skriptbeispielen verknüpft.</span><span class="sxs-lookup"><span data-stu-id="7a15d-122">The following tasks are linked to their associated scripting samples.</span></span>

-   [<span data-ttu-id="7a15d-123">Beenden eines DNS-Servers</span><span class="sxs-lookup"><span data-stu-id="7a15d-123">Stopping a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="7a15d-124">Starten eines DNS-Servers</span><span class="sxs-lookup"><span data-stu-id="7a15d-124">Starting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="7a15d-125">Neustarten eines DNS-Servers</span><span class="sxs-lookup"><span data-stu-id="7a15d-125">Restarting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="7a15d-126">Hinzufügen einer IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="7a15d-126">Adding an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="7a15d-127">Entfernen einer IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="7a15d-127">Removing an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="7a15d-128">Auflisten von DNS-Servereigenschaften</span><span class="sxs-lookup"><span data-stu-id="7a15d-128">Listing DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="7a15d-129">Anzeigen von DNS-Servereigenschaftstypen</span><span class="sxs-lookup"><span data-stu-id="7a15d-129">Displaying DNS Server Property Types</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="7a15d-130">Ändern von DNS-Servereigenschaften</span><span class="sxs-lookup"><span data-stu-id="7a15d-130">Modifying DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 




