---
title: OMT-Guid-Attribut
description: Der eindeutige Bezeichner für einen Link-Track-Object-Move-Tabelleneintrag.
ms.assetid: c8266178-4d0d-46d6-8fd9-d0c11c11c036
ms.tgt_platform: multiple
keywords:
- AD-Schema für OMT-Guid-Attribut
- omtguid-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- OMT-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379cdf49a6ee1a467a0e5120e841e4d2179447be
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346573"
---
# <a name="omt-guid-attribute"></a><span data-ttu-id="04021-105">OMT-Guid-Attribut</span><span class="sxs-lookup"><span data-stu-id="04021-105">OMT-Guid attribute</span></span>

<span data-ttu-id="04021-106">Der eindeutige Bezeichner für einen Link-Track-Object-Move-Tabelleneintrag.</span><span class="sxs-lookup"><span data-stu-id="04021-106">The unique identifier for a Link-Track-Object-Move table entry.</span></span>



| <span data-ttu-id="04021-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04021-107">Entry</span></span> | <span data-ttu-id="04021-108">Wert</span><span class="sxs-lookup"><span data-stu-id="04021-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="04021-109">CN</span><span class="sxs-lookup"><span data-stu-id="04021-109">CN</span></span>                | <span data-ttu-id="04021-110">OMT-Guid</span><span class="sxs-lookup"><span data-stu-id="04021-110">OMT-Guid</span></span>                                              |
| <span data-ttu-id="04021-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="04021-111">Ldap-Display-Name</span></span> | <span data-ttu-id="04021-112">omtguid</span><span class="sxs-lookup"><span data-stu-id="04021-112">oMTGuid</span></span>                                               |
| <span data-ttu-id="04021-113">Size</span><span class="sxs-lookup"><span data-stu-id="04021-113">Size</span></span>              | <span data-ttu-id="04021-114">16 Bytes</span><span class="sxs-lookup"><span data-stu-id="04021-114">16 bytes</span></span>                                              |
| <span data-ttu-id="04021-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="04021-115">Update Privilege</span></span>  | <span data-ttu-id="04021-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="04021-116">This value is set by the system.</span></span>                      |
| <span data-ttu-id="04021-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="04021-117">Update Frequency</span></span>  | <span data-ttu-id="04021-118">Jedes Mal, wenn sich der Link für eine Datei ändert.</span><span class="sxs-lookup"><span data-stu-id="04021-118">Whenever the link for a file changes.</span></span>                 |
| <span data-ttu-id="04021-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="04021-119">Attribute-Id</span></span>      | <span data-ttu-id="04021-120">1.2.840.113556.1.4.505</span><span class="sxs-lookup"><span data-stu-id="04021-120">1.2.840.113556.1.4.505</span></span>                                |
| <span data-ttu-id="04021-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="04021-121">System-Id-Guid</span></span>    | <span data-ttu-id="04021-122">ddac0cf3-af8f-11d0-afeb-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="04021-122">ddac0cf3-af8f-11d0-afeb-00c04fd930c9</span></span>                  |
| <span data-ttu-id="04021-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="04021-123">Syntax</span></span>            | [<span data-ttu-id="04021-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="04021-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="04021-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="04021-125">Implementations</span></span>

