---
title: REPL-upydate-Vector-Attribut
description: Verfolgt interne Replikations Zustandsinformationen für einen gesamten NC. Informationen können hier über die API dsreplicagetinfo () im öffentlichen Format extrahiert werden. In allen NC-Stamm Objekten vorhanden.
ms.assetid: f23d94f8-c31b-447f-98c3-c35a4f5f1d43
ms.tgt_platform: multiple
keywords:
- REPL-upydate-Vector-Attribut AD-Schema
- replupydatevector-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Repl-UpToDate-Vector
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9263111459d01d99cf5990d1c818b5ff2a7a19be
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346793"
---
# <a name="repl-uptodate-vector-attribute"></a><span data-ttu-id="a0836-107">REPL-upydate-Vector-Attribut</span><span class="sxs-lookup"><span data-stu-id="a0836-107">Repl-UpToDate-Vector attribute</span></span>

<span data-ttu-id="a0836-108">Verfolgt interne Replikations Zustandsinformationen für einen gesamten NC.</span><span class="sxs-lookup"><span data-stu-id="a0836-108">Tracks internal replication state information for an entire NC.</span></span> <span data-ttu-id="a0836-109">Informationen können hier über die API dsreplicagetinfo () im öffentlichen Format extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0836-109">Information here can be extracted in public form through the API DsReplicaGetInfo().</span></span> <span data-ttu-id="a0836-110">In allen NC-Stamm Objekten vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a0836-110">Present on all NC root objects.</span></span>



