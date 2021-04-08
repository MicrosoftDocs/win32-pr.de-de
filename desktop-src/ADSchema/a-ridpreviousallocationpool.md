---
title: Rid-Previous-Allocation-Pool-Attribut
description: Enthält den Pool relativer Bezeichner (RIDs), von denen ein Domänen Controller zugeordnet wird.
ms.assetid: d2f60259-388b-4dea-a1f7-9e650b1a66db
ms.tgt_platform: multiple
keywords:
- AD-Schema für Rid-Previous-Allocation-Pool-Attribut
- "\"ridpreviousallocationpool\"-Attribut, AD-Schema"
topic_type:
- apiref
api_name:
- RID-Previous-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15438d55c9540ecca873395cc329058bc0773399
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859577"
---
# <a name="rid-previous-allocation-pool-attribute"></a><span data-ttu-id="5036e-105">Rid-Previous-Allocation-Pool-Attribut</span><span class="sxs-lookup"><span data-stu-id="5036e-105">RID-Previous-Allocation-Pool attribute</span></span>

<span data-ttu-id="5036e-106">Das **RID-Previous-Allocation-Pool-** Attribut enthält den Pool von relativen Bezeichners (RIDs), von denen ein Domänen Controller zuweist.</span><span class="sxs-lookup"><span data-stu-id="5036e-106">The **RID-Previous-Allocation-Pool** attribute contains the pool of relative identifiers (RIDs) that a domain controller allocates from.</span></span> <span data-ttu-id="5036e-107">Bei diesem Attribut handelt es sich um einen 8-Byte-Wert, der ein paar von vier-Byte-Ganzzahlen enthält, die die Start-und Endwerte des RID-Pools darstellen.</span><span class="sxs-lookup"><span data-stu-id="5036e-107">This attribute is an eight-byte value that contains a pair of four-byte integers that represent the start and end values of the RID pool.</span></span> <span data-ttu-id="5036e-108">Der Startwert liegt in den unteren vier Bytes, und der Endwert liegt in den oberen vier Bytes.</span><span class="sxs-lookup"><span data-stu-id="5036e-108">The start value is in the lower four bytes and the end value is in the upper four bytes.</span></span>



| <span data-ttu-id="5036e-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5036e-109">Entry</span></span> | <span data-ttu-id="5036e-110">Wert</span><span class="sxs-lookup"><span data-stu-id="5036e-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="5036e-111">CN</span><span class="sxs-lookup"><span data-stu-id="5036e-111">CN</span></span>                | <span data-ttu-id="5036e-112">Rid-Previous-Allocation-Pool</span><span class="sxs-lookup"><span data-stu-id="5036e-112">RID-Previous-Allocation-Pool</span></span>         |
| <span data-ttu-id="5036e-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5036e-113">Ldap-Display-Name</span></span> | <span data-ttu-id="5036e-114">ridpreviousallocationpool</span><span class="sxs-lookup"><span data-stu-id="5036e-114">rIDPreviousAllocationPool</span></span>            |
| <span data-ttu-id="5036e-115">Size</span><span class="sxs-lookup"><span data-stu-id="5036e-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="5036e-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="5036e-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="5036e-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="5036e-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="5036e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5036e-118">Attribute-Id</span></span>      | <span data-ttu-id="5036e-119">1.2.840.113556.1.4.372</span><span class="sxs-lookup"><span data-stu-id="5036e-119">1.2.840.113556.1.4.372</span></span>               |
| <span data-ttu-id="5036e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5036e-120">System-Id-Guid</span></span>    | <span data-ttu-id="5036e-121">6617188a-8-Datei mit dem Namen "", "AFDA-00c04"</span><span class="sxs-lookup"><span data-stu-id="5036e-121">6617188a-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="5036e-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="5036e-122">Syntax</span></span>            | [<span data-ttu-id="5036e-123">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="5036e-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="5036e-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="5036e-124">Implementations</span></span>

