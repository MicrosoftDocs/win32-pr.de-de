---
title: GPC-WQL-Filter-Attribut
description: Wird verwendet, um eine Zeichenfolge zu speichern, die eine GUID für den Filter und einen WMI-Namespace Pfad enthält.
ms.assetid: ea76239b-79e2-49b2-a848-a924450d332a
ms.tgt_platform: multiple
keywords:
- GPC-WQL-Filter Attribut AD-Schema
- AD-Schema des GpcWQLFilter-Attributs
topic_type:
- apiref
api_name:
- GPC-WQL-Filter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c9a6b8d3715c1692e93579d3c94cdfa44f4192e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859731"
---
# <a name="gpc-wql-filter-attribute"></a><span data-ttu-id="09d2f-105">GPC-WQL-Filter-Attribut</span><span class="sxs-lookup"><span data-stu-id="09d2f-105">GPC-WQL-Filter attribute</span></span>

<span data-ttu-id="09d2f-106">Wird verwendet, um eine Zeichenfolge zu speichern, die eine GUID für den Filter und einen WMI-Namespace Pfad enthält.</span><span class="sxs-lookup"><span data-stu-id="09d2f-106">Used to store a string that contains a GUID for the filter and a WMI namespace path.</span></span>



| <span data-ttu-id="09d2f-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="09d2f-107">Entry</span></span> | <span data-ttu-id="09d2f-108">Wert</span><span class="sxs-lookup"><span data-stu-id="09d2f-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="09d2f-109">CN</span><span class="sxs-lookup"><span data-stu-id="09d2f-109">CN</span></span>                | <span data-ttu-id="09d2f-110">GPC-WQL-Filter</span><span class="sxs-lookup"><span data-stu-id="09d2f-110">GPC-WQL-Filter</span></span>                                                                  |
| <span data-ttu-id="09d2f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="09d2f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="09d2f-112">GpcWQLFilter</span><span class="sxs-lookup"><span data-stu-id="09d2f-112">gPCWQLFilter</span></span>                                                                    |
| <span data-ttu-id="09d2f-113">Size</span><span class="sxs-lookup"><span data-stu-id="09d2f-113">Size</span></span>              | \-                                                                              |
| <span data-ttu-id="09d2f-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="09d2f-114">Update Privilege</span></span>  | <span data-ttu-id="09d2f-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="09d2f-115">Domain administrator</span></span>                                                            |
| <span data-ttu-id="09d2f-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="09d2f-116">Update Frequency</span></span>  | <span data-ttu-id="09d2f-117">Nur, wenn der Administrator die Filter-Eigenschaft in der Gruppenrichtlinie-Benutzeroberfläche ändert.</span><span class="sxs-lookup"><span data-stu-id="09d2f-117">Only when the administrator changes the filter property in the Group Policy UI.</span></span> |
| <span data-ttu-id="09d2f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="09d2f-118">Attribute-Id</span></span>      | <span data-ttu-id="09d2f-119">1.2.840.113556.1.4.1694</span><span class="sxs-lookup"><span data-stu-id="09d2f-119">1.2.840.113556.1.4.1694</span></span>                                                         |
| <span data-ttu-id="09d2f-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="09d2f-120">System-Id-Guid</span></span>    | <span data-ttu-id="09d2f-121">7bd4c7a6-1ADD-4436-8c04-3999a880154c</span><span class="sxs-lookup"><span data-stu-id="09d2f-121">7bd4c7a6-1add-4436-8c04-3999a880154c</span></span>                                            |
| <span data-ttu-id="09d2f-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="09d2f-122">Syntax</span></span>            | [<span data-ttu-id="09d2f-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="09d2f-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                     |



## <a name="implementations"></a><span data-ttu-id="09d2f-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="09d2f-124">Implementations</span></span>

