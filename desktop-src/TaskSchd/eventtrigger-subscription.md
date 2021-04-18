---
title: EventTrigger. Abonnement (Eigenschaft)
description: Ruft bei der Skripterstellung eine Abfrage Zeichenfolge ab, die das Ereignis identifiziert, das den-Triggern auslöst
ms.assetid: 31d32426-3dd7-41f9-89cc-b13767871b74
keywords:
- Abonnement Eigenschaft Taskplaner
- Abonnement Eigenschaft Taskplaner, EventTrigger-Objekt
- EventTrigger-Objekt Taskplaner, Abonnement Eigenschaft
topic_type:
- apiref
api_name:
- EventTrigger.Subscription
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68ad05576e248d3ad6c2551a8654a9198ca3c0f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338781"
---
# <a name="eventtriggersubscription-property"></a><span data-ttu-id="fd1aa-106">EventTrigger. Abonnement (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fd1aa-106">EventTrigger.Subscription property</span></span>

<span data-ttu-id="fd1aa-107">Ruft bei der Skripterstellung eine Abfrage Zeichenfolge ab, die das Ereignis identifiziert, das den-Triggern auslöst</span><span class="sxs-lookup"><span data-stu-id="fd1aa-107">For scripting, gets or sets a query string that identifies the event that fires the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd1aa-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd1aa-108">Syntax</span></span>


```VB
EventTrigger.Subscription As String
```



## <a name="property-value"></a><span data-ttu-id="fd1aa-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="fd1aa-109">Property value</span></span>

<span data-ttu-id="fd1aa-110">Eine Abfrage Zeichenfolge, die das Ereignis identifiziert, das den-Triggern auslöst.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-110">A query string that identifies the event that fires the trigger.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd1aa-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd1aa-111">Remarks</span></span>

<span data-ttu-id="fd1aa-112">Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird das Ereignis Abonnement mit dem [**Abonnement**](taskschedulerschema-subscription-eventtriggertype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-112">When reading or writing your own XML for a task, the event subscription is specified using the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="fd1aa-113">Weitere Informationen zum Schreiben einer Abfrage Zeichenfolge für bestimmte Ereignisse finden Sie unter [Ereignis Auswahl](/previous-versions//aa385231(v=vs.85)) und [Abonnieren von Ereignissen](../wes/subscribing-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="fd1aa-113">For more information about writing a query string for certain events, see [Event Selection](/previous-versions//aa385231(v=vs.85)) and [Subscribing to Events](../wes/subscribing-to-events.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fd1aa-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd1aa-114">Examples</span></span>

<span data-ttu-id="fd1aa-115">Die folgende Abfrage Zeichenfolge definiert ein Abonnement für alle Ereignisse der Ebene 2 im System Kanal:</span><span class="sxs-lookup"><span data-stu-id="fd1aa-115">The following query string defines a subscription to all level 2 events in the System channel:</span></span>


```XML
"<QueryList>
    <Query Id='1'>
        <Select Path='System'>*[System/Level=2]</Select>
    </Query>
</QueryList>" 
```



## <a name="requirements"></a><span data-ttu-id="fd1aa-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd1aa-116">Requirements</span></span>



| <span data-ttu-id="fd1aa-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd1aa-117">Requirement</span></span> | <span data-ttu-id="fd1aa-118">Wert</span><span class="sxs-lookup"><span data-stu-id="fd1aa-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd1aa-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd1aa-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fd1aa-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd1aa-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fd1aa-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd1aa-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fd1aa-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd1aa-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fd1aa-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="fd1aa-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="fd1aa-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fd1aa-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fd1aa-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fd1aa-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd1aa-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd1aa-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd1aa-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd1aa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd1aa-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="fd1aa-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="fd1aa-129">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="fd1aa-129">**EventTrigger**</span></span>](eventtrigger.md)
</dt> </dl>

 

