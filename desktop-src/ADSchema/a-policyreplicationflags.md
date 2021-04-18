---
title: Policy-Replication-Flags-Attribut
description: Bestimmt, welche LSA-Eigenschaften auf Clients repliziert werden.
ms.assetid: 2dadd659-c834-4105-ab3e-8ce0b8811212
ms.tgt_platform: multiple
keywords:
- Richtlinien Replikations-Flags-Attribut AD-Schema
- policyreplicationflags-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Policy-Replication-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42da6509662d11c4a069ba58dff5f648e7ab2261
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344519"
---
# <a name="policy-replication-flags-attribute"></a><span data-ttu-id="64edd-105">Policy-Replication-Flags-Attribut</span><span class="sxs-lookup"><span data-stu-id="64edd-105">Policy-Replication-Flags attribute</span></span>

<span data-ttu-id="64edd-106">Bestimmt, welche LSA-Eigenschaften auf Clients repliziert werden.</span><span class="sxs-lookup"><span data-stu-id="64edd-106">Determines which LSA properties are replicated to clients.</span></span>



| <span data-ttu-id="64edd-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64edd-107">Entry</span></span> | <span data-ttu-id="64edd-108">Wert</span><span class="sxs-lookup"><span data-stu-id="64edd-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="64edd-109">CN</span><span class="sxs-lookup"><span data-stu-id="64edd-109">CN</span></span>                | <span data-ttu-id="64edd-110">Richtlinienreplizierung: Flags</span><span class="sxs-lookup"><span data-stu-id="64edd-110">Policy-Replication-Flags</span></span>             |
| <span data-ttu-id="64edd-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="64edd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="64edd-112">policyreplicationflags</span><span class="sxs-lookup"><span data-stu-id="64edd-112">policyReplicationFlags</span></span>               |
| <span data-ttu-id="64edd-113">Size</span><span class="sxs-lookup"><span data-stu-id="64edd-113">Size</span></span>              | <span data-ttu-id="64edd-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="64edd-114">4 bytes</span></span>                              |
| <span data-ttu-id="64edd-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="64edd-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="64edd-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="64edd-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="64edd-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="64edd-117">Attribute-Id</span></span>      | <span data-ttu-id="64edd-118">1.2.840.113556.1.4.633</span><span class="sxs-lookup"><span data-stu-id="64edd-118">1.2.840.113556.1.4.633</span></span>               |
| <span data-ttu-id="64edd-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="64edd-119">System-Id-Guid</span></span>    | <span data-ttu-id="64edd-120">19405b96-3cfa-11d1-a9c0-0000f 80367c1</span><span class="sxs-lookup"><span data-stu-id="64edd-120">19405b96-3cfa-11d1-a9c0-0000f80367c1</span></span> |
| <span data-ttu-id="64edd-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="64edd-121">Syntax</span></span>            | [<span data-ttu-id="64edd-122">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="64edd-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="64edd-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="64edd-123">Implementations</span></span>

