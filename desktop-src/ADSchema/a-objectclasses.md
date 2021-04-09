---
title: Object-Classes-Attribut
description: Eine mehrwertige Eigenschaft, die Zeichen folgen enthält, die jede Klasse im Schema darstellen. Jeder Wert enthält die governsID, den ldapDisplayName, mustare, mayare und so weiter.
ms.assetid: 7e3eda48-8e64-4a52-8d92-7a0d37e513ef
ms.tgt_platform: multiple
keywords:
- AD-Schema für Object-Classes-Attribut
- AD-Schema des ObjectClasses-Attributs
topic_type:
- apiref
api_name:
- Object-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b799c725790115152ac70c0214d82a8c242ea600
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859797"
---
# <a name="object-classes-attribute"></a><span data-ttu-id="6416b-106">Object-Classes-Attribut</span><span class="sxs-lookup"><span data-stu-id="6416b-106">Object-Classes attribute</span></span>

<span data-ttu-id="6416b-107">Eine mehrwertige Eigenschaft, die Zeichen folgen enthält, die jede Klasse im Schema darstellen.</span><span class="sxs-lookup"><span data-stu-id="6416b-107">A multiple-valued property that contains strings that represent each class in the schema.</span></span> <span data-ttu-id="6416b-108">Jeder Wert enthält die governsID, den ldapDisplayName, mustare, mayare und so weiter.</span><span class="sxs-lookup"><span data-stu-id="6416b-108">Each value contains the governsID, lDAPDisplayName, mustContain, mayContain, and so on.</span></span>



| <span data-ttu-id="6416b-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6416b-109">Entry</span></span> | <span data-ttu-id="6416b-110">Wert</span><span class="sxs-lookup"><span data-stu-id="6416b-110">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="6416b-111">CN</span><span class="sxs-lookup"><span data-stu-id="6416b-111">CN</span></span>                | <span data-ttu-id="6416b-112">Object-Classes</span><span class="sxs-lookup"><span data-stu-id="6416b-112">Object-Classes</span></span>                                   |
| <span data-ttu-id="6416b-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6416b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6416b-114">ObjectClasses</span><span class="sxs-lookup"><span data-stu-id="6416b-114">objectClasses</span></span>                                    |
| <span data-ttu-id="6416b-115">Size</span><span class="sxs-lookup"><span data-stu-id="6416b-115">Size</span></span>              | <span data-ttu-id="6416b-116">Etwa 20 Bytes im Durchschnitt pro Klassenname.</span><span class="sxs-lookup"><span data-stu-id="6416b-116">About 20 bytes on average per class name.</span></span>        |
| <span data-ttu-id="6416b-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="6416b-117">Update Privilege</span></span>  | <span data-ttu-id="6416b-118">Dieser Wert wird vom Designer des-Objekts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6416b-118">The designer of the object would set this value.</span></span> |
| <span data-ttu-id="6416b-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="6416b-119">Update Frequency</span></span>  | <span data-ttu-id="6416b-120">Wenn der Entwurf der-Klasse geändert wird.</span><span class="sxs-lookup"><span data-stu-id="6416b-120">Whenever the design of the class changes.</span></span>        |
| <span data-ttu-id="6416b-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6416b-121">Attribute-Id</span></span>      | <span data-ttu-id="6416b-122">2.5.21.6</span><span class="sxs-lookup"><span data-stu-id="6416b-122">2.5.21.6</span></span>                                         |
| <span data-ttu-id="6416b-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6416b-123">System-Id-Guid</span></span>    | <span data-ttu-id="6416b-124">9a7ad94b-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="6416b-124">9a7ad94b-ca53-11d1-bbd0-0080c76670c0</span></span>             |
| <span data-ttu-id="6416b-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="6416b-125">Syntax</span></span>            | [<span data-ttu-id="6416b-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6416b-126">**String(Unicode)**</span></span>](s-string-unicode.md)      |



## <a name="implementations"></a><span data-ttu-id="6416b-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="6416b-127">Implementations</span></span>

