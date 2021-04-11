---
title: Builtin-modified-count-Attribut
description: Das Attribut "builtin-modified-count" wird zur Unterstützung der Replikation in Windows NT 4,0-Domänen verwendet.
ms.assetid: e5a0f299-1e69-4b47-a0b1-e5bcf7bd47eb
ms.tgt_platform: multiple
keywords:
- Builtin-modified-count-Attribut AD-Schema
- builtinmodifiedcount-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Builtin-Modified-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7731cd27ef5cb5d25dcd4bced4dbc5932225ba5d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123097"
---
# <a name="builtin-modified-count-attribute"></a><span data-ttu-id="8e705-105">Builtin-modified-count-Attribut</span><span class="sxs-lookup"><span data-stu-id="8e705-105">Builtin-Modified-Count attribute</span></span>

<span data-ttu-id="8e705-106">Das Attribut " **builtin-modified-count** " wird zur Unterstützung der Replikation in Windows NT 4,0-Domänen verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e705-106">The **Builtin-Modified-Count** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="8e705-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e705-107">Entry</span></span> | <span data-ttu-id="8e705-108">Wert</span><span class="sxs-lookup"><span data-stu-id="8e705-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8e705-109">CN</span><span class="sxs-lookup"><span data-stu-id="8e705-109">CN</span></span>                | <span data-ttu-id="8e705-110">Builtin-modified-count</span><span class="sxs-lookup"><span data-stu-id="8e705-110">Builtin-Modified-Count</span></span>               |
| <span data-ttu-id="8e705-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8e705-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8e705-112">builtinmodifiedcount</span><span class="sxs-lookup"><span data-stu-id="8e705-112">builtinModifiedCount</span></span>                 |
| <span data-ttu-id="8e705-113">Size</span><span class="sxs-lookup"><span data-stu-id="8e705-113">Size</span></span>              | <span data-ttu-id="8e705-114">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="8e705-114">8 bytes</span></span>                              |
| <span data-ttu-id="8e705-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="8e705-115">Update Privilege</span></span>  | <span data-ttu-id="8e705-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8e705-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="8e705-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="8e705-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8e705-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8e705-118">Attribute-Id</span></span>      | <span data-ttu-id="8e705-119">1.2.840.113556.1.4.14</span><span class="sxs-lookup"><span data-stu-id="8e705-119">1.2.840.113556.1.4.14</span></span>                |
| <span data-ttu-id="8e705-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8e705-120">System-Id-Guid</span></span>    | <span data-ttu-id="8e705-121">bf967930-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="8e705-121">bf967930-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="8e705-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e705-122">Syntax</span></span>            | [<span data-ttu-id="8e705-123">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="8e705-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="8e705-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="8e705-124">Implementations</span></span>

-   [<span data-ttu-id="8e705-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8e705-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8e705-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8e705-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8e705-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8e705-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8e705-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8e705-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8e705-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8e705-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8e705-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8e705-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8e705-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8e705-131">Windows 2000 Server</span></span>



| <span data-ttu-id="8e705-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e705-132">Entry</span></span> | <span data-ttu-id="8e705-133">Wert</span><span class="sxs-lookup"><span data-stu-id="8e705-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8e705-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8e705-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8e705-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e705-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8e705-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e705-136">System-Only</span></span>            | <span data-ttu-id="8e705-137">False</span><span class="sxs-lookup"><span data-stu-id="8e705-137">False</span></span>                                        |
| <span data-ttu-id="8e705-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8e705-138">Is-Single-Valued</span></span>       | <span data-ttu-id="8e705-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="8e705-139">True</span></span>                                         |
| <span data-ttu-id="8e705-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8e705-140">Is Indexed</span></span>             | <span data-ttu-id="8e705-141">False</span><span class="sxs-lookup"><span data-stu-id="8e705-141">False</span></span>                                        |
| <span data-ttu-id="8e705-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8e705-142">In Global Catalog</span></span>      | <span data-ttu-id="8e705-143">False</span><span class="sxs-lookup"><span data-stu-id="8e705-143">False</span></span>                                        |
| <span data-ttu-id="8e705-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8e705-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e705-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8e705-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8e705-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e705-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8e705-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e705-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8e705-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e705-148">Search-Flags</span></span>           | <span data-ttu-id="8e705-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e705-149">0x00000000</span></span>                                   |
| <span data-ttu-id="8e705-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e705-150">System-Flags</span></span>           | <span data-ttu-id="8e705-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e705-151">0x00000010</span></span>                                   |
| <span data-ttu-id="8e705-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8e705-152">Classes used in</span></span>        | [<span data-ttu-id="8e705-153">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="8e705-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8e705-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8e705-154">Windows Server 2003</span></span>



| <span data-ttu-id="8e705-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e705-155">Entry</span></span> | <span data-ttu-id="8e705-156">Wert</span><span class="sxs-lookup"><span data-stu-id="8e705-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8e705-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8e705-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8e705-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e705-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8e705-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e705-159">System-Only</span></span>            | <span data-ttu-id="8e705-160">False</span><span class="sxs-lookup"><span data-stu-id="8e705-160">False</span></span>                                        |
| <span data-ttu-id="8e705-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8e705-161">Is-Single-Valued</span></span>       | <span data-ttu-id="8e705-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="8e705-162">True</span></span>                                         |
| <span data-ttu-id="8e705-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8e705-163">Is Indexed</span></span>             | <span data-ttu-id="8e705-164">False</span><span class="sxs-lookup"><span data-stu-id="8e705-164">False</span></span>                                        |
| <span data-ttu-id="8e705-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8e705-165">In Global Catalog</span></span>      | <span data-ttu-id="8e705-166">False</span><span class="sxs-lookup"><span data-stu-id="8e705-166">False</span></span>                                        |
| <span data-ttu-id="8e705-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8e705-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e705-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8e705-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8e705-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e705-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8e705-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e705-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8e705-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e705-171">Search-Flags</span></span>           | <span data-ttu-id="8e705-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e705-172">0x00000000</span></span>                                   |
| <span data-ttu-id="8e705-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e705-173">System-Flags</span></span>           | <span data-ttu-id="8e705-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e705-174">0x00000010</span></span>                                   |
| <span data-ttu-id="8e705-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8e705-175">Classes used in</span></span>        | [<span data-ttu-id="8e705-176">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="8e705-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8e705-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8e705-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8e705-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e705-178">Entry</span></span> | <span data-ttu-id="8e705-179">Wert</span><span class="sxs-lookup"><span data-stu-id="8e705-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8e705-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8e705-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8e705-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e705-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8e705-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e705-182">System-Only</span></span>            | <span data-ttu-id="8e705-183">False</span><span class="sxs-lookup"><span data-stu-id="8e705-183">False</span></span>                                        |
| <span data-ttu-id="8e705-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8e705-184">Is-Single-Valued</span></span>       | <span data-ttu-id="8e705-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="8e705-185">True</span></span>                                         |
| <span data-ttu-id="8e705-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8e705-186">Is Indexed</span></span>             | <span data-ttu-id="8e705-187">False</span><span class="sxs-lookup"><span data-stu-id="8e705-187">False</span></span>                                        |
| <span data-ttu-id="8e705-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8e705-188">In Global Catalog</span></span>      | <span data-ttu-id="8e705-189">False</span><span class="sxs-lookup"><span data-stu-id="8e705-189">False</span></span>                                        |
| <span data-ttu-id="8e705-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8e705-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e705-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8e705-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8e705-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e705-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8e705-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e705-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8e705-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e705-194">Search-Flags</span></span>           | <span data-ttu-id="8e705-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e705-195">0x00000000</span></span>                                   |
| <span data-ttu-id="8e705-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e705-196">System-Flags</span></span>           | <span data-ttu-id="8e705-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e705-197">0x00000010</span></span>                                   |
| <span data-ttu-id="8e705-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8e705-198">Classes used in</span></span>        | [<span data-ttu-id="8e705-199">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="8e705-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8e705-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e705-200">Windows Server 2008</span></span>



| <span data-ttu-id="8e705-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e705-201">Entry</span></span> | <span data-ttu-id="8e705-202">Wert</span><span class="sxs-lookup"><span data-stu-id="8e705-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8e705-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8e705-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8e705-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e705-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8e705-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e705-205">System-Only</span></span>            | <span data-ttu-id="8e705-206">False</span><span class="sxs-lookup"><span data-stu-id="8e705-206">False</span></span>                                        |
| <span data-ttu-id="8e705-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8e705-207">Is-Single-Valued</span></span>       | <span data-ttu-id="8e705-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="8e705-208">True</span></span>                                         |
| <span data-ttu-id="8e705-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8e705-209">Is Indexed</span></span>             | <span data-ttu-id="8e705-210">False</span><span class="sxs-lookup"><span data-stu-id="8e705-210">False</span></span>                                        |
| <span data-ttu-id="8e705-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8e705-211">In Global Catalog</span></span>      | <span data-ttu-id="8e705-212">False</span><span class="sxs-lookup"><span data-stu-id="8e705-212">False</span></span>                                        |
| <span data-ttu-id="8e705-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8e705-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e705-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8e705-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8e705-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e705-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8e705-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e705-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8e705-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e705-217">Search-Flags</span></span>           | <span data-ttu-id="8e705-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e705-218">0x00000000</span></span>                                   |
| <span data-ttu-id="8e705-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e705-219">System-Flags</span></span>           | <span data-ttu-id="8e705-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e705-220">0x00000010</span></span>                                   |
| <span data-ttu-id="8e705-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8e705-221">Classes used in</span></span>        | [<span data-ttu-id="8e705-222">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="8e705-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8e705-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8e705-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8e705-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e705-224">Entry</span></span> | <span data-ttu-id="8e705-225">Wert</span><span class="sxs-lookup"><span data-stu-id="8e705-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8e705-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8e705-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8e705-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e705-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8e705-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e705-228">System-Only</span></span>            | <span data-ttu-id="8e705-229">False</span><span class="sxs-lookup"><span data-stu-id="8e705-229">False</span></span>                                        |
| <span data-ttu-id="8e705-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8e705-230">Is-Single-Valued</span></span>       | <span data-ttu-id="8e705-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="8e705-231">True</span></span>                                         |
| <span data-ttu-id="8e705-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8e705-232">Is Indexed</span></span>             | <span data-ttu-id="8e705-233">False</span><span class="sxs-lookup"><span data-stu-id="8e705-233">False</span></span>                                        |
| <span data-ttu-id="8e705-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8e705-234">In Global Catalog</span></span>      | <span data-ttu-id="8e705-235">False</span><span class="sxs-lookup"><span data-stu-id="8e705-235">False</span></span>                                        |
| <span data-ttu-id="8e705-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8e705-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e705-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8e705-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8e705-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e705-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8e705-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e705-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8e705-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e705-240">Search-Flags</span></span>           | <span data-ttu-id="8e705-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e705-241">0x00000000</span></span>                                   |
| <span data-ttu-id="8e705-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e705-242">System-Flags</span></span>           | <span data-ttu-id="8e705-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e705-243">0x00000010</span></span>                                   |
| <span data-ttu-id="8e705-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8e705-244">Classes used in</span></span>        | [<span data-ttu-id="8e705-245">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="8e705-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8e705-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8e705-246">Windows Server 2012</span></span>



| <span data-ttu-id="8e705-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e705-247">Entry</span></span> | <span data-ttu-id="8e705-248">Wert</span><span class="sxs-lookup"><span data-stu-id="8e705-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8e705-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8e705-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8e705-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e705-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8e705-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e705-251">System-Only</span></span>            | <span data-ttu-id="8e705-252">False</span><span class="sxs-lookup"><span data-stu-id="8e705-252">False</span></span>                                        |
| <span data-ttu-id="8e705-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8e705-253">Is-Single-Valued</span></span>       | <span data-ttu-id="8e705-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="8e705-254">True</span></span>                                         |
| <span data-ttu-id="8e705-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8e705-255">Is Indexed</span></span>             | <span data-ttu-id="8e705-256">False</span><span class="sxs-lookup"><span data-stu-id="8e705-256">False</span></span>                                        |
| <span data-ttu-id="8e705-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8e705-257">In Global Catalog</span></span>      | <span data-ttu-id="8e705-258">False</span><span class="sxs-lookup"><span data-stu-id="8e705-258">False</span></span>                                        |
| <span data-ttu-id="8e705-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8e705-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e705-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8e705-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8e705-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e705-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8e705-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e705-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8e705-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e705-263">Search-Flags</span></span>           | <span data-ttu-id="8e705-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e705-264">0x00000000</span></span>                                   |
| <span data-ttu-id="8e705-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e705-265">System-Flags</span></span>           | <span data-ttu-id="8e705-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e705-266">0x00000010</span></span>                                   |
| <span data-ttu-id="8e705-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8e705-267">Classes used in</span></span>        | [<span data-ttu-id="8e705-268">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="8e705-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





