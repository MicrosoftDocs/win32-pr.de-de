---
title: System-Poss-Vorgesetzten-Attribut
description: Die Liste der Klassen, die diese Klasse enthalten können. Diese Liste kann nur vom System geändert werden.
ms.assetid: 8b98249a-fe9a-4a42-abb8-a8b042250a76
ms.tgt_platform: multiple
keywords:
- AD-Schema für das System-Poss-Vorgesetzten-Attribut
- Systembesitzer-Attribut AD-Schema
topic_type:
- apiref
api_name:
- System-Poss-Superiors
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b2116dfb8d2ad21d8a52854b1eb98ef156eb46a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859752"
---
# <a name="system-poss-superiors-attribute"></a><span data-ttu-id="20d0a-106">System-Poss-Vorgesetzten-Attribut</span><span class="sxs-lookup"><span data-stu-id="20d0a-106">System-Poss-Superiors attribute</span></span>

<span data-ttu-id="20d0a-107">Die Liste der Klassen, die diese Klasse enthalten können.</span><span class="sxs-lookup"><span data-stu-id="20d0a-107">The list of classes that can contain this class.</span></span> <span data-ttu-id="20d0a-108">Diese Liste kann nur vom System geändert werden.</span><span class="sxs-lookup"><span data-stu-id="20d0a-108">This list can only be modified by the system.</span></span>



| <span data-ttu-id="20d0a-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="20d0a-109">Entry</span></span> | <span data-ttu-id="20d0a-110">Wert</span><span class="sxs-lookup"><span data-stu-id="20d0a-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="20d0a-111">CN</span><span class="sxs-lookup"><span data-stu-id="20d0a-111">CN</span></span>                | <span data-ttu-id="20d0a-112">System-Poss-Vorgesetzten</span><span class="sxs-lookup"><span data-stu-id="20d0a-112">System-Poss-Superiors</span></span>                                                       |
| <span data-ttu-id="20d0a-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="20d0a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="20d0a-114">systempossvorgesetzten</span><span class="sxs-lookup"><span data-stu-id="20d0a-114">systemPossSuperiors</span></span>                                                         |
| <span data-ttu-id="20d0a-115">Size</span><span class="sxs-lookup"><span data-stu-id="20d0a-115">Size</span></span>              | \-                                                                          |
| <span data-ttu-id="20d0a-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="20d0a-116">Update Privilege</span></span>  | <span data-ttu-id="20d0a-117">Schema Administrator</span><span class="sxs-lookup"><span data-stu-id="20d0a-117">Schema administrator</span></span>                                                        |
| <span data-ttu-id="20d0a-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="20d0a-118">Update Frequency</span></span>  | <span data-ttu-id="20d0a-119">Wenn die Klasse erstellt oder eine neue mögliche übergeordnete Klasse der Klasse hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="20d0a-119">When the class is created or a new possible superior is added to the class.</span></span> |
| <span data-ttu-id="20d0a-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="20d0a-120">Attribute-Id</span></span>      | <span data-ttu-id="20d0a-121">1.2.840.113556.1.4.195</span><span class="sxs-lookup"><span data-stu-id="20d0a-121">1.2.840.113556.1.4.195</span></span>                                                      |
| <span data-ttu-id="20d0a-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="20d0a-122">System-Id-Guid</span></span>    | <span data-ttu-id="20d0a-123">bf967a47-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="20d0a-123">bf967a47-0de6-11d0-a285-00aa003049e2</span></span>                                        |
| <span data-ttu-id="20d0a-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="20d0a-124">Syntax</span></span>            | [<span data-ttu-id="20d0a-125">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="20d0a-125">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md)             |



## <a name="implementations"></a><span data-ttu-id="20d0a-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="20d0a-126">Implementations</span></span>

