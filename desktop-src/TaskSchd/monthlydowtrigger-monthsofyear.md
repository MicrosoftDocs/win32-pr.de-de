---
title: Monthlydowauslöst. MONTHSOFYEAR (Eigenschaft)
description: Ruft bei der Skripterstellung die Monate des Jahres ab, in denen die Aufgabe ausgeführt wird, oder legt diese fest. | Monthlydowauslöst. MONTHSOFYEAR (Eigenschaft)
ms.assetid: 4ab7ab43-9c9b-4cd3-be8f-1989b83e8cf3
keywords:
- MONTHSOFYEAR-Eigenschaft Taskplaner
- MONTHSOFYEAR-Eigenschaft Taskplaner, monthlydowauslöserobjekt
- Monthlydowauslöserobjekt Taskplaner, MONTHSOFYEAR (Eigenschaft)
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c345cd3de12d7dba3450f62bdb18bfdcee496b13
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869979"
---
# <a name="monthlydowtriggermonthsofyear-property"></a><span data-ttu-id="a01d6-107">Monthlydowauslöst. MONTHSOFYEAR (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a01d6-107">MonthlyDOWTrigger.MonthsOfYear property</span></span>

<span data-ttu-id="a01d6-108">Ruft bei der Skripterstellung die Monate des Jahres ab, in denen die Aufgabe ausgeführt wird, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="a01d6-108">For scripting, gets or sets the months of the year during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="a01d6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a01d6-109">Syntax</span></span>


```VB
MonthlyDOWTrigger.MonthsOfYear As short
```



## <a name="property-value"></a><span data-ttu-id="a01d6-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a01d6-110">Property value</span></span>

<span data-ttu-id="a01d6-111">Eine bitweise Maske, die die Monate des Jahres angibt, in dem die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a01d6-111">A bitwise mask that indicates the months of the year during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="a01d6-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a01d6-112">Remarks</span></span>

