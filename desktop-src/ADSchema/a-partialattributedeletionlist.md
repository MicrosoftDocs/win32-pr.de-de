---
title: Attribut "Partial-Attribute-Lösch-List"
description: Verfolgt den internen Replikations Status von partiellen Replikaten (d. h. auf GCS). Attribut des partiellen Replikat-NC-Objekts. Wird verwendet, wenn der GC gerade Attribute aus den Objekten in seinen partiellen Replikat-NCS entfernt.
ms.assetid: 0084774b-7231-4cfc-8f60-c014006da2b9
ms.tgt_platform: multiple
keywords:
- "\"Partial-Attribute-Lösch-List\"-Attribut AD-Schema"
- "\"partialattributedeletionlist\"-Attribut, AD-Schema"
topic_type:
- apiref
api_name:
- Partial-Attribute-Deletion-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c2c6c0428d71dbba4199eeb441c838fb54a4463
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106341065"
---
# <a name="partial-attribute-deletion-list-attribute"></a><span data-ttu-id="4a6e2-107">Attribut "Partial-Attribute-Lösch-List"</span><span class="sxs-lookup"><span data-stu-id="4a6e2-107">Partial-Attribute-Deletion-List attribute</span></span>

<span data-ttu-id="4a6e2-108">Verfolgt den internen Replikations Status von partiellen Replikaten (d. h. auf GCS).</span><span class="sxs-lookup"><span data-stu-id="4a6e2-108">Tracks the internal replication state of partial replicas (that is, on GCs).</span></span> <span data-ttu-id="4a6e2-109">Attribut des partiellen Replikat-NC-Objekts.</span><span class="sxs-lookup"><span data-stu-id="4a6e2-109">Attribute of the partial replica NC object.</span></span> <span data-ttu-id="4a6e2-110">Wird verwendet, wenn der GC gerade Attribute aus den Objekten in seinen partiellen Replikat-NCS entfernt.</span><span class="sxs-lookup"><span data-stu-id="4a6e2-110">Used when the GC is in the process of removing attributes from the objects in its partial replica NCs.</span></span>



