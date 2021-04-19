---
title: Attribut "Partial-Attribute-Set"
description: Verfolgt den internen Replikations Status von partiellen Replikaten (d. h. auf GCS). Attribut des partiellen Replikat-NC-Objekts. Definiert den Satz von Attributen, die auf einem bestimmten partiellen Replikat-NC vorhanden sind
ms.assetid: 2840d2b7-e186-4ef2-9107-f1e5c0c2f760
ms.tgt_platform: multiple
keywords:
- AD-Schema für partielle Attribut Attribut Satz
- AD-Schema des partialattributeset-Attributs
topic_type:
- apiref
api_name:
- Partial-Attribute-Set
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e932c07b0d4a8e3ea8f30f504194093d61912b7b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106343100"
---
# <a name="partial-attribute-set-attribute"></a><span data-ttu-id="b3bbb-107">Attribut "Partial-Attribute-Set"</span><span class="sxs-lookup"><span data-stu-id="b3bbb-107">Partial-Attribute-Set attribute</span></span>

<span data-ttu-id="b3bbb-108">Verfolgt den internen Replikations Status von partiellen Replikaten (d. h. auf GCS).</span><span class="sxs-lookup"><span data-stu-id="b3bbb-108">Tracks the internal replication state of partial replicas (that is, on GCs).</span></span> <span data-ttu-id="b3bbb-109">Attribut des partiellen Replikat-NC-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b3bbb-109">Attribute of the partial replica NC object.</span></span> <span data-ttu-id="b3bbb-110">Definiert den Satz von Attributen, die auf einem bestimmten partiellen Replikat-NC vorhanden sind</span><span class="sxs-lookup"><span data-stu-id="b3bbb-110">Defines the set of attributes present on a particular partial replica NC.</span></span>



