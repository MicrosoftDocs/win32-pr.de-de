---
title: Search-Flags-Attribut
description: Enthält einen Satz von Flags, die Such-und Indizierungs Informationen für ein Attribut angeben.
ms.assetid: 55fc4398-25d2-466a-9aa9-fa375d827023
ms.tgt_platform: multiple
keywords:
- AD-Schema für Search-Flags-Attribut
- searchFlags-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Search-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86f615464aa0aed69dd9590f668e37ec8c789c88
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106345558"
---
# <a name="search-flags-attribute"></a><span data-ttu-id="2ac11-105">Search-Flags-Attribut</span><span class="sxs-lookup"><span data-stu-id="2ac11-105">Search-Flags attribute</span></span>

<span data-ttu-id="2ac11-106">Enthält einen Satz von Flags, die Such-und Indizierungs Informationen für ein Attribut angeben.</span><span class="sxs-lookup"><span data-stu-id="2ac11-106">Contains a set of flags that specify search and indexing information for an attribute.</span></span> <span data-ttu-id="2ac11-107">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="2ac11-107">See Remarks.</span></span>



| <span data-ttu-id="2ac11-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2ac11-108">Entry</span></span> | <span data-ttu-id="2ac11-109">Wert</span><span class="sxs-lookup"><span data-stu-id="2ac11-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2ac11-110">CN</span><span class="sxs-lookup"><span data-stu-id="2ac11-110">CN</span></span>                | <span data-ttu-id="2ac11-111">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ac11-111">Search-Flags</span></span>                         |
| <span data-ttu-id="2ac11-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2ac11-112">Ldap-Display-Name</span></span> | <span data-ttu-id="2ac11-113">searchFlags</span><span class="sxs-lookup"><span data-stu-id="2ac11-113">searchFlags</span></span>                          |
| <span data-ttu-id="2ac11-114">Size</span><span class="sxs-lookup"><span data-stu-id="2ac11-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="2ac11-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2ac11-115">Update Privilege</span></span>  | <span data-ttu-id="2ac11-116">Schema Administrator</span><span class="sxs-lookup"><span data-stu-id="2ac11-116">Schema administrator</span></span>                 |
| <span data-ttu-id="2ac11-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="2ac11-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="2ac11-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2ac11-118">Attribute-Id</span></span>      | <span data-ttu-id="2ac11-119">1.2.840.113556.1.2.334</span><span class="sxs-lookup"><span data-stu-id="2ac11-119">1.2.840.113556.1.2.334</span></span>               |
| <span data-ttu-id="2ac11-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2ac11-120">System-Id-Guid</span></span>    | <span data-ttu-id="2ac11-121">bf967a2d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="2ac11-121">bf967a2d-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="2ac11-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ac11-122">Syntax</span></span>            | [<span data-ttu-id="2ac11-123">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="2ac11-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="2ac11-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="2ac11-124">Implementations</span></span>

-   [<span data-ttu-id="2ac11-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2ac11-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2ac11-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2ac11-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2ac11-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="2ac11-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2ac11-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2ac11-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2ac11-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2ac11-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2ac11-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2ac11-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2ac11-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2ac11-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2ac11-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2ac11-132">Windows 2000 Server</span></span>



| <span data-ttu-id="2ac11-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2ac11-133">Entry</span></span> | <span data-ttu-id="2ac11-134">Wert</span><span class="sxs-lookup"><span data-stu-id="2ac11-134">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="2ac11-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2ac11-135">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="2ac11-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ac11-136">MAPI-Id</span></span>                | <span data-ttu-id="2ac11-137">0x812d</span><span class="sxs-lookup"><span data-stu-id="2ac11-137">0x812D</span></span>                                                   |
| <span data-ttu-id="2ac11-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ac11-138">System-Only</span></span>            | <span data-ttu-id="2ac11-139">False</span><span class="sxs-lookup"><span data-stu-id="2ac11-139">False</span></span>                                                    |
| <span data-ttu-id="2ac11-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2ac11-140">Is-Single-Valued</span></span>       | <span data-ttu-id="2ac11-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="2ac11-141">True</span></span>                                                     |
| <span data-ttu-id="2ac11-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2ac11-142">Is Indexed</span></span>             | <span data-ttu-id="2ac11-143">False</span><span class="sxs-lookup"><span data-stu-id="2ac11-143">False</span></span>                                                    |
| <span data-ttu-id="2ac11-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2ac11-144">In Global Catalog</span></span>      | <span data-ttu-id="2ac11-145">False</span><span class="sxs-lookup"><span data-stu-id="2ac11-145">False</span></span>                                                    |
| <span data-ttu-id="2ac11-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2ac11-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ac11-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2ac11-147">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="2ac11-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ac11-148">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="2ac11-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ac11-149">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="2ac11-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ac11-150">Search-Flags</span></span>           | <span data-ttu-id="2ac11-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ac11-151">0x00000000</span></span>                                               |
| <span data-ttu-id="2ac11-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ac11-152">System-Flags</span></span>           | <span data-ttu-id="2ac11-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ac11-153">0x00000010</span></span>                                               |
| <span data-ttu-id="2ac11-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2ac11-154">Classes used in</span></span>        | [<span data-ttu-id="2ac11-155">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="2ac11-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2ac11-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2ac11-156">Windows Server 2003</span></span>



| <span data-ttu-id="2ac11-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2ac11-157">Entry</span></span> | <span data-ttu-id="2ac11-158">Wert</span><span class="sxs-lookup"><span data-stu-id="2ac11-158">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="2ac11-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2ac11-159">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="2ac11-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ac11-160">MAPI-Id</span></span>                | <span data-ttu-id="2ac11-161">0x812d</span><span class="sxs-lookup"><span data-stu-id="2ac11-161">0x812D</span></span>                                                   |
| <span data-ttu-id="2ac11-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ac11-162">System-Only</span></span>            | <span data-ttu-id="2ac11-163">False</span><span class="sxs-lookup"><span data-stu-id="2ac11-163">False</span></span>                                                    |
| <span data-ttu-id="2ac11-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2ac11-164">Is-Single-Valued</span></span>       | <span data-ttu-id="2ac11-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="2ac11-165">True</span></span>                                                     |
| <span data-ttu-id="2ac11-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2ac11-166">Is Indexed</span></span>             | <span data-ttu-id="2ac11-167">False</span><span class="sxs-lookup"><span data-stu-id="2ac11-167">False</span></span>                                                    |
| <span data-ttu-id="2ac11-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2ac11-168">In Global Catalog</span></span>      | <span data-ttu-id="2ac11-169">False</span><span class="sxs-lookup"><span data-stu-id="2ac11-169">False</span></span>                                                    |
| <span data-ttu-id="2ac11-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2ac11-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ac11-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2ac11-171">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="2ac11-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ac11-172">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="2ac11-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ac11-173">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="2ac11-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ac11-174">Search-Flags</span></span>           | <span data-ttu-id="2ac11-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ac11-175">0x00000000</span></span>                                               |
| <span data-ttu-id="2ac11-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ac11-176">System-Flags</span></span>           | <span data-ttu-id="2ac11-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ac11-177">0x00000010</span></span>                                               |
| <span data-ttu-id="2ac11-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2ac11-178">Classes used in</span></span>        | [<span data-ttu-id="2ac11-179">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="2ac11-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2ac11-180">Adam</span><span class="sxs-lookup"><span data-stu-id="2ac11-180">ADAM</span></span>



| <span data-ttu-id="2ac11-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2ac11-181">Entry</span></span> | <span data-ttu-id="2ac11-182">Wert</span><span class="sxs-lookup"><span data-stu-id="2ac11-182">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="2ac11-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2ac11-183">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="2ac11-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ac11-184">MAPI-Id</span></span>                | <span data-ttu-id="2ac11-185">0x812d</span><span class="sxs-lookup"><span data-stu-id="2ac11-185">0x812D</span></span>                                                   |
| <span data-ttu-id="2ac11-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ac11-186">System-Only</span></span>            | <span data-ttu-id="2ac11-187">False</span><span class="sxs-lookup"><span data-stu-id="2ac11-187">False</span></span>                                                    |
| <span data-ttu-id="2ac11-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2ac11-188">Is-Single-Valued</span></span>       | <span data-ttu-id="2ac11-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="2ac11-189">True</span></span>                                                     |
| <span data-ttu-id="2ac11-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2ac11-190">Is Indexed</span></span>             | <span data-ttu-id="2ac11-191">False</span><span class="sxs-lookup"><span data-stu-id="2ac11-191">False</span></span>                                                    |
| <span data-ttu-id="2ac11-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2ac11-192">In Global Catalog</span></span>      | <span data-ttu-id="2ac11-193">False</span><span class="sxs-lookup"><span data-stu-id="2ac11-193">False</span></span>                                                    |
| <span data-ttu-id="2ac11-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2ac11-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ac11-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2ac11-195">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="2ac11-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ac11-196">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="2ac11-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ac11-197">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="2ac11-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ac11-198">Search-Flags</span></span>           | <span data-ttu-id="2ac11-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ac11-199">0x00000000</span></span>                                               |
| <span data-ttu-id="2ac11-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ac11-200">System-Flags</span></span>           | <span data-ttu-id="2ac11-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ac11-201">0x00000010</span></span>                                               |
| <span data-ttu-id="2ac11-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2ac11-202">Classes used in</span></span>        | [<span data-ttu-id="2ac11-203">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="2ac11-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2ac11-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2ac11-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2ac11-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2ac11-205">Entry</span></span> | <span data-ttu-id="2ac11-206">Wert</span><span class="sxs-lookup"><span data-stu-id="2ac11-206">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="2ac11-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2ac11-207">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="2ac11-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ac11-208">MAPI-Id</span></span>                | <span data-ttu-id="2ac11-209">0x812d</span><span class="sxs-lookup"><span data-stu-id="2ac11-209">0x812D</span></span>                                                   |
| <span data-ttu-id="2ac11-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ac11-210">System-Only</span></span>            | <span data-ttu-id="2ac11-211">False</span><span class="sxs-lookup"><span data-stu-id="2ac11-211">False</span></span>                                                    |
| <span data-ttu-id="2ac11-212">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2ac11-212">Is-Single-Valued</span></span>       | <span data-ttu-id="2ac11-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="2ac11-213">True</span></span>                                                     |
| <span data-ttu-id="2ac11-214">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2ac11-214">Is Indexed</span></span>             | <span data-ttu-id="2ac11-215">False</span><span class="sxs-lookup"><span data-stu-id="2ac11-215">False</span></span>                                                    |
| <span data-ttu-id="2ac11-216">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2ac11-216">In Global Catalog</span></span>      | <span data-ttu-id="2ac11-217">False</span><span class="sxs-lookup"><span data-stu-id="2ac11-217">False</span></span>                                                    |
| <span data-ttu-id="2ac11-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2ac11-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ac11-219">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2ac11-219">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="2ac11-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ac11-220">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="2ac11-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ac11-221">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="2ac11-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ac11-222">Search-Flags</span></span>           | <span data-ttu-id="2ac11-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ac11-223">0x00000000</span></span>                                               |
| <span data-ttu-id="2ac11-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ac11-224">System-Flags</span></span>           | <span data-ttu-id="2ac11-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ac11-225">0x00000010</span></span>                                               |
| <span data-ttu-id="2ac11-226">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2ac11-226">Classes used in</span></span>        | [<span data-ttu-id="2ac11-227">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="2ac11-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2ac11-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ac11-228">Windows Server 2008</span></span>



| <span data-ttu-id="2ac11-229">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2ac11-229">Entry</span></span> | <span data-ttu-id="2ac11-230">Wert</span><span class="sxs-lookup"><span data-stu-id="2ac11-230">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="2ac11-231">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2ac11-231">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="2ac11-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ac11-232">MAPI-Id</span></span>                | <span data-ttu-id="2ac11-233">0x812d</span><span class="sxs-lookup"><span data-stu-id="2ac11-233">0x812D</span></span>                                                   |
| <span data-ttu-id="2ac11-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ac11-234">System-Only</span></span>            | <span data-ttu-id="2ac11-235">False</span><span class="sxs-lookup"><span data-stu-id="2ac11-235">False</span></span>                                                    |
| <span data-ttu-id="2ac11-236">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2ac11-236">Is-Single-Valued</span></span>       | <span data-ttu-id="2ac11-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="2ac11-237">True</span></span>                                                     |
| <span data-ttu-id="2ac11-238">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2ac11-238">Is Indexed</span></span>             | <span data-ttu-id="2ac11-239">False</span><span class="sxs-lookup"><span data-stu-id="2ac11-239">False</span></span>                                                    |
| <span data-ttu-id="2ac11-240">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2ac11-240">In Global Catalog</span></span>      | <span data-ttu-id="2ac11-241">False</span><span class="sxs-lookup"><span data-stu-id="2ac11-241">False</span></span>                                                    |
| <span data-ttu-id="2ac11-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2ac11-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ac11-243">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2ac11-243">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="2ac11-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ac11-244">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="2ac11-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ac11-245">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="2ac11-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ac11-246">Search-Flags</span></span>           | <span data-ttu-id="2ac11-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ac11-247">0x00000000</span></span>                                               |
| <span data-ttu-id="2ac11-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ac11-248">System-Flags</span></span>           | <span data-ttu-id="2ac11-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ac11-249">0x00000010</span></span>                                               |
| <span data-ttu-id="2ac11-250">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2ac11-250">Classes used in</span></span>        | [<span data-ttu-id="2ac11-251">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="2ac11-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2ac11-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2ac11-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2ac11-253">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2ac11-253">Entry</span></span> | <span data-ttu-id="2ac11-254">Wert</span><span class="sxs-lookup"><span data-stu-id="2ac11-254">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="2ac11-255">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2ac11-255">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="2ac11-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ac11-256">MAPI-Id</span></span>                | <span data-ttu-id="2ac11-257">0x812d</span><span class="sxs-lookup"><span data-stu-id="2ac11-257">0x812D</span></span>                                                   |
| <span data-ttu-id="2ac11-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ac11-258">System-Only</span></span>            | <span data-ttu-id="2ac11-259">False</span><span class="sxs-lookup"><span data-stu-id="2ac11-259">False</span></span>                                                    |
| <span data-ttu-id="2ac11-260">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2ac11-260">Is-Single-Valued</span></span>       | <span data-ttu-id="2ac11-261">Richtig</span><span class="sxs-lookup"><span data-stu-id="2ac11-261">True</span></span>                                                     |
| <span data-ttu-id="2ac11-262">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2ac11-262">Is Indexed</span></span>             | <span data-ttu-id="2ac11-263">False</span><span class="sxs-lookup"><span data-stu-id="2ac11-263">False</span></span>                                                    |
| <span data-ttu-id="2ac11-264">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2ac11-264">In Global Catalog</span></span>      | <span data-ttu-id="2ac11-265">False</span><span class="sxs-lookup"><span data-stu-id="2ac11-265">False</span></span>                                                    |
| <span data-ttu-id="2ac11-266">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2ac11-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ac11-267">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2ac11-267">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="2ac11-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ac11-268">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="2ac11-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ac11-269">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="2ac11-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ac11-270">Search-Flags</span></span>           | <span data-ttu-id="2ac11-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ac11-271">0x00000000</span></span>                                               |
| <span data-ttu-id="2ac11-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ac11-272">System-Flags</span></span>           | <span data-ttu-id="2ac11-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ac11-273">0x00000010</span></span>                                               |
| <span data-ttu-id="2ac11-274">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2ac11-274">Classes used in</span></span>        | [<span data-ttu-id="2ac11-275">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="2ac11-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2ac11-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2ac11-276">Windows Server 2012</span></span>



| <span data-ttu-id="2ac11-277">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2ac11-277">Entry</span></span> | <span data-ttu-id="2ac11-278">Wert</span><span class="sxs-lookup"><span data-stu-id="2ac11-278">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="2ac11-279">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2ac11-279">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="2ac11-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ac11-280">MAPI-Id</span></span>                | <span data-ttu-id="2ac11-281">0x812d</span><span class="sxs-lookup"><span data-stu-id="2ac11-281">0x812D</span></span>                                                   |
| <span data-ttu-id="2ac11-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ac11-282">System-Only</span></span>            | <span data-ttu-id="2ac11-283">False</span><span class="sxs-lookup"><span data-stu-id="2ac11-283">False</span></span>                                                    |
| <span data-ttu-id="2ac11-284">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2ac11-284">Is-Single-Valued</span></span>       | <span data-ttu-id="2ac11-285">Richtig</span><span class="sxs-lookup"><span data-stu-id="2ac11-285">True</span></span>                                                     |
| <span data-ttu-id="2ac11-286">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2ac11-286">Is Indexed</span></span>             | <span data-ttu-id="2ac11-287">False</span><span class="sxs-lookup"><span data-stu-id="2ac11-287">False</span></span>                                                    |
| <span data-ttu-id="2ac11-288">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2ac11-288">In Global Catalog</span></span>      | <span data-ttu-id="2ac11-289">False</span><span class="sxs-lookup"><span data-stu-id="2ac11-289">False</span></span>                                                    |
| <span data-ttu-id="2ac11-290">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2ac11-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ac11-291">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2ac11-291">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="2ac11-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ac11-292">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="2ac11-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ac11-293">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="2ac11-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ac11-294">Search-Flags</span></span>           | <span data-ttu-id="2ac11-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ac11-295">0x00000000</span></span>                                               |
| <span data-ttu-id="2ac11-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ac11-296">System-Flags</span></span>           | <span data-ttu-id="2ac11-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ac11-297">0x00000010</span></span>                                               |
| <span data-ttu-id="2ac11-298">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2ac11-298">Classes used in</span></span>        | [<span data-ttu-id="2ac11-299">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="2ac11-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="2ac11-300">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ac11-300">Remarks</span></span>

<span data-ttu-id="2ac11-301">Dieses Attribut kann NULL sein oder eine Kombination aus einem oder mehreren der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2ac11-301">This attribute can be zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="2ac11-302">Wert</span><span class="sxs-lookup"><span data-stu-id="2ac11-302">Value</span></span>            | <span data-ttu-id="2ac11-303">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ac11-303">Description</span></span>                                                                                                                                                                                                                                                                                                                                                               |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ac11-304">1 (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="2ac11-304">1 (0x00000001)</span></span>   | <span data-ttu-id="2ac11-305">Erstellen Sie einen Index für das-Attribut.</span><span class="sxs-lookup"><span data-stu-id="2ac11-305">Create an index for the attribute.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="2ac11-306">2 (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="2ac11-306">2 (0x00000002)</span></span>   | <span data-ttu-id="2ac11-307">Erstellen Sie in jedem Container einen Index für das-Attribut.</span><span class="sxs-lookup"><span data-stu-id="2ac11-307">Create an index for the attribute in each container.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="2ac11-308">4 (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="2ac11-308">4 (0x00000004)</span></span>   | <span data-ttu-id="2ac11-309">Fügen Sie dieses Attribut dem ANR-Satz (mehrdeutige Namensauflösung) hinzu.</span><span class="sxs-lookup"><span data-stu-id="2ac11-309">Add this attribute to the Ambiguous Name Resolution (ANR) set.</span></span> <span data-ttu-id="2ac11-310">Diese dient zur Unterstützung bei der Suche nach einem Objekt, wenn nur partielle Informationen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2ac11-310">This is used to assist in finding an object when only partial information is given.</span></span> <span data-ttu-id="2ac11-311">Wenn der LDAP-Filter beispielsweise (ANR = Jeff) lautet, findet die Suche jedes Objekt, bei dem Vorname, Nachname, e-Mail-Adresse oder anderes ANR-Attribut gleich Jeff ist.</span><span class="sxs-lookup"><span data-stu-id="2ac11-311">For example, if the LDAP filter is (ANR=JEFF), the search will find each object where the first name, last name, email address, or other ANR attribute is equal to JEFF.</span></span> <span data-ttu-id="2ac11-312">Für diesen Index muss das Bit 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2ac11-312">Bit 0 must be set for this index take affect.</span></span> |
| <span data-ttu-id="2ac11-313">8 (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="2ac11-313">8 (0x00000008)</span></span>   | <span data-ttu-id="2ac11-314">Behalten Sie dieses Attribut im Tombstone-Objekt für gelöschte Objekte bei.</span><span class="sxs-lookup"><span data-stu-id="2ac11-314">Preserve this attribute in the tombstone object for deleted objects.</span></span>                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="2ac11-315">16 (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="2ac11-315">16 (0x00000010)</span></span>  | <span data-ttu-id="2ac11-316">Kopieren Sie den Wert für dieses Attribut, wenn das Objekt kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="2ac11-316">Copy the value for this attribute when the object is copied.</span></span>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="2ac11-317">32 (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="2ac11-317">32 (0x00000020)</span></span>  | <span data-ttu-id="2ac11-318">Erstellen Sie einen Tupelindex für das Attribut.</span><span class="sxs-lookup"><span data-stu-id="2ac11-318">Create a tuple index for the attribute.</span></span> <span data-ttu-id="2ac11-319">Dies verbessert die Suche, bei der der Platzhalter am Anfang der Such Zeichenfolge angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2ac11-319">This will improve searches where the wildcard appears at the front of the search string.</span></span> <span data-ttu-id="2ac11-320">Beispiel: (SN = \* mith).</span><span class="sxs-lookup"><span data-stu-id="2ac11-320">For example, (sn=\*mith).</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="2ac11-321">64 (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="2ac11-321">64(0x00000040)</span></span>   | <span data-ttu-id="2ac11-322">Wird ab Adam unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2ac11-322">Supported beginning with ADAM.</span></span> <span data-ttu-id="2ac11-323">Erstellt einen Index, der die Leistung von VLV bei beliebigen Attributen erheblich unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2ac11-323">Creates an index to greatly help VLV performance on arbitrary attributes.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="2ac11-324">128 (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="2ac11-324">128 (0x00000080)</span></span> | <span data-ttu-id="2ac11-325">Markieren Sie das Attribut als vertraulich.</span><span class="sxs-lookup"><span data-stu-id="2ac11-325">Mark attribute as confidential.</span></span> <span data-ttu-id="2ac11-326">Ignoriert für Basis Schema Attribute (systemFlags = 0x10).</span><span class="sxs-lookup"><span data-stu-id="2ac11-326">Ignored for base schema attributes (systemFlags=0x10).</span></span>                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="2ac11-327">64 (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="2ac11-327">64 (0x00000040)</span></span>  | <span data-ttu-id="2ac11-328">Unterstützt ab Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="2ac11-328">Supported beginning with Windows Server 2008.</span></span> <span data-ttu-id="2ac11-329">Erstellen Sie einen Index zum Verbessern der Leistung der VLV-Suche für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="2ac11-329">Create an index to improve VLV search performance on this attribute.</span></span>                                                                                                                                                                                                                                                        |



 

 

 





