---
title: System-muss-Attribute enthalten
description: Die Liste der obligatorischen Attribute für eine Klasse. Diese Attribute müssen angegeben werden, wenn eine Instanz der-Klasse erstellt wird. Die Liste der Attribute kann nur vom System geändert werden.
ms.assetid: 5131bd16-1a8d-4d4a-98e4-6140438c6517
ms.tgt_platform: multiple
keywords:
- AD-Schema für das System-muss-Attribut enthalten
- cschema des systemmustare-Attributs
topic_type:
- apiref
api_name:
- System-Must-Contain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f8d36419ca7e6cd24422645579fb7f9ecc69457
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519967"
---
# <a name="system-must-contain-attribute"></a><span data-ttu-id="38fd0-107">System-muss-Attribute enthalten</span><span class="sxs-lookup"><span data-stu-id="38fd0-107">System-Must-Contain attribute</span></span>

<span data-ttu-id="38fd0-108">Die Liste der obligatorischen Attribute für eine Klasse.</span><span class="sxs-lookup"><span data-stu-id="38fd0-108">The list of mandatory attributes for a class.</span></span> <span data-ttu-id="38fd0-109">Diese Attribute müssen angegeben werden, wenn eine Instanz der-Klasse erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="38fd0-109">These attributes must be specified when an instance of the class is created.</span></span> <span data-ttu-id="38fd0-110">Die Liste der Attribute kann nur vom System geändert werden.</span><span class="sxs-lookup"><span data-stu-id="38fd0-110">The list of attributes can only be modified by the system.</span></span>



| <span data-ttu-id="38fd0-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38fd0-111">Entry</span></span> | <span data-ttu-id="38fd0-112">Wert</span><span class="sxs-lookup"><span data-stu-id="38fd0-112">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="38fd0-113">CN</span><span class="sxs-lookup"><span data-stu-id="38fd0-113">CN</span></span>                | <span data-ttu-id="38fd0-114">System-muss enthalten</span><span class="sxs-lookup"><span data-stu-id="38fd0-114">System-Must-Contain</span></span>                                                           |
| <span data-ttu-id="38fd0-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="38fd0-115">Ldap-Display-Name</span></span> | <span data-ttu-id="38fd0-116">systemmustenthalten</span><span class="sxs-lookup"><span data-stu-id="38fd0-116">systemMustContain</span></span>                                                             |
| <span data-ttu-id="38fd0-117">Size</span><span class="sxs-lookup"><span data-stu-id="38fd0-117">Size</span></span>              | \-                                                                            |
| <span data-ttu-id="38fd0-118">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="38fd0-118">Update Privilege</span></span>  | <span data-ttu-id="38fd0-119">Schema Administrator</span><span class="sxs-lookup"><span data-stu-id="38fd0-119">Schema administrator</span></span>                                                          |
| <span data-ttu-id="38fd0-120">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="38fd0-120">Update Frequency</span></span>  | <span data-ttu-id="38fd0-121">Wenn die Klasse erstellt wird oder ein neues obligatorisches Attribut der Klasse hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="38fd0-121">When the class is created or a new mandatory attribute is added to the class.</span></span> |
| <span data-ttu-id="38fd0-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="38fd0-122">Attribute-Id</span></span>      | <span data-ttu-id="38fd0-123">1.2.840.113556.1.4.197</span><span class="sxs-lookup"><span data-stu-id="38fd0-123">1.2.840.113556.1.4.197</span></span>                                                        |
| <span data-ttu-id="38fd0-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="38fd0-124">System-Id-Guid</span></span>    | <span data-ttu-id="38fd0-125">bf967a45-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="38fd0-125">bf967a45-0de6-11d0-a285-00aa003049e2</span></span>                                          |
| <span data-ttu-id="38fd0-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="38fd0-126">Syntax</span></span>            | [<span data-ttu-id="38fd0-127">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="38fd0-127">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md)               |



## <a name="implementations"></a><span data-ttu-id="38fd0-128">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="38fd0-128">Implementations</span></span>

