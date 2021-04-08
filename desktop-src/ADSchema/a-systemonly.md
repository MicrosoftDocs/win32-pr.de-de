---
title: System-Only-Attribut
description: Ein boolescher Wert, der angibt, ob nur Active Directory die Klasse ändern können. Reine System Klassen können nur vom Verzeichnis System-Agent erstellt oder gelöscht werden.
ms.assetid: 78d2da1f-bdf1-452b-bc64-78088f3630dd
ms.tgt_platform: multiple
keywords:
- AD-Schema für System-Only-Attribut
- System only-Attribut AD-Schema
topic_type:
- apiref
api_name:
- System-Only
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1310eb5f13da3c17c20ac9c01f337ff2a018a545
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859565"
---
# <a name="system-only-attribute"></a><span data-ttu-id="0f112-106">System-Only-Attribut</span><span class="sxs-lookup"><span data-stu-id="0f112-106">System-Only attribute</span></span>

<span data-ttu-id="0f112-107">Ein boolescher Wert, der angibt, ob nur Active Directory die Klasse ändern können.</span><span class="sxs-lookup"><span data-stu-id="0f112-107">A Boolean value that specifies whether only Active Directory can modify the class.</span></span> <span data-ttu-id="0f112-108">Reine System Klassen können nur vom Verzeichnis System-Agent erstellt oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="0f112-108">System-only classes can only be created or deleted by the Directory System Agent.</span></span>



