---
title: GPC-Machine-Extension-names-Attribut
description: Wird vom Gruppenrichtlinie-Objekt für Computer Richtlinien verwendet.
ms.assetid: a5e00bf6-d311-4ccd-a2cf-4f7506fec419
ms.tgt_platform: multiple
keywords:
- AD-Schema für GPC-Machine-Extension-names-Attribut
- AD-Schema des gpcmachineextensionnames-Attributs
topic_type:
- apiref
api_name:
- GPC-Machine-Extension-Names
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc9d9c1ce435a017bfefe88d728004f619e193f9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957553"
---
# <a name="gpc-machine-extension-names-attribute"></a><span data-ttu-id="ff06b-105">GPC-Machine-Extension-names-Attribut</span><span class="sxs-lookup"><span data-stu-id="ff06b-105">GPC-Machine-Extension-Names attribute</span></span>

<span data-ttu-id="ff06b-106">Wird vom Gruppenrichtlinie-Objekt für Computer Richtlinien verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff06b-106">Used by the Group Policy Object for computer policies.</span></span>



| <span data-ttu-id="ff06b-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ff06b-107">Entry</span></span> | <span data-ttu-id="ff06b-108">Wert</span><span class="sxs-lookup"><span data-stu-id="ff06b-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="ff06b-109">CN</span><span class="sxs-lookup"><span data-stu-id="ff06b-109">CN</span></span>                | <span data-ttu-id="ff06b-110">GPC-Computer-Erweiterungs Namen</span><span class="sxs-lookup"><span data-stu-id="ff06b-110">GPC-Machine-Extension-Names</span></span>                                                     |
| <span data-ttu-id="ff06b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ff06b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ff06b-112">gpcmachineextensionnames</span><span class="sxs-lookup"><span data-stu-id="ff06b-112">gPCMachineExtensionNames</span></span>                                                        |
| <span data-ttu-id="ff06b-113">Size</span><span class="sxs-lookup"><span data-stu-id="ff06b-113">Size</span></span>              | <span data-ttu-id="ff06b-114">Hängt von der Anzahl der Client seitigen Erweiterungen ab, die in diesem Gruppenrichtlinien Objekt über eine Richtlinie verfügen.</span><span class="sxs-lookup"><span data-stu-id="ff06b-114">Depends on the number of client-side extensions that have a policy in this GPO.</span></span> |
| <span data-ttu-id="ff06b-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ff06b-115">Update Privilege</span></span>  | <span data-ttu-id="ff06b-116">Domänen-oder Richtlinien Administrator.</span><span class="sxs-lookup"><span data-stu-id="ff06b-116">Domain or policy administrator.</span></span>                                                 |
| <span data-ttu-id="ff06b-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="ff06b-117">Update Frequency</span></span>  | <span data-ttu-id="ff06b-118">Jedes Mal, wenn ein GPO über das gpe aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ff06b-118">Whenever a GPO is updated through the GPE.</span></span>                                      |
| <span data-ttu-id="ff06b-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ff06b-119">Attribute-Id</span></span>      | <span data-ttu-id="ff06b-120">1.2.840.113556.1.4.1348</span><span class="sxs-lookup"><span data-stu-id="ff06b-120">1.2.840.113556.1.4.1348</span></span>                                                         |
| <span data-ttu-id="ff06b-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ff06b-121">System-Id-Guid</span></span>    | <span data-ttu-id="ff06b-122">32ff8ecc-783f-11d2-9916-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="ff06b-122">32ff8ecc-783f-11d2-9916-0000f87a57d4</span></span>                                            |
| <span data-ttu-id="ff06b-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff06b-123">Syntax</span></span>            | [<span data-ttu-id="ff06b-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ff06b-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                     |



## <a name="implementations"></a><span data-ttu-id="ff06b-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="ff06b-125">Implementations</span></span>

-   [<span data-ttu-id="ff06b-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ff06b-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ff06b-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ff06b-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ff06b-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ff06b-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ff06b-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ff06b-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ff06b-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ff06b-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ff06b-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ff06b-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ff06b-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ff06b-132">Windows 2000 Server</span></span>



| <span data-ttu-id="ff06b-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ff06b-133">Entry</span></span> | <span data-ttu-id="ff06b-134">Wert</span><span class="sxs-lookup"><span data-stu-id="ff06b-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ff06b-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ff06b-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ff06b-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff06b-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ff06b-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff06b-137">System-Only</span></span>            | <span data-ttu-id="ff06b-138">False</span><span class="sxs-lookup"><span data-stu-id="ff06b-138">False</span></span>                                                               |
| <span data-ttu-id="ff06b-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ff06b-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ff06b-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="ff06b-140">True</span></span>                                                                |
| <span data-ttu-id="ff06b-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ff06b-141">Is Indexed</span></span>             | <span data-ttu-id="ff06b-142">False</span><span class="sxs-lookup"><span data-stu-id="ff06b-142">False</span></span>                                                               |
| <span data-ttu-id="ff06b-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ff06b-143">In Global Catalog</span></span>      | <span data-ttu-id="ff06b-144">False</span><span class="sxs-lookup"><span data-stu-id="ff06b-144">False</span></span>                                                               |
| <span data-ttu-id="ff06b-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ff06b-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff06b-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ff06b-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ff06b-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff06b-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ff06b-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff06b-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ff06b-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff06b-149">Search-Flags</span></span>           | <span data-ttu-id="ff06b-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff06b-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="ff06b-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff06b-151">System-Flags</span></span>           | <span data-ttu-id="ff06b-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff06b-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="ff06b-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ff06b-153">Classes used in</span></span>        | [<span data-ttu-id="ff06b-154">**Gruppenrichtlinien Container**</span><span class="sxs-lookup"><span data-stu-id="ff06b-154">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ff06b-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ff06b-155">Windows Server 2003</span></span>



| <span data-ttu-id="ff06b-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ff06b-156">Entry</span></span> | <span data-ttu-id="ff06b-157">Wert</span><span class="sxs-lookup"><span data-stu-id="ff06b-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ff06b-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ff06b-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ff06b-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff06b-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ff06b-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff06b-160">System-Only</span></span>            | <span data-ttu-id="ff06b-161">False</span><span class="sxs-lookup"><span data-stu-id="ff06b-161">False</span></span>                                                               |
| <span data-ttu-id="ff06b-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ff06b-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ff06b-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="ff06b-163">True</span></span>                                                                |
| <span data-ttu-id="ff06b-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ff06b-164">Is Indexed</span></span>             | <span data-ttu-id="ff06b-165">False</span><span class="sxs-lookup"><span data-stu-id="ff06b-165">False</span></span>                                                               |
| <span data-ttu-id="ff06b-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ff06b-166">In Global Catalog</span></span>      | <span data-ttu-id="ff06b-167">False</span><span class="sxs-lookup"><span data-stu-id="ff06b-167">False</span></span>                                                               |
| <span data-ttu-id="ff06b-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ff06b-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff06b-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ff06b-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ff06b-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff06b-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ff06b-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff06b-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ff06b-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff06b-172">Search-Flags</span></span>           | <span data-ttu-id="ff06b-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff06b-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="ff06b-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff06b-174">System-Flags</span></span>           | <span data-ttu-id="ff06b-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff06b-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="ff06b-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ff06b-176">Classes used in</span></span>        | [<span data-ttu-id="ff06b-177">**Gruppenrichtlinien Container**</span><span class="sxs-lookup"><span data-stu-id="ff06b-177">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ff06b-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ff06b-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ff06b-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ff06b-179">Entry</span></span> | <span data-ttu-id="ff06b-180">Wert</span><span class="sxs-lookup"><span data-stu-id="ff06b-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ff06b-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ff06b-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ff06b-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff06b-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ff06b-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff06b-183">System-Only</span></span>            | <span data-ttu-id="ff06b-184">False</span><span class="sxs-lookup"><span data-stu-id="ff06b-184">False</span></span>                                                               |
| <span data-ttu-id="ff06b-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ff06b-185">Is-Single-Valued</span></span>       | <span data-ttu-id="ff06b-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="ff06b-186">True</span></span>                                                                |
| <span data-ttu-id="ff06b-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ff06b-187">Is Indexed</span></span>             | <span data-ttu-id="ff06b-188">False</span><span class="sxs-lookup"><span data-stu-id="ff06b-188">False</span></span>                                                               |
| <span data-ttu-id="ff06b-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ff06b-189">In Global Catalog</span></span>      | <span data-ttu-id="ff06b-190">False</span><span class="sxs-lookup"><span data-stu-id="ff06b-190">False</span></span>                                                               |
| <span data-ttu-id="ff06b-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ff06b-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff06b-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ff06b-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ff06b-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff06b-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ff06b-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff06b-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ff06b-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff06b-195">Search-Flags</span></span>           | <span data-ttu-id="ff06b-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff06b-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="ff06b-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff06b-197">System-Flags</span></span>           | <span data-ttu-id="ff06b-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff06b-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="ff06b-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ff06b-199">Classes used in</span></span>        | [<span data-ttu-id="ff06b-200">**Gruppenrichtlinien Container**</span><span class="sxs-lookup"><span data-stu-id="ff06b-200">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ff06b-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff06b-201">Windows Server 2008</span></span>



| <span data-ttu-id="ff06b-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ff06b-202">Entry</span></span> | <span data-ttu-id="ff06b-203">Wert</span><span class="sxs-lookup"><span data-stu-id="ff06b-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ff06b-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ff06b-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ff06b-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff06b-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ff06b-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff06b-206">System-Only</span></span>            | <span data-ttu-id="ff06b-207">False</span><span class="sxs-lookup"><span data-stu-id="ff06b-207">False</span></span>                                                               |
| <span data-ttu-id="ff06b-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ff06b-208">Is-Single-Valued</span></span>       | <span data-ttu-id="ff06b-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="ff06b-209">True</span></span>                                                                |
| <span data-ttu-id="ff06b-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ff06b-210">Is Indexed</span></span>             | <span data-ttu-id="ff06b-211">False</span><span class="sxs-lookup"><span data-stu-id="ff06b-211">False</span></span>                                                               |
| <span data-ttu-id="ff06b-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ff06b-212">In Global Catalog</span></span>      | <span data-ttu-id="ff06b-213">False</span><span class="sxs-lookup"><span data-stu-id="ff06b-213">False</span></span>                                                               |
| <span data-ttu-id="ff06b-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ff06b-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff06b-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ff06b-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ff06b-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff06b-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ff06b-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff06b-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ff06b-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff06b-218">Search-Flags</span></span>           | <span data-ttu-id="ff06b-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff06b-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="ff06b-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff06b-220">System-Flags</span></span>           | <span data-ttu-id="ff06b-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff06b-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="ff06b-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ff06b-222">Classes used in</span></span>        | [<span data-ttu-id="ff06b-223">**Gruppenrichtlinien Container**</span><span class="sxs-lookup"><span data-stu-id="ff06b-223">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ff06b-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ff06b-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ff06b-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ff06b-225">Entry</span></span> | <span data-ttu-id="ff06b-226">Wert</span><span class="sxs-lookup"><span data-stu-id="ff06b-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ff06b-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ff06b-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ff06b-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff06b-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ff06b-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff06b-229">System-Only</span></span>            | <span data-ttu-id="ff06b-230">False</span><span class="sxs-lookup"><span data-stu-id="ff06b-230">False</span></span>                                                               |
| <span data-ttu-id="ff06b-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ff06b-231">Is-Single-Valued</span></span>       | <span data-ttu-id="ff06b-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="ff06b-232">True</span></span>                                                                |
| <span data-ttu-id="ff06b-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ff06b-233">Is Indexed</span></span>             | <span data-ttu-id="ff06b-234">False</span><span class="sxs-lookup"><span data-stu-id="ff06b-234">False</span></span>                                                               |
| <span data-ttu-id="ff06b-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ff06b-235">In Global Catalog</span></span>      | <span data-ttu-id="ff06b-236">False</span><span class="sxs-lookup"><span data-stu-id="ff06b-236">False</span></span>                                                               |
| <span data-ttu-id="ff06b-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ff06b-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff06b-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ff06b-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ff06b-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff06b-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ff06b-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff06b-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ff06b-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff06b-241">Search-Flags</span></span>           | <span data-ttu-id="ff06b-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff06b-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="ff06b-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff06b-243">System-Flags</span></span>           | <span data-ttu-id="ff06b-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff06b-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="ff06b-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ff06b-245">Classes used in</span></span>        | [<span data-ttu-id="ff06b-246">**Gruppenrichtlinien Container**</span><span class="sxs-lookup"><span data-stu-id="ff06b-246">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ff06b-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ff06b-247">Windows Server 2012</span></span>



| <span data-ttu-id="ff06b-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ff06b-248">Entry</span></span> | <span data-ttu-id="ff06b-249">Wert</span><span class="sxs-lookup"><span data-stu-id="ff06b-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ff06b-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ff06b-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ff06b-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff06b-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ff06b-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff06b-252">System-Only</span></span>            | <span data-ttu-id="ff06b-253">False</span><span class="sxs-lookup"><span data-stu-id="ff06b-253">False</span></span>                                                               |
| <span data-ttu-id="ff06b-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ff06b-254">Is-Single-Valued</span></span>       | <span data-ttu-id="ff06b-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="ff06b-255">True</span></span>                                                                |
| <span data-ttu-id="ff06b-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ff06b-256">Is Indexed</span></span>             | <span data-ttu-id="ff06b-257">False</span><span class="sxs-lookup"><span data-stu-id="ff06b-257">False</span></span>                                                               |
| <span data-ttu-id="ff06b-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ff06b-258">In Global Catalog</span></span>      | <span data-ttu-id="ff06b-259">False</span><span class="sxs-lookup"><span data-stu-id="ff06b-259">False</span></span>                                                               |
| <span data-ttu-id="ff06b-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ff06b-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff06b-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ff06b-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ff06b-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff06b-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ff06b-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff06b-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ff06b-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff06b-264">Search-Flags</span></span>           | <span data-ttu-id="ff06b-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff06b-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="ff06b-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff06b-266">System-Flags</span></span>           | <span data-ttu-id="ff06b-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff06b-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="ff06b-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ff06b-268">Classes used in</span></span>        | [<span data-ttu-id="ff06b-269">**Gruppenrichtlinien Container**</span><span class="sxs-lookup"><span data-stu-id="ff06b-269">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



 

 





