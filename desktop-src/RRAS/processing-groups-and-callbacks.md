---
title: Verarbeiten von Gruppen und Rückrufen
description: In der folgenden Tabelle werden eine Reihe von Schritten für eine operative Interaktion zwischen einem Routing Protokoll und dem Multicast-Gruppen-Manager zusammengefasst.
ms.assetid: 43c1dc12-70fd-4e02-a7b1-5818e6d7ddc6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2878ec15cfb663353f3dd0bc1dc5aeadbd2e1e7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316635"
---
# <a name="processing-groups-and-callbacks"></a><span data-ttu-id="62091-103">Verarbeiten von Gruppen und Rückrufen</span><span class="sxs-lookup"><span data-stu-id="62091-103">Processing Groups and Callbacks</span></span>

<span data-ttu-id="62091-104">In der folgenden Tabelle werden eine Reihe von Schritten für eine operative Interaktion zwischen einem Routing Protokoll und dem Multicast-Gruppen-Manager zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="62091-104">The following table summarizes a series of steps in an operational interaction between a routing protocol and the multicast group manager.</span></span> <span data-ttu-id="62091-105">In der ersten Spalte werden die Aktionen beschrieben, die das Routing Protokoll ausführt, und die Antwort des Routing Protokolls an den Multicast-Gruppen-Manager.</span><span class="sxs-lookup"><span data-stu-id="62091-105">The first column describes the actions that the routing protocol performs and the routing protocol's responses to the multicast group manager.</span></span> <span data-ttu-id="62091-106">In der zweiten Spalte werden die Antworten des Multicast Gruppen-Managers auf das Routing Protokoll und alle Aktionen beschrieben, die der Multicast-Gruppen-Manager ausführt, z. b. Rückrufe.</span><span class="sxs-lookup"><span data-stu-id="62091-106">The second column describes the multicast group manager's responses to the routing protocol and any actions the multicast group manager performs such as callbacks.</span></span> <span data-ttu-id="62091-107">Die dritte Spalte enthält alle zusätzlichen Informationen.</span><span class="sxs-lookup"><span data-stu-id="62091-107">The third column presents any additional information.</span></span>

<span data-ttu-id="62091-108">Jede Zeile der Tabelle stellt einen Schritt dar.</span><span class="sxs-lookup"><span data-stu-id="62091-108">Each row of the table represents one step.</span></span>

<span data-ttu-id="62091-109">Die in dieser Tabelle aufgeführten Tasks treten nicht in einer bestimmten Reihenfolge auf. Stattdessen erfolgen Sie basierend auf dem Status von Multicast Gruppenmitgliedschaften.</span><span class="sxs-lookup"><span data-stu-id="62091-109">The tasks listed in this table do not occur in any specific order; rather, they occur based on the status of multicast group memberships.</span></span> <span data-ttu-id="62091-110">Die folgende Tabelle zeigt eine Beispiel Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="62091-110">The table below shows an example order.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="62091-111">Routing Protokoll Aktion</span><span class="sxs-lookup"><span data-stu-id="62091-111">Routing protocol action</span></span></th>
<th><span data-ttu-id="62091-112">Multicast-Gruppen-Manager-Aktion</span><span class="sxs-lookup"><span data-stu-id="62091-112">Multicast group manager action</span></span></th>
<th><span data-ttu-id="62091-113">Notizen</span><span class="sxs-lookup"><span data-stu-id="62091-113">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="62091-114">Verwalten von Gruppenmitgliedschaften auf der Grundlage von Protokollinformationen, die über die Schnittstellen des Protokolls empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="62091-114">Manage group memberships based on protocol information received on those interfaces that the protocol owns.</span></span> <span data-ttu-id="62091-115">Die Verwaltung erfolgt mithilfe der folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="62091-115">Management is performed using the following functions:</span></span>
<ul>
<li><span data-ttu-id="62091-116"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>Mgmaddgroupmembership shipentry</strong></a></span><span class="sxs-lookup"><span data-stu-id="62091-116"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>MgmAddGroupMembershipEntry</strong></a></span></span></li>
<li><span data-ttu-id="62091-117"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>Mgmdeletegroupmembership shipentry</strong></a></span><span class="sxs-lookup"><span data-stu-id="62091-117"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>MgmDeleteGroupMembershipEntry</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="62091-118">Fügen Sie in der Liste der ausgehenden Schnittstellen zu und für die angegebenen Einträge (s, g), (*, g) und (*, \*) hinzu, und löschen Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="62091-118">Add to and delete from the outgoing interface list for the specified (s, g), (*, g), and (*, \*) entries.</span></span> <span data-ttu-id="62091-119">Diese Liste stellt den Satz von Schnittstellen dar, an denen Daten für diese Gruppe weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="62091-119">This list represents the set of interfaces on which data for this group is forwarded.</span></span> <span data-ttu-id="62091-120">Die Daten für diese Gruppe werden aus der angegebenen Quelle abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="62091-120">The data for this group is from the specified source.</span></span></td>

