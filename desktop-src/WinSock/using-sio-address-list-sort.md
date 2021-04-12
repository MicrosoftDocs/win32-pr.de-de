---
description: Mit der Liste "die Liste der \_ \_ \_ verfügbaren ioctl-Adressen" können Anwendungsentwickler eine Liste von IPv6-und IPv4-Zieladressen sortieren, um die beste verfügbare Adresse für eine Verbindung zu ermitteln. Die Liste der in der Liste für die Liste der IP \_ \_ -Adressen \_ Sortierungen wird unter Windows XP und höher unterstützt
ms.assetid: bf380ddf-8171-4ef4-be47-94c7a6aabf0a
title: Verwenden von SIO_ADDRESS_LIST_SORT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6452023b69ccf72c78b393c5059fee497997af51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217979"
---
# <a name="using-sio_address_list_sort"></a><span data-ttu-id="12f29-104">Verwenden der "sio- \_ Adress \_ Liste" \_</span><span class="sxs-lookup"><span data-stu-id="12f29-104">Using SIO\_ADDRESS\_LIST\_SORT</span></span>

<span data-ttu-id="12f29-105">Mit **der \_ \_ Liste \_** "die Liste der verfügbaren ioctl-Adressen" können Anwendungsentwickler eine Liste von IPv6-und IPv4-Zieladressen sortieren, um die beste verfügbare Adresse für eine Verbindung zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="12f29-105">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL allows application developers to sort a list of IPv6 and IPv4 destination addresses to determine the best available address for making a connection.</span></span> <span data-ttu-id="12f29-106">Die Liste der in der Liste für die Liste der IP- **\_ Adressen \_ \_ Sortierungen** wird unter Windows XP und höher unterstützt</span><span class="sxs-lookup"><span data-stu-id="12f29-106">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL is supported on Windows XP and later.</span></span>

<span data-ttu-id="12f29-107">Unter Windows Vista und höher übernimmt die Funktion "Funktion" von "| [**atesortedadresssspairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) " eine angegebene Liste potenzieller IP-Zieladressen, fasst die Zieladressen mit den lokalen IP-Adressen des Host Computers zusammen und sortiert die Paare entsprechend dem Adress Paar, das sich am besten für die Kommunikation zwischen den beiden Peers eignet.</span><span class="sxs-lookup"><span data-stu-id="12f29-107">On Windows Vista and later, the [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) function takes a supplied list of potential IP destination addresses, pairs the destination addresses with the host machine's local IP addresses, and sorts the pairs according to which address pair is best suited for communication between the two peers.</span></span> <span data-ttu-id="12f29-108">Die Funktion "| **atesortedadresssspairs** " sollte anstelle der " **SIO \_ Address \_ List \_** ioctl" unter Windows Vista und höher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12f29-108">The **CreateSortedAddressPairs** function should be used instead of the **SIO\_ADDRESS\_LIST\_SORT** IOCTL on Windows Vista and later.</span></span>

<span data-ttu-id="12f29-109">In den folgenden Abschnitten werden die Verwendungs Überlegungen für die Verwendung der Liste "die **\_ \_ Liste \_** der</span><span class="sxs-lookup"><span data-stu-id="12f29-109">The following sections describe usage considerations for **SIO\_ADDRESS\_LIST\_SORT**.</span></span>

## <a name="parameters"></a><span data-ttu-id="12f29-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="12f29-110">Parameters</span></span>

