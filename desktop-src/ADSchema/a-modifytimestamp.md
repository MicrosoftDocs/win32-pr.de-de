---
title: Modify-Zeitstempel Attribut
description: Ein berechnetes Attribut, das das Datum darstellt, an dem das Objekt zuletzt geändert wurde. Dieser Wert wird nicht repliziert.
ms.assetid: ad8fea90-9a78-484d-9549-26d78e87ec44
ms.tgt_platform: multiple
keywords:
- AD-Schema für das Modify-Zeitstempel Attribut
- Schema des modifytimestamp-Attributs
topic_type:
- apiref
api_name:
- Modify-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c032d19c3bd2bf5a6ee0cfe038e9fa9b184d36
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744337"
---
# <a name="modify-time-stamp-attribute"></a><span data-ttu-id="8161d-106">Modify-Zeitstempel Attribut</span><span class="sxs-lookup"><span data-stu-id="8161d-106">Modify-Time-Stamp attribute</span></span>

<span data-ttu-id="8161d-107">Ein berechnetes Attribut, das das Datum darstellt, an dem das Objekt zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="8161d-107">A computed attribute that represents the date when this object was last changed.</span></span> <span data-ttu-id="8161d-108">Dieser Wert wird nicht repliziert.</span><span class="sxs-lookup"><span data-stu-id="8161d-108">This value is not replicated.</span></span>



| <span data-ttu-id="8161d-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8161d-109">Entry</span></span> | <span data-ttu-id="8161d-110">Wert</span><span class="sxs-lookup"><span data-stu-id="8161d-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="8161d-111">CN</span><span class="sxs-lookup"><span data-stu-id="8161d-111">CN</span></span>                | <span data-ttu-id="8161d-112">Modify-Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="8161d-112">Modify-Time-Stamp</span></span>                                             |
| <span data-ttu-id="8161d-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8161d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8161d-114">modifyTimeStamp</span><span class="sxs-lookup"><span data-stu-id="8161d-114">modifyTimeStamp</span></span>                                               |
| <span data-ttu-id="8161d-115">Size</span><span class="sxs-lookup"><span data-stu-id="8161d-115">Size</span></span>              | <span data-ttu-id="8161d-116">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="8161d-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="8161d-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="8161d-117">Update Privilege</span></span>  | <span data-ttu-id="8161d-118">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8161d-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="8161d-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="8161d-119">Update Frequency</span></span>  | \-                                                            |
| <span data-ttu-id="8161d-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8161d-120">Attribute-Id</span></span>      | <span data-ttu-id="8161d-121">2.5.18.2</span><span class="sxs-lookup"><span data-stu-id="8161d-121">2.5.18.2</span></span>                                                      |
| <span data-ttu-id="8161d-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8161d-122">System-Id-Guid</span></span>    | <span data-ttu-id="8161d-123">9a7ad94a-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="8161d-123">9a7ad94a-ca53-11d1-bbd0-0080c76670c0</span></span>                          |
| <span data-ttu-id="8161d-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="8161d-124">Syntax</span></span>            | [<span data-ttu-id="8161d-125">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="8161d-125">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="8161d-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="8161d-126">Implementations</span></span>

