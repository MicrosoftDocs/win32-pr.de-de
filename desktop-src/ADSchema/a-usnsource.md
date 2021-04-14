---
title: USN-Source-Attribut
description: Der Wert des USN-Changed-Attributs des-Objekts aus dem Remote Verzeichnis, das die Änderung auf den lokalen Server repliziert hat.
ms.assetid: b307f84a-3ab1-4bfa-afc2-e74055f2a652
ms.tgt_platform: multiple
keywords:
- AD-Schema für USN-Source-Attribut
- AD-Schema für das Quell Attribut
topic_type:
- apiref
api_name:
- USN-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0998ffb73fc02511d77440550c8c669b35a98563
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104392264"
---
# <a name="usn-source-attribute"></a><span data-ttu-id="da30d-105">USN-Source-Attribut</span><span class="sxs-lookup"><span data-stu-id="da30d-105">USN-Source attribute</span></span>

<span data-ttu-id="da30d-106">Wert des Attributs, das von der Attribut-Änderung des [**-**](a-usnchanged.md) Objekts aus dem Remote Verzeichnis abgeleitet wurde, von dem die Änderung auf den lokalen Server repliziert wurde.</span><span class="sxs-lookup"><span data-stu-id="da30d-106">Value of the [**USN-Changed**](a-usnchanged.md) attribute of the object from the remote directory that replicated the change to the local server.</span></span>



| <span data-ttu-id="da30d-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da30d-107">Entry</span></span> | <span data-ttu-id="da30d-108">Wert</span><span class="sxs-lookup"><span data-stu-id="da30d-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da30d-109">CN</span><span class="sxs-lookup"><span data-stu-id="da30d-109">CN</span></span>                | <span data-ttu-id="da30d-110">USN-Source</span><span class="sxs-lookup"><span data-stu-id="da30d-110">USN-Source</span></span>                                                                                          |
| <span data-ttu-id="da30d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="da30d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="da30d-112">Quelle</span><span class="sxs-lookup"><span data-stu-id="da30d-112">uSNSource</span></span>                                                                                           |
| <span data-ttu-id="da30d-113">Size</span><span class="sxs-lookup"><span data-stu-id="da30d-113">Size</span></span>              | <span data-ttu-id="da30d-114">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="da30d-114">8 bytes</span></span>                                                                                             |
| <span data-ttu-id="da30d-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="da30d-115">Update Privilege</span></span>  | <span data-ttu-id="da30d-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="da30d-116">This value is set by the system.</span></span>                                                                    |
| <span data-ttu-id="da30d-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="da30d-117">Update Frequency</span></span>  | <span data-ttu-id="da30d-118">Wenn das Objekt in einem Remote Verzeichnis geändert wird, das die Änderung in das lokale Verzeichnis repliziert hat.</span><span class="sxs-lookup"><span data-stu-id="da30d-118">When the object is changed on a remote directory that replicated the change to the local directory.</span></span> |
| <span data-ttu-id="da30d-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="da30d-119">Attribute-Id</span></span>      | <span data-ttu-id="da30d-120">1.2.840.113556.1.4.896</span><span class="sxs-lookup"><span data-stu-id="da30d-120">1.2.840.113556.1.4.896</span></span>                                                                              |
| <span data-ttu-id="da30d-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="da30d-121">System-Id-Guid</span></span>    | <span data-ttu-id="da30d-122">167758ad-47b3-11d1-a9c3-0000f 80367c1</span><span class="sxs-lookup"><span data-stu-id="da30d-122">167758ad-47f3-11d1-a9c3-0000f80367c1</span></span>                                                                |
| <span data-ttu-id="da30d-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="da30d-123">Syntax</span></span>            | [<span data-ttu-id="da30d-124">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="da30d-124">**Interval**</span></span>](s-interval.md)                                                                      |



## <a name="implementations"></a><span data-ttu-id="da30d-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="da30d-125">Implementations</span></span>