-   [<span data-ttu-id="04021-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="04021-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="04021-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="04021-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="04021-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="04021-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="04021-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="04021-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="04021-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="04021-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="04021-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="04021-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="04021-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="04021-132">Windows 2000 Server</span></span>



| <span data-ttu-id="04021-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04021-133">Entry</span></span> | <span data-ttu-id="04021-134">Wert</span><span class="sxs-lookup"><span data-stu-id="04021-134">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="04021-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04021-135">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="04021-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04021-136">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="04021-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="04021-137">System-Only</span></span>            | <span data-ttu-id="04021-138">False</span><span class="sxs-lookup"><span data-stu-id="04021-138">False</span></span>                                                          |
| <span data-ttu-id="04021-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04021-139">Is-Single-Valued</span></span>       | <span data-ttu-id="04021-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="04021-140">True</span></span>                                                           |
| <span data-ttu-id="04021-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04021-141">Is Indexed</span></span>             | <span data-ttu-id="04021-142">False</span><span class="sxs-lookup"><span data-stu-id="04021-142">False</span></span>                                                          |
| <span data-ttu-id="04021-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04021-143">In Global Catalog</span></span>      | <span data-ttu-id="04021-144">False</span><span class="sxs-lookup"><span data-stu-id="04021-144">False</span></span>                                                          |
| <span data-ttu-id="04021-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04021-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="04021-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04021-146">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="04021-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04021-147">Range-Lower</span></span>            | <span data-ttu-id="04021-148">0</span><span class="sxs-lookup"><span data-stu-id="04021-148">0</span></span>                                                              |
| <span data-ttu-id="04021-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04021-149">Range-Upper</span></span>            | <span data-ttu-id="04021-150">16</span><span class="sxs-lookup"><span data-stu-id="04021-150">16</span></span>                                                             |
| <span data-ttu-id="04021-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04021-151">Search-Flags</span></span>           | <span data-ttu-id="04021-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04021-152">0x00000000</span></span>                                                     |
| <span data-ttu-id="04021-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04021-153">System-Flags</span></span>           | <span data-ttu-id="04021-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04021-154">0x00000010</span></span>                                                     |
| <span data-ttu-id="04021-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04021-155">Classes used in</span></span>        | [<span data-ttu-id="04021-156">**Link-Track-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="04021-156">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="04021-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="04021-157">Windows Server 2003</span></span>



| <span data-ttu-id="04021-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04021-158">Entry</span></span> | <span data-ttu-id="04021-159">Wert</span><span class="sxs-lookup"><span data-stu-id="04021-159">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="04021-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04021-160">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="04021-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04021-161">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="04021-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="04021-162">System-Only</span></span>            | <span data-ttu-id="04021-163">False</span><span class="sxs-lookup"><span data-stu-id="04021-163">False</span></span>                                                          |
| <span data-ttu-id="04021-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04021-164">Is-Single-Valued</span></span>       | <span data-ttu-id="04021-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="04021-165">True</span></span>                                                           |
| <span data-ttu-id="04021-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04021-166">Is Indexed</span></span>             | <span data-ttu-id="04021-167">False</span><span class="sxs-lookup"><span data-stu-id="04021-167">False</span></span>                                                          |
| <span data-ttu-id="04021-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04021-168">In Global Catalog</span></span>      | <span data-ttu-id="04021-169">False</span><span class="sxs-lookup"><span data-stu-id="04021-169">False</span></span>                                                          |
| <span data-ttu-id="04021-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04021-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="04021-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04021-171">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="04021-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04021-172">Range-Lower</span></span>            | <span data-ttu-id="04021-173">0</span><span class="sxs-lookup"><span data-stu-id="04021-173">0</span></span>                                                              |
| <span data-ttu-id="04021-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04021-174">Range-Upper</span></span>            | <span data-ttu-id="04021-175">16</span><span class="sxs-lookup"><span data-stu-id="04021-175">16</span></span>                                                             |
| <span data-ttu-id="04021-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04021-176">Search-Flags</span></span>           | <span data-ttu-id="04021-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04021-177">0x00000000</span></span>                                                     |
| <span data-ttu-id="04021-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04021-178">System-Flags</span></span>           | <span data-ttu-id="04021-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04021-179">0x00000010</span></span>                                                     |
| <span data-ttu-id="04021-180">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04021-180">Classes used in</span></span>        | [<span data-ttu-id="04021-181">**Link-Track-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="04021-181">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="04021-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="04021-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="04021-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04021-183">Entry</span></span> | <span data-ttu-id="04021-184">Wert</span><span class="sxs-lookup"><span data-stu-id="04021-184">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="04021-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04021-185">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="04021-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04021-186">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="04021-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="04021-187">System-Only</span></span>            | <span data-ttu-id="04021-188">False</span><span class="sxs-lookup"><span data-stu-id="04021-188">False</span></span>                                                          |
| <span data-ttu-id="04021-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04021-189">Is-Single-Valued</span></span>       | <span data-ttu-id="04021-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="04021-190">True</span></span>                                                           |
| <span data-ttu-id="04021-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04021-191">Is Indexed</span></span>             | <span data-ttu-id="04021-192">False</span><span class="sxs-lookup"><span data-stu-id="04021-192">False</span></span>                                                          |
| <span data-ttu-id="04021-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04021-193">In Global Catalog</span></span>      | <span data-ttu-id="04021-194">False</span><span class="sxs-lookup"><span data-stu-id="04021-194">False</span></span>                                                          |
| <span data-ttu-id="04021-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04021-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="04021-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04021-196">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="04021-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04021-197">Range-Lower</span></span>            | <span data-ttu-id="04021-198">0</span><span class="sxs-lookup"><span data-stu-id="04021-198">0</span></span>                                                              |
| <span data-ttu-id="04021-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04021-199">Range-Upper</span></span>            | <span data-ttu-id="04021-200">16</span><span class="sxs-lookup"><span data-stu-id="04021-200">16</span></span>                                                             |
| <span data-ttu-id="04021-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04021-201">Search-Flags</span></span>           | <span data-ttu-id="04021-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04021-202">0x00000000</span></span>                                                     |
| <span data-ttu-id="04021-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04021-203">System-Flags</span></span>           | <span data-ttu-id="04021-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04021-204">0x00000010</span></span>                                                     |
| <span data-ttu-id="04021-205">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04021-205">Classes used in</span></span>        | [<span data-ttu-id="04021-206">**Link-Track-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="04021-206">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="04021-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04021-207">Windows Server 2008</span></span>



| <span data-ttu-id="04021-208">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04021-208">Entry</span></span> | <span data-ttu-id="04021-209">Wert</span><span class="sxs-lookup"><span data-stu-id="04021-209">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="04021-210">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04021-210">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="04021-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04021-211">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="04021-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="04021-212">System-Only</span></span>            | <span data-ttu-id="04021-213">False</span><span class="sxs-lookup"><span data-stu-id="04021-213">False</span></span>                                                          |
| <span data-ttu-id="04021-214">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04021-214">Is-Single-Valued</span></span>       | <span data-ttu-id="04021-215">Richtig</span><span class="sxs-lookup"><span data-stu-id="04021-215">True</span></span>                                                           |
| <span data-ttu-id="04021-216">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04021-216">Is Indexed</span></span>             | <span data-ttu-id="04021-217">False</span><span class="sxs-lookup"><span data-stu-id="04021-217">False</span></span>                                                          |
| <span data-ttu-id="04021-218">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04021-218">In Global Catalog</span></span>      | <span data-ttu-id="04021-219">False</span><span class="sxs-lookup"><span data-stu-id="04021-219">False</span></span>                                                          |
| <span data-ttu-id="04021-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04021-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="04021-221">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04021-221">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="04021-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04021-222">Range-Lower</span></span>            | <span data-ttu-id="04021-223">0</span><span class="sxs-lookup"><span data-stu-id="04021-223">0</span></span>                                                              |
| <span data-ttu-id="04021-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04021-224">Range-Upper</span></span>            | <span data-ttu-id="04021-225">16</span><span class="sxs-lookup"><span data-stu-id="04021-225">16</span></span>                                                             |
| <span data-ttu-id="04021-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04021-226">Search-Flags</span></span>           | <span data-ttu-id="04021-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04021-227">0x00000000</span></span>                                                     |
| <span data-ttu-id="04021-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04021-228">System-Flags</span></span>           | <span data-ttu-id="04021-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04021-229">0x00000010</span></span>                                                     |
| <span data-ttu-id="04021-230">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04021-230">Classes used in</span></span>        | [<span data-ttu-id="04021-231">**Link-Track-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="04021-231">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="04021-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="04021-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="04021-233">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04021-233">Entry</span></span> | <span data-ttu-id="04021-234">Wert</span><span class="sxs-lookup"><span data-stu-id="04021-234">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="04021-235">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04021-235">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="04021-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04021-236">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="04021-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="04021-237">System-Only</span></span>            | <span data-ttu-id="04021-238">False</span><span class="sxs-lookup"><span data-stu-id="04021-238">False</span></span>                                                          |
| <span data-ttu-id="04021-239">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04021-239">Is-Single-Valued</span></span>       | <span data-ttu-id="04021-240">Richtig</span><span class="sxs-lookup"><span data-stu-id="04021-240">True</span></span>                                                           |
| <span data-ttu-id="04021-241">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04021-241">Is Indexed</span></span>             | <span data-ttu-id="04021-242">False</span><span class="sxs-lookup"><span data-stu-id="04021-242">False</span></span>                                                          |
| <span data-ttu-id="04021-243">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04021-243">In Global Catalog</span></span>      | <span data-ttu-id="04021-244">False</span><span class="sxs-lookup"><span data-stu-id="04021-244">False</span></span>                                                          |
| <span data-ttu-id="04021-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04021-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="04021-246">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04021-246">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="04021-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04021-247">Range-Lower</span></span>            | <span data-ttu-id="04021-248">0</span><span class="sxs-lookup"><span data-stu-id="04021-248">0</span></span>                                                              |
| <span data-ttu-id="04021-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04021-249">Range-Upper</span></span>            | <span data-ttu-id="04021-250">16</span><span class="sxs-lookup"><span data-stu-id="04021-250">16</span></span>                                                             |
| <span data-ttu-id="04021-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04021-251">Search-Flags</span></span>           | <span data-ttu-id="04021-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04021-252">0x00000000</span></span>                                                     |
| <span data-ttu-id="04021-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04021-253">System-Flags</span></span>           | <span data-ttu-id="04021-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04021-254">0x00000010</span></span>                                                     |
| <span data-ttu-id="04021-255">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04021-255">Classes used in</span></span>        | [<span data-ttu-id="04021-256">**Link-Track-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="04021-256">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="04021-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="04021-257">Windows Server 2012</span></span>



| <span data-ttu-id="04021-258">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04021-258">Entry</span></span> | <span data-ttu-id="04021-259">Wert</span><span class="sxs-lookup"><span data-stu-id="04021-259">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="04021-260">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04021-260">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="04021-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04021-261">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="04021-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="04021-262">System-Only</span></span>            | <span data-ttu-id="04021-263">False</span><span class="sxs-lookup"><span data-stu-id="04021-263">False</span></span>                                                          |
| <span data-ttu-id="04021-264">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04021-264">Is-Single-Valued</span></span>       | <span data-ttu-id="04021-265">Richtig</span><span class="sxs-lookup"><span data-stu-id="04021-265">True</span></span>                                                           |
| <span data-ttu-id="04021-266">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04021-266">Is Indexed</span></span>             | <span data-ttu-id="04021-267">False</span><span class="sxs-lookup"><span data-stu-id="04021-267">False</span></span>                                                          |
| <span data-ttu-id="04021-268">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04021-268">In Global Catalog</span></span>      | <span data-ttu-id="04021-269">False</span><span class="sxs-lookup"><span data-stu-id="04021-269">False</span></span>                                                          |
| <span data-ttu-id="04021-270">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04021-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="04021-271">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04021-271">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="04021-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04021-272">Range-Lower</span></span>            | <span data-ttu-id="04021-273">0</span><span class="sxs-lookup"><span data-stu-id="04021-273">0</span></span>                                                              |
| <span data-ttu-id="04021-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04021-274">Range-Upper</span></span>            | <span data-ttu-id="04021-275">16</span><span class="sxs-lookup"><span data-stu-id="04021-275">16</span></span>                                                             |
| <span data-ttu-id="04021-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04021-276">Search-Flags</span></span>           | <span data-ttu-id="04021-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04021-277">0x00000000</span></span>                                                     |
| <span data-ttu-id="04021-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04021-278">System-Flags</span></span>           | <span data-ttu-id="04021-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04021-279">0x00000010</span></span>                                                     |
| <span data-ttu-id="04021-280">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04021-280">Classes used in</span></span>        | [<span data-ttu-id="04021-281">**Link-Track-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="04021-281">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



 

 





