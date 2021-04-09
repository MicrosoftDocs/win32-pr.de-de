---
title: Allowed-Child-Classes-effektives Attribut
description: Eine Liste der Klassen, die geändert werden können.
ms.assetid: e7c30918-3aac-4c08-bd98-60ddc704769f
ms.tgt_platform: multiple
keywords:
- Zulässige und untergeordnete Klassen-effektives Attribut AD-Schema
- AD-Schema für das Attribut "attribuwedchildclasseseffective"
topic_type:
- apiref
api_name:
- Allowed-Child-Classes-Effective
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c9ead0a7f8e03b545d28c5f4c3bf266c3acba54
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859926"
---
# <a name="allowed-child-classes-effective-attribute"></a><span data-ttu-id="e5a34-105">Allowed-Child-Classes-effektives Attribut</span><span class="sxs-lookup"><span data-stu-id="e5a34-105">Allowed-Child-Classes-Effective attribute</span></span>

<span data-ttu-id="e5a34-106">Eine Liste der Klassen, die geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="e5a34-106">A list of classes that can be modified.</span></span>



| <span data-ttu-id="e5a34-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e5a34-107">Entry</span></span> | <span data-ttu-id="e5a34-108">Wert</span><span class="sxs-lookup"><span data-stu-id="e5a34-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="e5a34-109">CN</span><span class="sxs-lookup"><span data-stu-id="e5a34-109">CN</span></span>                | <span data-ttu-id="e5a34-110">Zulässig-untergeordnete Klassen-gültig</span><span class="sxs-lookup"><span data-stu-id="e5a34-110">Allowed-Child-Classes-Effective</span></span>                                 |
| <span data-ttu-id="e5a34-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e5a34-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e5a34-112">Zuordnung von "Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="e5a34-112">allowedChildClassesEffective</span></span>                                    |
| <span data-ttu-id="e5a34-113">Size</span><span class="sxs-lookup"><span data-stu-id="e5a34-113">Size</span></span>              | \-                                                              |
| <span data-ttu-id="e5a34-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="e5a34-114">Update Privilege</span></span>  | \-                                                              |
| <span data-ttu-id="e5a34-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="e5a34-115">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="e5a34-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e5a34-116">Attribute-Id</span></span>      | <span data-ttu-id="e5a34-117">1.2.840.113556.1.4.912</span><span class="sxs-lookup"><span data-stu-id="e5a34-117">1.2.840.113556.1.4.912</span></span>                                          |
| <span data-ttu-id="e5a34-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e5a34-118">System-Id-Guid</span></span>    | <span data-ttu-id="e5a34-119">9a7ad943-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="e5a34-119">9a7ad943-ca53-11d1-bbd0-0080c76670c0</span></span>                            |
| <span data-ttu-id="e5a34-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5a34-120">Syntax</span></span>            | [<span data-ttu-id="e5a34-121">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="e5a34-121">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="e5a34-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="e5a34-122">Implementations</span></span>

-   [<span data-ttu-id="e5a34-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e5a34-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e5a34-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e5a34-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e5a34-125">**Adam**</span><span class="sxs-lookup"><span data-stu-id="e5a34-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e5a34-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e5a34-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e5a34-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e5a34-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e5a34-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e5a34-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e5a34-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e5a34-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e5a34-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e5a34-130">Windows 2000 Server</span></span>



| <span data-ttu-id="e5a34-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e5a34-131">Entry</span></span> | <span data-ttu-id="e5a34-132">Wert</span><span class="sxs-lookup"><span data-stu-id="e5a34-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e5a34-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e5a34-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e5a34-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5a34-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e5a34-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5a34-135">System-Only</span></span>            | <span data-ttu-id="e5a34-136">Richtig</span><span class="sxs-lookup"><span data-stu-id="e5a34-136">True</span></span>                            |
| <span data-ttu-id="e5a34-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e5a34-137">Is-Single-Valued</span></span>       | <span data-ttu-id="e5a34-138">False</span><span class="sxs-lookup"><span data-stu-id="e5a34-138">False</span></span>                           |
| <span data-ttu-id="e5a34-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e5a34-139">Is Indexed</span></span>             | <span data-ttu-id="e5a34-140">False</span><span class="sxs-lookup"><span data-stu-id="e5a34-140">False</span></span>                           |
| <span data-ttu-id="e5a34-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e5a34-141">In Global Catalog</span></span>      | <span data-ttu-id="e5a34-142">False</span><span class="sxs-lookup"><span data-stu-id="e5a34-142">False</span></span>                           |
| <span data-ttu-id="e5a34-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e5a34-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5a34-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e5a34-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e5a34-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5a34-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e5a34-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5a34-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e5a34-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5a34-147">Search-Flags</span></span>           | <span data-ttu-id="e5a34-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5a34-148">0x00000000</span></span>                      |
| <span data-ttu-id="e5a34-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5a34-149">System-Flags</span></span>           | <span data-ttu-id="e5a34-150">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e5a34-150">0x08000014</span></span>                      |
| <span data-ttu-id="e5a34-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e5a34-151">Classes used in</span></span>        | [<span data-ttu-id="e5a34-152">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="e5a34-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e5a34-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e5a34-153">Windows Server 2003</span></span>



| <span data-ttu-id="e5a34-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e5a34-154">Entry</span></span> | <span data-ttu-id="e5a34-155">Wert</span><span class="sxs-lookup"><span data-stu-id="e5a34-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e5a34-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e5a34-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e5a34-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5a34-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e5a34-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5a34-158">System-Only</span></span>            | <span data-ttu-id="e5a34-159">Richtig</span><span class="sxs-lookup"><span data-stu-id="e5a34-159">True</span></span>                            |
| <span data-ttu-id="e5a34-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e5a34-160">Is-Single-Valued</span></span>       | <span data-ttu-id="e5a34-161">False</span><span class="sxs-lookup"><span data-stu-id="e5a34-161">False</span></span>                           |
| <span data-ttu-id="e5a34-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e5a34-162">Is Indexed</span></span>             | <span data-ttu-id="e5a34-163">False</span><span class="sxs-lookup"><span data-stu-id="e5a34-163">False</span></span>                           |
| <span data-ttu-id="e5a34-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e5a34-164">In Global Catalog</span></span>      | <span data-ttu-id="e5a34-165">False</span><span class="sxs-lookup"><span data-stu-id="e5a34-165">False</span></span>                           |
| <span data-ttu-id="e5a34-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e5a34-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5a34-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e5a34-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e5a34-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5a34-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e5a34-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5a34-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e5a34-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5a34-170">Search-Flags</span></span>           | <span data-ttu-id="e5a34-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5a34-171">0x00000000</span></span>                      |
| <span data-ttu-id="e5a34-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5a34-172">System-Flags</span></span>           | <span data-ttu-id="e5a34-173">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e5a34-173">0x08000014</span></span>                      |
| <span data-ttu-id="e5a34-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e5a34-174">Classes used in</span></span>        | [<span data-ttu-id="e5a34-175">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="e5a34-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e5a34-176">Adam</span><span class="sxs-lookup"><span data-stu-id="e5a34-176">ADAM</span></span>



| <span data-ttu-id="e5a34-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e5a34-177">Entry</span></span> | <span data-ttu-id="e5a34-178">Wert</span><span class="sxs-lookup"><span data-stu-id="e5a34-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e5a34-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e5a34-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e5a34-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5a34-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e5a34-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5a34-181">System-Only</span></span>            | <span data-ttu-id="e5a34-182">Richtig</span><span class="sxs-lookup"><span data-stu-id="e5a34-182">True</span></span>                            |
| <span data-ttu-id="e5a34-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e5a34-183">Is-Single-Valued</span></span>       | <span data-ttu-id="e5a34-184">False</span><span class="sxs-lookup"><span data-stu-id="e5a34-184">False</span></span>                           |
| <span data-ttu-id="e5a34-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e5a34-185">Is Indexed</span></span>             | <span data-ttu-id="e5a34-186">False</span><span class="sxs-lookup"><span data-stu-id="e5a34-186">False</span></span>                           |
| <span data-ttu-id="e5a34-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e5a34-187">In Global Catalog</span></span>      | <span data-ttu-id="e5a34-188">False</span><span class="sxs-lookup"><span data-stu-id="e5a34-188">False</span></span>                           |
| <span data-ttu-id="e5a34-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e5a34-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5a34-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e5a34-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e5a34-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5a34-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e5a34-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5a34-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e5a34-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5a34-193">Search-Flags</span></span>           | <span data-ttu-id="e5a34-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5a34-194">0x00000000</span></span>                      |
| <span data-ttu-id="e5a34-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5a34-195">System-Flags</span></span>           | <span data-ttu-id="e5a34-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e5a34-196">0x08000014</span></span>                      |
| <span data-ttu-id="e5a34-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e5a34-197">Classes used in</span></span>        | [<span data-ttu-id="e5a34-198">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="e5a34-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e5a34-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e5a34-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e5a34-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e5a34-200">Entry</span></span> | <span data-ttu-id="e5a34-201">Wert</span><span class="sxs-lookup"><span data-stu-id="e5a34-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e5a34-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e5a34-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e5a34-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5a34-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e5a34-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5a34-204">System-Only</span></span>            | <span data-ttu-id="e5a34-205">Richtig</span><span class="sxs-lookup"><span data-stu-id="e5a34-205">True</span></span>                            |
| <span data-ttu-id="e5a34-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e5a34-206">Is-Single-Valued</span></span>       | <span data-ttu-id="e5a34-207">False</span><span class="sxs-lookup"><span data-stu-id="e5a34-207">False</span></span>                           |
| <span data-ttu-id="e5a34-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e5a34-208">Is Indexed</span></span>             | <span data-ttu-id="e5a34-209">False</span><span class="sxs-lookup"><span data-stu-id="e5a34-209">False</span></span>                           |
| <span data-ttu-id="e5a34-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e5a34-210">In Global Catalog</span></span>      | <span data-ttu-id="e5a34-211">False</span><span class="sxs-lookup"><span data-stu-id="e5a34-211">False</span></span>                           |
| <span data-ttu-id="e5a34-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e5a34-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5a34-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e5a34-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e5a34-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5a34-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e5a34-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5a34-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e5a34-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5a34-216">Search-Flags</span></span>           | <span data-ttu-id="e5a34-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5a34-217">0x00000000</span></span>                      |
| <span data-ttu-id="e5a34-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5a34-218">System-Flags</span></span>           | <span data-ttu-id="e5a34-219">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e5a34-219">0x08000014</span></span>                      |
| <span data-ttu-id="e5a34-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e5a34-220">Classes used in</span></span>        | [<span data-ttu-id="e5a34-221">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="e5a34-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e5a34-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5a34-222">Windows Server 2008</span></span>



| <span data-ttu-id="e5a34-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e5a34-223">Entry</span></span> | <span data-ttu-id="e5a34-224">Wert</span><span class="sxs-lookup"><span data-stu-id="e5a34-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e5a34-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e5a34-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e5a34-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5a34-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e5a34-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5a34-227">System-Only</span></span>            | <span data-ttu-id="e5a34-228">Richtig</span><span class="sxs-lookup"><span data-stu-id="e5a34-228">True</span></span>                            |
| <span data-ttu-id="e5a34-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e5a34-229">Is-Single-Valued</span></span>       | <span data-ttu-id="e5a34-230">False</span><span class="sxs-lookup"><span data-stu-id="e5a34-230">False</span></span>                           |
| <span data-ttu-id="e5a34-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e5a34-231">Is Indexed</span></span>             | <span data-ttu-id="e5a34-232">False</span><span class="sxs-lookup"><span data-stu-id="e5a34-232">False</span></span>                           |
| <span data-ttu-id="e5a34-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e5a34-233">In Global Catalog</span></span>      | <span data-ttu-id="e5a34-234">False</span><span class="sxs-lookup"><span data-stu-id="e5a34-234">False</span></span>                           |
| <span data-ttu-id="e5a34-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e5a34-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5a34-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e5a34-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e5a34-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5a34-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e5a34-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5a34-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e5a34-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5a34-239">Search-Flags</span></span>           | <span data-ttu-id="e5a34-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5a34-240">0x00000000</span></span>                      |
| <span data-ttu-id="e5a34-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5a34-241">System-Flags</span></span>           | <span data-ttu-id="e5a34-242">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e5a34-242">0x08000014</span></span>                      |
| <span data-ttu-id="e5a34-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e5a34-243">Classes used in</span></span>        | [<span data-ttu-id="e5a34-244">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="e5a34-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e5a34-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e5a34-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e5a34-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e5a34-246">Entry</span></span> | <span data-ttu-id="e5a34-247">Wert</span><span class="sxs-lookup"><span data-stu-id="e5a34-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e5a34-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e5a34-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e5a34-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5a34-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e5a34-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5a34-250">System-Only</span></span>            | <span data-ttu-id="e5a34-251">Richtig</span><span class="sxs-lookup"><span data-stu-id="e5a34-251">True</span></span>                            |
| <span data-ttu-id="e5a34-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e5a34-252">Is-Single-Valued</span></span>       | <span data-ttu-id="e5a34-253">False</span><span class="sxs-lookup"><span data-stu-id="e5a34-253">False</span></span>                           |
| <span data-ttu-id="e5a34-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e5a34-254">Is Indexed</span></span>             | <span data-ttu-id="e5a34-255">False</span><span class="sxs-lookup"><span data-stu-id="e5a34-255">False</span></span>                           |
| <span data-ttu-id="e5a34-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e5a34-256">In Global Catalog</span></span>      | <span data-ttu-id="e5a34-257">False</span><span class="sxs-lookup"><span data-stu-id="e5a34-257">False</span></span>                           |
| <span data-ttu-id="e5a34-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e5a34-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5a34-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e5a34-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e5a34-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5a34-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e5a34-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5a34-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e5a34-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5a34-262">Search-Flags</span></span>           | <span data-ttu-id="e5a34-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5a34-263">0x00000000</span></span>                      |
| <span data-ttu-id="e5a34-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5a34-264">System-Flags</span></span>           | <span data-ttu-id="e5a34-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e5a34-265">0x08000014</span></span>                      |
| <span data-ttu-id="e5a34-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e5a34-266">Classes used in</span></span>        | [<span data-ttu-id="e5a34-267">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="e5a34-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e5a34-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e5a34-268">Windows Server 2012</span></span>



| <span data-ttu-id="e5a34-269">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e5a34-269">Entry</span></span> | <span data-ttu-id="e5a34-270">Wert</span><span class="sxs-lookup"><span data-stu-id="e5a34-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e5a34-271">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e5a34-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e5a34-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5a34-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e5a34-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5a34-273">System-Only</span></span>            | <span data-ttu-id="e5a34-274">Richtig</span><span class="sxs-lookup"><span data-stu-id="e5a34-274">True</span></span>                            |
| <span data-ttu-id="e5a34-275">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e5a34-275">Is-Single-Valued</span></span>       | <span data-ttu-id="e5a34-276">False</span><span class="sxs-lookup"><span data-stu-id="e5a34-276">False</span></span>                           |
| <span data-ttu-id="e5a34-277">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e5a34-277">Is Indexed</span></span>             | <span data-ttu-id="e5a34-278">False</span><span class="sxs-lookup"><span data-stu-id="e5a34-278">False</span></span>                           |
| <span data-ttu-id="e5a34-279">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e5a34-279">In Global Catalog</span></span>      | <span data-ttu-id="e5a34-280">False</span><span class="sxs-lookup"><span data-stu-id="e5a34-280">False</span></span>                           |
| <span data-ttu-id="e5a34-281">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e5a34-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5a34-282">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e5a34-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e5a34-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5a34-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e5a34-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5a34-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e5a34-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5a34-285">Search-Flags</span></span>           | <span data-ttu-id="e5a34-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5a34-286">0x00000000</span></span>                      |
| <span data-ttu-id="e5a34-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5a34-287">System-Flags</span></span>           | <span data-ttu-id="e5a34-288">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e5a34-288">0x08000014</span></span>                      |
| <span data-ttu-id="e5a34-289">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e5a34-289">Classes used in</span></span>        | [<span data-ttu-id="e5a34-290">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="e5a34-290">**Top**</span></span>](c-top.md)<br/> |



 

 





