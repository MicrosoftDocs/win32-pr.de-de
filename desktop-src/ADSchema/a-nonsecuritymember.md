---
title: Nicht-Security-Member-Attribut
description: Nicht Sicherheits Mitglieder einer Gruppe. Wird für Exchange-Verteilerlisten verwendet.
ms.assetid: 0db135e4-dcba-4afb-a174-3c7b2b40688e
ms.tgt_platform: multiple
keywords:
- AD-Schema für nicht-Sicherheits Mitglieder-Attribut
- nicht Securitymember-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Non-Security-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a04919d9d538ff4da97d73e79d14e9a2706032b8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957601"
---
# <a name="non-security-member-attribute"></a><span data-ttu-id="85be5-106">Nicht-Security-Member-Attribut</span><span class="sxs-lookup"><span data-stu-id="85be5-106">Non-Security-Member attribute</span></span>

<span data-ttu-id="85be5-107">Nicht Sicherheits Mitglieder einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="85be5-107">Nonsecurity members of a group.</span></span> <span data-ttu-id="85be5-108">Wird für Exchange-Verteilerlisten verwendet.</span><span class="sxs-lookup"><span data-stu-id="85be5-108">Used for Exchange distribution lists.</span></span>



| <span data-ttu-id="85be5-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="85be5-109">Entry</span></span> | <span data-ttu-id="85be5-110">Wert</span><span class="sxs-lookup"><span data-stu-id="85be5-110">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="85be5-111">CN</span><span class="sxs-lookup"><span data-stu-id="85be5-111">CN</span></span>                | <span data-ttu-id="85be5-112">Nicht sicherheitsmitglied</span><span class="sxs-lookup"><span data-stu-id="85be5-112">Non-Security-Member</span></span>                              |
| <span data-ttu-id="85be5-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="85be5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="85be5-114">nonsecuritymember</span><span class="sxs-lookup"><span data-stu-id="85be5-114">nonSecurityMember</span></span>                                |
| <span data-ttu-id="85be5-115">Size</span><span class="sxs-lookup"><span data-stu-id="85be5-115">Size</span></span>              | \-                                               |
| <span data-ttu-id="85be5-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="85be5-116">Update Privilege</span></span>  | <span data-ttu-id="85be5-117">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="85be5-117">Domain administrator</span></span>                             |
| <span data-ttu-id="85be5-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="85be5-118">Update Frequency</span></span>  | <span data-ttu-id="85be5-119">Jedes Mal, wenn ein Benutzer der DL hinzugefügt oder aus dieser entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="85be5-119">Whenever a user is added or removed from the DL.</span></span> |
| <span data-ttu-id="85be5-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="85be5-120">Attribute-Id</span></span>      | <span data-ttu-id="85be5-121">1.2.840.113556.1.4.530</span><span class="sxs-lookup"><span data-stu-id="85be5-121">1.2.840.113556.1.4.530</span></span>                           |
| <span data-ttu-id="85be5-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="85be5-122">System-Id-Guid</span></span>    | <span data-ttu-id="85be5-123">52458018-ca6a-11D0-affinf-0000f 80367c1</span><span class="sxs-lookup"><span data-stu-id="85be5-123">52458018-ca6a-11d0-afff-0000f80367c1</span></span>             |
| <span data-ttu-id="85be5-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="85be5-124">Syntax</span></span>            | [<span data-ttu-id="85be5-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="85be5-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)          |



## <a name="implementations"></a><span data-ttu-id="85be5-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="85be5-126">Implementations</span></span>

