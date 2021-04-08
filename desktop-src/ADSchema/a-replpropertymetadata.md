---
title: REPL-Property-Meta-Data-Attribut
description: Verfolgt interne Replikations Zustandsinformationen für DS-Objekte. Informationen können Sie im öffentlichen Format über die öffentliche API dsreplicagetinfo () extrahieren. Auf allen DS-Objekten vorhanden.
ms.assetid: 5776208c-8138-4b0a-855a-8bddcbd2e532
ms.tgt_platform: multiple
keywords:
- REPL-Property-Meta-Data-Attribut, AD-Schema
- replpropertymetadata-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Repl-Property-Meta-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7639d9bca600457d519862e1f57d9ee698d2a155
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744905"
---
# <a name="repl-property-meta-data-attribute"></a><span data-ttu-id="0546c-107">REPL-Property-Meta-Data-Attribut</span><span class="sxs-lookup"><span data-stu-id="0546c-107">Repl-Property-Meta-Data attribute</span></span>

<span data-ttu-id="0546c-108">Verfolgt interne Replikations Zustandsinformationen für DS-Objekte.</span><span class="sxs-lookup"><span data-stu-id="0546c-108">Tracks internal replication state information for DS objects.</span></span> <span data-ttu-id="0546c-109">Informationen können Sie im öffentlichen Format über die öffentliche API dsreplicagetinfo () extrahieren.</span><span class="sxs-lookup"><span data-stu-id="0546c-109">Information here can be extracted in public form through the public API DsReplicaGetInfo().</span></span> <span data-ttu-id="0546c-110">Auf allen DS-Objekten vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0546c-110">Present on all DS objects.</span></span>



| <span data-ttu-id="0546c-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0546c-111">Entry</span></span> | <span data-ttu-id="0546c-112">Wert</span><span class="sxs-lookup"><span data-stu-id="0546c-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0546c-113">CN</span><span class="sxs-lookup"><span data-stu-id="0546c-113">CN</span></span>                | <span data-ttu-id="0546c-114">REPL-Property-Meta-Data</span><span class="sxs-lookup"><span data-stu-id="0546c-114">Repl-Property-Meta-Data</span></span>                                                      |
| <span data-ttu-id="0546c-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0546c-115">Ldap-Display-Name</span></span> | <span data-ttu-id="0546c-116">replpropertymetadata</span><span class="sxs-lookup"><span data-stu-id="0546c-116">replPropertyMetaData</span></span>                                                         |
| <span data-ttu-id="0546c-117">Size</span><span class="sxs-lookup"><span data-stu-id="0546c-117">Size</span></span>              | <span data-ttu-id="0546c-118">Die Länge ist proportional zur Anzahl der replizierbaren Attribute für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="0546c-118">Length is proportional to the number of replicable attributes on the object.</span></span> |
| <span data-ttu-id="0546c-119">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="0546c-119">Update Privilege</span></span>  | <span data-ttu-id="0546c-120">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0546c-120">This value is set by the system.</span></span>                                             |
| <span data-ttu-id="0546c-121">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="0546c-121">Update Frequency</span></span>  | <span data-ttu-id="0546c-122">Änderungen in Reaktion auf replizierende Änderungen im-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0546c-122">Changes in response to any replicating changes in the object.</span></span>                |
| <span data-ttu-id="0546c-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0546c-123">Attribute-Id</span></span>      | <span data-ttu-id="0546c-124">1.2.840.113556.1.4.3</span><span class="sxs-lookup"><span data-stu-id="0546c-124">1.2.840.113556.1.4.3</span></span>                                                         |
| <span data-ttu-id="0546c-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0546c-125">System-Id-Guid</span></span>    | <span data-ttu-id="0546c-126">281416c0-1968-11D0-a28f -00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="0546c-126">281416c0-1968-11d0-a28f-00aa003049e2</span></span>                                         |
| <span data-ttu-id="0546c-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="0546c-127">Syntax</span></span>            | [<span data-ttu-id="0546c-128">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="0546c-128">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                        |



## <a name="implementations"></a><span data-ttu-id="0546c-129">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="0546c-129">Implementations</span></span>

