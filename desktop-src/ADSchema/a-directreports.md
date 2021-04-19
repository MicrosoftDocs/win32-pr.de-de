---
title: Reports-Attribut
description: Enthält die Liste der Benutzer, die dem Benutzer direkt einen Bericht erstatten. Bei den als Berichte aufgeführten Benutzern handelt es sich um Benutzer, deren Eigenschaften-Manager-Eigenschaft auf diesen Benutzer festgelegt ist. Jedes Element in der Liste ist ein verknüpfter Verweis auf das Objekt, das den Benutzer darstellt.
ms.assetid: 369fc457-685c-4875-aed3-0a246a219512
ms.tgt_platform: multiple
keywords:
- AD-Schema für Berichte-Attribut
- DirectReports-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Reports
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ef5a555b7c1d48fdb337f2c876abf3f15ae8daa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106342925"
---
# <a name="reports-attribute"></a><span data-ttu-id="0b410-107">Reports-Attribut</span><span class="sxs-lookup"><span data-stu-id="0b410-107">Reports attribute</span></span>

<span data-ttu-id="0b410-108">Enthält die Liste der Benutzer, die dem Benutzer direkt einen Bericht erstatten.</span><span class="sxs-lookup"><span data-stu-id="0b410-108">Contains the list of users that directly report to the user.</span></span> <span data-ttu-id="0b410-109">Bei den als Berichte aufgeführten Benutzern handelt es sich um Benutzer, deren Eigenschaften-Manager-Eigenschaft auf diesen Benutzer festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0b410-109">The users listed as reports are those that have the property manager property set to this user.</span></span> <span data-ttu-id="0b410-110">Jedes Element in der Liste ist ein verknüpfter Verweis auf das Objekt, das den Benutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="0b410-110">Each item in the list is a linked reference to the object that represents the user.</span></span>



| <span data-ttu-id="0b410-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0b410-111">Entry</span></span> | <span data-ttu-id="0b410-112">Wert</span><span class="sxs-lookup"><span data-stu-id="0b410-112">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="0b410-113">CN</span><span class="sxs-lookup"><span data-stu-id="0b410-113">CN</span></span>                | <span data-ttu-id="0b410-114">Berichte</span><span class="sxs-lookup"><span data-stu-id="0b410-114">Reports</span></span>                                         |
| <span data-ttu-id="0b410-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0b410-115">Ldap-Display-Name</span></span> | <span data-ttu-id="0b410-116">directReports</span><span class="sxs-lookup"><span data-stu-id="0b410-116">directReports</span></span>                                   |
| <span data-ttu-id="0b410-117">Size</span><span class="sxs-lookup"><span data-stu-id="0b410-117">Size</span></span>              | \-                                              |
| <span data-ttu-id="0b410-118">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="0b410-118">Update Privilege</span></span>  | <span data-ttu-id="0b410-119">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0b410-119">This value is set by the system.</span></span>                |
| <span data-ttu-id="0b410-120">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="0b410-120">Update Frequency</span></span>  | <span data-ttu-id="0b410-121">Jedes Mal, wenn der direkte Bericht über einen Benutzer ändert.</span><span class="sxs-lookup"><span data-stu-id="0b410-121">Whenever the direct reports for a user changes.</span></span> |
| <span data-ttu-id="0b410-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0b410-122">Attribute-Id</span></span>      | <span data-ttu-id="0b410-123">1.2.840.113556.1.2.436</span><span class="sxs-lookup"><span data-stu-id="0b410-123">1.2.840.113556.1.2.436</span></span>                          |
| <span data-ttu-id="0b410-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0b410-124">System-Id-Guid</span></span>    | <span data-ttu-id="0b410-125">bf967a1c-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="0b410-125">bf967a1c-0de6-11d0-a285-00aa003049e2</span></span>            |
| <span data-ttu-id="0b410-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b410-126">Syntax</span></span>            | [<span data-ttu-id="0b410-127">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="0b410-127">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)         |



## <a name="implementations"></a><span data-ttu-id="0b410-128">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="0b410-128">Implementations</span></span>

