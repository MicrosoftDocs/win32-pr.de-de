---
title: Rid-Allocation-Pool-Attribut
description: Ein Pool, der für die Verwendung durch den RID-Manager vorab abgerufen wurde, als der RID-Previous-Allocation-Pool aufgebraucht wurde.
ms.assetid: 6d49b497-322f-424c-badc-4801f51481f3
ms.tgt_platform: multiple
keywords:
- AD-Schema für Rid-Allocation-Pool-Attribut
- cenzuzucationpool-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- RID-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a035cef460cc3081144d66391db78fb32c61108b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344743"
---
# <a name="rid-allocation-pool-attribute"></a><span data-ttu-id="0b472-105">Rid-Allocation-Pool-Attribut</span><span class="sxs-lookup"><span data-stu-id="0b472-105">RID-Allocation-Pool attribute</span></span>

<span data-ttu-id="0b472-106">Ein Pool, der für die Verwendung durch den RID-Manager vorab abgerufen wurde, als der RID-Previous-Allocation-Pool aufgebraucht wurde.</span><span class="sxs-lookup"><span data-stu-id="0b472-106">A pool that was prefetched for use by the RID manager when the RID-Previous-Allocation-Pool has been used up.</span></span>



| <span data-ttu-id="0b472-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0b472-107">Entry</span></span> | <span data-ttu-id="0b472-108">Wert</span><span class="sxs-lookup"><span data-stu-id="0b472-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="0b472-109">CN</span><span class="sxs-lookup"><span data-stu-id="0b472-109">CN</span></span>                | <span data-ttu-id="0b472-110">RID-Zuordnung-Pool</span><span class="sxs-lookup"><span data-stu-id="0b472-110">RID-Allocation-Pool</span></span>                  |
| <span data-ttu-id="0b472-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0b472-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0b472-112">ridzugecationpool</span><span class="sxs-lookup"><span data-stu-id="0b472-112">rIDAllocationPool</span></span>                    |
| <span data-ttu-id="0b472-113">Size</span><span class="sxs-lookup"><span data-stu-id="0b472-113">Size</span></span>              | <span data-ttu-id="0b472-114">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="0b472-114">8 bytes</span></span>                              |
| <span data-ttu-id="0b472-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="0b472-115">Update Privilege</span></span>  | <span data-ttu-id="0b472-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0b472-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="0b472-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="0b472-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="0b472-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0b472-118">Attribute-Id</span></span>      | <span data-ttu-id="0b472-119">1.2.840.113556.1.4.371</span><span class="sxs-lookup"><span data-stu-id="0b472-119">1.2.840.113556.1.4.371</span></span>               |
| <span data-ttu-id="0b472-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0b472-120">System-Id-Guid</span></span>    | <span data-ttu-id="0b472-121">66171889-8F -11D0-AFDA-00c04f-930c9</span><span class="sxs-lookup"><span data-stu-id="0b472-121">66171889-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="0b472-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b472-122">Syntax</span></span>            | [<span data-ttu-id="0b472-123">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="0b472-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="0b472-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="0b472-124">Implementations</span></span>

-   [<span data-ttu-id="0b472-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0b472-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0b472-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0b472-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0b472-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0b472-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0b472-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0b472-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0b472-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0b472-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0b472-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0b472-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0b472-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0b472-131">Windows 2000 Server</span></span>



| <span data-ttu-id="0b472-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0b472-132">Entry</span></span> | <span data-ttu-id="0b472-133">Wert</span><span class="sxs-lookup"><span data-stu-id="0b472-133">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="0b472-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0b472-134">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="0b472-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b472-135">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="0b472-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b472-136">System-Only</span></span>            | <span data-ttu-id="0b472-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b472-137">True</span></span>                                   |
| <span data-ttu-id="0b472-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0b472-138">Is-Single-Valued</span></span>       | <span data-ttu-id="0b472-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b472-139">True</span></span>                                   |
| <span data-ttu-id="0b472-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0b472-140">Is Indexed</span></span>             | <span data-ttu-id="0b472-141">False</span><span class="sxs-lookup"><span data-stu-id="0b472-141">False</span></span>                                  |
| <span data-ttu-id="0b472-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0b472-142">In Global Catalog</span></span>      | <span data-ttu-id="0b472-143">False</span><span class="sxs-lookup"><span data-stu-id="0b472-143">False</span></span>                                  |
| <span data-ttu-id="0b472-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0b472-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b472-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0b472-145">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="0b472-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b472-146">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="0b472-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b472-147">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="0b472-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b472-148">Search-Flags</span></span>           | <span data-ttu-id="0b472-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b472-149">0x00000000</span></span>                             |
| <span data-ttu-id="0b472-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b472-150">System-Flags</span></span>           | <span data-ttu-id="0b472-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b472-151">0x00000010</span></span>                             |
| <span data-ttu-id="0b472-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0b472-152">Classes used in</span></span>        | [<span data-ttu-id="0b472-153">**Rid-Satz**</span><span class="sxs-lookup"><span data-stu-id="0b472-153">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0b472-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0b472-154">Windows Server 2003</span></span>



| <span data-ttu-id="0b472-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0b472-155">Entry</span></span> | <span data-ttu-id="0b472-156">Wert</span><span class="sxs-lookup"><span data-stu-id="0b472-156">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="0b472-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0b472-157">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="0b472-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b472-158">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="0b472-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b472-159">System-Only</span></span>            | <span data-ttu-id="0b472-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b472-160">True</span></span>                                   |
| <span data-ttu-id="0b472-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0b472-161">Is-Single-Valued</span></span>       | <span data-ttu-id="0b472-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b472-162">True</span></span>                                   |
| <span data-ttu-id="0b472-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0b472-163">Is Indexed</span></span>             | <span data-ttu-id="0b472-164">False</span><span class="sxs-lookup"><span data-stu-id="0b472-164">False</span></span>                                  |
| <span data-ttu-id="0b472-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0b472-165">In Global Catalog</span></span>      | <span data-ttu-id="0b472-166">False</span><span class="sxs-lookup"><span data-stu-id="0b472-166">False</span></span>                                  |
| <span data-ttu-id="0b472-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0b472-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b472-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0b472-168">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="0b472-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b472-169">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="0b472-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b472-170">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="0b472-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b472-171">Search-Flags</span></span>           | <span data-ttu-id="0b472-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b472-172">0x00000000</span></span>                             |
| <span data-ttu-id="0b472-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b472-173">System-Flags</span></span>           | <span data-ttu-id="0b472-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b472-174">0x00000010</span></span>                             |
| <span data-ttu-id="0b472-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0b472-175">Classes used in</span></span>        | [<span data-ttu-id="0b472-176">**Rid-Satz**</span><span class="sxs-lookup"><span data-stu-id="0b472-176">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0b472-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0b472-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0b472-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0b472-178">Entry</span></span> | <span data-ttu-id="0b472-179">Wert</span><span class="sxs-lookup"><span data-stu-id="0b472-179">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="0b472-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0b472-180">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="0b472-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b472-181">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="0b472-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b472-182">System-Only</span></span>            | <span data-ttu-id="0b472-183">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b472-183">True</span></span>                                   |
| <span data-ttu-id="0b472-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0b472-184">Is-Single-Valued</span></span>       | <span data-ttu-id="0b472-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b472-185">True</span></span>                                   |
| <span data-ttu-id="0b472-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0b472-186">Is Indexed</span></span>             | <span data-ttu-id="0b472-187">False</span><span class="sxs-lookup"><span data-stu-id="0b472-187">False</span></span>                                  |
| <span data-ttu-id="0b472-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0b472-188">In Global Catalog</span></span>      | <span data-ttu-id="0b472-189">False</span><span class="sxs-lookup"><span data-stu-id="0b472-189">False</span></span>                                  |
| <span data-ttu-id="0b472-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0b472-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b472-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0b472-191">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="0b472-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b472-192">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="0b472-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b472-193">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="0b472-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b472-194">Search-Flags</span></span>           | <span data-ttu-id="0b472-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b472-195">0x00000000</span></span>                             |
| <span data-ttu-id="0b472-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b472-196">System-Flags</span></span>           | <span data-ttu-id="0b472-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b472-197">0x00000010</span></span>                             |
| <span data-ttu-id="0b472-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0b472-198">Classes used in</span></span>        | [<span data-ttu-id="0b472-199">**Rid-Satz**</span><span class="sxs-lookup"><span data-stu-id="0b472-199">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0b472-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b472-200">Windows Server 2008</span></span>



| <span data-ttu-id="0b472-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0b472-201">Entry</span></span> | <span data-ttu-id="0b472-202">Wert</span><span class="sxs-lookup"><span data-stu-id="0b472-202">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="0b472-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0b472-203">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="0b472-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b472-204">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="0b472-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b472-205">System-Only</span></span>            | <span data-ttu-id="0b472-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b472-206">True</span></span>                                   |
| <span data-ttu-id="0b472-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0b472-207">Is-Single-Valued</span></span>       | <span data-ttu-id="0b472-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b472-208">True</span></span>                                   |
| <span data-ttu-id="0b472-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0b472-209">Is Indexed</span></span>             | <span data-ttu-id="0b472-210">False</span><span class="sxs-lookup"><span data-stu-id="0b472-210">False</span></span>                                  |
| <span data-ttu-id="0b472-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0b472-211">In Global Catalog</span></span>      | <span data-ttu-id="0b472-212">False</span><span class="sxs-lookup"><span data-stu-id="0b472-212">False</span></span>                                  |
| <span data-ttu-id="0b472-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0b472-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b472-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0b472-214">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="0b472-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b472-215">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="0b472-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b472-216">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="0b472-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b472-217">Search-Flags</span></span>           | <span data-ttu-id="0b472-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b472-218">0x00000000</span></span>                             |
| <span data-ttu-id="0b472-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b472-219">System-Flags</span></span>           | <span data-ttu-id="0b472-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b472-220">0x00000010</span></span>                             |
| <span data-ttu-id="0b472-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0b472-221">Classes used in</span></span>        | [<span data-ttu-id="0b472-222">**Rid-Satz**</span><span class="sxs-lookup"><span data-stu-id="0b472-222">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0b472-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0b472-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0b472-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0b472-224">Entry</span></span> | <span data-ttu-id="0b472-225">Wert</span><span class="sxs-lookup"><span data-stu-id="0b472-225">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="0b472-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0b472-226">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="0b472-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b472-227">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="0b472-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b472-228">System-Only</span></span>            | <span data-ttu-id="0b472-229">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b472-229">True</span></span>                                   |
| <span data-ttu-id="0b472-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0b472-230">Is-Single-Valued</span></span>       | <span data-ttu-id="0b472-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b472-231">True</span></span>                                   |
| <span data-ttu-id="0b472-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0b472-232">Is Indexed</span></span>             | <span data-ttu-id="0b472-233">False</span><span class="sxs-lookup"><span data-stu-id="0b472-233">False</span></span>                                  |
| <span data-ttu-id="0b472-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0b472-234">In Global Catalog</span></span>      | <span data-ttu-id="0b472-235">False</span><span class="sxs-lookup"><span data-stu-id="0b472-235">False</span></span>                                  |
| <span data-ttu-id="0b472-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0b472-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b472-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0b472-237">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="0b472-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b472-238">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="0b472-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b472-239">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="0b472-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b472-240">Search-Flags</span></span>           | <span data-ttu-id="0b472-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b472-241">0x00000000</span></span>                             |
| <span data-ttu-id="0b472-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b472-242">System-Flags</span></span>           | <span data-ttu-id="0b472-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b472-243">0x00000010</span></span>                             |
| <span data-ttu-id="0b472-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0b472-244">Classes used in</span></span>        | [<span data-ttu-id="0b472-245">**Rid-Satz**</span><span class="sxs-lookup"><span data-stu-id="0b472-245">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0b472-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0b472-246">Windows Server 2012</span></span>



| <span data-ttu-id="0b472-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0b472-247">Entry</span></span> | <span data-ttu-id="0b472-248">Wert</span><span class="sxs-lookup"><span data-stu-id="0b472-248">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="0b472-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0b472-249">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="0b472-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b472-250">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="0b472-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b472-251">System-Only</span></span>            | <span data-ttu-id="0b472-252">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b472-252">True</span></span>                                   |
| <span data-ttu-id="0b472-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0b472-253">Is-Single-Valued</span></span>       | <span data-ttu-id="0b472-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b472-254">True</span></span>                                   |
| <span data-ttu-id="0b472-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0b472-255">Is Indexed</span></span>             | <span data-ttu-id="0b472-256">False</span><span class="sxs-lookup"><span data-stu-id="0b472-256">False</span></span>                                  |
| <span data-ttu-id="0b472-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0b472-257">In Global Catalog</span></span>      | <span data-ttu-id="0b472-258">False</span><span class="sxs-lookup"><span data-stu-id="0b472-258">False</span></span>                                  |
| <span data-ttu-id="0b472-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0b472-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b472-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0b472-260">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="0b472-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b472-261">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="0b472-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b472-262">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="0b472-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b472-263">Search-Flags</span></span>           | <span data-ttu-id="0b472-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b472-264">0x00000000</span></span>                             |
| <span data-ttu-id="0b472-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b472-265">System-Flags</span></span>           | <span data-ttu-id="0b472-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b472-266">0x00000010</span></span>                             |
| <span data-ttu-id="0b472-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0b472-267">Classes used in</span></span>        | [<span data-ttu-id="0b472-268">**Rid-Satz**</span><span class="sxs-lookup"><span data-stu-id="0b472-268">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 





