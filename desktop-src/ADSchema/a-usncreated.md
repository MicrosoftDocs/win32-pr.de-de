---
title: USN-Created-Attribut
description: Die bei der Objekt Erstellung zugewiesene Aktualisierungs Sequenznummer (Update Sequence Number, en). Siehe auch.
ms.assetid: c38456b8-fc8f-4ea0-8f3d-e2bb3b44ff50
ms.tgt_platform: multiple
keywords:
- AD-Schema für USN-Created-Attribut
- Schema für Schema-AD-Attribut
topic_type:
- apiref
api_name:
- USN-Created
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b950ddfe261de5d46980e51b236da0f775fcb01b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106343905"
---
# <a name="usn-created-attribute"></a><span data-ttu-id="1a2de-106">USN-Created-Attribut</span><span class="sxs-lookup"><span data-stu-id="1a2de-106">USN-Created attribute</span></span>

<span data-ttu-id="1a2de-107">Die bei der Objekt Erstellung zugewiesene Aktualisierungs Sequenznummer (Update Sequence Number, en).</span><span class="sxs-lookup"><span data-stu-id="1a2de-107">The update sequence number (USN) assigned at object creation.</span></span> <span data-ttu-id="1a2de-108">Siehe [**auch.**](a-usnchanged.md)</span><span class="sxs-lookup"><span data-stu-id="1a2de-108">See also, [**USN-Changed**](a-usnchanged.md).</span></span>



