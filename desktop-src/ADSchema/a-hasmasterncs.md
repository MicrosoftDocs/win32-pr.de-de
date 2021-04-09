---
title: Has-Master-NCS-Attribut
description: Der Distinguished Name für die Benennungs Kontexte für den DC. Forward-Link für das Mastered-By-Attribut.
ms.assetid: 77a7e693-513f-4f76-8c4f-d2ef3240323b
ms.tgt_platform: multiple
keywords:
- "\"Has-Master-NCS\"-Attribut AD-Schema"
- AD-Schema des hasmasterncs-Attributs
topic_type:
- apiref
api_name:
- Has-Master-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34756c491c5228c58da1b95d4fd7b838c691f38
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957550"
---
# <a name="has-master-ncs-attribute"></a><span data-ttu-id="b7c5f-106">Has-Master-NCS-Attribut</span><span class="sxs-lookup"><span data-stu-id="b7c5f-106">Has-Master-NCs attribute</span></span>

<span data-ttu-id="b7c5f-107">Der Distinguished Name für die Benennungs Kontexte für den DC.</span><span class="sxs-lookup"><span data-stu-id="b7c5f-107">The distinguished name for the naming contexts for the DC.</span></span> <span data-ttu-id="b7c5f-108">Forward-Link für das Mastered-By-Attribut.</span><span class="sxs-lookup"><span data-stu-id="b7c5f-108">Forward link for the Mastered-By attribute.</span></span>



| <span data-ttu-id="b7c5f-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b7c5f-109">Entry</span></span> | <span data-ttu-id="b7c5f-110">Wert</span><span class="sxs-lookup"><span data-stu-id="b7c5f-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="b7c5f-111">CN</span><span class="sxs-lookup"><span data-stu-id="b7c5f-111">CN</span></span>                | <span data-ttu-id="b7c5f-112">Has-Master-NCS</span><span class="sxs-lookup"><span data-stu-id="b7c5f-112">Has-Master-NCs</span></span>                          |
| <span data-ttu-id="b7c5f-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b7c5f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b7c5f-114">hasmasterncs</span><span class="sxs-lookup"><span data-stu-id="b7c5f-114">hasMasterNCs</span></span>                            |
| <span data-ttu-id="b7c5f-115">Size</span><span class="sxs-lookup"><span data-stu-id="b7c5f-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="b7c5f-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b7c5f-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="b7c5f-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="b7c5f-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="b7c5f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b7c5f-118">Attribute-Id</span></span>      | <span data-ttu-id="b7c5f-119">1.2.840.113556.1.2.14</span><span class="sxs-lookup"><span data-stu-id="b7c5f-119">1.2.840.113556.1.2.14</span></span>                   |
| <span data-ttu-id="b7c5f-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b7c5f-120">System-Id-Guid</span></span>    | <span data-ttu-id="b7c5f-121">bf967982-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b7c5f-121">bf967982-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="b7c5f-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7c5f-122">Syntax</span></span>            | [<span data-ttu-id="b7c5f-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="b7c5f-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="b7c5f-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="b7c5f-124">Implementations</span></span>

