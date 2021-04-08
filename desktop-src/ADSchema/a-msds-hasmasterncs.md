---
title: ms-DS-has-Master-NCS-Attribut
description: Enthält die von einem Domänen Controller gehaltenen Namenskontexte. Mit diesem Attribut wird "-Master-NCS" als veraltet markiert.
ms.assetid: 5325db42-afd7-472c-8797-447e752a3907
ms.tgt_platform: multiple
keywords:
- AD-Schema für ms-DS-has-Master-NCS-Attribut
- AD-Schema des msDS-hasmasterncs-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Has-Master-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24507460eaa7653cfc2c98d3772942de9936162c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859853"
---
# <a name="ms-ds-has-master-ncs-attribute"></a><span data-ttu-id="f7f4d-106">ms-DS-has-Master-NCS-Attribut</span><span class="sxs-lookup"><span data-stu-id="f7f4d-106">ms-DS-Has-Master-NCs attribute</span></span>

<span data-ttu-id="f7f4d-107">Enthält die von einem Domänen Controller gehaltenen Namenskontexte.</span><span class="sxs-lookup"><span data-stu-id="f7f4d-107">Contains the naming contexts held by a domain controller.</span></span> <span data-ttu-id="f7f4d-108">Mit diesem Attribut wird "-Master-NCS" als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="f7f4d-108">This attribute deprecates has-Master-NCs.</span></span>



