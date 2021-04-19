---
title: LSA-modified-count-Attribut
description: Das LSA-modified-count-Attribut wird zur Unterstützung der Replikation in Windows NT 4,0-Domänen verwendet.
ms.assetid: 6af5931c-5d4f-4061-81a1-e8947d760abc
ms.tgt_platform: multiple
keywords:
- LSA-modified-count-Attribut AD-Schema
- Schema des lsamodimecount-Attributs
topic_type:
- apiref
api_name:
- LSA-Modified-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e042d4d52974457eb1853a3705adb87cc24a7dc3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346369"
---
# <a name="lsa-modified-count-attribute"></a><span data-ttu-id="5335c-105">LSA-modified-count-Attribut</span><span class="sxs-lookup"><span data-stu-id="5335c-105">LSA-Modified-Count attribute</span></span>

<span data-ttu-id="5335c-106">Das **LSA-modified-count-** Attribut wird zur Unterstützung der Replikation in Windows NT 4,0-Domänen verwendet.</span><span class="sxs-lookup"><span data-stu-id="5335c-106">The **LSA-Modified-Count** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="5335c-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5335c-107">Entry</span></span> | <span data-ttu-id="5335c-108">Wert</span><span class="sxs-lookup"><span data-stu-id="5335c-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="5335c-109">CN</span><span class="sxs-lookup"><span data-stu-id="5335c-109">CN</span></span>                | <span data-ttu-id="5335c-110">LSA-geändert-Anzahl</span><span class="sxs-lookup"><span data-stu-id="5335c-110">LSA-Modified-Count</span></span>                   |
| <span data-ttu-id="5335c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5335c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5335c-112">lsamodimecount</span><span class="sxs-lookup"><span data-stu-id="5335c-112">lSAModifiedCount</span></span>                     |
| <span data-ttu-id="5335c-113">Size</span><span class="sxs-lookup"><span data-stu-id="5335c-113">Size</span></span>              | <span data-ttu-id="5335c-114">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="5335c-114">8 bytes</span></span>                              |
| <span data-ttu-id="5335c-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="5335c-115">Update Privilege</span></span>  | <span data-ttu-id="5335c-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5335c-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="5335c-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="5335c-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="5335c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5335c-118">Attribute-Id</span></span>      | <span data-ttu-id="5335c-119">1.2.840.113556.1.4.67</span><span class="sxs-lookup"><span data-stu-id="5335c-119">1.2.840.113556.1.4.67</span></span>                |
| <span data-ttu-id="5335c-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5335c-120">System-Id-Guid</span></span>    | <span data-ttu-id="5335c-121">bf9679ae-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="5335c-121">bf9679ae-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="5335c-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="5335c-122">Syntax</span></span>            | [<span data-ttu-id="5335c-123">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="5335c-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="5335c-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="5335c-124">Implementations</span></span>

