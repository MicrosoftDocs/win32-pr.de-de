---
title: Is-Defunct-Attribut
description: TRUE gibt an, dass die Klasse oder das Attribut nicht mehr verwendet werden kann. Alte Versionen dieses Objekts können vorhanden sein, es können jedoch keine neuen Versionen erstellt werden.
ms.assetid: ca1b7701-e501-424d-9c07-20835b23dcd3
ms.tgt_platform: multiple
keywords:
- AD-Schema für Is-Defunct-Attribut
- AD-Schema des isaußerfunct-Attributs
topic_type:
- apiref
api_name:
- Is-Defunct
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c895a4af5d02c76a709607753065b6e965966bb6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106341071"
---
# <a name="is-defunct-attribute"></a><span data-ttu-id="b713a-106">Is-Defunct-Attribut</span><span class="sxs-lookup"><span data-stu-id="b713a-106">Is-Defunct attribute</span></span>

<span data-ttu-id="b713a-107">**True** gibt an, dass die Klasse oder das Attribut nicht mehr verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b713a-107">If **TRUE**, the class or attribute is no longer usable.</span></span> <span data-ttu-id="b713a-108">Alte Versionen dieses Objekts können vorhanden sein, es können jedoch keine neuen Versionen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b713a-108">Old versions of this object may exist, but new ones cannot be created.</span></span>



| <span data-ttu-id="b713a-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b713a-109">Entry</span></span> | <span data-ttu-id="b713a-110">Wert</span><span class="sxs-lookup"><span data-stu-id="b713a-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b713a-111">CN</span><span class="sxs-lookup"><span data-stu-id="b713a-111">CN</span></span>                | <span data-ttu-id="b713a-112">Is-Defunct</span><span class="sxs-lookup"><span data-stu-id="b713a-112">Is-Defunct</span></span>                           |
| <span data-ttu-id="b713a-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b713a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b713a-114">isDefunct</span><span class="sxs-lookup"><span data-stu-id="b713a-114">isDefunct</span></span>                            |
| <span data-ttu-id="b713a-115">Size</span><span class="sxs-lookup"><span data-stu-id="b713a-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="b713a-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b713a-116">Update Privilege</span></span>  | <span data-ttu-id="b713a-117">Schema Administrator</span><span class="sxs-lookup"><span data-stu-id="b713a-117">Schema administrator</span></span>                 |
| <span data-ttu-id="b713a-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="b713a-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b713a-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b713a-119">Attribute-Id</span></span>      | <span data-ttu-id="b713a-120">1.2.840.113556.1.4.661</span><span class="sxs-lookup"><span data-stu-id="b713a-120">1.2.840.113556.1.4.661</span></span>               |
| <span data-ttu-id="b713a-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b713a-121">System-Id-Guid</span></span>    | <span data-ttu-id="b713a-122">28630ebe-41d5-11d1-a9c1-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="b713a-122">28630ebe-41d5-11d1-a9c1-0000f80367c1</span></span> |
| <span data-ttu-id="b713a-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="b713a-123">Syntax</span></span>            | [<span data-ttu-id="b713a-124">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="b713a-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="b713a-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="b713a-125">Implementations</span></span>