-   [<span data-ttu-id="5036e-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5036e-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5036e-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5036e-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5036e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5036e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5036e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5036e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5036e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5036e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5036e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5036e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5036e-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5036e-131">Windows 2000 Server</span></span>



| <span data-ttu-id="5036e-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5036e-132">Entry</span></span> | <span data-ttu-id="5036e-133">Wert</span><span class="sxs-lookup"><span data-stu-id="5036e-133">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="5036e-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5036e-134">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="5036e-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5036e-135">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="5036e-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="5036e-136">System-Only</span></span>            | <span data-ttu-id="5036e-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="5036e-137">True</span></span>                                   |
| <span data-ttu-id="5036e-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5036e-138">Is-Single-Valued</span></span>       | <span data-ttu-id="5036e-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="5036e-139">True</span></span>                                   |
| <span data-ttu-id="5036e-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5036e-140">Is Indexed</span></span>             | <span data-ttu-id="5036e-141">False</span><span class="sxs-lookup"><span data-stu-id="5036e-141">False</span></span>                                  |
| <span data-ttu-id="5036e-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5036e-142">In Global Catalog</span></span>      | <span data-ttu-id="5036e-143">False</span><span class="sxs-lookup"><span data-stu-id="5036e-143">False</span></span>                                  |
| <span data-ttu-id="5036e-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5036e-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="5036e-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5036e-145">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="5036e-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5036e-146">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="5036e-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5036e-147">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="5036e-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5036e-148">Search-Flags</span></span>           | <span data-ttu-id="5036e-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5036e-149">0x00000000</span></span>                             |
| <span data-ttu-id="5036e-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5036e-150">System-Flags</span></span>           | <span data-ttu-id="5036e-151">0x00000011</span><span class="sxs-lookup"><span data-stu-id="5036e-151">0x00000011</span></span>                             |
| <span data-ttu-id="5036e-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5036e-152">Classes used in</span></span>        | [<span data-ttu-id="5036e-153">**Rid-Satz**</span><span class="sxs-lookup"><span data-stu-id="5036e-153">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5036e-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5036e-154">Windows Server 2003</span></span>



| <span data-ttu-id="5036e-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5036e-155">Entry</span></span> | <span data-ttu-id="5036e-156">Wert</span><span class="sxs-lookup"><span data-stu-id="5036e-156">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="5036e-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5036e-157">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="5036e-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5036e-158">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="5036e-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="5036e-159">System-Only</span></span>            | <span data-ttu-id="5036e-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="5036e-160">True</span></span>                                   |
| <span data-ttu-id="5036e-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5036e-161">Is-Single-Valued</span></span>       | <span data-ttu-id="5036e-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="5036e-162">True</span></span>                                   |
| <span data-ttu-id="5036e-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5036e-163">Is Indexed</span></span>             | <span data-ttu-id="5036e-164">False</span><span class="sxs-lookup"><span data-stu-id="5036e-164">False</span></span>                                  |
| <span data-ttu-id="5036e-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5036e-165">In Global Catalog</span></span>      | <span data-ttu-id="5036e-166">False</span><span class="sxs-lookup"><span data-stu-id="5036e-166">False</span></span>                                  |
| <span data-ttu-id="5036e-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5036e-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="5036e-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5036e-168">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="5036e-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5036e-169">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="5036e-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5036e-170">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="5036e-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5036e-171">Search-Flags</span></span>           | <span data-ttu-id="5036e-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5036e-172">0x00000000</span></span>                             |
| <span data-ttu-id="5036e-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5036e-173">System-Flags</span></span>           | <span data-ttu-id="5036e-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="5036e-174">0x00000011</span></span>                             |
| <span data-ttu-id="5036e-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5036e-175">Classes used in</span></span>        | [<span data-ttu-id="5036e-176">**Rid-Satz**</span><span class="sxs-lookup"><span data-stu-id="5036e-176">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5036e-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5036e-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5036e-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5036e-178">Entry</span></span> | <span data-ttu-id="5036e-179">Wert</span><span class="sxs-lookup"><span data-stu-id="5036e-179">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="5036e-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5036e-180">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="5036e-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5036e-181">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="5036e-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="5036e-182">System-Only</span></span>            | <span data-ttu-id="5036e-183">Richtig</span><span class="sxs-lookup"><span data-stu-id="5036e-183">True</span></span>                                   |
| <span data-ttu-id="5036e-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5036e-184">Is-Single-Valued</span></span>       | <span data-ttu-id="5036e-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="5036e-185">True</span></span>                                   |
| <span data-ttu-id="5036e-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5036e-186">Is Indexed</span></span>             | <span data-ttu-id="5036e-187">False</span><span class="sxs-lookup"><span data-stu-id="5036e-187">False</span></span>                                  |
| <span data-ttu-id="5036e-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5036e-188">In Global Catalog</span></span>      | <span data-ttu-id="5036e-189">False</span><span class="sxs-lookup"><span data-stu-id="5036e-189">False</span></span>                                  |
| <span data-ttu-id="5036e-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5036e-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="5036e-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5036e-191">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="5036e-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5036e-192">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="5036e-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5036e-193">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="5036e-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5036e-194">Search-Flags</span></span>           | <span data-ttu-id="5036e-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5036e-195">0x00000000</span></span>                             |
| <span data-ttu-id="5036e-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5036e-196">System-Flags</span></span>           | <span data-ttu-id="5036e-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="5036e-197">0x00000011</span></span>                             |
| <span data-ttu-id="5036e-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5036e-198">Classes used in</span></span>        | [<span data-ttu-id="5036e-199">**Rid-Satz**</span><span class="sxs-lookup"><span data-stu-id="5036e-199">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5036e-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5036e-200">Windows Server 2008</span></span>



| <span data-ttu-id="5036e-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5036e-201">Entry</span></span> | <span data-ttu-id="5036e-202">Wert</span><span class="sxs-lookup"><span data-stu-id="5036e-202">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="5036e-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5036e-203">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="5036e-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5036e-204">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="5036e-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="5036e-205">System-Only</span></span>            | <span data-ttu-id="5036e-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="5036e-206">True</span></span>                                   |
| <span data-ttu-id="5036e-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5036e-207">Is-Single-Valued</span></span>       | <span data-ttu-id="5036e-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="5036e-208">True</span></span>                                   |
| <span data-ttu-id="5036e-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5036e-209">Is Indexed</span></span>             | <span data-ttu-id="5036e-210">False</span><span class="sxs-lookup"><span data-stu-id="5036e-210">False</span></span>                                  |
| <span data-ttu-id="5036e-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5036e-211">In Global Catalog</span></span>      | <span data-ttu-id="5036e-212">False</span><span class="sxs-lookup"><span data-stu-id="5036e-212">False</span></span>                                  |
| <span data-ttu-id="5036e-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5036e-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="5036e-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5036e-214">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="5036e-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5036e-215">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="5036e-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5036e-216">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="5036e-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5036e-217">Search-Flags</span></span>           | <span data-ttu-id="5036e-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5036e-218">0x00000000</span></span>                             |
| <span data-ttu-id="5036e-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5036e-219">System-Flags</span></span>           | <span data-ttu-id="5036e-220">0x00000011</span><span class="sxs-lookup"><span data-stu-id="5036e-220">0x00000011</span></span>                             |
| <span data-ttu-id="5036e-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5036e-221">Classes used in</span></span>        | [<span data-ttu-id="5036e-222">**Rid-Satz**</span><span class="sxs-lookup"><span data-stu-id="5036e-222">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5036e-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5036e-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5036e-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5036e-224">Entry</span></span> | <span data-ttu-id="5036e-225">Wert</span><span class="sxs-lookup"><span data-stu-id="5036e-225">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="5036e-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5036e-226">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="5036e-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5036e-227">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="5036e-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="5036e-228">System-Only</span></span>            | <span data-ttu-id="5036e-229">Richtig</span><span class="sxs-lookup"><span data-stu-id="5036e-229">True</span></span>                                   |
| <span data-ttu-id="5036e-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5036e-230">Is-Single-Valued</span></span>       | <span data-ttu-id="5036e-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="5036e-231">True</span></span>                                   |
| <span data-ttu-id="5036e-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5036e-232">Is Indexed</span></span>             | <span data-ttu-id="5036e-233">False</span><span class="sxs-lookup"><span data-stu-id="5036e-233">False</span></span>                                  |
| <span data-ttu-id="5036e-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5036e-234">In Global Catalog</span></span>      | <span data-ttu-id="5036e-235">False</span><span class="sxs-lookup"><span data-stu-id="5036e-235">False</span></span>                                  |
| <span data-ttu-id="5036e-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5036e-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="5036e-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5036e-237">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="5036e-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5036e-238">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="5036e-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5036e-239">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="5036e-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5036e-240">Search-Flags</span></span>           | <span data-ttu-id="5036e-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5036e-241">0x00000000</span></span>                             |
| <span data-ttu-id="5036e-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5036e-242">System-Flags</span></span>           | <span data-ttu-id="5036e-243">0x00000011</span><span class="sxs-lookup"><span data-stu-id="5036e-243">0x00000011</span></span>                             |
| <span data-ttu-id="5036e-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5036e-244">Classes used in</span></span>        | [<span data-ttu-id="5036e-245">**Rid-Satz**</span><span class="sxs-lookup"><span data-stu-id="5036e-245">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5036e-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5036e-246">Windows Server 2012</span></span>



| <span data-ttu-id="5036e-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5036e-247">Entry</span></span> | <span data-ttu-id="5036e-248">Wert</span><span class="sxs-lookup"><span data-stu-id="5036e-248">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="5036e-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5036e-249">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="5036e-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5036e-250">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="5036e-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="5036e-251">System-Only</span></span>            | <span data-ttu-id="5036e-252">Richtig</span><span class="sxs-lookup"><span data-stu-id="5036e-252">True</span></span>                                   |
| <span data-ttu-id="5036e-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5036e-253">Is-Single-Valued</span></span>       | <span data-ttu-id="5036e-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="5036e-254">True</span></span>                                   |
| <span data-ttu-id="5036e-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5036e-255">Is Indexed</span></span>             | <span data-ttu-id="5036e-256">False</span><span class="sxs-lookup"><span data-stu-id="5036e-256">False</span></span>                                  |
| <span data-ttu-id="5036e-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5036e-257">In Global Catalog</span></span>      | <span data-ttu-id="5036e-258">False</span><span class="sxs-lookup"><span data-stu-id="5036e-258">False</span></span>                                  |
| <span data-ttu-id="5036e-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5036e-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="5036e-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5036e-260">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="5036e-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5036e-261">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="5036e-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5036e-262">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="5036e-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5036e-263">Search-Flags</span></span>           | <span data-ttu-id="5036e-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5036e-264">0x00000000</span></span>                             |
| <span data-ttu-id="5036e-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5036e-265">System-Flags</span></span>           | <span data-ttu-id="5036e-266">0x00000011</span><span class="sxs-lookup"><span data-stu-id="5036e-266">0x00000011</span></span>                             |
| <span data-ttu-id="5036e-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5036e-267">Classes used in</span></span>        | [<span data-ttu-id="5036e-268">**Rid-Satz**</span><span class="sxs-lookup"><span data-stu-id="5036e-268">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 





