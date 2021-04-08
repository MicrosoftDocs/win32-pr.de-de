---
title: Remotedesktopdienste API-Funktionen
description: Die folgenden Funktionen werden mit Remotedesktopdienste verwendet.
ms.assetid: e99a86ee-af0e-46db-8dad-69703ca84fa0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94a2168f5ad4501b9725b72923c98ea97cc707c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727977"
---
# <a name="remote-desktop-services-api-functions"></a><span data-ttu-id="c3c81-103">Remotedesktopdienste API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="c3c81-103">Remote Desktop Services API Functions</span></span>

<span data-ttu-id="c3c81-104">Die folgenden Funktionen werden mit Remotedesktopdienste verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3c81-104">The following functions are used with Remote Desktop Services.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c3c81-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c3c81-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="c3c81-106">**Processidtosessionid**</span><span class="sxs-lookup"><span data-stu-id="c3c81-106">**ProcessIdToSessionId**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid)
</dt> <dd>

<span data-ttu-id="c3c81-107">Ruft die Remotedesktopdienste Sitzung ab, die einem angegebenen Prozess zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c3c81-107">Retrieves the Remote Desktop Services session associated with a specified process.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-108">**Tlsconnecttolsserver**</span><span class="sxs-lookup"><span data-stu-id="c3c81-108">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dd>

<span data-ttu-id="c3c81-109">Öffnet ein Handle für die angegebene Remotedesktop Lizenzservers.</span><span class="sxs-lookup"><span data-stu-id="c3c81-109">Opens a handle to the specified Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-110">**Tlsdisconnectfromserver**</span><span class="sxs-lookup"><span data-stu-id="c3c81-110">**TLSDisconnectFromServer**</span></span>](tlsdisconnectfromserver.md)
</dt> <dd>

<span data-ttu-id="c3c81-111">Schließt ein geöffnetes Handle für einen Remotedesktop-Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="c3c81-111">Closes an open handle to a Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-112">**Tlsgetservercertificate**</span><span class="sxs-lookup"><span data-stu-id="c3c81-112">**TLSGetServerCertificate**</span></span>](tlsgetservercertificate.md)
</dt> <dd>

<span data-ttu-id="c3c81-113">Gibt das Zertifikat des Remotedesktop Lizenzservers zurück.</span><span class="sxs-lookup"><span data-stu-id="c3c81-113">Returns the certificate of the Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-114">**Tlskeypackenumbegin**</span><span class="sxs-lookup"><span data-stu-id="c3c81-114">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dd>

<span data-ttu-id="c3c81-115">Beginnt die Enumeration über alle auf einem Remotedesktop Lizenzserver installierten Schlüsselpakete auf der Grundlage von Suchkriterien.</span><span class="sxs-lookup"><span data-stu-id="c3c81-115">Begins enumeration through all key packs that are installed on a Remote Desktop license server based on search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-116">**Tlskeypackenumend**</span><span class="sxs-lookup"><span data-stu-id="c3c81-116">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> <dd>

<span data-ttu-id="c3c81-117">Wird von einem vorherigen-Befehl der [**tlskeypackenumbegin**](tlskeypackenumbegin.md) -Funktion fortgesetzt und beendet die-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="c3c81-117">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and terminates the enumeration.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-118">**Tlskeypackenumnext**</span><span class="sxs-lookup"><span data-stu-id="c3c81-118">**TLSKeyPackEnumNext**</span></span>](tlskeypackenumnext.md)
</dt> <dd>

<span data-ttu-id="c3c81-119">Wird von einem vorherigen-Befehl der [**tlskeypackenumbegin**](tlskeypackenumbegin.md) -Funktion fortgesetzt und gibt das nächste Key Pack zurück, das auf einem Remotedesktop-Lizenzserver installiert ist, der den Suchkriterien entspricht.</span><span class="sxs-lookup"><span data-stu-id="c3c81-119">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and returns the next key pack that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-120">**Tlslicenseenumbegin**</span><span class="sxs-lookup"><span data-stu-id="c3c81-120">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dd>

