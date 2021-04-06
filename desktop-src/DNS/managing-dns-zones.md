---
title: Verwalten von DNS-Zonen
description: Eine DNS-Zone ist eine Datenbank mit RR-Einträgen, die einem Teil des hierarchischen DNS-namesplatzes entspricht. DNS-Zonen werden verwendet, um die autorisierenden DNS-Server zum Auflösen von namens Auflösungs Abfragen für einen bestimmten Abschnitt der DNS-Hierarchie zu definieren.
ms.assetid: d4aa94e0-36f7-4b97-8a0a-c677c8a826a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c4cc991821f88076d3c3e9b2bfcbddc3ab662d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712425"
---
# <a name="managing-dns-zones"></a><span data-ttu-id="de58d-104">Verwalten von DNS-Zonen</span><span class="sxs-lookup"><span data-stu-id="de58d-104">Managing DNS Zones</span></span>

<span data-ttu-id="de58d-105">Eine DNS-Zone ist eine Datenbank mit RR-Einträgen, die einem Teil des hierarchischen DNS-namesplatzes entspricht.</span><span class="sxs-lookup"><span data-stu-id="de58d-105">A DNS zone is a database of RR entries that corresponds to part of the DNS hierarchical name space.</span></span> <span data-ttu-id="de58d-106">DNS-Zonen werden verwendet, um die autorisierenden DNS-Server zum Auflösen von namens Auflösungs Abfragen für einen bestimmten Abschnitt der DNS-Hierarchie zu definieren.</span><span class="sxs-lookup"><span data-stu-id="de58d-106">DNS zones are used to delineate which DNS Servers are authoritative for resolving name-resolution queries for a given section of the DNS hierarchy.</span></span>

## <a name="administration-steps"></a><span data-ttu-id="de58d-107">Verwaltungsschritte</span><span class="sxs-lookup"><span data-stu-id="de58d-107">Administration Steps</span></span>

<span data-ttu-id="de58d-108">Der DNS-WMI-Anbieter ermöglicht die Verwaltung von DNS-Zonen über den autorisierenden DNS-Server selbst oder über Remote Hosts.</span><span class="sxs-lookup"><span data-stu-id="de58d-108">The DNS WMI Provider enables the administration of DNS zones from the authoritative DNS Server itself, or from remote hosts.</span></span> <span data-ttu-id="de58d-109">Die folgenden allgemeinen Schritte sind erforderlich, um eine Zone mit dem DNS-WMI-Anbieter zu verwalten:</span><span class="sxs-lookup"><span data-stu-id="de58d-109">The general steps necessary to administer a zone using the DNS WMI Provider are:</span></span>

-   <span data-ttu-id="de58d-110">Herstellen einer Verbindung mit dem DNS-WMI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="de58d-110">Connecting to the DNS WMI Provider</span></span>
-   <span data-ttu-id="de58d-111">So erhalten Sie eine Zonen Instanz</span><span class="sxs-lookup"><span data-stu-id="de58d-111">Getting a zone instance</span></span>
-   <span data-ttu-id="de58d-112">Auflisten oder Ändern einer Zonen Eigenschaft oder Verwenden einer Methode</span><span class="sxs-lookup"><span data-stu-id="de58d-112">Listing or modifying a zone property, or using a method</span></span>

<span data-ttu-id="de58d-113">Die folgenden Aufgaben sind mit den dazugehörigen Skript Beispielen verknüpft:</span><span class="sxs-lookup"><span data-stu-id="de58d-113">The following tasks are linked to their associated scripting samples:</span></span>

-   [<span data-ttu-id="de58d-114">Erstellen einer DNS-Zone</span><span class="sxs-lookup"><span data-stu-id="de58d-114">Creating a DNS Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="de58d-115">Ändern einer DNS-Zone</span><span class="sxs-lookup"><span data-stu-id="de58d-115">Modifying a DNS Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="de58d-116">Löschen einer DNS-Zone</span><span class="sxs-lookup"><span data-stu-id="de58d-116">Deleting a DNS Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="de58d-117">Hinzufügen einer Zonen-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="de58d-117">Adding a Zone IP Address</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="de58d-118">Löschen einer Zonen-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="de58d-118">Deleting a Zone IP Address</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="de58d-119">Anhalten einer Zone</span><span class="sxs-lookup"><span data-stu-id="de58d-119">Pausing a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="de58d-120">Fortsetzen einer Zone</span><span class="sxs-lookup"><span data-stu-id="de58d-120">Resuming a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="de58d-121">Aktualisieren einer Zone</span><span class="sxs-lookup"><span data-stu-id="de58d-121">Updating a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="de58d-122">Erneutes Laden einer Zone</span><span class="sxs-lookup"><span data-stu-id="de58d-122">Reloading a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="de58d-123">Aktualisieren einer Zone</span><span class="sxs-lookup"><span data-stu-id="de58d-123">Refreshing a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)

 

 




