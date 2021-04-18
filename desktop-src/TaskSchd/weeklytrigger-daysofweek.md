---
title: Weeklyauslöst. DaysOfWeek (Eigenschaft)
description: Ruft bei der Skripterstellung die Wochentage ab, an denen der Task ausgeführt wird, oder legt diese fest.
ms.assetid: 79f279d4-d6d2-428b-bbed-226e4eaaefb6
keywords:
- DaysOfWeek-Eigenschaft Taskplaner
- DaysOfWeek-Eigenschaft Taskplaner, weeklyauslöserobjekt
- Weeklyauslöserobjekt Taskplaner, DaysOfWeek (Eigenschaft)
topic_type:
- apiref
api_name:
- WeeklyTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f0a27ef031e7baf46d2d3c0e33c23fb505c7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519255"
---
# <a name="weeklytriggerdaysofweek-property"></a><span data-ttu-id="ca28a-106">Weeklyauslöst. DaysOfWeek (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ca28a-106">WeeklyTrigger.DaysOfWeek property</span></span>

<span data-ttu-id="ca28a-107">Ruft bei der Skripterstellung die Wochentage ab, an denen der Task ausgeführt wird, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="ca28a-107">For scripting, gets or sets the days of the week on which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca28a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca28a-108">Syntax</span></span>


```VB
WeeklyTrigger.DaysOfWeek As short
```



## <a name="property-value"></a><span data-ttu-id="ca28a-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ca28a-109">Property value</span></span>

<span data-ttu-id="ca28a-110">Eine bitweise Maske, die die Wochentage angibt, an denen die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca28a-110">A bitwise mask that indicates the days of the week on which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca28a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca28a-111">Remarks</span></span>

<span data-ttu-id="ca28a-112">Die folgende Tabelle zeigt die Zuordnung der bitweisen Maske, die von dieser Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ca28a-112">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="ca28a-113">Monat</span><span class="sxs-lookup"><span data-stu-id="ca28a-113">Month</span></span>     | <span data-ttu-id="ca28a-114">Farbtonwert</span><span class="sxs-lookup"><span data-stu-id="ca28a-114">Hex value</span></span> | <span data-ttu-id="ca28a-115">Dezimalzahl</span><span class="sxs-lookup"><span data-stu-id="ca28a-115">Decimal value</span></span> |
|-----------|-----------|---------------|
| <span data-ttu-id="ca28a-116">Sonntag</span><span class="sxs-lookup"><span data-stu-id="ca28a-116">Sunday</span></span>    | <span data-ttu-id="ca28a-117">0X01</span><span class="sxs-lookup"><span data-stu-id="ca28a-117">0X01</span></span>      | <span data-ttu-id="ca28a-118">1</span><span class="sxs-lookup"><span data-stu-id="ca28a-118">1</span></span>             |
| <span data-ttu-id="ca28a-119">Montag</span><span class="sxs-lookup"><span data-stu-id="ca28a-119">Monday</span></span>    | <span data-ttu-id="ca28a-120">0x02</span><span class="sxs-lookup"><span data-stu-id="ca28a-120">0x02</span></span>      | <span data-ttu-id="ca28a-121">2</span><span class="sxs-lookup"><span data-stu-id="ca28a-121">2</span></span>             |
| <span data-ttu-id="ca28a-122">Tuesday</span><span class="sxs-lookup"><span data-stu-id="ca28a-122">Tuesday</span></span>   | <span data-ttu-id="ca28a-123">0X04</span><span class="sxs-lookup"><span data-stu-id="ca28a-123">0X04</span></span>      | <span data-ttu-id="ca28a-124">4</span><span class="sxs-lookup"><span data-stu-id="ca28a-124">4</span></span>             |
| <span data-ttu-id="ca28a-125">Wednesday</span><span class="sxs-lookup"><span data-stu-id="ca28a-125">Wednesday</span></span> | <span data-ttu-id="ca28a-126">0X08</span><span class="sxs-lookup"><span data-stu-id="ca28a-126">0X08</span></span>      | <span data-ttu-id="ca28a-127">8</span><span class="sxs-lookup"><span data-stu-id="ca28a-127">8</span></span>             |
| <span data-ttu-id="ca28a-128">Thursday</span><span class="sxs-lookup"><span data-stu-id="ca28a-128">Thursday</span></span>  | <span data-ttu-id="ca28a-129">0X10</span><span class="sxs-lookup"><span data-stu-id="ca28a-129">0X10</span></span>      | <span data-ttu-id="ca28a-130">16</span><span class="sxs-lookup"><span data-stu-id="ca28a-130">16</span></span>            |
| <span data-ttu-id="ca28a-131">Freitag</span><span class="sxs-lookup"><span data-stu-id="ca28a-131">Friday</span></span>    | <span data-ttu-id="ca28a-132">0x20</span><span class="sxs-lookup"><span data-stu-id="ca28a-132">0x20</span></span>      | <span data-ttu-id="ca28a-133">32</span><span class="sxs-lookup"><span data-stu-id="ca28a-133">32</span></span>            |
| <span data-ttu-id="ca28a-134">Samstag</span><span class="sxs-lookup"><span data-stu-id="ca28a-134">Saturday</span></span>  | <span data-ttu-id="ca28a-135">0X40</span><span class="sxs-lookup"><span data-stu-id="ca28a-135">0X40</span></span>      | <span data-ttu-id="ca28a-136">64</span><span class="sxs-lookup"><span data-stu-id="ca28a-136">64</span></span>            |



 

<span data-ttu-id="ca28a-137">Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe werden die Wochentage mit dem [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="ca28a-137">When reading or writing your own XML for a task, the days of the week are specified using the [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca28a-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca28a-138">Requirements</span></span>



| <span data-ttu-id="ca28a-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca28a-139">Requirement</span></span> | <span data-ttu-id="ca28a-140">Wert</span><span class="sxs-lookup"><span data-stu-id="ca28a-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca28a-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ca28a-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ca28a-142">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca28a-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ca28a-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ca28a-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ca28a-144">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca28a-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ca28a-145">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ca28a-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="ca28a-146"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ca28a-146"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ca28a-147">DLL</span><span class="sxs-lookup"><span data-stu-id="ca28a-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca28a-148"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca28a-148"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca28a-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca28a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca28a-150">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="ca28a-150">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





