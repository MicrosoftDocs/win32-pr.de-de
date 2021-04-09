---
title: ms-DS-NC-Replikat-Locations-Attribut
description: Eine Liste der Server, die als Replikat für den entsprechenden nicht-Domänen namens Kontext festgelegt sind.
ms.assetid: b0379bb6-feee-432a-b484-1a6c8100d027
ms.tgt_platform: multiple
keywords:
- AD-Schema für das Attribut "ms-DS-NC-Replica-Locations"
- "\"msDS-NC-Replikat-Locations\"-Attribut AD Schema"
topic_type:
- apiref
api_name:
- ms-DS-NC-Replica-Locations
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4adc3d3ca3553c8e57cdc114eb045206c1501060
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957634"
---
# <a name="ms-ds-nc-replica-locations-attribute"></a><span data-ttu-id="c8471-105">ms-DS-NC-Replikat-Locations-Attribut</span><span class="sxs-lookup"><span data-stu-id="c8471-105">ms-DS-NC-Replica-Locations attribute</span></span>

<span data-ttu-id="c8471-106">Eine Liste der Server, die als Replikat für den entsprechenden nicht-Domänen namens Kontext festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="c8471-106">A list of servers that are the replica set for the corresponding Non-Domain Naming Context.</span></span>



| <span data-ttu-id="c8471-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c8471-107">Entry</span></span> | <span data-ttu-id="c8471-108">Wert</span><span class="sxs-lookup"><span data-stu-id="c8471-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="c8471-109">CN</span><span class="sxs-lookup"><span data-stu-id="c8471-109">CN</span></span>                | <span data-ttu-id="c8471-110">ms-DS-NC-Replikat-Standorte</span><span class="sxs-lookup"><span data-stu-id="c8471-110">ms-DS-NC-Replica-Locations</span></span>              |
| <span data-ttu-id="c8471-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c8471-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c8471-112">MSDS-NC-Replikat-Standorte</span><span class="sxs-lookup"><span data-stu-id="c8471-112">msDS-NC-Replica-Locations</span></span>               |
| <span data-ttu-id="c8471-113">Size</span><span class="sxs-lookup"><span data-stu-id="c8471-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="c8471-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c8471-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="c8471-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="c8471-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="c8471-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c8471-116">Attribute-Id</span></span>      | <span data-ttu-id="c8471-117">1.2.840.113556.1.4.1661</span><span class="sxs-lookup"><span data-stu-id="c8471-117">1.2.840.113556.1.4.1661</span></span>                 |
| <span data-ttu-id="c8471-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c8471-118">System-Id-Guid</span></span>    | <span data-ttu-id="c8471-119">97de9615-B537-46bc-ac0b-10720f 3909f</span><span class="sxs-lookup"><span data-stu-id="c8471-119">97de9615-b537-46bc-ac0f-10720f3909f3</span></span>    |
| <span data-ttu-id="c8471-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8471-120">Syntax</span></span>            | [<span data-ttu-id="c8471-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="c8471-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="c8471-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="c8471-122">Implementations</span></span>

-   [<span data-ttu-id="c8471-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c8471-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c8471-124">**Adam**</span><span class="sxs-lookup"><span data-stu-id="c8471-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c8471-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c8471-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c8471-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c8471-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c8471-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c8471-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c8471-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c8471-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c8471-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c8471-129">Windows Server 2003</span></span>



| <span data-ttu-id="c8471-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c8471-130">Entry</span></span> | <span data-ttu-id="c8471-131">Wert</span><span class="sxs-lookup"><span data-stu-id="c8471-131">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="c8471-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c8471-132">Link-Id</span></span>                | <span data-ttu-id="c8471-133">1044</span><span class="sxs-lookup"><span data-stu-id="c8471-133">1044</span></span>                                       |
| <span data-ttu-id="c8471-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8471-134">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="c8471-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8471-135">System-Only</span></span>            | <span data-ttu-id="c8471-136">False</span><span class="sxs-lookup"><span data-stu-id="c8471-136">False</span></span>                                      |
| <span data-ttu-id="c8471-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c8471-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c8471-138">False</span><span class="sxs-lookup"><span data-stu-id="c8471-138">False</span></span>                                      |
| <span data-ttu-id="c8471-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c8471-139">Is Indexed</span></span>             | <span data-ttu-id="c8471-140">False</span><span class="sxs-lookup"><span data-stu-id="c8471-140">False</span></span>                                      |
| <span data-ttu-id="c8471-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c8471-141">In Global Catalog</span></span>      | <span data-ttu-id="c8471-142">False</span><span class="sxs-lookup"><span data-stu-id="c8471-142">False</span></span>                                      |
| <span data-ttu-id="c8471-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c8471-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8471-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c8471-144">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="c8471-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8471-145">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="c8471-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8471-146">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="c8471-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8471-147">Search-Flags</span></span>           | <span data-ttu-id="c8471-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8471-148">0x00000000</span></span>                                 |
| <span data-ttu-id="c8471-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8471-149">System-Flags</span></span>           | <span data-ttu-id="c8471-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8471-150">0x00000010</span></span>                                 |
| <span data-ttu-id="c8471-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c8471-151">Classes used in</span></span>        | [<span data-ttu-id="c8471-152">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="c8471-152">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c8471-153">Adam</span><span class="sxs-lookup"><span data-stu-id="c8471-153">ADAM</span></span>



| <span data-ttu-id="c8471-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c8471-154">Entry</span></span> | <span data-ttu-id="c8471-155">Wert</span><span class="sxs-lookup"><span data-stu-id="c8471-155">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="c8471-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c8471-156">Link-Id</span></span>                | <span data-ttu-id="c8471-157">1044</span><span class="sxs-lookup"><span data-stu-id="c8471-157">1044</span></span>                                       |
| <span data-ttu-id="c8471-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8471-158">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="c8471-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8471-159">System-Only</span></span>            | <span data-ttu-id="c8471-160">False</span><span class="sxs-lookup"><span data-stu-id="c8471-160">False</span></span>                                      |
| <span data-ttu-id="c8471-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c8471-161">Is-Single-Valued</span></span>       | <span data-ttu-id="c8471-162">False</span><span class="sxs-lookup"><span data-stu-id="c8471-162">False</span></span>                                      |
| <span data-ttu-id="c8471-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c8471-163">Is Indexed</span></span>             | <span data-ttu-id="c8471-164">False</span><span class="sxs-lookup"><span data-stu-id="c8471-164">False</span></span>                                      |
| <span data-ttu-id="c8471-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c8471-165">In Global Catalog</span></span>      | <span data-ttu-id="c8471-166">False</span><span class="sxs-lookup"><span data-stu-id="c8471-166">False</span></span>                                      |
| <span data-ttu-id="c8471-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c8471-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8471-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c8471-168">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="c8471-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8471-169">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="c8471-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8471-170">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="c8471-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8471-171">Search-Flags</span></span>           | <span data-ttu-id="c8471-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8471-172">0x00000000</span></span>                                 |
| <span data-ttu-id="c8471-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8471-173">System-Flags</span></span>           | <span data-ttu-id="c8471-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8471-174">0x00000010</span></span>                                 |
| <span data-ttu-id="c8471-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c8471-175">Classes used in</span></span>        | [<span data-ttu-id="c8471-176">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="c8471-176">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c8471-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c8471-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c8471-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c8471-178">Entry</span></span> | <span data-ttu-id="c8471-179">Wert</span><span class="sxs-lookup"><span data-stu-id="c8471-179">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="c8471-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c8471-180">Link-Id</span></span>                | <span data-ttu-id="c8471-181">1044</span><span class="sxs-lookup"><span data-stu-id="c8471-181">1044</span></span>                                       |
| <span data-ttu-id="c8471-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8471-182">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="c8471-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8471-183">System-Only</span></span>            | <span data-ttu-id="c8471-184">False</span><span class="sxs-lookup"><span data-stu-id="c8471-184">False</span></span>                                      |
| <span data-ttu-id="c8471-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c8471-185">Is-Single-Valued</span></span>       | <span data-ttu-id="c8471-186">False</span><span class="sxs-lookup"><span data-stu-id="c8471-186">False</span></span>                                      |
| <span data-ttu-id="c8471-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c8471-187">Is Indexed</span></span>             | <span data-ttu-id="c8471-188">False</span><span class="sxs-lookup"><span data-stu-id="c8471-188">False</span></span>                                      |
| <span data-ttu-id="c8471-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c8471-189">In Global Catalog</span></span>      | <span data-ttu-id="c8471-190">False</span><span class="sxs-lookup"><span data-stu-id="c8471-190">False</span></span>                                      |
| <span data-ttu-id="c8471-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c8471-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8471-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c8471-192">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="c8471-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8471-193">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="c8471-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8471-194">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="c8471-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8471-195">Search-Flags</span></span>           | <span data-ttu-id="c8471-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8471-196">0x00000000</span></span>                                 |
| <span data-ttu-id="c8471-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8471-197">System-Flags</span></span>           | <span data-ttu-id="c8471-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8471-198">0x00000010</span></span>                                 |
| <span data-ttu-id="c8471-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c8471-199">Classes used in</span></span>        | [<span data-ttu-id="c8471-200">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="c8471-200">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c8471-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8471-201">Windows Server 2008</span></span>



| <span data-ttu-id="c8471-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c8471-202">Entry</span></span> | <span data-ttu-id="c8471-203">Wert</span><span class="sxs-lookup"><span data-stu-id="c8471-203">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="c8471-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c8471-204">Link-Id</span></span>                | <span data-ttu-id="c8471-205">1044</span><span class="sxs-lookup"><span data-stu-id="c8471-205">1044</span></span>                                       |
| <span data-ttu-id="c8471-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8471-206">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="c8471-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8471-207">System-Only</span></span>            | <span data-ttu-id="c8471-208">False</span><span class="sxs-lookup"><span data-stu-id="c8471-208">False</span></span>                                      |
| <span data-ttu-id="c8471-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c8471-209">Is-Single-Valued</span></span>       | <span data-ttu-id="c8471-210">False</span><span class="sxs-lookup"><span data-stu-id="c8471-210">False</span></span>                                      |
| <span data-ttu-id="c8471-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c8471-211">Is Indexed</span></span>             | <span data-ttu-id="c8471-212">False</span><span class="sxs-lookup"><span data-stu-id="c8471-212">False</span></span>                                      |
| <span data-ttu-id="c8471-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c8471-213">In Global Catalog</span></span>      | <span data-ttu-id="c8471-214">False</span><span class="sxs-lookup"><span data-stu-id="c8471-214">False</span></span>                                      |
| <span data-ttu-id="c8471-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c8471-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8471-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c8471-216">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="c8471-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8471-217">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="c8471-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8471-218">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="c8471-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8471-219">Search-Flags</span></span>           | <span data-ttu-id="c8471-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8471-220">0x00000000</span></span>                                 |
| <span data-ttu-id="c8471-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8471-221">System-Flags</span></span>           | <span data-ttu-id="c8471-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8471-222">0x00000010</span></span>                                 |
| <span data-ttu-id="c8471-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c8471-223">Classes used in</span></span>        | [<span data-ttu-id="c8471-224">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="c8471-224">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c8471-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c8471-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c8471-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c8471-226">Entry</span></span> | <span data-ttu-id="c8471-227">Wert</span><span class="sxs-lookup"><span data-stu-id="c8471-227">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="c8471-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c8471-228">Link-Id</span></span>                | <span data-ttu-id="c8471-229">1044</span><span class="sxs-lookup"><span data-stu-id="c8471-229">1044</span></span>                                       |
| <span data-ttu-id="c8471-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8471-230">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="c8471-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8471-231">System-Only</span></span>            | <span data-ttu-id="c8471-232">False</span><span class="sxs-lookup"><span data-stu-id="c8471-232">False</span></span>                                      |
| <span data-ttu-id="c8471-233">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c8471-233">Is-Single-Valued</span></span>       | <span data-ttu-id="c8471-234">False</span><span class="sxs-lookup"><span data-stu-id="c8471-234">False</span></span>                                      |
| <span data-ttu-id="c8471-235">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c8471-235">Is Indexed</span></span>             | <span data-ttu-id="c8471-236">False</span><span class="sxs-lookup"><span data-stu-id="c8471-236">False</span></span>                                      |
| <span data-ttu-id="c8471-237">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c8471-237">In Global Catalog</span></span>      | <span data-ttu-id="c8471-238">False</span><span class="sxs-lookup"><span data-stu-id="c8471-238">False</span></span>                                      |
| <span data-ttu-id="c8471-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c8471-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8471-240">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c8471-240">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="c8471-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8471-241">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="c8471-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8471-242">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="c8471-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8471-243">Search-Flags</span></span>           | <span data-ttu-id="c8471-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8471-244">0x00000000</span></span>                                 |
| <span data-ttu-id="c8471-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8471-245">System-Flags</span></span>           | <span data-ttu-id="c8471-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8471-246">0x00000010</span></span>                                 |
| <span data-ttu-id="c8471-247">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c8471-247">Classes used in</span></span>        | [<span data-ttu-id="c8471-248">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="c8471-248">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c8471-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c8471-249">Windows Server 2012</span></span>



| <span data-ttu-id="c8471-250">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c8471-250">Entry</span></span> | <span data-ttu-id="c8471-251">Wert</span><span class="sxs-lookup"><span data-stu-id="c8471-251">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="c8471-252">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c8471-252">Link-Id</span></span>                | <span data-ttu-id="c8471-253">1044</span><span class="sxs-lookup"><span data-stu-id="c8471-253">1044</span></span>                                       |
| <span data-ttu-id="c8471-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8471-254">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="c8471-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8471-255">System-Only</span></span>            | <span data-ttu-id="c8471-256">False</span><span class="sxs-lookup"><span data-stu-id="c8471-256">False</span></span>                                      |
| <span data-ttu-id="c8471-257">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c8471-257">Is-Single-Valued</span></span>       | <span data-ttu-id="c8471-258">False</span><span class="sxs-lookup"><span data-stu-id="c8471-258">False</span></span>                                      |
| <span data-ttu-id="c8471-259">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c8471-259">Is Indexed</span></span>             | <span data-ttu-id="c8471-260">False</span><span class="sxs-lookup"><span data-stu-id="c8471-260">False</span></span>                                      |
| <span data-ttu-id="c8471-261">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c8471-261">In Global Catalog</span></span>      | <span data-ttu-id="c8471-262">False</span><span class="sxs-lookup"><span data-stu-id="c8471-262">False</span></span>                                      |
| <span data-ttu-id="c8471-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c8471-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8471-264">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c8471-264">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="c8471-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8471-265">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="c8471-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8471-266">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="c8471-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8471-267">Search-Flags</span></span>           | <span data-ttu-id="c8471-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8471-268">0x00000000</span></span>                                 |
| <span data-ttu-id="c8471-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8471-269">System-Flags</span></span>           | <span data-ttu-id="c8471-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8471-270">0x00000010</span></span>                                 |
| <span data-ttu-id="c8471-271">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c8471-271">Classes used in</span></span>        | [<span data-ttu-id="c8471-272">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="c8471-272">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





