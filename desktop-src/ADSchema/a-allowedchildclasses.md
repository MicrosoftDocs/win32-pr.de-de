---
title: Zulässige Attribute für untergeordnete Klassen
description: Klassen, die in einer Klasse enthalten sein können.
ms.assetid: 3bfeefe3-b728-40a2-8b0a-3064a9ca42d0
ms.tgt_platform: multiple
keywords:
- Das Active Directory-Attribut für den untergeordneten Klassen
- AD-Schema des attribuwedchildclasses-Attributs
topic_type:
- apiref
api_name:
- Allowed-Child-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45c295036ad8b1c132e2dbf97d2e0d9ab38f9598
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103745304"
---
# <a name="allowed-child-classes-attribute"></a><span data-ttu-id="431bf-105">Zulässige Attribute für untergeordnete Klassen</span><span class="sxs-lookup"><span data-stu-id="431bf-105">Allowed-Child-Classes attribute</span></span>

<span data-ttu-id="431bf-106">Klassen, die in einer Klasse enthalten sein können.</span><span class="sxs-lookup"><span data-stu-id="431bf-106">Classes that can be contained by a class.</span></span>



| <span data-ttu-id="431bf-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="431bf-107">Entry</span></span> | <span data-ttu-id="431bf-108">Wert</span><span class="sxs-lookup"><span data-stu-id="431bf-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="431bf-109">CN</span><span class="sxs-lookup"><span data-stu-id="431bf-109">CN</span></span>                | <span data-ttu-id="431bf-110">Zulässige, untergeordnete Klassen</span><span class="sxs-lookup"><span data-stu-id="431bf-110">Allowed-Child-Classes</span></span>                                           |
| <span data-ttu-id="431bf-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="431bf-111">Ldap-Display-Name</span></span> | <span data-ttu-id="431bf-112">"Zuweisung von Klassen"</span><span class="sxs-lookup"><span data-stu-id="431bf-112">allowedChildClasses</span></span>                                             |
| <span data-ttu-id="431bf-113">Size</span><span class="sxs-lookup"><span data-stu-id="431bf-113">Size</span></span>              | \-                                                              |
| <span data-ttu-id="431bf-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="431bf-114">Update Privilege</span></span>  | \-                                                              |
| <span data-ttu-id="431bf-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="431bf-115">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="431bf-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="431bf-116">Attribute-Id</span></span>      | <span data-ttu-id="431bf-117">1.2.840.113556.1.4.911</span><span class="sxs-lookup"><span data-stu-id="431bf-117">1.2.840.113556.1.4.911</span></span>                                          |
| <span data-ttu-id="431bf-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="431bf-118">System-Id-Guid</span></span>    | <span data-ttu-id="431bf-119">9a7ad942-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="431bf-119">9a7ad942-ca53-11d1-bbd0-0080c76670c0</span></span>                            |
| <span data-ttu-id="431bf-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="431bf-120">Syntax</span></span>            | [<span data-ttu-id="431bf-121">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="431bf-121">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="431bf-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="431bf-122">Implementations</span></span>

