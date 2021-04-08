---
title: Object-Class-Category-Attribut
description: Dieses Attribut enthält den Klassentyp, z. b. abstrakt, Zusatz oder strukturiert.
ms.assetid: 0698392d-991e-4a3c-b734-54d025a38d50
ms.tgt_platform: multiple
keywords:
- Objektklassen-Kategorieattribut AD-Schema
- objectClassCategory-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Object-Class-Category
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397bb50e0af0c9dcddcc535d0bcddb1c8d525cfc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957456"
---
# <a name="object-class-category-attribute"></a><span data-ttu-id="80539-105">Object-Class-Category-Attribut</span><span class="sxs-lookup"><span data-stu-id="80539-105">Object-Class-Category attribute</span></span>

<span data-ttu-id="80539-106">Dieses Attribut enthält den Klassentyp, z. b. abstrakt, Zusatz oder strukturiert.</span><span class="sxs-lookup"><span data-stu-id="80539-106">This attribute contains the class type, such as abstract, auxiliary, or structured.</span></span>



| <span data-ttu-id="80539-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="80539-107">Entry</span></span> | <span data-ttu-id="80539-108">Wert</span><span class="sxs-lookup"><span data-stu-id="80539-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="80539-109">CN</span><span class="sxs-lookup"><span data-stu-id="80539-109">CN</span></span>                | <span data-ttu-id="80539-110">Object-Class-Category</span><span class="sxs-lookup"><span data-stu-id="80539-110">Object-Class-Category</span></span>                                                           |
| <span data-ttu-id="80539-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="80539-111">Ldap-Display-Name</span></span> | <span data-ttu-id="80539-112">objectClassCategory</span><span class="sxs-lookup"><span data-stu-id="80539-112">objectClassCategory</span></span>                                                             |
| <span data-ttu-id="80539-113">Size</span><span class="sxs-lookup"><span data-stu-id="80539-113">Size</span></span>              | <span data-ttu-id="80539-114">4 Bytes.</span><span class="sxs-lookup"><span data-stu-id="80539-114">4 bytes.</span></span> <span data-ttu-id="80539-115">Strukturell 1, abstract 2, Zusatz 3.</span><span class="sxs-lookup"><span data-stu-id="80539-115">Structural 1, abstract 2, auxiliary 3.</span></span> <span data-ttu-id="80539-116">Die Klasse 88, 0 sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="80539-116">Class 88, 0 should not be used.</span></span> |
| <span data-ttu-id="80539-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="80539-117">Update Privilege</span></span>  | <span data-ttu-id="80539-118">Dieser Wert wird vom Designer des-Objekts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="80539-118">The designer of the object would set this value.</span></span>                                |
| <span data-ttu-id="80539-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="80539-119">Update Frequency</span></span>  | <span data-ttu-id="80539-120">Dieser Wert sollte sich nie ändern.</span><span class="sxs-lookup"><span data-stu-id="80539-120">This value should never change.</span></span>                                                 |
| <span data-ttu-id="80539-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="80539-121">Attribute-Id</span></span>      | <span data-ttu-id="80539-122">1.2.840.113556.1.2.370</span><span class="sxs-lookup"><span data-stu-id="80539-122">1.2.840.113556.1.2.370</span></span>                                                          |
| <span data-ttu-id="80539-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="80539-123">System-Id-Guid</span></span>    | <span data-ttu-id="80539-124">bf9679e6-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="80539-124">bf9679e6-0de6-11d0-a285-00aa003049e2</span></span>                                            |
| <span data-ttu-id="80539-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="80539-125">Syntax</span></span>            | [<span data-ttu-id="80539-126">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="80539-126">**Enumeration**</span></span>](s-enumeration.md)                                            |



## <a name="implementations"></a><span data-ttu-id="80539-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="80539-127">Implementations</span></span>

