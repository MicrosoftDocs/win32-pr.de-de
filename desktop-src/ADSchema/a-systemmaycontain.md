---
title: System-darf-Attribut enthalten
description: Die Liste optionaler Attribute für eine Klasse. Die Liste der Attribute kann nur vom System geändert werden.
ms.assetid: b2fbeb64-d147-4c1a-a609-4f16327609ce
ms.tgt_platform: multiple
keywords:
- AD-Schema des Attributs "System-May"
- Active Directory-Attribut (AD-Schema)
topic_type:
- apiref
api_name:
- System-May-Contain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c03730e9904cbaa6ee5954662556fba261c51cd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107504"
---
# <a name="system-may-contain-attribute"></a><span data-ttu-id="ead0f-106">System-darf-Attribut enthalten</span><span class="sxs-lookup"><span data-stu-id="ead0f-106">System-May-Contain attribute</span></span>

<span data-ttu-id="ead0f-107">Die Liste optionaler Attribute für eine Klasse.</span><span class="sxs-lookup"><span data-stu-id="ead0f-107">The list of optional attributes for a class.</span></span> <span data-ttu-id="ead0f-108">Die Liste der Attribute kann nur vom System geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ead0f-108">The list of attributes can only be modified by the system.</span></span>



| <span data-ttu-id="ead0f-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ead0f-109">Entry</span></span> | <span data-ttu-id="ead0f-110">Wert</span><span class="sxs-lookup"><span data-stu-id="ead0f-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ead0f-111">CN</span><span class="sxs-lookup"><span data-stu-id="ead0f-111">CN</span></span>                | <span data-ttu-id="ead0f-112">System-kann enthalten</span><span class="sxs-lookup"><span data-stu-id="ead0f-112">System-May-Contain</span></span>                                                           |
| <span data-ttu-id="ead0f-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ead0f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ead0f-114">systemmay-enthalten</span><span class="sxs-lookup"><span data-stu-id="ead0f-114">systemMayContain</span></span>                                                             |
| <span data-ttu-id="ead0f-115">Size</span><span class="sxs-lookup"><span data-stu-id="ead0f-115">Size</span></span>              | \-                                                                           |
| <span data-ttu-id="ead0f-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ead0f-116">Update Privilege</span></span>  | <span data-ttu-id="ead0f-117">Schema Administrator</span><span class="sxs-lookup"><span data-stu-id="ead0f-117">Schema administrator</span></span>                                                         |
| <span data-ttu-id="ead0f-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="ead0f-118">Update Frequency</span></span>  | <span data-ttu-id="ead0f-119">Wenn die-Klasse erstellt wird oder ein neues optionales-Attribut zur-Klasse hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="ead0f-119">When the class is created or a new optional attribute is added to the class.</span></span> |
| <span data-ttu-id="ead0f-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ead0f-120">Attribute-Id</span></span>      | <span data-ttu-id="ead0f-121">1.2.840.113556.1.4.196</span><span class="sxs-lookup"><span data-stu-id="ead0f-121">1.2.840.113556.1.4.196</span></span>                                                       |
| <span data-ttu-id="ead0f-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ead0f-122">System-Id-Guid</span></span>    | <span data-ttu-id="ead0f-123">bf967a44-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ead0f-123">bf967a44-0de6-11d0-a285-00aa003049e2</span></span>                                         |
| <span data-ttu-id="ead0f-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="ead0f-124">Syntax</span></span>            | [<span data-ttu-id="ead0f-125">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="ead0f-125">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md)              |



## <a name="implementations"></a><span data-ttu-id="ead0f-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="ead0f-126">Implementations</span></span>

