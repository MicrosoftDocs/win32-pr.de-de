---
title: Builtin-Erstellungszeit Attribut
description: Das Builtin-Creation-time-Attribut wird zur Unterstützung der Replikation in Windows NT 4,0-Domänen verwendet.
ms.assetid: b3da9913-8c7b-481b-ae47-6b124544f1e2
ms.tgt_platform: multiple
keywords:
- Builtin-Erstellungszeit Attribut AD-Schema
- builtincreationtime-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Builtin-Creation-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54d5b6d37ee0242999afd47415cb067abe26e7fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859918"
---
# <a name="builtin-creation-time-attribute"></a><span data-ttu-id="38022-105">Builtin-Erstellungszeit Attribut</span><span class="sxs-lookup"><span data-stu-id="38022-105">Builtin-Creation-Time attribute</span></span>

<span data-ttu-id="38022-106">Das **BuiltIn-Creation-time** -Attribut wird zur Unterstützung der Replikation in Windows NT 4,0-Domänen verwendet.</span><span class="sxs-lookup"><span data-stu-id="38022-106">The **Builtin-Creation-Time** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="38022-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38022-107">Entry</span></span> | <span data-ttu-id="38022-108">Wert</span><span class="sxs-lookup"><span data-stu-id="38022-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="38022-109">CN</span><span class="sxs-lookup"><span data-stu-id="38022-109">CN</span></span>                | <span data-ttu-id="38022-110">Builtin-Erstellungszeit</span><span class="sxs-lookup"><span data-stu-id="38022-110">Builtin-Creation-Time</span></span>                |
| <span data-ttu-id="38022-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="38022-111">Ldap-Display-Name</span></span> | <span data-ttu-id="38022-112">builtincreationtime</span><span class="sxs-lookup"><span data-stu-id="38022-112">builtinCreationTime</span></span>                  |
| <span data-ttu-id="38022-113">Size</span><span class="sxs-lookup"><span data-stu-id="38022-113">Size</span></span>              | <span data-ttu-id="38022-114">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="38022-114">8 bytes</span></span>                              |
| <span data-ttu-id="38022-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="38022-115">Update Privilege</span></span>  | <span data-ttu-id="38022-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="38022-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="38022-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="38022-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="38022-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="38022-118">Attribute-Id</span></span>      | <span data-ttu-id="38022-119">1.2.840.113556.1.4.13</span><span class="sxs-lookup"><span data-stu-id="38022-119">1.2.840.113556.1.4.13</span></span>                |
| <span data-ttu-id="38022-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="38022-120">System-Id-Guid</span></span>    | <span data-ttu-id="38022-121">bf96792f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="38022-121">bf96792f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="38022-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="38022-122">Syntax</span></span>            | [<span data-ttu-id="38022-123">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="38022-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="38022-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="38022-124">Implementations</span></span>

-   [<span data-ttu-id="38022-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="38022-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="38022-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="38022-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="38022-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="38022-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="38022-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="38022-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="38022-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="38022-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="38022-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="38022-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="38022-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="38022-131">Windows 2000 Server</span></span>



| <span data-ttu-id="38022-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38022-132">Entry</span></span> | <span data-ttu-id="38022-133">Wert</span><span class="sxs-lookup"><span data-stu-id="38022-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="38022-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="38022-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="38022-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38022-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="38022-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="38022-136">System-Only</span></span>            | <span data-ttu-id="38022-137">False</span><span class="sxs-lookup"><span data-stu-id="38022-137">False</span></span>                                        |
| <span data-ttu-id="38022-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="38022-138">Is-Single-Valued</span></span>       | <span data-ttu-id="38022-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="38022-139">True</span></span>                                         |
| <span data-ttu-id="38022-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="38022-140">Is Indexed</span></span>             | <span data-ttu-id="38022-141">False</span><span class="sxs-lookup"><span data-stu-id="38022-141">False</span></span>                                        |
| <span data-ttu-id="38022-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="38022-142">In Global Catalog</span></span>      | <span data-ttu-id="38022-143">False</span><span class="sxs-lookup"><span data-stu-id="38022-143">False</span></span>                                        |
| <span data-ttu-id="38022-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="38022-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="38022-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="38022-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="38022-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38022-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="38022-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38022-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="38022-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38022-148">Search-Flags</span></span>           | <span data-ttu-id="38022-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38022-149">0x00000000</span></span>                                   |
| <span data-ttu-id="38022-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38022-150">System-Flags</span></span>           | <span data-ttu-id="38022-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38022-151">0x00000010</span></span>                                   |
| <span data-ttu-id="38022-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="38022-152">Classes used in</span></span>        | [<span data-ttu-id="38022-153">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="38022-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="38022-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="38022-154">Windows Server 2003</span></span>



| <span data-ttu-id="38022-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38022-155">Entry</span></span> | <span data-ttu-id="38022-156">Wert</span><span class="sxs-lookup"><span data-stu-id="38022-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="38022-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="38022-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="38022-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38022-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="38022-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="38022-159">System-Only</span></span>            | <span data-ttu-id="38022-160">False</span><span class="sxs-lookup"><span data-stu-id="38022-160">False</span></span>                                        |
| <span data-ttu-id="38022-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="38022-161">Is-Single-Valued</span></span>       | <span data-ttu-id="38022-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="38022-162">True</span></span>                                         |
| <span data-ttu-id="38022-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="38022-163">Is Indexed</span></span>             | <span data-ttu-id="38022-164">False</span><span class="sxs-lookup"><span data-stu-id="38022-164">False</span></span>                                        |
| <span data-ttu-id="38022-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="38022-165">In Global Catalog</span></span>      | <span data-ttu-id="38022-166">False</span><span class="sxs-lookup"><span data-stu-id="38022-166">False</span></span>                                        |
| <span data-ttu-id="38022-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="38022-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="38022-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="38022-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="38022-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38022-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="38022-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38022-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="38022-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38022-171">Search-Flags</span></span>           | <span data-ttu-id="38022-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38022-172">0x00000000</span></span>                                   |
| <span data-ttu-id="38022-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38022-173">System-Flags</span></span>           | <span data-ttu-id="38022-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38022-174">0x00000010</span></span>                                   |
| <span data-ttu-id="38022-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="38022-175">Classes used in</span></span>        | [<span data-ttu-id="38022-176">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="38022-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="38022-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="38022-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="38022-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38022-178">Entry</span></span> | <span data-ttu-id="38022-179">Wert</span><span class="sxs-lookup"><span data-stu-id="38022-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="38022-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="38022-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="38022-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38022-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="38022-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="38022-182">System-Only</span></span>            | <span data-ttu-id="38022-183">False</span><span class="sxs-lookup"><span data-stu-id="38022-183">False</span></span>                                        |
| <span data-ttu-id="38022-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="38022-184">Is-Single-Valued</span></span>       | <span data-ttu-id="38022-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="38022-185">True</span></span>                                         |
| <span data-ttu-id="38022-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="38022-186">Is Indexed</span></span>             | <span data-ttu-id="38022-187">False</span><span class="sxs-lookup"><span data-stu-id="38022-187">False</span></span>                                        |
| <span data-ttu-id="38022-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="38022-188">In Global Catalog</span></span>      | <span data-ttu-id="38022-189">False</span><span class="sxs-lookup"><span data-stu-id="38022-189">False</span></span>                                        |
| <span data-ttu-id="38022-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="38022-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="38022-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="38022-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="38022-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38022-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="38022-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38022-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="38022-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38022-194">Search-Flags</span></span>           | <span data-ttu-id="38022-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38022-195">0x00000000</span></span>                                   |
| <span data-ttu-id="38022-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38022-196">System-Flags</span></span>           | <span data-ttu-id="38022-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38022-197">0x00000010</span></span>                                   |
| <span data-ttu-id="38022-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="38022-198">Classes used in</span></span>        | [<span data-ttu-id="38022-199">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="38022-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="38022-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38022-200">Windows Server 2008</span></span>



| <span data-ttu-id="38022-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38022-201">Entry</span></span> | <span data-ttu-id="38022-202">Wert</span><span class="sxs-lookup"><span data-stu-id="38022-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="38022-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="38022-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="38022-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38022-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="38022-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="38022-205">System-Only</span></span>            | <span data-ttu-id="38022-206">False</span><span class="sxs-lookup"><span data-stu-id="38022-206">False</span></span>                                        |
| <span data-ttu-id="38022-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="38022-207">Is-Single-Valued</span></span>       | <span data-ttu-id="38022-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="38022-208">True</span></span>                                         |
| <span data-ttu-id="38022-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="38022-209">Is Indexed</span></span>             | <span data-ttu-id="38022-210">False</span><span class="sxs-lookup"><span data-stu-id="38022-210">False</span></span>                                        |
| <span data-ttu-id="38022-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="38022-211">In Global Catalog</span></span>      | <span data-ttu-id="38022-212">False</span><span class="sxs-lookup"><span data-stu-id="38022-212">False</span></span>                                        |
| <span data-ttu-id="38022-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="38022-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="38022-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="38022-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="38022-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38022-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="38022-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38022-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="38022-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38022-217">Search-Flags</span></span>           | <span data-ttu-id="38022-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38022-218">0x00000000</span></span>                                   |
| <span data-ttu-id="38022-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38022-219">System-Flags</span></span>           | <span data-ttu-id="38022-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38022-220">0x00000010</span></span>                                   |
| <span data-ttu-id="38022-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="38022-221">Classes used in</span></span>        | [<span data-ttu-id="38022-222">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="38022-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="38022-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="38022-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="38022-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38022-224">Entry</span></span> | <span data-ttu-id="38022-225">Wert</span><span class="sxs-lookup"><span data-stu-id="38022-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="38022-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="38022-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="38022-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38022-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="38022-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="38022-228">System-Only</span></span>            | <span data-ttu-id="38022-229">False</span><span class="sxs-lookup"><span data-stu-id="38022-229">False</span></span>                                        |
| <span data-ttu-id="38022-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="38022-230">Is-Single-Valued</span></span>       | <span data-ttu-id="38022-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="38022-231">True</span></span>                                         |
| <span data-ttu-id="38022-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="38022-232">Is Indexed</span></span>             | <span data-ttu-id="38022-233">False</span><span class="sxs-lookup"><span data-stu-id="38022-233">False</span></span>                                        |
| <span data-ttu-id="38022-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="38022-234">In Global Catalog</span></span>      | <span data-ttu-id="38022-235">False</span><span class="sxs-lookup"><span data-stu-id="38022-235">False</span></span>                                        |
| <span data-ttu-id="38022-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="38022-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="38022-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="38022-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="38022-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38022-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="38022-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38022-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="38022-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38022-240">Search-Flags</span></span>           | <span data-ttu-id="38022-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38022-241">0x00000000</span></span>                                   |
| <span data-ttu-id="38022-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38022-242">System-Flags</span></span>           | <span data-ttu-id="38022-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38022-243">0x00000010</span></span>                                   |
| <span data-ttu-id="38022-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="38022-244">Classes used in</span></span>        | [<span data-ttu-id="38022-245">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="38022-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="38022-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="38022-246">Windows Server 2012</span></span>



| <span data-ttu-id="38022-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38022-247">Entry</span></span> | <span data-ttu-id="38022-248">Wert</span><span class="sxs-lookup"><span data-stu-id="38022-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="38022-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="38022-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="38022-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38022-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="38022-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="38022-251">System-Only</span></span>            | <span data-ttu-id="38022-252">False</span><span class="sxs-lookup"><span data-stu-id="38022-252">False</span></span>                                        |
| <span data-ttu-id="38022-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="38022-253">Is-Single-Valued</span></span>       | <span data-ttu-id="38022-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="38022-254">True</span></span>                                         |
| <span data-ttu-id="38022-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="38022-255">Is Indexed</span></span>             | <span data-ttu-id="38022-256">False</span><span class="sxs-lookup"><span data-stu-id="38022-256">False</span></span>                                        |
| <span data-ttu-id="38022-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="38022-257">In Global Catalog</span></span>      | <span data-ttu-id="38022-258">False</span><span class="sxs-lookup"><span data-stu-id="38022-258">False</span></span>                                        |
| <span data-ttu-id="38022-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="38022-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="38022-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="38022-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="38022-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38022-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="38022-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38022-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="38022-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38022-263">Search-Flags</span></span>           | <span data-ttu-id="38022-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38022-264">0x00000000</span></span>                                   |
| <span data-ttu-id="38022-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38022-265">System-Flags</span></span>           | <span data-ttu-id="38022-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38022-266">0x00000010</span></span>                                   |
| <span data-ttu-id="38022-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="38022-267">Classes used in</span></span>        | [<span data-ttu-id="38022-268">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="38022-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





