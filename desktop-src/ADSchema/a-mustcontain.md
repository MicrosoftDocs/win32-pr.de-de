---
title: Must-Contain-Attribut
description: Die Liste der obligatorischen Attribute für eine Klasse. Diese Attribute müssen angegeben werden, wenn eine Instanz der-Klasse erstellt wird.
ms.assetid: ad112640-0e99-453a-8eff-f964419d8631
ms.tgt_platform: multiple
keywords:
- AD-Schema für Must-Contain-Attribut
- c#-Attribut
topic_type:
- apiref
api_name:
- Must-Contain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d791468691f438d01161f0d6252f7b995fc0f51e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744592"
---
# <a name="must-contain-attribute"></a><span data-ttu-id="1320b-106">Must-Contain-Attribut</span><span class="sxs-lookup"><span data-stu-id="1320b-106">Must-Contain attribute</span></span>

<span data-ttu-id="1320b-107">Die Liste der obligatorischen Attribute für eine Klasse.</span><span class="sxs-lookup"><span data-stu-id="1320b-107">The list of mandatory attributes for a class.</span></span> <span data-ttu-id="1320b-108">Diese Attribute müssen angegeben werden, wenn eine Instanz der-Klasse erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1320b-108">These attributes must be specified when an instance of the class is created.</span></span>



| <span data-ttu-id="1320b-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1320b-109">Entry</span></span> | <span data-ttu-id="1320b-110">Wert</span><span class="sxs-lookup"><span data-stu-id="1320b-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="1320b-111">CN</span><span class="sxs-lookup"><span data-stu-id="1320b-111">CN</span></span>                | <span data-ttu-id="1320b-112">Must-Contain</span><span class="sxs-lookup"><span data-stu-id="1320b-112">Must-Contain</span></span>                                                    |
| <span data-ttu-id="1320b-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1320b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1320b-114">mustContain</span><span class="sxs-lookup"><span data-stu-id="1320b-114">mustContain</span></span>                                                     |
| <span data-ttu-id="1320b-115">Size</span><span class="sxs-lookup"><span data-stu-id="1320b-115">Size</span></span>              | \-                                                              |
| <span data-ttu-id="1320b-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="1320b-116">Update Privilege</span></span>  | <span data-ttu-id="1320b-117">Schema Administrator</span><span class="sxs-lookup"><span data-stu-id="1320b-117">Schema administrator</span></span>                                            |
| <span data-ttu-id="1320b-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="1320b-118">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="1320b-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1320b-119">Attribute-Id</span></span>      | <span data-ttu-id="1320b-120">1.2.840.113556.1.2.24</span><span class="sxs-lookup"><span data-stu-id="1320b-120">1.2.840.113556.1.2.24</span></span>                                           |
| <span data-ttu-id="1320b-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1320b-121">System-Id-Guid</span></span>    | <span data-ttu-id="1320b-122">bf9679d3-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="1320b-122">bf9679d3-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="1320b-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="1320b-123">Syntax</span></span>            | [<span data-ttu-id="1320b-124">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="1320b-124">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="1320b-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="1320b-125">Implementations</span></span>

