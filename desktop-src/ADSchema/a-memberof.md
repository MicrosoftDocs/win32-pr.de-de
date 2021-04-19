---
title: Is-Member-of-DL-Attribut
description: Der Distinguished Name der Gruppen, zu denen dieses-Objekt gehört.
ms.assetid: 28fe1991-291b-4531-aec2-b1a1910be464
ms.tgt_platform: multiple
keywords:
- Is-Member-of-DL-Attribut AD-Schema
- Schema der Attribut Mitgliedschaft
topic_type:
- apiref
api_name:
- Is-Member-Of-DL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad522fcba256e0965057a9f8a8505e99a3fdbdeb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346350"
---
# <a name="is-member-of-dl-attribute"></a><span data-ttu-id="c99d1-105">Is-Member-of-DL-Attribut</span><span class="sxs-lookup"><span data-stu-id="c99d1-105">Is-Member-Of-DL attribute</span></span>

<span data-ttu-id="c99d1-106">Der Distinguished Name der Gruppen, zu denen dieses-Objekt gehört.</span><span class="sxs-lookup"><span data-stu-id="c99d1-106">The distinguished name of the groups to which this object belongs.</span></span>



| <span data-ttu-id="c99d1-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c99d1-107">Entry</span></span> | <span data-ttu-id="c99d1-108">Wert</span><span class="sxs-lookup"><span data-stu-id="c99d1-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="c99d1-109">CN</span><span class="sxs-lookup"><span data-stu-id="c99d1-109">CN</span></span>                | <span data-ttu-id="c99d1-110">Is-Member-of-DL</span><span class="sxs-lookup"><span data-stu-id="c99d1-110">Is-Member-Of-DL</span></span>                         |
| <span data-ttu-id="c99d1-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c99d1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c99d1-112">memberOf</span><span class="sxs-lookup"><span data-stu-id="c99d1-112">memberOf</span></span>                                |
| <span data-ttu-id="c99d1-113">Size</span><span class="sxs-lookup"><span data-stu-id="c99d1-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="c99d1-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c99d1-114">Update Privilege</span></span>  | <span data-ttu-id="c99d1-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="c99d1-115">Domain administrator</span></span>                    |
| <span data-ttu-id="c99d1-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="c99d1-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="c99d1-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c99d1-117">Attribute-Id</span></span>      | <span data-ttu-id="c99d1-118">1.2.840.113556.1.2.102</span><span class="sxs-lookup"><span data-stu-id="c99d1-118">1.2.840.113556.1.2.102</span></span>                  |
| <span data-ttu-id="c99d1-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c99d1-119">System-Id-Guid</span></span>    | <span data-ttu-id="c99d1-120">bf967991-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c99d1-120">bf967991-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="c99d1-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="c99d1-121">Syntax</span></span>            | [<span data-ttu-id="c99d1-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="c99d1-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="c99d1-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="c99d1-123">Implementations</span></span>

-   [<span data-ttu-id="c99d1-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c99d1-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c99d1-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c99d1-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c99d1-126">**Adam**</span><span class="sxs-lookup"><span data-stu-id="c99d1-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c99d1-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c99d1-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c99d1-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c99d1-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c99d1-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c99d1-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c99d1-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c99d1-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c99d1-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c99d1-131">Windows 2000 Server</span></span>



| <span data-ttu-id="c99d1-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c99d1-132">Entry</span></span> | <span data-ttu-id="c99d1-133">Wert</span><span class="sxs-lookup"><span data-stu-id="c99d1-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c99d1-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c99d1-134">Link-Id</span></span>                | <span data-ttu-id="c99d1-135">3</span><span class="sxs-lookup"><span data-stu-id="c99d1-135">3</span></span>                               |
| <span data-ttu-id="c99d1-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c99d1-136">MAPI-Id</span></span>                | <span data-ttu-id="c99d1-137">0x8008</span><span class="sxs-lookup"><span data-stu-id="c99d1-137">0x8008</span></span>                          |
| <span data-ttu-id="c99d1-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="c99d1-138">System-Only</span></span>            | <span data-ttu-id="c99d1-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="c99d1-139">True</span></span>                            |
| <span data-ttu-id="c99d1-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c99d1-140">Is-Single-Valued</span></span>       | <span data-ttu-id="c99d1-141">False</span><span class="sxs-lookup"><span data-stu-id="c99d1-141">False</span></span>                           |
| <span data-ttu-id="c99d1-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c99d1-142">Is Indexed</span></span>             | <span data-ttu-id="c99d1-143">False</span><span class="sxs-lookup"><span data-stu-id="c99d1-143">False</span></span>                           |
| <span data-ttu-id="c99d1-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c99d1-144">In Global Catalog</span></span>      | <span data-ttu-id="c99d1-145">False</span><span class="sxs-lookup"><span data-stu-id="c99d1-145">False</span></span>                           |
| <span data-ttu-id="c99d1-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c99d1-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="c99d1-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c99d1-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c99d1-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c99d1-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c99d1-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c99d1-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c99d1-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c99d1-150">Search-Flags</span></span>           | <span data-ttu-id="c99d1-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c99d1-151">0x00000010</span></span>                      |
| <span data-ttu-id="c99d1-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c99d1-152">System-Flags</span></span>           | <span data-ttu-id="c99d1-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c99d1-153">0x00000010</span></span>                      |
| <span data-ttu-id="c99d1-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c99d1-154">Classes used in</span></span>        | [<span data-ttu-id="c99d1-155">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="c99d1-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c99d1-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c99d1-156">Windows Server 2003</span></span>



| <span data-ttu-id="c99d1-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c99d1-157">Entry</span></span> | <span data-ttu-id="c99d1-158">Wert</span><span class="sxs-lookup"><span data-stu-id="c99d1-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c99d1-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c99d1-159">Link-Id</span></span>                | <span data-ttu-id="c99d1-160">3</span><span class="sxs-lookup"><span data-stu-id="c99d1-160">3</span></span>                               |
| <span data-ttu-id="c99d1-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c99d1-161">MAPI-Id</span></span>                | <span data-ttu-id="c99d1-162">0x8008</span><span class="sxs-lookup"><span data-stu-id="c99d1-162">0x8008</span></span>                          |
| <span data-ttu-id="c99d1-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="c99d1-163">System-Only</span></span>            | <span data-ttu-id="c99d1-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="c99d1-164">True</span></span>                            |
| <span data-ttu-id="c99d1-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c99d1-165">Is-Single-Valued</span></span>       | <span data-ttu-id="c99d1-166">False</span><span class="sxs-lookup"><span data-stu-id="c99d1-166">False</span></span>                           |
| <span data-ttu-id="c99d1-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c99d1-167">Is Indexed</span></span>             | <span data-ttu-id="c99d1-168">False</span><span class="sxs-lookup"><span data-stu-id="c99d1-168">False</span></span>                           |
| <span data-ttu-id="c99d1-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c99d1-169">In Global Catalog</span></span>      | <span data-ttu-id="c99d1-170">False</span><span class="sxs-lookup"><span data-stu-id="c99d1-170">False</span></span>                           |
| <span data-ttu-id="c99d1-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c99d1-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="c99d1-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c99d1-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c99d1-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c99d1-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c99d1-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c99d1-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c99d1-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c99d1-175">Search-Flags</span></span>           | <span data-ttu-id="c99d1-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c99d1-176">0x00000010</span></span>                      |
| <span data-ttu-id="c99d1-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c99d1-177">System-Flags</span></span>           | <span data-ttu-id="c99d1-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c99d1-178">0x00000010</span></span>                      |
| <span data-ttu-id="c99d1-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c99d1-179">Classes used in</span></span>        | [<span data-ttu-id="c99d1-180">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="c99d1-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c99d1-181">Adam</span><span class="sxs-lookup"><span data-stu-id="c99d1-181">ADAM</span></span>



| <span data-ttu-id="c99d1-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c99d1-182">Entry</span></span> | <span data-ttu-id="c99d1-183">Wert</span><span class="sxs-lookup"><span data-stu-id="c99d1-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c99d1-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c99d1-184">Link-Id</span></span>                | <span data-ttu-id="c99d1-185">3</span><span class="sxs-lookup"><span data-stu-id="c99d1-185">3</span></span>                               |
| <span data-ttu-id="c99d1-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c99d1-186">MAPI-Id</span></span>                | <span data-ttu-id="c99d1-187">0x8008</span><span class="sxs-lookup"><span data-stu-id="c99d1-187">0x8008</span></span>                          |
| <span data-ttu-id="c99d1-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="c99d1-188">System-Only</span></span>            | <span data-ttu-id="c99d1-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="c99d1-189">True</span></span>                            |
| <span data-ttu-id="c99d1-190">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c99d1-190">Is-Single-Valued</span></span>       | <span data-ttu-id="c99d1-191">False</span><span class="sxs-lookup"><span data-stu-id="c99d1-191">False</span></span>                           |
| <span data-ttu-id="c99d1-192">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c99d1-192">Is Indexed</span></span>             | <span data-ttu-id="c99d1-193">False</span><span class="sxs-lookup"><span data-stu-id="c99d1-193">False</span></span>                           |
| <span data-ttu-id="c99d1-194">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c99d1-194">In Global Catalog</span></span>      | <span data-ttu-id="c99d1-195">False</span><span class="sxs-lookup"><span data-stu-id="c99d1-195">False</span></span>                           |
| <span data-ttu-id="c99d1-196">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c99d1-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="c99d1-197">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c99d1-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c99d1-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c99d1-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c99d1-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c99d1-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c99d1-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c99d1-200">Search-Flags</span></span>           | <span data-ttu-id="c99d1-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c99d1-201">0x00000010</span></span>                      |
| <span data-ttu-id="c99d1-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c99d1-202">System-Flags</span></span>           | <span data-ttu-id="c99d1-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c99d1-203">0x00000010</span></span>                      |
| <span data-ttu-id="c99d1-204">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c99d1-204">Classes used in</span></span>        | [<span data-ttu-id="c99d1-205">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="c99d1-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c99d1-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c99d1-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c99d1-207">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c99d1-207">Entry</span></span> | <span data-ttu-id="c99d1-208">Wert</span><span class="sxs-lookup"><span data-stu-id="c99d1-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c99d1-209">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c99d1-209">Link-Id</span></span>                | <span data-ttu-id="c99d1-210">3</span><span class="sxs-lookup"><span data-stu-id="c99d1-210">3</span></span>                               |
| <span data-ttu-id="c99d1-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c99d1-211">MAPI-Id</span></span>                | <span data-ttu-id="c99d1-212">0x8008</span><span class="sxs-lookup"><span data-stu-id="c99d1-212">0x8008</span></span>                          |
| <span data-ttu-id="c99d1-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="c99d1-213">System-Only</span></span>            | <span data-ttu-id="c99d1-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="c99d1-214">True</span></span>                            |
| <span data-ttu-id="c99d1-215">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c99d1-215">Is-Single-Valued</span></span>       | <span data-ttu-id="c99d1-216">False</span><span class="sxs-lookup"><span data-stu-id="c99d1-216">False</span></span>                           |
| <span data-ttu-id="c99d1-217">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c99d1-217">Is Indexed</span></span>             | <span data-ttu-id="c99d1-218">False</span><span class="sxs-lookup"><span data-stu-id="c99d1-218">False</span></span>                           |
| <span data-ttu-id="c99d1-219">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c99d1-219">In Global Catalog</span></span>      | <span data-ttu-id="c99d1-220">False</span><span class="sxs-lookup"><span data-stu-id="c99d1-220">False</span></span>                           |
| <span data-ttu-id="c99d1-221">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c99d1-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="c99d1-222">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c99d1-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c99d1-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c99d1-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c99d1-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c99d1-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c99d1-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c99d1-225">Search-Flags</span></span>           | <span data-ttu-id="c99d1-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c99d1-226">0x00000010</span></span>                      |
| <span data-ttu-id="c99d1-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c99d1-227">System-Flags</span></span>           | <span data-ttu-id="c99d1-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c99d1-228">0x00000010</span></span>                      |
| <span data-ttu-id="c99d1-229">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c99d1-229">Classes used in</span></span>        | [<span data-ttu-id="c99d1-230">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="c99d1-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c99d1-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c99d1-231">Windows Server 2008</span></span>



| <span data-ttu-id="c99d1-232">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c99d1-232">Entry</span></span> | <span data-ttu-id="c99d1-233">Wert</span><span class="sxs-lookup"><span data-stu-id="c99d1-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c99d1-234">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c99d1-234">Link-Id</span></span>                | <span data-ttu-id="c99d1-235">3</span><span class="sxs-lookup"><span data-stu-id="c99d1-235">3</span></span>                               |
| <span data-ttu-id="c99d1-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c99d1-236">MAPI-Id</span></span>                | <span data-ttu-id="c99d1-237">0x8008</span><span class="sxs-lookup"><span data-stu-id="c99d1-237">0x8008</span></span>                          |
| <span data-ttu-id="c99d1-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="c99d1-238">System-Only</span></span>            | <span data-ttu-id="c99d1-239">Richtig</span><span class="sxs-lookup"><span data-stu-id="c99d1-239">True</span></span>                            |
| <span data-ttu-id="c99d1-240">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c99d1-240">Is-Single-Valued</span></span>       | <span data-ttu-id="c99d1-241">False</span><span class="sxs-lookup"><span data-stu-id="c99d1-241">False</span></span>                           |
| <span data-ttu-id="c99d1-242">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c99d1-242">Is Indexed</span></span>             | <span data-ttu-id="c99d1-243">False</span><span class="sxs-lookup"><span data-stu-id="c99d1-243">False</span></span>                           |
| <span data-ttu-id="c99d1-244">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c99d1-244">In Global Catalog</span></span>      | <span data-ttu-id="c99d1-245">False</span><span class="sxs-lookup"><span data-stu-id="c99d1-245">False</span></span>                           |
| <span data-ttu-id="c99d1-246">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c99d1-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="c99d1-247">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c99d1-247">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c99d1-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c99d1-248">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c99d1-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c99d1-249">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c99d1-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c99d1-250">Search-Flags</span></span>           | <span data-ttu-id="c99d1-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c99d1-251">0x00000010</span></span>                      |
| <span data-ttu-id="c99d1-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c99d1-252">System-Flags</span></span>           | <span data-ttu-id="c99d1-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c99d1-253">0x00000010</span></span>                      |
| <span data-ttu-id="c99d1-254">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c99d1-254">Classes used in</span></span>        | [<span data-ttu-id="c99d1-255">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="c99d1-255">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c99d1-256">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c99d1-256">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c99d1-257">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c99d1-257">Entry</span></span> | <span data-ttu-id="c99d1-258">Wert</span><span class="sxs-lookup"><span data-stu-id="c99d1-258">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c99d1-259">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c99d1-259">Link-Id</span></span>                | <span data-ttu-id="c99d1-260">3</span><span class="sxs-lookup"><span data-stu-id="c99d1-260">3</span></span>                               |
| <span data-ttu-id="c99d1-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c99d1-261">MAPI-Id</span></span>                | <span data-ttu-id="c99d1-262">0x8008</span><span class="sxs-lookup"><span data-stu-id="c99d1-262">0x8008</span></span>                          |
| <span data-ttu-id="c99d1-263">System-Only</span><span class="sxs-lookup"><span data-stu-id="c99d1-263">System-Only</span></span>            | <span data-ttu-id="c99d1-264">Richtig</span><span class="sxs-lookup"><span data-stu-id="c99d1-264">True</span></span>                            |
| <span data-ttu-id="c99d1-265">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c99d1-265">Is-Single-Valued</span></span>       | <span data-ttu-id="c99d1-266">False</span><span class="sxs-lookup"><span data-stu-id="c99d1-266">False</span></span>                           |
| <span data-ttu-id="c99d1-267">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c99d1-267">Is Indexed</span></span>             | <span data-ttu-id="c99d1-268">False</span><span class="sxs-lookup"><span data-stu-id="c99d1-268">False</span></span>                           |
| <span data-ttu-id="c99d1-269">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c99d1-269">In Global Catalog</span></span>      | <span data-ttu-id="c99d1-270">False</span><span class="sxs-lookup"><span data-stu-id="c99d1-270">False</span></span>                           |
| <span data-ttu-id="c99d1-271">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c99d1-271">NT-Security-Descriptor</span></span> | <span data-ttu-id="c99d1-272">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c99d1-272">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c99d1-273">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c99d1-273">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c99d1-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c99d1-274">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c99d1-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c99d1-275">Search-Flags</span></span>           | <span data-ttu-id="c99d1-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c99d1-276">0x00000010</span></span>                      |
| <span data-ttu-id="c99d1-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c99d1-277">System-Flags</span></span>           | <span data-ttu-id="c99d1-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c99d1-278">0x00000010</span></span>                      |
| <span data-ttu-id="c99d1-279">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c99d1-279">Classes used in</span></span>        | [<span data-ttu-id="c99d1-280">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="c99d1-280">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c99d1-281">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c99d1-281">Windows Server 2012</span></span>



| <span data-ttu-id="c99d1-282">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c99d1-282">Entry</span></span> | <span data-ttu-id="c99d1-283">Wert</span><span class="sxs-lookup"><span data-stu-id="c99d1-283">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c99d1-284">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c99d1-284">Link-Id</span></span>                | <span data-ttu-id="c99d1-285">3</span><span class="sxs-lookup"><span data-stu-id="c99d1-285">3</span></span>                               |
| <span data-ttu-id="c99d1-286">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c99d1-286">MAPI-Id</span></span>                | <span data-ttu-id="c99d1-287">0x8008</span><span class="sxs-lookup"><span data-stu-id="c99d1-287">0x8008</span></span>                          |
| <span data-ttu-id="c99d1-288">System-Only</span><span class="sxs-lookup"><span data-stu-id="c99d1-288">System-Only</span></span>            | <span data-ttu-id="c99d1-289">Richtig</span><span class="sxs-lookup"><span data-stu-id="c99d1-289">True</span></span>                            |
| <span data-ttu-id="c99d1-290">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c99d1-290">Is-Single-Valued</span></span>       | <span data-ttu-id="c99d1-291">False</span><span class="sxs-lookup"><span data-stu-id="c99d1-291">False</span></span>                           |
| <span data-ttu-id="c99d1-292">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c99d1-292">Is Indexed</span></span>             | <span data-ttu-id="c99d1-293">False</span><span class="sxs-lookup"><span data-stu-id="c99d1-293">False</span></span>                           |
| <span data-ttu-id="c99d1-294">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c99d1-294">In Global Catalog</span></span>      | <span data-ttu-id="c99d1-295">False</span><span class="sxs-lookup"><span data-stu-id="c99d1-295">False</span></span>                           |
| <span data-ttu-id="c99d1-296">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c99d1-296">NT-Security-Descriptor</span></span> | <span data-ttu-id="c99d1-297">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c99d1-297">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c99d1-298">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c99d1-298">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c99d1-299">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c99d1-299">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c99d1-300">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c99d1-300">Search-Flags</span></span>           | <span data-ttu-id="c99d1-301">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c99d1-301">0x00000010</span></span>                      |
| <span data-ttu-id="c99d1-302">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c99d1-302">System-Flags</span></span>           | <span data-ttu-id="c99d1-303">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c99d1-303">0x00000010</span></span>                      |
| <span data-ttu-id="c99d1-304">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c99d1-304">Classes used in</span></span>        | [<span data-ttu-id="c99d1-305">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="c99d1-305">**Top**</span></span>](c-top.md)<br/> |



 

 





