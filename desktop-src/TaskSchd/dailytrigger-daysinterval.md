---
title: Dailydie. daysinterval (Eigenschaft)
description: Ruft bei der Skripterstellung das Intervall zwischen den Tagen im Zeitplan ab oder legt es fest.
ms.assetid: 13e9f6fd-62ee-4b19-8b3d-a6808e146340
keywords:
- Daysinterval-Eigenschaft Taskplaner
- Daysinterval-Eigenschaft Taskplaner, dailyauslöserobjekt
- Dailyauslöserobjekt Taskplaner, daysinterval-Eigenschaft
topic_type:
- apiref
api_name:
- DailyTrigger.DaysInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6499f3b900fe10b2a2527c2e2ee675cca3151204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517915"
---
# <a name="dailytriggerdaysinterval-property"></a><span data-ttu-id="e4e7d-106">Dailydie. daysinterval (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e4e7d-106">DailyTrigger.DaysInterval property</span></span>

<span data-ttu-id="e4e7d-107">Ruft bei der Skripterstellung das Intervall zwischen den Tagen im Zeitplan ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="e4e7d-107">For scripting, gets or sets the interval between the days in the schedule.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4e7d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4e7d-108">Syntax</span></span>


```VB
DailyTrigger.DaysInterval As short
```



## <a name="property-value"></a><span data-ttu-id="e4e7d-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e4e7d-109">Property value</span></span>

<span data-ttu-id="e4e7d-110">Das Intervall zwischen den Tagen im Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="e4e7d-110">The interval between the days in the schedule.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4e7d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4e7d-111">Remarks</span></span>

<span data-ttu-id="e4e7d-112">Ein Intervall von 1 erzeugt einen täglichen Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="e4e7d-112">An interval of 1 produces a daily schedule.</span></span> <span data-ttu-id="e4e7d-113">Ein Intervall von 2 erzeugt einen Zeitplan für jeden anderen Tag.</span><span class="sxs-lookup"><span data-stu-id="e4e7d-113">An interval of 2 produces an every-other day schedule.</span></span>

<span data-ttu-id="e4e7d-114">Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird das Intervall für einen täglichen Zeitplan mit dem [**daysinterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="e4e7d-114">When reading or writing your own XML for a task, the interval for a daily schedule is specified using the [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4e7d-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4e7d-115">Requirements</span></span>



| <span data-ttu-id="e4e7d-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4e7d-116">Requirement</span></span> | <span data-ttu-id="e4e7d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e4e7d-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4e7d-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4e7d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e4e7d-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4e7d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e4e7d-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4e7d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e4e7d-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4e7d-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e4e7d-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="e4e7d-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="e4e7d-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e4e7d-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e4e7d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e4e7d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4e7d-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4e7d-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4e7d-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4e7d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4e7d-127">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="e4e7d-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="e4e7d-128">**Dailylöst**</span><span class="sxs-lookup"><span data-stu-id="e4e7d-128">**DailyTrigger**</span></span>](dailytrigger.md)
</dt> </dl>

 

 