<span data-ttu-id="c3c81-121">Beginnt die Enumeration von Lizenzen, die vom Remotedesktop Lizenzserver basierend auf Suchkriterien ausgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c3c81-121">Begins enumeration of licenses that are issued by the Remote Desktop license server based on search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-122">**Tlslicenabenumend**</span><span class="sxs-lookup"><span data-stu-id="c3c81-122">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> <dd>

<span data-ttu-id="c3c81-123">Wird von einem vorherigen-Befehl der [**tlslicenseenumbegin**](tlslicenseenumbegin.md) -Funktion fortgesetzt und beendet die-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="c3c81-123">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and terminates the enumeration.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-124">**Tlslicensitztenenumnext**</span><span class="sxs-lookup"><span data-stu-id="c3c81-124">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> <dd>

<span data-ttu-id="c3c81-125">Wird von einem vorherigen aufrufsvorgang der [**tlslicenseenumbegin**](tlslicenseenumbegin.md) -Funktion fortgesetzt und gibt die nächste Lizenz zurück, die auf einem Remotedesktop Lizenzserver installiert ist, der den Suchkriterien entspricht.</span><span class="sxs-lookup"><span data-stu-id="c3c81-125">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and returns the next license that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-126">**Virtualchannelclose**</span><span class="sxs-lookup"><span data-stu-id="c3c81-126">**VirtualChannelClose**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)
</dt> <dd>

<span data-ttu-id="c3c81-127">Schließt das Client Ende eines virtuellen Kanals.</span><span class="sxs-lookup"><span data-stu-id="c3c81-127">Closes the client end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-128">**Virtualchannelentry**</span><span class="sxs-lookup"><span data-stu-id="c3c81-128">**VirtualChannelEntry**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry)
</dt> <dd>

<span data-ttu-id="c3c81-129">Ein Anwendungs definierter Einstiegspunkt für die Client seitige dll einer Anwendung, die Remotedesktopdienste virtuellen Kanälen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3c81-129">An application-defined entry point for the client-side DLL of an application that uses Remote Desktop Services virtual channels.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-130">**Virtualchannelinit**</span><span class="sxs-lookup"><span data-stu-id="c3c81-130">**VirtualChannelInit**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)
</dt> <dd>

<span data-ttu-id="c3c81-131">Initialisiert den Zugriff einer Client-DLL auf Remotedesktopdienste virtuellen Channels.</span><span class="sxs-lookup"><span data-stu-id="c3c81-131">Initializes a client DLL's access to Remote Desktop Services virtual channels.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-132">*Virtualchannelinitevent*</span><span class="sxs-lookup"><span data-stu-id="c3c81-132">*VirtualChannelInitEvent*</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn)
</dt> <dd>

<span data-ttu-id="c3c81-133">Eine von der Anwendung definierte Rückruffunktion, Remotedesktopdienste die aufruft, um die Client-DLL von virtuellen Kanal Ereignissen zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="c3c81-133">An application-defined callback function that Remote Desktop Services calls to notify the client DLL of virtual channel events.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-134">**Virtualchannelopen**</span><span class="sxs-lookup"><span data-stu-id="c3c81-134">**VirtualChannelOpen**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)
</dt> <dd>

<span data-ttu-id="c3c81-135">Öffnet das Client Ende eines virtuellen Kanals.</span><span class="sxs-lookup"><span data-stu-id="c3c81-135">Opens the client end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-136">*Virtualchannelopenevent*</span><span class="sxs-lookup"><span data-stu-id="c3c81-136">*VirtualChannelOpenEvent*</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn)
</dt> <dd>

<span data-ttu-id="c3c81-137">Eine von der Anwendung definierte Rückruffunktion, mit der aufgerufen wird Remotedesktopdienste, um die Client-DLL über Ereignisse für einen bestimmten virtuellen Kanal zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="c3c81-137">An application-defined callback function that Remote Desktop Services calls to notify the client DLL of events for a specific virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-138">**Virtualchannelwrite**</span><span class="sxs-lookup"><span data-stu-id="c3c81-138">**VirtualChannelWrite**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)
</dt> <dd>

