---
title: ms-DS-has-Domain-NCS-Attribut
description: Verzeichnisdienst-Replikations Informationen, die Details zu den Domänen Namen Kontexten auf einem bestimmten Server enthalten.
ms.assetid: e5a7c371-5a37-466e-b56f-ee261b48e3b2
ms.tgt_platform: multiple
keywords:
- ms-DS-has-Domain-NCS-Attribut AD-Schema
- AD-Schema des msDS-hasdomainncs-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Has-Domain-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83b946286974cc6ba4e6d30484e7768a1daeccb6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480098"
---
# <a name="ms-ds-has-domain-ncs-attribute"></a><span data-ttu-id="2ed8e-105">ms-DS-has-Domain-NCS-Attribut</span><span class="sxs-lookup"><span data-stu-id="2ed8e-105">ms-DS-Has-Domain-NCs attribute</span></span>

<span data-ttu-id="2ed8e-106">Verzeichnisdienst-Replikations Informationen, die Details zu den Domänen Namen Kontexten auf einem bestimmten Server enthalten.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-106">Directory service replication information that details the domain naming contexts present on a particular server.</span></span>



| <span data-ttu-id="2ed8e-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2ed8e-107">Entry</span></span> | <span data-ttu-id="2ed8e-108">Wert</span><span class="sxs-lookup"><span data-stu-id="2ed8e-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="2ed8e-109">CN</span><span class="sxs-lookup"><span data-stu-id="2ed8e-109">CN</span></span>                | <span data-ttu-id="2ed8e-110">ms-DS-has-Domain-NCS</span><span class="sxs-lookup"><span data-stu-id="2ed8e-110">ms-DS-Has-Domain-NCs</span></span>                                |
| <span data-ttu-id="2ed8e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2ed8e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2ed8e-112">MSDS-hasdomainncs</span><span class="sxs-lookup"><span data-stu-id="2ed8e-112">msDS-HasDomainNCs</span></span>                                   |
| <span data-ttu-id="2ed8e-113">Size</span><span class="sxs-lookup"><span data-stu-id="2ed8e-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="2ed8e-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2ed8e-114">Update Privilege</span></span>  | <span data-ttu-id="2ed8e-115">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-115">This value is set by the system</span></span>                     |
| <span data-ttu-id="2ed8e-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="2ed8e-116">Update Frequency</span></span>  | <span data-ttu-id="2ed8e-117">Sie wird von Dcpromo festgelegt und danach nie geändert.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-117">It is set by DCPromo and never modified thereafter.</span></span> |
| <span data-ttu-id="2ed8e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2ed8e-118">Attribute-Id</span></span>      | <span data-ttu-id="2ed8e-119">1.2.840.113556.1.4.1820</span><span class="sxs-lookup"><span data-stu-id="2ed8e-119">1.2.840.113556.1.4.1820</span></span>                             |
| <span data-ttu-id="2ed8e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2ed8e-120">System-Id-Guid</span></span>    | <span data-ttu-id="2ed8e-121">6f 17e347-a842-4498-b8b3-15e007da4fed</span><span class="sxs-lookup"><span data-stu-id="2ed8e-121">6f17e347-a842-4498-b8b3-15e007da4fed</span></span>                |
| <span data-ttu-id="2ed8e-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ed8e-122">Syntax</span></span>            | [<span data-ttu-id="2ed8e-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="2ed8e-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)             |



## <a name="implementations"></a><span data-ttu-id="2ed8e-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="2ed8e-124">Implementations</span></span>

