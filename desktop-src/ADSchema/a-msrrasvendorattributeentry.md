---
title: MS-RRAS-Vendor-Attribute-Entry-Attribut
description: Eine Zeichenfolge, die es Anbietern ermöglicht, den DS routerattribute zur Verwendung in Abfragen in der Form AttributeName VendorID attributeType hinzuzufügen.
ms.assetid: 07bc4d9b-eba9-456b-be21-cd7bb8a5b0b6
ms.tgt_platform: multiple
keywords:
- "\"MS-RRAS-Vendor-Attribute-Entry\"-Attribut AD-Schema"
- AD-Schema des msrrasvendorattributeentry-Attributs
topic_type:
- apiref
api_name:
- ms-RRAS-Vendor-Attribute-Entry
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28ee353122107db5b1247860e9799db861b4d6bf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480026"
---
# <a name="ms-rras-vendor-attribute-entry-attribute"></a><span data-ttu-id="f42bb-105">MS-RRAS-Vendor-Attribute-Entry-Attribut</span><span class="sxs-lookup"><span data-stu-id="f42bb-105">ms-RRAS-Vendor-Attribute-Entry attribute</span></span>

<span data-ttu-id="f42bb-106">Eine Zeichenfolge, die es Anbietern ermöglicht, den DS routerattribute zur Verwendung in Abfragen in der Form AttributeName: VendorID: attributeType hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f42bb-106">A string that enables vendors to add router attributes to the DS for use in queries, in the form AttributeName:vendorID:AttributeType.</span></span>



| <span data-ttu-id="f42bb-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f42bb-107">Entry</span></span> | <span data-ttu-id="f42bb-108">Wert</span><span class="sxs-lookup"><span data-stu-id="f42bb-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f42bb-109">CN</span><span class="sxs-lookup"><span data-stu-id="f42bb-109">CN</span></span>                | <span data-ttu-id="f42bb-110">MS-RRAS-Vendor-Attribute-Entry</span><span class="sxs-lookup"><span data-stu-id="f42bb-110">ms-RRAS-Vendor-Attribute-Entry</span></span>              |
| <span data-ttu-id="f42bb-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f42bb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f42bb-112">msrrasvendorattributeentry</span><span class="sxs-lookup"><span data-stu-id="f42bb-112">msRRASVendorAttributeEntry</span></span>                  |
| <span data-ttu-id="f42bb-113">Size</span><span class="sxs-lookup"><span data-stu-id="f42bb-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="f42bb-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="f42bb-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="f42bb-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="f42bb-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="f42bb-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f42bb-116">Attribute-Id</span></span>      | <span data-ttu-id="f42bb-117">1.2.840.113556.1.4.883</span><span class="sxs-lookup"><span data-stu-id="f42bb-117">1.2.840.113556.1.4.883</span></span>                      |
| <span data-ttu-id="f42bb-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f42bb-118">System-Id-Guid</span></span>    | <span data-ttu-id="f42bb-119">f39b98ac-938d-11d1-aebd-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="f42bb-119">f39b98ac-938d-11d1-aebd-0000f80367c1</span></span>        |
| <span data-ttu-id="f42bb-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="f42bb-120">Syntax</span></span>            | [<span data-ttu-id="f42bb-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f42bb-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f42bb-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="f42bb-122">Implementations</span></span>

