---
title: Remotedesktopdienste API-Strukturen
description: Listet Strukturen auf, die mit der Remotedesktopdienste-API verwendet werden.
ms.assetid: 5d467241-499c-4038-8d9c-4244457e484f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fb8de65f7f234f85eb8071cc66743c9c26cc9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101690"
---
# <a name="remote-desktop-services-api-structures"></a><span data-ttu-id="f55e7-103">Remotedesktopdienste API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f55e7-103">Remote Desktop Services API Structures</span></span>

<span data-ttu-id="f55e7-104">Die folgenden Strukturen werden mit der Remotedesktopdienste-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="f55e7-104">The following structures are used with the Remote Desktop Services API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f55e7-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="f55e7-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="f55e7-106">**Channel \_ DEF**</span><span class="sxs-lookup"><span data-stu-id="f55e7-106">**CHANNEL\_DEF**</span></span>](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dd>

<span data-ttu-id="f55e7-107">Enthält den Namen und die Optionen eines Remotedesktopdienste virtuellen Kanals.</span><span class="sxs-lookup"><span data-stu-id="f55e7-107">Contains the name and options of a Remote Desktop Services virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-108">**Kanal \_ Einstiegs \_ Punkte**</span><span class="sxs-lookup"><span data-stu-id="f55e7-108">**CHANNEL\_ENTRY\_POINTS**</span></span>](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points)
</dt> <dd>

<span data-ttu-id="f55e7-109">Enthält Zeiger auf die Funktionen, die von einer Client seitigen dll aufgerufen werden, um auf virtuelle Kanäle zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="f55e7-109">Contains pointers to the functions called by a client-side DLL to access virtual channels.</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-110">**Channel- \_ PDU- \_ Header**</span><span class="sxs-lookup"><span data-stu-id="f55e7-110">**CHANNEL\_PDU\_HEADER**</span></span>](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)
</dt> <dd>

<span data-ttu-id="f55e7-111">Enthält Informationen zu einem Datenblock, der vom Server Ende eines virtuellen Kanals empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="f55e7-111">Contains information about a data block being received by the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-112">**Lschräypack**</span><span class="sxs-lookup"><span data-stu-id="f55e7-112">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dd>

<span data-ttu-id="f55e7-113">Enthält Informationen zu einem bestimmten Remotedesktopdienste Licensing Key Pack.</span><span class="sxs-lookup"><span data-stu-id="f55e7-113">Contains information about a specific Remote Desktop Services licensing key pack.</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-114">**Lslicense**</span><span class="sxs-lookup"><span data-stu-id="f55e7-114">**LSLicense**</span></span>](lslicense.md)
</dt> <dd>

<span data-ttu-id="f55e7-115">Enthält Informationen zu einer bestimmten Remotedesktopdienste Lizenz.</span><span class="sxs-lookup"><span data-stu-id="f55e7-115">Contains information about a specific Remote Desktop Services license.</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-116">**WTSClient**</span><span class="sxs-lookup"><span data-stu-id="f55e7-116">**WTSCLIENT**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta)
</dt> <dd>

<span data-ttu-id="f55e7-117">Enthält Informationen zu einem Remotedesktopverbindung-Client (RDC).</span><span class="sxs-lookup"><span data-stu-id="f55e7-117">Contains information about a Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-118">**WT configinfo**</span><span class="sxs-lookup"><span data-stu-id="f55e7-118">**WTSCONFIGINFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsconfiginfoa)
</dt> <dd>

<span data-ttu-id="f55e7-119">Enthält Informationen zu einer Remotedesktopdienste Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f55e7-119">Contains information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-120">**Wtsinfo**</span><span class="sxs-lookup"><span data-stu-id="f55e7-120">**WTSINFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa)
</dt> <dd>

<span data-ttu-id="f55e7-121">Enthält Informationen zu einer Remotedesktopdienste Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f55e7-121">Contains information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-122">**Wtsinfoex**</span><span class="sxs-lookup"><span data-stu-id="f55e7-122">**WTSINFOEX**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoexa)
</dt> <dd>

