---
title: Die SNMP-Verwaltungs Informationsbasis (MIB)
description: Eine Management Information Base (MIB) beschreibt einen Satz verwalteter Objekte. Eine SNMP-Verwaltungs Konsolenanwendung kann die Objekte auf einem bestimmten Computer bearbeiten, wenn der SNMP-Dienst über eine Erweiterungs-Agent-dll verfügt, die das MIB unterstützt.
ms.assetid: 684200b6-a5e4-42bb-8a01-fcb6100967c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ba4612c026aa5a3a1a1574556f58207bad08e06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708826"
---
# <a name="the-snmp-management-information-base-mib"></a><span data-ttu-id="b73a2-104">Die SNMP-Verwaltungs Informationsbasis (MIB)</span><span class="sxs-lookup"><span data-stu-id="b73a2-104">The SNMP Management Information Base (MIB)</span></span>

<span data-ttu-id="b73a2-105">Eine Management Information Base (MIB) beschreibt einen Satz verwalteter Objekte.</span><span class="sxs-lookup"><span data-stu-id="b73a2-105">A Management Information Base (MIB) describes a set of managed objects.</span></span> <span data-ttu-id="b73a2-106">Eine SNMP-Verwaltungs Konsolenanwendung kann die Objekte auf einem bestimmten Computer bearbeiten, wenn der SNMP-Dienst über eine Erweiterungs-Agent-dll verfügt, die das MIB unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b73a2-106">An SNMP management console application can manipulate the objects on a specific computer if the SNMP service has an extension agent DLL that supports the MIB.</span></span>

<span data-ttu-id="b73a2-107">Jedes verwaltete Objekt in einem MIB hat einen eindeutigen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="b73a2-107">Each managed object in a MIB has a unique identifier.</span></span> <span data-ttu-id="b73a2-108">Der Bezeichner enthält den Objekttyp (z. b. Counter, String, Messgerät oder Address), die Zugriffsebene des Objekts (z. b. Lese-oder Lese-/Schreibzugriff), Größenbeschränkungen und Bereichs Informationen.</span><span class="sxs-lookup"><span data-stu-id="b73a2-108">The identifier includes the object's type (such as counter, string, gauge, or address), the object's access level (such as read or read/write), size restrictions, and range information.</span></span>

<span data-ttu-id="b73a2-109">Die folgende Tabelle enthält eine partielle Liste der im System enthaltenen MISB.</span><span class="sxs-lookup"><span data-stu-id="b73a2-109">The following table contains a partial list of the MIBs that ship with the system.</span></span> <span data-ttu-id="b73a2-110">Sie werden mit dem SNMP-Dienst im Verzeichnis% systemroot% \\ System32 installiert.</span><span class="sxs-lookup"><span data-stu-id="b73a2-110">They are installed with the SNMP service in the %systemroot%\\system32 directory.</span></span> <span data-ttu-id="b73a2-111">Eine umfassende Auflistung von MISB finden Sie im Windows Resource Kit.</span><span class="sxs-lookup"><span data-stu-id="b73a2-111">For a complete listing of MIBs, refer to the Windows Resource Kit.</span></span>