-   [<span data-ttu-id="ead0f-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ead0f-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ead0f-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ead0f-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ead0f-129">**Adam**</span><span class="sxs-lookup"><span data-stu-id="ead0f-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ead0f-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ead0f-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ead0f-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ead0f-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ead0f-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ead0f-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ead0f-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ead0f-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ead0f-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ead0f-134">Windows 2000 Server</span></span>



| <span data-ttu-id="ead0f-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ead0f-135">Entry</span></span> | <span data-ttu-id="ead0f-136">Wert</span><span class="sxs-lookup"><span data-stu-id="ead0f-136">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ead0f-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ead0f-137">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ead0f-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead0f-138">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ead0f-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead0f-139">System-Only</span></span>            | <span data-ttu-id="ead0f-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="ead0f-140">True</span></span>                                             |
| <span data-ttu-id="ead0f-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ead0f-141">Is-Single-Valued</span></span>       | <span data-ttu-id="ead0f-142">False</span><span class="sxs-lookup"><span data-stu-id="ead0f-142">False</span></span>                                            |
| <span data-ttu-id="ead0f-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ead0f-143">Is Indexed</span></span>             | <span data-ttu-id="ead0f-144">False</span><span class="sxs-lookup"><span data-stu-id="ead0f-144">False</span></span>                                            |
| <span data-ttu-id="ead0f-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ead0f-145">In Global Catalog</span></span>      | <span data-ttu-id="ead0f-146">False</span><span class="sxs-lookup"><span data-stu-id="ead0f-146">False</span></span>                                            |
| <span data-ttu-id="ead0f-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ead0f-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead0f-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ead0f-148">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ead0f-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead0f-149">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ead0f-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead0f-150">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ead0f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead0f-151">Search-Flags</span></span>           | <span data-ttu-id="ead0f-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ead0f-152">0x00000000</span></span>                                       |
| <span data-ttu-id="ead0f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead0f-153">System-Flags</span></span>           | <span data-ttu-id="ead0f-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ead0f-154">0x00000010</span></span>                                       |
| <span data-ttu-id="ead0f-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ead0f-155">Classes used in</span></span>        | [<span data-ttu-id="ead0f-156">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="ead0f-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ead0f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ead0f-157">Windows Server 2003</span></span>



| <span data-ttu-id="ead0f-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ead0f-158">Entry</span></span> | <span data-ttu-id="ead0f-159">Wert</span><span class="sxs-lookup"><span data-stu-id="ead0f-159">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ead0f-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ead0f-160">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ead0f-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead0f-161">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ead0f-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead0f-162">System-Only</span></span>            | <span data-ttu-id="ead0f-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="ead0f-163">True</span></span>                                             |
| <span data-ttu-id="ead0f-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ead0f-164">Is-Single-Valued</span></span>       | <span data-ttu-id="ead0f-165">False</span><span class="sxs-lookup"><span data-stu-id="ead0f-165">False</span></span>                                            |
| <span data-ttu-id="ead0f-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ead0f-166">Is Indexed</span></span>             | <span data-ttu-id="ead0f-167">False</span><span class="sxs-lookup"><span data-stu-id="ead0f-167">False</span></span>                                            |
| <span data-ttu-id="ead0f-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ead0f-168">In Global Catalog</span></span>      | <span data-ttu-id="ead0f-169">False</span><span class="sxs-lookup"><span data-stu-id="ead0f-169">False</span></span>                                            |
| <span data-ttu-id="ead0f-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ead0f-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead0f-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ead0f-171">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ead0f-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead0f-172">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ead0f-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead0f-173">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ead0f-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead0f-174">Search-Flags</span></span>           | <span data-ttu-id="ead0f-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ead0f-175">0x00000000</span></span>                                       |
| <span data-ttu-id="ead0f-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead0f-176">System-Flags</span></span>           | <span data-ttu-id="ead0f-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ead0f-177">0x00000010</span></span>                                       |
| <span data-ttu-id="ead0f-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ead0f-178">Classes used in</span></span>        | [<span data-ttu-id="ead0f-179">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="ead0f-179">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ead0f-180">Adam</span><span class="sxs-lookup"><span data-stu-id="ead0f-180">ADAM</span></span>



| <span data-ttu-id="ead0f-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ead0f-181">Entry</span></span> | <span data-ttu-id="ead0f-182">Wert</span><span class="sxs-lookup"><span data-stu-id="ead0f-182">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ead0f-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ead0f-183">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ead0f-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead0f-184">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ead0f-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead0f-185">System-Only</span></span>            | <span data-ttu-id="ead0f-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="ead0f-186">True</span></span>                                             |
| <span data-ttu-id="ead0f-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ead0f-187">Is-Single-Valued</span></span>       | <span data-ttu-id="ead0f-188">False</span><span class="sxs-lookup"><span data-stu-id="ead0f-188">False</span></span>                                            |
| <span data-ttu-id="ead0f-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ead0f-189">Is Indexed</span></span>             | <span data-ttu-id="ead0f-190">False</span><span class="sxs-lookup"><span data-stu-id="ead0f-190">False</span></span>                                            |
| <span data-ttu-id="ead0f-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ead0f-191">In Global Catalog</span></span>      | <span data-ttu-id="ead0f-192">False</span><span class="sxs-lookup"><span data-stu-id="ead0f-192">False</span></span>                                            |
| <span data-ttu-id="ead0f-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ead0f-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead0f-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ead0f-194">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ead0f-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead0f-195">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ead0f-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead0f-196">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ead0f-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead0f-197">Search-Flags</span></span>           | <span data-ttu-id="ead0f-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ead0f-198">0x00000000</span></span>                                       |
| <span data-ttu-id="ead0f-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead0f-199">System-Flags</span></span>           | <span data-ttu-id="ead0f-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ead0f-200">0x00000010</span></span>                                       |
| <span data-ttu-id="ead0f-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ead0f-201">Classes used in</span></span>        | [<span data-ttu-id="ead0f-202">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="ead0f-202">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ead0f-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ead0f-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ead0f-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ead0f-204">Entry</span></span> | <span data-ttu-id="ead0f-205">Wert</span><span class="sxs-lookup"><span data-stu-id="ead0f-205">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ead0f-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ead0f-206">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ead0f-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead0f-207">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ead0f-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead0f-208">System-Only</span></span>            | <span data-ttu-id="ead0f-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="ead0f-209">True</span></span>                                             |
| <span data-ttu-id="ead0f-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ead0f-210">Is-Single-Valued</span></span>       | <span data-ttu-id="ead0f-211">False</span><span class="sxs-lookup"><span data-stu-id="ead0f-211">False</span></span>                                            |
| <span data-ttu-id="ead0f-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ead0f-212">Is Indexed</span></span>             | <span data-ttu-id="ead0f-213">False</span><span class="sxs-lookup"><span data-stu-id="ead0f-213">False</span></span>                                            |
| <span data-ttu-id="ead0f-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ead0f-214">In Global Catalog</span></span>      | <span data-ttu-id="ead0f-215">False</span><span class="sxs-lookup"><span data-stu-id="ead0f-215">False</span></span>                                            |
| <span data-ttu-id="ead0f-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ead0f-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead0f-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ead0f-217">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ead0f-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead0f-218">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ead0f-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead0f-219">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ead0f-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead0f-220">Search-Flags</span></span>           | <span data-ttu-id="ead0f-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ead0f-221">0x00000000</span></span>                                       |
| <span data-ttu-id="ead0f-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead0f-222">System-Flags</span></span>           | <span data-ttu-id="ead0f-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ead0f-223">0x00000010</span></span>                                       |
| <span data-ttu-id="ead0f-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ead0f-224">Classes used in</span></span>        | [<span data-ttu-id="ead0f-225">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="ead0f-225">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ead0f-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ead0f-226">Windows Server 2008</span></span>



| <span data-ttu-id="ead0f-227">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ead0f-227">Entry</span></span> | <span data-ttu-id="ead0f-228">Wert</span><span class="sxs-lookup"><span data-stu-id="ead0f-228">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ead0f-229">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ead0f-229">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ead0f-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead0f-230">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ead0f-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead0f-231">System-Only</span></span>            | <span data-ttu-id="ead0f-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="ead0f-232">True</span></span>                                             |
| <span data-ttu-id="ead0f-233">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ead0f-233">Is-Single-Valued</span></span>       | <span data-ttu-id="ead0f-234">False</span><span class="sxs-lookup"><span data-stu-id="ead0f-234">False</span></span>                                            |
| <span data-ttu-id="ead0f-235">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ead0f-235">Is Indexed</span></span>             | <span data-ttu-id="ead0f-236">False</span><span class="sxs-lookup"><span data-stu-id="ead0f-236">False</span></span>                                            |
| <span data-ttu-id="ead0f-237">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ead0f-237">In Global Catalog</span></span>      | <span data-ttu-id="ead0f-238">False</span><span class="sxs-lookup"><span data-stu-id="ead0f-238">False</span></span>                                            |
| <span data-ttu-id="ead0f-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ead0f-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead0f-240">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ead0f-240">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ead0f-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead0f-241">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ead0f-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead0f-242">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ead0f-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead0f-243">Search-Flags</span></span>           | <span data-ttu-id="ead0f-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ead0f-244">0x00000000</span></span>                                       |
| <span data-ttu-id="ead0f-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead0f-245">System-Flags</span></span>           | <span data-ttu-id="ead0f-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ead0f-246">0x00000010</span></span>                                       |
| <span data-ttu-id="ead0f-247">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ead0f-247">Classes used in</span></span>        | [<span data-ttu-id="ead0f-248">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="ead0f-248">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ead0f-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ead0f-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ead0f-250">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ead0f-250">Entry</span></span> | <span data-ttu-id="ead0f-251">Wert</span><span class="sxs-lookup"><span data-stu-id="ead0f-251">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ead0f-252">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ead0f-252">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ead0f-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead0f-253">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ead0f-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead0f-254">System-Only</span></span>            | <span data-ttu-id="ead0f-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="ead0f-255">True</span></span>                                             |
| <span data-ttu-id="ead0f-256">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ead0f-256">Is-Single-Valued</span></span>       | <span data-ttu-id="ead0f-257">False</span><span class="sxs-lookup"><span data-stu-id="ead0f-257">False</span></span>                                            |
| <span data-ttu-id="ead0f-258">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ead0f-258">Is Indexed</span></span>             | <span data-ttu-id="ead0f-259">False</span><span class="sxs-lookup"><span data-stu-id="ead0f-259">False</span></span>                                            |
| <span data-ttu-id="ead0f-260">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ead0f-260">In Global Catalog</span></span>      | <span data-ttu-id="ead0f-261">False</span><span class="sxs-lookup"><span data-stu-id="ead0f-261">False</span></span>                                            |
| <span data-ttu-id="ead0f-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ead0f-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead0f-263">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ead0f-263">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ead0f-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead0f-264">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ead0f-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead0f-265">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ead0f-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead0f-266">Search-Flags</span></span>           | <span data-ttu-id="ead0f-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ead0f-267">0x00000000</span></span>                                       |
| <span data-ttu-id="ead0f-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead0f-268">System-Flags</span></span>           | <span data-ttu-id="ead0f-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ead0f-269">0x00000010</span></span>                                       |
| <span data-ttu-id="ead0f-270">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ead0f-270">Classes used in</span></span>        | [<span data-ttu-id="ead0f-271">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="ead0f-271">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ead0f-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ead0f-272">Windows Server 2012</span></span>



| <span data-ttu-id="ead0f-273">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ead0f-273">Entry</span></span> | <span data-ttu-id="ead0f-274">Wert</span><span class="sxs-lookup"><span data-stu-id="ead0f-274">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ead0f-275">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ead0f-275">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ead0f-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead0f-276">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ead0f-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead0f-277">System-Only</span></span>            | <span data-ttu-id="ead0f-278">Richtig</span><span class="sxs-lookup"><span data-stu-id="ead0f-278">True</span></span>                                             |
| <span data-ttu-id="ead0f-279">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ead0f-279">Is-Single-Valued</span></span>       | <span data-ttu-id="ead0f-280">False</span><span class="sxs-lookup"><span data-stu-id="ead0f-280">False</span></span>                                            |
| <span data-ttu-id="ead0f-281">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ead0f-281">Is Indexed</span></span>             | <span data-ttu-id="ead0f-282">False</span><span class="sxs-lookup"><span data-stu-id="ead0f-282">False</span></span>                                            |
| <span data-ttu-id="ead0f-283">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ead0f-283">In Global Catalog</span></span>      | <span data-ttu-id="ead0f-284">False</span><span class="sxs-lookup"><span data-stu-id="ead0f-284">False</span></span>                                            |
| <span data-ttu-id="ead0f-285">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ead0f-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead0f-286">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ead0f-286">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ead0f-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead0f-287">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ead0f-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead0f-288">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ead0f-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead0f-289">Search-Flags</span></span>           | <span data-ttu-id="ead0f-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ead0f-290">0x00000000</span></span>                                       |
| <span data-ttu-id="ead0f-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead0f-291">System-Flags</span></span>           | <span data-ttu-id="ead0f-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ead0f-292">0x00000010</span></span>                                       |
| <span data-ttu-id="ead0f-293">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ead0f-293">Classes used in</span></span>        | [<span data-ttu-id="ead0f-294">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="ead0f-294">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





