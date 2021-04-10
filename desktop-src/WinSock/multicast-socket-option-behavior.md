---
description: Auf dieser Seite wird das Verhalten von Multicast Socketoptionen basierend auf verschiedenen Einstellungen für Socketoptionen beschrieben.
ms.assetid: a411e831-7b28-4ab5-a09a-650db99a7cd5
title: Multicast-socketoptionsverhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd10094750bea59b844ad1fcdac70be0c7f9646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041726"
---
# <a name="multicast-socket-option-behavior"></a><span data-ttu-id="a5f39-103">Multicast-socketoptionsverhalten</span><span class="sxs-lookup"><span data-stu-id="a5f39-103">Multicast Socket Option Behavior</span></span>

<span data-ttu-id="a5f39-104">Auf dieser Seite wird das Verhalten von Multicast Socketoptionen basierend auf verschiedenen Einstellungen für Socketoptionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a5f39-104">This page describes the behavior of multicast socket options based on various socket option settings states.</span></span>

<span data-ttu-id="a5f39-105">Auf dieser Seite wird z. b. das Verhalten beschrieben, wenn die IP- \_ \_ \_ Option Quell Mitgliedschafts Socket hinzufügen für einen Socket festgelegt ist, für den die IP- \_ \_ Option Quell- \_ Mitgliedschaftsoption bereits mit dem angegebenen Gruppen-/quellpaar auf derselben Netzwerkschnittstelle festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="a5f39-105">For example, this page describes the behavior when the IP\_ADD\_SOURCE\_MEMBERSHIP socket option is set on a socket for which the IP\_ADD\_SOURCE\_MEMBERSHIP option has already been set with the specified group/source pair on the same network interface.</span></span> <span data-ttu-id="a5f39-106">Es ist zulässig, IP- \_ Add- \_ Source- \_ Mitgliedschaft in derselben Gruppe auf einer anderen Netzwerkschnittstelle aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="a5f39-106">It is permitted to call IP\_ADD\_SOURCE\_MEMBERSHIP on the same group on a different network interface.</span></span>

