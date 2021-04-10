---
title: Monthly-Eigenschaft. MONTHSOFYEAR (Eigenschaft)
description: Ruft bei der Skripterstellung die Monate des Jahres ab, in denen die Aufgabe ausgeführt wird, oder legt diese fest. | Monthly-Eigenschaft. MONTHSOFYEAR (Eigenschaft)
ms.assetid: cf26a815-7f4f-4b7a-8db8-a4bd9b77cf49
keywords:
- MONTHSOFYEAR-Eigenschaft Taskplaner
- MONTHSOFYEAR-Eigenschaft Taskplaner, Monthly-Auslöserobjekt
- Monthly-Auslöserobjekt Taskplaner, MONTHSOFYEAR (Eigenschaft)
topic_type:
- apiref
api_name:
- MonthlyTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5683fb1c85e470ca7c82b069929de0351ea7cffe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869879"
---
# <a name="monthlytriggermonthsofyear-property"></a><span data-ttu-id="f3a27-107">Monthly-Eigenschaft. MONTHSOFYEAR (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f3a27-107">MonthlyTrigger.MonthsOfYear property</span></span>

<span data-ttu-id="f3a27-108">Ruft bei der Skripterstellung die Monate des Jahres ab, in denen die Aufgabe ausgeführt wird, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="f3a27-108">For scripting, gets or sets the months of the year during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3a27-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3a27-109">Syntax</span></span>


```VB
MonthlyTrigger.MonthsOfYear As short
```



## <a name="property-value"></a><span data-ttu-id="f3a27-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f3a27-110">Property value</span></span>

<span data-ttu-id="f3a27-111">Eine bitweise Maske, die die Monate des Jahres angibt, in dem die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f3a27-111">A bitwise mask that indicates the months of the year during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3a27-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3a27-112">Remarks</span></span>

<span data-ttu-id="f3a27-113">Die folgende Tabelle zeigt die Zuordnung der bitweisen Maske, die von dieser Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f3a27-113">The following table shows the mapping of the bitwise mask that is used by this property.</span></span>