-   [<span data-ttu-id="0b410-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0b410-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0b410-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0b410-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0b410-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0b410-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0b410-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0b410-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0b410-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0b410-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0b410-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0b410-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0b410-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0b410-135">Windows 2000 Server</span></span>



| <span data-ttu-id="0b410-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0b410-136">Entry</span></span> | <span data-ttu-id="0b410-137">Wert</span><span class="sxs-lookup"><span data-stu-id="0b410-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0b410-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0b410-138">Link-Id</span></span>                | <span data-ttu-id="0b410-139">43</span><span class="sxs-lookup"><span data-stu-id="0b410-139">43</span></span>                              |
| <span data-ttu-id="0b410-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b410-140">MAPI-Id</span></span>                | <span data-ttu-id="0b410-141">0x800e</span><span class="sxs-lookup"><span data-stu-id="0b410-141">0x800E</span></span>                          |
| <span data-ttu-id="0b410-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b410-142">System-Only</span></span>            | <span data-ttu-id="0b410-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b410-143">True</span></span>                            |
| <span data-ttu-id="0b410-144">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0b410-144">Is-Single-Valued</span></span>       | <span data-ttu-id="0b410-145">False</span><span class="sxs-lookup"><span data-stu-id="0b410-145">False</span></span>                           |
| <span data-ttu-id="0b410-146">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0b410-146">Is Indexed</span></span>             | <span data-ttu-id="0b410-147">False</span><span class="sxs-lookup"><span data-stu-id="0b410-147">False</span></span>                           |
| <span data-ttu-id="0b410-148">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0b410-148">In Global Catalog</span></span>      | <span data-ttu-id="0b410-149">False</span><span class="sxs-lookup"><span data-stu-id="0b410-149">False</span></span>                           |
| <span data-ttu-id="0b410-150">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0b410-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b410-151">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0b410-151">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0b410-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b410-152">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0b410-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b410-153">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0b410-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b410-154">Search-Flags</span></span>           | <span data-ttu-id="0b410-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b410-155">0x00000000</span></span>                      |
| <span data-ttu-id="0b410-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b410-156">System-Flags</span></span>           | <span data-ttu-id="0b410-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b410-157">0x00000010</span></span>                      |
| <span data-ttu-id="0b410-158">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0b410-158">Classes used in</span></span>        | [<span data-ttu-id="0b410-159">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="0b410-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0b410-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0b410-160">Windows Server 2003</span></span>



| <span data-ttu-id="0b410-161">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0b410-161">Entry</span></span> | <span data-ttu-id="0b410-162">Wert</span><span class="sxs-lookup"><span data-stu-id="0b410-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0b410-163">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0b410-163">Link-Id</span></span>                | <span data-ttu-id="0b410-164">43</span><span class="sxs-lookup"><span data-stu-id="0b410-164">43</span></span>                              |
| <span data-ttu-id="0b410-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b410-165">MAPI-Id</span></span>                | <span data-ttu-id="0b410-166">0x800e</span><span class="sxs-lookup"><span data-stu-id="0b410-166">0x800E</span></span>                          |
| <span data-ttu-id="0b410-167">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b410-167">System-Only</span></span>            | <span data-ttu-id="0b410-168">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b410-168">True</span></span>                            |
| <span data-ttu-id="0b410-169">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0b410-169">Is-Single-Valued</span></span>       | <span data-ttu-id="0b410-170">False</span><span class="sxs-lookup"><span data-stu-id="0b410-170">False</span></span>                           |
| <span data-ttu-id="0b410-171">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0b410-171">Is Indexed</span></span>             | <span data-ttu-id="0b410-172">False</span><span class="sxs-lookup"><span data-stu-id="0b410-172">False</span></span>                           |
| <span data-ttu-id="0b410-173">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0b410-173">In Global Catalog</span></span>      | <span data-ttu-id="0b410-174">False</span><span class="sxs-lookup"><span data-stu-id="0b410-174">False</span></span>                           |
| <span data-ttu-id="0b410-175">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0b410-175">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b410-176">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0b410-176">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0b410-177">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b410-177">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0b410-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b410-178">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0b410-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b410-179">Search-Flags</span></span>           | <span data-ttu-id="0b410-180">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b410-180">0x00000000</span></span>                      |
| <span data-ttu-id="0b410-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b410-181">System-Flags</span></span>           | <span data-ttu-id="0b410-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b410-182">0x00000010</span></span>                      |
| <span data-ttu-id="0b410-183">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0b410-183">Classes used in</span></span>        | [<span data-ttu-id="0b410-184">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="0b410-184">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0b410-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0b410-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0b410-186">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0b410-186">Entry</span></span> | <span data-ttu-id="0b410-187">Wert</span><span class="sxs-lookup"><span data-stu-id="0b410-187">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0b410-188">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0b410-188">Link-Id</span></span>                | <span data-ttu-id="0b410-189">43</span><span class="sxs-lookup"><span data-stu-id="0b410-189">43</span></span>                              |
| <span data-ttu-id="0b410-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b410-190">MAPI-Id</span></span>                | <span data-ttu-id="0b410-191">0x800e</span><span class="sxs-lookup"><span data-stu-id="0b410-191">0x800E</span></span>                          |
| <span data-ttu-id="0b410-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b410-192">System-Only</span></span>            | <span data-ttu-id="0b410-193">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b410-193">True</span></span>                            |
| <span data-ttu-id="0b410-194">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0b410-194">Is-Single-Valued</span></span>       | <span data-ttu-id="0b410-195">False</span><span class="sxs-lookup"><span data-stu-id="0b410-195">False</span></span>                           |
| <span data-ttu-id="0b410-196">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0b410-196">Is Indexed</span></span>             | <span data-ttu-id="0b410-197">False</span><span class="sxs-lookup"><span data-stu-id="0b410-197">False</span></span>                           |
| <span data-ttu-id="0b410-198">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0b410-198">In Global Catalog</span></span>      | <span data-ttu-id="0b410-199">False</span><span class="sxs-lookup"><span data-stu-id="0b410-199">False</span></span>                           |
| <span data-ttu-id="0b410-200">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0b410-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b410-201">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0b410-201">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0b410-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b410-202">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0b410-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b410-203">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0b410-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b410-204">Search-Flags</span></span>           | <span data-ttu-id="0b410-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b410-205">0x00000000</span></span>                      |
| <span data-ttu-id="0b410-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b410-206">System-Flags</span></span>           | <span data-ttu-id="0b410-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b410-207">0x00000010</span></span>                      |
| <span data-ttu-id="0b410-208">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0b410-208">Classes used in</span></span>        | [<span data-ttu-id="0b410-209">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="0b410-209">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0b410-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b410-210">Windows Server 2008</span></span>



| <span data-ttu-id="0b410-211">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0b410-211">Entry</span></span> | <span data-ttu-id="0b410-212">Wert</span><span class="sxs-lookup"><span data-stu-id="0b410-212">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0b410-213">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0b410-213">Link-Id</span></span>                | <span data-ttu-id="0b410-214">43</span><span class="sxs-lookup"><span data-stu-id="0b410-214">43</span></span>                              |
| <span data-ttu-id="0b410-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b410-215">MAPI-Id</span></span>                | <span data-ttu-id="0b410-216">0x800e</span><span class="sxs-lookup"><span data-stu-id="0b410-216">0x800E</span></span>                          |
| <span data-ttu-id="0b410-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b410-217">System-Only</span></span>            | <span data-ttu-id="0b410-218">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b410-218">True</span></span>                            |
| <span data-ttu-id="0b410-219">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0b410-219">Is-Single-Valued</span></span>       | <span data-ttu-id="0b410-220">False</span><span class="sxs-lookup"><span data-stu-id="0b410-220">False</span></span>                           |
| <span data-ttu-id="0b410-221">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0b410-221">Is Indexed</span></span>             | <span data-ttu-id="0b410-222">False</span><span class="sxs-lookup"><span data-stu-id="0b410-222">False</span></span>                           |
| <span data-ttu-id="0b410-223">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0b410-223">In Global Catalog</span></span>      | <span data-ttu-id="0b410-224">False</span><span class="sxs-lookup"><span data-stu-id="0b410-224">False</span></span>                           |
| <span data-ttu-id="0b410-225">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0b410-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b410-226">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0b410-226">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0b410-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b410-227">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0b410-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b410-228">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0b410-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b410-229">Search-Flags</span></span>           | <span data-ttu-id="0b410-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b410-230">0x00000000</span></span>                      |
| <span data-ttu-id="0b410-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b410-231">System-Flags</span></span>           | <span data-ttu-id="0b410-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b410-232">0x00000010</span></span>                      |
| <span data-ttu-id="0b410-233">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0b410-233">Classes used in</span></span>        | [<span data-ttu-id="0b410-234">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="0b410-234">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0b410-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0b410-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0b410-236">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0b410-236">Entry</span></span> | <span data-ttu-id="0b410-237">Wert</span><span class="sxs-lookup"><span data-stu-id="0b410-237">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0b410-238">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0b410-238">Link-Id</span></span>                | <span data-ttu-id="0b410-239">43</span><span class="sxs-lookup"><span data-stu-id="0b410-239">43</span></span>                              |
| <span data-ttu-id="0b410-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b410-240">MAPI-Id</span></span>                | <span data-ttu-id="0b410-241">0x800e</span><span class="sxs-lookup"><span data-stu-id="0b410-241">0x800E</span></span>                          |
| <span data-ttu-id="0b410-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b410-242">System-Only</span></span>            | <span data-ttu-id="0b410-243">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b410-243">True</span></span>                            |
| <span data-ttu-id="0b410-244">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0b410-244">Is-Single-Valued</span></span>       | <span data-ttu-id="0b410-245">False</span><span class="sxs-lookup"><span data-stu-id="0b410-245">False</span></span>                           |
| <span data-ttu-id="0b410-246">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0b410-246">Is Indexed</span></span>             | <span data-ttu-id="0b410-247">False</span><span class="sxs-lookup"><span data-stu-id="0b410-247">False</span></span>                           |
| <span data-ttu-id="0b410-248">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0b410-248">In Global Catalog</span></span>      | <span data-ttu-id="0b410-249">False</span><span class="sxs-lookup"><span data-stu-id="0b410-249">False</span></span>                           |
| <span data-ttu-id="0b410-250">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0b410-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b410-251">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0b410-251">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0b410-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b410-252">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0b410-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b410-253">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0b410-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b410-254">Search-Flags</span></span>           | <span data-ttu-id="0b410-255">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b410-255">0x00000000</span></span>                      |
| <span data-ttu-id="0b410-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b410-256">System-Flags</span></span>           | <span data-ttu-id="0b410-257">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b410-257">0x00000010</span></span>                      |
| <span data-ttu-id="0b410-258">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0b410-258">Classes used in</span></span>        | [<span data-ttu-id="0b410-259">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="0b410-259">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0b410-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0b410-260">Windows Server 2012</span></span>



| <span data-ttu-id="0b410-261">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0b410-261">Entry</span></span> | <span data-ttu-id="0b410-262">Wert</span><span class="sxs-lookup"><span data-stu-id="0b410-262">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0b410-263">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0b410-263">Link-Id</span></span>                | <span data-ttu-id="0b410-264">43</span><span class="sxs-lookup"><span data-stu-id="0b410-264">43</span></span>                              |
| <span data-ttu-id="0b410-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b410-265">MAPI-Id</span></span>                | <span data-ttu-id="0b410-266">0x800e</span><span class="sxs-lookup"><span data-stu-id="0b410-266">0x800E</span></span>                          |
| <span data-ttu-id="0b410-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b410-267">System-Only</span></span>            | <span data-ttu-id="0b410-268">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b410-268">True</span></span>                            |
| <span data-ttu-id="0b410-269">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0b410-269">Is-Single-Valued</span></span>       | <span data-ttu-id="0b410-270">False</span><span class="sxs-lookup"><span data-stu-id="0b410-270">False</span></span>                           |
| <span data-ttu-id="0b410-271">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0b410-271">Is Indexed</span></span>             | <span data-ttu-id="0b410-272">False</span><span class="sxs-lookup"><span data-stu-id="0b410-272">False</span></span>                           |
| <span data-ttu-id="0b410-273">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0b410-273">In Global Catalog</span></span>      | <span data-ttu-id="0b410-274">False</span><span class="sxs-lookup"><span data-stu-id="0b410-274">False</span></span>                           |
| <span data-ttu-id="0b410-275">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0b410-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b410-276">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0b410-276">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0b410-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b410-277">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0b410-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b410-278">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0b410-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b410-279">Search-Flags</span></span>           | <span data-ttu-id="0b410-280">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b410-280">0x00000000</span></span>                      |
| <span data-ttu-id="0b410-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b410-281">System-Flags</span></span>           | <span data-ttu-id="0b410-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b410-282">0x00000010</span></span>                      |
| <span data-ttu-id="0b410-283">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0b410-283">Classes used in</span></span>        | [<span data-ttu-id="0b410-284">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="0b410-284">**Top**</span></span>](c-top.md)<br/> |



 

 





