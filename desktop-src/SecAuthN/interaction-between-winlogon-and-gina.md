---
description: Winlogon und Gina müssen Initialisierungs Informationen kommunizieren, die Überwachung und Benachrichtigung über die Sicherheitsüberwachung (Secure Monitoring Sequence, SAS) verarbeiten und die Aktivitäten zum Abmelden und Herunterfahren zulassen.
ms.assetid: ea45cd5f-9cb0-41bb-99bf-f84781ae9604
title: 'Interaktion zwischen Windows-Anmeldung und GINA '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 759d9171bca02e0a00fd35b77a4514d7438d43f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050387"
---
# <a name="interaction-between-winlogon-and-gina"></a><span data-ttu-id="3c5ca-103">Interaktion zwischen Windows-Anmeldung und GINA </span><span class="sxs-lookup"><span data-stu-id="3c5ca-103">Interaction Between Winlogon and GINA</span></span>

<span data-ttu-id="3c5ca-104">[*Winlogon*](../secgloss/w-gly.md) und [*Gina*](../secgloss/g-gly.md) müssen Initialisierungs Informationen kommunizieren, die Überwachung und Benachrichtigung über die Sicherheitsüberwachung ( [*Secure Monitoring Sequence*](../secgloss/s-gly.md) , SAS) verarbeiten und die Aktivitäten zum Abmelden und Herunterfahren zulassen.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-104">[*Winlogon*](../secgloss/w-gly.md) and the [*GINA*](../secgloss/g-gly.md) must communicate initialization information, handle [*secure attention sequence*](../secgloss/s-gly.md) (SAS) monitoring and notification, and permit logoff and shutdown activities.</span></span> <span data-ttu-id="3c5ca-105">Der Status von Winlogon bestimmt, welche Gina-Funktion aufgerufen wird, um ein bestimmtes SAS-Ereignis zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-105">The state of Winlogon determines which GINA function is called to process any given SAS event.</span></span> <span data-ttu-id="3c5ca-106">Die Kommunikation erfolgt in der hier gezeigten Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-106">Communications occur in the order shown here.</span></span>

