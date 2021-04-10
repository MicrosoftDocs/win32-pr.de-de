---
title: Monthly-Eigenschaft. daysOfMonth (Eigenschaft)
description: Ruft bei der Skripterstellung die Tage des Monats ab, in denen die Aufgabe ausgeführt wird, oder legt diese fest.
ms.assetid: 4da80d0f-ae0c-4e56-b51b-6ee6ab309d7c
keywords:
- DaysOfMonth-Eigenschaft Taskplaner
- DaysOfMonth-Eigenschaft Taskplaner, Monthly-Auslöserobjekt
- Monthly-Auslöserobjekt Taskplaner, daysOfMonth (Eigenschaft)
topic_type:
- apiref
api_name:
- MonthlyTrigger.DaysOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81a3bd671266cfbe459218367fadf20fd52f94a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104360"
---
# <a name="monthlytriggerdaysofmonth-property"></a><span data-ttu-id="b77d0-106">Monthly-Eigenschaft. daysOfMonth (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b77d0-106">MonthlyTrigger.DaysOfMonth property</span></span>

<span data-ttu-id="b77d0-107">Ruft bei der Skripterstellung die Tage des Monats ab, in denen die Aufgabe ausgeführt wird, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="b77d0-107">For scripting, gets or sets the days of the month during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="b77d0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b77d0-108">Syntax</span></span>


```VB
MonthlyTrigger.DaysOfMonth As long
```



## <a name="property-value"></a><span data-ttu-id="b77d0-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b77d0-109">Property value</span></span>

<span data-ttu-id="b77d0-110">Eine bitweise Maske, die die Tage des Monats angibt, in denen die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b77d0-110">A bitwise mask that indicates the days of the month during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="b77d0-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b77d0-111">Remarks</span></span>



