---
title: Rid-available-Pool-Attribut
description: Der Speicherplatz, von dem RID-Pools zugeordnet werden.
ms.assetid: abb6218f-def2-4a38-964f-3f0ee6c6f917
ms.tgt_platform: multiple
keywords:
- AD-Schema für Rid-available-Pool-Attribut
- ridavailablepool-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- RID-Available-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59faf801b7f6f70e92c55a1d2a27857ed6ecb0c9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104213783"
---
# <a name="rid-available-pool-attribute"></a><span data-ttu-id="ab1c9-105">Rid-available-Pool-Attribut</span><span class="sxs-lookup"><span data-stu-id="ab1c9-105">RID-Available-Pool attribute</span></span>

<span data-ttu-id="ab1c9-106">Der Speicherplatz, von dem RID-Pools zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="ab1c9-106">The space from which RID Pools are allocated.</span></span>



| <span data-ttu-id="ab1c9-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ab1c9-107">Entry</span></span> | <span data-ttu-id="ab1c9-108">Wert</span><span class="sxs-lookup"><span data-stu-id="ab1c9-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ab1c9-109">CN</span><span class="sxs-lookup"><span data-stu-id="ab1c9-109">CN</span></span>                | <span data-ttu-id="ab1c9-110">Rid-available-Pool</span><span class="sxs-lookup"><span data-stu-id="ab1c9-110">RID-Available-Pool</span></span>                   |
| <span data-ttu-id="ab1c9-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ab1c9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ab1c9-112">ridavailablepool</span><span class="sxs-lookup"><span data-stu-id="ab1c9-112">rIDAvailablePool</span></span>                     |
| <span data-ttu-id="ab1c9-113">Size</span><span class="sxs-lookup"><span data-stu-id="ab1c9-113">Size</span></span>              | <span data-ttu-id="ab1c9-114">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="ab1c9-114">8 bytes</span></span>                              |
| <span data-ttu-id="ab1c9-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ab1c9-115">Update Privilege</span></span>  | <span data-ttu-id="ab1c9-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ab1c9-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="ab1c9-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="ab1c9-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ab1c9-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ab1c9-118">Attribute-Id</span></span>      | <span data-ttu-id="ab1c9-119">1.2.840.113556.1.4.370</span><span class="sxs-lookup"><span data-stu-id="ab1c9-119">1.2.840.113556.1.4.370</span></span>               |
| <span data-ttu-id="ab1c9-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ab1c9-120">System-Id-Guid</span></span>    | <span data-ttu-id="ab1c9-121">66171888-8F -11D0-AFDA-00c04f-930c9</span><span class="sxs-lookup"><span data-stu-id="ab1c9-121">66171888-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="ab1c9-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab1c9-122">Syntax</span></span>            | [<span data-ttu-id="ab1c9-123">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="ab1c9-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="ab1c9-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="ab1c9-124">Implementations</span></span>

-   [<span data-ttu-id="ab1c9-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ab1c9-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ab1c9-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ab1c9-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ab1c9-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ab1c9-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ab1c9-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ab1c9-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ab1c9-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ab1c9-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ab1c9-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ab1c9-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ab1c9-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ab1c9-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ab1c9-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ab1c9-132">Entry</span></span> | <span data-ttu-id="ab1c9-133">Wert</span><span class="sxs-lookup"><span data-stu-id="ab1c9-133">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="ab1c9-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ab1c9-134">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="ab1c9-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab1c9-135">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="ab1c9-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab1c9-136">System-Only</span></span>            | <span data-ttu-id="ab1c9-137">False</span><span class="sxs-lookup"><span data-stu-id="ab1c9-137">False</span></span>                                          |
| <span data-ttu-id="ab1c9-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ab1c9-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ab1c9-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="ab1c9-139">True</span></span>                                           |
| <span data-ttu-id="ab1c9-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ab1c9-140">Is Indexed</span></span>             | <span data-ttu-id="ab1c9-141">False</span><span class="sxs-lookup"><span data-stu-id="ab1c9-141">False</span></span>                                          |
| <span data-ttu-id="ab1c9-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ab1c9-142">In Global Catalog</span></span>      | <span data-ttu-id="ab1c9-143">False</span><span class="sxs-lookup"><span data-stu-id="ab1c9-143">False</span></span>                                          |
| <span data-ttu-id="ab1c9-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ab1c9-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab1c9-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ab1c9-145">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="ab1c9-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab1c9-146">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="ab1c9-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab1c9-147">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="ab1c9-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab1c9-148">Search-Flags</span></span>           | <span data-ttu-id="ab1c9-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab1c9-149">0x00000000</span></span>                                     |
| <span data-ttu-id="ab1c9-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab1c9-150">System-Flags</span></span>           | <span data-ttu-id="ab1c9-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab1c9-151">0x00000010</span></span>                                     |
| <span data-ttu-id="ab1c9-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ab1c9-152">Classes used in</span></span>        | [<span data-ttu-id="ab1c9-153">**RID-Manager**</span><span class="sxs-lookup"><span data-stu-id="ab1c9-153">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ab1c9-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ab1c9-154">Windows Server 2003</span></span>



| <span data-ttu-id="ab1c9-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ab1c9-155">Entry</span></span> | <span data-ttu-id="ab1c9-156">Wert</span><span class="sxs-lookup"><span data-stu-id="ab1c9-156">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="ab1c9-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ab1c9-157">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="ab1c9-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab1c9-158">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="ab1c9-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab1c9-159">System-Only</span></span>            | <span data-ttu-id="ab1c9-160">False</span><span class="sxs-lookup"><span data-stu-id="ab1c9-160">False</span></span>                                          |
| <span data-ttu-id="ab1c9-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ab1c9-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ab1c9-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="ab1c9-162">True</span></span>                                           |
| <span data-ttu-id="ab1c9-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ab1c9-163">Is Indexed</span></span>             | <span data-ttu-id="ab1c9-164">False</span><span class="sxs-lookup"><span data-stu-id="ab1c9-164">False</span></span>                                          |
| <span data-ttu-id="ab1c9-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ab1c9-165">In Global Catalog</span></span>      | <span data-ttu-id="ab1c9-166">False</span><span class="sxs-lookup"><span data-stu-id="ab1c9-166">False</span></span>                                          |
| <span data-ttu-id="ab1c9-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ab1c9-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab1c9-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ab1c9-168">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="ab1c9-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab1c9-169">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="ab1c9-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab1c9-170">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="ab1c9-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab1c9-171">Search-Flags</span></span>           | <span data-ttu-id="ab1c9-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab1c9-172">0x00000000</span></span>                                     |
| <span data-ttu-id="ab1c9-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab1c9-173">System-Flags</span></span>           | <span data-ttu-id="ab1c9-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab1c9-174">0x00000010</span></span>                                     |
| <span data-ttu-id="ab1c9-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ab1c9-175">Classes used in</span></span>        | [<span data-ttu-id="ab1c9-176">**RID-Manager**</span><span class="sxs-lookup"><span data-stu-id="ab1c9-176">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ab1c9-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ab1c9-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ab1c9-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ab1c9-178">Entry</span></span> | <span data-ttu-id="ab1c9-179">Wert</span><span class="sxs-lookup"><span data-stu-id="ab1c9-179">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="ab1c9-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ab1c9-180">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="ab1c9-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab1c9-181">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="ab1c9-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab1c9-182">System-Only</span></span>            | <span data-ttu-id="ab1c9-183">False</span><span class="sxs-lookup"><span data-stu-id="ab1c9-183">False</span></span>                                          |
| <span data-ttu-id="ab1c9-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ab1c9-184">Is-Single-Valued</span></span>       | <span data-ttu-id="ab1c9-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="ab1c9-185">True</span></span>                                           |
| <span data-ttu-id="ab1c9-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ab1c9-186">Is Indexed</span></span>             | <span data-ttu-id="ab1c9-187">False</span><span class="sxs-lookup"><span data-stu-id="ab1c9-187">False</span></span>                                          |
| <span data-ttu-id="ab1c9-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ab1c9-188">In Global Catalog</span></span>      | <span data-ttu-id="ab1c9-189">False</span><span class="sxs-lookup"><span data-stu-id="ab1c9-189">False</span></span>                                          |
| <span data-ttu-id="ab1c9-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ab1c9-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab1c9-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ab1c9-191">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="ab1c9-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab1c9-192">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="ab1c9-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab1c9-193">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="ab1c9-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab1c9-194">Search-Flags</span></span>           | <span data-ttu-id="ab1c9-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab1c9-195">0x00000000</span></span>                                     |
| <span data-ttu-id="ab1c9-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab1c9-196">System-Flags</span></span>           | <span data-ttu-id="ab1c9-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab1c9-197">0x00000010</span></span>                                     |
| <span data-ttu-id="ab1c9-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ab1c9-198">Classes used in</span></span>        | [<span data-ttu-id="ab1c9-199">**RID-Manager**</span><span class="sxs-lookup"><span data-stu-id="ab1c9-199">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ab1c9-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab1c9-200">Windows Server 2008</span></span>



| <span data-ttu-id="ab1c9-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ab1c9-201">Entry</span></span> | <span data-ttu-id="ab1c9-202">Wert</span><span class="sxs-lookup"><span data-stu-id="ab1c9-202">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="ab1c9-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ab1c9-203">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="ab1c9-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab1c9-204">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="ab1c9-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab1c9-205">System-Only</span></span>            | <span data-ttu-id="ab1c9-206">False</span><span class="sxs-lookup"><span data-stu-id="ab1c9-206">False</span></span>                                          |
| <span data-ttu-id="ab1c9-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ab1c9-207">Is-Single-Valued</span></span>       | <span data-ttu-id="ab1c9-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="ab1c9-208">True</span></span>                                           |
| <span data-ttu-id="ab1c9-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ab1c9-209">Is Indexed</span></span>             | <span data-ttu-id="ab1c9-210">False</span><span class="sxs-lookup"><span data-stu-id="ab1c9-210">False</span></span>                                          |
| <span data-ttu-id="ab1c9-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ab1c9-211">In Global Catalog</span></span>      | <span data-ttu-id="ab1c9-212">False</span><span class="sxs-lookup"><span data-stu-id="ab1c9-212">False</span></span>                                          |
| <span data-ttu-id="ab1c9-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ab1c9-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab1c9-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ab1c9-214">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="ab1c9-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab1c9-215">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="ab1c9-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab1c9-216">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="ab1c9-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab1c9-217">Search-Flags</span></span>           | <span data-ttu-id="ab1c9-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab1c9-218">0x00000000</span></span>                                     |
| <span data-ttu-id="ab1c9-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab1c9-219">System-Flags</span></span>           | <span data-ttu-id="ab1c9-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab1c9-220">0x00000010</span></span>                                     |
| <span data-ttu-id="ab1c9-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ab1c9-221">Classes used in</span></span>        | [<span data-ttu-id="ab1c9-222">**RID-Manager**</span><span class="sxs-lookup"><span data-stu-id="ab1c9-222">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ab1c9-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ab1c9-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ab1c9-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ab1c9-224">Entry</span></span> | <span data-ttu-id="ab1c9-225">Wert</span><span class="sxs-lookup"><span data-stu-id="ab1c9-225">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="ab1c9-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ab1c9-226">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="ab1c9-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab1c9-227">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="ab1c9-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab1c9-228">System-Only</span></span>            | <span data-ttu-id="ab1c9-229">False</span><span class="sxs-lookup"><span data-stu-id="ab1c9-229">False</span></span>                                          |
| <span data-ttu-id="ab1c9-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ab1c9-230">Is-Single-Valued</span></span>       | <span data-ttu-id="ab1c9-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="ab1c9-231">True</span></span>                                           |
| <span data-ttu-id="ab1c9-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ab1c9-232">Is Indexed</span></span>             | <span data-ttu-id="ab1c9-233">False</span><span class="sxs-lookup"><span data-stu-id="ab1c9-233">False</span></span>                                          |
| <span data-ttu-id="ab1c9-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ab1c9-234">In Global Catalog</span></span>      | <span data-ttu-id="ab1c9-235">False</span><span class="sxs-lookup"><span data-stu-id="ab1c9-235">False</span></span>                                          |
| <span data-ttu-id="ab1c9-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ab1c9-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab1c9-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ab1c9-237">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="ab1c9-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab1c9-238">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="ab1c9-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab1c9-239">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="ab1c9-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab1c9-240">Search-Flags</span></span>           | <span data-ttu-id="ab1c9-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab1c9-241">0x00000000</span></span>                                     |
| <span data-ttu-id="ab1c9-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab1c9-242">System-Flags</span></span>           | <span data-ttu-id="ab1c9-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab1c9-243">0x00000010</span></span>                                     |
| <span data-ttu-id="ab1c9-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ab1c9-244">Classes used in</span></span>        | [<span data-ttu-id="ab1c9-245">**RID-Manager**</span><span class="sxs-lookup"><span data-stu-id="ab1c9-245">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ab1c9-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ab1c9-246">Windows Server 2012</span></span>



| <span data-ttu-id="ab1c9-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ab1c9-247">Entry</span></span> | <span data-ttu-id="ab1c9-248">Wert</span><span class="sxs-lookup"><span data-stu-id="ab1c9-248">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="ab1c9-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ab1c9-249">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="ab1c9-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab1c9-250">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="ab1c9-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab1c9-251">System-Only</span></span>            | <span data-ttu-id="ab1c9-252">False</span><span class="sxs-lookup"><span data-stu-id="ab1c9-252">False</span></span>                                          |
| <span data-ttu-id="ab1c9-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ab1c9-253">Is-Single-Valued</span></span>       | <span data-ttu-id="ab1c9-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="ab1c9-254">True</span></span>                                           |
| <span data-ttu-id="ab1c9-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ab1c9-255">Is Indexed</span></span>             | <span data-ttu-id="ab1c9-256">False</span><span class="sxs-lookup"><span data-stu-id="ab1c9-256">False</span></span>                                          |
| <span data-ttu-id="ab1c9-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ab1c9-257">In Global Catalog</span></span>      | <span data-ttu-id="ab1c9-258">False</span><span class="sxs-lookup"><span data-stu-id="ab1c9-258">False</span></span>                                          |
| <span data-ttu-id="ab1c9-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ab1c9-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab1c9-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ab1c9-260">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="ab1c9-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab1c9-261">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="ab1c9-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab1c9-262">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="ab1c9-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab1c9-263">Search-Flags</span></span>           | <span data-ttu-id="ab1c9-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab1c9-264">0x00000000</span></span>                                     |
| <span data-ttu-id="ab1c9-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab1c9-265">System-Flags</span></span>           | <span data-ttu-id="ab1c9-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab1c9-266">0x00000010</span></span>                                     |
| <span data-ttu-id="ab1c9-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ab1c9-267">Classes used in</span></span>        | [<span data-ttu-id="ab1c9-268">**RID-Manager**</span><span class="sxs-lookup"><span data-stu-id="ab1c9-268">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



 

 





