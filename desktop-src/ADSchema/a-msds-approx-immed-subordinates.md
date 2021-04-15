---
title: ms-DS-ca-immed-untergeordnete Attribute
description: Der von diesem Attribut zurückgegebene Wert basiert auf Index Größen. Dies ist möglicherweise auf "+/\ 8211; 10" für große Container deaktiviert, und der Fehler ist theoretisch unbegrenzt, aber die Verwendung dieses Attributs hilft der Benutzeroberfläche, den Inhalt eines Containers anzuzeigen.
ms.assetid: 0d6e3b53-dfad-49ac-bbb3-e53c33ea9cd8
ms.tgt_platform: multiple
keywords:
- ms-DS-ca-immed-untergeordnete Attribute ad-Schema
- MSDS-ca-immed-untergeordnete Attribute ad-Schema
topic_type:
- apiref
api_name:
- ms-DS-Approx-Immed-Subordinates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdb51ef642c216d8e41b774ffc596a8f3d4feb28
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104520191"
---
# <a name="ms-ds-approx-immed-subordinates-attribute"></a><span data-ttu-id="1af86-106">ms-DS-ca-immed-untergeordnete Attribute</span><span class="sxs-lookup"><span data-stu-id="1af86-106">ms-DS-Approx-Immed-Subordinates attribute</span></span>

<span data-ttu-id="1af86-107">Der von diesem Attribut zurückgegebene Wert basiert auf Index Größen.</span><span class="sxs-lookup"><span data-stu-id="1af86-107">The value returned by this attribute is based on index sizes.</span></span> <span data-ttu-id="1af86-108">Dies kann für große Container von +/10% liegen, und der Fehler ist theoretisch unbegrenzt, aber die Verwendung dieses Attributs ermöglicht der Benutzeroberfläche, den Inhalt eines Containers anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1af86-108">This may be off by +/ 10% on large containers, and the error is theoretically unbounded, but using this attribute helps the UI display the contents of a container.</span></span>



| <span data-ttu-id="1af86-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1af86-109">Entry</span></span> | <span data-ttu-id="1af86-110">Wert</span><span class="sxs-lookup"><span data-stu-id="1af86-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="1af86-111">CN</span><span class="sxs-lookup"><span data-stu-id="1af86-111">CN</span></span>                | <span data-ttu-id="1af86-112">ms-DS-ca-immed-untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1af86-112">ms-DS-Approx-Immed-Subordinates</span></span>      |
| <span data-ttu-id="1af86-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1af86-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1af86-114">MSDS-ca-immed-untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1af86-114">msDS-Approx-Immed-Subordinates</span></span>       |
| <span data-ttu-id="1af86-115">Size</span><span class="sxs-lookup"><span data-stu-id="1af86-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="1af86-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="1af86-116">Update Privilege</span></span>  | <span data-ttu-id="1af86-117">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1af86-117">This value is set by the system.</span></span>     |
| <span data-ttu-id="1af86-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="1af86-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="1af86-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1af86-119">Attribute-Id</span></span>      | <span data-ttu-id="1af86-120">1.2.840.113556.1.4.1669</span><span class="sxs-lookup"><span data-stu-id="1af86-120">1.2.840.113556.1.4.1669</span></span>              |
| <span data-ttu-id="1af86-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1af86-121">System-Id-Guid</span></span>    | <span data-ttu-id="1af86-122">e185d243-f6ce-4adb-b496-b0c005d7823c</span><span class="sxs-lookup"><span data-stu-id="1af86-122">e185d243-f6ce-4adb-b496-b0c005d7823c</span></span> |
| <span data-ttu-id="1af86-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="1af86-123">Syntax</span></span>            | [<span data-ttu-id="1af86-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="1af86-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="1af86-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="1af86-125">Implementations</span></span>