-   [<span data-ttu-id="0546c-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0546c-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0546c-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0546c-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0546c-132">**Adam**</span><span class="sxs-lookup"><span data-stu-id="0546c-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="0546c-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0546c-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0546c-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0546c-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0546c-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0546c-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0546c-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0546c-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0546c-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0546c-137">Windows 2000 Server</span></span>



| <span data-ttu-id="0546c-138">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0546c-138">Entry</span></span> | <span data-ttu-id="0546c-139">Wert</span><span class="sxs-lookup"><span data-stu-id="0546c-139">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0546c-140">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0546c-140">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0546c-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0546c-141">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0546c-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="0546c-142">System-Only</span></span>            | <span data-ttu-id="0546c-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="0546c-143">True</span></span>                            |
| <span data-ttu-id="0546c-144">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0546c-144">Is-Single-Valued</span></span>       | <span data-ttu-id="0546c-145">Richtig</span><span class="sxs-lookup"><span data-stu-id="0546c-145">True</span></span>                            |
| <span data-ttu-id="0546c-146">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0546c-146">Is Indexed</span></span>             | <span data-ttu-id="0546c-147">False</span><span class="sxs-lookup"><span data-stu-id="0546c-147">False</span></span>                           |
| <span data-ttu-id="0546c-148">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0546c-148">In Global Catalog</span></span>      | <span data-ttu-id="0546c-149">Richtig</span><span class="sxs-lookup"><span data-stu-id="0546c-149">True</span></span>                            |
| <span data-ttu-id="0546c-150">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0546c-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="0546c-151">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0546c-151">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0546c-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0546c-152">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0546c-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0546c-153">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0546c-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0546c-154">Search-Flags</span></span>           | <span data-ttu-id="0546c-155">0x00000008</span><span class="sxs-lookup"><span data-stu-id="0546c-155">0x00000008</span></span>                      |
| <span data-ttu-id="0546c-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0546c-156">System-Flags</span></span>           | <span data-ttu-id="0546c-157">0x00000013</span><span class="sxs-lookup"><span data-stu-id="0546c-157">0x00000013</span></span>                      |
| <span data-ttu-id="0546c-158">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0546c-158">Classes used in</span></span>        | [<span data-ttu-id="0546c-159">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="0546c-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0546c-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0546c-160">Windows Server 2003</span></span>



| <span data-ttu-id="0546c-161">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0546c-161">Entry</span></span> | <span data-ttu-id="0546c-162">Wert</span><span class="sxs-lookup"><span data-stu-id="0546c-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0546c-163">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0546c-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0546c-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0546c-164">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0546c-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="0546c-165">System-Only</span></span>            | <span data-ttu-id="0546c-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="0546c-166">True</span></span>                            |
| <span data-ttu-id="0546c-167">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0546c-167">Is-Single-Valued</span></span>       | <span data-ttu-id="0546c-168">Richtig</span><span class="sxs-lookup"><span data-stu-id="0546c-168">True</span></span>                            |
| <span data-ttu-id="0546c-169">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0546c-169">Is Indexed</span></span>             | <span data-ttu-id="0546c-170">False</span><span class="sxs-lookup"><span data-stu-id="0546c-170">False</span></span>                           |
| <span data-ttu-id="0546c-171">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0546c-171">In Global Catalog</span></span>      | <span data-ttu-id="0546c-172">Richtig</span><span class="sxs-lookup"><span data-stu-id="0546c-172">True</span></span>                            |
| <span data-ttu-id="0546c-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0546c-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="0546c-174">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0546c-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0546c-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0546c-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0546c-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0546c-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0546c-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0546c-177">Search-Flags</span></span>           | <span data-ttu-id="0546c-178">0x00000008</span><span class="sxs-lookup"><span data-stu-id="0546c-178">0x00000008</span></span>                      |
| <span data-ttu-id="0546c-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0546c-179">System-Flags</span></span>           | <span data-ttu-id="0546c-180">0x0000001b</span><span class="sxs-lookup"><span data-stu-id="0546c-180">0x0000001B</span></span>                      |
| <span data-ttu-id="0546c-181">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0546c-181">Classes used in</span></span>        | [<span data-ttu-id="0546c-182">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="0546c-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="0546c-183">Adam</span><span class="sxs-lookup"><span data-stu-id="0546c-183">ADAM</span></span>



| <span data-ttu-id="0546c-184">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0546c-184">Entry</span></span> | <span data-ttu-id="0546c-185">Wert</span><span class="sxs-lookup"><span data-stu-id="0546c-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0546c-186">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0546c-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0546c-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0546c-187">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0546c-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="0546c-188">System-Only</span></span>            | <span data-ttu-id="0546c-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="0546c-189">True</span></span>                            |
| <span data-ttu-id="0546c-190">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0546c-190">Is-Single-Valued</span></span>       | <span data-ttu-id="0546c-191">Richtig</span><span class="sxs-lookup"><span data-stu-id="0546c-191">True</span></span>                            |
| <span data-ttu-id="0546c-192">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0546c-192">Is Indexed</span></span>             | <span data-ttu-id="0546c-193">False</span><span class="sxs-lookup"><span data-stu-id="0546c-193">False</span></span>                           |
| <span data-ttu-id="0546c-194">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0546c-194">In Global Catalog</span></span>      | <span data-ttu-id="0546c-195">Richtig</span><span class="sxs-lookup"><span data-stu-id="0546c-195">True</span></span>                            |
| <span data-ttu-id="0546c-196">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0546c-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="0546c-197">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0546c-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0546c-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0546c-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0546c-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0546c-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0546c-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0546c-200">Search-Flags</span></span>           | <span data-ttu-id="0546c-201">0x00000008</span><span class="sxs-lookup"><span data-stu-id="0546c-201">0x00000008</span></span>                      |
| <span data-ttu-id="0546c-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0546c-202">System-Flags</span></span>           | <span data-ttu-id="0546c-203">0x0000001b</span><span class="sxs-lookup"><span data-stu-id="0546c-203">0x0000001B</span></span>                      |
| <span data-ttu-id="0546c-204">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0546c-204">Classes used in</span></span>        | [<span data-ttu-id="0546c-205">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="0546c-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0546c-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0546c-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0546c-207">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0546c-207">Entry</span></span> | <span data-ttu-id="0546c-208">Wert</span><span class="sxs-lookup"><span data-stu-id="0546c-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0546c-209">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0546c-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0546c-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0546c-210">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0546c-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="0546c-211">System-Only</span></span>            | <span data-ttu-id="0546c-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="0546c-212">True</span></span>                            |
| <span data-ttu-id="0546c-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0546c-213">Is-Single-Valued</span></span>       | <span data-ttu-id="0546c-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="0546c-214">True</span></span>                            |
| <span data-ttu-id="0546c-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0546c-215">Is Indexed</span></span>             | <span data-ttu-id="0546c-216">False</span><span class="sxs-lookup"><span data-stu-id="0546c-216">False</span></span>                           |
| <span data-ttu-id="0546c-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0546c-217">In Global Catalog</span></span>      | <span data-ttu-id="0546c-218">Richtig</span><span class="sxs-lookup"><span data-stu-id="0546c-218">True</span></span>                            |
| <span data-ttu-id="0546c-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0546c-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="0546c-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0546c-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0546c-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0546c-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0546c-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0546c-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0546c-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0546c-223">Search-Flags</span></span>           | <span data-ttu-id="0546c-224">0x00000008</span><span class="sxs-lookup"><span data-stu-id="0546c-224">0x00000008</span></span>                      |
| <span data-ttu-id="0546c-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0546c-225">System-Flags</span></span>           | <span data-ttu-id="0546c-226">0x0000001b</span><span class="sxs-lookup"><span data-stu-id="0546c-226">0x0000001B</span></span>                      |
| <span data-ttu-id="0546c-227">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0546c-227">Classes used in</span></span>        | [<span data-ttu-id="0546c-228">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="0546c-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0546c-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0546c-229">Windows Server 2008</span></span>



| <span data-ttu-id="0546c-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0546c-230">Entry</span></span> | <span data-ttu-id="0546c-231">Wert</span><span class="sxs-lookup"><span data-stu-id="0546c-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0546c-232">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0546c-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0546c-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0546c-233">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0546c-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="0546c-234">System-Only</span></span>            | <span data-ttu-id="0546c-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="0546c-235">True</span></span>                            |
| <span data-ttu-id="0546c-236">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0546c-236">Is-Single-Valued</span></span>       | <span data-ttu-id="0546c-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="0546c-237">True</span></span>                            |
| <span data-ttu-id="0546c-238">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0546c-238">Is Indexed</span></span>             | <span data-ttu-id="0546c-239">False</span><span class="sxs-lookup"><span data-stu-id="0546c-239">False</span></span>                           |
| <span data-ttu-id="0546c-240">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0546c-240">In Global Catalog</span></span>      | <span data-ttu-id="0546c-241">Richtig</span><span class="sxs-lookup"><span data-stu-id="0546c-241">True</span></span>                            |
| <span data-ttu-id="0546c-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0546c-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="0546c-243">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0546c-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0546c-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0546c-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0546c-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0546c-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0546c-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0546c-246">Search-Flags</span></span>           | <span data-ttu-id="0546c-247">0x00000008</span><span class="sxs-lookup"><span data-stu-id="0546c-247">0x00000008</span></span>                      |
| <span data-ttu-id="0546c-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0546c-248">System-Flags</span></span>           | <span data-ttu-id="0546c-249">0x0000001b</span><span class="sxs-lookup"><span data-stu-id="0546c-249">0x0000001B</span></span>                      |
| <span data-ttu-id="0546c-250">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0546c-250">Classes used in</span></span>        | [<span data-ttu-id="0546c-251">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="0546c-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0546c-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0546c-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0546c-253">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0546c-253">Entry</span></span> | <span data-ttu-id="0546c-254">Wert</span><span class="sxs-lookup"><span data-stu-id="0546c-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0546c-255">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0546c-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0546c-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0546c-256">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0546c-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="0546c-257">System-Only</span></span>            | <span data-ttu-id="0546c-258">Richtig</span><span class="sxs-lookup"><span data-stu-id="0546c-258">True</span></span>                            |
| <span data-ttu-id="0546c-259">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0546c-259">Is-Single-Valued</span></span>       | <span data-ttu-id="0546c-260">Richtig</span><span class="sxs-lookup"><span data-stu-id="0546c-260">True</span></span>                            |
| <span data-ttu-id="0546c-261">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0546c-261">Is Indexed</span></span>             | <span data-ttu-id="0546c-262">False</span><span class="sxs-lookup"><span data-stu-id="0546c-262">False</span></span>                           |
| <span data-ttu-id="0546c-263">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0546c-263">In Global Catalog</span></span>      | <span data-ttu-id="0546c-264">Richtig</span><span class="sxs-lookup"><span data-stu-id="0546c-264">True</span></span>                            |
| <span data-ttu-id="0546c-265">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0546c-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="0546c-266">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0546c-266">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0546c-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0546c-267">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0546c-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0546c-268">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0546c-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0546c-269">Search-Flags</span></span>           | <span data-ttu-id="0546c-270">0x00000008</span><span class="sxs-lookup"><span data-stu-id="0546c-270">0x00000008</span></span>                      |
| <span data-ttu-id="0546c-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0546c-271">System-Flags</span></span>           | <span data-ttu-id="0546c-272">0x0000001b</span><span class="sxs-lookup"><span data-stu-id="0546c-272">0x0000001B</span></span>                      |
| <span data-ttu-id="0546c-273">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0546c-273">Classes used in</span></span>        | [<span data-ttu-id="0546c-274">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="0546c-274">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0546c-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0546c-275">Windows Server 2012</span></span>



| <span data-ttu-id="0546c-276">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0546c-276">Entry</span></span> | <span data-ttu-id="0546c-277">Wert</span><span class="sxs-lookup"><span data-stu-id="0546c-277">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0546c-278">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0546c-278">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0546c-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0546c-279">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0546c-280">System-Only</span><span class="sxs-lookup"><span data-stu-id="0546c-280">System-Only</span></span>            | <span data-ttu-id="0546c-281">Richtig</span><span class="sxs-lookup"><span data-stu-id="0546c-281">True</span></span>                            |
| <span data-ttu-id="0546c-282">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0546c-282">Is-Single-Valued</span></span>       | <span data-ttu-id="0546c-283">Richtig</span><span class="sxs-lookup"><span data-stu-id="0546c-283">True</span></span>                            |
| <span data-ttu-id="0546c-284">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0546c-284">Is Indexed</span></span>             | <span data-ttu-id="0546c-285">False</span><span class="sxs-lookup"><span data-stu-id="0546c-285">False</span></span>                           |
| <span data-ttu-id="0546c-286">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0546c-286">In Global Catalog</span></span>      | <span data-ttu-id="0546c-287">Richtig</span><span class="sxs-lookup"><span data-stu-id="0546c-287">True</span></span>                            |
| <span data-ttu-id="0546c-288">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0546c-288">NT-Security-Descriptor</span></span> | <span data-ttu-id="0546c-289">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0546c-289">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0546c-290">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0546c-290">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0546c-291">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0546c-291">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0546c-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0546c-292">Search-Flags</span></span>           | <span data-ttu-id="0546c-293">0x00000008</span><span class="sxs-lookup"><span data-stu-id="0546c-293">0x00000008</span></span>                      |
| <span data-ttu-id="0546c-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0546c-294">System-Flags</span></span>           | <span data-ttu-id="0546c-295">0x0000001b</span><span class="sxs-lookup"><span data-stu-id="0546c-295">0x0000001B</span></span>                      |
| <span data-ttu-id="0546c-296">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0546c-296">Classes used in</span></span>        | [<span data-ttu-id="0546c-297">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="0546c-297">**Top**</span></span>](c-top.md)<br/> |



 

 





