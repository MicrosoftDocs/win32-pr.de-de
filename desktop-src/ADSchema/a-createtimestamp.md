---
title: Create-Time-Stamp-Attribut
description: Das Datum, an dem dieses Objekt erstellt wurde. Dieser Wert wird repliziert.
ms.assetid: 7b957a44-7185-49fa-a219-7c7f4b3e9fce
ms.tgt_platform: multiple
keywords:
- AD-Schema für die Erstellung eines Zeitstempel Attributs
- Schema für das Attribut "kreatetimestamp"
topic_type:
- apiref
api_name:
- Create-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66714aeb035667bc858b7a2e888f6334e7d09c7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103745265"
---
# <a name="create-time-stamp-attribute"></a><span data-ttu-id="043d6-106">Create-Time-Stamp-Attribut</span><span class="sxs-lookup"><span data-stu-id="043d6-106">Create-Time-Stamp attribute</span></span>

<span data-ttu-id="043d6-107">Das Datum, an dem dieses Objekt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="043d6-107">The date when this object was created.</span></span> <span data-ttu-id="043d6-108">Dieser Wert wird repliziert.</span><span class="sxs-lookup"><span data-stu-id="043d6-108">This value is replicated.</span></span>



| <span data-ttu-id="043d6-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="043d6-109">Entry</span></span> | <span data-ttu-id="043d6-110">Wert</span><span class="sxs-lookup"><span data-stu-id="043d6-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="043d6-111">CN</span><span class="sxs-lookup"><span data-stu-id="043d6-111">CN</span></span>                | <span data-ttu-id="043d6-112">Create-Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="043d6-112">Create-Time-Stamp</span></span>                                             |
| <span data-ttu-id="043d6-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="043d6-113">Ldap-Display-Name</span></span> | <span data-ttu-id="043d6-114">"kreatetimestamp"</span><span class="sxs-lookup"><span data-stu-id="043d6-114">createTimeStamp</span></span>                                               |
| <span data-ttu-id="043d6-115">Size</span><span class="sxs-lookup"><span data-stu-id="043d6-115">Size</span></span>              | <span data-ttu-id="043d6-116">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="043d6-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="043d6-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="043d6-117">Update Privilege</span></span>  | <span data-ttu-id="043d6-118">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="043d6-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="043d6-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="043d6-119">Update Frequency</span></span>  | <span data-ttu-id="043d6-120">Wenn das Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="043d6-120">When the object is created.</span></span>                                   |
| <span data-ttu-id="043d6-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="043d6-121">Attribute-Id</span></span>      | <span data-ttu-id="043d6-122">2.5.18.1</span><span class="sxs-lookup"><span data-stu-id="043d6-122">2.5.18.1</span></span>                                                      |
| <span data-ttu-id="043d6-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="043d6-123">System-Id-Guid</span></span>    | <span data-ttu-id="043d6-124">2df90d73-009F -11d2-aa4c-00c04f d83a</span><span class="sxs-lookup"><span data-stu-id="043d6-124">2df90d73-009f-11d2-aa4c-00c04fd7d83a</span></span>                          |
| <span data-ttu-id="043d6-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="043d6-125">Syntax</span></span>            | [<span data-ttu-id="043d6-126">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="043d6-126">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="043d6-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="043d6-127">Implementations</span></span>

