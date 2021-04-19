---
description: Speichert Informationen zu Ereignis Abonnements und ruft Sie ab. Diese Schnittstelle erweitert die IEventSubscription2-Schnittstelle.
ms.assetid: fd1c136e-6e4e-42ca-a951-4aa5fcdfaa49
title: IEventSubscription3-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3
api_type:
- COM
api_location: ''
ms.openlocfilehash: 94225faf957b2eac3388422d74df3cfdb8bf6d90
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346456"
---
# <a name="ieventsubscription3-interface"></a><span data-ttu-id="aecd0-104">IEventSubscription3-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="aecd0-104">IEventSubscription3 interface</span></span>

<span data-ttu-id="aecd0-105">Speichert Informationen zu Ereignis Abonnements und ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="aecd0-105">Stores and retrieves information about event subscriptions.</span></span> <span data-ttu-id="aecd0-106">Diese Schnittstelle erweitert die [**IEventSubscription2**](ieventsubscription2.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="aecd0-106">This interface extends the [**IEventSubscription2**](ieventsubscription2.md) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="aecd0-107">Gründe für die Implementierung</span><span class="sxs-lookup"><span data-stu-id="aecd0-107">When to implement</span></span>

<span data-ttu-id="aecd0-108">Sie müssen die **IEventSubscription3** -Schnittstelle nicht implementieren.</span><span class="sxs-lookup"><span data-stu-id="aecd0-108">You do not need to implement the **IEventSubscription3** interface.</span></span> <span data-ttu-id="aecd0-109">Eine vom System bereitgestellte Ereignis Objektklasse (CLSID \_ ceventabonnement) implementiert **IEventSubscription3**.</span><span class="sxs-lookup"><span data-stu-id="aecd0-109">A system-supplied event object class (CLSID\_CEventSubscription) implements **IEventSubscription3**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="aecd0-110">Verwendung</span><span class="sxs-lookup"><span data-stu-id="aecd0-110">When to use</span></span>

<span data-ttu-id="aecd0-111">Das [com+-Ereignis](com--events.md) System verwendet diese Schnittstelle zum Abrufen von Informationen zu einzelnen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="aecd0-111">The [COM+ Events](com--events.md) system uses this interface to obtain information about individual subscriptions.</span></span>

## <a name="members"></a><span data-ttu-id="aecd0-112">Member</span><span class="sxs-lookup"><span data-stu-id="aecd0-112">Members</span></span>

<span data-ttu-id="aecd0-113">Die **IEventSubscription3** -Schnittstelle erbt von **IEventSubscription2**.</span><span class="sxs-lookup"><span data-stu-id="aecd0-113">The **IEventSubscription3** interface inherits from **IEventSubscription2**.</span></span> <span data-ttu-id="aecd0-114">**IEventSubscription3** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="aecd0-114">**IEventSubscription3** also has these types of members:</span></span>

-   [<span data-ttu-id="aecd0-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aecd0-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aecd0-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aecd0-116">Properties</span></span>

<span data-ttu-id="aecd0-117">Die **IEventSubscription3** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="aecd0-117">The **IEventSubscription3** interface has these properties.</span></span>



| <span data-ttu-id="aecd0-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="aecd0-118">Property</span></span>                                                                                  | <span data-ttu-id="aecd0-119">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="aecd0-119">Access type</span></span>           | <span data-ttu-id="aecd0-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aecd0-120">Description</span></span>                                                |
|:------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="aecd0-121">**Eventclassapplicationid**</span><span class="sxs-lookup"><span data-stu-id="aecd0-121">**EventClassApplicationID**</span></span>](ieventsubscription3-eventclassapplicationid.md)<br/> | <span data-ttu-id="aecd0-122">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="aecd0-122">Read/write</span></span><br/> | <span data-ttu-id="aecd0-123">Die Anwendungs-GUID des Ereignis Klassen Objekts.</span><span class="sxs-lookup"><span data-stu-id="aecd0-123">The application GUID of the event class object.</span></span><br/> |
| [<span data-ttu-id="aecd0-124">**Eventclasspartitionid**</span><span class="sxs-lookup"><span data-stu-id="aecd0-124">**EventClassPartitionID**</span></span>](ieventsubscription3-eventclasspartitionid.md)<br/>     | <span data-ttu-id="aecd0-125">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="aecd0-125">Read/write</span></span><br/> | <span data-ttu-id="aecd0-126">Die Partitions-GUID des Ereignis Klassen Objekts.</span><span class="sxs-lookup"><span data-stu-id="aecd0-126">The partition GUID of the event class object.</span></span><br/>   |
| [<span data-ttu-id="aecd0-127">**Abonnement-ID**</span><span class="sxs-lookup"><span data-stu-id="aecd0-127">**SubscriberApplicationID**</span></span>](ieventsubscription3-subscriberapplicationid.md)<br/> | <span data-ttu-id="aecd0-128">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="aecd0-128">Read/write</span></span><br/> | <span data-ttu-id="aecd0-129">Die Anwendungs-GUID des Abonnenten.</span><span class="sxs-lookup"><span data-stu-id="aecd0-129">The application GUID of the subscriber.</span></span><br/>         |
| [<span data-ttu-id="aecd0-130">**Abonnement-ID**</span><span class="sxs-lookup"><span data-stu-id="aecd0-130">**SubscriberPartitionID**</span></span>](ieventsubscription3-subscriberpartitionid.md)<br/>     | <span data-ttu-id="aecd0-131">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="aecd0-131">Read/write</span></span><br/> | <span data-ttu-id="aecd0-132">Die Partitions-GUID des Abonnenten.</span><span class="sxs-lookup"><span data-stu-id="aecd0-132">The partition GUID of the subscriber.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="aecd0-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aecd0-133">Requirements</span></span>



| <span data-ttu-id="aecd0-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aecd0-134">Requirement</span></span> | <span data-ttu-id="aecd0-135">Wert</span><span class="sxs-lookup"><span data-stu-id="aecd0-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="aecd0-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aecd0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="aecd0-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aecd0-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="aecd0-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aecd0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="aecd0-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aecd0-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="aecd0-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aecd0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aecd0-141">**IEventSubscription2**</span><span class="sxs-lookup"><span data-stu-id="aecd0-141">**IEventSubscription2**</span></span>](ieventsubscription2.md)
</dt> </dl>

 

 




