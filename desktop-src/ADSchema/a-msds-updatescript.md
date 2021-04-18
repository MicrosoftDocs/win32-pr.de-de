---
title: ms-DS-updateScript-Attribut
description: Dies wird zum Speichern des Skripts mit den Anweisungen für die Domänen Umstrukturierung verwendet.
ms.assetid: a9dd205d-f6c3-4eeb-95dc-491bfe30ab8b
ms.tgt_platform: multiple
keywords:
- AD-Schema des ms-DS-updateScript-Attributs
- AD-Schema des msDS-updateScript-Attributs
topic_type:
- apiref
api_name:
- ms-DS-UpdateScript
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7809bf6fdbaabb38976068d1998cacfb12bdaf3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106343525"
---
# <a name="ms-ds-updatescript-attribute"></a><span data-ttu-id="325f1-105">ms-DS-updateScript-Attribut</span><span class="sxs-lookup"><span data-stu-id="325f1-105">ms-DS-UpdateScript attribute</span></span>

<span data-ttu-id="325f1-106">Dies wird zum Speichern des Skripts mit den Anweisungen für die Domänen Umstrukturierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="325f1-106">This is used to hold the script with the domain restructure instructions.</span></span>



| <span data-ttu-id="325f1-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="325f1-107">Entry</span></span> | <span data-ttu-id="325f1-108">Wert</span><span class="sxs-lookup"><span data-stu-id="325f1-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="325f1-109">CN</span><span class="sxs-lookup"><span data-stu-id="325f1-109">CN</span></span>                | <span data-ttu-id="325f1-110">ms-DS-updateScript</span><span class="sxs-lookup"><span data-stu-id="325f1-110">ms-DS-UpdateScript</span></span>                          |
| <span data-ttu-id="325f1-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="325f1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="325f1-112">MSDS-updateScript</span><span class="sxs-lookup"><span data-stu-id="325f1-112">msDS-UpdateScript</span></span>                           |
| <span data-ttu-id="325f1-113">Size</span><span class="sxs-lookup"><span data-stu-id="325f1-113">Size</span></span>              | <span data-ttu-id="325f1-114">Maximale Größe von 10K bytes.</span><span class="sxs-lookup"><span data-stu-id="325f1-114">Maximum size 10K bytes.</span></span>                     |
| <span data-ttu-id="325f1-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="325f1-115">Update Privilege</span></span>  | <span data-ttu-id="325f1-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="325f1-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="325f1-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="325f1-117">Update Frequency</span></span>  | <span data-ttu-id="325f1-118">Nur während der Domänen Umstrukturierung.</span><span class="sxs-lookup"><span data-stu-id="325f1-118">Only during domain restructure.</span></span>             |
| <span data-ttu-id="325f1-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="325f1-119">Attribute-Id</span></span>      | <span data-ttu-id="325f1-120">1.2.840.113556.1.4.1721</span><span class="sxs-lookup"><span data-stu-id="325f1-120">1.2.840.113556.1.4.1721</span></span>                     |
| <span data-ttu-id="325f1-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="325f1-121">System-Id-Guid</span></span>    | <span data-ttu-id="325f1-122">146 eb639-bb9f-4fc1-a825-e29e00c77920</span><span class="sxs-lookup"><span data-stu-id="325f1-122">146eb639-bb9f-4fc1-a825-e29e00c77920</span></span>        |
| <span data-ttu-id="325f1-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="325f1-123">Syntax</span></span>            | [<span data-ttu-id="325f1-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="325f1-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="325f1-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="325f1-125">Implementations</span></span>

