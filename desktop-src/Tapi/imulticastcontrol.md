---
description: Die imulticastcontrol-Schnittstelle wird vom ipconf-MSP implementiert und ist nur für Multicast-aufrufobjekte verfügbar.
ms.assetid: 9bdb4ab9-30b3-46fb-b13a-de9c294c8046
title: Imulticastcontrol-Schnittstelle (confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98ad006ea41034d6d4da32359d1ecbcdd250ab6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366844"
---
# <a name="imulticastcontrol-interface"></a><span data-ttu-id="37361-103">Imulticastcontrol-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="37361-103">IMulticastControl interface</span></span>

<span data-ttu-id="37361-104">\[**Imulticastcontrol** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="37361-104">\[**IMulticastControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="37361-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="37361-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="37361-106">Die **imulticastcontrol** -Schnittstelle wird vom ipconf-MSP implementiert und ist nur für Multicast-aufrufobjekte verfügbar.</span><span class="sxs-lookup"><span data-stu-id="37361-106">The **IMulticastControl** interface is implemented by the IPConf MSP and available only on multicast call objects.</span></span> <span data-ttu-id="37361-107">Diese Schnittstelle macht Methoden verfügbar, die das Erstellen und manipulieren von Terminals ermöglichen, die zwischen h323-und SDP-Clients kommunizieren können.</span><span class="sxs-lookup"><span data-stu-id="37361-107">This interface exposes methods that enable creation and manipulation of terminals that can communicate between H323 and SDP clients.</span></span> <span data-ttu-id="37361-108">Die **imulticastcontrol** -Schnittstelle steuert den Multicast-Loopback Modus.</span><span class="sxs-lookup"><span data-stu-id="37361-108">The **IMulticastControl** interface controls the multicast loopback mode.</span></span>

<span data-ttu-id="37361-109">Im Modus " \_ kein \_ Loopback" ist das Multicast-Loopback deaktiviert. Dies bedeutet, dass zwei Anwendungen auf dem gleichen Computer, die derselben Multicast Gruppe beitreten, die Pakete der anderen erhalten.</span><span class="sxs-lookup"><span data-stu-id="37361-109">In the MM\_NO\_LOOPBACK mode, multicast loopback is disabled, which means two applications on the same machine who join the same multicast group will get each other's packets.</span></span> <span data-ttu-id="37361-110">Dieser Modus hat die beste Leistung, wenn immer nur eine Anwendung zur Multicast Gruppe auf dem Computer gehört.</span><span class="sxs-lookup"><span data-stu-id="37361-110">This mode has the best performance if there is always only one application joining the multicast group on the machine.</span></span> <span data-ttu-id="37361-111">MM \_ kein \_ Loopback Modus ist der Standardmodus.</span><span class="sxs-lookup"><span data-stu-id="37361-111">MM\_NO\_LOOPBACK mode is the default mode.</span></span>

<span data-ttu-id="37361-112">Der \_ vollständige \_ Modus von mm ist nur für Testzwecke geeignet.</span><span class="sxs-lookup"><span data-stu-id="37361-112">The MM\_FULL\_LOOPBACK mode is good only for testing.</span></span> <span data-ttu-id="37361-113">Alle gesendeten Pakete werden ebenfalls in eine Schleife zurückgeleitet.</span><span class="sxs-lookup"><span data-stu-id="37361-113">All the packets sent out are looped back as well.</span></span> <span data-ttu-id="37361-114">Dies kann verwendet werden, um zu testen, ob die Geräte funktionieren.</span><span class="sxs-lookup"><span data-stu-id="37361-114">This can be used to test if the devices are working.</span></span>

<span data-ttu-id="37361-115">Der selektive mm- \_ \_ Loopback Modus wird verwendet, um es mehreren Anwendungen auf einem Computer zu ermöglichen, derselben Multicast Gruppe beizutreten.</span><span class="sxs-lookup"><span data-stu-id="37361-115">The MM\_SELECTIVE\_LOOPBACK mode is used to enable multiple applications on one machine to join the same multicast group.</span></span> <span data-ttu-id="37361-116">Die Pakete werden vom Stapel zurückgeleitet, und jede RTP-Sitzung ist für das Herausfiltern unerwünschter Pakete zuständig.</span><span class="sxs-lookup"><span data-stu-id="37361-116">The packets are looped back from the stack, and each RTP session is responsible for filtering out unwanted packets.</span></span>

## <a name="members"></a><span data-ttu-id="37361-117">Member</span><span class="sxs-lookup"><span data-stu-id="37361-117">Members</span></span>

<span data-ttu-id="37361-118">Die **imulticastcontrol** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="37361-118">The **IMulticastControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="37361-119">**Imulticastcontrol** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="37361-119">**IMulticastControl** also has these types of members:</span></span>

-   [<span data-ttu-id="37361-120">Methoden</span><span class="sxs-lookup"><span data-stu-id="37361-120">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="37361-121">Methoden</span><span class="sxs-lookup"><span data-stu-id="37361-121">Methods</span></span>

<span data-ttu-id="37361-122">Die **imulticastcontrol** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="37361-122">The **IMulticastControl** interface has these methods.</span></span>



| <span data-ttu-id="37361-123">Methode</span><span class="sxs-lookup"><span data-stu-id="37361-123">Method</span></span>                                                          | <span data-ttu-id="37361-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37361-124">Description</span></span>                                  |
|:----------------------------------------------------------------|:---------------------------------------------|
| [<span data-ttu-id="37361-125">**\_Loopbackmodus erhalten**</span><span class="sxs-lookup"><span data-stu-id="37361-125">**get\_LoopbackMode**</span></span>](imulticastcontrol-get-loopbackmode.md) | <span data-ttu-id="37361-126">Ruft den Multicast-Loopback Modus ab.</span><span class="sxs-lookup"><span data-stu-id="37361-126">Gets the multicast loopback mode.</span></span><br/> |
| [<span data-ttu-id="37361-127">**\_loopbackmode platzieren**</span><span class="sxs-lookup"><span data-stu-id="37361-127">**put\_LoopbackMode**</span></span>](imulticastcontrol-put-loopbackmode.md) | <span data-ttu-id="37361-128">Legt den Multicast-Loopback Modus fest.</span><span class="sxs-lookup"><span data-stu-id="37361-128">Sets the multicast loopback mode.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="37361-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37361-129">Requirements</span></span>



| <span data-ttu-id="37361-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37361-130">Requirement</span></span> | <span data-ttu-id="37361-131">Wert</span><span class="sxs-lookup"><span data-stu-id="37361-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37361-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="37361-132">TAPI version</span></span><br/> | <span data-ttu-id="37361-133">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="37361-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="37361-134">Header</span><span class="sxs-lookup"><span data-stu-id="37361-134">Header</span></span><br/>       | <dl> <span data-ttu-id="37361-135"><dt>"Confpriv. h"</dt></span><span class="sxs-lookup"><span data-stu-id="37361-135"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="37361-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="37361-136">Library</span></span><br/>      | <dl> <span data-ttu-id="37361-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="37361-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="37361-138">DLL</span><span class="sxs-lookup"><span data-stu-id="37361-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="37361-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37361-139"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="37361-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37361-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37361-141">Ipconf-msp</span><span class="sxs-lookup"><span data-stu-id="37361-141">IPConf MSP</span></span>](ipconf-msp.md)
</dt> </dl>

 