-   [<span data-ttu-id="09d2f-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="09d2f-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="09d2f-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="09d2f-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="09d2f-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="09d2f-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="09d2f-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="09d2f-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="09d2f-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="09d2f-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="09d2f-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="09d2f-130">Windows Server 2003</span></span>



| <span data-ttu-id="09d2f-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="09d2f-131">Entry</span></span> | <span data-ttu-id="09d2f-132">Wert</span><span class="sxs-lookup"><span data-stu-id="09d2f-132">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="09d2f-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="09d2f-133">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="09d2f-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09d2f-134">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="09d2f-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="09d2f-135">System-Only</span></span>            | <span data-ttu-id="09d2f-136">False</span><span class="sxs-lookup"><span data-stu-id="09d2f-136">False</span></span>                                                               |
| <span data-ttu-id="09d2f-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="09d2f-137">Is-Single-Valued</span></span>       | <span data-ttu-id="09d2f-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="09d2f-138">True</span></span>                                                                |
| <span data-ttu-id="09d2f-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="09d2f-139">Is Indexed</span></span>             | <span data-ttu-id="09d2f-140">False</span><span class="sxs-lookup"><span data-stu-id="09d2f-140">False</span></span>                                                               |
| <span data-ttu-id="09d2f-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="09d2f-141">In Global Catalog</span></span>      | <span data-ttu-id="09d2f-142">False</span><span class="sxs-lookup"><span data-stu-id="09d2f-142">False</span></span>                                                               |
| <span data-ttu-id="09d2f-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="09d2f-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="09d2f-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="09d2f-144">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="09d2f-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09d2f-145">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="09d2f-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09d2f-146">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="09d2f-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09d2f-147">Search-Flags</span></span>           | <span data-ttu-id="09d2f-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09d2f-148">0x00000000</span></span>                                                          |
| <span data-ttu-id="09d2f-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09d2f-149">System-Flags</span></span>           | <span data-ttu-id="09d2f-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09d2f-150">0x00000010</span></span>                                                          |
| <span data-ttu-id="09d2f-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="09d2f-151">Classes used in</span></span>        | [<span data-ttu-id="09d2f-152">**Gruppenrichtlinien Container**</span><span class="sxs-lookup"><span data-stu-id="09d2f-152">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="09d2f-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="09d2f-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="09d2f-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="09d2f-154">Entry</span></span> | <span data-ttu-id="09d2f-155">Wert</span><span class="sxs-lookup"><span data-stu-id="09d2f-155">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="09d2f-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="09d2f-156">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="09d2f-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09d2f-157">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="09d2f-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="09d2f-158">System-Only</span></span>            | <span data-ttu-id="09d2f-159">False</span><span class="sxs-lookup"><span data-stu-id="09d2f-159">False</span></span>                                                               |
| <span data-ttu-id="09d2f-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="09d2f-160">Is-Single-Valued</span></span>       | <span data-ttu-id="09d2f-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="09d2f-161">True</span></span>                                                                |
| <span data-ttu-id="09d2f-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="09d2f-162">Is Indexed</span></span>             | <span data-ttu-id="09d2f-163">False</span><span class="sxs-lookup"><span data-stu-id="09d2f-163">False</span></span>                                                               |
| <span data-ttu-id="09d2f-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="09d2f-164">In Global Catalog</span></span>      | <span data-ttu-id="09d2f-165">False</span><span class="sxs-lookup"><span data-stu-id="09d2f-165">False</span></span>                                                               |
| <span data-ttu-id="09d2f-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="09d2f-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="09d2f-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="09d2f-167">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="09d2f-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09d2f-168">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="09d2f-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09d2f-169">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="09d2f-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09d2f-170">Search-Flags</span></span>           | <span data-ttu-id="09d2f-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09d2f-171">0x00000000</span></span>                                                          |
| <span data-ttu-id="09d2f-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09d2f-172">System-Flags</span></span>           | <span data-ttu-id="09d2f-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09d2f-173">0x00000010</span></span>                                                          |
| <span data-ttu-id="09d2f-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="09d2f-174">Classes used in</span></span>        | [<span data-ttu-id="09d2f-175">**Gruppenrichtlinien Container**</span><span class="sxs-lookup"><span data-stu-id="09d2f-175">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="09d2f-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09d2f-176">Windows Server 2008</span></span>



| <span data-ttu-id="09d2f-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="09d2f-177">Entry</span></span> | <span data-ttu-id="09d2f-178">Wert</span><span class="sxs-lookup"><span data-stu-id="09d2f-178">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="09d2f-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="09d2f-179">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="09d2f-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09d2f-180">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="09d2f-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="09d2f-181">System-Only</span></span>            | <span data-ttu-id="09d2f-182">False</span><span class="sxs-lookup"><span data-stu-id="09d2f-182">False</span></span>                                                               |
| <span data-ttu-id="09d2f-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="09d2f-183">Is-Single-Valued</span></span>       | <span data-ttu-id="09d2f-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="09d2f-184">True</span></span>                                                                |
| <span data-ttu-id="09d2f-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="09d2f-185">Is Indexed</span></span>             | <span data-ttu-id="09d2f-186">False</span><span class="sxs-lookup"><span data-stu-id="09d2f-186">False</span></span>                                                               |
| <span data-ttu-id="09d2f-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="09d2f-187">In Global Catalog</span></span>      | <span data-ttu-id="09d2f-188">False</span><span class="sxs-lookup"><span data-stu-id="09d2f-188">False</span></span>                                                               |
| <span data-ttu-id="09d2f-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="09d2f-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="09d2f-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="09d2f-190">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="09d2f-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09d2f-191">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="09d2f-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09d2f-192">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="09d2f-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09d2f-193">Search-Flags</span></span>           | <span data-ttu-id="09d2f-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09d2f-194">0x00000000</span></span>                                                          |
| <span data-ttu-id="09d2f-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09d2f-195">System-Flags</span></span>           | <span data-ttu-id="09d2f-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09d2f-196">0x00000010</span></span>                                                          |
| <span data-ttu-id="09d2f-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="09d2f-197">Classes used in</span></span>        | [<span data-ttu-id="09d2f-198">**Gruppenrichtlinien Container**</span><span class="sxs-lookup"><span data-stu-id="09d2f-198">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="09d2f-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="09d2f-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="09d2f-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="09d2f-200">Entry</span></span> | <span data-ttu-id="09d2f-201">Wert</span><span class="sxs-lookup"><span data-stu-id="09d2f-201">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="09d2f-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="09d2f-202">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="09d2f-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09d2f-203">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="09d2f-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="09d2f-204">System-Only</span></span>            | <span data-ttu-id="09d2f-205">False</span><span class="sxs-lookup"><span data-stu-id="09d2f-205">False</span></span>                                                               |
| <span data-ttu-id="09d2f-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="09d2f-206">Is-Single-Valued</span></span>       | <span data-ttu-id="09d2f-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="09d2f-207">True</span></span>                                                                |
| <span data-ttu-id="09d2f-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="09d2f-208">Is Indexed</span></span>             | <span data-ttu-id="09d2f-209">False</span><span class="sxs-lookup"><span data-stu-id="09d2f-209">False</span></span>                                                               |
| <span data-ttu-id="09d2f-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="09d2f-210">In Global Catalog</span></span>      | <span data-ttu-id="09d2f-211">False</span><span class="sxs-lookup"><span data-stu-id="09d2f-211">False</span></span>                                                               |
| <span data-ttu-id="09d2f-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="09d2f-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="09d2f-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="09d2f-213">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="09d2f-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09d2f-214">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="09d2f-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09d2f-215">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="09d2f-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09d2f-216">Search-Flags</span></span>           | <span data-ttu-id="09d2f-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09d2f-217">0x00000000</span></span>                                                          |
| <span data-ttu-id="09d2f-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09d2f-218">System-Flags</span></span>           | <span data-ttu-id="09d2f-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09d2f-219">0x00000010</span></span>                                                          |
| <span data-ttu-id="09d2f-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="09d2f-220">Classes used in</span></span>        | [<span data-ttu-id="09d2f-221">**Gruppenrichtlinien Container**</span><span class="sxs-lookup"><span data-stu-id="09d2f-221">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="09d2f-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="09d2f-222">Windows Server 2012</span></span>



| <span data-ttu-id="09d2f-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="09d2f-223">Entry</span></span> | <span data-ttu-id="09d2f-224">Wert</span><span class="sxs-lookup"><span data-stu-id="09d2f-224">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="09d2f-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="09d2f-225">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="09d2f-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09d2f-226">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="09d2f-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="09d2f-227">System-Only</span></span>            | <span data-ttu-id="09d2f-228">False</span><span class="sxs-lookup"><span data-stu-id="09d2f-228">False</span></span>                                                               |
| <span data-ttu-id="09d2f-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="09d2f-229">Is-Single-Valued</span></span>       | <span data-ttu-id="09d2f-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="09d2f-230">True</span></span>                                                                |
| <span data-ttu-id="09d2f-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="09d2f-231">Is Indexed</span></span>             | <span data-ttu-id="09d2f-232">False</span><span class="sxs-lookup"><span data-stu-id="09d2f-232">False</span></span>                                                               |
| <span data-ttu-id="09d2f-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="09d2f-233">In Global Catalog</span></span>      | <span data-ttu-id="09d2f-234">False</span><span class="sxs-lookup"><span data-stu-id="09d2f-234">False</span></span>                                                               |
| <span data-ttu-id="09d2f-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="09d2f-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="09d2f-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="09d2f-236">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="09d2f-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09d2f-237">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="09d2f-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09d2f-238">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="09d2f-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09d2f-239">Search-Flags</span></span>           | <span data-ttu-id="09d2f-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09d2f-240">0x00000000</span></span>                                                          |
| <span data-ttu-id="09d2f-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09d2f-241">System-Flags</span></span>           | <span data-ttu-id="09d2f-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09d2f-242">0x00000010</span></span>                                                          |
| <span data-ttu-id="09d2f-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="09d2f-243">Classes used in</span></span>        | [<span data-ttu-id="09d2f-244">**Gruppenrichtlinien Container**</span><span class="sxs-lookup"><span data-stu-id="09d2f-244">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



 

 





