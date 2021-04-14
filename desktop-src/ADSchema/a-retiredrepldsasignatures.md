---
title: Zurückgezogene-repl-DSA-Signaturen-Attribut
description: Verfolgt die letzten DS-Replikations Identitäten eines bestimmten Domänen Controllers.
ms.assetid: 82e8b222-5635-41ad-b2ab-386c9e6aa280
ms.tgt_platform: multiple
keywords:
- AD-Schema für das zurückgezogene repl-DSA-Signaturen-Attribut
- retiredrepldsasignaturen-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Retired-Repl-DSA-Signatures
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a9a4cb4030a8d3aa24244bc2e7a2702e83686fc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104392298"
---
# <a name="retired-repl-dsa-signatures-attribute"></a><span data-ttu-id="ef275-105">Zurückgezogene-repl-DSA-Signaturen-Attribut</span><span class="sxs-lookup"><span data-stu-id="ef275-105">Retired-Repl-DSA-Signatures attribute</span></span>

<span data-ttu-id="ef275-106">Verfolgt die letzten DS-Replikations Identitäten eines bestimmten Domänen Controllers.</span><span class="sxs-lookup"><span data-stu-id="ef275-106">Tracks the past DS replication identities of a given DC.</span></span>



| <span data-ttu-id="ef275-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ef275-107">Entry</span></span> | <span data-ttu-id="ef275-108">Wert</span><span class="sxs-lookup"><span data-stu-id="ef275-108">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ef275-109">CN</span><span class="sxs-lookup"><span data-stu-id="ef275-109">CN</span></span>                | <span data-ttu-id="ef275-110">Veraltet-repl-DSA-Signaturen</span><span class="sxs-lookup"><span data-stu-id="ef275-110">Retired-Repl-DSA-Signatures</span></span>                                                         |
| <span data-ttu-id="ef275-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ef275-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ef275-112">retiredrepldsasignaturen</span><span class="sxs-lookup"><span data-stu-id="ef275-112">retiredReplDSASignatures</span></span>                                                            |
| <span data-ttu-id="ef275-113">Size</span><span class="sxs-lookup"><span data-stu-id="ef275-113">Size</span></span>              | <span data-ttu-id="ef275-114">Die Länge ist proportional zur Häufigkeit, mit der der DC von der Sicherung wieder hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ef275-114">Length is proportional to the number of times the DC has been restored from backup.</span></span> |
| <span data-ttu-id="ef275-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ef275-115">Update Privilege</span></span>  | <span data-ttu-id="ef275-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ef275-116">This value is set by the system.</span></span>                                                    |
| <span data-ttu-id="ef275-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="ef275-117">Update Frequency</span></span>  | \-                                                                                  |
| <span data-ttu-id="ef275-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ef275-118">Attribute-Id</span></span>      | <span data-ttu-id="ef275-119">1.2.840.113556.1.4.673</span><span class="sxs-lookup"><span data-stu-id="ef275-119">1.2.840.113556.1.4.673</span></span>                                                              |
| <span data-ttu-id="ef275-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ef275-120">System-Id-Guid</span></span>    | <span data-ttu-id="ef275-121">7bf dcb7f -4807-11d1-a9c3-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="ef275-121">7bfdcb7f-4807-11d1-a9c3-0000f80367c1</span></span>                                                |
| <span data-ttu-id="ef275-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef275-122">Syntax</span></span>            | [<span data-ttu-id="ef275-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="ef275-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                               |



## <a name="implementations"></a><span data-ttu-id="ef275-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="ef275-124">Implementations</span></span>

-   [<span data-ttu-id="ef275-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ef275-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ef275-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ef275-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ef275-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="ef275-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ef275-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ef275-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ef275-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ef275-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ef275-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ef275-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ef275-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ef275-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ef275-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ef275-132">Windows 2000 Server</span></span>



| <span data-ttu-id="ef275-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ef275-133">Entry</span></span> | <span data-ttu-id="ef275-134">Wert</span><span class="sxs-lookup"><span data-stu-id="ef275-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="ef275-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ef275-135">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="ef275-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef275-136">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="ef275-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef275-137">System-Only</span></span>            | <span data-ttu-id="ef275-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="ef275-138">True</span></span>                                     |
| <span data-ttu-id="ef275-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ef275-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ef275-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="ef275-140">True</span></span>                                     |
| <span data-ttu-id="ef275-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ef275-141">Is Indexed</span></span>             | <span data-ttu-id="ef275-142">False</span><span class="sxs-lookup"><span data-stu-id="ef275-142">False</span></span>                                    |
| <span data-ttu-id="ef275-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ef275-143">In Global Catalog</span></span>      | <span data-ttu-id="ef275-144">False</span><span class="sxs-lookup"><span data-stu-id="ef275-144">False</span></span>                                    |
| <span data-ttu-id="ef275-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ef275-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef275-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ef275-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="ef275-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef275-147">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="ef275-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef275-148">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="ef275-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef275-149">Search-Flags</span></span>           | <span data-ttu-id="ef275-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef275-150">0x00000000</span></span>                               |
| <span data-ttu-id="ef275-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef275-151">System-Flags</span></span>           | <span data-ttu-id="ef275-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef275-152">0x00000010</span></span>                               |
| <span data-ttu-id="ef275-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ef275-153">Classes used in</span></span>        | [<span data-ttu-id="ef275-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ef275-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ef275-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ef275-155">Windows Server 2003</span></span>



| <span data-ttu-id="ef275-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ef275-156">Entry</span></span> | <span data-ttu-id="ef275-157">Wert</span><span class="sxs-lookup"><span data-stu-id="ef275-157">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="ef275-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ef275-158">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="ef275-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef275-159">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="ef275-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef275-160">System-Only</span></span>            | <span data-ttu-id="ef275-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="ef275-161">True</span></span>                                     |
| <span data-ttu-id="ef275-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ef275-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ef275-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="ef275-163">True</span></span>                                     |
| <span data-ttu-id="ef275-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ef275-164">Is Indexed</span></span>             | <span data-ttu-id="ef275-165">False</span><span class="sxs-lookup"><span data-stu-id="ef275-165">False</span></span>                                    |
| <span data-ttu-id="ef275-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ef275-166">In Global Catalog</span></span>      | <span data-ttu-id="ef275-167">False</span><span class="sxs-lookup"><span data-stu-id="ef275-167">False</span></span>                                    |
| <span data-ttu-id="ef275-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ef275-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef275-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ef275-169">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="ef275-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef275-170">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="ef275-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef275-171">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="ef275-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef275-172">Search-Flags</span></span>           | <span data-ttu-id="ef275-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef275-173">0x00000000</span></span>                               |
| <span data-ttu-id="ef275-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef275-174">System-Flags</span></span>           | <span data-ttu-id="ef275-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef275-175">0x00000010</span></span>                               |
| <span data-ttu-id="ef275-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ef275-176">Classes used in</span></span>        | [<span data-ttu-id="ef275-177">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ef275-177">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ef275-178">Adam</span><span class="sxs-lookup"><span data-stu-id="ef275-178">ADAM</span></span>



| <span data-ttu-id="ef275-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ef275-179">Entry</span></span> | <span data-ttu-id="ef275-180">Wert</span><span class="sxs-lookup"><span data-stu-id="ef275-180">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="ef275-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ef275-181">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="ef275-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef275-182">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="ef275-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef275-183">System-Only</span></span>            | <span data-ttu-id="ef275-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="ef275-184">True</span></span>                                     |
| <span data-ttu-id="ef275-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ef275-185">Is-Single-Valued</span></span>       | <span data-ttu-id="ef275-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="ef275-186">True</span></span>                                     |
| <span data-ttu-id="ef275-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ef275-187">Is Indexed</span></span>             | <span data-ttu-id="ef275-188">False</span><span class="sxs-lookup"><span data-stu-id="ef275-188">False</span></span>                                    |
| <span data-ttu-id="ef275-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ef275-189">In Global Catalog</span></span>      | <span data-ttu-id="ef275-190">False</span><span class="sxs-lookup"><span data-stu-id="ef275-190">False</span></span>                                    |
| <span data-ttu-id="ef275-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ef275-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef275-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ef275-192">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="ef275-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef275-193">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="ef275-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef275-194">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="ef275-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef275-195">Search-Flags</span></span>           | <span data-ttu-id="ef275-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef275-196">0x00000000</span></span>                               |
| <span data-ttu-id="ef275-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef275-197">System-Flags</span></span>           | <span data-ttu-id="ef275-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef275-198">0x00000010</span></span>                               |
| <span data-ttu-id="ef275-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ef275-199">Classes used in</span></span>        | [<span data-ttu-id="ef275-200">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ef275-200">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ef275-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ef275-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ef275-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ef275-202">Entry</span></span> | <span data-ttu-id="ef275-203">Wert</span><span class="sxs-lookup"><span data-stu-id="ef275-203">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="ef275-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ef275-204">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="ef275-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef275-205">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="ef275-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef275-206">System-Only</span></span>            | <span data-ttu-id="ef275-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="ef275-207">True</span></span>                                     |
| <span data-ttu-id="ef275-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ef275-208">Is-Single-Valued</span></span>       | <span data-ttu-id="ef275-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="ef275-209">True</span></span>                                     |
| <span data-ttu-id="ef275-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ef275-210">Is Indexed</span></span>             | <span data-ttu-id="ef275-211">False</span><span class="sxs-lookup"><span data-stu-id="ef275-211">False</span></span>                                    |
| <span data-ttu-id="ef275-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ef275-212">In Global Catalog</span></span>      | <span data-ttu-id="ef275-213">False</span><span class="sxs-lookup"><span data-stu-id="ef275-213">False</span></span>                                    |
| <span data-ttu-id="ef275-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ef275-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef275-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ef275-215">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="ef275-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef275-216">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="ef275-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef275-217">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="ef275-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef275-218">Search-Flags</span></span>           | <span data-ttu-id="ef275-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef275-219">0x00000000</span></span>                               |
| <span data-ttu-id="ef275-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef275-220">System-Flags</span></span>           | <span data-ttu-id="ef275-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef275-221">0x00000010</span></span>                               |
| <span data-ttu-id="ef275-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ef275-222">Classes used in</span></span>        | [<span data-ttu-id="ef275-223">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ef275-223">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ef275-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef275-224">Windows Server 2008</span></span>



| <span data-ttu-id="ef275-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ef275-225">Entry</span></span> | <span data-ttu-id="ef275-226">Wert</span><span class="sxs-lookup"><span data-stu-id="ef275-226">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="ef275-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ef275-227">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="ef275-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef275-228">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="ef275-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef275-229">System-Only</span></span>            | <span data-ttu-id="ef275-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="ef275-230">True</span></span>                                     |
| <span data-ttu-id="ef275-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ef275-231">Is-Single-Valued</span></span>       | <span data-ttu-id="ef275-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="ef275-232">True</span></span>                                     |
| <span data-ttu-id="ef275-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ef275-233">Is Indexed</span></span>             | <span data-ttu-id="ef275-234">False</span><span class="sxs-lookup"><span data-stu-id="ef275-234">False</span></span>                                    |
| <span data-ttu-id="ef275-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ef275-235">In Global Catalog</span></span>      | <span data-ttu-id="ef275-236">False</span><span class="sxs-lookup"><span data-stu-id="ef275-236">False</span></span>                                    |
| <span data-ttu-id="ef275-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ef275-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef275-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ef275-238">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="ef275-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef275-239">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="ef275-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef275-240">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="ef275-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef275-241">Search-Flags</span></span>           | <span data-ttu-id="ef275-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef275-242">0x00000000</span></span>                               |
| <span data-ttu-id="ef275-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef275-243">System-Flags</span></span>           | <span data-ttu-id="ef275-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef275-244">0x00000010</span></span>                               |
| <span data-ttu-id="ef275-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ef275-245">Classes used in</span></span>        | [<span data-ttu-id="ef275-246">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ef275-246">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ef275-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ef275-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ef275-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ef275-248">Entry</span></span> | <span data-ttu-id="ef275-249">Wert</span><span class="sxs-lookup"><span data-stu-id="ef275-249">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="ef275-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ef275-250">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="ef275-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef275-251">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="ef275-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef275-252">System-Only</span></span>            | <span data-ttu-id="ef275-253">Richtig</span><span class="sxs-lookup"><span data-stu-id="ef275-253">True</span></span>                                     |
| <span data-ttu-id="ef275-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ef275-254">Is-Single-Valued</span></span>       | <span data-ttu-id="ef275-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="ef275-255">True</span></span>                                     |
| <span data-ttu-id="ef275-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ef275-256">Is Indexed</span></span>             | <span data-ttu-id="ef275-257">False</span><span class="sxs-lookup"><span data-stu-id="ef275-257">False</span></span>                                    |
| <span data-ttu-id="ef275-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ef275-258">In Global Catalog</span></span>      | <span data-ttu-id="ef275-259">False</span><span class="sxs-lookup"><span data-stu-id="ef275-259">False</span></span>                                    |
| <span data-ttu-id="ef275-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ef275-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef275-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ef275-261">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="ef275-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef275-262">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="ef275-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef275-263">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="ef275-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef275-264">Search-Flags</span></span>           | <span data-ttu-id="ef275-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef275-265">0x00000000</span></span>                               |
| <span data-ttu-id="ef275-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef275-266">System-Flags</span></span>           | <span data-ttu-id="ef275-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef275-267">0x00000010</span></span>                               |
| <span data-ttu-id="ef275-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ef275-268">Classes used in</span></span>        | [<span data-ttu-id="ef275-269">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ef275-269">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ef275-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ef275-270">Windows Server 2012</span></span>



| <span data-ttu-id="ef275-271">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ef275-271">Entry</span></span> | <span data-ttu-id="ef275-272">Wert</span><span class="sxs-lookup"><span data-stu-id="ef275-272">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="ef275-273">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ef275-273">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="ef275-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef275-274">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="ef275-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef275-275">System-Only</span></span>            | <span data-ttu-id="ef275-276">Richtig</span><span class="sxs-lookup"><span data-stu-id="ef275-276">True</span></span>                                     |
| <span data-ttu-id="ef275-277">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ef275-277">Is-Single-Valued</span></span>       | <span data-ttu-id="ef275-278">Richtig</span><span class="sxs-lookup"><span data-stu-id="ef275-278">True</span></span>                                     |
| <span data-ttu-id="ef275-279">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ef275-279">Is Indexed</span></span>             | <span data-ttu-id="ef275-280">False</span><span class="sxs-lookup"><span data-stu-id="ef275-280">False</span></span>                                    |
| <span data-ttu-id="ef275-281">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ef275-281">In Global Catalog</span></span>      | <span data-ttu-id="ef275-282">False</span><span class="sxs-lookup"><span data-stu-id="ef275-282">False</span></span>                                    |
| <span data-ttu-id="ef275-283">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ef275-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef275-284">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ef275-284">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="ef275-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef275-285">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="ef275-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef275-286">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="ef275-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef275-287">Search-Flags</span></span>           | <span data-ttu-id="ef275-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef275-288">0x00000000</span></span>                               |
| <span data-ttu-id="ef275-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef275-289">System-Flags</span></span>           | <span data-ttu-id="ef275-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef275-290">0x00000010</span></span>                               |
| <span data-ttu-id="ef275-291">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ef275-291">Classes used in</span></span>        | [<span data-ttu-id="ef275-292">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ef275-292">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





