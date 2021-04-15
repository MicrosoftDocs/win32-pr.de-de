---
title: MS-DS-replicates-NC-Reason-Attribut
description: Das Attribut des nTDSConnection-Objekts, das angibt, warum (oder ob) die KCC anzeigt, dass die Verbindung in der Replikations Topologie nützlich ist. Ist mit mehreren Werten und verfügt über die Syntax "DISTNAME + Binary", wobei der binäre Teil ein Bitfeld mit int-Größe ist.
ms.assetid: ba66e346-d288-4c0b-b41e-599c3f8e8405
ms.tgt_platform: multiple
keywords:
- MS-DS-replicates-NC-Reason-Attribut AD-Schema
- AD-Schema des ms-DS-replitoresnkreason-Attributs
topic_type:
- apiref
api_name:
- MS-DS-Replicates-NC-Reason
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a45c587ef82773b5e7fd310e8e8591f18ad27ab
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104392252"
---
# <a name="ms-ds-replicates-nc-reason-attribute"></a><span data-ttu-id="6f98d-106">MS-DS-replicates-NC-Reason-Attribut</span><span class="sxs-lookup"><span data-stu-id="6f98d-106">MS-DS-Replicates-NC-Reason attribute</span></span>

<span data-ttu-id="6f98d-107">Das Attribut des nTDSConnection-Objekts, das angibt, warum (oder ob) die KCC anzeigt, dass die Verbindung in der Replikations Topologie nützlich ist.</span><span class="sxs-lookup"><span data-stu-id="6f98d-107">Attribute of ntdsConnection object that indicates why (or whether) the KCC shows the connection is useful in the replication topology.</span></span> <span data-ttu-id="6f98d-108">Ist mit mehreren Werten und verfügt über die Syntax "DISTNAME + Binary", wobei der binäre Teil ein Bitfeld mit int-Größe ist.</span><span class="sxs-lookup"><span data-stu-id="6f98d-108">Is multiple-valued and has DistName+Binary syntax, where the binary part is an int-size bitfield.</span></span>



| <span data-ttu-id="6f98d-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6f98d-109">Entry</span></span> | <span data-ttu-id="6f98d-110">Wert</span><span class="sxs-lookup"><span data-stu-id="6f98d-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f98d-111">CN</span><span class="sxs-lookup"><span data-stu-id="6f98d-111">CN</span></span>                | <span data-ttu-id="6f98d-112">MS-DS-replicates-NC-Reason</span><span class="sxs-lookup"><span data-stu-id="6f98d-112">MS-DS-Replicates-NC-Reason</span></span>                                                                                                                 |
| <span data-ttu-id="6f98d-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6f98d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6f98d-114">mS-DS-replialisiesnkreason</span><span class="sxs-lookup"><span data-stu-id="6f98d-114">mS-DS-ReplicatesNCReason</span></span>                                                                                                                   |
| <span data-ttu-id="6f98d-115">Size</span><span class="sxs-lookup"><span data-stu-id="6f98d-115">Size</span></span>              | <span data-ttu-id="6f98d-116">Wert für binären Teil: 0 = kein \_ Grund, 1 = GC- \_ Topologie, 2 = Ring \_ Topologie, 4 = \_ \_ hoptopologie minimieren, 8 = veraltete \_ Server \_ Topologie.</span><span class="sxs-lookup"><span data-stu-id="6f98d-116">Value for binary portion: 0 = NO\_REASON,1 = GC\_TOPOLOGY, 2 = RING\_TOPOLOGY, 4 = MINIMIZE\_HOPS\_TOPOLOGY, 8 = STALE\_SERVERS\_TOPOLOGY.</span></span> |
| <span data-ttu-id="6f98d-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="6f98d-117">Update Privilege</span></span>  | <span data-ttu-id="6f98d-118">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6f98d-118">This value is set by the system.</span></span>                                                                                                           |
| <span data-ttu-id="6f98d-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="6f98d-119">Update Frequency</span></span>  | <span data-ttu-id="6f98d-120">Kann als Reaktion auf Änderungen in der Netzwerktopologie geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6f98d-120">Can change in response to changes in the network topology.</span></span>                                                                                 |
| <span data-ttu-id="6f98d-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6f98d-121">Attribute-Id</span></span>      | <span data-ttu-id="6f98d-122">1.2.840.113556.1.4.1408</span><span class="sxs-lookup"><span data-stu-id="6f98d-122">1.2.840.113556.1.4.1408</span></span>                                                                                                                    |
| <span data-ttu-id="6f98d-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6f98d-123">System-Id-Guid</span></span>    | <span data-ttu-id="6f98d-124">0ea12b84-08b3-11d3-91bc-0000f 87a57d4</span><span class="sxs-lookup"><span data-stu-id="6f98d-124">0ea12b84-08b3-11d3-91bc-0000f87a57d4</span></span>                                                                                                       |
| <span data-ttu-id="6f98d-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f98d-125">Syntax</span></span>            | [<span data-ttu-id="6f98d-126">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="6f98d-126">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md)                                                                                            |