| <span data-ttu-id="f7f4d-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f7f4d-109">Entry</span></span> | <span data-ttu-id="f7f4d-110">Wert</span><span class="sxs-lookup"><span data-stu-id="f7f4d-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="f7f4d-111">CN</span><span class="sxs-lookup"><span data-stu-id="f7f4d-111">CN</span></span>                | <span data-ttu-id="f7f4d-112">ms-DS-has-Master-NCS</span><span class="sxs-lookup"><span data-stu-id="f7f4d-112">ms-DS-Has-Master-NCs</span></span>                    |
| <span data-ttu-id="f7f4d-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f7f4d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f7f4d-114">MSDS-hasmasterncs</span><span class="sxs-lookup"><span data-stu-id="f7f4d-114">msDS-hasMasterNCs</span></span>                       |
| <span data-ttu-id="f7f4d-115">Size</span><span class="sxs-lookup"><span data-stu-id="f7f4d-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="f7f4d-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="f7f4d-116">Update Privilege</span></span>  | <span data-ttu-id="f7f4d-117">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f7f4d-117">This value is set by the system</span></span>         |
| <span data-ttu-id="f7f4d-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="f7f4d-118">Update Frequency</span></span>  | <span data-ttu-id="f7f4d-119">Jedes Mal, wenn ein neuer NC erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f7f4d-119">Each time a new NC is created.</span></span>          |
| <span data-ttu-id="f7f4d-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f7f4d-120">Attribute-Id</span></span>      | <span data-ttu-id="f7f4d-121">1.2.840.113556.1.4.1836</span><span class="sxs-lookup"><span data-stu-id="f7f4d-121">1.2.840.113556.1.4.1836</span></span>                 |
| <span data-ttu-id="f7f4d-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f7f4d-122">System-Id-Guid</span></span>    | <span data-ttu-id="f7f4d-123">ae2de0e2-59d7-4d47-8d47-ed4dfe4357ad</span><span class="sxs-lookup"><span data-stu-id="f7f4d-123">ae2de0e2-59d7-4d47-8d47-ed4dfe4357ad</span></span>    |
| <span data-ttu-id="f7f4d-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7f4d-124">Syntax</span></span>            | [<span data-ttu-id="f7f4d-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="f7f4d-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="f7f4d-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="f7f4d-126">Implementations</span></span>

-   [<span data-ttu-id="f7f4d-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f7f4d-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f7f4d-128">**Adam**</span><span class="sxs-lookup"><span data-stu-id="f7f4d-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f7f4d-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f7f4d-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f7f4d-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f7f4d-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f7f4d-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f7f4d-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f7f4d-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f7f4d-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f7f4d-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f7f4d-133">Windows Server 2003</span></span>



| <span data-ttu-id="f7f4d-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f7f4d-134">Entry</span></span> | <span data-ttu-id="f7f4d-135">Wert</span><span class="sxs-lookup"><span data-stu-id="f7f4d-135">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f7f4d-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f7f4d-136">Link-Id</span></span>                | <span data-ttu-id="f7f4d-137">2036</span><span class="sxs-lookup"><span data-stu-id="f7f4d-137">2036</span></span>                                     |
| <span data-ttu-id="f7f4d-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7f4d-138">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f7f4d-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7f4d-139">System-Only</span></span>            | <span data-ttu-id="f7f4d-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="f7f4d-140">True</span></span>                                     |
| <span data-ttu-id="f7f4d-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f7f4d-141">Is-Single-Valued</span></span>       | <span data-ttu-id="f7f4d-142">False</span><span class="sxs-lookup"><span data-stu-id="f7f4d-142">False</span></span>                                    |
| <span data-ttu-id="f7f4d-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f7f4d-143">Is Indexed</span></span>             | <span data-ttu-id="f7f4d-144">False</span><span class="sxs-lookup"><span data-stu-id="f7f4d-144">False</span></span>                                    |
| <span data-ttu-id="f7f4d-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f7f4d-145">In Global Catalog</span></span>      | <span data-ttu-id="f7f4d-146">False</span><span class="sxs-lookup"><span data-stu-id="f7f4d-146">False</span></span>                                    |
| <span data-ttu-id="f7f4d-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f7f4d-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7f4d-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f7f4d-148">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f7f4d-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7f4d-149">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f7f4d-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7f4d-150">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f7f4d-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f4d-151">Search-Flags</span></span>           | <span data-ttu-id="f7f4d-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f4d-152">0x00000000</span></span>                               |
| <span data-ttu-id="f7f4d-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f4d-153">System-Flags</span></span>           | <span data-ttu-id="f7f4d-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7f4d-154">0x00000010</span></span>                               |
| <span data-ttu-id="f7f4d-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f7f4d-155">Classes used in</span></span>        | [<span data-ttu-id="f7f4d-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f7f4d-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f7f4d-157">Adam</span><span class="sxs-lookup"><span data-stu-id="f7f4d-157">ADAM</span></span>



| <span data-ttu-id="f7f4d-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f7f4d-158">Entry</span></span> | <span data-ttu-id="f7f4d-159">Wert</span><span class="sxs-lookup"><span data-stu-id="f7f4d-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f7f4d-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f7f4d-160">Link-Id</span></span>                | <span data-ttu-id="f7f4d-161">2036</span><span class="sxs-lookup"><span data-stu-id="f7f4d-161">2036</span></span>                                     |
| <span data-ttu-id="f7f4d-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7f4d-162">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f7f4d-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7f4d-163">System-Only</span></span>            | <span data-ttu-id="f7f4d-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="f7f4d-164">True</span></span>                                     |
| <span data-ttu-id="f7f4d-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f7f4d-165">Is-Single-Valued</span></span>       | <span data-ttu-id="f7f4d-166">False</span><span class="sxs-lookup"><span data-stu-id="f7f4d-166">False</span></span>                                    |
| <span data-ttu-id="f7f4d-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f7f4d-167">Is Indexed</span></span>             | <span data-ttu-id="f7f4d-168">False</span><span class="sxs-lookup"><span data-stu-id="f7f4d-168">False</span></span>                                    |
| <span data-ttu-id="f7f4d-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f7f4d-169">In Global Catalog</span></span>      | <span data-ttu-id="f7f4d-170">False</span><span class="sxs-lookup"><span data-stu-id="f7f4d-170">False</span></span>                                    |
| <span data-ttu-id="f7f4d-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f7f4d-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7f4d-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f7f4d-172">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f7f4d-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7f4d-173">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f7f4d-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7f4d-174">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f7f4d-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f4d-175">Search-Flags</span></span>           | <span data-ttu-id="f7f4d-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f4d-176">0x00000000</span></span>                               |
| <span data-ttu-id="f7f4d-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f4d-177">System-Flags</span></span>           | <span data-ttu-id="f7f4d-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7f4d-178">0x00000010</span></span>                               |
| <span data-ttu-id="f7f4d-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f7f4d-179">Classes used in</span></span>        | [<span data-ttu-id="f7f4d-180">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f7f4d-180">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f7f4d-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f7f4d-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f7f4d-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f7f4d-182">Entry</span></span> | <span data-ttu-id="f7f4d-183">Wert</span><span class="sxs-lookup"><span data-stu-id="f7f4d-183">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f7f4d-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f7f4d-184">Link-Id</span></span>                | <span data-ttu-id="f7f4d-185">2036</span><span class="sxs-lookup"><span data-stu-id="f7f4d-185">2036</span></span>                                     |
| <span data-ttu-id="f7f4d-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7f4d-186">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f7f4d-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7f4d-187">System-Only</span></span>            | <span data-ttu-id="f7f4d-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="f7f4d-188">True</span></span>                                     |
| <span data-ttu-id="f7f4d-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f7f4d-189">Is-Single-Valued</span></span>       | <span data-ttu-id="f7f4d-190">False</span><span class="sxs-lookup"><span data-stu-id="f7f4d-190">False</span></span>                                    |
| <span data-ttu-id="f7f4d-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f7f4d-191">Is Indexed</span></span>             | <span data-ttu-id="f7f4d-192">False</span><span class="sxs-lookup"><span data-stu-id="f7f4d-192">False</span></span>                                    |
| <span data-ttu-id="f7f4d-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f7f4d-193">In Global Catalog</span></span>      | <span data-ttu-id="f7f4d-194">False</span><span class="sxs-lookup"><span data-stu-id="f7f4d-194">False</span></span>                                    |
| <span data-ttu-id="f7f4d-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f7f4d-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7f4d-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f7f4d-196">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f7f4d-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7f4d-197">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f7f4d-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7f4d-198">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f7f4d-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f4d-199">Search-Flags</span></span>           | <span data-ttu-id="f7f4d-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f4d-200">0x00000000</span></span>                               |
| <span data-ttu-id="f7f4d-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f4d-201">System-Flags</span></span>           | <span data-ttu-id="f7f4d-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7f4d-202">0x00000010</span></span>                               |
| <span data-ttu-id="f7f4d-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f7f4d-203">Classes used in</span></span>        | [<span data-ttu-id="f7f4d-204">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f7f4d-204">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f7f4d-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7f4d-205">Windows Server 2008</span></span>



| <span data-ttu-id="f7f4d-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f7f4d-206">Entry</span></span> | <span data-ttu-id="f7f4d-207">Wert</span><span class="sxs-lookup"><span data-stu-id="f7f4d-207">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f7f4d-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f7f4d-208">Link-Id</span></span>                | <span data-ttu-id="f7f4d-209">2036</span><span class="sxs-lookup"><span data-stu-id="f7f4d-209">2036</span></span>                                     |
| <span data-ttu-id="f7f4d-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7f4d-210">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f7f4d-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7f4d-211">System-Only</span></span>            | <span data-ttu-id="f7f4d-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="f7f4d-212">True</span></span>                                     |
| <span data-ttu-id="f7f4d-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f7f4d-213">Is-Single-Valued</span></span>       | <span data-ttu-id="f7f4d-214">False</span><span class="sxs-lookup"><span data-stu-id="f7f4d-214">False</span></span>                                    |
| <span data-ttu-id="f7f4d-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f7f4d-215">Is Indexed</span></span>             | <span data-ttu-id="f7f4d-216">False</span><span class="sxs-lookup"><span data-stu-id="f7f4d-216">False</span></span>                                    |
| <span data-ttu-id="f7f4d-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f7f4d-217">In Global Catalog</span></span>      | <span data-ttu-id="f7f4d-218">False</span><span class="sxs-lookup"><span data-stu-id="f7f4d-218">False</span></span>                                    |
| <span data-ttu-id="f7f4d-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f7f4d-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7f4d-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f7f4d-220">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f7f4d-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7f4d-221">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f7f4d-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7f4d-222">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f7f4d-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f4d-223">Search-Flags</span></span>           | <span data-ttu-id="f7f4d-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f4d-224">0x00000000</span></span>                               |
| <span data-ttu-id="f7f4d-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f4d-225">System-Flags</span></span>           | <span data-ttu-id="f7f4d-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7f4d-226">0x00000010</span></span>                               |
| <span data-ttu-id="f7f4d-227">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f7f4d-227">Classes used in</span></span>        | [<span data-ttu-id="f7f4d-228">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f7f4d-228">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f7f4d-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f7f4d-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f7f4d-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f7f4d-230">Entry</span></span> | <span data-ttu-id="f7f4d-231">Wert</span><span class="sxs-lookup"><span data-stu-id="f7f4d-231">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f7f4d-232">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f7f4d-232">Link-Id</span></span>                | <span data-ttu-id="f7f4d-233">2036</span><span class="sxs-lookup"><span data-stu-id="f7f4d-233">2036</span></span>                                     |
| <span data-ttu-id="f7f4d-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7f4d-234">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f7f4d-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7f4d-235">System-Only</span></span>            | <span data-ttu-id="f7f4d-236">Richtig</span><span class="sxs-lookup"><span data-stu-id="f7f4d-236">True</span></span>                                     |
| <span data-ttu-id="f7f4d-237">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f7f4d-237">Is-Single-Valued</span></span>       | <span data-ttu-id="f7f4d-238">False</span><span class="sxs-lookup"><span data-stu-id="f7f4d-238">False</span></span>                                    |
| <span data-ttu-id="f7f4d-239">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f7f4d-239">Is Indexed</span></span>             | <span data-ttu-id="f7f4d-240">False</span><span class="sxs-lookup"><span data-stu-id="f7f4d-240">False</span></span>                                    |
| <span data-ttu-id="f7f4d-241">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f7f4d-241">In Global Catalog</span></span>      | <span data-ttu-id="f7f4d-242">False</span><span class="sxs-lookup"><span data-stu-id="f7f4d-242">False</span></span>                                    |
| <span data-ttu-id="f7f4d-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f7f4d-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7f4d-244">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f7f4d-244">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f7f4d-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7f4d-245">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f7f4d-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7f4d-246">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f7f4d-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f4d-247">Search-Flags</span></span>           | <span data-ttu-id="f7f4d-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f4d-248">0x00000000</span></span>                               |
| <span data-ttu-id="f7f4d-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f4d-249">System-Flags</span></span>           | <span data-ttu-id="f7f4d-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7f4d-250">0x00000010</span></span>                               |
| <span data-ttu-id="f7f4d-251">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f7f4d-251">Classes used in</span></span>        | [<span data-ttu-id="f7f4d-252">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f7f4d-252">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f7f4d-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f7f4d-253">Windows Server 2012</span></span>



| <span data-ttu-id="f7f4d-254">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f7f4d-254">Entry</span></span> | <span data-ttu-id="f7f4d-255">Wert</span><span class="sxs-lookup"><span data-stu-id="f7f4d-255">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f7f4d-256">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f7f4d-256">Link-Id</span></span>                | <span data-ttu-id="f7f4d-257">2036</span><span class="sxs-lookup"><span data-stu-id="f7f4d-257">2036</span></span>                                     |
| <span data-ttu-id="f7f4d-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7f4d-258">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f7f4d-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7f4d-259">System-Only</span></span>            | <span data-ttu-id="f7f4d-260">Richtig</span><span class="sxs-lookup"><span data-stu-id="f7f4d-260">True</span></span>                                     |
| <span data-ttu-id="f7f4d-261">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f7f4d-261">Is-Single-Valued</span></span>       | <span data-ttu-id="f7f4d-262">False</span><span class="sxs-lookup"><span data-stu-id="f7f4d-262">False</span></span>                                    |
| <span data-ttu-id="f7f4d-263">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f7f4d-263">Is Indexed</span></span>             | <span data-ttu-id="f7f4d-264">False</span><span class="sxs-lookup"><span data-stu-id="f7f4d-264">False</span></span>                                    |
| <span data-ttu-id="f7f4d-265">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f7f4d-265">In Global Catalog</span></span>      | <span data-ttu-id="f7f4d-266">False</span><span class="sxs-lookup"><span data-stu-id="f7f4d-266">False</span></span>                                    |
| <span data-ttu-id="f7f4d-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f7f4d-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7f4d-268">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f7f4d-268">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f7f4d-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7f4d-269">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f7f4d-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7f4d-270">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f7f4d-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f4d-271">Search-Flags</span></span>           | <span data-ttu-id="f7f4d-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f4d-272">0x00000000</span></span>                               |
| <span data-ttu-id="f7f4d-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f4d-273">System-Flags</span></span>           | <span data-ttu-id="f7f4d-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7f4d-274">0x00000010</span></span>                               |
| <span data-ttu-id="f7f4d-275">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f7f4d-275">Classes used in</span></span>        | [<span data-ttu-id="f7f4d-276">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f7f4d-276">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





