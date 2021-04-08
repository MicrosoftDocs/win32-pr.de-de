---
title: FRS-Replikat-Set-type-Attribut
description: Dies ist ein Code, der angibt, ob es sich um eine SYSVOL-Replikat Gruppe, eine DFS-Replikat Gruppe oder eine andere Replikat
ms.assetid: 687a854f-ffa1-41f4-a515-5224759696ab
ms.tgt_platform: multiple
keywords:
- AD-Schema für FRS-Replikat-Set-Type
- frsreplicasettype-Attribut AD-Schema
topic_type:
- apiref
api_name:
- FRS-Replica-Set-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18046c9b4edb794687d275af52e35416419c7e2d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859438"
---
# <a name="frs-replica-set-type-attribute"></a><span data-ttu-id="c1230-105">FRS-Replikat-Set-type-Attribut</span><span class="sxs-lookup"><span data-stu-id="c1230-105">FRS-Replica-Set-Type attribute</span></span>

<span data-ttu-id="c1230-106">Dies ist ein Code, der angibt, ob es sich um eine SYSVOL-Replikat Gruppe, eine DFS-Replikat Gruppe oder eine andere Replikat</span><span class="sxs-lookup"><span data-stu-id="c1230-106">This is a code that indicates whether this is a sysvol replica set, a DFS replica set, or other replica set.</span></span>