| <span data-ttu-id="b3bbb-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b3bbb-111">Entry</span></span> | <span data-ttu-id="b3bbb-112">Wert</span><span class="sxs-lookup"><span data-stu-id="b3bbb-112">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="b3bbb-113">CN</span><span class="sxs-lookup"><span data-stu-id="b3bbb-113">CN</span></span>                | <span data-ttu-id="b3bbb-114">Partiell-Attribut Satz</span><span class="sxs-lookup"><span data-stu-id="b3bbb-114">Partial-Attribute-Set</span></span>                                 |
| <span data-ttu-id="b3bbb-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b3bbb-115">Ldap-Display-Name</span></span> | <span data-ttu-id="b3bbb-116">partialattributeset</span><span class="sxs-lookup"><span data-stu-id="b3bbb-116">partialAttributeSet</span></span>                                   |
| <span data-ttu-id="b3bbb-117">Size</span><span class="sxs-lookup"><span data-stu-id="b3bbb-117">Size</span></span>              | \-                                                    |
| <span data-ttu-id="b3bbb-118">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b3bbb-118">Update Privilege</span></span>  | <span data-ttu-id="b3bbb-119">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b3bbb-119">This value is set by the system.</span></span>                      |
| <span data-ttu-id="b3bbb-120">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="b3bbb-120">Update Frequency</span></span>  | <span data-ttu-id="b3bbb-121">Während der Replikation</span><span class="sxs-lookup"><span data-stu-id="b3bbb-121">During replication</span></span>                                    |
| <span data-ttu-id="b3bbb-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b3bbb-122">Attribute-Id</span></span>      | <span data-ttu-id="b3bbb-123">1.2.840.113556.1.4.640</span><span class="sxs-lookup"><span data-stu-id="b3bbb-123">1.2.840.113556.1.4.640</span></span>                                |
| <span data-ttu-id="b3bbb-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b3bbb-124">System-Id-Guid</span></span>    | <span data-ttu-id="b3bbb-125">19405b9e-3cfa-11d1-a9c0-0000f 80367c1</span><span class="sxs-lookup"><span data-stu-id="b3bbb-125">19405b9e-3cfa-11d1-a9c0-0000f80367c1</span></span>                  |
| <span data-ttu-id="b3bbb-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3bbb-126">Syntax</span></span>            | [<span data-ttu-id="b3bbb-127">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-127">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="b3bbb-128">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="b3bbb-128">Implementations</span></span>

-   [<span data-ttu-id="b3bbb-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b3bbb-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b3bbb-131">**Adam**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b3bbb-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b3bbb-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b3bbb-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b3bbb-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b3bbb-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b3bbb-136">Windows 2000 Server</span></span>



| <span data-ttu-id="b3bbb-137">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b3bbb-137">Entry</span></span> | <span data-ttu-id="b3bbb-138">Wert</span><span class="sxs-lookup"><span data-stu-id="b3bbb-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b3bbb-139">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b3bbb-139">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b3bbb-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3bbb-140">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b3bbb-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3bbb-141">System-Only</span></span>            | <span data-ttu-id="b3bbb-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-142">True</span></span>                            |
| <span data-ttu-id="b3bbb-143">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-143">Is-Single-Valued</span></span>       | <span data-ttu-id="b3bbb-144">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-144">True</span></span>                            |
| <span data-ttu-id="b3bbb-145">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b3bbb-145">Is Indexed</span></span>             | <span data-ttu-id="b3bbb-146">False</span><span class="sxs-lookup"><span data-stu-id="b3bbb-146">False</span></span>                           |
| <span data-ttu-id="b3bbb-147">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b3bbb-147">In Global Catalog</span></span>      | <span data-ttu-id="b3bbb-148">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-148">True</span></span>                            |
| <span data-ttu-id="b3bbb-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b3bbb-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3bbb-150">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b3bbb-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b3bbb-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3bbb-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b3bbb-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3bbb-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b3bbb-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3bbb-153">Search-Flags</span></span>           | <span data-ttu-id="b3bbb-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3bbb-154">0x00000000</span></span>                      |
| <span data-ttu-id="b3bbb-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3bbb-155">System-Flags</span></span>           | <span data-ttu-id="b3bbb-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b3bbb-156">0x00000013</span></span>                      |
| <span data-ttu-id="b3bbb-157">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b3bbb-157">Classes used in</span></span>        | [<span data-ttu-id="b3bbb-158">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b3bbb-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b3bbb-159">Windows Server 2003</span></span>



| <span data-ttu-id="b3bbb-160">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b3bbb-160">Entry</span></span> | <span data-ttu-id="b3bbb-161">Wert</span><span class="sxs-lookup"><span data-stu-id="b3bbb-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b3bbb-162">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b3bbb-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b3bbb-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3bbb-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b3bbb-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3bbb-164">System-Only</span></span>            | <span data-ttu-id="b3bbb-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-165">True</span></span>                            |
| <span data-ttu-id="b3bbb-166">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-166">Is-Single-Valued</span></span>       | <span data-ttu-id="b3bbb-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-167">True</span></span>                            |
| <span data-ttu-id="b3bbb-168">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b3bbb-168">Is Indexed</span></span>             | <span data-ttu-id="b3bbb-169">False</span><span class="sxs-lookup"><span data-stu-id="b3bbb-169">False</span></span>                           |
| <span data-ttu-id="b3bbb-170">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b3bbb-170">In Global Catalog</span></span>      | <span data-ttu-id="b3bbb-171">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-171">True</span></span>                            |
| <span data-ttu-id="b3bbb-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b3bbb-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3bbb-173">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b3bbb-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b3bbb-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3bbb-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b3bbb-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3bbb-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b3bbb-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3bbb-176">Search-Flags</span></span>           | <span data-ttu-id="b3bbb-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3bbb-177">0x00000000</span></span>                      |
| <span data-ttu-id="b3bbb-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3bbb-178">System-Flags</span></span>           | <span data-ttu-id="b3bbb-179">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b3bbb-179">0x00000013</span></span>                      |
| <span data-ttu-id="b3bbb-180">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b3bbb-180">Classes used in</span></span>        | [<span data-ttu-id="b3bbb-181">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b3bbb-182">Adam</span><span class="sxs-lookup"><span data-stu-id="b3bbb-182">ADAM</span></span>



| <span data-ttu-id="b3bbb-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b3bbb-183">Entry</span></span> | <span data-ttu-id="b3bbb-184">Wert</span><span class="sxs-lookup"><span data-stu-id="b3bbb-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b3bbb-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b3bbb-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b3bbb-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3bbb-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b3bbb-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3bbb-187">System-Only</span></span>            | <span data-ttu-id="b3bbb-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-188">True</span></span>                            |
| <span data-ttu-id="b3bbb-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-189">Is-Single-Valued</span></span>       | <span data-ttu-id="b3bbb-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-190">True</span></span>                            |
| <span data-ttu-id="b3bbb-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b3bbb-191">Is Indexed</span></span>             | <span data-ttu-id="b3bbb-192">False</span><span class="sxs-lookup"><span data-stu-id="b3bbb-192">False</span></span>                           |
| <span data-ttu-id="b3bbb-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b3bbb-193">In Global Catalog</span></span>      | <span data-ttu-id="b3bbb-194">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-194">True</span></span>                            |
| <span data-ttu-id="b3bbb-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b3bbb-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3bbb-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b3bbb-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b3bbb-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3bbb-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b3bbb-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3bbb-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b3bbb-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3bbb-199">Search-Flags</span></span>           | <span data-ttu-id="b3bbb-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3bbb-200">0x00000000</span></span>                      |
| <span data-ttu-id="b3bbb-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3bbb-201">System-Flags</span></span>           | <span data-ttu-id="b3bbb-202">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b3bbb-202">0x00000013</span></span>                      |
| <span data-ttu-id="b3bbb-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b3bbb-203">Classes used in</span></span>        | [<span data-ttu-id="b3bbb-204">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b3bbb-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b3bbb-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b3bbb-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b3bbb-206">Entry</span></span> | <span data-ttu-id="b3bbb-207">Wert</span><span class="sxs-lookup"><span data-stu-id="b3bbb-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b3bbb-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b3bbb-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b3bbb-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3bbb-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b3bbb-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3bbb-210">System-Only</span></span>            | <span data-ttu-id="b3bbb-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-211">True</span></span>                            |
| <span data-ttu-id="b3bbb-212">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-212">Is-Single-Valued</span></span>       | <span data-ttu-id="b3bbb-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-213">True</span></span>                            |
| <span data-ttu-id="b3bbb-214">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b3bbb-214">Is Indexed</span></span>             | <span data-ttu-id="b3bbb-215">False</span><span class="sxs-lookup"><span data-stu-id="b3bbb-215">False</span></span>                           |
| <span data-ttu-id="b3bbb-216">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b3bbb-216">In Global Catalog</span></span>      | <span data-ttu-id="b3bbb-217">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-217">True</span></span>                            |
| <span data-ttu-id="b3bbb-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b3bbb-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3bbb-219">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b3bbb-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b3bbb-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3bbb-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b3bbb-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3bbb-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b3bbb-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3bbb-222">Search-Flags</span></span>           | <span data-ttu-id="b3bbb-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3bbb-223">0x00000000</span></span>                      |
| <span data-ttu-id="b3bbb-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3bbb-224">System-Flags</span></span>           | <span data-ttu-id="b3bbb-225">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b3bbb-225">0x00000013</span></span>                      |
| <span data-ttu-id="b3bbb-226">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b3bbb-226">Classes used in</span></span>        | [<span data-ttu-id="b3bbb-227">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b3bbb-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3bbb-228">Windows Server 2008</span></span>



| <span data-ttu-id="b3bbb-229">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b3bbb-229">Entry</span></span> | <span data-ttu-id="b3bbb-230">Wert</span><span class="sxs-lookup"><span data-stu-id="b3bbb-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b3bbb-231">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b3bbb-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b3bbb-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3bbb-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b3bbb-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3bbb-233">System-Only</span></span>            | <span data-ttu-id="b3bbb-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-234">True</span></span>                            |
| <span data-ttu-id="b3bbb-235">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-235">Is-Single-Valued</span></span>       | <span data-ttu-id="b3bbb-236">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-236">True</span></span>                            |
| <span data-ttu-id="b3bbb-237">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b3bbb-237">Is Indexed</span></span>             | <span data-ttu-id="b3bbb-238">False</span><span class="sxs-lookup"><span data-stu-id="b3bbb-238">False</span></span>                           |
| <span data-ttu-id="b3bbb-239">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b3bbb-239">In Global Catalog</span></span>      | <span data-ttu-id="b3bbb-240">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-240">True</span></span>                            |
| <span data-ttu-id="b3bbb-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b3bbb-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3bbb-242">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b3bbb-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b3bbb-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3bbb-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b3bbb-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3bbb-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b3bbb-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3bbb-245">Search-Flags</span></span>           | <span data-ttu-id="b3bbb-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3bbb-246">0x00000000</span></span>                      |
| <span data-ttu-id="b3bbb-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3bbb-247">System-Flags</span></span>           | <span data-ttu-id="b3bbb-248">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b3bbb-248">0x00000013</span></span>                      |
| <span data-ttu-id="b3bbb-249">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b3bbb-249">Classes used in</span></span>        | [<span data-ttu-id="b3bbb-250">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b3bbb-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b3bbb-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b3bbb-252">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b3bbb-252">Entry</span></span> | <span data-ttu-id="b3bbb-253">Wert</span><span class="sxs-lookup"><span data-stu-id="b3bbb-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b3bbb-254">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b3bbb-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b3bbb-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3bbb-255">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b3bbb-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3bbb-256">System-Only</span></span>            | <span data-ttu-id="b3bbb-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-257">True</span></span>                            |
| <span data-ttu-id="b3bbb-258">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-258">Is-Single-Valued</span></span>       | <span data-ttu-id="b3bbb-259">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-259">True</span></span>                            |
| <span data-ttu-id="b3bbb-260">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b3bbb-260">Is Indexed</span></span>             | <span data-ttu-id="b3bbb-261">False</span><span class="sxs-lookup"><span data-stu-id="b3bbb-261">False</span></span>                           |
| <span data-ttu-id="b3bbb-262">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b3bbb-262">In Global Catalog</span></span>      | <span data-ttu-id="b3bbb-263">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-263">True</span></span>                            |
| <span data-ttu-id="b3bbb-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b3bbb-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3bbb-265">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b3bbb-265">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b3bbb-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3bbb-266">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b3bbb-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3bbb-267">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b3bbb-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3bbb-268">Search-Flags</span></span>           | <span data-ttu-id="b3bbb-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3bbb-269">0x00000000</span></span>                      |
| <span data-ttu-id="b3bbb-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3bbb-270">System-Flags</span></span>           | <span data-ttu-id="b3bbb-271">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b3bbb-271">0x00000013</span></span>                      |
| <span data-ttu-id="b3bbb-272">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b3bbb-272">Classes used in</span></span>        | [<span data-ttu-id="b3bbb-273">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-273">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b3bbb-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b3bbb-274">Windows Server 2012</span></span>



| <span data-ttu-id="b3bbb-275">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b3bbb-275">Entry</span></span> | <span data-ttu-id="b3bbb-276">Wert</span><span class="sxs-lookup"><span data-stu-id="b3bbb-276">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b3bbb-277">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b3bbb-277">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b3bbb-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3bbb-278">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b3bbb-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3bbb-279">System-Only</span></span>            | <span data-ttu-id="b3bbb-280">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-280">True</span></span>                            |
| <span data-ttu-id="b3bbb-281">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-281">Is-Single-Valued</span></span>       | <span data-ttu-id="b3bbb-282">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-282">True</span></span>                            |
| <span data-ttu-id="b3bbb-283">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b3bbb-283">Is Indexed</span></span>             | <span data-ttu-id="b3bbb-284">False</span><span class="sxs-lookup"><span data-stu-id="b3bbb-284">False</span></span>                           |
| <span data-ttu-id="b3bbb-285">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b3bbb-285">In Global Catalog</span></span>      | <span data-ttu-id="b3bbb-286">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3bbb-286">True</span></span>                            |
| <span data-ttu-id="b3bbb-287">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b3bbb-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3bbb-288">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b3bbb-288">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b3bbb-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3bbb-289">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b3bbb-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3bbb-290">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b3bbb-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3bbb-291">Search-Flags</span></span>           | <span data-ttu-id="b3bbb-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3bbb-292">0x00000000</span></span>                      |
| <span data-ttu-id="b3bbb-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3bbb-293">System-Flags</span></span>           | <span data-ttu-id="b3bbb-294">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b3bbb-294">0x00000013</span></span>                      |
| <span data-ttu-id="b3bbb-295">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b3bbb-295">Classes used in</span></span>        | [<span data-ttu-id="b3bbb-296">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-296">**Top**</span></span>](c-top.md)<br/> |



 

 