-   [<span data-ttu-id="8161d-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8161d-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8161d-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8161d-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8161d-129">**Adam**</span><span class="sxs-lookup"><span data-stu-id="8161d-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8161d-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8161d-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8161d-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8161d-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8161d-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8161d-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8161d-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8161d-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8161d-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8161d-134">Windows 2000 Server</span></span>



| <span data-ttu-id="8161d-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8161d-135">Entry</span></span> | <span data-ttu-id="8161d-136">Wert</span><span class="sxs-lookup"><span data-stu-id="8161d-136">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="8161d-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8161d-137">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8161d-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8161d-138">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8161d-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="8161d-139">System-Only</span></span>            | <span data-ttu-id="8161d-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="8161d-140">True</span></span>                                                                        |
| <span data-ttu-id="8161d-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8161d-141">Is-Single-Valued</span></span>       | <span data-ttu-id="8161d-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="8161d-142">True</span></span>                                                                        |
| <span data-ttu-id="8161d-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8161d-143">Is Indexed</span></span>             | <span data-ttu-id="8161d-144">False</span><span class="sxs-lookup"><span data-stu-id="8161d-144">False</span></span>                                                                       |
| <span data-ttu-id="8161d-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8161d-145">In Global Catalog</span></span>      | <span data-ttu-id="8161d-146">False</span><span class="sxs-lookup"><span data-stu-id="8161d-146">False</span></span>                                                                       |
| <span data-ttu-id="8161d-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8161d-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="8161d-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8161d-148">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="8161d-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8161d-149">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="8161d-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8161d-150">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="8161d-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8161d-151">Search-Flags</span></span>           | <span data-ttu-id="8161d-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8161d-152">0x00000000</span></span>                                                                  |
| <span data-ttu-id="8161d-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8161d-153">System-Flags</span></span>           | <span data-ttu-id="8161d-154">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8161d-154">0x08000014</span></span>                                                                  |
| <span data-ttu-id="8161d-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8161d-155">Classes used in</span></span>        | [<span data-ttu-id="8161d-156">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="8161d-156">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="8161d-157">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="8161d-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8161d-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8161d-158">Windows Server 2003</span></span>



| <span data-ttu-id="8161d-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8161d-159">Entry</span></span> | <span data-ttu-id="8161d-160">Wert</span><span class="sxs-lookup"><span data-stu-id="8161d-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="8161d-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8161d-161">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8161d-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8161d-162">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8161d-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="8161d-163">System-Only</span></span>            | <span data-ttu-id="8161d-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="8161d-164">True</span></span>                                                                        |
| <span data-ttu-id="8161d-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8161d-165">Is-Single-Valued</span></span>       | <span data-ttu-id="8161d-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="8161d-166">True</span></span>                                                                        |
| <span data-ttu-id="8161d-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8161d-167">Is Indexed</span></span>             | <span data-ttu-id="8161d-168">False</span><span class="sxs-lookup"><span data-stu-id="8161d-168">False</span></span>                                                                       |
| <span data-ttu-id="8161d-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8161d-169">In Global Catalog</span></span>      | <span data-ttu-id="8161d-170">False</span><span class="sxs-lookup"><span data-stu-id="8161d-170">False</span></span>                                                                       |
| <span data-ttu-id="8161d-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8161d-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="8161d-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8161d-172">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="8161d-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8161d-173">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="8161d-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8161d-174">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="8161d-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8161d-175">Search-Flags</span></span>           | <span data-ttu-id="8161d-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8161d-176">0x00000000</span></span>                                                                  |
| <span data-ttu-id="8161d-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8161d-177">System-Flags</span></span>           | <span data-ttu-id="8161d-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8161d-178">0x08000014</span></span>                                                                  |
| <span data-ttu-id="8161d-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8161d-179">Classes used in</span></span>        | [<span data-ttu-id="8161d-180">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="8161d-180">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="8161d-181">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="8161d-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8161d-182">Adam</span><span class="sxs-lookup"><span data-stu-id="8161d-182">ADAM</span></span>



| <span data-ttu-id="8161d-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8161d-183">Entry</span></span> | <span data-ttu-id="8161d-184">Wert</span><span class="sxs-lookup"><span data-stu-id="8161d-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="8161d-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8161d-185">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8161d-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8161d-186">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8161d-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="8161d-187">System-Only</span></span>            | <span data-ttu-id="8161d-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="8161d-188">True</span></span>                                                                        |
| <span data-ttu-id="8161d-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8161d-189">Is-Single-Valued</span></span>       | <span data-ttu-id="8161d-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="8161d-190">True</span></span>                                                                        |
| <span data-ttu-id="8161d-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8161d-191">Is Indexed</span></span>             | <span data-ttu-id="8161d-192">False</span><span class="sxs-lookup"><span data-stu-id="8161d-192">False</span></span>                                                                       |
| <span data-ttu-id="8161d-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8161d-193">In Global Catalog</span></span>      | <span data-ttu-id="8161d-194">False</span><span class="sxs-lookup"><span data-stu-id="8161d-194">False</span></span>                                                                       |
| <span data-ttu-id="8161d-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8161d-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="8161d-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8161d-196">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="8161d-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8161d-197">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="8161d-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8161d-198">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="8161d-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8161d-199">Search-Flags</span></span>           | <span data-ttu-id="8161d-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8161d-200">0x00000000</span></span>                                                                  |
| <span data-ttu-id="8161d-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8161d-201">System-Flags</span></span>           | <span data-ttu-id="8161d-202">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8161d-202">0x08000014</span></span>                                                                  |
| <span data-ttu-id="8161d-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8161d-203">Classes used in</span></span>        | [<span data-ttu-id="8161d-204">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="8161d-204">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="8161d-205">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="8161d-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8161d-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8161d-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8161d-207">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8161d-207">Entry</span></span> | <span data-ttu-id="8161d-208">Wert</span><span class="sxs-lookup"><span data-stu-id="8161d-208">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="8161d-209">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8161d-209">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8161d-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8161d-210">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8161d-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="8161d-211">System-Only</span></span>            | <span data-ttu-id="8161d-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="8161d-212">True</span></span>                                                                        |
| <span data-ttu-id="8161d-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8161d-213">Is-Single-Valued</span></span>       | <span data-ttu-id="8161d-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="8161d-214">True</span></span>                                                                        |
| <span data-ttu-id="8161d-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8161d-215">Is Indexed</span></span>             | <span data-ttu-id="8161d-216">False</span><span class="sxs-lookup"><span data-stu-id="8161d-216">False</span></span>                                                                       |
| <span data-ttu-id="8161d-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8161d-217">In Global Catalog</span></span>      | <span data-ttu-id="8161d-218">False</span><span class="sxs-lookup"><span data-stu-id="8161d-218">False</span></span>                                                                       |
| <span data-ttu-id="8161d-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8161d-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="8161d-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8161d-220">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="8161d-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8161d-221">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="8161d-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8161d-222">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="8161d-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8161d-223">Search-Flags</span></span>           | <span data-ttu-id="8161d-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8161d-224">0x00000000</span></span>                                                                  |
| <span data-ttu-id="8161d-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8161d-225">System-Flags</span></span>           | <span data-ttu-id="8161d-226">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8161d-226">0x08000014</span></span>                                                                  |
| <span data-ttu-id="8161d-227">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8161d-227">Classes used in</span></span>        | [<span data-ttu-id="8161d-228">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="8161d-228">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="8161d-229">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="8161d-229">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8161d-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8161d-230">Windows Server 2008</span></span>



| <span data-ttu-id="8161d-231">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8161d-231">Entry</span></span> | <span data-ttu-id="8161d-232">Wert</span><span class="sxs-lookup"><span data-stu-id="8161d-232">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="8161d-233">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8161d-233">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8161d-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8161d-234">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8161d-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="8161d-235">System-Only</span></span>            | <span data-ttu-id="8161d-236">Richtig</span><span class="sxs-lookup"><span data-stu-id="8161d-236">True</span></span>                                                                        |
| <span data-ttu-id="8161d-237">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8161d-237">Is-Single-Valued</span></span>       | <span data-ttu-id="8161d-238">Richtig</span><span class="sxs-lookup"><span data-stu-id="8161d-238">True</span></span>                                                                        |
| <span data-ttu-id="8161d-239">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8161d-239">Is Indexed</span></span>             | <span data-ttu-id="8161d-240">False</span><span class="sxs-lookup"><span data-stu-id="8161d-240">False</span></span>                                                                       |
| <span data-ttu-id="8161d-241">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8161d-241">In Global Catalog</span></span>      | <span data-ttu-id="8161d-242">False</span><span class="sxs-lookup"><span data-stu-id="8161d-242">False</span></span>                                                                       |
| <span data-ttu-id="8161d-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8161d-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="8161d-244">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8161d-244">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="8161d-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8161d-245">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="8161d-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8161d-246">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="8161d-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8161d-247">Search-Flags</span></span>           | <span data-ttu-id="8161d-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8161d-248">0x00000000</span></span>                                                                  |
| <span data-ttu-id="8161d-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8161d-249">System-Flags</span></span>           | <span data-ttu-id="8161d-250">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8161d-250">0x08000014</span></span>                                                                  |
| <span data-ttu-id="8161d-251">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8161d-251">Classes used in</span></span>        | [<span data-ttu-id="8161d-252">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="8161d-252">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="8161d-253">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="8161d-253">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8161d-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8161d-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8161d-255">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8161d-255">Entry</span></span> | <span data-ttu-id="8161d-256">Wert</span><span class="sxs-lookup"><span data-stu-id="8161d-256">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="8161d-257">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8161d-257">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8161d-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8161d-258">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8161d-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="8161d-259">System-Only</span></span>            | <span data-ttu-id="8161d-260">Richtig</span><span class="sxs-lookup"><span data-stu-id="8161d-260">True</span></span>                                                                        |
| <span data-ttu-id="8161d-261">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8161d-261">Is-Single-Valued</span></span>       | <span data-ttu-id="8161d-262">Richtig</span><span class="sxs-lookup"><span data-stu-id="8161d-262">True</span></span>                                                                        |
| <span data-ttu-id="8161d-263">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8161d-263">Is Indexed</span></span>             | <span data-ttu-id="8161d-264">False</span><span class="sxs-lookup"><span data-stu-id="8161d-264">False</span></span>                                                                       |
| <span data-ttu-id="8161d-265">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8161d-265">In Global Catalog</span></span>      | <span data-ttu-id="8161d-266">False</span><span class="sxs-lookup"><span data-stu-id="8161d-266">False</span></span>                                                                       |
| <span data-ttu-id="8161d-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8161d-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="8161d-268">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8161d-268">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="8161d-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8161d-269">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="8161d-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8161d-270">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="8161d-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8161d-271">Search-Flags</span></span>           | <span data-ttu-id="8161d-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8161d-272">0x00000000</span></span>                                                                  |
| <span data-ttu-id="8161d-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8161d-273">System-Flags</span></span>           | <span data-ttu-id="8161d-274">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8161d-274">0x08000014</span></span>                                                                  |
| <span data-ttu-id="8161d-275">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8161d-275">Classes used in</span></span>        | [<span data-ttu-id="8161d-276">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="8161d-276">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="8161d-277">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="8161d-277">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8161d-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8161d-278">Windows Server 2012</span></span>



| <span data-ttu-id="8161d-279">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8161d-279">Entry</span></span> | <span data-ttu-id="8161d-280">Wert</span><span class="sxs-lookup"><span data-stu-id="8161d-280">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="8161d-281">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8161d-281">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8161d-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8161d-282">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8161d-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="8161d-283">System-Only</span></span>            | <span data-ttu-id="8161d-284">Richtig</span><span class="sxs-lookup"><span data-stu-id="8161d-284">True</span></span>                                                                        |
| <span data-ttu-id="8161d-285">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8161d-285">Is-Single-Valued</span></span>       | <span data-ttu-id="8161d-286">Richtig</span><span class="sxs-lookup"><span data-stu-id="8161d-286">True</span></span>                                                                        |
| <span data-ttu-id="8161d-287">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8161d-287">Is Indexed</span></span>             | <span data-ttu-id="8161d-288">False</span><span class="sxs-lookup"><span data-stu-id="8161d-288">False</span></span>                                                                       |
| <span data-ttu-id="8161d-289">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8161d-289">In Global Catalog</span></span>      | <span data-ttu-id="8161d-290">False</span><span class="sxs-lookup"><span data-stu-id="8161d-290">False</span></span>                                                                       |
| <span data-ttu-id="8161d-291">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8161d-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="8161d-292">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8161d-292">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="8161d-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8161d-293">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="8161d-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8161d-294">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="8161d-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8161d-295">Search-Flags</span></span>           | <span data-ttu-id="8161d-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8161d-296">0x00000000</span></span>                                                                  |
| <span data-ttu-id="8161d-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8161d-297">System-Flags</span></span>           | <span data-ttu-id="8161d-298">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8161d-298">0x08000014</span></span>                                                                  |
| <span data-ttu-id="8161d-299">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8161d-299">Classes used in</span></span>        | [<span data-ttu-id="8161d-300">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="8161d-300">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="8161d-301">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="8161d-301">**Top**</span></span>](c-top.md)<br/> |



 

 





