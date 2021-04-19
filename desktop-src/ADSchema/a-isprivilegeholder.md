---
title: Is-Privilege-Holder-Attribut
description: Rückwärts Verknüpfung zu den Berechtigungen, die ein bestimmter Prinzipal innehat.
ms.assetid: 94355fbc-f7d8-460b-a516-1576629ca63e
ms.tgt_platform: multiple
keywords:
- AD-Schema für das is-Privilege-Holder-Attribut
- AD-Schema des isprivilegeholder-Attributs
topic_type:
- apiref
api_name:
- Is-Privilege-Holder
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 895a0202f6ca51ffe7982f33c1fc9f02d021d2a9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106342704"
---
# <a name="is-privilege-holder-attribute"></a><span data-ttu-id="990eb-105">Is-Privilege-Holder-Attribut</span><span class="sxs-lookup"><span data-stu-id="990eb-105">Is-Privilege-Holder attribute</span></span>

<span data-ttu-id="990eb-106">Rückwärts Verknüpfung zu den Berechtigungen, die ein bestimmter Prinzipal innehat.</span><span class="sxs-lookup"><span data-stu-id="990eb-106">Backward link to privileges held by a given principal.</span></span>



| <span data-ttu-id="990eb-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="990eb-107">Entry</span></span> | <span data-ttu-id="990eb-108">Wert</span><span class="sxs-lookup"><span data-stu-id="990eb-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="990eb-109">CN</span><span class="sxs-lookup"><span data-stu-id="990eb-109">CN</span></span>                | <span data-ttu-id="990eb-110">Is-Privilege-Inhaber</span><span class="sxs-lookup"><span data-stu-id="990eb-110">Is-Privilege-Holder</span></span>                     |
| <span data-ttu-id="990eb-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="990eb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="990eb-112">isprivilegeholder</span><span class="sxs-lookup"><span data-stu-id="990eb-112">isPrivilegeHolder</span></span>                       |
| <span data-ttu-id="990eb-113">Size</span><span class="sxs-lookup"><span data-stu-id="990eb-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="990eb-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="990eb-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="990eb-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="990eb-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="990eb-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="990eb-116">Attribute-Id</span></span>      | <span data-ttu-id="990eb-117">1.2.840.113556.1.4.638</span><span class="sxs-lookup"><span data-stu-id="990eb-117">1.2.840.113556.1.4.638</span></span>                  |
| <span data-ttu-id="990eb-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="990eb-118">System-Id-Guid</span></span>    | <span data-ttu-id="990eb-119">19405b9c-3cfa-11d1-a9c0-0000f 80367c1</span><span class="sxs-lookup"><span data-stu-id="990eb-119">19405b9c-3cfa-11d1-a9c0-0000f80367c1</span></span>    |
| <span data-ttu-id="990eb-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="990eb-120">Syntax</span></span>            | [<span data-ttu-id="990eb-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="990eb-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="990eb-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="990eb-122">Implementations</span></span>