| <span data-ttu-id="f3a27-114">Monat</span><span class="sxs-lookup"><span data-stu-id="f3a27-114">Month</span></span>     | <span data-ttu-id="f3a27-115">Farbtonwert</span><span class="sxs-lookup"><span data-stu-id="f3a27-115">Hex value</span></span> | <span data-ttu-id="f3a27-116">Dezimalzahl</span><span class="sxs-lookup"><span data-stu-id="f3a27-116">Decimal value</span></span> |
|-----------|-----------|---------------|
| <span data-ttu-id="f3a27-117">January</span><span class="sxs-lookup"><span data-stu-id="f3a27-117">January</span></span>   | <span data-ttu-id="f3a27-118">0X01</span><span class="sxs-lookup"><span data-stu-id="f3a27-118">0X01</span></span>      | <span data-ttu-id="f3a27-119">1</span><span class="sxs-lookup"><span data-stu-id="f3a27-119">1</span></span>             |
| <span data-ttu-id="f3a27-120">Februar</span><span class="sxs-lookup"><span data-stu-id="f3a27-120">February</span></span>  | <span data-ttu-id="f3a27-121">0x02</span><span class="sxs-lookup"><span data-stu-id="f3a27-121">0x02</span></span>      | <span data-ttu-id="f3a27-122">2</span><span class="sxs-lookup"><span data-stu-id="f3a27-122">2</span></span>             |
| <span data-ttu-id="f3a27-123">März</span><span class="sxs-lookup"><span data-stu-id="f3a27-123">March</span></span>     | <span data-ttu-id="f3a27-124">0X04</span><span class="sxs-lookup"><span data-stu-id="f3a27-124">0X04</span></span>      | <span data-ttu-id="f3a27-125">4</span><span class="sxs-lookup"><span data-stu-id="f3a27-125">4</span></span>             |
| <span data-ttu-id="f3a27-126">April</span><span class="sxs-lookup"><span data-stu-id="f3a27-126">April</span></span>     | <span data-ttu-id="f3a27-127">0X08</span><span class="sxs-lookup"><span data-stu-id="f3a27-127">0X08</span></span>      | <span data-ttu-id="f3a27-128">8</span><span class="sxs-lookup"><span data-stu-id="f3a27-128">8</span></span>             |
| <span data-ttu-id="f3a27-129">May</span><span class="sxs-lookup"><span data-stu-id="f3a27-129">May</span></span>       | <span data-ttu-id="f3a27-130">0X10</span><span class="sxs-lookup"><span data-stu-id="f3a27-130">0X10</span></span>      | <span data-ttu-id="f3a27-131">16</span><span class="sxs-lookup"><span data-stu-id="f3a27-131">16</span></span>            |
| <span data-ttu-id="f3a27-132">June</span><span class="sxs-lookup"><span data-stu-id="f3a27-132">June</span></span>      | <span data-ttu-id="f3a27-133">0X20</span><span class="sxs-lookup"><span data-stu-id="f3a27-133">0X20</span></span>      | <span data-ttu-id="f3a27-134">32</span><span class="sxs-lookup"><span data-stu-id="f3a27-134">32</span></span>            |
| <span data-ttu-id="f3a27-135">Juli</span><span class="sxs-lookup"><span data-stu-id="f3a27-135">July</span></span>      | <span data-ttu-id="f3a27-136">0x40</span><span class="sxs-lookup"><span data-stu-id="f3a27-136">0x40</span></span>      | <span data-ttu-id="f3a27-137">64</span><span class="sxs-lookup"><span data-stu-id="f3a27-137">64</span></span>            |
| <span data-ttu-id="f3a27-138">August</span><span class="sxs-lookup"><span data-stu-id="f3a27-138">August</span></span>    | <span data-ttu-id="f3a27-139">0X80</span><span class="sxs-lookup"><span data-stu-id="f3a27-139">0X80</span></span>      | <span data-ttu-id="f3a27-140">128</span><span class="sxs-lookup"><span data-stu-id="f3a27-140">128</span></span>           |
| <span data-ttu-id="f3a27-141">September</span><span class="sxs-lookup"><span data-stu-id="f3a27-141">September</span></span> | <span data-ttu-id="f3a27-142">0X100</span><span class="sxs-lookup"><span data-stu-id="f3a27-142">0X100</span></span>     | <span data-ttu-id="f3a27-143">256</span><span class="sxs-lookup"><span data-stu-id="f3a27-143">256</span></span>           |
| <span data-ttu-id="f3a27-144">Oktober</span><span class="sxs-lookup"><span data-stu-id="f3a27-144">October</span></span>   | <span data-ttu-id="f3a27-145">0X200</span><span class="sxs-lookup"><span data-stu-id="f3a27-145">0X200</span></span>     | <span data-ttu-id="f3a27-146">512</span><span class="sxs-lookup"><span data-stu-id="f3a27-146">512</span></span>           |
| <span data-ttu-id="f3a27-147">November</span><span class="sxs-lookup"><span data-stu-id="f3a27-147">November</span></span>  | <span data-ttu-id="f3a27-148">0X400</span><span class="sxs-lookup"><span data-stu-id="f3a27-148">0X400</span></span>     | <span data-ttu-id="f3a27-149">1024</span><span class="sxs-lookup"><span data-stu-id="f3a27-149">1024</span></span>          |
| <span data-ttu-id="f3a27-150">Dezember</span><span class="sxs-lookup"><span data-stu-id="f3a27-150">December</span></span>  | <span data-ttu-id="f3a27-151">0X800</span><span class="sxs-lookup"><span data-stu-id="f3a27-151">0X800</span></span>     | <span data-ttu-id="f3a27-152">2048</span><span class="sxs-lookup"><span data-stu-id="f3a27-152">2048</span></span>          |



 

<span data-ttu-id="f3a27-153">Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe werden die Monate des Jahres mit dem Element [**Monate**](taskschedulerschema-months-monthlyscheduletype-element.md) des Taskplaner Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="f3a27-153">When reading or writing your own XML for a task, the months of the year are specified using the [**Months**](taskschedulerschema-months-monthlyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3a27-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3a27-154">Requirements</span></span>



| <span data-ttu-id="f3a27-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3a27-155">Requirement</span></span> | <span data-ttu-id="f3a27-156">Wert</span><span class="sxs-lookup"><span data-stu-id="f3a27-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a27-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3a27-157">Minimum supported client</span></span><br/> | <span data-ttu-id="f3a27-158">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3a27-158">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f3a27-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3a27-159">Minimum supported server</span></span><br/> | <span data-ttu-id="f3a27-160">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3a27-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f3a27-161">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f3a27-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="f3a27-162"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f3a27-162"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f3a27-163">DLL</span><span class="sxs-lookup"><span data-stu-id="f3a27-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3a27-164"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3a27-164"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3a27-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3a27-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3a27-166">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="f3a27-166">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="f3a27-167">**Monthly-auslöst**</span><span class="sxs-lookup"><span data-stu-id="f3a27-167">**MonthlyTrigger**</span></span>](monthlytrigger.md)
</dt> </dl>

 

 





