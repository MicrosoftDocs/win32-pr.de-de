---
title: Sessionstatechangetrigger (triggergroup)-Element
description: Gibt einen-Endpunkt an, der einen Task startet, wenn sich der Status einer Terminal Server Sitzung ändert.
ms.assetid: 38b0da3c-205f-48c5-83e6-ff7c432c02b9
keywords:
- Sessionstatechange-Element Taskplaner
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d21847a929e79e2da53b1e66a23aec0c2f1c630f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742753"
---
# <a name="sessionstatechangetrigger-triggergroup-element"></a><span data-ttu-id="ce9ea-104">Sessionstatechangetrigger (triggergroup)-Element</span><span class="sxs-lookup"><span data-stu-id="ce9ea-104">SessionStateChangeTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="ce9ea-105">Gibt einen-Endpunkt an, der einen Task startet, wenn sich der Status einer Terminal Server Sitzung ändert.</span><span class="sxs-lookup"><span data-stu-id="ce9ea-105">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span>

``` syntax
<xs:element name="SessionStateChangeTrigger"
    type="sessionStateChangeTriggerType"
 />
```

<span data-ttu-id="ce9ea-106">Das **sessionstatechangetrigger** -Element wird von [**triggergroup**](taskschedulerschema-triggergroup-group.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="ce9ea-106">The **SessionStateChangeTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="ce9ea-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="ce9ea-107">Parent element</span></span>



| <span data-ttu-id="ce9ea-108">Element</span><span class="sxs-lookup"><span data-stu-id="ce9ea-108">Element</span></span>                                                           | <span data-ttu-id="ce9ea-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="ce9ea-109">Derived from</span></span>                                                         | <span data-ttu-id="ce9ea-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce9ea-110">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="ce9ea-111">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="ce9ea-111">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="ce9ea-112">**triggerstype**</span><span class="sxs-lookup"><span data-stu-id="ce9ea-112">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="ce9ea-113">Gibt die Trigger an, die den Task starten.</span><span class="sxs-lookup"><span data-stu-id="ce9ea-113">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="ce9ea-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ce9ea-114">Child elements</span></span>



| <span data-ttu-id="ce9ea-115">Element</span><span class="sxs-lookup"><span data-stu-id="ce9ea-115">Element</span></span>                                                                                      | <span data-ttu-id="ce9ea-116">type</span><span class="sxs-lookup"><span data-stu-id="ce9ea-116">Type</span></span>                                                                                    | <span data-ttu-id="ce9ea-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce9ea-117">Description</span></span>                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce9ea-118">**Verzögern**</span><span class="sxs-lookup"><span data-stu-id="ce9ea-118">**Delay**</span></span>](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | <span data-ttu-id="ce9ea-119">duration</span><span class="sxs-lookup"><span data-stu-id="ce9ea-119">duration</span></span>                                                                                | <span data-ttu-id="ce9ea-120">Gibt einen Wert an, der die Länge der Verzögerung angibt, bevor ein Task gestartet wird, wenn eine Terminal Server-Sitzungs Zustandsänderung erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="ce9ea-120">Specifies a value that indicates the length of the delay before a task is started when a Terminal Server session state change is detected.</span></span><br/> |
| [<span data-ttu-id="ce9ea-121">**StateChange**</span><span class="sxs-lookup"><span data-stu-id="ce9ea-121">**StateChange**</span></span>](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [<span data-ttu-id="ce9ea-122">**sessionstatechangetype**</span><span class="sxs-lookup"><span data-stu-id="ce9ea-122">**sessionStateChangeType**</span></span>](taskschedulerschema-sessionstatechangetype-simpletype.md) | <span data-ttu-id="ce9ea-123">Gibt die Art der Terminal Server-Sitzungs Änderung an, die einen Task Start auslöst.</span><span class="sxs-lookup"><span data-stu-id="ce9ea-123">Specifies the kind of Terminal Server session change that would trigger a task launch.</span></span><br/>                                                     |
| [<span data-ttu-id="ce9ea-124">**UserID**</span><span class="sxs-lookup"><span data-stu-id="ce9ea-124">**UserId**</span></span>](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [<span data-ttu-id="ce9ea-125">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="ce9ea-125">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                 | <span data-ttu-id="ce9ea-126">Gibt den Benutzer für die Terminal Server Sitzung an.</span><span class="sxs-lookup"><span data-stu-id="ce9ea-126">Specifies the user for the Terminal Server session.</span></span> <span data-ttu-id="ce9ea-127">Wenn eine Sitzungs Zustandsänderung für diesen Benutzer erkannt wird, wird eine Aufgabe gestartet.</span><span class="sxs-lookup"><span data-stu-id="ce9ea-127">When a session state change is detected for this user, a task is started.</span></span><br/>              |



## <a name="remarks"></a><span data-ttu-id="ce9ea-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce9ea-128">Remarks</span></span>

<span data-ttu-id="ce9ea-129">Bei der Skripterstellung wird ein Sitzungs Status Änderungs-Auslösung mithilfe des [**sessionstatechangeghost**](sessionstatechangetrigger.md) -Objekts angegeben.</span><span class="sxs-lookup"><span data-stu-id="ce9ea-129">For scripting development, a session state change trigger is specified using the [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) object.</span></span>

<span data-ttu-id="ce9ea-130">Bei der C++-Entwicklung wird ein Sitzungs Status Änderungs-Auslösung mithilfe der [**isessionstatechange-**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) Schnittstelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="ce9ea-130">For C++ development, a session state change trigger is specified using the [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce9ea-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce9ea-131">Requirements</span></span>



| <span data-ttu-id="ce9ea-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce9ea-132">Requirement</span></span> | <span data-ttu-id="ce9ea-133">Wert</span><span class="sxs-lookup"><span data-stu-id="ce9ea-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ce9ea-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce9ea-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ce9ea-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce9ea-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ce9ea-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce9ea-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ce9ea-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce9ea-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





