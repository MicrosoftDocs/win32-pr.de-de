---
title: Rid-used-Pool-Attribut
description: Die RID-Pools, die von einem DC verwendet wurden.
ms.assetid: ca779461-5b8f-4ab2-b9cf-5f829889f10d
ms.tgt_platform: multiple
keywords:
- 'Rid-used: AD-Schema des Pool-Attributs'
- AD-Schema für das ridusedpool-Attribut
topic_type:
- apiref
api_name:
- RID-Used-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84547d99b162da9da6e634a7c35eb9700e84e2a6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107571"
---
# <a name="rid-used-pool-attribute"></a><span data-ttu-id="4ceae-105">Rid-used-Pool-Attribut</span><span class="sxs-lookup"><span data-stu-id="4ceae-105">RID-Used-Pool attribute</span></span>

<span data-ttu-id="4ceae-106">Die RID-Pools, die von einem DC verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="4ceae-106">The RID Pools that have been used by a DC.</span></span>



| <span data-ttu-id="4ceae-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4ceae-107">Entry</span></span> | <span data-ttu-id="4ceae-108">Wert</span><span class="sxs-lookup"><span data-stu-id="4ceae-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="4ceae-109">CN</span><span class="sxs-lookup"><span data-stu-id="4ceae-109">CN</span></span>                | <span data-ttu-id="4ceae-110">Rid-used-Pool</span><span class="sxs-lookup"><span data-stu-id="4ceae-110">RID-Used-Pool</span></span>                        |
| <span data-ttu-id="4ceae-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4ceae-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4ceae-112">ridusedpool</span><span class="sxs-lookup"><span data-stu-id="4ceae-112">rIDUsedPool</span></span>                          |
| <span data-ttu-id="4ceae-113">Size</span><span class="sxs-lookup"><span data-stu-id="4ceae-113">Size</span></span>              | <span data-ttu-id="4ceae-114">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="4ceae-114">8 bytes</span></span>                              |
| <span data-ttu-id="4ceae-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="4ceae-115">Update Privilege</span></span>  | <span data-ttu-id="4ceae-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4ceae-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="4ceae-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="4ceae-117">Update Frequency</span></span>  | <span data-ttu-id="4ceae-118">Jedes Mal, wenn ein RID-Pool geleert wird.</span><span class="sxs-lookup"><span data-stu-id="4ceae-118">Whenever a RID pool is emptied.</span></span>      |
| <span data-ttu-id="4ceae-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4ceae-119">Attribute-Id</span></span>      | <span data-ttu-id="4ceae-120">1.2.840.113556.1.4.373</span><span class="sxs-lookup"><span data-stu-id="4ceae-120">1.2.840.113556.1.4.373</span></span>               |
| <span data-ttu-id="4ceae-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4ceae-121">System-Id-Guid</span></span>    | <span data-ttu-id="4ceae-122">6617188b-8B f -11D0-AFDA-00c04f 930c9</span><span class="sxs-lookup"><span data-stu-id="4ceae-122">6617188b-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="4ceae-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ceae-123">Syntax</span></span>            | [<span data-ttu-id="4ceae-124">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="4ceae-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="4ceae-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="4ceae-125">Implementations</span></span>

-   [<span data-ttu-id="4ceae-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4ceae-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4ceae-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4ceae-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4ceae-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4ceae-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4ceae-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4ceae-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4ceae-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4ceae-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4ceae-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4ceae-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4ceae-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4ceae-132">Windows 2000 Server</span></span>



| <span data-ttu-id="4ceae-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4ceae-133">Entry</span></span> | <span data-ttu-id="4ceae-134">Wert</span><span class="sxs-lookup"><span data-stu-id="4ceae-134">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="4ceae-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4ceae-135">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="4ceae-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ceae-136">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="4ceae-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ceae-137">System-Only</span></span>            | <span data-ttu-id="4ceae-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="4ceae-138">True</span></span>                                   |
| <span data-ttu-id="4ceae-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4ceae-139">Is-Single-Valued</span></span>       | <span data-ttu-id="4ceae-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="4ceae-140">True</span></span>                                   |
| <span data-ttu-id="4ceae-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4ceae-141">Is Indexed</span></span>             | <span data-ttu-id="4ceae-142">False</span><span class="sxs-lookup"><span data-stu-id="4ceae-142">False</span></span>                                  |
| <span data-ttu-id="4ceae-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4ceae-143">In Global Catalog</span></span>      | <span data-ttu-id="4ceae-144">False</span><span class="sxs-lookup"><span data-stu-id="4ceae-144">False</span></span>                                  |
| <span data-ttu-id="4ceae-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4ceae-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ceae-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4ceae-146">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="4ceae-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ceae-147">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="4ceae-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ceae-148">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="4ceae-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ceae-149">Search-Flags</span></span>           | <span data-ttu-id="4ceae-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ceae-150">0x00000000</span></span>                             |
| <span data-ttu-id="4ceae-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ceae-151">System-Flags</span></span>           | <span data-ttu-id="4ceae-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ceae-152">0x00000010</span></span>                             |
| <span data-ttu-id="4ceae-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4ceae-153">Classes used in</span></span>        | [<span data-ttu-id="4ceae-154">**Rid-Satz**</span><span class="sxs-lookup"><span data-stu-id="4ceae-154">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4ceae-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4ceae-155">Windows Server 2003</span></span>



| <span data-ttu-id="4ceae-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4ceae-156">Entry</span></span> | <span data-ttu-id="4ceae-157">Wert</span><span class="sxs-lookup"><span data-stu-id="4ceae-157">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="4ceae-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4ceae-158">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="4ceae-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ceae-159">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="4ceae-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ceae-160">System-Only</span></span>            | <span data-ttu-id="4ceae-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="4ceae-161">True</span></span>                                   |
| <span data-ttu-id="4ceae-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4ceae-162">Is-Single-Valued</span></span>       | <span data-ttu-id="4ceae-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="4ceae-163">True</span></span>                                   |
| <span data-ttu-id="4ceae-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4ceae-164">Is Indexed</span></span>             | <span data-ttu-id="4ceae-165">False</span><span class="sxs-lookup"><span data-stu-id="4ceae-165">False</span></span>                                  |
| <span data-ttu-id="4ceae-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4ceae-166">In Global Catalog</span></span>      | <span data-ttu-id="4ceae-167">False</span><span class="sxs-lookup"><span data-stu-id="4ceae-167">False</span></span>                                  |
| <span data-ttu-id="4ceae-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4ceae-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ceae-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4ceae-169">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="4ceae-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ceae-170">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="4ceae-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ceae-171">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="4ceae-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ceae-172">Search-Flags</span></span>           | <span data-ttu-id="4ceae-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ceae-173">0x00000000</span></span>                             |
| <span data-ttu-id="4ceae-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ceae-174">System-Flags</span></span>           | <span data-ttu-id="4ceae-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ceae-175">0x00000010</span></span>                             |
| <span data-ttu-id="4ceae-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4ceae-176">Classes used in</span></span>        | [<span data-ttu-id="4ceae-177">**Rid-Satz**</span><span class="sxs-lookup"><span data-stu-id="4ceae-177">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4ceae-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4ceae-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4ceae-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4ceae-179">Entry</span></span> | <span data-ttu-id="4ceae-180">Wert</span><span class="sxs-lookup"><span data-stu-id="4ceae-180">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="4ceae-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4ceae-181">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="4ceae-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ceae-182">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="4ceae-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ceae-183">System-Only</span></span>            | <span data-ttu-id="4ceae-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="4ceae-184">True</span></span>                                   |
| <span data-ttu-id="4ceae-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4ceae-185">Is-Single-Valued</span></span>       | <span data-ttu-id="4ceae-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="4ceae-186">True</span></span>                                   |
| <span data-ttu-id="4ceae-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4ceae-187">Is Indexed</span></span>             | <span data-ttu-id="4ceae-188">False</span><span class="sxs-lookup"><span data-stu-id="4ceae-188">False</span></span>                                  |
| <span data-ttu-id="4ceae-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4ceae-189">In Global Catalog</span></span>      | <span data-ttu-id="4ceae-190">False</span><span class="sxs-lookup"><span data-stu-id="4ceae-190">False</span></span>                                  |
| <span data-ttu-id="4ceae-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4ceae-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ceae-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4ceae-192">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="4ceae-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ceae-193">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="4ceae-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ceae-194">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="4ceae-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ceae-195">Search-Flags</span></span>           | <span data-ttu-id="4ceae-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ceae-196">0x00000000</span></span>                             |
| <span data-ttu-id="4ceae-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ceae-197">System-Flags</span></span>           | <span data-ttu-id="4ceae-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ceae-198">0x00000010</span></span>                             |
| <span data-ttu-id="4ceae-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4ceae-199">Classes used in</span></span>        | [<span data-ttu-id="4ceae-200">**Rid-Satz**</span><span class="sxs-lookup"><span data-stu-id="4ceae-200">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4ceae-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ceae-201">Windows Server 2008</span></span>



| <span data-ttu-id="4ceae-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4ceae-202">Entry</span></span> | <span data-ttu-id="4ceae-203">Wert</span><span class="sxs-lookup"><span data-stu-id="4ceae-203">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="4ceae-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4ceae-204">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="4ceae-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ceae-205">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="4ceae-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ceae-206">System-Only</span></span>            | <span data-ttu-id="4ceae-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="4ceae-207">True</span></span>                                   |
| <span data-ttu-id="4ceae-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4ceae-208">Is-Single-Valued</span></span>       | <span data-ttu-id="4ceae-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="4ceae-209">True</span></span>                                   |
| <span data-ttu-id="4ceae-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4ceae-210">Is Indexed</span></span>             | <span data-ttu-id="4ceae-211">False</span><span class="sxs-lookup"><span data-stu-id="4ceae-211">False</span></span>                                  |
| <span data-ttu-id="4ceae-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4ceae-212">In Global Catalog</span></span>      | <span data-ttu-id="4ceae-213">False</span><span class="sxs-lookup"><span data-stu-id="4ceae-213">False</span></span>                                  |
| <span data-ttu-id="4ceae-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4ceae-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ceae-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4ceae-215">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="4ceae-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ceae-216">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="4ceae-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ceae-217">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="4ceae-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ceae-218">Search-Flags</span></span>           | <span data-ttu-id="4ceae-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ceae-219">0x00000000</span></span>                             |
| <span data-ttu-id="4ceae-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ceae-220">System-Flags</span></span>           | <span data-ttu-id="4ceae-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ceae-221">0x00000010</span></span>                             |
| <span data-ttu-id="4ceae-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4ceae-222">Classes used in</span></span>        | [<span data-ttu-id="4ceae-223">**Rid-Satz**</span><span class="sxs-lookup"><span data-stu-id="4ceae-223">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4ceae-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4ceae-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4ceae-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4ceae-225">Entry</span></span> | <span data-ttu-id="4ceae-226">Wert</span><span class="sxs-lookup"><span data-stu-id="4ceae-226">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="4ceae-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4ceae-227">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="4ceae-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ceae-228">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="4ceae-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ceae-229">System-Only</span></span>            | <span data-ttu-id="4ceae-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="4ceae-230">True</span></span>                                   |
| <span data-ttu-id="4ceae-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4ceae-231">Is-Single-Valued</span></span>       | <span data-ttu-id="4ceae-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="4ceae-232">True</span></span>                                   |
| <span data-ttu-id="4ceae-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4ceae-233">Is Indexed</span></span>             | <span data-ttu-id="4ceae-234">False</span><span class="sxs-lookup"><span data-stu-id="4ceae-234">False</span></span>                                  |
| <span data-ttu-id="4ceae-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4ceae-235">In Global Catalog</span></span>      | <span data-ttu-id="4ceae-236">False</span><span class="sxs-lookup"><span data-stu-id="4ceae-236">False</span></span>                                  |
| <span data-ttu-id="4ceae-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4ceae-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ceae-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4ceae-238">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="4ceae-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ceae-239">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="4ceae-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ceae-240">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="4ceae-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ceae-241">Search-Flags</span></span>           | <span data-ttu-id="4ceae-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ceae-242">0x00000000</span></span>                             |
| <span data-ttu-id="4ceae-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ceae-243">System-Flags</span></span>           | <span data-ttu-id="4ceae-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ceae-244">0x00000010</span></span>                             |
| <span data-ttu-id="4ceae-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4ceae-245">Classes used in</span></span>        | [<span data-ttu-id="4ceae-246">**Rid-Satz**</span><span class="sxs-lookup"><span data-stu-id="4ceae-246">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4ceae-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4ceae-247">Windows Server 2012</span></span>



| <span data-ttu-id="4ceae-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4ceae-248">Entry</span></span> | <span data-ttu-id="4ceae-249">Wert</span><span class="sxs-lookup"><span data-stu-id="4ceae-249">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="4ceae-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4ceae-250">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="4ceae-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ceae-251">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="4ceae-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ceae-252">System-Only</span></span>            | <span data-ttu-id="4ceae-253">Richtig</span><span class="sxs-lookup"><span data-stu-id="4ceae-253">True</span></span>                                   |
| <span data-ttu-id="4ceae-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4ceae-254">Is-Single-Valued</span></span>       | <span data-ttu-id="4ceae-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="4ceae-255">True</span></span>                                   |
| <span data-ttu-id="4ceae-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4ceae-256">Is Indexed</span></span>             | <span data-ttu-id="4ceae-257">False</span><span class="sxs-lookup"><span data-stu-id="4ceae-257">False</span></span>                                  |
| <span data-ttu-id="4ceae-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4ceae-258">In Global Catalog</span></span>      | <span data-ttu-id="4ceae-259">False</span><span class="sxs-lookup"><span data-stu-id="4ceae-259">False</span></span>                                  |
| <span data-ttu-id="4ceae-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4ceae-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ceae-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4ceae-261">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="4ceae-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ceae-262">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="4ceae-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ceae-263">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="4ceae-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ceae-264">Search-Flags</span></span>           | <span data-ttu-id="4ceae-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ceae-265">0x00000000</span></span>                             |
| <span data-ttu-id="4ceae-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ceae-266">System-Flags</span></span>           | <span data-ttu-id="4ceae-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ceae-267">0x00000010</span></span>                             |
| <span data-ttu-id="4ceae-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4ceae-268">Classes used in</span></span>        | [<span data-ttu-id="4ceae-269">**Rid-Satz**</span><span class="sxs-lookup"><span data-stu-id="4ceae-269">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 





