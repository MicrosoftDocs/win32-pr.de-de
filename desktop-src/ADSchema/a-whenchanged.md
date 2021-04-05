---
title: When-Changed-Attribut
description: Das Datum, an dem das Objekt zuletzt geändert wurde. Dieser Wert wird nicht repliziert und ist im globalen Katalog vorhanden.
ms.assetid: 32dc9458-5692-4bce-abc1-7bea3ea680a9
ms.tgt_platform: multiple
keywords:
- AD-Schema für When-Changed-Attribut
- AD-Schema für das-Attribut
topic_type:
- apiref
api_name:
- When-Changed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7c3608a33aa5d5ac52b226cd7a3d94ff0b95520
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859377"
---
# <a name="when-changed-attribute"></a><span data-ttu-id="a47d0-106">When-Changed-Attribut</span><span class="sxs-lookup"><span data-stu-id="a47d0-106">When-Changed attribute</span></span>

<span data-ttu-id="a47d0-107">Das Datum, an dem das Objekt zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="a47d0-107">The date when this object was last changed.</span></span> <span data-ttu-id="a47d0-108">Dieser Wert wird nicht repliziert und ist im globalen Katalog vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a47d0-108">This value is not replicated and exists in the global catalog.</span></span>



| <span data-ttu-id="a47d0-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a47d0-109">Entry</span></span> | <span data-ttu-id="a47d0-110">Wert</span><span class="sxs-lookup"><span data-stu-id="a47d0-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="a47d0-111">CN</span><span class="sxs-lookup"><span data-stu-id="a47d0-111">CN</span></span>                | <span data-ttu-id="a47d0-112">When-Changed</span><span class="sxs-lookup"><span data-stu-id="a47d0-112">When-Changed</span></span>                                                  |
| <span data-ttu-id="a47d0-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a47d0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a47d0-114">whenChanged</span><span class="sxs-lookup"><span data-stu-id="a47d0-114">whenChanged</span></span>                                                   |
| <span data-ttu-id="a47d0-115">Size</span><span class="sxs-lookup"><span data-stu-id="a47d0-115">Size</span></span>              | <span data-ttu-id="a47d0-116">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="a47d0-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="a47d0-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="a47d0-117">Update Privilege</span></span>  | <span data-ttu-id="a47d0-118">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a47d0-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="a47d0-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="a47d0-119">Update Frequency</span></span>  | <span data-ttu-id="a47d0-120">Jedes Mal, wenn das Objekt geändert wird.</span><span class="sxs-lookup"><span data-stu-id="a47d0-120">Each time the object is changed.</span></span>                              |
| <span data-ttu-id="a47d0-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a47d0-121">Attribute-Id</span></span>      | <span data-ttu-id="a47d0-122">1.2.840.113556.1.2.3</span><span class="sxs-lookup"><span data-stu-id="a47d0-122">1.2.840.113556.1.2.3</span></span>                                          |
| <span data-ttu-id="a47d0-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a47d0-123">System-Id-Guid</span></span>    | <span data-ttu-id="a47d0-124">bf967a77-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a47d0-124">bf967a77-0de6-11d0-a285-00aa003049e2</span></span>                          |
| <span data-ttu-id="a47d0-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="a47d0-125">Syntax</span></span>            | [<span data-ttu-id="a47d0-126">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="a47d0-126">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="a47d0-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="a47d0-127">Implementations</span></span>

