---
title: Routing
description: Die Routing-APIs ermöglichen das Erstellen von Anwendungen, um die Routing Funktionen des Betriebssystems zu verwalten.
ms.assetid: 66e1bbb4-73c8-40fc-9575-ffe76d4b697b
keywords:
- Routing-RAS
- Routing-RAS, Startseite
- RRAS-RAS
- RRAS-RAS, siehe Routing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e3b2a92a6c54f47693d657315ec0a48e660061
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858442"
---
# <a name="routing"></a><span data-ttu-id="08c10-107">Routing</span><span class="sxs-lookup"><span data-stu-id="08c10-107">Routing</span></span>

## <a name="purpose"></a><span data-ttu-id="08c10-108">Zweck</span><span class="sxs-lookup"><span data-stu-id="08c10-108">Purpose</span></span>

<span data-ttu-id="08c10-109">Die Routing-APIs ermöglichen das Erstellen von Anwendungen, um die Routing Funktionen des Betriebssystems zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="08c10-109">The Routing APIs make it possible to create applications to administer the routing capabilities of the operating system.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="08c10-110">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="08c10-110">Where applicable</span></span>

<span data-ttu-id="08c10-111">Das Routing ermöglicht es, dass ein Computer als Netzwerk Router fungiert.</span><span class="sxs-lookup"><span data-stu-id="08c10-111">Routing makes it possible for a computer to function as a network router.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="08c10-112">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="08c10-112">Developer audience</span></span>

<span data-ttu-id="08c10-113">Die Routing-APIs sind für die Verwendung durch C/C++-Programmierer konzipiert.</span><span class="sxs-lookup"><span data-stu-id="08c10-113">The Routing APIs are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="08c10-114">Programmierer sollten auch mit den Netzwerk Konzepten vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="08c10-114">Programmers should also be familiar with networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="08c10-115">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="08c10-115">Run-time requirements</span></span>

<span data-ttu-id="08c10-116">Das Routing ist eine serverbasierte Technologie.</span><span class="sxs-lookup"><span data-stu-id="08c10-116">Routing is a server-based technology.</span></span> <span data-ttu-id="08c10-117">Die gesamte Funktionalität des Routings ist in Windows 2000 Server und Windows Server 2003 integriert.</span><span class="sxs-lookup"><span data-stu-id="08c10-117">All the functionality of Routing is incorporated into Windows 2000 Server and the Windows Server 2003.</span></span> <span data-ttu-id="08c10-118">Routing Anwendungen können nicht auf Windows NT-Arbeitsstationen 4,0 oder Client Betriebssystemen (z. b. Windows 95) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="08c10-118">Routing applications cannot run on Windows NT Workstation 4.0 or on client operating systems, such as Windows 95.</span></span> <span data-ttu-id="08c10-119">Spezifischere Informationen dazu, welche Betriebssysteme eine bestimmte Funktion unterstützen, finden Sie in den Abschnitten zu den Anforderungen in der-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="08c10-119">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="08c10-120">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="08c10-120">In this section</span></span>



| <span data-ttu-id="08c10-121">Thema</span><span class="sxs-lookup"><span data-stu-id="08c10-121">Topic</span></span>                                                                                               | <span data-ttu-id="08c10-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08c10-122">Description</span></span>                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="08c10-123">Routerverwaltung</span><span class="sxs-lookup"><span data-stu-id="08c10-123">Router Management</span></span>](about-router-management.md)<br/>                                         | <span data-ttu-id="08c10-124">Mithilfe der routerverwaltungs-API können Entwickler Anwendungen erstellen, um den Routerdienst auf einem Computer zu verwalten, auf dem Windows 2000 Server und spätere Betriebssysteme ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="08c10-124">The router administration API allows developers to create applications to manage the router service on a computer running Windows 2000 Server and later operating systems.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="08c10-125">Routermanager und Verwaltungs Informationsbasis</span><span class="sxs-lookup"><span data-stu-id="08c10-125">Router Managers and Management Information Base</span></span>](/windows/desktop/RRAS/about-router-management-with-mib)<br/> | <span data-ttu-id="08c10-126">Die MIB-APIs (Management Information Base) für die Routerverwaltung ermöglichen es, die Werte von MIB-Variablen abzufragen und festzulegen, die von einem der routermanager oder einem der Routing Protokolle exportiert werden, die der routermanager-Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="08c10-126">The Management Information Base (MIB) APIs for router management makes it possible to query and set the values of MIB variables exported by one of the router managers or any of the routing protocols that the router managers service.</span></span> <span data-ttu-id="08c10-127">Wenn Sie diese API verwenden, unterstützt der Router das Simple Network Management-Protokoll (SNMP).</span><span class="sxs-lookup"><span data-stu-id="08c10-127">By using this API, the router supports the Simple Network Management Protocol (SNMP).</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="08c10-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="08c10-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08c10-129">Funktionen des IP-Hilfsprogramms</span><span class="sxs-lookup"><span data-stu-id="08c10-129">IP Helper Functions</span></span>](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[<span data-ttu-id="08c10-130">Remotezugriff</span><span class="sxs-lookup"><span data-stu-id="08c10-130">Remote Access</span></span>](remote-access-start-page.md)
</dt> <dt>

[<span data-ttu-id="08c10-131">Routing Protokolle</span><span class="sxs-lookup"><span data-stu-id="08c10-131">Routing Protocols</span></span>](routing-protocols-start-page.md)
</dt> </dl>

 