-   [<span data-ttu-id="64edd-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="64edd-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="64edd-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="64edd-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="64edd-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="64edd-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="64edd-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="64edd-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="64edd-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="64edd-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="64edd-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="64edd-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="64edd-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="64edd-130">Windows 2000 Server</span></span>



| <span data-ttu-id="64edd-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64edd-131">Entry</span></span> | <span data-ttu-id="64edd-132">Wert</span><span class="sxs-lookup"><span data-stu-id="64edd-132">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="64edd-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="64edd-133">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="64edd-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64edd-134">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="64edd-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="64edd-135">System-Only</span></span>            | <span data-ttu-id="64edd-136">False</span><span class="sxs-lookup"><span data-stu-id="64edd-136">False</span></span>                                     |
| <span data-ttu-id="64edd-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="64edd-137">Is-Single-Valued</span></span>       | <span data-ttu-id="64edd-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="64edd-138">True</span></span>                                      |
| <span data-ttu-id="64edd-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="64edd-139">Is Indexed</span></span>             | <span data-ttu-id="64edd-140">False</span><span class="sxs-lookup"><span data-stu-id="64edd-140">False</span></span>                                     |
| <span data-ttu-id="64edd-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="64edd-141">In Global Catalog</span></span>      | <span data-ttu-id="64edd-142">False</span><span class="sxs-lookup"><span data-stu-id="64edd-142">False</span></span>                                     |
| <span data-ttu-id="64edd-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64edd-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="64edd-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="64edd-144">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="64edd-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64edd-145">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="64edd-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64edd-146">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="64edd-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64edd-147">Search-Flags</span></span>           | <span data-ttu-id="64edd-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64edd-148">0x00000000</span></span>                                |
| <span data-ttu-id="64edd-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64edd-149">System-Flags</span></span>           | <span data-ttu-id="64edd-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64edd-150">0x00000010</span></span>                                |
| <span data-ttu-id="64edd-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="64edd-151">Classes used in</span></span>        | [<span data-ttu-id="64edd-152">**Computer**</span><span class="sxs-lookup"><span data-stu-id="64edd-152">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="64edd-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="64edd-153">Windows Server 2003</span></span>



| <span data-ttu-id="64edd-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64edd-154">Entry</span></span> | <span data-ttu-id="64edd-155">Wert</span><span class="sxs-lookup"><span data-stu-id="64edd-155">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="64edd-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="64edd-156">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="64edd-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64edd-157">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="64edd-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="64edd-158">System-Only</span></span>            | <span data-ttu-id="64edd-159">False</span><span class="sxs-lookup"><span data-stu-id="64edd-159">False</span></span>                                     |
| <span data-ttu-id="64edd-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="64edd-160">Is-Single-Valued</span></span>       | <span data-ttu-id="64edd-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="64edd-161">True</span></span>                                      |
| <span data-ttu-id="64edd-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="64edd-162">Is Indexed</span></span>             | <span data-ttu-id="64edd-163">False</span><span class="sxs-lookup"><span data-stu-id="64edd-163">False</span></span>                                     |
| <span data-ttu-id="64edd-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="64edd-164">In Global Catalog</span></span>      | <span data-ttu-id="64edd-165">False</span><span class="sxs-lookup"><span data-stu-id="64edd-165">False</span></span>                                     |
| <span data-ttu-id="64edd-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64edd-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="64edd-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="64edd-167">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="64edd-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64edd-168">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="64edd-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64edd-169">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="64edd-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64edd-170">Search-Flags</span></span>           | <span data-ttu-id="64edd-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64edd-171">0x00000000</span></span>                                |
| <span data-ttu-id="64edd-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64edd-172">System-Flags</span></span>           | <span data-ttu-id="64edd-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64edd-173">0x00000010</span></span>                                |
| <span data-ttu-id="64edd-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="64edd-174">Classes used in</span></span>        | [<span data-ttu-id="64edd-175">**Computer**</span><span class="sxs-lookup"><span data-stu-id="64edd-175">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="64edd-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="64edd-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="64edd-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64edd-177">Entry</span></span> | <span data-ttu-id="64edd-178">Wert</span><span class="sxs-lookup"><span data-stu-id="64edd-178">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="64edd-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="64edd-179">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="64edd-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64edd-180">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="64edd-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="64edd-181">System-Only</span></span>            | <span data-ttu-id="64edd-182">False</span><span class="sxs-lookup"><span data-stu-id="64edd-182">False</span></span>                                     |
| <span data-ttu-id="64edd-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="64edd-183">Is-Single-Valued</span></span>       | <span data-ttu-id="64edd-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="64edd-184">True</span></span>                                      |
| <span data-ttu-id="64edd-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="64edd-185">Is Indexed</span></span>             | <span data-ttu-id="64edd-186">False</span><span class="sxs-lookup"><span data-stu-id="64edd-186">False</span></span>                                     |
| <span data-ttu-id="64edd-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="64edd-187">In Global Catalog</span></span>      | <span data-ttu-id="64edd-188">False</span><span class="sxs-lookup"><span data-stu-id="64edd-188">False</span></span>                                     |
| <span data-ttu-id="64edd-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64edd-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="64edd-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="64edd-190">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="64edd-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64edd-191">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="64edd-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64edd-192">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="64edd-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64edd-193">Search-Flags</span></span>           | <span data-ttu-id="64edd-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64edd-194">0x00000000</span></span>                                |
| <span data-ttu-id="64edd-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64edd-195">System-Flags</span></span>           | <span data-ttu-id="64edd-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64edd-196">0x00000010</span></span>                                |
| <span data-ttu-id="64edd-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="64edd-197">Classes used in</span></span>        | [<span data-ttu-id="64edd-198">**Computer**</span><span class="sxs-lookup"><span data-stu-id="64edd-198">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="64edd-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64edd-199">Windows Server 2008</span></span>



| <span data-ttu-id="64edd-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64edd-200">Entry</span></span> | <span data-ttu-id="64edd-201">Wert</span><span class="sxs-lookup"><span data-stu-id="64edd-201">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="64edd-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="64edd-202">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="64edd-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64edd-203">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="64edd-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="64edd-204">System-Only</span></span>            | <span data-ttu-id="64edd-205">False</span><span class="sxs-lookup"><span data-stu-id="64edd-205">False</span></span>                                     |
| <span data-ttu-id="64edd-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="64edd-206">Is-Single-Valued</span></span>       | <span data-ttu-id="64edd-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="64edd-207">True</span></span>                                      |
| <span data-ttu-id="64edd-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="64edd-208">Is Indexed</span></span>             | <span data-ttu-id="64edd-209">False</span><span class="sxs-lookup"><span data-stu-id="64edd-209">False</span></span>                                     |
| <span data-ttu-id="64edd-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="64edd-210">In Global Catalog</span></span>      | <span data-ttu-id="64edd-211">False</span><span class="sxs-lookup"><span data-stu-id="64edd-211">False</span></span>                                     |
| <span data-ttu-id="64edd-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64edd-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="64edd-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="64edd-213">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="64edd-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64edd-214">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="64edd-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64edd-215">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="64edd-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64edd-216">Search-Flags</span></span>           | <span data-ttu-id="64edd-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64edd-217">0x00000000</span></span>                                |
| <span data-ttu-id="64edd-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64edd-218">System-Flags</span></span>           | <span data-ttu-id="64edd-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64edd-219">0x00000010</span></span>                                |
| <span data-ttu-id="64edd-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="64edd-220">Classes used in</span></span>        | [<span data-ttu-id="64edd-221">**Computer**</span><span class="sxs-lookup"><span data-stu-id="64edd-221">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="64edd-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="64edd-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="64edd-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64edd-223">Entry</span></span> | <span data-ttu-id="64edd-224">Wert</span><span class="sxs-lookup"><span data-stu-id="64edd-224">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="64edd-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="64edd-225">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="64edd-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64edd-226">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="64edd-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="64edd-227">System-Only</span></span>            | <span data-ttu-id="64edd-228">False</span><span class="sxs-lookup"><span data-stu-id="64edd-228">False</span></span>                                     |
| <span data-ttu-id="64edd-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="64edd-229">Is-Single-Valued</span></span>       | <span data-ttu-id="64edd-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="64edd-230">True</span></span>                                      |
| <span data-ttu-id="64edd-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="64edd-231">Is Indexed</span></span>             | <span data-ttu-id="64edd-232">False</span><span class="sxs-lookup"><span data-stu-id="64edd-232">False</span></span>                                     |
| <span data-ttu-id="64edd-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="64edd-233">In Global Catalog</span></span>      | <span data-ttu-id="64edd-234">False</span><span class="sxs-lookup"><span data-stu-id="64edd-234">False</span></span>                                     |
| <span data-ttu-id="64edd-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64edd-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="64edd-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="64edd-236">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="64edd-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64edd-237">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="64edd-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64edd-238">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="64edd-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64edd-239">Search-Flags</span></span>           | <span data-ttu-id="64edd-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64edd-240">0x00000000</span></span>                                |
| <span data-ttu-id="64edd-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64edd-241">System-Flags</span></span>           | <span data-ttu-id="64edd-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64edd-242">0x00000010</span></span>                                |
| <span data-ttu-id="64edd-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="64edd-243">Classes used in</span></span>        | [<span data-ttu-id="64edd-244">**Computer**</span><span class="sxs-lookup"><span data-stu-id="64edd-244">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="64edd-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="64edd-245">Windows Server 2012</span></span>



| <span data-ttu-id="64edd-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64edd-246">Entry</span></span> | <span data-ttu-id="64edd-247">Wert</span><span class="sxs-lookup"><span data-stu-id="64edd-247">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="64edd-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="64edd-248">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="64edd-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64edd-249">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="64edd-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="64edd-250">System-Only</span></span>            | <span data-ttu-id="64edd-251">False</span><span class="sxs-lookup"><span data-stu-id="64edd-251">False</span></span>                                     |
| <span data-ttu-id="64edd-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="64edd-252">Is-Single-Valued</span></span>       | <span data-ttu-id="64edd-253">Richtig</span><span class="sxs-lookup"><span data-stu-id="64edd-253">True</span></span>                                      |
| <span data-ttu-id="64edd-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="64edd-254">Is Indexed</span></span>             | <span data-ttu-id="64edd-255">False</span><span class="sxs-lookup"><span data-stu-id="64edd-255">False</span></span>                                     |
| <span data-ttu-id="64edd-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="64edd-256">In Global Catalog</span></span>      | <span data-ttu-id="64edd-257">False</span><span class="sxs-lookup"><span data-stu-id="64edd-257">False</span></span>                                     |
| <span data-ttu-id="64edd-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64edd-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="64edd-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="64edd-259">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="64edd-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64edd-260">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="64edd-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64edd-261">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="64edd-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64edd-262">Search-Flags</span></span>           | <span data-ttu-id="64edd-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64edd-263">0x00000000</span></span>                                |
| <span data-ttu-id="64edd-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64edd-264">System-Flags</span></span>           | <span data-ttu-id="64edd-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64edd-265">0x00000010</span></span>                                |
| <span data-ttu-id="64edd-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="64edd-266">Classes used in</span></span>        | [<span data-ttu-id="64edd-267">**Computer**</span><span class="sxs-lookup"><span data-stu-id="64edd-267">**Computer**</span></span>](c-computer.md)<br/> |



 

 