## <a name="implementations"></a><span data-ttu-id="6f98d-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="6f98d-127">Implementations</span></span>

-   [<span data-ttu-id="6f98d-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6f98d-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6f98d-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6f98d-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6f98d-130">**Adam**</span><span class="sxs-lookup"><span data-stu-id="6f98d-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6f98d-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6f98d-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6f98d-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6f98d-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6f98d-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6f98d-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6f98d-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6f98d-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6f98d-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6f98d-135">Windows 2000 Server</span></span>



| <span data-ttu-id="6f98d-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6f98d-136">Entry</span></span> | <span data-ttu-id="6f98d-137">Wert</span><span class="sxs-lookup"><span data-stu-id="6f98d-137">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="6f98d-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6f98d-138">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6f98d-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f98d-139">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6f98d-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f98d-140">System-Only</span></span>            | <span data-ttu-id="6f98d-141">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-141">False</span></span>                                                  |
| <span data-ttu-id="6f98d-142">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6f98d-142">Is-Single-Valued</span></span>       | <span data-ttu-id="6f98d-143">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-143">False</span></span>                                                  |
| <span data-ttu-id="6f98d-144">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6f98d-144">Is Indexed</span></span>             | <span data-ttu-id="6f98d-145">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-145">False</span></span>                                                  |
| <span data-ttu-id="6f98d-146">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6f98d-146">In Global Catalog</span></span>      | <span data-ttu-id="6f98d-147">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-147">False</span></span>                                                  |
| <span data-ttu-id="6f98d-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6f98d-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f98d-149">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6f98d-149">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="6f98d-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f98d-150">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="6f98d-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f98d-151">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="6f98d-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f98d-152">Search-Flags</span></span>           | <span data-ttu-id="6f98d-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f98d-153">0x00000000</span></span>                                             |
| <span data-ttu-id="6f98d-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f98d-154">System-Flags</span></span>           | <span data-ttu-id="6f98d-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f98d-155">0x00000010</span></span>                                             |
| <span data-ttu-id="6f98d-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6f98d-156">Classes used in</span></span>        | [<span data-ttu-id="6f98d-157">**NTDS-Verbindung**</span><span class="sxs-lookup"><span data-stu-id="6f98d-157">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6f98d-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6f98d-158">Windows Server 2003</span></span>



| <span data-ttu-id="6f98d-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6f98d-159">Entry</span></span> | <span data-ttu-id="6f98d-160">Wert</span><span class="sxs-lookup"><span data-stu-id="6f98d-160">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="6f98d-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6f98d-161">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6f98d-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f98d-162">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6f98d-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f98d-163">System-Only</span></span>            | <span data-ttu-id="6f98d-164">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-164">False</span></span>                                                  |
| <span data-ttu-id="6f98d-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6f98d-165">Is-Single-Valued</span></span>       | <span data-ttu-id="6f98d-166">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-166">False</span></span>                                                  |
| <span data-ttu-id="6f98d-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6f98d-167">Is Indexed</span></span>             | <span data-ttu-id="6f98d-168">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-168">False</span></span>                                                  |
| <span data-ttu-id="6f98d-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6f98d-169">In Global Catalog</span></span>      | <span data-ttu-id="6f98d-170">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-170">False</span></span>                                                  |
| <span data-ttu-id="6f98d-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6f98d-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f98d-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6f98d-172">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="6f98d-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f98d-173">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="6f98d-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f98d-174">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="6f98d-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f98d-175">Search-Flags</span></span>           | <span data-ttu-id="6f98d-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f98d-176">0x00000000</span></span>                                             |
| <span data-ttu-id="6f98d-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f98d-177">System-Flags</span></span>           | <span data-ttu-id="6f98d-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f98d-178">0x00000010</span></span>                                             |
| <span data-ttu-id="6f98d-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6f98d-179">Classes used in</span></span>        | [<span data-ttu-id="6f98d-180">**NTDS-Verbindung**</span><span class="sxs-lookup"><span data-stu-id="6f98d-180">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6f98d-181">Adam</span><span class="sxs-lookup"><span data-stu-id="6f98d-181">ADAM</span></span>



| <span data-ttu-id="6f98d-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6f98d-182">Entry</span></span> | <span data-ttu-id="6f98d-183">Wert</span><span class="sxs-lookup"><span data-stu-id="6f98d-183">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="6f98d-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6f98d-184">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6f98d-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f98d-185">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6f98d-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f98d-186">System-Only</span></span>            | <span data-ttu-id="6f98d-187">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-187">False</span></span>                                                  |
| <span data-ttu-id="6f98d-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6f98d-188">Is-Single-Valued</span></span>       | <span data-ttu-id="6f98d-189">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-189">False</span></span>                                                  |
| <span data-ttu-id="6f98d-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6f98d-190">Is Indexed</span></span>             | <span data-ttu-id="6f98d-191">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-191">False</span></span>                                                  |
| <span data-ttu-id="6f98d-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6f98d-192">In Global Catalog</span></span>      | <span data-ttu-id="6f98d-193">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-193">False</span></span>                                                  |
| <span data-ttu-id="6f98d-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6f98d-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f98d-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6f98d-195">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="6f98d-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f98d-196">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="6f98d-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f98d-197">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="6f98d-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f98d-198">Search-Flags</span></span>           | <span data-ttu-id="6f98d-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f98d-199">0x00000000</span></span>                                             |
| <span data-ttu-id="6f98d-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f98d-200">System-Flags</span></span>           | <span data-ttu-id="6f98d-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f98d-201">0x00000010</span></span>                                             |
| <span data-ttu-id="6f98d-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6f98d-202">Classes used in</span></span>        | [<span data-ttu-id="6f98d-203">**NTDS-Verbindung**</span><span class="sxs-lookup"><span data-stu-id="6f98d-203">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6f98d-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6f98d-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6f98d-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6f98d-205">Entry</span></span> | <span data-ttu-id="6f98d-206">Wert</span><span class="sxs-lookup"><span data-stu-id="6f98d-206">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="6f98d-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6f98d-207">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6f98d-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f98d-208">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6f98d-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f98d-209">System-Only</span></span>            | <span data-ttu-id="6f98d-210">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-210">False</span></span>                                                  |
| <span data-ttu-id="6f98d-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6f98d-211">Is-Single-Valued</span></span>       | <span data-ttu-id="6f98d-212">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-212">False</span></span>                                                  |
| <span data-ttu-id="6f98d-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6f98d-213">Is Indexed</span></span>             | <span data-ttu-id="6f98d-214">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-214">False</span></span>                                                  |
| <span data-ttu-id="6f98d-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6f98d-215">In Global Catalog</span></span>      | <span data-ttu-id="6f98d-216">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-216">False</span></span>                                                  |
| <span data-ttu-id="6f98d-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6f98d-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f98d-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6f98d-218">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="6f98d-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f98d-219">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="6f98d-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f98d-220">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="6f98d-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f98d-221">Search-Flags</span></span>           | <span data-ttu-id="6f98d-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f98d-222">0x00000000</span></span>                                             |
| <span data-ttu-id="6f98d-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f98d-223">System-Flags</span></span>           | <span data-ttu-id="6f98d-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f98d-224">0x00000010</span></span>                                             |
| <span data-ttu-id="6f98d-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6f98d-225">Classes used in</span></span>        | [<span data-ttu-id="6f98d-226">**NTDS-Verbindung**</span><span class="sxs-lookup"><span data-stu-id="6f98d-226">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6f98d-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f98d-227">Windows Server 2008</span></span>



| <span data-ttu-id="6f98d-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6f98d-228">Entry</span></span> | <span data-ttu-id="6f98d-229">Wert</span><span class="sxs-lookup"><span data-stu-id="6f98d-229">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="6f98d-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6f98d-230">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6f98d-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f98d-231">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6f98d-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f98d-232">System-Only</span></span>            | <span data-ttu-id="6f98d-233">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-233">False</span></span>                                                  |
| <span data-ttu-id="6f98d-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6f98d-234">Is-Single-Valued</span></span>       | <span data-ttu-id="6f98d-235">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-235">False</span></span>                                                  |
| <span data-ttu-id="6f98d-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6f98d-236">Is Indexed</span></span>             | <span data-ttu-id="6f98d-237">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-237">False</span></span>                                                  |
| <span data-ttu-id="6f98d-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6f98d-238">In Global Catalog</span></span>      | <span data-ttu-id="6f98d-239">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-239">False</span></span>                                                  |
| <span data-ttu-id="6f98d-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6f98d-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f98d-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6f98d-241">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="6f98d-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f98d-242">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="6f98d-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f98d-243">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="6f98d-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f98d-244">Search-Flags</span></span>           | <span data-ttu-id="6f98d-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f98d-245">0x00000000</span></span>                                             |
| <span data-ttu-id="6f98d-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f98d-246">System-Flags</span></span>           | <span data-ttu-id="6f98d-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f98d-247">0x00000010</span></span>                                             |
| <span data-ttu-id="6f98d-248">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6f98d-248">Classes used in</span></span>        | [<span data-ttu-id="6f98d-249">**NTDS-Verbindung**</span><span class="sxs-lookup"><span data-stu-id="6f98d-249">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6f98d-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6f98d-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6f98d-251">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6f98d-251">Entry</span></span> | <span data-ttu-id="6f98d-252">Wert</span><span class="sxs-lookup"><span data-stu-id="6f98d-252">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="6f98d-253">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6f98d-253">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6f98d-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f98d-254">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6f98d-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f98d-255">System-Only</span></span>            | <span data-ttu-id="6f98d-256">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-256">False</span></span>                                                  |
| <span data-ttu-id="6f98d-257">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6f98d-257">Is-Single-Valued</span></span>       | <span data-ttu-id="6f98d-258">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-258">False</span></span>                                                  |
| <span data-ttu-id="6f98d-259">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6f98d-259">Is Indexed</span></span>             | <span data-ttu-id="6f98d-260">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-260">False</span></span>                                                  |
| <span data-ttu-id="6f98d-261">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6f98d-261">In Global Catalog</span></span>      | <span data-ttu-id="6f98d-262">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-262">False</span></span>                                                  |
| <span data-ttu-id="6f98d-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6f98d-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f98d-264">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6f98d-264">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="6f98d-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f98d-265">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="6f98d-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f98d-266">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="6f98d-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f98d-267">Search-Flags</span></span>           | <span data-ttu-id="6f98d-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f98d-268">0x00000000</span></span>                                             |
| <span data-ttu-id="6f98d-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f98d-269">System-Flags</span></span>           | <span data-ttu-id="6f98d-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f98d-270">0x00000010</span></span>                                             |
| <span data-ttu-id="6f98d-271">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6f98d-271">Classes used in</span></span>        | [<span data-ttu-id="6f98d-272">**NTDS-Verbindung**</span><span class="sxs-lookup"><span data-stu-id="6f98d-272">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6f98d-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6f98d-273">Windows Server 2012</span></span>



| <span data-ttu-id="6f98d-274">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6f98d-274">Entry</span></span> | <span data-ttu-id="6f98d-275">Wert</span><span class="sxs-lookup"><span data-stu-id="6f98d-275">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="6f98d-276">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6f98d-276">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6f98d-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f98d-277">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6f98d-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f98d-278">System-Only</span></span>            | <span data-ttu-id="6f98d-279">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-279">False</span></span>                                                  |
| <span data-ttu-id="6f98d-280">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6f98d-280">Is-Single-Valued</span></span>       | <span data-ttu-id="6f98d-281">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-281">False</span></span>                                                  |
| <span data-ttu-id="6f98d-282">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6f98d-282">Is Indexed</span></span>             | <span data-ttu-id="6f98d-283">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-283">False</span></span>                                                  |
| <span data-ttu-id="6f98d-284">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6f98d-284">In Global Catalog</span></span>      | <span data-ttu-id="6f98d-285">False</span><span class="sxs-lookup"><span data-stu-id="6f98d-285">False</span></span>                                                  |
| <span data-ttu-id="6f98d-286">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6f98d-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f98d-287">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6f98d-287">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="6f98d-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f98d-288">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="6f98d-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f98d-289">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="6f98d-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f98d-290">Search-Flags</span></span>           | <span data-ttu-id="6f98d-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f98d-291">0x00000000</span></span>                                             |
| <span data-ttu-id="6f98d-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f98d-292">System-Flags</span></span>           | <span data-ttu-id="6f98d-293">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f98d-293">0x00000010</span></span>                                             |
| <span data-ttu-id="6f98d-294">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6f98d-294">Classes used in</span></span>        | [<span data-ttu-id="6f98d-295">**NTDS-Verbindung**</span><span class="sxs-lookup"><span data-stu-id="6f98d-295">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



 

 





