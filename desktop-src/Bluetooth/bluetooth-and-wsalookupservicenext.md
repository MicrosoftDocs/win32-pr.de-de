---
title: Bluetooth und WSALookupServiceNext
description: Bluetooth verwendet die WSALookupServiceNext-Funktion zum Abgleichen von Abfragen, die in einem vorherigen wsalookupservicebegin-Befehl angegeben wurden.
ms.assetid: d43cf444-adb6-4313-9614-a8d6d868a88f
keywords:
- Bluetooth
- WSALookupServiceNext
- Bluetooth und WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3ece06e27c9e80e25f22ef0fb09a5790cdf69b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858283"
---
# <a name="bluetooth-and-wsalookupservicenext"></a><span data-ttu-id="eb715-106">Bluetooth und WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="eb715-106">Bluetooth and WSALookupServiceNext</span></span>

<span data-ttu-id="eb715-107">Bluetooth verwendet die [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) -Funktion zum Abgleichen von Abfragen, die in einem vorherigen [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)-Befehl angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="eb715-107">Bluetooth uses the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function to match queries specified in a previous call to [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina).</span></span> <span data-ttu-id="eb715-108">Die Ergebnisse der **WSALookupServiceNext** -Funktion werden durch Einstellungen festgelegt, die in der [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur festgelegt sind, die im anfänglichen **wsalookupservicebegin** -Funktions aufzurufen ist.</span><span class="sxs-lookup"><span data-stu-id="eb715-108">The results of the **WSALookupServiceNext** function are determined by settings set forth in the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure passed in the initial **WSALookupServiceBegin** function call.</span></span>

<span data-ttu-id="eb715-109">Die Schritte für die Geräte Anfrage und die Dienst Ermittlung in Bluetooth sind ausreichend verschieden, um eine separate Behandlung zu verdienen.</span><span class="sxs-lookup"><span data-stu-id="eb715-109">The steps for device inquiry and service discovery in Bluetooth are sufficiently different to merit separate treatment.</span></span> <span data-ttu-id="eb715-110">Weitere Informationen zu Bluetooth und der [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) -Funktion für Geräte Anfragen finden Sie unter [Bluetooth und wsalookupservicebegin für die Geräte Anfrage](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md).</span><span class="sxs-lookup"><span data-stu-id="eb715-110">For more information on Bluetooth and the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function for device inquiries, see [Bluetooth and WSALookupServiceBegin for Device Inquiry](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md).</span></span> <span data-ttu-id="eb715-111">Weitere Informationen zu Bluetooth und der **wsalookupservicebegin** -Funktion für die Dienst Ermittlung finden Sie unter [Bluetooth und wsalookupservicebegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="eb715-111">For more information on Bluetooth and the **WSALookupServiceBegin** function for service discovery, see [Bluetooth and WSALookupServiceBegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb715-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eb715-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb715-113">Ermitteln von Bluetooth-Geräten und -Diensten</span><span class="sxs-lookup"><span data-stu-id="eb715-113">Discovering Bluetooth Devices and Services</span></span>](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[<span data-ttu-id="eb715-114">Bluetooth und wsalookupservicebegin für Geräte Anfrage</span><span class="sxs-lookup"><span data-stu-id="eb715-114">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="eb715-115">Bluetooth und wsalookupservicebegin für die Dienst Ermittlung</span><span class="sxs-lookup"><span data-stu-id="eb715-115">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="eb715-116">Bluetooth und WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="eb715-116">Bluetooth and WSALookupServiceEnd</span></span>](bluetooth-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="eb715-117">**BTH- \_ Abfrage \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="eb715-117">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="eb715-118">**herzustellen**</span><span class="sxs-lookup"><span data-stu-id="eb715-118">**connect**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[<span data-ttu-id="eb715-119">**sockaddr- \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="eb715-119">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="eb715-120">**Wsalookupservicebegin**</span><span class="sxs-lookup"><span data-stu-id="eb715-120">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="eb715-121">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="eb715-121">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="eb715-122">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="eb715-122">**WSALookupServiceNext**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="eb715-123">**Wsaqueryset**</span><span class="sxs-lookup"><span data-stu-id="eb715-123">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> </dl>

 

 