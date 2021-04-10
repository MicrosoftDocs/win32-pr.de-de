---
title: Min-pwd-Age-Attribut
description: Die minimale Zeitspanne in 100-Nanosekunden-Intervallen, dass ein Kennwort gültig ist.
ms.assetid: c1ddd8a3-8481-4b6e-95ac-1cdc81a4cf78
ms.tgt_platform: multiple
keywords:
- "\"Min-pwd-Age\"-Attribut, AD-Schema"
- minpwdage-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Min-Pwd-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c733f1a6f6803b10f04d6b0f9e367a9933cd9330
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107205"
---
# <a name="min-pwd-age-attribute"></a><span data-ttu-id="ef6b6-105">Min-pwd-Age-Attribut</span><span class="sxs-lookup"><span data-stu-id="ef6b6-105">Min-Pwd-Age attribute</span></span>

<span data-ttu-id="ef6b6-106">Die minimale Zeitspanne in 100-Nanosekunden-Intervallen, dass ein Kennwort gültig ist.</span><span class="sxs-lookup"><span data-stu-id="ef6b6-106">The minimum amount of time, in 100-nanosecond intervals, that a password is valid.</span></span>



| <span data-ttu-id="ef6b6-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ef6b6-107">Entry</span></span> | <span data-ttu-id="ef6b6-108">Wert</span><span class="sxs-lookup"><span data-stu-id="ef6b6-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ef6b6-109">CN</span><span class="sxs-lookup"><span data-stu-id="ef6b6-109">CN</span></span>                | <span data-ttu-id="ef6b6-110">Min-pwd-Age</span><span class="sxs-lookup"><span data-stu-id="ef6b6-110">Min-Pwd-Age</span></span>                          |
| <span data-ttu-id="ef6b6-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ef6b6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ef6b6-112">minpwdage</span><span class="sxs-lookup"><span data-stu-id="ef6b6-112">minPwdAge</span></span>                            |
| <span data-ttu-id="ef6b6-113">Size</span><span class="sxs-lookup"><span data-stu-id="ef6b6-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="ef6b6-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ef6b6-114">Update Privilege</span></span>  | <span data-ttu-id="ef6b6-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="ef6b6-115">Domain administrator</span></span>                 |
| <span data-ttu-id="ef6b6-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="ef6b6-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ef6b6-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ef6b6-117">Attribute-Id</span></span>      | <span data-ttu-id="ef6b6-118">1.2.840.113556.1.4.78</span><span class="sxs-lookup"><span data-stu-id="ef6b6-118">1.2.840.113556.1.4.78</span></span>                |
| <span data-ttu-id="ef6b6-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ef6b6-119">System-Id-Guid</span></span>    | <span data-ttu-id="ef6b6-120">bf9679c2-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ef6b6-120">bf9679c2-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="ef6b6-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef6b6-121">Syntax</span></span>            | [<span data-ttu-id="ef6b6-122">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="ef6b6-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="ef6b6-123">Implementations</span></span>