-   [<span data-ttu-id="b7c5f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b7c5f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b7c5f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b7c5f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b7c5f-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="b7c5f-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b7c5f-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b7c5f-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b7c5f-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b7c5f-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b7c5f-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b7c5f-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b7c5f-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b7c5f-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b7c5f-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b7c5f-132">Windows 2000 Server</span></span>



| <span data-ttu-id="b7c5f-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b7c5f-133">Entry</span></span> | <span data-ttu-id="b7c5f-134">Wert</span><span class="sxs-lookup"><span data-stu-id="b7c5f-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="b7c5f-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b7c5f-135">Link-Id</span></span>                | <span data-ttu-id="b7c5f-136">76</span><span class="sxs-lookup"><span data-stu-id="b7c5f-136">76</span></span>                                       |
| <span data-ttu-id="b7c5f-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7c5f-137">MAPI-Id</span></span>                | <span data-ttu-id="b7c5f-138">0x80b6</span><span class="sxs-lookup"><span data-stu-id="b7c5f-138">0x80B6</span></span>                                   |
| <span data-ttu-id="b7c5f-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7c5f-139">System-Only</span></span>            | <span data-ttu-id="b7c5f-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="b7c5f-140">True</span></span>                                     |
| <span data-ttu-id="b7c5f-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b7c5f-141">Is-Single-Valued</span></span>       | <span data-ttu-id="b7c5f-142">False</span><span class="sxs-lookup"><span data-stu-id="b7c5f-142">False</span></span>                                    |
| <span data-ttu-id="b7c5f-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b7c5f-143">Is Indexed</span></span>             | <span data-ttu-id="b7c5f-144">False</span><span class="sxs-lookup"><span data-stu-id="b7c5f-144">False</span></span>                                    |
| <span data-ttu-id="b7c5f-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b7c5f-145">In Global Catalog</span></span>      | <span data-ttu-id="b7c5f-146">False</span><span class="sxs-lookup"><span data-stu-id="b7c5f-146">False</span></span>                                    |
| <span data-ttu-id="b7c5f-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7c5f-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7c5f-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b7c5f-148">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="b7c5f-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7c5f-149">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="b7c5f-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7c5f-150">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="b7c5f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7c5f-151">Search-Flags</span></span>           | <span data-ttu-id="b7c5f-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7c5f-152">0x00000000</span></span>                               |
| <span data-ttu-id="b7c5f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7c5f-153">System-Flags</span></span>           | <span data-ttu-id="b7c5f-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7c5f-154">0x00000010</span></span>                               |
| <span data-ttu-id="b7c5f-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b7c5f-155">Classes used in</span></span>        | [<span data-ttu-id="b7c5f-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="b7c5f-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b7c5f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b7c5f-157">Windows Server 2003</span></span>



| <span data-ttu-id="b7c5f-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b7c5f-158">Entry</span></span> | <span data-ttu-id="b7c5f-159">Wert</span><span class="sxs-lookup"><span data-stu-id="b7c5f-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="b7c5f-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b7c5f-160">Link-Id</span></span>                | <span data-ttu-id="b7c5f-161">76</span><span class="sxs-lookup"><span data-stu-id="b7c5f-161">76</span></span>                                       |
| <span data-ttu-id="b7c5f-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7c5f-162">MAPI-Id</span></span>                | <span data-ttu-id="b7c5f-163">0x80b6</span><span class="sxs-lookup"><span data-stu-id="b7c5f-163">0x80B6</span></span>                                   |
| <span data-ttu-id="b7c5f-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7c5f-164">System-Only</span></span>            | <span data-ttu-id="b7c5f-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="b7c5f-165">True</span></span>                                     |
| <span data-ttu-id="b7c5f-166">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b7c5f-166">Is-Single-Valued</span></span>       | <span data-ttu-id="b7c5f-167">False</span><span class="sxs-lookup"><span data-stu-id="b7c5f-167">False</span></span>                                    |
| <span data-ttu-id="b7c5f-168">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b7c5f-168">Is Indexed</span></span>             | <span data-ttu-id="b7c5f-169">False</span><span class="sxs-lookup"><span data-stu-id="b7c5f-169">False</span></span>                                    |
| <span data-ttu-id="b7c5f-170">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b7c5f-170">In Global Catalog</span></span>      | <span data-ttu-id="b7c5f-171">False</span><span class="sxs-lookup"><span data-stu-id="b7c5f-171">False</span></span>                                    |
| <span data-ttu-id="b7c5f-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7c5f-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7c5f-173">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b7c5f-173">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="b7c5f-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7c5f-174">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="b7c5f-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7c5f-175">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="b7c5f-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7c5f-176">Search-Flags</span></span>           | <span data-ttu-id="b7c5f-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7c5f-177">0x00000000</span></span>                               |
| <span data-ttu-id="b7c5f-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7c5f-178">System-Flags</span></span>           | <span data-ttu-id="b7c5f-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7c5f-179">0x00000010</span></span>                               |
| <span data-ttu-id="b7c5f-180">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b7c5f-180">Classes used in</span></span>        | [<span data-ttu-id="b7c5f-181">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="b7c5f-181">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b7c5f-182">Adam</span><span class="sxs-lookup"><span data-stu-id="b7c5f-182">ADAM</span></span>



| <span data-ttu-id="b7c5f-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b7c5f-183">Entry</span></span> | <span data-ttu-id="b7c5f-184">Wert</span><span class="sxs-lookup"><span data-stu-id="b7c5f-184">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="b7c5f-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b7c5f-185">Link-Id</span></span>                | <span data-ttu-id="b7c5f-186">76</span><span class="sxs-lookup"><span data-stu-id="b7c5f-186">76</span></span>                                       |
| <span data-ttu-id="b7c5f-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7c5f-187">MAPI-Id</span></span>                | <span data-ttu-id="b7c5f-188">0x80b6</span><span class="sxs-lookup"><span data-stu-id="b7c5f-188">0x80B6</span></span>                                   |
| <span data-ttu-id="b7c5f-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7c5f-189">System-Only</span></span>            | <span data-ttu-id="b7c5f-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="b7c5f-190">True</span></span>                                     |
| <span data-ttu-id="b7c5f-191">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b7c5f-191">Is-Single-Valued</span></span>       | <span data-ttu-id="b7c5f-192">False</span><span class="sxs-lookup"><span data-stu-id="b7c5f-192">False</span></span>                                    |
| <span data-ttu-id="b7c5f-193">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b7c5f-193">Is Indexed</span></span>             | <span data-ttu-id="b7c5f-194">False</span><span class="sxs-lookup"><span data-stu-id="b7c5f-194">False</span></span>                                    |
| <span data-ttu-id="b7c5f-195">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b7c5f-195">In Global Catalog</span></span>      | <span data-ttu-id="b7c5f-196">False</span><span class="sxs-lookup"><span data-stu-id="b7c5f-196">False</span></span>                                    |
| <span data-ttu-id="b7c5f-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7c5f-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7c5f-198">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b7c5f-198">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="b7c5f-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7c5f-199">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="b7c5f-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7c5f-200">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="b7c5f-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7c5f-201">Search-Flags</span></span>           | <span data-ttu-id="b7c5f-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7c5f-202">0x00000000</span></span>                               |
| <span data-ttu-id="b7c5f-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7c5f-203">System-Flags</span></span>           | <span data-ttu-id="b7c5f-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7c5f-204">0x00000010</span></span>                               |
| <span data-ttu-id="b7c5f-205">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b7c5f-205">Classes used in</span></span>        | [<span data-ttu-id="b7c5f-206">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="b7c5f-206">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b7c5f-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b7c5f-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b7c5f-208">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b7c5f-208">Entry</span></span> | <span data-ttu-id="b7c5f-209">Wert</span><span class="sxs-lookup"><span data-stu-id="b7c5f-209">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="b7c5f-210">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b7c5f-210">Link-Id</span></span>                | <span data-ttu-id="b7c5f-211">76</span><span class="sxs-lookup"><span data-stu-id="b7c5f-211">76</span></span>                                       |
| <span data-ttu-id="b7c5f-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7c5f-212">MAPI-Id</span></span>                | <span data-ttu-id="b7c5f-213">0x80b6</span><span class="sxs-lookup"><span data-stu-id="b7c5f-213">0x80B6</span></span>                                   |
| <span data-ttu-id="b7c5f-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7c5f-214">System-Only</span></span>            | <span data-ttu-id="b7c5f-215">Richtig</span><span class="sxs-lookup"><span data-stu-id="b7c5f-215">True</span></span>                                     |
| <span data-ttu-id="b7c5f-216">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b7c5f-216">Is-Single-Valued</span></span>       | <span data-ttu-id="b7c5f-217">False</span><span class="sxs-lookup"><span data-stu-id="b7c5f-217">False</span></span>                                    |
| <span data-ttu-id="b7c5f-218">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b7c5f-218">Is Indexed</span></span>             | <span data-ttu-id="b7c5f-219">False</span><span class="sxs-lookup"><span data-stu-id="b7c5f-219">False</span></span>                                    |
| <span data-ttu-id="b7c5f-220">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b7c5f-220">In Global Catalog</span></span>      | <span data-ttu-id="b7c5f-221">False</span><span class="sxs-lookup"><span data-stu-id="b7c5f-221">False</span></span>                                    |
| <span data-ttu-id="b7c5f-222">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7c5f-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7c5f-223">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b7c5f-223">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="b7c5f-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7c5f-224">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="b7c5f-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7c5f-225">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="b7c5f-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7c5f-226">Search-Flags</span></span>           | <span data-ttu-id="b7c5f-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7c5f-227">0x00000000</span></span>                               |
| <span data-ttu-id="b7c5f-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7c5f-228">System-Flags</span></span>           | <span data-ttu-id="b7c5f-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7c5f-229">0x00000010</span></span>                               |
| <span data-ttu-id="b7c5f-230">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b7c5f-230">Classes used in</span></span>        | [<span data-ttu-id="b7c5f-231">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="b7c5f-231">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b7c5f-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7c5f-232">Windows Server 2008</span></span>



| <span data-ttu-id="b7c5f-233">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b7c5f-233">Entry</span></span> | <span data-ttu-id="b7c5f-234">Wert</span><span class="sxs-lookup"><span data-stu-id="b7c5f-234">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="b7c5f-235">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b7c5f-235">Link-Id</span></span>                | <span data-ttu-id="b7c5f-236">76</span><span class="sxs-lookup"><span data-stu-id="b7c5f-236">76</span></span>                                       |
| <span data-ttu-id="b7c5f-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7c5f-237">MAPI-Id</span></span>                | <span data-ttu-id="b7c5f-238">0x80b6</span><span class="sxs-lookup"><span data-stu-id="b7c5f-238">0x80B6</span></span>                                   |
| <span data-ttu-id="b7c5f-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7c5f-239">System-Only</span></span>            | <span data-ttu-id="b7c5f-240">Richtig</span><span class="sxs-lookup"><span data-stu-id="b7c5f-240">True</span></span>                                     |
| <span data-ttu-id="b7c5f-241">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b7c5f-241">Is-Single-Valued</span></span>       | <span data-ttu-id="b7c5f-242">False</span><span class="sxs-lookup"><span data-stu-id="b7c5f-242">False</span></span>                                    |
| <span data-ttu-id="b7c5f-243">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b7c5f-243">Is Indexed</span></span>             | <span data-ttu-id="b7c5f-244">False</span><span class="sxs-lookup"><span data-stu-id="b7c5f-244">False</span></span>                                    |
| <span data-ttu-id="b7c5f-245">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b7c5f-245">In Global Catalog</span></span>      | <span data-ttu-id="b7c5f-246">False</span><span class="sxs-lookup"><span data-stu-id="b7c5f-246">False</span></span>                                    |
| <span data-ttu-id="b7c5f-247">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7c5f-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7c5f-248">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b7c5f-248">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="b7c5f-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7c5f-249">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="b7c5f-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7c5f-250">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="b7c5f-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7c5f-251">Search-Flags</span></span>           | <span data-ttu-id="b7c5f-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7c5f-252">0x00000000</span></span>                               |
| <span data-ttu-id="b7c5f-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7c5f-253">System-Flags</span></span>           | <span data-ttu-id="b7c5f-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7c5f-254">0x00000010</span></span>                               |
| <span data-ttu-id="b7c5f-255">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b7c5f-255">Classes used in</span></span>        | [<span data-ttu-id="b7c5f-256">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="b7c5f-256">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b7c5f-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b7c5f-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b7c5f-258">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b7c5f-258">Entry</span></span> | <span data-ttu-id="b7c5f-259">Wert</span><span class="sxs-lookup"><span data-stu-id="b7c5f-259">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="b7c5f-260">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b7c5f-260">Link-Id</span></span>                | <span data-ttu-id="b7c5f-261">76</span><span class="sxs-lookup"><span data-stu-id="b7c5f-261">76</span></span>                                       |
| <span data-ttu-id="b7c5f-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7c5f-262">MAPI-Id</span></span>                | <span data-ttu-id="b7c5f-263">0x80b6</span><span class="sxs-lookup"><span data-stu-id="b7c5f-263">0x80B6</span></span>                                   |
| <span data-ttu-id="b7c5f-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7c5f-264">System-Only</span></span>            | <span data-ttu-id="b7c5f-265">Richtig</span><span class="sxs-lookup"><span data-stu-id="b7c5f-265">True</span></span>                                     |
| <span data-ttu-id="b7c5f-266">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b7c5f-266">Is-Single-Valued</span></span>       | <span data-ttu-id="b7c5f-267">False</span><span class="sxs-lookup"><span data-stu-id="b7c5f-267">False</span></span>                                    |
| <span data-ttu-id="b7c5f-268">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b7c5f-268">Is Indexed</span></span>             | <span data-ttu-id="b7c5f-269">False</span><span class="sxs-lookup"><span data-stu-id="b7c5f-269">False</span></span>                                    |
| <span data-ttu-id="b7c5f-270">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b7c5f-270">In Global Catalog</span></span>      | <span data-ttu-id="b7c5f-271">False</span><span class="sxs-lookup"><span data-stu-id="b7c5f-271">False</span></span>                                    |
| <span data-ttu-id="b7c5f-272">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7c5f-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7c5f-273">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b7c5f-273">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="b7c5f-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7c5f-274">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="b7c5f-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7c5f-275">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="b7c5f-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7c5f-276">Search-Flags</span></span>           | <span data-ttu-id="b7c5f-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7c5f-277">0x00000000</span></span>                               |
| <span data-ttu-id="b7c5f-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7c5f-278">System-Flags</span></span>           | <span data-ttu-id="b7c5f-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7c5f-279">0x00000010</span></span>                               |
| <span data-ttu-id="b7c5f-280">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b7c5f-280">Classes used in</span></span>        | [<span data-ttu-id="b7c5f-281">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="b7c5f-281">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b7c5f-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b7c5f-282">Windows Server 2012</span></span>



| <span data-ttu-id="b7c5f-283">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b7c5f-283">Entry</span></span> | <span data-ttu-id="b7c5f-284">Wert</span><span class="sxs-lookup"><span data-stu-id="b7c5f-284">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="b7c5f-285">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b7c5f-285">Link-Id</span></span>                | <span data-ttu-id="b7c5f-286">76</span><span class="sxs-lookup"><span data-stu-id="b7c5f-286">76</span></span>                                       |
| <span data-ttu-id="b7c5f-287">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7c5f-287">MAPI-Id</span></span>                | <span data-ttu-id="b7c5f-288">0x80b6</span><span class="sxs-lookup"><span data-stu-id="b7c5f-288">0x80B6</span></span>                                   |
| <span data-ttu-id="b7c5f-289">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7c5f-289">System-Only</span></span>            | <span data-ttu-id="b7c5f-290">Richtig</span><span class="sxs-lookup"><span data-stu-id="b7c5f-290">True</span></span>                                     |
| <span data-ttu-id="b7c5f-291">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b7c5f-291">Is-Single-Valued</span></span>       | <span data-ttu-id="b7c5f-292">False</span><span class="sxs-lookup"><span data-stu-id="b7c5f-292">False</span></span>                                    |
| <span data-ttu-id="b7c5f-293">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b7c5f-293">Is Indexed</span></span>             | <span data-ttu-id="b7c5f-294">False</span><span class="sxs-lookup"><span data-stu-id="b7c5f-294">False</span></span>                                    |
| <span data-ttu-id="b7c5f-295">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b7c5f-295">In Global Catalog</span></span>      | <span data-ttu-id="b7c5f-296">False</span><span class="sxs-lookup"><span data-stu-id="b7c5f-296">False</span></span>                                    |
| <span data-ttu-id="b7c5f-297">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7c5f-297">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7c5f-298">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b7c5f-298">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="b7c5f-299">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7c5f-299">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="b7c5f-300">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7c5f-300">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="b7c5f-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7c5f-301">Search-Flags</span></span>           | <span data-ttu-id="b7c5f-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7c5f-302">0x00000000</span></span>                               |
| <span data-ttu-id="b7c5f-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7c5f-303">System-Flags</span></span>           | <span data-ttu-id="b7c5f-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7c5f-304">0x00000010</span></span>                               |
| <span data-ttu-id="b7c5f-305">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b7c5f-305">Classes used in</span></span>        | [<span data-ttu-id="b7c5f-306">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="b7c5f-306">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





