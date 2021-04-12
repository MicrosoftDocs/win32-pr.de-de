---
title: Flat-Name-Attribut
description: Bei Windows NT-Domänen ist der flache Name der NetBIOS-Name. Für Links mit nicht \ 8211; Windows NT-Domänen, der flache Name ist der identifizierende Name dieser Domäne, oder der Name ist NULL.
ms.assetid: ec368657-a0e7-4416-ab80-1d18d98bbcfa
ms.tgt_platform: multiple
keywords:
- AD-Schema für Flat-Name-Attribut
- flatname-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Flat-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 373ee0736c051932fdb6dd20701f0c5ec353ad3b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479791"
---
# <a name="flat-name-attribute"></a><span data-ttu-id="06235-106">Flat-Name-Attribut</span><span class="sxs-lookup"><span data-stu-id="06235-106">Flat-Name attribute</span></span>

<span data-ttu-id="06235-107">Bei Windows NT-Domänen ist der flache Name der NetBIOS-Name.</span><span class="sxs-lookup"><span data-stu-id="06235-107">For Windows NT domains, the flat name is the NetBIOS name.</span></span> <span data-ttu-id="06235-108">Für Verknüpfungen mit nicht-Windows NT-Domänen ist der flache Name der identifizierende Name dieser Domäne, oder der Name ist **null**.</span><span class="sxs-lookup"><span data-stu-id="06235-108">For links with non Windows NT domains, the flat name is the identifying name of that domain, or it is **NULL**.</span></span>



| <span data-ttu-id="06235-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="06235-109">Entry</span></span> | <span data-ttu-id="06235-110">Wert</span><span class="sxs-lookup"><span data-stu-id="06235-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="06235-111">CN</span><span class="sxs-lookup"><span data-stu-id="06235-111">CN</span></span>                | <span data-ttu-id="06235-112">Flat-Name</span><span class="sxs-lookup"><span data-stu-id="06235-112">Flat-Name</span></span>                                   |
| <span data-ttu-id="06235-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="06235-113">Ldap-Display-Name</span></span> | <span data-ttu-id="06235-114">flatname</span><span class="sxs-lookup"><span data-stu-id="06235-114">flatName</span></span>                                    |
| <span data-ttu-id="06235-115">Size</span><span class="sxs-lookup"><span data-stu-id="06235-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="06235-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="06235-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="06235-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="06235-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="06235-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="06235-118">Attribute-Id</span></span>      | <span data-ttu-id="06235-119">1.2.840.113556.1.4.511</span><span class="sxs-lookup"><span data-stu-id="06235-119">1.2.840.113556.1.4.511</span></span>                      |
| <span data-ttu-id="06235-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="06235-120">System-Id-Guid</span></span>    | <span data-ttu-id="06235-121">b7b13117-b82e-11d0-afee-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="06235-121">b7b13117-b82e-11d0-afee-0000f80367c1</span></span>        |
| <span data-ttu-id="06235-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="06235-122">Syntax</span></span>            | [<span data-ttu-id="06235-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="06235-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="06235-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="06235-124">Implementations</span></span>

