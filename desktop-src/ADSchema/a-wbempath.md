---
title: Wbem-Path-Attribut
description: Verweise auf Objekte in anderen ADSI-Namespaces.
ms.assetid: d659029b-f929-4810-a369-d6d1062b33b8
ms.tgt_platform: multiple
keywords:
- AD-Schema für Wbem-Path-Attribut
- AD-Schema für wbempath-Attribut
topic_type:
- apiref
api_name:
- Wbem-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06bf3628ff9f44f1a928ca88c6bb8af62f61af91
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479543"
---
# <a name="wbem-path-attribute"></a><span data-ttu-id="b01fe-105">Wbem-Path-Attribut</span><span class="sxs-lookup"><span data-stu-id="b01fe-105">Wbem-Path attribute</span></span>

<span data-ttu-id="b01fe-106">Verweise auf Objekte in anderen ADSI-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="b01fe-106">References to objects in other ADSI namespaces.</span></span>



| <span data-ttu-id="b01fe-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b01fe-107">Entry</span></span> | <span data-ttu-id="b01fe-108">Wert</span><span class="sxs-lookup"><span data-stu-id="b01fe-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b01fe-109">CN</span><span class="sxs-lookup"><span data-stu-id="b01fe-109">CN</span></span>                | <span data-ttu-id="b01fe-110">Wbem-Path</span><span class="sxs-lookup"><span data-stu-id="b01fe-110">Wbem-Path</span></span>                                   |
| <span data-ttu-id="b01fe-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b01fe-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b01fe-112">wbempath</span><span class="sxs-lookup"><span data-stu-id="b01fe-112">wbemPath</span></span>                                    |
| <span data-ttu-id="b01fe-113">Size</span><span class="sxs-lookup"><span data-stu-id="b01fe-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="b01fe-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b01fe-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="b01fe-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="b01fe-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="b01fe-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b01fe-116">Attribute-Id</span></span>      | <span data-ttu-id="b01fe-117">1.2.840.113556.1.4.301</span><span class="sxs-lookup"><span data-stu-id="b01fe-117">1.2.840.113556.1.4.301</span></span>                      |
| <span data-ttu-id="b01fe-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b01fe-118">System-Id-Guid</span></span>    | <span data-ttu-id="b01fe-119">244b2970-5abd-11D0-afd2-00c04f 930c9</span><span class="sxs-lookup"><span data-stu-id="b01fe-119">244b2970-5abd-11d0-afd2-00c04fd930c9</span></span>        |
| <span data-ttu-id="b01fe-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="b01fe-120">Syntax</span></span>            | [<span data-ttu-id="b01fe-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b01fe-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b01fe-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="b01fe-122">Implementations</span></span>

