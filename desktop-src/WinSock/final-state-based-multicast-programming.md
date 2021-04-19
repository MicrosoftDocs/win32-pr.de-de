---
description: In diesem Abschnitt wird die endgültige Zustands basierte Multicast Programmierung mithilfe von IOCTLs anstelle von Socketoptionen beschrieben. Eine Übersicht über die Unterschiede zwischen der auf dem Endzustand basierenden Multicast Programmierung und der Änderungs basierten Multicast Programmierung finden Sie unter Multicast Programmierung.
ms.assetid: 71c05393-3f8c-42c0-9060-e0df9b5e2578
title: Abschließende Zustands basierte Multicast Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6abfebfc7efe27f1c5a6d63312c376bd659dce57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360037"
---
# <a name="final-state-based-multicast-programming"></a><span data-ttu-id="f2c5f-104">Abschließende Zustands basierte Multicast Programmierung</span><span class="sxs-lookup"><span data-stu-id="f2c5f-104">Final-State-Based Multicast Programming</span></span>

<span data-ttu-id="f2c5f-105">In diesem Abschnitt wird die endgültige Zustands basierte Multicast Programmierung mithilfe von IOCTLs anstelle von Socketoptionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f2c5f-105">This section describes final-state-based multicast programming using IOCTLs instead of socket options.</span></span> <span data-ttu-id="f2c5f-106">Eine Übersicht über die Unterschiede zwischen der auf dem Endzustand basierenden Multicast Programmierung und der Änderungs basierten Multicast Programmierung finden Sie unter [Multicast Programmierung](multicast-programming.md).</span><span class="sxs-lookup"><span data-stu-id="f2c5f-106">For an overview of how final-state-based multicast programming differs from change-based multicast programming, see [Multicast Programming](multicast-programming.md).</span></span>

<span data-ttu-id="f2c5f-107">In der folgenden Tabelle werden die Windows Sockets-IOCTLs beschrieben, die für die Multicast Programmierung unter Windows verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2c5f-107">The following table describes the Windows Sockets IOCTLs used for multicast programming on Windows.</span></span> 

| <span data-ttu-id="f2c5f-108">IOCTL</span><span class="sxs-lookup"><span data-stu-id="f2c5f-108">IOCTL</span></span>                       | <span data-ttu-id="f2c5f-109">Argumenttyp</span><span class="sxs-lookup"><span data-stu-id="f2c5f-109">Argument type</span></span>                                   |
|-----------------------------|-------------------------------------------------|
| <span data-ttu-id="f2c5f-110">Siocsmsfilter</span><span class="sxs-lookup"><span data-stu-id="f2c5f-110">SIOCSMSFILTER</span></span>               | <span data-ttu-id="f2c5f-111">[**Gruppe \_ Filter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) Struktur</span><span class="sxs-lookup"><span data-stu-id="f2c5f-111">[**GROUP\_FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) structure</span></span> |
| <span data-ttu-id="f2c5f-112">Siocgmsfilter</span><span class="sxs-lookup"><span data-stu-id="f2c5f-112">SIOCGMSFILTER</span></span>               | <span data-ttu-id="f2c5f-113">[**Gruppe \_ Filter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) Struktur</span><span class="sxs-lookup"><span data-stu-id="f2c5f-113">[**GROUP\_FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) structure</span></span> |
| <span data-ttu-id="f2c5f-114">Prozessor \_ get- \_ Multicast \_ Filter</span><span class="sxs-lookup"><span data-stu-id="f2c5f-114">SIO\_GET\_MULTICAST\_FILTER</span></span> | <span data-ttu-id="f2c5f-115">[**IP- \_ msfilter-**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) Struktur</span><span class="sxs-lookup"><span data-stu-id="f2c5f-115">[**ip\_msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) structure</span></span>   |
| <span data-ttu-id="f2c5f-116">\_ \_ Multicast Filter für die SIO-Gruppe \_</span><span class="sxs-lookup"><span data-stu-id="f2c5f-116">SIO\_SET\_MULTICAST\_FILTER</span></span> | <span data-ttu-id="f2c5f-117">[**IP- \_ msfilter-**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) Struktur</span><span class="sxs-lookup"><span data-stu-id="f2c5f-117">[**ip\_msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) structure</span></span>   |



 

<span data-ttu-id="f2c5f-118">Beachten Sie, dass **siocsmsfilter** und **siocgmsfilter** IOCTLs unter Windows Vista und höher verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f2c5f-118">Note that the **SIOCSMSFILTER** and **SIOCGMSFILTER** IOCTLS are available on Windows Vista and later.</span></span>

<span data-ttu-id="f2c5f-119">Die Verwendung dieser IOCTLs für Multicast Programmierung bietet bei der Arbeit mit großen Quell Listen Leistungsvorteile.</span><span class="sxs-lookup"><span data-stu-id="f2c5f-119">Using these IOCTLs for multicast programming has performance benefits when working with large source lists.</span></span> <span data-ttu-id="f2c5f-120">Weitere Informationen zu den Parametern und Einstellungen, die mit der Verwendung von "sio \_ get \_ Multicast \_ Filter" oder "sio Set Multicast Filter" verknüpft sind, finden Sie auf \_ \_ \_ der Seite [**Gruppen \_ Filter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) Referenz</span><span class="sxs-lookup"><span data-stu-id="f2c5f-120">For more information about the parameters and settings associated with using SIO\_GET\_MULTICAST\_FILTER or SIO\_SET\_MULTICAST\_FILTER, consult the [**GROUP\_FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) reference page.</span></span> <span data-ttu-id="f2c5f-121">Weitere Informationen zu den Parametern und Einstellungen, die mit der Verwendung von " \_ mget \_ -Multicast \_ Filter" oder "sio \_ \_ -Multicast Filter" verknüpft sind, finden Sie auf \_ der Referenzseite zu [**IP \_**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)</span><span class="sxs-lookup"><span data-stu-id="f2c5f-121">For more information about the parameters and settings associated with using SIO\_GET\_MULTICAST\_FILTER or SIO\_SET\_MULTICAST\_FILTER, consult the [**ip\_msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) reference page.</span></span>

 

 