<span data-ttu-id="f55e7-123">Enthält eine Union der [**wtsinfoex- \_ Ebene**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) , die erweiterte Informationen zu einer Remotedesktopdienste Sitzung enthält.</span><span class="sxs-lookup"><span data-stu-id="f55e7-123">Contains a [**WTSINFOEX\_LEVEL**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) union that contains extended information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-124">**Wtsinfoex \_ Level1**</span><span class="sxs-lookup"><span data-stu-id="f55e7-124">**WTSINFOEX\_LEVEL1**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level1_a)
</dt> <dd>

<span data-ttu-id="f55e7-125">Enthält erweiterte Informationen zu einer Remotedesktopdienste Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f55e7-125">Contains extended information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-126">**Wout-listenerconfig**</span><span class="sxs-lookup"><span data-stu-id="f55e7-126">**WTSLISTENERCONFIG**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtslistenerconfiga)
</dt> <dd>

<span data-ttu-id="f55e7-127">Enthält Informationen zu einem Remotedesktopdienste Listener.</span><span class="sxs-lookup"><span data-stu-id="f55e7-127">Contains information about a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-128">**wtssbx \_ -IP- \_ Adresse**</span><span class="sxs-lookup"><span data-stu-id="f55e7-128">**WTSSBX\_IP\_ADDRESS**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_ip_address)
</dt> <dd>

<span data-ttu-id="f55e7-129">Enthält Informationen über die IP-Adresse einer Netzwerkressource.</span><span class="sxs-lookup"><span data-stu-id="f55e7-129">Contains information about the IP address of a network resource.</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-130">**wtssbx- \_ Computer \_ Verbindungs \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="f55e7-130">**WTSSBX\_MACHINE\_CONNECT\_INFO**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_connect_info)
</dt> <dd>

<span data-ttu-id="f55e7-131">Enthält Informationen zu einem Computer, der Remote Verbindungen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="f55e7-131">Contains information about a computer that is accepting remote connections.</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-132">**wtssbx- \_ Computer \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="f55e7-132">**WTSSBX\_MACHINE\_INFO**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_info)
</dt> <dd>

<span data-ttu-id="f55e7-133">Enthält Informationen über einen Computer und seinen aktuellen Zustand.</span><span class="sxs-lookup"><span data-stu-id="f55e7-133">Contains information about a computer and its current state.</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-134">**wtssbx- \_ Sitzungs \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="f55e7-134">**WTSSBX\_SESSION\_INFO**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_session_info)
</dt> <dd>

<span data-ttu-id="f55e7-135">Enthält Informationen zu Sitzungen, die für Remotedesktopverbindung Broker (RD-Verbindungsbroker) verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f55e7-135">Contains information about sessions that are available to Remote Desktop Connection Broker (RD Connection Broker).</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-136">**wtssession- \_ Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="f55e7-136">**WTSSESSION\_NOTIFICATION**</span></span>](/windows/win32/api/winuser/ns-winuser-wtssession_notification)
</dt> <dd>

<span data-ttu-id="f55e7-137">Enthält Informationen über die Sitzungs Änderungs Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="f55e7-137">Provides information about the session change notification.</span></span> <span data-ttu-id="f55e7-138">Ein Dienst empfängt diese Struktur in seiner [*handlerex*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) -Funktion als Reaktion auf ein Sitzungs Änderungs Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f55e7-138">A service receives this structure in its [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) function in response to a session change event.</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-139">**Wtsuserconfig**</span><span class="sxs-lookup"><span data-stu-id="f55e7-139">**WTSUSERCONFIG**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsuserconfiga)
</dt> <dd>

<span data-ttu-id="f55e7-140">Enthält Konfigurationsinformationen für einen Benutzer auf einem Domänen Controller oder Remotedesktop-Sitzungshost Server (RD-Sitzungshost).</span><span class="sxs-lookup"><span data-stu-id="f55e7-140">Contains configuration information for a user on a domain controller or Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-141">**WTS- \_ Client \_ Adresse**</span><span class="sxs-lookup"><span data-stu-id="f55e7-141">**WTS\_CLIENT\_ADDRESS**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_address)
</dt> <dd>