-   [<span data-ttu-id="2ed8e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2ed8e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2ed8e-126">**Adam**</span><span class="sxs-lookup"><span data-stu-id="2ed8e-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2ed8e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2ed8e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2ed8e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2ed8e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2ed8e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2ed8e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2ed8e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2ed8e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="2ed8e-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2ed8e-131">Windows Server 2003</span></span>



| <span data-ttu-id="2ed8e-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2ed8e-132">Entry</span></span> | <span data-ttu-id="2ed8e-133">Wert</span><span class="sxs-lookup"><span data-stu-id="2ed8e-133">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2ed8e-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2ed8e-134">Link-Id</span></span>                | <span data-ttu-id="2ed8e-135">2026</span><span class="sxs-lookup"><span data-stu-id="2ed8e-135">2026</span></span>                                     |
| <span data-ttu-id="2ed8e-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ed8e-136">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="2ed8e-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ed8e-137">System-Only</span></span>            | <span data-ttu-id="2ed8e-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="2ed8e-138">True</span></span>                                     |
| <span data-ttu-id="2ed8e-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2ed8e-139">Is-Single-Valued</span></span>       | <span data-ttu-id="2ed8e-140">False</span><span class="sxs-lookup"><span data-stu-id="2ed8e-140">False</span></span>                                    |
| <span data-ttu-id="2ed8e-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2ed8e-141">Is Indexed</span></span>             | <span data-ttu-id="2ed8e-142">False</span><span class="sxs-lookup"><span data-stu-id="2ed8e-142">False</span></span>                                    |
| <span data-ttu-id="2ed8e-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2ed8e-143">In Global Catalog</span></span>      | <span data-ttu-id="2ed8e-144">False</span><span class="sxs-lookup"><span data-stu-id="2ed8e-144">False</span></span>                                    |
| <span data-ttu-id="2ed8e-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2ed8e-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ed8e-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2ed8e-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2ed8e-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ed8e-147">Range-Lower</span></span>            | <span data-ttu-id="2ed8e-148">4</span><span class="sxs-lookup"><span data-stu-id="2ed8e-148">4</span></span>                                        |
| <span data-ttu-id="2ed8e-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ed8e-149">Range-Upper</span></span>            | <span data-ttu-id="2ed8e-150">4</span><span class="sxs-lookup"><span data-stu-id="2ed8e-150">4</span></span>                                        |
| <span data-ttu-id="2ed8e-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ed8e-151">Search-Flags</span></span>           | <span data-ttu-id="2ed8e-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ed8e-152">0x00000000</span></span>                               |
| <span data-ttu-id="2ed8e-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ed8e-153">System-Flags</span></span>           | <span data-ttu-id="2ed8e-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ed8e-154">0x00000010</span></span>                               |
| <span data-ttu-id="2ed8e-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2ed8e-155">Classes used in</span></span>        | [<span data-ttu-id="2ed8e-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2ed8e-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2ed8e-157">Adam</span><span class="sxs-lookup"><span data-stu-id="2ed8e-157">ADAM</span></span>



| <span data-ttu-id="2ed8e-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2ed8e-158">Entry</span></span> | <span data-ttu-id="2ed8e-159">Wert</span><span class="sxs-lookup"><span data-stu-id="2ed8e-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2ed8e-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2ed8e-160">Link-Id</span></span>                | <span data-ttu-id="2ed8e-161">2026</span><span class="sxs-lookup"><span data-stu-id="2ed8e-161">2026</span></span>                                     |
| <span data-ttu-id="2ed8e-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ed8e-162">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="2ed8e-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ed8e-163">System-Only</span></span>            | <span data-ttu-id="2ed8e-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="2ed8e-164">True</span></span>                                     |
| <span data-ttu-id="2ed8e-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2ed8e-165">Is-Single-Valued</span></span>       | <span data-ttu-id="2ed8e-166">False</span><span class="sxs-lookup"><span data-stu-id="2ed8e-166">False</span></span>                                    |
| <span data-ttu-id="2ed8e-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2ed8e-167">Is Indexed</span></span>             | <span data-ttu-id="2ed8e-168">False</span><span class="sxs-lookup"><span data-stu-id="2ed8e-168">False</span></span>                                    |
| <span data-ttu-id="2ed8e-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2ed8e-169">In Global Catalog</span></span>      | <span data-ttu-id="2ed8e-170">False</span><span class="sxs-lookup"><span data-stu-id="2ed8e-170">False</span></span>                                    |
| <span data-ttu-id="2ed8e-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2ed8e-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ed8e-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2ed8e-172">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2ed8e-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ed8e-173">Range-Lower</span></span>            | <span data-ttu-id="2ed8e-174">4</span><span class="sxs-lookup"><span data-stu-id="2ed8e-174">4</span></span>                                        |
| <span data-ttu-id="2ed8e-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ed8e-175">Range-Upper</span></span>            | <span data-ttu-id="2ed8e-176">4</span><span class="sxs-lookup"><span data-stu-id="2ed8e-176">4</span></span>                                        |
| <span data-ttu-id="2ed8e-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ed8e-177">Search-Flags</span></span>           | <span data-ttu-id="2ed8e-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ed8e-178">0x00000000</span></span>                               |
| <span data-ttu-id="2ed8e-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ed8e-179">System-Flags</span></span>           | <span data-ttu-id="2ed8e-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ed8e-180">0x00000010</span></span>                               |
| <span data-ttu-id="2ed8e-181">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2ed8e-181">Classes used in</span></span>        | [<span data-ttu-id="2ed8e-182">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2ed8e-182">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2ed8e-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2ed8e-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2ed8e-184">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2ed8e-184">Entry</span></span> | <span data-ttu-id="2ed8e-185">Wert</span><span class="sxs-lookup"><span data-stu-id="2ed8e-185">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2ed8e-186">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2ed8e-186">Link-Id</span></span>                | <span data-ttu-id="2ed8e-187">2026</span><span class="sxs-lookup"><span data-stu-id="2ed8e-187">2026</span></span>                                     |
| <span data-ttu-id="2ed8e-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ed8e-188">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="2ed8e-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ed8e-189">System-Only</span></span>            | <span data-ttu-id="2ed8e-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="2ed8e-190">True</span></span>                                     |
| <span data-ttu-id="2ed8e-191">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2ed8e-191">Is-Single-Valued</span></span>       | <span data-ttu-id="2ed8e-192">False</span><span class="sxs-lookup"><span data-stu-id="2ed8e-192">False</span></span>                                    |
| <span data-ttu-id="2ed8e-193">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2ed8e-193">Is Indexed</span></span>             | <span data-ttu-id="2ed8e-194">False</span><span class="sxs-lookup"><span data-stu-id="2ed8e-194">False</span></span>                                    |
| <span data-ttu-id="2ed8e-195">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2ed8e-195">In Global Catalog</span></span>      | <span data-ttu-id="2ed8e-196">False</span><span class="sxs-lookup"><span data-stu-id="2ed8e-196">False</span></span>                                    |
| <span data-ttu-id="2ed8e-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2ed8e-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ed8e-198">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2ed8e-198">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2ed8e-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ed8e-199">Range-Lower</span></span>            | <span data-ttu-id="2ed8e-200">4</span><span class="sxs-lookup"><span data-stu-id="2ed8e-200">4</span></span>                                        |
| <span data-ttu-id="2ed8e-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ed8e-201">Range-Upper</span></span>            | <span data-ttu-id="2ed8e-202">4</span><span class="sxs-lookup"><span data-stu-id="2ed8e-202">4</span></span>                                        |
| <span data-ttu-id="2ed8e-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ed8e-203">Search-Flags</span></span>           | <span data-ttu-id="2ed8e-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ed8e-204">0x00000000</span></span>                               |
| <span data-ttu-id="2ed8e-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ed8e-205">System-Flags</span></span>           | <span data-ttu-id="2ed8e-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ed8e-206">0x00000010</span></span>                               |
| <span data-ttu-id="2ed8e-207">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2ed8e-207">Classes used in</span></span>        | [<span data-ttu-id="2ed8e-208">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2ed8e-208">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2ed8e-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ed8e-209">Windows Server 2008</span></span>



| <span data-ttu-id="2ed8e-210">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2ed8e-210">Entry</span></span> | <span data-ttu-id="2ed8e-211">Wert</span><span class="sxs-lookup"><span data-stu-id="2ed8e-211">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2ed8e-212">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2ed8e-212">Link-Id</span></span>                | <span data-ttu-id="2ed8e-213">2026</span><span class="sxs-lookup"><span data-stu-id="2ed8e-213">2026</span></span>                                     |
| <span data-ttu-id="2ed8e-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ed8e-214">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="2ed8e-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ed8e-215">System-Only</span></span>            | <span data-ttu-id="2ed8e-216">Richtig</span><span class="sxs-lookup"><span data-stu-id="2ed8e-216">True</span></span>                                     |
| <span data-ttu-id="2ed8e-217">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2ed8e-217">Is-Single-Valued</span></span>       | <span data-ttu-id="2ed8e-218">False</span><span class="sxs-lookup"><span data-stu-id="2ed8e-218">False</span></span>                                    |
| <span data-ttu-id="2ed8e-219">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2ed8e-219">Is Indexed</span></span>             | <span data-ttu-id="2ed8e-220">False</span><span class="sxs-lookup"><span data-stu-id="2ed8e-220">False</span></span>                                    |
| <span data-ttu-id="2ed8e-221">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2ed8e-221">In Global Catalog</span></span>      | <span data-ttu-id="2ed8e-222">False</span><span class="sxs-lookup"><span data-stu-id="2ed8e-222">False</span></span>                                    |
| <span data-ttu-id="2ed8e-223">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2ed8e-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ed8e-224">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2ed8e-224">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2ed8e-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ed8e-225">Range-Lower</span></span>            | <span data-ttu-id="2ed8e-226">4</span><span class="sxs-lookup"><span data-stu-id="2ed8e-226">4</span></span>                                        |
| <span data-ttu-id="2ed8e-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ed8e-227">Range-Upper</span></span>            | <span data-ttu-id="2ed8e-228">4</span><span class="sxs-lookup"><span data-stu-id="2ed8e-228">4</span></span>                                        |
| <span data-ttu-id="2ed8e-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ed8e-229">Search-Flags</span></span>           | <span data-ttu-id="2ed8e-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ed8e-230">0x00000000</span></span>                               |
| <span data-ttu-id="2ed8e-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ed8e-231">System-Flags</span></span>           | <span data-ttu-id="2ed8e-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ed8e-232">0x00000010</span></span>                               |
| <span data-ttu-id="2ed8e-233">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2ed8e-233">Classes used in</span></span>        | [<span data-ttu-id="2ed8e-234">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2ed8e-234">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2ed8e-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2ed8e-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2ed8e-236">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2ed8e-236">Entry</span></span> | <span data-ttu-id="2ed8e-237">Wert</span><span class="sxs-lookup"><span data-stu-id="2ed8e-237">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2ed8e-238">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2ed8e-238">Link-Id</span></span>                | <span data-ttu-id="2ed8e-239">2026</span><span class="sxs-lookup"><span data-stu-id="2ed8e-239">2026</span></span>                                     |
| <span data-ttu-id="2ed8e-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ed8e-240">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="2ed8e-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ed8e-241">System-Only</span></span>            | <span data-ttu-id="2ed8e-242">Richtig</span><span class="sxs-lookup"><span data-stu-id="2ed8e-242">True</span></span>                                     |
| <span data-ttu-id="2ed8e-243">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2ed8e-243">Is-Single-Valued</span></span>       | <span data-ttu-id="2ed8e-244">False</span><span class="sxs-lookup"><span data-stu-id="2ed8e-244">False</span></span>                                    |
| <span data-ttu-id="2ed8e-245">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2ed8e-245">Is Indexed</span></span>             | <span data-ttu-id="2ed8e-246">False</span><span class="sxs-lookup"><span data-stu-id="2ed8e-246">False</span></span>                                    |
| <span data-ttu-id="2ed8e-247">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2ed8e-247">In Global Catalog</span></span>      | <span data-ttu-id="2ed8e-248">False</span><span class="sxs-lookup"><span data-stu-id="2ed8e-248">False</span></span>                                    |
| <span data-ttu-id="2ed8e-249">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2ed8e-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ed8e-250">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2ed8e-250">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2ed8e-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ed8e-251">Range-Lower</span></span>            | <span data-ttu-id="2ed8e-252">4</span><span class="sxs-lookup"><span data-stu-id="2ed8e-252">4</span></span>                                        |
| <span data-ttu-id="2ed8e-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ed8e-253">Range-Upper</span></span>            | <span data-ttu-id="2ed8e-254">4</span><span class="sxs-lookup"><span data-stu-id="2ed8e-254">4</span></span>                                        |
| <span data-ttu-id="2ed8e-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ed8e-255">Search-Flags</span></span>           | <span data-ttu-id="2ed8e-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ed8e-256">0x00000000</span></span>                               |
| <span data-ttu-id="2ed8e-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ed8e-257">System-Flags</span></span>           | <span data-ttu-id="2ed8e-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ed8e-258">0x00000010</span></span>                               |
| <span data-ttu-id="2ed8e-259">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2ed8e-259">Classes used in</span></span>        | [<span data-ttu-id="2ed8e-260">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2ed8e-260">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2ed8e-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2ed8e-261">Windows Server 2012</span></span>



| <span data-ttu-id="2ed8e-262">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2ed8e-262">Entry</span></span> | <span data-ttu-id="2ed8e-263">Wert</span><span class="sxs-lookup"><span data-stu-id="2ed8e-263">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2ed8e-264">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2ed8e-264">Link-Id</span></span>                | <span data-ttu-id="2ed8e-265">2026</span><span class="sxs-lookup"><span data-stu-id="2ed8e-265">2026</span></span>                                     |
| <span data-ttu-id="2ed8e-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ed8e-266">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="2ed8e-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ed8e-267">System-Only</span></span>            | <span data-ttu-id="2ed8e-268">Richtig</span><span class="sxs-lookup"><span data-stu-id="2ed8e-268">True</span></span>                                     |
| <span data-ttu-id="2ed8e-269">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2ed8e-269">Is-Single-Valued</span></span>       | <span data-ttu-id="2ed8e-270">False</span><span class="sxs-lookup"><span data-stu-id="2ed8e-270">False</span></span>                                    |
| <span data-ttu-id="2ed8e-271">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2ed8e-271">Is Indexed</span></span>             | <span data-ttu-id="2ed8e-272">False</span><span class="sxs-lookup"><span data-stu-id="2ed8e-272">False</span></span>                                    |
| <span data-ttu-id="2ed8e-273">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2ed8e-273">In Global Catalog</span></span>      | <span data-ttu-id="2ed8e-274">False</span><span class="sxs-lookup"><span data-stu-id="2ed8e-274">False</span></span>                                    |
| <span data-ttu-id="2ed8e-275">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2ed8e-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ed8e-276">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2ed8e-276">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2ed8e-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ed8e-277">Range-Lower</span></span>            | <span data-ttu-id="2ed8e-278">4</span><span class="sxs-lookup"><span data-stu-id="2ed8e-278">4</span></span>                                        |
| <span data-ttu-id="2ed8e-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ed8e-279">Range-Upper</span></span>            | <span data-ttu-id="2ed8e-280">4</span><span class="sxs-lookup"><span data-stu-id="2ed8e-280">4</span></span>                                        |
| <span data-ttu-id="2ed8e-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ed8e-281">Search-Flags</span></span>           | <span data-ttu-id="2ed8e-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ed8e-282">0x00000000</span></span>                               |
| <span data-ttu-id="2ed8e-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ed8e-283">System-Flags</span></span>           | <span data-ttu-id="2ed8e-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ed8e-284">0x00000010</span></span>                               |
| <span data-ttu-id="2ed8e-285">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2ed8e-285">Classes used in</span></span>        | [<span data-ttu-id="2ed8e-286">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2ed8e-286">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