-   [<span data-ttu-id="6416b-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6416b-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6416b-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6416b-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6416b-130">**Adam**</span><span class="sxs-lookup"><span data-stu-id="6416b-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6416b-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6416b-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6416b-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6416b-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6416b-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6416b-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6416b-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6416b-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6416b-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6416b-135">Windows 2000 Server</span></span>



| <span data-ttu-id="6416b-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6416b-136">Entry</span></span> | <span data-ttu-id="6416b-137">Wert</span><span class="sxs-lookup"><span data-stu-id="6416b-137">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="6416b-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6416b-138">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="6416b-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6416b-139">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="6416b-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="6416b-140">System-Only</span></span>            | <span data-ttu-id="6416b-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="6416b-141">True</span></span>                                        |
| <span data-ttu-id="6416b-142">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6416b-142">Is-Single-Valued</span></span>       | <span data-ttu-id="6416b-143">False</span><span class="sxs-lookup"><span data-stu-id="6416b-143">False</span></span>                                       |
| <span data-ttu-id="6416b-144">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6416b-144">Is Indexed</span></span>             | <span data-ttu-id="6416b-145">False</span><span class="sxs-lookup"><span data-stu-id="6416b-145">False</span></span>                                       |
| <span data-ttu-id="6416b-146">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6416b-146">In Global Catalog</span></span>      | <span data-ttu-id="6416b-147">False</span><span class="sxs-lookup"><span data-stu-id="6416b-147">False</span></span>                                       |
| <span data-ttu-id="6416b-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6416b-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="6416b-149">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6416b-149">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="6416b-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6416b-150">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="6416b-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6416b-151">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="6416b-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6416b-152">Search-Flags</span></span>           | <span data-ttu-id="6416b-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6416b-153">0x00000000</span></span>                                  |
| <span data-ttu-id="6416b-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6416b-154">System-Flags</span></span>           | <span data-ttu-id="6416b-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6416b-155">0x08000014</span></span>                                  |
| <span data-ttu-id="6416b-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6416b-156">Classes used in</span></span>        | [<span data-ttu-id="6416b-157">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="6416b-157">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6416b-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6416b-158">Windows Server 2003</span></span>



| <span data-ttu-id="6416b-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6416b-159">Entry</span></span> | <span data-ttu-id="6416b-160">Wert</span><span class="sxs-lookup"><span data-stu-id="6416b-160">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="6416b-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6416b-161">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="6416b-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6416b-162">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="6416b-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="6416b-163">System-Only</span></span>            | <span data-ttu-id="6416b-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="6416b-164">True</span></span>                                        |
| <span data-ttu-id="6416b-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6416b-165">Is-Single-Valued</span></span>       | <span data-ttu-id="6416b-166">False</span><span class="sxs-lookup"><span data-stu-id="6416b-166">False</span></span>                                       |
| <span data-ttu-id="6416b-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6416b-167">Is Indexed</span></span>             | <span data-ttu-id="6416b-168">False</span><span class="sxs-lookup"><span data-stu-id="6416b-168">False</span></span>                                       |
| <span data-ttu-id="6416b-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6416b-169">In Global Catalog</span></span>      | <span data-ttu-id="6416b-170">False</span><span class="sxs-lookup"><span data-stu-id="6416b-170">False</span></span>                                       |
| <span data-ttu-id="6416b-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6416b-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="6416b-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6416b-172">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="6416b-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6416b-173">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="6416b-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6416b-174">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="6416b-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6416b-175">Search-Flags</span></span>           | <span data-ttu-id="6416b-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6416b-176">0x00000000</span></span>                                  |
| <span data-ttu-id="6416b-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6416b-177">System-Flags</span></span>           | <span data-ttu-id="6416b-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6416b-178">0x08000014</span></span>                                  |
| <span data-ttu-id="6416b-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6416b-179">Classes used in</span></span>        | [<span data-ttu-id="6416b-180">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="6416b-180">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6416b-181">Adam</span><span class="sxs-lookup"><span data-stu-id="6416b-181">ADAM</span></span>



| <span data-ttu-id="6416b-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6416b-182">Entry</span></span> | <span data-ttu-id="6416b-183">Wert</span><span class="sxs-lookup"><span data-stu-id="6416b-183">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="6416b-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6416b-184">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="6416b-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6416b-185">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="6416b-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="6416b-186">System-Only</span></span>            | <span data-ttu-id="6416b-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="6416b-187">True</span></span>                                        |
| <span data-ttu-id="6416b-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6416b-188">Is-Single-Valued</span></span>       | <span data-ttu-id="6416b-189">False</span><span class="sxs-lookup"><span data-stu-id="6416b-189">False</span></span>                                       |
| <span data-ttu-id="6416b-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6416b-190">Is Indexed</span></span>             | <span data-ttu-id="6416b-191">False</span><span class="sxs-lookup"><span data-stu-id="6416b-191">False</span></span>                                       |
| <span data-ttu-id="6416b-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6416b-192">In Global Catalog</span></span>      | <span data-ttu-id="6416b-193">False</span><span class="sxs-lookup"><span data-stu-id="6416b-193">False</span></span>                                       |
| <span data-ttu-id="6416b-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6416b-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="6416b-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6416b-195">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="6416b-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6416b-196">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="6416b-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6416b-197">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="6416b-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6416b-198">Search-Flags</span></span>           | <span data-ttu-id="6416b-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6416b-199">0x00000000</span></span>                                  |
| <span data-ttu-id="6416b-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6416b-200">System-Flags</span></span>           | <span data-ttu-id="6416b-201">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6416b-201">0x08000014</span></span>                                  |
| <span data-ttu-id="6416b-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6416b-202">Classes used in</span></span>        | [<span data-ttu-id="6416b-203">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="6416b-203">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6416b-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6416b-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6416b-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6416b-205">Entry</span></span> | <span data-ttu-id="6416b-206">Wert</span><span class="sxs-lookup"><span data-stu-id="6416b-206">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="6416b-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6416b-207">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="6416b-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6416b-208">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="6416b-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="6416b-209">System-Only</span></span>            | <span data-ttu-id="6416b-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="6416b-210">True</span></span>                                        |
| <span data-ttu-id="6416b-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6416b-211">Is-Single-Valued</span></span>       | <span data-ttu-id="6416b-212">False</span><span class="sxs-lookup"><span data-stu-id="6416b-212">False</span></span>                                       |
| <span data-ttu-id="6416b-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6416b-213">Is Indexed</span></span>             | <span data-ttu-id="6416b-214">False</span><span class="sxs-lookup"><span data-stu-id="6416b-214">False</span></span>                                       |
| <span data-ttu-id="6416b-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6416b-215">In Global Catalog</span></span>      | <span data-ttu-id="6416b-216">False</span><span class="sxs-lookup"><span data-stu-id="6416b-216">False</span></span>                                       |
| <span data-ttu-id="6416b-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6416b-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="6416b-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6416b-218">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="6416b-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6416b-219">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="6416b-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6416b-220">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="6416b-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6416b-221">Search-Flags</span></span>           | <span data-ttu-id="6416b-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6416b-222">0x00000000</span></span>                                  |
| <span data-ttu-id="6416b-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6416b-223">System-Flags</span></span>           | <span data-ttu-id="6416b-224">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6416b-224">0x08000014</span></span>                                  |
| <span data-ttu-id="6416b-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6416b-225">Classes used in</span></span>        | [<span data-ttu-id="6416b-226">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="6416b-226">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6416b-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6416b-227">Windows Server 2008</span></span>



| <span data-ttu-id="6416b-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6416b-228">Entry</span></span> | <span data-ttu-id="6416b-229">Wert</span><span class="sxs-lookup"><span data-stu-id="6416b-229">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="6416b-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6416b-230">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="6416b-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6416b-231">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="6416b-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="6416b-232">System-Only</span></span>            | <span data-ttu-id="6416b-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="6416b-233">True</span></span>                                        |
| <span data-ttu-id="6416b-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6416b-234">Is-Single-Valued</span></span>       | <span data-ttu-id="6416b-235">False</span><span class="sxs-lookup"><span data-stu-id="6416b-235">False</span></span>                                       |
| <span data-ttu-id="6416b-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6416b-236">Is Indexed</span></span>             | <span data-ttu-id="6416b-237">False</span><span class="sxs-lookup"><span data-stu-id="6416b-237">False</span></span>                                       |
| <span data-ttu-id="6416b-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6416b-238">In Global Catalog</span></span>      | <span data-ttu-id="6416b-239">False</span><span class="sxs-lookup"><span data-stu-id="6416b-239">False</span></span>                                       |
| <span data-ttu-id="6416b-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6416b-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="6416b-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6416b-241">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="6416b-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6416b-242">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="6416b-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6416b-243">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="6416b-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6416b-244">Search-Flags</span></span>           | <span data-ttu-id="6416b-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6416b-245">0x00000000</span></span>                                  |
| <span data-ttu-id="6416b-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6416b-246">System-Flags</span></span>           | <span data-ttu-id="6416b-247">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6416b-247">0x08000014</span></span>                                  |
| <span data-ttu-id="6416b-248">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6416b-248">Classes used in</span></span>        | [<span data-ttu-id="6416b-249">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="6416b-249">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6416b-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6416b-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6416b-251">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6416b-251">Entry</span></span> | <span data-ttu-id="6416b-252">Wert</span><span class="sxs-lookup"><span data-stu-id="6416b-252">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="6416b-253">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6416b-253">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="6416b-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6416b-254">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="6416b-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="6416b-255">System-Only</span></span>            | <span data-ttu-id="6416b-256">Richtig</span><span class="sxs-lookup"><span data-stu-id="6416b-256">True</span></span>                                        |
| <span data-ttu-id="6416b-257">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6416b-257">Is-Single-Valued</span></span>       | <span data-ttu-id="6416b-258">False</span><span class="sxs-lookup"><span data-stu-id="6416b-258">False</span></span>                                       |
| <span data-ttu-id="6416b-259">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6416b-259">Is Indexed</span></span>             | <span data-ttu-id="6416b-260">False</span><span class="sxs-lookup"><span data-stu-id="6416b-260">False</span></span>                                       |
| <span data-ttu-id="6416b-261">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6416b-261">In Global Catalog</span></span>      | <span data-ttu-id="6416b-262">False</span><span class="sxs-lookup"><span data-stu-id="6416b-262">False</span></span>                                       |
| <span data-ttu-id="6416b-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6416b-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="6416b-264">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6416b-264">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="6416b-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6416b-265">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="6416b-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6416b-266">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="6416b-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6416b-267">Search-Flags</span></span>           | <span data-ttu-id="6416b-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6416b-268">0x00000000</span></span>                                  |
| <span data-ttu-id="6416b-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6416b-269">System-Flags</span></span>           | <span data-ttu-id="6416b-270">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6416b-270">0x08000014</span></span>                                  |
| <span data-ttu-id="6416b-271">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6416b-271">Classes used in</span></span>        | [<span data-ttu-id="6416b-272">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="6416b-272">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6416b-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6416b-273">Windows Server 2012</span></span>



| <span data-ttu-id="6416b-274">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6416b-274">Entry</span></span> | <span data-ttu-id="6416b-275">Wert</span><span class="sxs-lookup"><span data-stu-id="6416b-275">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="6416b-276">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6416b-276">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="6416b-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6416b-277">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="6416b-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="6416b-278">System-Only</span></span>            | <span data-ttu-id="6416b-279">Richtig</span><span class="sxs-lookup"><span data-stu-id="6416b-279">True</span></span>                                        |
| <span data-ttu-id="6416b-280">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6416b-280">Is-Single-Valued</span></span>       | <span data-ttu-id="6416b-281">False</span><span class="sxs-lookup"><span data-stu-id="6416b-281">False</span></span>                                       |
| <span data-ttu-id="6416b-282">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6416b-282">Is Indexed</span></span>             | <span data-ttu-id="6416b-283">False</span><span class="sxs-lookup"><span data-stu-id="6416b-283">False</span></span>                                       |
| <span data-ttu-id="6416b-284">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6416b-284">In Global Catalog</span></span>      | <span data-ttu-id="6416b-285">False</span><span class="sxs-lookup"><span data-stu-id="6416b-285">False</span></span>                                       |
| <span data-ttu-id="6416b-286">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6416b-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="6416b-287">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6416b-287">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="6416b-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6416b-288">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="6416b-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6416b-289">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="6416b-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6416b-290">Search-Flags</span></span>           | <span data-ttu-id="6416b-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6416b-291">0x00000000</span></span>                                  |
| <span data-ttu-id="6416b-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6416b-292">System-Flags</span></span>           | <span data-ttu-id="6416b-293">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6416b-293">0x08000014</span></span>                                  |
| <span data-ttu-id="6416b-294">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6416b-294">Classes used in</span></span>        | [<span data-ttu-id="6416b-295">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="6416b-295">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