-   [<span data-ttu-id="325f1-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="325f1-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="325f1-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="325f1-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="325f1-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="325f1-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="325f1-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="325f1-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="325f1-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="325f1-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="325f1-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="325f1-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="325f1-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="325f1-132">Windows Server 2003</span></span>



| <span data-ttu-id="325f1-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="325f1-133">Entry</span></span> | <span data-ttu-id="325f1-134">Wert</span><span class="sxs-lookup"><span data-stu-id="325f1-134">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="325f1-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="325f1-135">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="325f1-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="325f1-136">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="325f1-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="325f1-137">System-Only</span></span>            | <span data-ttu-id="325f1-138">False</span><span class="sxs-lookup"><span data-stu-id="325f1-138">False</span></span>                                                         |
| <span data-ttu-id="325f1-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="325f1-139">Is-Single-Valued</span></span>       | <span data-ttu-id="325f1-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="325f1-140">True</span></span>                                                          |
| <span data-ttu-id="325f1-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="325f1-141">Is Indexed</span></span>             | <span data-ttu-id="325f1-142">False</span><span class="sxs-lookup"><span data-stu-id="325f1-142">False</span></span>                                                         |
| <span data-ttu-id="325f1-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="325f1-143">In Global Catalog</span></span>      | <span data-ttu-id="325f1-144">False</span><span class="sxs-lookup"><span data-stu-id="325f1-144">False</span></span>                                                         |
| <span data-ttu-id="325f1-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="325f1-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="325f1-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="325f1-146">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="325f1-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="325f1-147">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="325f1-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="325f1-148">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="325f1-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="325f1-149">Search-Flags</span></span>           | <span data-ttu-id="325f1-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="325f1-150">0x00000000</span></span>                                                    |
| <span data-ttu-id="325f1-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="325f1-151">System-Flags</span></span>           | <span data-ttu-id="325f1-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="325f1-152">0x00000010</span></span>                                                    |
| <span data-ttu-id="325f1-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="325f1-153">Classes used in</span></span>        | [<span data-ttu-id="325f1-154">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="325f1-154">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="325f1-155">Adam</span><span class="sxs-lookup"><span data-stu-id="325f1-155">ADAM</span></span>



| <span data-ttu-id="325f1-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="325f1-156">Entry</span></span> | <span data-ttu-id="325f1-157">Wert</span><span class="sxs-lookup"><span data-stu-id="325f1-157">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="325f1-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="325f1-158">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="325f1-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="325f1-159">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="325f1-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="325f1-160">System-Only</span></span>            | <span data-ttu-id="325f1-161">False</span><span class="sxs-lookup"><span data-stu-id="325f1-161">False</span></span>                                                         |
| <span data-ttu-id="325f1-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="325f1-162">Is-Single-Valued</span></span>       | <span data-ttu-id="325f1-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="325f1-163">True</span></span>                                                          |
| <span data-ttu-id="325f1-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="325f1-164">Is Indexed</span></span>             | <span data-ttu-id="325f1-165">False</span><span class="sxs-lookup"><span data-stu-id="325f1-165">False</span></span>                                                         |
| <span data-ttu-id="325f1-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="325f1-166">In Global Catalog</span></span>      | <span data-ttu-id="325f1-167">False</span><span class="sxs-lookup"><span data-stu-id="325f1-167">False</span></span>                                                         |
| <span data-ttu-id="325f1-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="325f1-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="325f1-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="325f1-169">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="325f1-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="325f1-170">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="325f1-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="325f1-171">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="325f1-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="325f1-172">Search-Flags</span></span>           | <span data-ttu-id="325f1-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="325f1-173">0x00000000</span></span>                                                    |
| <span data-ttu-id="325f1-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="325f1-174">System-Flags</span></span>           | <span data-ttu-id="325f1-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="325f1-175">0x00000010</span></span>                                                    |
| <span data-ttu-id="325f1-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="325f1-176">Classes used in</span></span>        | [<span data-ttu-id="325f1-177">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="325f1-177">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="325f1-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="325f1-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="325f1-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="325f1-179">Entry</span></span> | <span data-ttu-id="325f1-180">Wert</span><span class="sxs-lookup"><span data-stu-id="325f1-180">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="325f1-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="325f1-181">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="325f1-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="325f1-182">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="325f1-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="325f1-183">System-Only</span></span>            | <span data-ttu-id="325f1-184">False</span><span class="sxs-lookup"><span data-stu-id="325f1-184">False</span></span>                                                         |
| <span data-ttu-id="325f1-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="325f1-185">Is-Single-Valued</span></span>       | <span data-ttu-id="325f1-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="325f1-186">True</span></span>                                                          |
| <span data-ttu-id="325f1-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="325f1-187">Is Indexed</span></span>             | <span data-ttu-id="325f1-188">False</span><span class="sxs-lookup"><span data-stu-id="325f1-188">False</span></span>                                                         |
| <span data-ttu-id="325f1-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="325f1-189">In Global Catalog</span></span>      | <span data-ttu-id="325f1-190">False</span><span class="sxs-lookup"><span data-stu-id="325f1-190">False</span></span>                                                         |
| <span data-ttu-id="325f1-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="325f1-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="325f1-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="325f1-192">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="325f1-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="325f1-193">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="325f1-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="325f1-194">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="325f1-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="325f1-195">Search-Flags</span></span>           | <span data-ttu-id="325f1-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="325f1-196">0x00000000</span></span>                                                    |
| <span data-ttu-id="325f1-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="325f1-197">System-Flags</span></span>           | <span data-ttu-id="325f1-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="325f1-198">0x00000010</span></span>                                                    |
| <span data-ttu-id="325f1-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="325f1-199">Classes used in</span></span>        | [<span data-ttu-id="325f1-200">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="325f1-200">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="325f1-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="325f1-201">Windows Server 2008</span></span>



| <span data-ttu-id="325f1-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="325f1-202">Entry</span></span> | <span data-ttu-id="325f1-203">Wert</span><span class="sxs-lookup"><span data-stu-id="325f1-203">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="325f1-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="325f1-204">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="325f1-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="325f1-205">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="325f1-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="325f1-206">System-Only</span></span>            | <span data-ttu-id="325f1-207">False</span><span class="sxs-lookup"><span data-stu-id="325f1-207">False</span></span>                                                         |
| <span data-ttu-id="325f1-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="325f1-208">Is-Single-Valued</span></span>       | <span data-ttu-id="325f1-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="325f1-209">True</span></span>                                                          |
| <span data-ttu-id="325f1-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="325f1-210">Is Indexed</span></span>             | <span data-ttu-id="325f1-211">False</span><span class="sxs-lookup"><span data-stu-id="325f1-211">False</span></span>                                                         |
| <span data-ttu-id="325f1-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="325f1-212">In Global Catalog</span></span>      | <span data-ttu-id="325f1-213">False</span><span class="sxs-lookup"><span data-stu-id="325f1-213">False</span></span>                                                         |
| <span data-ttu-id="325f1-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="325f1-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="325f1-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="325f1-215">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="325f1-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="325f1-216">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="325f1-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="325f1-217">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="325f1-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="325f1-218">Search-Flags</span></span>           | <span data-ttu-id="325f1-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="325f1-219">0x00000000</span></span>                                                    |
| <span data-ttu-id="325f1-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="325f1-220">System-Flags</span></span>           | <span data-ttu-id="325f1-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="325f1-221">0x00000010</span></span>                                                    |
| <span data-ttu-id="325f1-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="325f1-222">Classes used in</span></span>        | [<span data-ttu-id="325f1-223">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="325f1-223">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="325f1-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="325f1-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="325f1-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="325f1-225">Entry</span></span> | <span data-ttu-id="325f1-226">Wert</span><span class="sxs-lookup"><span data-stu-id="325f1-226">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="325f1-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="325f1-227">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="325f1-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="325f1-228">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="325f1-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="325f1-229">System-Only</span></span>            | <span data-ttu-id="325f1-230">False</span><span class="sxs-lookup"><span data-stu-id="325f1-230">False</span></span>                                                         |
| <span data-ttu-id="325f1-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="325f1-231">Is-Single-Valued</span></span>       | <span data-ttu-id="325f1-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="325f1-232">True</span></span>                                                          |
| <span data-ttu-id="325f1-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="325f1-233">Is Indexed</span></span>             | <span data-ttu-id="325f1-234">False</span><span class="sxs-lookup"><span data-stu-id="325f1-234">False</span></span>                                                         |
| <span data-ttu-id="325f1-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="325f1-235">In Global Catalog</span></span>      | <span data-ttu-id="325f1-236">False</span><span class="sxs-lookup"><span data-stu-id="325f1-236">False</span></span>                                                         |
| <span data-ttu-id="325f1-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="325f1-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="325f1-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="325f1-238">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="325f1-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="325f1-239">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="325f1-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="325f1-240">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="325f1-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="325f1-241">Search-Flags</span></span>           | <span data-ttu-id="325f1-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="325f1-242">0x00000000</span></span>                                                    |
| <span data-ttu-id="325f1-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="325f1-243">System-Flags</span></span>           | <span data-ttu-id="325f1-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="325f1-244">0x00000010</span></span>                                                    |
| <span data-ttu-id="325f1-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="325f1-245">Classes used in</span></span>        | [<span data-ttu-id="325f1-246">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="325f1-246">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="325f1-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="325f1-247">Windows Server 2012</span></span>



| <span data-ttu-id="325f1-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="325f1-248">Entry</span></span> | <span data-ttu-id="325f1-249">Wert</span><span class="sxs-lookup"><span data-stu-id="325f1-249">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="325f1-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="325f1-250">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="325f1-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="325f1-251">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="325f1-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="325f1-252">System-Only</span></span>            | <span data-ttu-id="325f1-253">False</span><span class="sxs-lookup"><span data-stu-id="325f1-253">False</span></span>                                                         |
| <span data-ttu-id="325f1-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="325f1-254">Is-Single-Valued</span></span>       | <span data-ttu-id="325f1-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="325f1-255">True</span></span>                                                          |
| <span data-ttu-id="325f1-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="325f1-256">Is Indexed</span></span>             | <span data-ttu-id="325f1-257">False</span><span class="sxs-lookup"><span data-stu-id="325f1-257">False</span></span>                                                         |
| <span data-ttu-id="325f1-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="325f1-258">In Global Catalog</span></span>      | <span data-ttu-id="325f1-259">False</span><span class="sxs-lookup"><span data-stu-id="325f1-259">False</span></span>                                                         |
| <span data-ttu-id="325f1-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="325f1-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="325f1-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="325f1-261">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="325f1-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="325f1-262">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="325f1-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="325f1-263">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="325f1-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="325f1-264">Search-Flags</span></span>           | <span data-ttu-id="325f1-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="325f1-265">0x00000000</span></span>                                                    |
| <span data-ttu-id="325f1-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="325f1-266">System-Flags</span></span>           | <span data-ttu-id="325f1-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="325f1-267">0x00000010</span></span>                                                    |
| <span data-ttu-id="325f1-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="325f1-268">Classes used in</span></span>        | [<span data-ttu-id="325f1-269">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="325f1-269">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



 

 





