---
title: System-hilfclass-Attribut
description: Eine Liste von Hilfsklassen, die nicht vom Benutzer geändert werden können.
ms.assetid: 6d629925-7321-4f3a-bf4c-4adf0d33c946
ms.tgt_platform: multiple
keywords:
- AD-Schema für System-hilfklassenattribut
- AD-Schema des systemAuxiliaryClass-Attributs
topic_type:
- apiref
api_name:
- System-Auxiliary-Class
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebe70899ba2bda8fe98b38228cb661e7a773ec1d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106342902"
---
# <a name="system-auxiliary-class-attribute"></a><span data-ttu-id="5d479-105">System-hilfclass-Attribut</span><span class="sxs-lookup"><span data-stu-id="5d479-105">System-Auxiliary-Class attribute</span></span>

<span data-ttu-id="5d479-106">Eine Liste von Hilfsklassen, die nicht vom Benutzer geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="5d479-106">A list of auxiliary classes that cannot be modified by the user.</span></span>



| <span data-ttu-id="5d479-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5d479-107">Entry</span></span> | <span data-ttu-id="5d479-108">Wert</span><span class="sxs-lookup"><span data-stu-id="5d479-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="5d479-109">CN</span><span class="sxs-lookup"><span data-stu-id="5d479-109">CN</span></span>                | <span data-ttu-id="5d479-110">System-Zusatz-Class</span><span class="sxs-lookup"><span data-stu-id="5d479-110">System-Auxiliary-Class</span></span>                                             |
| <span data-ttu-id="5d479-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5d479-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5d479-112">systemAuxiliaryClass</span><span class="sxs-lookup"><span data-stu-id="5d479-112">systemAuxiliaryClass</span></span>                                               |
| <span data-ttu-id="5d479-113">Size</span><span class="sxs-lookup"><span data-stu-id="5d479-113">Size</span></span>              | \-                                                                 |
| <span data-ttu-id="5d479-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="5d479-114">Update Privilege</span></span>  | <span data-ttu-id="5d479-115">Schema Administrator</span><span class="sxs-lookup"><span data-stu-id="5d479-115">Schema administrator</span></span>                                               |
| <span data-ttu-id="5d479-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="5d479-116">Update Frequency</span></span>  | <span data-ttu-id="5d479-117">Wenn die Klasse erstellt oder eine neue Erweiterungs Klasse hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="5d479-117">When the class is created or a new auxiliary class is added to it.</span></span> |
| <span data-ttu-id="5d479-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5d479-118">Attribute-Id</span></span>      | <span data-ttu-id="5d479-119">1.2.840.113556.1.4.198</span><span class="sxs-lookup"><span data-stu-id="5d479-119">1.2.840.113556.1.4.198</span></span>                                             |
| <span data-ttu-id="5d479-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5d479-120">System-Id-Guid</span></span>    | <span data-ttu-id="5d479-121">bf967a43-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="5d479-121">bf967a43-0de6-11d0-a285-00aa003049e2</span></span>                               |
| <span data-ttu-id="5d479-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d479-122">Syntax</span></span>            | [<span data-ttu-id="5d479-123">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="5d479-123">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md)    |



## <a name="implementations"></a><span data-ttu-id="5d479-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="5d479-124">Implementations</span></span>

