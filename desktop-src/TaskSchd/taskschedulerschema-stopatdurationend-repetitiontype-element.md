---
title: Stopatdurationend (repetitiontype)-Element
description: Gibt an, dass eine laufende Instanz der Aufgabe am Ende der Wiederholungsmuster Dauer beendet wird.
ms.assetid: 4e34b5b2-ac93-4951-9de4-3e89614517d1
keywords:
- Stopatdurationend-Element Taskplaner
topic_type:
- apiref
api_name:
- StopAtDurationEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a95f15f3a62d05b9bc28dc9f50b924979e2b748c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343064"
---
# <a name="stopatdurationend-repetitiontype-element"></a><span data-ttu-id="f58cb-104">Stopatdurationend (repetitiontype)-Element</span><span class="sxs-lookup"><span data-stu-id="f58cb-104">StopAtDurationEnd (repetitionType) Element</span></span>

<span data-ttu-id="f58cb-105">Gibt an, dass eine laufende Instanz der Aufgabe am Ende der Wiederholungsmuster Dauer beendet wird.</span><span class="sxs-lookup"><span data-stu-id="f58cb-105">Specifies that a running instance of the task is stopped at the end of the repetition pattern duration.</span></span> <span data-ttu-id="f58cb-106">Dies gilt nur, wenn Wiederholungen festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="f58cb-106">This is applicable only if repetitions are set.</span></span>

``` syntax
<xs:element name="StopAtDurationEnd"
 type="boolean"
 />
```

<span data-ttu-id="f58cb-107">Das **stopatdurationend** -Element wird durch den komplexen Typ " [**wiederholtiontype**](taskschedulerschema-repetitiontype-complextype.md) " definiert.</span><span class="sxs-lookup"><span data-stu-id="f58cb-107">The **StopAtDurationEnd** element is defined by the [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f58cb-108">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="f58cb-108">Parent element</span></span>

| <span data-ttu-id="f58cb-109">Element</span><span class="sxs-lookup"><span data-stu-id="f58cb-109">Element</span></span> | <span data-ttu-id="f58cb-110">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="f58cb-110">Derived from</span></span> | <span data-ttu-id="f58cb-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f58cb-111">Description</span></span> |
|-|-|-|
| [<span data-ttu-id="f58cb-112">**Wiederholen**</span><span class="sxs-lookup"><span data-stu-id="f58cb-112">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md) | [<span data-ttu-id="f58cb-113">**Wiederholungstyp**</span><span class="sxs-lookup"><span data-stu-id="f58cb-113">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="f58cb-114">Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="f58cb-114">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |

## <a name="remarks"></a><span data-ttu-id="f58cb-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f58cb-115">Remarks</span></span>

<span data-ttu-id="f58cb-116">Bei der Skripterstellung wird diese Einstellung mithilfe der [**wiederholungspattern. stopatdurationend**](repetitionpattern-stopatdurationend.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="f58cb-116">For scripting development, this setting is specified using the [**RepetitionPattern.StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) property.</span></span>

<span data-ttu-id="f58cb-117">Bei der C++-Entwicklung wird diese Einstellung mithilfe der [**irepetitionpattern:: stopatdurationend**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="f58cb-117">For C++ development, this setting is specified using the [**IRepetitionPattern::StopAtDurationEnd**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f58cb-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f58cb-118">Requirements</span></span>

| <span data-ttu-id="f58cb-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f58cb-119">Requirement</span></span> | <span data-ttu-id="f58cb-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f58cb-120">Value</span></span> |
|-|-|
| <span data-ttu-id="f58cb-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f58cb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f58cb-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f58cb-122">Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f58cb-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f58cb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f58cb-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f58cb-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |

## <a name="see-also"></a><span data-ttu-id="f58cb-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f58cb-125">See also</span></span>

[<span data-ttu-id="f58cb-126">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="f58cb-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)

[<span data-ttu-id="f58cb-127">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="f58cb-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
