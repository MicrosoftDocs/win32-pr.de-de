---
title: ms-DS-NC-repl-Outbound-Nachbarn-Attribut
description: Replikations Partner für diese Partition. Dieser Server sendet Replikations Daten an diese anderen Server, die als Ziele fungieren. Dieser Server benachrichtigt diese anderen Server, wenn neue Daten verfügbar sind.
ms.assetid: 9dcc7485-1999-47ff-bb57-8193768a15a9
ms.tgt_platform: multiple
keywords:
- "\"ms-DS-NC-repl-Outbound-Neighbors\"-Attribut AD-Schema"
- AD-Schema des msDS-nkreploutboundneighbors-Attributs
topic_type:
- apiref
api_name:
- ms-DS-NC-Repl-Outbound-Neighbors
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fd37ccab1b3faef6ca2c84a52c05249a52ff38a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859685"
---
# <a name="ms-ds-nc-repl-outbound-neighbors-attribute"></a><span data-ttu-id="b64b0-107">ms-DS-NC-repl-Outbound-Nachbarn-Attribut</span><span class="sxs-lookup"><span data-stu-id="b64b0-107">ms-DS-NC-Repl-Outbound-Neighbors attribute</span></span>

<span data-ttu-id="b64b0-108">Replikations Partner für diese Partition.</span><span class="sxs-lookup"><span data-stu-id="b64b0-108">Replication partners for this partition.</span></span> <span data-ttu-id="b64b0-109">Dieser Server sendet Replikations Daten an diese anderen Server, die als Ziele fungieren.</span><span class="sxs-lookup"><span data-stu-id="b64b0-109">This server sends replication data to these other servers, which act as destinations.</span></span> <span data-ttu-id="b64b0-110">Dieser Server benachrichtigt diese anderen Server, wenn neue Daten verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b64b0-110">This server will notify these other servers when new data is available.</span></span>



| <span data-ttu-id="b64b0-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b64b0-111">Entry</span></span> | <span data-ttu-id="b64b0-112">Wert</span><span class="sxs-lookup"><span data-stu-id="b64b0-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b64b0-113">CN</span><span class="sxs-lookup"><span data-stu-id="b64b0-113">CN</span></span>                | <span data-ttu-id="b64b0-114">ms-DS-NC-repl-Outbound-Nachbarn</span><span class="sxs-lookup"><span data-stu-id="b64b0-114">ms-DS-NC-Repl-Outbound-Neighbors</span></span>            |
| <span data-ttu-id="b64b0-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b64b0-115">Ldap-Display-Name</span></span> | <span data-ttu-id="b64b0-116">MSDS-nkreploutboundnachbarn</span><span class="sxs-lookup"><span data-stu-id="b64b0-116">msDS-NCReplOutboundNeighbors</span></span>                |
| <span data-ttu-id="b64b0-117">Size</span><span class="sxs-lookup"><span data-stu-id="b64b0-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="b64b0-118">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b64b0-118">Update Privilege</span></span>  | <span data-ttu-id="b64b0-119">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b64b0-119">This value is set by the system.</span></span>            |
| <span data-ttu-id="b64b0-120">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="b64b0-120">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="b64b0-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b64b0-121">Attribute-Id</span></span>      | <span data-ttu-id="b64b0-122">1.2.840.113556.1.4.1706</span><span class="sxs-lookup"><span data-stu-id="b64b0-122">1.2.840.113556.1.4.1706</span></span>                     |
| <span data-ttu-id="b64b0-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b64b0-123">System-Id-Guid</span></span>    | <span data-ttu-id="b64b0-124">855b61ef5-a1c5-4cc4-ba6d-32522848b61f</span><span class="sxs-lookup"><span data-stu-id="b64b0-124">855f2ef5-a1c5-4cc4-ba6d-32522848b61f</span></span>        |
| <span data-ttu-id="b64b0-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="b64b0-125">Syntax</span></span>            | [<span data-ttu-id="b64b0-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b64b0-126">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b64b0-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="b64b0-127">Implementations</span></span>

