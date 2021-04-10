---
title: Force-Logoff-Attribut
description: Wird zum Berechnen der Anfangszeit in samigetaccountrestrictions verwendet. Die Abmelde Zeit minus "Abmelde Zeit" ist gleich der Start Zeit.
ms.assetid: 2ce1d5db-52aa-49c5-aef2-ec67122100ed
ms.tgt_platform: multiple
keywords:
- AD-Schema für Force-Logoff-Attribut
- ForceLogoff-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Force-Logoff
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63e31cb241cde4deb40d5978594b4354fbcc564b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107085"
---
# <a name="force-logoff-attribute"></a><span data-ttu-id="d9cf1-106">Force-Logoff-Attribut</span><span class="sxs-lookup"><span data-stu-id="d9cf1-106">Force-Logoff attribute</span></span>

<span data-ttu-id="d9cf1-107">Wird zum Berechnen der Anfangszeit in samigetaccountrestrictions verwendet.</span><span class="sxs-lookup"><span data-stu-id="d9cf1-107">Used in computing the kick off time in SamIGetAccountRestrictions.</span></span> <span data-ttu-id="d9cf1-108">Die Abmelde Zeit minus "Abmelde Zeit" ist gleich der Start Zeit.</span><span class="sxs-lookup"><span data-stu-id="d9cf1-108">Logoff time minus Force Log off equals kick off time.</span></span>



