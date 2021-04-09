---
description: IP-Hilfsprogramm bietet Funktionen zum Verwalten des Netzwerk Routings. Verwenden Sie die folgenden Funktionen zum Verwalten der IP-Routing Tabelle und zum Abrufen weiterer Routing Informationen.
ms.assetid: 879b90e3-aecc-492e-9b22-9ebbf505a610
title: Verwalten des Routings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ec199de19b4c8d724fbe6a2e77c3fac7dc19b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862436"
---
# <a name="managing-routing"></a><span data-ttu-id="fa285-104">Verwalten des Routings</span><span class="sxs-lookup"><span data-stu-id="fa285-104">Managing Routing</span></span>

<span data-ttu-id="fa285-105">IP-Hilfsprogramm bietet Funktionen zum Verwalten des Netzwerk Routings.</span><span class="sxs-lookup"><span data-stu-id="fa285-105">IP Helper provides features to manage network routing.</span></span> <span data-ttu-id="fa285-106">Verwenden Sie die folgenden Funktionen zum Verwalten der IP-Routing Tabelle und zum Abrufen weiterer Routing Informationen.</span><span class="sxs-lookup"><span data-stu-id="fa285-106">Use the following functions to manage the IP routing table, and to obtain other routing information.</span></span>

<span data-ttu-id="fa285-107">Rufen Sie den Inhalt der IP-Routing Tabelle ab, indem Sie die [**getipforwardtable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipforwardtable) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fa285-107">Retrieve the contents of the IP routing table by making a call to the [**GetIpForwardTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipforwardtable) function.</span></span> <span data-ttu-id="fa285-108">Bearbeiten Sie bestimmte Einträge in der IP-Routing Tabelle mithilfe der Funktionen " [**kreateipforwardentry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipforwardentry)", " [**deleteipforwardentry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)" und " [**stipforwardentry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipforwardentry) ".</span><span class="sxs-lookup"><span data-stu-id="fa285-108">Manipulate specific entries in the IP routing table using the [**CreateIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipforwardentry), [**DeleteIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry), and [**SetIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipforwardentry) functions.</span></span> <span data-ttu-id="fa285-109">Verwenden Sie die Funktion " **kreateipforwardentry** ", um einen neuen Routing Tabelleneintrag hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="fa285-109">Use the **CreateIpForwardEntry** function to add a new routing table entry.</span></span> <span data-ttu-id="fa285-110">Verwenden Sie die **deleteipforwardentry** -Funktion, um einen vorhandenen Eintrag zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="fa285-110">Use the **DeleteIpForwardEntry** function to remove an existing entry.</span></span> <span data-ttu-id="fa285-111">Die Funktion " **settipforwardentry** " ändert einen vorhandenen Eintrag.</span><span class="sxs-lookup"><span data-stu-id="fa285-111">The **SetIpForwardEntry** function modifies an existing entry.</span></span>

<span data-ttu-id="fa285-112">Mithilfe der routerverwaltungsfunktionen von IP Helper können Informationen darüber abgerufen werden, wie Datagramme über das Netzwerk weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="fa285-112">The router management capabilities of IP Helper can be used to retrieve information about how datagrams are routed over the network.</span></span> <span data-ttu-id="fa285-113">Die [**getbestroute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute) -Funktion Ruft die beste Route an eine angegebene Zieladresse ab.</span><span class="sxs-lookup"><span data-stu-id="fa285-113">The [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute) function retrieves the best route to a specified destination address.</span></span> <span data-ttu-id="fa285-114">Die [**getbestinterface**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestinterface) -Funktion Ruft den Index der-Schnittstelle ab, die von der optimalen Route zu einer angegebenen Zieladresse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fa285-114">The [**GetBestInterface**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestinterface) function retrieves the index of the interface used by the best route to a specified destination address.</span></span> <span data-ttu-id="fa285-115">Schließlich ruft die [**getrttandhopcount**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getrttandhopcount) -Funktion die Roundtripzeit (RTT) und die Anzahl der Hops an eine angegebene Zieladresse ab.</span><span class="sxs-lookup"><span data-stu-id="fa285-115">Lastly, the [**GetRTTAndHopCount**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getrttandhopcount) function retrieves the round-trip time (RTT) and number of hops to a specified destination address.</span></span>

 

 



