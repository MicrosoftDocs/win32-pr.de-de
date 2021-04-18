---
title: Weeklyauslöst. weeksinterval (Eigenschaft)
description: Ruft bei der Skripterstellung das Intervall zwischen den Wochen im Zeitplan ab oder legt es fest.
ms.assetid: 7992dee2-1725-4325-9fe9-eaff84fa5adc
keywords:
- Weeksinterval-Eigenschaft Taskplaner
- Weeksinterval-Eigenschaft Taskplaner, weeklyauslöserobjekt
- Weeklyauslöserobjekt Taskplaner, weeksinterval (Eigenschaft)
topic_type:
- apiref
api_name:
- WeeklyTrigger.WeeksInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4668b68d0b3f83e096284db35df799a63eb677b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340768"
---
# <a name="weeklytriggerweeksinterval-property"></a><span data-ttu-id="4b71e-106">Weeklyauslöst. weeksinterval (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4b71e-106">WeeklyTrigger.WeeksInterval property</span></span>

<span data-ttu-id="4b71e-107">Ruft bei der Skripterstellung das Intervall zwischen den Wochen im Zeitplan ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="4b71e-107">For scripting, gets or sets the interval between the weeks in the schedule.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b71e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b71e-108">Syntax</span></span>


```VB
WeeklyTrigger.WeeksInterval As short
```



## <a name="property-value"></a><span data-ttu-id="4b71e-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4b71e-109">Property value</span></span>

<span data-ttu-id="4b71e-110">Das Intervall zwischen den Wochen im Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="4b71e-110">The interval between the weeks in the schedule.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b71e-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b71e-111">Remarks</span></span>

<span data-ttu-id="4b71e-112">Ein Intervall von 1 erzeugt einen wöchentlichen Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="4b71e-112">An interval of 1 produces a weekly schedule.</span></span> <span data-ttu-id="4b71e-113">Ein Intervall von 2 erzeugt einen Zeitplan für jede Woche.</span><span class="sxs-lookup"><span data-stu-id="4b71e-113">An interval of 2 produces an every-other week schedule.</span></span>

<span data-ttu-id="4b71e-114">Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird das Intervall für einen wöchentlichen Zeitplan mit dem [**weeksinterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="4b71e-114">When reading or writing your own XML for a task, the interval for a weekly schedule is specified using the [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b71e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b71e-115">Requirements</span></span>



| <span data-ttu-id="4b71e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b71e-116">Requirement</span></span> | <span data-ttu-id="4b71e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4b71e-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b71e-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4b71e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4b71e-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b71e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4b71e-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4b71e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4b71e-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b71e-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4b71e-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="4b71e-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="4b71e-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4b71e-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4b71e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4b71e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b71e-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b71e-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b71e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b71e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b71e-127">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="4b71e-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