> [!Note]  
> <span data-ttu-id="3c5ca-107">Gina-DLLs werden in Windows Vista ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-107">GINA DLLs are ignored in Windows Vista.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3c5ca-108">Ereignis</span><span class="sxs-lookup"><span data-stu-id="3c5ca-108">Event</span></span></th>
<th><span data-ttu-id="3c5ca-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c5ca-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3c5ca-110">Arbeitsstation starten</span><span class="sxs-lookup"><span data-stu-id="3c5ca-110">Workstation boot</span></span></td>
<td><ol>
<li><span data-ttu-id="3c5ca-111">Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>wlxaushandlungs</strong></a> -Funktion von Gina auf, um die Gina über die verwendete Version von Winlogon zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-111">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>WlxNegotiate</strong></a> function to notify the GINA about the version of Winlogon in use.</span></span></li>
<li><span data-ttu-id="3c5ca-112">Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>wlxinitialize</strong></a> -Funktion von Gina auf, um der Gina die Adressen der Unterstützungsfunktionen, ein Handle für die Winlogon-Funktion und zum Abrufen der <a href="/windows/desktop/SecGloss/c-gly"><em>Kontext</em></a> Informationen für die Gina (für die Verwendung in allen zukünftigen Aufrufen der Gina) zu geben.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-112">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>WlxInitialize</strong></a> function to give the GINA the addresses of the support functions, a handle to Winlogon, and to obtain the <a href="/windows/desktop/SecGloss/c-gly"><em>context</em></a> information for the GINA (to be used in all future calls to the GINA).</span></span><br/> <span data-ttu-id="3c5ca-113">Winlogon befindet sich im Abmelde Zustand.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-113">Winlogon is in the logged-out state.</span></span><br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c5ca-114">Niemand ist angemeldet.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-114">No one is logged on</span></span></td>
<td><span data-ttu-id="3c5ca-115">(Die Gina überwacht Geräte auf SAS-Ereignisse).</span><span class="sxs-lookup"><span data-stu-id="3c5ca-115">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="3c5ca-116">Die Gina Ruft die <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>wlxsasnotify</strong></a> -Funktion von Winlogon auf, wenn ein SAS-Ereignis empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-116">The GINA calls Winlogon's <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function when a SAS event has been received.</span></span></li>
<li><span data-ttu-id="3c5ca-117">Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>wlxloggedoutsas</strong></a> -Funktion von Gina auf und ermöglicht es der Gina, die Identifikations-und Authentifizierungsinformationen eines Benutzers zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-117">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>WlxLoggedOutSAS</strong></a> function, allowing the GINA to process a user's identification and authentication information.</span></span><br/> <span data-ttu-id="3c5ca-118">Wenn die Anmeldung erfolgreich ist, befindet sich die Winlogon im angemeldeten Zustand.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-118">When logon is successful, Winlogon is in the logged-on state.</span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c5ca-119">Der Benutzer ist angemeldet.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-119">The user is logged on</span></span></td>
<td><span data-ttu-id="3c5ca-120">(Die Gina überwacht Geräte auf SAS-Ereignisse).</span><span class="sxs-lookup"><span data-stu-id="3c5ca-120">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="3c5ca-121">Die Gina Ruft die <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>wlxsasnotify</strong></a> -Funktion von Winlogon auf, wenn ein SAS-Ereignis empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-121">The GINA calls Winlogon's <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function when a SAS event has been received.</span></span></li>
<li><span data-ttu-id="3c5ca-122">Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>wlxloggedonsas</strong></a> -Funktion von Gina auf, sodass die Gina Optionen für den aktuell angemeldeten Benutzer präsentieren kann.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-122">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function, allowing the GINA to present options to the user who is currently logged on.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c5ca-123">Der Benutzer ist angemeldet und möchte den Computer sperren.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-123">The user is logged on and wants to lock computer</span></span></td>
<td><span data-ttu-id="3c5ca-124">(Die Gina überwacht Geräte auf SAS-Ereignisse).</span><span class="sxs-lookup"><span data-stu-id="3c5ca-124">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="3c5ca-125">Die Gina Ruft die <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>wlxsasnotify</strong></a> -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-125">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="3c5ca-126">Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>wlxloggedonsas</strong></a> -Funktion von Gina auf.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-126">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="3c5ca-127">Die Gina gibt WLX_SAS_ACTION_LOCK_WKSTA zurück.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-127">The GINA returns WLX_SAS_ACTION_LOCK_WKSTA.</span></span><br/> <span data-ttu-id="3c5ca-128">Winlogon befindet sich im Zustand der Arbeitsstation.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-128">Winlogon is in the workstation-locked state.</span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c5ca-129">Der Benutzer ist angemeldet, die Arbeitsstation ist gesperrt, und der Benutzer möchte den Computer entsperren.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-129">The user is logged on, the workstation is locked, and the user wants to unlock computer</span></span></td>
<td><span data-ttu-id="3c5ca-130">(Die Gina überwacht Geräte auf SAS-Ereignisse).</span><span class="sxs-lookup"><span data-stu-id="3c5ca-130">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="3c5ca-131">Die Gina Ruft die <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>wlxsasnotify</strong></a> -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-131">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="3c5ca-132">Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>wlxwkstalockedsas</strong></a> -Funktion von Gina auf.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-132">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>WlxWkstaLockedSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="3c5ca-133">Die Gina gibt WLX_SAS_ACTION_UNLOCK_WKSTA zurück.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-133">The GINA returns WLX_SAS_ACTION_UNLOCK_WKSTA.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c5ca-134">Der Benutzer ist angemeldet, und das Programm ruft die <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a> -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-134">The user is logged on, and the program calls the <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a> function</span></span></td>
<td><span data-ttu-id="3c5ca-135">Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>wlxlogoff</strong></a> -Funktion von Gina auf.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-135">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c5ca-136">Der Benutzer ist angemeldet und möchte sich mithilfe von SAS abmelden.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-136">The user is logged on and wants to log off by using SAS</span></span></td>
<td><span data-ttu-id="3c5ca-137">(Die Gina überwacht Geräte auf SAS-Ereignisse).</span><span class="sxs-lookup"><span data-stu-id="3c5ca-137">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="3c5ca-138">Die Gina Ruft die <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>wlxsasnotify</strong></a> -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-138">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="3c5ca-139">Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>wlxloggedonsas</strong></a> -Funktion von Gina auf.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-139">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="3c5ca-140">Die Gina gibt WLX_SAS_ACTION_LOGOFF zurück.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-140">The GINA returns WLX_SAS_ACTION_LOGOFF.</span></span></li>
<li><span data-ttu-id="3c5ca-141">Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>wlxlogoff</strong></a> -Funktion von Gina auf.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-141">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c5ca-142">Der Benutzer ist angemeldet und möchte sich abmelden und mithilfe von <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"> <strong>ExitWindowsEx</strong> Herunterfahren.</a></span><span class="sxs-lookup"><span data-stu-id="3c5ca-142">The user is logged on and wants to log off and shut down by using <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="3c5ca-143">Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>wlxlogoff</strong></a> -Funktion von Gina auf.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-143">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></li>
<li><span data-ttu-id="3c5ca-144">Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>wlxshutdown</strong></a> -Funktion von Gina auf.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-144">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> function.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c5ca-145">Der Benutzer ist angemeldet und möchte sich abmelden und mithilfe von SAS Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-145">The user is logged on and wants to log off and shut down by using SAS</span></span></td>
<td><span data-ttu-id="3c5ca-146">(Die Gina überwacht Geräte auf SAS-Ereignisse).</span><span class="sxs-lookup"><span data-stu-id="3c5ca-146">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="3c5ca-147">Die Gina Ruft die <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>wlxsasnotify</strong></a> -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-147">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="3c5ca-148">Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>wlxloggedonsas</strong></a> -Funktion von Gina auf.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-148">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="3c5ca-149">Die Gina gibt WLX_SAS_ACTION_SHUTDOWN zurück.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-149">The GINA returns WLX_SAS_ACTION_SHUTDOWN.</span></span></li>
<li><span data-ttu-id="3c5ca-150">Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>wlxlogoff</strong></a> -Funktion von Gina auf.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-150">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></li>
<li><span data-ttu-id="3c5ca-151">Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>wlxshutdown</strong></a> -Funktion von Gina auf.</span><span class="sxs-lookup"><span data-stu-id="3c5ca-151">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> function.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

 

 