| <span data-ttu-id="0f112-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0f112-109">Entry</span></span> | <span data-ttu-id="0f112-110">Wert</span><span class="sxs-lookup"><span data-stu-id="0f112-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="0f112-111">CN</span><span class="sxs-lookup"><span data-stu-id="0f112-111">CN</span></span>                | <span data-ttu-id="0f112-112">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f112-112">System-Only</span></span>                          |
| <span data-ttu-id="0f112-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0f112-113">Ldap-Display-Name</span></span> | <span data-ttu-id="0f112-114">systemOnly</span><span class="sxs-lookup"><span data-stu-id="0f112-114">systemOnly</span></span>                           |
| <span data-ttu-id="0f112-115">Size</span><span class="sxs-lookup"><span data-stu-id="0f112-115">Size</span></span>              | <span data-ttu-id="0f112-116">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="0f112-116">4 bytes</span></span>                              |
| <span data-ttu-id="0f112-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="0f112-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="0f112-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="0f112-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="0f112-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0f112-119">Attribute-Id</span></span>      | <span data-ttu-id="0f112-120">1.2.840.113556.1.4.170</span><span class="sxs-lookup"><span data-stu-id="0f112-120">1.2.840.113556.1.4.170</span></span>               |
| <span data-ttu-id="0f112-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0f112-121">System-Id-Guid</span></span>    | <span data-ttu-id="0f112-122">bf967a46-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="0f112-122">bf967a46-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="0f112-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f112-123">Syntax</span></span>            | [<span data-ttu-id="0f112-124">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="0f112-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="0f112-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="0f112-125">Implementations</span></span>

-   [<span data-ttu-id="0f112-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0f112-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0f112-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0f112-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0f112-128">**Adam**</span><span class="sxs-lookup"><span data-stu-id="0f112-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="0f112-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0f112-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0f112-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0f112-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0f112-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0f112-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0f112-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0f112-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0f112-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0f112-133">Windows 2000 Server</span></span>



| <span data-ttu-id="0f112-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0f112-134">Entry</span></span> | <span data-ttu-id="0f112-135">Wert</span><span class="sxs-lookup"><span data-stu-id="0f112-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f112-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0f112-136">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0f112-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f112-137">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0f112-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f112-138">System-Only</span></span>            | <span data-ttu-id="0f112-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="0f112-139">True</span></span>                                                                                                      |
| <span data-ttu-id="0f112-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0f112-140">Is-Single-Valued</span></span>       | <span data-ttu-id="0f112-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="0f112-141">True</span></span>                                                                                                      |
| <span data-ttu-id="0f112-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0f112-142">Is Indexed</span></span>             | <span data-ttu-id="0f112-143">False</span><span class="sxs-lookup"><span data-stu-id="0f112-143">False</span></span>                                                                                                     |
| <span data-ttu-id="0f112-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0f112-144">In Global Catalog</span></span>      | <span data-ttu-id="0f112-145">False</span><span class="sxs-lookup"><span data-stu-id="0f112-145">False</span></span>                                                                                                     |
| <span data-ttu-id="0f112-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f112-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f112-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0f112-147">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="0f112-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f112-148">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="0f112-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f112-149">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="0f112-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f112-150">Search-Flags</span></span>           | <span data-ttu-id="0f112-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f112-151">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="0f112-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f112-152">System-Flags</span></span>           | <span data-ttu-id="0f112-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0f112-153">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="0f112-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0f112-154">Classes used in</span></span>        | [<span data-ttu-id="0f112-155">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="0f112-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="0f112-156">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="0f112-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0f112-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0f112-157">Windows Server 2003</span></span>



| <span data-ttu-id="0f112-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0f112-158">Entry</span></span> | <span data-ttu-id="0f112-159">Wert</span><span class="sxs-lookup"><span data-stu-id="0f112-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f112-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0f112-160">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0f112-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f112-161">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0f112-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f112-162">System-Only</span></span>            | <span data-ttu-id="0f112-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="0f112-163">True</span></span>                                                                                                      |
| <span data-ttu-id="0f112-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0f112-164">Is-Single-Valued</span></span>       | <span data-ttu-id="0f112-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="0f112-165">True</span></span>                                                                                                      |
| <span data-ttu-id="0f112-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0f112-166">Is Indexed</span></span>             | <span data-ttu-id="0f112-167">False</span><span class="sxs-lookup"><span data-stu-id="0f112-167">False</span></span>                                                                                                     |
| <span data-ttu-id="0f112-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0f112-168">In Global Catalog</span></span>      | <span data-ttu-id="0f112-169">False</span><span class="sxs-lookup"><span data-stu-id="0f112-169">False</span></span>                                                                                                     |
| <span data-ttu-id="0f112-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f112-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f112-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0f112-171">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="0f112-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f112-172">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="0f112-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f112-173">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="0f112-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f112-174">Search-Flags</span></span>           | <span data-ttu-id="0f112-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f112-175">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="0f112-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f112-176">System-Flags</span></span>           | <span data-ttu-id="0f112-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0f112-177">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="0f112-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0f112-178">Classes used in</span></span>        | [<span data-ttu-id="0f112-179">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="0f112-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="0f112-180">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="0f112-180">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="0f112-181">Adam</span><span class="sxs-lookup"><span data-stu-id="0f112-181">ADAM</span></span>



| <span data-ttu-id="0f112-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0f112-182">Entry</span></span> | <span data-ttu-id="0f112-183">Wert</span><span class="sxs-lookup"><span data-stu-id="0f112-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f112-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0f112-184">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0f112-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f112-185">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0f112-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f112-186">System-Only</span></span>            | <span data-ttu-id="0f112-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="0f112-187">True</span></span>                                                                                                      |
| <span data-ttu-id="0f112-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0f112-188">Is-Single-Valued</span></span>       | <span data-ttu-id="0f112-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="0f112-189">True</span></span>                                                                                                      |
| <span data-ttu-id="0f112-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0f112-190">Is Indexed</span></span>             | <span data-ttu-id="0f112-191">False</span><span class="sxs-lookup"><span data-stu-id="0f112-191">False</span></span>                                                                                                     |
| <span data-ttu-id="0f112-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0f112-192">In Global Catalog</span></span>      | <span data-ttu-id="0f112-193">False</span><span class="sxs-lookup"><span data-stu-id="0f112-193">False</span></span>                                                                                                     |
| <span data-ttu-id="0f112-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f112-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f112-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0f112-195">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="0f112-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f112-196">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="0f112-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f112-197">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="0f112-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f112-198">Search-Flags</span></span>           | <span data-ttu-id="0f112-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f112-199">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="0f112-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f112-200">System-Flags</span></span>           | <span data-ttu-id="0f112-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0f112-201">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="0f112-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0f112-202">Classes used in</span></span>        | [<span data-ttu-id="0f112-203">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="0f112-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="0f112-204">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="0f112-204">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0f112-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0f112-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0f112-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0f112-206">Entry</span></span> | <span data-ttu-id="0f112-207">Wert</span><span class="sxs-lookup"><span data-stu-id="0f112-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f112-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0f112-208">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0f112-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f112-209">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0f112-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f112-210">System-Only</span></span>            | <span data-ttu-id="0f112-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="0f112-211">True</span></span>                                                                                                      |
| <span data-ttu-id="0f112-212">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0f112-212">Is-Single-Valued</span></span>       | <span data-ttu-id="0f112-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="0f112-213">True</span></span>                                                                                                      |
| <span data-ttu-id="0f112-214">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0f112-214">Is Indexed</span></span>             | <span data-ttu-id="0f112-215">False</span><span class="sxs-lookup"><span data-stu-id="0f112-215">False</span></span>                                                                                                     |
| <span data-ttu-id="0f112-216">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0f112-216">In Global Catalog</span></span>      | <span data-ttu-id="0f112-217">False</span><span class="sxs-lookup"><span data-stu-id="0f112-217">False</span></span>                                                                                                     |
| <span data-ttu-id="0f112-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f112-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f112-219">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0f112-219">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="0f112-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f112-220">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="0f112-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f112-221">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="0f112-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f112-222">Search-Flags</span></span>           | <span data-ttu-id="0f112-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f112-223">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="0f112-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f112-224">System-Flags</span></span>           | <span data-ttu-id="0f112-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0f112-225">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="0f112-226">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0f112-226">Classes used in</span></span>        | [<span data-ttu-id="0f112-227">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="0f112-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="0f112-228">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="0f112-228">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0f112-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f112-229">Windows Server 2008</span></span>



| <span data-ttu-id="0f112-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0f112-230">Entry</span></span> | <span data-ttu-id="0f112-231">Wert</span><span class="sxs-lookup"><span data-stu-id="0f112-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f112-232">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0f112-232">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0f112-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f112-233">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0f112-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f112-234">System-Only</span></span>            | <span data-ttu-id="0f112-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="0f112-235">True</span></span>                                                                                                      |
| <span data-ttu-id="0f112-236">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0f112-236">Is-Single-Valued</span></span>       | <span data-ttu-id="0f112-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="0f112-237">True</span></span>                                                                                                      |
| <span data-ttu-id="0f112-238">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0f112-238">Is Indexed</span></span>             | <span data-ttu-id="0f112-239">False</span><span class="sxs-lookup"><span data-stu-id="0f112-239">False</span></span>                                                                                                     |
| <span data-ttu-id="0f112-240">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0f112-240">In Global Catalog</span></span>      | <span data-ttu-id="0f112-241">False</span><span class="sxs-lookup"><span data-stu-id="0f112-241">False</span></span>                                                                                                     |
| <span data-ttu-id="0f112-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f112-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f112-243">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0f112-243">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="0f112-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f112-244">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="0f112-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f112-245">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="0f112-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f112-246">Search-Flags</span></span>           | <span data-ttu-id="0f112-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f112-247">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="0f112-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f112-248">System-Flags</span></span>           | <span data-ttu-id="0f112-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0f112-249">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="0f112-250">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0f112-250">Classes used in</span></span>        | [<span data-ttu-id="0f112-251">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="0f112-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="0f112-252">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="0f112-252">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0f112-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0f112-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0f112-254">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0f112-254">Entry</span></span> | <span data-ttu-id="0f112-255">Wert</span><span class="sxs-lookup"><span data-stu-id="0f112-255">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f112-256">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0f112-256">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0f112-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f112-257">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0f112-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f112-258">System-Only</span></span>            | <span data-ttu-id="0f112-259">Richtig</span><span class="sxs-lookup"><span data-stu-id="0f112-259">True</span></span>                                                                                                      |
| <span data-ttu-id="0f112-260">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0f112-260">Is-Single-Valued</span></span>       | <span data-ttu-id="0f112-261">Richtig</span><span class="sxs-lookup"><span data-stu-id="0f112-261">True</span></span>                                                                                                      |
| <span data-ttu-id="0f112-262">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0f112-262">Is Indexed</span></span>             | <span data-ttu-id="0f112-263">False</span><span class="sxs-lookup"><span data-stu-id="0f112-263">False</span></span>                                                                                                     |
| <span data-ttu-id="0f112-264">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0f112-264">In Global Catalog</span></span>      | <span data-ttu-id="0f112-265">False</span><span class="sxs-lookup"><span data-stu-id="0f112-265">False</span></span>                                                                                                     |
| <span data-ttu-id="0f112-266">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f112-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f112-267">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0f112-267">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="0f112-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f112-268">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="0f112-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f112-269">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="0f112-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f112-270">Search-Flags</span></span>           | <span data-ttu-id="0f112-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f112-271">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="0f112-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f112-272">System-Flags</span></span>           | <span data-ttu-id="0f112-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0f112-273">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="0f112-274">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0f112-274">Classes used in</span></span>        | [<span data-ttu-id="0f112-275">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="0f112-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="0f112-276">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="0f112-276">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0f112-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0f112-277">Windows Server 2012</span></span>



| <span data-ttu-id="0f112-278">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0f112-278">Entry</span></span> | <span data-ttu-id="0f112-279">Wert</span><span class="sxs-lookup"><span data-stu-id="0f112-279">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f112-280">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0f112-280">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0f112-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f112-281">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0f112-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f112-282">System-Only</span></span>            | <span data-ttu-id="0f112-283">Richtig</span><span class="sxs-lookup"><span data-stu-id="0f112-283">True</span></span>                                                                                                      |
| <span data-ttu-id="0f112-284">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0f112-284">Is-Single-Valued</span></span>       | <span data-ttu-id="0f112-285">Richtig</span><span class="sxs-lookup"><span data-stu-id="0f112-285">True</span></span>                                                                                                      |
| <span data-ttu-id="0f112-286">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0f112-286">Is Indexed</span></span>             | <span data-ttu-id="0f112-287">False</span><span class="sxs-lookup"><span data-stu-id="0f112-287">False</span></span>                                                                                                     |
| <span data-ttu-id="0f112-288">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0f112-288">In Global Catalog</span></span>      | <span data-ttu-id="0f112-289">False</span><span class="sxs-lookup"><span data-stu-id="0f112-289">False</span></span>                                                                                                     |
| <span data-ttu-id="0f112-290">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f112-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f112-291">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0f112-291">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="0f112-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f112-292">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="0f112-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f112-293">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="0f112-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f112-294">Search-Flags</span></span>           | <span data-ttu-id="0f112-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f112-295">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="0f112-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f112-296">System-Flags</span></span>           | <span data-ttu-id="0f112-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0f112-297">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="0f112-298">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0f112-298">Classes used in</span></span>        | [<span data-ttu-id="0f112-299">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="0f112-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="0f112-300">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="0f112-300">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





