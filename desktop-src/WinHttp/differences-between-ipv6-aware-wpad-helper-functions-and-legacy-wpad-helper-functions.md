---
title: IPv6-Aware und ältere WPAD-Hilfsfunktionen
description: Unterschiede zwischen IPv6-Aware WPAD-Hilfsfunktionen und älteren WPAD-Hilfsfunktionen
ms.assetid: ea4b1c0d-ce02-477b-85c8-44e1beef90c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511b7f04aa0a2abe04b99562c15aeb3a53bdaadf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366083"
---
# <a name="ipv6-aware-and-legacy-wpad-helper-functions"></a><span data-ttu-id="8a1a4-103">IPv6-Aware und ältere WPAD-Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="8a1a4-103">IPv6-Aware and Legacy WPAD helper functions</span></span>

<span data-ttu-id="8a1a4-104">In den folgenden Tabellen werden die Unterschiede zwischen den neuen WPAD-Hilfsobjekten und den alten WPAD-Hilfsfunktionen erläutert.</span><span class="sxs-lookup"><span data-stu-id="8a1a4-104">The following tables explain the differences between the new WPAD helper functions and the legacy WPAD helper functions.</span></span> <span data-ttu-id="8a1a4-105">Die neuen Funktionen sind mit einem Sternchen gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8a1a4-105">The new functions are marked with an asterisk.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8a1a4-106">Functions</span><span class="sxs-lookup"><span data-stu-id="8a1a4-106">Functions</span></span></th>
<th><span data-ttu-id="8a1a4-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8a1a4-107">Input</span></span></th>
<th><span data-ttu-id="8a1a4-108">Output</span><span class="sxs-lookup"><span data-stu-id="8a1a4-108">Output</span></span></th>
<th><span data-ttu-id="8a1a4-109">Grund für Änderungen</span><span class="sxs-lookup"><span data-stu-id="8a1a4-109">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8a1a4-110">dnsResolve</span><span class="sxs-lookup"><span data-stu-id="8a1a4-110">dnsResolve</span></span></td>
<td><span data-ttu-id="8a1a4-111">Host</span><span class="sxs-lookup"><span data-stu-id="8a1a4-111">Host</span></span></td>
<td><span data-ttu-id="8a1a4-112">IPv4-Adresse</span><span class="sxs-lookup"><span data-stu-id="8a1a4-112">IPv4 address</span></span></td>
<td rowspan="2"><span data-ttu-id="8a1a4-113">Die Funktion "ex" gibt eine Liste von IPv6/IPv4 zurück.</span><span class="sxs-lookup"><span data-stu-id="8a1a4-113">Ex function will return a list of IPv6/IPv4.</span></span> <span data-ttu-id="8a1a4-114">Erforderlich, da IPv6-oder IPv4-Adressen mehrere Unicastadressen für eine einzelne Schnittstelle aufweisen können. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="8a1a4-114">Necessary since IPv6 or IPv4 addresses can have multiple unicast addresses for a single interface.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a1a4-115">dnsresolveex \*</span><span class="sxs-lookup"><span data-stu-id="8a1a4-115">dnsResolveEx\*</span></span></td>
<td><span data-ttu-id="8a1a4-116">Host</span><span class="sxs-lookup"><span data-stu-id="8a1a4-116">Host</span></span></td>
<td><span data-ttu-id="8a1a4-117">Liste der IPv6/IPv4-Adressen</span><span class="sxs-lookup"><span data-stu-id="8a1a4-117">List of IPv6/IPv4 addresses</span></span></td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8a1a4-118">Functions</span><span class="sxs-lookup"><span data-stu-id="8a1a4-118">Functions</span></span></th>
<th><span data-ttu-id="8a1a4-119">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8a1a4-119">Input</span></span></th>
<th><span data-ttu-id="8a1a4-120">Output</span><span class="sxs-lookup"><span data-stu-id="8a1a4-120">Output</span></span></th>
<th><span data-ttu-id="8a1a4-121">Grund für Änderungen</span><span class="sxs-lookup"><span data-stu-id="8a1a4-121">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8a1a4-122">isresolveable</span><span class="sxs-lookup"><span data-stu-id="8a1a4-122">isResolveable</span></span></td>
<td><span data-ttu-id="8a1a4-123">IPv4-Host</span><span class="sxs-lookup"><span data-stu-id="8a1a4-123">IPv4 host</span></span></td>
<td><span data-ttu-id="8a1a4-124">TRUE/FALSE</span><span class="sxs-lookup"><span data-stu-id="8a1a4-124">TRUE / FALSE</span></span></td>
<td rowspan="2"><span data-ttu-id="8a1a4-125">Die Funktion Ex gibt true zurück, wenn ein Host in eine IPv6-oder IPv4-Adresse aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="8a1a4-125">The Ex function will return TRUE if a host can resolve to an IPv6 or IPv4 address.</span></span> <span data-ttu-id="8a1a4-126">Die Legacy Funktion gibt nur dann true zurück, wenn der Host zu einer IPv4-Adresse aufgelöst wird. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="8a1a4-126">The legacy function only returns TRUE if the host resolves to an IPv4 address.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a1a4-127">isresolveableex \*</span><span class="sxs-lookup"><span data-stu-id="8a1a4-127">isResolveableEx\*</span></span></td>
<td><span data-ttu-id="8a1a4-128">IPv6/IPv4-Host</span><span class="sxs-lookup"><span data-stu-id="8a1a4-128">IPv6/IPv4 host</span></span></td>
<td><span data-ttu-id="8a1a4-129">TRUE/FALSE</span><span class="sxs-lookup"><span data-stu-id="8a1a4-129">TRUE / FALSE</span></span></td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8a1a4-130">Functions</span><span class="sxs-lookup"><span data-stu-id="8a1a4-130">Functions</span></span></th>
<th><span data-ttu-id="8a1a4-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8a1a4-131">Input</span></span></th>
<th><span data-ttu-id="8a1a4-132">Output</span><span class="sxs-lookup"><span data-stu-id="8a1a4-132">Output</span></span></th>
<th><span data-ttu-id="8a1a4-133">Grund für Änderungen</span><span class="sxs-lookup"><span data-stu-id="8a1a4-133">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8a1a4-134">myIpAddress</span><span class="sxs-lookup"><span data-stu-id="8a1a4-134">myIPAddress</span></span></td>
<td><span data-ttu-id="8a1a4-135">none</span><span class="sxs-lookup"><span data-stu-id="8a1a4-135">none</span></span></td>
<td><span data-ttu-id="8a1a4-136">IPv4-Adresse</span><span class="sxs-lookup"><span data-stu-id="8a1a4-136">IPv4 address</span></span></td>
<td rowspan="2"><span data-ttu-id="8a1a4-137">Die Funktion "ex" gibt eine Liste von IPv6/IPv4 zurück.</span><span class="sxs-lookup"><span data-stu-id="8a1a4-137">Ex function will return a list of IPv6/IPv4.</span></span> <span data-ttu-id="8a1a4-138">Erforderlich, da IPv6-oder IPv4-Adressen mehrere Unicastadressen für eine einzelne Schnittstelle $ {Remove} $ aufweisen können.</span><span class="sxs-lookup"><span data-stu-id="8a1a4-138">Necessary since IPv6 or IPv4 addresses can have multiple unicast addresses for a single interface ${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a1a4-139">myIPAddressEx\*</span><span class="sxs-lookup"><span data-stu-id="8a1a4-139">myIPAddressEx\*</span></span></td>
<td><span data-ttu-id="8a1a4-140">none</span><span class="sxs-lookup"><span data-stu-id="8a1a4-140">none</span></span></td>
<td><span data-ttu-id="8a1a4-141">Liste der IPv6/IPv4-Adressen</span><span class="sxs-lookup"><span data-stu-id="8a1a4-141">List of IPv6/IPv4 addresses</span></span></td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8a1a4-142">Functions</span><span class="sxs-lookup"><span data-stu-id="8a1a4-142">Functions</span></span></th>
<th><span data-ttu-id="8a1a4-143">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8a1a4-143">Input</span></span></th>
<th><span data-ttu-id="8a1a4-144">Output</span><span class="sxs-lookup"><span data-stu-id="8a1a4-144">Output</span></span></th>
<th><span data-ttu-id="8a1a4-145">Grund für Änderungen</span><span class="sxs-lookup"><span data-stu-id="8a1a4-145">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8a1a4-146">isInNet</span><span class="sxs-lookup"><span data-stu-id="8a1a4-146">isInNet</span></span></td>
<td><span data-ttu-id="8a1a4-147">Host, durch Punkte getrenntes IP-Adress Muster, IP-Adress Maske</span><span class="sxs-lookup"><span data-stu-id="8a1a4-147">Host, Dot separated IP address pattern, IP address Mask</span></span></td>
<td><span data-ttu-id="8a1a4-148">TRUE/FALSE</span><span class="sxs-lookup"><span data-stu-id="8a1a4-148">TRUE / FALSE</span></span></td>
<td rowspan="2"><span data-ttu-id="8a1a4-149">Stellen Sie eine auf IP-Version unabhängige Weise bereit, um zu ermitteln, ob sich eine IP-Adresse in einem bestimmten Subnetz befindet.</span><span class="sxs-lookup"><span data-stu-id="8a1a4-149">Provide an IP version agnostic way to find if an IP address is in a given subnet.</span></span> <span data-ttu-id="8a1a4-150">Außerdem ist die Mask-Notation in IPv4 veraltet. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="8a1a4-150">Also, the mask notation in IPv4 is deprecated.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a1a4-151">isinnettex \*</span><span class="sxs-lookup"><span data-stu-id="8a1a4-151">isInNetEx\*</span></span></td>
<td><span data-ttu-id="8a1a4-152">IP-Adress Präfix</span><span class="sxs-lookup"><span data-stu-id="8a1a4-152">IP Address IP Prefix</span></span></td>
<td><span data-ttu-id="8a1a4-153">TRUE/FALSE</span><span class="sxs-lookup"><span data-stu-id="8a1a4-153">TRUE / FALSE</span></span></td>

</tr>
</tbody>
</table>



 



| <span data-ttu-id="8a1a4-154">Functions</span><span class="sxs-lookup"><span data-stu-id="8a1a4-154">Functions</span></span>           | <span data-ttu-id="8a1a4-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8a1a4-155">Input</span></span>                       | <span data-ttu-id="8a1a4-156">Output</span><span class="sxs-lookup"><span data-stu-id="8a1a4-156">Output</span></span>                             | <span data-ttu-id="8a1a4-157">Grund für Änderungen</span><span class="sxs-lookup"><span data-stu-id="8a1a4-157">Reason for Change</span></span>                                                                                                                           |
|---------------------|-----------------------------|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a1a4-158">"menpaddresslist"\*</span><span class="sxs-lookup"><span data-stu-id="8a1a4-158">sortIPAddressList\*</span></span> | <span data-ttu-id="8a1a4-159">Liste der IPv6/IPv4-Adressen</span><span class="sxs-lookup"><span data-stu-id="8a1a4-159">List of IPv6/IPv4 addresses</span></span> | <span data-ttu-id="8a1a4-160">Sortierte Liste der IPv6/IPv4-Adressen</span><span class="sxs-lookup"><span data-stu-id="8a1a4-160">Sorted List of IPv6/IPv4 addresses</span></span> | <span data-ttu-id="8a1a4-161">Es gibt keine Entsprechung für die Legacy Funktion, da Legacy Funktionen nur eine einzelne IPv4-Adresse zurückgegeben haben, daher war keine Sortierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8a1a4-161">There is no counterpart legacy function because legacy functions only returned a single IPv4 address, therefore there was no need to sort .</span></span> |



 



| <span data-ttu-id="8a1a4-162">Functions</span><span class="sxs-lookup"><span data-stu-id="8a1a4-162">Functions</span></span>          | <span data-ttu-id="8a1a4-163">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8a1a4-163">Input</span></span> | <span data-ttu-id="8a1a4-164">Output</span><span class="sxs-lookup"><span data-stu-id="8a1a4-164">Output</span></span>                     | <span data-ttu-id="8a1a4-165">Grund für Änderungen</span><span class="sxs-lookup"><span data-stu-id="8a1a4-165">Reason for Change</span></span>                                                                                                                                                                                                           |
|--------------------|-------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a1a4-166">GetClientVersion\*</span><span class="sxs-lookup"><span data-stu-id="8a1a4-166">getClientVersion\*</span></span> | <span data-ttu-id="8a1a4-167">none</span><span class="sxs-lookup"><span data-stu-id="8a1a4-167">none</span></span>  | <span data-ttu-id="8a1a4-168">WPAD-Engine-Versionsnummer</span><span class="sxs-lookup"><span data-stu-id="8a1a4-168">WPAD engine version number</span></span> | <span data-ttu-id="8a1a4-169">Diese Funktion gibt derzeit Version 1,0 zurück.</span><span class="sxs-lookup"><span data-stu-id="8a1a4-169">Currently this function returns version 1.0.</span></span> <span data-ttu-id="8a1a4-170">Wir haben diese Funktion hinzugefügt, damit IT-Administratoren ihr WPAD aktualisieren können, sodass Sie mit unterschiedlichen Versionen der WPAD-Engine funktionieren, ohne dass die vorhandene Bereitstellung unterbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="8a1a4-170">We added this function to allow IT administrators to update their WPAD to work with different versions of the WPAD engine without causing breaks to their existent deployment.</span></span> |



 

> [!Note]  
> <span data-ttu-id="8a1a4-171">Diese Funktionalität erfordert Windows Internet Explorer 7 oder höher.</span><span class="sxs-lookup"><span data-stu-id="8a1a4-171">This functionality requires Windows Internet Explorer 7 or greater.</span></span>

 

 

 



