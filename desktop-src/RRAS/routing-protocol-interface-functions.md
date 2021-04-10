---
title: Routing Protokoll Schnittstellen-Funktionen
description: Implementieren Sie die folgenden Funktionen für eine Routing Protokoll-dll.
ms.assetid: fd780458-ef23-4ef2-8fe8-29b32100917f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b696d516cf0fc0b13d66fdc53b384a28fac8696a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949072"
---
# <a name="routing-protocol-interface-functions"></a><span data-ttu-id="995d9-103">Routing Protokoll Schnittstellen-Funktionen</span><span class="sxs-lookup"><span data-stu-id="995d9-103">Routing Protocol Interface Functions</span></span>

<span data-ttu-id="995d9-104">Implementieren Sie die folgenden Funktionen für eine Routing Protokoll-dll:</span><span class="sxs-lookup"><span data-stu-id="995d9-104">Implement the following functions for a routing protocol DLL:</span></span>

[<span data-ttu-id="995d9-105">**AddInterface**</span><span class="sxs-lookup"><span data-stu-id="995d9-105">**AddInterface**</span></span>](/windows/desktop/api/Routprot/nc-routprot-padd_interface)

[<span data-ttu-id="995d9-106">**Connectclient**</span><span class="sxs-lookup"><span data-stu-id="995d9-106">**ConnectClient**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pconnect_client)

[<span data-ttu-id="995d9-107">**Delta Info**</span><span class="sxs-lookup"><span data-stu-id="995d9-107">**DeleteInterface**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pdelete_interface)

[<span data-ttu-id="995d9-108">**Disconnectclient**</span><span class="sxs-lookup"><span data-stu-id="995d9-108">**DisconnectClient**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pdisconnect_client)

[<span data-ttu-id="995d9-109">**Doupdateroutes**</span><span class="sxs-lookup"><span data-stu-id="995d9-109">**DoUpdateRoutes**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pdo_update_routes)

<span data-ttu-id="995d9-110">[*"Doupdateservices"*](/previous-versions/windows/desktop/legacy/aa374005(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="995d9-110">[*DoUpdateServices*](/previous-versions/windows/desktop/legacy/aa374005(v=vs.85))</span></span>

[<span data-ttu-id="995d9-111">**Geteventmessage**</span><span class="sxs-lookup"><span data-stu-id="995d9-111">**GetEventMessage**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pget_event_message)

[<span data-ttu-id="995d9-112">**GetGlobalInfo**</span><span class="sxs-lookup"><span data-stu-id="995d9-112">**GetGlobalInfo**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pget_global_info)

[<span data-ttu-id="995d9-113">**Getinterfacetten Info**</span><span class="sxs-lookup"><span data-stu-id="995d9-113">**GetInterfaceInfo**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info)

[<span data-ttu-id="995d9-114">**Getmfestatus**</span><span class="sxs-lookup"><span data-stu-id="995d9-114">**GetMfeStatus**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pget_mfe_status)

[<span data-ttu-id="995d9-115">**GetNeighbors**</span><span class="sxs-lookup"><span data-stu-id="995d9-115">**GetNeighbors**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pget_neighbors)

[<span data-ttu-id="995d9-116">**Interfacestatus**</span><span class="sxs-lookup"><span data-stu-id="995d9-116">**InterfaceStatus**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pinterface_status)

[<span data-ttu-id="995d9-117">**Mibcreate**</span><span class="sxs-lookup"><span data-stu-id="995d9-117">**MibCreate**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_create)

[<span data-ttu-id="995d9-118">**Mibdelete**</span><span class="sxs-lookup"><span data-stu-id="995d9-118">**MibDelete**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_delete)

[<span data-ttu-id="995d9-119">**Mibget**</span><span class="sxs-lookup"><span data-stu-id="995d9-119">**MibGet**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_get)

[<span data-ttu-id="995d9-120">**Mibgetfirst**</span><span class="sxs-lookup"><span data-stu-id="995d9-120">**MibGetFirst**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_get_first)

[<span data-ttu-id="995d9-121">**Mibgetnext**</span><span class="sxs-lookup"><span data-stu-id="995d9-121">**MibGetNext**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_get_next)

[<span data-ttu-id="995d9-122">*Mibgettrapinfo*</span><span class="sxs-lookup"><span data-stu-id="995d9-122">*MibGetTrapInfo*</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_get_trap_info)

[<span data-ttu-id="995d9-123">**Mibset**</span><span class="sxs-lookup"><span data-stu-id="995d9-123">**MibSet**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_set)

[<span data-ttu-id="995d9-124">**Mibsettrapinfo**</span><span class="sxs-lookup"><span data-stu-id="995d9-124">**MibSetTrapInfo**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_set_trap_info)

[<span data-ttu-id="995d9-125">**Querypower**</span><span class="sxs-lookup"><span data-stu-id="995d9-125">**QueryPower**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pquery_power)

[<span data-ttu-id="995d9-126">**Register Protocol**</span><span class="sxs-lookup"><span data-stu-id="995d9-126">**RegisterProtocol**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)

[<span data-ttu-id="995d9-127">**Setglobalinfo**</span><span class="sxs-lookup"><span data-stu-id="995d9-127">**SetGlobalInfo**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pset_global_info)

[<span data-ttu-id="995d9-128">**Setinterfacetten Info**</span><span class="sxs-lookup"><span data-stu-id="995d9-128">**SetInterfaceInfo**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info)

[<span data-ttu-id="995d9-129">**SetPower**</span><span class="sxs-lookup"><span data-stu-id="995d9-129">**SetPower**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pset_power)

[<span data-ttu-id="995d9-130">**Startcomplete**</span><span class="sxs-lookup"><span data-stu-id="995d9-130">**StartComplete**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pstart_complete)

[<span data-ttu-id="995d9-131">**Startprotokoll**</span><span class="sxs-lookup"><span data-stu-id="995d9-131">**StartProtocol**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol)

[<span data-ttu-id="995d9-132">**Stop Protocol**</span><span class="sxs-lookup"><span data-stu-id="995d9-132">**StopProtocol**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pstop_protocol)

<span data-ttu-id="995d9-133">[**Unbindinterface**](/previous-versions/windows/desktop/legacy/aa382296(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="995d9-133">[**UnbindInterface**](/previous-versions/windows/desktop/legacy/aa382296(v=vs.85))</span></span>

<span data-ttu-id="995d9-134">Wenn das Routing Protokoll die Dienst Verarbeitung unterstützt, implementieren Sie zusätzlich zu den oben aufgeführten die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="995d9-134">If the routing protocol supports service handling, implement the following function in addition to those listed preceding:</span></span>

<span data-ttu-id="995d9-135">[**"Doupdateservices"**](/previous-versions/windows/desktop/legacy/aa374005(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="995d9-135">[**DoUpdateServices**](/previous-versions/windows/desktop/legacy/aa374005(v=vs.85))</span></span>

 

 