---
title: ms-DS-has-instantiated-NCS-Attribut
description: DS-Replikations Zustandsinformationen, analog zu (und einer übergeordneten Menge) der vorhandenen Attribute hasmasterncs und haspartialreplicancs. Für die Verwendung durch die KCC beim Einrichten von Replikations Partnern.
ms.assetid: 00dda441-e382-4fb2-b735-ae547901c11f
ms.tgt_platform: multiple
keywords:
- 'ms-DS-has-instanziiert: AD-Schema des NCS-Attributs'
- AD-Schema des msDS-hasinstantiatedncs-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Has-Instantiated-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2900d68f82e859bac7ce1dabbfea2d28fd8998b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480095"
---
# <a name="ms-ds-has-instantiated-ncs-attribute"></a><span data-ttu-id="4a847-106">ms-DS-has-instantiated-NCS-Attribut</span><span class="sxs-lookup"><span data-stu-id="4a847-106">ms-DS-Has-Instantiated-NCs attribute</span></span>

<span data-ttu-id="4a847-107">DS-Replikations Zustandsinformationen, analog zu (und einer übergeordneten Menge) der vorhandenen Attribute hasmasterncs und haspartialreplicancs.</span><span class="sxs-lookup"><span data-stu-id="4a847-107">DS replication state information, analogous to (and a superset of) the existing attributes hasMasterNCs and hasPartialReplicaNCs.</span></span> <span data-ttu-id="4a847-108">Für die Verwendung durch die KCC beim Einrichten von Replikations Partnern.</span><span class="sxs-lookup"><span data-stu-id="4a847-108">To be used by the KCC when setting up replication partners.</span></span>



| <span data-ttu-id="4a847-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a847-109">Entry</span></span> | <span data-ttu-id="4a847-110">Wert</span><span class="sxs-lookup"><span data-stu-id="4a847-110">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a847-111">CN</span><span class="sxs-lookup"><span data-stu-id="4a847-111">CN</span></span>                | <span data-ttu-id="4a847-112">ms-DS-has-instantiated-NCS</span><span class="sxs-lookup"><span data-stu-id="4a847-112">ms-DS-Has-Instantiated-NCs</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="4a847-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4a847-113">Ldap-Display-Name</span></span> | <span data-ttu-id="4a847-114">MSDS-hasinstantiatedncs</span><span class="sxs-lookup"><span data-stu-id="4a847-114">msDS-HasInstantiatedNCs</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="4a847-115">Size</span><span class="sxs-lookup"><span data-stu-id="4a847-115">Size</span></span>              | <span data-ttu-id="4a847-116">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="4a847-116">4 bytes</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="4a847-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="4a847-117">Update Privilege</span></span>  | <span data-ttu-id="4a847-118">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4a847-118">This value is set by the system.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="4a847-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="4a847-119">Update Frequency</span></span>  | <span data-ttu-id="4a847-120">Ungefähr doppelt so oft wie hasmasterncs/haspartialreplicancs.</span><span class="sxs-lookup"><span data-stu-id="4a847-120">Roughly twice as often as hasMasterNCs / hasPartialReplicaNCs.</span></span> <span data-ttu-id="4a847-121">Diese vorhandenen Attribute werden nur aktualisiert, wenn der Domänen Controller eine Partition hinzufügt oder entfernt (z. b. bei Wechsel von DC in GC oder umgekehrt).</span><span class="sxs-lookup"><span data-stu-id="4a847-121">These existing attributes are updated only when the DC adds or removes a partition (For example, when changing from DC to GC or vice versa).</span></span> |
| <span data-ttu-id="4a847-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4a847-122">Attribute-Id</span></span>      | <span data-ttu-id="4a847-123">1.2.840.113556.1.4.1709</span><span class="sxs-lookup"><span data-stu-id="4a847-123">1.2.840.113556.1.4.1709</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="4a847-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4a847-124">System-Id-Guid</span></span>    | <span data-ttu-id="4a847-125">11e9a5bc-4517-4049-af9c-51554, b0fc09</span><span class="sxs-lookup"><span data-stu-id="4a847-125">11e9a5bc-4517-4049-af9c-51554fb0fc09</span></span>                                                                                                                                                                        |
| <span data-ttu-id="4a847-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a847-126">Syntax</span></span>            | [<span data-ttu-id="4a847-127">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="4a847-127">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md)                                                                                                                                                             |



## <a name="implementations"></a><span data-ttu-id="4a847-128">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="4a847-128">Implementations</span></span>

