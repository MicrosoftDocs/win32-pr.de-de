---
title: Default-Security-Descriptor-Attribut
description: Die Sicherheits Beschreibung, die dem-Objekt bei der ersten Erstellung zugewiesen werden soll.
ms.assetid: 22575883-2ef3-492b-9868-1eb350c4f547
ms.tgt_platform: multiple
keywords:
- Standard-Security-Descriptor-Attribut AD-Schema
- AD-Schema des defaultSecurityDescriptor-Attributs
topic_type:
- apiref
api_name:
- Default-Security-Descriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cd0b4a8dbe0c633a15b6a5167cb1171a14d1769
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479735"
---
# <a name="default-security-descriptor-attribute"></a><span data-ttu-id="f879a-105">Default-Security-Descriptor-Attribut</span><span class="sxs-lookup"><span data-stu-id="f879a-105">Default-Security-Descriptor attribute</span></span>

<span data-ttu-id="f879a-106">Die Sicherheits Beschreibung, die dem-Objekt bei der ersten Erstellung zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f879a-106">The security descriptor to be assigned to the object when it is first created.</span></span>



| <span data-ttu-id="f879a-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f879a-107">Entry</span></span> | <span data-ttu-id="f879a-108">Wert</span><span class="sxs-lookup"><span data-stu-id="f879a-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f879a-109">CN</span><span class="sxs-lookup"><span data-stu-id="f879a-109">CN</span></span>                | <span data-ttu-id="f879a-110">Standard-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f879a-110">Default-Security-Descriptor</span></span>                 |
| <span data-ttu-id="f879a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f879a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f879a-112">defaultSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="f879a-112">defaultSecurityDescriptor</span></span>                   |
| <span data-ttu-id="f879a-113">Size</span><span class="sxs-lookup"><span data-stu-id="f879a-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="f879a-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="f879a-114">Update Privilege</span></span>  | <span data-ttu-id="f879a-115">Schema Administrator</span><span class="sxs-lookup"><span data-stu-id="f879a-115">Schema administrator</span></span>                        |
| <span data-ttu-id="f879a-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="f879a-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="f879a-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f879a-117">Attribute-Id</span></span>      | <span data-ttu-id="f879a-118">1.2.840.113556.1.4.224</span><span class="sxs-lookup"><span data-stu-id="f879a-118">1.2.840.113556.1.4.224</span></span>                      |
| <span data-ttu-id="f879a-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f879a-119">System-Id-Guid</span></span>    | <span data-ttu-id="f879a-120">807a6d30-1669-11D0-A064-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="f879a-120">807a6d30-1669-11d0-a064-00aa006c33ed</span></span>        |
| <span data-ttu-id="f879a-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="f879a-121">Syntax</span></span>            | [<span data-ttu-id="f879a-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f879a-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f879a-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="f879a-123">Implementations</span></span>