-   [<span data-ttu-id="b64b0-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b64b0-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b64b0-129">**Adam**</span><span class="sxs-lookup"><span data-stu-id="b64b0-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b64b0-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b64b0-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b64b0-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b64b0-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b64b0-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b64b0-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b64b0-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b64b0-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b64b0-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b64b0-134">Windows Server 2003</span></span>



| <span data-ttu-id="b64b0-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b64b0-135">Entry</span></span> | <span data-ttu-id="b64b0-136">Wert</span><span class="sxs-lookup"><span data-stu-id="b64b0-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b64b0-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b64b0-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b64b0-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b64b0-138">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b64b0-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="b64b0-139">System-Only</span></span>            | <span data-ttu-id="b64b0-140">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-140">False</span></span>                           |
| <span data-ttu-id="b64b0-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b64b0-141">Is-Single-Valued</span></span>       | <span data-ttu-id="b64b0-142">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-142">False</span></span>                           |
| <span data-ttu-id="b64b0-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b64b0-143">Is Indexed</span></span>             | <span data-ttu-id="b64b0-144">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-144">False</span></span>                           |
| <span data-ttu-id="b64b0-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b64b0-145">In Global Catalog</span></span>      | <span data-ttu-id="b64b0-146">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-146">False</span></span>                           |
| <span data-ttu-id="b64b0-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b64b0-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="b64b0-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b64b0-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b64b0-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b64b0-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b64b0-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b64b0-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b64b0-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b64b0-151">Search-Flags</span></span>           | <span data-ttu-id="b64b0-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b64b0-152">0x00000000</span></span>                      |
| <span data-ttu-id="b64b0-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b64b0-153">System-Flags</span></span>           | <span data-ttu-id="b64b0-154">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b64b0-154">0x00000014</span></span>                      |
| <span data-ttu-id="b64b0-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b64b0-155">Classes used in</span></span>        | [<span data-ttu-id="b64b0-156">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b64b0-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b64b0-157">Adam</span><span class="sxs-lookup"><span data-stu-id="b64b0-157">ADAM</span></span>



| <span data-ttu-id="b64b0-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b64b0-158">Entry</span></span> | <span data-ttu-id="b64b0-159">Wert</span><span class="sxs-lookup"><span data-stu-id="b64b0-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b64b0-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b64b0-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b64b0-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b64b0-161">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b64b0-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="b64b0-162">System-Only</span></span>            | <span data-ttu-id="b64b0-163">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-163">False</span></span>                           |
| <span data-ttu-id="b64b0-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b64b0-164">Is-Single-Valued</span></span>       | <span data-ttu-id="b64b0-165">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-165">False</span></span>                           |
| <span data-ttu-id="b64b0-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b64b0-166">Is Indexed</span></span>             | <span data-ttu-id="b64b0-167">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-167">False</span></span>                           |
| <span data-ttu-id="b64b0-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b64b0-168">In Global Catalog</span></span>      | <span data-ttu-id="b64b0-169">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-169">False</span></span>                           |
| <span data-ttu-id="b64b0-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b64b0-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="b64b0-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b64b0-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b64b0-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b64b0-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b64b0-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b64b0-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b64b0-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b64b0-174">Search-Flags</span></span>           | <span data-ttu-id="b64b0-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b64b0-175">0x00000000</span></span>                      |
| <span data-ttu-id="b64b0-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b64b0-176">System-Flags</span></span>           | <span data-ttu-id="b64b0-177">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b64b0-177">0x00000014</span></span>                      |
| <span data-ttu-id="b64b0-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b64b0-178">Classes used in</span></span>        | [<span data-ttu-id="b64b0-179">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b64b0-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b64b0-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b64b0-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b64b0-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b64b0-181">Entry</span></span> | <span data-ttu-id="b64b0-182">Wert</span><span class="sxs-lookup"><span data-stu-id="b64b0-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b64b0-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b64b0-183">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b64b0-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b64b0-184">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b64b0-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="b64b0-185">System-Only</span></span>            | <span data-ttu-id="b64b0-186">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-186">False</span></span>                           |
| <span data-ttu-id="b64b0-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b64b0-187">Is-Single-Valued</span></span>       | <span data-ttu-id="b64b0-188">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-188">False</span></span>                           |
| <span data-ttu-id="b64b0-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b64b0-189">Is Indexed</span></span>             | <span data-ttu-id="b64b0-190">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-190">False</span></span>                           |
| <span data-ttu-id="b64b0-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b64b0-191">In Global Catalog</span></span>      | <span data-ttu-id="b64b0-192">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-192">False</span></span>                           |
| <span data-ttu-id="b64b0-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b64b0-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="b64b0-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b64b0-194">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b64b0-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b64b0-195">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b64b0-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b64b0-196">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b64b0-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b64b0-197">Search-Flags</span></span>           | <span data-ttu-id="b64b0-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b64b0-198">0x00000000</span></span>                      |
| <span data-ttu-id="b64b0-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b64b0-199">System-Flags</span></span>           | <span data-ttu-id="b64b0-200">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b64b0-200">0x00000014</span></span>                      |
| <span data-ttu-id="b64b0-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b64b0-201">Classes used in</span></span>        | [<span data-ttu-id="b64b0-202">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b64b0-202">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b64b0-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b64b0-203">Windows Server 2008</span></span>



| <span data-ttu-id="b64b0-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b64b0-204">Entry</span></span> | <span data-ttu-id="b64b0-205">Wert</span><span class="sxs-lookup"><span data-stu-id="b64b0-205">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b64b0-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b64b0-206">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b64b0-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b64b0-207">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b64b0-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="b64b0-208">System-Only</span></span>            | <span data-ttu-id="b64b0-209">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-209">False</span></span>                           |
| <span data-ttu-id="b64b0-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b64b0-210">Is-Single-Valued</span></span>       | <span data-ttu-id="b64b0-211">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-211">False</span></span>                           |
| <span data-ttu-id="b64b0-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b64b0-212">Is Indexed</span></span>             | <span data-ttu-id="b64b0-213">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-213">False</span></span>                           |
| <span data-ttu-id="b64b0-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b64b0-214">In Global Catalog</span></span>      | <span data-ttu-id="b64b0-215">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-215">False</span></span>                           |
| <span data-ttu-id="b64b0-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b64b0-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="b64b0-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b64b0-217">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b64b0-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b64b0-218">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b64b0-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b64b0-219">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b64b0-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b64b0-220">Search-Flags</span></span>           | <span data-ttu-id="b64b0-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b64b0-221">0x00000000</span></span>                      |
| <span data-ttu-id="b64b0-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b64b0-222">System-Flags</span></span>           | <span data-ttu-id="b64b0-223">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b64b0-223">0x00000014</span></span>                      |
| <span data-ttu-id="b64b0-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b64b0-224">Classes used in</span></span>        | [<span data-ttu-id="b64b0-225">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b64b0-225">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b64b0-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b64b0-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b64b0-227">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b64b0-227">Entry</span></span> | <span data-ttu-id="b64b0-228">Wert</span><span class="sxs-lookup"><span data-stu-id="b64b0-228">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b64b0-229">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b64b0-229">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b64b0-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b64b0-230">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b64b0-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="b64b0-231">System-Only</span></span>            | <span data-ttu-id="b64b0-232">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-232">False</span></span>                           |
| <span data-ttu-id="b64b0-233">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b64b0-233">Is-Single-Valued</span></span>       | <span data-ttu-id="b64b0-234">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-234">False</span></span>                           |
| <span data-ttu-id="b64b0-235">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b64b0-235">Is Indexed</span></span>             | <span data-ttu-id="b64b0-236">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-236">False</span></span>                           |
| <span data-ttu-id="b64b0-237">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b64b0-237">In Global Catalog</span></span>      | <span data-ttu-id="b64b0-238">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-238">False</span></span>                           |
| <span data-ttu-id="b64b0-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b64b0-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="b64b0-240">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b64b0-240">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b64b0-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b64b0-241">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b64b0-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b64b0-242">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b64b0-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b64b0-243">Search-Flags</span></span>           | <span data-ttu-id="b64b0-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b64b0-244">0x00000000</span></span>                      |
| <span data-ttu-id="b64b0-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b64b0-245">System-Flags</span></span>           | <span data-ttu-id="b64b0-246">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b64b0-246">0x00000014</span></span>                      |
| <span data-ttu-id="b64b0-247">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b64b0-247">Classes used in</span></span>        | [<span data-ttu-id="b64b0-248">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b64b0-248">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b64b0-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b64b0-249">Windows Server 2012</span></span>



| <span data-ttu-id="b64b0-250">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b64b0-250">Entry</span></span> | <span data-ttu-id="b64b0-251">Wert</span><span class="sxs-lookup"><span data-stu-id="b64b0-251">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b64b0-252">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b64b0-252">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b64b0-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b64b0-253">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b64b0-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="b64b0-254">System-Only</span></span>            | <span data-ttu-id="b64b0-255">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-255">False</span></span>                           |
| <span data-ttu-id="b64b0-256">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b64b0-256">Is-Single-Valued</span></span>       | <span data-ttu-id="b64b0-257">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-257">False</span></span>                           |
| <span data-ttu-id="b64b0-258">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b64b0-258">Is Indexed</span></span>             | <span data-ttu-id="b64b0-259">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-259">False</span></span>                           |
| <span data-ttu-id="b64b0-260">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b64b0-260">In Global Catalog</span></span>      | <span data-ttu-id="b64b0-261">False</span><span class="sxs-lookup"><span data-stu-id="b64b0-261">False</span></span>                           |
| <span data-ttu-id="b64b0-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b64b0-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="b64b0-263">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b64b0-263">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b64b0-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b64b0-264">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b64b0-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b64b0-265">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b64b0-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b64b0-266">Search-Flags</span></span>           | <span data-ttu-id="b64b0-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b64b0-267">0x00000000</span></span>                      |
| <span data-ttu-id="b64b0-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b64b0-268">System-Flags</span></span>           | <span data-ttu-id="b64b0-269">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b64b0-269">0x00000014</span></span>                      |
| <span data-ttu-id="b64b0-270">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b64b0-270">Classes used in</span></span>        | [<span data-ttu-id="b64b0-271">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b64b0-271">**Top**</span></span>](c-top.md)<br/> |



 

 





