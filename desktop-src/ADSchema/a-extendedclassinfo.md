---
title: Extended-Class-Info-Attribut
description: Eine mehrwertige Eigenschaft, die Zeichen folgen enthält, die zusätzliche Informationen für jede Klasse darstellen. Jeder Wert enthält die governsID, den ldapDisplayName und die schemaIDGUID der Klasse.
ms.assetid: f0f07950-28f8-4fe7-b030-1ab7632569e1
ms.tgt_platform: multiple
keywords:
- AD-Schema für das Extended-Class-Info-Attribut
- extendedclassinfo-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Extended-Class-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1b3320f547a3dbb41a151a33765cf9729e82c6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104392258"
---
# <a name="extended-class-info-attribute"></a><span data-ttu-id="ad972-106">Extended-Class-Info-Attribut</span><span class="sxs-lookup"><span data-stu-id="ad972-106">Extended-Class-Info attribute</span></span>

<span data-ttu-id="ad972-107">Eine mehrwertige Eigenschaft, die Zeichen folgen enthält, die zusätzliche Informationen für jede Klasse darstellen.</span><span class="sxs-lookup"><span data-stu-id="ad972-107">A multi-valued property that contains strings that represent additional information for each class.</span></span> <span data-ttu-id="ad972-108">Jeder Wert enthält die governsID, den ldapDisplayName und die schemaIDGUID der Klasse.</span><span class="sxs-lookup"><span data-stu-id="ad972-108">Each value contains the governsID, lDAPDisplayName, and schemaIDGUID of the class.</span></span>