-   [<span data-ttu-id="5335c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5335c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5335c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5335c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5335c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5335c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5335c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5335c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5335c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5335c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5335c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5335c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5335c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5335c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="5335c-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5335c-132">Entry</span></span> | <span data-ttu-id="5335c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="5335c-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5335c-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5335c-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5335c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5335c-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5335c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="5335c-136">System-Only</span></span>            | <span data-ttu-id="5335c-137">False</span><span class="sxs-lookup"><span data-stu-id="5335c-137">False</span></span>                                        |
| <span data-ttu-id="5335c-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5335c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="5335c-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="5335c-139">True</span></span>                                         |
| <span data-ttu-id="5335c-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5335c-140">Is Indexed</span></span>             | <span data-ttu-id="5335c-141">False</span><span class="sxs-lookup"><span data-stu-id="5335c-141">False</span></span>                                        |
| <span data-ttu-id="5335c-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5335c-142">In Global Catalog</span></span>      | <span data-ttu-id="5335c-143">False</span><span class="sxs-lookup"><span data-stu-id="5335c-143">False</span></span>                                        |
| <span data-ttu-id="5335c-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5335c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="5335c-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5335c-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5335c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5335c-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5335c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5335c-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5335c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5335c-148">Search-Flags</span></span>           | <span data-ttu-id="5335c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5335c-149">0x00000000</span></span>                                   |
| <span data-ttu-id="5335c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5335c-150">System-Flags</span></span>           | <span data-ttu-id="5335c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5335c-151">0x00000010</span></span>                                   |
| <span data-ttu-id="5335c-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5335c-152">Classes used in</span></span>        | [<span data-ttu-id="5335c-153">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="5335c-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5335c-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5335c-154">Windows Server 2003</span></span>



| <span data-ttu-id="5335c-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5335c-155">Entry</span></span> | <span data-ttu-id="5335c-156">Wert</span><span class="sxs-lookup"><span data-stu-id="5335c-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5335c-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5335c-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5335c-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5335c-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5335c-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="5335c-159">System-Only</span></span>            | <span data-ttu-id="5335c-160">False</span><span class="sxs-lookup"><span data-stu-id="5335c-160">False</span></span>                                        |
| <span data-ttu-id="5335c-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5335c-161">Is-Single-Valued</span></span>       | <span data-ttu-id="5335c-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="5335c-162">True</span></span>                                         |
| <span data-ttu-id="5335c-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5335c-163">Is Indexed</span></span>             | <span data-ttu-id="5335c-164">False</span><span class="sxs-lookup"><span data-stu-id="5335c-164">False</span></span>                                        |
| <span data-ttu-id="5335c-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5335c-165">In Global Catalog</span></span>      | <span data-ttu-id="5335c-166">False</span><span class="sxs-lookup"><span data-stu-id="5335c-166">False</span></span>                                        |
| <span data-ttu-id="5335c-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5335c-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="5335c-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5335c-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5335c-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5335c-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5335c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5335c-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5335c-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5335c-171">Search-Flags</span></span>           | <span data-ttu-id="5335c-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5335c-172">0x00000000</span></span>                                   |
| <span data-ttu-id="5335c-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5335c-173">System-Flags</span></span>           | <span data-ttu-id="5335c-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5335c-174">0x00000010</span></span>                                   |
| <span data-ttu-id="5335c-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5335c-175">Classes used in</span></span>        | [<span data-ttu-id="5335c-176">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="5335c-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5335c-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5335c-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5335c-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5335c-178">Entry</span></span> | <span data-ttu-id="5335c-179">Wert</span><span class="sxs-lookup"><span data-stu-id="5335c-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5335c-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5335c-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5335c-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5335c-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5335c-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="5335c-182">System-Only</span></span>            | <span data-ttu-id="5335c-183">False</span><span class="sxs-lookup"><span data-stu-id="5335c-183">False</span></span>                                        |
| <span data-ttu-id="5335c-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5335c-184">Is-Single-Valued</span></span>       | <span data-ttu-id="5335c-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="5335c-185">True</span></span>                                         |
| <span data-ttu-id="5335c-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5335c-186">Is Indexed</span></span>             | <span data-ttu-id="5335c-187">False</span><span class="sxs-lookup"><span data-stu-id="5335c-187">False</span></span>                                        |
| <span data-ttu-id="5335c-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5335c-188">In Global Catalog</span></span>      | <span data-ttu-id="5335c-189">False</span><span class="sxs-lookup"><span data-stu-id="5335c-189">False</span></span>                                        |
| <span data-ttu-id="5335c-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5335c-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="5335c-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5335c-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5335c-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5335c-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5335c-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5335c-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5335c-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5335c-194">Search-Flags</span></span>           | <span data-ttu-id="5335c-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5335c-195">0x00000000</span></span>                                   |
| <span data-ttu-id="5335c-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5335c-196">System-Flags</span></span>           | <span data-ttu-id="5335c-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5335c-197">0x00000010</span></span>                                   |
| <span data-ttu-id="5335c-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5335c-198">Classes used in</span></span>        | [<span data-ttu-id="5335c-199">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="5335c-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5335c-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5335c-200">Windows Server 2008</span></span>



| <span data-ttu-id="5335c-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5335c-201">Entry</span></span> | <span data-ttu-id="5335c-202">Wert</span><span class="sxs-lookup"><span data-stu-id="5335c-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5335c-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5335c-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5335c-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5335c-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5335c-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="5335c-205">System-Only</span></span>            | <span data-ttu-id="5335c-206">False</span><span class="sxs-lookup"><span data-stu-id="5335c-206">False</span></span>                                        |
| <span data-ttu-id="5335c-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5335c-207">Is-Single-Valued</span></span>       | <span data-ttu-id="5335c-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="5335c-208">True</span></span>                                         |
| <span data-ttu-id="5335c-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5335c-209">Is Indexed</span></span>             | <span data-ttu-id="5335c-210">False</span><span class="sxs-lookup"><span data-stu-id="5335c-210">False</span></span>                                        |
| <span data-ttu-id="5335c-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5335c-211">In Global Catalog</span></span>      | <span data-ttu-id="5335c-212">False</span><span class="sxs-lookup"><span data-stu-id="5335c-212">False</span></span>                                        |
| <span data-ttu-id="5335c-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5335c-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="5335c-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5335c-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5335c-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5335c-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5335c-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5335c-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5335c-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5335c-217">Search-Flags</span></span>           | <span data-ttu-id="5335c-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5335c-218">0x00000000</span></span>                                   |
| <span data-ttu-id="5335c-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5335c-219">System-Flags</span></span>           | <span data-ttu-id="5335c-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5335c-220">0x00000010</span></span>                                   |
| <span data-ttu-id="5335c-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5335c-221">Classes used in</span></span>        | [<span data-ttu-id="5335c-222">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="5335c-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5335c-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5335c-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5335c-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5335c-224">Entry</span></span> | <span data-ttu-id="5335c-225">Wert</span><span class="sxs-lookup"><span data-stu-id="5335c-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5335c-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5335c-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5335c-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5335c-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5335c-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="5335c-228">System-Only</span></span>            | <span data-ttu-id="5335c-229">False</span><span class="sxs-lookup"><span data-stu-id="5335c-229">False</span></span>                                        |
| <span data-ttu-id="5335c-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5335c-230">Is-Single-Valued</span></span>       | <span data-ttu-id="5335c-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="5335c-231">True</span></span>                                         |
| <span data-ttu-id="5335c-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5335c-232">Is Indexed</span></span>             | <span data-ttu-id="5335c-233">False</span><span class="sxs-lookup"><span data-stu-id="5335c-233">False</span></span>                                        |
| <span data-ttu-id="5335c-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5335c-234">In Global Catalog</span></span>      | <span data-ttu-id="5335c-235">False</span><span class="sxs-lookup"><span data-stu-id="5335c-235">False</span></span>                                        |
| <span data-ttu-id="5335c-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5335c-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="5335c-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5335c-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5335c-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5335c-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5335c-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5335c-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5335c-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5335c-240">Search-Flags</span></span>           | <span data-ttu-id="5335c-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5335c-241">0x00000000</span></span>                                   |
| <span data-ttu-id="5335c-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5335c-242">System-Flags</span></span>           | <span data-ttu-id="5335c-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5335c-243">0x00000010</span></span>                                   |
| <span data-ttu-id="5335c-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5335c-244">Classes used in</span></span>        | [<span data-ttu-id="5335c-245">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="5335c-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5335c-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5335c-246">Windows Server 2012</span></span>



| <span data-ttu-id="5335c-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5335c-247">Entry</span></span> | <span data-ttu-id="5335c-248">Wert</span><span class="sxs-lookup"><span data-stu-id="5335c-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5335c-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5335c-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5335c-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5335c-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5335c-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="5335c-251">System-Only</span></span>            | <span data-ttu-id="5335c-252">False</span><span class="sxs-lookup"><span data-stu-id="5335c-252">False</span></span>                                        |
| <span data-ttu-id="5335c-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5335c-253">Is-Single-Valued</span></span>       | <span data-ttu-id="5335c-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="5335c-254">True</span></span>                                         |
| <span data-ttu-id="5335c-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5335c-255">Is Indexed</span></span>             | <span data-ttu-id="5335c-256">False</span><span class="sxs-lookup"><span data-stu-id="5335c-256">False</span></span>                                        |
| <span data-ttu-id="5335c-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5335c-257">In Global Catalog</span></span>      | <span data-ttu-id="5335c-258">False</span><span class="sxs-lookup"><span data-stu-id="5335c-258">False</span></span>                                        |
| <span data-ttu-id="5335c-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5335c-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="5335c-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5335c-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5335c-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5335c-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5335c-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5335c-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5335c-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5335c-263">Search-Flags</span></span>           | <span data-ttu-id="5335c-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5335c-264">0x00000000</span></span>                                   |
| <span data-ttu-id="5335c-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5335c-265">System-Flags</span></span>           | <span data-ttu-id="5335c-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5335c-266">0x00000010</span></span>                                   |
| <span data-ttu-id="5335c-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5335c-267">Classes used in</span></span>        | [<span data-ttu-id="5335c-268">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="5335c-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





