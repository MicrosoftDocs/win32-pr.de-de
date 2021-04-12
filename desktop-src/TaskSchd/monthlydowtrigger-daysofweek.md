---
title: Monthlydowauslöst. DaysOfWeek (Eigenschaft)
description: Ruft bei der Skripterstellung die Wochentage ab, an denen die Aufgabe ausgeführt wird, oder legt diese fest.
ms.assetid: dd9b2463-69a1-4e77-a8f7-26b186d3d02d
keywords:
- DaysOfWeek-Eigenschaft Taskplaner
- DaysOfWeek-Eigenschaft Taskplaner, monthlydowauslöserobjekt
- Monthlydowauslöserobjekt Taskplaner, DaysOfWeek (Eigenschaft)
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15344650dabdec2bcbacf91397b37b97ce3f0772
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478417"
---
# <a name="monthlydowtriggerdaysofweek-property"></a><span data-ttu-id="0e905-106">Monthlydowauslöst. DaysOfWeek (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0e905-106">MonthlyDOWTrigger.DaysOfWeek property</span></span>

<span data-ttu-id="0e905-107">Ruft bei der Skripterstellung die Wochentage ab, an denen die Aufgabe ausgeführt wird, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="0e905-107">For scripting, gets or sets the days of the week during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e905-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e905-108">Syntax</span></span>


```VB
MonthlyDOWTrigger.DaysOfWeek As short
```



## <a name="property-value"></a><span data-ttu-id="0e905-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0e905-109">Property value</span></span>

<span data-ttu-id="0e905-110">Eine bitweise Maske, die die Wochentage angibt, an denen die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0e905-110">A bitwise mask that indicates the days of the week during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e905-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e905-111">Remarks</span></span>

<span data-ttu-id="0e905-112">Die folgende Tabelle zeigt die Zuordnung der bitweisen Maske, die von dieser Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0e905-112">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="0e905-113">Tag der Woche</span><span class="sxs-lookup"><span data-stu-id="0e905-113">Day of Week</span></span> | <span data-ttu-id="0e905-114">Hexadezimalwert</span><span class="sxs-lookup"><span data-stu-id="0e905-114">Hex Value</span></span> | <span data-ttu-id="0e905-115">Dezimalwert</span><span class="sxs-lookup"><span data-stu-id="0e905-115">Decimal Value</span></span> |
|-------------|-----------|---------------|
| <span data-ttu-id="0e905-116">Sonntag</span><span class="sxs-lookup"><span data-stu-id="0e905-116">Sunday</span></span>      | <span data-ttu-id="0e905-117">0x01</span><span class="sxs-lookup"><span data-stu-id="0e905-117">0x01</span></span>      | <span data-ttu-id="0e905-118">1</span><span class="sxs-lookup"><span data-stu-id="0e905-118">1</span></span>             |
| <span data-ttu-id="0e905-119">Montag</span><span class="sxs-lookup"><span data-stu-id="0e905-119">Monday</span></span>      | <span data-ttu-id="0e905-120">0x02</span><span class="sxs-lookup"><span data-stu-id="0e905-120">0x02</span></span>      | <span data-ttu-id="0e905-121">2</span><span class="sxs-lookup"><span data-stu-id="0e905-121">2</span></span>             |
| <span data-ttu-id="0e905-122">Tuesday</span><span class="sxs-lookup"><span data-stu-id="0e905-122">Tuesday</span></span>     | <span data-ttu-id="0e905-123">0x04</span><span class="sxs-lookup"><span data-stu-id="0e905-123">0x04</span></span>      | <span data-ttu-id="0e905-124">4</span><span class="sxs-lookup"><span data-stu-id="0e905-124">4</span></span>             |
| <span data-ttu-id="0e905-125">Wednesday</span><span class="sxs-lookup"><span data-stu-id="0e905-125">Wednesday</span></span>   | <span data-ttu-id="0e905-126">0x08</span><span class="sxs-lookup"><span data-stu-id="0e905-126">0x08</span></span>      | <span data-ttu-id="0e905-127">8</span><span class="sxs-lookup"><span data-stu-id="0e905-127">8</span></span>             |
| <span data-ttu-id="0e905-128">Thursday</span><span class="sxs-lookup"><span data-stu-id="0e905-128">Thursday</span></span>    | <span data-ttu-id="0e905-129">0x10</span><span class="sxs-lookup"><span data-stu-id="0e905-129">0x10</span></span>      | <span data-ttu-id="0e905-130">16</span><span class="sxs-lookup"><span data-stu-id="0e905-130">16</span></span>            |
| <span data-ttu-id="0e905-131">Freitag</span><span class="sxs-lookup"><span data-stu-id="0e905-131">Friday</span></span>      | <span data-ttu-id="0e905-132">0x20</span><span class="sxs-lookup"><span data-stu-id="0e905-132">0x20</span></span>      | <span data-ttu-id="0e905-133">32</span><span class="sxs-lookup"><span data-stu-id="0e905-133">32</span></span>            |
| <span data-ttu-id="0e905-134">Samstag</span><span class="sxs-lookup"><span data-stu-id="0e905-134">Saturday</span></span>    | <span data-ttu-id="0e905-135">0x40</span><span class="sxs-lookup"><span data-stu-id="0e905-135">0x40</span></span>      | <span data-ttu-id="0e905-136">64</span><span class="sxs-lookup"><span data-stu-id="0e905-136">64</span></span>            |



 

<span data-ttu-id="0e905-137">Beim Lesen oder Schreiben von XML für eine Aufgabe werden die Wochentage eines monatlichen wochentags mit dem [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) -Element angegeben.</span><span class="sxs-lookup"><span data-stu-id="0e905-137">When reading or writing XML for a task, the days of the week of a monthly day-of-week calendar are specified by the [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e905-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e905-138">Requirements</span></span>



| <span data-ttu-id="0e905-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e905-139">Requirement</span></span> | <span data-ttu-id="0e905-140">Wert</span><span class="sxs-lookup"><span data-stu-id="0e905-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e905-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0e905-141">Minimum supported client</span></span><br/> | <span data-ttu-id="0e905-142">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e905-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0e905-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0e905-143">Minimum supported server</span></span><br/> | <span data-ttu-id="0e905-144">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e905-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0e905-145">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="0e905-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="0e905-146"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0e905-146"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0e905-147">DLL</span><span class="sxs-lookup"><span data-stu-id="0e905-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e905-148"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e905-148"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e905-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e905-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e905-150">**Monthlydowlöst**</span><span class="sxs-lookup"><span data-stu-id="0e905-150">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> <dt>

[<span data-ttu-id="0e905-151">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="0e905-151">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