| <span data-ttu-id="ad972-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ad972-109">Entry</span></span> | <span data-ttu-id="ad972-110">Wert</span><span class="sxs-lookup"><span data-stu-id="ad972-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="ad972-111">CN</span><span class="sxs-lookup"><span data-stu-id="ad972-111">CN</span></span>                | <span data-ttu-id="ad972-112">Extended-Class-Info</span><span class="sxs-lookup"><span data-stu-id="ad972-112">Extended-Class-Info</span></span>                         |
| <span data-ttu-id="ad972-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ad972-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ad972-114">extendedclassinfo</span><span class="sxs-lookup"><span data-stu-id="ad972-114">extendedClassInfo</span></span>                           |
| <span data-ttu-id="ad972-115">Size</span><span class="sxs-lookup"><span data-stu-id="ad972-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="ad972-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ad972-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="ad972-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="ad972-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="ad972-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ad972-118">Attribute-Id</span></span>      | <span data-ttu-id="ad972-119">1.2.840.113556.1.4.908</span><span class="sxs-lookup"><span data-stu-id="ad972-119">1.2.840.113556.1.4.908</span></span>                      |
| <span data-ttu-id="ad972-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ad972-120">System-Id-Guid</span></span>    | <span data-ttu-id="ad972-121">9a7ad948-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="ad972-121">9a7ad948-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="ad972-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad972-122">Syntax</span></span>            | [<span data-ttu-id="ad972-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ad972-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="ad972-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="ad972-124">Implementations</span></span>

-   [<span data-ttu-id="ad972-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ad972-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ad972-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ad972-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ad972-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="ad972-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ad972-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ad972-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ad972-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ad972-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ad972-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ad972-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ad972-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ad972-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ad972-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ad972-132">Windows 2000 Server</span></span>



| <span data-ttu-id="ad972-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ad972-133">Entry</span></span> | <span data-ttu-id="ad972-134">Wert</span><span class="sxs-lookup"><span data-stu-id="ad972-134">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="ad972-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ad972-135">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="ad972-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad972-136">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="ad972-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad972-137">System-Only</span></span>            | <span data-ttu-id="ad972-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="ad972-138">True</span></span>                                        |
| <span data-ttu-id="ad972-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ad972-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ad972-140">False</span><span class="sxs-lookup"><span data-stu-id="ad972-140">False</span></span>                                       |
| <span data-ttu-id="ad972-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ad972-141">Is Indexed</span></span>             | <span data-ttu-id="ad972-142">False</span><span class="sxs-lookup"><span data-stu-id="ad972-142">False</span></span>                                       |
| <span data-ttu-id="ad972-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ad972-143">In Global Catalog</span></span>      | <span data-ttu-id="ad972-144">False</span><span class="sxs-lookup"><span data-stu-id="ad972-144">False</span></span>                                       |
| <span data-ttu-id="ad972-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ad972-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad972-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ad972-146">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="ad972-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad972-147">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="ad972-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad972-148">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="ad972-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad972-149">Search-Flags</span></span>           | <span data-ttu-id="ad972-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad972-150">0x00000000</span></span>                                  |
| <span data-ttu-id="ad972-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad972-151">System-Flags</span></span>           | <span data-ttu-id="ad972-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="ad972-152">0x08000014</span></span>                                  |
| <span data-ttu-id="ad972-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ad972-153">Classes used in</span></span>        | [<span data-ttu-id="ad972-154">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="ad972-154">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ad972-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ad972-155">Windows Server 2003</span></span>



| <span data-ttu-id="ad972-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ad972-156">Entry</span></span> | <span data-ttu-id="ad972-157">Wert</span><span class="sxs-lookup"><span data-stu-id="ad972-157">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="ad972-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ad972-158">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="ad972-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad972-159">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="ad972-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad972-160">System-Only</span></span>            | <span data-ttu-id="ad972-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="ad972-161">True</span></span>                                        |
| <span data-ttu-id="ad972-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ad972-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ad972-163">False</span><span class="sxs-lookup"><span data-stu-id="ad972-163">False</span></span>                                       |
| <span data-ttu-id="ad972-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ad972-164">Is Indexed</span></span>             | <span data-ttu-id="ad972-165">False</span><span class="sxs-lookup"><span data-stu-id="ad972-165">False</span></span>                                       |
| <span data-ttu-id="ad972-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ad972-166">In Global Catalog</span></span>      | <span data-ttu-id="ad972-167">False</span><span class="sxs-lookup"><span data-stu-id="ad972-167">False</span></span>                                       |
| <span data-ttu-id="ad972-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ad972-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad972-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ad972-169">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="ad972-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad972-170">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="ad972-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad972-171">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="ad972-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad972-172">Search-Flags</span></span>           | <span data-ttu-id="ad972-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad972-173">0x00000000</span></span>                                  |
| <span data-ttu-id="ad972-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad972-174">System-Flags</span></span>           | <span data-ttu-id="ad972-175">0x08000014</span><span class="sxs-lookup"><span data-stu-id="ad972-175">0x08000014</span></span>                                  |
| <span data-ttu-id="ad972-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ad972-176">Classes used in</span></span>        | [<span data-ttu-id="ad972-177">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="ad972-177">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ad972-178">Adam</span><span class="sxs-lookup"><span data-stu-id="ad972-178">ADAM</span></span>



| <span data-ttu-id="ad972-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ad972-179">Entry</span></span> | <span data-ttu-id="ad972-180">Wert</span><span class="sxs-lookup"><span data-stu-id="ad972-180">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="ad972-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ad972-181">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="ad972-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad972-182">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="ad972-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad972-183">System-Only</span></span>            | <span data-ttu-id="ad972-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="ad972-184">True</span></span>                                        |
| <span data-ttu-id="ad972-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ad972-185">Is-Single-Valued</span></span>       | <span data-ttu-id="ad972-186">False</span><span class="sxs-lookup"><span data-stu-id="ad972-186">False</span></span>                                       |
| <span data-ttu-id="ad972-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ad972-187">Is Indexed</span></span>             | <span data-ttu-id="ad972-188">False</span><span class="sxs-lookup"><span data-stu-id="ad972-188">False</span></span>                                       |
| <span data-ttu-id="ad972-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ad972-189">In Global Catalog</span></span>      | <span data-ttu-id="ad972-190">False</span><span class="sxs-lookup"><span data-stu-id="ad972-190">False</span></span>                                       |
| <span data-ttu-id="ad972-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ad972-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad972-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ad972-192">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="ad972-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad972-193">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="ad972-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad972-194">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="ad972-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad972-195">Search-Flags</span></span>           | <span data-ttu-id="ad972-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad972-196">0x00000000</span></span>                                  |
| <span data-ttu-id="ad972-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad972-197">System-Flags</span></span>           | <span data-ttu-id="ad972-198">0x08000014</span><span class="sxs-lookup"><span data-stu-id="ad972-198">0x08000014</span></span>                                  |
| <span data-ttu-id="ad972-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ad972-199">Classes used in</span></span>        | [<span data-ttu-id="ad972-200">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="ad972-200">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ad972-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ad972-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ad972-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ad972-202">Entry</span></span> | <span data-ttu-id="ad972-203">Wert</span><span class="sxs-lookup"><span data-stu-id="ad972-203">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="ad972-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ad972-204">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="ad972-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad972-205">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="ad972-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad972-206">System-Only</span></span>            | <span data-ttu-id="ad972-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="ad972-207">True</span></span>                                        |
| <span data-ttu-id="ad972-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ad972-208">Is-Single-Valued</span></span>       | <span data-ttu-id="ad972-209">False</span><span class="sxs-lookup"><span data-stu-id="ad972-209">False</span></span>                                       |
| <span data-ttu-id="ad972-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ad972-210">Is Indexed</span></span>             | <span data-ttu-id="ad972-211">False</span><span class="sxs-lookup"><span data-stu-id="ad972-211">False</span></span>                                       |
| <span data-ttu-id="ad972-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ad972-212">In Global Catalog</span></span>      | <span data-ttu-id="ad972-213">False</span><span class="sxs-lookup"><span data-stu-id="ad972-213">False</span></span>                                       |
| <span data-ttu-id="ad972-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ad972-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad972-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ad972-215">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="ad972-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad972-216">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="ad972-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad972-217">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="ad972-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad972-218">Search-Flags</span></span>           | <span data-ttu-id="ad972-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad972-219">0x00000000</span></span>                                  |
| <span data-ttu-id="ad972-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad972-220">System-Flags</span></span>           | <span data-ttu-id="ad972-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="ad972-221">0x08000014</span></span>                                  |
| <span data-ttu-id="ad972-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ad972-222">Classes used in</span></span>        | [<span data-ttu-id="ad972-223">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="ad972-223">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ad972-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad972-224">Windows Server 2008</span></span>



| <span data-ttu-id="ad972-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ad972-225">Entry</span></span> | <span data-ttu-id="ad972-226">Wert</span><span class="sxs-lookup"><span data-stu-id="ad972-226">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="ad972-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ad972-227">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="ad972-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad972-228">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="ad972-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad972-229">System-Only</span></span>            | <span data-ttu-id="ad972-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="ad972-230">True</span></span>                                        |
| <span data-ttu-id="ad972-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ad972-231">Is-Single-Valued</span></span>       | <span data-ttu-id="ad972-232">False</span><span class="sxs-lookup"><span data-stu-id="ad972-232">False</span></span>                                       |
| <span data-ttu-id="ad972-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ad972-233">Is Indexed</span></span>             | <span data-ttu-id="ad972-234">False</span><span class="sxs-lookup"><span data-stu-id="ad972-234">False</span></span>                                       |
| <span data-ttu-id="ad972-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ad972-235">In Global Catalog</span></span>      | <span data-ttu-id="ad972-236">False</span><span class="sxs-lookup"><span data-stu-id="ad972-236">False</span></span>                                       |
| <span data-ttu-id="ad972-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ad972-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad972-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ad972-238">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="ad972-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad972-239">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="ad972-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad972-240">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="ad972-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad972-241">Search-Flags</span></span>           | <span data-ttu-id="ad972-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad972-242">0x00000000</span></span>                                  |
| <span data-ttu-id="ad972-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad972-243">System-Flags</span></span>           | <span data-ttu-id="ad972-244">0x08000014</span><span class="sxs-lookup"><span data-stu-id="ad972-244">0x08000014</span></span>                                  |
| <span data-ttu-id="ad972-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ad972-245">Classes used in</span></span>        | [<span data-ttu-id="ad972-246">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="ad972-246">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ad972-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ad972-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ad972-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ad972-248">Entry</span></span> | <span data-ttu-id="ad972-249">Wert</span><span class="sxs-lookup"><span data-stu-id="ad972-249">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="ad972-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ad972-250">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="ad972-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad972-251">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="ad972-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad972-252">System-Only</span></span>            | <span data-ttu-id="ad972-253">Richtig</span><span class="sxs-lookup"><span data-stu-id="ad972-253">True</span></span>                                        |
| <span data-ttu-id="ad972-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ad972-254">Is-Single-Valued</span></span>       | <span data-ttu-id="ad972-255">False</span><span class="sxs-lookup"><span data-stu-id="ad972-255">False</span></span>                                       |
| <span data-ttu-id="ad972-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ad972-256">Is Indexed</span></span>             | <span data-ttu-id="ad972-257">False</span><span class="sxs-lookup"><span data-stu-id="ad972-257">False</span></span>                                       |
| <span data-ttu-id="ad972-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ad972-258">In Global Catalog</span></span>      | <span data-ttu-id="ad972-259">False</span><span class="sxs-lookup"><span data-stu-id="ad972-259">False</span></span>                                       |
| <span data-ttu-id="ad972-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ad972-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad972-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ad972-261">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="ad972-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad972-262">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="ad972-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad972-263">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="ad972-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad972-264">Search-Flags</span></span>           | <span data-ttu-id="ad972-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad972-265">0x00000000</span></span>                                  |
| <span data-ttu-id="ad972-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad972-266">System-Flags</span></span>           | <span data-ttu-id="ad972-267">0x08000014</span><span class="sxs-lookup"><span data-stu-id="ad972-267">0x08000014</span></span>                                  |
| <span data-ttu-id="ad972-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ad972-268">Classes used in</span></span>        | [<span data-ttu-id="ad972-269">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="ad972-269">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ad972-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ad972-270">Windows Server 2012</span></span>



| <span data-ttu-id="ad972-271">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ad972-271">Entry</span></span> | <span data-ttu-id="ad972-272">Wert</span><span class="sxs-lookup"><span data-stu-id="ad972-272">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="ad972-273">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ad972-273">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="ad972-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad972-274">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="ad972-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad972-275">System-Only</span></span>            | <span data-ttu-id="ad972-276">Richtig</span><span class="sxs-lookup"><span data-stu-id="ad972-276">True</span></span>                                        |
| <span data-ttu-id="ad972-277">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ad972-277">Is-Single-Valued</span></span>       | <span data-ttu-id="ad972-278">False</span><span class="sxs-lookup"><span data-stu-id="ad972-278">False</span></span>                                       |
| <span data-ttu-id="ad972-279">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ad972-279">Is Indexed</span></span>             | <span data-ttu-id="ad972-280">False</span><span class="sxs-lookup"><span data-stu-id="ad972-280">False</span></span>                                       |
| <span data-ttu-id="ad972-281">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ad972-281">In Global Catalog</span></span>      | <span data-ttu-id="ad972-282">False</span><span class="sxs-lookup"><span data-stu-id="ad972-282">False</span></span>                                       |
| <span data-ttu-id="ad972-283">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ad972-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad972-284">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ad972-284">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="ad972-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad972-285">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="ad972-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad972-286">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="ad972-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad972-287">Search-Flags</span></span>           | <span data-ttu-id="ad972-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad972-288">0x00000000</span></span>                                  |
| <span data-ttu-id="ad972-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad972-289">System-Flags</span></span>           | <span data-ttu-id="ad972-290">0x08000014</span><span class="sxs-lookup"><span data-stu-id="ad972-290">0x08000014</span></span>                                  |
| <span data-ttu-id="ad972-291">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ad972-291">Classes used in</span></span>        | [<span data-ttu-id="ad972-292">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="ad972-292">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