-   [<span data-ttu-id="20d0a-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="20d0a-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="20d0a-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="20d0a-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="20d0a-129">**Adam**</span><span class="sxs-lookup"><span data-stu-id="20d0a-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="20d0a-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="20d0a-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="20d0a-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="20d0a-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="20d0a-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="20d0a-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="20d0a-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="20d0a-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="20d0a-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="20d0a-134">Windows 2000 Server</span></span>



| <span data-ttu-id="20d0a-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="20d0a-135">Entry</span></span> | <span data-ttu-id="20d0a-136">Wert</span><span class="sxs-lookup"><span data-stu-id="20d0a-136">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="20d0a-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="20d0a-137">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="20d0a-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="20d0a-138">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="20d0a-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="20d0a-139">System-Only</span></span>            | <span data-ttu-id="20d0a-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="20d0a-140">True</span></span>                                             |
| <span data-ttu-id="20d0a-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="20d0a-141">Is-Single-Valued</span></span>       | <span data-ttu-id="20d0a-142">False</span><span class="sxs-lookup"><span data-stu-id="20d0a-142">False</span></span>                                            |
| <span data-ttu-id="20d0a-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="20d0a-143">Is Indexed</span></span>             | <span data-ttu-id="20d0a-144">False</span><span class="sxs-lookup"><span data-stu-id="20d0a-144">False</span></span>                                            |
| <span data-ttu-id="20d0a-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="20d0a-145">In Global Catalog</span></span>      | <span data-ttu-id="20d0a-146">Richtig</span><span class="sxs-lookup"><span data-stu-id="20d0a-146">True</span></span>                                             |
| <span data-ttu-id="20d0a-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="20d0a-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="20d0a-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="20d0a-148">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="20d0a-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="20d0a-149">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="20d0a-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="20d0a-150">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="20d0a-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="20d0a-151">Search-Flags</span></span>           | <span data-ttu-id="20d0a-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="20d0a-152">0x00000000</span></span>                                       |
| <span data-ttu-id="20d0a-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="20d0a-153">System-Flags</span></span>           | <span data-ttu-id="20d0a-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="20d0a-154">0x00000010</span></span>                                       |
| <span data-ttu-id="20d0a-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="20d0a-155">Classes used in</span></span>        | [<span data-ttu-id="20d0a-156">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="20d0a-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="20d0a-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="20d0a-157">Windows Server 2003</span></span>



| <span data-ttu-id="20d0a-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="20d0a-158">Entry</span></span> | <span data-ttu-id="20d0a-159">Wert</span><span class="sxs-lookup"><span data-stu-id="20d0a-159">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="20d0a-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="20d0a-160">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="20d0a-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="20d0a-161">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="20d0a-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="20d0a-162">System-Only</span></span>            | <span data-ttu-id="20d0a-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="20d0a-163">True</span></span>                                             |
| <span data-ttu-id="20d0a-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="20d0a-164">Is-Single-Valued</span></span>       | <span data-ttu-id="20d0a-165">False</span><span class="sxs-lookup"><span data-stu-id="20d0a-165">False</span></span>                                            |
| <span data-ttu-id="20d0a-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="20d0a-166">Is Indexed</span></span>             | <span data-ttu-id="20d0a-167">False</span><span class="sxs-lookup"><span data-stu-id="20d0a-167">False</span></span>                                            |
| <span data-ttu-id="20d0a-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="20d0a-168">In Global Catalog</span></span>      | <span data-ttu-id="20d0a-169">Richtig</span><span class="sxs-lookup"><span data-stu-id="20d0a-169">True</span></span>                                             |
| <span data-ttu-id="20d0a-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="20d0a-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="20d0a-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="20d0a-171">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="20d0a-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="20d0a-172">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="20d0a-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="20d0a-173">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="20d0a-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="20d0a-174">Search-Flags</span></span>           | <span data-ttu-id="20d0a-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="20d0a-175">0x00000000</span></span>                                       |
| <span data-ttu-id="20d0a-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="20d0a-176">System-Flags</span></span>           | <span data-ttu-id="20d0a-177">0x00000012</span><span class="sxs-lookup"><span data-stu-id="20d0a-177">0x00000012</span></span>                                       |
| <span data-ttu-id="20d0a-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="20d0a-178">Classes used in</span></span>        | [<span data-ttu-id="20d0a-179">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="20d0a-179">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="20d0a-180">Adam</span><span class="sxs-lookup"><span data-stu-id="20d0a-180">ADAM</span></span>



| <span data-ttu-id="20d0a-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="20d0a-181">Entry</span></span> | <span data-ttu-id="20d0a-182">Wert</span><span class="sxs-lookup"><span data-stu-id="20d0a-182">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="20d0a-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="20d0a-183">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="20d0a-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="20d0a-184">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="20d0a-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="20d0a-185">System-Only</span></span>            | <span data-ttu-id="20d0a-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="20d0a-186">True</span></span>                                             |
| <span data-ttu-id="20d0a-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="20d0a-187">Is-Single-Valued</span></span>       | <span data-ttu-id="20d0a-188">False</span><span class="sxs-lookup"><span data-stu-id="20d0a-188">False</span></span>                                            |
| <span data-ttu-id="20d0a-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="20d0a-189">Is Indexed</span></span>             | <span data-ttu-id="20d0a-190">False</span><span class="sxs-lookup"><span data-stu-id="20d0a-190">False</span></span>                                            |
| <span data-ttu-id="20d0a-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="20d0a-191">In Global Catalog</span></span>      | <span data-ttu-id="20d0a-192">Richtig</span><span class="sxs-lookup"><span data-stu-id="20d0a-192">True</span></span>                                             |
| <span data-ttu-id="20d0a-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="20d0a-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="20d0a-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="20d0a-194">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="20d0a-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="20d0a-195">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="20d0a-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="20d0a-196">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="20d0a-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="20d0a-197">Search-Flags</span></span>           | <span data-ttu-id="20d0a-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="20d0a-198">0x00000000</span></span>                                       |
| <span data-ttu-id="20d0a-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="20d0a-199">System-Flags</span></span>           | <span data-ttu-id="20d0a-200">0x00000012</span><span class="sxs-lookup"><span data-stu-id="20d0a-200">0x00000012</span></span>                                       |
| <span data-ttu-id="20d0a-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="20d0a-201">Classes used in</span></span>        | [<span data-ttu-id="20d0a-202">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="20d0a-202">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="20d0a-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="20d0a-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="20d0a-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="20d0a-204">Entry</span></span> | <span data-ttu-id="20d0a-205">Wert</span><span class="sxs-lookup"><span data-stu-id="20d0a-205">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="20d0a-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="20d0a-206">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="20d0a-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="20d0a-207">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="20d0a-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="20d0a-208">System-Only</span></span>            | <span data-ttu-id="20d0a-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="20d0a-209">True</span></span>                                             |
| <span data-ttu-id="20d0a-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="20d0a-210">Is-Single-Valued</span></span>       | <span data-ttu-id="20d0a-211">False</span><span class="sxs-lookup"><span data-stu-id="20d0a-211">False</span></span>                                            |
| <span data-ttu-id="20d0a-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="20d0a-212">Is Indexed</span></span>             | <span data-ttu-id="20d0a-213">False</span><span class="sxs-lookup"><span data-stu-id="20d0a-213">False</span></span>                                            |
| <span data-ttu-id="20d0a-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="20d0a-214">In Global Catalog</span></span>      | <span data-ttu-id="20d0a-215">Richtig</span><span class="sxs-lookup"><span data-stu-id="20d0a-215">True</span></span>                                             |
| <span data-ttu-id="20d0a-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="20d0a-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="20d0a-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="20d0a-217">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="20d0a-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="20d0a-218">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="20d0a-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="20d0a-219">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="20d0a-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="20d0a-220">Search-Flags</span></span>           | <span data-ttu-id="20d0a-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="20d0a-221">0x00000000</span></span>                                       |
| <span data-ttu-id="20d0a-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="20d0a-222">System-Flags</span></span>           | <span data-ttu-id="20d0a-223">0x00000012</span><span class="sxs-lookup"><span data-stu-id="20d0a-223">0x00000012</span></span>                                       |
| <span data-ttu-id="20d0a-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="20d0a-224">Classes used in</span></span>        | [<span data-ttu-id="20d0a-225">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="20d0a-225">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="20d0a-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20d0a-226">Windows Server 2008</span></span>



| <span data-ttu-id="20d0a-227">Eingabe</span><span class="sxs-lookup"><span data-stu-id="20d0a-227">Entry</span></span> | <span data-ttu-id="20d0a-228">Wert</span><span class="sxs-lookup"><span data-stu-id="20d0a-228">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="20d0a-229">Link-ID</span><span class="sxs-lookup"><span data-stu-id="20d0a-229">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="20d0a-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="20d0a-230">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="20d0a-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="20d0a-231">System-Only</span></span>            | <span data-ttu-id="20d0a-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="20d0a-232">True</span></span>                                             |
| <span data-ttu-id="20d0a-233">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="20d0a-233">Is-Single-Valued</span></span>       | <span data-ttu-id="20d0a-234">False</span><span class="sxs-lookup"><span data-stu-id="20d0a-234">False</span></span>                                            |
| <span data-ttu-id="20d0a-235">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="20d0a-235">Is Indexed</span></span>             | <span data-ttu-id="20d0a-236">False</span><span class="sxs-lookup"><span data-stu-id="20d0a-236">False</span></span>                                            |
| <span data-ttu-id="20d0a-237">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="20d0a-237">In Global Catalog</span></span>      | <span data-ttu-id="20d0a-238">Richtig</span><span class="sxs-lookup"><span data-stu-id="20d0a-238">True</span></span>                                             |
| <span data-ttu-id="20d0a-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="20d0a-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="20d0a-240">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="20d0a-240">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="20d0a-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="20d0a-241">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="20d0a-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="20d0a-242">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="20d0a-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="20d0a-243">Search-Flags</span></span>           | <span data-ttu-id="20d0a-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="20d0a-244">0x00000000</span></span>                                       |
| <span data-ttu-id="20d0a-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="20d0a-245">System-Flags</span></span>           | <span data-ttu-id="20d0a-246">0x00000012</span><span class="sxs-lookup"><span data-stu-id="20d0a-246">0x00000012</span></span>                                       |
| <span data-ttu-id="20d0a-247">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="20d0a-247">Classes used in</span></span>        | [<span data-ttu-id="20d0a-248">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="20d0a-248">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="20d0a-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="20d0a-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="20d0a-250">Eingabe</span><span class="sxs-lookup"><span data-stu-id="20d0a-250">Entry</span></span> | <span data-ttu-id="20d0a-251">Wert</span><span class="sxs-lookup"><span data-stu-id="20d0a-251">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="20d0a-252">Link-ID</span><span class="sxs-lookup"><span data-stu-id="20d0a-252">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="20d0a-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="20d0a-253">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="20d0a-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="20d0a-254">System-Only</span></span>            | <span data-ttu-id="20d0a-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="20d0a-255">True</span></span>                                             |
| <span data-ttu-id="20d0a-256">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="20d0a-256">Is-Single-Valued</span></span>       | <span data-ttu-id="20d0a-257">False</span><span class="sxs-lookup"><span data-stu-id="20d0a-257">False</span></span>                                            |
| <span data-ttu-id="20d0a-258">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="20d0a-258">Is Indexed</span></span>             | <span data-ttu-id="20d0a-259">False</span><span class="sxs-lookup"><span data-stu-id="20d0a-259">False</span></span>                                            |
| <span data-ttu-id="20d0a-260">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="20d0a-260">In Global Catalog</span></span>      | <span data-ttu-id="20d0a-261">Richtig</span><span class="sxs-lookup"><span data-stu-id="20d0a-261">True</span></span>                                             |
| <span data-ttu-id="20d0a-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="20d0a-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="20d0a-263">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="20d0a-263">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="20d0a-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="20d0a-264">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="20d0a-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="20d0a-265">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="20d0a-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="20d0a-266">Search-Flags</span></span>           | <span data-ttu-id="20d0a-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="20d0a-267">0x00000000</span></span>                                       |
| <span data-ttu-id="20d0a-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="20d0a-268">System-Flags</span></span>           | <span data-ttu-id="20d0a-269">0x00000012</span><span class="sxs-lookup"><span data-stu-id="20d0a-269">0x00000012</span></span>                                       |
| <span data-ttu-id="20d0a-270">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="20d0a-270">Classes used in</span></span>        | [<span data-ttu-id="20d0a-271">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="20d0a-271">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="20d0a-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="20d0a-272">Windows Server 2012</span></span>



| <span data-ttu-id="20d0a-273">Eingabe</span><span class="sxs-lookup"><span data-stu-id="20d0a-273">Entry</span></span> | <span data-ttu-id="20d0a-274">Wert</span><span class="sxs-lookup"><span data-stu-id="20d0a-274">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="20d0a-275">Link-ID</span><span class="sxs-lookup"><span data-stu-id="20d0a-275">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="20d0a-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="20d0a-276">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="20d0a-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="20d0a-277">System-Only</span></span>            | <span data-ttu-id="20d0a-278">Richtig</span><span class="sxs-lookup"><span data-stu-id="20d0a-278">True</span></span>                                             |
| <span data-ttu-id="20d0a-279">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="20d0a-279">Is-Single-Valued</span></span>       | <span data-ttu-id="20d0a-280">False</span><span class="sxs-lookup"><span data-stu-id="20d0a-280">False</span></span>                                            |
| <span data-ttu-id="20d0a-281">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="20d0a-281">Is Indexed</span></span>             | <span data-ttu-id="20d0a-282">False</span><span class="sxs-lookup"><span data-stu-id="20d0a-282">False</span></span>                                            |
| <span data-ttu-id="20d0a-283">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="20d0a-283">In Global Catalog</span></span>      | <span data-ttu-id="20d0a-284">Richtig</span><span class="sxs-lookup"><span data-stu-id="20d0a-284">True</span></span>                                             |
| <span data-ttu-id="20d0a-285">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="20d0a-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="20d0a-286">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="20d0a-286">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="20d0a-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="20d0a-287">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="20d0a-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="20d0a-288">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="20d0a-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="20d0a-289">Search-Flags</span></span>           | <span data-ttu-id="20d0a-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="20d0a-290">0x00000000</span></span>                                       |
| <span data-ttu-id="20d0a-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="20d0a-291">System-Flags</span></span>           | <span data-ttu-id="20d0a-292">0x00000012</span><span class="sxs-lookup"><span data-stu-id="20d0a-292">0x00000012</span></span>                                       |
| <span data-ttu-id="20d0a-293">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="20d0a-293">Classes used in</span></span>        | [<span data-ttu-id="20d0a-294">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="20d0a-294">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





