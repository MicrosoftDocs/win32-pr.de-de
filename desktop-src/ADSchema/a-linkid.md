---
title: Link-ID-Attribut
description: Eine ganze Zahl, die angibt, dass das Attribut ein verknüpftes Attribut ist. Eine gerade ganze Zahl ist ein Forward-Link, und eine ungerade ganze Zahl ist ein rückwärts Link.
ms.assetid: 73851839-f70c-40c6-976c-0bf727083791
ms.tgt_platform: multiple
keywords:
- AD-Schema für Link-ID-Attribut
- AD-Schema für linkid-Attribut
topic_type:
- apiref
api_name:
- Link-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a64ad1d26ce5510ac5643419ade46d0565df6487
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519903"
---
# <a name="link-id-attribute"></a><span data-ttu-id="ed392-106">Link-ID-Attribut</span><span class="sxs-lookup"><span data-stu-id="ed392-106">Link-ID attribute</span></span>

<span data-ttu-id="ed392-107">Eine ganze Zahl, die angibt, dass das Attribut ein verknüpftes Attribut ist.</span><span class="sxs-lookup"><span data-stu-id="ed392-107">An integer that indicates that the attribute is a linked attribute.</span></span> <span data-ttu-id="ed392-108">Eine gerade ganze Zahl ist ein Forward-Link, und eine ungerade ganze Zahl ist ein rückwärts Link.</span><span class="sxs-lookup"><span data-stu-id="ed392-108">An even integer is a forward link and an odd integer is a backward link.</span></span>



| <span data-ttu-id="ed392-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ed392-109">Entry</span></span> | <span data-ttu-id="ed392-110">Wert</span><span class="sxs-lookup"><span data-stu-id="ed392-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ed392-111">CN</span><span class="sxs-lookup"><span data-stu-id="ed392-111">CN</span></span>                | <span data-ttu-id="ed392-112">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ed392-112">Link-ID</span></span>                              |
| <span data-ttu-id="ed392-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ed392-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ed392-114">LinkId</span><span class="sxs-lookup"><span data-stu-id="ed392-114">linkID</span></span>                               |
| <span data-ttu-id="ed392-115">Size</span><span class="sxs-lookup"><span data-stu-id="ed392-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="ed392-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ed392-116">Update Privilege</span></span>  | <span data-ttu-id="ed392-117">Schema Administrator</span><span class="sxs-lookup"><span data-stu-id="ed392-117">Schema administrator</span></span>                 |
| <span data-ttu-id="ed392-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="ed392-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ed392-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ed392-119">Attribute-Id</span></span>      | <span data-ttu-id="ed392-120">1.2.840.113556.1.2.50</span><span class="sxs-lookup"><span data-stu-id="ed392-120">1.2.840.113556.1.2.50</span></span>                |
| <span data-ttu-id="ed392-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ed392-121">System-Id-Guid</span></span>    | <span data-ttu-id="ed392-122">bf96799b-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ed392-122">bf96799b-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="ed392-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed392-123">Syntax</span></span>            | [<span data-ttu-id="ed392-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="ed392-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="ed392-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="ed392-125">Implementations</span></span>

