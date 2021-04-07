---
title: Admin-Count-Attribut
description: Gibt an, dass die ACLs für ein bestimmtes Objekt vom System in einen sichereren Wert geändert wurden, weil es Mitglied einer der administrativen Gruppen (direkt oder transitiv) war.
ms.assetid: b2384ada-a792-42fa-be64-291d23e00887
ms.tgt_platform: multiple
keywords:
- AD-Schema für Admin-Count-Attribut
- adminCount-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Admin-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95b953aebaa39bb3fc3e4c9cf96632f32a37850
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103745305"
---
# <a name="admin-count-attribute"></a><span data-ttu-id="ca6ad-105">Admin-Count-Attribut</span><span class="sxs-lookup"><span data-stu-id="ca6ad-105">Admin-Count attribute</span></span>

<span data-ttu-id="ca6ad-106">Gibt an, dass die ACLs für ein bestimmtes Objekt vom System in einen sichereren Wert geändert wurden, weil es Mitglied einer der administrativen Gruppen (direkt oder transitiv) war.</span><span class="sxs-lookup"><span data-stu-id="ca6ad-106">Indicates that a given object has had its ACLs changed to a more secure value by the system because it was a member of one of the administrative groups (directly or transitively).</span></span>



| <span data-ttu-id="ca6ad-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ca6ad-107">Entry</span></span> | <span data-ttu-id="ca6ad-108">Wert</span><span class="sxs-lookup"><span data-stu-id="ca6ad-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="ca6ad-109">CN</span><span class="sxs-lookup"><span data-stu-id="ca6ad-109">CN</span></span>                | <span data-ttu-id="ca6ad-110">Admin-Count</span><span class="sxs-lookup"><span data-stu-id="ca6ad-110">Admin-Count</span></span>                                         |
| <span data-ttu-id="ca6ad-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ca6ad-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ca6ad-112">adminCount</span><span class="sxs-lookup"><span data-stu-id="ca6ad-112">adminCount</span></span>                                          |
| <span data-ttu-id="ca6ad-113">Size</span><span class="sxs-lookup"><span data-stu-id="ca6ad-113">Size</span></span>              | <span data-ttu-id="ca6ad-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="ca6ad-114">4 bytes</span></span>                                             |
| <span data-ttu-id="ca6ad-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ca6ad-115">Update Privilege</span></span>  | <span data-ttu-id="ca6ad-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ca6ad-116">This value is set by the system.</span></span>                    |
| <span data-ttu-id="ca6ad-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="ca6ad-117">Update Frequency</span></span>  | <span data-ttu-id="ca6ad-118">Wenn ein Objekt einer administrativen Gruppe hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="ca6ad-118">When an object is added to an administrative group.</span></span> |
| <span data-ttu-id="ca6ad-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ca6ad-119">Attribute-Id</span></span>      | <span data-ttu-id="ca6ad-120">1.2.840.113556.1.4.150</span><span class="sxs-lookup"><span data-stu-id="ca6ad-120">1.2.840.113556.1.4.150</span></span>                              |
| <span data-ttu-id="ca6ad-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ca6ad-121">System-Id-Guid</span></span>    | <span data-ttu-id="ca6ad-122">bf967918-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ca6ad-122">bf967918-0de6-11d0-a285-00aa003049e2</span></span>                |
| <span data-ttu-id="ca6ad-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca6ad-123">Syntax</span></span>            | [<span data-ttu-id="ca6ad-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="ca6ad-124">**Enumeration**</span></span>](s-enumeration.md)                |



## <a name="implementations"></a><span data-ttu-id="ca6ad-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="ca6ad-125">Implementations</span></span>

-   [<span data-ttu-id="ca6ad-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ca6ad-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ca6ad-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ca6ad-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ca6ad-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ca6ad-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ca6ad-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ca6ad-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ca6ad-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ca6ad-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ca6ad-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ca6ad-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ca6ad-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ca6ad-132">Windows 2000 Server</span></span>



| <span data-ttu-id="ca6ad-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ca6ad-133">Entry</span></span> | <span data-ttu-id="ca6ad-134">Wert</span><span class="sxs-lookup"><span data-stu-id="ca6ad-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="ca6ad-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ca6ad-135">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="ca6ad-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca6ad-136">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="ca6ad-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca6ad-137">System-Only</span></span>            | <span data-ttu-id="ca6ad-138">False</span><span class="sxs-lookup"><span data-stu-id="ca6ad-138">False</span></span>                                                                 |
| <span data-ttu-id="ca6ad-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ca6ad-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ca6ad-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="ca6ad-140">True</span></span>                                                                  |
| <span data-ttu-id="ca6ad-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ca6ad-141">Is Indexed</span></span>             | <span data-ttu-id="ca6ad-142">False</span><span class="sxs-lookup"><span data-stu-id="ca6ad-142">False</span></span>                                                                 |
| <span data-ttu-id="ca6ad-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ca6ad-143">In Global Catalog</span></span>      | <span data-ttu-id="ca6ad-144">False</span><span class="sxs-lookup"><span data-stu-id="ca6ad-144">False</span></span>                                                                 |
| <span data-ttu-id="ca6ad-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ca6ad-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca6ad-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ca6ad-146">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="ca6ad-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca6ad-147">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="ca6ad-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca6ad-148">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="ca6ad-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6ad-149">Search-Flags</span></span>           | <span data-ttu-id="ca6ad-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca6ad-150">0x00000000</span></span>                                                            |
| <span data-ttu-id="ca6ad-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6ad-151">System-Flags</span></span>           | <span data-ttu-id="ca6ad-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca6ad-152">0x00000010</span></span>                                                            |
| <span data-ttu-id="ca6ad-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ca6ad-153">Classes used in</span></span>        | [<span data-ttu-id="ca6ad-154">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="ca6ad-154">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="ca6ad-155">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="ca6ad-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ca6ad-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ca6ad-156">Windows Server 2003</span></span>



| <span data-ttu-id="ca6ad-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ca6ad-157">Entry</span></span> | <span data-ttu-id="ca6ad-158">Wert</span><span class="sxs-lookup"><span data-stu-id="ca6ad-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="ca6ad-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ca6ad-159">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="ca6ad-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca6ad-160">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="ca6ad-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca6ad-161">System-Only</span></span>            | <span data-ttu-id="ca6ad-162">False</span><span class="sxs-lookup"><span data-stu-id="ca6ad-162">False</span></span>                                                                 |
| <span data-ttu-id="ca6ad-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ca6ad-163">Is-Single-Valued</span></span>       | <span data-ttu-id="ca6ad-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="ca6ad-164">True</span></span>                                                                  |
| <span data-ttu-id="ca6ad-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ca6ad-165">Is Indexed</span></span>             | <span data-ttu-id="ca6ad-166">False</span><span class="sxs-lookup"><span data-stu-id="ca6ad-166">False</span></span>                                                                 |
| <span data-ttu-id="ca6ad-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ca6ad-167">In Global Catalog</span></span>      | <span data-ttu-id="ca6ad-168">False</span><span class="sxs-lookup"><span data-stu-id="ca6ad-168">False</span></span>                                                                 |
| <span data-ttu-id="ca6ad-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ca6ad-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca6ad-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ca6ad-170">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="ca6ad-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca6ad-171">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="ca6ad-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca6ad-172">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="ca6ad-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6ad-173">Search-Flags</span></span>           | <span data-ttu-id="ca6ad-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca6ad-174">0x00000000</span></span>                                                            |
| <span data-ttu-id="ca6ad-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6ad-175">System-Flags</span></span>           | <span data-ttu-id="ca6ad-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca6ad-176">0x00000010</span></span>                                                            |
| <span data-ttu-id="ca6ad-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ca6ad-177">Classes used in</span></span>        | [<span data-ttu-id="ca6ad-178">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="ca6ad-178">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="ca6ad-179">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="ca6ad-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ca6ad-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ca6ad-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ca6ad-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ca6ad-181">Entry</span></span> | <span data-ttu-id="ca6ad-182">Wert</span><span class="sxs-lookup"><span data-stu-id="ca6ad-182">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="ca6ad-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ca6ad-183">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="ca6ad-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca6ad-184">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="ca6ad-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca6ad-185">System-Only</span></span>            | <span data-ttu-id="ca6ad-186">False</span><span class="sxs-lookup"><span data-stu-id="ca6ad-186">False</span></span>                                                                 |
| <span data-ttu-id="ca6ad-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ca6ad-187">Is-Single-Valued</span></span>       | <span data-ttu-id="ca6ad-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="ca6ad-188">True</span></span>                                                                  |
| <span data-ttu-id="ca6ad-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ca6ad-189">Is Indexed</span></span>             | <span data-ttu-id="ca6ad-190">False</span><span class="sxs-lookup"><span data-stu-id="ca6ad-190">False</span></span>                                                                 |
| <span data-ttu-id="ca6ad-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ca6ad-191">In Global Catalog</span></span>      | <span data-ttu-id="ca6ad-192">False</span><span class="sxs-lookup"><span data-stu-id="ca6ad-192">False</span></span>                                                                 |
| <span data-ttu-id="ca6ad-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ca6ad-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca6ad-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ca6ad-194">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="ca6ad-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca6ad-195">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="ca6ad-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca6ad-196">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="ca6ad-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6ad-197">Search-Flags</span></span>           | <span data-ttu-id="ca6ad-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca6ad-198">0x00000000</span></span>                                                            |
| <span data-ttu-id="ca6ad-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6ad-199">System-Flags</span></span>           | <span data-ttu-id="ca6ad-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca6ad-200">0x00000010</span></span>                                                            |
| <span data-ttu-id="ca6ad-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ca6ad-201">Classes used in</span></span>        | [<span data-ttu-id="ca6ad-202">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="ca6ad-202">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="ca6ad-203">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="ca6ad-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ca6ad-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca6ad-204">Windows Server 2008</span></span>



| <span data-ttu-id="ca6ad-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ca6ad-205">Entry</span></span> | <span data-ttu-id="ca6ad-206">Wert</span><span class="sxs-lookup"><span data-stu-id="ca6ad-206">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="ca6ad-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ca6ad-207">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="ca6ad-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca6ad-208">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="ca6ad-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca6ad-209">System-Only</span></span>            | <span data-ttu-id="ca6ad-210">False</span><span class="sxs-lookup"><span data-stu-id="ca6ad-210">False</span></span>                                                                 |
| <span data-ttu-id="ca6ad-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ca6ad-211">Is-Single-Valued</span></span>       | <span data-ttu-id="ca6ad-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="ca6ad-212">True</span></span>                                                                  |
| <span data-ttu-id="ca6ad-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ca6ad-213">Is Indexed</span></span>             | <span data-ttu-id="ca6ad-214">False</span><span class="sxs-lookup"><span data-stu-id="ca6ad-214">False</span></span>                                                                 |
| <span data-ttu-id="ca6ad-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ca6ad-215">In Global Catalog</span></span>      | <span data-ttu-id="ca6ad-216">False</span><span class="sxs-lookup"><span data-stu-id="ca6ad-216">False</span></span>                                                                 |
| <span data-ttu-id="ca6ad-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ca6ad-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca6ad-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ca6ad-218">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="ca6ad-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca6ad-219">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="ca6ad-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca6ad-220">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="ca6ad-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6ad-221">Search-Flags</span></span>           | <span data-ttu-id="ca6ad-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca6ad-222">0x00000000</span></span>                                                            |
| <span data-ttu-id="ca6ad-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6ad-223">System-Flags</span></span>           | <span data-ttu-id="ca6ad-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca6ad-224">0x00000010</span></span>                                                            |
| <span data-ttu-id="ca6ad-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ca6ad-225">Classes used in</span></span>        | [<span data-ttu-id="ca6ad-226">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="ca6ad-226">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="ca6ad-227">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="ca6ad-227">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ca6ad-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ca6ad-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ca6ad-229">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ca6ad-229">Entry</span></span> | <span data-ttu-id="ca6ad-230">Wert</span><span class="sxs-lookup"><span data-stu-id="ca6ad-230">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="ca6ad-231">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ca6ad-231">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="ca6ad-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca6ad-232">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="ca6ad-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca6ad-233">System-Only</span></span>            | <span data-ttu-id="ca6ad-234">False</span><span class="sxs-lookup"><span data-stu-id="ca6ad-234">False</span></span>                                                                 |
| <span data-ttu-id="ca6ad-235">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ca6ad-235">Is-Single-Valued</span></span>       | <span data-ttu-id="ca6ad-236">Richtig</span><span class="sxs-lookup"><span data-stu-id="ca6ad-236">True</span></span>                                                                  |
| <span data-ttu-id="ca6ad-237">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ca6ad-237">Is Indexed</span></span>             | <span data-ttu-id="ca6ad-238">False</span><span class="sxs-lookup"><span data-stu-id="ca6ad-238">False</span></span>                                                                 |
| <span data-ttu-id="ca6ad-239">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ca6ad-239">In Global Catalog</span></span>      | <span data-ttu-id="ca6ad-240">False</span><span class="sxs-lookup"><span data-stu-id="ca6ad-240">False</span></span>                                                                 |
| <span data-ttu-id="ca6ad-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ca6ad-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca6ad-242">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ca6ad-242">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="ca6ad-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca6ad-243">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="ca6ad-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca6ad-244">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="ca6ad-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6ad-245">Search-Flags</span></span>           | <span data-ttu-id="ca6ad-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca6ad-246">0x00000000</span></span>                                                            |
| <span data-ttu-id="ca6ad-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6ad-247">System-Flags</span></span>           | <span data-ttu-id="ca6ad-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca6ad-248">0x00000010</span></span>                                                            |
| <span data-ttu-id="ca6ad-249">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ca6ad-249">Classes used in</span></span>        | [<span data-ttu-id="ca6ad-250">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="ca6ad-250">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="ca6ad-251">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="ca6ad-251">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ca6ad-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ca6ad-252">Windows Server 2012</span></span>



| <span data-ttu-id="ca6ad-253">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ca6ad-253">Entry</span></span> | <span data-ttu-id="ca6ad-254">Wert</span><span class="sxs-lookup"><span data-stu-id="ca6ad-254">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="ca6ad-255">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ca6ad-255">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="ca6ad-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca6ad-256">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="ca6ad-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca6ad-257">System-Only</span></span>            | <span data-ttu-id="ca6ad-258">False</span><span class="sxs-lookup"><span data-stu-id="ca6ad-258">False</span></span>                                                                 |
| <span data-ttu-id="ca6ad-259">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ca6ad-259">Is-Single-Valued</span></span>       | <span data-ttu-id="ca6ad-260">Richtig</span><span class="sxs-lookup"><span data-stu-id="ca6ad-260">True</span></span>                                                                  |
| <span data-ttu-id="ca6ad-261">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ca6ad-261">Is Indexed</span></span>             | <span data-ttu-id="ca6ad-262">False</span><span class="sxs-lookup"><span data-stu-id="ca6ad-262">False</span></span>                                                                 |
| <span data-ttu-id="ca6ad-263">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ca6ad-263">In Global Catalog</span></span>      | <span data-ttu-id="ca6ad-264">False</span><span class="sxs-lookup"><span data-stu-id="ca6ad-264">False</span></span>                                                                 |
| <span data-ttu-id="ca6ad-265">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ca6ad-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca6ad-266">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ca6ad-266">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="ca6ad-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca6ad-267">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="ca6ad-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca6ad-268">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="ca6ad-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6ad-269">Search-Flags</span></span>           | <span data-ttu-id="ca6ad-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca6ad-270">0x00000000</span></span>                                                            |
| <span data-ttu-id="ca6ad-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6ad-271">System-Flags</span></span>           | <span data-ttu-id="ca6ad-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca6ad-272">0x00000010</span></span>                                                            |
| <span data-ttu-id="ca6ad-273">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ca6ad-273">Classes used in</span></span>        | [<span data-ttu-id="ca6ad-274">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="ca6ad-274">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="ca6ad-275">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="ca6ad-275">**User**</span></span>](c-user.md)<br/> |



 

 