-   [<span data-ttu-id="431bf-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="431bf-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="431bf-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="431bf-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="431bf-125">**Adam**</span><span class="sxs-lookup"><span data-stu-id="431bf-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="431bf-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="431bf-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="431bf-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="431bf-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="431bf-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="431bf-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="431bf-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="431bf-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="431bf-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="431bf-130">Windows 2000 Server</span></span>



| <span data-ttu-id="431bf-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="431bf-131">Entry</span></span> | <span data-ttu-id="431bf-132">Wert</span><span class="sxs-lookup"><span data-stu-id="431bf-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="431bf-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="431bf-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="431bf-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="431bf-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="431bf-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="431bf-135">System-Only</span></span>            | <span data-ttu-id="431bf-136">Richtig</span><span class="sxs-lookup"><span data-stu-id="431bf-136">True</span></span>                            |
| <span data-ttu-id="431bf-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="431bf-137">Is-Single-Valued</span></span>       | <span data-ttu-id="431bf-138">False</span><span class="sxs-lookup"><span data-stu-id="431bf-138">False</span></span>                           |
| <span data-ttu-id="431bf-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="431bf-139">Is Indexed</span></span>             | <span data-ttu-id="431bf-140">False</span><span class="sxs-lookup"><span data-stu-id="431bf-140">False</span></span>                           |
| <span data-ttu-id="431bf-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="431bf-141">In Global Catalog</span></span>      | <span data-ttu-id="431bf-142">False</span><span class="sxs-lookup"><span data-stu-id="431bf-142">False</span></span>                           |
| <span data-ttu-id="431bf-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="431bf-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="431bf-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="431bf-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="431bf-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="431bf-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="431bf-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="431bf-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="431bf-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="431bf-147">Search-Flags</span></span>           | <span data-ttu-id="431bf-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="431bf-148">0x00000000</span></span>                      |
| <span data-ttu-id="431bf-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="431bf-149">System-Flags</span></span>           | <span data-ttu-id="431bf-150">0x08000014</span><span class="sxs-lookup"><span data-stu-id="431bf-150">0x08000014</span></span>                      |
| <span data-ttu-id="431bf-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="431bf-151">Classes used in</span></span>        | [<span data-ttu-id="431bf-152">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="431bf-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="431bf-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="431bf-153">Windows Server 2003</span></span>



| <span data-ttu-id="431bf-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="431bf-154">Entry</span></span> | <span data-ttu-id="431bf-155">Wert</span><span class="sxs-lookup"><span data-stu-id="431bf-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="431bf-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="431bf-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="431bf-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="431bf-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="431bf-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="431bf-158">System-Only</span></span>            | <span data-ttu-id="431bf-159">Richtig</span><span class="sxs-lookup"><span data-stu-id="431bf-159">True</span></span>                            |
| <span data-ttu-id="431bf-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="431bf-160">Is-Single-Valued</span></span>       | <span data-ttu-id="431bf-161">False</span><span class="sxs-lookup"><span data-stu-id="431bf-161">False</span></span>                           |
| <span data-ttu-id="431bf-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="431bf-162">Is Indexed</span></span>             | <span data-ttu-id="431bf-163">False</span><span class="sxs-lookup"><span data-stu-id="431bf-163">False</span></span>                           |
| <span data-ttu-id="431bf-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="431bf-164">In Global Catalog</span></span>      | <span data-ttu-id="431bf-165">False</span><span class="sxs-lookup"><span data-stu-id="431bf-165">False</span></span>                           |
| <span data-ttu-id="431bf-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="431bf-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="431bf-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="431bf-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="431bf-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="431bf-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="431bf-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="431bf-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="431bf-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="431bf-170">Search-Flags</span></span>           | <span data-ttu-id="431bf-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="431bf-171">0x00000000</span></span>                      |
| <span data-ttu-id="431bf-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="431bf-172">System-Flags</span></span>           | <span data-ttu-id="431bf-173">0x08000014</span><span class="sxs-lookup"><span data-stu-id="431bf-173">0x08000014</span></span>                      |
| <span data-ttu-id="431bf-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="431bf-174">Classes used in</span></span>        | [<span data-ttu-id="431bf-175">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="431bf-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="431bf-176">Adam</span><span class="sxs-lookup"><span data-stu-id="431bf-176">ADAM</span></span>



| <span data-ttu-id="431bf-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="431bf-177">Entry</span></span> | <span data-ttu-id="431bf-178">Wert</span><span class="sxs-lookup"><span data-stu-id="431bf-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="431bf-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="431bf-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="431bf-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="431bf-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="431bf-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="431bf-181">System-Only</span></span>            | <span data-ttu-id="431bf-182">Richtig</span><span class="sxs-lookup"><span data-stu-id="431bf-182">True</span></span>                            |
| <span data-ttu-id="431bf-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="431bf-183">Is-Single-Valued</span></span>       | <span data-ttu-id="431bf-184">False</span><span class="sxs-lookup"><span data-stu-id="431bf-184">False</span></span>                           |
| <span data-ttu-id="431bf-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="431bf-185">Is Indexed</span></span>             | <span data-ttu-id="431bf-186">False</span><span class="sxs-lookup"><span data-stu-id="431bf-186">False</span></span>                           |
| <span data-ttu-id="431bf-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="431bf-187">In Global Catalog</span></span>      | <span data-ttu-id="431bf-188">False</span><span class="sxs-lookup"><span data-stu-id="431bf-188">False</span></span>                           |
| <span data-ttu-id="431bf-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="431bf-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="431bf-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="431bf-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="431bf-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="431bf-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="431bf-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="431bf-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="431bf-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="431bf-193">Search-Flags</span></span>           | <span data-ttu-id="431bf-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="431bf-194">0x00000000</span></span>                      |
| <span data-ttu-id="431bf-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="431bf-195">System-Flags</span></span>           | <span data-ttu-id="431bf-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="431bf-196">0x08000014</span></span>                      |
| <span data-ttu-id="431bf-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="431bf-197">Classes used in</span></span>        | [<span data-ttu-id="431bf-198">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="431bf-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="431bf-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="431bf-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="431bf-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="431bf-200">Entry</span></span> | <span data-ttu-id="431bf-201">Wert</span><span class="sxs-lookup"><span data-stu-id="431bf-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="431bf-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="431bf-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="431bf-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="431bf-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="431bf-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="431bf-204">System-Only</span></span>            | <span data-ttu-id="431bf-205">Richtig</span><span class="sxs-lookup"><span data-stu-id="431bf-205">True</span></span>                            |
| <span data-ttu-id="431bf-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="431bf-206">Is-Single-Valued</span></span>       | <span data-ttu-id="431bf-207">False</span><span class="sxs-lookup"><span data-stu-id="431bf-207">False</span></span>                           |
| <span data-ttu-id="431bf-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="431bf-208">Is Indexed</span></span>             | <span data-ttu-id="431bf-209">False</span><span class="sxs-lookup"><span data-stu-id="431bf-209">False</span></span>                           |
| <span data-ttu-id="431bf-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="431bf-210">In Global Catalog</span></span>      | <span data-ttu-id="431bf-211">False</span><span class="sxs-lookup"><span data-stu-id="431bf-211">False</span></span>                           |
| <span data-ttu-id="431bf-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="431bf-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="431bf-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="431bf-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="431bf-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="431bf-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="431bf-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="431bf-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="431bf-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="431bf-216">Search-Flags</span></span>           | <span data-ttu-id="431bf-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="431bf-217">0x00000000</span></span>                      |
| <span data-ttu-id="431bf-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="431bf-218">System-Flags</span></span>           | <span data-ttu-id="431bf-219">0x08000014</span><span class="sxs-lookup"><span data-stu-id="431bf-219">0x08000014</span></span>                      |
| <span data-ttu-id="431bf-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="431bf-220">Classes used in</span></span>        | [<span data-ttu-id="431bf-221">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="431bf-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="431bf-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="431bf-222">Windows Server 2008</span></span>



| <span data-ttu-id="431bf-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="431bf-223">Entry</span></span> | <span data-ttu-id="431bf-224">Wert</span><span class="sxs-lookup"><span data-stu-id="431bf-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="431bf-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="431bf-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="431bf-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="431bf-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="431bf-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="431bf-227">System-Only</span></span>            | <span data-ttu-id="431bf-228">Richtig</span><span class="sxs-lookup"><span data-stu-id="431bf-228">True</span></span>                            |
| <span data-ttu-id="431bf-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="431bf-229">Is-Single-Valued</span></span>       | <span data-ttu-id="431bf-230">False</span><span class="sxs-lookup"><span data-stu-id="431bf-230">False</span></span>                           |
| <span data-ttu-id="431bf-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="431bf-231">Is Indexed</span></span>             | <span data-ttu-id="431bf-232">False</span><span class="sxs-lookup"><span data-stu-id="431bf-232">False</span></span>                           |
| <span data-ttu-id="431bf-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="431bf-233">In Global Catalog</span></span>      | <span data-ttu-id="431bf-234">False</span><span class="sxs-lookup"><span data-stu-id="431bf-234">False</span></span>                           |
| <span data-ttu-id="431bf-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="431bf-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="431bf-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="431bf-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="431bf-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="431bf-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="431bf-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="431bf-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="431bf-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="431bf-239">Search-Flags</span></span>           | <span data-ttu-id="431bf-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="431bf-240">0x00000000</span></span>                      |
| <span data-ttu-id="431bf-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="431bf-241">System-Flags</span></span>           | <span data-ttu-id="431bf-242">0x08000014</span><span class="sxs-lookup"><span data-stu-id="431bf-242">0x08000014</span></span>                      |
| <span data-ttu-id="431bf-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="431bf-243">Classes used in</span></span>        | [<span data-ttu-id="431bf-244">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="431bf-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="431bf-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="431bf-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="431bf-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="431bf-246">Entry</span></span> | <span data-ttu-id="431bf-247">Wert</span><span class="sxs-lookup"><span data-stu-id="431bf-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="431bf-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="431bf-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="431bf-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="431bf-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="431bf-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="431bf-250">System-Only</span></span>            | <span data-ttu-id="431bf-251">Richtig</span><span class="sxs-lookup"><span data-stu-id="431bf-251">True</span></span>                            |
| <span data-ttu-id="431bf-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="431bf-252">Is-Single-Valued</span></span>       | <span data-ttu-id="431bf-253">False</span><span class="sxs-lookup"><span data-stu-id="431bf-253">False</span></span>                           |
| <span data-ttu-id="431bf-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="431bf-254">Is Indexed</span></span>             | <span data-ttu-id="431bf-255">False</span><span class="sxs-lookup"><span data-stu-id="431bf-255">False</span></span>                           |
| <span data-ttu-id="431bf-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="431bf-256">In Global Catalog</span></span>      | <span data-ttu-id="431bf-257">False</span><span class="sxs-lookup"><span data-stu-id="431bf-257">False</span></span>                           |
| <span data-ttu-id="431bf-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="431bf-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="431bf-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="431bf-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="431bf-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="431bf-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="431bf-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="431bf-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="431bf-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="431bf-262">Search-Flags</span></span>           | <span data-ttu-id="431bf-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="431bf-263">0x00000000</span></span>                      |
| <span data-ttu-id="431bf-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="431bf-264">System-Flags</span></span>           | <span data-ttu-id="431bf-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="431bf-265">0x08000014</span></span>                      |
| <span data-ttu-id="431bf-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="431bf-266">Classes used in</span></span>        | [<span data-ttu-id="431bf-267">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="431bf-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="431bf-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="431bf-268">Windows Server 2012</span></span>



| <span data-ttu-id="431bf-269">Eingabe</span><span class="sxs-lookup"><span data-stu-id="431bf-269">Entry</span></span> | <span data-ttu-id="431bf-270">Wert</span><span class="sxs-lookup"><span data-stu-id="431bf-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="431bf-271">Link-ID</span><span class="sxs-lookup"><span data-stu-id="431bf-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="431bf-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="431bf-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="431bf-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="431bf-273">System-Only</span></span>            | <span data-ttu-id="431bf-274">Richtig</span><span class="sxs-lookup"><span data-stu-id="431bf-274">True</span></span>                            |
| <span data-ttu-id="431bf-275">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="431bf-275">Is-Single-Valued</span></span>       | <span data-ttu-id="431bf-276">False</span><span class="sxs-lookup"><span data-stu-id="431bf-276">False</span></span>                           |
| <span data-ttu-id="431bf-277">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="431bf-277">Is Indexed</span></span>             | <span data-ttu-id="431bf-278">False</span><span class="sxs-lookup"><span data-stu-id="431bf-278">False</span></span>                           |
| <span data-ttu-id="431bf-279">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="431bf-279">In Global Catalog</span></span>      | <span data-ttu-id="431bf-280">False</span><span class="sxs-lookup"><span data-stu-id="431bf-280">False</span></span>                           |
| <span data-ttu-id="431bf-281">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="431bf-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="431bf-282">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="431bf-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="431bf-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="431bf-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="431bf-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="431bf-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="431bf-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="431bf-285">Search-Flags</span></span>           | <span data-ttu-id="431bf-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="431bf-286">0x00000000</span></span>                      |
| <span data-ttu-id="431bf-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="431bf-287">System-Flags</span></span>           | <span data-ttu-id="431bf-288">0x08000014</span><span class="sxs-lookup"><span data-stu-id="431bf-288">0x08000014</span></span>                      |
| <span data-ttu-id="431bf-289">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="431bf-289">Classes used in</span></span>        | [<span data-ttu-id="431bf-290">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="431bf-290">**Top**</span></span>](c-top.md)<br/> |



 

 





