---
title: Obj-Dist-Name-Attribut
description: Identisch mit dem Distinguished Name für ein Objekt. Wird von Exchange verwendet.
ms.assetid: 0dc2855c-2707-49d8-80e6-27f163a59bc8
ms.tgt_platform: multiple
keywords:
- Obj-Dist-Name-Attribut AD-Schema
- das Attribut "-AD-Schema"
topic_type:
- apiref
api_name:
- Obj-Dist-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42cd118f38de78546b7b792bca3c8c9ef6d229cb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859449"
---
# <a name="obj-dist-name-attribute"></a><span data-ttu-id="2b24d-106">Obj-Dist-Name-Attribut</span><span class="sxs-lookup"><span data-stu-id="2b24d-106">Obj-Dist-Name attribute</span></span>

<span data-ttu-id="2b24d-107">Identisch mit dem Distinguished Name für ein Objekt.</span><span class="sxs-lookup"><span data-stu-id="2b24d-107">Same as the Distinguished Name for an object.</span></span> <span data-ttu-id="2b24d-108">Wird von Exchange verwendet.</span><span class="sxs-lookup"><span data-stu-id="2b24d-108">Used by Exchange.</span></span>



| <span data-ttu-id="2b24d-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2b24d-109">Entry</span></span> | <span data-ttu-id="2b24d-110">Wert</span><span class="sxs-lookup"><span data-stu-id="2b24d-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="2b24d-111">CN</span><span class="sxs-lookup"><span data-stu-id="2b24d-111">CN</span></span>                | <span data-ttu-id="2b24d-112">Obj-Dist-Name</span><span class="sxs-lookup"><span data-stu-id="2b24d-112">Obj-Dist-Name</span></span>                           |
| <span data-ttu-id="2b24d-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2b24d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="2b24d-114">distinguishedName</span><span class="sxs-lookup"><span data-stu-id="2b24d-114">distinguishedName</span></span>                       |
| <span data-ttu-id="2b24d-115">Size</span><span class="sxs-lookup"><span data-stu-id="2b24d-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="2b24d-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2b24d-116">Update Privilege</span></span>  | <span data-ttu-id="2b24d-117">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2b24d-117">This value is set by the system.</span></span>        |
| <span data-ttu-id="2b24d-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="2b24d-118">Update Frequency</span></span>  | <span data-ttu-id="2b24d-119">Jedes Mal, wenn ein Objekt erstellt oder verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="2b24d-119">Whenever an object is created or moved.</span></span> |
| <span data-ttu-id="2b24d-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2b24d-120">Attribute-Id</span></span>      | <span data-ttu-id="2b24d-121">2.5.4.49</span><span class="sxs-lookup"><span data-stu-id="2b24d-121">2.5.4.49</span></span>                                |
| <span data-ttu-id="2b24d-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2b24d-122">System-Id-Guid</span></span>    | <span data-ttu-id="2b24d-123">bf9679e4-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="2b24d-123">bf9679e4-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="2b24d-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b24d-124">Syntax</span></span>            | [<span data-ttu-id="2b24d-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="2b24d-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="2b24d-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="2b24d-126">Implementations</span></span>

-   [<span data-ttu-id="2b24d-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2b24d-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2b24d-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2b24d-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2b24d-129">**Adam**</span><span class="sxs-lookup"><span data-stu-id="2b24d-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2b24d-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2b24d-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2b24d-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2b24d-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2b24d-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2b24d-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2b24d-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2b24d-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2b24d-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2b24d-134">Windows 2000 Server</span></span>



| <span data-ttu-id="2b24d-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2b24d-135">Entry</span></span> | <span data-ttu-id="2b24d-136">Wert</span><span class="sxs-lookup"><span data-stu-id="2b24d-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2b24d-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2b24d-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2b24d-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b24d-138">MAPI-Id</span></span>                | <span data-ttu-id="2b24d-139">0x803c</span><span class="sxs-lookup"><span data-stu-id="2b24d-139">0x803C</span></span>                          |
| <span data-ttu-id="2b24d-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b24d-140">System-Only</span></span>            | <span data-ttu-id="2b24d-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="2b24d-141">True</span></span>                            |
| <span data-ttu-id="2b24d-142">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2b24d-142">Is-Single-Valued</span></span>       | <span data-ttu-id="2b24d-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="2b24d-143">True</span></span>                            |
| <span data-ttu-id="2b24d-144">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2b24d-144">Is Indexed</span></span>             | <span data-ttu-id="2b24d-145">False</span><span class="sxs-lookup"><span data-stu-id="2b24d-145">False</span></span>                           |
| <span data-ttu-id="2b24d-146">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2b24d-146">In Global Catalog</span></span>      | <span data-ttu-id="2b24d-147">Richtig</span><span class="sxs-lookup"><span data-stu-id="2b24d-147">True</span></span>                            |
| <span data-ttu-id="2b24d-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2b24d-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b24d-149">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2b24d-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2b24d-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b24d-150">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2b24d-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b24d-151">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2b24d-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b24d-152">Search-Flags</span></span>           | <span data-ttu-id="2b24d-153">0x00000008</span><span class="sxs-lookup"><span data-stu-id="2b24d-153">0x00000008</span></span>                      |
| <span data-ttu-id="2b24d-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b24d-154">System-Flags</span></span>           | <span data-ttu-id="2b24d-155">0x00000013</span><span class="sxs-lookup"><span data-stu-id="2b24d-155">0x00000013</span></span>                      |
| <span data-ttu-id="2b24d-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2b24d-156">Classes used in</span></span>        | [<span data-ttu-id="2b24d-157">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="2b24d-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2b24d-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2b24d-158">Windows Server 2003</span></span>



| <span data-ttu-id="2b24d-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2b24d-159">Entry</span></span> | <span data-ttu-id="2b24d-160">Wert</span><span class="sxs-lookup"><span data-stu-id="2b24d-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2b24d-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2b24d-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2b24d-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b24d-162">MAPI-Id</span></span>                | <span data-ttu-id="2b24d-163">0x803c</span><span class="sxs-lookup"><span data-stu-id="2b24d-163">0x803C</span></span>                          |
| <span data-ttu-id="2b24d-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b24d-164">System-Only</span></span>            | <span data-ttu-id="2b24d-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="2b24d-165">True</span></span>                            |
| <span data-ttu-id="2b24d-166">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2b24d-166">Is-Single-Valued</span></span>       | <span data-ttu-id="2b24d-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="2b24d-167">True</span></span>                            |
| <span data-ttu-id="2b24d-168">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2b24d-168">Is Indexed</span></span>             | <span data-ttu-id="2b24d-169">False</span><span class="sxs-lookup"><span data-stu-id="2b24d-169">False</span></span>                           |
| <span data-ttu-id="2b24d-170">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2b24d-170">In Global Catalog</span></span>      | <span data-ttu-id="2b24d-171">Richtig</span><span class="sxs-lookup"><span data-stu-id="2b24d-171">True</span></span>                            |
| <span data-ttu-id="2b24d-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2b24d-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b24d-173">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2b24d-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2b24d-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b24d-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2b24d-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b24d-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2b24d-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b24d-176">Search-Flags</span></span>           | <span data-ttu-id="2b24d-177">0x00000008</span><span class="sxs-lookup"><span data-stu-id="2b24d-177">0x00000008</span></span>                      |
| <span data-ttu-id="2b24d-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b24d-178">System-Flags</span></span>           | <span data-ttu-id="2b24d-179">0x00000013</span><span class="sxs-lookup"><span data-stu-id="2b24d-179">0x00000013</span></span>                      |
| <span data-ttu-id="2b24d-180">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2b24d-180">Classes used in</span></span>        | [<span data-ttu-id="2b24d-181">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="2b24d-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2b24d-182">Adam</span><span class="sxs-lookup"><span data-stu-id="2b24d-182">ADAM</span></span>



| <span data-ttu-id="2b24d-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2b24d-183">Entry</span></span> | <span data-ttu-id="2b24d-184">Wert</span><span class="sxs-lookup"><span data-stu-id="2b24d-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2b24d-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2b24d-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2b24d-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b24d-186">MAPI-Id</span></span>                | <span data-ttu-id="2b24d-187">0x803c</span><span class="sxs-lookup"><span data-stu-id="2b24d-187">0x803C</span></span>                          |
| <span data-ttu-id="2b24d-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b24d-188">System-Only</span></span>            | <span data-ttu-id="2b24d-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="2b24d-189">True</span></span>                            |
| <span data-ttu-id="2b24d-190">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2b24d-190">Is-Single-Valued</span></span>       | <span data-ttu-id="2b24d-191">Richtig</span><span class="sxs-lookup"><span data-stu-id="2b24d-191">True</span></span>                            |
| <span data-ttu-id="2b24d-192">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2b24d-192">Is Indexed</span></span>             | <span data-ttu-id="2b24d-193">False</span><span class="sxs-lookup"><span data-stu-id="2b24d-193">False</span></span>                           |
| <span data-ttu-id="2b24d-194">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2b24d-194">In Global Catalog</span></span>      | <span data-ttu-id="2b24d-195">Richtig</span><span class="sxs-lookup"><span data-stu-id="2b24d-195">True</span></span>                            |
| <span data-ttu-id="2b24d-196">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2b24d-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b24d-197">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2b24d-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2b24d-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b24d-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2b24d-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b24d-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2b24d-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b24d-200">Search-Flags</span></span>           | <span data-ttu-id="2b24d-201">0x00000008</span><span class="sxs-lookup"><span data-stu-id="2b24d-201">0x00000008</span></span>                      |
| <span data-ttu-id="2b24d-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b24d-202">System-Flags</span></span>           | <span data-ttu-id="2b24d-203">0x00000013</span><span class="sxs-lookup"><span data-stu-id="2b24d-203">0x00000013</span></span>                      |
| <span data-ttu-id="2b24d-204">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2b24d-204">Classes used in</span></span>        | [<span data-ttu-id="2b24d-205">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="2b24d-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2b24d-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2b24d-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2b24d-207">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2b24d-207">Entry</span></span> | <span data-ttu-id="2b24d-208">Wert</span><span class="sxs-lookup"><span data-stu-id="2b24d-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2b24d-209">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2b24d-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2b24d-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b24d-210">MAPI-Id</span></span>                | <span data-ttu-id="2b24d-211">0x803c</span><span class="sxs-lookup"><span data-stu-id="2b24d-211">0x803C</span></span>                          |
| <span data-ttu-id="2b24d-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b24d-212">System-Only</span></span>            | <span data-ttu-id="2b24d-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="2b24d-213">True</span></span>                            |
| <span data-ttu-id="2b24d-214">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2b24d-214">Is-Single-Valued</span></span>       | <span data-ttu-id="2b24d-215">Richtig</span><span class="sxs-lookup"><span data-stu-id="2b24d-215">True</span></span>                            |
| <span data-ttu-id="2b24d-216">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2b24d-216">Is Indexed</span></span>             | <span data-ttu-id="2b24d-217">False</span><span class="sxs-lookup"><span data-stu-id="2b24d-217">False</span></span>                           |
| <span data-ttu-id="2b24d-218">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2b24d-218">In Global Catalog</span></span>      | <span data-ttu-id="2b24d-219">Richtig</span><span class="sxs-lookup"><span data-stu-id="2b24d-219">True</span></span>                            |
| <span data-ttu-id="2b24d-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2b24d-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b24d-221">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2b24d-221">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2b24d-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b24d-222">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2b24d-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b24d-223">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2b24d-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b24d-224">Search-Flags</span></span>           | <span data-ttu-id="2b24d-225">0x00000008</span><span class="sxs-lookup"><span data-stu-id="2b24d-225">0x00000008</span></span>                      |
| <span data-ttu-id="2b24d-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b24d-226">System-Flags</span></span>           | <span data-ttu-id="2b24d-227">0x00000013</span><span class="sxs-lookup"><span data-stu-id="2b24d-227">0x00000013</span></span>                      |
| <span data-ttu-id="2b24d-228">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2b24d-228">Classes used in</span></span>        | [<span data-ttu-id="2b24d-229">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="2b24d-229">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2b24d-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b24d-230">Windows Server 2008</span></span>



| <span data-ttu-id="2b24d-231">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2b24d-231">Entry</span></span> | <span data-ttu-id="2b24d-232">Wert</span><span class="sxs-lookup"><span data-stu-id="2b24d-232">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2b24d-233">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2b24d-233">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2b24d-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b24d-234">MAPI-Id</span></span>                | <span data-ttu-id="2b24d-235">0x803c</span><span class="sxs-lookup"><span data-stu-id="2b24d-235">0x803C</span></span>                          |
| <span data-ttu-id="2b24d-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b24d-236">System-Only</span></span>            | <span data-ttu-id="2b24d-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="2b24d-237">True</span></span>                            |
| <span data-ttu-id="2b24d-238">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2b24d-238">Is-Single-Valued</span></span>       | <span data-ttu-id="2b24d-239">Richtig</span><span class="sxs-lookup"><span data-stu-id="2b24d-239">True</span></span>                            |
| <span data-ttu-id="2b24d-240">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2b24d-240">Is Indexed</span></span>             | <span data-ttu-id="2b24d-241">False</span><span class="sxs-lookup"><span data-stu-id="2b24d-241">False</span></span>                           |
| <span data-ttu-id="2b24d-242">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2b24d-242">In Global Catalog</span></span>      | <span data-ttu-id="2b24d-243">Richtig</span><span class="sxs-lookup"><span data-stu-id="2b24d-243">True</span></span>                            |
| <span data-ttu-id="2b24d-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2b24d-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b24d-245">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2b24d-245">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2b24d-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b24d-246">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2b24d-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b24d-247">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2b24d-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b24d-248">Search-Flags</span></span>           | <span data-ttu-id="2b24d-249">0x00000008</span><span class="sxs-lookup"><span data-stu-id="2b24d-249">0x00000008</span></span>                      |
| <span data-ttu-id="2b24d-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b24d-250">System-Flags</span></span>           | <span data-ttu-id="2b24d-251">0x00000013</span><span class="sxs-lookup"><span data-stu-id="2b24d-251">0x00000013</span></span>                      |
| <span data-ttu-id="2b24d-252">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2b24d-252">Classes used in</span></span>        | [<span data-ttu-id="2b24d-253">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="2b24d-253">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2b24d-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2b24d-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2b24d-255">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2b24d-255">Entry</span></span> | <span data-ttu-id="2b24d-256">Wert</span><span class="sxs-lookup"><span data-stu-id="2b24d-256">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2b24d-257">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2b24d-257">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2b24d-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b24d-258">MAPI-Id</span></span>                | <span data-ttu-id="2b24d-259">0x803c</span><span class="sxs-lookup"><span data-stu-id="2b24d-259">0x803C</span></span>                          |
| <span data-ttu-id="2b24d-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b24d-260">System-Only</span></span>            | <span data-ttu-id="2b24d-261">Richtig</span><span class="sxs-lookup"><span data-stu-id="2b24d-261">True</span></span>                            |
| <span data-ttu-id="2b24d-262">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2b24d-262">Is-Single-Valued</span></span>       | <span data-ttu-id="2b24d-263">Richtig</span><span class="sxs-lookup"><span data-stu-id="2b24d-263">True</span></span>                            |
| <span data-ttu-id="2b24d-264">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2b24d-264">Is Indexed</span></span>             | <span data-ttu-id="2b24d-265">False</span><span class="sxs-lookup"><span data-stu-id="2b24d-265">False</span></span>                           |
| <span data-ttu-id="2b24d-266">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2b24d-266">In Global Catalog</span></span>      | <span data-ttu-id="2b24d-267">Richtig</span><span class="sxs-lookup"><span data-stu-id="2b24d-267">True</span></span>                            |
| <span data-ttu-id="2b24d-268">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2b24d-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b24d-269">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2b24d-269">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2b24d-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b24d-270">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2b24d-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b24d-271">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2b24d-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b24d-272">Search-Flags</span></span>           | <span data-ttu-id="2b24d-273">0x00000008</span><span class="sxs-lookup"><span data-stu-id="2b24d-273">0x00000008</span></span>                      |
| <span data-ttu-id="2b24d-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b24d-274">System-Flags</span></span>           | <span data-ttu-id="2b24d-275">0x00000013</span><span class="sxs-lookup"><span data-stu-id="2b24d-275">0x00000013</span></span>                      |
| <span data-ttu-id="2b24d-276">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2b24d-276">Classes used in</span></span>        | [<span data-ttu-id="2b24d-277">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="2b24d-277">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2b24d-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2b24d-278">Windows Server 2012</span></span>



| <span data-ttu-id="2b24d-279">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2b24d-279">Entry</span></span> | <span data-ttu-id="2b24d-280">Wert</span><span class="sxs-lookup"><span data-stu-id="2b24d-280">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2b24d-281">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2b24d-281">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2b24d-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b24d-282">MAPI-Id</span></span>                | <span data-ttu-id="2b24d-283">0x803c</span><span class="sxs-lookup"><span data-stu-id="2b24d-283">0x803C</span></span>                          |
| <span data-ttu-id="2b24d-284">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b24d-284">System-Only</span></span>            | <span data-ttu-id="2b24d-285">Richtig</span><span class="sxs-lookup"><span data-stu-id="2b24d-285">True</span></span>                            |
| <span data-ttu-id="2b24d-286">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2b24d-286">Is-Single-Valued</span></span>       | <span data-ttu-id="2b24d-287">Richtig</span><span class="sxs-lookup"><span data-stu-id="2b24d-287">True</span></span>                            |
| <span data-ttu-id="2b24d-288">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2b24d-288">Is Indexed</span></span>             | <span data-ttu-id="2b24d-289">False</span><span class="sxs-lookup"><span data-stu-id="2b24d-289">False</span></span>                           |
| <span data-ttu-id="2b24d-290">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2b24d-290">In Global Catalog</span></span>      | <span data-ttu-id="2b24d-291">Richtig</span><span class="sxs-lookup"><span data-stu-id="2b24d-291">True</span></span>                            |
| <span data-ttu-id="2b24d-292">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2b24d-292">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b24d-293">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2b24d-293">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2b24d-294">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b24d-294">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2b24d-295">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b24d-295">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2b24d-296">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b24d-296">Search-Flags</span></span>           | <span data-ttu-id="2b24d-297">0x00000008</span><span class="sxs-lookup"><span data-stu-id="2b24d-297">0x00000008</span></span>                      |
| <span data-ttu-id="2b24d-298">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b24d-298">System-Flags</span></span>           | <span data-ttu-id="2b24d-299">0x00000013</span><span class="sxs-lookup"><span data-stu-id="2b24d-299">0x00000013</span></span>                      |
| <span data-ttu-id="2b24d-300">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2b24d-300">Classes used in</span></span>        | [<span data-ttu-id="2b24d-301">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="2b24d-301">**Top**</span></span>](c-top.md)<br/> |



 

 