-   [<span data-ttu-id="80539-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="80539-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="80539-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="80539-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="80539-130">**Adam**</span><span class="sxs-lookup"><span data-stu-id="80539-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="80539-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="80539-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="80539-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="80539-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="80539-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="80539-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="80539-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="80539-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="80539-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="80539-135">Windows 2000 Server</span></span>



| <span data-ttu-id="80539-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="80539-136">Entry</span></span> | <span data-ttu-id="80539-137">Wert</span><span class="sxs-lookup"><span data-stu-id="80539-137">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="80539-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="80539-138">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="80539-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80539-139">MAPI-Id</span></span>                | <span data-ttu-id="80539-140">0x80f 6</span><span class="sxs-lookup"><span data-stu-id="80539-140">0x80F6</span></span>                                           |
| <span data-ttu-id="80539-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="80539-141">System-Only</span></span>            | <span data-ttu-id="80539-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="80539-142">True</span></span>                                             |
| <span data-ttu-id="80539-143">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="80539-143">Is-Single-Valued</span></span>       | <span data-ttu-id="80539-144">Richtig</span><span class="sxs-lookup"><span data-stu-id="80539-144">True</span></span>                                             |
| <span data-ttu-id="80539-145">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="80539-145">Is Indexed</span></span>             | <span data-ttu-id="80539-146">False</span><span class="sxs-lookup"><span data-stu-id="80539-146">False</span></span>                                            |
| <span data-ttu-id="80539-147">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="80539-147">In Global Catalog</span></span>      | <span data-ttu-id="80539-148">False</span><span class="sxs-lookup"><span data-stu-id="80539-148">False</span></span>                                            |
| <span data-ttu-id="80539-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="80539-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="80539-150">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="80539-150">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="80539-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80539-151">Range-Lower</span></span>            | <span data-ttu-id="80539-152">0</span><span class="sxs-lookup"><span data-stu-id="80539-152">0</span></span>                                                |
| <span data-ttu-id="80539-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80539-153">Range-Upper</span></span>            | <span data-ttu-id="80539-154">3</span><span class="sxs-lookup"><span data-stu-id="80539-154">3</span></span>                                                |
| <span data-ttu-id="80539-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80539-155">Search-Flags</span></span>           | <span data-ttu-id="80539-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80539-156">0x00000000</span></span>                                       |
| <span data-ttu-id="80539-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80539-157">System-Flags</span></span>           | <span data-ttu-id="80539-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80539-158">0x00000010</span></span>                                       |
| <span data-ttu-id="80539-159">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="80539-159">Classes used in</span></span>        | [<span data-ttu-id="80539-160">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="80539-160">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="80539-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="80539-161">Windows Server 2003</span></span>



| <span data-ttu-id="80539-162">Eingabe</span><span class="sxs-lookup"><span data-stu-id="80539-162">Entry</span></span> | <span data-ttu-id="80539-163">Wert</span><span class="sxs-lookup"><span data-stu-id="80539-163">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="80539-164">Link-ID</span><span class="sxs-lookup"><span data-stu-id="80539-164">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="80539-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80539-165">MAPI-Id</span></span>                | <span data-ttu-id="80539-166">0x80f 6</span><span class="sxs-lookup"><span data-stu-id="80539-166">0x80F6</span></span>                                           |
| <span data-ttu-id="80539-167">System-Only</span><span class="sxs-lookup"><span data-stu-id="80539-167">System-Only</span></span>            | <span data-ttu-id="80539-168">Richtig</span><span class="sxs-lookup"><span data-stu-id="80539-168">True</span></span>                                             |
| <span data-ttu-id="80539-169">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="80539-169">Is-Single-Valued</span></span>       | <span data-ttu-id="80539-170">Richtig</span><span class="sxs-lookup"><span data-stu-id="80539-170">True</span></span>                                             |
| <span data-ttu-id="80539-171">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="80539-171">Is Indexed</span></span>             | <span data-ttu-id="80539-172">False</span><span class="sxs-lookup"><span data-stu-id="80539-172">False</span></span>                                            |
| <span data-ttu-id="80539-173">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="80539-173">In Global Catalog</span></span>      | <span data-ttu-id="80539-174">False</span><span class="sxs-lookup"><span data-stu-id="80539-174">False</span></span>                                            |
| <span data-ttu-id="80539-175">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="80539-175">NT-Security-Descriptor</span></span> | <span data-ttu-id="80539-176">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="80539-176">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="80539-177">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80539-177">Range-Lower</span></span>            | <span data-ttu-id="80539-178">0</span><span class="sxs-lookup"><span data-stu-id="80539-178">0</span></span>                                                |
| <span data-ttu-id="80539-179">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80539-179">Range-Upper</span></span>            | <span data-ttu-id="80539-180">3</span><span class="sxs-lookup"><span data-stu-id="80539-180">3</span></span>                                                |
| <span data-ttu-id="80539-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80539-181">Search-Flags</span></span>           | <span data-ttu-id="80539-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80539-182">0x00000000</span></span>                                       |
| <span data-ttu-id="80539-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80539-183">System-Flags</span></span>           | <span data-ttu-id="80539-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80539-184">0x00000010</span></span>                                       |
| <span data-ttu-id="80539-185">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="80539-185">Classes used in</span></span>        | [<span data-ttu-id="80539-186">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="80539-186">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="80539-187">Adam</span><span class="sxs-lookup"><span data-stu-id="80539-187">ADAM</span></span>



| <span data-ttu-id="80539-188">Eingabe</span><span class="sxs-lookup"><span data-stu-id="80539-188">Entry</span></span> | <span data-ttu-id="80539-189">Wert</span><span class="sxs-lookup"><span data-stu-id="80539-189">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="80539-190">Link-ID</span><span class="sxs-lookup"><span data-stu-id="80539-190">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="80539-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80539-191">MAPI-Id</span></span>                | <span data-ttu-id="80539-192">0x80f 6</span><span class="sxs-lookup"><span data-stu-id="80539-192">0x80F6</span></span>                                           |
| <span data-ttu-id="80539-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="80539-193">System-Only</span></span>            | <span data-ttu-id="80539-194">Richtig</span><span class="sxs-lookup"><span data-stu-id="80539-194">True</span></span>                                             |
| <span data-ttu-id="80539-195">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="80539-195">Is-Single-Valued</span></span>       | <span data-ttu-id="80539-196">Richtig</span><span class="sxs-lookup"><span data-stu-id="80539-196">True</span></span>                                             |
| <span data-ttu-id="80539-197">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="80539-197">Is Indexed</span></span>             | <span data-ttu-id="80539-198">False</span><span class="sxs-lookup"><span data-stu-id="80539-198">False</span></span>                                            |
| <span data-ttu-id="80539-199">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="80539-199">In Global Catalog</span></span>      | <span data-ttu-id="80539-200">False</span><span class="sxs-lookup"><span data-stu-id="80539-200">False</span></span>                                            |
| <span data-ttu-id="80539-201">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="80539-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="80539-202">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="80539-202">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="80539-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80539-203">Range-Lower</span></span>            | <span data-ttu-id="80539-204">0</span><span class="sxs-lookup"><span data-stu-id="80539-204">0</span></span>                                                |
| <span data-ttu-id="80539-205">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80539-205">Range-Upper</span></span>            | <span data-ttu-id="80539-206">3</span><span class="sxs-lookup"><span data-stu-id="80539-206">3</span></span>                                                |
| <span data-ttu-id="80539-207">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80539-207">Search-Flags</span></span>           | <span data-ttu-id="80539-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80539-208">0x00000000</span></span>                                       |
| <span data-ttu-id="80539-209">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80539-209">System-Flags</span></span>           | <span data-ttu-id="80539-210">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80539-210">0x00000010</span></span>                                       |
| <span data-ttu-id="80539-211">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="80539-211">Classes used in</span></span>        | [<span data-ttu-id="80539-212">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="80539-212">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="80539-213">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="80539-213">Windows Server 2003 R2</span></span>



| <span data-ttu-id="80539-214">Eingabe</span><span class="sxs-lookup"><span data-stu-id="80539-214">Entry</span></span> | <span data-ttu-id="80539-215">Wert</span><span class="sxs-lookup"><span data-stu-id="80539-215">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="80539-216">Link-ID</span><span class="sxs-lookup"><span data-stu-id="80539-216">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="80539-217">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80539-217">MAPI-Id</span></span>                | <span data-ttu-id="80539-218">0x80f 6</span><span class="sxs-lookup"><span data-stu-id="80539-218">0x80F6</span></span>                                           |
| <span data-ttu-id="80539-219">System-Only</span><span class="sxs-lookup"><span data-stu-id="80539-219">System-Only</span></span>            | <span data-ttu-id="80539-220">Richtig</span><span class="sxs-lookup"><span data-stu-id="80539-220">True</span></span>                                             |
| <span data-ttu-id="80539-221">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="80539-221">Is-Single-Valued</span></span>       | <span data-ttu-id="80539-222">Richtig</span><span class="sxs-lookup"><span data-stu-id="80539-222">True</span></span>                                             |
| <span data-ttu-id="80539-223">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="80539-223">Is Indexed</span></span>             | <span data-ttu-id="80539-224">False</span><span class="sxs-lookup"><span data-stu-id="80539-224">False</span></span>                                            |
| <span data-ttu-id="80539-225">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="80539-225">In Global Catalog</span></span>      | <span data-ttu-id="80539-226">False</span><span class="sxs-lookup"><span data-stu-id="80539-226">False</span></span>                                            |
| <span data-ttu-id="80539-227">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="80539-227">NT-Security-Descriptor</span></span> | <span data-ttu-id="80539-228">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="80539-228">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="80539-229">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80539-229">Range-Lower</span></span>            | <span data-ttu-id="80539-230">0</span><span class="sxs-lookup"><span data-stu-id="80539-230">0</span></span>                                                |
| <span data-ttu-id="80539-231">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80539-231">Range-Upper</span></span>            | <span data-ttu-id="80539-232">3</span><span class="sxs-lookup"><span data-stu-id="80539-232">3</span></span>                                                |
| <span data-ttu-id="80539-233">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80539-233">Search-Flags</span></span>           | <span data-ttu-id="80539-234">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80539-234">0x00000000</span></span>                                       |
| <span data-ttu-id="80539-235">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80539-235">System-Flags</span></span>           | <span data-ttu-id="80539-236">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80539-236">0x00000010</span></span>                                       |
| <span data-ttu-id="80539-237">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="80539-237">Classes used in</span></span>        | [<span data-ttu-id="80539-238">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="80539-238">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="80539-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80539-239">Windows Server 2008</span></span>



| <span data-ttu-id="80539-240">Eingabe</span><span class="sxs-lookup"><span data-stu-id="80539-240">Entry</span></span> | <span data-ttu-id="80539-241">Wert</span><span class="sxs-lookup"><span data-stu-id="80539-241">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="80539-242">Link-ID</span><span class="sxs-lookup"><span data-stu-id="80539-242">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="80539-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80539-243">MAPI-Id</span></span>                | <span data-ttu-id="80539-244">0x80f 6</span><span class="sxs-lookup"><span data-stu-id="80539-244">0x80F6</span></span>                                           |
| <span data-ttu-id="80539-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="80539-245">System-Only</span></span>            | <span data-ttu-id="80539-246">Richtig</span><span class="sxs-lookup"><span data-stu-id="80539-246">True</span></span>                                             |
| <span data-ttu-id="80539-247">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="80539-247">Is-Single-Valued</span></span>       | <span data-ttu-id="80539-248">Richtig</span><span class="sxs-lookup"><span data-stu-id="80539-248">True</span></span>                                             |
| <span data-ttu-id="80539-249">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="80539-249">Is Indexed</span></span>             | <span data-ttu-id="80539-250">False</span><span class="sxs-lookup"><span data-stu-id="80539-250">False</span></span>                                            |
| <span data-ttu-id="80539-251">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="80539-251">In Global Catalog</span></span>      | <span data-ttu-id="80539-252">False</span><span class="sxs-lookup"><span data-stu-id="80539-252">False</span></span>                                            |
| <span data-ttu-id="80539-253">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="80539-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="80539-254">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="80539-254">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="80539-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80539-255">Range-Lower</span></span>            | <span data-ttu-id="80539-256">0</span><span class="sxs-lookup"><span data-stu-id="80539-256">0</span></span>                                                |
| <span data-ttu-id="80539-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80539-257">Range-Upper</span></span>            | <span data-ttu-id="80539-258">3</span><span class="sxs-lookup"><span data-stu-id="80539-258">3</span></span>                                                |
| <span data-ttu-id="80539-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80539-259">Search-Flags</span></span>           | <span data-ttu-id="80539-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80539-260">0x00000000</span></span>                                       |
| <span data-ttu-id="80539-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80539-261">System-Flags</span></span>           | <span data-ttu-id="80539-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80539-262">0x00000010</span></span>                                       |
| <span data-ttu-id="80539-263">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="80539-263">Classes used in</span></span>        | [<span data-ttu-id="80539-264">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="80539-264">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="80539-265">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="80539-265">Windows Server 2008 R2</span></span>



| <span data-ttu-id="80539-266">Eingabe</span><span class="sxs-lookup"><span data-stu-id="80539-266">Entry</span></span> | <span data-ttu-id="80539-267">Wert</span><span class="sxs-lookup"><span data-stu-id="80539-267">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="80539-268">Link-ID</span><span class="sxs-lookup"><span data-stu-id="80539-268">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="80539-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80539-269">MAPI-Id</span></span>                | <span data-ttu-id="80539-270">0x80f 6</span><span class="sxs-lookup"><span data-stu-id="80539-270">0x80F6</span></span>                                           |
| <span data-ttu-id="80539-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="80539-271">System-Only</span></span>            | <span data-ttu-id="80539-272">Richtig</span><span class="sxs-lookup"><span data-stu-id="80539-272">True</span></span>                                             |
| <span data-ttu-id="80539-273">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="80539-273">Is-Single-Valued</span></span>       | <span data-ttu-id="80539-274">Richtig</span><span class="sxs-lookup"><span data-stu-id="80539-274">True</span></span>                                             |
| <span data-ttu-id="80539-275">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="80539-275">Is Indexed</span></span>             | <span data-ttu-id="80539-276">False</span><span class="sxs-lookup"><span data-stu-id="80539-276">False</span></span>                                            |
| <span data-ttu-id="80539-277">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="80539-277">In Global Catalog</span></span>      | <span data-ttu-id="80539-278">False</span><span class="sxs-lookup"><span data-stu-id="80539-278">False</span></span>                                            |
| <span data-ttu-id="80539-279">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="80539-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="80539-280">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="80539-280">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="80539-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80539-281">Range-Lower</span></span>            | <span data-ttu-id="80539-282">0</span><span class="sxs-lookup"><span data-stu-id="80539-282">0</span></span>                                                |
| <span data-ttu-id="80539-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80539-283">Range-Upper</span></span>            | <span data-ttu-id="80539-284">3</span><span class="sxs-lookup"><span data-stu-id="80539-284">3</span></span>                                                |
| <span data-ttu-id="80539-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80539-285">Search-Flags</span></span>           | <span data-ttu-id="80539-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80539-286">0x00000000</span></span>                                       |
| <span data-ttu-id="80539-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80539-287">System-Flags</span></span>           | <span data-ttu-id="80539-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80539-288">0x00000010</span></span>                                       |
| <span data-ttu-id="80539-289">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="80539-289">Classes used in</span></span>        | [<span data-ttu-id="80539-290">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="80539-290">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="80539-291">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="80539-291">Windows Server 2012</span></span>



| <span data-ttu-id="80539-292">Eingabe</span><span class="sxs-lookup"><span data-stu-id="80539-292">Entry</span></span> | <span data-ttu-id="80539-293">Wert</span><span class="sxs-lookup"><span data-stu-id="80539-293">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="80539-294">Link-ID</span><span class="sxs-lookup"><span data-stu-id="80539-294">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="80539-295">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80539-295">MAPI-Id</span></span>                | <span data-ttu-id="80539-296">0x80f 6</span><span class="sxs-lookup"><span data-stu-id="80539-296">0x80F6</span></span>                                           |
| <span data-ttu-id="80539-297">System-Only</span><span class="sxs-lookup"><span data-stu-id="80539-297">System-Only</span></span>            | <span data-ttu-id="80539-298">Richtig</span><span class="sxs-lookup"><span data-stu-id="80539-298">True</span></span>                                             |
| <span data-ttu-id="80539-299">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="80539-299">Is-Single-Valued</span></span>       | <span data-ttu-id="80539-300">Richtig</span><span class="sxs-lookup"><span data-stu-id="80539-300">True</span></span>                                             |
| <span data-ttu-id="80539-301">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="80539-301">Is Indexed</span></span>             | <span data-ttu-id="80539-302">False</span><span class="sxs-lookup"><span data-stu-id="80539-302">False</span></span>                                            |
| <span data-ttu-id="80539-303">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="80539-303">In Global Catalog</span></span>      | <span data-ttu-id="80539-304">False</span><span class="sxs-lookup"><span data-stu-id="80539-304">False</span></span>                                            |
| <span data-ttu-id="80539-305">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="80539-305">NT-Security-Descriptor</span></span> | <span data-ttu-id="80539-306">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="80539-306">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="80539-307">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80539-307">Range-Lower</span></span>            | <span data-ttu-id="80539-308">0</span><span class="sxs-lookup"><span data-stu-id="80539-308">0</span></span>                                                |
| <span data-ttu-id="80539-309">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80539-309">Range-Upper</span></span>            | <span data-ttu-id="80539-310">3</span><span class="sxs-lookup"><span data-stu-id="80539-310">3</span></span>                                                |
| <span data-ttu-id="80539-311">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80539-311">Search-Flags</span></span>           | <span data-ttu-id="80539-312">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80539-312">0x00000000</span></span>                                       |
| <span data-ttu-id="80539-313">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80539-313">System-Flags</span></span>           | <span data-ttu-id="80539-314">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80539-314">0x00000010</span></span>                                       |
| <span data-ttu-id="80539-315">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="80539-315">Classes used in</span></span>        | [<span data-ttu-id="80539-316">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="80539-316">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





