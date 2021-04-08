---
title: Das Attribut "US-DSA-Last-obj" wurde entfernt.
description: Enthält die Aktualisierungs Sequenznummer (Update Sequence Number, US) für das letzte Systemobjekt, das von einem Server entfernt wurde.
ms.assetid: af0afd80-fe4a-4bc6-84e3-14c2900bec93
ms.tgt_platform: multiple
keywords:
- Das AD-Schema für das Attribut "US-DSA-Last-obj" wurde entfernt.
- das Attribut "" des Attributs "" für das Attribut "".
topic_type:
- apiref
api_name:
- USN-DSA-Last-Obj-Removed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcbc246aa1a0f7c794b9dc0a9d2a725273a918e3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957562"
---
# <a name="usn-dsa-last-obj-removed-attribute"></a><span data-ttu-id="cac23-105">Das Attribut "US-DSA-Last-obj" wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="cac23-105">USN-DSA-Last-Obj-Removed attribute</span></span>

<span data-ttu-id="cac23-106">Enthält die Aktualisierungs Sequenznummer (Update Sequence Number, US) für das letzte Systemobjekt, das von einem Server entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="cac23-106">Contains the update sequence number (USN) for the last system object that was removed from a server.</span></span>



| <span data-ttu-id="cac23-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cac23-107">Entry</span></span> | <span data-ttu-id="cac23-108">Wert</span><span class="sxs-lookup"><span data-stu-id="cac23-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="cac23-109">CN</span><span class="sxs-lookup"><span data-stu-id="cac23-109">CN</span></span>                | <span data-ttu-id="cac23-110">USA-DSA-letzte-obj-entfernt</span><span class="sxs-lookup"><span data-stu-id="cac23-110">USN-DSA-Last-Obj-Removed</span></span>             |
| <span data-ttu-id="cac23-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cac23-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cac23-112">"", "".</span><span class="sxs-lookup"><span data-stu-id="cac23-112">uSNDSALastObjRemoved</span></span>                 |
| <span data-ttu-id="cac23-113">Size</span><span class="sxs-lookup"><span data-stu-id="cac23-113">Size</span></span>              | <span data-ttu-id="cac23-114">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="cac23-114">8 bytes</span></span>                              |
| <span data-ttu-id="cac23-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="cac23-115">Update Privilege</span></span>  | <span data-ttu-id="cac23-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cac23-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="cac23-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="cac23-117">Update Frequency</span></span>  | <span data-ttu-id="cac23-118">Jedes Mal, wenn sich ein Verzeichnis Objekt ändert.</span><span class="sxs-lookup"><span data-stu-id="cac23-118">Whenever a directory object changes.</span></span> |
| <span data-ttu-id="cac23-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cac23-119">Attribute-Id</span></span>      | <span data-ttu-id="cac23-120">1.2.840.113556.1.2.267</span><span class="sxs-lookup"><span data-stu-id="cac23-120">1.2.840.113556.1.2.267</span></span>               |
| <span data-ttu-id="cac23-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cac23-121">System-Id-Guid</span></span>    | <span data-ttu-id="cac23-122">bf967a71-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="cac23-122">bf967a71-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="cac23-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="cac23-123">Syntax</span></span>            | [<span data-ttu-id="cac23-124">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="cac23-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="cac23-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="cac23-125">Implementations</span></span>