<span data-ttu-id="f55e7-142">Enthält die Client Netzwerkadresse einer Remotedesktopdienste Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f55e7-142">Contains the client network address of a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-143">**Anzeige des WTS- \_ Clients \_**</span><span class="sxs-lookup"><span data-stu-id="f55e7-143">**WTS\_CLIENT\_DISPLAY**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_display)
</dt> <dd>

<span data-ttu-id="f55e7-144">Enthält Informationen zur Anzeige eines-Remotedesktopverbindung (RDC)-Clients.</span><span class="sxs-lookup"><span data-stu-id="f55e7-144">Contains information about the display of a Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-145">**Informationen zum WTS- \_ Prozess \_**</span><span class="sxs-lookup"><span data-stu-id="f55e7-145">**WTS\_PROCESS\_INFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_infoa)
</dt> <dd>

<span data-ttu-id="f55e7-146">Enthält Informationen zu einem Prozess, der auf einem RD-Sitzungshost Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f55e7-146">Contains information about a process running on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-147">**Informationen zum WTS- \_ Prozess \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f55e7-147">**WTS\_PROCESS\_INFO\_EX**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa)
</dt> <dd>

<span data-ttu-id="f55e7-148">Enthält erweiterte Informationen zu einem Prozess, der auf einem RD-Sitzungshost Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f55e7-148">Contains extended information about a process running on a RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="f55e7-149">[**WTS- \_ Produkt \_ Informationen**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="f55e7-149">[**WTS\_PRODUCT\_INFO**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)</span></span>
</dt> <dd>

<span data-ttu-id="f55e7-150">Die Details der Produktlizenz, die benötigt wird, um eine Verbindung mit einem Terminal Server herzustellen.</span><span class="sxs-lookup"><span data-stu-id="f55e7-150">The details of the product license that is required to connect to a terminal server.</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-151">**Informationen zum WTS- \_ Server \_**</span><span class="sxs-lookup"><span data-stu-id="f55e7-151">**WTS\_SERVER\_INFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_server_infoa)
</dt> <dd>

<span data-ttu-id="f55e7-152">Enthält Informationen zu einem bestimmten Remotedesktopdienste Server.</span><span class="sxs-lookup"><span data-stu-id="f55e7-152">Contains information about a specific Remote Desktop Services server.</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-153">**WTS- \_ Sitzungs \_ Adresse**</span><span class="sxs-lookup"><span data-stu-id="f55e7-153">**WTS\_SESSION\_ADDRESS**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_address)
</dt> <dd>

<span data-ttu-id="f55e7-154">Enthält die virtuelle IP-Adresse, die einer Sitzung zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="f55e7-154">Contains the virtual IP address assigned to a session.</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-155">**Informationen zur WTS- \_ Sitzung \_**</span><span class="sxs-lookup"><span data-stu-id="f55e7-155">**WTS\_SESSION\_INFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_infoa)
</dt> <dd>

<span data-ttu-id="f55e7-156">Enthält Informationen über eine Client Sitzung auf einem RD-Sitzungshost-Server.</span><span class="sxs-lookup"><span data-stu-id="f55e7-156">Contains information about a client session on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="f55e7-157">**Informationen zur WTS- \_ Sitzung \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="f55e7-157">**WTS\_SESSION\_INFO\_1**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a)
</dt> <dd>

<span data-ttu-id="f55e7-158">Enthält erweiterte Informationen über eine Client Sitzung auf einem RD-Sitzungshost Server oder Remotedesktop-Virtualisierungshost-Server (RD-Virtualisierungshost).</span><span class="sxs-lookup"><span data-stu-id="f55e7-158">Contains extended information about a client session on a RD Session Host server or Remote Desktop Virtualization Host (RD Virtualization Host) server.</span></span>

</dd> </dl>

 

 