</tr>
<tr class="even">

<td><span data-ttu-id="62091-121">Senden von Warnungen an Routing Protokolle in Form von Rückrufen</span><span class="sxs-lookup"><span data-stu-id="62091-121">Send alerts to routing protocols in the form of callbacks.</span></span> <span data-ttu-id="62091-122">Die folgenden Ereignisse lösen den Multicast-Gruppen-Manager aus, um einen Rückruf aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="62091-122">The following events trigger the multicast group manager to invoke a callback:</span></span>
<ul>
<li><span data-ttu-id="62091-123">Beitreten oder verlassen Sie Gruppen <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong></strong></a>(PMGM_JOIN_ALERT_CALLBACK <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="62091-123">Join or leave groups ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong>PMGM_JOIN_ALERT_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>).</span></span></li>
<li><span data-ttu-id="62091-124">Die Gruppenmitgliedschaft wurde von IGMP geändert ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a> <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="62091-124">Group membership changed by IGMP ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>).</span></span></li>
<li><span data-ttu-id="62091-125">An falscher Schnittstelle empfangene Daten ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="62091-125">Data received on wrong interface ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>).</span></span></li>
<li><span data-ttu-id="62091-126">Daten, die von neuen Quellen oder einer neuen Gruppe ( <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>PMGM_CREATION_ALERT_CALLBACK</strong></a> und <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>) empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="62091-126">Data received from new sources or to a new group ( <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>PMGM_CREATION_ALERT_CALLBACK</strong></a> and <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>).</span></span></li>
</ul></td>
<td><span data-ttu-id="62091-127">Mithilfe dieser Rückrufe kann der Multicast-Gruppen-Manager die Paket Weiterleitung koordinieren, wenn mehrere Multicast-Routing Protokolle auf einem Router vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="62091-127">Using these callbacks, the multicast group manager is able to coordinate packet forwarding when several multicast routing protocols are present on a router.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62091-128">Auflisten der Multicast Weiterleitungs Einträge (MFEs) mithilfe der <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>mgmgetfirstmfe</strong></a>-, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>mgmgetnextmfe</strong></a>-und <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>mgmgetmfe</strong></a> -Funktionen.</span><span class="sxs-lookup"><span data-stu-id="62091-128">Enumerate the multicast forwarding entries (MFEs), using the <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>MgmGetFirstMfe</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>MgmGetNextMfe</strong></a>, and <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>MgmGetMfe</strong></a> functions.</span></span> <span data-ttu-id="62091-129">Treffen Sie Entscheidungen über Multicast Daten basierend auf den Ergebnissen der-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="62091-129">Make decisions about multicast data based on the results of the enumeration.</span></span></td>
<td><span data-ttu-id="62091-130">Gibt die angeforderten MFEs zurück.</span><span class="sxs-lookup"><span data-stu-id="62091-130">Return the requested MFEs.</span></span> <span data-ttu-id="62091-131">Gibt ERROR_NO_MORE Elemente zurück, wenn keine weiteren MFEs zurückgegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="62091-131">Return ERROR_NO_MORE ITEMS when there are no more MFEs to return.</span></span><br/></td>
<td><span data-ttu-id="62091-132">Verwenden Sie die <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>mgmgetfirstmfestats</strong></a>-, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>mgmgetnextmfestats</strong></a>-und <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>mgmgetmfestats</strong></a> -Funktionen, um MFE-Statistiken aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="62091-132">Use the <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>MgmGetFirstMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>MgmGetNextMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>MgmGetMfeStats</strong></a> functions to enumerate MFE statistics.</span></span> <span data-ttu-id="62091-133">Ein umfassendes Beispiel für die Verwendung dieser Funktionen finden Sie unter <a href="administrative-application-scenario.md">Verwaltungs Anwendungsszenario</a> .</span><span class="sxs-lookup"><span data-stu-id="62091-133">See <a href="administrative-application-scenario.md">Administrative Application Scenario</a> for a complete example of using these functions.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62091-134">Ändern Sie den Upstream-Nachbar in einem MFE mithilfe der <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>mgmabtmfe</strong></a> -Funktion.</span><span class="sxs-lookup"><span data-stu-id="62091-134">Modify the upstream neighbor in an MFE using the <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>MgmSetMfe</strong></a> function.</span></span></td>

<td><span data-ttu-id="62091-135">Clients verwenden diese Funktion, um die Informationen in Bezug auf die eingehende Schnittstelle zu ändern.</span><span class="sxs-lookup"><span data-stu-id="62091-135">Clients use this function to modify the information regarding the incoming interface.</span></span></td>
</tr>
</tbody>
</table>



 

 

