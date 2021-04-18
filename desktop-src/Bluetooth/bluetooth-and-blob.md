---
title: Bluetooth und BLOB
description: Bluetooth verwendet die BLOB-Struktur, um bei Aufrufen der wsasetservice-oder WSALookupService \-Funktionen Transport spezifische Daten an die wsaqueryset-Struktur zu übergeben oder zu empfangen.
ms.assetid: d71f3661-0efb-4376-966c-fb5c340ce1c5
keywords:
- BLOB
- Bluetooth
- Bluetooth
- Bluetooth und BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385f4fab053f975672d3b94fa231b3d7632e58eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340522"
---
# <a name="bluetooth-and-blob"></a><span data-ttu-id="01782-107">Bluetooth und BLOB</span><span class="sxs-lookup"><span data-stu-id="01782-107">Bluetooth and BLOB</span></span>

<span data-ttu-id="01782-108">Bluetooth verwendet die [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) -Struktur, um bei Aufrufen der [**wsasetservice**](bluetooth-and-wsasetservice.md) -oder **WSALookupService** -Funktionen Transport spezifische Daten an die [**wsaqueryset**](bluetooth-and-wsaqueryset-for-set-service.md) -Struktur zu übergeben oder zu empfangen \* .</span><span class="sxs-lookup"><span data-stu-id="01782-108">Bluetooth uses the [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) structure to pass or receive transport-specific data to the [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) structure during calls to the [**WSASetService**](bluetooth-and-wsasetservice.md) or **WSALookupService**\* functions.</span></span>

<span data-ttu-id="01782-109">Zur Verwendung mit Bluetooth und der [**wsasetservice**](bluetooth-and-wsasetservice.md) -Funktion benötigen die [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) -Strukturmember die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="01782-109">For use with Bluetooth and the [**WSASetService**](bluetooth-and-wsasetservice.md) function, the [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) structure members are required to have the following settings:</span></span>

-   <span data-ttu-id="01782-110">Das **CBSIZE** -Element muss auf die Größe der im **pblobdata** -Member verwendeten Struktur des [**BTH- \_ Set- \_ dienstansatzes**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) (in Bytes) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="01782-110">The **cbsize** member must be set to the size of the [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure used in the **pBlobData** member, in bytes.</span></span>
-   <span data-ttu-id="01782-111">Der **pblobdata** -Member muss ein Zeiger auf eine [**BTH \_ Set \_ Service**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) -Struktur sein.</span><span class="sxs-lookup"><span data-stu-id="01782-111">The **pBlobData** member must be a pointer to a [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure.</span></span>

<span data-ttu-id="01782-112">Verwenden Sie für die Verwendung mit Bluetooth und [wsalookupservicebegin für die Geräte Anfrage](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="01782-112">For use with Bluetooth and [WSALookupServiceBegin for Device Inquiry](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), use the following settings:</span></span>

-   <span data-ttu-id="01782-113">Das **CBSIZE** -Element muss auf die Größe der [**BTH- \_ Abfrage \_ Geräte**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) Struktur, die im **pblobdata** -Element verwendet wird, in Bytes festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="01782-113">The **cbsize** member must be set to the size of the [**BTH\_QUERY\_DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) structure used in the **pBlobData** member, in bytes.</span></span>
-   <span data-ttu-id="01782-114">Der **pblobdata** -Member muss ein Zeiger auf eine [**BTH- \_ Abfrage \_ Geräte**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) Struktur sein.</span><span class="sxs-lookup"><span data-stu-id="01782-114">The **pBlobData** member must be a pointer to a [**BTH\_QUERY\_DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) structure.</span></span>

<span data-ttu-id="01782-115">Verwenden Sie für die Verwendung mit Bluetooth und [wsalookupservicebegin für die Dienst](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)Ermittlung die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="01782-115">For use with Bluetooth and [WSALookupServiceBegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md), use the following settings:</span></span>

-   <span data-ttu-id="01782-116">Das **CBSIZE** -Element muss auf die Größe der [**BTH- \_ Abfrage \_ Dienst**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) Struktur festgelegt werden, die im **pblobdata** -Member verwendet wird (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="01782-116">The **cbsize** member must be set to the size of the [**BTH\_QUERY\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) structure used in the **pBlobData** member, in bytes.</span></span>
-   <span data-ttu-id="01782-117">Der **pblobdata** -Member muss ein Zeiger auf eine [**BTH- \_ Abfrage \_ Dienst**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) Struktur sein.</span><span class="sxs-lookup"><span data-stu-id="01782-117">The **pBlobData** member must be a pointer to a [**BTH\_QUERY\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) structure.</span></span>

<span data-ttu-id="01782-118">Weitere Informationen finden Sie im Abschnitt "Hinweise" auf der Referenzseite zum [**BTH- \_ Satz der \_ Dienst**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) Struktur.</span><span class="sxs-lookup"><span data-stu-id="01782-118">For more information, see the Remarks section in the [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure reference page.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01782-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="01782-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01782-120">Bluetooth und wsalookupservicebegin für Geräte Anfrage</span><span class="sxs-lookup"><span data-stu-id="01782-120">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="01782-121">Bluetooth und wsalookupservicebegin für die Dienst Ermittlung</span><span class="sxs-lookup"><span data-stu-id="01782-121">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="01782-122">Bluetooth und wsasetservice</span><span class="sxs-lookup"><span data-stu-id="01782-122">Bluetooth and WSASetService</span></span>](bluetooth-and-wsasetservice.md)
</dt> <dt>

[<span data-ttu-id="01782-123">Windows-Sockets</span><span class="sxs-lookup"><span data-stu-id="01782-123">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="01782-124">**BLOB**</span><span class="sxs-lookup"><span data-stu-id="01782-124">**BLOB**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[<span data-ttu-id="01782-125">**BTH- \_ Abfrage \_ Gerät**</span><span class="sxs-lookup"><span data-stu-id="01782-125">**BTH\_QUERY\_DEVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[<span data-ttu-id="01782-126">**BTH- \_ Abfrage \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="01782-126">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="01782-127">**BTH- \_ Set- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="01782-127">**BTH\_SET\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)
</dt> <dt>

[<span data-ttu-id="01782-128">**Wsalookupservicebegin**</span><span class="sxs-lookup"><span data-stu-id="01782-128">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="01782-129">**Wsaqueryset**</span><span class="sxs-lookup"><span data-stu-id="01782-129">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="01782-130">**Wsasetservice**</span><span class="sxs-lookup"><span data-stu-id="01782-130">**WSASetService**</span></span>](bluetooth-and-wsasetservice.md)
</dt> </dl>

 

 