<span data-ttu-id="a5f39-107">Diese Seite hilft bei der ordnungsgemäßen Entwicklung und Problembehandlung von Windows Sockets-Multicast Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="a5f39-107">This page assists in properly designing and troubleshooting Windows Sockets multicast applications.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a5f39-108">Anfängliche Socketoption</span><span class="sxs-lookup"><span data-stu-id="a5f39-108">Initial socket option</span></span></th>
<th><span data-ttu-id="a5f39-109">Widersprüchliche nachfolgende Socketoption</span><span class="sxs-lookup"><span data-stu-id="a5f39-109">Conflicting subsequent socket option</span></span></th>
<th><span data-ttu-id="a5f39-110">Fehler zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="a5f39-110">Error returned</span></span></th>
<th><span data-ttu-id="a5f39-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5f39-111">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="a5f39-112">IP_ADD_MEMBERSHIP $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="a5f39-112">IP_ADD_MEMBERSHIP${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="a5f39-113">IP_ADD_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="a5f39-113">IP_ADD_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="a5f39-114">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="a5f39-114">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="a5f39-115">Nennen Sie IP_ADD_MEMBERSHIP nicht mehr als einmal in derselben Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a5f39-115">Do not call IP_ADD_MEMBERSHIP with the same group more than once on the same network interface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a5f39-116">IP_ADD_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="a5f39-116">IP_ADD_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="a5f39-117">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="a5f39-117">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="a5f39-118">Nennen Sie IP_ADD_SOURCE_MEMBERSHIP nicht mit derselben Gruppe, die zuvor mit IP_ADD_MEMBERSHIP auf derselben Netzwerkschnittstelle aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a5f39-118">Do not call IP_ADD_SOURCE_MEMBERSHIP with the same group previously called with IP_ADD_MEMBERSHIP on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="a5f39-119">IP_DROP_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="a5f39-119">IP_DROP_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="a5f39-120">Wsaabval</span><span class="sxs-lookup"><span data-stu-id="a5f39-120">WSAEINVAL</span></span></td>
<td><span data-ttu-id="a5f39-121">Verwenden Sie stattdessen IP_BLOCK_SOURCE.</span><span class="sxs-lookup"><span data-stu-id="a5f39-121">Use IP_BLOCK_SOURCE instead.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="a5f39-122">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="a5f39-122">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="a5f39-123">Wsaabval</span><span class="sxs-lookup"><span data-stu-id="a5f39-123">WSAEINVAL</span></span></td>
<td><span data-ttu-id="a5f39-124">Gibt einen Fehler zurück, wenn versucht wird, die Blockierung eines Gruppen-/Quell-Paars aufzuheben, das zuvor nicht an derselben Netzwerkschnittstelle blockiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a5f39-124">Returns an error when attempting to unblock a group/source pair that has not previously been blocked on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="a5f39-125">IP_DROP_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="a5f39-125">IP_DROP_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="a5f39-126">Alle nachfolgenden Aufrufe für dasselbe Gruppen-oder Gruppen-/quellpaar</span><span class="sxs-lookup"><span data-stu-id="a5f39-126">Any subsequent call on the same group or group/source pair</span></span></td>
<td><span data-ttu-id="a5f39-127">Wsaabval</span><span class="sxs-lookup"><span data-stu-id="a5f39-127">WSAEINVAL</span></span></td>
<td><span data-ttu-id="a5f39-128">Das Erstellen von socketoptionsaufrufen für eine Gruppe oder ein Gruppen-/Quell-Paar, das sich derzeit nicht in der Aufnahme Liste (aufgrund der Löschung der Mitgliedschaft oder anderweitig), führt zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="a5f39-128">Making socket option calls on a group or group/source pair not currently in the inclusion list (due to dropping membership, or otherwise) results in an error.</span></span></td>
</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="a5f39-129">IP_ADD_SOURCE_MEMBERSHIP $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="a5f39-129">IP_ADD_SOURCE_MEMBERSHIP${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="a5f39-130">IP_ADD_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="a5f39-130">IP_ADD_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="a5f39-131">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="a5f39-131">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="a5f39-132">Nennen Sie IP_ADD_MEMBERSHIP nicht mit derselben Gruppe, die zuvor mit IP_ADD_SOURCE_MEMBERSHIP auf derselben Netzwerkschnittstelle aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a5f39-132">Do not call IP_ADD_MEMBERSHIP with the same group previously called with IP_ADD_SOURCE_MEMBERSHIP on the same network interface.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a5f39-133">IP_ADD_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="a5f39-133">IP_ADD_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="a5f39-134">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="a5f39-134">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="a5f39-135">Sie sollten IP_ADD_SOURCE_MEMBERSHIP nicht mit demselben Gruppen-/quellpaar aufrufen, das zuvor mit IP_ADD_SOURCE_MEMBERSHIP auf derselben Netzwerkschnittstelle aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a5f39-135">Do not call IP_ADD_SOURCE_MEMBERSHIP with the same group/source pair previously called with IP_ADD_SOURCE_MEMBERSHIP on the same network interface.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="a5f39-136">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="a5f39-136">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="a5f39-137">Wsaabval</span><span class="sxs-lookup"><span data-stu-id="a5f39-137">WSAEINVAL</span></span></td>
<td><span data-ttu-id="a5f39-138">Gibt einen Fehler zurück, wenn versucht wird, die Blockierung eines Gruppen-/Quell-Paars aufzuheben, das zuvor nicht an derselben Netzwerkschnittstelle blockiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a5f39-138">Returns an error when attempting to unblock a group/source pair that has not previously been blocked on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="a5f39-139">IP_DROP_SOURCE_MEMBERSHIP $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="a5f39-139">IP_DROP_SOURCE_MEMBERSHIP${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="a5f39-140">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="a5f39-140">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="a5f39-141">Wsaabval</span><span class="sxs-lookup"><span data-stu-id="a5f39-141">WSAEINVAL</span></span></td>
<td><span data-ttu-id="a5f39-142">Gibt einen Fehler zurück, wenn versucht wird, die Blockierung eines Gruppen-/Quell-Paars aufzuheben, das zuvor nicht an derselben Netzwerkschnittstelle blockiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a5f39-142">Returns an error when attempting to unblock a group/source pair that has not previously been blocked on the same network interface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a5f39-143">IP_DROP_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="a5f39-143">IP_DROP_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="a5f39-144">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="a5f39-144">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="a5f39-145">Gibt einen Fehler zurück, wenn versucht wird, ein Gruppen-/quellpaar zu löschen, das sich nicht in der Aufnahme Liste auf derselben Netzwerkschnittstelle befindet.</span><span class="sxs-lookup"><span data-stu-id="a5f39-145">Returns an error when attempting to drop a group/source pair that is not in the inclusion list on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="a5f39-146">IP_BLOCK_SOURCE $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="a5f39-146">IP_BLOCK_SOURCE${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="a5f39-147">IP_BLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="a5f39-147">IP_BLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="a5f39-148">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="a5f39-148">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="a5f39-149">Gibt einen Fehler zurück, wenn versucht wird, ein Gruppen-/Quell-paar zu blockieren, das bereits auf derselben Netzwerkschnittstelle blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="a5f39-149">Returns an error when attempting to block a group/source pair that is already blocked on the same network interface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a5f39-150">IP_ADD_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="a5f39-150">IP_ADD_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="a5f39-151">Wsaabval</span><span class="sxs-lookup"><span data-stu-id="a5f39-151">WSAEINVAL</span></span></td>
<td><span data-ttu-id="a5f39-152">Verwenden Sie stattdessen IP_UNBLOCK_SOURCE.</span><span class="sxs-lookup"><span data-stu-id="a5f39-152">Use IP_UNBLOCK_SOURCE instead.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="a5f39-153">IP_ADD_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="a5f39-153">IP_ADD_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="a5f39-154">Wsaabval</span><span class="sxs-lookup"><span data-stu-id="a5f39-154">WSAEINVAL</span></span></td>
<td><span data-ttu-id="a5f39-155">Verwenden Sie stattdessen IP_UNBLOCK_SOURCE.</span><span class="sxs-lookup"><span data-stu-id="a5f39-155">Use IP_UNBLOCK_SOURCE instead.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="a5f39-156">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="a5f39-156">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="a5f39-157">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="a5f39-157">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="a5f39-158">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="a5f39-158">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="a5f39-159">Gibt einen Fehler zurück, wenn versucht wird, ein Gruppen-/quellpaar aufzuheben, das sich nicht in der Liste der blockierten Netzwerke auf derselben Netzwerkschnittstelle befindet.</span><span class="sxs-lookup"><span data-stu-id="a5f39-159">Returns an error when attempting to unblock a group/source pair that is not in the blocked list on the same network interface.</span></span></td>
</tr>
</tbody>
</table>



 

 

 



