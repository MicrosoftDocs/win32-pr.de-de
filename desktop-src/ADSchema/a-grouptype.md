---
title: Group-Type-Attribut
description: Enthält einen Satz von Flags, die den Typ und den Gültigkeitsbereich eines Gruppen Objekts definieren.
ms.assetid: cd37ed2f-8503-4227-b0d2-c8135605cb84
ms.tgt_platform: multiple
keywords:
- AD-Schema für Group-Type-Attribut
- GroupType-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Group-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e1db8f102e7e56b38d15d74fedb7c5a5366ee47
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106342500"
---
# <a name="group-type-attribute"></a><span data-ttu-id="d258e-105">Group-Type-Attribut</span><span class="sxs-lookup"><span data-stu-id="d258e-105">Group-Type attribute</span></span>

<span data-ttu-id="d258e-106">Enthält einen Satz von Flags, die den Typ und den Gültigkeitsbereich eines Gruppen Objekts definieren.</span><span class="sxs-lookup"><span data-stu-id="d258e-106">Contains a set of flags that define the type and scope of a group object.</span></span> <span data-ttu-id="d258e-107">Die möglichen Werte für dieses Attribut finden Sie unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="d258e-107">For the possible values for this attribute, see Remarks.</span></span>



| <span data-ttu-id="d258e-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d258e-108">Entry</span></span> | <span data-ttu-id="d258e-109">Wert</span><span class="sxs-lookup"><span data-stu-id="d258e-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d258e-110">CN</span><span class="sxs-lookup"><span data-stu-id="d258e-110">CN</span></span>                | <span data-ttu-id="d258e-111">Group-Type</span><span class="sxs-lookup"><span data-stu-id="d258e-111">Group-Type</span></span>                           |
| <span data-ttu-id="d258e-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d258e-112">Ldap-Display-Name</span></span> | <span data-ttu-id="d258e-113">groupType</span><span class="sxs-lookup"><span data-stu-id="d258e-113">groupType</span></span>                            |
| <span data-ttu-id="d258e-114">Size</span><span class="sxs-lookup"><span data-stu-id="d258e-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="d258e-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d258e-115">Update Privilege</span></span>  | <span data-ttu-id="d258e-116">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="d258e-116">Domain administrator</span></span>                 |
| <span data-ttu-id="d258e-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="d258e-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="d258e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d258e-118">Attribute-Id</span></span>      | <span data-ttu-id="d258e-119">1.2.840.113556.1.4.750</span><span class="sxs-lookup"><span data-stu-id="d258e-119">1.2.840.113556.1.4.750</span></span>               |
| <span data-ttu-id="d258e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d258e-120">System-Id-Guid</span></span>    | <span data-ttu-id="d258e-121">9a9a021e-4a5b-11d1-a9c3-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="d258e-121">9a9a021e-4a5b-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="d258e-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="d258e-122">Syntax</span></span>            | [<span data-ttu-id="d258e-123">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="d258e-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="d258e-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="d258e-124">Implementations</span></span>