-   [<span data-ttu-id="990eb-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="990eb-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="990eb-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="990eb-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="990eb-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="990eb-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="990eb-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="990eb-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="990eb-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="990eb-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="990eb-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="990eb-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="990eb-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="990eb-129">Windows 2000 Server</span></span>



| <span data-ttu-id="990eb-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="990eb-130">Entry</span></span> | <span data-ttu-id="990eb-131">Wert</span><span class="sxs-lookup"><span data-stu-id="990eb-131">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="990eb-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="990eb-132">Link-Id</span></span>                | <span data-ttu-id="990eb-133">71</span><span class="sxs-lookup"><span data-stu-id="990eb-133">71</span></span>                              |
| <span data-ttu-id="990eb-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="990eb-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="990eb-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="990eb-135">System-Only</span></span>            | <span data-ttu-id="990eb-136">Richtig</span><span class="sxs-lookup"><span data-stu-id="990eb-136">True</span></span>                            |
| <span data-ttu-id="990eb-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="990eb-137">Is-Single-Valued</span></span>       | <span data-ttu-id="990eb-138">False</span><span class="sxs-lookup"><span data-stu-id="990eb-138">False</span></span>                           |
| <span data-ttu-id="990eb-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="990eb-139">Is Indexed</span></span>             | <span data-ttu-id="990eb-140">False</span><span class="sxs-lookup"><span data-stu-id="990eb-140">False</span></span>                           |
| <span data-ttu-id="990eb-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="990eb-141">In Global Catalog</span></span>      | <span data-ttu-id="990eb-142">False</span><span class="sxs-lookup"><span data-stu-id="990eb-142">False</span></span>                           |
| <span data-ttu-id="990eb-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="990eb-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="990eb-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="990eb-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="990eb-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="990eb-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="990eb-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="990eb-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="990eb-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="990eb-147">Search-Flags</span></span>           | <span data-ttu-id="990eb-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="990eb-148">0x00000000</span></span>                      |
| <span data-ttu-id="990eb-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="990eb-149">System-Flags</span></span>           | <span data-ttu-id="990eb-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="990eb-150">0x00000010</span></span>                      |
| <span data-ttu-id="990eb-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="990eb-151">Classes used in</span></span>        | [<span data-ttu-id="990eb-152">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="990eb-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="990eb-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="990eb-153">Windows Server 2003</span></span>



| <span data-ttu-id="990eb-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="990eb-154">Entry</span></span> | <span data-ttu-id="990eb-155">Wert</span><span class="sxs-lookup"><span data-stu-id="990eb-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="990eb-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="990eb-156">Link-Id</span></span>                | <span data-ttu-id="990eb-157">71</span><span class="sxs-lookup"><span data-stu-id="990eb-157">71</span></span>                              |
| <span data-ttu-id="990eb-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="990eb-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="990eb-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="990eb-159">System-Only</span></span>            | <span data-ttu-id="990eb-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="990eb-160">True</span></span>                            |
| <span data-ttu-id="990eb-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="990eb-161">Is-Single-Valued</span></span>       | <span data-ttu-id="990eb-162">False</span><span class="sxs-lookup"><span data-stu-id="990eb-162">False</span></span>                           |
| <span data-ttu-id="990eb-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="990eb-163">Is Indexed</span></span>             | <span data-ttu-id="990eb-164">False</span><span class="sxs-lookup"><span data-stu-id="990eb-164">False</span></span>                           |
| <span data-ttu-id="990eb-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="990eb-165">In Global Catalog</span></span>      | <span data-ttu-id="990eb-166">False</span><span class="sxs-lookup"><span data-stu-id="990eb-166">False</span></span>                           |
| <span data-ttu-id="990eb-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="990eb-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="990eb-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="990eb-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="990eb-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="990eb-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="990eb-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="990eb-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="990eb-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="990eb-171">Search-Flags</span></span>           | <span data-ttu-id="990eb-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="990eb-172">0x00000000</span></span>                      |
| <span data-ttu-id="990eb-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="990eb-173">System-Flags</span></span>           | <span data-ttu-id="990eb-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="990eb-174">0x00000010</span></span>                      |
| <span data-ttu-id="990eb-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="990eb-175">Classes used in</span></span>        | [<span data-ttu-id="990eb-176">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="990eb-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="990eb-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="990eb-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="990eb-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="990eb-178">Entry</span></span> | <span data-ttu-id="990eb-179">Wert</span><span class="sxs-lookup"><span data-stu-id="990eb-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="990eb-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="990eb-180">Link-Id</span></span>                | <span data-ttu-id="990eb-181">71</span><span class="sxs-lookup"><span data-stu-id="990eb-181">71</span></span>                              |
| <span data-ttu-id="990eb-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="990eb-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="990eb-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="990eb-183">System-Only</span></span>            | <span data-ttu-id="990eb-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="990eb-184">True</span></span>                            |
| <span data-ttu-id="990eb-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="990eb-185">Is-Single-Valued</span></span>       | <span data-ttu-id="990eb-186">False</span><span class="sxs-lookup"><span data-stu-id="990eb-186">False</span></span>                           |
| <span data-ttu-id="990eb-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="990eb-187">Is Indexed</span></span>             | <span data-ttu-id="990eb-188">False</span><span class="sxs-lookup"><span data-stu-id="990eb-188">False</span></span>                           |
| <span data-ttu-id="990eb-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="990eb-189">In Global Catalog</span></span>      | <span data-ttu-id="990eb-190">False</span><span class="sxs-lookup"><span data-stu-id="990eb-190">False</span></span>                           |
| <span data-ttu-id="990eb-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="990eb-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="990eb-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="990eb-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="990eb-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="990eb-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="990eb-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="990eb-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="990eb-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="990eb-195">Search-Flags</span></span>           | <span data-ttu-id="990eb-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="990eb-196">0x00000000</span></span>                      |
| <span data-ttu-id="990eb-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="990eb-197">System-Flags</span></span>           | <span data-ttu-id="990eb-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="990eb-198">0x00000010</span></span>                      |
| <span data-ttu-id="990eb-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="990eb-199">Classes used in</span></span>        | [<span data-ttu-id="990eb-200">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="990eb-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="990eb-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="990eb-201">Windows Server 2008</span></span>



| <span data-ttu-id="990eb-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="990eb-202">Entry</span></span> | <span data-ttu-id="990eb-203">Wert</span><span class="sxs-lookup"><span data-stu-id="990eb-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="990eb-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="990eb-204">Link-Id</span></span>                | <span data-ttu-id="990eb-205">71</span><span class="sxs-lookup"><span data-stu-id="990eb-205">71</span></span>                              |
| <span data-ttu-id="990eb-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="990eb-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="990eb-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="990eb-207">System-Only</span></span>            | <span data-ttu-id="990eb-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="990eb-208">True</span></span>                            |
| <span data-ttu-id="990eb-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="990eb-209">Is-Single-Valued</span></span>       | <span data-ttu-id="990eb-210">False</span><span class="sxs-lookup"><span data-stu-id="990eb-210">False</span></span>                           |
| <span data-ttu-id="990eb-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="990eb-211">Is Indexed</span></span>             | <span data-ttu-id="990eb-212">False</span><span class="sxs-lookup"><span data-stu-id="990eb-212">False</span></span>                           |
| <span data-ttu-id="990eb-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="990eb-213">In Global Catalog</span></span>      | <span data-ttu-id="990eb-214">False</span><span class="sxs-lookup"><span data-stu-id="990eb-214">False</span></span>                           |
| <span data-ttu-id="990eb-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="990eb-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="990eb-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="990eb-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="990eb-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="990eb-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="990eb-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="990eb-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="990eb-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="990eb-219">Search-Flags</span></span>           | <span data-ttu-id="990eb-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="990eb-220">0x00000000</span></span>                      |
| <span data-ttu-id="990eb-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="990eb-221">System-Flags</span></span>           | <span data-ttu-id="990eb-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="990eb-222">0x00000010</span></span>                      |
| <span data-ttu-id="990eb-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="990eb-223">Classes used in</span></span>        | [<span data-ttu-id="990eb-224">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="990eb-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="990eb-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="990eb-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="990eb-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="990eb-226">Entry</span></span> | <span data-ttu-id="990eb-227">Wert</span><span class="sxs-lookup"><span data-stu-id="990eb-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="990eb-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="990eb-228">Link-Id</span></span>                | <span data-ttu-id="990eb-229">71</span><span class="sxs-lookup"><span data-stu-id="990eb-229">71</span></span>                              |
| <span data-ttu-id="990eb-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="990eb-230">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="990eb-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="990eb-231">System-Only</span></span>            | <span data-ttu-id="990eb-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="990eb-232">True</span></span>                            |
| <span data-ttu-id="990eb-233">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="990eb-233">Is-Single-Valued</span></span>       | <span data-ttu-id="990eb-234">False</span><span class="sxs-lookup"><span data-stu-id="990eb-234">False</span></span>                           |
| <span data-ttu-id="990eb-235">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="990eb-235">Is Indexed</span></span>             | <span data-ttu-id="990eb-236">False</span><span class="sxs-lookup"><span data-stu-id="990eb-236">False</span></span>                           |
| <span data-ttu-id="990eb-237">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="990eb-237">In Global Catalog</span></span>      | <span data-ttu-id="990eb-238">False</span><span class="sxs-lookup"><span data-stu-id="990eb-238">False</span></span>                           |
| <span data-ttu-id="990eb-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="990eb-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="990eb-240">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="990eb-240">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="990eb-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="990eb-241">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="990eb-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="990eb-242">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="990eb-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="990eb-243">Search-Flags</span></span>           | <span data-ttu-id="990eb-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="990eb-244">0x00000000</span></span>                      |
| <span data-ttu-id="990eb-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="990eb-245">System-Flags</span></span>           | <span data-ttu-id="990eb-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="990eb-246">0x00000010</span></span>                      |
| <span data-ttu-id="990eb-247">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="990eb-247">Classes used in</span></span>        | [<span data-ttu-id="990eb-248">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="990eb-248">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="990eb-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="990eb-249">Windows Server 2012</span></span>



| <span data-ttu-id="990eb-250">Eingabe</span><span class="sxs-lookup"><span data-stu-id="990eb-250">Entry</span></span> | <span data-ttu-id="990eb-251">Wert</span><span class="sxs-lookup"><span data-stu-id="990eb-251">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="990eb-252">Link-ID</span><span class="sxs-lookup"><span data-stu-id="990eb-252">Link-Id</span></span>                | <span data-ttu-id="990eb-253">71</span><span class="sxs-lookup"><span data-stu-id="990eb-253">71</span></span>                              |
| <span data-ttu-id="990eb-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="990eb-254">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="990eb-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="990eb-255">System-Only</span></span>            | <span data-ttu-id="990eb-256">Richtig</span><span class="sxs-lookup"><span data-stu-id="990eb-256">True</span></span>                            |
| <span data-ttu-id="990eb-257">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="990eb-257">Is-Single-Valued</span></span>       | <span data-ttu-id="990eb-258">False</span><span class="sxs-lookup"><span data-stu-id="990eb-258">False</span></span>                           |
| <span data-ttu-id="990eb-259">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="990eb-259">Is Indexed</span></span>             | <span data-ttu-id="990eb-260">False</span><span class="sxs-lookup"><span data-stu-id="990eb-260">False</span></span>                           |
| <span data-ttu-id="990eb-261">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="990eb-261">In Global Catalog</span></span>      | <span data-ttu-id="990eb-262">False</span><span class="sxs-lookup"><span data-stu-id="990eb-262">False</span></span>                           |
| <span data-ttu-id="990eb-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="990eb-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="990eb-264">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="990eb-264">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="990eb-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="990eb-265">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="990eb-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="990eb-266">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="990eb-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="990eb-267">Search-Flags</span></span>           | <span data-ttu-id="990eb-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="990eb-268">0x00000000</span></span>                      |
| <span data-ttu-id="990eb-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="990eb-269">System-Flags</span></span>           | <span data-ttu-id="990eb-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="990eb-270">0x00000010</span></span>                      |
| <span data-ttu-id="990eb-271">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="990eb-271">Classes used in</span></span>        | [<span data-ttu-id="990eb-272">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="990eb-272">**Top**</span></span>](c-top.md)<br/> |



 

 