-   [<span data-ttu-id="ed392-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ed392-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ed392-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ed392-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ed392-128">**Adam**</span><span class="sxs-lookup"><span data-stu-id="ed392-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ed392-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ed392-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ed392-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ed392-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ed392-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ed392-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ed392-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ed392-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ed392-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ed392-133">Windows 2000 Server</span></span>



| <span data-ttu-id="ed392-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ed392-134">Entry</span></span> | <span data-ttu-id="ed392-135">Wert</span><span class="sxs-lookup"><span data-stu-id="ed392-135">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ed392-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ed392-136">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ed392-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed392-137">MAPI-Id</span></span>                | <span data-ttu-id="ed392-138">0x80c5</span><span class="sxs-lookup"><span data-stu-id="ed392-138">0x80C5</span></span>                                                   |
| <span data-ttu-id="ed392-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed392-139">System-Only</span></span>            | <span data-ttu-id="ed392-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="ed392-140">True</span></span>                                                     |
| <span data-ttu-id="ed392-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ed392-141">Is-Single-Valued</span></span>       | <span data-ttu-id="ed392-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="ed392-142">True</span></span>                                                     |
| <span data-ttu-id="ed392-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ed392-143">Is Indexed</span></span>             | <span data-ttu-id="ed392-144">False</span><span class="sxs-lookup"><span data-stu-id="ed392-144">False</span></span>                                                    |
| <span data-ttu-id="ed392-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ed392-145">In Global Catalog</span></span>      | <span data-ttu-id="ed392-146">False</span><span class="sxs-lookup"><span data-stu-id="ed392-146">False</span></span>                                                    |
| <span data-ttu-id="ed392-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ed392-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed392-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ed392-148">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ed392-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed392-149">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="ed392-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed392-150">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="ed392-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed392-151">Search-Flags</span></span>           | <span data-ttu-id="ed392-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed392-152">0x00000000</span></span>                                               |
| <span data-ttu-id="ed392-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed392-153">System-Flags</span></span>           | <span data-ttu-id="ed392-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed392-154">0x00000010</span></span>                                               |
| <span data-ttu-id="ed392-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ed392-155">Classes used in</span></span>        | [<span data-ttu-id="ed392-156">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="ed392-156">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ed392-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ed392-157">Windows Server 2003</span></span>



| <span data-ttu-id="ed392-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ed392-158">Entry</span></span> | <span data-ttu-id="ed392-159">Wert</span><span class="sxs-lookup"><span data-stu-id="ed392-159">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ed392-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ed392-160">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ed392-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed392-161">MAPI-Id</span></span>                | <span data-ttu-id="ed392-162">0x80c5</span><span class="sxs-lookup"><span data-stu-id="ed392-162">0x80C5</span></span>                                                   |
| <span data-ttu-id="ed392-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed392-163">System-Only</span></span>            | <span data-ttu-id="ed392-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="ed392-164">True</span></span>                                                     |
| <span data-ttu-id="ed392-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ed392-165">Is-Single-Valued</span></span>       | <span data-ttu-id="ed392-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="ed392-166">True</span></span>                                                     |
| <span data-ttu-id="ed392-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ed392-167">Is Indexed</span></span>             | <span data-ttu-id="ed392-168">False</span><span class="sxs-lookup"><span data-stu-id="ed392-168">False</span></span>                                                    |
| <span data-ttu-id="ed392-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ed392-169">In Global Catalog</span></span>      | <span data-ttu-id="ed392-170">False</span><span class="sxs-lookup"><span data-stu-id="ed392-170">False</span></span>                                                    |
| <span data-ttu-id="ed392-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ed392-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed392-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ed392-172">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ed392-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed392-173">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="ed392-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed392-174">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="ed392-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed392-175">Search-Flags</span></span>           | <span data-ttu-id="ed392-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed392-176">0x00000000</span></span>                                               |
| <span data-ttu-id="ed392-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed392-177">System-Flags</span></span>           | <span data-ttu-id="ed392-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed392-178">0x00000010</span></span>                                               |
| <span data-ttu-id="ed392-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ed392-179">Classes used in</span></span>        | [<span data-ttu-id="ed392-180">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="ed392-180">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ed392-181">Adam</span><span class="sxs-lookup"><span data-stu-id="ed392-181">ADAM</span></span>



| <span data-ttu-id="ed392-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ed392-182">Entry</span></span> | <span data-ttu-id="ed392-183">Wert</span><span class="sxs-lookup"><span data-stu-id="ed392-183">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ed392-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ed392-184">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ed392-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed392-185">MAPI-Id</span></span>                | <span data-ttu-id="ed392-186">0x80c5</span><span class="sxs-lookup"><span data-stu-id="ed392-186">0x80C5</span></span>                                                   |
| <span data-ttu-id="ed392-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed392-187">System-Only</span></span>            | <span data-ttu-id="ed392-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="ed392-188">True</span></span>                                                     |
| <span data-ttu-id="ed392-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ed392-189">Is-Single-Valued</span></span>       | <span data-ttu-id="ed392-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="ed392-190">True</span></span>                                                     |
| <span data-ttu-id="ed392-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ed392-191">Is Indexed</span></span>             | <span data-ttu-id="ed392-192">False</span><span class="sxs-lookup"><span data-stu-id="ed392-192">False</span></span>                                                    |
| <span data-ttu-id="ed392-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ed392-193">In Global Catalog</span></span>      | <span data-ttu-id="ed392-194">False</span><span class="sxs-lookup"><span data-stu-id="ed392-194">False</span></span>                                                    |
| <span data-ttu-id="ed392-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ed392-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed392-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ed392-196">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ed392-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed392-197">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="ed392-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed392-198">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="ed392-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed392-199">Search-Flags</span></span>           | <span data-ttu-id="ed392-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed392-200">0x00000000</span></span>                                               |
| <span data-ttu-id="ed392-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed392-201">System-Flags</span></span>           | <span data-ttu-id="ed392-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed392-202">0x00000010</span></span>                                               |
| <span data-ttu-id="ed392-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ed392-203">Classes used in</span></span>        | [<span data-ttu-id="ed392-204">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="ed392-204">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ed392-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ed392-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ed392-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ed392-206">Entry</span></span> | <span data-ttu-id="ed392-207">Wert</span><span class="sxs-lookup"><span data-stu-id="ed392-207">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ed392-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ed392-208">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ed392-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed392-209">MAPI-Id</span></span>                | <span data-ttu-id="ed392-210">0x80c5</span><span class="sxs-lookup"><span data-stu-id="ed392-210">0x80C5</span></span>                                                   |
| <span data-ttu-id="ed392-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed392-211">System-Only</span></span>            | <span data-ttu-id="ed392-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="ed392-212">True</span></span>                                                     |
| <span data-ttu-id="ed392-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ed392-213">Is-Single-Valued</span></span>       | <span data-ttu-id="ed392-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="ed392-214">True</span></span>                                                     |
| <span data-ttu-id="ed392-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ed392-215">Is Indexed</span></span>             | <span data-ttu-id="ed392-216">False</span><span class="sxs-lookup"><span data-stu-id="ed392-216">False</span></span>                                                    |
| <span data-ttu-id="ed392-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ed392-217">In Global Catalog</span></span>      | <span data-ttu-id="ed392-218">False</span><span class="sxs-lookup"><span data-stu-id="ed392-218">False</span></span>                                                    |
| <span data-ttu-id="ed392-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ed392-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed392-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ed392-220">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ed392-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed392-221">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="ed392-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed392-222">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="ed392-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed392-223">Search-Flags</span></span>           | <span data-ttu-id="ed392-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed392-224">0x00000000</span></span>                                               |
| <span data-ttu-id="ed392-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed392-225">System-Flags</span></span>           | <span data-ttu-id="ed392-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed392-226">0x00000010</span></span>                                               |
| <span data-ttu-id="ed392-227">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ed392-227">Classes used in</span></span>        | [<span data-ttu-id="ed392-228">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="ed392-228">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ed392-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed392-229">Windows Server 2008</span></span>



| <span data-ttu-id="ed392-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ed392-230">Entry</span></span> | <span data-ttu-id="ed392-231">Wert</span><span class="sxs-lookup"><span data-stu-id="ed392-231">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ed392-232">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ed392-232">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ed392-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed392-233">MAPI-Id</span></span>                | <span data-ttu-id="ed392-234">0x80c5</span><span class="sxs-lookup"><span data-stu-id="ed392-234">0x80C5</span></span>                                                   |
| <span data-ttu-id="ed392-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed392-235">System-Only</span></span>            | <span data-ttu-id="ed392-236">Richtig</span><span class="sxs-lookup"><span data-stu-id="ed392-236">True</span></span>                                                     |
| <span data-ttu-id="ed392-237">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ed392-237">Is-Single-Valued</span></span>       | <span data-ttu-id="ed392-238">Richtig</span><span class="sxs-lookup"><span data-stu-id="ed392-238">True</span></span>                                                     |
| <span data-ttu-id="ed392-239">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ed392-239">Is Indexed</span></span>             | <span data-ttu-id="ed392-240">False</span><span class="sxs-lookup"><span data-stu-id="ed392-240">False</span></span>                                                    |
| <span data-ttu-id="ed392-241">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ed392-241">In Global Catalog</span></span>      | <span data-ttu-id="ed392-242">False</span><span class="sxs-lookup"><span data-stu-id="ed392-242">False</span></span>                                                    |
| <span data-ttu-id="ed392-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ed392-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed392-244">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ed392-244">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ed392-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed392-245">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="ed392-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed392-246">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="ed392-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed392-247">Search-Flags</span></span>           | <span data-ttu-id="ed392-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed392-248">0x00000000</span></span>                                               |
| <span data-ttu-id="ed392-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed392-249">System-Flags</span></span>           | <span data-ttu-id="ed392-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed392-250">0x00000010</span></span>                                               |
| <span data-ttu-id="ed392-251">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ed392-251">Classes used in</span></span>        | [<span data-ttu-id="ed392-252">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="ed392-252">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ed392-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ed392-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ed392-254">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ed392-254">Entry</span></span> | <span data-ttu-id="ed392-255">Wert</span><span class="sxs-lookup"><span data-stu-id="ed392-255">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ed392-256">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ed392-256">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ed392-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed392-257">MAPI-Id</span></span>                | <span data-ttu-id="ed392-258">0x80c5</span><span class="sxs-lookup"><span data-stu-id="ed392-258">0x80C5</span></span>                                                   |
| <span data-ttu-id="ed392-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed392-259">System-Only</span></span>            | <span data-ttu-id="ed392-260">Richtig</span><span class="sxs-lookup"><span data-stu-id="ed392-260">True</span></span>                                                     |
| <span data-ttu-id="ed392-261">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ed392-261">Is-Single-Valued</span></span>       | <span data-ttu-id="ed392-262">Richtig</span><span class="sxs-lookup"><span data-stu-id="ed392-262">True</span></span>                                                     |
| <span data-ttu-id="ed392-263">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ed392-263">Is Indexed</span></span>             | <span data-ttu-id="ed392-264">False</span><span class="sxs-lookup"><span data-stu-id="ed392-264">False</span></span>                                                    |
| <span data-ttu-id="ed392-265">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ed392-265">In Global Catalog</span></span>      | <span data-ttu-id="ed392-266">False</span><span class="sxs-lookup"><span data-stu-id="ed392-266">False</span></span>                                                    |
| <span data-ttu-id="ed392-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ed392-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed392-268">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ed392-268">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ed392-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed392-269">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="ed392-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed392-270">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="ed392-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed392-271">Search-Flags</span></span>           | <span data-ttu-id="ed392-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed392-272">0x00000000</span></span>                                               |
| <span data-ttu-id="ed392-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed392-273">System-Flags</span></span>           | <span data-ttu-id="ed392-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed392-274">0x00000010</span></span>                                               |
| <span data-ttu-id="ed392-275">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ed392-275">Classes used in</span></span>        | [<span data-ttu-id="ed392-276">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="ed392-276">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ed392-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ed392-277">Windows Server 2012</span></span>



| <span data-ttu-id="ed392-278">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ed392-278">Entry</span></span> | <span data-ttu-id="ed392-279">Wert</span><span class="sxs-lookup"><span data-stu-id="ed392-279">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ed392-280">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ed392-280">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ed392-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed392-281">MAPI-Id</span></span>                | <span data-ttu-id="ed392-282">0x80c5</span><span class="sxs-lookup"><span data-stu-id="ed392-282">0x80C5</span></span>                                                   |
| <span data-ttu-id="ed392-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed392-283">System-Only</span></span>            | <span data-ttu-id="ed392-284">Richtig</span><span class="sxs-lookup"><span data-stu-id="ed392-284">True</span></span>                                                     |
| <span data-ttu-id="ed392-285">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ed392-285">Is-Single-Valued</span></span>       | <span data-ttu-id="ed392-286">Richtig</span><span class="sxs-lookup"><span data-stu-id="ed392-286">True</span></span>                                                     |
| <span data-ttu-id="ed392-287">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ed392-287">Is Indexed</span></span>             | <span data-ttu-id="ed392-288">False</span><span class="sxs-lookup"><span data-stu-id="ed392-288">False</span></span>                                                    |
| <span data-ttu-id="ed392-289">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ed392-289">In Global Catalog</span></span>      | <span data-ttu-id="ed392-290">False</span><span class="sxs-lookup"><span data-stu-id="ed392-290">False</span></span>                                                    |
| <span data-ttu-id="ed392-291">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ed392-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed392-292">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ed392-292">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ed392-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed392-293">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="ed392-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed392-294">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="ed392-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed392-295">Search-Flags</span></span>           | <span data-ttu-id="ed392-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed392-296">0x00000000</span></span>                                               |
| <span data-ttu-id="ed392-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed392-297">System-Flags</span></span>           | <span data-ttu-id="ed392-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed392-298">0x00000010</span></span>                                               |
| <span data-ttu-id="ed392-299">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ed392-299">Classes used in</span></span>        | [<span data-ttu-id="ed392-300">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="ed392-300">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