<span data-ttu-id="c3c81-139">Sendet Daten vom Client Ende eines virtuellen Kanals an eine Partner Anwendung auf dem Server Ende.</span><span class="sxs-lookup"><span data-stu-id="c3c81-139">Sends data from the client end of a virtual channel to a partner application on the server end.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-140">**Wtscloseserver**</span><span class="sxs-lookup"><span data-stu-id="c3c81-140">**WTSCloseServer**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver)
</dt> <dd>

<span data-ttu-id="c3c81-141">Schließt ein geöffnetes Handle für einen Remotedesktop-Sitzungshost Server (RD-Sitzungshost).</span><span class="sxs-lookup"><span data-stu-id="c3c81-141">Closes an open handle to a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-142">**Wzconneczession**</span><span class="sxs-lookup"><span data-stu-id="c3c81-142">**WTSConnectSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona)
</dt> <dd>

<span data-ttu-id="c3c81-143">Verbindet eine Remotedesktopdienste Sitzung mit einer vorhandenen Sitzung auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="c3c81-143">Connects a Remote Desktop Services session to an existing session on the local computer.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-144">**Wtscreatelistener**</span><span class="sxs-lookup"><span data-stu-id="c3c81-144">**WTSCreateListener**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscreatelistenera)
</dt> <dd>

<span data-ttu-id="c3c81-145">Erstellt einen neuen Remotedesktopdienste Listener oder konfiguriert einen vorhandenen Listener.</span><span class="sxs-lookup"><span data-stu-id="c3c81-145">Creates a new Remote Desktop Services listener or configures an existing listener.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-146">**Wzdisconneczession**</span><span class="sxs-lookup"><span data-stu-id="c3c81-146">**WTSDisconnectSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)
</dt> <dd>

<span data-ttu-id="c3c81-147">Trennt den angemeldeten Benutzer von der angegebenen Remotedesktopdienste Sitzung, ohne die Sitzung zu schließen.</span><span class="sxs-lookup"><span data-stu-id="c3c81-147">Disconnects the logged-on user from the specified Remote Desktop Services session without closing the session.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-148">**Wtsenablechildsessions**</span><span class="sxs-lookup"><span data-stu-id="c3c81-148">**WTSEnableChildSessions**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
</dt> <dd>

