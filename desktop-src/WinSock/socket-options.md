---
description: Navigationsseite für Socketoptionen für Windows Sockets (Winsock).
ms.assetid: e2831f76-4499-45b6-bc60-2908ec3a246c
title: Socketoptionen
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPPROTO_IP
- IPPROTO_IPV6
- IPPROTO_RM
- IPPROTO_TCP
- IPPROTO_UDP
- NSPROTO_IPX
- SOL_APPLETALK
- SOL_IRLMP
- SOL_SOCKET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 805f779965afc808e32952b58815c7b6bc528fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348994"
---
# <a name="socket-options"></a><span data-ttu-id="d3e94-103">Socketoptionen</span><span class="sxs-lookup"><span data-stu-id="d3e94-103">Socket Options</span></span>

<span data-ttu-id="d3e94-104">In diesem Abschnitt werden die Winsock-Socketoptionen für verschiedene Editionen von Windows-Betriebssystemen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d3e94-104">This section describes Winsock Socket Options for various editions of Windows operating systems.</span></span> <span data-ttu-id="d3e94-105">Verwenden Sie die Funktionen [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) und [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) , um die Socketoptionen zu erhalten und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d3e94-105">Use the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) and [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) functions for more getting and setting socket options.</span></span> <span data-ttu-id="d3e94-106">Verwenden Sie die [**wsaenumprotokolls**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) -Funktion, um Protokolle aufzulisten und die unterstützten Eigenschaften für jedes installierte Protokoll zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="d3e94-106">To enumerate protocols and discover supported properties for each installed protocol, use the [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) function.</span></span>

<span data-ttu-id="d3e94-107">Einige Socketoptionen erfordern eine ausführlichere Erläuterung, als diese Tabellen vermitteln können. Diese Optionen enthalten Links zu weiteren Seiten.</span><span class="sxs-lookup"><span data-stu-id="d3e94-107">Some socket options require more explanation than these tables can convey; such options contain links to additional pages.</span></span>

<dl> <dt>