<span data-ttu-id="12f29-111">Der an die Größe der " **SIO \_ Address \_ List \_** "-Sortierung an [**\_ \_**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="12f29-111">The buffer passed to **SIO\_ADDRESS\_LIST\_SORT** is a [**SOCKET\_ADDRESS\_LIST**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) structure.</span></span> <span data-ttu-id="12f29-112">Jede [**\_ Socketadresse**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) in der Liste muss das sockaddr \_ IN6-Format aufweisen.</span><span class="sxs-lookup"><span data-stu-id="12f29-112">Each [**SOCKET\_ADDRESS**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) in the list must be in SOCKADDR\_IN6 format.</span></span>

<span data-ttu-id="12f29-113">In der Liste der "sio-Adressen" **\_ \_ \_ Sortieren** "ioctl" sortiert IPv6-und IPv4-Adressen unter Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="12f29-113">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL sorts both IPv6 and IPv4 addresses on Windows Vista and later.</span></span> <span data-ttu-id="12f29-114">Alle IPv4-Adressen in der Liste, die sortiert werden sollen, müssen im IPv4-zugeordneten IPv6-Adressformat vorliegen.</span><span class="sxs-lookup"><span data-stu-id="12f29-114">Any IPv4 addresses in the list to be sorted must be in the IPv4-mapped IPv6 address format.</span></span> <span data-ttu-id="12f29-115">Weitere Informationen zum IPv4-zugeordneten IPv6-Adressformat finden Sie unter [Dual Stack Sockets (Dual-Stack-Sockets](dual-stack-sockets.md)).</span><span class="sxs-lookup"><span data-stu-id="12f29-115">For more information on the IPv4-mapped IPv6 address format, see [Dual-Stack Sockets](dual-stack-sockets.md).</span></span>

<span data-ttu-id="12f29-116">Unter Windows Server 2003 und Windows XP sortiert die **Liste der "sio- \_ Adress \_ Liste \_** " nur IPv6-Adressen.</span><span class="sxs-lookup"><span data-stu-id="12f29-116">On Windows Server 2003, and Windows XP, **SIO\_ADDRESS\_LIST\_SORT** sorts only IPv6 addresses.</span></span> <span data-ttu-id="12f29-117">IPv4-Adressen im IPv4-zugeordneten IPv6-Adressformat werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12f29-117">IPv4 addresses in the IPv4-mapped IPv6 address format are not supported.</span></span>

<span data-ttu-id="12f29-118">Bei der Ausgabe kann der **iaddresscount** -Member [**der \_ socketadressauflistungs \_**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) -Struktur kleiner als bei der Eingabe sein, wenn der IOCTL-Code ermittelt, dass einige Zieladressen ungültig sind.</span><span class="sxs-lookup"><span data-stu-id="12f29-118">On output, the **iAddressCount** member of the [**SOCKET\_ADDRESS\_LIST**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) structure may be smaller than on input if the IOCTL code determines that some destination addresses are invalid.</span></span>

## <a name="sorting-determination"></a><span data-ttu-id="12f29-119">Sortier Bestimmung</span><span class="sxs-lookup"><span data-stu-id="12f29-119">Sorting Determination</span></span>

<span data-ttu-id="12f29-120">Die Sortierreihenfolge für IPv6-Adressen für die Liste der "sio- \_ Adresse" \_ sortiert " \_ ioctl" basiert auf der Präfix Richtlinien Tabelle.</span><span class="sxs-lookup"><span data-stu-id="12f29-120">The sorting order for IPv6 addresses for the SIO\_ADDRESS\_LIST\_SORT IOCTL is based on the prefix policy table.</span></span> <span data-ttu-id="12f29-121">Die Präfix Richtlinien Tabelle wird mithilfe des Befehlszeilen-Hilfsprogramms *Netsh.exe* konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="12f29-121">The prefix policy table is configured using the *Netsh.exe* command line utility.</span></span> <span data-ttu-id="12f29-122">Die folgenden Befehlszeilen Ausschnitte veranschaulichen grundlegende Konfigurations Befehle für *Netsh.exe* -Präfix der Richtlinien Tabelle:</span><span class="sxs-lookup"><span data-stu-id="12f29-122">The following command line snippets illustrate basic *Netsh.exe* prefix policy table configuration commands:</span></span>

``` syntax
netsh interface ipv6 show prefixpolicies
netsh interface ipv6 add prefixpolicy ::/96 3 4
netsh interface ipv6 delete prefixpolicy ::/96
netsh interface ipv6 set prefixpolicy ::/96 3 4
```

> [!Note]  
> <span data-ttu-id="12f29-123">Unter Windows Server 2003 und Windows XP lautete der erste oben aufgeführte Netsh-Befehl wie folgt.</span><span class="sxs-lookup"><span data-stu-id="12f29-123">On Windows Server 2003 and Windows XP, the first netsh command listed above was as follows.</span></span> <span data-ttu-id="12f29-124">Alle anderen zugehörigen Befehle sind identisch.</span><span class="sxs-lookup"><span data-stu-id="12f29-124">All other related commands are the same.</span></span>

 

``` syntax
netsh interface ipv6 show prefixpolicy
```

<span data-ttu-id="12f29-125">Die Adress Reihenfolge wird auch durch einen Algorithmus bestimmt, der in RFC 3484 bei der *Standard Adressauswahl für IPv6 (Internet Protocol, Version 6)* , die vom IETF veröffentlicht wurde, beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="12f29-125">Address ordering is also determined by an algorithm outlined in the RFC 3484 on *Default Address Selection for Internet Protocol version 6 (IPv6)* published by the IETF.</span></span> <span data-ttu-id="12f29-126">Weitere Informationen finden Sie unter [https://www.ietf.org/rfc/rfc3484.txt](https://tools.ietf.org/html/rfc3484).</span><span class="sxs-lookup"><span data-stu-id="12f29-126">For more information, see [https://www.ietf.org/rfc/rfc3484.txt](https://tools.ietf.org/html/rfc3484).</span></span> <span data-ttu-id="12f29-127">(Diese Ressource ist möglicherweise nur in englischer Sprache verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="12f29-127">(This resource may only be available in English.)</span></span>

<span data-ttu-id="12f29-128">**In der \_ \_** Liste der "sio-Adressen" können Sie ioctl sortieren, um Adressen vom besten zum schlechtesten zu **\_ \_ \_ Sortieren**</span><span class="sxs-lookup"><span data-stu-id="12f29-128">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL sorts addresses from best to worst, and fills in **sin6\_scope\_id** members, if needed.</span></span> <span data-ttu-id="12f29-129">Bei Site-Local-Adressen wird \_ durch \_ \_ die Liste der in der Liste der Adresslisten Sortierungen entweder die Bereichs-ID ausgefüllt oder die Adresse entfernt.</span><span class="sxs-lookup"><span data-stu-id="12f29-129">For site-local addresses, SIO\_ADDRESS\_LIST\_SORT either fills in the scope-id, or removes the address.</span></span>

<span data-ttu-id="12f29-130">In der Liste der für die zu **\_ \_ \_ Sortier** enden IP-Adressen wird die Quelladresse ignoriert, die an den Socket gebunden ist, und nur nach der als Parameter übergebenen Ziel Adressliste sortiert.</span><span class="sxs-lookup"><span data-stu-id="12f29-130">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL ignores the source address bound to the socket and only sorts by the destination address list passed as a parameter.</span></span>

<span data-ttu-id="12f29-131">Die Funktion "| [**atesortedadresssspairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) " sollte anstelle der " **SIO \_ Address \_ List \_** ioctl" unter Windows Vista und höher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12f29-131">The [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) function should be used instead of the **SIO\_ADDRESS\_LIST\_SORT** IOCTL on Windows Vista and later.</span></span> <span data-ttu-id="12f29-132">Die Funktion " **anatesortedadresssspairs** " gibt eine Liste von Adress Paaren zurück, die eine lokale Quelladresse und eine Zieladresse enthalten.</span><span class="sxs-lookup"><span data-stu-id="12f29-132">The **CreateSortedAddressPairs** function returns a list of address pairs that contains a local source address and a destination address.</span></span> <span data-ttu-id="12f29-133">Dadurch wird eine Anwendung zur richtigen Quelladresse für die einzelnen Zieladressen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="12f29-133">This provides an application the correct source address to use for each destination address.</span></span> <span data-ttu-id="12f29-134">Eine Anwendung kann die Ergebnisse auch filtern, indem Sie nach einer bestimmten Quelladresse sucht.</span><span class="sxs-lookup"><span data-stu-id="12f29-134">An application can also filter the results by looking for a specific source address.</span></span> <span data-ttu-id="12f29-135">in den Ergebnissen.</span><span class="sxs-lookup"><span data-stu-id="12f29-135">in the results.</span></span>

## <a name="requirements"></a><span data-ttu-id="12f29-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12f29-136">Requirements</span></span>

<span data-ttu-id="12f29-137">Die Liste der in der Liste für die TLS- **\_ Adressen \_ \_ Sortierung** ist in der Header Datei " *Winsock2. h* " definiert.</span><span class="sxs-lookup"><span data-stu-id="12f29-137">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL is defined in the *Winsock2.h* header file.</span></span> <span data-ttu-id="12f29-138">Auf dem Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, hat sich die Organisation der Header Dateien geändert, und die Datei "IOCTL **\_ \_ \_ Sort** " in der " *Ws2def. h* "-Header Datei ist in der Header Datei "</span><span class="sxs-lookup"><span data-stu-id="12f29-138">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and **SIO\_ADDRESS\_LIST\_SORT** IOCTL is defined in the *Ws2def.h* header file.</span></span> <span data-ttu-id="12f29-139">Beachten Sie, dass die Header Datei " *Ws2def. h* " automatisch in " *Winsock2. h*" enthalten ist und niemals direkt verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="12f29-139">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

<span data-ttu-id="12f29-140">Die Liste der in der Liste für die Liste der IP- **\_ Adressen \_ \_ Sortierungen** wird unter Windows XP und höher unterstützt</span><span class="sxs-lookup"><span data-stu-id="12f29-140">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL is supported on Windows XP and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12f29-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="12f29-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12f29-142">**"Kreatesortedadresssspairs"**</span><span class="sxs-lookup"><span data-stu-id="12f29-142">**CreateSortedAddressPairs**</span></span>](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs)
</dt> </dl>

 

 
