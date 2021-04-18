---
title: Query-Policy-BL-Attribut
description: Liste aller Objekte, die Verweise auf eine bestimmte Abfrage Richtlinie enthalten.
ms.assetid: af421d00-2cc8-4ea1-8374-148db58c493b
ms.tgt_platform: multiple
keywords:
- AD-Schema für Abfrage-Policy-BL-Attribut
- querypolicybl-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Query-Policy-BL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 739abe3dbf67e5e8d154ef1424db81476f153858
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106343506"
---
# <a name="query-policy-bl-attribute"></a><span data-ttu-id="a7a19-105">Query-Policy-BL-Attribut</span><span class="sxs-lookup"><span data-stu-id="a7a19-105">Query-Policy-BL attribute</span></span>

<span data-ttu-id="a7a19-106">Liste aller Objekte, die Verweise auf eine bestimmte Abfrage Richtlinie enthalten.</span><span class="sxs-lookup"><span data-stu-id="a7a19-106">List of all objects holding references to a given Query-Policy.</span></span>



| <span data-ttu-id="a7a19-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a7a19-107">Entry</span></span> | <span data-ttu-id="a7a19-108">Wert</span><span class="sxs-lookup"><span data-stu-id="a7a19-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="a7a19-109">CN</span><span class="sxs-lookup"><span data-stu-id="a7a19-109">CN</span></span>                | <span data-ttu-id="a7a19-110">Abfrage-Richtlinie-BL</span><span class="sxs-lookup"><span data-stu-id="a7a19-110">Query-Policy-BL</span></span>                         |
| <span data-ttu-id="a7a19-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a7a19-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a7a19-112">querypolicybl</span><span class="sxs-lookup"><span data-stu-id="a7a19-112">queryPolicyBL</span></span>                           |
| <span data-ttu-id="a7a19-113">Size</span><span class="sxs-lookup"><span data-stu-id="a7a19-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="a7a19-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="a7a19-114">Update Privilege</span></span>  | <span data-ttu-id="a7a19-115">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a7a19-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="a7a19-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="a7a19-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="a7a19-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a7a19-117">Attribute-Id</span></span>      | <span data-ttu-id="a7a19-118">1.2.840.113556.1.4.608</span><span class="sxs-lookup"><span data-stu-id="a7a19-118">1.2.840.113556.1.4.608</span></span>                  |
| <span data-ttu-id="a7a19-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a7a19-119">System-Id-Guid</span></span>    | <span data-ttu-id="a7a19-120">e1aea404-cd5b-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a7a19-120">e1aea404-cd5b-11d0-afff-0000f80367c1</span></span>    |
| <span data-ttu-id="a7a19-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7a19-121">Syntax</span></span>            | [<span data-ttu-id="a7a19-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="a7a19-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="a7a19-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="a7a19-123">Implementations</span></span>

-   [<span data-ttu-id="a7a19-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a7a19-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a7a19-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a7a19-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a7a19-126">**Adam**</span><span class="sxs-lookup"><span data-stu-id="a7a19-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a7a19-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a7a19-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a7a19-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a7a19-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a7a19-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a7a19-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a7a19-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a7a19-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a7a19-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a7a19-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a7a19-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a7a19-132">Entry</span></span> | <span data-ttu-id="a7a19-133">Wert</span><span class="sxs-lookup"><span data-stu-id="a7a19-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a7a19-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a7a19-134">Link-Id</span></span>                | <span data-ttu-id="a7a19-135">69</span><span class="sxs-lookup"><span data-stu-id="a7a19-135">69</span></span>                              |
| <span data-ttu-id="a7a19-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7a19-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a7a19-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7a19-137">System-Only</span></span>            | <span data-ttu-id="a7a19-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="a7a19-138">True</span></span>                            |
| <span data-ttu-id="a7a19-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a7a19-139">Is-Single-Valued</span></span>       | <span data-ttu-id="a7a19-140">False</span><span class="sxs-lookup"><span data-stu-id="a7a19-140">False</span></span>                           |
| <span data-ttu-id="a7a19-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a7a19-141">Is Indexed</span></span>             | <span data-ttu-id="a7a19-142">False</span><span class="sxs-lookup"><span data-stu-id="a7a19-142">False</span></span>                           |
| <span data-ttu-id="a7a19-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a7a19-143">In Global Catalog</span></span>      | <span data-ttu-id="a7a19-144">False</span><span class="sxs-lookup"><span data-stu-id="a7a19-144">False</span></span>                           |
| <span data-ttu-id="a7a19-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a7a19-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7a19-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a7a19-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a7a19-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7a19-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a7a19-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7a19-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a7a19-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7a19-149">Search-Flags</span></span>           | <span data-ttu-id="a7a19-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7a19-150">0x00000000</span></span>                      |
| <span data-ttu-id="a7a19-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7a19-151">System-Flags</span></span>           | <span data-ttu-id="a7a19-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7a19-152">0x00000010</span></span>                      |
| <span data-ttu-id="a7a19-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a7a19-153">Classes used in</span></span>        | [<span data-ttu-id="a7a19-154">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a7a19-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a7a19-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a7a19-155">Windows Server 2003</span></span>



| <span data-ttu-id="a7a19-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a7a19-156">Entry</span></span> | <span data-ttu-id="a7a19-157">Wert</span><span class="sxs-lookup"><span data-stu-id="a7a19-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a7a19-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a7a19-158">Link-Id</span></span>                | <span data-ttu-id="a7a19-159">69</span><span class="sxs-lookup"><span data-stu-id="a7a19-159">69</span></span>                              |
| <span data-ttu-id="a7a19-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7a19-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a7a19-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7a19-161">System-Only</span></span>            | <span data-ttu-id="a7a19-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="a7a19-162">True</span></span>                            |
| <span data-ttu-id="a7a19-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a7a19-163">Is-Single-Valued</span></span>       | <span data-ttu-id="a7a19-164">False</span><span class="sxs-lookup"><span data-stu-id="a7a19-164">False</span></span>                           |
| <span data-ttu-id="a7a19-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a7a19-165">Is Indexed</span></span>             | <span data-ttu-id="a7a19-166">False</span><span class="sxs-lookup"><span data-stu-id="a7a19-166">False</span></span>                           |
| <span data-ttu-id="a7a19-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a7a19-167">In Global Catalog</span></span>      | <span data-ttu-id="a7a19-168">False</span><span class="sxs-lookup"><span data-stu-id="a7a19-168">False</span></span>                           |
| <span data-ttu-id="a7a19-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a7a19-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7a19-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a7a19-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a7a19-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7a19-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a7a19-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7a19-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a7a19-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7a19-173">Search-Flags</span></span>           | <span data-ttu-id="a7a19-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7a19-174">0x00000000</span></span>                      |
| <span data-ttu-id="a7a19-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7a19-175">System-Flags</span></span>           | <span data-ttu-id="a7a19-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7a19-176">0x00000010</span></span>                      |
| <span data-ttu-id="a7a19-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a7a19-177">Classes used in</span></span>        | [<span data-ttu-id="a7a19-178">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a7a19-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a7a19-179">Adam</span><span class="sxs-lookup"><span data-stu-id="a7a19-179">ADAM</span></span>



| <span data-ttu-id="a7a19-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a7a19-180">Entry</span></span> | <span data-ttu-id="a7a19-181">Wert</span><span class="sxs-lookup"><span data-stu-id="a7a19-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a7a19-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a7a19-182">Link-Id</span></span>                | <span data-ttu-id="a7a19-183">69</span><span class="sxs-lookup"><span data-stu-id="a7a19-183">69</span></span>                              |
| <span data-ttu-id="a7a19-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7a19-184">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a7a19-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7a19-185">System-Only</span></span>            | <span data-ttu-id="a7a19-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="a7a19-186">True</span></span>                            |
| <span data-ttu-id="a7a19-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a7a19-187">Is-Single-Valued</span></span>       | <span data-ttu-id="a7a19-188">False</span><span class="sxs-lookup"><span data-stu-id="a7a19-188">False</span></span>                           |
| <span data-ttu-id="a7a19-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a7a19-189">Is Indexed</span></span>             | <span data-ttu-id="a7a19-190">False</span><span class="sxs-lookup"><span data-stu-id="a7a19-190">False</span></span>                           |
| <span data-ttu-id="a7a19-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a7a19-191">In Global Catalog</span></span>      | <span data-ttu-id="a7a19-192">False</span><span class="sxs-lookup"><span data-stu-id="a7a19-192">False</span></span>                           |
| <span data-ttu-id="a7a19-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a7a19-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7a19-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a7a19-194">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a7a19-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7a19-195">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a7a19-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7a19-196">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a7a19-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7a19-197">Search-Flags</span></span>           | <span data-ttu-id="a7a19-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7a19-198">0x00000000</span></span>                      |
| <span data-ttu-id="a7a19-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7a19-199">System-Flags</span></span>           | <span data-ttu-id="a7a19-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7a19-200">0x00000010</span></span>                      |
| <span data-ttu-id="a7a19-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a7a19-201">Classes used in</span></span>        | [<span data-ttu-id="a7a19-202">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a7a19-202">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a7a19-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a7a19-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a7a19-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a7a19-204">Entry</span></span> | <span data-ttu-id="a7a19-205">Wert</span><span class="sxs-lookup"><span data-stu-id="a7a19-205">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a7a19-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a7a19-206">Link-Id</span></span>                | <span data-ttu-id="a7a19-207">69</span><span class="sxs-lookup"><span data-stu-id="a7a19-207">69</span></span>                              |
| <span data-ttu-id="a7a19-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7a19-208">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a7a19-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7a19-209">System-Only</span></span>            | <span data-ttu-id="a7a19-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="a7a19-210">True</span></span>                            |
| <span data-ttu-id="a7a19-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a7a19-211">Is-Single-Valued</span></span>       | <span data-ttu-id="a7a19-212">False</span><span class="sxs-lookup"><span data-stu-id="a7a19-212">False</span></span>                           |
| <span data-ttu-id="a7a19-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a7a19-213">Is Indexed</span></span>             | <span data-ttu-id="a7a19-214">False</span><span class="sxs-lookup"><span data-stu-id="a7a19-214">False</span></span>                           |
| <span data-ttu-id="a7a19-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a7a19-215">In Global Catalog</span></span>      | <span data-ttu-id="a7a19-216">False</span><span class="sxs-lookup"><span data-stu-id="a7a19-216">False</span></span>                           |
| <span data-ttu-id="a7a19-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a7a19-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7a19-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a7a19-218">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a7a19-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7a19-219">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a7a19-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7a19-220">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a7a19-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7a19-221">Search-Flags</span></span>           | <span data-ttu-id="a7a19-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7a19-222">0x00000000</span></span>                      |
| <span data-ttu-id="a7a19-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7a19-223">System-Flags</span></span>           | <span data-ttu-id="a7a19-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7a19-224">0x00000010</span></span>                      |
| <span data-ttu-id="a7a19-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a7a19-225">Classes used in</span></span>        | [<span data-ttu-id="a7a19-226">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a7a19-226">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a7a19-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7a19-227">Windows Server 2008</span></span>



| <span data-ttu-id="a7a19-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a7a19-228">Entry</span></span> | <span data-ttu-id="a7a19-229">Wert</span><span class="sxs-lookup"><span data-stu-id="a7a19-229">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a7a19-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a7a19-230">Link-Id</span></span>                | <span data-ttu-id="a7a19-231">69</span><span class="sxs-lookup"><span data-stu-id="a7a19-231">69</span></span>                              |
| <span data-ttu-id="a7a19-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7a19-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a7a19-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7a19-233">System-Only</span></span>            | <span data-ttu-id="a7a19-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="a7a19-234">True</span></span>                            |
| <span data-ttu-id="a7a19-235">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a7a19-235">Is-Single-Valued</span></span>       | <span data-ttu-id="a7a19-236">False</span><span class="sxs-lookup"><span data-stu-id="a7a19-236">False</span></span>                           |
| <span data-ttu-id="a7a19-237">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a7a19-237">Is Indexed</span></span>             | <span data-ttu-id="a7a19-238">False</span><span class="sxs-lookup"><span data-stu-id="a7a19-238">False</span></span>                           |
| <span data-ttu-id="a7a19-239">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a7a19-239">In Global Catalog</span></span>      | <span data-ttu-id="a7a19-240">False</span><span class="sxs-lookup"><span data-stu-id="a7a19-240">False</span></span>                           |
| <span data-ttu-id="a7a19-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a7a19-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7a19-242">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a7a19-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a7a19-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7a19-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a7a19-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7a19-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a7a19-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7a19-245">Search-Flags</span></span>           | <span data-ttu-id="a7a19-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7a19-246">0x00000000</span></span>                      |
| <span data-ttu-id="a7a19-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7a19-247">System-Flags</span></span>           | <span data-ttu-id="a7a19-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7a19-248">0x00000010</span></span>                      |
| <span data-ttu-id="a7a19-249">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a7a19-249">Classes used in</span></span>        | [<span data-ttu-id="a7a19-250">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a7a19-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a7a19-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a7a19-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a7a19-252">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a7a19-252">Entry</span></span> | <span data-ttu-id="a7a19-253">Wert</span><span class="sxs-lookup"><span data-stu-id="a7a19-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a7a19-254">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a7a19-254">Link-Id</span></span>                | <span data-ttu-id="a7a19-255">69</span><span class="sxs-lookup"><span data-stu-id="a7a19-255">69</span></span>                              |
| <span data-ttu-id="a7a19-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7a19-256">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a7a19-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7a19-257">System-Only</span></span>            | <span data-ttu-id="a7a19-258">Richtig</span><span class="sxs-lookup"><span data-stu-id="a7a19-258">True</span></span>                            |
| <span data-ttu-id="a7a19-259">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a7a19-259">Is-Single-Valued</span></span>       | <span data-ttu-id="a7a19-260">False</span><span class="sxs-lookup"><span data-stu-id="a7a19-260">False</span></span>                           |
| <span data-ttu-id="a7a19-261">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a7a19-261">Is Indexed</span></span>             | <span data-ttu-id="a7a19-262">False</span><span class="sxs-lookup"><span data-stu-id="a7a19-262">False</span></span>                           |
| <span data-ttu-id="a7a19-263">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a7a19-263">In Global Catalog</span></span>      | <span data-ttu-id="a7a19-264">False</span><span class="sxs-lookup"><span data-stu-id="a7a19-264">False</span></span>                           |
| <span data-ttu-id="a7a19-265">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a7a19-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7a19-266">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a7a19-266">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a7a19-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7a19-267">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a7a19-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7a19-268">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a7a19-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7a19-269">Search-Flags</span></span>           | <span data-ttu-id="a7a19-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7a19-270">0x00000000</span></span>                      |
| <span data-ttu-id="a7a19-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7a19-271">System-Flags</span></span>           | <span data-ttu-id="a7a19-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7a19-272">0x00000010</span></span>                      |
| <span data-ttu-id="a7a19-273">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a7a19-273">Classes used in</span></span>        | [<span data-ttu-id="a7a19-274">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a7a19-274">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a7a19-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a7a19-275">Windows Server 2012</span></span>



| <span data-ttu-id="a7a19-276">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a7a19-276">Entry</span></span> | <span data-ttu-id="a7a19-277">Wert</span><span class="sxs-lookup"><span data-stu-id="a7a19-277">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a7a19-278">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a7a19-278">Link-Id</span></span>                | <span data-ttu-id="a7a19-279">69</span><span class="sxs-lookup"><span data-stu-id="a7a19-279">69</span></span>                              |
| <span data-ttu-id="a7a19-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7a19-280">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a7a19-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7a19-281">System-Only</span></span>            | <span data-ttu-id="a7a19-282">Richtig</span><span class="sxs-lookup"><span data-stu-id="a7a19-282">True</span></span>                            |
| <span data-ttu-id="a7a19-283">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a7a19-283">Is-Single-Valued</span></span>       | <span data-ttu-id="a7a19-284">False</span><span class="sxs-lookup"><span data-stu-id="a7a19-284">False</span></span>                           |
| <span data-ttu-id="a7a19-285">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a7a19-285">Is Indexed</span></span>             | <span data-ttu-id="a7a19-286">False</span><span class="sxs-lookup"><span data-stu-id="a7a19-286">False</span></span>                           |
| <span data-ttu-id="a7a19-287">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a7a19-287">In Global Catalog</span></span>      | <span data-ttu-id="a7a19-288">False</span><span class="sxs-lookup"><span data-stu-id="a7a19-288">False</span></span>                           |
| <span data-ttu-id="a7a19-289">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a7a19-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7a19-290">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a7a19-290">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a7a19-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7a19-291">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a7a19-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7a19-292">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a7a19-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7a19-293">Search-Flags</span></span>           | <span data-ttu-id="a7a19-294">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7a19-294">0x00000000</span></span>                      |
| <span data-ttu-id="a7a19-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7a19-295">System-Flags</span></span>           | <span data-ttu-id="a7a19-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7a19-296">0x00000010</span></span>                      |
| <span data-ttu-id="a7a19-297">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a7a19-297">Classes used in</span></span>        | [<span data-ttu-id="a7a19-298">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a7a19-298">**Top**</span></span>](c-top.md)<br/> |



 

 