| <span data-ttu-id="b77d0-112">Tag des Monats</span><span class="sxs-lookup"><span data-stu-id="b77d0-112">Day of month</span></span> | <span data-ttu-id="b77d0-113">Farbtonwert</span><span class="sxs-lookup"><span data-stu-id="b77d0-113">Hex value</span></span>  | <span data-ttu-id="b77d0-114">Dezimalzahl</span><span class="sxs-lookup"><span data-stu-id="b77d0-114">Decimal value</span></span> |
|--------------|------------|---------------|
| <span data-ttu-id="b77d0-115">1</span><span class="sxs-lookup"><span data-stu-id="b77d0-115">1</span></span>            | <span data-ttu-id="b77d0-116">0x01</span><span class="sxs-lookup"><span data-stu-id="b77d0-116">0x01</span></span>       | <span data-ttu-id="b77d0-117">1</span><span class="sxs-lookup"><span data-stu-id="b77d0-117">1</span></span>             |
| <span data-ttu-id="b77d0-118">2</span><span class="sxs-lookup"><span data-stu-id="b77d0-118">2</span></span>            | <span data-ttu-id="b77d0-119">0x02</span><span class="sxs-lookup"><span data-stu-id="b77d0-119">0x02</span></span>       | <span data-ttu-id="b77d0-120">2</span><span class="sxs-lookup"><span data-stu-id="b77d0-120">2</span></span>             |
| <span data-ttu-id="b77d0-121">3</span><span class="sxs-lookup"><span data-stu-id="b77d0-121">3</span></span>            | <span data-ttu-id="b77d0-122">0x04</span><span class="sxs-lookup"><span data-stu-id="b77d0-122">0x04</span></span>       | <span data-ttu-id="b77d0-123">4</span><span class="sxs-lookup"><span data-stu-id="b77d0-123">4</span></span>             |
| <span data-ttu-id="b77d0-124">4</span><span class="sxs-lookup"><span data-stu-id="b77d0-124">4</span></span>            | <span data-ttu-id="b77d0-125">0x08</span><span class="sxs-lookup"><span data-stu-id="b77d0-125">0x08</span></span>       | <span data-ttu-id="b77d0-126">8</span><span class="sxs-lookup"><span data-stu-id="b77d0-126">8</span></span>             |
| <span data-ttu-id="b77d0-127">5</span><span class="sxs-lookup"><span data-stu-id="b77d0-127">5</span></span>            | <span data-ttu-id="b77d0-128">0x10</span><span class="sxs-lookup"><span data-stu-id="b77d0-128">0x10</span></span>       | <span data-ttu-id="b77d0-129">16</span><span class="sxs-lookup"><span data-stu-id="b77d0-129">16</span></span>            |
| <span data-ttu-id="b77d0-130">6</span><span class="sxs-lookup"><span data-stu-id="b77d0-130">6</span></span>            | <span data-ttu-id="b77d0-131">0x20</span><span class="sxs-lookup"><span data-stu-id="b77d0-131">0x20</span></span>       | <span data-ttu-id="b77d0-132">32</span><span class="sxs-lookup"><span data-stu-id="b77d0-132">32</span></span>            |
| <span data-ttu-id="b77d0-133">7</span><span class="sxs-lookup"><span data-stu-id="b77d0-133">7</span></span>            | <span data-ttu-id="b77d0-134">0x40</span><span class="sxs-lookup"><span data-stu-id="b77d0-134">0x40</span></span>       | <span data-ttu-id="b77d0-135">64</span><span class="sxs-lookup"><span data-stu-id="b77d0-135">64</span></span>            |
| <span data-ttu-id="b77d0-136">8</span><span class="sxs-lookup"><span data-stu-id="b77d0-136">8</span></span>            | <span data-ttu-id="b77d0-137">0x80</span><span class="sxs-lookup"><span data-stu-id="b77d0-137">0x80</span></span>       | <span data-ttu-id="b77d0-138">128</span><span class="sxs-lookup"><span data-stu-id="b77d0-138">128</span></span>           |
| <span data-ttu-id="b77d0-139">9</span><span class="sxs-lookup"><span data-stu-id="b77d0-139">9</span></span>            | <span data-ttu-id="b77d0-140">0x100</span><span class="sxs-lookup"><span data-stu-id="b77d0-140">0x100</span></span>      | <span data-ttu-id="b77d0-141">256</span><span class="sxs-lookup"><span data-stu-id="b77d0-141">256</span></span>           |
| <span data-ttu-id="b77d0-142">10</span><span class="sxs-lookup"><span data-stu-id="b77d0-142">10</span></span>           | <span data-ttu-id="b77d0-143">0x200</span><span class="sxs-lookup"><span data-stu-id="b77d0-143">0x200</span></span>      | <span data-ttu-id="b77d0-144">512</span><span class="sxs-lookup"><span data-stu-id="b77d0-144">512</span></span>           |
| <span data-ttu-id="b77d0-145">11</span><span class="sxs-lookup"><span data-stu-id="b77d0-145">11</span></span>           | <span data-ttu-id="b77d0-146">0x400</span><span class="sxs-lookup"><span data-stu-id="b77d0-146">0x400</span></span>      | <span data-ttu-id="b77d0-147">1024</span><span class="sxs-lookup"><span data-stu-id="b77d0-147">1024</span></span>          |
| <span data-ttu-id="b77d0-148">12</span><span class="sxs-lookup"><span data-stu-id="b77d0-148">12</span></span>           | <span data-ttu-id="b77d0-149">0x800</span><span class="sxs-lookup"><span data-stu-id="b77d0-149">0x800</span></span>      | <span data-ttu-id="b77d0-150">2048</span><span class="sxs-lookup"><span data-stu-id="b77d0-150">2048</span></span>          |
| <span data-ttu-id="b77d0-151">13</span><span class="sxs-lookup"><span data-stu-id="b77d0-151">13</span></span>           | <span data-ttu-id="b77d0-152">0x1000</span><span class="sxs-lookup"><span data-stu-id="b77d0-152">0x1000</span></span>     | <span data-ttu-id="b77d0-153">4096</span><span class="sxs-lookup"><span data-stu-id="b77d0-153">4096</span></span>          |
| <span data-ttu-id="b77d0-154">14</span><span class="sxs-lookup"><span data-stu-id="b77d0-154">14</span></span>           | <span data-ttu-id="b77d0-155">0x2000</span><span class="sxs-lookup"><span data-stu-id="b77d0-155">0x2000</span></span>     | <span data-ttu-id="b77d0-156">8192</span><span class="sxs-lookup"><span data-stu-id="b77d0-156">8192</span></span>          |
| <span data-ttu-id="b77d0-157">15</span><span class="sxs-lookup"><span data-stu-id="b77d0-157">15</span></span>           | <span data-ttu-id="b77d0-158">0x4000</span><span class="sxs-lookup"><span data-stu-id="b77d0-158">0x4000</span></span>     | <span data-ttu-id="b77d0-159">16384</span><span class="sxs-lookup"><span data-stu-id="b77d0-159">16384</span></span>         |
| <span data-ttu-id="b77d0-160">16</span><span class="sxs-lookup"><span data-stu-id="b77d0-160">16</span></span>           | <span data-ttu-id="b77d0-161">0x8000</span><span class="sxs-lookup"><span data-stu-id="b77d0-161">0x8000</span></span>     | <span data-ttu-id="b77d0-162">32768</span><span class="sxs-lookup"><span data-stu-id="b77d0-162">32768</span></span>         |
| <span data-ttu-id="b77d0-163">17</span><span class="sxs-lookup"><span data-stu-id="b77d0-163">17</span></span>           | <span data-ttu-id="b77d0-164">0x10000</span><span class="sxs-lookup"><span data-stu-id="b77d0-164">0x10000</span></span>    | <span data-ttu-id="b77d0-165">65536</span><span class="sxs-lookup"><span data-stu-id="b77d0-165">65536</span></span>         |
| <span data-ttu-id="b77d0-166">18</span><span class="sxs-lookup"><span data-stu-id="b77d0-166">18</span></span>           | <span data-ttu-id="b77d0-167">0x20000</span><span class="sxs-lookup"><span data-stu-id="b77d0-167">0x20000</span></span>    | <span data-ttu-id="b77d0-168">131072</span><span class="sxs-lookup"><span data-stu-id="b77d0-168">131072</span></span>        |
| <span data-ttu-id="b77d0-169">19</span><span class="sxs-lookup"><span data-stu-id="b77d0-169">19</span></span>           | <span data-ttu-id="b77d0-170">0x40000</span><span class="sxs-lookup"><span data-stu-id="b77d0-170">0x40000</span></span>    | <span data-ttu-id="b77d0-171">262144</span><span class="sxs-lookup"><span data-stu-id="b77d0-171">262144</span></span>        |
| <span data-ttu-id="b77d0-172">20</span><span class="sxs-lookup"><span data-stu-id="b77d0-172">20</span></span>           | <span data-ttu-id="b77d0-173">0x80000</span><span class="sxs-lookup"><span data-stu-id="b77d0-173">0x80000</span></span>    | <span data-ttu-id="b77d0-174">524288</span><span class="sxs-lookup"><span data-stu-id="b77d0-174">524288</span></span>        |
| <span data-ttu-id="b77d0-175">21</span><span class="sxs-lookup"><span data-stu-id="b77d0-175">21</span></span>           | <span data-ttu-id="b77d0-176">0x100000</span><span class="sxs-lookup"><span data-stu-id="b77d0-176">0x100000</span></span>   | <span data-ttu-id="b77d0-177">1048576</span><span class="sxs-lookup"><span data-stu-id="b77d0-177">1048576</span></span>       |
| <span data-ttu-id="b77d0-178">22</span><span class="sxs-lookup"><span data-stu-id="b77d0-178">22</span></span>           | <span data-ttu-id="b77d0-179">0x200000</span><span class="sxs-lookup"><span data-stu-id="b77d0-179">0x200000</span></span>   | <span data-ttu-id="b77d0-180">2097152</span><span class="sxs-lookup"><span data-stu-id="b77d0-180">2097152</span></span>       |
| <span data-ttu-id="b77d0-181">23</span><span class="sxs-lookup"><span data-stu-id="b77d0-181">23</span></span>           | <span data-ttu-id="b77d0-182">0x400000</span><span class="sxs-lookup"><span data-stu-id="b77d0-182">0x400000</span></span>   | <span data-ttu-id="b77d0-183">4194304</span><span class="sxs-lookup"><span data-stu-id="b77d0-183">4194304</span></span>       |
| <span data-ttu-id="b77d0-184">24</span><span class="sxs-lookup"><span data-stu-id="b77d0-184">24</span></span>           | <span data-ttu-id="b77d0-185">0x800000</span><span class="sxs-lookup"><span data-stu-id="b77d0-185">0x800000</span></span>   | <span data-ttu-id="b77d0-186">8388608</span><span class="sxs-lookup"><span data-stu-id="b77d0-186">8388608</span></span>       |
| <span data-ttu-id="b77d0-187">25</span><span class="sxs-lookup"><span data-stu-id="b77d0-187">25</span></span>           | <span data-ttu-id="b77d0-188">0x1000000</span><span class="sxs-lookup"><span data-stu-id="b77d0-188">0x1000000</span></span>  | <span data-ttu-id="b77d0-189">16777216</span><span class="sxs-lookup"><span data-stu-id="b77d0-189">16777216</span></span>      |
| <span data-ttu-id="b77d0-190">26</span><span class="sxs-lookup"><span data-stu-id="b77d0-190">26</span></span>           | <span data-ttu-id="b77d0-191">0x2000000</span><span class="sxs-lookup"><span data-stu-id="b77d0-191">0x2000000</span></span>  | <span data-ttu-id="b77d0-192">33554432</span><span class="sxs-lookup"><span data-stu-id="b77d0-192">33554432</span></span>      |
| <span data-ttu-id="b77d0-193">27</span><span class="sxs-lookup"><span data-stu-id="b77d0-193">27</span></span>           | <span data-ttu-id="b77d0-194">0x4000000</span><span class="sxs-lookup"><span data-stu-id="b77d0-194">0x4000000</span></span>  | <span data-ttu-id="b77d0-195">67108864</span><span class="sxs-lookup"><span data-stu-id="b77d0-195">67108864</span></span>      |
| <span data-ttu-id="b77d0-196">28</span><span class="sxs-lookup"><span data-stu-id="b77d0-196">28</span></span>           | <span data-ttu-id="b77d0-197">0x8000000</span><span class="sxs-lookup"><span data-stu-id="b77d0-197">0x8000000</span></span>  | <span data-ttu-id="b77d0-198">134217728</span><span class="sxs-lookup"><span data-stu-id="b77d0-198">134217728</span></span>     |
| <span data-ttu-id="b77d0-199">29</span><span class="sxs-lookup"><span data-stu-id="b77d0-199">29</span></span>           | <span data-ttu-id="b77d0-200">0x10000000</span><span class="sxs-lookup"><span data-stu-id="b77d0-200">0x10000000</span></span> | <span data-ttu-id="b77d0-201">268435456</span><span class="sxs-lookup"><span data-stu-id="b77d0-201">268435456</span></span>     |
| <span data-ttu-id="b77d0-202">30</span><span class="sxs-lookup"><span data-stu-id="b77d0-202">30</span></span>           | <span data-ttu-id="b77d0-203">0x20000000</span><span class="sxs-lookup"><span data-stu-id="b77d0-203">0x20000000</span></span> | <span data-ttu-id="b77d0-204">536870912</span><span class="sxs-lookup"><span data-stu-id="b77d0-204">536870912</span></span>     |
| <span data-ttu-id="b77d0-205">31</span><span class="sxs-lookup"><span data-stu-id="b77d0-205">31</span></span>           | <span data-ttu-id="b77d0-206">0x40000000</span><span class="sxs-lookup"><span data-stu-id="b77d0-206">0x40000000</span></span> | <span data-ttu-id="b77d0-207">1073741824</span><span class="sxs-lookup"><span data-stu-id="b77d0-207">1073741824</span></span>    |
| <span data-ttu-id="b77d0-208">Letzter</span><span class="sxs-lookup"><span data-stu-id="b77d0-208">Last</span></span>         | <span data-ttu-id="b77d0-209">0x80000000</span><span class="sxs-lookup"><span data-stu-id="b77d0-209">0x80000000</span></span> | <span data-ttu-id="b77d0-210">2147483648</span><span class="sxs-lookup"><span data-stu-id="b77d0-210">2147483648</span></span>    |



 

