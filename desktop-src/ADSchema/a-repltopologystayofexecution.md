---
title: REPL-Topology--Attribut für Ausführungsdauer
description: Die Verzögerung zwischen dem Löschen eines Server Objekts und dem permanenten Entfernen aus der Replikations Topologie.
ms.assetid: 770231b0-4886-41c2-a3b5-ac488ac09669
ms.tgt_platform: multiple
keywords:
- Adschema für repl-Topology-be-of-Execution-Attribut
- AD-Schema für repltopologystayosexecution-Attribut
topic_type:
- apiref
api_name:
- Repl-Topology-Stay-Of-Execution
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a51c74c477cce926dd18ea17b8df2b1adcf99df1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744553"
---
# <a name="repl-topology-stay-of-execution-attribute"></a><span data-ttu-id="14f90-105">REPL-Topology--Attribut für Ausführungsdauer</span><span class="sxs-lookup"><span data-stu-id="14f90-105">Repl-Topology-Stay-Of-Execution attribute</span></span>

<span data-ttu-id="14f90-106">Die Verzögerung zwischen dem Löschen eines Server Objekts und dem permanenten Entfernen aus der Replikations Topologie.</span><span class="sxs-lookup"><span data-stu-id="14f90-106">The delay between deleting a server object and it being permanently removed from the replication topology.</span></span>