-   [<span data-ttu-id="5d479-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5d479-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5d479-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5d479-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5d479-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="5d479-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="5d479-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5d479-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5d479-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5d479-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5d479-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5d479-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5d479-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5d479-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5d479-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5d479-132">Windows 2000 Server</span></span>



| <span data-ttu-id="5d479-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5d479-133">Entry</span></span> | <span data-ttu-id="5d479-134">Wert</span><span class="sxs-lookup"><span data-stu-id="5d479-134">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5d479-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5d479-135">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5d479-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d479-136">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5d479-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d479-137">System-Only</span></span>            | <span data-ttu-id="5d479-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="5d479-138">True</span></span>                                             |
| <span data-ttu-id="5d479-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5d479-139">Is-Single-Valued</span></span>       | <span data-ttu-id="5d479-140">False</span><span class="sxs-lookup"><span data-stu-id="5d479-140">False</span></span>                                            |
| <span data-ttu-id="5d479-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5d479-141">Is Indexed</span></span>             | <span data-ttu-id="5d479-142">False</span><span class="sxs-lookup"><span data-stu-id="5d479-142">False</span></span>                                            |
| <span data-ttu-id="5d479-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5d479-143">In Global Catalog</span></span>      | <span data-ttu-id="5d479-144">False</span><span class="sxs-lookup"><span data-stu-id="5d479-144">False</span></span>                                            |
| <span data-ttu-id="5d479-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5d479-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d479-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5d479-146">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5d479-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d479-147">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5d479-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d479-148">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5d479-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d479-149">Search-Flags</span></span>           | <span data-ttu-id="5d479-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d479-150">0x00000000</span></span>                                       |
| <span data-ttu-id="5d479-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d479-151">System-Flags</span></span>           | <span data-ttu-id="5d479-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d479-152">0x00000010</span></span>                                       |
| <span data-ttu-id="5d479-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5d479-153">Classes used in</span></span>        | [<span data-ttu-id="5d479-154">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="5d479-154">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5d479-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5d479-155">Windows Server 2003</span></span>



| <span data-ttu-id="5d479-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5d479-156">Entry</span></span> | <span data-ttu-id="5d479-157">Wert</span><span class="sxs-lookup"><span data-stu-id="5d479-157">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5d479-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5d479-158">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5d479-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d479-159">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5d479-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d479-160">System-Only</span></span>            | <span data-ttu-id="5d479-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="5d479-161">True</span></span>                                             |
| <span data-ttu-id="5d479-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5d479-162">Is-Single-Valued</span></span>       | <span data-ttu-id="5d479-163">False</span><span class="sxs-lookup"><span data-stu-id="5d479-163">False</span></span>                                            |
| <span data-ttu-id="5d479-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5d479-164">Is Indexed</span></span>             | <span data-ttu-id="5d479-165">False</span><span class="sxs-lookup"><span data-stu-id="5d479-165">False</span></span>                                            |
| <span data-ttu-id="5d479-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5d479-166">In Global Catalog</span></span>      | <span data-ttu-id="5d479-167">False</span><span class="sxs-lookup"><span data-stu-id="5d479-167">False</span></span>                                            |
| <span data-ttu-id="5d479-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5d479-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d479-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5d479-169">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5d479-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d479-170">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5d479-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d479-171">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5d479-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d479-172">Search-Flags</span></span>           | <span data-ttu-id="5d479-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d479-173">0x00000000</span></span>                                       |
| <span data-ttu-id="5d479-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d479-174">System-Flags</span></span>           | <span data-ttu-id="5d479-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d479-175">0x00000010</span></span>                                       |
| <span data-ttu-id="5d479-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5d479-176">Classes used in</span></span>        | [<span data-ttu-id="5d479-177">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="5d479-177">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="5d479-178">Adam</span><span class="sxs-lookup"><span data-stu-id="5d479-178">ADAM</span></span>



| <span data-ttu-id="5d479-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5d479-179">Entry</span></span> | <span data-ttu-id="5d479-180">Wert</span><span class="sxs-lookup"><span data-stu-id="5d479-180">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5d479-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5d479-181">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5d479-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d479-182">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5d479-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d479-183">System-Only</span></span>            | <span data-ttu-id="5d479-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="5d479-184">True</span></span>                                             |
| <span data-ttu-id="5d479-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5d479-185">Is-Single-Valued</span></span>       | <span data-ttu-id="5d479-186">False</span><span class="sxs-lookup"><span data-stu-id="5d479-186">False</span></span>                                            |
| <span data-ttu-id="5d479-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5d479-187">Is Indexed</span></span>             | <span data-ttu-id="5d479-188">False</span><span class="sxs-lookup"><span data-stu-id="5d479-188">False</span></span>                                            |
| <span data-ttu-id="5d479-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5d479-189">In Global Catalog</span></span>      | <span data-ttu-id="5d479-190">False</span><span class="sxs-lookup"><span data-stu-id="5d479-190">False</span></span>                                            |
| <span data-ttu-id="5d479-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5d479-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d479-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5d479-192">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5d479-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d479-193">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5d479-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d479-194">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5d479-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d479-195">Search-Flags</span></span>           | <span data-ttu-id="5d479-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d479-196">0x00000000</span></span>                                       |
| <span data-ttu-id="5d479-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d479-197">System-Flags</span></span>           | <span data-ttu-id="5d479-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d479-198">0x00000010</span></span>                                       |
| <span data-ttu-id="5d479-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5d479-199">Classes used in</span></span>        | [<span data-ttu-id="5d479-200">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="5d479-200">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5d479-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5d479-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5d479-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5d479-202">Entry</span></span> | <span data-ttu-id="5d479-203">Wert</span><span class="sxs-lookup"><span data-stu-id="5d479-203">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5d479-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5d479-204">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5d479-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d479-205">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5d479-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d479-206">System-Only</span></span>            | <span data-ttu-id="5d479-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="5d479-207">True</span></span>                                             |
| <span data-ttu-id="5d479-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5d479-208">Is-Single-Valued</span></span>       | <span data-ttu-id="5d479-209">False</span><span class="sxs-lookup"><span data-stu-id="5d479-209">False</span></span>                                            |
| <span data-ttu-id="5d479-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5d479-210">Is Indexed</span></span>             | <span data-ttu-id="5d479-211">False</span><span class="sxs-lookup"><span data-stu-id="5d479-211">False</span></span>                                            |
| <span data-ttu-id="5d479-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5d479-212">In Global Catalog</span></span>      | <span data-ttu-id="5d479-213">False</span><span class="sxs-lookup"><span data-stu-id="5d479-213">False</span></span>                                            |
| <span data-ttu-id="5d479-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5d479-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d479-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5d479-215">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5d479-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d479-216">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5d479-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d479-217">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5d479-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d479-218">Search-Flags</span></span>           | <span data-ttu-id="5d479-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d479-219">0x00000000</span></span>                                       |
| <span data-ttu-id="5d479-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d479-220">System-Flags</span></span>           | <span data-ttu-id="5d479-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d479-221">0x00000010</span></span>                                       |
| <span data-ttu-id="5d479-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5d479-222">Classes used in</span></span>        | [<span data-ttu-id="5d479-223">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="5d479-223">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5d479-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d479-224">Windows Server 2008</span></span>



| <span data-ttu-id="5d479-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5d479-225">Entry</span></span> | <span data-ttu-id="5d479-226">Wert</span><span class="sxs-lookup"><span data-stu-id="5d479-226">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5d479-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5d479-227">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5d479-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d479-228">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5d479-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d479-229">System-Only</span></span>            | <span data-ttu-id="5d479-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="5d479-230">True</span></span>                                             |
| <span data-ttu-id="5d479-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5d479-231">Is-Single-Valued</span></span>       | <span data-ttu-id="5d479-232">False</span><span class="sxs-lookup"><span data-stu-id="5d479-232">False</span></span>                                            |
| <span data-ttu-id="5d479-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5d479-233">Is Indexed</span></span>             | <span data-ttu-id="5d479-234">False</span><span class="sxs-lookup"><span data-stu-id="5d479-234">False</span></span>                                            |
| <span data-ttu-id="5d479-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5d479-235">In Global Catalog</span></span>      | <span data-ttu-id="5d479-236">False</span><span class="sxs-lookup"><span data-stu-id="5d479-236">False</span></span>                                            |
| <span data-ttu-id="5d479-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5d479-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d479-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5d479-238">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5d479-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d479-239">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5d479-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d479-240">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5d479-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d479-241">Search-Flags</span></span>           | <span data-ttu-id="5d479-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d479-242">0x00000000</span></span>                                       |
| <span data-ttu-id="5d479-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d479-243">System-Flags</span></span>           | <span data-ttu-id="5d479-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d479-244">0x00000010</span></span>                                       |
| <span data-ttu-id="5d479-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5d479-245">Classes used in</span></span>        | [<span data-ttu-id="5d479-246">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="5d479-246">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5d479-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5d479-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5d479-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5d479-248">Entry</span></span> | <span data-ttu-id="5d479-249">Wert</span><span class="sxs-lookup"><span data-stu-id="5d479-249">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5d479-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5d479-250">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5d479-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d479-251">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5d479-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d479-252">System-Only</span></span>            | <span data-ttu-id="5d479-253">Richtig</span><span class="sxs-lookup"><span data-stu-id="5d479-253">True</span></span>                                             |
| <span data-ttu-id="5d479-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5d479-254">Is-Single-Valued</span></span>       | <span data-ttu-id="5d479-255">False</span><span class="sxs-lookup"><span data-stu-id="5d479-255">False</span></span>                                            |
| <span data-ttu-id="5d479-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5d479-256">Is Indexed</span></span>             | <span data-ttu-id="5d479-257">False</span><span class="sxs-lookup"><span data-stu-id="5d479-257">False</span></span>                                            |
| <span data-ttu-id="5d479-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5d479-258">In Global Catalog</span></span>      | <span data-ttu-id="5d479-259">False</span><span class="sxs-lookup"><span data-stu-id="5d479-259">False</span></span>                                            |
| <span data-ttu-id="5d479-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5d479-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d479-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5d479-261">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5d479-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d479-262">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5d479-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d479-263">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5d479-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d479-264">Search-Flags</span></span>           | <span data-ttu-id="5d479-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d479-265">0x00000000</span></span>                                       |
| <span data-ttu-id="5d479-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d479-266">System-Flags</span></span>           | <span data-ttu-id="5d479-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d479-267">0x00000010</span></span>                                       |
| <span data-ttu-id="5d479-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5d479-268">Classes used in</span></span>        | [<span data-ttu-id="5d479-269">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="5d479-269">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5d479-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5d479-270">Windows Server 2012</span></span>



| <span data-ttu-id="5d479-271">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5d479-271">Entry</span></span> | <span data-ttu-id="5d479-272">Wert</span><span class="sxs-lookup"><span data-stu-id="5d479-272">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5d479-273">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5d479-273">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5d479-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d479-274">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5d479-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d479-275">System-Only</span></span>            | <span data-ttu-id="5d479-276">Richtig</span><span class="sxs-lookup"><span data-stu-id="5d479-276">True</span></span>                                             |
| <span data-ttu-id="5d479-277">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5d479-277">Is-Single-Valued</span></span>       | <span data-ttu-id="5d479-278">False</span><span class="sxs-lookup"><span data-stu-id="5d479-278">False</span></span>                                            |
| <span data-ttu-id="5d479-279">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5d479-279">Is Indexed</span></span>             | <span data-ttu-id="5d479-280">False</span><span class="sxs-lookup"><span data-stu-id="5d479-280">False</span></span>                                            |
| <span data-ttu-id="5d479-281">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5d479-281">In Global Catalog</span></span>      | <span data-ttu-id="5d479-282">False</span><span class="sxs-lookup"><span data-stu-id="5d479-282">False</span></span>                                            |
| <span data-ttu-id="5d479-283">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5d479-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d479-284">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5d479-284">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5d479-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d479-285">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5d479-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d479-286">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5d479-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d479-287">Search-Flags</span></span>           | <span data-ttu-id="5d479-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d479-288">0x00000000</span></span>                                       |
| <span data-ttu-id="5d479-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d479-289">System-Flags</span></span>           | <span data-ttu-id="5d479-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d479-290">0x00000010</span></span>                                       |
| <span data-ttu-id="5d479-291">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5d479-291">Classes used in</span></span>        | [<span data-ttu-id="5d479-292">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="5d479-292">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





