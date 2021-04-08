---
title: USN-Changed-Attribut
description: Die vom lokalen Verzeichnis zugewiesene Update Sequenznummer (Update Sequence Number, US-v) für die letzte Änderung, einschließlich der Erstellung. Siehe auch.
ms.assetid: ccd61940-2c0a-4d46-af9f-5f23f577a1ad
ms.tgt_platform: multiple
keywords:
- AD-Schema für USN-Changed-Attribut
- AD-Schema für das Attribut "Attribut"
topic_type:
- apiref
api_name:
- USN-Changed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c00f30a2ba7ca38f78246cd14b33ea358da6fa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744865"
---
# <a name="usn-changed-attribute"></a><span data-ttu-id="da67b-106">USN-Changed-Attribut</span><span class="sxs-lookup"><span data-stu-id="da67b-106">USN-Changed attribute</span></span>

<span data-ttu-id="da67b-107">Die vom lokalen Verzeichnis zugewiesene Update Sequenznummer (Update Sequence Number, US-v) für die letzte Änderung, einschließlich der Erstellung.</span><span class="sxs-lookup"><span data-stu-id="da67b-107">The update sequence number (USN) assigned by the local directory for the latest change, including creation.</span></span> <span data-ttu-id="da67b-108">Siehe [**auch.**](a-usncreated.md)</span><span class="sxs-lookup"><span data-stu-id="da67b-108">See also , [**USN-Created**](a-usncreated.md).</span></span>



