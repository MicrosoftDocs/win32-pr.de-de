---
title: Bluetooth und WSALookupServiceEnd
description: Bluetooth verwendet die WSALookupServiceEnd-Funktion, um eine Abfrage zu beenden, die in einem vorherigen Aufruf von wsalookupservicebegin initiiert wurde, und möglicherweise in nachfolgenden Aufrufen von WSALookupServiceNext erweitert wurde.
ms.assetid: 3f901176-2433-4d51-ae52-648abbd2e318
keywords:
- Bluetooth
- WSALookupServiceEnd
- Bluetooth und WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a032ef5d0e4fa785626ad10c64d6ddc5d383be2c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948827"
---
# <a name="bluetooth-and-wsalookupserviceend"></a><span data-ttu-id="56f3c-106">Bluetooth und WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="56f3c-106">Bluetooth and WSALookupServiceEnd</span></span>

<span data-ttu-id="56f3c-107">Bluetooth verwendet die [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) -Funktion, um eine Abfrage zu beenden, die in einem vorherigen Aufruf von [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)initiiert wurde, und möglicherweise in nachfolgenden Aufrufen von [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)erweitert wurde.</span><span class="sxs-lookup"><span data-stu-id="56f3c-107">Bluetooth uses the [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) function to terminate a query initiated in a previous call to [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina), and perhaps extended in subsequent calls to [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span></span> <span data-ttu-id="56f3c-108">Der **WSALookupServiceEnd** -Befehl beendet die Abfrage und bereinigt den Kontext.</span><span class="sxs-lookup"><span data-stu-id="56f3c-108">The call to **WSALookupServiceEnd** terminates the query and cleans up the context.</span></span>

<span data-ttu-id="56f3c-109">Die Schritte für die Geräte Anfrage und die Dienst Ermittlung in Bluetooth sind ausreichend verschieden, um eine separate Behandlung zu verdienen.</span><span class="sxs-lookup"><span data-stu-id="56f3c-109">The steps for device inquiry and service discovery in Bluetooth are sufficiently different to merit separate treatment.</span></span> <span data-ttu-id="56f3c-110">Weitere Informationen zu Bluetooth und der [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) -Funktion für Geräte Anfragen finden Sie unter [Bluetooth und wsalookupservicebegin für die Geräte Anfrage](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md).</span><span class="sxs-lookup"><span data-stu-id="56f3c-110">For more information on Bluetooth and the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function for device inquiries, see [Bluetooth and WSALookupServiceBegin for Device Inquiry](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md).</span></span> <span data-ttu-id="56f3c-111">Weitere Informationen zu Bluetooth und der **wsalookupservicebegin** -Funktion für die Dienst Ermittlung finden Sie unter [Bluetooth und wsalookupservicebegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="56f3c-111">For more information on Bluetooth and the **WSALookupServiceBegin** function for service discovery, see [Bluetooth and WSALookupServiceBegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="56f3c-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="56f3c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56f3c-113">Ermitteln von Bluetooth-Geräten und -Diensten</span><span class="sxs-lookup"><span data-stu-id="56f3c-113">Discovering Bluetooth Devices and Services</span></span>](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[<span data-ttu-id="56f3c-114">Bluetooth und wsalookupservicebegin für Geräte Anfrage</span><span class="sxs-lookup"><span data-stu-id="56f3c-114">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="56f3c-115">Bluetooth und wsalookupservicebegin für die Dienst Ermittlung</span><span class="sxs-lookup"><span data-stu-id="56f3c-115">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="56f3c-116">Bluetooth und WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="56f3c-116">Bluetooth and WSALookupServiceNext</span></span>](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[<span data-ttu-id="56f3c-117">**BTH- \_ Abfrage \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="56f3c-117">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="56f3c-118">**herzustellen**</span><span class="sxs-lookup"><span data-stu-id="56f3c-118">**connect**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[<span data-ttu-id="56f3c-119">**sockaddr- \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="56f3c-119">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="56f3c-120">**Wsalookupservicebegin**</span><span class="sxs-lookup"><span data-stu-id="56f3c-120">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="56f3c-121">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="56f3c-121">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="56f3c-122">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="56f3c-122">**WSALookupServiceNext**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="56f3c-123">**Wsaqueryset**</span><span class="sxs-lookup"><span data-stu-id="56f3c-123">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="56f3c-124">Windows-Sockets</span><span class="sxs-lookup"><span data-stu-id="56f3c-124">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 