-   [<span data-ttu-id="cac23-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cac23-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cac23-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cac23-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cac23-128">**Adam**</span><span class="sxs-lookup"><span data-stu-id="cac23-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cac23-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cac23-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cac23-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cac23-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cac23-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cac23-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cac23-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cac23-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cac23-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cac23-133">Windows 2000 Server</span></span>



| <span data-ttu-id="cac23-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cac23-134">Entry</span></span> | <span data-ttu-id="cac23-135">Wert</span><span class="sxs-lookup"><span data-stu-id="cac23-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cac23-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cac23-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cac23-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cac23-137">MAPI-Id</span></span>                | <span data-ttu-id="cac23-138">0x8155</span><span class="sxs-lookup"><span data-stu-id="cac23-138">0x8155</span></span>                          |
| <span data-ttu-id="cac23-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="cac23-139">System-Only</span></span>            | <span data-ttu-id="cac23-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="cac23-140">True</span></span>                            |
| <span data-ttu-id="cac23-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cac23-141">Is-Single-Valued</span></span>       | <span data-ttu-id="cac23-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="cac23-142">True</span></span>                            |
| <span data-ttu-id="cac23-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cac23-143">Is Indexed</span></span>             | <span data-ttu-id="cac23-144">False</span><span class="sxs-lookup"><span data-stu-id="cac23-144">False</span></span>                           |
| <span data-ttu-id="cac23-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cac23-145">In Global Catalog</span></span>      | <span data-ttu-id="cac23-146">False</span><span class="sxs-lookup"><span data-stu-id="cac23-146">False</span></span>                           |
| <span data-ttu-id="cac23-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cac23-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="cac23-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cac23-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cac23-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cac23-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cac23-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cac23-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cac23-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cac23-151">Search-Flags</span></span>           | <span data-ttu-id="cac23-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cac23-152">0x00000000</span></span>                      |
| <span data-ttu-id="cac23-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cac23-153">System-Flags</span></span>           | <span data-ttu-id="cac23-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cac23-154">0x00000010</span></span>                      |
| <span data-ttu-id="cac23-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cac23-155">Classes used in</span></span>        | [<span data-ttu-id="cac23-156">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="cac23-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cac23-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cac23-157">Windows Server 2003</span></span>



| <span data-ttu-id="cac23-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cac23-158">Entry</span></span> | <span data-ttu-id="cac23-159">Wert</span><span class="sxs-lookup"><span data-stu-id="cac23-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cac23-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cac23-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cac23-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cac23-161">MAPI-Id</span></span>                | <span data-ttu-id="cac23-162">0x8155</span><span class="sxs-lookup"><span data-stu-id="cac23-162">0x8155</span></span>                          |
| <span data-ttu-id="cac23-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="cac23-163">System-Only</span></span>            | <span data-ttu-id="cac23-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="cac23-164">True</span></span>                            |
| <span data-ttu-id="cac23-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cac23-165">Is-Single-Valued</span></span>       | <span data-ttu-id="cac23-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="cac23-166">True</span></span>                            |
| <span data-ttu-id="cac23-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cac23-167">Is Indexed</span></span>             | <span data-ttu-id="cac23-168">False</span><span class="sxs-lookup"><span data-stu-id="cac23-168">False</span></span>                           |
| <span data-ttu-id="cac23-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cac23-169">In Global Catalog</span></span>      | <span data-ttu-id="cac23-170">False</span><span class="sxs-lookup"><span data-stu-id="cac23-170">False</span></span>                           |
| <span data-ttu-id="cac23-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cac23-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="cac23-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cac23-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cac23-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cac23-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cac23-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cac23-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cac23-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cac23-175">Search-Flags</span></span>           | <span data-ttu-id="cac23-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cac23-176">0x00000000</span></span>                      |
| <span data-ttu-id="cac23-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cac23-177">System-Flags</span></span>           | <span data-ttu-id="cac23-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cac23-178">0x00000010</span></span>                      |
| <span data-ttu-id="cac23-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cac23-179">Classes used in</span></span>        | [<span data-ttu-id="cac23-180">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="cac23-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="cac23-181">Adam</span><span class="sxs-lookup"><span data-stu-id="cac23-181">ADAM</span></span>



| <span data-ttu-id="cac23-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cac23-182">Entry</span></span> | <span data-ttu-id="cac23-183">Wert</span><span class="sxs-lookup"><span data-stu-id="cac23-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cac23-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cac23-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cac23-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cac23-185">MAPI-Id</span></span>                | <span data-ttu-id="cac23-186">0x8155</span><span class="sxs-lookup"><span data-stu-id="cac23-186">0x8155</span></span>                          |
| <span data-ttu-id="cac23-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="cac23-187">System-Only</span></span>            | <span data-ttu-id="cac23-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="cac23-188">True</span></span>                            |
| <span data-ttu-id="cac23-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cac23-189">Is-Single-Valued</span></span>       | <span data-ttu-id="cac23-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="cac23-190">True</span></span>                            |
| <span data-ttu-id="cac23-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cac23-191">Is Indexed</span></span>             | <span data-ttu-id="cac23-192">False</span><span class="sxs-lookup"><span data-stu-id="cac23-192">False</span></span>                           |
| <span data-ttu-id="cac23-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cac23-193">In Global Catalog</span></span>      | <span data-ttu-id="cac23-194">False</span><span class="sxs-lookup"><span data-stu-id="cac23-194">False</span></span>                           |
| <span data-ttu-id="cac23-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cac23-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="cac23-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cac23-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cac23-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cac23-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cac23-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cac23-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cac23-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cac23-199">Search-Flags</span></span>           | <span data-ttu-id="cac23-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cac23-200">0x00000000</span></span>                      |
| <span data-ttu-id="cac23-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cac23-201">System-Flags</span></span>           | <span data-ttu-id="cac23-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cac23-202">0x00000010</span></span>                      |
| <span data-ttu-id="cac23-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cac23-203">Classes used in</span></span>        | [<span data-ttu-id="cac23-204">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="cac23-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cac23-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cac23-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cac23-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cac23-206">Entry</span></span> | <span data-ttu-id="cac23-207">Wert</span><span class="sxs-lookup"><span data-stu-id="cac23-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cac23-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cac23-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cac23-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cac23-209">MAPI-Id</span></span>                | <span data-ttu-id="cac23-210">0x8155</span><span class="sxs-lookup"><span data-stu-id="cac23-210">0x8155</span></span>                          |
| <span data-ttu-id="cac23-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="cac23-211">System-Only</span></span>            | <span data-ttu-id="cac23-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="cac23-212">True</span></span>                            |
| <span data-ttu-id="cac23-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cac23-213">Is-Single-Valued</span></span>       | <span data-ttu-id="cac23-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="cac23-214">True</span></span>                            |
| <span data-ttu-id="cac23-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cac23-215">Is Indexed</span></span>             | <span data-ttu-id="cac23-216">False</span><span class="sxs-lookup"><span data-stu-id="cac23-216">False</span></span>                           |
| <span data-ttu-id="cac23-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cac23-217">In Global Catalog</span></span>      | <span data-ttu-id="cac23-218">False</span><span class="sxs-lookup"><span data-stu-id="cac23-218">False</span></span>                           |
| <span data-ttu-id="cac23-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cac23-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="cac23-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cac23-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cac23-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cac23-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cac23-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cac23-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cac23-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cac23-223">Search-Flags</span></span>           | <span data-ttu-id="cac23-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cac23-224">0x00000000</span></span>                      |
| <span data-ttu-id="cac23-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cac23-225">System-Flags</span></span>           | <span data-ttu-id="cac23-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cac23-226">0x00000010</span></span>                      |
| <span data-ttu-id="cac23-227">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cac23-227">Classes used in</span></span>        | [<span data-ttu-id="cac23-228">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="cac23-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cac23-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cac23-229">Windows Server 2008</span></span>



| <span data-ttu-id="cac23-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cac23-230">Entry</span></span> | <span data-ttu-id="cac23-231">Wert</span><span class="sxs-lookup"><span data-stu-id="cac23-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cac23-232">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cac23-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cac23-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cac23-233">MAPI-Id</span></span>                | <span data-ttu-id="cac23-234">0x8155</span><span class="sxs-lookup"><span data-stu-id="cac23-234">0x8155</span></span>                          |
| <span data-ttu-id="cac23-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="cac23-235">System-Only</span></span>            | <span data-ttu-id="cac23-236">Richtig</span><span class="sxs-lookup"><span data-stu-id="cac23-236">True</span></span>                            |
| <span data-ttu-id="cac23-237">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cac23-237">Is-Single-Valued</span></span>       | <span data-ttu-id="cac23-238">Richtig</span><span class="sxs-lookup"><span data-stu-id="cac23-238">True</span></span>                            |
| <span data-ttu-id="cac23-239">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cac23-239">Is Indexed</span></span>             | <span data-ttu-id="cac23-240">False</span><span class="sxs-lookup"><span data-stu-id="cac23-240">False</span></span>                           |
| <span data-ttu-id="cac23-241">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cac23-241">In Global Catalog</span></span>      | <span data-ttu-id="cac23-242">False</span><span class="sxs-lookup"><span data-stu-id="cac23-242">False</span></span>                           |
| <span data-ttu-id="cac23-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cac23-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="cac23-244">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cac23-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cac23-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cac23-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cac23-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cac23-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cac23-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cac23-247">Search-Flags</span></span>           | <span data-ttu-id="cac23-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cac23-248">0x00000000</span></span>                      |
| <span data-ttu-id="cac23-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cac23-249">System-Flags</span></span>           | <span data-ttu-id="cac23-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cac23-250">0x00000010</span></span>                      |
| <span data-ttu-id="cac23-251">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cac23-251">Classes used in</span></span>        | [<span data-ttu-id="cac23-252">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="cac23-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cac23-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cac23-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cac23-254">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cac23-254">Entry</span></span> | <span data-ttu-id="cac23-255">Wert</span><span class="sxs-lookup"><span data-stu-id="cac23-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cac23-256">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cac23-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cac23-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cac23-257">MAPI-Id</span></span>                | <span data-ttu-id="cac23-258">0x8155</span><span class="sxs-lookup"><span data-stu-id="cac23-258">0x8155</span></span>                          |
| <span data-ttu-id="cac23-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="cac23-259">System-Only</span></span>            | <span data-ttu-id="cac23-260">Richtig</span><span class="sxs-lookup"><span data-stu-id="cac23-260">True</span></span>                            |
| <span data-ttu-id="cac23-261">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cac23-261">Is-Single-Valued</span></span>       | <span data-ttu-id="cac23-262">Richtig</span><span class="sxs-lookup"><span data-stu-id="cac23-262">True</span></span>                            |
| <span data-ttu-id="cac23-263">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cac23-263">Is Indexed</span></span>             | <span data-ttu-id="cac23-264">False</span><span class="sxs-lookup"><span data-stu-id="cac23-264">False</span></span>                           |
| <span data-ttu-id="cac23-265">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cac23-265">In Global Catalog</span></span>      | <span data-ttu-id="cac23-266">False</span><span class="sxs-lookup"><span data-stu-id="cac23-266">False</span></span>                           |
| <span data-ttu-id="cac23-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cac23-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="cac23-268">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cac23-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cac23-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cac23-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cac23-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cac23-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cac23-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cac23-271">Search-Flags</span></span>           | <span data-ttu-id="cac23-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cac23-272">0x00000000</span></span>                      |
| <span data-ttu-id="cac23-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cac23-273">System-Flags</span></span>           | <span data-ttu-id="cac23-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cac23-274">0x00000010</span></span>                      |
| <span data-ttu-id="cac23-275">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cac23-275">Classes used in</span></span>        | [<span data-ttu-id="cac23-276">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="cac23-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cac23-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cac23-277">Windows Server 2012</span></span>



| <span data-ttu-id="cac23-278">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cac23-278">Entry</span></span> | <span data-ttu-id="cac23-279">Wert</span><span class="sxs-lookup"><span data-stu-id="cac23-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cac23-280">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cac23-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cac23-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cac23-281">MAPI-Id</span></span>                | <span data-ttu-id="cac23-282">0x8155</span><span class="sxs-lookup"><span data-stu-id="cac23-282">0x8155</span></span>                          |
| <span data-ttu-id="cac23-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="cac23-283">System-Only</span></span>            | <span data-ttu-id="cac23-284">Richtig</span><span class="sxs-lookup"><span data-stu-id="cac23-284">True</span></span>                            |
| <span data-ttu-id="cac23-285">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cac23-285">Is-Single-Valued</span></span>       | <span data-ttu-id="cac23-286">Richtig</span><span class="sxs-lookup"><span data-stu-id="cac23-286">True</span></span>                            |
| <span data-ttu-id="cac23-287">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cac23-287">Is Indexed</span></span>             | <span data-ttu-id="cac23-288">False</span><span class="sxs-lookup"><span data-stu-id="cac23-288">False</span></span>                           |
| <span data-ttu-id="cac23-289">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cac23-289">In Global Catalog</span></span>      | <span data-ttu-id="cac23-290">False</span><span class="sxs-lookup"><span data-stu-id="cac23-290">False</span></span>                           |
| <span data-ttu-id="cac23-291">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cac23-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="cac23-292">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cac23-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cac23-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cac23-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cac23-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cac23-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cac23-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cac23-295">Search-Flags</span></span>           | <span data-ttu-id="cac23-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cac23-296">0x00000000</span></span>                      |
| <span data-ttu-id="cac23-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cac23-297">System-Flags</span></span>           | <span data-ttu-id="cac23-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cac23-298">0x00000010</span></span>                      |
| <span data-ttu-id="cac23-299">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cac23-299">Classes used in</span></span>        | [<span data-ttu-id="cac23-300">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="cac23-300">**Top**</span></span>](c-top.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="cac23-301">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cac23-301">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cac23-302">**"An-Last-obj-REM"**</span><span class="sxs-lookup"><span data-stu-id="cac23-302">**USN-Last-Obj-Rem**</span></span>](a-usnlastobjrem.md)
</dt> </dl>

 

 