-   [<span data-ttu-id="1af86-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1af86-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1af86-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="1af86-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1af86-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1af86-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1af86-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1af86-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1af86-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1af86-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1af86-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1af86-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="1af86-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1af86-132">Windows Server 2003</span></span>



| <span data-ttu-id="1af86-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1af86-133">Entry</span></span> | <span data-ttu-id="1af86-134">Wert</span><span class="sxs-lookup"><span data-stu-id="1af86-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1af86-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1af86-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1af86-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1af86-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1af86-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="1af86-137">System-Only</span></span>            | <span data-ttu-id="1af86-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="1af86-138">True</span></span>                            |
| <span data-ttu-id="1af86-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1af86-139">Is-Single-Valued</span></span>       | <span data-ttu-id="1af86-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="1af86-140">True</span></span>                            |
| <span data-ttu-id="1af86-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1af86-141">Is Indexed</span></span>             | <span data-ttu-id="1af86-142">False</span><span class="sxs-lookup"><span data-stu-id="1af86-142">False</span></span>                           |
| <span data-ttu-id="1af86-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1af86-143">In Global Catalog</span></span>      | <span data-ttu-id="1af86-144">False</span><span class="sxs-lookup"><span data-stu-id="1af86-144">False</span></span>                           |
| <span data-ttu-id="1af86-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1af86-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="1af86-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1af86-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1af86-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1af86-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1af86-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1af86-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1af86-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1af86-149">Search-Flags</span></span>           | <span data-ttu-id="1af86-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1af86-150">0x00000000</span></span>                      |
| <span data-ttu-id="1af86-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1af86-151">System-Flags</span></span>           | <span data-ttu-id="1af86-152">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1af86-152">0x00000014</span></span>                      |
| <span data-ttu-id="1af86-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1af86-153">Classes used in</span></span>        | [<span data-ttu-id="1af86-154">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="1af86-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1af86-155">Adam</span><span class="sxs-lookup"><span data-stu-id="1af86-155">ADAM</span></span>



| <span data-ttu-id="1af86-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1af86-156">Entry</span></span> | <span data-ttu-id="1af86-157">Wert</span><span class="sxs-lookup"><span data-stu-id="1af86-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1af86-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1af86-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1af86-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1af86-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1af86-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="1af86-160">System-Only</span></span>            | <span data-ttu-id="1af86-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="1af86-161">True</span></span>                            |
| <span data-ttu-id="1af86-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1af86-162">Is-Single-Valued</span></span>       | <span data-ttu-id="1af86-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="1af86-163">True</span></span>                            |
| <span data-ttu-id="1af86-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1af86-164">Is Indexed</span></span>             | <span data-ttu-id="1af86-165">False</span><span class="sxs-lookup"><span data-stu-id="1af86-165">False</span></span>                           |
| <span data-ttu-id="1af86-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1af86-166">In Global Catalog</span></span>      | <span data-ttu-id="1af86-167">False</span><span class="sxs-lookup"><span data-stu-id="1af86-167">False</span></span>                           |
| <span data-ttu-id="1af86-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1af86-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="1af86-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1af86-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1af86-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1af86-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1af86-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1af86-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1af86-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1af86-172">Search-Flags</span></span>           | <span data-ttu-id="1af86-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1af86-173">0x00000000</span></span>                      |
| <span data-ttu-id="1af86-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1af86-174">System-Flags</span></span>           | <span data-ttu-id="1af86-175">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1af86-175">0x00000014</span></span>                      |
| <span data-ttu-id="1af86-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1af86-176">Classes used in</span></span>        | [<span data-ttu-id="1af86-177">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="1af86-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1af86-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1af86-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1af86-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1af86-179">Entry</span></span> | <span data-ttu-id="1af86-180">Wert</span><span class="sxs-lookup"><span data-stu-id="1af86-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1af86-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1af86-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1af86-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1af86-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1af86-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="1af86-183">System-Only</span></span>            | <span data-ttu-id="1af86-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="1af86-184">True</span></span>                            |
| <span data-ttu-id="1af86-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1af86-185">Is-Single-Valued</span></span>       | <span data-ttu-id="1af86-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="1af86-186">True</span></span>                            |
| <span data-ttu-id="1af86-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1af86-187">Is Indexed</span></span>             | <span data-ttu-id="1af86-188">False</span><span class="sxs-lookup"><span data-stu-id="1af86-188">False</span></span>                           |
| <span data-ttu-id="1af86-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1af86-189">In Global Catalog</span></span>      | <span data-ttu-id="1af86-190">False</span><span class="sxs-lookup"><span data-stu-id="1af86-190">False</span></span>                           |
| <span data-ttu-id="1af86-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1af86-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="1af86-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1af86-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1af86-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1af86-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1af86-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1af86-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1af86-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1af86-195">Search-Flags</span></span>           | <span data-ttu-id="1af86-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1af86-196">0x00000000</span></span>                      |
| <span data-ttu-id="1af86-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1af86-197">System-Flags</span></span>           | <span data-ttu-id="1af86-198">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1af86-198">0x00000014</span></span>                      |
| <span data-ttu-id="1af86-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1af86-199">Classes used in</span></span>        | [<span data-ttu-id="1af86-200">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="1af86-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1af86-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1af86-201">Windows Server 2008</span></span>



| <span data-ttu-id="1af86-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1af86-202">Entry</span></span> | <span data-ttu-id="1af86-203">Wert</span><span class="sxs-lookup"><span data-stu-id="1af86-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1af86-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1af86-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1af86-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1af86-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1af86-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="1af86-206">System-Only</span></span>            | <span data-ttu-id="1af86-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="1af86-207">True</span></span>                            |
| <span data-ttu-id="1af86-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1af86-208">Is-Single-Valued</span></span>       | <span data-ttu-id="1af86-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="1af86-209">True</span></span>                            |
| <span data-ttu-id="1af86-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1af86-210">Is Indexed</span></span>             | <span data-ttu-id="1af86-211">False</span><span class="sxs-lookup"><span data-stu-id="1af86-211">False</span></span>                           |
| <span data-ttu-id="1af86-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1af86-212">In Global Catalog</span></span>      | <span data-ttu-id="1af86-213">False</span><span class="sxs-lookup"><span data-stu-id="1af86-213">False</span></span>                           |
| <span data-ttu-id="1af86-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1af86-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="1af86-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1af86-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1af86-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1af86-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1af86-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1af86-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1af86-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1af86-218">Search-Flags</span></span>           | <span data-ttu-id="1af86-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1af86-219">0x00000000</span></span>                      |
| <span data-ttu-id="1af86-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1af86-220">System-Flags</span></span>           | <span data-ttu-id="1af86-221">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1af86-221">0x00000014</span></span>                      |
| <span data-ttu-id="1af86-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1af86-222">Classes used in</span></span>        | [<span data-ttu-id="1af86-223">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="1af86-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1af86-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1af86-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1af86-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1af86-225">Entry</span></span> | <span data-ttu-id="1af86-226">Wert</span><span class="sxs-lookup"><span data-stu-id="1af86-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1af86-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1af86-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1af86-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1af86-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1af86-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="1af86-229">System-Only</span></span>            | <span data-ttu-id="1af86-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="1af86-230">True</span></span>                            |
| <span data-ttu-id="1af86-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1af86-231">Is-Single-Valued</span></span>       | <span data-ttu-id="1af86-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="1af86-232">True</span></span>                            |
| <span data-ttu-id="1af86-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1af86-233">Is Indexed</span></span>             | <span data-ttu-id="1af86-234">False</span><span class="sxs-lookup"><span data-stu-id="1af86-234">False</span></span>                           |
| <span data-ttu-id="1af86-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1af86-235">In Global Catalog</span></span>      | <span data-ttu-id="1af86-236">False</span><span class="sxs-lookup"><span data-stu-id="1af86-236">False</span></span>                           |
| <span data-ttu-id="1af86-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1af86-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="1af86-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1af86-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1af86-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1af86-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1af86-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1af86-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1af86-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1af86-241">Search-Flags</span></span>           | <span data-ttu-id="1af86-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1af86-242">0x00000000</span></span>                      |
| <span data-ttu-id="1af86-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1af86-243">System-Flags</span></span>           | <span data-ttu-id="1af86-244">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1af86-244">0x00000014</span></span>                      |
| <span data-ttu-id="1af86-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1af86-245">Classes used in</span></span>        | [<span data-ttu-id="1af86-246">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="1af86-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1af86-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1af86-247">Windows Server 2012</span></span>



| <span data-ttu-id="1af86-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1af86-248">Entry</span></span> | <span data-ttu-id="1af86-249">Wert</span><span class="sxs-lookup"><span data-stu-id="1af86-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1af86-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1af86-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1af86-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1af86-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1af86-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="1af86-252">System-Only</span></span>            | <span data-ttu-id="1af86-253">Richtig</span><span class="sxs-lookup"><span data-stu-id="1af86-253">True</span></span>                            |
| <span data-ttu-id="1af86-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1af86-254">Is-Single-Valued</span></span>       | <span data-ttu-id="1af86-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="1af86-255">True</span></span>                            |
| <span data-ttu-id="1af86-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1af86-256">Is Indexed</span></span>             | <span data-ttu-id="1af86-257">False</span><span class="sxs-lookup"><span data-stu-id="1af86-257">False</span></span>                           |
| <span data-ttu-id="1af86-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1af86-258">In Global Catalog</span></span>      | <span data-ttu-id="1af86-259">False</span><span class="sxs-lookup"><span data-stu-id="1af86-259">False</span></span>                           |
| <span data-ttu-id="1af86-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1af86-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="1af86-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1af86-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1af86-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1af86-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1af86-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1af86-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1af86-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1af86-264">Search-Flags</span></span>           | <span data-ttu-id="1af86-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1af86-265">0x00000000</span></span>                      |
| <span data-ttu-id="1af86-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1af86-266">System-Flags</span></span>           | <span data-ttu-id="1af86-267">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1af86-267">0x00000014</span></span>                      |
| <span data-ttu-id="1af86-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1af86-268">Classes used in</span></span>        | [<span data-ttu-id="1af86-269">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="1af86-269">**Top**</span></span>](c-top.md)<br/> |



 

 