-   [<span data-ttu-id="38fd0-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="38fd0-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="38fd0-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="38fd0-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="38fd0-131">**Adam**</span><span class="sxs-lookup"><span data-stu-id="38fd0-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="38fd0-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="38fd0-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="38fd0-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="38fd0-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="38fd0-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="38fd0-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="38fd0-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="38fd0-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="38fd0-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="38fd0-136">Windows 2000 Server</span></span>



| <span data-ttu-id="38fd0-137">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38fd0-137">Entry</span></span> | <span data-ttu-id="38fd0-138">Wert</span><span class="sxs-lookup"><span data-stu-id="38fd0-138">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="38fd0-139">Link-ID</span><span class="sxs-lookup"><span data-stu-id="38fd0-139">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="38fd0-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38fd0-140">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="38fd0-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="38fd0-141">System-Only</span></span>            | <span data-ttu-id="38fd0-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="38fd0-142">True</span></span>                                             |
| <span data-ttu-id="38fd0-143">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="38fd0-143">Is-Single-Valued</span></span>       | <span data-ttu-id="38fd0-144">False</span><span class="sxs-lookup"><span data-stu-id="38fd0-144">False</span></span>                                            |
| <span data-ttu-id="38fd0-145">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="38fd0-145">Is Indexed</span></span>             | <span data-ttu-id="38fd0-146">False</span><span class="sxs-lookup"><span data-stu-id="38fd0-146">False</span></span>                                            |
| <span data-ttu-id="38fd0-147">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="38fd0-147">In Global Catalog</span></span>      | <span data-ttu-id="38fd0-148">False</span><span class="sxs-lookup"><span data-stu-id="38fd0-148">False</span></span>                                            |
| <span data-ttu-id="38fd0-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="38fd0-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="38fd0-150">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="38fd0-150">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="38fd0-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38fd0-151">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="38fd0-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38fd0-152">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="38fd0-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38fd0-153">Search-Flags</span></span>           | <span data-ttu-id="38fd0-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38fd0-154">0x00000000</span></span>                                       |
| <span data-ttu-id="38fd0-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38fd0-155">System-Flags</span></span>           | <span data-ttu-id="38fd0-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38fd0-156">0x00000010</span></span>                                       |
| <span data-ttu-id="38fd0-157">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="38fd0-157">Classes used in</span></span>        | [<span data-ttu-id="38fd0-158">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="38fd0-158">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="38fd0-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="38fd0-159">Windows Server 2003</span></span>



| <span data-ttu-id="38fd0-160">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38fd0-160">Entry</span></span> | <span data-ttu-id="38fd0-161">Wert</span><span class="sxs-lookup"><span data-stu-id="38fd0-161">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="38fd0-162">Link-ID</span><span class="sxs-lookup"><span data-stu-id="38fd0-162">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="38fd0-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38fd0-163">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="38fd0-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="38fd0-164">System-Only</span></span>            | <span data-ttu-id="38fd0-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="38fd0-165">True</span></span>                                             |
| <span data-ttu-id="38fd0-166">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="38fd0-166">Is-Single-Valued</span></span>       | <span data-ttu-id="38fd0-167">False</span><span class="sxs-lookup"><span data-stu-id="38fd0-167">False</span></span>                                            |
| <span data-ttu-id="38fd0-168">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="38fd0-168">Is Indexed</span></span>             | <span data-ttu-id="38fd0-169">False</span><span class="sxs-lookup"><span data-stu-id="38fd0-169">False</span></span>                                            |
| <span data-ttu-id="38fd0-170">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="38fd0-170">In Global Catalog</span></span>      | <span data-ttu-id="38fd0-171">False</span><span class="sxs-lookup"><span data-stu-id="38fd0-171">False</span></span>                                            |
| <span data-ttu-id="38fd0-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="38fd0-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="38fd0-173">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="38fd0-173">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="38fd0-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38fd0-174">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="38fd0-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38fd0-175">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="38fd0-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38fd0-176">Search-Flags</span></span>           | <span data-ttu-id="38fd0-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38fd0-177">0x00000000</span></span>                                       |
| <span data-ttu-id="38fd0-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38fd0-178">System-Flags</span></span>           | <span data-ttu-id="38fd0-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38fd0-179">0x00000010</span></span>                                       |
| <span data-ttu-id="38fd0-180">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="38fd0-180">Classes used in</span></span>        | [<span data-ttu-id="38fd0-181">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="38fd0-181">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="38fd0-182">Adam</span><span class="sxs-lookup"><span data-stu-id="38fd0-182">ADAM</span></span>



| <span data-ttu-id="38fd0-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38fd0-183">Entry</span></span> | <span data-ttu-id="38fd0-184">Wert</span><span class="sxs-lookup"><span data-stu-id="38fd0-184">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="38fd0-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="38fd0-185">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="38fd0-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38fd0-186">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="38fd0-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="38fd0-187">System-Only</span></span>            | <span data-ttu-id="38fd0-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="38fd0-188">True</span></span>                                             |
| <span data-ttu-id="38fd0-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="38fd0-189">Is-Single-Valued</span></span>       | <span data-ttu-id="38fd0-190">False</span><span class="sxs-lookup"><span data-stu-id="38fd0-190">False</span></span>                                            |
| <span data-ttu-id="38fd0-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="38fd0-191">Is Indexed</span></span>             | <span data-ttu-id="38fd0-192">False</span><span class="sxs-lookup"><span data-stu-id="38fd0-192">False</span></span>                                            |
| <span data-ttu-id="38fd0-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="38fd0-193">In Global Catalog</span></span>      | <span data-ttu-id="38fd0-194">False</span><span class="sxs-lookup"><span data-stu-id="38fd0-194">False</span></span>                                            |
| <span data-ttu-id="38fd0-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="38fd0-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="38fd0-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="38fd0-196">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="38fd0-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38fd0-197">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="38fd0-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38fd0-198">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="38fd0-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38fd0-199">Search-Flags</span></span>           | <span data-ttu-id="38fd0-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38fd0-200">0x00000000</span></span>                                       |
| <span data-ttu-id="38fd0-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38fd0-201">System-Flags</span></span>           | <span data-ttu-id="38fd0-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38fd0-202">0x00000010</span></span>                                       |
| <span data-ttu-id="38fd0-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="38fd0-203">Classes used in</span></span>        | [<span data-ttu-id="38fd0-204">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="38fd0-204">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="38fd0-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="38fd0-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="38fd0-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38fd0-206">Entry</span></span> | <span data-ttu-id="38fd0-207">Wert</span><span class="sxs-lookup"><span data-stu-id="38fd0-207">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="38fd0-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="38fd0-208">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="38fd0-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38fd0-209">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="38fd0-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="38fd0-210">System-Only</span></span>            | <span data-ttu-id="38fd0-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="38fd0-211">True</span></span>                                             |
| <span data-ttu-id="38fd0-212">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="38fd0-212">Is-Single-Valued</span></span>       | <span data-ttu-id="38fd0-213">False</span><span class="sxs-lookup"><span data-stu-id="38fd0-213">False</span></span>                                            |
| <span data-ttu-id="38fd0-214">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="38fd0-214">Is Indexed</span></span>             | <span data-ttu-id="38fd0-215">False</span><span class="sxs-lookup"><span data-stu-id="38fd0-215">False</span></span>                                            |
| <span data-ttu-id="38fd0-216">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="38fd0-216">In Global Catalog</span></span>      | <span data-ttu-id="38fd0-217">False</span><span class="sxs-lookup"><span data-stu-id="38fd0-217">False</span></span>                                            |
| <span data-ttu-id="38fd0-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="38fd0-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="38fd0-219">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="38fd0-219">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="38fd0-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38fd0-220">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="38fd0-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38fd0-221">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="38fd0-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38fd0-222">Search-Flags</span></span>           | <span data-ttu-id="38fd0-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38fd0-223">0x00000000</span></span>                                       |
| <span data-ttu-id="38fd0-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38fd0-224">System-Flags</span></span>           | <span data-ttu-id="38fd0-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38fd0-225">0x00000010</span></span>                                       |
| <span data-ttu-id="38fd0-226">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="38fd0-226">Classes used in</span></span>        | [<span data-ttu-id="38fd0-227">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="38fd0-227">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="38fd0-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38fd0-228">Windows Server 2008</span></span>



| <span data-ttu-id="38fd0-229">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38fd0-229">Entry</span></span> | <span data-ttu-id="38fd0-230">Wert</span><span class="sxs-lookup"><span data-stu-id="38fd0-230">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="38fd0-231">Link-ID</span><span class="sxs-lookup"><span data-stu-id="38fd0-231">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="38fd0-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38fd0-232">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="38fd0-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="38fd0-233">System-Only</span></span>            | <span data-ttu-id="38fd0-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="38fd0-234">True</span></span>                                             |
| <span data-ttu-id="38fd0-235">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="38fd0-235">Is-Single-Valued</span></span>       | <span data-ttu-id="38fd0-236">False</span><span class="sxs-lookup"><span data-stu-id="38fd0-236">False</span></span>                                            |
| <span data-ttu-id="38fd0-237">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="38fd0-237">Is Indexed</span></span>             | <span data-ttu-id="38fd0-238">False</span><span class="sxs-lookup"><span data-stu-id="38fd0-238">False</span></span>                                            |
| <span data-ttu-id="38fd0-239">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="38fd0-239">In Global Catalog</span></span>      | <span data-ttu-id="38fd0-240">False</span><span class="sxs-lookup"><span data-stu-id="38fd0-240">False</span></span>                                            |
| <span data-ttu-id="38fd0-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="38fd0-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="38fd0-242">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="38fd0-242">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="38fd0-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38fd0-243">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="38fd0-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38fd0-244">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="38fd0-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38fd0-245">Search-Flags</span></span>           | <span data-ttu-id="38fd0-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38fd0-246">0x00000000</span></span>                                       |
| <span data-ttu-id="38fd0-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38fd0-247">System-Flags</span></span>           | <span data-ttu-id="38fd0-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38fd0-248">0x00000010</span></span>                                       |
| <span data-ttu-id="38fd0-249">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="38fd0-249">Classes used in</span></span>        | [<span data-ttu-id="38fd0-250">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="38fd0-250">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="38fd0-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="38fd0-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="38fd0-252">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38fd0-252">Entry</span></span> | <span data-ttu-id="38fd0-253">Wert</span><span class="sxs-lookup"><span data-stu-id="38fd0-253">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="38fd0-254">Link-ID</span><span class="sxs-lookup"><span data-stu-id="38fd0-254">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="38fd0-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38fd0-255">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="38fd0-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="38fd0-256">System-Only</span></span>            | <span data-ttu-id="38fd0-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="38fd0-257">True</span></span>                                             |
| <span data-ttu-id="38fd0-258">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="38fd0-258">Is-Single-Valued</span></span>       | <span data-ttu-id="38fd0-259">False</span><span class="sxs-lookup"><span data-stu-id="38fd0-259">False</span></span>                                            |
| <span data-ttu-id="38fd0-260">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="38fd0-260">Is Indexed</span></span>             | <span data-ttu-id="38fd0-261">False</span><span class="sxs-lookup"><span data-stu-id="38fd0-261">False</span></span>                                            |
| <span data-ttu-id="38fd0-262">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="38fd0-262">In Global Catalog</span></span>      | <span data-ttu-id="38fd0-263">False</span><span class="sxs-lookup"><span data-stu-id="38fd0-263">False</span></span>                                            |
| <span data-ttu-id="38fd0-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="38fd0-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="38fd0-265">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="38fd0-265">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="38fd0-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38fd0-266">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="38fd0-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38fd0-267">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="38fd0-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38fd0-268">Search-Flags</span></span>           | <span data-ttu-id="38fd0-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38fd0-269">0x00000000</span></span>                                       |
| <span data-ttu-id="38fd0-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38fd0-270">System-Flags</span></span>           | <span data-ttu-id="38fd0-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38fd0-271">0x00000010</span></span>                                       |
| <span data-ttu-id="38fd0-272">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="38fd0-272">Classes used in</span></span>        | [<span data-ttu-id="38fd0-273">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="38fd0-273">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="38fd0-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="38fd0-274">Windows Server 2012</span></span>



| <span data-ttu-id="38fd0-275">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38fd0-275">Entry</span></span> | <span data-ttu-id="38fd0-276">Wert</span><span class="sxs-lookup"><span data-stu-id="38fd0-276">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="38fd0-277">Link-ID</span><span class="sxs-lookup"><span data-stu-id="38fd0-277">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="38fd0-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38fd0-278">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="38fd0-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="38fd0-279">System-Only</span></span>            | <span data-ttu-id="38fd0-280">Richtig</span><span class="sxs-lookup"><span data-stu-id="38fd0-280">True</span></span>                                             |
| <span data-ttu-id="38fd0-281">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="38fd0-281">Is-Single-Valued</span></span>       | <span data-ttu-id="38fd0-282">False</span><span class="sxs-lookup"><span data-stu-id="38fd0-282">False</span></span>                                            |
| <span data-ttu-id="38fd0-283">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="38fd0-283">Is Indexed</span></span>             | <span data-ttu-id="38fd0-284">False</span><span class="sxs-lookup"><span data-stu-id="38fd0-284">False</span></span>                                            |
| <span data-ttu-id="38fd0-285">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="38fd0-285">In Global Catalog</span></span>      | <span data-ttu-id="38fd0-286">False</span><span class="sxs-lookup"><span data-stu-id="38fd0-286">False</span></span>                                            |
| <span data-ttu-id="38fd0-287">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="38fd0-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="38fd0-288">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="38fd0-288">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="38fd0-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38fd0-289">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="38fd0-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38fd0-290">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="38fd0-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38fd0-291">Search-Flags</span></span>           | <span data-ttu-id="38fd0-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38fd0-292">0x00000000</span></span>                                       |
| <span data-ttu-id="38fd0-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38fd0-293">System-Flags</span></span>           | <span data-ttu-id="38fd0-294">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38fd0-294">0x00000010</span></span>                                       |
| <span data-ttu-id="38fd0-295">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="38fd0-295">Classes used in</span></span>        | [<span data-ttu-id="38fd0-296">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="38fd0-296">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





