---
title: Max-Storage-Attribut
description: Die maximale Menge an Speicherplatz, die der Benutzer verwenden kann. Verwenden Sie den in Benutzer \_ maxstorage unbegrenzt angegebenen Wert \_ , um den gesamten verfügbaren Speicherplatz zu verwenden.
ms.assetid: 69302641-ecfc-4b0f-81f8-f69b48c6faa7
ms.tgt_platform: multiple
keywords:
- AD-Schema für Max-Storage-Attribut
- maxstorage-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Max-Storage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac6caff3f85de7073818096324445b63a3c1c9be
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859719"
---
# <a name="max-storage-attribute"></a><span data-ttu-id="291fb-106">Max-Storage-Attribut</span><span class="sxs-lookup"><span data-stu-id="291fb-106">Max-Storage attribute</span></span>

<span data-ttu-id="291fb-107">Die maximale Menge an Speicherplatz, die der Benutzer verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="291fb-107">The maximum amount of disk space the user can use.</span></span> <span data-ttu-id="291fb-108">Verwenden Sie den in Benutzer \_ maxstorage unbegrenzt angegebenen Wert \_ , um den gesamten verfügbaren Speicherplatz zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="291fb-108">Use the value specified in USER\_MAXSTORAGE\_UNLIMITED to use all available disk space.</span></span>



| <span data-ttu-id="291fb-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="291fb-109">Entry</span></span> | <span data-ttu-id="291fb-110">Wert</span><span class="sxs-lookup"><span data-stu-id="291fb-110">Value</span></span> |
|-------------------|------------------------------------------------------------|
| <span data-ttu-id="291fb-111">CN</span><span class="sxs-lookup"><span data-stu-id="291fb-111">CN</span></span>                | <span data-ttu-id="291fb-112">Max-Storage</span><span class="sxs-lookup"><span data-stu-id="291fb-112">Max-Storage</span></span>                                                |
| <span data-ttu-id="291fb-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="291fb-113">Ldap-Display-Name</span></span> | <span data-ttu-id="291fb-114">maxstorage</span><span class="sxs-lookup"><span data-stu-id="291fb-114">maxStorage</span></span>                                                 |
| <span data-ttu-id="291fb-115">Size</span><span class="sxs-lookup"><span data-stu-id="291fb-115">Size</span></span>              | <span data-ttu-id="291fb-116">8 Bytes: Benutzer \_ maxstorage \_ unbegrenzt ((unsigned long)-1L)</span><span class="sxs-lookup"><span data-stu-id="291fb-116">8 bytes: USER\_MAXSTORAGE\_UNLIMITED ((unsigned long) -1L)</span></span> |
| <span data-ttu-id="291fb-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="291fb-117">Update Privilege</span></span>  | <span data-ttu-id="291fb-118">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="291fb-118">Domain administrator</span></span>                                       |
| <span data-ttu-id="291fb-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="291fb-119">Update Frequency</span></span>  | <span data-ttu-id="291fb-120">Jedes Mal, wenn das Datenträger Kontingent geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="291fb-120">Whenever the disk quota needs to change.</span></span>                   |
| <span data-ttu-id="291fb-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="291fb-121">Attribute-Id</span></span>      | <span data-ttu-id="291fb-122">1.2.840.113556.1.4.76</span><span class="sxs-lookup"><span data-stu-id="291fb-122">1.2.840.113556.1.4.76</span></span>                                      |
| <span data-ttu-id="291fb-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="291fb-123">System-Id-Guid</span></span>    | <span data-ttu-id="291fb-124">bf9679bd-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="291fb-124">bf9679bd-0de6-11d0-a285-00aa003049e2</span></span>                       |
| <span data-ttu-id="291fb-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="291fb-125">Syntax</span></span>            | [<span data-ttu-id="291fb-126">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="291fb-126">**Interval**</span></span>](s-interval.md)                             |



## <a name="implementations"></a><span data-ttu-id="291fb-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="291fb-127">Implementations</span></span>

