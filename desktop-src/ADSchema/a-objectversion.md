---
title: Object-Version-Attribut
description: Diese kann verwendet werden, um eine Versionsnummer für das-Objekt zu speichern.
ms.assetid: 1aa8520b-c640-4ea2-9230-f28154bf69b0
ms.tgt_platform: multiple
keywords:
- AD-Schema für Object-Version-Attribut
- objectVersion-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Object-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f038f6286db575f4141c2e306086bb9a8faac71
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344758"
---
# <a name="object-version-attribute"></a><span data-ttu-id="b7837-105">Object-Version-Attribut</span><span class="sxs-lookup"><span data-stu-id="b7837-105">Object-Version attribute</span></span>

<span data-ttu-id="b7837-106">Diese kann verwendet werden, um eine Versionsnummer für das-Objekt zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b7837-106">This can be used to store a version number for the object.</span></span>



| <span data-ttu-id="b7837-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b7837-107">Entry</span></span> | <span data-ttu-id="b7837-108">Wert</span><span class="sxs-lookup"><span data-stu-id="b7837-108">Value</span></span> |
|-------------------|----------------------------------------------------------------|
| <span data-ttu-id="b7837-109">CN</span><span class="sxs-lookup"><span data-stu-id="b7837-109">CN</span></span>                | <span data-ttu-id="b7837-110">Object-Version</span><span class="sxs-lookup"><span data-stu-id="b7837-110">Object-Version</span></span>                                                 |
| <span data-ttu-id="b7837-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b7837-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b7837-112">ob objectVersion für</span><span class="sxs-lookup"><span data-stu-id="b7837-112">objectVersion</span></span>                                                  |
| <span data-ttu-id="b7837-113">Size</span><span class="sxs-lookup"><span data-stu-id="b7837-113">Size</span></span>              | <span data-ttu-id="b7837-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="b7837-114">4 bytes</span></span>                                                        |
| <span data-ttu-id="b7837-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b7837-115">Update Privilege</span></span>  | <span data-ttu-id="b7837-116">Dieser Wert wird vom Designer des-Objekts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b7837-116">The designer of the object would set this value.</span></span>               |
| <span data-ttu-id="b7837-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="b7837-117">Update Frequency</span></span>  | <span data-ttu-id="b7837-118">Dieser Wert sollte jedes Mal erhöht werden, wenn sich das Objekt ändert.</span><span class="sxs-lookup"><span data-stu-id="b7837-118">This value should be incremented each time the object changes.</span></span> |
| <span data-ttu-id="b7837-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b7837-119">Attribute-Id</span></span>      | <span data-ttu-id="b7837-120">1.2.840.113556.1.2.76</span><span class="sxs-lookup"><span data-stu-id="b7837-120">1.2.840.113556.1.2.76</span></span>                                          |
| <span data-ttu-id="b7837-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b7837-121">System-Id-Guid</span></span>    | <span data-ttu-id="b7837-122">16775848-47F 3-11d1-a9c3-0000 C1</span><span class="sxs-lookup"><span data-stu-id="b7837-122">16775848-47f3-11d1-a9c3-0000f80367c1</span></span>                           |
| <span data-ttu-id="b7837-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7837-123">Syntax</span></span>            | [<span data-ttu-id="b7837-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="b7837-124">**Enumeration**</span></span>](s-enumeration.md)                           |



## <a name="implementations"></a><span data-ttu-id="b7837-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="b7837-125">Implementations</span></span>

-   [<span data-ttu-id="b7837-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b7837-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b7837-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b7837-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b7837-128">**Adam**</span><span class="sxs-lookup"><span data-stu-id="b7837-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b7837-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b7837-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b7837-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b7837-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b7837-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b7837-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b7837-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b7837-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b7837-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b7837-133">Windows 2000 Server</span></span>



| <span data-ttu-id="b7837-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b7837-134">Entry</span></span> | <span data-ttu-id="b7837-135">Wert</span><span class="sxs-lookup"><span data-stu-id="b7837-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b7837-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b7837-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b7837-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7837-137">MAPI-Id</span></span>                | <span data-ttu-id="b7837-138">0x80f 7</span><span class="sxs-lookup"><span data-stu-id="b7837-138">0x80F7</span></span>                          |
| <span data-ttu-id="b7837-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7837-139">System-Only</span></span>            | <span data-ttu-id="b7837-140">False</span><span class="sxs-lookup"><span data-stu-id="b7837-140">False</span></span>                           |
| <span data-ttu-id="b7837-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b7837-141">Is-Single-Valued</span></span>       | <span data-ttu-id="b7837-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="b7837-142">True</span></span>                            |
| <span data-ttu-id="b7837-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b7837-143">Is Indexed</span></span>             | <span data-ttu-id="b7837-144">False</span><span class="sxs-lookup"><span data-stu-id="b7837-144">False</span></span>                           |
| <span data-ttu-id="b7837-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b7837-145">In Global Catalog</span></span>      | <span data-ttu-id="b7837-146">False</span><span class="sxs-lookup"><span data-stu-id="b7837-146">False</span></span>                           |
| <span data-ttu-id="b7837-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7837-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7837-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b7837-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b7837-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7837-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b7837-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7837-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b7837-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7837-151">Search-Flags</span></span>           | <span data-ttu-id="b7837-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7837-152">0x00000000</span></span>                      |
| <span data-ttu-id="b7837-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7837-153">System-Flags</span></span>           | <span data-ttu-id="b7837-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7837-154">0x00000010</span></span>                      |
| <span data-ttu-id="b7837-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b7837-155">Classes used in</span></span>        | [<span data-ttu-id="b7837-156">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b7837-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b7837-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b7837-157">Windows Server 2003</span></span>



| <span data-ttu-id="b7837-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b7837-158">Entry</span></span> | <span data-ttu-id="b7837-159">Wert</span><span class="sxs-lookup"><span data-stu-id="b7837-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b7837-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b7837-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b7837-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7837-161">MAPI-Id</span></span>                | <span data-ttu-id="b7837-162">0x80f 7</span><span class="sxs-lookup"><span data-stu-id="b7837-162">0x80F7</span></span>                          |
| <span data-ttu-id="b7837-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7837-163">System-Only</span></span>            | <span data-ttu-id="b7837-164">False</span><span class="sxs-lookup"><span data-stu-id="b7837-164">False</span></span>                           |
| <span data-ttu-id="b7837-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b7837-165">Is-Single-Valued</span></span>       | <span data-ttu-id="b7837-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="b7837-166">True</span></span>                            |
| <span data-ttu-id="b7837-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b7837-167">Is Indexed</span></span>             | <span data-ttu-id="b7837-168">False</span><span class="sxs-lookup"><span data-stu-id="b7837-168">False</span></span>                           |
| <span data-ttu-id="b7837-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b7837-169">In Global Catalog</span></span>      | <span data-ttu-id="b7837-170">False</span><span class="sxs-lookup"><span data-stu-id="b7837-170">False</span></span>                           |
| <span data-ttu-id="b7837-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7837-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7837-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b7837-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b7837-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7837-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b7837-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7837-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b7837-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7837-175">Search-Flags</span></span>           | <span data-ttu-id="b7837-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7837-176">0x00000000</span></span>                      |
| <span data-ttu-id="b7837-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7837-177">System-Flags</span></span>           | <span data-ttu-id="b7837-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7837-178">0x00000010</span></span>                      |
| <span data-ttu-id="b7837-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b7837-179">Classes used in</span></span>        | [<span data-ttu-id="b7837-180">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b7837-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b7837-181">Adam</span><span class="sxs-lookup"><span data-stu-id="b7837-181">ADAM</span></span>



| <span data-ttu-id="b7837-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b7837-182">Entry</span></span> | <span data-ttu-id="b7837-183">Wert</span><span class="sxs-lookup"><span data-stu-id="b7837-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b7837-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b7837-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b7837-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7837-185">MAPI-Id</span></span>                | <span data-ttu-id="b7837-186">0x80f 7</span><span class="sxs-lookup"><span data-stu-id="b7837-186">0x80F7</span></span>                          |
| <span data-ttu-id="b7837-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7837-187">System-Only</span></span>            | <span data-ttu-id="b7837-188">False</span><span class="sxs-lookup"><span data-stu-id="b7837-188">False</span></span>                           |
| <span data-ttu-id="b7837-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b7837-189">Is-Single-Valued</span></span>       | <span data-ttu-id="b7837-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="b7837-190">True</span></span>                            |
| <span data-ttu-id="b7837-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b7837-191">Is Indexed</span></span>             | <span data-ttu-id="b7837-192">False</span><span class="sxs-lookup"><span data-stu-id="b7837-192">False</span></span>                           |
| <span data-ttu-id="b7837-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b7837-193">In Global Catalog</span></span>      | <span data-ttu-id="b7837-194">False</span><span class="sxs-lookup"><span data-stu-id="b7837-194">False</span></span>                           |
| <span data-ttu-id="b7837-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7837-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7837-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b7837-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b7837-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7837-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b7837-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7837-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b7837-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7837-199">Search-Flags</span></span>           | <span data-ttu-id="b7837-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7837-200">0x00000000</span></span>                      |
| <span data-ttu-id="b7837-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7837-201">System-Flags</span></span>           | <span data-ttu-id="b7837-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7837-202">0x00000010</span></span>                      |
| <span data-ttu-id="b7837-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b7837-203">Classes used in</span></span>        | [<span data-ttu-id="b7837-204">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b7837-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b7837-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b7837-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b7837-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b7837-206">Entry</span></span> | <span data-ttu-id="b7837-207">Wert</span><span class="sxs-lookup"><span data-stu-id="b7837-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b7837-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b7837-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b7837-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7837-209">MAPI-Id</span></span>                | <span data-ttu-id="b7837-210">0x80f 7</span><span class="sxs-lookup"><span data-stu-id="b7837-210">0x80F7</span></span>                          |
| <span data-ttu-id="b7837-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7837-211">System-Only</span></span>            | <span data-ttu-id="b7837-212">False</span><span class="sxs-lookup"><span data-stu-id="b7837-212">False</span></span>                           |
| <span data-ttu-id="b7837-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b7837-213">Is-Single-Valued</span></span>       | <span data-ttu-id="b7837-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="b7837-214">True</span></span>                            |
| <span data-ttu-id="b7837-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b7837-215">Is Indexed</span></span>             | <span data-ttu-id="b7837-216">False</span><span class="sxs-lookup"><span data-stu-id="b7837-216">False</span></span>                           |
| <span data-ttu-id="b7837-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b7837-217">In Global Catalog</span></span>      | <span data-ttu-id="b7837-218">False</span><span class="sxs-lookup"><span data-stu-id="b7837-218">False</span></span>                           |
| <span data-ttu-id="b7837-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7837-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7837-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b7837-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b7837-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7837-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b7837-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7837-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b7837-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7837-223">Search-Flags</span></span>           | <span data-ttu-id="b7837-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7837-224">0x00000000</span></span>                      |
| <span data-ttu-id="b7837-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7837-225">System-Flags</span></span>           | <span data-ttu-id="b7837-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7837-226">0x00000010</span></span>                      |
| <span data-ttu-id="b7837-227">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b7837-227">Classes used in</span></span>        | [<span data-ttu-id="b7837-228">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b7837-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b7837-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7837-229">Windows Server 2008</span></span>



| <span data-ttu-id="b7837-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b7837-230">Entry</span></span> | <span data-ttu-id="b7837-231">Wert</span><span class="sxs-lookup"><span data-stu-id="b7837-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b7837-232">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b7837-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b7837-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7837-233">MAPI-Id</span></span>                | <span data-ttu-id="b7837-234">0x80f 7</span><span class="sxs-lookup"><span data-stu-id="b7837-234">0x80F7</span></span>                          |
| <span data-ttu-id="b7837-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7837-235">System-Only</span></span>            | <span data-ttu-id="b7837-236">False</span><span class="sxs-lookup"><span data-stu-id="b7837-236">False</span></span>                           |
| <span data-ttu-id="b7837-237">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b7837-237">Is-Single-Valued</span></span>       | <span data-ttu-id="b7837-238">Richtig</span><span class="sxs-lookup"><span data-stu-id="b7837-238">True</span></span>                            |
| <span data-ttu-id="b7837-239">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b7837-239">Is Indexed</span></span>             | <span data-ttu-id="b7837-240">False</span><span class="sxs-lookup"><span data-stu-id="b7837-240">False</span></span>                           |
| <span data-ttu-id="b7837-241">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b7837-241">In Global Catalog</span></span>      | <span data-ttu-id="b7837-242">False</span><span class="sxs-lookup"><span data-stu-id="b7837-242">False</span></span>                           |
| <span data-ttu-id="b7837-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7837-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7837-244">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b7837-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b7837-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7837-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b7837-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7837-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b7837-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7837-247">Search-Flags</span></span>           | <span data-ttu-id="b7837-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7837-248">0x00000000</span></span>                      |
| <span data-ttu-id="b7837-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7837-249">System-Flags</span></span>           | <span data-ttu-id="b7837-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7837-250">0x00000010</span></span>                      |
| <span data-ttu-id="b7837-251">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b7837-251">Classes used in</span></span>        | [<span data-ttu-id="b7837-252">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b7837-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b7837-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b7837-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b7837-254">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b7837-254">Entry</span></span> | <span data-ttu-id="b7837-255">Wert</span><span class="sxs-lookup"><span data-stu-id="b7837-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b7837-256">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b7837-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b7837-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7837-257">MAPI-Id</span></span>                | <span data-ttu-id="b7837-258">0x80f 7</span><span class="sxs-lookup"><span data-stu-id="b7837-258">0x80F7</span></span>                          |
| <span data-ttu-id="b7837-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7837-259">System-Only</span></span>            | <span data-ttu-id="b7837-260">False</span><span class="sxs-lookup"><span data-stu-id="b7837-260">False</span></span>                           |
| <span data-ttu-id="b7837-261">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b7837-261">Is-Single-Valued</span></span>       | <span data-ttu-id="b7837-262">Richtig</span><span class="sxs-lookup"><span data-stu-id="b7837-262">True</span></span>                            |
| <span data-ttu-id="b7837-263">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b7837-263">Is Indexed</span></span>             | <span data-ttu-id="b7837-264">False</span><span class="sxs-lookup"><span data-stu-id="b7837-264">False</span></span>                           |
| <span data-ttu-id="b7837-265">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b7837-265">In Global Catalog</span></span>      | <span data-ttu-id="b7837-266">False</span><span class="sxs-lookup"><span data-stu-id="b7837-266">False</span></span>                           |
| <span data-ttu-id="b7837-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7837-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7837-268">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b7837-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b7837-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7837-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b7837-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7837-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b7837-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7837-271">Search-Flags</span></span>           | <span data-ttu-id="b7837-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7837-272">0x00000000</span></span>                      |
| <span data-ttu-id="b7837-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7837-273">System-Flags</span></span>           | <span data-ttu-id="b7837-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7837-274">0x00000010</span></span>                      |
| <span data-ttu-id="b7837-275">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b7837-275">Classes used in</span></span>        | [<span data-ttu-id="b7837-276">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b7837-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b7837-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b7837-277">Windows Server 2012</span></span>



| <span data-ttu-id="b7837-278">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b7837-278">Entry</span></span> | <span data-ttu-id="b7837-279">Wert</span><span class="sxs-lookup"><span data-stu-id="b7837-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b7837-280">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b7837-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b7837-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7837-281">MAPI-Id</span></span>                | <span data-ttu-id="b7837-282">0x80f 7</span><span class="sxs-lookup"><span data-stu-id="b7837-282">0x80F7</span></span>                          |
| <span data-ttu-id="b7837-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7837-283">System-Only</span></span>            | <span data-ttu-id="b7837-284">False</span><span class="sxs-lookup"><span data-stu-id="b7837-284">False</span></span>                           |
| <span data-ttu-id="b7837-285">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b7837-285">Is-Single-Valued</span></span>       | <span data-ttu-id="b7837-286">Richtig</span><span class="sxs-lookup"><span data-stu-id="b7837-286">True</span></span>                            |
| <span data-ttu-id="b7837-287">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b7837-287">Is Indexed</span></span>             | <span data-ttu-id="b7837-288">False</span><span class="sxs-lookup"><span data-stu-id="b7837-288">False</span></span>                           |
| <span data-ttu-id="b7837-289">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b7837-289">In Global Catalog</span></span>      | <span data-ttu-id="b7837-290">False</span><span class="sxs-lookup"><span data-stu-id="b7837-290">False</span></span>                           |
| <span data-ttu-id="b7837-291">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7837-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7837-292">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b7837-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b7837-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7837-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b7837-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7837-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b7837-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7837-295">Search-Flags</span></span>           | <span data-ttu-id="b7837-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7837-296">0x00000000</span></span>                      |
| <span data-ttu-id="b7837-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7837-297">System-Flags</span></span>           | <span data-ttu-id="b7837-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7837-298">0x00000010</span></span>                      |
| <span data-ttu-id="b7837-299">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b7837-299">Classes used in</span></span>        | [<span data-ttu-id="b7837-300">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b7837-300">**Top**</span></span>](c-top.md)<br/> |



 

 