| <span data-ttu-id="b73a2-112">MIB</span><span class="sxs-lookup"><span data-stu-id="b73a2-112">MIB</span></span>         | <span data-ttu-id="b73a2-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b73a2-113">Description</span></span>                                                                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b73a2-114">Konfiguriert. MIB</span><span class="sxs-lookup"><span data-stu-id="b73a2-114">DHCP.MIB</span></span>    | <span data-ttu-id="b73a2-115">Von Microsoft definiertes MIB, das Objekttypen zum Überwachen des Netzwerk Datenverkehrs zwischen Remote Hosts und DHCP-Servern enthält</span><span class="sxs-lookup"><span data-stu-id="b73a2-115">Microsoft-defined MIB that contains object types for monitoring the network traffic between remote hosts and DHCP servers</span></span>                        |
| <span data-ttu-id="b73a2-116">Hostmib. MIB</span><span class="sxs-lookup"><span data-stu-id="b73a2-116">HOSTMIB.MIB</span></span> | <span data-ttu-id="b73a2-117">Enthält Objekttypen zum Überwachen und Verwalten von Host Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b73a2-117">Contains object types for monitoring and managing host resources</span></span>                                                                                 |
| <span data-ttu-id="b73a2-118">LMMIB2. MIB</span><span class="sxs-lookup"><span data-stu-id="b73a2-118">LMMIB2.MIB</span></span>  | <span data-ttu-id="b73a2-119">Umfasst Arbeitsstations-und Server Dienste</span><span class="sxs-lookup"><span data-stu-id="b73a2-119">Covers workstation and server services</span></span>                                                                                                           |
| <span data-ttu-id="b73a2-120">MIB \_ II. MIB</span><span class="sxs-lookup"><span data-stu-id="b73a2-120">MIB\_II.MIB</span></span> | <span data-ttu-id="b73a2-121">Enthält die Management Information Base (MIB-II), die eine einfache, funktionierende Architektur und ein einfaches System zum Verwalten von TCP/IP-basierten Internetinformationsdienste bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="b73a2-121">Contains the Management Information Base (MIB-II), which provides a simple, workable architecture and system for managing TCP/IP-based internets</span></span> |
| <span data-ttu-id="b73a2-122">Sie. MIB</span><span class="sxs-lookup"><span data-stu-id="b73a2-122">WINS.MIB</span></span>    | <span data-ttu-id="b73a2-123">Von Microsoft definiertes MIB für den Windows Internet Name Service (WINS)</span><span class="sxs-lookup"><span data-stu-id="b73a2-123">Microsoft-defined MIB for the Windows Internet Name Service (WINS)</span></span>                                                                               |



 

<span data-ttu-id="b73a2-124">**Windows NT:** In der Regel können Sie ein MIB aus dem SNMP-Erweiterungs-Agent kopieren, der das jeweilige MIB unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b73a2-124">**Windows NT:** Typically, you can copy a MIB from the SNMP extension agent that supports the particular MIB.</span></span> <span data-ttu-id="b73a2-125">Einige zusätzliche MISB sind mit dem Windows NT 4,0 Resource Kit verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b73a2-125">Some additional MIBs are available with the Windows NT 4.0 Resource Kit.</span></span>

<span data-ttu-id="b73a2-126">Die Erweiterungs-Agent-DLLs für MIB-II, LAN-Manager MIB-II und die Hostressourcen-MIB werden mit dem SNMP-Dienst installiert.</span><span class="sxs-lookup"><span data-stu-id="b73a2-126">The extension agent DLLs for MIB-II, LAN Manager MIB-II, and the Host Resources MIB are installed with the SNMP service.</span></span> <span data-ttu-id="b73a2-127">Die Erweiterungs-Agent-DLLs für die anderen MISB werden installiert, wenn die entsprechenden Dienste installiert sind.</span><span class="sxs-lookup"><span data-stu-id="b73a2-127">The extension agent DLLs for the other MIBs are installed when their respective services are installed.</span></span> <span data-ttu-id="b73a2-128">Beim Startzeitpunkt des dienstanseins lädt der SNMP-Dienst alle Erweiterungs-Agent-DLLs, die in der Registrierung aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b73a2-128">At service startup time, the SNMP service loads all of the extension agent DLLs that are listed in the registry.</span></span>

<span data-ttu-id="b73a2-129">Benutzer können weitere DLLs für Erweiterungs-Agents hinzufügen, die zusätzliche MIB implementieren.</span><span class="sxs-lookup"><span data-stu-id="b73a2-129">Users can add other extension agent DLLs that implement additional MIBs.</span></span> <span data-ttu-id="b73a2-130">Zu diesem Zweck müssen Sie einen Registrierungs Eintrag für die neue dll unter dem SNMP-Dienst hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b73a2-130">To do this, they must add a registry entry for the new DLL under the SNMP service.</span></span> <span data-ttu-id="b73a2-131">Außerdem müssen Sie das neue MIB bei der SNMP-Verwaltungs Konsolenanwendung registrieren.</span><span class="sxs-lookup"><span data-stu-id="b73a2-131">They must also register the new MIB with the SNMP management console application.</span></span> <span data-ttu-id="b73a2-132">Weitere Informationen finden Sie in der Dokumentation, die in ihrer Verwaltungs Konsolenanwendung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="b73a2-132">For more information, see the documentation included with your management console application.</span></span>

<span data-ttu-id="b73a2-133">Weitere Informationen finden Sie unter [MIB Name Tree](mib-name-tree.md).</span><span class="sxs-lookup"><span data-stu-id="b73a2-133">For more information, see [MIB Name Tree](mib-name-tree.md).</span></span>

 

 