| <span data-ttu-id="14f90-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="14f90-107">Entry</span></span> | <span data-ttu-id="14f90-108">Wert</span><span class="sxs-lookup"><span data-stu-id="14f90-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="14f90-109">CN</span><span class="sxs-lookup"><span data-stu-id="14f90-109">CN</span></span>                | <span data-ttu-id="14f90-110">REPL-Topologie-der Ausführungsdauer</span><span class="sxs-lookup"><span data-stu-id="14f90-110">Repl-Topology-Stay-Of-Execution</span></span>      |
| <span data-ttu-id="14f90-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="14f90-111">Ldap-Display-Name</span></span> | <span data-ttu-id="14f90-112">repltopologystayof Execution</span><span class="sxs-lookup"><span data-stu-id="14f90-112">replTopologyStayOfExecution</span></span>          |
| <span data-ttu-id="14f90-113">Size</span><span class="sxs-lookup"><span data-stu-id="14f90-113">Size</span></span>              | <span data-ttu-id="14f90-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="14f90-114">4 bytes</span></span>                              |
| <span data-ttu-id="14f90-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="14f90-115">Update Privilege</span></span>  | <span data-ttu-id="14f90-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="14f90-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="14f90-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="14f90-117">Update Frequency</span></span>  | <span data-ttu-id="14f90-118">Jedes Mal, wenn ein Server Objekt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="14f90-118">Whenever a server object is deleted.</span></span> |
| <span data-ttu-id="14f90-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="14f90-119">Attribute-Id</span></span>      | <span data-ttu-id="14f90-120">1.2.840.113556.1.4.677</span><span class="sxs-lookup"><span data-stu-id="14f90-120">1.2.840.113556.1.4.677</span></span>               |
| <span data-ttu-id="14f90-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="14f90-121">System-Id-Guid</span></span>    | <span data-ttu-id="14f90-122">7bf dcb83-4807-11d1-a9c3-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="14f90-122">7bfdcb83-4807-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="14f90-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="14f90-123">Syntax</span></span>            | [<span data-ttu-id="14f90-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="14f90-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="14f90-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="14f90-125">Implementations</span></span>

-   [<span data-ttu-id="14f90-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="14f90-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="14f90-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="14f90-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="14f90-128">**Adam**</span><span class="sxs-lookup"><span data-stu-id="14f90-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="14f90-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="14f90-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="14f90-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="14f90-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="14f90-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="14f90-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="14f90-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="14f90-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="14f90-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="14f90-133">Windows 2000 Server</span></span>



| <span data-ttu-id="14f90-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="14f90-134">Entry</span></span> | <span data-ttu-id="14f90-135">Wert</span><span class="sxs-lookup"><span data-stu-id="14f90-135">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="14f90-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="14f90-136">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="14f90-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14f90-137">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="14f90-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="14f90-138">System-Only</span></span>            | <span data-ttu-id="14f90-139">False</span><span class="sxs-lookup"><span data-stu-id="14f90-139">False</span></span>                                            |
| <span data-ttu-id="14f90-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="14f90-140">Is-Single-Valued</span></span>       | <span data-ttu-id="14f90-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="14f90-141">True</span></span>                                             |
| <span data-ttu-id="14f90-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="14f90-142">Is Indexed</span></span>             | <span data-ttu-id="14f90-143">False</span><span class="sxs-lookup"><span data-stu-id="14f90-143">False</span></span>                                            |
| <span data-ttu-id="14f90-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="14f90-144">In Global Catalog</span></span>      | <span data-ttu-id="14f90-145">False</span><span class="sxs-lookup"><span data-stu-id="14f90-145">False</span></span>                                            |
| <span data-ttu-id="14f90-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="14f90-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="14f90-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="14f90-147">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="14f90-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14f90-148">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="14f90-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14f90-149">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="14f90-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14f90-150">Search-Flags</span></span>           | <span data-ttu-id="14f90-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14f90-151">0x00000000</span></span>                                       |
| <span data-ttu-id="14f90-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14f90-152">System-Flags</span></span>           | <span data-ttu-id="14f90-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14f90-153">0x00000010</span></span>                                       |
| <span data-ttu-id="14f90-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="14f90-154">Classes used in</span></span>        | [<span data-ttu-id="14f90-155">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="14f90-155">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="14f90-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="14f90-156">Windows Server 2003</span></span>



| <span data-ttu-id="14f90-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="14f90-157">Entry</span></span> | <span data-ttu-id="14f90-158">Wert</span><span class="sxs-lookup"><span data-stu-id="14f90-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="14f90-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="14f90-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="14f90-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14f90-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="14f90-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="14f90-161">System-Only</span></span>            | <span data-ttu-id="14f90-162">False</span><span class="sxs-lookup"><span data-stu-id="14f90-162">False</span></span>                                            |
| <span data-ttu-id="14f90-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="14f90-163">Is-Single-Valued</span></span>       | <span data-ttu-id="14f90-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="14f90-164">True</span></span>                                             |
| <span data-ttu-id="14f90-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="14f90-165">Is Indexed</span></span>             | <span data-ttu-id="14f90-166">False</span><span class="sxs-lookup"><span data-stu-id="14f90-166">False</span></span>                                            |
| <span data-ttu-id="14f90-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="14f90-167">In Global Catalog</span></span>      | <span data-ttu-id="14f90-168">False</span><span class="sxs-lookup"><span data-stu-id="14f90-168">False</span></span>                                            |
| <span data-ttu-id="14f90-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="14f90-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="14f90-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="14f90-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="14f90-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14f90-171">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="14f90-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14f90-172">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="14f90-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14f90-173">Search-Flags</span></span>           | <span data-ttu-id="14f90-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14f90-174">0x00000000</span></span>                                       |
| <span data-ttu-id="14f90-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14f90-175">System-Flags</span></span>           | <span data-ttu-id="14f90-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14f90-176">0x00000010</span></span>                                       |
| <span data-ttu-id="14f90-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="14f90-177">Classes used in</span></span>        | [<span data-ttu-id="14f90-178">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="14f90-178">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="14f90-179">Adam</span><span class="sxs-lookup"><span data-stu-id="14f90-179">ADAM</span></span>



| <span data-ttu-id="14f90-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="14f90-180">Entry</span></span> | <span data-ttu-id="14f90-181">Wert</span><span class="sxs-lookup"><span data-stu-id="14f90-181">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="14f90-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="14f90-182">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="14f90-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14f90-183">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="14f90-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="14f90-184">System-Only</span></span>            | <span data-ttu-id="14f90-185">False</span><span class="sxs-lookup"><span data-stu-id="14f90-185">False</span></span>                                            |
| <span data-ttu-id="14f90-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="14f90-186">Is-Single-Valued</span></span>       | <span data-ttu-id="14f90-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="14f90-187">True</span></span>                                             |
| <span data-ttu-id="14f90-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="14f90-188">Is Indexed</span></span>             | <span data-ttu-id="14f90-189">False</span><span class="sxs-lookup"><span data-stu-id="14f90-189">False</span></span>                                            |
| <span data-ttu-id="14f90-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="14f90-190">In Global Catalog</span></span>      | <span data-ttu-id="14f90-191">False</span><span class="sxs-lookup"><span data-stu-id="14f90-191">False</span></span>                                            |
| <span data-ttu-id="14f90-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="14f90-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="14f90-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="14f90-193">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="14f90-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14f90-194">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="14f90-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14f90-195">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="14f90-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14f90-196">Search-Flags</span></span>           | <span data-ttu-id="14f90-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14f90-197">0x00000000</span></span>                                       |
| <span data-ttu-id="14f90-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14f90-198">System-Flags</span></span>           | <span data-ttu-id="14f90-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14f90-199">0x00000010</span></span>                                       |
| <span data-ttu-id="14f90-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="14f90-200">Classes used in</span></span>        | [<span data-ttu-id="14f90-201">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="14f90-201">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="14f90-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="14f90-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="14f90-203">Eingabe</span><span class="sxs-lookup"><span data-stu-id="14f90-203">Entry</span></span> | <span data-ttu-id="14f90-204">Wert</span><span class="sxs-lookup"><span data-stu-id="14f90-204">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="14f90-205">Link-ID</span><span class="sxs-lookup"><span data-stu-id="14f90-205">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="14f90-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14f90-206">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="14f90-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="14f90-207">System-Only</span></span>            | <span data-ttu-id="14f90-208">False</span><span class="sxs-lookup"><span data-stu-id="14f90-208">False</span></span>                                            |
| <span data-ttu-id="14f90-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="14f90-209">Is-Single-Valued</span></span>       | <span data-ttu-id="14f90-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="14f90-210">True</span></span>                                             |
| <span data-ttu-id="14f90-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="14f90-211">Is Indexed</span></span>             | <span data-ttu-id="14f90-212">False</span><span class="sxs-lookup"><span data-stu-id="14f90-212">False</span></span>                                            |
| <span data-ttu-id="14f90-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="14f90-213">In Global Catalog</span></span>      | <span data-ttu-id="14f90-214">False</span><span class="sxs-lookup"><span data-stu-id="14f90-214">False</span></span>                                            |
| <span data-ttu-id="14f90-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="14f90-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="14f90-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="14f90-216">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="14f90-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14f90-217">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="14f90-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14f90-218">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="14f90-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14f90-219">Search-Flags</span></span>           | <span data-ttu-id="14f90-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14f90-220">0x00000000</span></span>                                       |
| <span data-ttu-id="14f90-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14f90-221">System-Flags</span></span>           | <span data-ttu-id="14f90-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14f90-222">0x00000010</span></span>                                       |
| <span data-ttu-id="14f90-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="14f90-223">Classes used in</span></span>        | [<span data-ttu-id="14f90-224">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="14f90-224">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="14f90-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14f90-225">Windows Server 2008</span></span>



| <span data-ttu-id="14f90-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="14f90-226">Entry</span></span> | <span data-ttu-id="14f90-227">Wert</span><span class="sxs-lookup"><span data-stu-id="14f90-227">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="14f90-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="14f90-228">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="14f90-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14f90-229">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="14f90-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="14f90-230">System-Only</span></span>            | <span data-ttu-id="14f90-231">False</span><span class="sxs-lookup"><span data-stu-id="14f90-231">False</span></span>                                            |
| <span data-ttu-id="14f90-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="14f90-232">Is-Single-Valued</span></span>       | <span data-ttu-id="14f90-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="14f90-233">True</span></span>                                             |
| <span data-ttu-id="14f90-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="14f90-234">Is Indexed</span></span>             | <span data-ttu-id="14f90-235">False</span><span class="sxs-lookup"><span data-stu-id="14f90-235">False</span></span>                                            |
| <span data-ttu-id="14f90-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="14f90-236">In Global Catalog</span></span>      | <span data-ttu-id="14f90-237">False</span><span class="sxs-lookup"><span data-stu-id="14f90-237">False</span></span>                                            |
| <span data-ttu-id="14f90-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="14f90-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="14f90-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="14f90-239">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="14f90-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14f90-240">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="14f90-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14f90-241">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="14f90-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14f90-242">Search-Flags</span></span>           | <span data-ttu-id="14f90-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14f90-243">0x00000000</span></span>                                       |
| <span data-ttu-id="14f90-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14f90-244">System-Flags</span></span>           | <span data-ttu-id="14f90-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14f90-245">0x00000010</span></span>                                       |
| <span data-ttu-id="14f90-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="14f90-246">Classes used in</span></span>        | [<span data-ttu-id="14f90-247">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="14f90-247">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="14f90-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="14f90-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="14f90-249">Eingabe</span><span class="sxs-lookup"><span data-stu-id="14f90-249">Entry</span></span> | <span data-ttu-id="14f90-250">Wert</span><span class="sxs-lookup"><span data-stu-id="14f90-250">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="14f90-251">Link-ID</span><span class="sxs-lookup"><span data-stu-id="14f90-251">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="14f90-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14f90-252">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="14f90-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="14f90-253">System-Only</span></span>            | <span data-ttu-id="14f90-254">False</span><span class="sxs-lookup"><span data-stu-id="14f90-254">False</span></span>                                            |
| <span data-ttu-id="14f90-255">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="14f90-255">Is-Single-Valued</span></span>       | <span data-ttu-id="14f90-256">Richtig</span><span class="sxs-lookup"><span data-stu-id="14f90-256">True</span></span>                                             |
| <span data-ttu-id="14f90-257">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="14f90-257">Is Indexed</span></span>             | <span data-ttu-id="14f90-258">False</span><span class="sxs-lookup"><span data-stu-id="14f90-258">False</span></span>                                            |
| <span data-ttu-id="14f90-259">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="14f90-259">In Global Catalog</span></span>      | <span data-ttu-id="14f90-260">False</span><span class="sxs-lookup"><span data-stu-id="14f90-260">False</span></span>                                            |
| <span data-ttu-id="14f90-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="14f90-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="14f90-262">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="14f90-262">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="14f90-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14f90-263">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="14f90-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14f90-264">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="14f90-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14f90-265">Search-Flags</span></span>           | <span data-ttu-id="14f90-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14f90-266">0x00000000</span></span>                                       |
| <span data-ttu-id="14f90-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14f90-267">System-Flags</span></span>           | <span data-ttu-id="14f90-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14f90-268">0x00000010</span></span>                                       |
| <span data-ttu-id="14f90-269">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="14f90-269">Classes used in</span></span>        | [<span data-ttu-id="14f90-270">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="14f90-270">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="14f90-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="14f90-271">Windows Server 2012</span></span>



| <span data-ttu-id="14f90-272">Eingabe</span><span class="sxs-lookup"><span data-stu-id="14f90-272">Entry</span></span> | <span data-ttu-id="14f90-273">Wert</span><span class="sxs-lookup"><span data-stu-id="14f90-273">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="14f90-274">Link-ID</span><span class="sxs-lookup"><span data-stu-id="14f90-274">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="14f90-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14f90-275">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="14f90-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="14f90-276">System-Only</span></span>            | <span data-ttu-id="14f90-277">False</span><span class="sxs-lookup"><span data-stu-id="14f90-277">False</span></span>                                            |
| <span data-ttu-id="14f90-278">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="14f90-278">Is-Single-Valued</span></span>       | <span data-ttu-id="14f90-279">Richtig</span><span class="sxs-lookup"><span data-stu-id="14f90-279">True</span></span>                                             |
| <span data-ttu-id="14f90-280">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="14f90-280">Is Indexed</span></span>             | <span data-ttu-id="14f90-281">False</span><span class="sxs-lookup"><span data-stu-id="14f90-281">False</span></span>                                            |
| <span data-ttu-id="14f90-282">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="14f90-282">In Global Catalog</span></span>      | <span data-ttu-id="14f90-283">False</span><span class="sxs-lookup"><span data-stu-id="14f90-283">False</span></span>                                            |
| <span data-ttu-id="14f90-284">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="14f90-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="14f90-285">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="14f90-285">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="14f90-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14f90-286">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="14f90-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14f90-287">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="14f90-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14f90-288">Search-Flags</span></span>           | <span data-ttu-id="14f90-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14f90-289">0x00000000</span></span>                                       |
| <span data-ttu-id="14f90-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14f90-290">System-Flags</span></span>           | <span data-ttu-id="14f90-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14f90-291">0x00000010</span></span>                                       |
| <span data-ttu-id="14f90-292">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="14f90-292">Classes used in</span></span>        | [<span data-ttu-id="14f90-293">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="14f90-293">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





