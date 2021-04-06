---
title: Abonnement (eventtriggertype)-Element
description: Gibt die XPath-Abfrage an, die das Ereignis identifiziert, das den-Triggern auslöst.
ms.assetid: ea351a55-c6f9-4e39-b15e-c2a1027a1360
keywords:
- Abonnement Element Taskplaner
topic_type:
- apiref
api_name:
- Subscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efe38f2e825e2de566391a7b1707ce1f8cfbbc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743768"
---
# <a name="subscription-eventtriggertype-element"></a><span data-ttu-id="d32a6-104">Abonnement (eventtriggertype)-Element</span><span class="sxs-lookup"><span data-stu-id="d32a6-104">Subscription (eventTriggerType) Element</span></span>

<span data-ttu-id="d32a6-105">Gibt die XPath-Abfrage an, die das Ereignis identifiziert, das den-Triggern auslöst.</span><span class="sxs-lookup"><span data-stu-id="d32a6-105">Specifies the XPath query that identifies the event that fires the trigger.</span></span>

``` syntax
<xs:element name="Subscription"
    type="nonEmptyString"
 />
```

<span data-ttu-id="d32a6-106">Das **Abonnement** Element wird durch den komplexen Typ [**eventtriggertype**](taskschedulerschema-eventtriggertype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="d32a6-106">The **Subscription** element is defined by the [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d32a6-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="d32a6-107">Parent element</span></span>



| <span data-ttu-id="d32a6-108">Element</span><span class="sxs-lookup"><span data-stu-id="d32a6-108">Element</span></span>                                                                       | <span data-ttu-id="d32a6-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="d32a6-109">Derived from</span></span>                                                                 | <span data-ttu-id="d32a6-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d32a6-110">Description</span></span>                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="d32a6-111">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="d32a6-111">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md) | [<span data-ttu-id="d32a6-112">**eventtriggertype**</span><span class="sxs-lookup"><span data-stu-id="d32a6-112">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md) | <span data-ttu-id="d32a6-113">Gibt einen-Fehler an, der einen Task startet, wenn ein System Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="d32a6-113">Specifies a trigger that starts a task when a system event occurs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d32a6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d32a6-114">Remarks</span></span>

<span data-ttu-id="d32a6-115">Bei der Skript Entwicklung wird das Ereignis Abonnement durch die [**EventTrigger. Abonnement**](eventtrigger-subscription.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="d32a6-115">For script development, the event subscription is specified by the [**EventTrigger.Subscription**](eventtrigger-subscription.md) property.</span></span>

<span data-ttu-id="d32a6-116">Bei der C++-Entwicklung wird das Ereignis Abonnement durch die [**ieventvent:: Abonnement**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="d32a6-116">For C++ development, the event subscription is specified by the [**IEventTrigger::Subscription**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d32a6-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d32a6-117">Requirements</span></span>



| <span data-ttu-id="d32a6-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d32a6-118">Requirement</span></span> | <span data-ttu-id="d32a6-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d32a6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d32a6-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d32a6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d32a6-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d32a6-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d32a6-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d32a6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d32a6-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d32a6-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d32a6-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d32a6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d32a6-125">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="d32a6-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="d32a6-126">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="d32a6-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





