---
title: Trust-Type-Attribut
description: Der Typ der Vertrauensstellung, z. b. Windows NT oder mit.
ms.assetid: ad3640cd-d634-4ec1-8be8-1fb8272e4b23
ms.tgt_platform: multiple
keywords:
- AD-Schema für Trust-Type-Attribut
- Trust Type-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Trust-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b8a8f59f7df976f968bb4f2915e667a06e95bb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957437"
---
# <a name="trust-type-attribute"></a><span data-ttu-id="6964c-105">Trust-Type-Attribut</span><span class="sxs-lookup"><span data-stu-id="6964c-105">Trust-Type attribute</span></span>

<span data-ttu-id="6964c-106">Der Typ der Vertrauensstellung, z. b. Windows NT oder mit.</span><span class="sxs-lookup"><span data-stu-id="6964c-106">The type of trust, for example, Windows NT or MIT.</span></span>



| <span data-ttu-id="6964c-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6964c-107">Entry</span></span> | <span data-ttu-id="6964c-108">Wert</span><span class="sxs-lookup"><span data-stu-id="6964c-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6964c-109">CN</span><span class="sxs-lookup"><span data-stu-id="6964c-109">CN</span></span>                | <span data-ttu-id="6964c-110">Trust-Type</span><span class="sxs-lookup"><span data-stu-id="6964c-110">Trust-Type</span></span>                           |
| <span data-ttu-id="6964c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6964c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6964c-112">trustType</span><span class="sxs-lookup"><span data-stu-id="6964c-112">trustType</span></span>                            |
| <span data-ttu-id="6964c-113">Size</span><span class="sxs-lookup"><span data-stu-id="6964c-113">Size</span></span>              | <span data-ttu-id="6964c-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="6964c-114">4 bytes</span></span>                              |
| <span data-ttu-id="6964c-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="6964c-115">Update Privilege</span></span>  | <span data-ttu-id="6964c-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6964c-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="6964c-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="6964c-117">Update Frequency</span></span>  | <span data-ttu-id="6964c-118">Wenn eine neue Vertrauensstellung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6964c-118">When a new trust is created.</span></span>         |
| <span data-ttu-id="6964c-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6964c-119">Attribute-Id</span></span>      | <span data-ttu-id="6964c-120">1.2.840.113556.1.4.136</span><span class="sxs-lookup"><span data-stu-id="6964c-120">1.2.840.113556.1.4.136</span></span>               |
| <span data-ttu-id="6964c-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6964c-121">System-Id-Guid</span></span>    | <span data-ttu-id="6964c-122">bf967a60-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6964c-122">bf967a60-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="6964c-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="6964c-123">Syntax</span></span>            | [<span data-ttu-id="6964c-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="6964c-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="6964c-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="6964c-125">Implementations</span></span>

-   [<span data-ttu-id="6964c-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6964c-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6964c-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6964c-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6964c-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6964c-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6964c-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6964c-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6964c-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6964c-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6964c-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6964c-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6964c-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6964c-132">Windows 2000 Server</span></span>



| <span data-ttu-id="6964c-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6964c-133">Entry</span></span> | <span data-ttu-id="6964c-134">Wert</span><span class="sxs-lookup"><span data-stu-id="6964c-134">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="6964c-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6964c-135">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6964c-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6964c-136">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6964c-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="6964c-137">System-Only</span></span>            | <span data-ttu-id="6964c-138">False</span><span class="sxs-lookup"><span data-stu-id="6964c-138">False</span></span>                                                |
| <span data-ttu-id="6964c-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6964c-139">Is-Single-Valued</span></span>       | <span data-ttu-id="6964c-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="6964c-140">True</span></span>                                                 |
| <span data-ttu-id="6964c-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6964c-141">Is Indexed</span></span>             | <span data-ttu-id="6964c-142">False</span><span class="sxs-lookup"><span data-stu-id="6964c-142">False</span></span>                                                |
| <span data-ttu-id="6964c-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6964c-143">In Global Catalog</span></span>      | <span data-ttu-id="6964c-144">False</span><span class="sxs-lookup"><span data-stu-id="6964c-144">False</span></span>                                                |
| <span data-ttu-id="6964c-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6964c-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="6964c-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6964c-146">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="6964c-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6964c-147">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="6964c-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6964c-148">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="6964c-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6964c-149">Search-Flags</span></span>           | <span data-ttu-id="6964c-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6964c-150">0x00000000</span></span>                                           |
| <span data-ttu-id="6964c-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6964c-151">System-Flags</span></span>           | <span data-ttu-id="6964c-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6964c-152">0x00000010</span></span>                                           |
| <span data-ttu-id="6964c-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6964c-153">Classes used in</span></span>        | [<span data-ttu-id="6964c-154">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="6964c-154">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6964c-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6964c-155">Windows Server 2003</span></span>



| <span data-ttu-id="6964c-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6964c-156">Entry</span></span> | <span data-ttu-id="6964c-157">Wert</span><span class="sxs-lookup"><span data-stu-id="6964c-157">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="6964c-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6964c-158">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6964c-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6964c-159">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6964c-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="6964c-160">System-Only</span></span>            | <span data-ttu-id="6964c-161">False</span><span class="sxs-lookup"><span data-stu-id="6964c-161">False</span></span>                                                |
| <span data-ttu-id="6964c-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6964c-162">Is-Single-Valued</span></span>       | <span data-ttu-id="6964c-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="6964c-163">True</span></span>                                                 |
| <span data-ttu-id="6964c-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6964c-164">Is Indexed</span></span>             | <span data-ttu-id="6964c-165">False</span><span class="sxs-lookup"><span data-stu-id="6964c-165">False</span></span>                                                |
| <span data-ttu-id="6964c-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6964c-166">In Global Catalog</span></span>      | <span data-ttu-id="6964c-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="6964c-167">True</span></span>                                                 |
| <span data-ttu-id="6964c-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6964c-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="6964c-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6964c-169">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="6964c-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6964c-170">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="6964c-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6964c-171">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="6964c-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6964c-172">Search-Flags</span></span>           | <span data-ttu-id="6964c-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6964c-173">0x00000000</span></span>                                           |
| <span data-ttu-id="6964c-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6964c-174">System-Flags</span></span>           | <span data-ttu-id="6964c-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6964c-175">0x00000010</span></span>                                           |
| <span data-ttu-id="6964c-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6964c-176">Classes used in</span></span>        | [<span data-ttu-id="6964c-177">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="6964c-177">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6964c-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6964c-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6964c-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6964c-179">Entry</span></span> | <span data-ttu-id="6964c-180">Wert</span><span class="sxs-lookup"><span data-stu-id="6964c-180">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="6964c-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6964c-181">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6964c-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6964c-182">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6964c-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="6964c-183">System-Only</span></span>            | <span data-ttu-id="6964c-184">False</span><span class="sxs-lookup"><span data-stu-id="6964c-184">False</span></span>                                                |
| <span data-ttu-id="6964c-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6964c-185">Is-Single-Valued</span></span>       | <span data-ttu-id="6964c-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="6964c-186">True</span></span>                                                 |
| <span data-ttu-id="6964c-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6964c-187">Is Indexed</span></span>             | <span data-ttu-id="6964c-188">False</span><span class="sxs-lookup"><span data-stu-id="6964c-188">False</span></span>                                                |
| <span data-ttu-id="6964c-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6964c-189">In Global Catalog</span></span>      | <span data-ttu-id="6964c-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="6964c-190">True</span></span>                                                 |
| <span data-ttu-id="6964c-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6964c-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="6964c-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6964c-192">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="6964c-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6964c-193">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="6964c-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6964c-194">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="6964c-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6964c-195">Search-Flags</span></span>           | <span data-ttu-id="6964c-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6964c-196">0x00000000</span></span>                                           |
| <span data-ttu-id="6964c-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6964c-197">System-Flags</span></span>           | <span data-ttu-id="6964c-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6964c-198">0x00000010</span></span>                                           |
| <span data-ttu-id="6964c-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6964c-199">Classes used in</span></span>        | [<span data-ttu-id="6964c-200">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="6964c-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6964c-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6964c-201">Windows Server 2008</span></span>



| <span data-ttu-id="6964c-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6964c-202">Entry</span></span> | <span data-ttu-id="6964c-203">Wert</span><span class="sxs-lookup"><span data-stu-id="6964c-203">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="6964c-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6964c-204">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6964c-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6964c-205">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6964c-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="6964c-206">System-Only</span></span>            | <span data-ttu-id="6964c-207">False</span><span class="sxs-lookup"><span data-stu-id="6964c-207">False</span></span>                                                |
| <span data-ttu-id="6964c-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6964c-208">Is-Single-Valued</span></span>       | <span data-ttu-id="6964c-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="6964c-209">True</span></span>                                                 |
| <span data-ttu-id="6964c-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6964c-210">Is Indexed</span></span>             | <span data-ttu-id="6964c-211">False</span><span class="sxs-lookup"><span data-stu-id="6964c-211">False</span></span>                                                |
| <span data-ttu-id="6964c-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6964c-212">In Global Catalog</span></span>      | <span data-ttu-id="6964c-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="6964c-213">True</span></span>                                                 |
| <span data-ttu-id="6964c-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6964c-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="6964c-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6964c-215">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="6964c-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6964c-216">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="6964c-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6964c-217">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="6964c-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6964c-218">Search-Flags</span></span>           | <span data-ttu-id="6964c-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6964c-219">0x00000000</span></span>                                           |
| <span data-ttu-id="6964c-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6964c-220">System-Flags</span></span>           | <span data-ttu-id="6964c-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6964c-221">0x00000010</span></span>                                           |
| <span data-ttu-id="6964c-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6964c-222">Classes used in</span></span>        | [<span data-ttu-id="6964c-223">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="6964c-223">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6964c-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6964c-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6964c-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6964c-225">Entry</span></span> | <span data-ttu-id="6964c-226">Wert</span><span class="sxs-lookup"><span data-stu-id="6964c-226">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="6964c-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6964c-227">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6964c-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6964c-228">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6964c-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="6964c-229">System-Only</span></span>            | <span data-ttu-id="6964c-230">False</span><span class="sxs-lookup"><span data-stu-id="6964c-230">False</span></span>                                                |
| <span data-ttu-id="6964c-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6964c-231">Is-Single-Valued</span></span>       | <span data-ttu-id="6964c-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="6964c-232">True</span></span>                                                 |
| <span data-ttu-id="6964c-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6964c-233">Is Indexed</span></span>             | <span data-ttu-id="6964c-234">False</span><span class="sxs-lookup"><span data-stu-id="6964c-234">False</span></span>                                                |
| <span data-ttu-id="6964c-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6964c-235">In Global Catalog</span></span>      | <span data-ttu-id="6964c-236">Richtig</span><span class="sxs-lookup"><span data-stu-id="6964c-236">True</span></span>                                                 |
| <span data-ttu-id="6964c-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6964c-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="6964c-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6964c-238">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="6964c-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6964c-239">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="6964c-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6964c-240">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="6964c-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6964c-241">Search-Flags</span></span>           | <span data-ttu-id="6964c-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6964c-242">0x00000000</span></span>                                           |
| <span data-ttu-id="6964c-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6964c-243">System-Flags</span></span>           | <span data-ttu-id="6964c-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6964c-244">0x00000010</span></span>                                           |
| <span data-ttu-id="6964c-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6964c-245">Classes used in</span></span>        | [<span data-ttu-id="6964c-246">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="6964c-246">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6964c-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6964c-247">Windows Server 2012</span></span>



| <span data-ttu-id="6964c-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6964c-248">Entry</span></span> | <span data-ttu-id="6964c-249">Wert</span><span class="sxs-lookup"><span data-stu-id="6964c-249">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="6964c-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6964c-250">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6964c-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6964c-251">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6964c-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="6964c-252">System-Only</span></span>            | <span data-ttu-id="6964c-253">False</span><span class="sxs-lookup"><span data-stu-id="6964c-253">False</span></span>                                                |
| <span data-ttu-id="6964c-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6964c-254">Is-Single-Valued</span></span>       | <span data-ttu-id="6964c-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="6964c-255">True</span></span>                                                 |
| <span data-ttu-id="6964c-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6964c-256">Is Indexed</span></span>             | <span data-ttu-id="6964c-257">False</span><span class="sxs-lookup"><span data-stu-id="6964c-257">False</span></span>                                                |
| <span data-ttu-id="6964c-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6964c-258">In Global Catalog</span></span>      | <span data-ttu-id="6964c-259">Richtig</span><span class="sxs-lookup"><span data-stu-id="6964c-259">True</span></span>                                                 |
| <span data-ttu-id="6964c-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6964c-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="6964c-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6964c-261">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="6964c-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6964c-262">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="6964c-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6964c-263">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="6964c-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6964c-264">Search-Flags</span></span>           | <span data-ttu-id="6964c-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6964c-265">0x00000000</span></span>                                           |
| <span data-ttu-id="6964c-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6964c-266">System-Flags</span></span>           | <span data-ttu-id="6964c-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6964c-267">0x00000010</span></span>                                           |
| <span data-ttu-id="6964c-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6964c-268">Classes used in</span></span>        | [<span data-ttu-id="6964c-269">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="6964c-269">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





