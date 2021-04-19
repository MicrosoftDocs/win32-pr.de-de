---
title: RDN-ATT-ID-Attribut
description: Der RDN für das Attribut, das verwendet wird, um eine Klasse zu benennen.
ms.assetid: 793199c4-6c5e-481f-8f73-bd59375ab51b
ms.tgt_platform: multiple
keywords:
- RDN-ATT-ID-Attribut, AD-Schema
- rDNAttID-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- RDN-Att-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b5fb573d289b71bb459cd8595b5df5115f42bf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346364"
---
# <a name="rdn-att-id-attribute"></a><span data-ttu-id="e29e6-105">RDN-ATT-ID-Attribut</span><span class="sxs-lookup"><span data-stu-id="e29e6-105">RDN-Att-ID attribute</span></span>

<span data-ttu-id="e29e6-106">Der RDN für das Attribut, das verwendet wird, um eine Klasse zu benennen.</span><span class="sxs-lookup"><span data-stu-id="e29e6-106">The RDN for the attribute that is used to name a class.</span></span>



| <span data-ttu-id="e29e6-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e29e6-107">Entry</span></span> | <span data-ttu-id="e29e6-108">Wert</span><span class="sxs-lookup"><span data-stu-id="e29e6-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="e29e6-109">CN</span><span class="sxs-lookup"><span data-stu-id="e29e6-109">CN</span></span>                | <span data-ttu-id="e29e6-110">RDN-ATT-ID</span><span class="sxs-lookup"><span data-stu-id="e29e6-110">RDN-Att-ID</span></span>                                                      |
| <span data-ttu-id="e29e6-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e29e6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e29e6-112">rDNAttID</span><span class="sxs-lookup"><span data-stu-id="e29e6-112">rDNAttID</span></span>                                                        |
| <span data-ttu-id="e29e6-113">Size</span><span class="sxs-lookup"><span data-stu-id="e29e6-113">Size</span></span>              | \-                                                              |
| <span data-ttu-id="e29e6-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="e29e6-114">Update Privilege</span></span>  | <span data-ttu-id="e29e6-115">Schema Administrator</span><span class="sxs-lookup"><span data-stu-id="e29e6-115">Schema administrator</span></span>                                            |
| <span data-ttu-id="e29e6-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="e29e6-116">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="e29e6-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e29e6-117">Attribute-Id</span></span>      | <span data-ttu-id="e29e6-118">1.2.840.113556.1.2.26</span><span class="sxs-lookup"><span data-stu-id="e29e6-118">1.2.840.113556.1.2.26</span></span>                                           |
| <span data-ttu-id="e29e6-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e29e6-119">System-Id-Guid</span></span>    | <span data-ttu-id="e29e6-120">bf967a0f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e29e6-120">bf967a0f-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="e29e6-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="e29e6-121">Syntax</span></span>            | [<span data-ttu-id="e29e6-122">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="e29e6-122">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="e29e6-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="e29e6-123">Implementations</span></span>

-   [<span data-ttu-id="e29e6-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e29e6-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e29e6-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e29e6-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e29e6-126">**Adam**</span><span class="sxs-lookup"><span data-stu-id="e29e6-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e29e6-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e29e6-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e29e6-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e29e6-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e29e6-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e29e6-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e29e6-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e29e6-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e29e6-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e29e6-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e29e6-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e29e6-132">Entry</span></span> | <span data-ttu-id="e29e6-133">Wert</span><span class="sxs-lookup"><span data-stu-id="e29e6-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e29e6-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e29e6-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e29e6-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e29e6-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e29e6-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e29e6-136">System-Only</span></span>            | <span data-ttu-id="e29e6-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="e29e6-137">True</span></span>                                             |
| <span data-ttu-id="e29e6-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e29e6-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e29e6-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="e29e6-139">True</span></span>                                             |
| <span data-ttu-id="e29e6-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e29e6-140">Is Indexed</span></span>             | <span data-ttu-id="e29e6-141">False</span><span class="sxs-lookup"><span data-stu-id="e29e6-141">False</span></span>                                            |
| <span data-ttu-id="e29e6-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e29e6-142">In Global Catalog</span></span>      | <span data-ttu-id="e29e6-143">False</span><span class="sxs-lookup"><span data-stu-id="e29e6-143">False</span></span>                                            |
| <span data-ttu-id="e29e6-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e29e6-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e29e6-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e29e6-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e29e6-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e29e6-146">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e29e6-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e29e6-147">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e29e6-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e29e6-148">Search-Flags</span></span>           | <span data-ttu-id="e29e6-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e29e6-149">0x00000000</span></span>                                       |
| <span data-ttu-id="e29e6-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e29e6-150">System-Flags</span></span>           | <span data-ttu-id="e29e6-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e29e6-151">0x00000010</span></span>                                       |
| <span data-ttu-id="e29e6-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e29e6-152">Classes used in</span></span>        | [<span data-ttu-id="e29e6-153">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="e29e6-153">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e29e6-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e29e6-154">Windows Server 2003</span></span>



| <span data-ttu-id="e29e6-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e29e6-155">Entry</span></span> | <span data-ttu-id="e29e6-156">Wert</span><span class="sxs-lookup"><span data-stu-id="e29e6-156">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e29e6-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e29e6-157">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e29e6-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e29e6-158">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e29e6-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e29e6-159">System-Only</span></span>            | <span data-ttu-id="e29e6-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="e29e6-160">True</span></span>                                             |
| <span data-ttu-id="e29e6-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e29e6-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e29e6-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="e29e6-162">True</span></span>                                             |
| <span data-ttu-id="e29e6-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e29e6-163">Is Indexed</span></span>             | <span data-ttu-id="e29e6-164">False</span><span class="sxs-lookup"><span data-stu-id="e29e6-164">False</span></span>                                            |
| <span data-ttu-id="e29e6-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e29e6-165">In Global Catalog</span></span>      | <span data-ttu-id="e29e6-166">False</span><span class="sxs-lookup"><span data-stu-id="e29e6-166">False</span></span>                                            |
| <span data-ttu-id="e29e6-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e29e6-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e29e6-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e29e6-168">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e29e6-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e29e6-169">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e29e6-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e29e6-170">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e29e6-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e29e6-171">Search-Flags</span></span>           | <span data-ttu-id="e29e6-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e29e6-172">0x00000000</span></span>                                       |
| <span data-ttu-id="e29e6-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e29e6-173">System-Flags</span></span>           | <span data-ttu-id="e29e6-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e29e6-174">0x00000010</span></span>                                       |
| <span data-ttu-id="e29e6-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e29e6-175">Classes used in</span></span>        | [<span data-ttu-id="e29e6-176">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="e29e6-176">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e29e6-177">Adam</span><span class="sxs-lookup"><span data-stu-id="e29e6-177">ADAM</span></span>



| <span data-ttu-id="e29e6-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e29e6-178">Entry</span></span> | <span data-ttu-id="e29e6-179">Wert</span><span class="sxs-lookup"><span data-stu-id="e29e6-179">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e29e6-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e29e6-180">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e29e6-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e29e6-181">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e29e6-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e29e6-182">System-Only</span></span>            | <span data-ttu-id="e29e6-183">Richtig</span><span class="sxs-lookup"><span data-stu-id="e29e6-183">True</span></span>                                             |
| <span data-ttu-id="e29e6-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e29e6-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e29e6-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="e29e6-185">True</span></span>                                             |
| <span data-ttu-id="e29e6-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e29e6-186">Is Indexed</span></span>             | <span data-ttu-id="e29e6-187">False</span><span class="sxs-lookup"><span data-stu-id="e29e6-187">False</span></span>                                            |
| <span data-ttu-id="e29e6-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e29e6-188">In Global Catalog</span></span>      | <span data-ttu-id="e29e6-189">False</span><span class="sxs-lookup"><span data-stu-id="e29e6-189">False</span></span>                                            |
| <span data-ttu-id="e29e6-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e29e6-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e29e6-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e29e6-191">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e29e6-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e29e6-192">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e29e6-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e29e6-193">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e29e6-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e29e6-194">Search-Flags</span></span>           | <span data-ttu-id="e29e6-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e29e6-195">0x00000000</span></span>                                       |
| <span data-ttu-id="e29e6-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e29e6-196">System-Flags</span></span>           | <span data-ttu-id="e29e6-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e29e6-197">0x00000010</span></span>                                       |
| <span data-ttu-id="e29e6-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e29e6-198">Classes used in</span></span>        | [<span data-ttu-id="e29e6-199">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="e29e6-199">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e29e6-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e29e6-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e29e6-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e29e6-201">Entry</span></span> | <span data-ttu-id="e29e6-202">Wert</span><span class="sxs-lookup"><span data-stu-id="e29e6-202">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e29e6-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e29e6-203">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e29e6-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e29e6-204">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e29e6-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="e29e6-205">System-Only</span></span>            | <span data-ttu-id="e29e6-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="e29e6-206">True</span></span>                                             |
| <span data-ttu-id="e29e6-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e29e6-207">Is-Single-Valued</span></span>       | <span data-ttu-id="e29e6-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="e29e6-208">True</span></span>                                             |
| <span data-ttu-id="e29e6-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e29e6-209">Is Indexed</span></span>             | <span data-ttu-id="e29e6-210">False</span><span class="sxs-lookup"><span data-stu-id="e29e6-210">False</span></span>                                            |
| <span data-ttu-id="e29e6-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e29e6-211">In Global Catalog</span></span>      | <span data-ttu-id="e29e6-212">False</span><span class="sxs-lookup"><span data-stu-id="e29e6-212">False</span></span>                                            |
| <span data-ttu-id="e29e6-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e29e6-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="e29e6-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e29e6-214">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e29e6-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e29e6-215">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e29e6-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e29e6-216">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e29e6-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e29e6-217">Search-Flags</span></span>           | <span data-ttu-id="e29e6-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e29e6-218">0x00000000</span></span>                                       |
| <span data-ttu-id="e29e6-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e29e6-219">System-Flags</span></span>           | <span data-ttu-id="e29e6-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e29e6-220">0x00000010</span></span>                                       |
| <span data-ttu-id="e29e6-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e29e6-221">Classes used in</span></span>        | [<span data-ttu-id="e29e6-222">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="e29e6-222">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e29e6-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e29e6-223">Windows Server 2008</span></span>



| <span data-ttu-id="e29e6-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e29e6-224">Entry</span></span> | <span data-ttu-id="e29e6-225">Wert</span><span class="sxs-lookup"><span data-stu-id="e29e6-225">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e29e6-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e29e6-226">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e29e6-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e29e6-227">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e29e6-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e29e6-228">System-Only</span></span>            | <span data-ttu-id="e29e6-229">Richtig</span><span class="sxs-lookup"><span data-stu-id="e29e6-229">True</span></span>                                             |
| <span data-ttu-id="e29e6-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e29e6-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e29e6-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="e29e6-231">True</span></span>                                             |
| <span data-ttu-id="e29e6-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e29e6-232">Is Indexed</span></span>             | <span data-ttu-id="e29e6-233">False</span><span class="sxs-lookup"><span data-stu-id="e29e6-233">False</span></span>                                            |
| <span data-ttu-id="e29e6-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e29e6-234">In Global Catalog</span></span>      | <span data-ttu-id="e29e6-235">False</span><span class="sxs-lookup"><span data-stu-id="e29e6-235">False</span></span>                                            |
| <span data-ttu-id="e29e6-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e29e6-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e29e6-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e29e6-237">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e29e6-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e29e6-238">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e29e6-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e29e6-239">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e29e6-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e29e6-240">Search-Flags</span></span>           | <span data-ttu-id="e29e6-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e29e6-241">0x00000000</span></span>                                       |
| <span data-ttu-id="e29e6-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e29e6-242">System-Flags</span></span>           | <span data-ttu-id="e29e6-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e29e6-243">0x00000010</span></span>                                       |
| <span data-ttu-id="e29e6-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e29e6-244">Classes used in</span></span>        | [<span data-ttu-id="e29e6-245">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="e29e6-245">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e29e6-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e29e6-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e29e6-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e29e6-247">Entry</span></span> | <span data-ttu-id="e29e6-248">Wert</span><span class="sxs-lookup"><span data-stu-id="e29e6-248">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e29e6-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e29e6-249">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e29e6-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e29e6-250">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e29e6-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="e29e6-251">System-Only</span></span>            | <span data-ttu-id="e29e6-252">Richtig</span><span class="sxs-lookup"><span data-stu-id="e29e6-252">True</span></span>                                             |
| <span data-ttu-id="e29e6-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e29e6-253">Is-Single-Valued</span></span>       | <span data-ttu-id="e29e6-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="e29e6-254">True</span></span>                                             |
| <span data-ttu-id="e29e6-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e29e6-255">Is Indexed</span></span>             | <span data-ttu-id="e29e6-256">False</span><span class="sxs-lookup"><span data-stu-id="e29e6-256">False</span></span>                                            |
| <span data-ttu-id="e29e6-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e29e6-257">In Global Catalog</span></span>      | <span data-ttu-id="e29e6-258">False</span><span class="sxs-lookup"><span data-stu-id="e29e6-258">False</span></span>                                            |
| <span data-ttu-id="e29e6-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e29e6-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="e29e6-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e29e6-260">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e29e6-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e29e6-261">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e29e6-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e29e6-262">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e29e6-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e29e6-263">Search-Flags</span></span>           | <span data-ttu-id="e29e6-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e29e6-264">0x00000000</span></span>                                       |
| <span data-ttu-id="e29e6-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e29e6-265">System-Flags</span></span>           | <span data-ttu-id="e29e6-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e29e6-266">0x00000010</span></span>                                       |
| <span data-ttu-id="e29e6-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e29e6-267">Classes used in</span></span>        | [<span data-ttu-id="e29e6-268">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="e29e6-268">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e29e6-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e29e6-269">Windows Server 2012</span></span>



| <span data-ttu-id="e29e6-270">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e29e6-270">Entry</span></span> | <span data-ttu-id="e29e6-271">Wert</span><span class="sxs-lookup"><span data-stu-id="e29e6-271">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e29e6-272">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e29e6-272">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e29e6-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e29e6-273">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e29e6-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="e29e6-274">System-Only</span></span>            | <span data-ttu-id="e29e6-275">Richtig</span><span class="sxs-lookup"><span data-stu-id="e29e6-275">True</span></span>                                             |
| <span data-ttu-id="e29e6-276">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e29e6-276">Is-Single-Valued</span></span>       | <span data-ttu-id="e29e6-277">Richtig</span><span class="sxs-lookup"><span data-stu-id="e29e6-277">True</span></span>                                             |
| <span data-ttu-id="e29e6-278">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e29e6-278">Is Indexed</span></span>             | <span data-ttu-id="e29e6-279">False</span><span class="sxs-lookup"><span data-stu-id="e29e6-279">False</span></span>                                            |
| <span data-ttu-id="e29e6-280">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e29e6-280">In Global Catalog</span></span>      | <span data-ttu-id="e29e6-281">False</span><span class="sxs-lookup"><span data-stu-id="e29e6-281">False</span></span>                                            |
| <span data-ttu-id="e29e6-282">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e29e6-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="e29e6-283">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e29e6-283">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e29e6-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e29e6-284">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e29e6-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e29e6-285">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e29e6-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e29e6-286">Search-Flags</span></span>           | <span data-ttu-id="e29e6-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e29e6-287">0x00000000</span></span>                                       |
| <span data-ttu-id="e29e6-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e29e6-288">System-Flags</span></span>           | <span data-ttu-id="e29e6-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e29e6-289">0x00000010</span></span>                                       |
| <span data-ttu-id="e29e6-290">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e29e6-290">Classes used in</span></span>        | [<span data-ttu-id="e29e6-291">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="e29e6-291">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