| <span data-ttu-id="a0836-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a0836-111">Entry</span></span> | <span data-ttu-id="a0836-112">Wert</span><span class="sxs-lookup"><span data-stu-id="a0836-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="a0836-113">CN</span><span class="sxs-lookup"><span data-stu-id="a0836-113">CN</span></span>                | <span data-ttu-id="a0836-114">REPL-Update-Vector</span><span class="sxs-lookup"><span data-stu-id="a0836-114">Repl-UpToDate-Vector</span></span>                                                           |
| <span data-ttu-id="a0836-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a0836-115">Ldap-Display-Name</span></span> | <span data-ttu-id="a0836-116">befindet</span><span class="sxs-lookup"><span data-stu-id="a0836-116">replUpToDateVector</span></span>                                                             |
| <span data-ttu-id="a0836-117">Size</span><span class="sxs-lookup"><span data-stu-id="a0836-117">Size</span></span>              | <span data-ttu-id="a0836-118">Die Länge ist proportional zur Anzahl der Replikate ("Past" und "Present") des NC.</span><span class="sxs-lookup"><span data-stu-id="a0836-118">Length is proportional to the number of replicas (past and present) of the NC.</span></span> |
| <span data-ttu-id="a0836-119">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="a0836-119">Update Privilege</span></span>  | <span data-ttu-id="a0836-120">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a0836-120">This value is set by the system.</span></span>                                               |
| <span data-ttu-id="a0836-121">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="a0836-121">Update Frequency</span></span>  | <span data-ttu-id="a0836-122">Änderungen in Reaktion auf abgeschlossene eingehende Replikations Zyklen.</span><span class="sxs-lookup"><span data-stu-id="a0836-122">Changes in response to completed inbound replication cycles.</span></span>                   |
| <span data-ttu-id="a0836-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a0836-123">Attribute-Id</span></span>      | <span data-ttu-id="a0836-124">1.2.840.113556.1.4.4</span><span class="sxs-lookup"><span data-stu-id="a0836-124">1.2.840.113556.1.4.4</span></span>                                                           |
| <span data-ttu-id="a0836-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a0836-125">System-Id-Guid</span></span>    | <span data-ttu-id="a0836-126">bf967a16-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a0836-126">bf967a16-0de6-11d0-a285-00aa003049e2</span></span>                                           |
| <span data-ttu-id="a0836-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0836-127">Syntax</span></span>            | [<span data-ttu-id="a0836-128">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="a0836-128">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                          |



## <a name="implementations"></a><span data-ttu-id="a0836-129">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="a0836-129">Implementations</span></span>

-   [<span data-ttu-id="a0836-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a0836-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a0836-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a0836-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a0836-132">**Adam**</span><span class="sxs-lookup"><span data-stu-id="a0836-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a0836-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a0836-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a0836-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a0836-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a0836-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a0836-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a0836-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a0836-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a0836-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a0836-137">Windows 2000 Server</span></span>



| <span data-ttu-id="a0836-138">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a0836-138">Entry</span></span> | <span data-ttu-id="a0836-139">Wert</span><span class="sxs-lookup"><span data-stu-id="a0836-139">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a0836-140">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a0836-140">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a0836-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0836-141">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a0836-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0836-142">System-Only</span></span>            | <span data-ttu-id="a0836-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="a0836-143">True</span></span>                            |
| <span data-ttu-id="a0836-144">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a0836-144">Is-Single-Valued</span></span>       | <span data-ttu-id="a0836-145">Richtig</span><span class="sxs-lookup"><span data-stu-id="a0836-145">True</span></span>                            |
| <span data-ttu-id="a0836-146">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a0836-146">Is Indexed</span></span>             | <span data-ttu-id="a0836-147">False</span><span class="sxs-lookup"><span data-stu-id="a0836-147">False</span></span>                           |
| <span data-ttu-id="a0836-148">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a0836-148">In Global Catalog</span></span>      | <span data-ttu-id="a0836-149">Richtig</span><span class="sxs-lookup"><span data-stu-id="a0836-149">True</span></span>                            |
| <span data-ttu-id="a0836-150">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a0836-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0836-151">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a0836-151">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a0836-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0836-152">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a0836-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0836-153">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a0836-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0836-154">Search-Flags</span></span>           | <span data-ttu-id="a0836-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0836-155">0x00000000</span></span>                      |
| <span data-ttu-id="a0836-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0836-156">System-Flags</span></span>           | <span data-ttu-id="a0836-157">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a0836-157">0x00000013</span></span>                      |
| <span data-ttu-id="a0836-158">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a0836-158">Classes used in</span></span>        | [<span data-ttu-id="a0836-159">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a0836-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a0836-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a0836-160">Windows Server 2003</span></span>



| <span data-ttu-id="a0836-161">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a0836-161">Entry</span></span> | <span data-ttu-id="a0836-162">Wert</span><span class="sxs-lookup"><span data-stu-id="a0836-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a0836-163">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a0836-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a0836-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0836-164">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a0836-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0836-165">System-Only</span></span>            | <span data-ttu-id="a0836-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="a0836-166">True</span></span>                            |
| <span data-ttu-id="a0836-167">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a0836-167">Is-Single-Valued</span></span>       | <span data-ttu-id="a0836-168">Richtig</span><span class="sxs-lookup"><span data-stu-id="a0836-168">True</span></span>                            |
| <span data-ttu-id="a0836-169">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a0836-169">Is Indexed</span></span>             | <span data-ttu-id="a0836-170">False</span><span class="sxs-lookup"><span data-stu-id="a0836-170">False</span></span>                           |
| <span data-ttu-id="a0836-171">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a0836-171">In Global Catalog</span></span>      | <span data-ttu-id="a0836-172">Richtig</span><span class="sxs-lookup"><span data-stu-id="a0836-172">True</span></span>                            |
| <span data-ttu-id="a0836-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a0836-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0836-174">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a0836-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a0836-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0836-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a0836-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0836-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a0836-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0836-177">Search-Flags</span></span>           | <span data-ttu-id="a0836-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0836-178">0x00000000</span></span>                      |
| <span data-ttu-id="a0836-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0836-179">System-Flags</span></span>           | <span data-ttu-id="a0836-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a0836-180">0x00000013</span></span>                      |
| <span data-ttu-id="a0836-181">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a0836-181">Classes used in</span></span>        | [<span data-ttu-id="a0836-182">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a0836-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a0836-183">Adam</span><span class="sxs-lookup"><span data-stu-id="a0836-183">ADAM</span></span>



| <span data-ttu-id="a0836-184">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a0836-184">Entry</span></span> | <span data-ttu-id="a0836-185">Wert</span><span class="sxs-lookup"><span data-stu-id="a0836-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a0836-186">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a0836-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a0836-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0836-187">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a0836-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0836-188">System-Only</span></span>            | <span data-ttu-id="a0836-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="a0836-189">True</span></span>                            |
| <span data-ttu-id="a0836-190">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a0836-190">Is-Single-Valued</span></span>       | <span data-ttu-id="a0836-191">Richtig</span><span class="sxs-lookup"><span data-stu-id="a0836-191">True</span></span>                            |
| <span data-ttu-id="a0836-192">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a0836-192">Is Indexed</span></span>             | <span data-ttu-id="a0836-193">False</span><span class="sxs-lookup"><span data-stu-id="a0836-193">False</span></span>                           |
| <span data-ttu-id="a0836-194">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a0836-194">In Global Catalog</span></span>      | <span data-ttu-id="a0836-195">Richtig</span><span class="sxs-lookup"><span data-stu-id="a0836-195">True</span></span>                            |
| <span data-ttu-id="a0836-196">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a0836-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0836-197">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a0836-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a0836-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0836-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a0836-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0836-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a0836-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0836-200">Search-Flags</span></span>           | <span data-ttu-id="a0836-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0836-201">0x00000000</span></span>                      |
| <span data-ttu-id="a0836-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0836-202">System-Flags</span></span>           | <span data-ttu-id="a0836-203">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a0836-203">0x00000013</span></span>                      |
| <span data-ttu-id="a0836-204">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a0836-204">Classes used in</span></span>        | [<span data-ttu-id="a0836-205">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a0836-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a0836-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a0836-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a0836-207">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a0836-207">Entry</span></span> | <span data-ttu-id="a0836-208">Wert</span><span class="sxs-lookup"><span data-stu-id="a0836-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a0836-209">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a0836-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a0836-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0836-210">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a0836-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0836-211">System-Only</span></span>            | <span data-ttu-id="a0836-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="a0836-212">True</span></span>                            |
| <span data-ttu-id="a0836-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a0836-213">Is-Single-Valued</span></span>       | <span data-ttu-id="a0836-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="a0836-214">True</span></span>                            |
| <span data-ttu-id="a0836-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a0836-215">Is Indexed</span></span>             | <span data-ttu-id="a0836-216">False</span><span class="sxs-lookup"><span data-stu-id="a0836-216">False</span></span>                           |
| <span data-ttu-id="a0836-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a0836-217">In Global Catalog</span></span>      | <span data-ttu-id="a0836-218">Richtig</span><span class="sxs-lookup"><span data-stu-id="a0836-218">True</span></span>                            |
| <span data-ttu-id="a0836-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a0836-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0836-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a0836-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a0836-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0836-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a0836-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0836-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a0836-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0836-223">Search-Flags</span></span>           | <span data-ttu-id="a0836-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0836-224">0x00000000</span></span>                      |
| <span data-ttu-id="a0836-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0836-225">System-Flags</span></span>           | <span data-ttu-id="a0836-226">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a0836-226">0x00000013</span></span>                      |
| <span data-ttu-id="a0836-227">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a0836-227">Classes used in</span></span>        | [<span data-ttu-id="a0836-228">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a0836-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a0836-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0836-229">Windows Server 2008</span></span>



| <span data-ttu-id="a0836-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a0836-230">Entry</span></span> | <span data-ttu-id="a0836-231">Wert</span><span class="sxs-lookup"><span data-stu-id="a0836-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a0836-232">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a0836-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a0836-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0836-233">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a0836-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0836-234">System-Only</span></span>            | <span data-ttu-id="a0836-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="a0836-235">True</span></span>                            |
| <span data-ttu-id="a0836-236">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a0836-236">Is-Single-Valued</span></span>       | <span data-ttu-id="a0836-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="a0836-237">True</span></span>                            |
| <span data-ttu-id="a0836-238">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a0836-238">Is Indexed</span></span>             | <span data-ttu-id="a0836-239">False</span><span class="sxs-lookup"><span data-stu-id="a0836-239">False</span></span>                           |
| <span data-ttu-id="a0836-240">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a0836-240">In Global Catalog</span></span>      | <span data-ttu-id="a0836-241">Richtig</span><span class="sxs-lookup"><span data-stu-id="a0836-241">True</span></span>                            |
| <span data-ttu-id="a0836-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a0836-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0836-243">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a0836-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a0836-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0836-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a0836-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0836-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a0836-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0836-246">Search-Flags</span></span>           | <span data-ttu-id="a0836-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0836-247">0x00000000</span></span>                      |
| <span data-ttu-id="a0836-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0836-248">System-Flags</span></span>           | <span data-ttu-id="a0836-249">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a0836-249">0x00000013</span></span>                      |
| <span data-ttu-id="a0836-250">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a0836-250">Classes used in</span></span>        | [<span data-ttu-id="a0836-251">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a0836-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a0836-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a0836-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a0836-253">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a0836-253">Entry</span></span> | <span data-ttu-id="a0836-254">Wert</span><span class="sxs-lookup"><span data-stu-id="a0836-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a0836-255">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a0836-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a0836-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0836-256">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a0836-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0836-257">System-Only</span></span>            | <span data-ttu-id="a0836-258">Richtig</span><span class="sxs-lookup"><span data-stu-id="a0836-258">True</span></span>                            |
| <span data-ttu-id="a0836-259">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a0836-259">Is-Single-Valued</span></span>       | <span data-ttu-id="a0836-260">Richtig</span><span class="sxs-lookup"><span data-stu-id="a0836-260">True</span></span>                            |
| <span data-ttu-id="a0836-261">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a0836-261">Is Indexed</span></span>             | <span data-ttu-id="a0836-262">False</span><span class="sxs-lookup"><span data-stu-id="a0836-262">False</span></span>                           |
| <span data-ttu-id="a0836-263">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a0836-263">In Global Catalog</span></span>      | <span data-ttu-id="a0836-264">Richtig</span><span class="sxs-lookup"><span data-stu-id="a0836-264">True</span></span>                            |
| <span data-ttu-id="a0836-265">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a0836-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0836-266">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a0836-266">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a0836-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0836-267">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a0836-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0836-268">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a0836-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0836-269">Search-Flags</span></span>           | <span data-ttu-id="a0836-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0836-270">0x00000000</span></span>                      |
| <span data-ttu-id="a0836-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0836-271">System-Flags</span></span>           | <span data-ttu-id="a0836-272">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a0836-272">0x00000013</span></span>                      |
| <span data-ttu-id="a0836-273">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a0836-273">Classes used in</span></span>        | [<span data-ttu-id="a0836-274">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a0836-274">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a0836-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a0836-275">Windows Server 2012</span></span>



| <span data-ttu-id="a0836-276">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a0836-276">Entry</span></span> | <span data-ttu-id="a0836-277">Wert</span><span class="sxs-lookup"><span data-stu-id="a0836-277">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a0836-278">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a0836-278">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a0836-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0836-279">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a0836-280">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0836-280">System-Only</span></span>            | <span data-ttu-id="a0836-281">Richtig</span><span class="sxs-lookup"><span data-stu-id="a0836-281">True</span></span>                            |
| <span data-ttu-id="a0836-282">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a0836-282">Is-Single-Valued</span></span>       | <span data-ttu-id="a0836-283">Richtig</span><span class="sxs-lookup"><span data-stu-id="a0836-283">True</span></span>                            |
| <span data-ttu-id="a0836-284">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a0836-284">Is Indexed</span></span>             | <span data-ttu-id="a0836-285">False</span><span class="sxs-lookup"><span data-stu-id="a0836-285">False</span></span>                           |
| <span data-ttu-id="a0836-286">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a0836-286">In Global Catalog</span></span>      | <span data-ttu-id="a0836-287">Richtig</span><span class="sxs-lookup"><span data-stu-id="a0836-287">True</span></span>                            |
| <span data-ttu-id="a0836-288">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a0836-288">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0836-289">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a0836-289">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a0836-290">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0836-290">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a0836-291">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0836-291">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a0836-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0836-292">Search-Flags</span></span>           | <span data-ttu-id="a0836-293">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0836-293">0x00000000</span></span>                      |
| <span data-ttu-id="a0836-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0836-294">System-Flags</span></span>           | <span data-ttu-id="a0836-295">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a0836-295">0x00000013</span></span>                      |
| <span data-ttu-id="a0836-296">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a0836-296">Classes used in</span></span>        | [<span data-ttu-id="a0836-297">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a0836-297">**Top**</span></span>](c-top.md)<br/> |



 

 