-   [<span data-ttu-id="06235-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="06235-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="06235-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="06235-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="06235-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="06235-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="06235-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="06235-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="06235-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="06235-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="06235-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="06235-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="06235-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="06235-131">Windows 2000 Server</span></span>



| <span data-ttu-id="06235-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="06235-132">Entry</span></span> | <span data-ttu-id="06235-133">Wert</span><span class="sxs-lookup"><span data-stu-id="06235-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="06235-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="06235-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="06235-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06235-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="06235-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="06235-136">System-Only</span></span>            | <span data-ttu-id="06235-137">False</span><span class="sxs-lookup"><span data-stu-id="06235-137">False</span></span>                                                |
| <span data-ttu-id="06235-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="06235-138">Is-Single-Valued</span></span>       | <span data-ttu-id="06235-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="06235-139">True</span></span>                                                 |
| <span data-ttu-id="06235-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="06235-140">Is Indexed</span></span>             | <span data-ttu-id="06235-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="06235-141">True</span></span>                                                 |
| <span data-ttu-id="06235-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="06235-142">In Global Catalog</span></span>      | <span data-ttu-id="06235-143">False</span><span class="sxs-lookup"><span data-stu-id="06235-143">False</span></span>                                                |
| <span data-ttu-id="06235-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06235-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="06235-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="06235-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="06235-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06235-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="06235-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06235-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="06235-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06235-148">Search-Flags</span></span>           | <span data-ttu-id="06235-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="06235-149">0x00000001</span></span>                                           |
| <span data-ttu-id="06235-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06235-150">System-Flags</span></span>           | <span data-ttu-id="06235-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06235-151">0x00000010</span></span>                                           |
| <span data-ttu-id="06235-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="06235-152">Classes used in</span></span>        | [<span data-ttu-id="06235-153">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="06235-153">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="06235-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="06235-154">Windows Server 2003</span></span>



| <span data-ttu-id="06235-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="06235-155">Entry</span></span> | <span data-ttu-id="06235-156">Wert</span><span class="sxs-lookup"><span data-stu-id="06235-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="06235-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="06235-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="06235-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06235-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="06235-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="06235-159">System-Only</span></span>            | <span data-ttu-id="06235-160">False</span><span class="sxs-lookup"><span data-stu-id="06235-160">False</span></span>                                                |
| <span data-ttu-id="06235-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="06235-161">Is-Single-Valued</span></span>       | <span data-ttu-id="06235-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="06235-162">True</span></span>                                                 |
| <span data-ttu-id="06235-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="06235-163">Is Indexed</span></span>             | <span data-ttu-id="06235-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="06235-164">True</span></span>                                                 |
| <span data-ttu-id="06235-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="06235-165">In Global Catalog</span></span>      | <span data-ttu-id="06235-166">False</span><span class="sxs-lookup"><span data-stu-id="06235-166">False</span></span>                                                |
| <span data-ttu-id="06235-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06235-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="06235-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="06235-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="06235-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06235-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="06235-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06235-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="06235-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06235-171">Search-Flags</span></span>           | <span data-ttu-id="06235-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="06235-172">0x00000001</span></span>                                           |
| <span data-ttu-id="06235-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06235-173">System-Flags</span></span>           | <span data-ttu-id="06235-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06235-174">0x00000010</span></span>                                           |
| <span data-ttu-id="06235-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="06235-175">Classes used in</span></span>        | [<span data-ttu-id="06235-176">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="06235-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="06235-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="06235-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="06235-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="06235-178">Entry</span></span> | <span data-ttu-id="06235-179">Wert</span><span class="sxs-lookup"><span data-stu-id="06235-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="06235-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="06235-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="06235-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06235-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="06235-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="06235-182">System-Only</span></span>            | <span data-ttu-id="06235-183">False</span><span class="sxs-lookup"><span data-stu-id="06235-183">False</span></span>                                                |
| <span data-ttu-id="06235-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="06235-184">Is-Single-Valued</span></span>       | <span data-ttu-id="06235-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="06235-185">True</span></span>                                                 |
| <span data-ttu-id="06235-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="06235-186">Is Indexed</span></span>             | <span data-ttu-id="06235-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="06235-187">True</span></span>                                                 |
| <span data-ttu-id="06235-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="06235-188">In Global Catalog</span></span>      | <span data-ttu-id="06235-189">False</span><span class="sxs-lookup"><span data-stu-id="06235-189">False</span></span>                                                |
| <span data-ttu-id="06235-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06235-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="06235-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="06235-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="06235-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06235-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="06235-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06235-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="06235-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06235-194">Search-Flags</span></span>           | <span data-ttu-id="06235-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="06235-195">0x00000001</span></span>                                           |
| <span data-ttu-id="06235-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06235-196">System-Flags</span></span>           | <span data-ttu-id="06235-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06235-197">0x00000010</span></span>                                           |
| <span data-ttu-id="06235-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="06235-198">Classes used in</span></span>        | [<span data-ttu-id="06235-199">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="06235-199">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="06235-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06235-200">Windows Server 2008</span></span>



| <span data-ttu-id="06235-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="06235-201">Entry</span></span> | <span data-ttu-id="06235-202">Wert</span><span class="sxs-lookup"><span data-stu-id="06235-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="06235-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="06235-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="06235-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06235-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="06235-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="06235-205">System-Only</span></span>            | <span data-ttu-id="06235-206">False</span><span class="sxs-lookup"><span data-stu-id="06235-206">False</span></span>                                                |
| <span data-ttu-id="06235-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="06235-207">Is-Single-Valued</span></span>       | <span data-ttu-id="06235-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="06235-208">True</span></span>                                                 |
| <span data-ttu-id="06235-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="06235-209">Is Indexed</span></span>             | <span data-ttu-id="06235-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="06235-210">True</span></span>                                                 |
| <span data-ttu-id="06235-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="06235-211">In Global Catalog</span></span>      | <span data-ttu-id="06235-212">False</span><span class="sxs-lookup"><span data-stu-id="06235-212">False</span></span>                                                |
| <span data-ttu-id="06235-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06235-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="06235-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="06235-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="06235-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06235-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="06235-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06235-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="06235-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06235-217">Search-Flags</span></span>           | <span data-ttu-id="06235-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="06235-218">0x00000001</span></span>                                           |
| <span data-ttu-id="06235-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06235-219">System-Flags</span></span>           | <span data-ttu-id="06235-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06235-220">0x00000010</span></span>                                           |
| <span data-ttu-id="06235-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="06235-221">Classes used in</span></span>        | [<span data-ttu-id="06235-222">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="06235-222">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="06235-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="06235-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="06235-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="06235-224">Entry</span></span> | <span data-ttu-id="06235-225">Wert</span><span class="sxs-lookup"><span data-stu-id="06235-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="06235-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="06235-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="06235-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06235-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="06235-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="06235-228">System-Only</span></span>            | <span data-ttu-id="06235-229">False</span><span class="sxs-lookup"><span data-stu-id="06235-229">False</span></span>                                                |
| <span data-ttu-id="06235-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="06235-230">Is-Single-Valued</span></span>       | <span data-ttu-id="06235-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="06235-231">True</span></span>                                                 |
| <span data-ttu-id="06235-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="06235-232">Is Indexed</span></span>             | <span data-ttu-id="06235-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="06235-233">True</span></span>                                                 |
| <span data-ttu-id="06235-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="06235-234">In Global Catalog</span></span>      | <span data-ttu-id="06235-235">False</span><span class="sxs-lookup"><span data-stu-id="06235-235">False</span></span>                                                |
| <span data-ttu-id="06235-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06235-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="06235-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="06235-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="06235-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06235-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="06235-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06235-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="06235-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06235-240">Search-Flags</span></span>           | <span data-ttu-id="06235-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="06235-241">0x00000001</span></span>                                           |
| <span data-ttu-id="06235-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06235-242">System-Flags</span></span>           | <span data-ttu-id="06235-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06235-243">0x00000010</span></span>                                           |
| <span data-ttu-id="06235-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="06235-244">Classes used in</span></span>        | [<span data-ttu-id="06235-245">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="06235-245">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="06235-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="06235-246">Windows Server 2012</span></span>



| <span data-ttu-id="06235-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="06235-247">Entry</span></span> | <span data-ttu-id="06235-248">Wert</span><span class="sxs-lookup"><span data-stu-id="06235-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="06235-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="06235-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="06235-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06235-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="06235-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="06235-251">System-Only</span></span>            | <span data-ttu-id="06235-252">False</span><span class="sxs-lookup"><span data-stu-id="06235-252">False</span></span>                                                |
| <span data-ttu-id="06235-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="06235-253">Is-Single-Valued</span></span>       | <span data-ttu-id="06235-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="06235-254">True</span></span>                                                 |
| <span data-ttu-id="06235-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="06235-255">Is Indexed</span></span>             | <span data-ttu-id="06235-256">Richtig</span><span class="sxs-lookup"><span data-stu-id="06235-256">True</span></span>                                                 |
| <span data-ttu-id="06235-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="06235-257">In Global Catalog</span></span>      | <span data-ttu-id="06235-258">False</span><span class="sxs-lookup"><span data-stu-id="06235-258">False</span></span>                                                |
| <span data-ttu-id="06235-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06235-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="06235-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="06235-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="06235-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06235-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="06235-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06235-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="06235-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06235-263">Search-Flags</span></span>           | <span data-ttu-id="06235-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="06235-264">0x00000001</span></span>                                           |
| <span data-ttu-id="06235-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06235-265">System-Flags</span></span>           | <span data-ttu-id="06235-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06235-266">0x00000010</span></span>                                           |
| <span data-ttu-id="06235-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="06235-267">Classes used in</span></span>        | [<span data-ttu-id="06235-268">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="06235-268">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





