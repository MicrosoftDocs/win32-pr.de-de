---
description: Sie können das IP-Hilfsprogramm verwenden, um ARP-Vorgänge (Address Resolution Protocol) für den lokalen Computer auszuführen. Verwenden Sie die folgenden Funktionen, um die ARP-Tabelle abzurufen und zu ändern.
ms.assetid: 2c5dc1f8-590f-4b41-b6bb-f82ab093252f
title: Verwenden des adressauflösungsprotokolls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec57c3b028f8f90135567bb07dbc00bda89036
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350917"
---
# <a name="using-the-address-resolution-protocol"></a><span data-ttu-id="0be70-104">Verwenden des adressauflösungsprotokolls</span><span class="sxs-lookup"><span data-stu-id="0be70-104">Using the Address Resolution Protocol</span></span>

<span data-ttu-id="0be70-105">Sie können das IP-Hilfsprogramm verwenden, um ARP-Vorgänge (Address Resolution Protocol) für den lokalen Computer auszuführen.</span><span class="sxs-lookup"><span data-stu-id="0be70-105">You can use IP Helper to perform Address Resolution Protocol (ARP) operations for the local computer.</span></span> <span data-ttu-id="0be70-106">Verwenden Sie die folgenden Funktionen, um die ARP-Tabelle abzurufen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="0be70-106">Use the following functions to retrieve and modify the ARP table.</span></span>

<span data-ttu-id="0be70-107">Die [**getipnetttabelle**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable) Ruft die ARP-Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="0be70-107">The [**GetIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable) retrieves the ARP table.</span></span> <span data-ttu-id="0be70-108">Die ARP-Tabelle enthält die Zuordnung von IP-Adressen zu physischen Adressen.</span><span class="sxs-lookup"><span data-stu-id="0be70-108">The ARP table contains the mapping of IP addresses to physical addresses.</span></span> <span data-ttu-id="0be70-109">Physische Adressen werden manchmal auch als Mac-Adressen (Media Access Controller) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0be70-109">Physical addresses are sometimes referred to as Media Access Controller (MAC) addresses.</span></span>

<span data-ttu-id="0be70-110">Verwenden Sie die Funktionen " [**forateipnetentry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) " und " [**deleteipnetentry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) ", um der Tabelle bestimmte ARP-Einträge hinzuzufügen oder daraus zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="0be70-110">Use the [**CreateIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) and [**DeleteIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) functions to add or remove particular ARP entries to or from the table.</span></span> <span data-ttu-id="0be70-111">Die [**flushipnettfunktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable) löscht alle Einträge aus der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0be70-111">The [**FlushIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable) function deletes all entries from the table.</span></span>

<span data-ttu-id="0be70-112">Um Proxy-ARP-Einträge zu erstellen oder zu löschen, verwenden Sie die Funktionen " [**forateproxyarpentry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) " und " [**deleteproxyarpentry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry) ".</span><span class="sxs-lookup"><span data-stu-id="0be70-112">To create or delete proxy ARP entries, use the [**CreateProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) and [**DeleteProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry) functions.</span></span>

<span data-ttu-id="0be70-113">Die [**sendarp**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp) -Funktion sendet eine ARP-Anforderung an das lokale Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="0be70-113">The [**SendARP**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp) function sends an ARP request to the local network.</span></span>

 

 



