---
title: Lockout-Threshold-Attribut
description: Die Anzahl der ungültigen Anmeldeversuche, die zulässig sind, bevor das Konto gesperrt wird.
ms.assetid: c4dcbbb6-0680-45f3-9b0b-f9c4bbf2b349
ms.tgt_platform: multiple
keywords:
- AD-Schema für Lockout-Threshold-Attribut
- AD-Schema für LockoutThreshold-Attribut
topic_type:
- apiref
api_name:
- Lockout-Threshold
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345977055597c48d70e30a20ce9bfbc9f07f3929
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859472"
---
# <a name="lockout-threshold-attribute"></a><span data-ttu-id="34802-105">Lockout-Threshold-Attribut</span><span class="sxs-lookup"><span data-stu-id="34802-105">Lockout-Threshold attribute</span></span>

<span data-ttu-id="34802-106">Die Anzahl der ungültigen Anmeldeversuche, die zulässig sind, bevor das Konto gesperrt wird.</span><span class="sxs-lookup"><span data-stu-id="34802-106">The number of invalid logon attempts that are permitted before the account is locked out.</span></span>



| <span data-ttu-id="34802-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34802-107">Entry</span></span> | <span data-ttu-id="34802-108">Wert</span><span class="sxs-lookup"><span data-stu-id="34802-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="34802-109">CN</span><span class="sxs-lookup"><span data-stu-id="34802-109">CN</span></span>                | <span data-ttu-id="34802-110">Lockout-Threshold</span><span class="sxs-lookup"><span data-stu-id="34802-110">Lockout-Threshold</span></span>                    |
| <span data-ttu-id="34802-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="34802-111">Ldap-Display-Name</span></span> | <span data-ttu-id="34802-112">LockoutThreshold</span><span class="sxs-lookup"><span data-stu-id="34802-112">lockoutThreshold</span></span>                     |
| <span data-ttu-id="34802-113">Size</span><span class="sxs-lookup"><span data-stu-id="34802-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="34802-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="34802-114">Update Privilege</span></span>  | <span data-ttu-id="34802-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="34802-115">Domain administrator</span></span>                 |
| <span data-ttu-id="34802-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="34802-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="34802-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="34802-117">Attribute-Id</span></span>      | <span data-ttu-id="34802-118">1.2.840.113556.1.4.73</span><span class="sxs-lookup"><span data-stu-id="34802-118">1.2.840.113556.1.4.73</span></span>                |
| <span data-ttu-id="34802-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="34802-119">System-Id-Guid</span></span>    | <span data-ttu-id="34802-120">bf9679a6-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="34802-120">bf9679a6-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="34802-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="34802-121">Syntax</span></span>            | [<span data-ttu-id="34802-122">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="34802-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="34802-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="34802-123">Implementations</span></span>

-   [<span data-ttu-id="34802-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="34802-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="34802-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="34802-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="34802-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="34802-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="34802-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="34802-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="34802-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="34802-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="34802-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="34802-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="34802-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="34802-130">Windows 2000 Server</span></span>



| <span data-ttu-id="34802-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34802-131">Entry</span></span> | <span data-ttu-id="34802-132">Wert</span><span class="sxs-lookup"><span data-stu-id="34802-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34802-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="34802-133">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="34802-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34802-134">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="34802-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="34802-135">System-Only</span></span>            | <span data-ttu-id="34802-136">False</span><span class="sxs-lookup"><span data-stu-id="34802-136">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="34802-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="34802-137">Is-Single-Valued</span></span>       | <span data-ttu-id="34802-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="34802-138">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="34802-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="34802-139">Is Indexed</span></span>             | <span data-ttu-id="34802-140">False</span><span class="sxs-lookup"><span data-stu-id="34802-140">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="34802-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="34802-141">In Global Catalog</span></span>      | <span data-ttu-id="34802-142">False</span><span class="sxs-lookup"><span data-stu-id="34802-142">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="34802-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="34802-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="34802-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="34802-144">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="34802-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34802-145">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="34802-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34802-146">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="34802-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34802-147">Search-Flags</span></span>           | <span data-ttu-id="34802-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34802-148">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="34802-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34802-149">System-Flags</span></span>           | <span data-ttu-id="34802-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34802-150">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="34802-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="34802-151">Classes used in</span></span>        | [<span data-ttu-id="34802-152">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="34802-152">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="34802-153">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="34802-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="34802-154">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="34802-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="34802-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="34802-155">Windows Server 2003</span></span>



| <span data-ttu-id="34802-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34802-156">Entry</span></span> | <span data-ttu-id="34802-157">Wert</span><span class="sxs-lookup"><span data-stu-id="34802-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34802-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="34802-158">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="34802-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34802-159">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="34802-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="34802-160">System-Only</span></span>            | <span data-ttu-id="34802-161">False</span><span class="sxs-lookup"><span data-stu-id="34802-161">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="34802-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="34802-162">Is-Single-Valued</span></span>       | <span data-ttu-id="34802-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="34802-163">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="34802-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="34802-164">Is Indexed</span></span>             | <span data-ttu-id="34802-165">False</span><span class="sxs-lookup"><span data-stu-id="34802-165">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="34802-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="34802-166">In Global Catalog</span></span>      | <span data-ttu-id="34802-167">False</span><span class="sxs-lookup"><span data-stu-id="34802-167">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="34802-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="34802-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="34802-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="34802-169">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="34802-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34802-170">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="34802-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34802-171">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="34802-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34802-172">Search-Flags</span></span>           | <span data-ttu-id="34802-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34802-173">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="34802-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34802-174">System-Flags</span></span>           | <span data-ttu-id="34802-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34802-175">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="34802-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="34802-176">Classes used in</span></span>        | [<span data-ttu-id="34802-177">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="34802-177">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="34802-178">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="34802-178">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="34802-179">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="34802-179">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="34802-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="34802-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="34802-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34802-181">Entry</span></span> | <span data-ttu-id="34802-182">Wert</span><span class="sxs-lookup"><span data-stu-id="34802-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34802-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="34802-183">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="34802-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34802-184">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="34802-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="34802-185">System-Only</span></span>            | <span data-ttu-id="34802-186">False</span><span class="sxs-lookup"><span data-stu-id="34802-186">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="34802-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="34802-187">Is-Single-Valued</span></span>       | <span data-ttu-id="34802-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="34802-188">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="34802-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="34802-189">Is Indexed</span></span>             | <span data-ttu-id="34802-190">False</span><span class="sxs-lookup"><span data-stu-id="34802-190">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="34802-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="34802-191">In Global Catalog</span></span>      | <span data-ttu-id="34802-192">False</span><span class="sxs-lookup"><span data-stu-id="34802-192">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="34802-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="34802-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="34802-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="34802-194">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="34802-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34802-195">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="34802-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34802-196">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="34802-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34802-197">Search-Flags</span></span>           | <span data-ttu-id="34802-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34802-198">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="34802-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34802-199">System-Flags</span></span>           | <span data-ttu-id="34802-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34802-200">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="34802-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="34802-201">Classes used in</span></span>        | [<span data-ttu-id="34802-202">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="34802-202">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="34802-203">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="34802-203">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="34802-204">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="34802-204">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="34802-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34802-205">Windows Server 2008</span></span>



| <span data-ttu-id="34802-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34802-206">Entry</span></span> | <span data-ttu-id="34802-207">Wert</span><span class="sxs-lookup"><span data-stu-id="34802-207">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34802-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="34802-208">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="34802-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34802-209">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="34802-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="34802-210">System-Only</span></span>            | <span data-ttu-id="34802-211">False</span><span class="sxs-lookup"><span data-stu-id="34802-211">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="34802-212">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="34802-212">Is-Single-Valued</span></span>       | <span data-ttu-id="34802-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="34802-213">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="34802-214">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="34802-214">Is Indexed</span></span>             | <span data-ttu-id="34802-215">False</span><span class="sxs-lookup"><span data-stu-id="34802-215">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="34802-216">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="34802-216">In Global Catalog</span></span>      | <span data-ttu-id="34802-217">False</span><span class="sxs-lookup"><span data-stu-id="34802-217">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="34802-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="34802-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="34802-219">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="34802-219">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="34802-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34802-220">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="34802-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34802-221">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="34802-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34802-222">Search-Flags</span></span>           | <span data-ttu-id="34802-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34802-223">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="34802-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34802-224">System-Flags</span></span>           | <span data-ttu-id="34802-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34802-225">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="34802-226">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="34802-226">Classes used in</span></span>        | [<span data-ttu-id="34802-227">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="34802-227">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="34802-228">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="34802-228">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="34802-229">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="34802-229">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="34802-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="34802-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="34802-231">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34802-231">Entry</span></span> | <span data-ttu-id="34802-232">Wert</span><span class="sxs-lookup"><span data-stu-id="34802-232">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34802-233">Link-ID</span><span class="sxs-lookup"><span data-stu-id="34802-233">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="34802-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34802-234">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="34802-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="34802-235">System-Only</span></span>            | <span data-ttu-id="34802-236">False</span><span class="sxs-lookup"><span data-stu-id="34802-236">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="34802-237">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="34802-237">Is-Single-Valued</span></span>       | <span data-ttu-id="34802-238">Richtig</span><span class="sxs-lookup"><span data-stu-id="34802-238">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="34802-239">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="34802-239">Is Indexed</span></span>             | <span data-ttu-id="34802-240">False</span><span class="sxs-lookup"><span data-stu-id="34802-240">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="34802-241">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="34802-241">In Global Catalog</span></span>      | <span data-ttu-id="34802-242">False</span><span class="sxs-lookup"><span data-stu-id="34802-242">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="34802-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="34802-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="34802-244">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="34802-244">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="34802-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34802-245">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="34802-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34802-246">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="34802-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34802-247">Search-Flags</span></span>           | <span data-ttu-id="34802-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34802-248">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="34802-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34802-249">System-Flags</span></span>           | <span data-ttu-id="34802-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34802-250">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="34802-251">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="34802-251">Classes used in</span></span>        | [<span data-ttu-id="34802-252">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="34802-252">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="34802-253">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="34802-253">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="34802-254">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="34802-254">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="34802-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="34802-255">Windows Server 2012</span></span>



| <span data-ttu-id="34802-256">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34802-256">Entry</span></span> | <span data-ttu-id="34802-257">Wert</span><span class="sxs-lookup"><span data-stu-id="34802-257">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34802-258">Link-ID</span><span class="sxs-lookup"><span data-stu-id="34802-258">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="34802-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34802-259">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="34802-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="34802-260">System-Only</span></span>            | <span data-ttu-id="34802-261">False</span><span class="sxs-lookup"><span data-stu-id="34802-261">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="34802-262">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="34802-262">Is-Single-Valued</span></span>       | <span data-ttu-id="34802-263">Richtig</span><span class="sxs-lookup"><span data-stu-id="34802-263">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="34802-264">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="34802-264">Is Indexed</span></span>             | <span data-ttu-id="34802-265">False</span><span class="sxs-lookup"><span data-stu-id="34802-265">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="34802-266">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="34802-266">In Global Catalog</span></span>      | <span data-ttu-id="34802-267">False</span><span class="sxs-lookup"><span data-stu-id="34802-267">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="34802-268">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="34802-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="34802-269">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="34802-269">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="34802-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34802-270">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="34802-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34802-271">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="34802-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34802-272">Search-Flags</span></span>           | <span data-ttu-id="34802-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34802-273">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="34802-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34802-274">System-Flags</span></span>           | <span data-ttu-id="34802-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34802-275">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="34802-276">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="34802-276">Classes used in</span></span>        | [<span data-ttu-id="34802-277">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="34802-277">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="34802-278">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="34802-278">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="34802-279">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="34802-279">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="34802-280">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34802-280">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34802-281">**Sperr Dauer**</span><span class="sxs-lookup"><span data-stu-id="34802-281">**Lockout-Duration**</span></span>](a-lockoutduration.md)
</dt> </dl>

 

 





