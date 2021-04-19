---
description: IP-Hilfsobjekte können bei der Verwaltung von IP-Adressen helfen, die Schnittstellen auf dem lokalen Computer zugeordnet sind Verwenden Sie die Funktionen, die in den folgenden Abschnitten für die IP-Adressverwaltung beschrieben werden.
ms.assetid: 94da3e53-1898-4721-b5f0-0b7244574c55
title: Verwalten von IP-Adressen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0917050799ea452cf1c6ee3e068cc29793df8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356736"
---
# <a name="managing-ip-addresses"></a><span data-ttu-id="fb3e4-104">Verwalten von IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="fb3e4-104">Managing IP Addresses</span></span>

<span data-ttu-id="fb3e4-105">IP-Hilfsobjekte können bei der Verwaltung von IP-Adressen helfen, die Schnittstellen auf dem lokalen Computer zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="fb3e4-105">IP Helper can assist in the management of IP addresses associated with interfaces on the local computer.</span></span> <span data-ttu-id="fb3e4-106">Verwenden Sie die Funktionen, die in den folgenden Abschnitten für die IP-Adressverwaltung beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="fb3e4-106">Use the functions described in the following paragraphs for IP address management.</span></span>

<span data-ttu-id="fb3e4-107">Die [**getipaddrtable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) -Funktion Ruft eine Tabelle ab, die die Zuordnung von IP-Adressen zu Schnittstellen enthält.</span><span class="sxs-lookup"><span data-stu-id="fb3e4-107">The [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function retrieves a table that contains the mapping of IP addresses to interfaces.</span></span> <span data-ttu-id="fb3e4-108">Der gleichen Schnittstelle können mehr als eine IP-Adresse zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="fb3e4-108">More than one IP address may be associated with the same interface.</span></span>

<span data-ttu-id="fb3e4-109">Verwenden Sie die [**addipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) -Funktion, um einer bestimmten Schnittstelle eine IP-Adresse hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="fb3e4-109">Use the [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function to add an IP address to a particular interface.</span></span> <span data-ttu-id="fb3e4-110">Verwenden Sie zum Entfernen von IP-Adressen, die zuvor mit **addipaddress** hinzugefügt wurden, die [**deleteipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="fb3e4-110">To remove IP addresses that were previously added using **AddIPAddress**, use the [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function.</span></span>

<span data-ttu-id="fb3e4-111">Die [**ipreleaseaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) -Funktion und die [**iprenewaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) -Funktion erfordern, dass der lokale Computer DHCP (Dynamic Host Configuration Protocol) verwendet.</span><span class="sxs-lookup"><span data-stu-id="fb3e4-111">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) functions require the local computer to be using Dynamic Host Configuration Protocol (DHCP).</span></span> <span data-ttu-id="fb3e4-112">Die **ipreleaseaddress** -Funktion gibt eine IP-Adresse frei, die zuvor von DHCP abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="fb3e4-112">The **IpReleaseAddress** function releases an IP address that was previously obtained from DHCP.</span></span> <span data-ttu-id="fb3e4-113">Die **iprenewaddress** -Funktion erneuert eine DHCP-Lease für eine bestimmte IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="fb3e4-113">The **IpRenewAddress** function renews a DHCP lease on a particular IP address.</span></span> <span data-ttu-id="fb3e4-114">Eine DHCP-Lease ermöglicht es einem Computer, eine IP-Adresse für einen bestimmten Zeitraum zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="fb3e4-114">A DHCP lease allows a computer to use an IP address for a specified period of time.</span></span>

-   <span data-ttu-id="fb3e4-115">Codebeispiele, die [**getipaddrtable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) betreffen, finden [Sie unter Verwalten von IP-Adressen mit getipaddrtable](managing-ip-addresses-using-getipaddrtable.md).</span><span class="sxs-lookup"><span data-stu-id="fb3e4-115">For code samples involving [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) see [Managing IP Addresses Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).</span></span>

-   <span data-ttu-id="fb3e4-116">Codebeispiele, die [**addipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) und [**deleteipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress)betreffen, finden [Sie unter Verwalten von IP-Adressen mit addipaddress und deleteipaddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md).</span><span class="sxs-lookup"><span data-stu-id="fb3e4-116">For code samples involving [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) and [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), see [Managing IP Addresses Using AddIPAddress and DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md).</span></span>

-   <span data-ttu-id="fb3e4-117">Codebeispiele, die [**ipreleaseaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) und [**iprenewaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) betreffen, finden [Sie unter Verwalten von DHCP-Leases mithilfe von ipreleaseaddress und iprenewaddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md).</span><span class="sxs-lookup"><span data-stu-id="fb3e4-117">For code samples involving [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) see [Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md).</span></span>

 

 