-   [<span data-ttu-id="043d6-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="043d6-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="043d6-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="043d6-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="043d6-130">**Adam**</span><span class="sxs-lookup"><span data-stu-id="043d6-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="043d6-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="043d6-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="043d6-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="043d6-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="043d6-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="043d6-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="043d6-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="043d6-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="043d6-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="043d6-135">Windows 2000 Server</span></span>



| <span data-ttu-id="043d6-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="043d6-136">Entry</span></span> | <span data-ttu-id="043d6-137">Wert</span><span class="sxs-lookup"><span data-stu-id="043d6-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="043d6-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="043d6-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="043d6-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="043d6-139">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="043d6-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="043d6-140">System-Only</span></span>            | <span data-ttu-id="043d6-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="043d6-141">True</span></span>                            |
| <span data-ttu-id="043d6-142">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="043d6-142">Is-Single-Valued</span></span>       | <span data-ttu-id="043d6-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="043d6-143">True</span></span>                            |
| <span data-ttu-id="043d6-144">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="043d6-144">Is Indexed</span></span>             | <span data-ttu-id="043d6-145">False</span><span class="sxs-lookup"><span data-stu-id="043d6-145">False</span></span>                           |
| <span data-ttu-id="043d6-146">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="043d6-146">In Global Catalog</span></span>      | <span data-ttu-id="043d6-147">False</span><span class="sxs-lookup"><span data-stu-id="043d6-147">False</span></span>                           |
| <span data-ttu-id="043d6-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="043d6-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="043d6-149">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="043d6-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="043d6-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="043d6-150">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="043d6-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="043d6-151">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="043d6-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="043d6-152">Search-Flags</span></span>           | <span data-ttu-id="043d6-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="043d6-153">0x00000000</span></span>                      |
| <span data-ttu-id="043d6-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="043d6-154">System-Flags</span></span>           | <span data-ttu-id="043d6-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="043d6-155">0x08000014</span></span>                      |
| <span data-ttu-id="043d6-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="043d6-156">Classes used in</span></span>        | [<span data-ttu-id="043d6-157">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="043d6-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="043d6-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="043d6-158">Windows Server 2003</span></span>



| <span data-ttu-id="043d6-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="043d6-159">Entry</span></span> | <span data-ttu-id="043d6-160">Wert</span><span class="sxs-lookup"><span data-stu-id="043d6-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="043d6-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="043d6-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="043d6-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="043d6-162">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="043d6-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="043d6-163">System-Only</span></span>            | <span data-ttu-id="043d6-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="043d6-164">True</span></span>                            |
| <span data-ttu-id="043d6-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="043d6-165">Is-Single-Valued</span></span>       | <span data-ttu-id="043d6-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="043d6-166">True</span></span>                            |
| <span data-ttu-id="043d6-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="043d6-167">Is Indexed</span></span>             | <span data-ttu-id="043d6-168">False</span><span class="sxs-lookup"><span data-stu-id="043d6-168">False</span></span>                           |
| <span data-ttu-id="043d6-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="043d6-169">In Global Catalog</span></span>      | <span data-ttu-id="043d6-170">False</span><span class="sxs-lookup"><span data-stu-id="043d6-170">False</span></span>                           |
| <span data-ttu-id="043d6-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="043d6-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="043d6-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="043d6-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="043d6-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="043d6-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="043d6-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="043d6-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="043d6-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="043d6-175">Search-Flags</span></span>           | <span data-ttu-id="043d6-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="043d6-176">0x00000000</span></span>                      |
| <span data-ttu-id="043d6-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="043d6-177">System-Flags</span></span>           | <span data-ttu-id="043d6-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="043d6-178">0x08000014</span></span>                      |
| <span data-ttu-id="043d6-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="043d6-179">Classes used in</span></span>        | [<span data-ttu-id="043d6-180">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="043d6-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="043d6-181">Adam</span><span class="sxs-lookup"><span data-stu-id="043d6-181">ADAM</span></span>



| <span data-ttu-id="043d6-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="043d6-182">Entry</span></span> | <span data-ttu-id="043d6-183">Wert</span><span class="sxs-lookup"><span data-stu-id="043d6-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="043d6-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="043d6-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="043d6-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="043d6-185">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="043d6-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="043d6-186">System-Only</span></span>            | <span data-ttu-id="043d6-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="043d6-187">True</span></span>                            |
| <span data-ttu-id="043d6-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="043d6-188">Is-Single-Valued</span></span>       | <span data-ttu-id="043d6-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="043d6-189">True</span></span>                            |
| <span data-ttu-id="043d6-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="043d6-190">Is Indexed</span></span>             | <span data-ttu-id="043d6-191">False</span><span class="sxs-lookup"><span data-stu-id="043d6-191">False</span></span>                           |
| <span data-ttu-id="043d6-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="043d6-192">In Global Catalog</span></span>      | <span data-ttu-id="043d6-193">False</span><span class="sxs-lookup"><span data-stu-id="043d6-193">False</span></span>                           |
| <span data-ttu-id="043d6-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="043d6-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="043d6-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="043d6-195">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="043d6-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="043d6-196">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="043d6-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="043d6-197">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="043d6-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="043d6-198">Search-Flags</span></span>           | <span data-ttu-id="043d6-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="043d6-199">0x00000000</span></span>                      |
| <span data-ttu-id="043d6-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="043d6-200">System-Flags</span></span>           | <span data-ttu-id="043d6-201">0x08000014</span><span class="sxs-lookup"><span data-stu-id="043d6-201">0x08000014</span></span>                      |
| <span data-ttu-id="043d6-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="043d6-202">Classes used in</span></span>        | [<span data-ttu-id="043d6-203">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="043d6-203">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="043d6-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="043d6-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="043d6-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="043d6-205">Entry</span></span> | <span data-ttu-id="043d6-206">Wert</span><span class="sxs-lookup"><span data-stu-id="043d6-206">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="043d6-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="043d6-207">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="043d6-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="043d6-208">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="043d6-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="043d6-209">System-Only</span></span>            | <span data-ttu-id="043d6-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="043d6-210">True</span></span>                            |
| <span data-ttu-id="043d6-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="043d6-211">Is-Single-Valued</span></span>       | <span data-ttu-id="043d6-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="043d6-212">True</span></span>                            |
| <span data-ttu-id="043d6-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="043d6-213">Is Indexed</span></span>             | <span data-ttu-id="043d6-214">False</span><span class="sxs-lookup"><span data-stu-id="043d6-214">False</span></span>                           |
| <span data-ttu-id="043d6-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="043d6-215">In Global Catalog</span></span>      | <span data-ttu-id="043d6-216">False</span><span class="sxs-lookup"><span data-stu-id="043d6-216">False</span></span>                           |
| <span data-ttu-id="043d6-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="043d6-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="043d6-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="043d6-218">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="043d6-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="043d6-219">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="043d6-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="043d6-220">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="043d6-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="043d6-221">Search-Flags</span></span>           | <span data-ttu-id="043d6-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="043d6-222">0x00000000</span></span>                      |
| <span data-ttu-id="043d6-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="043d6-223">System-Flags</span></span>           | <span data-ttu-id="043d6-224">0x08000014</span><span class="sxs-lookup"><span data-stu-id="043d6-224">0x08000014</span></span>                      |
| <span data-ttu-id="043d6-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="043d6-225">Classes used in</span></span>        | [<span data-ttu-id="043d6-226">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="043d6-226">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="043d6-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="043d6-227">Windows Server 2008</span></span>



| <span data-ttu-id="043d6-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="043d6-228">Entry</span></span> | <span data-ttu-id="043d6-229">Wert</span><span class="sxs-lookup"><span data-stu-id="043d6-229">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="043d6-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="043d6-230">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="043d6-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="043d6-231">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="043d6-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="043d6-232">System-Only</span></span>            | <span data-ttu-id="043d6-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="043d6-233">True</span></span>                            |
| <span data-ttu-id="043d6-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="043d6-234">Is-Single-Valued</span></span>       | <span data-ttu-id="043d6-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="043d6-235">True</span></span>                            |
| <span data-ttu-id="043d6-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="043d6-236">Is Indexed</span></span>             | <span data-ttu-id="043d6-237">False</span><span class="sxs-lookup"><span data-stu-id="043d6-237">False</span></span>                           |
| <span data-ttu-id="043d6-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="043d6-238">In Global Catalog</span></span>      | <span data-ttu-id="043d6-239">False</span><span class="sxs-lookup"><span data-stu-id="043d6-239">False</span></span>                           |
| <span data-ttu-id="043d6-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="043d6-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="043d6-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="043d6-241">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="043d6-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="043d6-242">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="043d6-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="043d6-243">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="043d6-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="043d6-244">Search-Flags</span></span>           | <span data-ttu-id="043d6-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="043d6-245">0x00000000</span></span>                      |
| <span data-ttu-id="043d6-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="043d6-246">System-Flags</span></span>           | <span data-ttu-id="043d6-247">0x08000014</span><span class="sxs-lookup"><span data-stu-id="043d6-247">0x08000014</span></span>                      |
| <span data-ttu-id="043d6-248">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="043d6-248">Classes used in</span></span>        | [<span data-ttu-id="043d6-249">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="043d6-249">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="043d6-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="043d6-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="043d6-251">Eingabe</span><span class="sxs-lookup"><span data-stu-id="043d6-251">Entry</span></span> | <span data-ttu-id="043d6-252">Wert</span><span class="sxs-lookup"><span data-stu-id="043d6-252">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="043d6-253">Link-ID</span><span class="sxs-lookup"><span data-stu-id="043d6-253">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="043d6-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="043d6-254">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="043d6-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="043d6-255">System-Only</span></span>            | <span data-ttu-id="043d6-256">Richtig</span><span class="sxs-lookup"><span data-stu-id="043d6-256">True</span></span>                            |
| <span data-ttu-id="043d6-257">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="043d6-257">Is-Single-Valued</span></span>       | <span data-ttu-id="043d6-258">Richtig</span><span class="sxs-lookup"><span data-stu-id="043d6-258">True</span></span>                            |
| <span data-ttu-id="043d6-259">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="043d6-259">Is Indexed</span></span>             | <span data-ttu-id="043d6-260">False</span><span class="sxs-lookup"><span data-stu-id="043d6-260">False</span></span>                           |
| <span data-ttu-id="043d6-261">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="043d6-261">In Global Catalog</span></span>      | <span data-ttu-id="043d6-262">False</span><span class="sxs-lookup"><span data-stu-id="043d6-262">False</span></span>                           |
| <span data-ttu-id="043d6-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="043d6-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="043d6-264">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="043d6-264">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="043d6-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="043d6-265">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="043d6-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="043d6-266">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="043d6-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="043d6-267">Search-Flags</span></span>           | <span data-ttu-id="043d6-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="043d6-268">0x00000000</span></span>                      |
| <span data-ttu-id="043d6-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="043d6-269">System-Flags</span></span>           | <span data-ttu-id="043d6-270">0x08000014</span><span class="sxs-lookup"><span data-stu-id="043d6-270">0x08000014</span></span>                      |
| <span data-ttu-id="043d6-271">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="043d6-271">Classes used in</span></span>        | [<span data-ttu-id="043d6-272">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="043d6-272">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="043d6-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="043d6-273">Windows Server 2012</span></span>



| <span data-ttu-id="043d6-274">Eingabe</span><span class="sxs-lookup"><span data-stu-id="043d6-274">Entry</span></span> | <span data-ttu-id="043d6-275">Wert</span><span class="sxs-lookup"><span data-stu-id="043d6-275">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="043d6-276">Link-ID</span><span class="sxs-lookup"><span data-stu-id="043d6-276">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="043d6-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="043d6-277">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="043d6-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="043d6-278">System-Only</span></span>            | <span data-ttu-id="043d6-279">Richtig</span><span class="sxs-lookup"><span data-stu-id="043d6-279">True</span></span>                            |
| <span data-ttu-id="043d6-280">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="043d6-280">Is-Single-Valued</span></span>       | <span data-ttu-id="043d6-281">Richtig</span><span class="sxs-lookup"><span data-stu-id="043d6-281">True</span></span>                            |
| <span data-ttu-id="043d6-282">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="043d6-282">Is Indexed</span></span>             | <span data-ttu-id="043d6-283">False</span><span class="sxs-lookup"><span data-stu-id="043d6-283">False</span></span>                           |
| <span data-ttu-id="043d6-284">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="043d6-284">In Global Catalog</span></span>      | <span data-ttu-id="043d6-285">False</span><span class="sxs-lookup"><span data-stu-id="043d6-285">False</span></span>                           |
| <span data-ttu-id="043d6-286">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="043d6-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="043d6-287">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="043d6-287">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="043d6-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="043d6-288">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="043d6-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="043d6-289">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="043d6-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="043d6-290">Search-Flags</span></span>           | <span data-ttu-id="043d6-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="043d6-291">0x00000000</span></span>                      |
| <span data-ttu-id="043d6-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="043d6-292">System-Flags</span></span>           | <span data-ttu-id="043d6-293">0x08000014</span><span class="sxs-lookup"><span data-stu-id="043d6-293">0x08000014</span></span>                      |
| <span data-ttu-id="043d6-294">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="043d6-294">Classes used in</span></span>        | [<span data-ttu-id="043d6-295">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="043d6-295">**Top**</span></span>](c-top.md)<br/> |



 

 