<span data-ttu-id="c3c81-149">Aktiviert oder deaktiviert untergeordnete [Sitzungen](child-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="c3c81-149">Enables or disables [Child Sessions](child-sessions.md).</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-150">**WTSEnumerateListeners**</span><span class="sxs-lookup"><span data-stu-id="c3c81-150">**WTSEnumerateListeners**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratelistenersa)
</dt> <dd>

<span data-ttu-id="c3c81-151">Listet alle Remotedesktopdienste Listener auf einem RD-Sitzungshost Server auf.</span><span class="sxs-lookup"><span data-stu-id="c3c81-151">Enumerates all the Remote Desktop Services listeners on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-152">**Wtsenum erateprocesses**</span><span class="sxs-lookup"><span data-stu-id="c3c81-152">**WTSEnumerateProcesses**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)
</dt> <dd>

<span data-ttu-id="c3c81-153">Ruft Informationen zu den aktiven Prozessen auf einem angegebenen RD-Sitzungshost Server ab.</span><span class="sxs-lookup"><span data-stu-id="c3c81-153">Retrieves information about the active processes on a specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-154">**Wtsenenerateprocessesex**</span><span class="sxs-lookup"><span data-stu-id="c3c81-154">**WTSEnumerateProcessesEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesexa)
</dt> <dd>

<span data-ttu-id="c3c81-155">Ruft Informationen zu den aktiven Prozessen auf dem angegebenen RD-Sitzungshost Server oder Remotedesktop-Virtualisierungshost Server (RD-Virtualisierungshost) ab.</span><span class="sxs-lookup"><span data-stu-id="c3c81-155">Retrieves information about the active processes on the specified RD Session Host server or Remote Desktop Virtualization Host (RD Virtualization Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-156">**Wtsenum erateservers**</span><span class="sxs-lookup"><span data-stu-id="c3c81-156">**WTSEnumerateServers**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateserversa)
</dt> <dd>

<span data-ttu-id="c3c81-157">Gibt eine Liste aller RD-Sitzungshost Server innerhalb der angegebenen Domäne zurück.</span><span class="sxs-lookup"><span data-stu-id="c3c81-157">Returns a list of all RD Session Host servers within the specified domain.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-158">**Wtseneneratesessions**</span><span class="sxs-lookup"><span data-stu-id="c3c81-158">**WTSEnumerateSessions**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)
</dt> <dd>

<span data-ttu-id="c3c81-159">Ruft eine Liste von Sitzungen auf einem RD-Sitzungshost Server ab.</span><span class="sxs-lookup"><span data-stu-id="c3c81-159">Retrieves a list of sessions on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-160">**Wtseneneratesessionsex**</span><span class="sxs-lookup"><span data-stu-id="c3c81-160">**WTSEnumerateSessionsEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsexa)
</dt> <dd>

<span data-ttu-id="c3c81-161">Ruft eine Liste von Sitzungen auf einem angegebenen RD-Sitzungshost Server oder Remote Desktop-Virtualisierungshostserver ab.</span><span class="sxs-lookup"><span data-stu-id="c3c81-161">Retrieves a list of sessions on a specified RD Session Host server or RD Virtualization Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-162">**Wout-Speicher**</span><span class="sxs-lookup"><span data-stu-id="c3c81-162">**WTSFreeMemory**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory)
</dt> <dd>

<span data-ttu-id="c3c81-163">Gibt durch eine Remotedesktopdienste Funktion zugeordnete Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="c3c81-163">Frees memory allocated by a Remote Desktop Services function.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-164">**Wout-memoryex**</span><span class="sxs-lookup"><span data-stu-id="c3c81-164">**WTSFreeMemoryEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememoryexa)
</dt> <dd>

<span data-ttu-id="c3c81-165">Gibt Arbeitsspeicher frei, der die von einer Remotedesktopdienste Funktion zugeordneten Strukturen der [**WTS \_ Process \_ Info \_ Ex**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa) oder der [**WTS \_ Session \_ Info \_ 1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a) enthält.</span><span class="sxs-lookup"><span data-stu-id="c3c81-165">Frees memory that contains [**WTS\_PROCESS\_INFO\_EX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa) or [**WTS\_SESSION\_INFO\_1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a) structures allocated by a Remote Desktop Services function.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-166">**Wout getactiveconsolesessionid**</span><span class="sxs-lookup"><span data-stu-id="c3c81-166">**WTSGetActiveConsoleSessionId**</span></span>](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid)
</dt> <dd>

<span data-ttu-id="c3c81-167">Ruft den Sitzungs Bezeichner der Konsolen Sitzung ab.</span><span class="sxs-lookup"><span data-stu-id="c3c81-167">Retrieves the session identifier of the console session.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-168">**Wout getchildsessionid**</span><span class="sxs-lookup"><span data-stu-id="c3c81-168">**WTSGetChildSessionId**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
</dt> <dd>

<span data-ttu-id="c3c81-169">Ruft den Bezeichner der untergeordneten Sitzung ab, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c3c81-169">Retrieves the child session identifier, if present.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-170">**Wtgetlistenersecurity**</span><span class="sxs-lookup"><span data-stu-id="c3c81-170">**WTSGetListenerSecurity**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetlistenersecuritya)
</dt> <dd>

<span data-ttu-id="c3c81-171">Ruft die Sicherheits Beschreibung eines Remotedesktopdienste Listener ab.</span><span class="sxs-lookup"><span data-stu-id="c3c81-171">Retrieves the security descriptor of a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-172">**Wtsischildsessionsenabled**</span><span class="sxs-lookup"><span data-stu-id="c3c81-172">**WTSIsChildSessionsEnabled**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
</dt> <dd>

<span data-ttu-id="c3c81-173">Bestimmt, ob untergeordnete Sitzungen aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="c3c81-173">Determines whether child sessions are enabled.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-174">**Wunglogoffsession**</span><span class="sxs-lookup"><span data-stu-id="c3c81-174">**WTSLogoffSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)
</dt> <dd>

<span data-ttu-id="c3c81-175">Protokolliert eine angegebene Remotedesktopdienste Sitzung ab.</span><span class="sxs-lookup"><span data-stu-id="c3c81-175">Logs off a specified Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-176">**Wout OpenServer**</span><span class="sxs-lookup"><span data-stu-id="c3c81-176">**WTSOpenServer**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera)
</dt> <dd>

<span data-ttu-id="c3c81-177">Öffnet ein Handle für den angegebenen RD-Sitzungshost Server.</span><span class="sxs-lookup"><span data-stu-id="c3c81-177">Opens a handle to the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-178">**Wout openserverex**</span><span class="sxs-lookup"><span data-stu-id="c3c81-178">**WTSOpenServerEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenserverexa)
</dt> <dd>

<span data-ttu-id="c3c81-179">Öffnet ein Handle für den angegebenen RD-Sitzungshost Server oder Remote Desktop-Virtualisierungshostserver.</span><span class="sxs-lookup"><span data-stu-id="c3c81-179">Opens a handle to the specified RD Session Host server or RD Virtualization Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-180">**Wout querylistenerconfig**</span><span class="sxs-lookup"><span data-stu-id="c3c81-180">**WTSQueryListenerConfig**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerylistenerconfiga)
</dt> <dd>

<span data-ttu-id="c3c81-181">Ruft Konfigurationsinformationen für einen Remotedesktopdienste Listener ab.</span><span class="sxs-lookup"><span data-stu-id="c3c81-181">Retrieves configuration information for a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-182">**Wzquerysessioninformation**</span><span class="sxs-lookup"><span data-stu-id="c3c81-182">**WTSQuerySessionInformation**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa)
</dt> <dd>

<span data-ttu-id="c3c81-183">Ruft Sitzungsinformationen für die angegebene Sitzung auf dem angegebenen RD-Sitzungshost Server ab.</span><span class="sxs-lookup"><span data-stu-id="c3c81-183">Retrieves session information for the specified session on the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-184">**Wout queryuserconfig**</span><span class="sxs-lookup"><span data-stu-id="c3c81-184">**WTSQueryUserConfig**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga)
</dt> <dd>

<span data-ttu-id="c3c81-185">Ruft Konfigurationsinformationen für den angegebenen Benutzer auf dem angegebenen Domänen Controller oder RD-Sitzungshost Server ab.</span><span class="sxs-lookup"><span data-stu-id="c3c81-185">Retrieves configuration information for the specified user on the specified domain controller or RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-186">**Wtqueryusertoken**</span><span class="sxs-lookup"><span data-stu-id="c3c81-186">**WTSQueryUserToken**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryusertoken)
</dt> <dd>

<span data-ttu-id="c3c81-187">Ruft das primäre Zugriffs Token des angemeldeten Benutzers ab, der von der Sitzungs-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c3c81-187">Obtains the primary access token of the logged-on user specified by the session ID.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-188">**Wwahrheits registersessionnotification**</span><span class="sxs-lookup"><span data-stu-id="c3c81-188">**WTSRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dd>

<span data-ttu-id="c3c81-189">Registriert das angegebene Fenster für den Empfang von Sitzungs Änderungs Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="c3c81-189">Registers the specified window to receive session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-190">**Wzregistersessionnotificationex**</span><span class="sxs-lookup"><span data-stu-id="c3c81-190">**WTSRegisterSessionNotificationEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex)
</dt> <dd>

<span data-ttu-id="c3c81-191">Registriert das angegebene Fenster für den Empfang von Sitzungs Änderungs Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="c3c81-191">Registers the specified window to receive session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-192">**Wtssendmessage**</span><span class="sxs-lookup"><span data-stu-id="c3c81-192">**WTSSendMessage**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)
</dt> <dd>

<span data-ttu-id="c3c81-193">Zeigt ein Meldungs Feld auf dem Client Desktop einer angegebenen Remotedesktopdienste Sitzung an.</span><span class="sxs-lookup"><span data-stu-id="c3c81-193">Displays a message box on the client desktop of a specified Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-194">**Wtsetlistenersecurity**</span><span class="sxs-lookup"><span data-stu-id="c3c81-194">**WTSSetListenerSecurity**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetlistenersecuritya)
</dt> <dd>

<span data-ttu-id="c3c81-195">Konfiguriert die Sicherheits Beschreibung eines Remotedesktopdienste Listener.</span><span class="sxs-lookup"><span data-stu-id="c3c81-195">Configures the security descriptor of a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-196">**Wout-tuserconfig**</span><span class="sxs-lookup"><span data-stu-id="c3c81-196">**WTSSetUserConfig**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga)
</dt> <dd>

<span data-ttu-id="c3c81-197">Ändert die Konfigurationsinformationen für den angegebenen Benutzer auf dem angegebenen Domänen Controller oder RD-Sitzungshost Server.</span><span class="sxs-lookup"><span data-stu-id="c3c81-197">Modifies configuration information for the specified user on the specified domain controller or RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-198">**Wungshutdownsystem**</span><span class="sxs-lookup"><span data-stu-id="c3c81-198">**WTSShutdownSystem**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)
</dt> <dd>

<span data-ttu-id="c3c81-199">Fährt den angegebenen RD-Sitzungshost Server herunter (und startet ihn optional neu).</span><span class="sxs-lookup"><span data-stu-id="c3c81-199">Shuts down (and optionally restarts) the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-200">**Wout startremotecontrolsession**</span><span class="sxs-lookup"><span data-stu-id="c3c81-200">**WTSStartRemoteControlSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona)
</dt> <dd>

<span data-ttu-id="c3c81-201">Startet die Remote Steuerung einer anderen Remotedesktopdienste Sitzung.</span><span class="sxs-lookup"><span data-stu-id="c3c81-201">Starts the remote control of another Remote Desktop Services session.</span></span> <span data-ttu-id="c3c81-202">Diese Funktion muss von einer Remote Sitzung aus aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c3c81-202">You must call this function from a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-203">**Wout stopremotecontrolsession**</span><span class="sxs-lookup"><span data-stu-id="c3c81-203">**WTSStopRemoteControlSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession)
</dt> <dd>