-   [<span data-ttu-id="1320b-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1320b-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1320b-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1320b-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1320b-128">**Adam**</span><span class="sxs-lookup"><span data-stu-id="1320b-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1320b-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1320b-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1320b-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1320b-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1320b-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1320b-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1320b-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1320b-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1320b-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1320b-133">Windows 2000 Server</span></span>



| <span data-ttu-id="1320b-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1320b-134">Entry</span></span> | <span data-ttu-id="1320b-135">Wert</span><span class="sxs-lookup"><span data-stu-id="1320b-135">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="1320b-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1320b-136">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="1320b-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1320b-137">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="1320b-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="1320b-138">System-Only</span></span>            | <span data-ttu-id="1320b-139">False</span><span class="sxs-lookup"><span data-stu-id="1320b-139">False</span></span>                                            |
| <span data-ttu-id="1320b-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1320b-140">Is-Single-Valued</span></span>       | <span data-ttu-id="1320b-141">False</span><span class="sxs-lookup"><span data-stu-id="1320b-141">False</span></span>                                            |
| <span data-ttu-id="1320b-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1320b-142">Is Indexed</span></span>             | <span data-ttu-id="1320b-143">False</span><span class="sxs-lookup"><span data-stu-id="1320b-143">False</span></span>                                            |
| <span data-ttu-id="1320b-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1320b-144">In Global Catalog</span></span>      | <span data-ttu-id="1320b-145">False</span><span class="sxs-lookup"><span data-stu-id="1320b-145">False</span></span>                                            |
| <span data-ttu-id="1320b-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1320b-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="1320b-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1320b-147">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="1320b-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1320b-148">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="1320b-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1320b-149">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="1320b-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1320b-150">Search-Flags</span></span>           | <span data-ttu-id="1320b-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1320b-151">0x00000000</span></span>                                       |
| <span data-ttu-id="1320b-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1320b-152">System-Flags</span></span>           | <span data-ttu-id="1320b-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1320b-153">0x00000010</span></span>                                       |
| <span data-ttu-id="1320b-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1320b-154">Classes used in</span></span>        | [<span data-ttu-id="1320b-155">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="1320b-155">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1320b-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1320b-156">Windows Server 2003</span></span>



| <span data-ttu-id="1320b-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1320b-157">Entry</span></span> | <span data-ttu-id="1320b-158">Wert</span><span class="sxs-lookup"><span data-stu-id="1320b-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="1320b-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1320b-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="1320b-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1320b-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="1320b-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="1320b-161">System-Only</span></span>            | <span data-ttu-id="1320b-162">False</span><span class="sxs-lookup"><span data-stu-id="1320b-162">False</span></span>                                            |
| <span data-ttu-id="1320b-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1320b-163">Is-Single-Valued</span></span>       | <span data-ttu-id="1320b-164">False</span><span class="sxs-lookup"><span data-stu-id="1320b-164">False</span></span>                                            |
| <span data-ttu-id="1320b-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1320b-165">Is Indexed</span></span>             | <span data-ttu-id="1320b-166">False</span><span class="sxs-lookup"><span data-stu-id="1320b-166">False</span></span>                                            |
| <span data-ttu-id="1320b-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1320b-167">In Global Catalog</span></span>      | <span data-ttu-id="1320b-168">False</span><span class="sxs-lookup"><span data-stu-id="1320b-168">False</span></span>                                            |
| <span data-ttu-id="1320b-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1320b-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="1320b-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1320b-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="1320b-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1320b-171">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="1320b-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1320b-172">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="1320b-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1320b-173">Search-Flags</span></span>           | <span data-ttu-id="1320b-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1320b-174">0x00000000</span></span>                                       |
| <span data-ttu-id="1320b-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1320b-175">System-Flags</span></span>           | <span data-ttu-id="1320b-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1320b-176">0x00000010</span></span>                                       |
| <span data-ttu-id="1320b-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1320b-177">Classes used in</span></span>        | [<span data-ttu-id="1320b-178">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="1320b-178">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1320b-179">Adam</span><span class="sxs-lookup"><span data-stu-id="1320b-179">ADAM</span></span>



| <span data-ttu-id="1320b-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1320b-180">Entry</span></span> | <span data-ttu-id="1320b-181">Wert</span><span class="sxs-lookup"><span data-stu-id="1320b-181">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="1320b-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1320b-182">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="1320b-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1320b-183">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="1320b-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="1320b-184">System-Only</span></span>            | <span data-ttu-id="1320b-185">False</span><span class="sxs-lookup"><span data-stu-id="1320b-185">False</span></span>                                            |
| <span data-ttu-id="1320b-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1320b-186">Is-Single-Valued</span></span>       | <span data-ttu-id="1320b-187">False</span><span class="sxs-lookup"><span data-stu-id="1320b-187">False</span></span>                                            |
| <span data-ttu-id="1320b-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1320b-188">Is Indexed</span></span>             | <span data-ttu-id="1320b-189">False</span><span class="sxs-lookup"><span data-stu-id="1320b-189">False</span></span>                                            |
| <span data-ttu-id="1320b-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1320b-190">In Global Catalog</span></span>      | <span data-ttu-id="1320b-191">False</span><span class="sxs-lookup"><span data-stu-id="1320b-191">False</span></span>                                            |
| <span data-ttu-id="1320b-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1320b-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="1320b-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1320b-193">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="1320b-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1320b-194">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="1320b-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1320b-195">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="1320b-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1320b-196">Search-Flags</span></span>           | <span data-ttu-id="1320b-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1320b-197">0x00000000</span></span>                                       |
| <span data-ttu-id="1320b-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1320b-198">System-Flags</span></span>           | <span data-ttu-id="1320b-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1320b-199">0x00000010</span></span>                                       |
| <span data-ttu-id="1320b-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1320b-200">Classes used in</span></span>        | [<span data-ttu-id="1320b-201">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="1320b-201">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1320b-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1320b-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1320b-203">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1320b-203">Entry</span></span> | <span data-ttu-id="1320b-204">Wert</span><span class="sxs-lookup"><span data-stu-id="1320b-204">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="1320b-205">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1320b-205">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="1320b-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1320b-206">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="1320b-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="1320b-207">System-Only</span></span>            | <span data-ttu-id="1320b-208">False</span><span class="sxs-lookup"><span data-stu-id="1320b-208">False</span></span>                                            |
| <span data-ttu-id="1320b-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1320b-209">Is-Single-Valued</span></span>       | <span data-ttu-id="1320b-210">False</span><span class="sxs-lookup"><span data-stu-id="1320b-210">False</span></span>                                            |
| <span data-ttu-id="1320b-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1320b-211">Is Indexed</span></span>             | <span data-ttu-id="1320b-212">False</span><span class="sxs-lookup"><span data-stu-id="1320b-212">False</span></span>                                            |
| <span data-ttu-id="1320b-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1320b-213">In Global Catalog</span></span>      | <span data-ttu-id="1320b-214">False</span><span class="sxs-lookup"><span data-stu-id="1320b-214">False</span></span>                                            |
| <span data-ttu-id="1320b-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1320b-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="1320b-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1320b-216">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="1320b-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1320b-217">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="1320b-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1320b-218">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="1320b-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1320b-219">Search-Flags</span></span>           | <span data-ttu-id="1320b-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1320b-220">0x00000000</span></span>                                       |
| <span data-ttu-id="1320b-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1320b-221">System-Flags</span></span>           | <span data-ttu-id="1320b-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1320b-222">0x00000010</span></span>                                       |
| <span data-ttu-id="1320b-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1320b-223">Classes used in</span></span>        | [<span data-ttu-id="1320b-224">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="1320b-224">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1320b-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1320b-225">Windows Server 2008</span></span>



| <span data-ttu-id="1320b-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1320b-226">Entry</span></span> | <span data-ttu-id="1320b-227">Wert</span><span class="sxs-lookup"><span data-stu-id="1320b-227">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="1320b-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1320b-228">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="1320b-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1320b-229">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="1320b-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="1320b-230">System-Only</span></span>            | <span data-ttu-id="1320b-231">False</span><span class="sxs-lookup"><span data-stu-id="1320b-231">False</span></span>                                            |
| <span data-ttu-id="1320b-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1320b-232">Is-Single-Valued</span></span>       | <span data-ttu-id="1320b-233">False</span><span class="sxs-lookup"><span data-stu-id="1320b-233">False</span></span>                                            |
| <span data-ttu-id="1320b-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1320b-234">Is Indexed</span></span>             | <span data-ttu-id="1320b-235">False</span><span class="sxs-lookup"><span data-stu-id="1320b-235">False</span></span>                                            |
| <span data-ttu-id="1320b-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1320b-236">In Global Catalog</span></span>      | <span data-ttu-id="1320b-237">False</span><span class="sxs-lookup"><span data-stu-id="1320b-237">False</span></span>                                            |
| <span data-ttu-id="1320b-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1320b-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="1320b-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1320b-239">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="1320b-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1320b-240">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="1320b-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1320b-241">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="1320b-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1320b-242">Search-Flags</span></span>           | <span data-ttu-id="1320b-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1320b-243">0x00000000</span></span>                                       |
| <span data-ttu-id="1320b-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1320b-244">System-Flags</span></span>           | <span data-ttu-id="1320b-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1320b-245">0x00000010</span></span>                                       |
| <span data-ttu-id="1320b-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1320b-246">Classes used in</span></span>        | [<span data-ttu-id="1320b-247">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="1320b-247">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1320b-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1320b-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1320b-249">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1320b-249">Entry</span></span> | <span data-ttu-id="1320b-250">Wert</span><span class="sxs-lookup"><span data-stu-id="1320b-250">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="1320b-251">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1320b-251">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="1320b-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1320b-252">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="1320b-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="1320b-253">System-Only</span></span>            | <span data-ttu-id="1320b-254">False</span><span class="sxs-lookup"><span data-stu-id="1320b-254">False</span></span>                                            |
| <span data-ttu-id="1320b-255">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1320b-255">Is-Single-Valued</span></span>       | <span data-ttu-id="1320b-256">False</span><span class="sxs-lookup"><span data-stu-id="1320b-256">False</span></span>                                            |
| <span data-ttu-id="1320b-257">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1320b-257">Is Indexed</span></span>             | <span data-ttu-id="1320b-258">False</span><span class="sxs-lookup"><span data-stu-id="1320b-258">False</span></span>                                            |
| <span data-ttu-id="1320b-259">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1320b-259">In Global Catalog</span></span>      | <span data-ttu-id="1320b-260">False</span><span class="sxs-lookup"><span data-stu-id="1320b-260">False</span></span>                                            |
| <span data-ttu-id="1320b-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1320b-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="1320b-262">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1320b-262">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="1320b-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1320b-263">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="1320b-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1320b-264">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="1320b-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1320b-265">Search-Flags</span></span>           | <span data-ttu-id="1320b-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1320b-266">0x00000000</span></span>                                       |
| <span data-ttu-id="1320b-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1320b-267">System-Flags</span></span>           | <span data-ttu-id="1320b-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1320b-268">0x00000010</span></span>                                       |
| <span data-ttu-id="1320b-269">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1320b-269">Classes used in</span></span>        | [<span data-ttu-id="1320b-270">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="1320b-270">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1320b-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1320b-271">Windows Server 2012</span></span>



| <span data-ttu-id="1320b-272">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1320b-272">Entry</span></span> | <span data-ttu-id="1320b-273">Wert</span><span class="sxs-lookup"><span data-stu-id="1320b-273">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="1320b-274">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1320b-274">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="1320b-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1320b-275">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="1320b-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="1320b-276">System-Only</span></span>            | <span data-ttu-id="1320b-277">False</span><span class="sxs-lookup"><span data-stu-id="1320b-277">False</span></span>                                            |
| <span data-ttu-id="1320b-278">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1320b-278">Is-Single-Valued</span></span>       | <span data-ttu-id="1320b-279">False</span><span class="sxs-lookup"><span data-stu-id="1320b-279">False</span></span>                                            |
| <span data-ttu-id="1320b-280">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1320b-280">Is Indexed</span></span>             | <span data-ttu-id="1320b-281">False</span><span class="sxs-lookup"><span data-stu-id="1320b-281">False</span></span>                                            |
| <span data-ttu-id="1320b-282">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1320b-282">In Global Catalog</span></span>      | <span data-ttu-id="1320b-283">False</span><span class="sxs-lookup"><span data-stu-id="1320b-283">False</span></span>                                            |
| <span data-ttu-id="1320b-284">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1320b-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="1320b-285">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1320b-285">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="1320b-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1320b-286">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="1320b-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1320b-287">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="1320b-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1320b-288">Search-Flags</span></span>           | <span data-ttu-id="1320b-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1320b-289">0x00000000</span></span>                                       |
| <span data-ttu-id="1320b-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1320b-290">System-Flags</span></span>           | <span data-ttu-id="1320b-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1320b-291">0x00000010</span></span>                                       |
| <span data-ttu-id="1320b-292">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1320b-292">Classes used in</span></span>        | [<span data-ttu-id="1320b-293">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="1320b-293">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