| <span data-ttu-id="4a6e2-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a6e2-111">Entry</span></span> | <span data-ttu-id="4a6e2-112">Wert</span><span class="sxs-lookup"><span data-stu-id="4a6e2-112">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="4a6e2-113">CN</span><span class="sxs-lookup"><span data-stu-id="4a6e2-113">CN</span></span>                | <span data-ttu-id="4a6e2-114">Partial-Attribute-löschen-List</span><span class="sxs-lookup"><span data-stu-id="4a6e2-114">Partial-Attribute-Deletion-List</span></span>                       |
| <span data-ttu-id="4a6e2-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4a6e2-115">Ldap-Display-Name</span></span> | <span data-ttu-id="4a6e2-116">partialattributedeletionlist</span><span class="sxs-lookup"><span data-stu-id="4a6e2-116">partialAttributeDeletionList</span></span>                          |
| <span data-ttu-id="4a6e2-117">Size</span><span class="sxs-lookup"><span data-stu-id="4a6e2-117">Size</span></span>              | \-                                                    |
| <span data-ttu-id="4a6e2-118">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="4a6e2-118">Update Privilege</span></span>  | <span data-ttu-id="4a6e2-119">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4a6e2-119">This value is set by the system.</span></span>                      |
| <span data-ttu-id="4a6e2-120">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="4a6e2-120">Update Frequency</span></span>  | <span data-ttu-id="4a6e2-121">Während der Replikation</span><span class="sxs-lookup"><span data-stu-id="4a6e2-121">During replication</span></span>                                    |
| <span data-ttu-id="4a6e2-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4a6e2-122">Attribute-Id</span></span>      | <span data-ttu-id="4a6e2-123">1.2.840.113556.1.4.663</span><span class="sxs-lookup"><span data-stu-id="4a6e2-123">1.2.840.113556.1.4.663</span></span>                                |
| <span data-ttu-id="4a6e2-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4a6e2-124">System-Id-Guid</span></span>    | <span data-ttu-id="4a6e2-125">28630ec0-41d5-11d1-a9c1-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="4a6e2-125">28630ec0-41d5-11d1-a9c1-0000f80367c1</span></span>                  |
| <span data-ttu-id="4a6e2-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a6e2-126">Syntax</span></span>            | [<span data-ttu-id="4a6e2-127">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="4a6e2-127">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="4a6e2-128">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="4a6e2-128">Implementations</span></span>

-   [<span data-ttu-id="4a6e2-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4a6e2-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4a6e2-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4a6e2-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4a6e2-131">**Adam**</span><span class="sxs-lookup"><span data-stu-id="4a6e2-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="4a6e2-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4a6e2-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4a6e2-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4a6e2-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4a6e2-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4a6e2-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4a6e2-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4a6e2-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4a6e2-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4a6e2-136">Windows 2000 Server</span></span>



| <span data-ttu-id="4a6e2-137">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a6e2-137">Entry</span></span> | <span data-ttu-id="4a6e2-138">Wert</span><span class="sxs-lookup"><span data-stu-id="4a6e2-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4a6e2-139">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4a6e2-139">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4a6e2-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a6e2-140">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="4a6e2-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a6e2-141">System-Only</span></span>            | <span data-ttu-id="4a6e2-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-142">True</span></span>                            |
| <span data-ttu-id="4a6e2-143">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-143">Is-Single-Valued</span></span>       | <span data-ttu-id="4a6e2-144">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-144">True</span></span>                            |
| <span data-ttu-id="4a6e2-145">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4a6e2-145">Is Indexed</span></span>             | <span data-ttu-id="4a6e2-146">False</span><span class="sxs-lookup"><span data-stu-id="4a6e2-146">False</span></span>                           |
| <span data-ttu-id="4a6e2-147">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4a6e2-147">In Global Catalog</span></span>      | <span data-ttu-id="4a6e2-148">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-148">True</span></span>                            |
| <span data-ttu-id="4a6e2-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a6e2-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a6e2-150">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4a6e2-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4a6e2-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a6e2-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4a6e2-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a6e2-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4a6e2-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a6e2-153">Search-Flags</span></span>           | <span data-ttu-id="4a6e2-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a6e2-154">0x00000000</span></span>                      |
| <span data-ttu-id="4a6e2-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a6e2-155">System-Flags</span></span>           | <span data-ttu-id="4a6e2-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="4a6e2-156">0x00000013</span></span>                      |
| <span data-ttu-id="4a6e2-157">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4a6e2-157">Classes used in</span></span>        | [<span data-ttu-id="4a6e2-158">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="4a6e2-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4a6e2-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4a6e2-159">Windows Server 2003</span></span>



| <span data-ttu-id="4a6e2-160">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a6e2-160">Entry</span></span> | <span data-ttu-id="4a6e2-161">Wert</span><span class="sxs-lookup"><span data-stu-id="4a6e2-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4a6e2-162">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4a6e2-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4a6e2-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a6e2-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="4a6e2-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a6e2-164">System-Only</span></span>            | <span data-ttu-id="4a6e2-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-165">True</span></span>                            |
| <span data-ttu-id="4a6e2-166">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-166">Is-Single-Valued</span></span>       | <span data-ttu-id="4a6e2-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-167">True</span></span>                            |
| <span data-ttu-id="4a6e2-168">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4a6e2-168">Is Indexed</span></span>             | <span data-ttu-id="4a6e2-169">False</span><span class="sxs-lookup"><span data-stu-id="4a6e2-169">False</span></span>                           |
| <span data-ttu-id="4a6e2-170">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4a6e2-170">In Global Catalog</span></span>      | <span data-ttu-id="4a6e2-171">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-171">True</span></span>                            |
| <span data-ttu-id="4a6e2-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a6e2-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a6e2-173">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4a6e2-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4a6e2-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a6e2-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4a6e2-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a6e2-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4a6e2-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a6e2-176">Search-Flags</span></span>           | <span data-ttu-id="4a6e2-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a6e2-177">0x00000000</span></span>                      |
| <span data-ttu-id="4a6e2-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a6e2-178">System-Flags</span></span>           | <span data-ttu-id="4a6e2-179">0x00000013</span><span class="sxs-lookup"><span data-stu-id="4a6e2-179">0x00000013</span></span>                      |
| <span data-ttu-id="4a6e2-180">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4a6e2-180">Classes used in</span></span>        | [<span data-ttu-id="4a6e2-181">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="4a6e2-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="4a6e2-182">Adam</span><span class="sxs-lookup"><span data-stu-id="4a6e2-182">ADAM</span></span>



| <span data-ttu-id="4a6e2-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a6e2-183">Entry</span></span> | <span data-ttu-id="4a6e2-184">Wert</span><span class="sxs-lookup"><span data-stu-id="4a6e2-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4a6e2-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4a6e2-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4a6e2-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a6e2-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="4a6e2-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a6e2-187">System-Only</span></span>            | <span data-ttu-id="4a6e2-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-188">True</span></span>                            |
| <span data-ttu-id="4a6e2-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-189">Is-Single-Valued</span></span>       | <span data-ttu-id="4a6e2-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-190">True</span></span>                            |
| <span data-ttu-id="4a6e2-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4a6e2-191">Is Indexed</span></span>             | <span data-ttu-id="4a6e2-192">False</span><span class="sxs-lookup"><span data-stu-id="4a6e2-192">False</span></span>                           |
| <span data-ttu-id="4a6e2-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4a6e2-193">In Global Catalog</span></span>      | <span data-ttu-id="4a6e2-194">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-194">True</span></span>                            |
| <span data-ttu-id="4a6e2-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a6e2-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a6e2-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4a6e2-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4a6e2-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a6e2-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4a6e2-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a6e2-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4a6e2-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a6e2-199">Search-Flags</span></span>           | <span data-ttu-id="4a6e2-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a6e2-200">0x00000000</span></span>                      |
| <span data-ttu-id="4a6e2-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a6e2-201">System-Flags</span></span>           | <span data-ttu-id="4a6e2-202">0x00000013</span><span class="sxs-lookup"><span data-stu-id="4a6e2-202">0x00000013</span></span>                      |
| <span data-ttu-id="4a6e2-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4a6e2-203">Classes used in</span></span>        | [<span data-ttu-id="4a6e2-204">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="4a6e2-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4a6e2-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4a6e2-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4a6e2-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a6e2-206">Entry</span></span> | <span data-ttu-id="4a6e2-207">Wert</span><span class="sxs-lookup"><span data-stu-id="4a6e2-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4a6e2-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4a6e2-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4a6e2-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a6e2-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="4a6e2-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a6e2-210">System-Only</span></span>            | <span data-ttu-id="4a6e2-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-211">True</span></span>                            |
| <span data-ttu-id="4a6e2-212">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-212">Is-Single-Valued</span></span>       | <span data-ttu-id="4a6e2-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-213">True</span></span>                            |
| <span data-ttu-id="4a6e2-214">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4a6e2-214">Is Indexed</span></span>             | <span data-ttu-id="4a6e2-215">False</span><span class="sxs-lookup"><span data-stu-id="4a6e2-215">False</span></span>                           |
| <span data-ttu-id="4a6e2-216">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4a6e2-216">In Global Catalog</span></span>      | <span data-ttu-id="4a6e2-217">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-217">True</span></span>                            |
| <span data-ttu-id="4a6e2-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a6e2-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a6e2-219">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4a6e2-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4a6e2-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a6e2-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4a6e2-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a6e2-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4a6e2-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a6e2-222">Search-Flags</span></span>           | <span data-ttu-id="4a6e2-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a6e2-223">0x00000000</span></span>                      |
| <span data-ttu-id="4a6e2-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a6e2-224">System-Flags</span></span>           | <span data-ttu-id="4a6e2-225">0x00000013</span><span class="sxs-lookup"><span data-stu-id="4a6e2-225">0x00000013</span></span>                      |
| <span data-ttu-id="4a6e2-226">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4a6e2-226">Classes used in</span></span>        | [<span data-ttu-id="4a6e2-227">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="4a6e2-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4a6e2-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a6e2-228">Windows Server 2008</span></span>



| <span data-ttu-id="4a6e2-229">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a6e2-229">Entry</span></span> | <span data-ttu-id="4a6e2-230">Wert</span><span class="sxs-lookup"><span data-stu-id="4a6e2-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4a6e2-231">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4a6e2-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4a6e2-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a6e2-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="4a6e2-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a6e2-233">System-Only</span></span>            | <span data-ttu-id="4a6e2-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-234">True</span></span>                            |
| <span data-ttu-id="4a6e2-235">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-235">Is-Single-Valued</span></span>       | <span data-ttu-id="4a6e2-236">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-236">True</span></span>                            |
| <span data-ttu-id="4a6e2-237">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4a6e2-237">Is Indexed</span></span>             | <span data-ttu-id="4a6e2-238">False</span><span class="sxs-lookup"><span data-stu-id="4a6e2-238">False</span></span>                           |
| <span data-ttu-id="4a6e2-239">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4a6e2-239">In Global Catalog</span></span>      | <span data-ttu-id="4a6e2-240">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-240">True</span></span>                            |
| <span data-ttu-id="4a6e2-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a6e2-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a6e2-242">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4a6e2-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4a6e2-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a6e2-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4a6e2-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a6e2-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4a6e2-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a6e2-245">Search-Flags</span></span>           | <span data-ttu-id="4a6e2-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a6e2-246">0x00000000</span></span>                      |
| <span data-ttu-id="4a6e2-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a6e2-247">System-Flags</span></span>           | <span data-ttu-id="4a6e2-248">0x00000013</span><span class="sxs-lookup"><span data-stu-id="4a6e2-248">0x00000013</span></span>                      |
| <span data-ttu-id="4a6e2-249">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4a6e2-249">Classes used in</span></span>        | [<span data-ttu-id="4a6e2-250">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="4a6e2-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4a6e2-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4a6e2-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4a6e2-252">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a6e2-252">Entry</span></span> | <span data-ttu-id="4a6e2-253">Wert</span><span class="sxs-lookup"><span data-stu-id="4a6e2-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4a6e2-254">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4a6e2-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4a6e2-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a6e2-255">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="4a6e2-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a6e2-256">System-Only</span></span>            | <span data-ttu-id="4a6e2-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-257">True</span></span>                            |
| <span data-ttu-id="4a6e2-258">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-258">Is-Single-Valued</span></span>       | <span data-ttu-id="4a6e2-259">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-259">True</span></span>                            |
| <span data-ttu-id="4a6e2-260">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4a6e2-260">Is Indexed</span></span>             | <span data-ttu-id="4a6e2-261">False</span><span class="sxs-lookup"><span data-stu-id="4a6e2-261">False</span></span>                           |
| <span data-ttu-id="4a6e2-262">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4a6e2-262">In Global Catalog</span></span>      | <span data-ttu-id="4a6e2-263">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-263">True</span></span>                            |
| <span data-ttu-id="4a6e2-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a6e2-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a6e2-265">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4a6e2-265">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4a6e2-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a6e2-266">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4a6e2-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a6e2-267">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4a6e2-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a6e2-268">Search-Flags</span></span>           | <span data-ttu-id="4a6e2-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a6e2-269">0x00000000</span></span>                      |
| <span data-ttu-id="4a6e2-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a6e2-270">System-Flags</span></span>           | <span data-ttu-id="4a6e2-271">0x00000013</span><span class="sxs-lookup"><span data-stu-id="4a6e2-271">0x00000013</span></span>                      |
| <span data-ttu-id="4a6e2-272">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4a6e2-272">Classes used in</span></span>        | [<span data-ttu-id="4a6e2-273">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="4a6e2-273">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4a6e2-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4a6e2-274">Windows Server 2012</span></span>



| <span data-ttu-id="4a6e2-275">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a6e2-275">Entry</span></span> | <span data-ttu-id="4a6e2-276">Wert</span><span class="sxs-lookup"><span data-stu-id="4a6e2-276">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4a6e2-277">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4a6e2-277">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4a6e2-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a6e2-278">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="4a6e2-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a6e2-279">System-Only</span></span>            | <span data-ttu-id="4a6e2-280">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-280">True</span></span>                            |
| <span data-ttu-id="4a6e2-281">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-281">Is-Single-Valued</span></span>       | <span data-ttu-id="4a6e2-282">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-282">True</span></span>                            |
| <span data-ttu-id="4a6e2-283">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4a6e2-283">Is Indexed</span></span>             | <span data-ttu-id="4a6e2-284">False</span><span class="sxs-lookup"><span data-stu-id="4a6e2-284">False</span></span>                           |
| <span data-ttu-id="4a6e2-285">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4a6e2-285">In Global Catalog</span></span>      | <span data-ttu-id="4a6e2-286">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a6e2-286">True</span></span>                            |
| <span data-ttu-id="4a6e2-287">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a6e2-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a6e2-288">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4a6e2-288">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4a6e2-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a6e2-289">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4a6e2-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a6e2-290">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4a6e2-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a6e2-291">Search-Flags</span></span>           | <span data-ttu-id="4a6e2-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a6e2-292">0x00000000</span></span>                      |
| <span data-ttu-id="4a6e2-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a6e2-293">System-Flags</span></span>           | <span data-ttu-id="4a6e2-294">0x00000013</span><span class="sxs-lookup"><span data-stu-id="4a6e2-294">0x00000013</span></span>                      |
| <span data-ttu-id="4a6e2-295">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4a6e2-295">Classes used in</span></span>        | [<span data-ttu-id="4a6e2-296">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="4a6e2-296">**Top**</span></span>](c-top.md)<br/> |



 

 