-   [<span data-ttu-id="4a847-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4a847-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4a847-130">**Adam**</span><span class="sxs-lookup"><span data-stu-id="4a847-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="4a847-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4a847-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4a847-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4a847-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4a847-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4a847-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4a847-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4a847-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="4a847-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4a847-135">Windows Server 2003</span></span>



| <span data-ttu-id="4a847-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a847-136">Entry</span></span> | <span data-ttu-id="4a847-137">Wert</span><span class="sxs-lookup"><span data-stu-id="4a847-137">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4a847-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4a847-138">Link-Id</span></span>                | <span data-ttu-id="4a847-139">2002</span><span class="sxs-lookup"><span data-stu-id="4a847-139">2002</span></span>                                     |
| <span data-ttu-id="4a847-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a847-140">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4a847-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a847-141">System-Only</span></span>            | <span data-ttu-id="4a847-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a847-142">True</span></span>                                     |
| <span data-ttu-id="4a847-143">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4a847-143">Is-Single-Valued</span></span>       | <span data-ttu-id="4a847-144">False</span><span class="sxs-lookup"><span data-stu-id="4a847-144">False</span></span>                                    |
| <span data-ttu-id="4a847-145">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4a847-145">Is Indexed</span></span>             | <span data-ttu-id="4a847-146">False</span><span class="sxs-lookup"><span data-stu-id="4a847-146">False</span></span>                                    |
| <span data-ttu-id="4a847-147">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4a847-147">In Global Catalog</span></span>      | <span data-ttu-id="4a847-148">False</span><span class="sxs-lookup"><span data-stu-id="4a847-148">False</span></span>                                    |
| <span data-ttu-id="4a847-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a847-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a847-150">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4a847-150">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4a847-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a847-151">Range-Lower</span></span>            | <span data-ttu-id="4a847-152">4</span><span class="sxs-lookup"><span data-stu-id="4a847-152">4</span></span>                                        |
| <span data-ttu-id="4a847-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a847-153">Range-Upper</span></span>            | <span data-ttu-id="4a847-154">4</span><span class="sxs-lookup"><span data-stu-id="4a847-154">4</span></span>                                        |
| <span data-ttu-id="4a847-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a847-155">Search-Flags</span></span>           | <span data-ttu-id="4a847-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a847-156">0x00000000</span></span>                               |
| <span data-ttu-id="4a847-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a847-157">System-Flags</span></span>           | <span data-ttu-id="4a847-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a847-158">0x00000010</span></span>                               |
| <span data-ttu-id="4a847-159">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4a847-159">Classes used in</span></span>        | [<span data-ttu-id="4a847-160">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="4a847-160">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="4a847-161">Adam</span><span class="sxs-lookup"><span data-stu-id="4a847-161">ADAM</span></span>



| <span data-ttu-id="4a847-162">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a847-162">Entry</span></span> | <span data-ttu-id="4a847-163">Wert</span><span class="sxs-lookup"><span data-stu-id="4a847-163">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4a847-164">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4a847-164">Link-Id</span></span>                | <span data-ttu-id="4a847-165">2002</span><span class="sxs-lookup"><span data-stu-id="4a847-165">2002</span></span>                                     |
| <span data-ttu-id="4a847-166">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a847-166">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4a847-167">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a847-167">System-Only</span></span>            | <span data-ttu-id="4a847-168">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a847-168">True</span></span>                                     |
| <span data-ttu-id="4a847-169">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4a847-169">Is-Single-Valued</span></span>       | <span data-ttu-id="4a847-170">False</span><span class="sxs-lookup"><span data-stu-id="4a847-170">False</span></span>                                    |
| <span data-ttu-id="4a847-171">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4a847-171">Is Indexed</span></span>             | <span data-ttu-id="4a847-172">False</span><span class="sxs-lookup"><span data-stu-id="4a847-172">False</span></span>                                    |
| <span data-ttu-id="4a847-173">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4a847-173">In Global Catalog</span></span>      | <span data-ttu-id="4a847-174">False</span><span class="sxs-lookup"><span data-stu-id="4a847-174">False</span></span>                                    |
| <span data-ttu-id="4a847-175">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a847-175">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a847-176">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4a847-176">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4a847-177">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a847-177">Range-Lower</span></span>            | <span data-ttu-id="4a847-178">4</span><span class="sxs-lookup"><span data-stu-id="4a847-178">4</span></span>                                        |
| <span data-ttu-id="4a847-179">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a847-179">Range-Upper</span></span>            | <span data-ttu-id="4a847-180">4</span><span class="sxs-lookup"><span data-stu-id="4a847-180">4</span></span>                                        |
| <span data-ttu-id="4a847-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a847-181">Search-Flags</span></span>           | <span data-ttu-id="4a847-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a847-182">0x00000000</span></span>                               |
| <span data-ttu-id="4a847-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a847-183">System-Flags</span></span>           | <span data-ttu-id="4a847-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a847-184">0x00000010</span></span>                               |
| <span data-ttu-id="4a847-185">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4a847-185">Classes used in</span></span>        | [<span data-ttu-id="4a847-186">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="4a847-186">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4a847-187">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4a847-187">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4a847-188">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a847-188">Entry</span></span> | <span data-ttu-id="4a847-189">Wert</span><span class="sxs-lookup"><span data-stu-id="4a847-189">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4a847-190">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4a847-190">Link-Id</span></span>                | <span data-ttu-id="4a847-191">2002</span><span class="sxs-lookup"><span data-stu-id="4a847-191">2002</span></span>                                     |
| <span data-ttu-id="4a847-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a847-192">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4a847-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a847-193">System-Only</span></span>            | <span data-ttu-id="4a847-194">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a847-194">True</span></span>                                     |
| <span data-ttu-id="4a847-195">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4a847-195">Is-Single-Valued</span></span>       | <span data-ttu-id="4a847-196">False</span><span class="sxs-lookup"><span data-stu-id="4a847-196">False</span></span>                                    |
| <span data-ttu-id="4a847-197">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4a847-197">Is Indexed</span></span>             | <span data-ttu-id="4a847-198">False</span><span class="sxs-lookup"><span data-stu-id="4a847-198">False</span></span>                                    |
| <span data-ttu-id="4a847-199">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4a847-199">In Global Catalog</span></span>      | <span data-ttu-id="4a847-200">False</span><span class="sxs-lookup"><span data-stu-id="4a847-200">False</span></span>                                    |
| <span data-ttu-id="4a847-201">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a847-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a847-202">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4a847-202">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4a847-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a847-203">Range-Lower</span></span>            | <span data-ttu-id="4a847-204">4</span><span class="sxs-lookup"><span data-stu-id="4a847-204">4</span></span>                                        |
| <span data-ttu-id="4a847-205">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a847-205">Range-Upper</span></span>            | <span data-ttu-id="4a847-206">4</span><span class="sxs-lookup"><span data-stu-id="4a847-206">4</span></span>                                        |
| <span data-ttu-id="4a847-207">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a847-207">Search-Flags</span></span>           | <span data-ttu-id="4a847-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a847-208">0x00000000</span></span>                               |
| <span data-ttu-id="4a847-209">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a847-209">System-Flags</span></span>           | <span data-ttu-id="4a847-210">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a847-210">0x00000010</span></span>                               |
| <span data-ttu-id="4a847-211">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4a847-211">Classes used in</span></span>        | [<span data-ttu-id="4a847-212">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="4a847-212">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4a847-213">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a847-213">Windows Server 2008</span></span>



| <span data-ttu-id="4a847-214">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a847-214">Entry</span></span> | <span data-ttu-id="4a847-215">Wert</span><span class="sxs-lookup"><span data-stu-id="4a847-215">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4a847-216">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4a847-216">Link-Id</span></span>                | <span data-ttu-id="4a847-217">2002</span><span class="sxs-lookup"><span data-stu-id="4a847-217">2002</span></span>                                     |
| <span data-ttu-id="4a847-218">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a847-218">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4a847-219">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a847-219">System-Only</span></span>            | <span data-ttu-id="4a847-220">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a847-220">True</span></span>                                     |
| <span data-ttu-id="4a847-221">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4a847-221">Is-Single-Valued</span></span>       | <span data-ttu-id="4a847-222">False</span><span class="sxs-lookup"><span data-stu-id="4a847-222">False</span></span>                                    |
| <span data-ttu-id="4a847-223">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4a847-223">Is Indexed</span></span>             | <span data-ttu-id="4a847-224">False</span><span class="sxs-lookup"><span data-stu-id="4a847-224">False</span></span>                                    |
| <span data-ttu-id="4a847-225">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4a847-225">In Global Catalog</span></span>      | <span data-ttu-id="4a847-226">False</span><span class="sxs-lookup"><span data-stu-id="4a847-226">False</span></span>                                    |
| <span data-ttu-id="4a847-227">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a847-227">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a847-228">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4a847-228">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4a847-229">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a847-229">Range-Lower</span></span>            | <span data-ttu-id="4a847-230">4</span><span class="sxs-lookup"><span data-stu-id="4a847-230">4</span></span>                                        |
| <span data-ttu-id="4a847-231">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a847-231">Range-Upper</span></span>            | <span data-ttu-id="4a847-232">4</span><span class="sxs-lookup"><span data-stu-id="4a847-232">4</span></span>                                        |
| <span data-ttu-id="4a847-233">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a847-233">Search-Flags</span></span>           | <span data-ttu-id="4a847-234">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a847-234">0x00000000</span></span>                               |
| <span data-ttu-id="4a847-235">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a847-235">System-Flags</span></span>           | <span data-ttu-id="4a847-236">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a847-236">0x00000010</span></span>                               |
| <span data-ttu-id="4a847-237">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4a847-237">Classes used in</span></span>        | [<span data-ttu-id="4a847-238">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="4a847-238">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4a847-239">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4a847-239">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4a847-240">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a847-240">Entry</span></span> | <span data-ttu-id="4a847-241">Wert</span><span class="sxs-lookup"><span data-stu-id="4a847-241">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4a847-242">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4a847-242">Link-Id</span></span>                | <span data-ttu-id="4a847-243">2002</span><span class="sxs-lookup"><span data-stu-id="4a847-243">2002</span></span>                                     |
| <span data-ttu-id="4a847-244">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a847-244">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4a847-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a847-245">System-Only</span></span>            | <span data-ttu-id="4a847-246">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a847-246">True</span></span>                                     |
| <span data-ttu-id="4a847-247">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4a847-247">Is-Single-Valued</span></span>       | <span data-ttu-id="4a847-248">False</span><span class="sxs-lookup"><span data-stu-id="4a847-248">False</span></span>                                    |
| <span data-ttu-id="4a847-249">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4a847-249">Is Indexed</span></span>             | <span data-ttu-id="4a847-250">False</span><span class="sxs-lookup"><span data-stu-id="4a847-250">False</span></span>                                    |
| <span data-ttu-id="4a847-251">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4a847-251">In Global Catalog</span></span>      | <span data-ttu-id="4a847-252">False</span><span class="sxs-lookup"><span data-stu-id="4a847-252">False</span></span>                                    |
| <span data-ttu-id="4a847-253">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a847-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a847-254">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4a847-254">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4a847-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a847-255">Range-Lower</span></span>            | <span data-ttu-id="4a847-256">4</span><span class="sxs-lookup"><span data-stu-id="4a847-256">4</span></span>                                        |
| <span data-ttu-id="4a847-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a847-257">Range-Upper</span></span>            | <span data-ttu-id="4a847-258">4</span><span class="sxs-lookup"><span data-stu-id="4a847-258">4</span></span>                                        |
| <span data-ttu-id="4a847-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a847-259">Search-Flags</span></span>           | <span data-ttu-id="4a847-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a847-260">0x00000000</span></span>                               |
| <span data-ttu-id="4a847-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a847-261">System-Flags</span></span>           | <span data-ttu-id="4a847-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a847-262">0x00000010</span></span>                               |
| <span data-ttu-id="4a847-263">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4a847-263">Classes used in</span></span>        | [<span data-ttu-id="4a847-264">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="4a847-264">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4a847-265">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4a847-265">Windows Server 2012</span></span>



| <span data-ttu-id="4a847-266">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a847-266">Entry</span></span> | <span data-ttu-id="4a847-267">Wert</span><span class="sxs-lookup"><span data-stu-id="4a847-267">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4a847-268">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4a847-268">Link-Id</span></span>                | <span data-ttu-id="4a847-269">2002</span><span class="sxs-lookup"><span data-stu-id="4a847-269">2002</span></span>                                     |
| <span data-ttu-id="4a847-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a847-270">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4a847-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a847-271">System-Only</span></span>            | <span data-ttu-id="4a847-272">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a847-272">True</span></span>                                     |
| <span data-ttu-id="4a847-273">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4a847-273">Is-Single-Valued</span></span>       | <span data-ttu-id="4a847-274">False</span><span class="sxs-lookup"><span data-stu-id="4a847-274">False</span></span>                                    |
| <span data-ttu-id="4a847-275">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4a847-275">Is Indexed</span></span>             | <span data-ttu-id="4a847-276">False</span><span class="sxs-lookup"><span data-stu-id="4a847-276">False</span></span>                                    |
| <span data-ttu-id="4a847-277">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4a847-277">In Global Catalog</span></span>      | <span data-ttu-id="4a847-278">False</span><span class="sxs-lookup"><span data-stu-id="4a847-278">False</span></span>                                    |
| <span data-ttu-id="4a847-279">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a847-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a847-280">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4a847-280">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4a847-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a847-281">Range-Lower</span></span>            | <span data-ttu-id="4a847-282">4</span><span class="sxs-lookup"><span data-stu-id="4a847-282">4</span></span>                                        |
| <span data-ttu-id="4a847-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a847-283">Range-Upper</span></span>            | <span data-ttu-id="4a847-284">4</span><span class="sxs-lookup"><span data-stu-id="4a847-284">4</span></span>                                        |
| <span data-ttu-id="4a847-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a847-285">Search-Flags</span></span>           | <span data-ttu-id="4a847-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a847-286">0x00000000</span></span>                               |
| <span data-ttu-id="4a847-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a847-287">System-Flags</span></span>           | <span data-ttu-id="4a847-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a847-288">0x00000010</span></span>                               |
| <span data-ttu-id="4a847-289">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4a847-289">Classes used in</span></span>        | [<span data-ttu-id="4a847-290">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="4a847-290">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





