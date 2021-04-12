---
title: Vol-Table-GUID-Attribut
description: Der eindeutige Bezeichner für einen Link-Track-Volume-Tabelleneintrag.
ms.assetid: 3a63406a-e751-4234-a601-8f5a57f0a3b7
ms.tgt_platform: multiple
keywords:
- Vol-Table-GUID-Attribut AD-Schema
- voltableguid-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Vol-Table-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2a23bcd088304b4a683ce3ff0f203d3c82fecf8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479874"
---
# <a name="vol-table-guid-attribute"></a><span data-ttu-id="9edaf-105">Vol-Table-GUID-Attribut</span><span class="sxs-lookup"><span data-stu-id="9edaf-105">Vol-Table-GUID attribute</span></span>

<span data-ttu-id="9edaf-106">Der eindeutige Bezeichner für einen Link-Track-Volume-Tabelleneintrag.</span><span class="sxs-lookup"><span data-stu-id="9edaf-106">The unique identifier for a Link-Track-Volume table entry.</span></span>



| <span data-ttu-id="9edaf-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9edaf-107">Entry</span></span> | <span data-ttu-id="9edaf-108">Wert</span><span class="sxs-lookup"><span data-stu-id="9edaf-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="9edaf-109">CN</span><span class="sxs-lookup"><span data-stu-id="9edaf-109">CN</span></span>                | <span data-ttu-id="9edaf-110">Vol-Table-GUID</span><span class="sxs-lookup"><span data-stu-id="9edaf-110">Vol-Table-GUID</span></span>                                        |
| <span data-ttu-id="9edaf-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9edaf-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9edaf-112">voltableguid</span><span class="sxs-lookup"><span data-stu-id="9edaf-112">volTableGUID</span></span>                                          |
| <span data-ttu-id="9edaf-113">Size</span><span class="sxs-lookup"><span data-stu-id="9edaf-113">Size</span></span>              | <span data-ttu-id="9edaf-114">16 Bytes</span><span class="sxs-lookup"><span data-stu-id="9edaf-114">16 bytes</span></span>                                              |
| <span data-ttu-id="9edaf-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="9edaf-115">Update Privilege</span></span>  | <span data-ttu-id="9edaf-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9edaf-116">This value is set by the system.</span></span>                      |
| <span data-ttu-id="9edaf-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="9edaf-117">Update Frequency</span></span>  | <span data-ttu-id="9edaf-118">Jedes Mal, wenn ein neuer Link zu einer Datei erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="9edaf-118">Whenever a new link to a file is created.</span></span>             |
| <span data-ttu-id="9edaf-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9edaf-119">Attribute-Id</span></span>      | <span data-ttu-id="9edaf-120">1.2.840.113556.1.4.336</span><span class="sxs-lookup"><span data-stu-id="9edaf-120">1.2.840.113556.1.4.336</span></span>                                |
| <span data-ttu-id="9edaf-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9edaf-121">System-Id-Guid</span></span>    | <span data-ttu-id="9edaf-122">1F 0075ld-7E40-11D0-afd6-00c04f 930c9</span><span class="sxs-lookup"><span data-stu-id="9edaf-122">1f0075fd-7e40-11d0-afd6-00c04fd930c9</span></span>                  |
| <span data-ttu-id="9edaf-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="9edaf-123">Syntax</span></span>            | [<span data-ttu-id="9edaf-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="9edaf-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="9edaf-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="9edaf-125">Implementations</span></span>