<span data-ttu-id="d3e94-108"><span id="IPPROTO_IP"></span><span id="ipproto_ip"></span>**ipproto \_ -IP**</span><span class="sxs-lookup"><span data-stu-id="d3e94-108"><span id="IPPROTO_IP"></span><span id="ipproto_ip"></span>**IPPROTO\_IP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d3e94-109">Socketoptionen, die auf IPv4-Ebene anwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="d3e94-109">Socket options applicable at the IPv4 level.</span></span> <span data-ttu-id="d3e94-110">Weitere Informationen finden Sie unter [**ipproto \_ IP Socket Options**](ipproto-ip-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="d3e94-110">For more information, see the [**IPPROTO\_IP Socket Options**](ipproto-ip-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e94-111"><span id="IPPROTO_IPV6"></span><span id="ipproto_ipv6"></span>**Ipproto \_ IPv6**</span><span class="sxs-lookup"><span data-stu-id="d3e94-111"><span id="IPPROTO_IPV6"></span><span id="ipproto_ipv6"></span>**IPPROTO\_IPV6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d3e94-112">Socketoptionen, die auf IPv6-Ebene anwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="d3e94-112">Socket options applicable at the IPv6 level.</span></span> <span data-ttu-id="d3e94-113">Weitere Informationen finden Sie unter [**ipproto \_ IPv6-Socketoptionen**](ipproto-ipv6-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="d3e94-113">For more information, see the [**IPPROTO\_IPV6 Socket Options**](ipproto-ipv6-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e94-114"><span id="IPPROTO_RM"></span><span id="ipproto_rm"></span>**ipproto \_ RM**</span><span class="sxs-lookup"><span data-stu-id="d3e94-114"><span id="IPPROTO_RM"></span><span id="ipproto_rm"></span>**IPPROTO\_RM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d3e94-115">Socketoptionen, die auf zuverlässiger Multicast Ebene anwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="d3e94-115">Socket options applicable at the reliable multicast level.</span></span> <span data-ttu-id="d3e94-116">Weitere Informationen finden Sie unter [**ipproto \_ RM Socket Options**](ipproto-rm-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="d3e94-116">For more information, see the [**IPPROTO\_RM Socket Options**](ipproto-rm-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e94-117"><span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span>**ipproto- \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="d3e94-117"><span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span>**IPPROTO\_TCP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d3e94-118">Socketoptionen, die auf TCP-Ebene anwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="d3e94-118">Socket options applicable at the TCP level.</span></span> <span data-ttu-id="d3e94-119">Weitere Informationen finden Sie unter [**ipproto \_ TCP Socket Options**](ipproto-tcp-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="d3e94-119">For more information, see the [**IPPROTO\_TCP Socket Options**](ipproto-tcp-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e94-120"><span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span>**ipproto- \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="d3e94-120"><span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span>**IPPROTO\_UDP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d3e94-121">Socketoptionen, die auf UDP-Ebene anwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="d3e94-121">Socket options applicable at the UDP level.</span></span> <span data-ttu-id="d3e94-122">Weitere Informationen finden Sie unter [**ipproto \_ UDP Socket Options**](ipproto-udp-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="d3e94-122">For more information, see the [**IPPROTO\_UDP Socket Options**](ipproto-udp-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e94-123"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>**nsproto- \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="d3e94-123"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>**NSPROTO\_IPX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d3e94-124">Socketoptionen, die auf IPX-Ebene anwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="d3e94-124">Socket options applicable at the IPX level.</span></span> <span data-ttu-id="d3e94-125">Weitere Informationen finden [**Sie unter nsproto \_ IPX Socket Options**](nsproto-ipx-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="d3e94-125">For more information, see the [**NSPROTO\_IPX Socket Options**](nsproto-ipx-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e94-126"><span id="SOL_APPLETALK"></span><span id="sol_appletalk"></span>**Sol \_ AppleTalk**</span><span class="sxs-lookup"><span data-stu-id="d3e94-126"><span id="SOL_APPLETALK"></span><span id="sol_appletalk"></span>**SOL\_APPLETALK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d3e94-127">Socketoptionen, die auf der AppleTalk-Ebene anwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="d3e94-127">Socket options applicable at the AppleTalk level.</span></span> <span data-ttu-id="d3e94-128">Weitere Informationen finden Sie in den [**Optionen für den Sol \_ AppleTalk-Socket**](sol-appletalk-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="d3e94-128">For more information, see the [**SOL\_APPLETALK Socket Options**](sol-appletalk-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e94-129"><span id="SOL_IRLMP"></span><span id="sol_irlmp"></span>**Sol- \_ irilmp**</span><span class="sxs-lookup"><span data-stu-id="d3e94-129"><span id="SOL_IRLMP"></span><span id="sol_irlmp"></span>**SOL\_IRLMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d3e94-130">Socketoptionen, die auf der Protokollebene der Infrarot-Verbindungs Verwaltung anwendbar sind</span><span class="sxs-lookup"><span data-stu-id="d3e94-130">Socket options applicable at the InfraRed Link Management Protocol level.</span></span> <span data-ttu-id="d3e94-131">Weitere Informationen finden Sie unter den [**Optionen für den Sol- \_ irilmp-Socket**](sol-irlmp-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="d3e94-131">For more information, see the [**SOL\_IRLMP Socket Options**](sol-irlmp-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e94-132"><span id="SOL_SOCKET"></span><span id="sol_socket"></span>**Sol- \_ Socket**</span><span class="sxs-lookup"><span data-stu-id="d3e94-132"><span id="SOL_SOCKET"></span><span id="sol_socket"></span>**SOL\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d3e94-133">Socketoptionen, die auf Socketebene anwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="d3e94-133">Socket options applicable at the socket level.</span></span> <span data-ttu-id="d3e94-134">Weitere Informationen finden Sie unter den [**Optionen für den Sol- \_ socketsocket**](sol-socket-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="d3e94-134">For more information, see the [**SOL\_SOCKET Socket Options**](sol-socket-socket-options.md).</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d3e94-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3e94-135">Remarks</span></span>

<span data-ttu-id="d3e94-136">Alle \_ \* Socketoptionen gelten gleichermaßen für IPv4 und IPv6 (mit Ausnahme von \_ Broadcast, da Broadcast nicht in IPv6 implementiert ist).</span><span class="sxs-lookup"><span data-stu-id="d3e94-136">All SO\_\* socket options apply equally to IPv4 and IPv6 (except SO\_BROADCAST, since broadcast is not implemented in IPv6).</span></span>

 

 