<span data-ttu-id="c3c81-204">Beendet eine Remote Steuerungs Sitzung.</span><span class="sxs-lookup"><span data-stu-id="c3c81-204">Stops a remote control session.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-205">**Wtsterminateprocess**</span><span class="sxs-lookup"><span data-stu-id="c3c81-205">**WTSTerminateProcess**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)
</dt> <dd>

<span data-ttu-id="c3c81-206">Beendet den angegebenen Prozess auf dem angegebenen RD-Sitzungshost Server.</span><span class="sxs-lookup"><span data-stu-id="c3c81-206">Terminates the specified process on the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-207">**WTSUnRegisterSessionNotification**</span><span class="sxs-lookup"><span data-stu-id="c3c81-207">**WTSUnRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> <dd>

<span data-ttu-id="c3c81-208">Hebt die Registrierung des angegebenen Fensters auf, sodass keine weiteren Sitzungs Änderungs Benachrichtigungen empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="c3c81-208">Unregisters the specified window so that it receives no further session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-209">**Wtsunregistersessionnotificationex**</span><span class="sxs-lookup"><span data-stu-id="c3c81-209">**WTSUnRegisterSessionNotificationEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex)
</dt> <dd>

<span data-ttu-id="c3c81-210">Hebt die Registrierung des angegebenen Fensters auf, sodass keine weiteren Sitzungs Änderungs Benachrichtigungen empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="c3c81-210">Unregisters the specified window so that it receives no further session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-211">**Wout virtualchannelclose**</span><span class="sxs-lookup"><span data-stu-id="c3c81-211">**WTSVirtualChannelClose**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