-   [<span data-ttu-id="ef6b6-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ef6b6-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ef6b6-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ef6b6-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ef6b6-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ef6b6-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ef6b6-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ef6b6-130">Windows 2000 Server</span></span>



| <span data-ttu-id="ef6b6-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ef6b6-131">Entry</span></span> | <span data-ttu-id="ef6b6-132">Wert</span><span class="sxs-lookup"><span data-stu-id="ef6b6-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef6b6-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ef6b6-133">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef6b6-134">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef6b6-135">System-Only</span></span>            | <span data-ttu-id="ef6b6-136">False</span><span class="sxs-lookup"><span data-stu-id="ef6b6-136">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ef6b6-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ef6b6-137">Is-Single-Valued</span></span>       | <span data-ttu-id="ef6b6-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="ef6b6-138">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ef6b6-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ef6b6-139">Is Indexed</span></span>             | <span data-ttu-id="ef6b6-140">False</span><span class="sxs-lookup"><span data-stu-id="ef6b6-140">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ef6b6-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ef6b6-141">In Global Catalog</span></span>      | <span data-ttu-id="ef6b6-142">False</span><span class="sxs-lookup"><span data-stu-id="ef6b6-142">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ef6b6-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ef6b6-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef6b6-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ef6b6-144">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ef6b6-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef6b6-145">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef6b6-146">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6b6-147">Search-Flags</span></span>           | <span data-ttu-id="ef6b6-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef6b6-148">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ef6b6-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6b6-149">System-Flags</span></span>           | <span data-ttu-id="ef6b6-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef6b6-150">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ef6b6-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ef6b6-151">Classes used in</span></span>        | [<span data-ttu-id="ef6b6-152">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-152">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ef6b6-153">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ef6b6-154">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ef6b6-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ef6b6-155">Windows Server 2003</span></span>



| <span data-ttu-id="ef6b6-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ef6b6-156">Entry</span></span> | <span data-ttu-id="ef6b6-157">Wert</span><span class="sxs-lookup"><span data-stu-id="ef6b6-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef6b6-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ef6b6-158">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef6b6-159">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef6b6-160">System-Only</span></span>            | <span data-ttu-id="ef6b6-161">False</span><span class="sxs-lookup"><span data-stu-id="ef6b6-161">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ef6b6-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ef6b6-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ef6b6-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="ef6b6-163">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ef6b6-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ef6b6-164">Is Indexed</span></span>             | <span data-ttu-id="ef6b6-165">False</span><span class="sxs-lookup"><span data-stu-id="ef6b6-165">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ef6b6-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ef6b6-166">In Global Catalog</span></span>      | <span data-ttu-id="ef6b6-167">False</span><span class="sxs-lookup"><span data-stu-id="ef6b6-167">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ef6b6-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ef6b6-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef6b6-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ef6b6-169">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ef6b6-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef6b6-170">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef6b6-171">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6b6-172">Search-Flags</span></span>           | <span data-ttu-id="ef6b6-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef6b6-173">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ef6b6-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6b6-174">System-Flags</span></span>           | <span data-ttu-id="ef6b6-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef6b6-175">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ef6b6-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ef6b6-176">Classes used in</span></span>        | [<span data-ttu-id="ef6b6-177">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-177">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ef6b6-178">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-178">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ef6b6-179">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-179">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ef6b6-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ef6b6-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ef6b6-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ef6b6-181">Entry</span></span> | <span data-ttu-id="ef6b6-182">Wert</span><span class="sxs-lookup"><span data-stu-id="ef6b6-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef6b6-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ef6b6-183">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef6b6-184">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef6b6-185">System-Only</span></span>            | <span data-ttu-id="ef6b6-186">False</span><span class="sxs-lookup"><span data-stu-id="ef6b6-186">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ef6b6-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ef6b6-187">Is-Single-Valued</span></span>       | <span data-ttu-id="ef6b6-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="ef6b6-188">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ef6b6-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ef6b6-189">Is Indexed</span></span>             | <span data-ttu-id="ef6b6-190">False</span><span class="sxs-lookup"><span data-stu-id="ef6b6-190">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ef6b6-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ef6b6-191">In Global Catalog</span></span>      | <span data-ttu-id="ef6b6-192">False</span><span class="sxs-lookup"><span data-stu-id="ef6b6-192">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ef6b6-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ef6b6-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef6b6-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ef6b6-194">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ef6b6-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef6b6-195">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef6b6-196">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6b6-197">Search-Flags</span></span>           | <span data-ttu-id="ef6b6-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef6b6-198">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ef6b6-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6b6-199">System-Flags</span></span>           | <span data-ttu-id="ef6b6-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef6b6-200">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ef6b6-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ef6b6-201">Classes used in</span></span>        | [<span data-ttu-id="ef6b6-202">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-202">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ef6b6-203">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-203">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ef6b6-204">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-204">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ef6b6-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef6b6-205">Windows Server 2008</span></span>



| <span data-ttu-id="ef6b6-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ef6b6-206">Entry</span></span> | <span data-ttu-id="ef6b6-207">Wert</span><span class="sxs-lookup"><span data-stu-id="ef6b6-207">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef6b6-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ef6b6-208">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef6b6-209">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef6b6-210">System-Only</span></span>            | <span data-ttu-id="ef6b6-211">False</span><span class="sxs-lookup"><span data-stu-id="ef6b6-211">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ef6b6-212">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ef6b6-212">Is-Single-Valued</span></span>       | <span data-ttu-id="ef6b6-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="ef6b6-213">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ef6b6-214">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ef6b6-214">Is Indexed</span></span>             | <span data-ttu-id="ef6b6-215">False</span><span class="sxs-lookup"><span data-stu-id="ef6b6-215">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ef6b6-216">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ef6b6-216">In Global Catalog</span></span>      | <span data-ttu-id="ef6b6-217">False</span><span class="sxs-lookup"><span data-stu-id="ef6b6-217">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ef6b6-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ef6b6-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef6b6-219">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ef6b6-219">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ef6b6-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef6b6-220">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef6b6-221">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6b6-222">Search-Flags</span></span>           | <span data-ttu-id="ef6b6-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef6b6-223">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ef6b6-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6b6-224">System-Flags</span></span>           | <span data-ttu-id="ef6b6-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef6b6-225">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ef6b6-226">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ef6b6-226">Classes used in</span></span>        | [<span data-ttu-id="ef6b6-227">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-227">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ef6b6-228">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-228">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ef6b6-229">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-229">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ef6b6-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ef6b6-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ef6b6-231">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ef6b6-231">Entry</span></span> | <span data-ttu-id="ef6b6-232">Wert</span><span class="sxs-lookup"><span data-stu-id="ef6b6-232">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef6b6-233">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ef6b6-233">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef6b6-234">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef6b6-235">System-Only</span></span>            | <span data-ttu-id="ef6b6-236">False</span><span class="sxs-lookup"><span data-stu-id="ef6b6-236">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ef6b6-237">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ef6b6-237">Is-Single-Valued</span></span>       | <span data-ttu-id="ef6b6-238">Richtig</span><span class="sxs-lookup"><span data-stu-id="ef6b6-238">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ef6b6-239">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ef6b6-239">Is Indexed</span></span>             | <span data-ttu-id="ef6b6-240">False</span><span class="sxs-lookup"><span data-stu-id="ef6b6-240">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ef6b6-241">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ef6b6-241">In Global Catalog</span></span>      | <span data-ttu-id="ef6b6-242">False</span><span class="sxs-lookup"><span data-stu-id="ef6b6-242">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ef6b6-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ef6b6-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef6b6-244">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ef6b6-244">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ef6b6-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef6b6-245">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef6b6-246">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6b6-247">Search-Flags</span></span>           | <span data-ttu-id="ef6b6-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef6b6-248">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ef6b6-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6b6-249">System-Flags</span></span>           | <span data-ttu-id="ef6b6-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef6b6-250">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ef6b6-251">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ef6b6-251">Classes used in</span></span>        | [<span data-ttu-id="ef6b6-252">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-252">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ef6b6-253">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-253">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ef6b6-254">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-254">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ef6b6-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ef6b6-255">Windows Server 2012</span></span>



| <span data-ttu-id="ef6b6-256">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ef6b6-256">Entry</span></span> | <span data-ttu-id="ef6b6-257">Wert</span><span class="sxs-lookup"><span data-stu-id="ef6b6-257">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef6b6-258">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ef6b6-258">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef6b6-259">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef6b6-260">System-Only</span></span>            | <span data-ttu-id="ef6b6-261">False</span><span class="sxs-lookup"><span data-stu-id="ef6b6-261">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ef6b6-262">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ef6b6-262">Is-Single-Valued</span></span>       | <span data-ttu-id="ef6b6-263">Richtig</span><span class="sxs-lookup"><span data-stu-id="ef6b6-263">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ef6b6-264">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ef6b6-264">Is Indexed</span></span>             | <span data-ttu-id="ef6b6-265">False</span><span class="sxs-lookup"><span data-stu-id="ef6b6-265">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ef6b6-266">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ef6b6-266">In Global Catalog</span></span>      | <span data-ttu-id="ef6b6-267">False</span><span class="sxs-lookup"><span data-stu-id="ef6b6-267">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ef6b6-268">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ef6b6-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef6b6-269">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ef6b6-269">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ef6b6-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef6b6-270">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef6b6-271">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ef6b6-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6b6-272">Search-Flags</span></span>           | <span data-ttu-id="ef6b6-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef6b6-273">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ef6b6-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6b6-274">System-Flags</span></span>           | <span data-ttu-id="ef6b6-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef6b6-275">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ef6b6-276">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ef6b6-276">Classes used in</span></span>        | [<span data-ttu-id="ef6b6-277">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-277">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ef6b6-278">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-278">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ef6b6-279">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-279">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





