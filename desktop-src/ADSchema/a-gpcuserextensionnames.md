---
title: GPC-User-Extension-names-Attribut
description: Wird vom Gruppenrichtlinie-Objekt für Benutzerrichtlinien verwendet.
ms.assetid: 3c6fa679-7597-4286-bd79-7a0030212810
ms.tgt_platform: multiple
keywords:
- AD-Schema für GPC-User-Extension-names-Attribut
- gpcuserextensionnames-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- GPC-User-Extension-Names
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12de39539af6ee523838f8081aa04a5d21b8a1d3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479687"
---
# <a name="gpc-user-extension-names-attribute"></a><span data-ttu-id="e7752-105">GPC-User-Extension-names-Attribut</span><span class="sxs-lookup"><span data-stu-id="e7752-105">GPC-User-Extension-Names attribute</span></span>

<span data-ttu-id="e7752-106">Wird vom Gruppenrichtlinie-Objekt für Benutzerrichtlinien verwendet.</span><span class="sxs-lookup"><span data-stu-id="e7752-106">Used by the Group Policy Object for user policies.</span></span>



| <span data-ttu-id="e7752-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e7752-107">Entry</span></span> | <span data-ttu-id="e7752-108">Wert</span><span class="sxs-lookup"><span data-stu-id="e7752-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="e7752-109">CN</span><span class="sxs-lookup"><span data-stu-id="e7752-109">CN</span></span>                | <span data-ttu-id="e7752-110">GPC-Benutzer-Erweiterungs Namen</span><span class="sxs-lookup"><span data-stu-id="e7752-110">GPC-User-Extension-Names</span></span>                                                        |
| <span data-ttu-id="e7752-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e7752-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e7752-112">gpcuserextensionnames</span><span class="sxs-lookup"><span data-stu-id="e7752-112">gPCUserExtensionNames</span></span>                                                           |
| <span data-ttu-id="e7752-113">Size</span><span class="sxs-lookup"><span data-stu-id="e7752-113">Size</span></span>              | <span data-ttu-id="e7752-114">Hängt von der Anzahl der Client seitigen Erweiterungen ab, die in diesem Gruppenrichtlinien Objekt über eine Richtlinie verfügen.</span><span class="sxs-lookup"><span data-stu-id="e7752-114">Depends on the number of client-side extensions that have a policy in this GPO.</span></span> |
| <span data-ttu-id="e7752-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="e7752-115">Update Privilege</span></span>  | <span data-ttu-id="e7752-116">Domänen-oder Richtlinien Administrator.</span><span class="sxs-lookup"><span data-stu-id="e7752-116">Domain or policy administrator.</span></span>                                                 |
| <span data-ttu-id="e7752-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="e7752-117">Update Frequency</span></span>  | <span data-ttu-id="e7752-118">Jedes Mal, wenn ein GPO über das gpe aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="e7752-118">Whenever a GPO is updated through the GPE.</span></span>                                      |
| <span data-ttu-id="e7752-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e7752-119">Attribute-Id</span></span>      | <span data-ttu-id="e7752-120">1.2.840.113556.1.4.1349</span><span class="sxs-lookup"><span data-stu-id="e7752-120">1.2.840.113556.1.4.1349</span></span>                                                         |
| <span data-ttu-id="e7752-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e7752-121">System-Id-Guid</span></span>    | <span data-ttu-id="e7752-122">42a75fc6-783f -11d2-9916-0000f 87a57d4</span><span class="sxs-lookup"><span data-stu-id="e7752-122">42a75fc6-783f-11d2-9916-0000f87a57d4</span></span>                                            |
| <span data-ttu-id="e7752-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7752-123">Syntax</span></span>            | [<span data-ttu-id="e7752-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e7752-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                     |



## <a name="implementations"></a><span data-ttu-id="e7752-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="e7752-125">Implementations</span></span>

-   [<span data-ttu-id="e7752-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e7752-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e7752-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e7752-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e7752-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e7752-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e7752-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e7752-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e7752-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e7752-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e7752-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e7752-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e7752-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e7752-132">Windows 2000 Server</span></span>



| <span data-ttu-id="e7752-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e7752-133">Entry</span></span> | <span data-ttu-id="e7752-134">Wert</span><span class="sxs-lookup"><span data-stu-id="e7752-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="e7752-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e7752-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e7752-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7752-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e7752-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7752-137">System-Only</span></span>            | <span data-ttu-id="e7752-138">False</span><span class="sxs-lookup"><span data-stu-id="e7752-138">False</span></span>                                                               |
| <span data-ttu-id="e7752-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e7752-139">Is-Single-Valued</span></span>       | <span data-ttu-id="e7752-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="e7752-140">True</span></span>                                                                |
| <span data-ttu-id="e7752-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e7752-141">Is Indexed</span></span>             | <span data-ttu-id="e7752-142">False</span><span class="sxs-lookup"><span data-stu-id="e7752-142">False</span></span>                                                               |
| <span data-ttu-id="e7752-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e7752-143">In Global Catalog</span></span>      | <span data-ttu-id="e7752-144">False</span><span class="sxs-lookup"><span data-stu-id="e7752-144">False</span></span>                                                               |
| <span data-ttu-id="e7752-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e7752-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7752-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e7752-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="e7752-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7752-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="e7752-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7752-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="e7752-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7752-149">Search-Flags</span></span>           | <span data-ttu-id="e7752-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7752-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="e7752-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7752-151">System-Flags</span></span>           | <span data-ttu-id="e7752-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7752-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="e7752-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e7752-153">Classes used in</span></span>        | [<span data-ttu-id="e7752-154">**Gruppenrichtlinien Container**</span><span class="sxs-lookup"><span data-stu-id="e7752-154">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e7752-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e7752-155">Windows Server 2003</span></span>



| <span data-ttu-id="e7752-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e7752-156">Entry</span></span> | <span data-ttu-id="e7752-157">Wert</span><span class="sxs-lookup"><span data-stu-id="e7752-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="e7752-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e7752-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e7752-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7752-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e7752-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7752-160">System-Only</span></span>            | <span data-ttu-id="e7752-161">False</span><span class="sxs-lookup"><span data-stu-id="e7752-161">False</span></span>                                                               |
| <span data-ttu-id="e7752-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e7752-162">Is-Single-Valued</span></span>       | <span data-ttu-id="e7752-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="e7752-163">True</span></span>                                                                |
| <span data-ttu-id="e7752-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e7752-164">Is Indexed</span></span>             | <span data-ttu-id="e7752-165">False</span><span class="sxs-lookup"><span data-stu-id="e7752-165">False</span></span>                                                               |
| <span data-ttu-id="e7752-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e7752-166">In Global Catalog</span></span>      | <span data-ttu-id="e7752-167">False</span><span class="sxs-lookup"><span data-stu-id="e7752-167">False</span></span>                                                               |
| <span data-ttu-id="e7752-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e7752-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7752-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e7752-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="e7752-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7752-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="e7752-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7752-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="e7752-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7752-172">Search-Flags</span></span>           | <span data-ttu-id="e7752-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7752-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="e7752-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7752-174">System-Flags</span></span>           | <span data-ttu-id="e7752-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7752-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="e7752-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e7752-176">Classes used in</span></span>        | [<span data-ttu-id="e7752-177">**Gruppenrichtlinien Container**</span><span class="sxs-lookup"><span data-stu-id="e7752-177">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e7752-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e7752-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e7752-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e7752-179">Entry</span></span> | <span data-ttu-id="e7752-180">Wert</span><span class="sxs-lookup"><span data-stu-id="e7752-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="e7752-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e7752-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e7752-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7752-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e7752-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7752-183">System-Only</span></span>            | <span data-ttu-id="e7752-184">False</span><span class="sxs-lookup"><span data-stu-id="e7752-184">False</span></span>                                                               |
| <span data-ttu-id="e7752-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e7752-185">Is-Single-Valued</span></span>       | <span data-ttu-id="e7752-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="e7752-186">True</span></span>                                                                |
| <span data-ttu-id="e7752-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e7752-187">Is Indexed</span></span>             | <span data-ttu-id="e7752-188">False</span><span class="sxs-lookup"><span data-stu-id="e7752-188">False</span></span>                                                               |
| <span data-ttu-id="e7752-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e7752-189">In Global Catalog</span></span>      | <span data-ttu-id="e7752-190">False</span><span class="sxs-lookup"><span data-stu-id="e7752-190">False</span></span>                                                               |
| <span data-ttu-id="e7752-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e7752-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7752-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e7752-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="e7752-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7752-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="e7752-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7752-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="e7752-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7752-195">Search-Flags</span></span>           | <span data-ttu-id="e7752-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7752-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="e7752-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7752-197">System-Flags</span></span>           | <span data-ttu-id="e7752-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7752-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="e7752-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e7752-199">Classes used in</span></span>        | [<span data-ttu-id="e7752-200">**Gruppenrichtlinien Container**</span><span class="sxs-lookup"><span data-stu-id="e7752-200">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e7752-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7752-201">Windows Server 2008</span></span>



| <span data-ttu-id="e7752-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e7752-202">Entry</span></span> | <span data-ttu-id="e7752-203">Wert</span><span class="sxs-lookup"><span data-stu-id="e7752-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="e7752-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e7752-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e7752-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7752-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e7752-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7752-206">System-Only</span></span>            | <span data-ttu-id="e7752-207">False</span><span class="sxs-lookup"><span data-stu-id="e7752-207">False</span></span>                                                               |
| <span data-ttu-id="e7752-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e7752-208">Is-Single-Valued</span></span>       | <span data-ttu-id="e7752-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="e7752-209">True</span></span>                                                                |
| <span data-ttu-id="e7752-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e7752-210">Is Indexed</span></span>             | <span data-ttu-id="e7752-211">False</span><span class="sxs-lookup"><span data-stu-id="e7752-211">False</span></span>                                                               |
| <span data-ttu-id="e7752-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e7752-212">In Global Catalog</span></span>      | <span data-ttu-id="e7752-213">False</span><span class="sxs-lookup"><span data-stu-id="e7752-213">False</span></span>                                                               |
| <span data-ttu-id="e7752-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e7752-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7752-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e7752-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="e7752-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7752-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="e7752-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7752-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="e7752-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7752-218">Search-Flags</span></span>           | <span data-ttu-id="e7752-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7752-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="e7752-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7752-220">System-Flags</span></span>           | <span data-ttu-id="e7752-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7752-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="e7752-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e7752-222">Classes used in</span></span>        | [<span data-ttu-id="e7752-223">**Gruppenrichtlinien Container**</span><span class="sxs-lookup"><span data-stu-id="e7752-223">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e7752-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e7752-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e7752-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e7752-225">Entry</span></span> | <span data-ttu-id="e7752-226">Wert</span><span class="sxs-lookup"><span data-stu-id="e7752-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="e7752-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e7752-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e7752-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7752-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e7752-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7752-229">System-Only</span></span>            | <span data-ttu-id="e7752-230">False</span><span class="sxs-lookup"><span data-stu-id="e7752-230">False</span></span>                                                               |
| <span data-ttu-id="e7752-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e7752-231">Is-Single-Valued</span></span>       | <span data-ttu-id="e7752-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="e7752-232">True</span></span>                                                                |
| <span data-ttu-id="e7752-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e7752-233">Is Indexed</span></span>             | <span data-ttu-id="e7752-234">False</span><span class="sxs-lookup"><span data-stu-id="e7752-234">False</span></span>                                                               |
| <span data-ttu-id="e7752-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e7752-235">In Global Catalog</span></span>      | <span data-ttu-id="e7752-236">False</span><span class="sxs-lookup"><span data-stu-id="e7752-236">False</span></span>                                                               |
| <span data-ttu-id="e7752-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e7752-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7752-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e7752-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="e7752-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7752-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="e7752-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7752-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="e7752-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7752-241">Search-Flags</span></span>           | <span data-ttu-id="e7752-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7752-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="e7752-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7752-243">System-Flags</span></span>           | <span data-ttu-id="e7752-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7752-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="e7752-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e7752-245">Classes used in</span></span>        | [<span data-ttu-id="e7752-246">**Gruppenrichtlinien Container**</span><span class="sxs-lookup"><span data-stu-id="e7752-246">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e7752-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e7752-247">Windows Server 2012</span></span>



| <span data-ttu-id="e7752-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e7752-248">Entry</span></span> | <span data-ttu-id="e7752-249">Wert</span><span class="sxs-lookup"><span data-stu-id="e7752-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="e7752-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e7752-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e7752-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7752-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e7752-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7752-252">System-Only</span></span>            | <span data-ttu-id="e7752-253">False</span><span class="sxs-lookup"><span data-stu-id="e7752-253">False</span></span>                                                               |
| <span data-ttu-id="e7752-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e7752-254">Is-Single-Valued</span></span>       | <span data-ttu-id="e7752-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="e7752-255">True</span></span>                                                                |
| <span data-ttu-id="e7752-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e7752-256">Is Indexed</span></span>             | <span data-ttu-id="e7752-257">False</span><span class="sxs-lookup"><span data-stu-id="e7752-257">False</span></span>                                                               |
| <span data-ttu-id="e7752-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e7752-258">In Global Catalog</span></span>      | <span data-ttu-id="e7752-259">False</span><span class="sxs-lookup"><span data-stu-id="e7752-259">False</span></span>                                                               |
| <span data-ttu-id="e7752-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e7752-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7752-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e7752-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="e7752-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7752-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="e7752-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7752-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="e7752-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7752-264">Search-Flags</span></span>           | <span data-ttu-id="e7752-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7752-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="e7752-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7752-266">System-Flags</span></span>           | <span data-ttu-id="e7752-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7752-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="e7752-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e7752-268">Classes used in</span></span>        | [<span data-ttu-id="e7752-269">**Gruppenrichtlinien Container**</span><span class="sxs-lookup"><span data-stu-id="e7752-269">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



 

 