<span data-ttu-id="c3c81-212">Schließt einen geöffneten virtuellen Kanal handle.</span><span class="sxs-lookup"><span data-stu-id="c3c81-212">Closes an open virtual channel handle.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-213">**Wout virtualchannelopen**</span><span class="sxs-lookup"><span data-stu-id="c3c81-213">**WTSVirtualChannelOpen**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)
</dt> <dd>

<span data-ttu-id="c3c81-214">Öffnet ein Handle für das Server Ende eines angegebenen virtuellen Kanals.</span><span class="sxs-lookup"><span data-stu-id="c3c81-214">Opens a handle to the server end of a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-215">**Wout virtualchannelopenex**</span><span class="sxs-lookup"><span data-stu-id="c3c81-215">**WTSVirtualChannelOpenEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex)
</dt> <dd>

<span data-ttu-id="c3c81-216">Erstellt einen virtuellen Kanal auf eine Weise, die dem [**Wout-virtualchannelopen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)ähnelt.</span><span class="sxs-lookup"><span data-stu-id="c3c81-216">Creates a virtual channel in a manner similar to [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen).</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-217">**WGs virtualchannelpurgeinput**</span><span class="sxs-lookup"><span data-stu-id="c3c81-217">**WTSVirtualChannelPurgeInput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