-   [<span data-ttu-id="d258e-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d258e-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d258e-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d258e-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d258e-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="d258e-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d258e-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d258e-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d258e-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d258e-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d258e-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d258e-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d258e-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d258e-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d258e-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d258e-132">Windows 2000 Server</span></span>



| <span data-ttu-id="d258e-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d258e-133">Entry</span></span> | <span data-ttu-id="d258e-134">Wert</span><span class="sxs-lookup"><span data-stu-id="d258e-134">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="d258e-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d258e-135">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="d258e-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d258e-136">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="d258e-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="d258e-137">System-Only</span></span>            | <span data-ttu-id="d258e-138">False</span><span class="sxs-lookup"><span data-stu-id="d258e-138">False</span></span>                               |
| <span data-ttu-id="d258e-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d258e-139">Is-Single-Valued</span></span>       | <span data-ttu-id="d258e-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="d258e-140">True</span></span>                                |
| <span data-ttu-id="d258e-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d258e-141">Is Indexed</span></span>             | <span data-ttu-id="d258e-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="d258e-142">True</span></span>                                |
| <span data-ttu-id="d258e-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d258e-143">In Global Catalog</span></span>      | <span data-ttu-id="d258e-144">Richtig</span><span class="sxs-lookup"><span data-stu-id="d258e-144">True</span></span>                                |
| <span data-ttu-id="d258e-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d258e-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="d258e-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d258e-146">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="d258e-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d258e-147">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="d258e-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d258e-148">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="d258e-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d258e-149">Search-Flags</span></span>           | <span data-ttu-id="d258e-150">0x00000009</span><span class="sxs-lookup"><span data-stu-id="d258e-150">0x00000009</span></span>                          |
| <span data-ttu-id="d258e-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d258e-151">System-Flags</span></span>           | <span data-ttu-id="d258e-152">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d258e-152">0x00000012</span></span>                          |
| <span data-ttu-id="d258e-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d258e-153">Classes used in</span></span>        | [<span data-ttu-id="d258e-154">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="d258e-154">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d258e-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d258e-155">Windows Server 2003</span></span>



| <span data-ttu-id="d258e-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d258e-156">Entry</span></span> | <span data-ttu-id="d258e-157">Wert</span><span class="sxs-lookup"><span data-stu-id="d258e-157">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="d258e-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d258e-158">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="d258e-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d258e-159">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="d258e-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="d258e-160">System-Only</span></span>            | <span data-ttu-id="d258e-161">False</span><span class="sxs-lookup"><span data-stu-id="d258e-161">False</span></span>                               |
| <span data-ttu-id="d258e-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d258e-162">Is-Single-Valued</span></span>       | <span data-ttu-id="d258e-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="d258e-163">True</span></span>                                |
| <span data-ttu-id="d258e-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d258e-164">Is Indexed</span></span>             | <span data-ttu-id="d258e-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="d258e-165">True</span></span>                                |
| <span data-ttu-id="d258e-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d258e-166">In Global Catalog</span></span>      | <span data-ttu-id="d258e-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="d258e-167">True</span></span>                                |
| <span data-ttu-id="d258e-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d258e-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="d258e-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d258e-169">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="d258e-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d258e-170">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="d258e-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d258e-171">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="d258e-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d258e-172">Search-Flags</span></span>           | <span data-ttu-id="d258e-173">0x00000009</span><span class="sxs-lookup"><span data-stu-id="d258e-173">0x00000009</span></span>                          |
| <span data-ttu-id="d258e-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d258e-174">System-Flags</span></span>           | <span data-ttu-id="d258e-175">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d258e-175">0x00000012</span></span>                          |
| <span data-ttu-id="d258e-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d258e-176">Classes used in</span></span>        | [<span data-ttu-id="d258e-177">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="d258e-177">**Group**</span></span>](c-group.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d258e-178">Adam</span><span class="sxs-lookup"><span data-stu-id="d258e-178">ADAM</span></span>



| <span data-ttu-id="d258e-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d258e-179">Entry</span></span> | <span data-ttu-id="d258e-180">Wert</span><span class="sxs-lookup"><span data-stu-id="d258e-180">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="d258e-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d258e-181">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="d258e-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d258e-182">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="d258e-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="d258e-183">System-Only</span></span>            | <span data-ttu-id="d258e-184">False</span><span class="sxs-lookup"><span data-stu-id="d258e-184">False</span></span>                               |
| <span data-ttu-id="d258e-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d258e-185">Is-Single-Valued</span></span>       | <span data-ttu-id="d258e-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="d258e-186">True</span></span>                                |
| <span data-ttu-id="d258e-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d258e-187">Is Indexed</span></span>             | <span data-ttu-id="d258e-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="d258e-188">True</span></span>                                |
| <span data-ttu-id="d258e-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d258e-189">In Global Catalog</span></span>      | <span data-ttu-id="d258e-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="d258e-190">True</span></span>                                |
| <span data-ttu-id="d258e-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d258e-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="d258e-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d258e-192">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="d258e-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d258e-193">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="d258e-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d258e-194">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="d258e-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d258e-195">Search-Flags</span></span>           | <span data-ttu-id="d258e-196">0x00000009</span><span class="sxs-lookup"><span data-stu-id="d258e-196">0x00000009</span></span>                          |
| <span data-ttu-id="d258e-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d258e-197">System-Flags</span></span>           | <span data-ttu-id="d258e-198">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d258e-198">0x00000012</span></span>                          |
| <span data-ttu-id="d258e-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d258e-199">Classes used in</span></span>        | [<span data-ttu-id="d258e-200">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="d258e-200">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d258e-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d258e-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d258e-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d258e-202">Entry</span></span> | <span data-ttu-id="d258e-203">Wert</span><span class="sxs-lookup"><span data-stu-id="d258e-203">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="d258e-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d258e-204">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="d258e-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d258e-205">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="d258e-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="d258e-206">System-Only</span></span>            | <span data-ttu-id="d258e-207">False</span><span class="sxs-lookup"><span data-stu-id="d258e-207">False</span></span>                               |
| <span data-ttu-id="d258e-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d258e-208">Is-Single-Valued</span></span>       | <span data-ttu-id="d258e-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="d258e-209">True</span></span>                                |
| <span data-ttu-id="d258e-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d258e-210">Is Indexed</span></span>             | <span data-ttu-id="d258e-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="d258e-211">True</span></span>                                |
| <span data-ttu-id="d258e-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d258e-212">In Global Catalog</span></span>      | <span data-ttu-id="d258e-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="d258e-213">True</span></span>                                |
| <span data-ttu-id="d258e-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d258e-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="d258e-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d258e-215">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="d258e-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d258e-216">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="d258e-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d258e-217">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="d258e-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d258e-218">Search-Flags</span></span>           | <span data-ttu-id="d258e-219">0x00000009</span><span class="sxs-lookup"><span data-stu-id="d258e-219">0x00000009</span></span>                          |
| <span data-ttu-id="d258e-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d258e-220">System-Flags</span></span>           | <span data-ttu-id="d258e-221">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d258e-221">0x00000012</span></span>                          |
| <span data-ttu-id="d258e-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d258e-222">Classes used in</span></span>        | [<span data-ttu-id="d258e-223">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="d258e-223">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d258e-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d258e-224">Windows Server 2008</span></span>



| <span data-ttu-id="d258e-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d258e-225">Entry</span></span> | <span data-ttu-id="d258e-226">Wert</span><span class="sxs-lookup"><span data-stu-id="d258e-226">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="d258e-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d258e-227">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="d258e-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d258e-228">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="d258e-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="d258e-229">System-Only</span></span>            | <span data-ttu-id="d258e-230">False</span><span class="sxs-lookup"><span data-stu-id="d258e-230">False</span></span>                               |
| <span data-ttu-id="d258e-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d258e-231">Is-Single-Valued</span></span>       | <span data-ttu-id="d258e-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="d258e-232">True</span></span>                                |
| <span data-ttu-id="d258e-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d258e-233">Is Indexed</span></span>             | <span data-ttu-id="d258e-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="d258e-234">True</span></span>                                |
| <span data-ttu-id="d258e-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d258e-235">In Global Catalog</span></span>      | <span data-ttu-id="d258e-236">Richtig</span><span class="sxs-lookup"><span data-stu-id="d258e-236">True</span></span>                                |
| <span data-ttu-id="d258e-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d258e-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="d258e-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d258e-238">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="d258e-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d258e-239">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="d258e-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d258e-240">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="d258e-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d258e-241">Search-Flags</span></span>           | <span data-ttu-id="d258e-242">0x00000009</span><span class="sxs-lookup"><span data-stu-id="d258e-242">0x00000009</span></span>                          |
| <span data-ttu-id="d258e-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d258e-243">System-Flags</span></span>           | <span data-ttu-id="d258e-244">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d258e-244">0x00000012</span></span>                          |
| <span data-ttu-id="d258e-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d258e-245">Classes used in</span></span>        | [<span data-ttu-id="d258e-246">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="d258e-246">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d258e-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d258e-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d258e-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d258e-248">Entry</span></span> | <span data-ttu-id="d258e-249">Wert</span><span class="sxs-lookup"><span data-stu-id="d258e-249">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="d258e-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d258e-250">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="d258e-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d258e-251">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="d258e-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="d258e-252">System-Only</span></span>            | <span data-ttu-id="d258e-253">False</span><span class="sxs-lookup"><span data-stu-id="d258e-253">False</span></span>                               |
| <span data-ttu-id="d258e-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d258e-254">Is-Single-Valued</span></span>       | <span data-ttu-id="d258e-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="d258e-255">True</span></span>                                |
| <span data-ttu-id="d258e-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d258e-256">Is Indexed</span></span>             | <span data-ttu-id="d258e-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="d258e-257">True</span></span>                                |
| <span data-ttu-id="d258e-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d258e-258">In Global Catalog</span></span>      | <span data-ttu-id="d258e-259">Richtig</span><span class="sxs-lookup"><span data-stu-id="d258e-259">True</span></span>                                |
| <span data-ttu-id="d258e-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d258e-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="d258e-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d258e-261">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="d258e-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d258e-262">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="d258e-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d258e-263">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="d258e-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d258e-264">Search-Flags</span></span>           | <span data-ttu-id="d258e-265">0x00000009</span><span class="sxs-lookup"><span data-stu-id="d258e-265">0x00000009</span></span>                          |
| <span data-ttu-id="d258e-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d258e-266">System-Flags</span></span>           | <span data-ttu-id="d258e-267">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d258e-267">0x00000012</span></span>                          |
| <span data-ttu-id="d258e-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d258e-268">Classes used in</span></span>        | [<span data-ttu-id="d258e-269">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="d258e-269">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d258e-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d258e-270">Windows Server 2012</span></span>



| <span data-ttu-id="d258e-271">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d258e-271">Entry</span></span> | <span data-ttu-id="d258e-272">Wert</span><span class="sxs-lookup"><span data-stu-id="d258e-272">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="d258e-273">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d258e-273">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="d258e-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d258e-274">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="d258e-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="d258e-275">System-Only</span></span>            | <span data-ttu-id="d258e-276">False</span><span class="sxs-lookup"><span data-stu-id="d258e-276">False</span></span>                               |
| <span data-ttu-id="d258e-277">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d258e-277">Is-Single-Valued</span></span>       | <span data-ttu-id="d258e-278">Richtig</span><span class="sxs-lookup"><span data-stu-id="d258e-278">True</span></span>                                |
| <span data-ttu-id="d258e-279">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d258e-279">Is Indexed</span></span>             | <span data-ttu-id="d258e-280">Richtig</span><span class="sxs-lookup"><span data-stu-id="d258e-280">True</span></span>                                |
| <span data-ttu-id="d258e-281">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d258e-281">In Global Catalog</span></span>      | <span data-ttu-id="d258e-282">Richtig</span><span class="sxs-lookup"><span data-stu-id="d258e-282">True</span></span>                                |
| <span data-ttu-id="d258e-283">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d258e-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="d258e-284">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d258e-284">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="d258e-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d258e-285">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="d258e-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d258e-286">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="d258e-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d258e-287">Search-Flags</span></span>           | <span data-ttu-id="d258e-288">0x00000009</span><span class="sxs-lookup"><span data-stu-id="d258e-288">0x00000009</span></span>                          |
| <span data-ttu-id="d258e-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d258e-289">System-Flags</span></span>           | <span data-ttu-id="d258e-290">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d258e-290">0x00000012</span></span>                          |
| <span data-ttu-id="d258e-291">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d258e-291">Classes used in</span></span>        | [<span data-ttu-id="d258e-292">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="d258e-292">**Group**</span></span>](c-group.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d258e-293">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d258e-293">Remarks</span></span>

<span data-ttu-id="d258e-294">Dieses Attribut kann NULL sein oder eine Kombination aus einem oder mehreren der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d258e-294">This attribute can be zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="d258e-295">Wert</span><span class="sxs-lookup"><span data-stu-id="d258e-295">Value</span></span>                   | <span data-ttu-id="d258e-296">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d258e-296">Description</span></span>                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d258e-297">1 (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="d258e-297">1 (0x00000001)</span></span>          | <span data-ttu-id="d258e-298">Gibt eine Gruppe an, die vom System erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d258e-298">Specifies a group that is created by the system.</span></span>                                             |
| <span data-ttu-id="d258e-299">2 (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="d258e-299">2 (0x00000002)</span></span>          | <span data-ttu-id="d258e-300">Gibt eine Gruppe mit globalem Gültigkeitsbereich an.</span><span class="sxs-lookup"><span data-stu-id="d258e-300">Specifies a group with global scope.</span></span>                                                         |
| <span data-ttu-id="d258e-301">4 (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="d258e-301">4 (0x00000004)</span></span>          | <span data-ttu-id="d258e-302">Gibt eine Gruppe mit lokalem Domänen Bereich an.</span><span class="sxs-lookup"><span data-stu-id="d258e-302">Specifies a group with domain local scope.</span></span>                                                   |
| <span data-ttu-id="d258e-303">8 (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="d258e-303">8 (0x00000008)</span></span>          | <span data-ttu-id="d258e-304">Gibt eine Gruppe mit universellem Gültigkeitsbereich an.</span><span class="sxs-lookup"><span data-stu-id="d258e-304">Specifies a group with universal scope.</span></span>                                                      |
| <span data-ttu-id="d258e-305">16 (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="d258e-305">16 (0x00000010)</span></span>         | <span data-ttu-id="d258e-306">Gibt eine APP- \_ Basisgruppe für den Windows Server Authorization Manager an.</span><span class="sxs-lookup"><span data-stu-id="d258e-306">Specifies an APP\_BASIC group for Windows Server Authorization Manager.</span></span>                      |
| <span data-ttu-id="d258e-307">32 (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="d258e-307">32 (0x00000020)</span></span>         | <span data-ttu-id="d258e-308">Gibt eine APP- \_ Abfrage Gruppe für den Windows Server Authorization Manager an.</span><span class="sxs-lookup"><span data-stu-id="d258e-308">Specifies an APP\_QUERY group for Windows Server Authorization Manager.</span></span>                      |
| <span data-ttu-id="d258e-309">2147483648 (0x80000000)</span><span class="sxs-lookup"><span data-stu-id="d258e-309">2147483648 (0x80000000)</span></span> | <span data-ttu-id="d258e-310">Gibt eine Sicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="d258e-310">Specifies a security group.</span></span> <span data-ttu-id="d258e-311">Wenn dieses Flag nicht festgelegt ist, handelt es sich bei der Gruppe um eine Verteiler Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d258e-311">If this flag is not set, then the group is a distribution group.</span></span> |



 

<span data-ttu-id="d258e-312">Weitere Informationen zu Gruppentyp und Gültigkeitsbereich finden Sie in den Themen zu [Gruppen Typen](/previous-versions/windows/it-pro/windows-server-2003/cc781446(v=ws.10)) und [Gruppenbereich](/previous-versions/windows/it-pro/windows-server-2003/cc755692(v=ws.10)) in Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="d258e-312">For more information about group type and scope, see the [Group types](/previous-versions/windows/it-pro/windows-server-2003/cc781446(v=ws.10)) and [Group scope](/previous-versions/windows/it-pro/windows-server-2003/cc755692(v=ws.10)) topics on Microsoft TechNet.</span></span>

 

