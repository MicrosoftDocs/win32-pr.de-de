---
title: "\"Kann-Last-obj-REM\"-Attribut"
description: Enthält die Aktualisierungs Sequenznummer (Update Sequence Number, US) für das letzte nicht-Systemobjekt, das von einem Server entfernt wurde.
ms.assetid: 34718bea-fa19-4084-b97f-d72a1681c3f4
ms.tgt_platform: multiple
keywords:
- AD-Schema für das "US-Last-obj-REM"-Attribut
- AD-Schema für das Attribut "US-lastobjrem"
topic_type:
- apiref
api_name:
- USN-Last-Obj-Rem
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9836bd93ca065fdfa53b0246a5bab0142e84ced6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519948"
---
# <a name="usn-last-obj-rem-attribute"></a><span data-ttu-id="02a30-105">"Kann-Last-obj-REM"-Attribut</span><span class="sxs-lookup"><span data-stu-id="02a30-105">USN-Last-Obj-Rem attribute</span></span>

<span data-ttu-id="02a30-106">Enthält die Aktualisierungs Sequenznummer (Update Sequence Number, US) für das letzte nicht-Systemobjekt, das von einem Server entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="02a30-106">Contains the update sequence number (USN) for the last non-system object that was removed from a server.</span></span>



| <span data-ttu-id="02a30-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="02a30-107">Entry</span></span> | <span data-ttu-id="02a30-108">Wert</span><span class="sxs-lookup"><span data-stu-id="02a30-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="02a30-109">CN</span><span class="sxs-lookup"><span data-stu-id="02a30-109">CN</span></span>                | <span data-ttu-id="02a30-110">"An-Last-obj-REM"</span><span class="sxs-lookup"><span data-stu-id="02a30-110">USN-Last-Obj-Rem</span></span>                     |
| <span data-ttu-id="02a30-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="02a30-111">Ldap-Display-Name</span></span> | <span data-ttu-id="02a30-112">"US-lastobjrem"</span><span class="sxs-lookup"><span data-stu-id="02a30-112">uSNLastObjRem</span></span>                        |
| <span data-ttu-id="02a30-113">Size</span><span class="sxs-lookup"><span data-stu-id="02a30-113">Size</span></span>              | <span data-ttu-id="02a30-114">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="02a30-114">8 bytes</span></span>                              |
| <span data-ttu-id="02a30-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="02a30-115">Update Privilege</span></span>  | <span data-ttu-id="02a30-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="02a30-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="02a30-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="02a30-117">Update Frequency</span></span>  | <span data-ttu-id="02a30-118">Jedes Mal, wenn sich ein Verzeichnis Objekt ändert.</span><span class="sxs-lookup"><span data-stu-id="02a30-118">Whenever a directory object changes.</span></span> |
| <span data-ttu-id="02a30-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="02a30-119">Attribute-Id</span></span>      | <span data-ttu-id="02a30-120">1.2.840.113556.1.2.121</span><span class="sxs-lookup"><span data-stu-id="02a30-120">1.2.840.113556.1.2.121</span></span>               |
| <span data-ttu-id="02a30-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="02a30-121">System-Id-Guid</span></span>    | <span data-ttu-id="02a30-122">bf967a73-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="02a30-122">bf967a73-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="02a30-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="02a30-123">Syntax</span></span>            | [<span data-ttu-id="02a30-124">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="02a30-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="02a30-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="02a30-125">Implementations</span></span>

-   [<span data-ttu-id="02a30-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="02a30-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="02a30-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="02a30-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="02a30-128">**Adam**</span><span class="sxs-lookup"><span data-stu-id="02a30-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="02a30-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="02a30-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="02a30-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="02a30-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="02a30-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="02a30-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="02a30-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="02a30-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="02a30-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="02a30-133">Windows 2000 Server</span></span>



| <span data-ttu-id="02a30-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="02a30-134">Entry</span></span> | <span data-ttu-id="02a30-135">Wert</span><span class="sxs-lookup"><span data-stu-id="02a30-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="02a30-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="02a30-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="02a30-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02a30-137">MAPI-Id</span></span>                | <span data-ttu-id="02a30-138">0x8156</span><span class="sxs-lookup"><span data-stu-id="02a30-138">0x8156</span></span>                          |
| <span data-ttu-id="02a30-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="02a30-139">System-Only</span></span>            | <span data-ttu-id="02a30-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="02a30-140">True</span></span>                            |
| <span data-ttu-id="02a30-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="02a30-141">Is-Single-Valued</span></span>       | <span data-ttu-id="02a30-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="02a30-142">True</span></span>                            |
| <span data-ttu-id="02a30-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="02a30-143">Is Indexed</span></span>             | <span data-ttu-id="02a30-144">False</span><span class="sxs-lookup"><span data-stu-id="02a30-144">False</span></span>                           |
| <span data-ttu-id="02a30-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="02a30-145">In Global Catalog</span></span>      | <span data-ttu-id="02a30-146">Richtig</span><span class="sxs-lookup"><span data-stu-id="02a30-146">True</span></span>                            |
| <span data-ttu-id="02a30-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="02a30-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="02a30-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="02a30-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="02a30-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02a30-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="02a30-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02a30-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="02a30-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02a30-151">Search-Flags</span></span>           | <span data-ttu-id="02a30-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="02a30-152">0x00000000</span></span>                      |
| <span data-ttu-id="02a30-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02a30-153">System-Flags</span></span>           | <span data-ttu-id="02a30-154">0x00000013</span><span class="sxs-lookup"><span data-stu-id="02a30-154">0x00000013</span></span>                      |
| <span data-ttu-id="02a30-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="02a30-155">Classes used in</span></span>        | [<span data-ttu-id="02a30-156">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="02a30-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="02a30-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="02a30-157">Windows Server 2003</span></span>



| <span data-ttu-id="02a30-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="02a30-158">Entry</span></span> | <span data-ttu-id="02a30-159">Wert</span><span class="sxs-lookup"><span data-stu-id="02a30-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="02a30-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="02a30-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="02a30-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02a30-161">MAPI-Id</span></span>                | <span data-ttu-id="02a30-162">0x8156</span><span class="sxs-lookup"><span data-stu-id="02a30-162">0x8156</span></span>                          |
| <span data-ttu-id="02a30-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="02a30-163">System-Only</span></span>            | <span data-ttu-id="02a30-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="02a30-164">True</span></span>                            |
| <span data-ttu-id="02a30-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="02a30-165">Is-Single-Valued</span></span>       | <span data-ttu-id="02a30-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="02a30-166">True</span></span>                            |
| <span data-ttu-id="02a30-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="02a30-167">Is Indexed</span></span>             | <span data-ttu-id="02a30-168">False</span><span class="sxs-lookup"><span data-stu-id="02a30-168">False</span></span>                           |
| <span data-ttu-id="02a30-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="02a30-169">In Global Catalog</span></span>      | <span data-ttu-id="02a30-170">Richtig</span><span class="sxs-lookup"><span data-stu-id="02a30-170">True</span></span>                            |
| <span data-ttu-id="02a30-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="02a30-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="02a30-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="02a30-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="02a30-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02a30-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="02a30-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02a30-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="02a30-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02a30-175">Search-Flags</span></span>           | <span data-ttu-id="02a30-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="02a30-176">0x00000000</span></span>                      |
| <span data-ttu-id="02a30-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02a30-177">System-Flags</span></span>           | <span data-ttu-id="02a30-178">0x00000013</span><span class="sxs-lookup"><span data-stu-id="02a30-178">0x00000013</span></span>                      |
| <span data-ttu-id="02a30-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="02a30-179">Classes used in</span></span>        | [<span data-ttu-id="02a30-180">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="02a30-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="02a30-181">Adam</span><span class="sxs-lookup"><span data-stu-id="02a30-181">ADAM</span></span>



| <span data-ttu-id="02a30-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="02a30-182">Entry</span></span> | <span data-ttu-id="02a30-183">Wert</span><span class="sxs-lookup"><span data-stu-id="02a30-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="02a30-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="02a30-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="02a30-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02a30-185">MAPI-Id</span></span>                | <span data-ttu-id="02a30-186">0x8156</span><span class="sxs-lookup"><span data-stu-id="02a30-186">0x8156</span></span>                          |
| <span data-ttu-id="02a30-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="02a30-187">System-Only</span></span>            | <span data-ttu-id="02a30-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="02a30-188">True</span></span>                            |
| <span data-ttu-id="02a30-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="02a30-189">Is-Single-Valued</span></span>       | <span data-ttu-id="02a30-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="02a30-190">True</span></span>                            |
| <span data-ttu-id="02a30-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="02a30-191">Is Indexed</span></span>             | <span data-ttu-id="02a30-192">False</span><span class="sxs-lookup"><span data-stu-id="02a30-192">False</span></span>                           |
| <span data-ttu-id="02a30-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="02a30-193">In Global Catalog</span></span>      | <span data-ttu-id="02a30-194">Richtig</span><span class="sxs-lookup"><span data-stu-id="02a30-194">True</span></span>                            |
| <span data-ttu-id="02a30-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="02a30-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="02a30-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="02a30-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="02a30-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02a30-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="02a30-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02a30-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="02a30-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02a30-199">Search-Flags</span></span>           | <span data-ttu-id="02a30-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="02a30-200">0x00000000</span></span>                      |
| <span data-ttu-id="02a30-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02a30-201">System-Flags</span></span>           | <span data-ttu-id="02a30-202">0x00000013</span><span class="sxs-lookup"><span data-stu-id="02a30-202">0x00000013</span></span>                      |
| <span data-ttu-id="02a30-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="02a30-203">Classes used in</span></span>        | [<span data-ttu-id="02a30-204">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="02a30-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="02a30-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="02a30-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="02a30-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="02a30-206">Entry</span></span> | <span data-ttu-id="02a30-207">Wert</span><span class="sxs-lookup"><span data-stu-id="02a30-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="02a30-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="02a30-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="02a30-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02a30-209">MAPI-Id</span></span>                | <span data-ttu-id="02a30-210">0x8156</span><span class="sxs-lookup"><span data-stu-id="02a30-210">0x8156</span></span>                          |
| <span data-ttu-id="02a30-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="02a30-211">System-Only</span></span>            | <span data-ttu-id="02a30-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="02a30-212">True</span></span>                            |
| <span data-ttu-id="02a30-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="02a30-213">Is-Single-Valued</span></span>       | <span data-ttu-id="02a30-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="02a30-214">True</span></span>                            |
| <span data-ttu-id="02a30-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="02a30-215">Is Indexed</span></span>             | <span data-ttu-id="02a30-216">False</span><span class="sxs-lookup"><span data-stu-id="02a30-216">False</span></span>                           |
| <span data-ttu-id="02a30-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="02a30-217">In Global Catalog</span></span>      | <span data-ttu-id="02a30-218">Richtig</span><span class="sxs-lookup"><span data-stu-id="02a30-218">True</span></span>                            |
| <span data-ttu-id="02a30-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="02a30-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="02a30-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="02a30-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="02a30-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02a30-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="02a30-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02a30-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="02a30-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02a30-223">Search-Flags</span></span>           | <span data-ttu-id="02a30-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="02a30-224">0x00000000</span></span>                      |
| <span data-ttu-id="02a30-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02a30-225">System-Flags</span></span>           | <span data-ttu-id="02a30-226">0x00000013</span><span class="sxs-lookup"><span data-stu-id="02a30-226">0x00000013</span></span>                      |
| <span data-ttu-id="02a30-227">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="02a30-227">Classes used in</span></span>        | [<span data-ttu-id="02a30-228">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="02a30-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="02a30-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02a30-229">Windows Server 2008</span></span>



| <span data-ttu-id="02a30-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="02a30-230">Entry</span></span> | <span data-ttu-id="02a30-231">Wert</span><span class="sxs-lookup"><span data-stu-id="02a30-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="02a30-232">Link-ID</span><span class="sxs-lookup"><span data-stu-id="02a30-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="02a30-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02a30-233">MAPI-Id</span></span>                | <span data-ttu-id="02a30-234">0x8156</span><span class="sxs-lookup"><span data-stu-id="02a30-234">0x8156</span></span>                          |
| <span data-ttu-id="02a30-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="02a30-235">System-Only</span></span>            | <span data-ttu-id="02a30-236">Richtig</span><span class="sxs-lookup"><span data-stu-id="02a30-236">True</span></span>                            |
| <span data-ttu-id="02a30-237">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="02a30-237">Is-Single-Valued</span></span>       | <span data-ttu-id="02a30-238">Richtig</span><span class="sxs-lookup"><span data-stu-id="02a30-238">True</span></span>                            |
| <span data-ttu-id="02a30-239">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="02a30-239">Is Indexed</span></span>             | <span data-ttu-id="02a30-240">False</span><span class="sxs-lookup"><span data-stu-id="02a30-240">False</span></span>                           |
| <span data-ttu-id="02a30-241">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="02a30-241">In Global Catalog</span></span>      | <span data-ttu-id="02a30-242">Richtig</span><span class="sxs-lookup"><span data-stu-id="02a30-242">True</span></span>                            |
| <span data-ttu-id="02a30-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="02a30-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="02a30-244">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="02a30-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="02a30-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02a30-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="02a30-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02a30-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="02a30-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02a30-247">Search-Flags</span></span>           | <span data-ttu-id="02a30-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="02a30-248">0x00000000</span></span>                      |
| <span data-ttu-id="02a30-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02a30-249">System-Flags</span></span>           | <span data-ttu-id="02a30-250">0x00000013</span><span class="sxs-lookup"><span data-stu-id="02a30-250">0x00000013</span></span>                      |
| <span data-ttu-id="02a30-251">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="02a30-251">Classes used in</span></span>        | [<span data-ttu-id="02a30-252">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="02a30-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="02a30-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="02a30-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="02a30-254">Eingabe</span><span class="sxs-lookup"><span data-stu-id="02a30-254">Entry</span></span> | <span data-ttu-id="02a30-255">Wert</span><span class="sxs-lookup"><span data-stu-id="02a30-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="02a30-256">Link-ID</span><span class="sxs-lookup"><span data-stu-id="02a30-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="02a30-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02a30-257">MAPI-Id</span></span>                | <span data-ttu-id="02a30-258">0x8156</span><span class="sxs-lookup"><span data-stu-id="02a30-258">0x8156</span></span>                          |
| <span data-ttu-id="02a30-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="02a30-259">System-Only</span></span>            | <span data-ttu-id="02a30-260">Richtig</span><span class="sxs-lookup"><span data-stu-id="02a30-260">True</span></span>                            |
| <span data-ttu-id="02a30-261">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="02a30-261">Is-Single-Valued</span></span>       | <span data-ttu-id="02a30-262">Richtig</span><span class="sxs-lookup"><span data-stu-id="02a30-262">True</span></span>                            |
| <span data-ttu-id="02a30-263">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="02a30-263">Is Indexed</span></span>             | <span data-ttu-id="02a30-264">False</span><span class="sxs-lookup"><span data-stu-id="02a30-264">False</span></span>                           |
| <span data-ttu-id="02a30-265">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="02a30-265">In Global Catalog</span></span>      | <span data-ttu-id="02a30-266">Richtig</span><span class="sxs-lookup"><span data-stu-id="02a30-266">True</span></span>                            |
| <span data-ttu-id="02a30-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="02a30-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="02a30-268">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="02a30-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="02a30-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02a30-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="02a30-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02a30-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="02a30-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02a30-271">Search-Flags</span></span>           | <span data-ttu-id="02a30-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="02a30-272">0x00000000</span></span>                      |
| <span data-ttu-id="02a30-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02a30-273">System-Flags</span></span>           | <span data-ttu-id="02a30-274">0x00000013</span><span class="sxs-lookup"><span data-stu-id="02a30-274">0x00000013</span></span>                      |
| <span data-ttu-id="02a30-275">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="02a30-275">Classes used in</span></span>        | [<span data-ttu-id="02a30-276">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="02a30-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="02a30-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="02a30-277">Windows Server 2012</span></span>



| <span data-ttu-id="02a30-278">Eingabe</span><span class="sxs-lookup"><span data-stu-id="02a30-278">Entry</span></span> | <span data-ttu-id="02a30-279">Wert</span><span class="sxs-lookup"><span data-stu-id="02a30-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="02a30-280">Link-ID</span><span class="sxs-lookup"><span data-stu-id="02a30-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="02a30-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02a30-281">MAPI-Id</span></span>                | <span data-ttu-id="02a30-282">0x8156</span><span class="sxs-lookup"><span data-stu-id="02a30-282">0x8156</span></span>                          |
| <span data-ttu-id="02a30-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="02a30-283">System-Only</span></span>            | <span data-ttu-id="02a30-284">Richtig</span><span class="sxs-lookup"><span data-stu-id="02a30-284">True</span></span>                            |
| <span data-ttu-id="02a30-285">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="02a30-285">Is-Single-Valued</span></span>       | <span data-ttu-id="02a30-286">Richtig</span><span class="sxs-lookup"><span data-stu-id="02a30-286">True</span></span>                            |
| <span data-ttu-id="02a30-287">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="02a30-287">Is Indexed</span></span>             | <span data-ttu-id="02a30-288">False</span><span class="sxs-lookup"><span data-stu-id="02a30-288">False</span></span>                           |
| <span data-ttu-id="02a30-289">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="02a30-289">In Global Catalog</span></span>      | <span data-ttu-id="02a30-290">Richtig</span><span class="sxs-lookup"><span data-stu-id="02a30-290">True</span></span>                            |
| <span data-ttu-id="02a30-291">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="02a30-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="02a30-292">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="02a30-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="02a30-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02a30-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="02a30-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02a30-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="02a30-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02a30-295">Search-Flags</span></span>           | <span data-ttu-id="02a30-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="02a30-296">0x00000000</span></span>                      |
| <span data-ttu-id="02a30-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02a30-297">System-Flags</span></span>           | <span data-ttu-id="02a30-298">0x00000013</span><span class="sxs-lookup"><span data-stu-id="02a30-298">0x00000013</span></span>                      |
| <span data-ttu-id="02a30-299">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="02a30-299">Classes used in</span></span>        | [<span data-ttu-id="02a30-300">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="02a30-300">**Top**</span></span>](c-top.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="02a30-301">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02a30-301">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02a30-302">**USA-DSA-letzte-obj-entfernt**</span><span class="sxs-lookup"><span data-stu-id="02a30-302">**USN-DSA-Last-Obj-Removed**</span></span>](a-usndsalastobjremoved.md)
</dt> </dl>

 

 





