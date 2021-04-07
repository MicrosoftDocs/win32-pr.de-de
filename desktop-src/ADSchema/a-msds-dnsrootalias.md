---
title: ms-DS-dnsrootalias-Attribut
description: Wird verwendet, um den Domänenalias zu speichern.
ms.assetid: 36b64363-947f-4af9-947f-eefead55bb02
ms.tgt_platform: multiple
keywords:
- AD-Schema des ms-DS-dnsrootalias-Attributs
- AD-Schema des msDS-dnsrootalias-Attributs
topic_type:
- apiref
api_name:
- ms-DS-DnsRootAlias
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f0b20b9316aaa9e68ab1ed907135c5640c1480f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103745169"
---
# <a name="ms-ds-dnsrootalias-attribute"></a><span data-ttu-id="449aa-105">ms-DS-dnsrootalias-Attribut</span><span class="sxs-lookup"><span data-stu-id="449aa-105">ms-DS-DnsRootAlias attribute</span></span>

<span data-ttu-id="449aa-106">Wird verwendet, um den Domänenalias zu speichern.</span><span class="sxs-lookup"><span data-stu-id="449aa-106">Used to store the domain alias.</span></span>



| <span data-ttu-id="449aa-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="449aa-107">Entry</span></span> | <span data-ttu-id="449aa-108">Wert</span><span class="sxs-lookup"><span data-stu-id="449aa-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="449aa-109">CN</span><span class="sxs-lookup"><span data-stu-id="449aa-109">CN</span></span>                | <span data-ttu-id="449aa-110">ms-DS-dnsrootalias</span><span class="sxs-lookup"><span data-stu-id="449aa-110">ms-DS-DnsRootAlias</span></span>                          |
| <span data-ttu-id="449aa-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="449aa-111">Ldap-Display-Name</span></span> | <span data-ttu-id="449aa-112">MSDS-dnsrootalias</span><span class="sxs-lookup"><span data-stu-id="449aa-112">msDS-DnsRootAlias</span></span>                           |
| <span data-ttu-id="449aa-113">Size</span><span class="sxs-lookup"><span data-stu-id="449aa-113">Size</span></span>              | <span data-ttu-id="449aa-114">Maximale Größe 255 Bytes.</span><span class="sxs-lookup"><span data-stu-id="449aa-114">Maximum size 255 bytes.</span></span>                     |
| <span data-ttu-id="449aa-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="449aa-115">Update Privilege</span></span>  | <span data-ttu-id="449aa-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="449aa-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="449aa-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="449aa-117">Update Frequency</span></span>  | <span data-ttu-id="449aa-118">Nur während der Domänen Umstrukturierung.</span><span class="sxs-lookup"><span data-stu-id="449aa-118">Only during domain restructure.</span></span>             |
| <span data-ttu-id="449aa-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="449aa-119">Attribute-Id</span></span>      | <span data-ttu-id="449aa-120">1.2.840.113556.1.4.1719</span><span class="sxs-lookup"><span data-stu-id="449aa-120">1.2.840.113556.1.4.1719</span></span>                     |
| <span data-ttu-id="449aa-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="449aa-121">System-Id-Guid</span></span>    | <span data-ttu-id="449aa-122">2143acca-eead-4D29-b591-85fa49ce9173</span><span class="sxs-lookup"><span data-stu-id="449aa-122">2143acca-eead-4d29-b591-85fa49ce9173</span></span>        |
| <span data-ttu-id="449aa-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="449aa-123">Syntax</span></span>            | [<span data-ttu-id="449aa-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="449aa-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="449aa-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="449aa-125">Implementations</span></span>