| <span data-ttu-id="da67b-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da67b-109">Entry</span></span> | <span data-ttu-id="da67b-110">Wert</span><span class="sxs-lookup"><span data-stu-id="da67b-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="da67b-111">CN</span><span class="sxs-lookup"><span data-stu-id="da67b-111">CN</span></span>                | <span data-ttu-id="da67b-112">USN-Changed</span><span class="sxs-lookup"><span data-stu-id="da67b-112">USN-Changed</span></span>                          |
| <span data-ttu-id="da67b-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="da67b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="da67b-114">uSNChanged</span><span class="sxs-lookup"><span data-stu-id="da67b-114">uSNChanged</span></span>                           |
| <span data-ttu-id="da67b-115">Size</span><span class="sxs-lookup"><span data-stu-id="da67b-115">Size</span></span>              | <span data-ttu-id="da67b-116">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="da67b-116">8 bytes</span></span>                              |
| <span data-ttu-id="da67b-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="da67b-117">Update Privilege</span></span>  | <span data-ttu-id="da67b-118">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="da67b-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="da67b-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="da67b-119">Update Frequency</span></span>  | <span data-ttu-id="da67b-120">Wenn das Objekt geändert wird.</span><span class="sxs-lookup"><span data-stu-id="da67b-120">When the object is changed.</span></span>          |
| <span data-ttu-id="da67b-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="da67b-121">Attribute-Id</span></span>      | <span data-ttu-id="da67b-122">1.2.840.113556.1.2.120</span><span class="sxs-lookup"><span data-stu-id="da67b-122">1.2.840.113556.1.2.120</span></span>               |
| <span data-ttu-id="da67b-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="da67b-123">System-Id-Guid</span></span>    | <span data-ttu-id="da67b-124">bf967a6f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="da67b-124">bf967a6f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="da67b-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="da67b-125">Syntax</span></span>            | [<span data-ttu-id="da67b-126">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="da67b-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="da67b-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="da67b-127">Implementations</span></span>

-   [<span data-ttu-id="da67b-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="da67b-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="da67b-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="da67b-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="da67b-130">**Adam**</span><span class="sxs-lookup"><span data-stu-id="da67b-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="da67b-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="da67b-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="da67b-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="da67b-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="da67b-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="da67b-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="da67b-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="da67b-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="da67b-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="da67b-135">Windows 2000 Server</span></span>



| <span data-ttu-id="da67b-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da67b-136">Entry</span></span> | <span data-ttu-id="da67b-137">Wert</span><span class="sxs-lookup"><span data-stu-id="da67b-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="da67b-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da67b-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="da67b-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da67b-139">MAPI-Id</span></span>                | <span data-ttu-id="da67b-140">0x8029</span><span class="sxs-lookup"><span data-stu-id="da67b-140">0x8029</span></span>                          |
| <span data-ttu-id="da67b-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="da67b-141">System-Only</span></span>            | <span data-ttu-id="da67b-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-142">True</span></span>                            |
| <span data-ttu-id="da67b-143">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da67b-143">Is-Single-Valued</span></span>       | <span data-ttu-id="da67b-144">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-144">True</span></span>                            |
| <span data-ttu-id="da67b-145">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da67b-145">Is Indexed</span></span>             | <span data-ttu-id="da67b-146">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-146">True</span></span>                            |
| <span data-ttu-id="da67b-147">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da67b-147">In Global Catalog</span></span>      | <span data-ttu-id="da67b-148">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-148">True</span></span>                            |
| <span data-ttu-id="da67b-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da67b-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="da67b-150">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da67b-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="da67b-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da67b-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="da67b-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da67b-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="da67b-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da67b-153">Search-Flags</span></span>           | <span data-ttu-id="da67b-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="da67b-154">0x00000009</span></span>                      |
| <span data-ttu-id="da67b-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da67b-155">System-Flags</span></span>           | <span data-ttu-id="da67b-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="da67b-156">0x00000013</span></span>                      |
| <span data-ttu-id="da67b-157">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da67b-157">Classes used in</span></span>        | [<span data-ttu-id="da67b-158">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="da67b-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="da67b-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="da67b-159">Windows Server 2003</span></span>



| <span data-ttu-id="da67b-160">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da67b-160">Entry</span></span> | <span data-ttu-id="da67b-161">Wert</span><span class="sxs-lookup"><span data-stu-id="da67b-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="da67b-162">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da67b-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="da67b-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da67b-163">MAPI-Id</span></span>                | <span data-ttu-id="da67b-164">0x8029</span><span class="sxs-lookup"><span data-stu-id="da67b-164">0x8029</span></span>                          |
| <span data-ttu-id="da67b-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="da67b-165">System-Only</span></span>            | <span data-ttu-id="da67b-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-166">True</span></span>                            |
| <span data-ttu-id="da67b-167">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da67b-167">Is-Single-Valued</span></span>       | <span data-ttu-id="da67b-168">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-168">True</span></span>                            |
| <span data-ttu-id="da67b-169">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da67b-169">Is Indexed</span></span>             | <span data-ttu-id="da67b-170">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-170">True</span></span>                            |
| <span data-ttu-id="da67b-171">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da67b-171">In Global Catalog</span></span>      | <span data-ttu-id="da67b-172">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-172">True</span></span>                            |
| <span data-ttu-id="da67b-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da67b-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="da67b-174">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da67b-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="da67b-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da67b-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="da67b-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da67b-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="da67b-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da67b-177">Search-Flags</span></span>           | <span data-ttu-id="da67b-178">0x00000009</span><span class="sxs-lookup"><span data-stu-id="da67b-178">0x00000009</span></span>                      |
| <span data-ttu-id="da67b-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da67b-179">System-Flags</span></span>           | <span data-ttu-id="da67b-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="da67b-180">0x00000013</span></span>                      |
| <span data-ttu-id="da67b-181">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da67b-181">Classes used in</span></span>        | [<span data-ttu-id="da67b-182">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="da67b-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="da67b-183">Adam</span><span class="sxs-lookup"><span data-stu-id="da67b-183">ADAM</span></span>



| <span data-ttu-id="da67b-184">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da67b-184">Entry</span></span> | <span data-ttu-id="da67b-185">Wert</span><span class="sxs-lookup"><span data-stu-id="da67b-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="da67b-186">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da67b-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="da67b-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da67b-187">MAPI-Id</span></span>                | <span data-ttu-id="da67b-188">0x8029</span><span class="sxs-lookup"><span data-stu-id="da67b-188">0x8029</span></span>                          |
| <span data-ttu-id="da67b-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="da67b-189">System-Only</span></span>            | <span data-ttu-id="da67b-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-190">True</span></span>                            |
| <span data-ttu-id="da67b-191">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da67b-191">Is-Single-Valued</span></span>       | <span data-ttu-id="da67b-192">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-192">True</span></span>                            |
| <span data-ttu-id="da67b-193">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da67b-193">Is Indexed</span></span>             | <span data-ttu-id="da67b-194">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-194">True</span></span>                            |
| <span data-ttu-id="da67b-195">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da67b-195">In Global Catalog</span></span>      | <span data-ttu-id="da67b-196">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-196">True</span></span>                            |
| <span data-ttu-id="da67b-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da67b-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="da67b-198">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da67b-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="da67b-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da67b-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="da67b-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da67b-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="da67b-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da67b-201">Search-Flags</span></span>           | <span data-ttu-id="da67b-202">0x00000009</span><span class="sxs-lookup"><span data-stu-id="da67b-202">0x00000009</span></span>                      |
| <span data-ttu-id="da67b-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da67b-203">System-Flags</span></span>           | <span data-ttu-id="da67b-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="da67b-204">0x00000013</span></span>                      |
| <span data-ttu-id="da67b-205">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da67b-205">Classes used in</span></span>        | [<span data-ttu-id="da67b-206">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="da67b-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="da67b-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="da67b-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="da67b-208">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da67b-208">Entry</span></span> | <span data-ttu-id="da67b-209">Wert</span><span class="sxs-lookup"><span data-stu-id="da67b-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="da67b-210">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da67b-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="da67b-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da67b-211">MAPI-Id</span></span>                | <span data-ttu-id="da67b-212">0x8029</span><span class="sxs-lookup"><span data-stu-id="da67b-212">0x8029</span></span>                          |
| <span data-ttu-id="da67b-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="da67b-213">System-Only</span></span>            | <span data-ttu-id="da67b-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-214">True</span></span>                            |
| <span data-ttu-id="da67b-215">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da67b-215">Is-Single-Valued</span></span>       | <span data-ttu-id="da67b-216">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-216">True</span></span>                            |
| <span data-ttu-id="da67b-217">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da67b-217">Is Indexed</span></span>             | <span data-ttu-id="da67b-218">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-218">True</span></span>                            |
| <span data-ttu-id="da67b-219">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da67b-219">In Global Catalog</span></span>      | <span data-ttu-id="da67b-220">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-220">True</span></span>                            |
| <span data-ttu-id="da67b-221">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da67b-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="da67b-222">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da67b-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="da67b-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da67b-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="da67b-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da67b-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="da67b-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da67b-225">Search-Flags</span></span>           | <span data-ttu-id="da67b-226">0x00000009</span><span class="sxs-lookup"><span data-stu-id="da67b-226">0x00000009</span></span>                      |
| <span data-ttu-id="da67b-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da67b-227">System-Flags</span></span>           | <span data-ttu-id="da67b-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="da67b-228">0x00000013</span></span>                      |
| <span data-ttu-id="da67b-229">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da67b-229">Classes used in</span></span>        | [<span data-ttu-id="da67b-230">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="da67b-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="da67b-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da67b-231">Windows Server 2008</span></span>



| <span data-ttu-id="da67b-232">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da67b-232">Entry</span></span> | <span data-ttu-id="da67b-233">Wert</span><span class="sxs-lookup"><span data-stu-id="da67b-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="da67b-234">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da67b-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="da67b-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da67b-235">MAPI-Id</span></span>                | <span data-ttu-id="da67b-236">0x8029</span><span class="sxs-lookup"><span data-stu-id="da67b-236">0x8029</span></span>                          |
| <span data-ttu-id="da67b-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="da67b-237">System-Only</span></span>            | <span data-ttu-id="da67b-238">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-238">True</span></span>                            |
| <span data-ttu-id="da67b-239">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da67b-239">Is-Single-Valued</span></span>       | <span data-ttu-id="da67b-240">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-240">True</span></span>                            |
| <span data-ttu-id="da67b-241">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da67b-241">Is Indexed</span></span>             | <span data-ttu-id="da67b-242">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-242">True</span></span>                            |
| <span data-ttu-id="da67b-243">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da67b-243">In Global Catalog</span></span>      | <span data-ttu-id="da67b-244">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-244">True</span></span>                            |
| <span data-ttu-id="da67b-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da67b-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="da67b-246">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da67b-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="da67b-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da67b-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="da67b-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da67b-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="da67b-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da67b-249">Search-Flags</span></span>           | <span data-ttu-id="da67b-250">0x00000009</span><span class="sxs-lookup"><span data-stu-id="da67b-250">0x00000009</span></span>                      |
| <span data-ttu-id="da67b-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da67b-251">System-Flags</span></span>           | <span data-ttu-id="da67b-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="da67b-252">0x00000013</span></span>                      |
| <span data-ttu-id="da67b-253">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da67b-253">Classes used in</span></span>        | [<span data-ttu-id="da67b-254">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="da67b-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="da67b-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="da67b-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="da67b-256">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da67b-256">Entry</span></span> | <span data-ttu-id="da67b-257">Wert</span><span class="sxs-lookup"><span data-stu-id="da67b-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="da67b-258">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da67b-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="da67b-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da67b-259">MAPI-Id</span></span>                | <span data-ttu-id="da67b-260">0x8029</span><span class="sxs-lookup"><span data-stu-id="da67b-260">0x8029</span></span>                          |
| <span data-ttu-id="da67b-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="da67b-261">System-Only</span></span>            | <span data-ttu-id="da67b-262">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-262">True</span></span>                            |
| <span data-ttu-id="da67b-263">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da67b-263">Is-Single-Valued</span></span>       | <span data-ttu-id="da67b-264">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-264">True</span></span>                            |
| <span data-ttu-id="da67b-265">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da67b-265">Is Indexed</span></span>             | <span data-ttu-id="da67b-266">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-266">True</span></span>                            |
| <span data-ttu-id="da67b-267">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da67b-267">In Global Catalog</span></span>      | <span data-ttu-id="da67b-268">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-268">True</span></span>                            |
| <span data-ttu-id="da67b-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da67b-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="da67b-270">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da67b-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="da67b-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da67b-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="da67b-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da67b-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="da67b-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da67b-273">Search-Flags</span></span>           | <span data-ttu-id="da67b-274">0x00000009</span><span class="sxs-lookup"><span data-stu-id="da67b-274">0x00000009</span></span>                      |
| <span data-ttu-id="da67b-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da67b-275">System-Flags</span></span>           | <span data-ttu-id="da67b-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="da67b-276">0x00000013</span></span>                      |
| <span data-ttu-id="da67b-277">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da67b-277">Classes used in</span></span>        | [<span data-ttu-id="da67b-278">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="da67b-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="da67b-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="da67b-279">Windows Server 2012</span></span>



| <span data-ttu-id="da67b-280">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da67b-280">Entry</span></span> | <span data-ttu-id="da67b-281">Wert</span><span class="sxs-lookup"><span data-stu-id="da67b-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="da67b-282">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da67b-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="da67b-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da67b-283">MAPI-Id</span></span>                | <span data-ttu-id="da67b-284">0x8029</span><span class="sxs-lookup"><span data-stu-id="da67b-284">0x8029</span></span>                          |
| <span data-ttu-id="da67b-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="da67b-285">System-Only</span></span>            | <span data-ttu-id="da67b-286">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-286">True</span></span>                            |
| <span data-ttu-id="da67b-287">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da67b-287">Is-Single-Valued</span></span>       | <span data-ttu-id="da67b-288">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-288">True</span></span>                            |
| <span data-ttu-id="da67b-289">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da67b-289">Is Indexed</span></span>             | <span data-ttu-id="da67b-290">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-290">True</span></span>                            |
| <span data-ttu-id="da67b-291">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da67b-291">In Global Catalog</span></span>      | <span data-ttu-id="da67b-292">Richtig</span><span class="sxs-lookup"><span data-stu-id="da67b-292">True</span></span>                            |
| <span data-ttu-id="da67b-293">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da67b-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="da67b-294">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da67b-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="da67b-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da67b-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="da67b-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da67b-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="da67b-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da67b-297">Search-Flags</span></span>           | <span data-ttu-id="da67b-298">0x00000009</span><span class="sxs-lookup"><span data-stu-id="da67b-298">0x00000009</span></span>                      |
| <span data-ttu-id="da67b-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da67b-299">System-Flags</span></span>           | <span data-ttu-id="da67b-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="da67b-300">0x00000013</span></span>                      |
| <span data-ttu-id="da67b-301">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da67b-301">Classes used in</span></span>        | [<span data-ttu-id="da67b-302">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="da67b-302">**Top**</span></span>](c-top.md)<br/> |



 

 





