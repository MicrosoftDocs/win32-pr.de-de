---
title: Primary-Group-Token-Attribut
description: Ein berechnetes Attribut, das zum Abrufen der Mitgliedschafts Liste einer Gruppe verwendet wird, z. b. Domänen Benutzer. Die komplette Mitgliedschaft dieser Gruppen wird aus Gründen der Skalierung nicht explizit gespeichert.
ms.assetid: b23d3b7f-074b-4f1b-bc06-b22738a8a79e
ms.tgt_platform: multiple
keywords:
- AD-Schema des Primary-Group-Token-Attributs
- primarygrouptoken-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Primary-Group-Token
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b237ab5998ca3f38f2d07128b36d9337c96935d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107607"
---
# <a name="primary-group-token-attribute"></a><span data-ttu-id="32081-106">Primary-Group-Token-Attribut</span><span class="sxs-lookup"><span data-stu-id="32081-106">Primary-Group-Token attribute</span></span>

<span data-ttu-id="32081-107">Ein berechnetes Attribut, das zum Abrufen der Mitgliedschafts Liste einer Gruppe verwendet wird, z. b. Domänen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="32081-107">A computed attribute that is used in retrieving the membership list of a group, such as Domain Users.</span></span> <span data-ttu-id="32081-108">Die komplette Mitgliedschaft dieser Gruppen wird aus Gründen der Skalierung nicht explizit gespeichert.</span><span class="sxs-lookup"><span data-stu-id="32081-108">The complete membership of such groups is not stored explicitly for scaling reasons.</span></span>



| <span data-ttu-id="32081-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="32081-109">Entry</span></span> | <span data-ttu-id="32081-110">Wert</span><span class="sxs-lookup"><span data-stu-id="32081-110">Value</span></span> |
|-------------------|--------------------------------------------|
| <span data-ttu-id="32081-111">CN</span><span class="sxs-lookup"><span data-stu-id="32081-111">CN</span></span>                | <span data-ttu-id="32081-112">Primary-Group-Token</span><span class="sxs-lookup"><span data-stu-id="32081-112">Primary-Group-Token</span></span>                        |
| <span data-ttu-id="32081-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="32081-113">Ldap-Display-Name</span></span> | <span data-ttu-id="32081-114">primarygrouptoken</span><span class="sxs-lookup"><span data-stu-id="32081-114">primaryGroupToken</span></span>                          |
| <span data-ttu-id="32081-115">Size</span><span class="sxs-lookup"><span data-stu-id="32081-115">Size</span></span>              | <span data-ttu-id="32081-116">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="32081-116">4 bytes</span></span>                                    |
| <span data-ttu-id="32081-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="32081-117">Update Privilege</span></span>  | <span data-ttu-id="32081-118">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="32081-118">This value is set by the system.</span></span>           |
| <span data-ttu-id="32081-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="32081-119">Update Frequency</span></span>  | <span data-ttu-id="32081-120">Jedes Mal, wenn sich eine primäre Gruppe von Objekten ändert.</span><span class="sxs-lookup"><span data-stu-id="32081-120">Whenever an objects primary group changes.</span></span> |
| <span data-ttu-id="32081-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="32081-121">Attribute-Id</span></span>      | <span data-ttu-id="32081-122">1.2.840.113556.1.4.1412</span><span class="sxs-lookup"><span data-stu-id="32081-122">1.2.840.113556.1.4.1412</span></span>                    |
| <span data-ttu-id="32081-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="32081-123">System-Id-Guid</span></span>    | <span data-ttu-id="32081-124">c0ed8738-7efd-4481-84d9-66d2db8be369</span><span class="sxs-lookup"><span data-stu-id="32081-124">c0ed8738-7efd-4481-84d9-66d2db8be369</span></span>       |
| <span data-ttu-id="32081-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="32081-125">Syntax</span></span>            | [<span data-ttu-id="32081-126">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="32081-126">**Enumeration**</span></span>](s-enumeration.md)       |



## <a name="implementations"></a><span data-ttu-id="32081-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="32081-127">Implementations</span></span>

