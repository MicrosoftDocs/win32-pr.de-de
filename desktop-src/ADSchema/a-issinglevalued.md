---
title: Ist-einwertiges Attribut
description: TRUE gibt an, dass mit diesem Attribut nur ein Wert gespeichert werden kann.
ms.assetid: 53dd8dfe-2123-4a61-a346-12abe340ea11
ms.tgt_platform: multiple
keywords:
- Is-Single-Wert-Attribut, AD-Schema
- issinglewertattribut AD-Schema
topic_type:
- apiref
api_name:
- Is-Single-Valued
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a1fafd047afa47b874fb0385a690e2c0d13161
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859478"
---
# <a name="is-single-valued-attribute"></a><span data-ttu-id="acd04-105">Ist-einwertiges Attribut</span><span class="sxs-lookup"><span data-stu-id="acd04-105">Is-Single-Valued attribute</span></span>

<span data-ttu-id="acd04-106">**True** gibt an, dass mit diesem Attribut nur ein Wert gespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="acd04-106">If **TRUE**, this attribute can only store one value.</span></span>



| <span data-ttu-id="acd04-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="acd04-107">Entry</span></span> | <span data-ttu-id="acd04-108">Wert</span><span class="sxs-lookup"><span data-stu-id="acd04-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="acd04-109">CN</span><span class="sxs-lookup"><span data-stu-id="acd04-109">CN</span></span>                | <span data-ttu-id="acd04-110">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="acd04-110">Is-Single-Valued</span></span>                     |
| <span data-ttu-id="acd04-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="acd04-111">Ldap-Display-Name</span></span> | <span data-ttu-id="acd04-112">isSingleValued</span><span class="sxs-lookup"><span data-stu-id="acd04-112">isSingleValued</span></span>                       |
| <span data-ttu-id="acd04-113">Size</span><span class="sxs-lookup"><span data-stu-id="acd04-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="acd04-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="acd04-114">Update Privilege</span></span>  | <span data-ttu-id="acd04-115">Schema Administrator</span><span class="sxs-lookup"><span data-stu-id="acd04-115">Schema administrator</span></span>                 |
| <span data-ttu-id="acd04-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="acd04-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="acd04-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="acd04-117">Attribute-Id</span></span>      | <span data-ttu-id="acd04-118">1.2.840.113556.1.2.33</span><span class="sxs-lookup"><span data-stu-id="acd04-118">1.2.840.113556.1.2.33</span></span>                |
| <span data-ttu-id="acd04-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="acd04-119">System-Id-Guid</span></span>    | <span data-ttu-id="acd04-120">bf967992-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="acd04-120">bf967992-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="acd04-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="acd04-121">Syntax</span></span>            | [<span data-ttu-id="acd04-122">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="acd04-122">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="acd04-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="acd04-123">Implementations</span></span>

-   [<span data-ttu-id="acd04-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="acd04-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="acd04-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="acd04-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="acd04-126">**Adam**</span><span class="sxs-lookup"><span data-stu-id="acd04-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="acd04-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="acd04-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="acd04-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="acd04-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="acd04-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="acd04-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="acd04-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="acd04-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="acd04-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="acd04-131">Windows 2000 Server</span></span>



| <span data-ttu-id="acd04-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="acd04-132">Entry</span></span> | <span data-ttu-id="acd04-133">Wert</span><span class="sxs-lookup"><span data-stu-id="acd04-133">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="acd04-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="acd04-134">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="acd04-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acd04-135">MAPI-Id</span></span>                | <span data-ttu-id="acd04-136">0x80c1</span><span class="sxs-lookup"><span data-stu-id="acd04-136">0x80C1</span></span>                                                   |
| <span data-ttu-id="acd04-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="acd04-137">System-Only</span></span>            | <span data-ttu-id="acd04-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="acd04-138">True</span></span>                                                     |
| <span data-ttu-id="acd04-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="acd04-139">Is-Single-Valued</span></span>       | <span data-ttu-id="acd04-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="acd04-140">True</span></span>                                                     |
| <span data-ttu-id="acd04-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="acd04-141">Is Indexed</span></span>             | <span data-ttu-id="acd04-142">False</span><span class="sxs-lookup"><span data-stu-id="acd04-142">False</span></span>                                                    |
| <span data-ttu-id="acd04-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="acd04-143">In Global Catalog</span></span>      | <span data-ttu-id="acd04-144">False</span><span class="sxs-lookup"><span data-stu-id="acd04-144">False</span></span>                                                    |
| <span data-ttu-id="acd04-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="acd04-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="acd04-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="acd04-146">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="acd04-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acd04-147">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="acd04-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acd04-148">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="acd04-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acd04-149">Search-Flags</span></span>           | <span data-ttu-id="acd04-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acd04-150">0x00000000</span></span>                                               |
| <span data-ttu-id="acd04-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acd04-151">System-Flags</span></span>           | <span data-ttu-id="acd04-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acd04-152">0x00000010</span></span>                                               |
| <span data-ttu-id="acd04-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="acd04-153">Classes used in</span></span>        | [<span data-ttu-id="acd04-154">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="acd04-154">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="acd04-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="acd04-155">Windows Server 2003</span></span>



| <span data-ttu-id="acd04-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="acd04-156">Entry</span></span> | <span data-ttu-id="acd04-157">Wert</span><span class="sxs-lookup"><span data-stu-id="acd04-157">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="acd04-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="acd04-158">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="acd04-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acd04-159">MAPI-Id</span></span>                | <span data-ttu-id="acd04-160">0x80c1</span><span class="sxs-lookup"><span data-stu-id="acd04-160">0x80C1</span></span>                                                   |
| <span data-ttu-id="acd04-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="acd04-161">System-Only</span></span>            | <span data-ttu-id="acd04-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="acd04-162">True</span></span>                                                     |
| <span data-ttu-id="acd04-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="acd04-163">Is-Single-Valued</span></span>       | <span data-ttu-id="acd04-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="acd04-164">True</span></span>                                                     |
| <span data-ttu-id="acd04-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="acd04-165">Is Indexed</span></span>             | <span data-ttu-id="acd04-166">False</span><span class="sxs-lookup"><span data-stu-id="acd04-166">False</span></span>                                                    |
| <span data-ttu-id="acd04-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="acd04-167">In Global Catalog</span></span>      | <span data-ttu-id="acd04-168">False</span><span class="sxs-lookup"><span data-stu-id="acd04-168">False</span></span>                                                    |
| <span data-ttu-id="acd04-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="acd04-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="acd04-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="acd04-170">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="acd04-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acd04-171">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="acd04-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acd04-172">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="acd04-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acd04-173">Search-Flags</span></span>           | <span data-ttu-id="acd04-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acd04-174">0x00000000</span></span>                                               |
| <span data-ttu-id="acd04-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acd04-175">System-Flags</span></span>           | <span data-ttu-id="acd04-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acd04-176">0x00000010</span></span>                                               |
| <span data-ttu-id="acd04-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="acd04-177">Classes used in</span></span>        | [<span data-ttu-id="acd04-178">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="acd04-178">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="acd04-179">Adam</span><span class="sxs-lookup"><span data-stu-id="acd04-179">ADAM</span></span>



| <span data-ttu-id="acd04-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="acd04-180">Entry</span></span> | <span data-ttu-id="acd04-181">Wert</span><span class="sxs-lookup"><span data-stu-id="acd04-181">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="acd04-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="acd04-182">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="acd04-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acd04-183">MAPI-Id</span></span>                | <span data-ttu-id="acd04-184">0x80c1</span><span class="sxs-lookup"><span data-stu-id="acd04-184">0x80C1</span></span>                                                   |
| <span data-ttu-id="acd04-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="acd04-185">System-Only</span></span>            | <span data-ttu-id="acd04-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="acd04-186">True</span></span>                                                     |
| <span data-ttu-id="acd04-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="acd04-187">Is-Single-Valued</span></span>       | <span data-ttu-id="acd04-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="acd04-188">True</span></span>                                                     |
| <span data-ttu-id="acd04-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="acd04-189">Is Indexed</span></span>             | <span data-ttu-id="acd04-190">False</span><span class="sxs-lookup"><span data-stu-id="acd04-190">False</span></span>                                                    |
| <span data-ttu-id="acd04-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="acd04-191">In Global Catalog</span></span>      | <span data-ttu-id="acd04-192">False</span><span class="sxs-lookup"><span data-stu-id="acd04-192">False</span></span>                                                    |
| <span data-ttu-id="acd04-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="acd04-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="acd04-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="acd04-194">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="acd04-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acd04-195">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="acd04-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acd04-196">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="acd04-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acd04-197">Search-Flags</span></span>           | <span data-ttu-id="acd04-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acd04-198">0x00000000</span></span>                                               |
| <span data-ttu-id="acd04-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acd04-199">System-Flags</span></span>           | <span data-ttu-id="acd04-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acd04-200">0x00000010</span></span>                                               |
| <span data-ttu-id="acd04-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="acd04-201">Classes used in</span></span>        | [<span data-ttu-id="acd04-202">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="acd04-202">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="acd04-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="acd04-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="acd04-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="acd04-204">Entry</span></span> | <span data-ttu-id="acd04-205">Wert</span><span class="sxs-lookup"><span data-stu-id="acd04-205">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="acd04-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="acd04-206">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="acd04-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acd04-207">MAPI-Id</span></span>                | <span data-ttu-id="acd04-208">0x80c1</span><span class="sxs-lookup"><span data-stu-id="acd04-208">0x80C1</span></span>                                                   |
| <span data-ttu-id="acd04-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="acd04-209">System-Only</span></span>            | <span data-ttu-id="acd04-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="acd04-210">True</span></span>                                                     |
| <span data-ttu-id="acd04-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="acd04-211">Is-Single-Valued</span></span>       | <span data-ttu-id="acd04-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="acd04-212">True</span></span>                                                     |
| <span data-ttu-id="acd04-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="acd04-213">Is Indexed</span></span>             | <span data-ttu-id="acd04-214">False</span><span class="sxs-lookup"><span data-stu-id="acd04-214">False</span></span>                                                    |
| <span data-ttu-id="acd04-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="acd04-215">In Global Catalog</span></span>      | <span data-ttu-id="acd04-216">False</span><span class="sxs-lookup"><span data-stu-id="acd04-216">False</span></span>                                                    |
| <span data-ttu-id="acd04-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="acd04-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="acd04-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="acd04-218">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="acd04-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acd04-219">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="acd04-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acd04-220">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="acd04-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acd04-221">Search-Flags</span></span>           | <span data-ttu-id="acd04-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acd04-222">0x00000000</span></span>                                               |
| <span data-ttu-id="acd04-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acd04-223">System-Flags</span></span>           | <span data-ttu-id="acd04-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acd04-224">0x00000010</span></span>                                               |
| <span data-ttu-id="acd04-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="acd04-225">Classes used in</span></span>        | [<span data-ttu-id="acd04-226">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="acd04-226">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="acd04-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="acd04-227">Windows Server 2008</span></span>



| <span data-ttu-id="acd04-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="acd04-228">Entry</span></span> | <span data-ttu-id="acd04-229">Wert</span><span class="sxs-lookup"><span data-stu-id="acd04-229">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="acd04-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="acd04-230">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="acd04-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acd04-231">MAPI-Id</span></span>                | <span data-ttu-id="acd04-232">0x80c1</span><span class="sxs-lookup"><span data-stu-id="acd04-232">0x80C1</span></span>                                                   |
| <span data-ttu-id="acd04-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="acd04-233">System-Only</span></span>            | <span data-ttu-id="acd04-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="acd04-234">True</span></span>                                                     |
| <span data-ttu-id="acd04-235">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="acd04-235">Is-Single-Valued</span></span>       | <span data-ttu-id="acd04-236">Richtig</span><span class="sxs-lookup"><span data-stu-id="acd04-236">True</span></span>                                                     |
| <span data-ttu-id="acd04-237">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="acd04-237">Is Indexed</span></span>             | <span data-ttu-id="acd04-238">False</span><span class="sxs-lookup"><span data-stu-id="acd04-238">False</span></span>                                                    |
| <span data-ttu-id="acd04-239">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="acd04-239">In Global Catalog</span></span>      | <span data-ttu-id="acd04-240">False</span><span class="sxs-lookup"><span data-stu-id="acd04-240">False</span></span>                                                    |
| <span data-ttu-id="acd04-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="acd04-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="acd04-242">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="acd04-242">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="acd04-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acd04-243">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="acd04-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acd04-244">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="acd04-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acd04-245">Search-Flags</span></span>           | <span data-ttu-id="acd04-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acd04-246">0x00000000</span></span>                                               |
| <span data-ttu-id="acd04-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acd04-247">System-Flags</span></span>           | <span data-ttu-id="acd04-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acd04-248">0x00000010</span></span>                                               |
| <span data-ttu-id="acd04-249">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="acd04-249">Classes used in</span></span>        | [<span data-ttu-id="acd04-250">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="acd04-250">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="acd04-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="acd04-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="acd04-252">Eingabe</span><span class="sxs-lookup"><span data-stu-id="acd04-252">Entry</span></span> | <span data-ttu-id="acd04-253">Wert</span><span class="sxs-lookup"><span data-stu-id="acd04-253">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="acd04-254">Link-ID</span><span class="sxs-lookup"><span data-stu-id="acd04-254">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="acd04-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acd04-255">MAPI-Id</span></span>                | <span data-ttu-id="acd04-256">0x80c1</span><span class="sxs-lookup"><span data-stu-id="acd04-256">0x80C1</span></span>                                                   |
| <span data-ttu-id="acd04-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="acd04-257">System-Only</span></span>            | <span data-ttu-id="acd04-258">Richtig</span><span class="sxs-lookup"><span data-stu-id="acd04-258">True</span></span>                                                     |
| <span data-ttu-id="acd04-259">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="acd04-259">Is-Single-Valued</span></span>       | <span data-ttu-id="acd04-260">Richtig</span><span class="sxs-lookup"><span data-stu-id="acd04-260">True</span></span>                                                     |
| <span data-ttu-id="acd04-261">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="acd04-261">Is Indexed</span></span>             | <span data-ttu-id="acd04-262">False</span><span class="sxs-lookup"><span data-stu-id="acd04-262">False</span></span>                                                    |
| <span data-ttu-id="acd04-263">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="acd04-263">In Global Catalog</span></span>      | <span data-ttu-id="acd04-264">False</span><span class="sxs-lookup"><span data-stu-id="acd04-264">False</span></span>                                                    |
| <span data-ttu-id="acd04-265">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="acd04-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="acd04-266">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="acd04-266">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="acd04-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acd04-267">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="acd04-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acd04-268">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="acd04-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acd04-269">Search-Flags</span></span>           | <span data-ttu-id="acd04-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acd04-270">0x00000000</span></span>                                               |
| <span data-ttu-id="acd04-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acd04-271">System-Flags</span></span>           | <span data-ttu-id="acd04-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acd04-272">0x00000010</span></span>                                               |
| <span data-ttu-id="acd04-273">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="acd04-273">Classes used in</span></span>        | [<span data-ttu-id="acd04-274">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="acd04-274">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="acd04-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="acd04-275">Windows Server 2012</span></span>



| <span data-ttu-id="acd04-276">Eingabe</span><span class="sxs-lookup"><span data-stu-id="acd04-276">Entry</span></span> | <span data-ttu-id="acd04-277">Wert</span><span class="sxs-lookup"><span data-stu-id="acd04-277">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="acd04-278">Link-ID</span><span class="sxs-lookup"><span data-stu-id="acd04-278">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="acd04-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acd04-279">MAPI-Id</span></span>                | <span data-ttu-id="acd04-280">0x80c1</span><span class="sxs-lookup"><span data-stu-id="acd04-280">0x80C1</span></span>                                                   |
| <span data-ttu-id="acd04-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="acd04-281">System-Only</span></span>            | <span data-ttu-id="acd04-282">Richtig</span><span class="sxs-lookup"><span data-stu-id="acd04-282">True</span></span>                                                     |
| <span data-ttu-id="acd04-283">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="acd04-283">Is-Single-Valued</span></span>       | <span data-ttu-id="acd04-284">Richtig</span><span class="sxs-lookup"><span data-stu-id="acd04-284">True</span></span>                                                     |
| <span data-ttu-id="acd04-285">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="acd04-285">Is Indexed</span></span>             | <span data-ttu-id="acd04-286">False</span><span class="sxs-lookup"><span data-stu-id="acd04-286">False</span></span>                                                    |
| <span data-ttu-id="acd04-287">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="acd04-287">In Global Catalog</span></span>      | <span data-ttu-id="acd04-288">False</span><span class="sxs-lookup"><span data-stu-id="acd04-288">False</span></span>                                                    |
| <span data-ttu-id="acd04-289">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="acd04-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="acd04-290">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="acd04-290">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="acd04-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acd04-291">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="acd04-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acd04-292">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="acd04-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acd04-293">Search-Flags</span></span>           | <span data-ttu-id="acd04-294">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acd04-294">0x00000000</span></span>                                               |
| <span data-ttu-id="acd04-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acd04-295">System-Flags</span></span>           | <span data-ttu-id="acd04-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acd04-296">0x00000010</span></span>                                               |
| <span data-ttu-id="acd04-297">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="acd04-297">Classes used in</span></span>        | [<span data-ttu-id="acd04-298">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="acd04-298">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