-   [<span data-ttu-id="a47d0-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a47d0-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a47d0-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a47d0-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a47d0-130">**Adam**</span><span class="sxs-lookup"><span data-stu-id="a47d0-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a47d0-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a47d0-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a47d0-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a47d0-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a47d0-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a47d0-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a47d0-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a47d0-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a47d0-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a47d0-135">Windows 2000 Server</span></span>



| <span data-ttu-id="a47d0-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a47d0-136">Entry</span></span> | <span data-ttu-id="a47d0-137">Wert</span><span class="sxs-lookup"><span data-stu-id="a47d0-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a47d0-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a47d0-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a47d0-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a47d0-139">MAPI-Id</span></span>                | <span data-ttu-id="a47d0-140">0x3008</span><span class="sxs-lookup"><span data-stu-id="a47d0-140">0x3008</span></span>                          |
| <span data-ttu-id="a47d0-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="a47d0-141">System-Only</span></span>            | <span data-ttu-id="a47d0-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="a47d0-142">True</span></span>                            |
| <span data-ttu-id="a47d0-143">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a47d0-143">Is-Single-Valued</span></span>       | <span data-ttu-id="a47d0-144">Richtig</span><span class="sxs-lookup"><span data-stu-id="a47d0-144">True</span></span>                            |
| <span data-ttu-id="a47d0-145">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a47d0-145">Is Indexed</span></span>             | <span data-ttu-id="a47d0-146">False</span><span class="sxs-lookup"><span data-stu-id="a47d0-146">False</span></span>                           |
| <span data-ttu-id="a47d0-147">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a47d0-147">In Global Catalog</span></span>      | <span data-ttu-id="a47d0-148">Richtig</span><span class="sxs-lookup"><span data-stu-id="a47d0-148">True</span></span>                            |
| <span data-ttu-id="a47d0-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a47d0-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="a47d0-150">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a47d0-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a47d0-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a47d0-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a47d0-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a47d0-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a47d0-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a47d0-153">Search-Flags</span></span>           | <span data-ttu-id="a47d0-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a47d0-154">0x00000000</span></span>                      |
| <span data-ttu-id="a47d0-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a47d0-155">System-Flags</span></span>           | <span data-ttu-id="a47d0-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a47d0-156">0x00000013</span></span>                      |
| <span data-ttu-id="a47d0-157">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a47d0-157">Classes used in</span></span>        | [<span data-ttu-id="a47d0-158">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a47d0-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a47d0-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a47d0-159">Windows Server 2003</span></span>



| <span data-ttu-id="a47d0-160">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a47d0-160">Entry</span></span> | <span data-ttu-id="a47d0-161">Wert</span><span class="sxs-lookup"><span data-stu-id="a47d0-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a47d0-162">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a47d0-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a47d0-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a47d0-163">MAPI-Id</span></span>                | <span data-ttu-id="a47d0-164">0x3008</span><span class="sxs-lookup"><span data-stu-id="a47d0-164">0x3008</span></span>                          |
| <span data-ttu-id="a47d0-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="a47d0-165">System-Only</span></span>            | <span data-ttu-id="a47d0-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="a47d0-166">True</span></span>                            |
| <span data-ttu-id="a47d0-167">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a47d0-167">Is-Single-Valued</span></span>       | <span data-ttu-id="a47d0-168">Richtig</span><span class="sxs-lookup"><span data-stu-id="a47d0-168">True</span></span>                            |
| <span data-ttu-id="a47d0-169">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a47d0-169">Is Indexed</span></span>             | <span data-ttu-id="a47d0-170">False</span><span class="sxs-lookup"><span data-stu-id="a47d0-170">False</span></span>                           |
| <span data-ttu-id="a47d0-171">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a47d0-171">In Global Catalog</span></span>      | <span data-ttu-id="a47d0-172">Richtig</span><span class="sxs-lookup"><span data-stu-id="a47d0-172">True</span></span>                            |
| <span data-ttu-id="a47d0-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a47d0-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="a47d0-174">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a47d0-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a47d0-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a47d0-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a47d0-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a47d0-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a47d0-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a47d0-177">Search-Flags</span></span>           | <span data-ttu-id="a47d0-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a47d0-178">0x00000000</span></span>                      |
| <span data-ttu-id="a47d0-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a47d0-179">System-Flags</span></span>           | <span data-ttu-id="a47d0-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a47d0-180">0x00000013</span></span>                      |
| <span data-ttu-id="a47d0-181">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a47d0-181">Classes used in</span></span>        | [<span data-ttu-id="a47d0-182">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a47d0-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a47d0-183">Adam</span><span class="sxs-lookup"><span data-stu-id="a47d0-183">ADAM</span></span>



| <span data-ttu-id="a47d0-184">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a47d0-184">Entry</span></span> | <span data-ttu-id="a47d0-185">Wert</span><span class="sxs-lookup"><span data-stu-id="a47d0-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a47d0-186">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a47d0-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a47d0-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a47d0-187">MAPI-Id</span></span>                | <span data-ttu-id="a47d0-188">0x3008</span><span class="sxs-lookup"><span data-stu-id="a47d0-188">0x3008</span></span>                          |
| <span data-ttu-id="a47d0-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="a47d0-189">System-Only</span></span>            | <span data-ttu-id="a47d0-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="a47d0-190">True</span></span>                            |
| <span data-ttu-id="a47d0-191">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a47d0-191">Is-Single-Valued</span></span>       | <span data-ttu-id="a47d0-192">Richtig</span><span class="sxs-lookup"><span data-stu-id="a47d0-192">True</span></span>                            |
| <span data-ttu-id="a47d0-193">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a47d0-193">Is Indexed</span></span>             | <span data-ttu-id="a47d0-194">False</span><span class="sxs-lookup"><span data-stu-id="a47d0-194">False</span></span>                           |
| <span data-ttu-id="a47d0-195">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a47d0-195">In Global Catalog</span></span>      | <span data-ttu-id="a47d0-196">Richtig</span><span class="sxs-lookup"><span data-stu-id="a47d0-196">True</span></span>                            |
| <span data-ttu-id="a47d0-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a47d0-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="a47d0-198">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a47d0-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a47d0-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a47d0-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a47d0-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a47d0-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a47d0-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a47d0-201">Search-Flags</span></span>           | <span data-ttu-id="a47d0-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a47d0-202">0x00000000</span></span>                      |
| <span data-ttu-id="a47d0-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a47d0-203">System-Flags</span></span>           | <span data-ttu-id="a47d0-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a47d0-204">0x00000013</span></span>                      |
| <span data-ttu-id="a47d0-205">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a47d0-205">Classes used in</span></span>        | [<span data-ttu-id="a47d0-206">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a47d0-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a47d0-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a47d0-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a47d0-208">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a47d0-208">Entry</span></span> | <span data-ttu-id="a47d0-209">Wert</span><span class="sxs-lookup"><span data-stu-id="a47d0-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a47d0-210">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a47d0-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a47d0-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a47d0-211">MAPI-Id</span></span>                | <span data-ttu-id="a47d0-212">0x3008</span><span class="sxs-lookup"><span data-stu-id="a47d0-212">0x3008</span></span>                          |
| <span data-ttu-id="a47d0-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="a47d0-213">System-Only</span></span>            | <span data-ttu-id="a47d0-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="a47d0-214">True</span></span>                            |
| <span data-ttu-id="a47d0-215">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a47d0-215">Is-Single-Valued</span></span>       | <span data-ttu-id="a47d0-216">Richtig</span><span class="sxs-lookup"><span data-stu-id="a47d0-216">True</span></span>                            |
| <span data-ttu-id="a47d0-217">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a47d0-217">Is Indexed</span></span>             | <span data-ttu-id="a47d0-218">False</span><span class="sxs-lookup"><span data-stu-id="a47d0-218">False</span></span>                           |
| <span data-ttu-id="a47d0-219">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a47d0-219">In Global Catalog</span></span>      | <span data-ttu-id="a47d0-220">Richtig</span><span class="sxs-lookup"><span data-stu-id="a47d0-220">True</span></span>                            |
| <span data-ttu-id="a47d0-221">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a47d0-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="a47d0-222">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a47d0-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a47d0-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a47d0-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a47d0-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a47d0-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a47d0-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a47d0-225">Search-Flags</span></span>           | <span data-ttu-id="a47d0-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a47d0-226">0x00000000</span></span>                      |
| <span data-ttu-id="a47d0-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a47d0-227">System-Flags</span></span>           | <span data-ttu-id="a47d0-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a47d0-228">0x00000013</span></span>                      |
| <span data-ttu-id="a47d0-229">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a47d0-229">Classes used in</span></span>        | [<span data-ttu-id="a47d0-230">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a47d0-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a47d0-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a47d0-231">Windows Server 2008</span></span>



| <span data-ttu-id="a47d0-232">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a47d0-232">Entry</span></span> | <span data-ttu-id="a47d0-233">Wert</span><span class="sxs-lookup"><span data-stu-id="a47d0-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a47d0-234">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a47d0-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a47d0-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a47d0-235">MAPI-Id</span></span>                | <span data-ttu-id="a47d0-236">0x3008</span><span class="sxs-lookup"><span data-stu-id="a47d0-236">0x3008</span></span>                          |
| <span data-ttu-id="a47d0-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="a47d0-237">System-Only</span></span>            | <span data-ttu-id="a47d0-238">Richtig</span><span class="sxs-lookup"><span data-stu-id="a47d0-238">True</span></span>                            |
| <span data-ttu-id="a47d0-239">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a47d0-239">Is-Single-Valued</span></span>       | <span data-ttu-id="a47d0-240">Richtig</span><span class="sxs-lookup"><span data-stu-id="a47d0-240">True</span></span>                            |
| <span data-ttu-id="a47d0-241">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a47d0-241">Is Indexed</span></span>             | <span data-ttu-id="a47d0-242">False</span><span class="sxs-lookup"><span data-stu-id="a47d0-242">False</span></span>                           |
| <span data-ttu-id="a47d0-243">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a47d0-243">In Global Catalog</span></span>      | <span data-ttu-id="a47d0-244">Richtig</span><span class="sxs-lookup"><span data-stu-id="a47d0-244">True</span></span>                            |
| <span data-ttu-id="a47d0-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a47d0-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="a47d0-246">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a47d0-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a47d0-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a47d0-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a47d0-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a47d0-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a47d0-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a47d0-249">Search-Flags</span></span>           | <span data-ttu-id="a47d0-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a47d0-250">0x00000000</span></span>                      |
| <span data-ttu-id="a47d0-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a47d0-251">System-Flags</span></span>           | <span data-ttu-id="a47d0-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a47d0-252">0x00000013</span></span>                      |
| <span data-ttu-id="a47d0-253">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a47d0-253">Classes used in</span></span>        | [<span data-ttu-id="a47d0-254">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a47d0-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a47d0-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a47d0-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a47d0-256">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a47d0-256">Entry</span></span> | <span data-ttu-id="a47d0-257">Wert</span><span class="sxs-lookup"><span data-stu-id="a47d0-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a47d0-258">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a47d0-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a47d0-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a47d0-259">MAPI-Id</span></span>                | <span data-ttu-id="a47d0-260">0x3008</span><span class="sxs-lookup"><span data-stu-id="a47d0-260">0x3008</span></span>                          |
| <span data-ttu-id="a47d0-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="a47d0-261">System-Only</span></span>            | <span data-ttu-id="a47d0-262">Richtig</span><span class="sxs-lookup"><span data-stu-id="a47d0-262">True</span></span>                            |
| <span data-ttu-id="a47d0-263">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a47d0-263">Is-Single-Valued</span></span>       | <span data-ttu-id="a47d0-264">Richtig</span><span class="sxs-lookup"><span data-stu-id="a47d0-264">True</span></span>                            |
| <span data-ttu-id="a47d0-265">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a47d0-265">Is Indexed</span></span>             | <span data-ttu-id="a47d0-266">False</span><span class="sxs-lookup"><span data-stu-id="a47d0-266">False</span></span>                           |
| <span data-ttu-id="a47d0-267">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a47d0-267">In Global Catalog</span></span>      | <span data-ttu-id="a47d0-268">Richtig</span><span class="sxs-lookup"><span data-stu-id="a47d0-268">True</span></span>                            |
| <span data-ttu-id="a47d0-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a47d0-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="a47d0-270">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a47d0-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a47d0-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a47d0-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a47d0-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a47d0-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a47d0-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a47d0-273">Search-Flags</span></span>           | <span data-ttu-id="a47d0-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a47d0-274">0x00000000</span></span>                      |
| <span data-ttu-id="a47d0-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a47d0-275">System-Flags</span></span>           | <span data-ttu-id="a47d0-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a47d0-276">0x00000013</span></span>                      |
| <span data-ttu-id="a47d0-277">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a47d0-277">Classes used in</span></span>        | [<span data-ttu-id="a47d0-278">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a47d0-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a47d0-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a47d0-279">Windows Server 2012</span></span>



| <span data-ttu-id="a47d0-280">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a47d0-280">Entry</span></span> | <span data-ttu-id="a47d0-281">Wert</span><span class="sxs-lookup"><span data-stu-id="a47d0-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a47d0-282">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a47d0-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a47d0-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a47d0-283">MAPI-Id</span></span>                | <span data-ttu-id="a47d0-284">0x3008</span><span class="sxs-lookup"><span data-stu-id="a47d0-284">0x3008</span></span>                          |
| <span data-ttu-id="a47d0-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="a47d0-285">System-Only</span></span>            | <span data-ttu-id="a47d0-286">Richtig</span><span class="sxs-lookup"><span data-stu-id="a47d0-286">True</span></span>                            |
| <span data-ttu-id="a47d0-287">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a47d0-287">Is-Single-Valued</span></span>       | <span data-ttu-id="a47d0-288">Richtig</span><span class="sxs-lookup"><span data-stu-id="a47d0-288">True</span></span>                            |
| <span data-ttu-id="a47d0-289">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a47d0-289">Is Indexed</span></span>             | <span data-ttu-id="a47d0-290">False</span><span class="sxs-lookup"><span data-stu-id="a47d0-290">False</span></span>                           |
| <span data-ttu-id="a47d0-291">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a47d0-291">In Global Catalog</span></span>      | <span data-ttu-id="a47d0-292">Richtig</span><span class="sxs-lookup"><span data-stu-id="a47d0-292">True</span></span>                            |
| <span data-ttu-id="a47d0-293">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a47d0-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="a47d0-294">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a47d0-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a47d0-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a47d0-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a47d0-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a47d0-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a47d0-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a47d0-297">Search-Flags</span></span>           | <span data-ttu-id="a47d0-298">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a47d0-298">0x00000000</span></span>                      |
| <span data-ttu-id="a47d0-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a47d0-299">System-Flags</span></span>           | <span data-ttu-id="a47d0-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a47d0-300">0x00000013</span></span>                      |
| <span data-ttu-id="a47d0-301">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a47d0-301">Classes used in</span></span>        | [<span data-ttu-id="a47d0-302">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a47d0-302">**Top**</span></span>](c-top.md)<br/> |



 

 