-   [<span data-ttu-id="da30d-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="da30d-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="da30d-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="da30d-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="da30d-128">**Adam**</span><span class="sxs-lookup"><span data-stu-id="da30d-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="da30d-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="da30d-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="da30d-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="da30d-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="da30d-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="da30d-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="da30d-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="da30d-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="da30d-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="da30d-133">Windows 2000 Server</span></span>



| <span data-ttu-id="da30d-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da30d-134">Entry</span></span> | <span data-ttu-id="da30d-135">Wert</span><span class="sxs-lookup"><span data-stu-id="da30d-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="da30d-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da30d-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="da30d-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da30d-137">MAPI-Id</span></span>                | <span data-ttu-id="da30d-138">0x8157</span><span class="sxs-lookup"><span data-stu-id="da30d-138">0x8157</span></span>                          |
| <span data-ttu-id="da30d-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="da30d-139">System-Only</span></span>            | <span data-ttu-id="da30d-140">False</span><span class="sxs-lookup"><span data-stu-id="da30d-140">False</span></span>                           |
| <span data-ttu-id="da30d-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da30d-141">Is-Single-Valued</span></span>       | <span data-ttu-id="da30d-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="da30d-142">True</span></span>                            |
| <span data-ttu-id="da30d-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da30d-143">Is Indexed</span></span>             | <span data-ttu-id="da30d-144">False</span><span class="sxs-lookup"><span data-stu-id="da30d-144">False</span></span>                           |
| <span data-ttu-id="da30d-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da30d-145">In Global Catalog</span></span>      | <span data-ttu-id="da30d-146">False</span><span class="sxs-lookup"><span data-stu-id="da30d-146">False</span></span>                           |
| <span data-ttu-id="da30d-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da30d-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="da30d-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da30d-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="da30d-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da30d-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="da30d-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da30d-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="da30d-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da30d-151">Search-Flags</span></span>           | <span data-ttu-id="da30d-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da30d-152">0x00000000</span></span>                      |
| <span data-ttu-id="da30d-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da30d-153">System-Flags</span></span>           | <span data-ttu-id="da30d-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da30d-154">0x00000010</span></span>                      |
| <span data-ttu-id="da30d-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da30d-155">Classes used in</span></span>        | [<span data-ttu-id="da30d-156">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="da30d-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="da30d-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="da30d-157">Windows Server 2003</span></span>



| <span data-ttu-id="da30d-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da30d-158">Entry</span></span> | <span data-ttu-id="da30d-159">Wert</span><span class="sxs-lookup"><span data-stu-id="da30d-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="da30d-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da30d-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="da30d-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da30d-161">MAPI-Id</span></span>                | <span data-ttu-id="da30d-162">0x8157</span><span class="sxs-lookup"><span data-stu-id="da30d-162">0x8157</span></span>                          |
| <span data-ttu-id="da30d-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="da30d-163">System-Only</span></span>            | <span data-ttu-id="da30d-164">False</span><span class="sxs-lookup"><span data-stu-id="da30d-164">False</span></span>                           |
| <span data-ttu-id="da30d-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da30d-165">Is-Single-Valued</span></span>       | <span data-ttu-id="da30d-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="da30d-166">True</span></span>                            |
| <span data-ttu-id="da30d-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da30d-167">Is Indexed</span></span>             | <span data-ttu-id="da30d-168">False</span><span class="sxs-lookup"><span data-stu-id="da30d-168">False</span></span>                           |
| <span data-ttu-id="da30d-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da30d-169">In Global Catalog</span></span>      | <span data-ttu-id="da30d-170">False</span><span class="sxs-lookup"><span data-stu-id="da30d-170">False</span></span>                           |
| <span data-ttu-id="da30d-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da30d-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="da30d-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da30d-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="da30d-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da30d-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="da30d-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da30d-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="da30d-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da30d-175">Search-Flags</span></span>           | <span data-ttu-id="da30d-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da30d-176">0x00000000</span></span>                      |
| <span data-ttu-id="da30d-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da30d-177">System-Flags</span></span>           | <span data-ttu-id="da30d-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da30d-178">0x00000010</span></span>                      |
| <span data-ttu-id="da30d-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da30d-179">Classes used in</span></span>        | [<span data-ttu-id="da30d-180">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="da30d-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="da30d-181">Adam</span><span class="sxs-lookup"><span data-stu-id="da30d-181">ADAM</span></span>



| <span data-ttu-id="da30d-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da30d-182">Entry</span></span> | <span data-ttu-id="da30d-183">Wert</span><span class="sxs-lookup"><span data-stu-id="da30d-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="da30d-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da30d-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="da30d-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da30d-185">MAPI-Id</span></span>                | <span data-ttu-id="da30d-186">0x8157</span><span class="sxs-lookup"><span data-stu-id="da30d-186">0x8157</span></span>                          |
| <span data-ttu-id="da30d-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="da30d-187">System-Only</span></span>            | <span data-ttu-id="da30d-188">False</span><span class="sxs-lookup"><span data-stu-id="da30d-188">False</span></span>                           |
| <span data-ttu-id="da30d-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da30d-189">Is-Single-Valued</span></span>       | <span data-ttu-id="da30d-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="da30d-190">True</span></span>                            |
| <span data-ttu-id="da30d-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da30d-191">Is Indexed</span></span>             | <span data-ttu-id="da30d-192">False</span><span class="sxs-lookup"><span data-stu-id="da30d-192">False</span></span>                           |
| <span data-ttu-id="da30d-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da30d-193">In Global Catalog</span></span>      | <span data-ttu-id="da30d-194">False</span><span class="sxs-lookup"><span data-stu-id="da30d-194">False</span></span>                           |
| <span data-ttu-id="da30d-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da30d-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="da30d-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da30d-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="da30d-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da30d-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="da30d-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da30d-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="da30d-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da30d-199">Search-Flags</span></span>           | <span data-ttu-id="da30d-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da30d-200">0x00000000</span></span>                      |
| <span data-ttu-id="da30d-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da30d-201">System-Flags</span></span>           | <span data-ttu-id="da30d-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da30d-202">0x00000010</span></span>                      |
| <span data-ttu-id="da30d-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da30d-203">Classes used in</span></span>        | [<span data-ttu-id="da30d-204">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="da30d-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="da30d-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="da30d-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="da30d-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da30d-206">Entry</span></span> | <span data-ttu-id="da30d-207">Wert</span><span class="sxs-lookup"><span data-stu-id="da30d-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="da30d-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da30d-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="da30d-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da30d-209">MAPI-Id</span></span>                | <span data-ttu-id="da30d-210">0x8157</span><span class="sxs-lookup"><span data-stu-id="da30d-210">0x8157</span></span>                          |
| <span data-ttu-id="da30d-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="da30d-211">System-Only</span></span>            | <span data-ttu-id="da30d-212">False</span><span class="sxs-lookup"><span data-stu-id="da30d-212">False</span></span>                           |
| <span data-ttu-id="da30d-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da30d-213">Is-Single-Valued</span></span>       | <span data-ttu-id="da30d-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="da30d-214">True</span></span>                            |
| <span data-ttu-id="da30d-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da30d-215">Is Indexed</span></span>             | <span data-ttu-id="da30d-216">False</span><span class="sxs-lookup"><span data-stu-id="da30d-216">False</span></span>                           |
| <span data-ttu-id="da30d-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da30d-217">In Global Catalog</span></span>      | <span data-ttu-id="da30d-218">False</span><span class="sxs-lookup"><span data-stu-id="da30d-218">False</span></span>                           |
| <span data-ttu-id="da30d-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da30d-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="da30d-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da30d-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="da30d-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da30d-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="da30d-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da30d-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="da30d-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da30d-223">Search-Flags</span></span>           | <span data-ttu-id="da30d-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da30d-224">0x00000000</span></span>                      |
| <span data-ttu-id="da30d-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da30d-225">System-Flags</span></span>           | <span data-ttu-id="da30d-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da30d-226">0x00000010</span></span>                      |
| <span data-ttu-id="da30d-227">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da30d-227">Classes used in</span></span>        | [<span data-ttu-id="da30d-228">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="da30d-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="da30d-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da30d-229">Windows Server 2008</span></span>



| <span data-ttu-id="da30d-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da30d-230">Entry</span></span> | <span data-ttu-id="da30d-231">Wert</span><span class="sxs-lookup"><span data-stu-id="da30d-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="da30d-232">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da30d-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="da30d-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da30d-233">MAPI-Id</span></span>                | <span data-ttu-id="da30d-234">0x8157</span><span class="sxs-lookup"><span data-stu-id="da30d-234">0x8157</span></span>                          |
| <span data-ttu-id="da30d-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="da30d-235">System-Only</span></span>            | <span data-ttu-id="da30d-236">False</span><span class="sxs-lookup"><span data-stu-id="da30d-236">False</span></span>                           |
| <span data-ttu-id="da30d-237">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da30d-237">Is-Single-Valued</span></span>       | <span data-ttu-id="da30d-238">Richtig</span><span class="sxs-lookup"><span data-stu-id="da30d-238">True</span></span>                            |
| <span data-ttu-id="da30d-239">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da30d-239">Is Indexed</span></span>             | <span data-ttu-id="da30d-240">False</span><span class="sxs-lookup"><span data-stu-id="da30d-240">False</span></span>                           |
| <span data-ttu-id="da30d-241">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da30d-241">In Global Catalog</span></span>      | <span data-ttu-id="da30d-242">False</span><span class="sxs-lookup"><span data-stu-id="da30d-242">False</span></span>                           |
| <span data-ttu-id="da30d-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da30d-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="da30d-244">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da30d-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="da30d-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da30d-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="da30d-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da30d-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="da30d-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da30d-247">Search-Flags</span></span>           | <span data-ttu-id="da30d-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da30d-248">0x00000000</span></span>                      |
| <span data-ttu-id="da30d-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da30d-249">System-Flags</span></span>           | <span data-ttu-id="da30d-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da30d-250">0x00000010</span></span>                      |
| <span data-ttu-id="da30d-251">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da30d-251">Classes used in</span></span>        | [<span data-ttu-id="da30d-252">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="da30d-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="da30d-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="da30d-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="da30d-254">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da30d-254">Entry</span></span> | <span data-ttu-id="da30d-255">Wert</span><span class="sxs-lookup"><span data-stu-id="da30d-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="da30d-256">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da30d-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="da30d-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da30d-257">MAPI-Id</span></span>                | <span data-ttu-id="da30d-258">0x8157</span><span class="sxs-lookup"><span data-stu-id="da30d-258">0x8157</span></span>                          |
| <span data-ttu-id="da30d-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="da30d-259">System-Only</span></span>            | <span data-ttu-id="da30d-260">False</span><span class="sxs-lookup"><span data-stu-id="da30d-260">False</span></span>                           |
| <span data-ttu-id="da30d-261">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da30d-261">Is-Single-Valued</span></span>       | <span data-ttu-id="da30d-262">Richtig</span><span class="sxs-lookup"><span data-stu-id="da30d-262">True</span></span>                            |
| <span data-ttu-id="da30d-263">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da30d-263">Is Indexed</span></span>             | <span data-ttu-id="da30d-264">False</span><span class="sxs-lookup"><span data-stu-id="da30d-264">False</span></span>                           |
| <span data-ttu-id="da30d-265">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da30d-265">In Global Catalog</span></span>      | <span data-ttu-id="da30d-266">False</span><span class="sxs-lookup"><span data-stu-id="da30d-266">False</span></span>                           |
| <span data-ttu-id="da30d-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da30d-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="da30d-268">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da30d-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="da30d-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da30d-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="da30d-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da30d-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="da30d-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da30d-271">Search-Flags</span></span>           | <span data-ttu-id="da30d-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da30d-272">0x00000000</span></span>                      |
| <span data-ttu-id="da30d-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da30d-273">System-Flags</span></span>           | <span data-ttu-id="da30d-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da30d-274">0x00000010</span></span>                      |
| <span data-ttu-id="da30d-275">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da30d-275">Classes used in</span></span>        | [<span data-ttu-id="da30d-276">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="da30d-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="da30d-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="da30d-277">Windows Server 2012</span></span>



| <span data-ttu-id="da30d-278">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da30d-278">Entry</span></span> | <span data-ttu-id="da30d-279">Wert</span><span class="sxs-lookup"><span data-stu-id="da30d-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="da30d-280">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da30d-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="da30d-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da30d-281">MAPI-Id</span></span>                | <span data-ttu-id="da30d-282">0x8157</span><span class="sxs-lookup"><span data-stu-id="da30d-282">0x8157</span></span>                          |
| <span data-ttu-id="da30d-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="da30d-283">System-Only</span></span>            | <span data-ttu-id="da30d-284">False</span><span class="sxs-lookup"><span data-stu-id="da30d-284">False</span></span>                           |
| <span data-ttu-id="da30d-285">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da30d-285">Is-Single-Valued</span></span>       | <span data-ttu-id="da30d-286">Richtig</span><span class="sxs-lookup"><span data-stu-id="da30d-286">True</span></span>                            |
| <span data-ttu-id="da30d-287">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da30d-287">Is Indexed</span></span>             | <span data-ttu-id="da30d-288">False</span><span class="sxs-lookup"><span data-stu-id="da30d-288">False</span></span>                           |
| <span data-ttu-id="da30d-289">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da30d-289">In Global Catalog</span></span>      | <span data-ttu-id="da30d-290">False</span><span class="sxs-lookup"><span data-stu-id="da30d-290">False</span></span>                           |
| <span data-ttu-id="da30d-291">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da30d-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="da30d-292">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da30d-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="da30d-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da30d-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="da30d-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da30d-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="da30d-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da30d-295">Search-Flags</span></span>           | <span data-ttu-id="da30d-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da30d-296">0x00000000</span></span>                      |
| <span data-ttu-id="da30d-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da30d-297">System-Flags</span></span>           | <span data-ttu-id="da30d-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da30d-298">0x00000010</span></span>                      |
| <span data-ttu-id="da30d-299">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da30d-299">Classes used in</span></span>        | [<span data-ttu-id="da30d-300">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="da30d-300">**Top**</span></span>](c-top.md)<br/> |



 

 





