---
description: 'Windows Sockets 1,1 hat eine Reihe von Routinen definiert, die für die IPv4-Namensauflösung mit TCP/IP-Netzwerken verwendet wurden. Diese werden in der Regel als getxbyy-Funktionen bezeichnet und umfassen Folgendes:'
ms.assetid: 7a3ff7f3-d4b9-4900-8fd8-708a89c78c0a
title: Kompatible Namensauflösung für TCP/IP in Windows Sockets 1,1 SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ca58f8868c17c9dad7c67fed083e9460272944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347172"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-spi"></a><span data-ttu-id="74a44-104">Kompatible Namensauflösung für TCP/IP in Windows Sockets 1,1 SPI</span><span class="sxs-lookup"><span data-stu-id="74a44-104">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 SPI</span></span>

<span data-ttu-id="74a44-105">Windows Sockets 1,1 hat eine Reihe von Routinen definiert, die für die IPv4-Namensauflösung mit TCP/IP-Netzwerken verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="74a44-105">Windows Sockets 1.1 defined a number of routines that were used for IPv4 name resolution with TCP/IP networks.</span></span> <span data-ttu-id="74a44-106">Diese werden in der Regel als **getxbyy** -Funktionen bezeichnet und umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="74a44-106">These are customarily called the **GetXbyY** functions and include the following.</span></span>

[<span data-ttu-id="74a44-107">**GetHostName**</span><span class="sxs-lookup"><span data-stu-id="74a44-107">**gethostname**</span></span>](/windows/desktop/api/winsock/nf-winsock-gethostname)

[<span data-ttu-id="74a44-108">**gethostbyaddr**</span><span class="sxs-lookup"><span data-stu-id="74a44-108">**gethostbyaddr**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)

[<span data-ttu-id="74a44-109">**gethostbyname**</span><span class="sxs-lookup"><span data-stu-id="74a44-109">**gethostbyname**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)

[<span data-ttu-id="74a44-110">**getprotobyname**</span><span class="sxs-lookup"><span data-stu-id="74a44-110">**getprotobyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobyname)

[<span data-ttu-id="74a44-111">**getprotobynumber**</span><span class="sxs-lookup"><span data-stu-id="74a44-111">**getprotobynumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)

[<span data-ttu-id="74a44-112">**getservbyname**</span><span class="sxs-lookup"><span data-stu-id="74a44-112">**getservbyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyname)

[<span data-ttu-id="74a44-113">**getservbyport**</span><span class="sxs-lookup"><span data-stu-id="74a44-113">**getservbyport**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyport)

<span data-ttu-id="74a44-114">Asynchrone Versionen dieser Funktionen wurden ebenfalls definiert.</span><span class="sxs-lookup"><span data-stu-id="74a44-114">Asynchronous versions of these functions were also defined.</span></span>

[<span data-ttu-id="74a44-115">**Wsaasyncgethostbyaddr**</span><span class="sxs-lookup"><span data-stu-id="74a44-115">**WSAAsyncGetHostByAddr**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)

[<span data-ttu-id="74a44-116">**Wsaasyncgethostbyname**</span><span class="sxs-lookup"><span data-stu-id="74a44-116">**WSAAsyncGetHostByName**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)

[<span data-ttu-id="74a44-117">**Wsaasyncgetprotobyname**</span><span class="sxs-lookup"><span data-stu-id="74a44-117">**WSAAsyncGetProtoByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)

[<span data-ttu-id="74a44-118">**Wsaasyncgetprotobynumber**</span><span class="sxs-lookup"><span data-stu-id="74a44-118">**WSAAsyncGetProtoByNumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)

[<span data-ttu-id="74a44-119">**Wsaasyncgetservbyname**</span><span class="sxs-lookup"><span data-stu-id="74a44-119">**WSAAsyncGetServByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)

[<span data-ttu-id="74a44-120">**Wsaasyncgetservbyport**</span><span class="sxs-lookup"><span data-stu-id="74a44-120">**WSAAsyncGetServByPort**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)

<span data-ttu-id="74a44-121">Diese Funktionen sind spezifisch für TCP/IP-Netzwerke. Entwickler von Protokoll unabhängigen Anwendungen werden davon abgeraten, diese Transport spezifischen Funktionen weiterhin zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="74a44-121">These functions are specific to TCP/IP networks; developers of protocol-independent applications are discouraged from continuing to utilize these transport-specific functions.</span></span> <span data-ttu-id="74a44-122">Um jedoch eine strikte Abwärtskompatibilität mit Windows Sockets 1,1 beizubehalten, werden die vorangehenden Funktionen weiterhin unterstützt, solange mindestens ein Namespace Anbieter vorhanden ist, der die AF \_ inet-Adressfamilie unterstützt.</span><span class="sxs-lookup"><span data-stu-id="74a44-122">However, to retain strict backward compatibility with Windows Sockets 1.1, the preceding functions continue to be supported as long as at least one namespace provider is present that supports the AF\_INET address family.</span></span>

<span data-ttu-id="74a44-123">Die *Ws2- \_32.dll* implementiert diese Kompatibilitätsfunktionen in Bezug auf die neuen, Protokoll unabhängigen namens Auflösungs Funktionen mit einer entsprechenden Sequenz von [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)und [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) -Funktionsaufrufen.</span><span class="sxs-lookup"><span data-stu-id="74a44-123">The *Ws2\_32.dll* implements these compatibility functions in terms of the new, protocol-independent name resolution facilities using an appropriate sequence of [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) function calls.</span></span> <span data-ttu-id="74a44-124">Die Details zur Zuordnung der **getxbyy** -Funktionen zu namens Auflösungs Funktionen finden Sie unten.</span><span class="sxs-lookup"><span data-stu-id="74a44-124">The details of how the **GetXbyY** functions are mapped to name resolution functions are provided below.</span></span> <span data-ttu-id="74a44-125">Der Ws2 \_ -32.dll behandelt die Unterschiede zwischen den asynchronen und synchronen Versionen der **getxbyy** -Funktionen, sodass nur die Implementierung der synchronen **getxbyy** -Funktionen erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="74a44-125">The Ws2\_32.dll handles the differences between the asynchronous and synchronous versions of the **GetXbyY** functions, so that only the implementation of the synchronous **GetXbyY** functions are discussed.</span></span>

 

 
