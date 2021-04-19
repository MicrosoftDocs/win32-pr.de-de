---
description: Beachten Sie, dass alle Windows Sockets 1,1-Funktionen für die Namensauflösung für IPv4-TCP/IP-Netzwerke spezifisch sind.
ms.assetid: 5a2a37f3-85c5-4b27-9ce3-f5b707b1564a
title: Kompatible Namensauflösung für TCP/IP in der Windows Sockets 1,1-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2447590b25861abc80bd0a89be173272fb809814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350437"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-api"></a><span data-ttu-id="87969-103">Kompatible Namensauflösung für TCP/IP in der Windows Sockets 1,1-API</span><span class="sxs-lookup"><span data-stu-id="87969-103">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>

> [!Note]  
> <span data-ttu-id="87969-104">Alle Windows Sockets 1,1-Funktionen für die Namensauflösung sind spezifisch für IPv4-TCP/IP-Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="87969-104">All of the Windows Sockets 1.1 functions for name resolution are specific to IPv4 TCP/IP networks.</span></span> <span data-ttu-id="87969-105">Anwendungsentwickler werden dringend davon abgeraten, diese Transport spezifischen Funktionen, die nur IPv4 unterstützen, weiterhin zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="87969-105">Application developers are strongly discouraged from continuing to utilize these transport-specific functions that only support IPv4.</span></span>

 

<span data-ttu-id="87969-106">Anwendungsentwickler sollten die folgenden Funktionen verwenden, die Protokoll unabhängig sind und sowohl die IPv6-als auch die IPv4-Namensauflösung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="87969-106">Application developers should be using the following functions that are protocol-independent and support both IPv6 and IPv4 name resolution.</span></span>