-   [<span data-ttu-id="32081-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="32081-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="32081-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="32081-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="32081-130">**Adam**</span><span class="sxs-lookup"><span data-stu-id="32081-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="32081-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="32081-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="32081-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="32081-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="32081-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="32081-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="32081-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="32081-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="32081-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="32081-135">Windows 2000 Server</span></span>



| <span data-ttu-id="32081-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="32081-136">Entry</span></span> | <span data-ttu-id="32081-137">Wert</span><span class="sxs-lookup"><span data-stu-id="32081-137">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="32081-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="32081-138">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="32081-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32081-139">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="32081-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="32081-140">System-Only</span></span>            | <span data-ttu-id="32081-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="32081-141">True</span></span>                                |
| <span data-ttu-id="32081-142">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="32081-142">Is-Single-Valued</span></span>       | <span data-ttu-id="32081-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="32081-143">True</span></span>                                |
| <span data-ttu-id="32081-144">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="32081-144">Is Indexed</span></span>             | <span data-ttu-id="32081-145">False</span><span class="sxs-lookup"><span data-stu-id="32081-145">False</span></span>                               |
| <span data-ttu-id="32081-146">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="32081-146">In Global Catalog</span></span>      | <span data-ttu-id="32081-147">False</span><span class="sxs-lookup"><span data-stu-id="32081-147">False</span></span>                               |
| <span data-ttu-id="32081-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="32081-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="32081-149">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="32081-149">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="32081-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32081-150">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="32081-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32081-151">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="32081-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32081-152">Search-Flags</span></span>           | <span data-ttu-id="32081-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32081-153">0x00000000</span></span>                          |
| <span data-ttu-id="32081-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32081-154">System-Flags</span></span>           | <span data-ttu-id="32081-155">0x00000014</span><span class="sxs-lookup"><span data-stu-id="32081-155">0x00000014</span></span>                          |
| <span data-ttu-id="32081-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="32081-156">Classes used in</span></span>        | [<span data-ttu-id="32081-157">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="32081-157">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="32081-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="32081-158">Windows Server 2003</span></span>



| <span data-ttu-id="32081-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="32081-159">Entry</span></span> | <span data-ttu-id="32081-160">Wert</span><span class="sxs-lookup"><span data-stu-id="32081-160">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="32081-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="32081-161">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="32081-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32081-162">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="32081-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="32081-163">System-Only</span></span>            | <span data-ttu-id="32081-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="32081-164">True</span></span>                                |
| <span data-ttu-id="32081-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="32081-165">Is-Single-Valued</span></span>       | <span data-ttu-id="32081-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="32081-166">True</span></span>                                |
| <span data-ttu-id="32081-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="32081-167">Is Indexed</span></span>             | <span data-ttu-id="32081-168">False</span><span class="sxs-lookup"><span data-stu-id="32081-168">False</span></span>                               |
| <span data-ttu-id="32081-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="32081-169">In Global Catalog</span></span>      | <span data-ttu-id="32081-170">False</span><span class="sxs-lookup"><span data-stu-id="32081-170">False</span></span>                               |
| <span data-ttu-id="32081-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="32081-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="32081-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="32081-172">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="32081-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32081-173">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="32081-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32081-174">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="32081-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32081-175">Search-Flags</span></span>           | <span data-ttu-id="32081-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32081-176">0x00000000</span></span>                          |
| <span data-ttu-id="32081-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32081-177">System-Flags</span></span>           | <span data-ttu-id="32081-178">0x00000014</span><span class="sxs-lookup"><span data-stu-id="32081-178">0x00000014</span></span>                          |
| <span data-ttu-id="32081-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="32081-179">Classes used in</span></span>        | [<span data-ttu-id="32081-180">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="32081-180">**Group**</span></span>](c-group.md)<br/> |



## <a name="adam"></a><span data-ttu-id="32081-181">Adam</span><span class="sxs-lookup"><span data-stu-id="32081-181">ADAM</span></span>



| <span data-ttu-id="32081-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="32081-182">Entry</span></span> | <span data-ttu-id="32081-183">Wert</span><span class="sxs-lookup"><span data-stu-id="32081-183">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="32081-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="32081-184">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="32081-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32081-185">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="32081-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="32081-186">System-Only</span></span>            | <span data-ttu-id="32081-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="32081-187">True</span></span>                                |
| <span data-ttu-id="32081-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="32081-188">Is-Single-Valued</span></span>       | <span data-ttu-id="32081-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="32081-189">True</span></span>                                |
| <span data-ttu-id="32081-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="32081-190">Is Indexed</span></span>             | <span data-ttu-id="32081-191">False</span><span class="sxs-lookup"><span data-stu-id="32081-191">False</span></span>                               |
| <span data-ttu-id="32081-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="32081-192">In Global Catalog</span></span>      | <span data-ttu-id="32081-193">False</span><span class="sxs-lookup"><span data-stu-id="32081-193">False</span></span>                               |
| <span data-ttu-id="32081-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="32081-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="32081-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="32081-195">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="32081-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32081-196">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="32081-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32081-197">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="32081-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32081-198">Search-Flags</span></span>           | <span data-ttu-id="32081-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32081-199">0x00000000</span></span>                          |
| <span data-ttu-id="32081-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32081-200">System-Flags</span></span>           | <span data-ttu-id="32081-201">0x00000014</span><span class="sxs-lookup"><span data-stu-id="32081-201">0x00000014</span></span>                          |
| <span data-ttu-id="32081-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="32081-202">Classes used in</span></span>        | [<span data-ttu-id="32081-203">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="32081-203">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="32081-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="32081-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="32081-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="32081-205">Entry</span></span> | <span data-ttu-id="32081-206">Wert</span><span class="sxs-lookup"><span data-stu-id="32081-206">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="32081-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="32081-207">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="32081-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32081-208">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="32081-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="32081-209">System-Only</span></span>            | <span data-ttu-id="32081-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="32081-210">True</span></span>                                |
| <span data-ttu-id="32081-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="32081-211">Is-Single-Valued</span></span>       | <span data-ttu-id="32081-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="32081-212">True</span></span>                                |
| <span data-ttu-id="32081-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="32081-213">Is Indexed</span></span>             | <span data-ttu-id="32081-214">False</span><span class="sxs-lookup"><span data-stu-id="32081-214">False</span></span>                               |
| <span data-ttu-id="32081-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="32081-215">In Global Catalog</span></span>      | <span data-ttu-id="32081-216">False</span><span class="sxs-lookup"><span data-stu-id="32081-216">False</span></span>                               |
| <span data-ttu-id="32081-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="32081-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="32081-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="32081-218">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="32081-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32081-219">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="32081-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32081-220">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="32081-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32081-221">Search-Flags</span></span>           | <span data-ttu-id="32081-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32081-222">0x00000000</span></span>                          |
| <span data-ttu-id="32081-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32081-223">System-Flags</span></span>           | <span data-ttu-id="32081-224">0x00000014</span><span class="sxs-lookup"><span data-stu-id="32081-224">0x00000014</span></span>                          |
| <span data-ttu-id="32081-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="32081-225">Classes used in</span></span>        | [<span data-ttu-id="32081-226">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="32081-226">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="32081-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32081-227">Windows Server 2008</span></span>



| <span data-ttu-id="32081-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="32081-228">Entry</span></span> | <span data-ttu-id="32081-229">Wert</span><span class="sxs-lookup"><span data-stu-id="32081-229">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="32081-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="32081-230">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="32081-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32081-231">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="32081-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="32081-232">System-Only</span></span>            | <span data-ttu-id="32081-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="32081-233">True</span></span>                                |
| <span data-ttu-id="32081-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="32081-234">Is-Single-Valued</span></span>       | <span data-ttu-id="32081-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="32081-235">True</span></span>                                |
| <span data-ttu-id="32081-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="32081-236">Is Indexed</span></span>             | <span data-ttu-id="32081-237">False</span><span class="sxs-lookup"><span data-stu-id="32081-237">False</span></span>                               |
| <span data-ttu-id="32081-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="32081-238">In Global Catalog</span></span>      | <span data-ttu-id="32081-239">False</span><span class="sxs-lookup"><span data-stu-id="32081-239">False</span></span>                               |
| <span data-ttu-id="32081-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="32081-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="32081-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="32081-241">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="32081-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32081-242">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="32081-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32081-243">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="32081-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32081-244">Search-Flags</span></span>           | <span data-ttu-id="32081-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32081-245">0x00000000</span></span>                          |
| <span data-ttu-id="32081-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32081-246">System-Flags</span></span>           | <span data-ttu-id="32081-247">0x00000014</span><span class="sxs-lookup"><span data-stu-id="32081-247">0x00000014</span></span>                          |
| <span data-ttu-id="32081-248">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="32081-248">Classes used in</span></span>        | [<span data-ttu-id="32081-249">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="32081-249">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="32081-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="32081-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="32081-251">Eingabe</span><span class="sxs-lookup"><span data-stu-id="32081-251">Entry</span></span> | <span data-ttu-id="32081-252">Wert</span><span class="sxs-lookup"><span data-stu-id="32081-252">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="32081-253">Link-ID</span><span class="sxs-lookup"><span data-stu-id="32081-253">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="32081-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32081-254">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="32081-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="32081-255">System-Only</span></span>            | <span data-ttu-id="32081-256">Richtig</span><span class="sxs-lookup"><span data-stu-id="32081-256">True</span></span>                                |
| <span data-ttu-id="32081-257">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="32081-257">Is-Single-Valued</span></span>       | <span data-ttu-id="32081-258">Richtig</span><span class="sxs-lookup"><span data-stu-id="32081-258">True</span></span>                                |
| <span data-ttu-id="32081-259">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="32081-259">Is Indexed</span></span>             | <span data-ttu-id="32081-260">False</span><span class="sxs-lookup"><span data-stu-id="32081-260">False</span></span>                               |
| <span data-ttu-id="32081-261">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="32081-261">In Global Catalog</span></span>      | <span data-ttu-id="32081-262">False</span><span class="sxs-lookup"><span data-stu-id="32081-262">False</span></span>                               |
| <span data-ttu-id="32081-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="32081-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="32081-264">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="32081-264">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="32081-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32081-265">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="32081-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32081-266">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="32081-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32081-267">Search-Flags</span></span>           | <span data-ttu-id="32081-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32081-268">0x00000000</span></span>                          |
| <span data-ttu-id="32081-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32081-269">System-Flags</span></span>           | <span data-ttu-id="32081-270">0x00000014</span><span class="sxs-lookup"><span data-stu-id="32081-270">0x00000014</span></span>                          |
| <span data-ttu-id="32081-271">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="32081-271">Classes used in</span></span>        | [<span data-ttu-id="32081-272">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="32081-272">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="32081-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="32081-273">Windows Server 2012</span></span>



| <span data-ttu-id="32081-274">Eingabe</span><span class="sxs-lookup"><span data-stu-id="32081-274">Entry</span></span> | <span data-ttu-id="32081-275">Wert</span><span class="sxs-lookup"><span data-stu-id="32081-275">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="32081-276">Link-ID</span><span class="sxs-lookup"><span data-stu-id="32081-276">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="32081-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32081-277">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="32081-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="32081-278">System-Only</span></span>            | <span data-ttu-id="32081-279">Richtig</span><span class="sxs-lookup"><span data-stu-id="32081-279">True</span></span>                                |
| <span data-ttu-id="32081-280">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="32081-280">Is-Single-Valued</span></span>       | <span data-ttu-id="32081-281">Richtig</span><span class="sxs-lookup"><span data-stu-id="32081-281">True</span></span>                                |
| <span data-ttu-id="32081-282">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="32081-282">Is Indexed</span></span>             | <span data-ttu-id="32081-283">False</span><span class="sxs-lookup"><span data-stu-id="32081-283">False</span></span>                               |
| <span data-ttu-id="32081-284">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="32081-284">In Global Catalog</span></span>      | <span data-ttu-id="32081-285">False</span><span class="sxs-lookup"><span data-stu-id="32081-285">False</span></span>                               |
| <span data-ttu-id="32081-286">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="32081-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="32081-287">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="32081-287">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="32081-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32081-288">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="32081-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32081-289">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="32081-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32081-290">Search-Flags</span></span>           | <span data-ttu-id="32081-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32081-291">0x00000000</span></span>                          |
| <span data-ttu-id="32081-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32081-292">System-Flags</span></span>           | <span data-ttu-id="32081-293">0x00000014</span><span class="sxs-lookup"><span data-stu-id="32081-293">0x00000014</span></span>                          |
| <span data-ttu-id="32081-294">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="32081-294">Classes used in</span></span>        | [<span data-ttu-id="32081-295">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="32081-295">**Group**</span></span>](c-group.md)<br/> |



 

 