| <span data-ttu-id="d9cf1-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d9cf1-109">Entry</span></span> | <span data-ttu-id="d9cf1-110">Wert</span><span class="sxs-lookup"><span data-stu-id="d9cf1-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d9cf1-111">CN</span><span class="sxs-lookup"><span data-stu-id="d9cf1-111">CN</span></span>                | <span data-ttu-id="d9cf1-112">Force-Logoff</span><span class="sxs-lookup"><span data-stu-id="d9cf1-112">Force-Logoff</span></span>                         |
| <span data-ttu-id="d9cf1-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d9cf1-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d9cf1-114">ForceLogoff</span><span class="sxs-lookup"><span data-stu-id="d9cf1-114">forceLogoff</span></span>                          |
| <span data-ttu-id="d9cf1-115">Size</span><span class="sxs-lookup"><span data-stu-id="d9cf1-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="d9cf1-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d9cf1-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="d9cf1-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="d9cf1-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="d9cf1-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d9cf1-118">Attribute-Id</span></span>      | <span data-ttu-id="d9cf1-119">1.2.840.113556.1.4.39</span><span class="sxs-lookup"><span data-stu-id="d9cf1-119">1.2.840.113556.1.4.39</span></span>                |
| <span data-ttu-id="d9cf1-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d9cf1-120">System-Id-Guid</span></span>    | <span data-ttu-id="d9cf1-121">bf967977-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="d9cf1-121">bf967977-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="d9cf1-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9cf1-122">Syntax</span></span>            | [<span data-ttu-id="d9cf1-123">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="d9cf1-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="d9cf1-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="d9cf1-124">Implementations</span></span>

-   [<span data-ttu-id="d9cf1-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d9cf1-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d9cf1-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d9cf1-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d9cf1-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d9cf1-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d9cf1-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d9cf1-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d9cf1-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d9cf1-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d9cf1-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d9cf1-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d9cf1-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d9cf1-131">Windows 2000 Server</span></span>



| <span data-ttu-id="d9cf1-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d9cf1-132">Entry</span></span> | <span data-ttu-id="d9cf1-133">Wert</span><span class="sxs-lookup"><span data-stu-id="d9cf1-133">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9cf1-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d9cf1-134">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="d9cf1-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9cf1-135">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="d9cf1-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9cf1-136">System-Only</span></span>            | <span data-ttu-id="d9cf1-137">False</span><span class="sxs-lookup"><span data-stu-id="d9cf1-137">False</span></span>                                                                                                    |
| <span data-ttu-id="d9cf1-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d9cf1-138">Is-Single-Valued</span></span>       | <span data-ttu-id="d9cf1-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="d9cf1-139">True</span></span>                                                                                                     |
| <span data-ttu-id="d9cf1-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d9cf1-140">Is Indexed</span></span>             | <span data-ttu-id="d9cf1-141">False</span><span class="sxs-lookup"><span data-stu-id="d9cf1-141">False</span></span>                                                                                                    |
| <span data-ttu-id="d9cf1-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d9cf1-142">In Global Catalog</span></span>      | <span data-ttu-id="d9cf1-143">False</span><span class="sxs-lookup"><span data-stu-id="d9cf1-143">False</span></span>                                                                                                    |
| <span data-ttu-id="d9cf1-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d9cf1-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9cf1-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d9cf1-145">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="d9cf1-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9cf1-146">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="d9cf1-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9cf1-147">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="d9cf1-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9cf1-148">Search-Flags</span></span>           | <span data-ttu-id="d9cf1-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9cf1-149">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="d9cf1-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9cf1-150">System-Flags</span></span>           | <span data-ttu-id="d9cf1-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9cf1-151">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="d9cf1-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d9cf1-152">Classes used in</span></span>        | [<span data-ttu-id="d9cf1-153">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="d9cf1-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="d9cf1-154">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="d9cf1-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d9cf1-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d9cf1-155">Windows Server 2003</span></span>



| <span data-ttu-id="d9cf1-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d9cf1-156">Entry</span></span> | <span data-ttu-id="d9cf1-157">Wert</span><span class="sxs-lookup"><span data-stu-id="d9cf1-157">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9cf1-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d9cf1-158">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="d9cf1-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9cf1-159">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="d9cf1-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9cf1-160">System-Only</span></span>            | <span data-ttu-id="d9cf1-161">False</span><span class="sxs-lookup"><span data-stu-id="d9cf1-161">False</span></span>                                                                                                    |
| <span data-ttu-id="d9cf1-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d9cf1-162">Is-Single-Valued</span></span>       | <span data-ttu-id="d9cf1-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="d9cf1-163">True</span></span>                                                                                                     |
| <span data-ttu-id="d9cf1-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d9cf1-164">Is Indexed</span></span>             | <span data-ttu-id="d9cf1-165">False</span><span class="sxs-lookup"><span data-stu-id="d9cf1-165">False</span></span>                                                                                                    |
| <span data-ttu-id="d9cf1-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d9cf1-166">In Global Catalog</span></span>      | <span data-ttu-id="d9cf1-167">False</span><span class="sxs-lookup"><span data-stu-id="d9cf1-167">False</span></span>                                                                                                    |
| <span data-ttu-id="d9cf1-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d9cf1-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9cf1-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d9cf1-169">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="d9cf1-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9cf1-170">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="d9cf1-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9cf1-171">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="d9cf1-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9cf1-172">Search-Flags</span></span>           | <span data-ttu-id="d9cf1-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9cf1-173">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="d9cf1-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9cf1-174">System-Flags</span></span>           | <span data-ttu-id="d9cf1-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9cf1-175">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="d9cf1-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d9cf1-176">Classes used in</span></span>        | [<span data-ttu-id="d9cf1-177">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="d9cf1-177">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="d9cf1-178">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="d9cf1-178">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d9cf1-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d9cf1-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d9cf1-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d9cf1-180">Entry</span></span> | <span data-ttu-id="d9cf1-181">Wert</span><span class="sxs-lookup"><span data-stu-id="d9cf1-181">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9cf1-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d9cf1-182">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="d9cf1-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9cf1-183">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="d9cf1-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9cf1-184">System-Only</span></span>            | <span data-ttu-id="d9cf1-185">False</span><span class="sxs-lookup"><span data-stu-id="d9cf1-185">False</span></span>                                                                                                    |
| <span data-ttu-id="d9cf1-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d9cf1-186">Is-Single-Valued</span></span>       | <span data-ttu-id="d9cf1-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="d9cf1-187">True</span></span>                                                                                                     |
| <span data-ttu-id="d9cf1-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d9cf1-188">Is Indexed</span></span>             | <span data-ttu-id="d9cf1-189">False</span><span class="sxs-lookup"><span data-stu-id="d9cf1-189">False</span></span>                                                                                                    |
| <span data-ttu-id="d9cf1-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d9cf1-190">In Global Catalog</span></span>      | <span data-ttu-id="d9cf1-191">False</span><span class="sxs-lookup"><span data-stu-id="d9cf1-191">False</span></span>                                                                                                    |
| <span data-ttu-id="d9cf1-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d9cf1-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9cf1-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d9cf1-193">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="d9cf1-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9cf1-194">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="d9cf1-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9cf1-195">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="d9cf1-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9cf1-196">Search-Flags</span></span>           | <span data-ttu-id="d9cf1-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9cf1-197">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="d9cf1-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9cf1-198">System-Flags</span></span>           | <span data-ttu-id="d9cf1-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9cf1-199">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="d9cf1-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d9cf1-200">Classes used in</span></span>        | [<span data-ttu-id="d9cf1-201">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="d9cf1-201">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="d9cf1-202">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="d9cf1-202">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d9cf1-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9cf1-203">Windows Server 2008</span></span>



| <span data-ttu-id="d9cf1-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d9cf1-204">Entry</span></span> | <span data-ttu-id="d9cf1-205">Wert</span><span class="sxs-lookup"><span data-stu-id="d9cf1-205">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9cf1-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d9cf1-206">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="d9cf1-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9cf1-207">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="d9cf1-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9cf1-208">System-Only</span></span>            | <span data-ttu-id="d9cf1-209">False</span><span class="sxs-lookup"><span data-stu-id="d9cf1-209">False</span></span>                                                                                                    |
| <span data-ttu-id="d9cf1-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d9cf1-210">Is-Single-Valued</span></span>       | <span data-ttu-id="d9cf1-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="d9cf1-211">True</span></span>                                                                                                     |
| <span data-ttu-id="d9cf1-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d9cf1-212">Is Indexed</span></span>             | <span data-ttu-id="d9cf1-213">False</span><span class="sxs-lookup"><span data-stu-id="d9cf1-213">False</span></span>                                                                                                    |
| <span data-ttu-id="d9cf1-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d9cf1-214">In Global Catalog</span></span>      | <span data-ttu-id="d9cf1-215">False</span><span class="sxs-lookup"><span data-stu-id="d9cf1-215">False</span></span>                                                                                                    |
| <span data-ttu-id="d9cf1-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d9cf1-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9cf1-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d9cf1-217">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="d9cf1-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9cf1-218">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="d9cf1-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9cf1-219">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="d9cf1-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9cf1-220">Search-Flags</span></span>           | <span data-ttu-id="d9cf1-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9cf1-221">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="d9cf1-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9cf1-222">System-Flags</span></span>           | <span data-ttu-id="d9cf1-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9cf1-223">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="d9cf1-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d9cf1-224">Classes used in</span></span>        | [<span data-ttu-id="d9cf1-225">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="d9cf1-225">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="d9cf1-226">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="d9cf1-226">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d9cf1-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d9cf1-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d9cf1-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d9cf1-228">Entry</span></span> | <span data-ttu-id="d9cf1-229">Wert</span><span class="sxs-lookup"><span data-stu-id="d9cf1-229">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9cf1-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d9cf1-230">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="d9cf1-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9cf1-231">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="d9cf1-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9cf1-232">System-Only</span></span>            | <span data-ttu-id="d9cf1-233">False</span><span class="sxs-lookup"><span data-stu-id="d9cf1-233">False</span></span>                                                                                                    |
| <span data-ttu-id="d9cf1-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d9cf1-234">Is-Single-Valued</span></span>       | <span data-ttu-id="d9cf1-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="d9cf1-235">True</span></span>                                                                                                     |
| <span data-ttu-id="d9cf1-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d9cf1-236">Is Indexed</span></span>             | <span data-ttu-id="d9cf1-237">False</span><span class="sxs-lookup"><span data-stu-id="d9cf1-237">False</span></span>                                                                                                    |
| <span data-ttu-id="d9cf1-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d9cf1-238">In Global Catalog</span></span>      | <span data-ttu-id="d9cf1-239">False</span><span class="sxs-lookup"><span data-stu-id="d9cf1-239">False</span></span>                                                                                                    |
| <span data-ttu-id="d9cf1-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d9cf1-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9cf1-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d9cf1-241">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="d9cf1-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9cf1-242">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="d9cf1-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9cf1-243">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="d9cf1-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9cf1-244">Search-Flags</span></span>           | <span data-ttu-id="d9cf1-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9cf1-245">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="d9cf1-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9cf1-246">System-Flags</span></span>           | <span data-ttu-id="d9cf1-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9cf1-247">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="d9cf1-248">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d9cf1-248">Classes used in</span></span>        | [<span data-ttu-id="d9cf1-249">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="d9cf1-249">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="d9cf1-250">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="d9cf1-250">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d9cf1-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d9cf1-251">Windows Server 2012</span></span>



| <span data-ttu-id="d9cf1-252">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d9cf1-252">Entry</span></span> | <span data-ttu-id="d9cf1-253">Wert</span><span class="sxs-lookup"><span data-stu-id="d9cf1-253">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9cf1-254">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d9cf1-254">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="d9cf1-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9cf1-255">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="d9cf1-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9cf1-256">System-Only</span></span>            | <span data-ttu-id="d9cf1-257">False</span><span class="sxs-lookup"><span data-stu-id="d9cf1-257">False</span></span>                                                                                                    |
| <span data-ttu-id="d9cf1-258">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d9cf1-258">Is-Single-Valued</span></span>       | <span data-ttu-id="d9cf1-259">Richtig</span><span class="sxs-lookup"><span data-stu-id="d9cf1-259">True</span></span>                                                                                                     |
| <span data-ttu-id="d9cf1-260">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d9cf1-260">Is Indexed</span></span>             | <span data-ttu-id="d9cf1-261">False</span><span class="sxs-lookup"><span data-stu-id="d9cf1-261">False</span></span>                                                                                                    |
| <span data-ttu-id="d9cf1-262">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d9cf1-262">In Global Catalog</span></span>      | <span data-ttu-id="d9cf1-263">False</span><span class="sxs-lookup"><span data-stu-id="d9cf1-263">False</span></span>                                                                                                    |
| <span data-ttu-id="d9cf1-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d9cf1-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9cf1-265">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d9cf1-265">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="d9cf1-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9cf1-266">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="d9cf1-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9cf1-267">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="d9cf1-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9cf1-268">Search-Flags</span></span>           | <span data-ttu-id="d9cf1-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9cf1-269">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="d9cf1-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9cf1-270">System-Flags</span></span>           | <span data-ttu-id="d9cf1-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9cf1-271">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="d9cf1-272">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d9cf1-272">Classes used in</span></span>        | [<span data-ttu-id="d9cf1-273">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="d9cf1-273">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="d9cf1-274">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="d9cf1-274">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





