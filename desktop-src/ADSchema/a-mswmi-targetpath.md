---
title: MS-WMI-TargetPath-Attribut
description: Liste der Schlüssel-Wert-Paare zum eindeutigen Identifizieren eines WMI-Objekts.
ms.assetid: b5d6c718-86f6-40a5-8fb1-e3ed4821ac62
ms.tgt_platform: multiple
keywords:
- AD-Schema für MS-WMI-TargetPath-Attribut
- AD-Schema für das mswap-TargetPath-Attribut
topic_type:
- apiref
api_name:
- ms-WMI-TargetPath
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9818125d757716970cff538167d5d737a8354555
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957466"
---
# <a name="ms-wmi-targetpath-attribute"></a><span data-ttu-id="aca2a-105">MS-WMI-TargetPath-Attribut</span><span class="sxs-lookup"><span data-stu-id="aca2a-105">ms-WMI-TargetPath attribute</span></span>

<span data-ttu-id="aca2a-106">Liste der Schlüssel-Wert-Paare zum eindeutigen Identifizieren eines WMI-Objekts.</span><span class="sxs-lookup"><span data-stu-id="aca2a-106">List of key/value pairs for uniquely identifying a WMI object.</span></span>



| <span data-ttu-id="aca2a-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aca2a-107">Entry</span></span> | <span data-ttu-id="aca2a-108">Wert</span><span class="sxs-lookup"><span data-stu-id="aca2a-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="aca2a-109">CN</span><span class="sxs-lookup"><span data-stu-id="aca2a-109">CN</span></span>                | <span data-ttu-id="aca2a-110">MS-WMI-TargetPath</span><span class="sxs-lookup"><span data-stu-id="aca2a-110">ms-WMI-TargetPath</span></span>                           |
| <span data-ttu-id="aca2a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="aca2a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="aca2a-112">mswap-TargetPath</span><span class="sxs-lookup"><span data-stu-id="aca2a-112">msWMI-TargetPath</span></span>                            |
| <span data-ttu-id="aca2a-113">Size</span><span class="sxs-lookup"><span data-stu-id="aca2a-113">Size</span></span>              | <span data-ttu-id="aca2a-114">Weniger als 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="aca2a-114">Less than 100 characters.</span></span>                   |
| <span data-ttu-id="aca2a-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="aca2a-115">Update Privilege</span></span>  | <span data-ttu-id="aca2a-116">Gruppenrichtlinie-Administrator</span><span class="sxs-lookup"><span data-stu-id="aca2a-116">Group Policy Administrator</span></span>                  |
| <span data-ttu-id="aca2a-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="aca2a-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="aca2a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="aca2a-118">Attribute-Id</span></span>      | <span data-ttu-id="aca2a-119">1.2.840.113556.1.4.1648</span><span class="sxs-lookup"><span data-stu-id="aca2a-119">1.2.840.113556.1.4.1648</span></span>                     |
| <span data-ttu-id="aca2a-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="aca2a-120">System-Id-Guid</span></span>    | <span data-ttu-id="aca2a-121">5006a79a-6bfe-4561-9f52-13cf4dd3e560</span><span class="sxs-lookup"><span data-stu-id="aca2a-121">5006a79a-6bfe-4561-9f52-13cf4dd3e560</span></span>        |
| <span data-ttu-id="aca2a-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="aca2a-122">Syntax</span></span>            | [<span data-ttu-id="aca2a-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="aca2a-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="aca2a-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="aca2a-124">Implementations</span></span>