-   [<span data-ttu-id="85be5-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="85be5-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="85be5-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="85be5-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="85be5-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="85be5-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="85be5-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="85be5-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="85be5-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="85be5-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="85be5-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="85be5-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="85be5-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="85be5-133">Windows 2000 Server</span></span>



| <span data-ttu-id="85be5-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="85be5-134">Entry</span></span> | <span data-ttu-id="85be5-135">Wert</span><span class="sxs-lookup"><span data-stu-id="85be5-135">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="85be5-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="85be5-136">Link-Id</span></span>                | <span data-ttu-id="85be5-137">50</span><span class="sxs-lookup"><span data-stu-id="85be5-137">50</span></span>                                  |
| <span data-ttu-id="85be5-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85be5-138">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="85be5-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="85be5-139">System-Only</span></span>            | <span data-ttu-id="85be5-140">False</span><span class="sxs-lookup"><span data-stu-id="85be5-140">False</span></span>                               |
| <span data-ttu-id="85be5-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="85be5-141">Is-Single-Valued</span></span>       | <span data-ttu-id="85be5-142">False</span><span class="sxs-lookup"><span data-stu-id="85be5-142">False</span></span>                               |
| <span data-ttu-id="85be5-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="85be5-143">Is Indexed</span></span>             | <span data-ttu-id="85be5-144">False</span><span class="sxs-lookup"><span data-stu-id="85be5-144">False</span></span>                               |
| <span data-ttu-id="85be5-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="85be5-145">In Global Catalog</span></span>      | <span data-ttu-id="85be5-146">False</span><span class="sxs-lookup"><span data-stu-id="85be5-146">False</span></span>                               |
| <span data-ttu-id="85be5-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="85be5-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="85be5-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="85be5-148">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="85be5-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85be5-149">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="85be5-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85be5-150">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="85be5-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85be5-151">Search-Flags</span></span>           | <span data-ttu-id="85be5-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85be5-152">0x00000000</span></span>                          |
| <span data-ttu-id="85be5-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85be5-153">System-Flags</span></span>           | <span data-ttu-id="85be5-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85be5-154">0x00000010</span></span>                          |
| <span data-ttu-id="85be5-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="85be5-155">Classes used in</span></span>        | [<span data-ttu-id="85be5-156">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="85be5-156">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="85be5-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="85be5-157">Windows Server 2003</span></span>



| <span data-ttu-id="85be5-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="85be5-158">Entry</span></span> | <span data-ttu-id="85be5-159">Wert</span><span class="sxs-lookup"><span data-stu-id="85be5-159">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="85be5-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="85be5-160">Link-Id</span></span>                | <span data-ttu-id="85be5-161">50</span><span class="sxs-lookup"><span data-stu-id="85be5-161">50</span></span>                                  |
| <span data-ttu-id="85be5-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85be5-162">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="85be5-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="85be5-163">System-Only</span></span>            | <span data-ttu-id="85be5-164">False</span><span class="sxs-lookup"><span data-stu-id="85be5-164">False</span></span>                               |
| <span data-ttu-id="85be5-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="85be5-165">Is-Single-Valued</span></span>       | <span data-ttu-id="85be5-166">False</span><span class="sxs-lookup"><span data-stu-id="85be5-166">False</span></span>                               |
| <span data-ttu-id="85be5-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="85be5-167">Is Indexed</span></span>             | <span data-ttu-id="85be5-168">False</span><span class="sxs-lookup"><span data-stu-id="85be5-168">False</span></span>                               |
| <span data-ttu-id="85be5-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="85be5-169">In Global Catalog</span></span>      | <span data-ttu-id="85be5-170">False</span><span class="sxs-lookup"><span data-stu-id="85be5-170">False</span></span>                               |
| <span data-ttu-id="85be5-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="85be5-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="85be5-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="85be5-172">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="85be5-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85be5-173">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="85be5-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85be5-174">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="85be5-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85be5-175">Search-Flags</span></span>           | <span data-ttu-id="85be5-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85be5-176">0x00000000</span></span>                          |
| <span data-ttu-id="85be5-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85be5-177">System-Flags</span></span>           | <span data-ttu-id="85be5-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85be5-178">0x00000010</span></span>                          |
| <span data-ttu-id="85be5-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="85be5-179">Classes used in</span></span>        | [<span data-ttu-id="85be5-180">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="85be5-180">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="85be5-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="85be5-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="85be5-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="85be5-182">Entry</span></span> | <span data-ttu-id="85be5-183">Wert</span><span class="sxs-lookup"><span data-stu-id="85be5-183">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="85be5-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="85be5-184">Link-Id</span></span>                | <span data-ttu-id="85be5-185">50</span><span class="sxs-lookup"><span data-stu-id="85be5-185">50</span></span>                                  |
| <span data-ttu-id="85be5-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85be5-186">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="85be5-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="85be5-187">System-Only</span></span>            | <span data-ttu-id="85be5-188">False</span><span class="sxs-lookup"><span data-stu-id="85be5-188">False</span></span>                               |
| <span data-ttu-id="85be5-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="85be5-189">Is-Single-Valued</span></span>       | <span data-ttu-id="85be5-190">False</span><span class="sxs-lookup"><span data-stu-id="85be5-190">False</span></span>                               |
| <span data-ttu-id="85be5-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="85be5-191">Is Indexed</span></span>             | <span data-ttu-id="85be5-192">False</span><span class="sxs-lookup"><span data-stu-id="85be5-192">False</span></span>                               |
| <span data-ttu-id="85be5-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="85be5-193">In Global Catalog</span></span>      | <span data-ttu-id="85be5-194">False</span><span class="sxs-lookup"><span data-stu-id="85be5-194">False</span></span>                               |
| <span data-ttu-id="85be5-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="85be5-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="85be5-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="85be5-196">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="85be5-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85be5-197">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="85be5-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85be5-198">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="85be5-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85be5-199">Search-Flags</span></span>           | <span data-ttu-id="85be5-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85be5-200">0x00000000</span></span>                          |
| <span data-ttu-id="85be5-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85be5-201">System-Flags</span></span>           | <span data-ttu-id="85be5-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85be5-202">0x00000010</span></span>                          |
| <span data-ttu-id="85be5-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="85be5-203">Classes used in</span></span>        | [<span data-ttu-id="85be5-204">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="85be5-204">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="85be5-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85be5-205">Windows Server 2008</span></span>



| <span data-ttu-id="85be5-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="85be5-206">Entry</span></span> | <span data-ttu-id="85be5-207">Wert</span><span class="sxs-lookup"><span data-stu-id="85be5-207">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="85be5-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="85be5-208">Link-Id</span></span>                | <span data-ttu-id="85be5-209">50</span><span class="sxs-lookup"><span data-stu-id="85be5-209">50</span></span>                                  |
| <span data-ttu-id="85be5-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85be5-210">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="85be5-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="85be5-211">System-Only</span></span>            | <span data-ttu-id="85be5-212">False</span><span class="sxs-lookup"><span data-stu-id="85be5-212">False</span></span>                               |
| <span data-ttu-id="85be5-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="85be5-213">Is-Single-Valued</span></span>       | <span data-ttu-id="85be5-214">False</span><span class="sxs-lookup"><span data-stu-id="85be5-214">False</span></span>                               |
| <span data-ttu-id="85be5-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="85be5-215">Is Indexed</span></span>             | <span data-ttu-id="85be5-216">False</span><span class="sxs-lookup"><span data-stu-id="85be5-216">False</span></span>                               |
| <span data-ttu-id="85be5-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="85be5-217">In Global Catalog</span></span>      | <span data-ttu-id="85be5-218">False</span><span class="sxs-lookup"><span data-stu-id="85be5-218">False</span></span>                               |
| <span data-ttu-id="85be5-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="85be5-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="85be5-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="85be5-220">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="85be5-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85be5-221">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="85be5-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85be5-222">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="85be5-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85be5-223">Search-Flags</span></span>           | <span data-ttu-id="85be5-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85be5-224">0x00000000</span></span>                          |
| <span data-ttu-id="85be5-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85be5-225">System-Flags</span></span>           | <span data-ttu-id="85be5-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85be5-226">0x00000010</span></span>                          |
| <span data-ttu-id="85be5-227">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="85be5-227">Classes used in</span></span>        | [<span data-ttu-id="85be5-228">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="85be5-228">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="85be5-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="85be5-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="85be5-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="85be5-230">Entry</span></span> | <span data-ttu-id="85be5-231">Wert</span><span class="sxs-lookup"><span data-stu-id="85be5-231">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="85be5-232">Link-ID</span><span class="sxs-lookup"><span data-stu-id="85be5-232">Link-Id</span></span>                | <span data-ttu-id="85be5-233">50</span><span class="sxs-lookup"><span data-stu-id="85be5-233">50</span></span>                                  |
| <span data-ttu-id="85be5-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85be5-234">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="85be5-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="85be5-235">System-Only</span></span>            | <span data-ttu-id="85be5-236">False</span><span class="sxs-lookup"><span data-stu-id="85be5-236">False</span></span>                               |
| <span data-ttu-id="85be5-237">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="85be5-237">Is-Single-Valued</span></span>       | <span data-ttu-id="85be5-238">False</span><span class="sxs-lookup"><span data-stu-id="85be5-238">False</span></span>                               |
| <span data-ttu-id="85be5-239">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="85be5-239">Is Indexed</span></span>             | <span data-ttu-id="85be5-240">False</span><span class="sxs-lookup"><span data-stu-id="85be5-240">False</span></span>                               |
| <span data-ttu-id="85be5-241">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="85be5-241">In Global Catalog</span></span>      | <span data-ttu-id="85be5-242">False</span><span class="sxs-lookup"><span data-stu-id="85be5-242">False</span></span>                               |
| <span data-ttu-id="85be5-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="85be5-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="85be5-244">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="85be5-244">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="85be5-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85be5-245">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="85be5-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85be5-246">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="85be5-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85be5-247">Search-Flags</span></span>           | <span data-ttu-id="85be5-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85be5-248">0x00000000</span></span>                          |
| <span data-ttu-id="85be5-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85be5-249">System-Flags</span></span>           | <span data-ttu-id="85be5-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85be5-250">0x00000010</span></span>                          |
| <span data-ttu-id="85be5-251">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="85be5-251">Classes used in</span></span>        | [<span data-ttu-id="85be5-252">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="85be5-252">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="85be5-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="85be5-253">Windows Server 2012</span></span>



| <span data-ttu-id="85be5-254">Eingabe</span><span class="sxs-lookup"><span data-stu-id="85be5-254">Entry</span></span> | <span data-ttu-id="85be5-255">Wert</span><span class="sxs-lookup"><span data-stu-id="85be5-255">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="85be5-256">Link-ID</span><span class="sxs-lookup"><span data-stu-id="85be5-256">Link-Id</span></span>                | <span data-ttu-id="85be5-257">50</span><span class="sxs-lookup"><span data-stu-id="85be5-257">50</span></span>                                  |
| <span data-ttu-id="85be5-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85be5-258">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="85be5-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="85be5-259">System-Only</span></span>            | <span data-ttu-id="85be5-260">False</span><span class="sxs-lookup"><span data-stu-id="85be5-260">False</span></span>                               |
| <span data-ttu-id="85be5-261">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="85be5-261">Is-Single-Valued</span></span>       | <span data-ttu-id="85be5-262">False</span><span class="sxs-lookup"><span data-stu-id="85be5-262">False</span></span>                               |
| <span data-ttu-id="85be5-263">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="85be5-263">Is Indexed</span></span>             | <span data-ttu-id="85be5-264">False</span><span class="sxs-lookup"><span data-stu-id="85be5-264">False</span></span>                               |
| <span data-ttu-id="85be5-265">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="85be5-265">In Global Catalog</span></span>      | <span data-ttu-id="85be5-266">False</span><span class="sxs-lookup"><span data-stu-id="85be5-266">False</span></span>                               |
| <span data-ttu-id="85be5-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="85be5-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="85be5-268">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="85be5-268">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="85be5-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85be5-269">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="85be5-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85be5-270">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="85be5-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85be5-271">Search-Flags</span></span>           | <span data-ttu-id="85be5-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85be5-272">0x00000000</span></span>                          |
| <span data-ttu-id="85be5-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85be5-273">System-Flags</span></span>           | <span data-ttu-id="85be5-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85be5-274">0x00000010</span></span>                          |
| <span data-ttu-id="85be5-275">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="85be5-275">Classes used in</span></span>        | [<span data-ttu-id="85be5-276">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="85be5-276">**Group**</span></span>](c-group.md)<br/> |



 

 