<span data-ttu-id="b77d0-211">Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe werden die Tage des Monats mit dem [**daysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="b77d0-211">When reading or writing your own XML for a task, the days of the month are specified using the [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="b77d0-212">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b77d0-212">Requirements</span></span>



| <span data-ttu-id="b77d0-213">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b77d0-213">Requirement</span></span> | <span data-ttu-id="b77d0-214">Wert</span><span class="sxs-lookup"><span data-stu-id="b77d0-214">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b77d0-215">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b77d0-215">Minimum supported client</span></span><br/> | <span data-ttu-id="b77d0-216">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b77d0-216">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b77d0-217">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b77d0-217">Minimum supported server</span></span><br/> | <span data-ttu-id="b77d0-218">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b77d0-218">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b77d0-219">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b77d0-219">Type library</span></span><br/>             | <dl> <span data-ttu-id="b77d0-220"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b77d0-220"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b77d0-221">DLL</span><span class="sxs-lookup"><span data-stu-id="b77d0-221">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b77d0-222"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b77d0-222"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b77d0-223">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b77d0-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b77d0-224">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="b77d0-224">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="b77d0-225">**Monthly-auslöst**</span><span class="sxs-lookup"><span data-stu-id="b77d0-225">**MonthlyTrigger**</span></span>](monthlytrigger.md)
</dt> </dl>

 

 