<span data-ttu-id="a01d6-113">Die folgende Tabelle zeigt die Zuordnung der bitweisen Maske, die von dieser Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a01d6-113">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="a01d6-114">Monat</span><span class="sxs-lookup"><span data-stu-id="a01d6-114">Month</span></span>     | <span data-ttu-id="a01d6-115">Farbtonwert</span><span class="sxs-lookup"><span data-stu-id="a01d6-115">Hex value</span></span> | <span data-ttu-id="a01d6-116">Dezimalzahl</span><span class="sxs-lookup"><span data-stu-id="a01d6-116">Decimal value</span></span> |
|-----------|-----------|---------------|
| <span data-ttu-id="a01d6-117">January</span><span class="sxs-lookup"><span data-stu-id="a01d6-117">January</span></span>   | <span data-ttu-id="a01d6-118">0X01</span><span class="sxs-lookup"><span data-stu-id="a01d6-118">0X01</span></span>      | <span data-ttu-id="a01d6-119">1</span><span class="sxs-lookup"><span data-stu-id="a01d6-119">1</span></span>             |
| <span data-ttu-id="a01d6-120">Februar</span><span class="sxs-lookup"><span data-stu-id="a01d6-120">February</span></span>  | <span data-ttu-id="a01d6-121">0x02</span><span class="sxs-lookup"><span data-stu-id="a01d6-121">0x02</span></span>      | <span data-ttu-id="a01d6-122">2</span><span class="sxs-lookup"><span data-stu-id="a01d6-122">2</span></span>             |
| <span data-ttu-id="a01d6-123">März</span><span class="sxs-lookup"><span data-stu-id="a01d6-123">March</span></span>     | <span data-ttu-id="a01d6-124">0X04</span><span class="sxs-lookup"><span data-stu-id="a01d6-124">0X04</span></span>      | <span data-ttu-id="a01d6-125">4</span><span class="sxs-lookup"><span data-stu-id="a01d6-125">4</span></span>             |
| <span data-ttu-id="a01d6-126">April</span><span class="sxs-lookup"><span data-stu-id="a01d6-126">April</span></span>     | <span data-ttu-id="a01d6-127">0X08</span><span class="sxs-lookup"><span data-stu-id="a01d6-127">0X08</span></span>      | <span data-ttu-id="a01d6-128">8</span><span class="sxs-lookup"><span data-stu-id="a01d6-128">8</span></span>             |
| <span data-ttu-id="a01d6-129">May</span><span class="sxs-lookup"><span data-stu-id="a01d6-129">May</span></span>       | <span data-ttu-id="a01d6-130">0X10</span><span class="sxs-lookup"><span data-stu-id="a01d6-130">0X10</span></span>      | <span data-ttu-id="a01d6-131">16</span><span class="sxs-lookup"><span data-stu-id="a01d6-131">16</span></span>            |
| <span data-ttu-id="a01d6-132">June</span><span class="sxs-lookup"><span data-stu-id="a01d6-132">June</span></span>      | <span data-ttu-id="a01d6-133">0X20</span><span class="sxs-lookup"><span data-stu-id="a01d6-133">0X20</span></span>      | <span data-ttu-id="a01d6-134">32</span><span class="sxs-lookup"><span data-stu-id="a01d6-134">32</span></span>            |
| <span data-ttu-id="a01d6-135">Juli</span><span class="sxs-lookup"><span data-stu-id="a01d6-135">July</span></span>      | <span data-ttu-id="a01d6-136">0x40</span><span class="sxs-lookup"><span data-stu-id="a01d6-136">0x40</span></span>      | <span data-ttu-id="a01d6-137">64</span><span class="sxs-lookup"><span data-stu-id="a01d6-137">64</span></span>            |
| <span data-ttu-id="a01d6-138">August</span><span class="sxs-lookup"><span data-stu-id="a01d6-138">August</span></span>    | <span data-ttu-id="a01d6-139">0X80</span><span class="sxs-lookup"><span data-stu-id="a01d6-139">0X80</span></span>      | <span data-ttu-id="a01d6-140">128</span><span class="sxs-lookup"><span data-stu-id="a01d6-140">128</span></span>           |
| <span data-ttu-id="a01d6-141">September</span><span class="sxs-lookup"><span data-stu-id="a01d6-141">September</span></span> | <span data-ttu-id="a01d6-142">0X100</span><span class="sxs-lookup"><span data-stu-id="a01d6-142">0X100</span></span>     | <span data-ttu-id="a01d6-143">256</span><span class="sxs-lookup"><span data-stu-id="a01d6-143">256</span></span>           |
| <span data-ttu-id="a01d6-144">Oktober</span><span class="sxs-lookup"><span data-stu-id="a01d6-144">October</span></span>   | <span data-ttu-id="a01d6-145">0X200</span><span class="sxs-lookup"><span data-stu-id="a01d6-145">0X200</span></span>     | <span data-ttu-id="a01d6-146">512</span><span class="sxs-lookup"><span data-stu-id="a01d6-146">512</span></span>           |
| <span data-ttu-id="a01d6-147">November</span><span class="sxs-lookup"><span data-stu-id="a01d6-147">November</span></span>  | <span data-ttu-id="a01d6-148">0X400</span><span class="sxs-lookup"><span data-stu-id="a01d6-148">0X400</span></span>     | <span data-ttu-id="a01d6-149">1024</span><span class="sxs-lookup"><span data-stu-id="a01d6-149">1024</span></span>          |
| <span data-ttu-id="a01d6-150">Dezember</span><span class="sxs-lookup"><span data-stu-id="a01d6-150">December</span></span>  | <span data-ttu-id="a01d6-151">0X800</span><span class="sxs-lookup"><span data-stu-id="a01d6-151">0X800</span></span>     | <span data-ttu-id="a01d6-152">2048</span><span class="sxs-lookup"><span data-stu-id="a01d6-152">2048</span></span>          |



 

<span data-ttu-id="a01d6-153">Beim Lesen oder Schreiben von XML für eine Aufgabe werden die Monate des Jahres eines monatlichen wochentags im Taskplaner Schema durch das [**Monate**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) -Element angegeben.</span><span class="sxs-lookup"><span data-stu-id="a01d6-153">When reading or writing XML for a task, the months of the year of a monthly day-of-week calendar are specified by the [**Months**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="a01d6-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a01d6-154">Requirements</span></span>



| <span data-ttu-id="a01d6-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a01d6-155">Requirement</span></span> | <span data-ttu-id="a01d6-156">Wert</span><span class="sxs-lookup"><span data-stu-id="a01d6-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a01d6-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a01d6-157">Minimum supported client</span></span><br/> | <span data-ttu-id="a01d6-158">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a01d6-158">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a01d6-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a01d6-159">Minimum supported server</span></span><br/> | <span data-ttu-id="a01d6-160">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a01d6-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a01d6-161">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a01d6-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="a01d6-162"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a01d6-162"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a01d6-163">DLL</span><span class="sxs-lookup"><span data-stu-id="a01d6-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a01d6-164"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a01d6-164"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a01d6-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a01d6-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a01d6-166">**Monthlydowlöst**</span><span class="sxs-lookup"><span data-stu-id="a01d6-166">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> <dt>

[<span data-ttu-id="a01d6-167">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="a01d6-167">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