-   [<span data-ttu-id="449aa-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="449aa-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="449aa-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="449aa-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="449aa-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="449aa-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="449aa-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="449aa-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="449aa-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="449aa-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="449aa-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="449aa-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="449aa-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="449aa-132">Windows Server 2003</span></span>



| <span data-ttu-id="449aa-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="449aa-133">Entry</span></span> | <span data-ttu-id="449aa-134">Wert</span><span class="sxs-lookup"><span data-stu-id="449aa-134">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="449aa-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="449aa-135">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="449aa-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="449aa-136">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="449aa-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="449aa-137">System-Only</span></span>            | <span data-ttu-id="449aa-138">False</span><span class="sxs-lookup"><span data-stu-id="449aa-138">False</span></span>                                      |
| <span data-ttu-id="449aa-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="449aa-139">Is-Single-Valued</span></span>       | <span data-ttu-id="449aa-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="449aa-140">True</span></span>                                       |
| <span data-ttu-id="449aa-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="449aa-141">Is Indexed</span></span>             | <span data-ttu-id="449aa-142">False</span><span class="sxs-lookup"><span data-stu-id="449aa-142">False</span></span>                                      |
| <span data-ttu-id="449aa-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="449aa-143">In Global Catalog</span></span>      | <span data-ttu-id="449aa-144">False</span><span class="sxs-lookup"><span data-stu-id="449aa-144">False</span></span>                                      |
| <span data-ttu-id="449aa-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="449aa-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="449aa-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="449aa-146">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="449aa-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="449aa-147">Range-Lower</span></span>            | <span data-ttu-id="449aa-148">0</span><span class="sxs-lookup"><span data-stu-id="449aa-148">0</span></span>                                          |
| <span data-ttu-id="449aa-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="449aa-149">Range-Upper</span></span>            | <span data-ttu-id="449aa-150">255</span><span class="sxs-lookup"><span data-stu-id="449aa-150">255</span></span>                                        |
| <span data-ttu-id="449aa-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="449aa-151">Search-Flags</span></span>           | <span data-ttu-id="449aa-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="449aa-152">0x00000000</span></span>                                 |
| <span data-ttu-id="449aa-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="449aa-153">System-Flags</span></span>           | <span data-ttu-id="449aa-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="449aa-154">0x00000010</span></span>                                 |
| <span data-ttu-id="449aa-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="449aa-155">Classes used in</span></span>        | [<span data-ttu-id="449aa-156">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="449aa-156">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="449aa-157">Adam</span><span class="sxs-lookup"><span data-stu-id="449aa-157">ADAM</span></span>



| <span data-ttu-id="449aa-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="449aa-158">Entry</span></span> | <span data-ttu-id="449aa-159">Wert</span><span class="sxs-lookup"><span data-stu-id="449aa-159">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="449aa-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="449aa-160">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="449aa-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="449aa-161">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="449aa-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="449aa-162">System-Only</span></span>            | <span data-ttu-id="449aa-163">False</span><span class="sxs-lookup"><span data-stu-id="449aa-163">False</span></span>                                      |
| <span data-ttu-id="449aa-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="449aa-164">Is-Single-Valued</span></span>       | <span data-ttu-id="449aa-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="449aa-165">True</span></span>                                       |
| <span data-ttu-id="449aa-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="449aa-166">Is Indexed</span></span>             | <span data-ttu-id="449aa-167">False</span><span class="sxs-lookup"><span data-stu-id="449aa-167">False</span></span>                                      |
| <span data-ttu-id="449aa-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="449aa-168">In Global Catalog</span></span>      | <span data-ttu-id="449aa-169">False</span><span class="sxs-lookup"><span data-stu-id="449aa-169">False</span></span>                                      |
| <span data-ttu-id="449aa-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="449aa-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="449aa-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="449aa-171">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="449aa-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="449aa-172">Range-Lower</span></span>            | <span data-ttu-id="449aa-173">0</span><span class="sxs-lookup"><span data-stu-id="449aa-173">0</span></span>                                          |
| <span data-ttu-id="449aa-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="449aa-174">Range-Upper</span></span>            | <span data-ttu-id="449aa-175">255</span><span class="sxs-lookup"><span data-stu-id="449aa-175">255</span></span>                                        |
| <span data-ttu-id="449aa-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="449aa-176">Search-Flags</span></span>           | <span data-ttu-id="449aa-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="449aa-177">0x00000000</span></span>                                 |
| <span data-ttu-id="449aa-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="449aa-178">System-Flags</span></span>           | <span data-ttu-id="449aa-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="449aa-179">0x00000010</span></span>                                 |
| <span data-ttu-id="449aa-180">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="449aa-180">Classes used in</span></span>        | [<span data-ttu-id="449aa-181">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="449aa-181">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="449aa-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="449aa-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="449aa-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="449aa-183">Entry</span></span> | <span data-ttu-id="449aa-184">Wert</span><span class="sxs-lookup"><span data-stu-id="449aa-184">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="449aa-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="449aa-185">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="449aa-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="449aa-186">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="449aa-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="449aa-187">System-Only</span></span>            | <span data-ttu-id="449aa-188">False</span><span class="sxs-lookup"><span data-stu-id="449aa-188">False</span></span>                                      |
| <span data-ttu-id="449aa-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="449aa-189">Is-Single-Valued</span></span>       | <span data-ttu-id="449aa-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="449aa-190">True</span></span>                                       |
| <span data-ttu-id="449aa-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="449aa-191">Is Indexed</span></span>             | <span data-ttu-id="449aa-192">False</span><span class="sxs-lookup"><span data-stu-id="449aa-192">False</span></span>                                      |
| <span data-ttu-id="449aa-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="449aa-193">In Global Catalog</span></span>      | <span data-ttu-id="449aa-194">False</span><span class="sxs-lookup"><span data-stu-id="449aa-194">False</span></span>                                      |
| <span data-ttu-id="449aa-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="449aa-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="449aa-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="449aa-196">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="449aa-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="449aa-197">Range-Lower</span></span>            | <span data-ttu-id="449aa-198">0</span><span class="sxs-lookup"><span data-stu-id="449aa-198">0</span></span>                                          |
| <span data-ttu-id="449aa-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="449aa-199">Range-Upper</span></span>            | <span data-ttu-id="449aa-200">255</span><span class="sxs-lookup"><span data-stu-id="449aa-200">255</span></span>                                        |
| <span data-ttu-id="449aa-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="449aa-201">Search-Flags</span></span>           | <span data-ttu-id="449aa-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="449aa-202">0x00000000</span></span>                                 |
| <span data-ttu-id="449aa-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="449aa-203">System-Flags</span></span>           | <span data-ttu-id="449aa-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="449aa-204">0x00000010</span></span>                                 |
| <span data-ttu-id="449aa-205">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="449aa-205">Classes used in</span></span>        | [<span data-ttu-id="449aa-206">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="449aa-206">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="449aa-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="449aa-207">Windows Server 2008</span></span>



| <span data-ttu-id="449aa-208">Eingabe</span><span class="sxs-lookup"><span data-stu-id="449aa-208">Entry</span></span> | <span data-ttu-id="449aa-209">Wert</span><span class="sxs-lookup"><span data-stu-id="449aa-209">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="449aa-210">Link-ID</span><span class="sxs-lookup"><span data-stu-id="449aa-210">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="449aa-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="449aa-211">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="449aa-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="449aa-212">System-Only</span></span>            | <span data-ttu-id="449aa-213">False</span><span class="sxs-lookup"><span data-stu-id="449aa-213">False</span></span>                                      |
| <span data-ttu-id="449aa-214">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="449aa-214">Is-Single-Valued</span></span>       | <span data-ttu-id="449aa-215">Richtig</span><span class="sxs-lookup"><span data-stu-id="449aa-215">True</span></span>                                       |
| <span data-ttu-id="449aa-216">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="449aa-216">Is Indexed</span></span>             | <span data-ttu-id="449aa-217">False</span><span class="sxs-lookup"><span data-stu-id="449aa-217">False</span></span>                                      |
| <span data-ttu-id="449aa-218">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="449aa-218">In Global Catalog</span></span>      | <span data-ttu-id="449aa-219">False</span><span class="sxs-lookup"><span data-stu-id="449aa-219">False</span></span>                                      |
| <span data-ttu-id="449aa-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="449aa-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="449aa-221">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="449aa-221">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="449aa-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="449aa-222">Range-Lower</span></span>            | <span data-ttu-id="449aa-223">0</span><span class="sxs-lookup"><span data-stu-id="449aa-223">0</span></span>                                          |
| <span data-ttu-id="449aa-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="449aa-224">Range-Upper</span></span>            | <span data-ttu-id="449aa-225">255</span><span class="sxs-lookup"><span data-stu-id="449aa-225">255</span></span>                                        |
| <span data-ttu-id="449aa-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="449aa-226">Search-Flags</span></span>           | <span data-ttu-id="449aa-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="449aa-227">0x00000000</span></span>                                 |
| <span data-ttu-id="449aa-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="449aa-228">System-Flags</span></span>           | <span data-ttu-id="449aa-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="449aa-229">0x00000010</span></span>                                 |
| <span data-ttu-id="449aa-230">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="449aa-230">Classes used in</span></span>        | [<span data-ttu-id="449aa-231">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="449aa-231">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="449aa-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="449aa-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="449aa-233">Eingabe</span><span class="sxs-lookup"><span data-stu-id="449aa-233">Entry</span></span> | <span data-ttu-id="449aa-234">Wert</span><span class="sxs-lookup"><span data-stu-id="449aa-234">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="449aa-235">Link-ID</span><span class="sxs-lookup"><span data-stu-id="449aa-235">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="449aa-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="449aa-236">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="449aa-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="449aa-237">System-Only</span></span>            | <span data-ttu-id="449aa-238">False</span><span class="sxs-lookup"><span data-stu-id="449aa-238">False</span></span>                                      |
| <span data-ttu-id="449aa-239">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="449aa-239">Is-Single-Valued</span></span>       | <span data-ttu-id="449aa-240">Richtig</span><span class="sxs-lookup"><span data-stu-id="449aa-240">True</span></span>                                       |
| <span data-ttu-id="449aa-241">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="449aa-241">Is Indexed</span></span>             | <span data-ttu-id="449aa-242">False</span><span class="sxs-lookup"><span data-stu-id="449aa-242">False</span></span>                                      |
| <span data-ttu-id="449aa-243">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="449aa-243">In Global Catalog</span></span>      | <span data-ttu-id="449aa-244">False</span><span class="sxs-lookup"><span data-stu-id="449aa-244">False</span></span>                                      |
| <span data-ttu-id="449aa-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="449aa-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="449aa-246">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="449aa-246">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="449aa-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="449aa-247">Range-Lower</span></span>            | <span data-ttu-id="449aa-248">0</span><span class="sxs-lookup"><span data-stu-id="449aa-248">0</span></span>                                          |
| <span data-ttu-id="449aa-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="449aa-249">Range-Upper</span></span>            | <span data-ttu-id="449aa-250">255</span><span class="sxs-lookup"><span data-stu-id="449aa-250">255</span></span>                                        |
| <span data-ttu-id="449aa-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="449aa-251">Search-Flags</span></span>           | <span data-ttu-id="449aa-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="449aa-252">0x00000000</span></span>                                 |
| <span data-ttu-id="449aa-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="449aa-253">System-Flags</span></span>           | <span data-ttu-id="449aa-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="449aa-254">0x00000010</span></span>                                 |
| <span data-ttu-id="449aa-255">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="449aa-255">Classes used in</span></span>        | [<span data-ttu-id="449aa-256">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="449aa-256">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="449aa-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="449aa-257">Windows Server 2012</span></span>



| <span data-ttu-id="449aa-258">Eingabe</span><span class="sxs-lookup"><span data-stu-id="449aa-258">Entry</span></span> | <span data-ttu-id="449aa-259">Wert</span><span class="sxs-lookup"><span data-stu-id="449aa-259">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="449aa-260">Link-ID</span><span class="sxs-lookup"><span data-stu-id="449aa-260">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="449aa-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="449aa-261">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="449aa-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="449aa-262">System-Only</span></span>            | <span data-ttu-id="449aa-263">False</span><span class="sxs-lookup"><span data-stu-id="449aa-263">False</span></span>                                      |
| <span data-ttu-id="449aa-264">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="449aa-264">Is-Single-Valued</span></span>       | <span data-ttu-id="449aa-265">Richtig</span><span class="sxs-lookup"><span data-stu-id="449aa-265">True</span></span>                                       |
| <span data-ttu-id="449aa-266">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="449aa-266">Is Indexed</span></span>             | <span data-ttu-id="449aa-267">False</span><span class="sxs-lookup"><span data-stu-id="449aa-267">False</span></span>                                      |
| <span data-ttu-id="449aa-268">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="449aa-268">In Global Catalog</span></span>      | <span data-ttu-id="449aa-269">False</span><span class="sxs-lookup"><span data-stu-id="449aa-269">False</span></span>                                      |
| <span data-ttu-id="449aa-270">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="449aa-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="449aa-271">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="449aa-271">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="449aa-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="449aa-272">Range-Lower</span></span>            | <span data-ttu-id="449aa-273">0</span><span class="sxs-lookup"><span data-stu-id="449aa-273">0</span></span>                                          |
| <span data-ttu-id="449aa-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="449aa-274">Range-Upper</span></span>            | <span data-ttu-id="449aa-275">255</span><span class="sxs-lookup"><span data-stu-id="449aa-275">255</span></span>                                        |
| <span data-ttu-id="449aa-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="449aa-276">Search-Flags</span></span>           | <span data-ttu-id="449aa-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="449aa-277">0x00000000</span></span>                                 |
| <span data-ttu-id="449aa-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="449aa-278">System-Flags</span></span>           | <span data-ttu-id="449aa-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="449aa-279">0x00000010</span></span>                                 |
| <span data-ttu-id="449aa-280">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="449aa-280">Classes used in</span></span>        | [<span data-ttu-id="449aa-281">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="449aa-281">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