-   [<span data-ttu-id="f42bb-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f42bb-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f42bb-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f42bb-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f42bb-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f42bb-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f42bb-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f42bb-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f42bb-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f42bb-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f42bb-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f42bb-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f42bb-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f42bb-129">Windows 2000 Server</span></span>



| <span data-ttu-id="f42bb-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f42bb-130">Entry</span></span> | <span data-ttu-id="f42bb-131">Wert</span><span class="sxs-lookup"><span data-stu-id="f42bb-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f42bb-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f42bb-132">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="f42bb-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f42bb-133">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="f42bb-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="f42bb-134">System-Only</span></span>            | <span data-ttu-id="f42bb-135">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-135">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f42bb-136">Is-Single-Valued</span></span>       | <span data-ttu-id="f42bb-137">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-137">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f42bb-138">Is Indexed</span></span>             | <span data-ttu-id="f42bb-139">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-139">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f42bb-140">In Global Catalog</span></span>      | <span data-ttu-id="f42bb-141">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-141">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f42bb-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="f42bb-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f42bb-143">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="f42bb-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f42bb-144">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="f42bb-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f42bb-145">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="f42bb-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bb-146">Search-Flags</span></span>           | <span data-ttu-id="f42bb-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f42bb-147">0x00000000</span></span>                                                                          |
| <span data-ttu-id="f42bb-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bb-148">System-Flags</span></span>           | <span data-ttu-id="f42bb-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f42bb-149">0x00000010</span></span>                                                                          |
| <span data-ttu-id="f42bb-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f42bb-150">Classes used in</span></span>        | [<span data-ttu-id="f42bb-151">**RRAS-Administration: Wörterbuch**</span><span class="sxs-lookup"><span data-stu-id="f42bb-151">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f42bb-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f42bb-152">Windows Server 2003</span></span>



| <span data-ttu-id="f42bb-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f42bb-153">Entry</span></span> | <span data-ttu-id="f42bb-154">Wert</span><span class="sxs-lookup"><span data-stu-id="f42bb-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f42bb-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f42bb-155">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="f42bb-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f42bb-156">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="f42bb-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="f42bb-157">System-Only</span></span>            | <span data-ttu-id="f42bb-158">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-158">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f42bb-159">Is-Single-Valued</span></span>       | <span data-ttu-id="f42bb-160">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-160">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f42bb-161">Is Indexed</span></span>             | <span data-ttu-id="f42bb-162">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-162">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f42bb-163">In Global Catalog</span></span>      | <span data-ttu-id="f42bb-164">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-164">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f42bb-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="f42bb-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f42bb-166">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="f42bb-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f42bb-167">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="f42bb-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f42bb-168">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="f42bb-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bb-169">Search-Flags</span></span>           | <span data-ttu-id="f42bb-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f42bb-170">0x00000000</span></span>                                                                          |
| <span data-ttu-id="f42bb-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bb-171">System-Flags</span></span>           | <span data-ttu-id="f42bb-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f42bb-172">0x00000010</span></span>                                                                          |
| <span data-ttu-id="f42bb-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f42bb-173">Classes used in</span></span>        | [<span data-ttu-id="f42bb-174">**RRAS-Administration: Wörterbuch**</span><span class="sxs-lookup"><span data-stu-id="f42bb-174">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f42bb-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f42bb-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f42bb-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f42bb-176">Entry</span></span> | <span data-ttu-id="f42bb-177">Wert</span><span class="sxs-lookup"><span data-stu-id="f42bb-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f42bb-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f42bb-178">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="f42bb-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f42bb-179">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="f42bb-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="f42bb-180">System-Only</span></span>            | <span data-ttu-id="f42bb-181">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-181">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f42bb-182">Is-Single-Valued</span></span>       | <span data-ttu-id="f42bb-183">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-183">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f42bb-184">Is Indexed</span></span>             | <span data-ttu-id="f42bb-185">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-185">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f42bb-186">In Global Catalog</span></span>      | <span data-ttu-id="f42bb-187">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-187">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f42bb-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="f42bb-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f42bb-189">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="f42bb-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f42bb-190">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="f42bb-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f42bb-191">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="f42bb-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bb-192">Search-Flags</span></span>           | <span data-ttu-id="f42bb-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f42bb-193">0x00000000</span></span>                                                                          |
| <span data-ttu-id="f42bb-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bb-194">System-Flags</span></span>           | <span data-ttu-id="f42bb-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f42bb-195">0x00000010</span></span>                                                                          |
| <span data-ttu-id="f42bb-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f42bb-196">Classes used in</span></span>        | [<span data-ttu-id="f42bb-197">**RRAS-Administration: Wörterbuch**</span><span class="sxs-lookup"><span data-stu-id="f42bb-197">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f42bb-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f42bb-198">Windows Server 2008</span></span>



| <span data-ttu-id="f42bb-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f42bb-199">Entry</span></span> | <span data-ttu-id="f42bb-200">Wert</span><span class="sxs-lookup"><span data-stu-id="f42bb-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f42bb-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f42bb-201">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="f42bb-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f42bb-202">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="f42bb-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="f42bb-203">System-Only</span></span>            | <span data-ttu-id="f42bb-204">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-204">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f42bb-205">Is-Single-Valued</span></span>       | <span data-ttu-id="f42bb-206">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-206">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f42bb-207">Is Indexed</span></span>             | <span data-ttu-id="f42bb-208">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-208">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f42bb-209">In Global Catalog</span></span>      | <span data-ttu-id="f42bb-210">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-210">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f42bb-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="f42bb-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f42bb-212">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="f42bb-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f42bb-213">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="f42bb-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f42bb-214">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="f42bb-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bb-215">Search-Flags</span></span>           | <span data-ttu-id="f42bb-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f42bb-216">0x00000000</span></span>                                                                          |
| <span data-ttu-id="f42bb-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bb-217">System-Flags</span></span>           | <span data-ttu-id="f42bb-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f42bb-218">0x00000010</span></span>                                                                          |
| <span data-ttu-id="f42bb-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f42bb-219">Classes used in</span></span>        | [<span data-ttu-id="f42bb-220">**RRAS-Administration: Wörterbuch**</span><span class="sxs-lookup"><span data-stu-id="f42bb-220">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f42bb-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f42bb-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f42bb-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f42bb-222">Entry</span></span> | <span data-ttu-id="f42bb-223">Wert</span><span class="sxs-lookup"><span data-stu-id="f42bb-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f42bb-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f42bb-224">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="f42bb-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f42bb-225">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="f42bb-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="f42bb-226">System-Only</span></span>            | <span data-ttu-id="f42bb-227">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-227">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f42bb-228">Is-Single-Valued</span></span>       | <span data-ttu-id="f42bb-229">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-229">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f42bb-230">Is Indexed</span></span>             | <span data-ttu-id="f42bb-231">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-231">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f42bb-232">In Global Catalog</span></span>      | <span data-ttu-id="f42bb-233">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-233">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f42bb-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="f42bb-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f42bb-235">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="f42bb-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f42bb-236">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="f42bb-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f42bb-237">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="f42bb-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bb-238">Search-Flags</span></span>           | <span data-ttu-id="f42bb-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f42bb-239">0x00000000</span></span>                                                                          |
| <span data-ttu-id="f42bb-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bb-240">System-Flags</span></span>           | <span data-ttu-id="f42bb-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f42bb-241">0x00000010</span></span>                                                                          |
| <span data-ttu-id="f42bb-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f42bb-242">Classes used in</span></span>        | [<span data-ttu-id="f42bb-243">**RRAS-Administration: Wörterbuch**</span><span class="sxs-lookup"><span data-stu-id="f42bb-243">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f42bb-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f42bb-244">Windows Server 2012</span></span>



| <span data-ttu-id="f42bb-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f42bb-245">Entry</span></span> | <span data-ttu-id="f42bb-246">Wert</span><span class="sxs-lookup"><span data-stu-id="f42bb-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f42bb-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f42bb-247">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="f42bb-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f42bb-248">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="f42bb-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="f42bb-249">System-Only</span></span>            | <span data-ttu-id="f42bb-250">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-250">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f42bb-251">Is-Single-Valued</span></span>       | <span data-ttu-id="f42bb-252">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-252">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f42bb-253">Is Indexed</span></span>             | <span data-ttu-id="f42bb-254">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-254">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f42bb-255">In Global Catalog</span></span>      | <span data-ttu-id="f42bb-256">False</span><span class="sxs-lookup"><span data-stu-id="f42bb-256">False</span></span>                                                                               |
| <span data-ttu-id="f42bb-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f42bb-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="f42bb-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f42bb-258">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="f42bb-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f42bb-259">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="f42bb-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f42bb-260">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="f42bb-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bb-261">Search-Flags</span></span>           | <span data-ttu-id="f42bb-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f42bb-262">0x00000000</span></span>                                                                          |
| <span data-ttu-id="f42bb-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bb-263">System-Flags</span></span>           | <span data-ttu-id="f42bb-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f42bb-264">0x00000010</span></span>                                                                          |
| <span data-ttu-id="f42bb-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f42bb-265">Classes used in</span></span>        | [<span data-ttu-id="f42bb-266">**RRAS-Administration: Wörterbuch**</span><span class="sxs-lookup"><span data-stu-id="f42bb-266">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



 

 