-   [<span data-ttu-id="f879a-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f879a-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f879a-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f879a-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f879a-126">**Adam**</span><span class="sxs-lookup"><span data-stu-id="f879a-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f879a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f879a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f879a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f879a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f879a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f879a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f879a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f879a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f879a-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f879a-131">Windows 2000 Server</span></span>



| <span data-ttu-id="f879a-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f879a-132">Entry</span></span> | <span data-ttu-id="f879a-133">Wert</span><span class="sxs-lookup"><span data-stu-id="f879a-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="f879a-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f879a-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="f879a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f879a-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="f879a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="f879a-136">System-Only</span></span>            | <span data-ttu-id="f879a-137">False</span><span class="sxs-lookup"><span data-stu-id="f879a-137">False</span></span>                                            |
| <span data-ttu-id="f879a-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f879a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="f879a-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="f879a-139">True</span></span>                                             |
| <span data-ttu-id="f879a-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f879a-140">Is Indexed</span></span>             | <span data-ttu-id="f879a-141">False</span><span class="sxs-lookup"><span data-stu-id="f879a-141">False</span></span>                                            |
| <span data-ttu-id="f879a-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f879a-142">In Global Catalog</span></span>      | <span data-ttu-id="f879a-143">False</span><span class="sxs-lookup"><span data-stu-id="f879a-143">False</span></span>                                            |
| <span data-ttu-id="f879a-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f879a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="f879a-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f879a-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="f879a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f879a-146">Range-Lower</span></span>            | <span data-ttu-id="f879a-147">0</span><span class="sxs-lookup"><span data-stu-id="f879a-147">0</span></span>                                                |
| <span data-ttu-id="f879a-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f879a-148">Range-Upper</span></span>            | <span data-ttu-id="f879a-149">32767</span><span class="sxs-lookup"><span data-stu-id="f879a-149">32767</span></span>                                            |
| <span data-ttu-id="f879a-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f879a-150">Search-Flags</span></span>           | <span data-ttu-id="f879a-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f879a-151">0x00000000</span></span>                                       |
| <span data-ttu-id="f879a-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f879a-152">System-Flags</span></span>           | <span data-ttu-id="f879a-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f879a-153">0x00000010</span></span>                                       |
| <span data-ttu-id="f879a-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f879a-154">Classes used in</span></span>        | [<span data-ttu-id="f879a-155">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="f879a-155">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f879a-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f879a-156">Windows Server 2003</span></span>



| <span data-ttu-id="f879a-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f879a-157">Entry</span></span> | <span data-ttu-id="f879a-158">Wert</span><span class="sxs-lookup"><span data-stu-id="f879a-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="f879a-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f879a-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="f879a-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f879a-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="f879a-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="f879a-161">System-Only</span></span>            | <span data-ttu-id="f879a-162">False</span><span class="sxs-lookup"><span data-stu-id="f879a-162">False</span></span>                                            |
| <span data-ttu-id="f879a-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f879a-163">Is-Single-Valued</span></span>       | <span data-ttu-id="f879a-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="f879a-164">True</span></span>                                             |
| <span data-ttu-id="f879a-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f879a-165">Is Indexed</span></span>             | <span data-ttu-id="f879a-166">False</span><span class="sxs-lookup"><span data-stu-id="f879a-166">False</span></span>                                            |
| <span data-ttu-id="f879a-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f879a-167">In Global Catalog</span></span>      | <span data-ttu-id="f879a-168">False</span><span class="sxs-lookup"><span data-stu-id="f879a-168">False</span></span>                                            |
| <span data-ttu-id="f879a-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f879a-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="f879a-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f879a-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="f879a-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f879a-171">Range-Lower</span></span>            | <span data-ttu-id="f879a-172">0</span><span class="sxs-lookup"><span data-stu-id="f879a-172">0</span></span>                                                |
| <span data-ttu-id="f879a-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f879a-173">Range-Upper</span></span>            | <span data-ttu-id="f879a-174">32767</span><span class="sxs-lookup"><span data-stu-id="f879a-174">32767</span></span>                                            |
| <span data-ttu-id="f879a-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f879a-175">Search-Flags</span></span>           | <span data-ttu-id="f879a-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f879a-176">0x00000000</span></span>                                       |
| <span data-ttu-id="f879a-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f879a-177">System-Flags</span></span>           | <span data-ttu-id="f879a-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f879a-178">0x00000010</span></span>                                       |
| <span data-ttu-id="f879a-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f879a-179">Classes used in</span></span>        | [<span data-ttu-id="f879a-180">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="f879a-180">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f879a-181">Adam</span><span class="sxs-lookup"><span data-stu-id="f879a-181">ADAM</span></span>



| <span data-ttu-id="f879a-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f879a-182">Entry</span></span> | <span data-ttu-id="f879a-183">Wert</span><span class="sxs-lookup"><span data-stu-id="f879a-183">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="f879a-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f879a-184">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="f879a-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f879a-185">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="f879a-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="f879a-186">System-Only</span></span>            | <span data-ttu-id="f879a-187">False</span><span class="sxs-lookup"><span data-stu-id="f879a-187">False</span></span>                                            |
| <span data-ttu-id="f879a-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f879a-188">Is-Single-Valued</span></span>       | <span data-ttu-id="f879a-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="f879a-189">True</span></span>                                             |
| <span data-ttu-id="f879a-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f879a-190">Is Indexed</span></span>             | <span data-ttu-id="f879a-191">False</span><span class="sxs-lookup"><span data-stu-id="f879a-191">False</span></span>                                            |
| <span data-ttu-id="f879a-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f879a-192">In Global Catalog</span></span>      | <span data-ttu-id="f879a-193">False</span><span class="sxs-lookup"><span data-stu-id="f879a-193">False</span></span>                                            |
| <span data-ttu-id="f879a-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f879a-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="f879a-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f879a-195">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="f879a-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f879a-196">Range-Lower</span></span>            | <span data-ttu-id="f879a-197">0</span><span class="sxs-lookup"><span data-stu-id="f879a-197">0</span></span>                                                |
| <span data-ttu-id="f879a-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f879a-198">Range-Upper</span></span>            | <span data-ttu-id="f879a-199">32767</span><span class="sxs-lookup"><span data-stu-id="f879a-199">32767</span></span>                                            |
| <span data-ttu-id="f879a-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f879a-200">Search-Flags</span></span>           | <span data-ttu-id="f879a-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f879a-201">0x00000000</span></span>                                       |
| <span data-ttu-id="f879a-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f879a-202">System-Flags</span></span>           | <span data-ttu-id="f879a-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f879a-203">0x00000010</span></span>                                       |
| <span data-ttu-id="f879a-204">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f879a-204">Classes used in</span></span>        | [<span data-ttu-id="f879a-205">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="f879a-205">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f879a-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f879a-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f879a-207">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f879a-207">Entry</span></span> | <span data-ttu-id="f879a-208">Wert</span><span class="sxs-lookup"><span data-stu-id="f879a-208">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="f879a-209">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f879a-209">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="f879a-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f879a-210">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="f879a-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="f879a-211">System-Only</span></span>            | <span data-ttu-id="f879a-212">False</span><span class="sxs-lookup"><span data-stu-id="f879a-212">False</span></span>                                            |
| <span data-ttu-id="f879a-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f879a-213">Is-Single-Valued</span></span>       | <span data-ttu-id="f879a-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="f879a-214">True</span></span>                                             |
| <span data-ttu-id="f879a-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f879a-215">Is Indexed</span></span>             | <span data-ttu-id="f879a-216">False</span><span class="sxs-lookup"><span data-stu-id="f879a-216">False</span></span>                                            |
| <span data-ttu-id="f879a-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f879a-217">In Global Catalog</span></span>      | <span data-ttu-id="f879a-218">False</span><span class="sxs-lookup"><span data-stu-id="f879a-218">False</span></span>                                            |
| <span data-ttu-id="f879a-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f879a-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="f879a-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f879a-220">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="f879a-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f879a-221">Range-Lower</span></span>            | <span data-ttu-id="f879a-222">0</span><span class="sxs-lookup"><span data-stu-id="f879a-222">0</span></span>                                                |
| <span data-ttu-id="f879a-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f879a-223">Range-Upper</span></span>            | <span data-ttu-id="f879a-224">32767</span><span class="sxs-lookup"><span data-stu-id="f879a-224">32767</span></span>                                            |
| <span data-ttu-id="f879a-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f879a-225">Search-Flags</span></span>           | <span data-ttu-id="f879a-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f879a-226">0x00000000</span></span>                                       |
| <span data-ttu-id="f879a-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f879a-227">System-Flags</span></span>           | <span data-ttu-id="f879a-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f879a-228">0x00000010</span></span>                                       |
| <span data-ttu-id="f879a-229">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f879a-229">Classes used in</span></span>        | [<span data-ttu-id="f879a-230">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="f879a-230">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f879a-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f879a-231">Windows Server 2008</span></span>



| <span data-ttu-id="f879a-232">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f879a-232">Entry</span></span> | <span data-ttu-id="f879a-233">Wert</span><span class="sxs-lookup"><span data-stu-id="f879a-233">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="f879a-234">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f879a-234">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="f879a-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f879a-235">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="f879a-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="f879a-236">System-Only</span></span>            | <span data-ttu-id="f879a-237">False</span><span class="sxs-lookup"><span data-stu-id="f879a-237">False</span></span>                                            |
| <span data-ttu-id="f879a-238">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f879a-238">Is-Single-Valued</span></span>       | <span data-ttu-id="f879a-239">Richtig</span><span class="sxs-lookup"><span data-stu-id="f879a-239">True</span></span>                                             |
| <span data-ttu-id="f879a-240">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f879a-240">Is Indexed</span></span>             | <span data-ttu-id="f879a-241">False</span><span class="sxs-lookup"><span data-stu-id="f879a-241">False</span></span>                                            |
| <span data-ttu-id="f879a-242">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f879a-242">In Global Catalog</span></span>      | <span data-ttu-id="f879a-243">False</span><span class="sxs-lookup"><span data-stu-id="f879a-243">False</span></span>                                            |
| <span data-ttu-id="f879a-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f879a-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="f879a-245">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f879a-245">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="f879a-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f879a-246">Range-Lower</span></span>            | <span data-ttu-id="f879a-247">0</span><span class="sxs-lookup"><span data-stu-id="f879a-247">0</span></span>                                                |
| <span data-ttu-id="f879a-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f879a-248">Range-Upper</span></span>            | <span data-ttu-id="f879a-249">32767</span><span class="sxs-lookup"><span data-stu-id="f879a-249">32767</span></span>                                            |
| <span data-ttu-id="f879a-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f879a-250">Search-Flags</span></span>           | <span data-ttu-id="f879a-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f879a-251">0x00000000</span></span>                                       |
| <span data-ttu-id="f879a-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f879a-252">System-Flags</span></span>           | <span data-ttu-id="f879a-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f879a-253">0x00000010</span></span>                                       |
| <span data-ttu-id="f879a-254">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f879a-254">Classes used in</span></span>        | [<span data-ttu-id="f879a-255">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="f879a-255">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f879a-256">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f879a-256">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f879a-257">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f879a-257">Entry</span></span> | <span data-ttu-id="f879a-258">Wert</span><span class="sxs-lookup"><span data-stu-id="f879a-258">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="f879a-259">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f879a-259">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="f879a-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f879a-260">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="f879a-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="f879a-261">System-Only</span></span>            | <span data-ttu-id="f879a-262">False</span><span class="sxs-lookup"><span data-stu-id="f879a-262">False</span></span>                                            |
| <span data-ttu-id="f879a-263">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f879a-263">Is-Single-Valued</span></span>       | <span data-ttu-id="f879a-264">Richtig</span><span class="sxs-lookup"><span data-stu-id="f879a-264">True</span></span>                                             |
| <span data-ttu-id="f879a-265">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f879a-265">Is Indexed</span></span>             | <span data-ttu-id="f879a-266">False</span><span class="sxs-lookup"><span data-stu-id="f879a-266">False</span></span>                                            |
| <span data-ttu-id="f879a-267">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f879a-267">In Global Catalog</span></span>      | <span data-ttu-id="f879a-268">False</span><span class="sxs-lookup"><span data-stu-id="f879a-268">False</span></span>                                            |
| <span data-ttu-id="f879a-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f879a-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="f879a-270">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f879a-270">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="f879a-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f879a-271">Range-Lower</span></span>            | <span data-ttu-id="f879a-272">0</span><span class="sxs-lookup"><span data-stu-id="f879a-272">0</span></span>                                                |
| <span data-ttu-id="f879a-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f879a-273">Range-Upper</span></span>            | <span data-ttu-id="f879a-274">32767</span><span class="sxs-lookup"><span data-stu-id="f879a-274">32767</span></span>                                            |
| <span data-ttu-id="f879a-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f879a-275">Search-Flags</span></span>           | <span data-ttu-id="f879a-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f879a-276">0x00000000</span></span>                                       |
| <span data-ttu-id="f879a-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f879a-277">System-Flags</span></span>           | <span data-ttu-id="f879a-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f879a-278">0x00000010</span></span>                                       |
| <span data-ttu-id="f879a-279">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f879a-279">Classes used in</span></span>        | [<span data-ttu-id="f879a-280">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="f879a-280">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f879a-281">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f879a-281">Windows Server 2012</span></span>



| <span data-ttu-id="f879a-282">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f879a-282">Entry</span></span> | <span data-ttu-id="f879a-283">Wert</span><span class="sxs-lookup"><span data-stu-id="f879a-283">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="f879a-284">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f879a-284">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="f879a-285">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f879a-285">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="f879a-286">System-Only</span><span class="sxs-lookup"><span data-stu-id="f879a-286">System-Only</span></span>            | <span data-ttu-id="f879a-287">False</span><span class="sxs-lookup"><span data-stu-id="f879a-287">False</span></span>                                            |
| <span data-ttu-id="f879a-288">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f879a-288">Is-Single-Valued</span></span>       | <span data-ttu-id="f879a-289">Richtig</span><span class="sxs-lookup"><span data-stu-id="f879a-289">True</span></span>                                             |
| <span data-ttu-id="f879a-290">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f879a-290">Is Indexed</span></span>             | <span data-ttu-id="f879a-291">False</span><span class="sxs-lookup"><span data-stu-id="f879a-291">False</span></span>                                            |
| <span data-ttu-id="f879a-292">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f879a-292">In Global Catalog</span></span>      | <span data-ttu-id="f879a-293">False</span><span class="sxs-lookup"><span data-stu-id="f879a-293">False</span></span>                                            |
| <span data-ttu-id="f879a-294">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f879a-294">NT-Security-Descriptor</span></span> | <span data-ttu-id="f879a-295">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f879a-295">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="f879a-296">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f879a-296">Range-Lower</span></span>            | <span data-ttu-id="f879a-297">0</span><span class="sxs-lookup"><span data-stu-id="f879a-297">0</span></span>                                                |
| <span data-ttu-id="f879a-298">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f879a-298">Range-Upper</span></span>            | <span data-ttu-id="f879a-299">32767</span><span class="sxs-lookup"><span data-stu-id="f879a-299">32767</span></span>                                            |
| <span data-ttu-id="f879a-300">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f879a-300">Search-Flags</span></span>           | <span data-ttu-id="f879a-301">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f879a-301">0x00000000</span></span>                                       |
| <span data-ttu-id="f879a-302">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f879a-302">System-Flags</span></span>           | <span data-ttu-id="f879a-303">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f879a-303">0x00000010</span></span>                                       |
| <span data-ttu-id="f879a-304">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f879a-304">Classes used in</span></span>        | [<span data-ttu-id="f879a-305">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="f879a-305">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