<span data-ttu-id="c3c81-218">Löscht alle in die Warteschlange eingereihten Eingabedaten, die vom Client an den Server auf einem angegebenen virtuellen Kanal gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3c81-218">Deletes all queued input data sent from the client to the server on a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-219">**Wzvirtualchannelpurgeoutput**</span><span class="sxs-lookup"><span data-stu-id="c3c81-219">**WTSVirtualChannelPurgeOutput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

<span data-ttu-id="c3c81-220">Löscht alle in die Warteschlange eingereihten Ausgabedaten, die vom Server an den Client auf einem angegebenen virtuellen Kanal gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3c81-220">Deletes all queued output data sent from the server to the client on a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-221">**Wout virtualchannelquery**</span><span class="sxs-lookup"><span data-stu-id="c3c81-221">**WTSVirtualChannelQuery**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

<span data-ttu-id="c3c81-222">Gibt Informationen zu einem angegebenen virtuellen Kanal zurück.</span><span class="sxs-lookup"><span data-stu-id="c3c81-222">Returns information about a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-223">**Wout virtualchannelread**</span><span class="sxs-lookup"><span data-stu-id="c3c81-223">**WTSVirtualChannelRead**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

<span data-ttu-id="c3c81-224">Liest Daten vom Server Ende eines virtuellen Kanals.</span><span class="sxs-lookup"><span data-stu-id="c3c81-224">Reads data from the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-225">**Wout virtualchannelwrite**</span><span class="sxs-lookup"><span data-stu-id="c3c81-225">**WTSVirtualChannelWrite**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

<span data-ttu-id="c3c81-226">Schreibt Daten auf das Server Ende eines virtuellen Kanals.</span><span class="sxs-lookup"><span data-stu-id="c3c81-226">Writes data to the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="c3c81-227">**Wout waitsystemevent**</span><span class="sxs-lookup"><span data-stu-id="c3c81-227">**WTSWaitSystemEvent**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)
</dt> <dd>

<span data-ttu-id="c3c81-228">Wartet auf ein Remotedesktopdienste Ereignis, bevor es zum Aufrufer zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="c3c81-228">Waits for a Remote Desktop Services event before returning to the caller.</span></span>

</dd> </dl>

 

 