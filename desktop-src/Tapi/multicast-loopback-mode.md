---
description: Die Multicast- \_ Loopback \_ Modus-Enumeration beschreibt den Multicast-Loopback Modus.
ms.assetid: bf9c3665-71cc-4cde-9ad4-1a8b62eddf9f
title: MULTICAST_LOOPBACK_MODE-Enumeration (confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a15505efcd1a9e399866b104da0582ccf846689
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355058"
---
# <a name="multicast_loopback_mode-enumeration"></a><span data-ttu-id="e1337-103">Multicast- \_ Loopback \_ Modus-Enumeration</span><span class="sxs-lookup"><span data-stu-id="e1337-103">MULTICAST\_LOOPBACK\_MODE enumeration</span></span>

<span data-ttu-id="e1337-104">\[**Multicast \_ Der Loopback \_ Modus** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e1337-104">\[**MULTICAST\_LOOPBACK\_MODE** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e1337-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="e1337-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e1337-106">Die **Multicast- \_ Loopback \_ Modus** -Enumeration beschreibt den Multicast-Loopback Modus.</span><span class="sxs-lookup"><span data-stu-id="e1337-106">The **MULTICAST\_LOOPBACK\_MODE** enum describes the multicast loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1337-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1337-107">Syntax</span></span>


```C++
} MULTICAST_LOOPBACK_MODE;
```



## <a name="constants"></a><span data-ttu-id="e1337-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="e1337-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e1337-109"><span id="MM_NO_LOOPBACK"></span><span id="mm_no_loopback"></span>**MM \_ kein \_ Loopback**</span><span class="sxs-lookup"><span data-stu-id="e1337-109"><span id="MM_NO_LOOPBACK"></span><span id="mm_no_loopback"></span>**MM\_NO\_LOOPBACK**</span></span>
</dt> <dd>

<span data-ttu-id="e1337-110">Multicast Loopback ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e1337-110">Multicast loopback is disabled.</span></span> <span data-ttu-id="e1337-111">Dies bedeutet, dass zwei Anwendungen auf dem gleichen Computer, die derselben Multicast Gruppe beitreten, die Pakete der anderen Anwendungen erhalten können.</span><span class="sxs-lookup"><span data-stu-id="e1337-111">That means two applications on the same machine joining the same multicast group can get each other's packets.</span></span>

</dd> <dt>

<span data-ttu-id="e1337-112"><span id="MM_FULL_LOOPBACK"></span><span id="mm_full_loopback"></span>**\_vollständiges \_ Loopback von mm**</span><span class="sxs-lookup"><span data-stu-id="e1337-112"><span id="MM_FULL_LOOPBACK"></span><span id="mm_full_loopback"></span>**MM\_FULL\_LOOPBACK**</span></span>
</dt> <dd>

<span data-ttu-id="e1337-113">Alle gesendeten Pakete werden ebenfalls in eine Schleife zurückgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e1337-113">All the packets sent out are looped back as well.</span></span> <span data-ttu-id="e1337-114">Dieser Modus ist nur für Tests nützlich.</span><span class="sxs-lookup"><span data-stu-id="e1337-114">This mode is useful only for testing.</span></span>

</dd> <dt>

<span data-ttu-id="e1337-115"><span id="MM_SELECTIVE_LOOPBACK"></span><span id="mm_selective_loopback"></span>**selektive mm- \_ \_ Loopback**</span><span class="sxs-lookup"><span data-stu-id="e1337-115"><span id="MM_SELECTIVE_LOOPBACK"></span><span id="mm_selective_loopback"></span>**MM\_SELECTIVE\_LOOPBACK**</span></span>
</dt> <dd>

<span data-ttu-id="e1337-116">Selektives Loopback ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e1337-116">Selective loopback is enabled.</span></span> <span data-ttu-id="e1337-117">Dies bedeutet, dass die Aktivierung mehrerer Anwendungen auf einem Computer ohne Verwirrung in die gleiche Multicast Gruppe eingebunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="e1337-117">That means enabled multiple applications on one machine can join the same multicast group without confusion.</span></span> <span data-ttu-id="e1337-118">Die Pakete werden vom Stapel zurückgeleitet, und jede RTP-Sitzung ist für das Herausfiltern unerwünschter Pakete zuständig.</span><span class="sxs-lookup"><span data-stu-id="e1337-118">The packets are looped back from the stack and each RTP session is responsible for filtering out unwanted packets.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1337-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1337-119">Requirements</span></span>



| <span data-ttu-id="e1337-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1337-120">Requirement</span></span> | <span data-ttu-id="e1337-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e1337-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1337-122">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="e1337-122">TAPI version</span></span><br/> | <span data-ttu-id="e1337-123">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="e1337-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e1337-124">Header</span><span class="sxs-lookup"><span data-stu-id="e1337-124">Header</span></span><br/>       | <dl> <span data-ttu-id="e1337-125"><dt>"Confpriv. h"</dt></span><span class="sxs-lookup"><span data-stu-id="e1337-125"><dt>Confpriv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1337-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1337-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1337-127">**Imulticastcontrol:: get \_ loopbackmode**</span><span class="sxs-lookup"><span data-stu-id="e1337-127">**IMulticastControl::get\_LoopbackMode**</span></span>](imulticastcontrol-get-loopbackmode.md)
</dt> <dt>

[<span data-ttu-id="e1337-128">**Imulticastcontrol::p UT- \_ Loopbackmodus**</span><span class="sxs-lookup"><span data-stu-id="e1337-128">**IMulticastControl::put\_LoopbackMode**</span></span>](imulticastcontrol-put-loopbackmode.md)
</dt> </dl>

 

 