-   [<span data-ttu-id="9edaf-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9edaf-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9edaf-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9edaf-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9edaf-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9edaf-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9edaf-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9edaf-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9edaf-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9edaf-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9edaf-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9edaf-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9edaf-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9edaf-132">Windows 2000 Server</span></span>



| <span data-ttu-id="9edaf-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9edaf-133">Entry</span></span> | <span data-ttu-id="9edaf-134">Wert</span><span class="sxs-lookup"><span data-stu-id="9edaf-134">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9edaf-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9edaf-135">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9edaf-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9edaf-136">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9edaf-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="9edaf-137">System-Only</span></span>            | <span data-ttu-id="9edaf-138">False</span><span class="sxs-lookup"><span data-stu-id="9edaf-138">False</span></span>                                                          |
| <span data-ttu-id="9edaf-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9edaf-139">Is-Single-Valued</span></span>       | <span data-ttu-id="9edaf-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="9edaf-140">True</span></span>                                                           |
| <span data-ttu-id="9edaf-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9edaf-141">Is Indexed</span></span>             | <span data-ttu-id="9edaf-142">False</span><span class="sxs-lookup"><span data-stu-id="9edaf-142">False</span></span>                                                          |
| <span data-ttu-id="9edaf-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9edaf-143">In Global Catalog</span></span>      | <span data-ttu-id="9edaf-144">False</span><span class="sxs-lookup"><span data-stu-id="9edaf-144">False</span></span>                                                          |
| <span data-ttu-id="9edaf-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9edaf-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="9edaf-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9edaf-146">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="9edaf-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9edaf-147">Range-Lower</span></span>            | <span data-ttu-id="9edaf-148">0</span><span class="sxs-lookup"><span data-stu-id="9edaf-148">0</span></span>                                                              |
| <span data-ttu-id="9edaf-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9edaf-149">Range-Upper</span></span>            | <span data-ttu-id="9edaf-150">16</span><span class="sxs-lookup"><span data-stu-id="9edaf-150">16</span></span>                                                             |
| <span data-ttu-id="9edaf-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9edaf-151">Search-Flags</span></span>           | <span data-ttu-id="9edaf-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9edaf-152">0x00000000</span></span>                                                     |
| <span data-ttu-id="9edaf-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9edaf-153">System-Flags</span></span>           | <span data-ttu-id="9edaf-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9edaf-154">0x00000010</span></span>                                                     |
| <span data-ttu-id="9edaf-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9edaf-155">Classes used in</span></span>        | [<span data-ttu-id="9edaf-156">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="9edaf-156">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9edaf-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9edaf-157">Windows Server 2003</span></span>



| <span data-ttu-id="9edaf-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9edaf-158">Entry</span></span> | <span data-ttu-id="9edaf-159">Wert</span><span class="sxs-lookup"><span data-stu-id="9edaf-159">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9edaf-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9edaf-160">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9edaf-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9edaf-161">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9edaf-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="9edaf-162">System-Only</span></span>            | <span data-ttu-id="9edaf-163">False</span><span class="sxs-lookup"><span data-stu-id="9edaf-163">False</span></span>                                                          |
| <span data-ttu-id="9edaf-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9edaf-164">Is-Single-Valued</span></span>       | <span data-ttu-id="9edaf-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="9edaf-165">True</span></span>                                                           |
| <span data-ttu-id="9edaf-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9edaf-166">Is Indexed</span></span>             | <span data-ttu-id="9edaf-167">False</span><span class="sxs-lookup"><span data-stu-id="9edaf-167">False</span></span>                                                          |
| <span data-ttu-id="9edaf-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9edaf-168">In Global Catalog</span></span>      | <span data-ttu-id="9edaf-169">False</span><span class="sxs-lookup"><span data-stu-id="9edaf-169">False</span></span>                                                          |
| <span data-ttu-id="9edaf-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9edaf-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="9edaf-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9edaf-171">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="9edaf-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9edaf-172">Range-Lower</span></span>            | <span data-ttu-id="9edaf-173">0</span><span class="sxs-lookup"><span data-stu-id="9edaf-173">0</span></span>                                                              |
| <span data-ttu-id="9edaf-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9edaf-174">Range-Upper</span></span>            | <span data-ttu-id="9edaf-175">16</span><span class="sxs-lookup"><span data-stu-id="9edaf-175">16</span></span>                                                             |
| <span data-ttu-id="9edaf-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9edaf-176">Search-Flags</span></span>           | <span data-ttu-id="9edaf-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9edaf-177">0x00000000</span></span>                                                     |
| <span data-ttu-id="9edaf-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9edaf-178">System-Flags</span></span>           | <span data-ttu-id="9edaf-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9edaf-179">0x00000010</span></span>                                                     |
| <span data-ttu-id="9edaf-180">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9edaf-180">Classes used in</span></span>        | [<span data-ttu-id="9edaf-181">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="9edaf-181">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9edaf-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9edaf-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9edaf-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9edaf-183">Entry</span></span> | <span data-ttu-id="9edaf-184">Wert</span><span class="sxs-lookup"><span data-stu-id="9edaf-184">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9edaf-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9edaf-185">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9edaf-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9edaf-186">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9edaf-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="9edaf-187">System-Only</span></span>            | <span data-ttu-id="9edaf-188">False</span><span class="sxs-lookup"><span data-stu-id="9edaf-188">False</span></span>                                                          |
| <span data-ttu-id="9edaf-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9edaf-189">Is-Single-Valued</span></span>       | <span data-ttu-id="9edaf-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="9edaf-190">True</span></span>                                                           |
| <span data-ttu-id="9edaf-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9edaf-191">Is Indexed</span></span>             | <span data-ttu-id="9edaf-192">False</span><span class="sxs-lookup"><span data-stu-id="9edaf-192">False</span></span>                                                          |
| <span data-ttu-id="9edaf-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9edaf-193">In Global Catalog</span></span>      | <span data-ttu-id="9edaf-194">False</span><span class="sxs-lookup"><span data-stu-id="9edaf-194">False</span></span>                                                          |
| <span data-ttu-id="9edaf-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9edaf-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="9edaf-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9edaf-196">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="9edaf-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9edaf-197">Range-Lower</span></span>            | <span data-ttu-id="9edaf-198">0</span><span class="sxs-lookup"><span data-stu-id="9edaf-198">0</span></span>                                                              |
| <span data-ttu-id="9edaf-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9edaf-199">Range-Upper</span></span>            | <span data-ttu-id="9edaf-200">16</span><span class="sxs-lookup"><span data-stu-id="9edaf-200">16</span></span>                                                             |
| <span data-ttu-id="9edaf-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9edaf-201">Search-Flags</span></span>           | <span data-ttu-id="9edaf-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9edaf-202">0x00000000</span></span>                                                     |
| <span data-ttu-id="9edaf-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9edaf-203">System-Flags</span></span>           | <span data-ttu-id="9edaf-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9edaf-204">0x00000010</span></span>                                                     |
| <span data-ttu-id="9edaf-205">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9edaf-205">Classes used in</span></span>        | [<span data-ttu-id="9edaf-206">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="9edaf-206">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9edaf-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9edaf-207">Windows Server 2008</span></span>



| <span data-ttu-id="9edaf-208">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9edaf-208">Entry</span></span> | <span data-ttu-id="9edaf-209">Wert</span><span class="sxs-lookup"><span data-stu-id="9edaf-209">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9edaf-210">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9edaf-210">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9edaf-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9edaf-211">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9edaf-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="9edaf-212">System-Only</span></span>            | <span data-ttu-id="9edaf-213">False</span><span class="sxs-lookup"><span data-stu-id="9edaf-213">False</span></span>                                                          |
| <span data-ttu-id="9edaf-214">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9edaf-214">Is-Single-Valued</span></span>       | <span data-ttu-id="9edaf-215">Richtig</span><span class="sxs-lookup"><span data-stu-id="9edaf-215">True</span></span>                                                           |
| <span data-ttu-id="9edaf-216">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9edaf-216">Is Indexed</span></span>             | <span data-ttu-id="9edaf-217">False</span><span class="sxs-lookup"><span data-stu-id="9edaf-217">False</span></span>                                                          |
| <span data-ttu-id="9edaf-218">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9edaf-218">In Global Catalog</span></span>      | <span data-ttu-id="9edaf-219">False</span><span class="sxs-lookup"><span data-stu-id="9edaf-219">False</span></span>                                                          |
| <span data-ttu-id="9edaf-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9edaf-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="9edaf-221">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9edaf-221">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="9edaf-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9edaf-222">Range-Lower</span></span>            | <span data-ttu-id="9edaf-223">0</span><span class="sxs-lookup"><span data-stu-id="9edaf-223">0</span></span>                                                              |
| <span data-ttu-id="9edaf-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9edaf-224">Range-Upper</span></span>            | <span data-ttu-id="9edaf-225">16</span><span class="sxs-lookup"><span data-stu-id="9edaf-225">16</span></span>                                                             |
| <span data-ttu-id="9edaf-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9edaf-226">Search-Flags</span></span>           | <span data-ttu-id="9edaf-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9edaf-227">0x00000000</span></span>                                                     |
| <span data-ttu-id="9edaf-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9edaf-228">System-Flags</span></span>           | <span data-ttu-id="9edaf-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9edaf-229">0x00000010</span></span>                                                     |
| <span data-ttu-id="9edaf-230">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9edaf-230">Classes used in</span></span>        | [<span data-ttu-id="9edaf-231">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="9edaf-231">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9edaf-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9edaf-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9edaf-233">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9edaf-233">Entry</span></span> | <span data-ttu-id="9edaf-234">Wert</span><span class="sxs-lookup"><span data-stu-id="9edaf-234">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9edaf-235">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9edaf-235">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9edaf-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9edaf-236">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9edaf-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="9edaf-237">System-Only</span></span>            | <span data-ttu-id="9edaf-238">False</span><span class="sxs-lookup"><span data-stu-id="9edaf-238">False</span></span>                                                          |
| <span data-ttu-id="9edaf-239">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9edaf-239">Is-Single-Valued</span></span>       | <span data-ttu-id="9edaf-240">Richtig</span><span class="sxs-lookup"><span data-stu-id="9edaf-240">True</span></span>                                                           |
| <span data-ttu-id="9edaf-241">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9edaf-241">Is Indexed</span></span>             | <span data-ttu-id="9edaf-242">False</span><span class="sxs-lookup"><span data-stu-id="9edaf-242">False</span></span>                                                          |
| <span data-ttu-id="9edaf-243">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9edaf-243">In Global Catalog</span></span>      | <span data-ttu-id="9edaf-244">False</span><span class="sxs-lookup"><span data-stu-id="9edaf-244">False</span></span>                                                          |
| <span data-ttu-id="9edaf-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9edaf-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="9edaf-246">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9edaf-246">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="9edaf-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9edaf-247">Range-Lower</span></span>            | <span data-ttu-id="9edaf-248">0</span><span class="sxs-lookup"><span data-stu-id="9edaf-248">0</span></span>                                                              |
| <span data-ttu-id="9edaf-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9edaf-249">Range-Upper</span></span>            | <span data-ttu-id="9edaf-250">16</span><span class="sxs-lookup"><span data-stu-id="9edaf-250">16</span></span>                                                             |
| <span data-ttu-id="9edaf-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9edaf-251">Search-Flags</span></span>           | <span data-ttu-id="9edaf-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9edaf-252">0x00000000</span></span>                                                     |
| <span data-ttu-id="9edaf-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9edaf-253">System-Flags</span></span>           | <span data-ttu-id="9edaf-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9edaf-254">0x00000010</span></span>                                                     |
| <span data-ttu-id="9edaf-255">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9edaf-255">Classes used in</span></span>        | [<span data-ttu-id="9edaf-256">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="9edaf-256">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9edaf-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9edaf-257">Windows Server 2012</span></span>



| <span data-ttu-id="9edaf-258">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9edaf-258">Entry</span></span> | <span data-ttu-id="9edaf-259">Wert</span><span class="sxs-lookup"><span data-stu-id="9edaf-259">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9edaf-260">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9edaf-260">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9edaf-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9edaf-261">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9edaf-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="9edaf-262">System-Only</span></span>            | <span data-ttu-id="9edaf-263">False</span><span class="sxs-lookup"><span data-stu-id="9edaf-263">False</span></span>                                                          |
| <span data-ttu-id="9edaf-264">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9edaf-264">Is-Single-Valued</span></span>       | <span data-ttu-id="9edaf-265">Richtig</span><span class="sxs-lookup"><span data-stu-id="9edaf-265">True</span></span>                                                           |
| <span data-ttu-id="9edaf-266">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9edaf-266">Is Indexed</span></span>             | <span data-ttu-id="9edaf-267">False</span><span class="sxs-lookup"><span data-stu-id="9edaf-267">False</span></span>                                                          |
| <span data-ttu-id="9edaf-268">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9edaf-268">In Global Catalog</span></span>      | <span data-ttu-id="9edaf-269">False</span><span class="sxs-lookup"><span data-stu-id="9edaf-269">False</span></span>                                                          |
| <span data-ttu-id="9edaf-270">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9edaf-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="9edaf-271">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9edaf-271">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="9edaf-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9edaf-272">Range-Lower</span></span>            | <span data-ttu-id="9edaf-273">0</span><span class="sxs-lookup"><span data-stu-id="9edaf-273">0</span></span>                                                              |
| <span data-ttu-id="9edaf-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9edaf-274">Range-Upper</span></span>            | <span data-ttu-id="9edaf-275">16</span><span class="sxs-lookup"><span data-stu-id="9edaf-275">16</span></span>                                                             |
| <span data-ttu-id="9edaf-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9edaf-276">Search-Flags</span></span>           | <span data-ttu-id="9edaf-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9edaf-277">0x00000000</span></span>                                                     |
| <span data-ttu-id="9edaf-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9edaf-278">System-Flags</span></span>           | <span data-ttu-id="9edaf-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9edaf-279">0x00000010</span></span>                                                     |
| <span data-ttu-id="9edaf-280">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9edaf-280">Classes used in</span></span>        | [<span data-ttu-id="9edaf-281">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="9edaf-281">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