-   [<span data-ttu-id="aca2a-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="aca2a-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="aca2a-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="aca2a-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="aca2a-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="aca2a-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="aca2a-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="aca2a-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="aca2a-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="aca2a-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="aca2a-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aca2a-130">Windows Server 2003</span></span>



| <span data-ttu-id="aca2a-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aca2a-131">Entry</span></span> | <span data-ttu-id="aca2a-132">Wert</span><span class="sxs-lookup"><span data-stu-id="aca2a-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="aca2a-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="aca2a-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="aca2a-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aca2a-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="aca2a-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="aca2a-135">System-Only</span></span>            | <span data-ttu-id="aca2a-136">False</span><span class="sxs-lookup"><span data-stu-id="aca2a-136">False</span></span>                                                              |
| <span data-ttu-id="aca2a-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="aca2a-137">Is-Single-Valued</span></span>       | <span data-ttu-id="aca2a-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="aca2a-138">True</span></span>                                                               |
| <span data-ttu-id="aca2a-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="aca2a-139">Is Indexed</span></span>             | <span data-ttu-id="aca2a-140">False</span><span class="sxs-lookup"><span data-stu-id="aca2a-140">False</span></span>                                                              |
| <span data-ttu-id="aca2a-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="aca2a-141">In Global Catalog</span></span>      | <span data-ttu-id="aca2a-142">False</span><span class="sxs-lookup"><span data-stu-id="aca2a-142">False</span></span>                                                              |
| <span data-ttu-id="aca2a-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aca2a-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="aca2a-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="aca2a-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="aca2a-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aca2a-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="aca2a-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aca2a-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="aca2a-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aca2a-147">Search-Flags</span></span>           | <span data-ttu-id="aca2a-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aca2a-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="aca2a-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aca2a-149">System-Flags</span></span>           | <span data-ttu-id="aca2a-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aca2a-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="aca2a-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="aca2a-151">Classes used in</span></span>        | [<span data-ttu-id="aca2a-152">**MS-WMI-policytemplate**</span><span class="sxs-lookup"><span data-stu-id="aca2a-152">**ms-WMI-PolicyTemplate**</span></span>](c-mswmi-policytemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="aca2a-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="aca2a-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="aca2a-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aca2a-154">Entry</span></span> | <span data-ttu-id="aca2a-155">Wert</span><span class="sxs-lookup"><span data-stu-id="aca2a-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="aca2a-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="aca2a-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="aca2a-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aca2a-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="aca2a-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="aca2a-158">System-Only</span></span>            | <span data-ttu-id="aca2a-159">False</span><span class="sxs-lookup"><span data-stu-id="aca2a-159">False</span></span>                                                              |
| <span data-ttu-id="aca2a-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="aca2a-160">Is-Single-Valued</span></span>       | <span data-ttu-id="aca2a-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="aca2a-161">True</span></span>                                                               |
| <span data-ttu-id="aca2a-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="aca2a-162">Is Indexed</span></span>             | <span data-ttu-id="aca2a-163">False</span><span class="sxs-lookup"><span data-stu-id="aca2a-163">False</span></span>                                                              |
| <span data-ttu-id="aca2a-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="aca2a-164">In Global Catalog</span></span>      | <span data-ttu-id="aca2a-165">False</span><span class="sxs-lookup"><span data-stu-id="aca2a-165">False</span></span>                                                              |
| <span data-ttu-id="aca2a-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aca2a-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="aca2a-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="aca2a-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="aca2a-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aca2a-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="aca2a-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aca2a-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="aca2a-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aca2a-170">Search-Flags</span></span>           | <span data-ttu-id="aca2a-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aca2a-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="aca2a-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aca2a-172">System-Flags</span></span>           | <span data-ttu-id="aca2a-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aca2a-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="aca2a-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="aca2a-174">Classes used in</span></span>        | [<span data-ttu-id="aca2a-175">**MS-WMI-policytemplate**</span><span class="sxs-lookup"><span data-stu-id="aca2a-175">**ms-WMI-PolicyTemplate**</span></span>](c-mswmi-policytemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="aca2a-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aca2a-176">Windows Server 2008</span></span>



| <span data-ttu-id="aca2a-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aca2a-177">Entry</span></span> | <span data-ttu-id="aca2a-178">Wert</span><span class="sxs-lookup"><span data-stu-id="aca2a-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="aca2a-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="aca2a-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="aca2a-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aca2a-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="aca2a-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="aca2a-181">System-Only</span></span>            | <span data-ttu-id="aca2a-182">False</span><span class="sxs-lookup"><span data-stu-id="aca2a-182">False</span></span>                                                              |
| <span data-ttu-id="aca2a-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="aca2a-183">Is-Single-Valued</span></span>       | <span data-ttu-id="aca2a-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="aca2a-184">True</span></span>                                                               |
| <span data-ttu-id="aca2a-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="aca2a-185">Is Indexed</span></span>             | <span data-ttu-id="aca2a-186">False</span><span class="sxs-lookup"><span data-stu-id="aca2a-186">False</span></span>                                                              |
| <span data-ttu-id="aca2a-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="aca2a-187">In Global Catalog</span></span>      | <span data-ttu-id="aca2a-188">False</span><span class="sxs-lookup"><span data-stu-id="aca2a-188">False</span></span>                                                              |
| <span data-ttu-id="aca2a-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aca2a-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="aca2a-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="aca2a-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="aca2a-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aca2a-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="aca2a-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aca2a-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="aca2a-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aca2a-193">Search-Flags</span></span>           | <span data-ttu-id="aca2a-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aca2a-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="aca2a-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aca2a-195">System-Flags</span></span>           | <span data-ttu-id="aca2a-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aca2a-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="aca2a-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="aca2a-197">Classes used in</span></span>        | [<span data-ttu-id="aca2a-198">**MS-WMI-policytemplate**</span><span class="sxs-lookup"><span data-stu-id="aca2a-198">**ms-WMI-PolicyTemplate**</span></span>](c-mswmi-policytemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="aca2a-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aca2a-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="aca2a-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aca2a-200">Entry</span></span> | <span data-ttu-id="aca2a-201">Wert</span><span class="sxs-lookup"><span data-stu-id="aca2a-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="aca2a-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="aca2a-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="aca2a-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aca2a-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="aca2a-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="aca2a-204">System-Only</span></span>            | <span data-ttu-id="aca2a-205">False</span><span class="sxs-lookup"><span data-stu-id="aca2a-205">False</span></span>                                                              |
| <span data-ttu-id="aca2a-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="aca2a-206">Is-Single-Valued</span></span>       | <span data-ttu-id="aca2a-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="aca2a-207">True</span></span>                                                               |
| <span data-ttu-id="aca2a-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="aca2a-208">Is Indexed</span></span>             | <span data-ttu-id="aca2a-209">False</span><span class="sxs-lookup"><span data-stu-id="aca2a-209">False</span></span>                                                              |
| <span data-ttu-id="aca2a-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="aca2a-210">In Global Catalog</span></span>      | <span data-ttu-id="aca2a-211">False</span><span class="sxs-lookup"><span data-stu-id="aca2a-211">False</span></span>                                                              |
| <span data-ttu-id="aca2a-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aca2a-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="aca2a-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="aca2a-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="aca2a-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aca2a-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="aca2a-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aca2a-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="aca2a-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aca2a-216">Search-Flags</span></span>           | <span data-ttu-id="aca2a-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aca2a-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="aca2a-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aca2a-218">System-Flags</span></span>           | <span data-ttu-id="aca2a-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aca2a-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="aca2a-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="aca2a-220">Classes used in</span></span>        | [<span data-ttu-id="aca2a-221">**MS-WMI-policytemplate**</span><span class="sxs-lookup"><span data-stu-id="aca2a-221">**ms-WMI-PolicyTemplate**</span></span>](c-mswmi-policytemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="aca2a-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aca2a-222">Windows Server 2012</span></span>



| <span data-ttu-id="aca2a-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aca2a-223">Entry</span></span> | <span data-ttu-id="aca2a-224">Wert</span><span class="sxs-lookup"><span data-stu-id="aca2a-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="aca2a-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="aca2a-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="aca2a-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aca2a-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="aca2a-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="aca2a-227">System-Only</span></span>            | <span data-ttu-id="aca2a-228">False</span><span class="sxs-lookup"><span data-stu-id="aca2a-228">False</span></span>                                                              |
| <span data-ttu-id="aca2a-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="aca2a-229">Is-Single-Valued</span></span>       | <span data-ttu-id="aca2a-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="aca2a-230">True</span></span>                                                               |
| <span data-ttu-id="aca2a-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="aca2a-231">Is Indexed</span></span>             | <span data-ttu-id="aca2a-232">False</span><span class="sxs-lookup"><span data-stu-id="aca2a-232">False</span></span>                                                              |
| <span data-ttu-id="aca2a-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="aca2a-233">In Global Catalog</span></span>      | <span data-ttu-id="aca2a-234">False</span><span class="sxs-lookup"><span data-stu-id="aca2a-234">False</span></span>                                                              |
| <span data-ttu-id="aca2a-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aca2a-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="aca2a-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="aca2a-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="aca2a-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aca2a-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="aca2a-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aca2a-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="aca2a-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aca2a-239">Search-Flags</span></span>           | <span data-ttu-id="aca2a-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aca2a-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="aca2a-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aca2a-241">System-Flags</span></span>           | <span data-ttu-id="aca2a-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aca2a-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="aca2a-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="aca2a-243">Classes used in</span></span>        | [<span data-ttu-id="aca2a-244">**MS-WMI-policytemplate**</span><span class="sxs-lookup"><span data-stu-id="aca2a-244">**ms-WMI-PolicyTemplate**</span></span>](c-mswmi-policytemplate.md)<br/> |



 

 