| <span data-ttu-id="c1230-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c1230-107">Entry</span></span> | <span data-ttu-id="c1230-108">Wert</span><span class="sxs-lookup"><span data-stu-id="c1230-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c1230-109">CN</span><span class="sxs-lookup"><span data-stu-id="c1230-109">CN</span></span>                | <span data-ttu-id="c1230-110">FRS-Replikat-Set-Type</span><span class="sxs-lookup"><span data-stu-id="c1230-110">FRS-Replica-Set-Type</span></span>                 |
| <span data-ttu-id="c1230-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c1230-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c1230-112">frsreplicasettype</span><span class="sxs-lookup"><span data-stu-id="c1230-112">fRSReplicaSetType</span></span>                    |
| <span data-ttu-id="c1230-113">Size</span><span class="sxs-lookup"><span data-stu-id="c1230-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="c1230-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c1230-114">Update Privilege</span></span>  | <span data-ttu-id="c1230-115">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c1230-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="c1230-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="c1230-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c1230-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c1230-117">Attribute-Id</span></span>      | <span data-ttu-id="c1230-118">1.2.840.113556.1.4.31</span><span class="sxs-lookup"><span data-stu-id="c1230-118">1.2.840.113556.1.4.31</span></span>                |
| <span data-ttu-id="c1230-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c1230-119">System-Id-Guid</span></span>    | <span data-ttu-id="c1230-120">26d9736b-6070-11d1-a9c6-0000t80367c1</span><span class="sxs-lookup"><span data-stu-id="c1230-120">26d9736b-6070-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="c1230-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1230-121">Syntax</span></span>            | [<span data-ttu-id="c1230-122">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="c1230-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="c1230-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="c1230-123">Implementations</span></span>

-   [<span data-ttu-id="c1230-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c1230-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c1230-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c1230-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c1230-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c1230-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c1230-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c1230-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c1230-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c1230-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c1230-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c1230-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c1230-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c1230-130">Windows 2000 Server</span></span>



| <span data-ttu-id="c1230-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c1230-131">Entry</span></span> | <span data-ttu-id="c1230-132">Wert</span><span class="sxs-lookup"><span data-stu-id="c1230-132">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c1230-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c1230-133">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c1230-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1230-134">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c1230-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1230-135">System-Only</span></span>            | <span data-ttu-id="c1230-136">False</span><span class="sxs-lookup"><span data-stu-id="c1230-136">False</span></span>                                                     |
| <span data-ttu-id="c1230-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c1230-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c1230-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="c1230-138">True</span></span>                                                      |
| <span data-ttu-id="c1230-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c1230-139">Is Indexed</span></span>             | <span data-ttu-id="c1230-140">False</span><span class="sxs-lookup"><span data-stu-id="c1230-140">False</span></span>                                                     |
| <span data-ttu-id="c1230-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c1230-141">In Global Catalog</span></span>      | <span data-ttu-id="c1230-142">False</span><span class="sxs-lookup"><span data-stu-id="c1230-142">False</span></span>                                                     |
| <span data-ttu-id="c1230-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c1230-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1230-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c1230-144">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c1230-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1230-145">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c1230-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1230-146">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c1230-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1230-147">Search-Flags</span></span>           | <span data-ttu-id="c1230-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1230-148">0x00000000</span></span>                                                |
| <span data-ttu-id="c1230-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1230-149">System-Flags</span></span>           | <span data-ttu-id="c1230-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1230-150">0x00000010</span></span>                                                |
| <span data-ttu-id="c1230-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c1230-151">Classes used in</span></span>        | [<span data-ttu-id="c1230-152">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="c1230-152">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c1230-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c1230-153">Windows Server 2003</span></span>



| <span data-ttu-id="c1230-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c1230-154">Entry</span></span> | <span data-ttu-id="c1230-155">Wert</span><span class="sxs-lookup"><span data-stu-id="c1230-155">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c1230-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c1230-156">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c1230-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1230-157">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c1230-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1230-158">System-Only</span></span>            | <span data-ttu-id="c1230-159">False</span><span class="sxs-lookup"><span data-stu-id="c1230-159">False</span></span>                                                     |
| <span data-ttu-id="c1230-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c1230-160">Is-Single-Valued</span></span>       | <span data-ttu-id="c1230-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="c1230-161">True</span></span>                                                      |
| <span data-ttu-id="c1230-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c1230-162">Is Indexed</span></span>             | <span data-ttu-id="c1230-163">False</span><span class="sxs-lookup"><span data-stu-id="c1230-163">False</span></span>                                                     |
| <span data-ttu-id="c1230-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c1230-164">In Global Catalog</span></span>      | <span data-ttu-id="c1230-165">False</span><span class="sxs-lookup"><span data-stu-id="c1230-165">False</span></span>                                                     |
| <span data-ttu-id="c1230-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c1230-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1230-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c1230-167">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c1230-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1230-168">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c1230-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1230-169">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c1230-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1230-170">Search-Flags</span></span>           | <span data-ttu-id="c1230-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1230-171">0x00000000</span></span>                                                |
| <span data-ttu-id="c1230-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1230-172">System-Flags</span></span>           | <span data-ttu-id="c1230-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1230-173">0x00000010</span></span>                                                |
| <span data-ttu-id="c1230-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c1230-174">Classes used in</span></span>        | [<span data-ttu-id="c1230-175">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="c1230-175">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c1230-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c1230-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c1230-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c1230-177">Entry</span></span> | <span data-ttu-id="c1230-178">Wert</span><span class="sxs-lookup"><span data-stu-id="c1230-178">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c1230-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c1230-179">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c1230-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1230-180">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c1230-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1230-181">System-Only</span></span>            | <span data-ttu-id="c1230-182">False</span><span class="sxs-lookup"><span data-stu-id="c1230-182">False</span></span>                                                     |
| <span data-ttu-id="c1230-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c1230-183">Is-Single-Valued</span></span>       | <span data-ttu-id="c1230-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="c1230-184">True</span></span>                                                      |
| <span data-ttu-id="c1230-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c1230-185">Is Indexed</span></span>             | <span data-ttu-id="c1230-186">False</span><span class="sxs-lookup"><span data-stu-id="c1230-186">False</span></span>                                                     |
| <span data-ttu-id="c1230-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c1230-187">In Global Catalog</span></span>      | <span data-ttu-id="c1230-188">False</span><span class="sxs-lookup"><span data-stu-id="c1230-188">False</span></span>                                                     |
| <span data-ttu-id="c1230-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c1230-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1230-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c1230-190">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c1230-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1230-191">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c1230-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1230-192">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c1230-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1230-193">Search-Flags</span></span>           | <span data-ttu-id="c1230-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1230-194">0x00000000</span></span>                                                |
| <span data-ttu-id="c1230-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1230-195">System-Flags</span></span>           | <span data-ttu-id="c1230-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1230-196">0x00000010</span></span>                                                |
| <span data-ttu-id="c1230-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c1230-197">Classes used in</span></span>        | [<span data-ttu-id="c1230-198">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="c1230-198">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c1230-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1230-199">Windows Server 2008</span></span>



| <span data-ttu-id="c1230-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c1230-200">Entry</span></span> | <span data-ttu-id="c1230-201">Wert</span><span class="sxs-lookup"><span data-stu-id="c1230-201">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c1230-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c1230-202">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c1230-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1230-203">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c1230-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1230-204">System-Only</span></span>            | <span data-ttu-id="c1230-205">False</span><span class="sxs-lookup"><span data-stu-id="c1230-205">False</span></span>                                                     |
| <span data-ttu-id="c1230-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c1230-206">Is-Single-Valued</span></span>       | <span data-ttu-id="c1230-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="c1230-207">True</span></span>                                                      |
| <span data-ttu-id="c1230-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c1230-208">Is Indexed</span></span>             | <span data-ttu-id="c1230-209">False</span><span class="sxs-lookup"><span data-stu-id="c1230-209">False</span></span>                                                     |
| <span data-ttu-id="c1230-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c1230-210">In Global Catalog</span></span>      | <span data-ttu-id="c1230-211">False</span><span class="sxs-lookup"><span data-stu-id="c1230-211">False</span></span>                                                     |
| <span data-ttu-id="c1230-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c1230-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1230-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c1230-213">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c1230-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1230-214">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c1230-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1230-215">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c1230-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1230-216">Search-Flags</span></span>           | <span data-ttu-id="c1230-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1230-217">0x00000000</span></span>                                                |
| <span data-ttu-id="c1230-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1230-218">System-Flags</span></span>           | <span data-ttu-id="c1230-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1230-219">0x00000010</span></span>                                                |
| <span data-ttu-id="c1230-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c1230-220">Classes used in</span></span>        | [<span data-ttu-id="c1230-221">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="c1230-221">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c1230-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c1230-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c1230-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c1230-223">Entry</span></span> | <span data-ttu-id="c1230-224">Wert</span><span class="sxs-lookup"><span data-stu-id="c1230-224">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c1230-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c1230-225">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c1230-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1230-226">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c1230-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1230-227">System-Only</span></span>            | <span data-ttu-id="c1230-228">False</span><span class="sxs-lookup"><span data-stu-id="c1230-228">False</span></span>                                                     |
| <span data-ttu-id="c1230-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c1230-229">Is-Single-Valued</span></span>       | <span data-ttu-id="c1230-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="c1230-230">True</span></span>                                                      |
| <span data-ttu-id="c1230-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c1230-231">Is Indexed</span></span>             | <span data-ttu-id="c1230-232">False</span><span class="sxs-lookup"><span data-stu-id="c1230-232">False</span></span>                                                     |
| <span data-ttu-id="c1230-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c1230-233">In Global Catalog</span></span>      | <span data-ttu-id="c1230-234">False</span><span class="sxs-lookup"><span data-stu-id="c1230-234">False</span></span>                                                     |
| <span data-ttu-id="c1230-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c1230-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1230-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c1230-236">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c1230-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1230-237">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c1230-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1230-238">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c1230-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1230-239">Search-Flags</span></span>           | <span data-ttu-id="c1230-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1230-240">0x00000000</span></span>                                                |
| <span data-ttu-id="c1230-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1230-241">System-Flags</span></span>           | <span data-ttu-id="c1230-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1230-242">0x00000010</span></span>                                                |
| <span data-ttu-id="c1230-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c1230-243">Classes used in</span></span>        | [<span data-ttu-id="c1230-244">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="c1230-244">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c1230-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c1230-245">Windows Server 2012</span></span>



| <span data-ttu-id="c1230-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c1230-246">Entry</span></span> | <span data-ttu-id="c1230-247">Wert</span><span class="sxs-lookup"><span data-stu-id="c1230-247">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c1230-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c1230-248">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c1230-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1230-249">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c1230-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1230-250">System-Only</span></span>            | <span data-ttu-id="c1230-251">False</span><span class="sxs-lookup"><span data-stu-id="c1230-251">False</span></span>                                                     |
| <span data-ttu-id="c1230-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c1230-252">Is-Single-Valued</span></span>       | <span data-ttu-id="c1230-253">Richtig</span><span class="sxs-lookup"><span data-stu-id="c1230-253">True</span></span>                                                      |
| <span data-ttu-id="c1230-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c1230-254">Is Indexed</span></span>             | <span data-ttu-id="c1230-255">False</span><span class="sxs-lookup"><span data-stu-id="c1230-255">False</span></span>                                                     |
| <span data-ttu-id="c1230-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c1230-256">In Global Catalog</span></span>      | <span data-ttu-id="c1230-257">False</span><span class="sxs-lookup"><span data-stu-id="c1230-257">False</span></span>                                                     |
| <span data-ttu-id="c1230-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c1230-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1230-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c1230-259">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c1230-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1230-260">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c1230-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1230-261">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c1230-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1230-262">Search-Flags</span></span>           | <span data-ttu-id="c1230-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1230-263">0x00000000</span></span>                                                |
| <span data-ttu-id="c1230-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1230-264">System-Flags</span></span>           | <span data-ttu-id="c1230-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1230-265">0x00000010</span></span>                                                |
| <span data-ttu-id="c1230-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c1230-266">Classes used in</span></span>        | [<span data-ttu-id="c1230-267">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="c1230-267">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