-   [<span data-ttu-id="87969-107">**getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="87969-107">**getaddrinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
-   [<span data-ttu-id="87969-108">**GetAddrInfoEx**</span><span class="sxs-lookup"><span data-stu-id="87969-108">**GetAddrInfoEx**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
-   [<span data-ttu-id="87969-109">**Getaddrinfow**</span><span class="sxs-lookup"><span data-stu-id="87969-109">**GetAddrInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
-   [<span data-ttu-id="87969-110">**getnameingefo**</span><span class="sxs-lookup"><span data-stu-id="87969-110">**getnameinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
-   [<span data-ttu-id="87969-111">**Getnameingefow**</span><span class="sxs-lookup"><span data-stu-id="87969-111">**GetNameInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)

<span data-ttu-id="87969-112">Windows Sockets 1,1 hat eine Reihe von Routinen definiert, die für die Namensauflösung mit TCP/IP-Netzwerken (IP-Version 4) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="87969-112">Windows Sockets 1.1 defined a number of routines used for name resolution with TCP/IP (IP version 4) networks.</span></span> <span data-ttu-id="87969-113">Diese werden mitunter als **getxbyy** -Funktionen bezeichnet und umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="87969-113">These are sometimes called the **getXbyY** functions and include the following:</span></span>

<dl>

[<span data-ttu-id="87969-114">**GetHostName**</span><span class="sxs-lookup"><span data-stu-id="87969-114">**gethostname**</span></span>](/windows/desktop/api/winsock/nf-winsock-gethostname)  
[<span data-ttu-id="87969-115">**gethostbyaddr**</span><span class="sxs-lookup"><span data-stu-id="87969-115">**gethostbyaddr**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)  
[<span data-ttu-id="87969-116">**gethostbyname**</span><span class="sxs-lookup"><span data-stu-id="87969-116">**gethostbyname**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)  
[<span data-ttu-id="87969-117">**getprotobyname**</span><span class="sxs-lookup"><span data-stu-id="87969-117">**getprotobyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobyname)  
[<span data-ttu-id="87969-118">**getprotobynumber**</span><span class="sxs-lookup"><span data-stu-id="87969-118">**getprotobynumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)  
[<span data-ttu-id="87969-119">**getservbyname**</span><span class="sxs-lookup"><span data-stu-id="87969-119">**getservbyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyname)  
[<span data-ttu-id="87969-120">**getservbyport**</span><span class="sxs-lookup"><span data-stu-id="87969-120">**getservbyport**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyport)  
</dl>

<span data-ttu-id="87969-121">Asynchrone Versionen dieser Funktionen wurden ebenfalls definiert.</span><span class="sxs-lookup"><span data-stu-id="87969-121">Asynchronous versions of these functions were also defined.</span></span>

<dl>

[<span data-ttu-id="87969-122">**Wsaasyncgethostbyaddr**</span><span class="sxs-lookup"><span data-stu-id="87969-122">**WSAAsyncGetHostByAddr**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)  
[<span data-ttu-id="87969-123">**Wsaasyncgethostbyname**</span><span class="sxs-lookup"><span data-stu-id="87969-123">**WSAAsyncGetHostByName**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)  
[<span data-ttu-id="87969-124">**Wsaasyncgetprotobyname**</span><span class="sxs-lookup"><span data-stu-id="87969-124">**WSAAsyncGetProtoByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)  
[<span data-ttu-id="87969-125">**Wsaasyncgetprotobynumber**</span><span class="sxs-lookup"><span data-stu-id="87969-125">**WSAAsyncGetProtoByNumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)  
[<span data-ttu-id="87969-126">**Wsaasyncgetservbyname**</span><span class="sxs-lookup"><span data-stu-id="87969-126">**WSAAsyncGetServByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)  
[<span data-ttu-id="87969-127">**Wsaasyncgetservbyport**</span><span class="sxs-lookup"><span data-stu-id="87969-127">**WSAAsyncGetServByPort**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)  
</dl>

<span data-ttu-id="87969-128">Es gibt auch zwei Funktionen, die jetzt in der Winsock2.dll implementiert sind und zum Konvertieren von gepunkteten IPv4-Adress Notation in bzw. aus Zeichen folgen-und Binär Darstellungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="87969-128">There are also two functions, now implemented in the Winsock2.dll, used to convert dotted Ipv4 address notation to and from string and binary representations, respectively.</span></span>

<dl>

[<span data-ttu-id="87969-129">**inet \_ addr**</span><span class="sxs-lookup"><span data-stu-id="87969-129">**inet\_addr**</span></span>](/windows/win32/api/winsock2/nf-winsock2-inet_addr)  
[<span data-ttu-id="87969-130">**inet \_ NUM**</span><span class="sxs-lookup"><span data-stu-id="87969-130">**inet\_ntoa**</span></span>](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)  
</dl>

<span data-ttu-id="87969-131">Um die strikte Abwärtskompatibilität mit Windows Sockets 1,1 beizubehalten, werden alle älteren reinen IPv4-Funktionen weiterhin unterstützt, solange mindestens ein Namespace Anbieter vorhanden ist, der die AF \_ inet-Adressfamilie unterstützt (diese Funktionen sind für die IP-Version 6, die durch AF inet6 gekennzeichnet ist, nicht relevant \_ ).</span><span class="sxs-lookup"><span data-stu-id="87969-131">In order to retain strict backward compatibility with Windows Sockets 1.1, all of the older IPv4-only functions continue to be supported as long as at least one namespace provider is present that supports the AF\_INET address family (these functions are not relevant to IP version 6, denoted by AF\_INET6).</span></span>

<span data-ttu-id="87969-132">Die Ws2- \_32.dll implementiert diese Kompatibilitätsfunktionen in Bezug auf die neuen, Protokoll unabhängigen namens Auflösungs Funktionen mit einer entsprechenden Sequenz von [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) / **Next** / **End** -Funktionsaufrufen.</span><span class="sxs-lookup"><span data-stu-id="87969-132">The Ws2\_32.dll implements these compatibility functions in terms of the new, protocol-independent name resolution facilities using an appropriate sequence of [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)/**Next**/**End** function calls.</span></span> <span data-ttu-id="87969-133">Die Details zur Zuordnung der **getxbyy** -Funktionen zu namens Auflösungs Funktionen finden Sie unten.</span><span class="sxs-lookup"><span data-stu-id="87969-133">The details of how the **getXbyY** functions are mapped to name resolution functions are provided below.</span></span> <span data-ttu-id="87969-134">Der WSs2 \_ -32.dll behandelt die Unterschiede zwischen den asynchronen und synchronen Versionen der **getxbyy** -Funktionen, sodass nur die Implementierung der synchronen **getxbyy** -Funktionen erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="87969-134">The WSs2\_32.dll handles the differences between the asynchronous and synchronous versions of the **getXbyY** functions, so only the implementation of the synchronous **getXbyY** functions are discussed.</span></span>

<span data-ttu-id="87969-135">In diesem Abschnitt wird die kompatible Namensauflösung für TCP/IP in der Windows Sockets 1,1-API beschrieben.</span><span class="sxs-lookup"><span data-stu-id="87969-135">This section describes compatible name resolution for TCP/IP in the Windows Sockets 1.1 API.</span></span> <span data-ttu-id="87969-136">In der folgenden Liste werden die Themen in diesem Abschnitt beschrieben:</span><span class="sxs-lookup"><span data-stu-id="87969-136">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="87969-137">Grundlegender Ansatz für getxbyy in der API</span><span class="sxs-lookup"><span data-stu-id="87969-137">Basic Approach for GetXbyY in the API</span></span>](basic-approach-for-getxbyy-in-the-api-2.md)
-   [<span data-ttu-id="87969-138">Funktionen "getprotobyname" und "getprotobynumber" in der API</span><span class="sxs-lookup"><span data-stu-id="87969-138">getprotobyname and getprotobynumber Functions in the API</span></span>](getprotobyname-and-getprotobynumber-functions-in-the-api-2.md)
-   [<span data-ttu-id="87969-139">Funktionen "getservbyname" und "getservbyport" in der API</span><span class="sxs-lookup"><span data-stu-id="87969-139">getservbyname and getservbyport Functions in the API</span></span>](getservbyname-and-getservbyport-functions-in-the-api-2.md)
-   [<span data-ttu-id="87969-140">Funktion "gethostbyname" in der API</span><span class="sxs-lookup"><span data-stu-id="87969-140">gethostbyname Function in the API</span></span>](gethostbyname-function-in-the-api-2.md)
-   [<span data-ttu-id="87969-141">Funktion "gethostbyaddr" in der API</span><span class="sxs-lookup"><span data-stu-id="87969-141">gethostbyaddr Function in the API</span></span>](gethostbyaddr-function-in-the-api-2.md)
-   [<span data-ttu-id="87969-142">Funktion "GetHostName" in der API</span><span class="sxs-lookup"><span data-stu-id="87969-142">gethostname Function in the API</span></span>](gethostname-function-in-the-api-2.md)

## <a name="related-topics"></a><span data-ttu-id="87969-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="87969-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87969-144">Protokoll unabhängige Namensauflösung</span><span class="sxs-lookup"><span data-stu-id="87969-144">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="87969-145">Registrierung und Namensauflösung</span><span class="sxs-lookup"><span data-stu-id="87969-145">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
