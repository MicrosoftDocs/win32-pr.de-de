---
title: Valid-Accesses-Attribut
description: Der Typ des Zugriffs, der mit einem erweiterten Recht zulässig ist.
ms.assetid: afb944ec-3b8f-41dd-8987-ed6c71f937ac
ms.tgt_platform: multiple
keywords:
- AD-Schema für Valid-Accesses-Attribut
- AD-Schema für validzugriffen
topic_type:
- apiref
api_name:
- Valid-Accesses
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c86ddf66affd4c6688ca331152a5d0c5af073a63
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957561"
---
# <a name="valid-accesses-attribute"></a><span data-ttu-id="cd5f2-105">Valid-Accesses-Attribut</span><span class="sxs-lookup"><span data-stu-id="cd5f2-105">Valid-Accesses attribute</span></span>

<span data-ttu-id="cd5f2-106">Der Typ des Zugriffs, der mit einem erweiterten Recht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="cd5f2-106">The type of access that is permitted with an extended right.</span></span>



| <span data-ttu-id="cd5f2-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cd5f2-107">Entry</span></span> | <span data-ttu-id="cd5f2-108">Wert</span><span class="sxs-lookup"><span data-stu-id="cd5f2-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="cd5f2-109">CN</span><span class="sxs-lookup"><span data-stu-id="cd5f2-109">CN</span></span>                | <span data-ttu-id="cd5f2-110">Valid-Accesses</span><span class="sxs-lookup"><span data-stu-id="cd5f2-110">Valid-Accesses</span></span>                       |
| <span data-ttu-id="cd5f2-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cd5f2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cd5f2-112">validzugriffe</span><span class="sxs-lookup"><span data-stu-id="cd5f2-112">validAccesses</span></span>                        |
| <span data-ttu-id="cd5f2-113">Size</span><span class="sxs-lookup"><span data-stu-id="cd5f2-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="cd5f2-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="cd5f2-114">Update Privilege</span></span>  | <span data-ttu-id="cd5f2-115">Objekt Ersteller</span><span class="sxs-lookup"><span data-stu-id="cd5f2-115">Object creator</span></span>                       |
| <span data-ttu-id="cd5f2-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="cd5f2-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="cd5f2-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cd5f2-117">Attribute-Id</span></span>      | <span data-ttu-id="cd5f2-118">1.2.840.113556.1.4.1356</span><span class="sxs-lookup"><span data-stu-id="cd5f2-118">1.2.840.113556.1.4.1356</span></span>              |
| <span data-ttu-id="cd5f2-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cd5f2-119">System-Id-Guid</span></span>    | <span data-ttu-id="cd5f2-120">4d2fa380-7F 54-11d2-992A-0000f 87a57d4</span><span class="sxs-lookup"><span data-stu-id="cd5f2-120">4d2fa380-7f54-11d2-992a-0000f87a57d4</span></span> |
| <span data-ttu-id="cd5f2-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd5f2-121">Syntax</span></span>            | [<span data-ttu-id="cd5f2-122">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="cd5f2-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="cd5f2-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="cd5f2-123">Implementations</span></span>

-   [<span data-ttu-id="cd5f2-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cd5f2-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cd5f2-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cd5f2-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cd5f2-126">**Adam**</span><span class="sxs-lookup"><span data-stu-id="cd5f2-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cd5f2-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cd5f2-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cd5f2-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cd5f2-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cd5f2-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cd5f2-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cd5f2-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cd5f2-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cd5f2-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cd5f2-131">Windows 2000 Server</span></span>



| <span data-ttu-id="cd5f2-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cd5f2-132">Entry</span></span> | <span data-ttu-id="cd5f2-133">Wert</span><span class="sxs-lookup"><span data-stu-id="cd5f2-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="cd5f2-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cd5f2-134">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="cd5f2-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd5f2-135">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="cd5f2-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd5f2-136">System-Only</span></span>            | <span data-ttu-id="cd5f2-137">False</span><span class="sxs-lookup"><span data-stu-id="cd5f2-137">False</span></span>                                                           |
| <span data-ttu-id="cd5f2-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cd5f2-138">Is-Single-Valued</span></span>       | <span data-ttu-id="cd5f2-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="cd5f2-139">True</span></span>                                                            |
| <span data-ttu-id="cd5f2-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cd5f2-140">Is Indexed</span></span>             | <span data-ttu-id="cd5f2-141">False</span><span class="sxs-lookup"><span data-stu-id="cd5f2-141">False</span></span>                                                           |
| <span data-ttu-id="cd5f2-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cd5f2-142">In Global Catalog</span></span>      | <span data-ttu-id="cd5f2-143">False</span><span class="sxs-lookup"><span data-stu-id="cd5f2-143">False</span></span>                                                           |
| <span data-ttu-id="cd5f2-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cd5f2-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd5f2-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cd5f2-145">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="cd5f2-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd5f2-146">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="cd5f2-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd5f2-147">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="cd5f2-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd5f2-148">Search-Flags</span></span>           | <span data-ttu-id="cd5f2-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd5f2-149">0x00000000</span></span>                                                      |
| <span data-ttu-id="cd5f2-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd5f2-150">System-Flags</span></span>           | <span data-ttu-id="cd5f2-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd5f2-151">0x00000010</span></span>                                                      |
| <span data-ttu-id="cd5f2-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cd5f2-152">Classes used in</span></span>        | [<span data-ttu-id="cd5f2-153">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="cd5f2-153">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cd5f2-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cd5f2-154">Windows Server 2003</span></span>



| <span data-ttu-id="cd5f2-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cd5f2-155">Entry</span></span> | <span data-ttu-id="cd5f2-156">Wert</span><span class="sxs-lookup"><span data-stu-id="cd5f2-156">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="cd5f2-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cd5f2-157">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="cd5f2-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd5f2-158">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="cd5f2-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd5f2-159">System-Only</span></span>            | <span data-ttu-id="cd5f2-160">False</span><span class="sxs-lookup"><span data-stu-id="cd5f2-160">False</span></span>                                                           |
| <span data-ttu-id="cd5f2-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cd5f2-161">Is-Single-Valued</span></span>       | <span data-ttu-id="cd5f2-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="cd5f2-162">True</span></span>                                                            |
| <span data-ttu-id="cd5f2-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cd5f2-163">Is Indexed</span></span>             | <span data-ttu-id="cd5f2-164">False</span><span class="sxs-lookup"><span data-stu-id="cd5f2-164">False</span></span>                                                           |
| <span data-ttu-id="cd5f2-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cd5f2-165">In Global Catalog</span></span>      | <span data-ttu-id="cd5f2-166">False</span><span class="sxs-lookup"><span data-stu-id="cd5f2-166">False</span></span>                                                           |
| <span data-ttu-id="cd5f2-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cd5f2-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd5f2-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cd5f2-168">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="cd5f2-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd5f2-169">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="cd5f2-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd5f2-170">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="cd5f2-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd5f2-171">Search-Flags</span></span>           | <span data-ttu-id="cd5f2-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd5f2-172">0x00000000</span></span>                                                      |
| <span data-ttu-id="cd5f2-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd5f2-173">System-Flags</span></span>           | <span data-ttu-id="cd5f2-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd5f2-174">0x00000010</span></span>                                                      |
| <span data-ttu-id="cd5f2-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cd5f2-175">Classes used in</span></span>        | [<span data-ttu-id="cd5f2-176">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="cd5f2-176">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="adam"></a><span data-ttu-id="cd5f2-177">Adam</span><span class="sxs-lookup"><span data-stu-id="cd5f2-177">ADAM</span></span>



| <span data-ttu-id="cd5f2-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cd5f2-178">Entry</span></span> | <span data-ttu-id="cd5f2-179">Wert</span><span class="sxs-lookup"><span data-stu-id="cd5f2-179">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="cd5f2-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cd5f2-180">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="cd5f2-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd5f2-181">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="cd5f2-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd5f2-182">System-Only</span></span>            | <span data-ttu-id="cd5f2-183">False</span><span class="sxs-lookup"><span data-stu-id="cd5f2-183">False</span></span>                                                           |
| <span data-ttu-id="cd5f2-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cd5f2-184">Is-Single-Valued</span></span>       | <span data-ttu-id="cd5f2-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="cd5f2-185">True</span></span>                                                            |
| <span data-ttu-id="cd5f2-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cd5f2-186">Is Indexed</span></span>             | <span data-ttu-id="cd5f2-187">False</span><span class="sxs-lookup"><span data-stu-id="cd5f2-187">False</span></span>                                                           |
| <span data-ttu-id="cd5f2-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cd5f2-188">In Global Catalog</span></span>      | <span data-ttu-id="cd5f2-189">False</span><span class="sxs-lookup"><span data-stu-id="cd5f2-189">False</span></span>                                                           |
| <span data-ttu-id="cd5f2-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cd5f2-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd5f2-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cd5f2-191">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="cd5f2-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd5f2-192">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="cd5f2-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd5f2-193">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="cd5f2-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd5f2-194">Search-Flags</span></span>           | <span data-ttu-id="cd5f2-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd5f2-195">0x00000000</span></span>                                                      |
| <span data-ttu-id="cd5f2-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd5f2-196">System-Flags</span></span>           | <span data-ttu-id="cd5f2-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd5f2-197">0x00000010</span></span>                                                      |
| <span data-ttu-id="cd5f2-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cd5f2-198">Classes used in</span></span>        | [<span data-ttu-id="cd5f2-199">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="cd5f2-199">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cd5f2-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cd5f2-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cd5f2-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cd5f2-201">Entry</span></span> | <span data-ttu-id="cd5f2-202">Wert</span><span class="sxs-lookup"><span data-stu-id="cd5f2-202">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="cd5f2-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cd5f2-203">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="cd5f2-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd5f2-204">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="cd5f2-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd5f2-205">System-Only</span></span>            | <span data-ttu-id="cd5f2-206">False</span><span class="sxs-lookup"><span data-stu-id="cd5f2-206">False</span></span>                                                           |
| <span data-ttu-id="cd5f2-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cd5f2-207">Is-Single-Valued</span></span>       | <span data-ttu-id="cd5f2-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="cd5f2-208">True</span></span>                                                            |
| <span data-ttu-id="cd5f2-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cd5f2-209">Is Indexed</span></span>             | <span data-ttu-id="cd5f2-210">False</span><span class="sxs-lookup"><span data-stu-id="cd5f2-210">False</span></span>                                                           |
| <span data-ttu-id="cd5f2-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cd5f2-211">In Global Catalog</span></span>      | <span data-ttu-id="cd5f2-212">False</span><span class="sxs-lookup"><span data-stu-id="cd5f2-212">False</span></span>                                                           |
| <span data-ttu-id="cd5f2-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cd5f2-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd5f2-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cd5f2-214">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="cd5f2-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd5f2-215">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="cd5f2-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd5f2-216">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="cd5f2-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd5f2-217">Search-Flags</span></span>           | <span data-ttu-id="cd5f2-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd5f2-218">0x00000000</span></span>                                                      |
| <span data-ttu-id="cd5f2-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd5f2-219">System-Flags</span></span>           | <span data-ttu-id="cd5f2-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd5f2-220">0x00000010</span></span>                                                      |
| <span data-ttu-id="cd5f2-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cd5f2-221">Classes used in</span></span>        | [<span data-ttu-id="cd5f2-222">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="cd5f2-222">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cd5f2-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd5f2-223">Windows Server 2008</span></span>



| <span data-ttu-id="cd5f2-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cd5f2-224">Entry</span></span> | <span data-ttu-id="cd5f2-225">Wert</span><span class="sxs-lookup"><span data-stu-id="cd5f2-225">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="cd5f2-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cd5f2-226">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="cd5f2-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd5f2-227">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="cd5f2-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd5f2-228">System-Only</span></span>            | <span data-ttu-id="cd5f2-229">False</span><span class="sxs-lookup"><span data-stu-id="cd5f2-229">False</span></span>                                                           |
| <span data-ttu-id="cd5f2-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cd5f2-230">Is-Single-Valued</span></span>       | <span data-ttu-id="cd5f2-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="cd5f2-231">True</span></span>                                                            |
| <span data-ttu-id="cd5f2-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cd5f2-232">Is Indexed</span></span>             | <span data-ttu-id="cd5f2-233">False</span><span class="sxs-lookup"><span data-stu-id="cd5f2-233">False</span></span>                                                           |
| <span data-ttu-id="cd5f2-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cd5f2-234">In Global Catalog</span></span>      | <span data-ttu-id="cd5f2-235">False</span><span class="sxs-lookup"><span data-stu-id="cd5f2-235">False</span></span>                                                           |
| <span data-ttu-id="cd5f2-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cd5f2-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd5f2-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cd5f2-237">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="cd5f2-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd5f2-238">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="cd5f2-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd5f2-239">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="cd5f2-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd5f2-240">Search-Flags</span></span>           | <span data-ttu-id="cd5f2-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd5f2-241">0x00000000</span></span>                                                      |
| <span data-ttu-id="cd5f2-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd5f2-242">System-Flags</span></span>           | <span data-ttu-id="cd5f2-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd5f2-243">0x00000010</span></span>                                                      |
| <span data-ttu-id="cd5f2-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cd5f2-244">Classes used in</span></span>        | [<span data-ttu-id="cd5f2-245">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="cd5f2-245">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cd5f2-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cd5f2-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cd5f2-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cd5f2-247">Entry</span></span> | <span data-ttu-id="cd5f2-248">Wert</span><span class="sxs-lookup"><span data-stu-id="cd5f2-248">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="cd5f2-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cd5f2-249">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="cd5f2-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd5f2-250">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="cd5f2-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd5f2-251">System-Only</span></span>            | <span data-ttu-id="cd5f2-252">False</span><span class="sxs-lookup"><span data-stu-id="cd5f2-252">False</span></span>                                                           |
| <span data-ttu-id="cd5f2-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cd5f2-253">Is-Single-Valued</span></span>       | <span data-ttu-id="cd5f2-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="cd5f2-254">True</span></span>                                                            |
| <span data-ttu-id="cd5f2-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cd5f2-255">Is Indexed</span></span>             | <span data-ttu-id="cd5f2-256">False</span><span class="sxs-lookup"><span data-stu-id="cd5f2-256">False</span></span>                                                           |
| <span data-ttu-id="cd5f2-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cd5f2-257">In Global Catalog</span></span>      | <span data-ttu-id="cd5f2-258">False</span><span class="sxs-lookup"><span data-stu-id="cd5f2-258">False</span></span>                                                           |
| <span data-ttu-id="cd5f2-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cd5f2-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd5f2-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cd5f2-260">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="cd5f2-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd5f2-261">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="cd5f2-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd5f2-262">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="cd5f2-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd5f2-263">Search-Flags</span></span>           | <span data-ttu-id="cd5f2-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd5f2-264">0x00000000</span></span>                                                      |
| <span data-ttu-id="cd5f2-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd5f2-265">System-Flags</span></span>           | <span data-ttu-id="cd5f2-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd5f2-266">0x00000010</span></span>                                                      |
| <span data-ttu-id="cd5f2-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cd5f2-267">Classes used in</span></span>        | [<span data-ttu-id="cd5f2-268">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="cd5f2-268">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cd5f2-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cd5f2-269">Windows Server 2012</span></span>



| <span data-ttu-id="cd5f2-270">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cd5f2-270">Entry</span></span> | <span data-ttu-id="cd5f2-271">Wert</span><span class="sxs-lookup"><span data-stu-id="cd5f2-271">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="cd5f2-272">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cd5f2-272">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="cd5f2-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd5f2-273">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="cd5f2-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd5f2-274">System-Only</span></span>            | <span data-ttu-id="cd5f2-275">False</span><span class="sxs-lookup"><span data-stu-id="cd5f2-275">False</span></span>                                                           |
| <span data-ttu-id="cd5f2-276">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cd5f2-276">Is-Single-Valued</span></span>       | <span data-ttu-id="cd5f2-277">Richtig</span><span class="sxs-lookup"><span data-stu-id="cd5f2-277">True</span></span>                                                            |
| <span data-ttu-id="cd5f2-278">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cd5f2-278">Is Indexed</span></span>             | <span data-ttu-id="cd5f2-279">False</span><span class="sxs-lookup"><span data-stu-id="cd5f2-279">False</span></span>                                                           |
| <span data-ttu-id="cd5f2-280">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cd5f2-280">In Global Catalog</span></span>      | <span data-ttu-id="cd5f2-281">False</span><span class="sxs-lookup"><span data-stu-id="cd5f2-281">False</span></span>                                                           |
| <span data-ttu-id="cd5f2-282">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cd5f2-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd5f2-283">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cd5f2-283">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="cd5f2-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd5f2-284">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="cd5f2-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd5f2-285">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="cd5f2-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd5f2-286">Search-Flags</span></span>           | <span data-ttu-id="cd5f2-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd5f2-287">0x00000000</span></span>                                                      |
| <span data-ttu-id="cd5f2-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd5f2-288">System-Flags</span></span>           | <span data-ttu-id="cd5f2-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd5f2-289">0x00000010</span></span>                                                      |
| <span data-ttu-id="cd5f2-290">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cd5f2-290">Classes used in</span></span>        | [<span data-ttu-id="cd5f2-291">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="cd5f2-291">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



 

 