-   [<span data-ttu-id="b713a-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b713a-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b713a-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b713a-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b713a-128">**Adam**</span><span class="sxs-lookup"><span data-stu-id="b713a-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b713a-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b713a-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b713a-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b713a-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b713a-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b713a-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b713a-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b713a-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b713a-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b713a-133">Windows 2000 Server</span></span>



| <span data-ttu-id="b713a-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b713a-134">Entry</span></span> | <span data-ttu-id="b713a-135">Wert</span><span class="sxs-lookup"><span data-stu-id="b713a-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b713a-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b713a-136">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="b713a-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b713a-137">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="b713a-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="b713a-138">System-Only</span></span>            | <span data-ttu-id="b713a-139">False</span><span class="sxs-lookup"><span data-stu-id="b713a-139">False</span></span>                                                                                                     |
| <span data-ttu-id="b713a-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b713a-140">Is-Single-Valued</span></span>       | <span data-ttu-id="b713a-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="b713a-141">True</span></span>                                                                                                      |
| <span data-ttu-id="b713a-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b713a-142">Is Indexed</span></span>             | <span data-ttu-id="b713a-143">False</span><span class="sxs-lookup"><span data-stu-id="b713a-143">False</span></span>                                                                                                     |
| <span data-ttu-id="b713a-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b713a-144">In Global Catalog</span></span>      | <span data-ttu-id="b713a-145">False</span><span class="sxs-lookup"><span data-stu-id="b713a-145">False</span></span>                                                                                                     |
| <span data-ttu-id="b713a-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b713a-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="b713a-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b713a-147">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="b713a-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b713a-148">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="b713a-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b713a-149">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="b713a-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b713a-150">Search-Flags</span></span>           | <span data-ttu-id="b713a-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b713a-151">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="b713a-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b713a-152">System-Flags</span></span>           | <span data-ttu-id="b713a-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b713a-153">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="b713a-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b713a-154">Classes used in</span></span>        | [<span data-ttu-id="b713a-155">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="b713a-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="b713a-156">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="b713a-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b713a-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b713a-157">Windows Server 2003</span></span>



| <span data-ttu-id="b713a-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b713a-158">Entry</span></span> | <span data-ttu-id="b713a-159">Wert</span><span class="sxs-lookup"><span data-stu-id="b713a-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b713a-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b713a-160">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="b713a-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b713a-161">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="b713a-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="b713a-162">System-Only</span></span>            | <span data-ttu-id="b713a-163">False</span><span class="sxs-lookup"><span data-stu-id="b713a-163">False</span></span>                                                                                                     |
| <span data-ttu-id="b713a-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b713a-164">Is-Single-Valued</span></span>       | <span data-ttu-id="b713a-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="b713a-165">True</span></span>                                                                                                      |
| <span data-ttu-id="b713a-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b713a-166">Is Indexed</span></span>             | <span data-ttu-id="b713a-167">False</span><span class="sxs-lookup"><span data-stu-id="b713a-167">False</span></span>                                                                                                     |
| <span data-ttu-id="b713a-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b713a-168">In Global Catalog</span></span>      | <span data-ttu-id="b713a-169">False</span><span class="sxs-lookup"><span data-stu-id="b713a-169">False</span></span>                                                                                                     |
| <span data-ttu-id="b713a-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b713a-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="b713a-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b713a-171">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="b713a-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b713a-172">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="b713a-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b713a-173">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="b713a-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b713a-174">Search-Flags</span></span>           | <span data-ttu-id="b713a-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b713a-175">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="b713a-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b713a-176">System-Flags</span></span>           | <span data-ttu-id="b713a-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b713a-177">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="b713a-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b713a-178">Classes used in</span></span>        | [<span data-ttu-id="b713a-179">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="b713a-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="b713a-180">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="b713a-180">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b713a-181">Adam</span><span class="sxs-lookup"><span data-stu-id="b713a-181">ADAM</span></span>



| <span data-ttu-id="b713a-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b713a-182">Entry</span></span> | <span data-ttu-id="b713a-183">Wert</span><span class="sxs-lookup"><span data-stu-id="b713a-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b713a-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b713a-184">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="b713a-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b713a-185">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="b713a-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="b713a-186">System-Only</span></span>            | <span data-ttu-id="b713a-187">False</span><span class="sxs-lookup"><span data-stu-id="b713a-187">False</span></span>                                                                                                     |
| <span data-ttu-id="b713a-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b713a-188">Is-Single-Valued</span></span>       | <span data-ttu-id="b713a-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="b713a-189">True</span></span>                                                                                                      |
| <span data-ttu-id="b713a-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b713a-190">Is Indexed</span></span>             | <span data-ttu-id="b713a-191">False</span><span class="sxs-lookup"><span data-stu-id="b713a-191">False</span></span>                                                                                                     |
| <span data-ttu-id="b713a-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b713a-192">In Global Catalog</span></span>      | <span data-ttu-id="b713a-193">False</span><span class="sxs-lookup"><span data-stu-id="b713a-193">False</span></span>                                                                                                     |
| <span data-ttu-id="b713a-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b713a-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="b713a-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b713a-195">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="b713a-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b713a-196">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="b713a-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b713a-197">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="b713a-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b713a-198">Search-Flags</span></span>           | <span data-ttu-id="b713a-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b713a-199">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="b713a-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b713a-200">System-Flags</span></span>           | <span data-ttu-id="b713a-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b713a-201">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="b713a-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b713a-202">Classes used in</span></span>        | [<span data-ttu-id="b713a-203">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="b713a-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="b713a-204">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="b713a-204">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b713a-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b713a-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b713a-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b713a-206">Entry</span></span> | <span data-ttu-id="b713a-207">Wert</span><span class="sxs-lookup"><span data-stu-id="b713a-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b713a-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b713a-208">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="b713a-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b713a-209">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="b713a-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="b713a-210">System-Only</span></span>            | <span data-ttu-id="b713a-211">False</span><span class="sxs-lookup"><span data-stu-id="b713a-211">False</span></span>                                                                                                     |
| <span data-ttu-id="b713a-212">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b713a-212">Is-Single-Valued</span></span>       | <span data-ttu-id="b713a-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="b713a-213">True</span></span>                                                                                                      |
| <span data-ttu-id="b713a-214">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b713a-214">Is Indexed</span></span>             | <span data-ttu-id="b713a-215">False</span><span class="sxs-lookup"><span data-stu-id="b713a-215">False</span></span>                                                                                                     |
| <span data-ttu-id="b713a-216">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b713a-216">In Global Catalog</span></span>      | <span data-ttu-id="b713a-217">False</span><span class="sxs-lookup"><span data-stu-id="b713a-217">False</span></span>                                                                                                     |
| <span data-ttu-id="b713a-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b713a-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="b713a-219">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b713a-219">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="b713a-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b713a-220">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="b713a-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b713a-221">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="b713a-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b713a-222">Search-Flags</span></span>           | <span data-ttu-id="b713a-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b713a-223">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="b713a-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b713a-224">System-Flags</span></span>           | <span data-ttu-id="b713a-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b713a-225">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="b713a-226">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b713a-226">Classes used in</span></span>        | [<span data-ttu-id="b713a-227">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="b713a-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="b713a-228">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="b713a-228">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b713a-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b713a-229">Windows Server 2008</span></span>



| <span data-ttu-id="b713a-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b713a-230">Entry</span></span> | <span data-ttu-id="b713a-231">Wert</span><span class="sxs-lookup"><span data-stu-id="b713a-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b713a-232">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b713a-232">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="b713a-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b713a-233">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="b713a-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="b713a-234">System-Only</span></span>            | <span data-ttu-id="b713a-235">False</span><span class="sxs-lookup"><span data-stu-id="b713a-235">False</span></span>                                                                                                     |
| <span data-ttu-id="b713a-236">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b713a-236">Is-Single-Valued</span></span>       | <span data-ttu-id="b713a-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="b713a-237">True</span></span>                                                                                                      |
| <span data-ttu-id="b713a-238">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b713a-238">Is Indexed</span></span>             | <span data-ttu-id="b713a-239">False</span><span class="sxs-lookup"><span data-stu-id="b713a-239">False</span></span>                                                                                                     |
| <span data-ttu-id="b713a-240">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b713a-240">In Global Catalog</span></span>      | <span data-ttu-id="b713a-241">False</span><span class="sxs-lookup"><span data-stu-id="b713a-241">False</span></span>                                                                                                     |
| <span data-ttu-id="b713a-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b713a-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="b713a-243">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b713a-243">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="b713a-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b713a-244">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="b713a-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b713a-245">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="b713a-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b713a-246">Search-Flags</span></span>           | <span data-ttu-id="b713a-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b713a-247">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="b713a-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b713a-248">System-Flags</span></span>           | <span data-ttu-id="b713a-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b713a-249">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="b713a-250">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b713a-250">Classes used in</span></span>        | [<span data-ttu-id="b713a-251">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="b713a-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="b713a-252">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="b713a-252">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b713a-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b713a-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b713a-254">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b713a-254">Entry</span></span> | <span data-ttu-id="b713a-255">Wert</span><span class="sxs-lookup"><span data-stu-id="b713a-255">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b713a-256">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b713a-256">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="b713a-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b713a-257">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="b713a-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="b713a-258">System-Only</span></span>            | <span data-ttu-id="b713a-259">False</span><span class="sxs-lookup"><span data-stu-id="b713a-259">False</span></span>                                                                                                     |
| <span data-ttu-id="b713a-260">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b713a-260">Is-Single-Valued</span></span>       | <span data-ttu-id="b713a-261">Richtig</span><span class="sxs-lookup"><span data-stu-id="b713a-261">True</span></span>                                                                                                      |
| <span data-ttu-id="b713a-262">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b713a-262">Is Indexed</span></span>             | <span data-ttu-id="b713a-263">False</span><span class="sxs-lookup"><span data-stu-id="b713a-263">False</span></span>                                                                                                     |
| <span data-ttu-id="b713a-264">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b713a-264">In Global Catalog</span></span>      | <span data-ttu-id="b713a-265">False</span><span class="sxs-lookup"><span data-stu-id="b713a-265">False</span></span>                                                                                                     |
| <span data-ttu-id="b713a-266">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b713a-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="b713a-267">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b713a-267">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="b713a-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b713a-268">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="b713a-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b713a-269">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="b713a-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b713a-270">Search-Flags</span></span>           | <span data-ttu-id="b713a-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b713a-271">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="b713a-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b713a-272">System-Flags</span></span>           | <span data-ttu-id="b713a-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b713a-273">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="b713a-274">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b713a-274">Classes used in</span></span>        | [<span data-ttu-id="b713a-275">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="b713a-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="b713a-276">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="b713a-276">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b713a-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b713a-277">Windows Server 2012</span></span>



| <span data-ttu-id="b713a-278">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b713a-278">Entry</span></span> | <span data-ttu-id="b713a-279">Wert</span><span class="sxs-lookup"><span data-stu-id="b713a-279">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b713a-280">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b713a-280">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="b713a-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b713a-281">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="b713a-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="b713a-282">System-Only</span></span>            | <span data-ttu-id="b713a-283">False</span><span class="sxs-lookup"><span data-stu-id="b713a-283">False</span></span>                                                                                                     |
| <span data-ttu-id="b713a-284">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b713a-284">Is-Single-Valued</span></span>       | <span data-ttu-id="b713a-285">Richtig</span><span class="sxs-lookup"><span data-stu-id="b713a-285">True</span></span>                                                                                                      |
| <span data-ttu-id="b713a-286">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b713a-286">Is Indexed</span></span>             | <span data-ttu-id="b713a-287">False</span><span class="sxs-lookup"><span data-stu-id="b713a-287">False</span></span>                                                                                                     |
| <span data-ttu-id="b713a-288">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b713a-288">In Global Catalog</span></span>      | <span data-ttu-id="b713a-289">False</span><span class="sxs-lookup"><span data-stu-id="b713a-289">False</span></span>                                                                                                     |
| <span data-ttu-id="b713a-290">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b713a-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="b713a-291">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b713a-291">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="b713a-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b713a-292">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="b713a-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b713a-293">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="b713a-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b713a-294">Search-Flags</span></span>           | <span data-ttu-id="b713a-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b713a-295">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="b713a-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b713a-296">System-Flags</span></span>           | <span data-ttu-id="b713a-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b713a-297">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="b713a-298">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b713a-298">Classes used in</span></span>        | [<span data-ttu-id="b713a-299">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="b713a-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="b713a-300">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="b713a-300">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





