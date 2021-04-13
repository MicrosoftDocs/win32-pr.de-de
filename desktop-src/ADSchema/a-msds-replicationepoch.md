---
title: ms-DS-ReplicationEpoch-Attribut
description: Diese wird verwendet, um die Epoche aufzunehmen, in der alle DCS replizieren. Eine Epoche ist die Zeitspanne, in der eine Domäne einen bestimmten Namen aufweist. Eine neue Epoche beginnt, wenn eine Domänen Namensänderung auftritt.
ms.assetid: d8a3c4fd-f416-483f-820f-7b3182d0bfc3
ms.tgt_platform: multiple
keywords:
- AD-Schema des ms-DS-ReplicationEpoch-Attributs
- AD-Schema des msDS-ReplicationEpoch-Attributs
topic_type:
- apiref
api_name:
- ms-DS-ReplicationEpoch
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef9aaefefe5cd1ae269508390ae13f67037fdb8a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519807"
---
# <a name="ms-ds-replicationepoch-attribute"></a><span data-ttu-id="c3882-107">ms-DS-ReplicationEpoch-Attribut</span><span class="sxs-lookup"><span data-stu-id="c3882-107">ms-DS-ReplicationEpoch attribute</span></span>

<span data-ttu-id="c3882-108">Diese wird verwendet, um die Epoche aufzunehmen, in der alle DCS replizieren.</span><span class="sxs-lookup"><span data-stu-id="c3882-108">This is used to hold the epoch under which all the DCs are replicating.</span></span> <span data-ttu-id="c3882-109">Eine Epoche ist die Zeitspanne, in der eine Domäne einen bestimmten Namen aufweist.</span><span class="sxs-lookup"><span data-stu-id="c3882-109">An epoch is the period of time in which a domain has a specific name.</span></span> <span data-ttu-id="c3882-110">Eine neue Epoche beginnt, wenn eine Domänen Namensänderung auftritt.</span><span class="sxs-lookup"><span data-stu-id="c3882-110">A new epoch starts when a domain name change occurs.</span></span>