| <span data-ttu-id="1a2de-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1a2de-109">Entry</span></span> | <span data-ttu-id="1a2de-110">Wert</span><span class="sxs-lookup"><span data-stu-id="1a2de-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="1a2de-111">CN</span><span class="sxs-lookup"><span data-stu-id="1a2de-111">CN</span></span>                | <span data-ttu-id="1a2de-112">USN-Created</span><span class="sxs-lookup"><span data-stu-id="1a2de-112">USN-Created</span></span>                          |
| <span data-ttu-id="1a2de-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1a2de-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1a2de-114">uSNCreated</span><span class="sxs-lookup"><span data-stu-id="1a2de-114">uSNCreated</span></span>                           |
| <span data-ttu-id="1a2de-115">Size</span><span class="sxs-lookup"><span data-stu-id="1a2de-115">Size</span></span>              | <span data-ttu-id="1a2de-116">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="1a2de-116">8 bytes</span></span>                              |
| <span data-ttu-id="1a2de-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="1a2de-117">Update Privilege</span></span>  | <span data-ttu-id="1a2de-118">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1a2de-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="1a2de-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="1a2de-119">Update Frequency</span></span>  | <span data-ttu-id="1a2de-120">Wenn das Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1a2de-120">When the object is created.</span></span>          |
| <span data-ttu-id="1a2de-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1a2de-121">Attribute-Id</span></span>      | <span data-ttu-id="1a2de-122">1.2.840.113556.1.2.19</span><span class="sxs-lookup"><span data-stu-id="1a2de-122">1.2.840.113556.1.2.19</span></span>                |
| <span data-ttu-id="1a2de-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1a2de-123">System-Id-Guid</span></span>    | <span data-ttu-id="1a2de-124">bf967a70-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="1a2de-124">bf967a70-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="1a2de-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a2de-125">Syntax</span></span>            | [<span data-ttu-id="1a2de-126">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="1a2de-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="1a2de-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="1a2de-127">Implementations</span></span>

-   [<span data-ttu-id="1a2de-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1a2de-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1a2de-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1a2de-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1a2de-130">**Adam**</span><span class="sxs-lookup"><span data-stu-id="1a2de-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1a2de-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1a2de-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1a2de-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1a2de-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1a2de-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1a2de-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1a2de-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1a2de-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1a2de-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1a2de-135">Windows 2000 Server</span></span>



| <span data-ttu-id="1a2de-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1a2de-136">Entry</span></span> | <span data-ttu-id="1a2de-137">Wert</span><span class="sxs-lookup"><span data-stu-id="1a2de-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1a2de-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1a2de-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1a2de-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a2de-139">MAPI-Id</span></span>                | <span data-ttu-id="1a2de-140">0x8154</span><span class="sxs-lookup"><span data-stu-id="1a2de-140">0x8154</span></span>                          |
| <span data-ttu-id="1a2de-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a2de-141">System-Only</span></span>            | <span data-ttu-id="1a2de-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-142">True</span></span>                            |
| <span data-ttu-id="1a2de-143">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1a2de-143">Is-Single-Valued</span></span>       | <span data-ttu-id="1a2de-144">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-144">True</span></span>                            |
| <span data-ttu-id="1a2de-145">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1a2de-145">Is Indexed</span></span>             | <span data-ttu-id="1a2de-146">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-146">True</span></span>                            |
| <span data-ttu-id="1a2de-147">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1a2de-147">In Global Catalog</span></span>      | <span data-ttu-id="1a2de-148">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-148">True</span></span>                            |
| <span data-ttu-id="1a2de-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1a2de-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a2de-150">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1a2de-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1a2de-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a2de-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1a2de-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a2de-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1a2de-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a2de-153">Search-Flags</span></span>           | <span data-ttu-id="1a2de-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="1a2de-154">0x00000009</span></span>                      |
| <span data-ttu-id="1a2de-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a2de-155">System-Flags</span></span>           | <span data-ttu-id="1a2de-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1a2de-156">0x00000013</span></span>                      |
| <span data-ttu-id="1a2de-157">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1a2de-157">Classes used in</span></span>        | [<span data-ttu-id="1a2de-158">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="1a2de-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1a2de-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1a2de-159">Windows Server 2003</span></span>



| <span data-ttu-id="1a2de-160">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1a2de-160">Entry</span></span> | <span data-ttu-id="1a2de-161">Wert</span><span class="sxs-lookup"><span data-stu-id="1a2de-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1a2de-162">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1a2de-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1a2de-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a2de-163">MAPI-Id</span></span>                | <span data-ttu-id="1a2de-164">0x8154</span><span class="sxs-lookup"><span data-stu-id="1a2de-164">0x8154</span></span>                          |
| <span data-ttu-id="1a2de-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a2de-165">System-Only</span></span>            | <span data-ttu-id="1a2de-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-166">True</span></span>                            |
| <span data-ttu-id="1a2de-167">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1a2de-167">Is-Single-Valued</span></span>       | <span data-ttu-id="1a2de-168">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-168">True</span></span>                            |
| <span data-ttu-id="1a2de-169">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1a2de-169">Is Indexed</span></span>             | <span data-ttu-id="1a2de-170">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-170">True</span></span>                            |
| <span data-ttu-id="1a2de-171">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1a2de-171">In Global Catalog</span></span>      | <span data-ttu-id="1a2de-172">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-172">True</span></span>                            |
| <span data-ttu-id="1a2de-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1a2de-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a2de-174">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1a2de-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1a2de-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a2de-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1a2de-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a2de-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1a2de-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a2de-177">Search-Flags</span></span>           | <span data-ttu-id="1a2de-178">0x00000009</span><span class="sxs-lookup"><span data-stu-id="1a2de-178">0x00000009</span></span>                      |
| <span data-ttu-id="1a2de-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a2de-179">System-Flags</span></span>           | <span data-ttu-id="1a2de-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1a2de-180">0x00000013</span></span>                      |
| <span data-ttu-id="1a2de-181">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1a2de-181">Classes used in</span></span>        | [<span data-ttu-id="1a2de-182">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="1a2de-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1a2de-183">Adam</span><span class="sxs-lookup"><span data-stu-id="1a2de-183">ADAM</span></span>



| <span data-ttu-id="1a2de-184">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1a2de-184">Entry</span></span> | <span data-ttu-id="1a2de-185">Wert</span><span class="sxs-lookup"><span data-stu-id="1a2de-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1a2de-186">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1a2de-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1a2de-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a2de-187">MAPI-Id</span></span>                | <span data-ttu-id="1a2de-188">0x8154</span><span class="sxs-lookup"><span data-stu-id="1a2de-188">0x8154</span></span>                          |
| <span data-ttu-id="1a2de-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a2de-189">System-Only</span></span>            | <span data-ttu-id="1a2de-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-190">True</span></span>                            |
| <span data-ttu-id="1a2de-191">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1a2de-191">Is-Single-Valued</span></span>       | <span data-ttu-id="1a2de-192">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-192">True</span></span>                            |
| <span data-ttu-id="1a2de-193">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1a2de-193">Is Indexed</span></span>             | <span data-ttu-id="1a2de-194">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-194">True</span></span>                            |
| <span data-ttu-id="1a2de-195">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1a2de-195">In Global Catalog</span></span>      | <span data-ttu-id="1a2de-196">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-196">True</span></span>                            |
| <span data-ttu-id="1a2de-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1a2de-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a2de-198">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1a2de-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1a2de-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a2de-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1a2de-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a2de-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1a2de-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a2de-201">Search-Flags</span></span>           | <span data-ttu-id="1a2de-202">0x00000009</span><span class="sxs-lookup"><span data-stu-id="1a2de-202">0x00000009</span></span>                      |
| <span data-ttu-id="1a2de-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a2de-203">System-Flags</span></span>           | <span data-ttu-id="1a2de-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1a2de-204">0x00000013</span></span>                      |
| <span data-ttu-id="1a2de-205">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1a2de-205">Classes used in</span></span>        | [<span data-ttu-id="1a2de-206">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="1a2de-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1a2de-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1a2de-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1a2de-208">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1a2de-208">Entry</span></span> | <span data-ttu-id="1a2de-209">Wert</span><span class="sxs-lookup"><span data-stu-id="1a2de-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1a2de-210">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1a2de-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1a2de-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a2de-211">MAPI-Id</span></span>                | <span data-ttu-id="1a2de-212">0x8154</span><span class="sxs-lookup"><span data-stu-id="1a2de-212">0x8154</span></span>                          |
| <span data-ttu-id="1a2de-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a2de-213">System-Only</span></span>            | <span data-ttu-id="1a2de-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-214">True</span></span>                            |
| <span data-ttu-id="1a2de-215">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1a2de-215">Is-Single-Valued</span></span>       | <span data-ttu-id="1a2de-216">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-216">True</span></span>                            |
| <span data-ttu-id="1a2de-217">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1a2de-217">Is Indexed</span></span>             | <span data-ttu-id="1a2de-218">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-218">True</span></span>                            |
| <span data-ttu-id="1a2de-219">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1a2de-219">In Global Catalog</span></span>      | <span data-ttu-id="1a2de-220">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-220">True</span></span>                            |
| <span data-ttu-id="1a2de-221">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1a2de-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a2de-222">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1a2de-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1a2de-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a2de-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1a2de-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a2de-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1a2de-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a2de-225">Search-Flags</span></span>           | <span data-ttu-id="1a2de-226">0x00000009</span><span class="sxs-lookup"><span data-stu-id="1a2de-226">0x00000009</span></span>                      |
| <span data-ttu-id="1a2de-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a2de-227">System-Flags</span></span>           | <span data-ttu-id="1a2de-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1a2de-228">0x00000013</span></span>                      |
| <span data-ttu-id="1a2de-229">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1a2de-229">Classes used in</span></span>        | [<span data-ttu-id="1a2de-230">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="1a2de-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1a2de-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a2de-231">Windows Server 2008</span></span>



| <span data-ttu-id="1a2de-232">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1a2de-232">Entry</span></span> | <span data-ttu-id="1a2de-233">Wert</span><span class="sxs-lookup"><span data-stu-id="1a2de-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1a2de-234">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1a2de-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1a2de-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a2de-235">MAPI-Id</span></span>                | <span data-ttu-id="1a2de-236">0x8154</span><span class="sxs-lookup"><span data-stu-id="1a2de-236">0x8154</span></span>                          |
| <span data-ttu-id="1a2de-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a2de-237">System-Only</span></span>            | <span data-ttu-id="1a2de-238">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-238">True</span></span>                            |
| <span data-ttu-id="1a2de-239">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1a2de-239">Is-Single-Valued</span></span>       | <span data-ttu-id="1a2de-240">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-240">True</span></span>                            |
| <span data-ttu-id="1a2de-241">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1a2de-241">Is Indexed</span></span>             | <span data-ttu-id="1a2de-242">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-242">True</span></span>                            |
| <span data-ttu-id="1a2de-243">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1a2de-243">In Global Catalog</span></span>      | <span data-ttu-id="1a2de-244">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-244">True</span></span>                            |
| <span data-ttu-id="1a2de-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1a2de-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a2de-246">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1a2de-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1a2de-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a2de-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1a2de-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a2de-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1a2de-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a2de-249">Search-Flags</span></span>           | <span data-ttu-id="1a2de-250">0x00000009</span><span class="sxs-lookup"><span data-stu-id="1a2de-250">0x00000009</span></span>                      |
| <span data-ttu-id="1a2de-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a2de-251">System-Flags</span></span>           | <span data-ttu-id="1a2de-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1a2de-252">0x00000013</span></span>                      |
| <span data-ttu-id="1a2de-253">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1a2de-253">Classes used in</span></span>        | [<span data-ttu-id="1a2de-254">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="1a2de-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1a2de-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1a2de-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1a2de-256">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1a2de-256">Entry</span></span> | <span data-ttu-id="1a2de-257">Wert</span><span class="sxs-lookup"><span data-stu-id="1a2de-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1a2de-258">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1a2de-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1a2de-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a2de-259">MAPI-Id</span></span>                | <span data-ttu-id="1a2de-260">0x8154</span><span class="sxs-lookup"><span data-stu-id="1a2de-260">0x8154</span></span>                          |
| <span data-ttu-id="1a2de-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a2de-261">System-Only</span></span>            | <span data-ttu-id="1a2de-262">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-262">True</span></span>                            |
| <span data-ttu-id="1a2de-263">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1a2de-263">Is-Single-Valued</span></span>       | <span data-ttu-id="1a2de-264">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-264">True</span></span>                            |
| <span data-ttu-id="1a2de-265">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1a2de-265">Is Indexed</span></span>             | <span data-ttu-id="1a2de-266">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-266">True</span></span>                            |
| <span data-ttu-id="1a2de-267">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1a2de-267">In Global Catalog</span></span>      | <span data-ttu-id="1a2de-268">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-268">True</span></span>                            |
| <span data-ttu-id="1a2de-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1a2de-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a2de-270">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1a2de-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1a2de-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a2de-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1a2de-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a2de-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1a2de-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a2de-273">Search-Flags</span></span>           | <span data-ttu-id="1a2de-274">0x00000009</span><span class="sxs-lookup"><span data-stu-id="1a2de-274">0x00000009</span></span>                      |
| <span data-ttu-id="1a2de-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a2de-275">System-Flags</span></span>           | <span data-ttu-id="1a2de-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1a2de-276">0x00000013</span></span>                      |
| <span data-ttu-id="1a2de-277">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1a2de-277">Classes used in</span></span>        | [<span data-ttu-id="1a2de-278">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="1a2de-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1a2de-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1a2de-279">Windows Server 2012</span></span>



| <span data-ttu-id="1a2de-280">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1a2de-280">Entry</span></span> | <span data-ttu-id="1a2de-281">Wert</span><span class="sxs-lookup"><span data-stu-id="1a2de-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1a2de-282">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1a2de-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1a2de-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a2de-283">MAPI-Id</span></span>                | <span data-ttu-id="1a2de-284">0x8154</span><span class="sxs-lookup"><span data-stu-id="1a2de-284">0x8154</span></span>                          |
| <span data-ttu-id="1a2de-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a2de-285">System-Only</span></span>            | <span data-ttu-id="1a2de-286">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-286">True</span></span>                            |
| <span data-ttu-id="1a2de-287">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1a2de-287">Is-Single-Valued</span></span>       | <span data-ttu-id="1a2de-288">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-288">True</span></span>                            |
| <span data-ttu-id="1a2de-289">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1a2de-289">Is Indexed</span></span>             | <span data-ttu-id="1a2de-290">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-290">True</span></span>                            |
| <span data-ttu-id="1a2de-291">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1a2de-291">In Global Catalog</span></span>      | <span data-ttu-id="1a2de-292">Richtig</span><span class="sxs-lookup"><span data-stu-id="1a2de-292">True</span></span>                            |
| <span data-ttu-id="1a2de-293">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1a2de-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a2de-294">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1a2de-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1a2de-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a2de-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1a2de-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a2de-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1a2de-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a2de-297">Search-Flags</span></span>           | <span data-ttu-id="1a2de-298">0x00000009</span><span class="sxs-lookup"><span data-stu-id="1a2de-298">0x00000009</span></span>                      |
| <span data-ttu-id="1a2de-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a2de-299">System-Flags</span></span>           | <span data-ttu-id="1a2de-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1a2de-300">0x00000013</span></span>                      |
| <span data-ttu-id="1a2de-301">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1a2de-301">Classes used in</span></span>        | [<span data-ttu-id="1a2de-302">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="1a2de-302">**Top**</span></span>](c-top.md)<br/> |



 

 