-   [<span data-ttu-id="b01fe-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b01fe-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b01fe-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b01fe-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b01fe-125">**Adam**</span><span class="sxs-lookup"><span data-stu-id="b01fe-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b01fe-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b01fe-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b01fe-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b01fe-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b01fe-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b01fe-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b01fe-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b01fe-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b01fe-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b01fe-130">Windows 2000 Server</span></span>



| <span data-ttu-id="b01fe-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b01fe-131">Entry</span></span> | <span data-ttu-id="b01fe-132">Wert</span><span class="sxs-lookup"><span data-stu-id="b01fe-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b01fe-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b01fe-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b01fe-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b01fe-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b01fe-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="b01fe-135">System-Only</span></span>            | <span data-ttu-id="b01fe-136">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-136">False</span></span>                           |
| <span data-ttu-id="b01fe-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b01fe-137">Is-Single-Valued</span></span>       | <span data-ttu-id="b01fe-138">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-138">False</span></span>                           |
| <span data-ttu-id="b01fe-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b01fe-139">Is Indexed</span></span>             | <span data-ttu-id="b01fe-140">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-140">False</span></span>                           |
| <span data-ttu-id="b01fe-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b01fe-141">In Global Catalog</span></span>      | <span data-ttu-id="b01fe-142">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-142">False</span></span>                           |
| <span data-ttu-id="b01fe-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b01fe-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="b01fe-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b01fe-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b01fe-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b01fe-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b01fe-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b01fe-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b01fe-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fe-147">Search-Flags</span></span>           | <span data-ttu-id="b01fe-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b01fe-148">0x00000000</span></span>                      |
| <span data-ttu-id="b01fe-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fe-149">System-Flags</span></span>           | <span data-ttu-id="b01fe-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b01fe-150">0x00000010</span></span>                      |
| <span data-ttu-id="b01fe-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b01fe-151">Classes used in</span></span>        | [<span data-ttu-id="b01fe-152">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b01fe-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b01fe-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b01fe-153">Windows Server 2003</span></span>



| <span data-ttu-id="b01fe-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b01fe-154">Entry</span></span> | <span data-ttu-id="b01fe-155">Wert</span><span class="sxs-lookup"><span data-stu-id="b01fe-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b01fe-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b01fe-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b01fe-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b01fe-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b01fe-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="b01fe-158">System-Only</span></span>            | <span data-ttu-id="b01fe-159">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-159">False</span></span>                           |
| <span data-ttu-id="b01fe-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b01fe-160">Is-Single-Valued</span></span>       | <span data-ttu-id="b01fe-161">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-161">False</span></span>                           |
| <span data-ttu-id="b01fe-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b01fe-162">Is Indexed</span></span>             | <span data-ttu-id="b01fe-163">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-163">False</span></span>                           |
| <span data-ttu-id="b01fe-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b01fe-164">In Global Catalog</span></span>      | <span data-ttu-id="b01fe-165">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-165">False</span></span>                           |
| <span data-ttu-id="b01fe-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b01fe-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="b01fe-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b01fe-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b01fe-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b01fe-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b01fe-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b01fe-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b01fe-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fe-170">Search-Flags</span></span>           | <span data-ttu-id="b01fe-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b01fe-171">0x00000000</span></span>                      |
| <span data-ttu-id="b01fe-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fe-172">System-Flags</span></span>           | <span data-ttu-id="b01fe-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b01fe-173">0x00000010</span></span>                      |
| <span data-ttu-id="b01fe-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b01fe-174">Classes used in</span></span>        | [<span data-ttu-id="b01fe-175">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b01fe-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b01fe-176">Adam</span><span class="sxs-lookup"><span data-stu-id="b01fe-176">ADAM</span></span>



| <span data-ttu-id="b01fe-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b01fe-177">Entry</span></span> | <span data-ttu-id="b01fe-178">Wert</span><span class="sxs-lookup"><span data-stu-id="b01fe-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b01fe-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b01fe-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b01fe-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b01fe-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b01fe-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="b01fe-181">System-Only</span></span>            | <span data-ttu-id="b01fe-182">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-182">False</span></span>                           |
| <span data-ttu-id="b01fe-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b01fe-183">Is-Single-Valued</span></span>       | <span data-ttu-id="b01fe-184">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-184">False</span></span>                           |
| <span data-ttu-id="b01fe-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b01fe-185">Is Indexed</span></span>             | <span data-ttu-id="b01fe-186">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-186">False</span></span>                           |
| <span data-ttu-id="b01fe-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b01fe-187">In Global Catalog</span></span>      | <span data-ttu-id="b01fe-188">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-188">False</span></span>                           |
| <span data-ttu-id="b01fe-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b01fe-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="b01fe-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b01fe-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b01fe-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b01fe-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b01fe-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b01fe-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b01fe-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fe-193">Search-Flags</span></span>           | <span data-ttu-id="b01fe-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b01fe-194">0x00000000</span></span>                      |
| <span data-ttu-id="b01fe-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fe-195">System-Flags</span></span>           | <span data-ttu-id="b01fe-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b01fe-196">0x00000010</span></span>                      |
| <span data-ttu-id="b01fe-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b01fe-197">Classes used in</span></span>        | [<span data-ttu-id="b01fe-198">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b01fe-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b01fe-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b01fe-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b01fe-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b01fe-200">Entry</span></span> | <span data-ttu-id="b01fe-201">Wert</span><span class="sxs-lookup"><span data-stu-id="b01fe-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b01fe-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b01fe-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b01fe-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b01fe-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b01fe-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="b01fe-204">System-Only</span></span>            | <span data-ttu-id="b01fe-205">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-205">False</span></span>                           |
| <span data-ttu-id="b01fe-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b01fe-206">Is-Single-Valued</span></span>       | <span data-ttu-id="b01fe-207">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-207">False</span></span>                           |
| <span data-ttu-id="b01fe-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b01fe-208">Is Indexed</span></span>             | <span data-ttu-id="b01fe-209">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-209">False</span></span>                           |
| <span data-ttu-id="b01fe-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b01fe-210">In Global Catalog</span></span>      | <span data-ttu-id="b01fe-211">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-211">False</span></span>                           |
| <span data-ttu-id="b01fe-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b01fe-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="b01fe-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b01fe-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b01fe-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b01fe-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b01fe-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b01fe-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b01fe-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fe-216">Search-Flags</span></span>           | <span data-ttu-id="b01fe-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b01fe-217">0x00000000</span></span>                      |
| <span data-ttu-id="b01fe-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fe-218">System-Flags</span></span>           | <span data-ttu-id="b01fe-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b01fe-219">0x00000010</span></span>                      |
| <span data-ttu-id="b01fe-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b01fe-220">Classes used in</span></span>        | [<span data-ttu-id="b01fe-221">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b01fe-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b01fe-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b01fe-222">Windows Server 2008</span></span>



| <span data-ttu-id="b01fe-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b01fe-223">Entry</span></span> | <span data-ttu-id="b01fe-224">Wert</span><span class="sxs-lookup"><span data-stu-id="b01fe-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b01fe-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b01fe-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b01fe-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b01fe-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b01fe-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="b01fe-227">System-Only</span></span>            | <span data-ttu-id="b01fe-228">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-228">False</span></span>                           |
| <span data-ttu-id="b01fe-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b01fe-229">Is-Single-Valued</span></span>       | <span data-ttu-id="b01fe-230">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-230">False</span></span>                           |
| <span data-ttu-id="b01fe-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b01fe-231">Is Indexed</span></span>             | <span data-ttu-id="b01fe-232">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-232">False</span></span>                           |
| <span data-ttu-id="b01fe-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b01fe-233">In Global Catalog</span></span>      | <span data-ttu-id="b01fe-234">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-234">False</span></span>                           |
| <span data-ttu-id="b01fe-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b01fe-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="b01fe-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b01fe-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b01fe-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b01fe-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b01fe-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b01fe-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b01fe-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fe-239">Search-Flags</span></span>           | <span data-ttu-id="b01fe-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b01fe-240">0x00000000</span></span>                      |
| <span data-ttu-id="b01fe-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fe-241">System-Flags</span></span>           | <span data-ttu-id="b01fe-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b01fe-242">0x00000010</span></span>                      |
| <span data-ttu-id="b01fe-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b01fe-243">Classes used in</span></span>        | [<span data-ttu-id="b01fe-244">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b01fe-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b01fe-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b01fe-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b01fe-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b01fe-246">Entry</span></span> | <span data-ttu-id="b01fe-247">Wert</span><span class="sxs-lookup"><span data-stu-id="b01fe-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b01fe-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b01fe-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b01fe-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b01fe-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b01fe-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="b01fe-250">System-Only</span></span>            | <span data-ttu-id="b01fe-251">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-251">False</span></span>                           |
| <span data-ttu-id="b01fe-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b01fe-252">Is-Single-Valued</span></span>       | <span data-ttu-id="b01fe-253">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-253">False</span></span>                           |
| <span data-ttu-id="b01fe-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b01fe-254">Is Indexed</span></span>             | <span data-ttu-id="b01fe-255">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-255">False</span></span>                           |
| <span data-ttu-id="b01fe-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b01fe-256">In Global Catalog</span></span>      | <span data-ttu-id="b01fe-257">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-257">False</span></span>                           |
| <span data-ttu-id="b01fe-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b01fe-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="b01fe-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b01fe-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b01fe-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b01fe-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b01fe-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b01fe-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b01fe-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fe-262">Search-Flags</span></span>           | <span data-ttu-id="b01fe-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b01fe-263">0x00000000</span></span>                      |
| <span data-ttu-id="b01fe-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fe-264">System-Flags</span></span>           | <span data-ttu-id="b01fe-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b01fe-265">0x00000010</span></span>                      |
| <span data-ttu-id="b01fe-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b01fe-266">Classes used in</span></span>        | [<span data-ttu-id="b01fe-267">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b01fe-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b01fe-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b01fe-268">Windows Server 2012</span></span>



| <span data-ttu-id="b01fe-269">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b01fe-269">Entry</span></span> | <span data-ttu-id="b01fe-270">Wert</span><span class="sxs-lookup"><span data-stu-id="b01fe-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b01fe-271">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b01fe-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b01fe-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b01fe-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b01fe-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="b01fe-273">System-Only</span></span>            | <span data-ttu-id="b01fe-274">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-274">False</span></span>                           |
| <span data-ttu-id="b01fe-275">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b01fe-275">Is-Single-Valued</span></span>       | <span data-ttu-id="b01fe-276">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-276">False</span></span>                           |
| <span data-ttu-id="b01fe-277">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b01fe-277">Is Indexed</span></span>             | <span data-ttu-id="b01fe-278">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-278">False</span></span>                           |
| <span data-ttu-id="b01fe-279">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b01fe-279">In Global Catalog</span></span>      | <span data-ttu-id="b01fe-280">False</span><span class="sxs-lookup"><span data-stu-id="b01fe-280">False</span></span>                           |
| <span data-ttu-id="b01fe-281">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b01fe-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="b01fe-282">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b01fe-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b01fe-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b01fe-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b01fe-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b01fe-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b01fe-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fe-285">Search-Flags</span></span>           | <span data-ttu-id="b01fe-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b01fe-286">0x00000000</span></span>                      |
| <span data-ttu-id="b01fe-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fe-287">System-Flags</span></span>           | <span data-ttu-id="b01fe-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b01fe-288">0x00000010</span></span>                      |
| <span data-ttu-id="b01fe-289">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b01fe-289">Classes used in</span></span>        | [<span data-ttu-id="b01fe-290">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b01fe-290">**Top**</span></span>](c-top.md)<br/> |



 

 