| <span data-ttu-id="c3882-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c3882-111">Entry</span></span> | <span data-ttu-id="c3882-112">Wert</span><span class="sxs-lookup"><span data-stu-id="c3882-112">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c3882-113">CN</span><span class="sxs-lookup"><span data-stu-id="c3882-113">CN</span></span>                | <span data-ttu-id="c3882-114">ms-DS-ReplicationEpoch</span><span class="sxs-lookup"><span data-stu-id="c3882-114">ms-DS-ReplicationEpoch</span></span>               |
| <span data-ttu-id="c3882-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c3882-115">Ldap-Display-Name</span></span> | <span data-ttu-id="c3882-116">MSDS-ReplicationEpoch</span><span class="sxs-lookup"><span data-stu-id="c3882-116">msDS-ReplicationEpoch</span></span>                |
| <span data-ttu-id="c3882-117">Size</span><span class="sxs-lookup"><span data-stu-id="c3882-117">Size</span></span>              | \-                                   |
| <span data-ttu-id="c3882-118">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c3882-118">Update Privilege</span></span>  | <span data-ttu-id="c3882-119">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3882-119">This value is set by the system.</span></span>     |
| <span data-ttu-id="c3882-120">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="c3882-120">Update Frequency</span></span>  | <span data-ttu-id="c3882-121">Nur während der Domänen Umstrukturierung.</span><span class="sxs-lookup"><span data-stu-id="c3882-121">Only during domain restructure.</span></span>      |
| <span data-ttu-id="c3882-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c3882-122">Attribute-Id</span></span>      | <span data-ttu-id="c3882-123">1.2.840.113556.1.4.1720</span><span class="sxs-lookup"><span data-stu-id="c3882-123">1.2.840.113556.1.4.1720</span></span>              |
| <span data-ttu-id="c3882-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c3882-124">System-Id-Guid</span></span>    | <span data-ttu-id="c3882-125">08e3aa79-eb1c-45b5-af7b-8l94246c8e41</span><span class="sxs-lookup"><span data-stu-id="c3882-125">08e3aa79-eb1c-45b5-af7b-8f94246c8e41</span></span> |
| <span data-ttu-id="c3882-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3882-126">Syntax</span></span>            | [<span data-ttu-id="c3882-127">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="c3882-127">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="c3882-128">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="c3882-128">Implementations</span></span>

-   [<span data-ttu-id="c3882-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c3882-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c3882-130">**Adam**</span><span class="sxs-lookup"><span data-stu-id="c3882-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c3882-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c3882-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c3882-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c3882-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c3882-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c3882-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c3882-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c3882-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c3882-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c3882-135">Windows Server 2003</span></span>



| <span data-ttu-id="c3882-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c3882-136">Entry</span></span> | <span data-ttu-id="c3882-137">Wert</span><span class="sxs-lookup"><span data-stu-id="c3882-137">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c3882-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c3882-138">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3882-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3882-139">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3882-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3882-140">System-Only</span></span>            | <span data-ttu-id="c3882-141">False</span><span class="sxs-lookup"><span data-stu-id="c3882-141">False</span></span>                                    |
| <span data-ttu-id="c3882-142">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c3882-142">Is-Single-Valued</span></span>       | <span data-ttu-id="c3882-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="c3882-143">True</span></span>                                     |
| <span data-ttu-id="c3882-144">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c3882-144">Is Indexed</span></span>             | <span data-ttu-id="c3882-145">False</span><span class="sxs-lookup"><span data-stu-id="c3882-145">False</span></span>                                    |
| <span data-ttu-id="c3882-146">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c3882-146">In Global Catalog</span></span>      | <span data-ttu-id="c3882-147">False</span><span class="sxs-lookup"><span data-stu-id="c3882-147">False</span></span>                                    |
| <span data-ttu-id="c3882-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c3882-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3882-149">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c3882-149">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c3882-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3882-150">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c3882-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3882-151">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c3882-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3882-152">Search-Flags</span></span>           | <span data-ttu-id="c3882-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3882-153">0x00000000</span></span>                               |
| <span data-ttu-id="c3882-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3882-154">System-Flags</span></span>           | <span data-ttu-id="c3882-155">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c3882-155">0x00000011</span></span>                               |
| <span data-ttu-id="c3882-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c3882-156">Classes used in</span></span>        | [<span data-ttu-id="c3882-157">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c3882-157">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c3882-158">Adam</span><span class="sxs-lookup"><span data-stu-id="c3882-158">ADAM</span></span>



| <span data-ttu-id="c3882-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c3882-159">Entry</span></span> | <span data-ttu-id="c3882-160">Wert</span><span class="sxs-lookup"><span data-stu-id="c3882-160">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c3882-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c3882-161">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3882-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3882-162">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3882-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3882-163">System-Only</span></span>            | <span data-ttu-id="c3882-164">False</span><span class="sxs-lookup"><span data-stu-id="c3882-164">False</span></span>                                    |
| <span data-ttu-id="c3882-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c3882-165">Is-Single-Valued</span></span>       | <span data-ttu-id="c3882-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="c3882-166">True</span></span>                                     |
| <span data-ttu-id="c3882-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c3882-167">Is Indexed</span></span>             | <span data-ttu-id="c3882-168">False</span><span class="sxs-lookup"><span data-stu-id="c3882-168">False</span></span>                                    |
| <span data-ttu-id="c3882-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c3882-169">In Global Catalog</span></span>      | <span data-ttu-id="c3882-170">False</span><span class="sxs-lookup"><span data-stu-id="c3882-170">False</span></span>                                    |
| <span data-ttu-id="c3882-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c3882-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3882-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c3882-172">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c3882-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3882-173">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c3882-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3882-174">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c3882-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3882-175">Search-Flags</span></span>           | <span data-ttu-id="c3882-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3882-176">0x00000000</span></span>                               |
| <span data-ttu-id="c3882-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3882-177">System-Flags</span></span>           | <span data-ttu-id="c3882-178">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c3882-178">0x00000011</span></span>                               |
| <span data-ttu-id="c3882-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c3882-179">Classes used in</span></span>        | [<span data-ttu-id="c3882-180">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c3882-180">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c3882-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c3882-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c3882-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c3882-182">Entry</span></span> | <span data-ttu-id="c3882-183">Wert</span><span class="sxs-lookup"><span data-stu-id="c3882-183">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c3882-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c3882-184">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3882-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3882-185">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3882-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3882-186">System-Only</span></span>            | <span data-ttu-id="c3882-187">False</span><span class="sxs-lookup"><span data-stu-id="c3882-187">False</span></span>                                    |
| <span data-ttu-id="c3882-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c3882-188">Is-Single-Valued</span></span>       | <span data-ttu-id="c3882-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="c3882-189">True</span></span>                                     |
| <span data-ttu-id="c3882-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c3882-190">Is Indexed</span></span>             | <span data-ttu-id="c3882-191">False</span><span class="sxs-lookup"><span data-stu-id="c3882-191">False</span></span>                                    |
| <span data-ttu-id="c3882-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c3882-192">In Global Catalog</span></span>      | <span data-ttu-id="c3882-193">False</span><span class="sxs-lookup"><span data-stu-id="c3882-193">False</span></span>                                    |
| <span data-ttu-id="c3882-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c3882-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3882-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c3882-195">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c3882-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3882-196">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c3882-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3882-197">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c3882-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3882-198">Search-Flags</span></span>           | <span data-ttu-id="c3882-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3882-199">0x00000000</span></span>                               |
| <span data-ttu-id="c3882-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3882-200">System-Flags</span></span>           | <span data-ttu-id="c3882-201">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c3882-201">0x00000011</span></span>                               |
| <span data-ttu-id="c3882-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c3882-202">Classes used in</span></span>        | [<span data-ttu-id="c3882-203">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c3882-203">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c3882-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3882-204">Windows Server 2008</span></span>



| <span data-ttu-id="c3882-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c3882-205">Entry</span></span> | <span data-ttu-id="c3882-206">Wert</span><span class="sxs-lookup"><span data-stu-id="c3882-206">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c3882-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c3882-207">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3882-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3882-208">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3882-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3882-209">System-Only</span></span>            | <span data-ttu-id="c3882-210">False</span><span class="sxs-lookup"><span data-stu-id="c3882-210">False</span></span>                                    |
| <span data-ttu-id="c3882-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c3882-211">Is-Single-Valued</span></span>       | <span data-ttu-id="c3882-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="c3882-212">True</span></span>                                     |
| <span data-ttu-id="c3882-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c3882-213">Is Indexed</span></span>             | <span data-ttu-id="c3882-214">False</span><span class="sxs-lookup"><span data-stu-id="c3882-214">False</span></span>                                    |
| <span data-ttu-id="c3882-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c3882-215">In Global Catalog</span></span>      | <span data-ttu-id="c3882-216">False</span><span class="sxs-lookup"><span data-stu-id="c3882-216">False</span></span>                                    |
| <span data-ttu-id="c3882-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c3882-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3882-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c3882-218">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c3882-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3882-219">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c3882-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3882-220">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c3882-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3882-221">Search-Flags</span></span>           | <span data-ttu-id="c3882-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3882-222">0x00000000</span></span>                               |
| <span data-ttu-id="c3882-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3882-223">System-Flags</span></span>           | <span data-ttu-id="c3882-224">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c3882-224">0x00000011</span></span>                               |
| <span data-ttu-id="c3882-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c3882-225">Classes used in</span></span>        | [<span data-ttu-id="c3882-226">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c3882-226">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c3882-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c3882-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c3882-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c3882-228">Entry</span></span> | <span data-ttu-id="c3882-229">Wert</span><span class="sxs-lookup"><span data-stu-id="c3882-229">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c3882-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c3882-230">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3882-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3882-231">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3882-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3882-232">System-Only</span></span>            | <span data-ttu-id="c3882-233">False</span><span class="sxs-lookup"><span data-stu-id="c3882-233">False</span></span>                                    |
| <span data-ttu-id="c3882-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c3882-234">Is-Single-Valued</span></span>       | <span data-ttu-id="c3882-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="c3882-235">True</span></span>                                     |
| <span data-ttu-id="c3882-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c3882-236">Is Indexed</span></span>             | <span data-ttu-id="c3882-237">False</span><span class="sxs-lookup"><span data-stu-id="c3882-237">False</span></span>                                    |
| <span data-ttu-id="c3882-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c3882-238">In Global Catalog</span></span>      | <span data-ttu-id="c3882-239">False</span><span class="sxs-lookup"><span data-stu-id="c3882-239">False</span></span>                                    |
| <span data-ttu-id="c3882-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c3882-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3882-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c3882-241">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c3882-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3882-242">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c3882-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3882-243">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c3882-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3882-244">Search-Flags</span></span>           | <span data-ttu-id="c3882-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3882-245">0x00000000</span></span>                               |
| <span data-ttu-id="c3882-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3882-246">System-Flags</span></span>           | <span data-ttu-id="c3882-247">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c3882-247">0x00000011</span></span>                               |
| <span data-ttu-id="c3882-248">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c3882-248">Classes used in</span></span>        | [<span data-ttu-id="c3882-249">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c3882-249">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c3882-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c3882-250">Windows Server 2012</span></span>



| <span data-ttu-id="c3882-251">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c3882-251">Entry</span></span> | <span data-ttu-id="c3882-252">Wert</span><span class="sxs-lookup"><span data-stu-id="c3882-252">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c3882-253">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c3882-253">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3882-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3882-254">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3882-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3882-255">System-Only</span></span>            | <span data-ttu-id="c3882-256">False</span><span class="sxs-lookup"><span data-stu-id="c3882-256">False</span></span>                                    |
| <span data-ttu-id="c3882-257">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c3882-257">Is-Single-Valued</span></span>       | <span data-ttu-id="c3882-258">Richtig</span><span class="sxs-lookup"><span data-stu-id="c3882-258">True</span></span>                                     |
| <span data-ttu-id="c3882-259">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c3882-259">Is Indexed</span></span>             | <span data-ttu-id="c3882-260">False</span><span class="sxs-lookup"><span data-stu-id="c3882-260">False</span></span>                                    |
| <span data-ttu-id="c3882-261">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c3882-261">In Global Catalog</span></span>      | <span data-ttu-id="c3882-262">False</span><span class="sxs-lookup"><span data-stu-id="c3882-262">False</span></span>                                    |
| <span data-ttu-id="c3882-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c3882-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3882-264">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c3882-264">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c3882-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3882-265">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c3882-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3882-266">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c3882-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3882-267">Search-Flags</span></span>           | <span data-ttu-id="c3882-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3882-268">0x00000000</span></span>                               |
| <span data-ttu-id="c3882-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3882-269">System-Flags</span></span>           | <span data-ttu-id="c3882-270">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c3882-270">0x00000011</span></span>                               |
| <span data-ttu-id="c3882-271">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c3882-271">Classes used in</span></span>        | [<span data-ttu-id="c3882-272">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c3882-272">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





