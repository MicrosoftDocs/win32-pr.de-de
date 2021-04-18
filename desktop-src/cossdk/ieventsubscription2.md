---
description: Speichert Informationen zu Ereignis Abonnements und ruft Sie ab. Diese Schnittstelle erweitert die ieventabonnement-Schnittstelle.
ms.assetid: f153afb7-c897-40f8-81ed-50308844cac5
title: IEventSubscription2-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2
api_type:
- COM
api_location: ''
ms.openlocfilehash: bc7e3e41efc4b44c00c23f0910b8b696940fc1df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344374"
---
# <a name="ieventsubscription2-interface"></a><span data-ttu-id="b714d-104">IEventSubscription2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b714d-104">IEventSubscription2 interface</span></span>

<span data-ttu-id="b714d-105">Speichert Informationen zu Ereignis Abonnements und ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="b714d-105">Stores and retrieves information about event subscriptions.</span></span> <span data-ttu-id="b714d-106">Diese Schnittstelle erweitert die [**ieventabonnement**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b714d-106">This interface extends the [**IEventSubscription**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="b714d-107">Gründe für die Implementierung</span><span class="sxs-lookup"><span data-stu-id="b714d-107">When to implement</span></span>

<span data-ttu-id="b714d-108">Sie müssen die **IEventSubscription2** -Schnittstelle nicht implementieren.</span><span class="sxs-lookup"><span data-stu-id="b714d-108">You do not need to implement the **IEventSubscription2** interface.</span></span> <span data-ttu-id="b714d-109">Eine vom System bereitgestellte Ereignis Objektklasse (CLSID \_ ceventabonnement) implementiert **IEventSubscription2**.</span><span class="sxs-lookup"><span data-stu-id="b714d-109">A system-supplied event object class (CLSID\_CEventSubscription) implements **IEventSubscription2**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="b714d-110">Verwendung</span><span class="sxs-lookup"><span data-stu-id="b714d-110">When to use</span></span>

<span data-ttu-id="b714d-111">Das [com+-Ereignis](com--events.md) System verwendet diese Schnittstelle zum Abrufen von Informationen zu einzelnen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="b714d-111">The [COM+ Events](com--events.md) system uses this interface to obtain information about individual subscriptions.</span></span>

## <a name="members"></a><span data-ttu-id="b714d-112">Member</span><span class="sxs-lookup"><span data-stu-id="b714d-112">Members</span></span>

<span data-ttu-id="b714d-113">Die **IEventSubscription2** -Schnittstelle erbt von **ieventabonnement**.</span><span class="sxs-lookup"><span data-stu-id="b714d-113">The **IEventSubscription2** interface inherits from **IEventSubscription**.</span></span> <span data-ttu-id="b714d-114">**IEventSubscription2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b714d-114">**IEventSubscription2** also has these types of members:</span></span>

-   [<span data-ttu-id="b714d-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b714d-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b714d-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b714d-116">Properties</span></span>

<span data-ttu-id="b714d-117">Die **IEventSubscription2** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b714d-117">The **IEventSubscription2** interface has these properties.</span></span>



| <span data-ttu-id="b714d-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b714d-118">Property</span></span>                                                                      | <span data-ttu-id="b714d-119">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="b714d-119">Access type</span></span>           | <span data-ttu-id="b714d-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b714d-120">Description</span></span>                                                |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="b714d-121">**FilterCriteria**</span><span class="sxs-lookup"><span data-stu-id="b714d-121">**FilterCriteria**</span></span>](ieventsubscription2-filtercriteria.md)<br/>       | <span data-ttu-id="b714d-122">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b714d-122">Read/write</span></span><br/> | <span data-ttu-id="b714d-123">Die Filterkriterien für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b714d-123">The filter criteria governing the subscription.</span></span><br/> |
| [<span data-ttu-id="b714d-124">**Abonniert**</span><span class="sxs-lookup"><span data-stu-id="b714d-124">**SubscriberMoniker**</span></span>](ieventsubscription2-subscribermoniker.md)<br/> | <span data-ttu-id="b714d-125">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b714d-125">Read/write</span></span><br/> | <span data-ttu-id="b714d-126">Der Moniker des Abonnenten.</span><span class="sxs-lookup"><span data-stu-id="b714d-126">The subscriber's moniker.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="b714d-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b714d-127">Requirements</span></span>



| <span data-ttu-id="b714d-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b714d-128">Requirement</span></span> | <span data-ttu-id="b714d-129">Wert</span><span class="sxs-lookup"><span data-stu-id="b714d-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b714d-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b714d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b714d-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b714d-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b714d-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b714d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b714d-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b714d-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b714d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b714d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b714d-135">**Ieventabonnement**</span><span class="sxs-lookup"><span data-stu-id="b714d-135">**IEventSubscription**</span></span>](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 




