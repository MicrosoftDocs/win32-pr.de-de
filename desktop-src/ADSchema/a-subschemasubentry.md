---
title: Subschemasubentry-Attribut
description: Der Distinguished Name für den Speicherort des unter Schema Objekts, in dem eine Klasse oder ein Attribut definiert ist.
ms.assetid: 16beeb31-436c-4ae1-b1f7-fa00abb3bcbb
ms.tgt_platform: multiple
keywords:
- Subschemasubentry-Attribut, AD-Schema
- subschemasubentry-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- SubSchemaSubEntry
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57a0278d63d3a6ed9d0f84ad67df87e248af31f1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519647"
---
# <a name="subschemasubentry-attribute"></a><span data-ttu-id="6d26c-105">Subschemasubentry-Attribut</span><span class="sxs-lookup"><span data-stu-id="6d26c-105">SubSchemaSubEntry attribute</span></span>

<span data-ttu-id="6d26c-106">Der Distinguished Name für den Speicherort des unter Schema Objekts, in dem eine Klasse oder ein Attribut definiert ist.</span><span class="sxs-lookup"><span data-stu-id="6d26c-106">The distinguished name for the location of the subschema object where a class or attribute is defined.</span></span>



| <span data-ttu-id="6d26c-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d26c-107">Entry</span></span> | <span data-ttu-id="6d26c-108">Wert</span><span class="sxs-lookup"><span data-stu-id="6d26c-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6d26c-109">CN</span><span class="sxs-lookup"><span data-stu-id="6d26c-109">CN</span></span>                | <span data-ttu-id="6d26c-110">Subschemasubentry</span><span class="sxs-lookup"><span data-stu-id="6d26c-110">SubSchemaSubEntry</span></span>                                                                |
| <span data-ttu-id="6d26c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6d26c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6d26c-112">subschemasubentry</span><span class="sxs-lookup"><span data-stu-id="6d26c-112">subSchemaSubEntry</span></span>                                                                |
| <span data-ttu-id="6d26c-113">Size</span><span class="sxs-lookup"><span data-stu-id="6d26c-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="6d26c-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="6d26c-114">Update Privilege</span></span>  | <span data-ttu-id="6d26c-115">Schema Administrator</span><span class="sxs-lookup"><span data-stu-id="6d26c-115">Schema administrator</span></span>                                                             |
| <span data-ttu-id="6d26c-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="6d26c-116">Update Frequency</span></span>  | <span data-ttu-id="6d26c-117">Wenn die Active Directory geladen wird oder wenn eine neue Klasse oder ein neues Attribut definiert wird.</span><span class="sxs-lookup"><span data-stu-id="6d26c-117">When the Active Directory is loaded or when a new class or attribute is defined.</span></span> |
| <span data-ttu-id="6d26c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6d26c-118">Attribute-Id</span></span>      | <span data-ttu-id="6d26c-119">2.5.18.10</span><span class="sxs-lookup"><span data-stu-id="6d26c-119">2.5.18.10</span></span>                                                                        |
| <span data-ttu-id="6d26c-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6d26c-120">System-Id-Guid</span></span>    | <span data-ttu-id="6d26c-121">9a7ad94d-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="6d26c-121">9a7ad94d-ca53-11d1-bbd0-0080c76670c0</span></span>                                             |
| <span data-ttu-id="6d26c-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d26c-122">Syntax</span></span>            | [<span data-ttu-id="6d26c-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="6d26c-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                                          |



## <a name="implementations"></a><span data-ttu-id="6d26c-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="6d26c-124">Implementations</span></span>

-   [<span data-ttu-id="6d26c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6d26c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6d26c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6d26c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6d26c-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="6d26c-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6d26c-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6d26c-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6d26c-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6d26c-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6d26c-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6d26c-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6d26c-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6d26c-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6d26c-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6d26c-132">Windows 2000 Server</span></span>



| <span data-ttu-id="6d26c-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d26c-133">Entry</span></span> | <span data-ttu-id="6d26c-134">Wert</span><span class="sxs-lookup"><span data-stu-id="6d26c-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6d26c-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6d26c-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6d26c-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d26c-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6d26c-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d26c-137">System-Only</span></span>            | <span data-ttu-id="6d26c-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="6d26c-138">True</span></span>                            |
| <span data-ttu-id="6d26c-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6d26c-139">Is-Single-Valued</span></span>       | <span data-ttu-id="6d26c-140">False</span><span class="sxs-lookup"><span data-stu-id="6d26c-140">False</span></span>                           |
| <span data-ttu-id="6d26c-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6d26c-141">Is Indexed</span></span>             | <span data-ttu-id="6d26c-142">False</span><span class="sxs-lookup"><span data-stu-id="6d26c-142">False</span></span>                           |
| <span data-ttu-id="6d26c-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6d26c-143">In Global Catalog</span></span>      | <span data-ttu-id="6d26c-144">False</span><span class="sxs-lookup"><span data-stu-id="6d26c-144">False</span></span>                           |
| <span data-ttu-id="6d26c-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6d26c-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d26c-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6d26c-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6d26c-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d26c-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6d26c-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d26c-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6d26c-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d26c-149">Search-Flags</span></span>           | <span data-ttu-id="6d26c-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d26c-150">0x00000000</span></span>                      |
| <span data-ttu-id="6d26c-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d26c-151">System-Flags</span></span>           | <span data-ttu-id="6d26c-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6d26c-152">0x08000014</span></span>                      |
| <span data-ttu-id="6d26c-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6d26c-153">Classes used in</span></span>        | [<span data-ttu-id="6d26c-154">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="6d26c-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6d26c-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6d26c-155">Windows Server 2003</span></span>



| <span data-ttu-id="6d26c-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d26c-156">Entry</span></span> | <span data-ttu-id="6d26c-157">Wert</span><span class="sxs-lookup"><span data-stu-id="6d26c-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6d26c-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6d26c-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6d26c-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d26c-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6d26c-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d26c-160">System-Only</span></span>            | <span data-ttu-id="6d26c-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="6d26c-161">True</span></span>                            |
| <span data-ttu-id="6d26c-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6d26c-162">Is-Single-Valued</span></span>       | <span data-ttu-id="6d26c-163">False</span><span class="sxs-lookup"><span data-stu-id="6d26c-163">False</span></span>                           |
| <span data-ttu-id="6d26c-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6d26c-164">Is Indexed</span></span>             | <span data-ttu-id="6d26c-165">False</span><span class="sxs-lookup"><span data-stu-id="6d26c-165">False</span></span>                           |
| <span data-ttu-id="6d26c-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6d26c-166">In Global Catalog</span></span>      | <span data-ttu-id="6d26c-167">False</span><span class="sxs-lookup"><span data-stu-id="6d26c-167">False</span></span>                           |
| <span data-ttu-id="6d26c-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6d26c-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d26c-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6d26c-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6d26c-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d26c-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6d26c-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d26c-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6d26c-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d26c-172">Search-Flags</span></span>           | <span data-ttu-id="6d26c-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d26c-173">0x00000000</span></span>                      |
| <span data-ttu-id="6d26c-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d26c-174">System-Flags</span></span>           | <span data-ttu-id="6d26c-175">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6d26c-175">0x08000014</span></span>                      |
| <span data-ttu-id="6d26c-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6d26c-176">Classes used in</span></span>        | [<span data-ttu-id="6d26c-177">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="6d26c-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6d26c-178">Adam</span><span class="sxs-lookup"><span data-stu-id="6d26c-178">ADAM</span></span>



| <span data-ttu-id="6d26c-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d26c-179">Entry</span></span> | <span data-ttu-id="6d26c-180">Wert</span><span class="sxs-lookup"><span data-stu-id="6d26c-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6d26c-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6d26c-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6d26c-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d26c-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6d26c-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d26c-183">System-Only</span></span>            | <span data-ttu-id="6d26c-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="6d26c-184">True</span></span>                            |
| <span data-ttu-id="6d26c-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6d26c-185">Is-Single-Valued</span></span>       | <span data-ttu-id="6d26c-186">False</span><span class="sxs-lookup"><span data-stu-id="6d26c-186">False</span></span>                           |
| <span data-ttu-id="6d26c-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6d26c-187">Is Indexed</span></span>             | <span data-ttu-id="6d26c-188">False</span><span class="sxs-lookup"><span data-stu-id="6d26c-188">False</span></span>                           |
| <span data-ttu-id="6d26c-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6d26c-189">In Global Catalog</span></span>      | <span data-ttu-id="6d26c-190">False</span><span class="sxs-lookup"><span data-stu-id="6d26c-190">False</span></span>                           |
| <span data-ttu-id="6d26c-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6d26c-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d26c-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6d26c-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6d26c-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d26c-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6d26c-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d26c-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6d26c-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d26c-195">Search-Flags</span></span>           | <span data-ttu-id="6d26c-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d26c-196">0x00000000</span></span>                      |
| <span data-ttu-id="6d26c-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d26c-197">System-Flags</span></span>           | <span data-ttu-id="6d26c-198">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6d26c-198">0x08000014</span></span>                      |
| <span data-ttu-id="6d26c-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6d26c-199">Classes used in</span></span>        | [<span data-ttu-id="6d26c-200">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="6d26c-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6d26c-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6d26c-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6d26c-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d26c-202">Entry</span></span> | <span data-ttu-id="6d26c-203">Wert</span><span class="sxs-lookup"><span data-stu-id="6d26c-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6d26c-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6d26c-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6d26c-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d26c-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6d26c-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d26c-206">System-Only</span></span>            | <span data-ttu-id="6d26c-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="6d26c-207">True</span></span>                            |
| <span data-ttu-id="6d26c-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6d26c-208">Is-Single-Valued</span></span>       | <span data-ttu-id="6d26c-209">False</span><span class="sxs-lookup"><span data-stu-id="6d26c-209">False</span></span>                           |
| <span data-ttu-id="6d26c-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6d26c-210">Is Indexed</span></span>             | <span data-ttu-id="6d26c-211">False</span><span class="sxs-lookup"><span data-stu-id="6d26c-211">False</span></span>                           |
| <span data-ttu-id="6d26c-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6d26c-212">In Global Catalog</span></span>      | <span data-ttu-id="6d26c-213">False</span><span class="sxs-lookup"><span data-stu-id="6d26c-213">False</span></span>                           |
| <span data-ttu-id="6d26c-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6d26c-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d26c-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6d26c-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6d26c-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d26c-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6d26c-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d26c-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6d26c-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d26c-218">Search-Flags</span></span>           | <span data-ttu-id="6d26c-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d26c-219">0x00000000</span></span>                      |
| <span data-ttu-id="6d26c-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d26c-220">System-Flags</span></span>           | <span data-ttu-id="6d26c-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6d26c-221">0x08000014</span></span>                      |
| <span data-ttu-id="6d26c-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6d26c-222">Classes used in</span></span>        | [<span data-ttu-id="6d26c-223">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="6d26c-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6d26c-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d26c-224">Windows Server 2008</span></span>



| <span data-ttu-id="6d26c-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d26c-225">Entry</span></span> | <span data-ttu-id="6d26c-226">Wert</span><span class="sxs-lookup"><span data-stu-id="6d26c-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6d26c-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6d26c-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6d26c-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d26c-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6d26c-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d26c-229">System-Only</span></span>            | <span data-ttu-id="6d26c-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="6d26c-230">True</span></span>                            |
| <span data-ttu-id="6d26c-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6d26c-231">Is-Single-Valued</span></span>       | <span data-ttu-id="6d26c-232">False</span><span class="sxs-lookup"><span data-stu-id="6d26c-232">False</span></span>                           |
| <span data-ttu-id="6d26c-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6d26c-233">Is Indexed</span></span>             | <span data-ttu-id="6d26c-234">False</span><span class="sxs-lookup"><span data-stu-id="6d26c-234">False</span></span>                           |
| <span data-ttu-id="6d26c-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6d26c-235">In Global Catalog</span></span>      | <span data-ttu-id="6d26c-236">False</span><span class="sxs-lookup"><span data-stu-id="6d26c-236">False</span></span>                           |
| <span data-ttu-id="6d26c-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6d26c-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d26c-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6d26c-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6d26c-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d26c-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6d26c-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d26c-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6d26c-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d26c-241">Search-Flags</span></span>           | <span data-ttu-id="6d26c-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d26c-242">0x00000000</span></span>                      |
| <span data-ttu-id="6d26c-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d26c-243">System-Flags</span></span>           | <span data-ttu-id="6d26c-244">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6d26c-244">0x08000014</span></span>                      |
| <span data-ttu-id="6d26c-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6d26c-245">Classes used in</span></span>        | [<span data-ttu-id="6d26c-246">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="6d26c-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6d26c-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6d26c-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6d26c-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d26c-248">Entry</span></span> | <span data-ttu-id="6d26c-249">Wert</span><span class="sxs-lookup"><span data-stu-id="6d26c-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6d26c-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6d26c-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6d26c-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d26c-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6d26c-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d26c-252">System-Only</span></span>            | <span data-ttu-id="6d26c-253">Richtig</span><span class="sxs-lookup"><span data-stu-id="6d26c-253">True</span></span>                            |
| <span data-ttu-id="6d26c-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6d26c-254">Is-Single-Valued</span></span>       | <span data-ttu-id="6d26c-255">False</span><span class="sxs-lookup"><span data-stu-id="6d26c-255">False</span></span>                           |
| <span data-ttu-id="6d26c-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6d26c-256">Is Indexed</span></span>             | <span data-ttu-id="6d26c-257">False</span><span class="sxs-lookup"><span data-stu-id="6d26c-257">False</span></span>                           |
| <span data-ttu-id="6d26c-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6d26c-258">In Global Catalog</span></span>      | <span data-ttu-id="6d26c-259">False</span><span class="sxs-lookup"><span data-stu-id="6d26c-259">False</span></span>                           |
| <span data-ttu-id="6d26c-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6d26c-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d26c-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6d26c-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6d26c-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d26c-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6d26c-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d26c-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6d26c-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d26c-264">Search-Flags</span></span>           | <span data-ttu-id="6d26c-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d26c-265">0x00000000</span></span>                      |
| <span data-ttu-id="6d26c-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d26c-266">System-Flags</span></span>           | <span data-ttu-id="6d26c-267">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6d26c-267">0x08000014</span></span>                      |
| <span data-ttu-id="6d26c-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6d26c-268">Classes used in</span></span>        | [<span data-ttu-id="6d26c-269">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="6d26c-269">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6d26c-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6d26c-270">Windows Server 2012</span></span>



| <span data-ttu-id="6d26c-271">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d26c-271">Entry</span></span> | <span data-ttu-id="6d26c-272">Wert</span><span class="sxs-lookup"><span data-stu-id="6d26c-272">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6d26c-273">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6d26c-273">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6d26c-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d26c-274">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6d26c-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d26c-275">System-Only</span></span>            | <span data-ttu-id="6d26c-276">Richtig</span><span class="sxs-lookup"><span data-stu-id="6d26c-276">True</span></span>                            |
| <span data-ttu-id="6d26c-277">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6d26c-277">Is-Single-Valued</span></span>       | <span data-ttu-id="6d26c-278">False</span><span class="sxs-lookup"><span data-stu-id="6d26c-278">False</span></span>                           |
| <span data-ttu-id="6d26c-279">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6d26c-279">Is Indexed</span></span>             | <span data-ttu-id="6d26c-280">False</span><span class="sxs-lookup"><span data-stu-id="6d26c-280">False</span></span>                           |
| <span data-ttu-id="6d26c-281">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6d26c-281">In Global Catalog</span></span>      | <span data-ttu-id="6d26c-282">False</span><span class="sxs-lookup"><span data-stu-id="6d26c-282">False</span></span>                           |
| <span data-ttu-id="6d26c-283">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6d26c-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d26c-284">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6d26c-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6d26c-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d26c-285">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6d26c-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d26c-286">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6d26c-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d26c-287">Search-Flags</span></span>           | <span data-ttu-id="6d26c-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d26c-288">0x00000000</span></span>                      |
| <span data-ttu-id="6d26c-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d26c-289">System-Flags</span></span>           | <span data-ttu-id="6d26c-290">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6d26c-290">0x08000014</span></span>                      |
| <span data-ttu-id="6d26c-291">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6d26c-291">Classes used in</span></span>        | [<span data-ttu-id="6d26c-292">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="6d26c-292">**Top**</span></span>](c-top.md)<br/> |



 

 