-   [<span data-ttu-id="291fb-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="291fb-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="291fb-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="291fb-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="291fb-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="291fb-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="291fb-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="291fb-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="291fb-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="291fb-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="291fb-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="291fb-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="291fb-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="291fb-134">Windows 2000 Server</span></span>



| <span data-ttu-id="291fb-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="291fb-135">Entry</span></span> | <span data-ttu-id="291fb-136">Wert</span><span class="sxs-lookup"><span data-stu-id="291fb-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="291fb-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="291fb-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="291fb-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="291fb-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="291fb-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="291fb-139">System-Only</span></span>            | <span data-ttu-id="291fb-140">False</span><span class="sxs-lookup"><span data-stu-id="291fb-140">False</span></span>                             |
| <span data-ttu-id="291fb-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="291fb-141">Is-Single-Valued</span></span>       | <span data-ttu-id="291fb-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="291fb-142">True</span></span>                              |
| <span data-ttu-id="291fb-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="291fb-143">Is Indexed</span></span>             | <span data-ttu-id="291fb-144">False</span><span class="sxs-lookup"><span data-stu-id="291fb-144">False</span></span>                             |
| <span data-ttu-id="291fb-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="291fb-145">In Global Catalog</span></span>      | <span data-ttu-id="291fb-146">False</span><span class="sxs-lookup"><span data-stu-id="291fb-146">False</span></span>                             |
| <span data-ttu-id="291fb-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="291fb-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="291fb-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="291fb-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="291fb-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="291fb-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="291fb-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="291fb-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="291fb-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="291fb-151">Search-Flags</span></span>           | <span data-ttu-id="291fb-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="291fb-152">0x00000010</span></span>                        |
| <span data-ttu-id="291fb-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="291fb-153">System-Flags</span></span>           | <span data-ttu-id="291fb-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="291fb-154">0x00000010</span></span>                        |
| <span data-ttu-id="291fb-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="291fb-155">Classes used in</span></span>        | [<span data-ttu-id="291fb-156">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="291fb-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="291fb-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="291fb-157">Windows Server 2003</span></span>



| <span data-ttu-id="291fb-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="291fb-158">Entry</span></span> | <span data-ttu-id="291fb-159">Wert</span><span class="sxs-lookup"><span data-stu-id="291fb-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="291fb-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="291fb-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="291fb-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="291fb-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="291fb-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="291fb-162">System-Only</span></span>            | <span data-ttu-id="291fb-163">False</span><span class="sxs-lookup"><span data-stu-id="291fb-163">False</span></span>                             |
| <span data-ttu-id="291fb-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="291fb-164">Is-Single-Valued</span></span>       | <span data-ttu-id="291fb-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="291fb-165">True</span></span>                              |
| <span data-ttu-id="291fb-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="291fb-166">Is Indexed</span></span>             | <span data-ttu-id="291fb-167">False</span><span class="sxs-lookup"><span data-stu-id="291fb-167">False</span></span>                             |
| <span data-ttu-id="291fb-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="291fb-168">In Global Catalog</span></span>      | <span data-ttu-id="291fb-169">False</span><span class="sxs-lookup"><span data-stu-id="291fb-169">False</span></span>                             |
| <span data-ttu-id="291fb-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="291fb-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="291fb-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="291fb-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="291fb-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="291fb-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="291fb-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="291fb-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="291fb-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="291fb-174">Search-Flags</span></span>           | <span data-ttu-id="291fb-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="291fb-175">0x00000010</span></span>                        |
| <span data-ttu-id="291fb-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="291fb-176">System-Flags</span></span>           | <span data-ttu-id="291fb-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="291fb-177">0x00000010</span></span>                        |
| <span data-ttu-id="291fb-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="291fb-178">Classes used in</span></span>        | [<span data-ttu-id="291fb-179">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="291fb-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="291fb-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="291fb-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="291fb-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="291fb-181">Entry</span></span> | <span data-ttu-id="291fb-182">Wert</span><span class="sxs-lookup"><span data-stu-id="291fb-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="291fb-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="291fb-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="291fb-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="291fb-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="291fb-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="291fb-185">System-Only</span></span>            | <span data-ttu-id="291fb-186">False</span><span class="sxs-lookup"><span data-stu-id="291fb-186">False</span></span>                             |
| <span data-ttu-id="291fb-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="291fb-187">Is-Single-Valued</span></span>       | <span data-ttu-id="291fb-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="291fb-188">True</span></span>                              |
| <span data-ttu-id="291fb-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="291fb-189">Is Indexed</span></span>             | <span data-ttu-id="291fb-190">False</span><span class="sxs-lookup"><span data-stu-id="291fb-190">False</span></span>                             |
| <span data-ttu-id="291fb-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="291fb-191">In Global Catalog</span></span>      | <span data-ttu-id="291fb-192">False</span><span class="sxs-lookup"><span data-stu-id="291fb-192">False</span></span>                             |
| <span data-ttu-id="291fb-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="291fb-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="291fb-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="291fb-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="291fb-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="291fb-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="291fb-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="291fb-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="291fb-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="291fb-197">Search-Flags</span></span>           | <span data-ttu-id="291fb-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="291fb-198">0x00000010</span></span>                        |
| <span data-ttu-id="291fb-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="291fb-199">System-Flags</span></span>           | <span data-ttu-id="291fb-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="291fb-200">0x00000010</span></span>                        |
| <span data-ttu-id="291fb-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="291fb-201">Classes used in</span></span>        | [<span data-ttu-id="291fb-202">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="291fb-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="291fb-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="291fb-203">Windows Server 2008</span></span>



| <span data-ttu-id="291fb-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="291fb-204">Entry</span></span> | <span data-ttu-id="291fb-205">Wert</span><span class="sxs-lookup"><span data-stu-id="291fb-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="291fb-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="291fb-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="291fb-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="291fb-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="291fb-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="291fb-208">System-Only</span></span>            | <span data-ttu-id="291fb-209">False</span><span class="sxs-lookup"><span data-stu-id="291fb-209">False</span></span>                             |
| <span data-ttu-id="291fb-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="291fb-210">Is-Single-Valued</span></span>       | <span data-ttu-id="291fb-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="291fb-211">True</span></span>                              |
| <span data-ttu-id="291fb-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="291fb-212">Is Indexed</span></span>             | <span data-ttu-id="291fb-213">False</span><span class="sxs-lookup"><span data-stu-id="291fb-213">False</span></span>                             |
| <span data-ttu-id="291fb-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="291fb-214">In Global Catalog</span></span>      | <span data-ttu-id="291fb-215">False</span><span class="sxs-lookup"><span data-stu-id="291fb-215">False</span></span>                             |
| <span data-ttu-id="291fb-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="291fb-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="291fb-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="291fb-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="291fb-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="291fb-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="291fb-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="291fb-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="291fb-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="291fb-220">Search-Flags</span></span>           | <span data-ttu-id="291fb-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="291fb-221">0x00000010</span></span>                        |
| <span data-ttu-id="291fb-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="291fb-222">System-Flags</span></span>           | <span data-ttu-id="291fb-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="291fb-223">0x00000010</span></span>                        |
| <span data-ttu-id="291fb-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="291fb-224">Classes used in</span></span>        | [<span data-ttu-id="291fb-225">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="291fb-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="291fb-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="291fb-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="291fb-227">Eingabe</span><span class="sxs-lookup"><span data-stu-id="291fb-227">Entry</span></span> | <span data-ttu-id="291fb-228">Wert</span><span class="sxs-lookup"><span data-stu-id="291fb-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="291fb-229">Link-ID</span><span class="sxs-lookup"><span data-stu-id="291fb-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="291fb-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="291fb-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="291fb-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="291fb-231">System-Only</span></span>            | <span data-ttu-id="291fb-232">False</span><span class="sxs-lookup"><span data-stu-id="291fb-232">False</span></span>                             |
| <span data-ttu-id="291fb-233">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="291fb-233">Is-Single-Valued</span></span>       | <span data-ttu-id="291fb-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="291fb-234">True</span></span>                              |
| <span data-ttu-id="291fb-235">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="291fb-235">Is Indexed</span></span>             | <span data-ttu-id="291fb-236">False</span><span class="sxs-lookup"><span data-stu-id="291fb-236">False</span></span>                             |
| <span data-ttu-id="291fb-237">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="291fb-237">In Global Catalog</span></span>      | <span data-ttu-id="291fb-238">False</span><span class="sxs-lookup"><span data-stu-id="291fb-238">False</span></span>                             |
| <span data-ttu-id="291fb-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="291fb-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="291fb-240">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="291fb-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="291fb-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="291fb-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="291fb-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="291fb-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="291fb-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="291fb-243">Search-Flags</span></span>           | <span data-ttu-id="291fb-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="291fb-244">0x00000010</span></span>                        |
| <span data-ttu-id="291fb-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="291fb-245">System-Flags</span></span>           | <span data-ttu-id="291fb-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="291fb-246">0x00000010</span></span>                        |
| <span data-ttu-id="291fb-247">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="291fb-247">Classes used in</span></span>        | [<span data-ttu-id="291fb-248">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="291fb-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="291fb-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="291fb-249">Windows Server 2012</span></span>



| <span data-ttu-id="291fb-250">Eingabe</span><span class="sxs-lookup"><span data-stu-id="291fb-250">Entry</span></span> | <span data-ttu-id="291fb-251">Wert</span><span class="sxs-lookup"><span data-stu-id="291fb-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="291fb-252">Link-ID</span><span class="sxs-lookup"><span data-stu-id="291fb-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="291fb-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="291fb-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="291fb-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="291fb-254">System-Only</span></span>            | <span data-ttu-id="291fb-255">False</span><span class="sxs-lookup"><span data-stu-id="291fb-255">False</span></span>                             |
| <span data-ttu-id="291fb-256">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="291fb-256">Is-Single-Valued</span></span>       | <span data-ttu-id="291fb-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="291fb-257">True</span></span>                              |
| <span data-ttu-id="291fb-258">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="291fb-258">Is Indexed</span></span>             | <span data-ttu-id="291fb-259">False</span><span class="sxs-lookup"><span data-stu-id="291fb-259">False</span></span>                             |
| <span data-ttu-id="291fb-260">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="291fb-260">In Global Catalog</span></span>      | <span data-ttu-id="291fb-261">False</span><span class="sxs-lookup"><span data-stu-id="291fb-261">False</span></span>                             |
| <span data-ttu-id="291fb-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="291fb-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="291fb-263">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="291fb-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="291fb-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="291fb-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="291fb-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="291fb-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="291fb-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="291fb-266">Search-Flags</span></span>           | <span data-ttu-id="291fb-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="291fb-267">0x00000010</span></span>                        |
| <span data-ttu-id="291fb-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="291fb-268">System-Flags</span></span>           | <span data-ttu-id="291fb-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="291fb-269">0x00000010</span></span>                        |
| <span data-ttu-id="291fb-270">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="291fb-270">Classes used in</span></span>        | [<span data-ttu-id="291fb-271">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="291fb-271">**User**</span></span>](c-user.md)<br/> |



 

 





